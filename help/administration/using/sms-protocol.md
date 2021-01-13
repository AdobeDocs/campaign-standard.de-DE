---
solution: Campaign Standard
product: campaign
title: Protokoll und Einstellungen für den SMS-Anschluss
description: Erfahren Sie mehr über den SMS-Connector und dessen Konfiguration.
audience: administration
content-type: reference
topic-tags: configuring-channels
translation-type: tm+mt
source-git-commit: 458517259c6668e08a25f8c3cd3f193f27e536fb
workflow-type: tm+mt
source-wordcount: '8382'
ht-degree: 1%

---


# SMS-Anschluss-Protokoll und -Einstellungen {#sms-connector-protocol}

>[!NOTE]
>
>Das **SMS-Connector-Protokoll und die Einstellungen** für Adobe Campaign Classic finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/sending-messages-on-mobiles/sms-protocol.htmln#sending-messages).
>
>In diesem Dokument beziehen sich alle Verweise auf Protokolldetails, Feldnamen und -werte auf die Spezifikation [SMPP 3.4](https://smpp.org/SMPP_v3_4_Issue1_2.pdf).

## Übersicht {#overview}

SMS kann auf das Versenden von Kurztexten ohne Formatierung beschränkt sein, aber seine Einfachheit macht es zu einem wertvollen Kommunikations-Kanal.

Es gibt zwei Möglichkeiten, eine SMS zu senden:

* Schicken Sie es manuell von einem Telefon, die übliche Art, direkt zwischen Menschen zu kommunizieren.

* Schicken Sie es aus dem Internet, wie Adobe Campaign Nachrichten sendet. Dazu benötigen Sie einen SMS-Dienstleister, der das Internet mit dem Mobilfunknetz verbindet.
Adobe Campaign verwendet das SMPP-Protokoll, um SMS an einen Dienstleister zu senden.

Dieses Dokument führt Sie durch die Verbindung zwischen Adobe Campaign und einem SMPP-Anbieter.

SMPP-Anbieter können manchmal von der offiziellen Spezifikation abweichen, aber der SMS-Stecker in Adobe Campaign bietet viele Möglichkeiten, sein Verhalten anzupassen, damit es mit den meisten Anbietern kompatibel ist.

>[!IMPORTANT]
>
>Die Einrichtung einer Verbindung zu einem neuen Anbieter erfordert möglicherweise einige technische Fähigkeiten, Kenntnisse über TCP, binäre, hexadezimale Darstellung und Textkodierungen. Es erfordert auch eine aktive Zusammenarbeit mit dem Anbieter.

### SMS-Typen {#sms-types}

Beim Versenden von SMS über einen SMS-Anbieter werden Sie mit drei verschiedenen Arten von SMS konfrontiert:

* **SMS MT (Mobilgerät beendet)**: eine SMS, die von Adobe Campaign über den SMPP-Anbieter an Mobiltelefone gesendet wird.

* **SMS MO (Mobilgeräte)**: eine SMS, die von einem Mobilgerät über den SMPP-Anbieter an Adobe Campaign gesendet wird.

* **SMS SR (Statusbericht) oder DR oder DLR (Versand-Empfangsbestätigung)**: eine vom Mobilgerät über den SMPP-Anbieter an Adobe Campaign gesendete Rückbestätigung, die angibt, dass die SMS erfolgreich empfangen wurde. Adobe Campaign erhält möglicherweise auch SR, der angibt, dass die Nachricht nicht zugestellt werden konnte, oft mit einer Fehlerbeschreibung.

Sie müssen zwischen den Bestätigungen (RESP PDU, Teil des SMPP-Protokolls) und SR unterscheiden: SR ist eine Art SMS, die über das Netzwerk von Ende zu Ende gesendet wird, während eine Bestätigung nur eine Bestätigung ist, dass eine Übertragung erfolgreich war.

Sowohl Bestätigungen als auch SR können Trigger verursachen, wobei die Unterscheidung zwischen den beiden hilft, die Fehlerbehebung durchzuführen.

### Informationen, die von einer SMS gesendet werden{#information-sms}

Eine SMS enthält mehr Informationen als Text. Hier eine Liste dessen, was Sie in einer SMS erwarten können:

* Der Text, der auf 140 Byte begrenzt ist, d. h. je nach Kodierung zwischen 70 und 160 Zeichen. Details und Einschränkungen finden Sie unter [SMS-Textkodierung](../../administration/using/sms-protocol.md#sms-text-encoding) weiter unten.

* Eine Empfänger-Adresse, manchmal auch `ADC` oder `MSISDN` genannt. Das ist die Nummer des Mobiltelefons, das die SMS erhält.

* Eine Absenderadresse, die als `oADC` oder manchmal `sender id` bezeichnet werden kann. Dabei kann es sich um eine Telefonnummer im täglichen Gebrauch handeln, um einen Kurzcode, wenn dieser über einen Anbieter gesendet wird, oder um einen Namen. Name ist eine optionale Funktion, in diesem Fall können Sie nicht auf die SMS antworten.

* Eine Flag, die angibt, ob es sich bei der Nachricht um eine Flash-Nachricht handelt. Eine Flash-Nachricht ist ein Popup, das nicht im Speicher gespeichert wird.

* Eine Flag, die angibt, ob ein SR erwartet wird oder nicht.

* Ein Gültigkeitsdatum, nach dem keine Netzwerkgeräte erneut versuchen dürfen.

* Ein `data_coding`-Feld, das die Kodierung des Textes angibt.

## SMPP-Protokoll {#smpp-protocol}

Adobe Campaign Standard unterstützt das SMPP-Protokoll Version 3.4. Dies ist ein weit verbreitetes Protokoll, das es erlaubt, SMS an einen Anbieter (SMSC) zu senden und SMS sowie Quittungen zu empfangen. Weitere Informationen finden Sie in der [SMPP-Dokumentation](https://smpp.org/SMPP_v3_4_Issue1_2.pdf).

Die Netzwerkausrüstung auf der SMS-Dienstleister-Seite wird oft als SMSC bezeichnet.

### SMPP-Verbindungen {#smpp-connections}

Adobe Campaign verbindet sich über TCP mit der Netzwerkausrüstung des SMS-Dienstleisters. Das SMPP-Protokoll stellt permanente TCP-Verbindungen vom Adobe Campaign zum Provider ein. TCP-Verbindungen werden immer von Adobe Campaign initiiert, auch um Nachrichten zu empfangen.
SMPP öffnet je nach Modus 1 oder 2 TCP-Verbindungen. Alle Verbindungen werden immer von Adobe Campaign initiiert.

Das SMPP-Protokoll kann in zwei Modi verwendet werden:

* **Transmitter+Receiver (oder TX+RX)**: zwei separate TCP-Verbindungen werden zum Senden und Empfangen von Nachrichten verwendet.
* **Transceiver (abor TRX)**: eine einzige TCP-Verbindung wird zum Senden und Empfangen von Nachrichten verwendet.

>[!NOTE]
>
>TRX wird für Adobe Campaign Standard bevorzugt, da es die Anzahl der Verbindungen verringert und die Wiederherstellung der Verbindung im Falle eines Ausfalls vereinfacht.

### SMPP PDU {#smpp-pdu}

SMPP-Übertragungseinheiten (&quot;Pakete&quot;) werden PDUs genannt. Eine **PDU** enthält einen Befehl, einen Status, eine Sequenznummer und Daten.

Jede PDU muss durch eine `SMPP RESP PDU` (synchrone Antwort) bestätigt werden. Anfragen können in Vorbereitung sein: der Absender kann viele Befehle senden, ohne auf `RESP` zu warten, wird die Anzahl der Anfragen, die zu jeder Zeit gesendet werden kann, das Fenster genannt. `RESP PDU` kann in jeder Reihenfolge eintreffen, unabhängig von der Reihenfolge der entsprechenden Initiator-PDU.

Im getrennten Modus **Transmitter+Receiver** hängt die verwendete Verbindung von der Art der gesendeten Nachricht ab. Die Transmitterverbindung wird für MT verwendet, und die Receiver-Verbindung wird für MO und SR verwendet. Anfragen und Antworten für jede Art von Nachricht werden über dieselbe TCP-Verbindung gesendet.

Wenn beispielsweise ein MT gesendet wird, wird die Senderverbindung verwendet und das `RESP`, das den MT bestätigt, wird auch über den Transmitter-Kanal gesendet. Wenn Sie ein MO (oder ein SR) erhalten, wird die Receiver-Verbindung verwendet, um das MO zu empfangen und das `RESP` zu senden, das das MO bestätigt.

![](assets/do-not-localize/sms_protocol_1.png)

In Adobe Campaign Standard ist die MT- und SR-Aussöhnung nativ zum MTA, sodass es keinen eigenen SMS-Prozess gibt.

Bei einem erfolgreichen `SUBMIT_SM_RESP PDU` wird der Status der &quot;gesendeten&quot;Nachricht im Sendetlog Trigger, während bei einem erfolgreichen `DELIVER_SM (SR) PDU` der Status der &quot;empfangenen&quot;Nachricht Trigger wird.

### Sicherheitsaspekte {#security-aspects}

Das Protokoll selbst ist nicht verschlüsselt. Die meisten Anbieter implementieren eine Variante der IP-Adresse auf der Zulassungsliste, sodass die IP-Adressen der Adobe Campaign-Server dem Provider gemeldet werden müssen.

Adobe Campaign unterstützt die Übergabe eines Logins und eines Passworts während der Bindungsphase. Es unterstützt auch SMPP über TLS. Es ist darauf hinzuweisen, dass die Bescheinigungen für eine ordnungsgemäße Sicherheit erforderlich sind. Während der SMPP-Connector das Umgehen von Zertifikatprüfungen erlaubt, sollte er nur zum Testen verwendet werden, da TLS ohne Zertifikate eine wesentlich geringere Sicherheit bietet.

Der Connector verwendet die Standardzertifikate, die von der Systembibliothek `openssl` bereitgestellt werden. Normalerweise wird es vom `/etc/ssl/certs` Verzeichnis auf Debian bereitgestellt. Dieser Ordner wird standardmäßig vom &quot;ca-certificates&quot;-Paket bereitgestellt, kann jedoch angepasst werden.

### Informationen in jeder Art von PDU {#information-pdu}

Jede Art von PDU hat unterschiedliche Felder, die verschiedene Informationen enthalten. Diese PDU sind in der Spezifikation [SMPP 3.4](https://smpp.org/SMPP_v3_4_Issue1_2.pdf) aufgeführt.

In jedem Abschnitt unten werden die PDU und ihre synchrone Antwort (`*_RESP PDU`) beschrieben. Alle PDUs müssen mit einem entsprechenden `RESP` bestätigt werden. Dies ist ein obligatorischer Teil der Spezifikation.

PDUs können optionale Felder haben. Hier werden nur die gebräuchlichsten Felder beschrieben. Weitere Informationen finden Sie in der Spezifikation [SMPP 3.4](https://smpp.org/SMPP_v3_4_Issue1_2.pdf).

#### BIND_TRANSMITTER / BIND_RECEIVER / BIND_TRANSCEIVER {#bind-transmitter}

Mit dieser PDU wird eine Verbindung zum SMSC initiiert. **Transmitter**,  **** Receiverund  **** Transceivermodi ändern nur die Art von SMS, die über diese Verbindung übertragen werden darf, insbesondere:

| Mode | Zulässige SMS-Typen |
|:-:|:-:|
| Transmitter | MT |
| Empfänger | MO + SR |
| Transceiver | MT + MO + SR |

Bemerkenswerte Felder in einem `BIND_* PDU`:

* **system_id**: Für die Authentifizierung verwendete Anmeldung. Wird im Externe Konto eingestellt.

* **password**: Für die Authentifizierung verwendetes Kennwort. Wird im Externe Konto eingestellt.

* **system_type**: Für einige Anbieter muss ein bestimmter Wert festgelegt werden. Wird im Externe Konto eingestellt und ist in allen Versionen verfügbar. Häufig wird zwischen verschiedenen Vertragsarten, Kanälen, Ländern usw. unterschieden.

* **addr_** tonand  **addr_npi**: Von einigen Anbietern erforderlich. Wird durch die Einstellungen `Bind TON` und `Bind NPI` im Externe Konto festgelegt.

* **address_range**: Von einigen Anbietern erforderlich. Meistens ist dies eine Liste von Kurzcodes, die für diese Verbindung zulässig sind. Wird im Externe Konto eingestellt.

`BIND_*_RESP` hat kein bestimmtes Feld, bestätigt es, ob die Verbindung erfolgreich war oder nicht.

#### UNBIND {#unbind}

Diese PDU muss vom System gesendet werden, bevor die Verbindung getrennt wird. Es muss die passende `UNBIND_RESP PDU` warten, bevor die Verbindung geschlossen wird.

Bei Übereinstimmung mit SMSC darf die Verbindung nicht geschlossen werden, die TCP-Verbindung wird vom Adobe Campaign-Anschluss gesteuert.

#### SUBMIT_SM {#submit-sm}

Diese PDU sendet ein MT an die SMSC. Seine Antwort PDU gibt die ID des MT.

Bemerkenswerte Felder in einem `SUBMIT_SM PDU`:

* **service_type**: von einigen Anbietern benötigt. Wird in den Eigenschaften des Versands festgelegt.

* **source_addr_** tonand  **source_addr_npi**: gibt an, welche Art von Quelladresse übertragen wird. Die Bedeutung dieser Felder ist standardisiert, da sie jedoch von einigen Anbietern unterschiedlich verwendet werden, sollten Sie den Anbieter nach seinem korrekten Wert fragen. Wird im Externe Konto eingestellt.

* **source_addr**: Quelladresse/ADC des MT. Es wird auf dem Handy angezeigt. Wird im Externe Konto und im Versand festgelegt, hat der Wert im Versand Vorrang vor dem Wert des Externen Kontos.

* **dest_addr_** tonand  **dest_addr_npi**: gibt an, welche Art von Zieladresse übermittelt wird (z. B. lokales oder internationales Format). Die Bedeutung dieser Felder ist standardisiert, da sie jedoch von einigen Anbietern unterschiedlich verwendet werden, sollten Sie den Anbieter nach seinem korrekten Wert fragen. Wird im Externe Konto eingestellt.

* **destination_addr**: empfänger-Adresse, Telefonnummer oder MSISDN.

* **esm_class**: , um festzustellen, ob UDH im Textfeld verwendet wird oder nicht. Aktiviert automatisch durch den Connector für geteilte SMS, wenn der `message_payload`-Modus nicht verwendet wird.

* **priority_Flag**: Priorität dieser Nachricht gegenüber anderen. Das hängt mit der Priorität des Versands selbst zusammen.

* **validity_period**: Zeitstempel, nach dem kein erneuter Versuch unternommen werden sollte. Wird im Versand selbst aufgestellt.

* **registered_Versand**: gibt an, ob ein SR angefordert wird oder nicht. Adobe Campaign setzt immer dieses Flag, mit Ausnahme der automatischen Antworten. Bei mehrteiligen Nachrichten wird das Flag nur für den ersten Teil eingestellt. Alle Versionen haben das gleiche Verhalten.

* **data_coding**: gibt die im Textfeld verwendete Kodierung an. Weitere Informationen finden Sie im Abschnitt [SMS-Textkodierung](../../administration/using/sms-protocol.md#sms-text-encoding).

* **short_message**: der Text der Nachricht. Wenn UDH verwendet wird, enthält dies auch den UHD-Header.

Adobe Campaign unterstützt die folgenden optionalen Felder:

* **dest_addr_subunit**: zur Angabe der Zielgruppe des SMS: Flash-, Mobil- oder SIM-Karte. Wird in den Eigenschaften des Versands festgelegt.

* **message_payload**: Wenn dies im Externe Konto aktiviert ist, werden lange Nachrichten in einer einzigen PDU gesendet und der Text wird in diesem Feld anstelle des  `short_message` Felds übertragen.

#### SENDEN_SM_RESP {#submit-sm-resp}

Diese PDU enthält die ID des MT. Dies ist nützlich, um es mit eingehender SR abzugleichen.

>[!IMPORTANT]
>
>Viele Anbieter übermitteln die MT-ID hexadezimal. Stellen Sie sicher, dass Sie die Einstellung **ID im MT-Bestätigungsformat** im Externe Konto korrekt festlegen.

Einige Anbieter senden `SUBMIT_SM_RESP` nach dem Senden des SR. Um dieses Verhalten zu berücksichtigen, wartet Adobe Campaign 30 Sekunden, bevor es **Ungültige Nachrichten-ID** auf einen SR mit einer unbekannten ID antwortet.

#### DELIVER_SM {#delivery-sm}

Diese PDU wird vom SMSC an Adobe Campaign gesendet. Es enthält entweder ein MO oder ein SR.

Die meisten Felder haben dieselbe Bedeutung wie das `SUBMIT_SM`-Gegenstück. Die folgenden Listen sind hilfreich:

* **source_addr**: Quelladresse des MO/SR. Normalerweise ist dies eine Telefonnummer.

* **destination_addr**: Kurzcode, der das MO oder die SR erhalten hat.

* **esm_class**: verwendet, um festzustellen, ob die PDU ein MO oder ein SR ist.

* **short_message**: Text der Nachricht. Für SR enthält dies Daten, die in Anhang B der SMPP-Protokollspezifikation beschrieben sind. Weitere Informationen finden Sie unter [SR-Fehlerverwaltung](../../administration/using/sms-protocol.md#sr-error-management).

Adobe Campaign kann die Nachrichten-ID im optionalen Feld `receipted_message_id` mit einer Konfigurationseinstellung lesen.

#### DELIVER_SM_RESP {#deliver-sm-resp}

Diese PDU wird von Adobe Campaign gesendet, um SR und MO zu bestätigen.

Adobe Campaign Standard sendet nur dann ein `DELIVER_SM_RESP`, wenn alle Verarbeitungsschritte erfolgreich sind. Dadurch wird gewährleistet, dass keine SR- oder MO-Angabe gemacht wird, während weiterhin die Gefahr von Verarbeitungsfehlern besteht.

#### INQUIRE_LINK {#enquire-links}

Diese PDU wird nur verwendet, um zu überprüfen, ob die Verbindung live ist. Die Häufigkeit sollte entsprechend den Bedürfnissen des Anbieters festgelegt werden.

Die Standardeinstellung von 60 Sekunden sollte mit den meisten im Externe Konto festgelegten Konfigurationen übereinstimmen.

#### INQUIRE_LINK_RESP {#enquire-links-resp}

Diese PDU erkennt an, dass die Verbindung am Leben ist.

### Mehrteilige SMS (lange SMS) {#multipart}

Mehrteilige SMS, oder lange SMS, sind SMS, die in mehreren Teilen gesendet werden. Aufgrund der technischen Einschränkungen des Mobilfunknetzprotokolls darf eine SMS nicht größer als 140 Byte sein oder muss geteilt werden. Weitere Informationen zur Anzahl der Zeichen, die in eine SMS passen können, finden Sie im Abschnitt [SMS-Textkodierung](../../administration/using/sms-protocol.md#sms-text-encoding).

Jeder Teil einer langen Nachricht ist eine individuelle SMS. Diese Teile werden unabhängig im Netzwerk montiert und vom empfangenden Handy montiert. Um weitere Zustellversuche- und Verbindungsprobleme zu verarbeiten, sendet Adobe Campaign diese Teile in umgekehrter Reihenfolge und fordert nur einen SR für den ersten Teil der Nachricht an, den letzten. Da das Handy nur eine Nachricht anzeigt, wenn der erste Teil des Handys empfangen wird, produzieren weitere Zustellversuche mit weiteren Teilen keine Duplikate auf dem Handy.

Die maximale Anzahl von SMS pro Nachricht kann pro Versand mithilfe der Einstellung **Maximale Anzahl von SMS pro Nachricht** in **Versandvorlage** eingestellt werden. Nachrichten, die diese Grenze überschreiten, schlagen während des Versands mit einer SMS zu lange Fehlerursache fehl.

Es gibt 2 Möglichkeiten, lange SMS zu senden:

* **UDH**: die standardmäßige und empfohlene Methode zum Senden langer Nachrichten. In diesem Modus teilt der Connector die Nachricht in mehrere `SUBMIT_SM PDU`s mit UDH-Informationen auf. Dieses Protokoll wird von Mobiltelefonen selbst verwendet. Das bedeutet, dass Adobe Campaign die größte Kontrolle über die Nachrichtengenerierung hat, sodass es genau berechnen kann, wie viele Teile gesendet und wie sie aufgeteilt wurden.

* **message_payload**: die Möglichkeit, die gesamte lange Nachricht in einer einzigen Nachricht zu senden  `SUBMIT_SM PDU`. Der Anbieter muss ihn aufteilen, was bedeutet, dass Adobe Campaign nicht genau wissen kann, wie viele Teile gesendet wurden. Einige Anbieter benötigen diesen Modus, aber wir empfehlen Ihnen, ihn nur zu verwenden, wenn sie UDH nicht unterstützen.

Weitere Informationen zum Protokoll und den Formaten finden Sie in der Beschreibung der Felder `esm_class`, `short_message` und `message_payload` der [SUBMIT_SM PDU](../../administration/using/sms-protocol.md#information-pdu).

### Durchsatzbegrenzung und Fenster {#throughput-capping}

Die meisten Anbieter benötigen für jede SMPP-Verbindung eine Grenze für den Durchsatz. Dies kann durch die Festlegung einer Reihe von SMS im Externe Konto erreicht werden. Beachten Sie, dass die Durchsatzeinschränkung pro Verbindung erfolgt. Der effektive Gesamtdurchsatz ist der Grenzwert pro Verbindung multipliziert mit der Gesamtanzahl der Verbindungen. Dies wird im Abschnitt [Gleichzeitige Verbindungen](../../administration/using/sms-protocol.md#connection-settings) beschrieben.

Um einen maximalen Durchsatz zu erreichen, müssen Sie das maximale sendende Fenster präzisieren. Das sendende Fenster ist die Anzahl der `SUBMIT_SM PDU`s, die gesendet werden können, ohne auf ein `SUBMIT_SM_RESP` zu warten. Weitere Informationen finden Sie im Abschnitt [Einstellung des Sendefensters](../../administration/using/sms-protocol.md#throughput-timeouts).

### SR und Fehlerverwaltung (&quot;Anhang B&quot;) {#sr-error-management}

Das SMPP-Protokoll definiert standardmäßige synchrone Fehler in `RESP PDU`s, definiert jedoch keine Fehlercodes für SR. Jeder Anbieter verwendet seine eigenen Fehlercodes mit ihrer Bedeutung.

Eine Empfehlung wird im Abschnitt &quot;Anhang B&quot;der [SMPP-Protokollspezifikation](https://smpp.org/SMPP_v3_4_Issue1_2.pdf) (Seite 167) abgegeben, wobei die eigentlichen Fehlercodes und ihre Bedeutung nicht Liste werden.

Um sich an das Fehlermanagement anzupassen, wurde das brelog-Meldungssystem von Adobe Campaign genutzt, um Fehler und deren Schwere (hart, weich usw.) ordnungsgemäß bereitzustellen.

Wie bereits erwähnt, gibt es zwei verschiedene Arten von Fehlern:

* synchrone Antworten in den `SUBMIT_SM_RESP`, die unmittelbar nach dem Senden der Nachricht an die SMSC erfolgen
* Empfangsbestätigungen, die viel später eingehen, wenn das Handy die Nachricht erhalten hat oder wenn die Nachricht abgelaufen ist. In diesem Fall wird der Fehler in einem SR gefunden.

Wenn ein SR empfangen wird, befinden sich Status und Fehler im Feld `short_message` (Beispiel für Implementierungen, die mit Anhang B übereinstimmen). Das Feld `short_message` der PDU wird häufig als **Textfeld** bezeichnet, da es Text in MT enthält. Bei SR enthält es technische Informationen sowie ein Unterfeld mit dem Namen **Text**. Diese beiden Felder unterscheiden sich und `short_message` enthält tatsächlich das Feld **Text** und andere Informationen.

#### SR-Textfeldformat {#sr-text-field-format}

Die Spezifikation empfiehlt die Verwendung dieses Formats für das SR-Textfeld. Es handelt sich dabei um eine Liste von Unterfeldern, die durch Leerzeichen voneinander getrennt sind und den Feldnamen und den zugehörigen Wert trennen. Bei Feldnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Beispiel eines SR-Textfelds, das der Empfehlung in Anhang B entspricht:

```
id:1234567890 sub:001 dlvrd:001 submit date:1608011415 done date:1608011417 stat:DELIVRD err:000 Text:Hello Adobe world
```

Das ID-Feld ist die ID, die im `SUBMIT_SM_RESP PDU`, der Bestätigung des MT erhalten wird.

`sub` und  `dlvrd` sollen die Menge der gelieferten Teile und zugestellten Nachrichten zählen, aber dies wird von Adobe Campaign nicht verwendet, da das Breitbandsystem bessere und besser integrierte Informationen liefert.

`submit date` und  `done date` Felder sind indikative Zeitstempel zum Zeitpunkt des Versands des MT und zum Zeitpunkt des Versands des SR durch das Mobilgerät. Erwarten Sie einige Probleme mit Zeitzonen oder sogar falschen Zeitstempeln, die von Mobiltelefonen mit falschem Datumsformat angegeben werden.

Das Feld &quot;state&quot;ist wichtig, da es den Status der Nachricht angibt. Der einzige wichtige Status ist `DELIVRD`, `UNDELIV` und `REJECTD`. Der Status `DELIVRD` gibt einen Erfolg an, die anderen beiden geben einen Fehler an. Andere Werte sind möglich, aber es handelt sich in der Regel um Zwischenbenachrichtigungen, z.B. wenn der MT den Mobilnetzbetreiber erreichte, nicht aber das Handy. Diese Zwischenbenachrichtigungen werden von Adobe Campaign ignoriert.

Das Feld &quot;Fehler&quot;enthält den anbieterspezifischen Fehlercode. Der Anbieter muss eine Tabelle möglicher Fehlercodes zusammen mit ihrer Bedeutung geben, um diesen Wert interpretieren zu können.

Schließlich enthält das Textfeld normalerweise den Anfang des Textes des MT. Dies wird von Adobe Campaign ignoriert, und einige Anbieter senden es nicht, um PII-Leckagen und Netzwerkbandbreitenverbrauch zu vermeiden. Es kann während der Fehlerbehebung verwendet werden, um die SR-Übereinstimmung mit einem Test MT leichter zu erkennen, indem Sie dieses Feld lesen.

### Beispiel für die SR-Verarbeitung in Adobe Campaign Standard Extended generischer SMPP {#sr-processing}

In diesem Beispiel werden die Fälle einer Implementierung nach der Empfehlung in Anhang B, die Standardwerte im Externe Konto und eine erfolgreiche SMS-MT angezeigt.

```
id:1234567890 sub:001 dlvrd:001 submit date:1608011415 done date:1608011417 stat:DELIVRD err:000 Text:Hello Adobe world
```

Erstens wird der Regex `id extraction` angewendet, um die ID zu extrahieren und mit dem entsprechenden MT abzustimmen.

Anschließend werden die Felder `status extraction` regex und `error code extraction` regex angewendet, um sie zu extrahieren, und sie werden an die Zeichenfolge angehängt.

Die Broadlog-Meldung wird mit folgenden Informationen erstellt und die ursprüngliche unveränderte Zeichenfolge wird als Referenz angehängt:

```
SR ExampleProvider DELIVRD 000|MESSAGE=id:1234567890 sub:001 dlvrd:001 submit date:1608011415 done date:1608011417 stat:DELIVRD err:000 Text:Hello Adobe world
```

Die Nachricht wird dann normalisiert und der MESSAGE-Teil wird entfernt, damit mehrere Nachrichten mit demselben STATUS- und Fehlercode übereinstimmen können.

```
SR ExampleProvider DELIVRD 000|#MESSAGE#
```

Wenn die Nachricht nicht bereits in der Tabelle mit der Breitbandmeldung bereitgestellt wurde, wird ein neuer Eintrag erstellt, wobei die gesamte Meldung als **firstText** und die normalisierte Meldung verwendet wird. Dann verwendet der Connector den success und den regex `error`, um festzustellen, ob es sich um einen Erfolg oder einen Fehler handelt:

* Wenn es mit dem Regex `success` übereinstimmt, wird es als Erfolg betrachtet.

* Wenn die Meldung mit dem Regex `error` übereinstimmt, ist sie als Fehler qualifiziert.

* Wenn keine dieser beiden Regex-Übereinstimmungen auftritt, wird der SR ignoriert. Es kann sich um eine Zwischenmeldung handeln, die nicht von Adobe Campaign verarbeitet wird.

Standardmäßig werden alle Fehler als weiche Fehler bereitgestellt. Das bedeutet, dass harte Fehler von Hand bereitgestellt werden müssen.

### SMS-Textkodierung {#sms-text-encoding}

Bei Kodierungsproblemen **sollten Sie sich immer an den SMSC-Anbieter wenden.** Nur die SMSC-Anbieter verfügen über genaue Kenntnisse der von ihnen unterstützten Kodierung und spezielle Regeln, die aufgrund von Einschränkungen in ihrer technischen Plattform gelten können.

SMS-Nachrichten verwenden eine spezielle 7-Bit-Kodierung, die oft GSM7-Kodierung genannt wird.

Im SMPP-Protokoll wird der GSM7-Text auf 8 Bit pro Zeichen erweitert, um die Fehlerbehebung zu erleichtern. Der SMSC packt es in 7 Bit pro Zeichen, bevor es an das Handy gesendet wird. Das bedeutet, dass das Feld `short_message` des SMS im SMPP-Frame bis zu 160 Byte lang sein kann, während es beim Senden im mobilen Netzwerk auf 140 Byte begrenzt ist.

Bei Kodierungsproblemen sollten Sie Folgendes überprüfen:

* Achten Sie darauf, dass Sie wissen, zu welcher Kodierung welche Zeichen gehören. GSM7 unterstützt nicht vollständig diakritische Zeichen (Akzente). Insbesondere auf Französisch, wo é und è Teil von GSM7, aber ê, â oder ï sind nicht. Dasselbe gilt für Spanisch.

* Die C mit cedilla (ç) ist nur im oberen Fall im GSM7 Alphabet vorhanden, aber einige Telefone geben es im unteren Fall oder &quot;smart&quot; Fall. Die allgemeine Empfehlung besteht darin, sie vollständig zu vermeiden und den Cedilla zu entfernen oder auf UCS-2 umzustellen.

* **Verwenden Sie ASCII nicht in** SMSs, es sei denn, Sie werden ausdrücklich vom SMSC-Anbieter angefordert. Durch diese Kodierung wird Platz verloren, da sie 8-Bit-Zeichen und eine geringere Abdeckung aufweist als GSM7. Diese Kodierung kann für CDMA-Netzwerke erforderlich sein, die in Nordamerika verwendet werden.

* Latein-1 wird nicht immer unterstützt. Überprüfen Sie die Kompatibilität mit Ihrem SMSC-Anbieter, bevor Sie versuchen, Latin-1 zu verwenden.

* Nationale Sprachverschiebungstabellen werden vom Adobe Campaign Connector nicht unterstützt. Sie müssen stattdessen UCS-2 oder andere `data_coding` verwenden.

* UCS-2 und UTF-16 werden oft per Telefon gemischt. Dies ist ein Problem bei der Verwendung von Emojis und anderen Zeichen, die nicht in UCS-2 vorhanden sind.

* Die meisten Telefone haben keine Schriftzeichen für alle UCS-2-Zeichen. Smartphones sind in der Regel in der Lage, seltene Zeichen relativ einfach anzuzeigen, aber Feature-Telefone bieten im Allgemeinen nur eine begrenzte Unterstützung für das, was in der Muttersprache des Landes nützlich ist, in dem sie gekauft wurden. Wenn Sie Emoji oder ASCII-art verwenden möchten, testen Sie es auf einer Vielzahl von Telefonen, bevor Sie es senden. Adobe Campaign Vorschau simuliert keine fehlenden Glyphen und zeigt Symbole an, die im Webbrowser verfügbar sind.

Das Feld `data_coding` gibt an, welche Kodierung verwendet wird. Ein Hauptproblem besteht darin, dass der Wert 0 die standardmäßige SMSC-Kodierung in der Spezifikation bedeutet, die normalerweise auf GSM7 verweist. Vergewissern Sie sich beim SMSC-Partner, welche Kodierung mit `data_coding` = 0 verknüpft ist, die nur von Adobe Campaign unterstützt wird. Andere `data_coding`-Werte folgen tendenziell der Spezifikation, aber die einzige Möglichkeit sicherzustellen ist, dass Sie beim SMSC-Anbieter nachfragen.

Die maximale Größe einer Nachricht hängt von ihrer Kodierung ab. In dieser Tabelle sind alle relevanten Informationen zusammengefasst:

| Kodierung | Übliche data_coding | Nachrichtengröße (Zeichen) | Teilgröße für mehrteilige SMS | Verfügbare Zeichen |
|:-:|:-:|:-:|:-:|:-:|
| GSM7 | 0 | 160 | 152 | GSM7-Basiszeichensatz + -Erweiterung (erweiterte Zeichen dürfen 2 Zeichen umfassen) |
| Latin-1 | 3 | 140 | 134 | ISO-8859-1 |
| UCS-2 <br>UTF-16 | 8 | 70 | 67 | Unicode (je nach Telefon unterschiedlich) |

## SMPP-Externe Konto-Parameter {#SMPP-parameters-external}

Jede Implementierung des SMPP-Protokolls hat viele Varianten. Zur Verbesserung der Kompatibilität und Anpassbarkeit stehen viele Einstellungen zur Verfügung, um das Verhalten des SMPP-Connectors zu ändern. In diesem Abschnitt werden alle Parameter und ihre Auswirkungen auf den Connector beschrieben.

### Allgemeine Parameter und Routing {#general-parameters-routing}

**MTA-Instanzen für dieses Konto beschränken**

Es ist möglich, eine Begrenzung für die Anzahl der MTA-Instanzen festzulegen, die eine Verbindung zum SMPP-Anbieter herstellen dürfen. Wenn diese Option aktiviert ist, können Sie angeben, wie viele MTAs maximal verwendet werden können.

Diese Option ermöglicht eine genauere Steuerung der Anzahl der Verbindungen, siehe [Gleichzeitige Verbindungen](../../administration/using/sms-protocol.md#connection-settings).

Wenn Sie einen Wert festlegen, der höher als die Anzahl der ausgeführten MTAs ist, werden alle MTAs wie normal ausgeführt: Diese Option ist nur eine Beschränkung und kann keine zusätzlichen MTAs hervorrufen.

Wenn Sie die Anzahl der Verbindungen genau steuern müssen, z. B. die Anbieteranforderung, sollten Sie diese Option immer einstellen, selbst wenn die aktuelle Bereitstellung die richtige Anzahl von MTAs hat. Wenn anschließend weitere MTAs hinzugefügt werden, wird die Verbindungsgrenze weiterhin eingehalten.

### Verbindungsparameter {#connection-settings}

#### SMPP-Verbindungsmodus {#smpp-connection-mode}

Legt die Verbindung im Modus **transceiver** oder im separaten Modus **sender+empfänger** fest. Wenn Sie zum getrennten Modus **sender+empfänger** wechseln, gelten die Einstellungen im Abschnitt **SMPP-Verbindungsmodus** für den Transmitter und die Einstellungen im Abschnitt **Receiver-Verbindungseinstellungen** nur, wenn Sie das Kontrollkästchen **Andere Parameter für den Empfänger** aktiviert haben.

#### Name der SMSC-Implementierung {#smsc-implementation-name}

Legt den Namen der SMSC-Implementierung fest. Es sollte auf den Namen Ihres Anbieters eingestellt werden. Wenden Sie sich an den Administrator oder das Zustellteam, um zu erfahren, was in diesem Feld hinzugefügt werden soll. Die Rolle dieses Felds wird im Abschnitt [SR-Fehlerverwaltung](../../administration/using/sms-protocol.md#sr-error-management) beschrieben.

#### Server {#server}

Der DNS-Name oder die IP-Adresse des Servers, mit dem eine Verbindung hergestellt werden soll.

#### Port {#port}

Der TCP-Anschluss, mit dem eine Verbindung hergestellt werden soll.

#### Konto {#account}

Die Anmeldung der Verbindung. Wird im Feld `system_id` der BIND-PDU übergeben.

#### Passwort {#password}

Kennwort der SMPP-Verbindung. Im Kennwortfeld der BIND PDU weitergegeben.

#### Systemtyp {#system-type}

Wert, der im Feld `system_id` der BIND-PDU übergeben wird. Einige Anbieter benötigen hier einen bestimmten Wert.

#### Simultane Verbindungen {#simultaneous-connections}

In Adobe Campaign Standard definiert es die Anzahl der Verbindungen pro SMS-Thread und pro MTA-Prozess.
Die Anzahl der MTA-Prozesse wird durch die Bereitstellung bestimmt: in der Regel gibt es 2 MTAs und 1 Thread. Die Anzahl der Threads kann in der Datei &quot;config-instance.xml&quot;mithilfe der Einstellung &quot;smppConnectorThreads&quot;geändert werden. Normalerweise gibt es 1 MTA-Prozess pro Container und 1 Thread pro MTA-Prozess.

Gesamtverbindungsformel für Adobe Campaign Standard:

* **Gesamtverbindungen = Gleichzeitige Verbindungen * Anzahl Threads * Anzahl der MTAs**

Simultane Verbindungen werden im Externe Konto festgelegt, die Anzahl der Threads in der Datei &quot;config-instance.xml&quot;(smppConnectorThreads) und die Anzahl der MTAs kann im Externe Konto begrenzt werden.

Im getrennten Modus **sender/empfänger** stellt die Anzahl der oben genannten Verbindungen die Anzahl der Paare **sender/empfänger** dar, was bedeutet, dass insgesamt doppelt so viele Anschlüsse vorhanden sind wie die Anzahl der Verbindungen.

#### TLS über SMPP aktivieren {#enable-TLS}

Verwenden Sie TLS, um eine Verbindung zum Anbieter herzustellen. Die Verbindung wird verschlüsselt. Die TLS-Verbindung wird von der OpenSSL-Bibliothek verwaltet. Alles, was für OpenSSL gilt, ist für diese Verbindung wahr.

#### Ausführliche SMPP-Verfolgung in Logdatei aktivieren {#enable-verbose-log-file}

Mit dieser Einstellung wird der gesamte SMPP-Traffic in Protokolldateien abgelegt. Es ist häufig erforderlich, Parameter während der ersten Einrichtung anzupassen. Dies muss bei der Fehlerbehebung für den Connector und im Vergleich zum vom Anbieter erkannten Traffic aktiviert werden.

### Verbindungseinstellung des Empfängers {#receiver-connection}

Dieser Abschnitt ist nur im getrennten Modus **sender+empfänger** sichtbar.

#### Andere Parameter für den Receiver verwenden {#receiver-parameters}

Wenn das Kontrollkästchen deaktiviert ist, werden dieselben Einstellungen für Sender und Empfänger verwendet.

Wenn das Kontrollkästchen aktiviert ist, gelten die Einstellungen im Abschnitt **Verbindungseinstellungen** für den Sender und die Einstellungen in den Einstellungen **Receiver-Verbindung** gelten für den Empfänger.

**Receiver-Server, Port, Konto, Kennwort, Systemtyp**

Diese Einstellungen gelten für den Empfänger im Modus **sender+empfänger**. Sie funktionieren wie der Transmitter-Teil, siehe oben für weitere Details.

### Parameter des SMPP-Kanals {#smpp-channel-settings}

#### Transliteration der Zeichen zulassen {#allow-character-transliteration}

Transliteration ist der Prozess der Suche nach Zeichen, die den fehlenden entsprechen. Beispielsweise fehlt das französische &quot;ê&quot;(z. B. mit Zirkumflex-Akzent) in der GSM-Kodierung, kann aber durch &quot;e&quot;ersetzt werden, ohne dass die Lesbarkeit beeinträchtigt wird.

Wenn dieses Kontrollkästchen deaktiviert ist, schlägt die Textkodierung fehl, wenn die Zeichenfolge nicht exakt so kodiert werden kann, wie es der Fall ist.

Wenn dieses Kontrollkästchen aktiviert ist, versucht die Textkodierung, die Zeichenfolge in eine ungefähre Version zu konvertieren, anstatt zu fehlschlagen. Wenn einige Zeichen keine Entsprechung in der Zielgruppe-Kodierung haben, schlägt die Textkodierung fehl.

Eine allgemeinere Erläuterung des Kodierungsprozesses finden Sie unter [Definieren einer bestimmten Zuordnung der Kodierungsvorgaben](../../administration/using/sms-protocol.md#SMSC-specifics).

#### Eingehende MO in Datenbank speichern {#incoming-mo-storing}

Bei Aktivierung wird das eingehende MO in der InSMS-Tabelle der Datenbank gespeichert. Diese Tabelle kann mit der Aktivität der Abfrage eines jeden Workflows abgefragt werden.

#### Echtzeit-KPI-Aktualisierungen während SR-Verarbeitung aktivieren {#real-time-kpi}

Wenn diese Option aktiviert ist, werden KPIs auf der Hauptseite des Versands in Echtzeit aktualisiert, wenn sie den Fehler SR erhalten.

Der Nachteil kann aufgrund der erzeugten Datenbankeinschränkung eine niedrige Leistung sein. Wenn diese Option deaktiviert ist, werden Statistiken vom **syncfromexec**-Workflow aktualisiert, der alle 20 Minuten ausgeführt wird.

#### Anrufernummer {#source-number}

Definiert die Standardquelladresse für Nachrichten. Diese Einstellung gilt nur, wenn die Quellnummer im Versand leer gelassen wurde.

Standardmäßig wird das Feld für die Quellnummer nicht übergeben, sodass der Anbieter es durch den Kurzcode ersetzen wird.

Dadurch wird die Funktion zum Überschreiben der Absenderadresse/des ADC aktiviert.

#### Kurzwahlnummer {#short-code}

Gibt den wichtigsten Kurzcode des Kontos an. Wenn für dieses Konto mehrere Kurzcodes verwendet werden oder der Kurzcode unbekannt ist, lassen Sie dieses Feld leer.

Die Angabe von Kurzcode ist für zwei Funktionen hilfreich:

* Die Vorschau zeigt den Kurzcode an, wenn keine Quellnummer angegeben wurde. Es wird das wahre Verhalten auf dem Handy widerspiegeln.

* Die Einstellung &quot;Blockierungsliste&quot;der Funktion für die automatische Antwort sendet nur für einen bestimmten Kurzcode an die Quarantäne des Benutzers.

#### Quell-TON/NPI, Ziel-TON/NPI {#ton-npi}

TON (Type of Number) und NPI (Numbering Plan Indicator) werden in Abschnitt 5.2.5 der Spezifikation [SMPP 3.4](https://smpp.org/SMPP_v3_4_Issue1_2.pdf) (Seite 117) beschrieben. Diese Werte sollten auf die Anforderungen des Anbieters eingestellt werden.

Sie werden wie folgt übertragen: in den Feldern `source_addr_ton`, `source_addr_npi`, `dest_addr_ton` und `dest_addr_npi` der Felder `SUBMIT_SM PDU`.

#### Diensttyp {#service-type}

Dieses Feld wird wie folgt im Feld `service_type` des Felds `SUBMIT_SM PDU` übertragen. Stellen Sie dies auf die Anforderungen des Anbieters ein.

### Durchsatz und Zeitüberschreitung {#throughput-timeouts}

Diese Einstellungen steuern alle Zeitaspekte des SMPP-Kanals. Einige Anbieter benötigen eine sehr genaue Steuerung der Nachrichtenrate, der Fenster- und Wiederholungszeiten. Diese Einstellungen sollten auf Werte gesetzt werden, die der Kapazität des Anbieters und den in ihrem Vertrag angegebenen Bedingungen entsprechen.

#### Übertragungsfenster {#sending-window}

Das Fenster ist die Anzahl der `SUBMIT_SM PDU`s, die gesendet werden können, ohne auf eine Übereinstimmung `SUBMIT_SM_RESP` zu warten.

Beispiel einer Übertragung mit einem maximalen Fenster von 4:

![](assets/do-not-localize/sms_protocol_2.png)

Das Fenster hilft, den Durchsatz zu erhöhen, wenn die Netzwerkverbindung eine hohe Latenz aufweist.  Der Wert des Fensters muss mindestens der Anzahl der SMS/s entsprechen, multipliziert mit der Latenz des Links in Sekunden, damit der Connector nie auf ein `SUBMIT_SM_RESP` wartet, bevor die nächste Nachricht gesendet wird.
Wenn das Fenster zu groß ist, können Sie bei Verbindungsproblemen mehr Duplikat-Nachrichten senden. Außerdem haben die meisten Anbieter eine sehr strenge Begrenzung für das Fenster und verweigern Nachrichten, die über die Grenze gehen.

Berechnung der optimalen Formel für das sendende Fenster:

* Messen Sie die maximale Latenz zwischen `SUBMIT_SM` und `SUBMIT_SM_RESP`.

* Multipliziert diesen Wert in Sekunden mit dem maximalen MT-Durchsatz. Dadurch erhalten Sie den optimalen Wert des sendenden Fensters.

Beispiel: Wenn Sie einen maximalen Durchsatz von 300 SMS/s festgelegt haben und eine Latenz von 100 ms zwischen `SUBMIT_SM` und `SUBMIT_SM_RESP` durchschnittlich besteht, ist der optimale Wert `300×0.1 = 30`.

#### Maximaler Durchsatz an MT {#max-mt-throughput}

Maximale Anzahl von MT pro Sekunde und pro Verbindung. Diese Einstellung wird strikt durchgesetzt, die MTA wird Nachrichten nie schneller als diese Grenze senden. Es ist nützlich für Anbieter, die eine genaue Drosselung benötigen.

Um die Gesamtdurchsatzgrenze zu kennen, multiplizieren Sie diese Zahl mit der Gesamtanzahl der Verbindungen, wie in der obigen Formel beschrieben.

0 bedeutet keine Begrenzung, die MTA wird MT so schnell wie möglich senden.

Es wird generell empfohlen, diese Einstellung unter 1000 zu halten, da es nicht möglich ist, einen präzisen Durchsatz über dieser Zahl zu garantieren, es sei denn, die endgültige Architektur wurde entsprechend bewertet und der SMPP-Anbieter wurde speziell angefordert. Möglicherweise ist es besser, die Anzahl der Verbindungen auf über 1000 MT/s zu erhöhen.

#### Dauer bis zu einer erneuten Verbindung {#time-reconnection}

Wenn die TCP-Verbindung verloren geht, wartet der Connector diese Zeit, bevor eine Verbindung hergestellt wird.

#### Gültigkeitsdauer der MT {#expiration-period}

Timeout zwischen `SUBMIT_SM` und dem zugehörigen `SUBMIT_SM_RESP` Wenn das `RESP` nicht rechtzeitig empfangen wird, gilt die Nachricht als fehlgeschlagen und die globale Wiederholungsrichtlinie der MTA gilt.

#### Bind-Timeout {#bind-timeout}

Timeout zwischen dem TCP-Verbindungsversuch und der `BIND_*_RESP`-Antwort. Nach Ablauf des Zeitlimits wird die Verbindung durch den Adobe Campaign-Connector geschlossen. Die Verbindung wird erst nach einer erneuten Verbindung hergestellt.

#### enquire_link-Zeitraum {#enquire-link-period}

`enquire_link` ist eine besondere Art von PDU gesendet, um die Verbindung am Leben zu halten. Dieser Zeitraum ist in Sekunden. Der Kampagnen-Connector sendet nur `enquire_link`, wenn die Verbindung untätig ist, um die Bandbreite zu sparen. Wenn nach diesem Zeitraum kein RESP empfangen wird, wird die Verbindung als &quot;tot&quot;betrachtet und ein erneuter Verbindungsvorgang wird ausgelöst.

### SMSC-Besonderheiten {#SMSC-specifics}

Bei diesen Einstellungen handelt es sich um erweiterte Einstellungen, mit denen der Adobe Campaign Connector an die meisten SMPP-Implementierungseigenschaften angepasst wird.

#### Definieren einer bestimmten Zuordnung von Kodierungen {#encoding-specific-mapping}

Einzelheiten zur Textkodierung finden Sie im Abschnitt [SMS-Textkodierung](../../administration/using/sms-protocol.md#sms-text-encoding).

Mit dieser Einstellung können Sie eine benutzerdefinierte Kodierungszuordnung definieren, die von der Spezifikation abweicht. Sie können eine Liste von Kodierungen mit ihrem `data_coding`-Wert deklarieren.

Die MTA versucht, die Kodierung mit der ersten Kodierung in der Liste durchzuführen. Falls dies fehlschlägt, wird versucht, die nächste Kodierung auf der Liste zu verwenden usw. Wenn keine Kodierung zum Kodieren der Nachricht verwendet werden kann, tritt ein Fehler auf. Sobald die Kodierung gefunden wurde, erstellt die MTA das `SUBMIT_SM PDU`-Feld mit dem kodierten Text und das `data_coding`-Feld mit dem in der Tabelle angegebenen Wert.

Die Reihenfolge der Elemente in der Tabelle ist wichtig: Kodierungen sind Versuche von oben nach unten. Sie sollten die billigste oder die am besten empfohlene Kodierung an die Spitze der Liste stellen und dann immer teurere Kodierungen folgen.

Bitte beachten Sie, dass UCS-2 nie ausfallen wird, da es alle in Adobe Campaign unterstützten Zeichen kodieren kann und dass die maximale Länge einer UCS-2 SMS viel kleiner ist: Nur 70 Zeichen.

Sie können diese Einstellung auch verwenden, um zu erzwingen, dass eine bestimmte Kodierung immer verwendet wird, indem Sie in der Zuordnungstabelle nur eine Zeile deklarieren.

Die Standardzuordnung, die verwendet wird, wenn das Kontrollkästchen nicht aktiviert ist, entspricht der folgenden Tabelle:

| data_coding | Kodierung |
|---|---|
| 0 | GSM |
| 9 | UCS-2 |

Das bedeutet, dass die MTA versuchen wird, die Nachricht im GSM zu kodieren. Wenn es erfolgreich ist, wird es gesendet, wenn `data_coding` auf 0 gesetzt ist.

Wenn die Nachricht nicht im GSM kodiert werden kann, wird sie in UCS-2 kodiert und `data_coding` auf 8 gesetzt.

#### message_payload aktivieren {#enable-message-payload}

Wenn diese Option deaktiviert ist, wird lange SMS durch die MTA aufgeteilt und mit UDH mehrmals gesendet. `SUBMIT_SM PDU` Die Nachricht wird nach UDH-Daten vom Mobiltelefon neu zusammengestellt.

Wenn diese Option aktiviert ist, wird lange SMS in einer PDU SUBMIT_SM gesendet, wobei der Text in das optionale Feld message_payload eingefügt wird. Weitere Informationen dazu finden Sie in der [SMPP-Spezifikation](../../administration/using/sms-protocol.md#ACS-SMPP-connector).

Wenn diese Funktion aktiviert ist, kann Adobe Campaign keine SMS-Teile einzeln zählen: alle Nachrichten werden als in einem Teil gesendet gezählt.

#### Senden Sie die vollständige Telefonnummer {#send-full-phone-number}

Wenn dieses Kontrollkästchen nicht aktiviert ist, werden nur Ziffern der Telefonnummer an den Anbieter gesendet (`destination_addr` Feld des Felds `SUBMIT_SM`). Dies ist das Standardverhalten, da der internationale Zahlenindikator, normalerweise ein +-Präfix, in SMPP durch TON- und NPI-Felder ersetzt wird.

Wenn das Kontrollkästchen aktiviert ist, wird die Telefonnummer unverändert gesendet, ohne Vorverarbeitung und potenzielle Leerzeichen, + Präfix oder Pfund/Hash/Star-Zeichen.

Diese Funktion wirkt sich auch auf das Verhalten der Funktion zur automatischen Blockierungsliste der Antwort- aus: Wenn das Kontrollkästchen nicht aktiviert ist, wird ein +-Präfix zu den Telefonnummern hinzugefügt, die in die Tabelle &quot;Quarantäne&quot;eingegeben wurden, um das +-Präfix auszugleichen, das vom SMPP-Protokoll selbst aus der Telefonnummer entfernt wurde.

#### TLS-Zertifikatsprüfung überspringen {#skip-tls}

Wenn TLS aktiviert ist, überspringen Sie alle Zertifikatprüfungen.

Wenn diese Option aktiviert ist, ist die Verbindung nicht mehr sicher, sie sollte nicht in der Produktion aktiviert werden.

Es kann für Debugging- oder Testzwecke nützlich sein.

#### Bind TON/NPI {#bind-ton-npi}

TON (Type of Number) und NPI (Numbering Plan Indicator), beschrieben in Abschnitt 5.2.5 der Spezifikation [SMPP 3.4](https://smpp.org/SMPP_v3_4_Issue1_2.pdf) (Seite 117). Diese Werte sollten auf die Anforderungen des Anbieters eingestellt werden.

Sie werden wie-is in den Feldern `addr_ton` und `addr_npi` der BIND-PDU übertragen.

#### Adressenbereich {#address-range}

Wird als &quot;is&quot;im Feld address_range der BIND-PDU gesendet. Dieser Wert sollte auf die Anforderungen des Anbieters eingestellt werden.

#### Anzahl ungültiger ID-Quittierungen {#invalid-id}

Begrenzt die Anzahl der **Nachrichten-ID ungültig** `DELIVER_SM_RESP`, die für ein einzelnes SR gesendet werden kann.

**Dies sollte nur zur Fehlerbehebung als** Workaround verwendet werden und unter normalen Bedingungen auf 0 gesetzt werden.

Beispiel für Fox bei Einstellung auf 2:

* Der Anbieter sendet ein SR (`DELIVER_SM`) mit der ID &quot;1234&quot;.

* Die ID &quot;1234&quot;konnte nicht in der Datenbank gefunden werden.

* Der Connector zählt für diese ID den Fehler 1 **Ungültige ID**, daher wird `DELIVER_SM_RESP` mit dem Fehlercode &quot;Nachrichten-ID ungültig&quot;(normales Verhalten) gesendet.

* Der Anbieter weitere Zustellversuche dieselbe SR-Nummer mit der ID &quot;1234&quot;.

* Die ID &quot;1234&quot;konnte immer noch nicht in der Datenbank gefunden werden.

* Der Connector zählt für diese ID den Fehler 2 **Ungültige ID**, daher wird `DELIVER_SM_RESP` &quot;OK&quot;gesendet, auch wenn er nicht korrekt verarbeitet wurde.

* Diese Funktion dient zum Entfernen von SR-Puffern auf der Anbieterseite, wenn ungültiger SR-Block zulässig ist, dass Nachrichten nicht verarbeitet werden können.

Wenn dieses Feld auf 0 gesetzt wird, wird der Mechanismus deaktiviert, bei dem **Nachrichten-ID ungültig** immer zurückgegeben wird. Dies ist ein normales Verhalten.

Wenn dieses Feld auf 1 gesetzt wird, reagiert der Connector immer auf &quot;OK&quot;, auch wenn die ID ungültig ist. Diese sollte nur unter Aufsicht, zur Fehlerbehebung und für die Mindestdauer, z. B. zur Behebung eines Problems auf 1 gesetzt werden.

#### Regex zur ID-Extraktion im SR {#regex-extraction}

Das SR-Format wird nicht strikt durch die SMPP-Protokollspezifikation durchgesetzt. Es handelt sich lediglich um eine Empfehlung, die in [Anhang B](../../administration/using/sms-protocol.md#sr-error-management) (Seite 167) der Spezifikation beschrieben ist. Einige SMPP-Implementierer formatieren dieses Feld anders, sodass Adobe Campaign eine Möglichkeit benötigt, das richtige Feld zu extrahieren.

Standardmäßig werden bis zu 10 alphanumerische Zeichen nach `id:` erfasst.

Der Regex muss über genau eine Erfassungsgruppe mit einem Teil in Klammern verfügen. Klammern müssen den ID-Teil umgeben. Das regex-Format ist PCRE.

Achten Sie beim Anpassen dieser Einstellung darauf, möglichst viel Kontext einzuschließen, um falsche Trigger zu vermeiden. Wenn bestimmte Präfixe vorhanden sind, z. B. `id:` im Standard, müssen Sie sie in den Regex aufnehmen. Verwenden Sie außerdem so weit wie möglich Worttrennzeichen (\b), um zu vermeiden, dass Text in der Mitte eines Wortes erfasst wird.

Wenn nicht genügend Kontext in den Regex aufgenommen wird, kann dies einen kleinen Sicherheitsfehler einleiten: der tatsächliche Inhalt der Nachricht kann in den SR aufgenommen werden. Wenn Sie nur ein bestimmtes ID-Format ohne Kontext verwenden, z. B. eine UUID, wird möglicherweise der eigentliche Textinhalt analysiert, z. B. eine UUID, die in das Textfeld eingebettet ist, anstatt der ID.

#### Regex angewendet zur Bestimmung des Erfolgs-/Fehlerstatus {#regex-applied}

Wenn Meldungen mit einer unbekannten Kombination aus Status-/Fehlerfeldern gefunden werden, werden diese Regex auf das Feld &quot;Statistik&quot;angewendet, um festzustellen, ob der SR ein Erfolg oder ein Fehler war. SR mit statischen Werten, die mit keinem dieser Regexes übereinstimmen, werden ignoriert.

Standardmäßig beginnen statische Werte, die mit `DELIV` beginnen, z. B. `DELIVRD` in [Anhang B](../../administration/using/sms-protocol.md#sr-error-management) wird als erfolgreich bereitgestellt und alle statischen Werte, die Fehler aufweisen, z.B. `REJECTED`, `UNDELIV` werden als Fehler betrachtet.

#### ID-Format in MT-Bestätigung {#id-format-mt}

Dies zeigt das Format der ID an, die im Feld `message_id` von `SUBMIT_SM_RESP PDU` zurückgegeben wird.

* **Ändern** Sie nicht: Die ID wird als ASCII-kodierter Text wie in der Datenbank gespeichert. Es erfolgt keine Vorverarbeitung oder Filterung.

* **Dezimalzahl**: Die ID wird als Dezimalzahl im ASCII-Formular erwartet. Leerzeichen am Anfang und Ende sowie vorangestellte Nullen werden entfernt, wenn diese Einstellung verwendet wird.

* **Hexadezimalzahl**: Die ID muss im ASCII-Format eine Hexadezimalzahl sein, ohne vorangestellte Zahl (0x) oder nachgestellte Zahl (h). Die ID wird dann in eine Dezimalzahl umgewandelt, bevor sie in der Datenbank gespeichert wird.

* **Hexadezimalzeichenfolge**: Die ID muss ein ASCII-kodierter Text sein, der selbst eine Zeichenfolge ist, die als Hexadezimalwert kodiert wurde. In der PDU finden Sie beispielsweise `0x34 0x31 0x34 0x32 0x34 0x33`, was in ASCII &quot;414243&quot;übersetzt. Diese Zeichenfolge wird dann als Hexadezimalzeichenfolge von Bytes dekodiert und Sie erhalten &quot;ABC&quot;: speichern Sie die ID &quot;ABC&quot; in der Datenbank.

#### ID-Format in SR {#id-format-sr}

Dies gibt das Format der ID an, die vom `Extraction`-Regex der ID im SR erfasst wird. Werte haben die gleiche Bedeutung und das gleiche Verhalten wie das Format in MT oben.

**SR-Kennung oder Fehlercode in einem optionalen Feld speichern**

Wenn diese Option aktiviert ist, wird der Inhalt der optionalen Felder an den Text angehängt, der durch die oben genannten Regexes verarbeitet wird. Der Text hat das Format `0xTAG:VALUE`, `0xTAG` ist der 4-stellige Hexadezimalwert des Tags in Großbuchstaben, z.B. `0x002E`.

Sie können beispielsweise die ID im Feld `receipted_message_id` erfassen. Aktivieren Sie dazu dieses Kontrollkästchen, und dem Status wird folgender Text hinzugefügt:

```
0x001E:05e3299e-8d37-49d0-97c6-8e4fe60c7739
```

In diesem Beispiel ist 0x001E das Tag des optionalen Felds und die UUID der Wert des Felds.

Um diesen Wert zu erfassen, können Sie jetzt den folgenden Regex in der Extraktion regex der ID im Feld SR festlegen:

```
\b0x001E:([0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12})\b
```

>[!IMPORTANT]
>
>Sie können nur optionale Felder mit Textwerten (ASCII/UTF-8) erfassen. Insbesondere können binäre Felder mit dem aktuellen regex-System nicht zuverlässig erfasst werden.

**SR-Kennung oder Fehlercode in einem Textfeld speichern**

Wenn diese Option aktiviert ist, wird das Feld **Text** während der Verarbeitung des Statustextes des SR beibehalten.

Dies ist nützlich, wenn der Anbieter wichtige Daten wie die ID oder den Status in dieses Feld eingibt. Normalerweise kann dieses Feld sicher verworfen werden, da es Text mit einer Nicht-ASCII-Kodierung enthält und die Regex-Verarbeitung stört.

Wenn Sie diese Option aktivieren, kann es zu einem sehr kleinen Sicherheitsfehler kommen, wenn der `Extraction`-Regex der ID im Feld SR nicht spezifisch genug ist. Der Inhalt des Felds **Text** kann als ID analysiert werden, und ein Angreifer kann es verwenden, um gefälschte IDs einzuschleusen, was zu einer teilweisen Diensteverweigerung führen kann.

**Dienst-ID-Tag**

Ermöglicht das Hinzufügen eines benutzerdefinierten TLV. Dieses Feld legt den Tag-Teil fest. Der Wert kann pro Versand im Wert **Dienst- oder Programm-ID** in den erweiterten Parametern des Versands angepasst werden.

Diese Einstellung erlaubt nur das Hinzufügen einer TLV-Option pro Nachricht.

### Automatische Antwort auf MO      {#automatic-reply}

Mit dieser Funktion können Sie schnell auf MO antworten und per Kurzcode an Blockierungsliste senden.

Die Spalten **Suchbegriff** und **Kurzcode** definieren Bedingungen zum Trigger der automatischen Antwort. Wenn beide Felder übereinstimmen, wird der MO gesendet und die zusätzliche Aktion ausgelöst. Um einen Platzhalter festzulegen, sollten Sie das Feld leer lassen. Suchbegriff wird mit dem ersten alphanumerischen Wort im MO-Text abgeglichen, wobei Interpunktion und vorangestellte Leerzeichen ignoriert werden. Das bedeutet, dass das Feld **Suchbegriff** keine Leerzeichen enthalten darf und ein einziges Wort sein muss.

Die Einstellung **Suchbegriff** ist ein Präfix. Wenn Sie beispielsweise &quot;Anzeige&quot;angeben, stimmt dies mit &quot;Anzeige&quot;, &quot;ADAPT&quot;und &quot;ADOBE&quot;überein. Wenn Sie mehrere Suchbegriffe mit einem gemeinsamen Präfix haben, müssen Sie auf die Reihenfolge achten, da Suchbegriffe von oben nach unten verarbeitet werden.

Die Spalte **Antwort** ist der zu antwortende Text. In diesem Bereich ist keine Personalisierung verfügbar. Wenn Sie dieses Feld leer lassen, wird keine Meldung beantwortet, aber die zusätzliche Aktion wird trotzdem ausgelöst.

Die Spalte **Zusätzliche Aktion** enthält eine zusätzliche Aktion, wenn sowohl **Suchbegriff** als auch **Kurzcode** übereinstimmt, leerer Kurzcode mit allen Kurzcodes übereinstimmt. Sie können den Wert Keine Antworten auf den Text an die Quarantäne senden oder aus der Quarantäne entfernen. Wenn Sie eine **Zusätzliche Aktion** angeben, aber das Feld **Antwort** leer lassen, wird die Aktion ausgeführt, aber es wird keine Antwort gesendet. Quarantäne wird nur für den angegebenen Kurzcode oder alle Kurzcodes angewendet, wenn das Feld leer gelassen wird.

>[!IMPORTANT]
>
>Die Einstellung der vollständigen Telefonnummer senden hat Auswirkungen auf das Verhalten der automatischen Quarantäne der Antwort: Wenn die vollständige Telefonnummer nicht markiert ist, wird der in Quarantäne gestellten Telefonnummer ein Pluszeichen (&quot;+&quot;) vorangestellt, um sie mit dem internationalen Telefonnummernformat kompatibel zu machen.

Alle Einträge in der Tabelle werden in der angegebenen Reihenfolge verarbeitet, bis eine Regel übereinstimmt. Wenn mehrere Regeln mit einem MO übereinstimmen, wird nur die oberste Regel angewendet.

## Parameter für die SMS-Versandvorlage {#sms-delivery-template-parameters}

Einige Parameter können pro Versandvorlage eingestellt werden.

### Von Feld {#from-field}

Dieses Feld ist optional. Es ermöglicht das Überschreiben der Absenderadresse (oADC). Der Inhalt dieses Felds wird im Feld `source_addr` des Felds `SUBMIT_SM PDU` platziert.

Das Feld ist durch die SMPP-Spezifikation auf 21 Zeichen begrenzt, einige Anbieter können jedoch längere Werte zulassen. Beachten Sie auch, dass in einigen Ländern sehr strenge Einschränkungen gelten können, z. B. Länge, Inhalt, zulässige Zeichen.

### Versandparameter {#delivery-parameters}

#### Maximale Anzahl an SMS pro Nachricht {#maximum-sms}

Diese Einstellung funktioniert nur, wenn die Einstellung **Message payload** deaktiviert ist. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/configuring-sms-channel.md). Wenn die Nachricht mehr SMS als diesen Wert erfordert, wird ein Fehler ausgelöst.

Das SMS-Protokoll begrenzt SMS auf 255 Teile, aber einige Mobiltelefone haben Probleme, lange Nachrichten mit mehr als 10 Teilen oder so, die Grenze hängt vom genauen Modell. Wir empfehlen Ihnen, nicht mehr als 5 Teile pro Nachricht zu verwenden.

Aufgrund der Funktionsweise personalisierter Nachrichten in Adobe Campaign kann die Größe der Nachrichten variieren. Eine große Menge an langen Nachrichten könnte die Versandkosten erhöhen.

#### Übermittlungsmodus {#transmission-mode}

Dieses Feld gibt die Art der SMS an, die Sie übertragen möchten: normale oder Flash-Nachrichten, die auf dem Mobilgerät oder der SIM-Karte gespeichert werden.

Diese Einstellung wird im optionalen Feld `dest_addr_subunit` in `SUBMIT_SM PDU` übertragen.

* **&quot;** Nicht angegeben&quot;sendet kein optionales Feld in der PDU.

* **Legt** den Wert 1 fest. Es sendet eine Flash-Nachricht, die auf dem Mobilgerät erscheint und nicht im Speicher gespeichert wird.

* **Legt** den Wert auf 0 fest. Es sendet eine normale Nachricht.

* **Speichern auf** Mobilgeräten setzt den Wert auf 2. Es weist das Telefon an, die SMS im internen Speicher zu speichern.

* **Speichern auf** Terminalsätzen setzt den Wert auf 3. Es weist das Telefon an, die SMS in der SIM-Karte zu speichern.

#### Gültigkeitszeitraum {#validity-period}

Die Gültigkeitsdauer wird im Feld `validity_period` von `SUBMIT_SM PDU` übertragen. Das Datum wird immer als absolutes UTC-Zeitformat formatiert, das Datumsfeld endet mit &quot;00+&quot;.

## SMPP-Anschluss {#ACS-SMPP-connector}

![](assets/do-not-localize/sms_protocol_3.png)

Pfeile stellen den Datenfluss dar.

Das Wichtigste ist, dass es mehrere SMPP-Connector-Threads gibt. Diese Threads sind alle identisch und verwenden dieselbe Konfiguration. Deshalb wird die Anzahl der Verbindungen immer mit der Anzahl der Threads multipliziert.

Die Anzahl der Threads kann vom Kunden nicht geändert werden, da Konfigurationsdateien geändert werden müssen.

### Beschreibung des Verhaltens des SMPP-Connectors {#behavior-smpp-connector}

#### Übereinstimmende Einträge für MT, SR und Broadlog {#matching-mt-sr}

In Adobe Campaign ist eine Nachricht ein Broadlog-Eintrag. In Adobe Campaign Standard müssen externe Connectors nur über die funktionierende Breitband-Tabelle Bescheid wissen: `nmsBroadLogExec`. Ein Workflow ist dafür zuständig, Broadlog-Einträge wieder in ihre jeweiligen Zielgruppendimensionen zu kopieren (nmsBroadLogXXX).

Leider erlaubt SMPP nicht, eine ID zusammen mit einer Nachricht zu senden: der Anbieter gibt jedem MT eine MT-ID und stellt dann eine oder mehrere SR mit derselben ID zur Verfügung.

Die vom Anbieter angegebene ID wird in der Spalte `sProviderId` der Tabelle `nmsBroadLogExec` gespeichert. SR kommt immer dann an, wenn der MT erfolgreich gesendet und bestätigt wurde, kann aber manchmal aus der Reihenfolge kommen, in Adobe Campaign als herausragende SR bekannt. Der Verarbeitungs-Thread speichert diese SR vorübergehend im RAM, bis die vollständigen Informationen eingehen.

Wenn ein MT angegeben wird (`SUBMIT_SM_RESP`), wird `sProviderId` sofort in der Datenbank aktualisiert.

Jeder SR wird einzeln von SMPP-Verarbeitungsthreads verarbeitet. Dieser Prozess ist pseudo-synchron: Es wird von außen als synchron angesehen, aber intern mit Ereignis-basierten Implementierungen implementiert. SR-Regeln werden nur dann anerkannt, wenn die Erweiterung erfolgreich aktualisiert wurde, wenn ein Fehler auftritt, der SR abgelehnt wird.

Im Folgenden finden Sie den Prozess, der auf die einzelnen SR-Regeln angewendet wird:

* Die ID des SR wird mithilfe eines Regex extrahiert.
* Die ID wird unter `nmsBroadLogExec:sProviderId` gesucht.
* Der Status- und Fehlercode werden mithilfe von Regexes aus dem SR extrahiert.
* Der Mechanismus der Breitbandmeldung wird verwendet, um den Fehler zu qualifizieren und die Broadlog-Nachrichten-ID zu finden.
* Die Erweiterung wird mit allen oben genannten Informationen aktualisiert.
* Der SR wird anerkannt.

Wenn Sie die oben genannten Schritte aktivieren, müssen Sie **Ausführliche SMPP-Spuren** aktivieren, um manuell zu überprüfen, ob alle Schritte korrekt angewendet wurden. Dies ist immer dann erforderlich, wenn ein Adobe Campaign mit einem neuen SMPP-Anbieter verbunden ist.

## Vor der Live-Schaltung {#checklist}

Diese Checkliste enthält eine Liste der Dinge, die Sie überprüfen sollten, bevor Sie leben. Eine unvollständige Einrichtung kann zu vielen Problemen führen.

### Suchen nach Externe Konto-Konflikten {#external-account-conflict}

Vergewissern Sie sich, dass Sie keine alten SMS-Externe Konti haben. Wenn Sie das Testkonto deaktiviert lassen, laufen Sie Gefahr, dass es im Produktionssystem erneut aktiviert wird und potenzielle Konflikte entstehen.

Wenn Sie mehrere Konten auf derselben Instanz des Adobe Campaigns haben, die eine Verbindung mit demselben Anbieter herstellen, wenden Sie sich an den Anbieter, um sicherzustellen, dass diese tatsächlich Verbindungen zwischen diesen Konten unterscheiden. Für mehrere Konten mit derselben Anmeldung ist eine zusätzliche Konfiguration erforderlich.

### Ausführliche SMPP-Spuren während der Prüfungen aktivieren {#enable-verbose}

Sie sollten während der Prüfungen immer ausführliche SMPP-Spuren aktivieren.
Auch wenn Sie die Protokolle nicht selbst überprüfen können, ist es einfacher für den Support, Ihnen zu helfen.

### Testen Sie Ihre SMS {#test}

* **SMS mit allen möglichen**
Zeichen sendenWenn Sie SMS mit Nicht-GSM- oder Nicht-ASCII-Zeichen senden möchten, versuchen Sie, einige Nachrichten mit möglichst vielen verschiedenen Zeichen zu senden. Wenn Sie eine benutzerdefinierte Zeichenzuordnungstabelle einrichten, senden Sie mindestens eine SMS für alle möglichen 
`data_coding` Werte.

* **Überprüfen Sie, ob SR korrekt**
verarbeitet werdenDie SMS sollte als empfangen im Versand-Protokoll markiert werden. Das Versand-Protokoll sollte erfolgreich sein und wie folgt aussehen:

Überprüfen Sie, ob Sie den Versand-Provider-Namen geändert haben. Das Versand-Protokoll sollte niemals    `SR yourProvider stat=DELIVRD err=000|#MESSAGE`
Überprüfen Sie, ob Sie den Versand-Provider-Namen geändert haben. Das Versand-Protokoll sollte niemals **SR Generic** auf Produktions-Umgebung enthalten.

* **Vergewissern Sie sich, dass MO**
verarbeitet werdenWenn Sie MO verarbeiten müssen (automatische Antworten, MO-Speicherung in der Datenbank usw.) versuchen, einige Tests durchzuführen. Senden Sie ein paar SMS für alle automatischen Antwort-Keywords und überprüfen Sie, ob die Antwort schnell genug ist, nicht mehr als ein paar Sekunden.
Überprüfen Sie das Protokoll, das das Adobe Campaign mit einem erfolgreichen 
`DELIVER_SM_RESP` (command_status=0).

### PDUs {#check-pdus} überprüfen

Auch wenn Meldungen erfolgreich aussehen, ist es wichtig, zu überprüfen, ob PDUs korrekt formatiert sind.

Dieser Schritt ist erforderlich, wenn eine Verbindung zu einem Provider hergestellt wird, der zuvor nicht mit Adobe Campaign verbunden war.

#### BIND {#bind}

Vergewissern Sie sich, dass `BIND_* PDUs` korrekt gesendet wurde. Das Wichtigste, was überprüft werden muss, ist, dass der Anbieter immer erfolgreich `BIND_*_RESP PDUs` zurückgibt (command_status = 0).

Vergewissern Sie sich, dass nicht zu viele `BIND_* PDU`s vorhanden sind. Wenn es zu viele davon gibt, könnte dies darauf hindeuten, dass die Verbindung instabil ist. Weitere Informationen finden Sie im Abschnitt [Probleme mit instabilen Verbindungen](../../administration/using/sms-protocol.md#issues-unstable-connection).

#### INQUIRE_LINK {#enquire-link-pdus}

Vergewissern Sie sich, dass `ENQUIRE_LINK PDU`s regelmäßig ausgetauscht werden, wenn die Verbindung untätig ist.

#### SUBMIT_SM / DELIVER_SM {#submit-sm-deliver-sm}

Senden Sie eine Nachricht und suchen Sie dann in den Protokollen nach den zugehörigen `SUBMIT_SM`, `SUBMIT_SM_RESP`, `DELIVER_SM` und `DELIVER_SM_RESP PDU`s.

Mit dem `SUBMIT_SM PDU`:

* Überprüfen Sie, ob `data_coding` korrekt ist, standardmäßig 0.
* Überprüfen Sie, ob `short_message` korrekt kodiert ist. Dekodieren Sie es mit einem Hexadezimalkonverter, der mehrere Kodierungen unterstützt.

Mit dem `SUBMIT_SM_RESP PDU`:

* Vergewissern Sie sich, dass sie erfolgreich war, command_status = 0.
* Vergewissern Sie sich, dass der Hauptteil eine ordnungsgemäß formatierte ID und anschließend ein 0-Byte enthält.

Mit dem `DELIVER_SM PDU`:

* Dekodieren Sie das hexadezimale `short_message`-Feld.
* Überprüfen Sie mit einem Regex-Überprüfungstool, ob der in `Extraction` regex der ID im SR definierte Regex genau eine Erfassungsgruppe zurückgibt und ob er die gesamte ID in der Nachricht erfasst.
* Überprüfen Sie, ob die extrahierte ID mit der in `SUBMIT_SM_RESP` übereinstimmt.
* Vergewissern Sie sich, dass der in `Extraction` regex des Status im SR definierte Regex den Inhalt des statischen Felds zurückgibt.
* Überprüfen Sie, ob der in `Extraction` regex des Fehlers im SR definierte Regex den Inhalt des Fehlers zurückgibt.

Mit dem `DELIVER_SM_RESP PDU`:

* Vergewissern Sie sich, dass das `DELIVER_SM PDU` schnell gesendet wurde, in der Regel weniger als 1 Sekunde.
* Vergewissern Sie sich, dass sie erfolgreich war, command_status = 0.

### Fragen Sie den Anbieter, ob alles OK ist.{#provider}

Auch wenn Ihre SMS erfolgreich ist, kontaktieren Sie den Anbieter, um zu sehen, ob alles in Ordnung ist.

### Ungefähre SMPP-Spuren {#disable-verbose} deaktivieren

Sobald alle Prüfungen abgeschlossen sind, ist es das Letzte, **Ausführliche SMPP-Spuren zu deaktivieren, um nicht zu viele Protokolle zu generieren.** Sie können sie für die Fehlerbehebung auch auf Produktionssystemen erneut aktivieren.
