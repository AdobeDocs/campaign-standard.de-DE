---
title: SMS-Kanal konfigurieren
description: '"Hier erfahren Sie, wie Sie Routing, Kodierung, Formate und erweiterte Eigenschaften für SMS konfigurieren. "'
page-status-flag: never-activated
uuid: 5f13dbd5-9522-4199-8d9a-44c397cb2458
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 356d4d4f-3d5a-468c-bff8-96767cd8fff6
context-tags: extAccountMobile,overview;extAccount,main;delivery,smsContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3325194881662dee94648ae3d5a03b2bdb6b41ba

---


# SMS-Kanal konfigurieren{#configuring-sms-channel}

Für den Versand von SMS-Nachrichten muss mindestens ein externes Konto von einem Administrator im Menü **[!UICONTROL Administration]**>**[!UICONTROL  Kanäle]** > **[!UICONTROL SMS]**>**[!UICONTROL  SMS-Konten]** konfiguriert werden.

Weiterführende Informationen zur Erstellung und Bearbeitung von externen Konten finden Sie im Abschnitt [Externe Konten. ](../../administration/using/external-accounts.md) Der folgende Absatz behandelt die spezifischen Parameter externer Konten, die dem SMS-Versand dienen.

## SMS-Routing definieren {#defining-an-sms-routing}

Standardmäßig enthält die Anwendung das externe Konto **[!UICONTROL SMS-Routing durch SMPP]**. Die Erstellung weiterer Konten kann jedoch von Nutzen sein.

Wenn Sie das SMPP-Protokoll verwenden möchten, können Sie auch ein neues externes Konto erstellen. Weitere Informationen zum SMS-Protokoll und zu den Einstellungen finden Sie in dieser [Technote](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html).

1. Ein neues externes Konto können Sie über **[!UICONTROL Administration > Anwendungskonfiguration > Externe Konten erstellen]**.
1. Definieren Sie den Kontotyp mit **[!UICONTROL Routing]**, den Kanal mit**[!UICONTROL  Mobiltelefon (SMS)]** und den Versandmodus mit **[!UICONTROL Gebündelter Versand]**.

   ![](assets/sms_routing.png)

1. Definieren Sie die Verbindungsparameter.

   Wenden Sie sich zur Konfiguration der für den SMS-Versand spezifischen Verbindungsparameter an Ihren Provider. Dieser kann Ihnen die für das externe Konto erforderlichen Angaben kommunizieren.

   ![](assets/sms_connection.png)

   Die Option **[!UICONTROL TLS über SMPP aktivieren]**ermöglicht die Verschlüsselung des SMPP-Traffics.

   **[!UICONTROL Mithilfe von Ausführliche SMPP-Verfolgung in Logdatei aktivieren]**können Sie den gesamten SMPP-Traffic in Logdateien speichern. Diese Option muss aktiviert sein, um beim Connector eine Fehlerbehebung durchzuführen und ihn mit dem Traffic auf Provider-Seite zu vergleichen.

1. Je nach gewähltem Provider kommuniziert Ihnen dann Adobe den im Feld **[!UICONTROL Name der SMSC-Implementierung]**einzufügenden Wert.
1. Definieren Sie die SMPP-Kanaleinstellungen. Weiterführende Informationen finden Sie im Abschnitt [SMS-Kodierung und -Formate](#sms-encoding-and-formats).

   Aktivieren Sie **[!UICONTROL Eingehende MO in Datenbank speichern]**, wenn alle eingehenden SMS-Nachrichten in der inSMS-Tabelle gespeichert werden sollen. Weiterführende Information zum Abrufen von eingehenden SMS-Nachrichten finden Sie in diesem[Abschnitt](../../channels/using/managing-incoming-sms.md#storing-incoming-sms).

   Mit der Option **[!UICONTROL Echtzeit-KPI-Aktualisierungen während SR-Verarbeitung aktivieren]**können die KPIs**[!UICONTROL  Zugestellt]** oder **[!UICONTROL Bounces + Fehler]**nach dem Versand in Echtzeit aktualisiert werden. Diese KPIs befinden sich im Fenster**[!UICONTROL  Freigabe]** und werden direkt auf Grundlage des vom Provider empfangenen SR (Status Report) neu berechnet.

   ![](assets/sms_connection_1.png)

1. Definieren Sie die Parameter **[!UICONTROL Durchsatz und Ausführungsdauer]**.

   Hier können Sie den maximalen Durchsatz für ausgehende Nachrichten (&quot;MT&quot;, Mobile Terminated) festlegen. Bei Angabe von &quot;0&quot; im entsprechenden Feld ist der Durchsatz unbegrenzt.

   Werte, die eine Dauer angeben, sind in Sekunden auszudrücken.

1. Konfigurieren Sie die Parameter für SMS-C, falls Sie ein spezifisches Kodierungs-Mapping definieren müssen. Weiterführende Informationen hierzu finden Sie im Abschnitt [SMSC-Besonderheiten](#smsc-specifics).

   Aktivieren Sie die Option **[!UICONTROL Vollständige Telefonnummer senden (Zeichen und nicht Ziffern senden)]**, wenn Sie die Konformität mit dem SMPP-Protokoll nicht wahren und das Vorzeichen**[!UICONTROL +]** an den Server des SMS-Anbieters (SMS-C) übertragen möchten.

   Bei gewissen Anbietern ist die Verwendung des Vorzeichens **[!UICONTROL +]**jedoch erforderlich, sodass es ratsam ist, mit Ihrem Anbieter Kontakt aufzunehmen, der Sie bei Bedarf dazu auffordern wird, diese Option zu aktivieren.

1. Definieren Sie bei Bedarf automatische Antworten, um Aktionen auf der Basis des Inhalts einer Antwort auszulösen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/managing-incoming-sms.md#managing-stop-sms).
1. Speichern Sie die Konfiguration des externen SMS-Routing-Kontos.

Jetzt können Sie mithilfe der neuen Routing-Konfiguration in Adobe Campaign SMS-Nachrichten senden.

## SMS-Kodierung und -Formate {#sms-encoding-and-formats}

### Kodierung, Länge und Tansliteration von SMS {#sms-encoding--length-and-transliteration}

Standardmäßig kommt in Bezug auf die maximal zulässige Zeichenanzahl einer SMS der Mobilfunkstandard GSM (Global System for Mobile Communications) zur Anwendung.

SMS, die das GSM-Alphabet verwenden, sind auf 160 Zeichen begrenzt oder auf 153 Zeichen pro SMS bei Nachrichten, die in mehreren Teilen gesendet werden.

>[!NOTE]
>
>Gewisse Zeichen zählen doppelt (Akkoladen, eckige Klammern, Eurozeichen etc.). Eine Liste der von GSM unterstützten Zeichen finden Sie im Abschnitt [Zeichensatztabelle - GSM-Standard](#table-of-characters---gsm-standard).

Bei Bedarf können Sie die Transliteration von Zeichen zulassen, indem Sie die entsprechende Option aktivieren.

![](assets/sms_transliteration.png)

Transliteration bezeichnet in einer SMS die Ersetzung eines Zeichens durch ein anderes, wenn das erste Zeichen nicht von GSM unterstützt wird.

* Wenn die Transliteration **zugelassen** wurde, wird jedes nicht unterstützte Zeichen beim Nachrichtenversand durch ein Zeichen des GSM-Alphabets ersetzt. So wird beispielsweise der Buchstabe &quot;ë&quot; durch &quot;e&quot; ersetzt. Der Nachrichteninhalt wird in diesem Fall leicht verändert übermittelt, aber die Zeichenanzahl bleibt identisch.
* Wenn die Transliteration **nicht zugelassen** wurde, werden alle Nachrichten mit nicht unterstützten Zeichen im Binärformat (Unicode) gesendet: Alle Zeichen werden unverändert übermittelt. In Unicode kodierte SMS sind auf 70 Zeichen (oder 67 Zeichen bei Nachrichten, die in mehreren Teilen gesendet werden) begrenzt. Bei Überschreitung der maximalen Zeichenanzahl werden mehrere Teilnachrichten gesendet, wodurch zusätzliche Kosten entstehen können.

>[!CAUTION]
>
>Die Verwendung von Personalisierungsfeldern im SMS-Inhalt führt u. U. dazu, dass nicht von GSM unterstützte Zeichen eingefügt werden. Im Abschnitt [SMS personalisieren](../../channels/using/personalizing-sms-messages.md) finden Sie ein Beispiel für einen SMS-Inhalt.

Die Transliteration von Zeichen ist standardmäßig deaktiviert. Es wird empfohlen, diese Option nicht zu aktivieren, wenn Sie alle Zeichen Ihrer SMS beibehalten möchten, um beispielsweise Eigennamen unverändert zu übermitteln.

Sollte Ihre SMS jedoch eine hohe Anzahl an Zeichen enthalten, die dem Unicode-Zeichensatz entstammen, können Sie diese Option wählen, um Ihre Versandkosten zu begrenzen.

### Zeichensatztabelle - GSM-Standard {#table-of-characters---gsm-standard}

Der folgende Abschnitt zeigt den vom GSM-Standard unterstützten Zeichensatz. Jedes im Nachrichteninhalt enthaltene Zeichen, das nicht in der unten stehenden Tabelle aufgeführt ist, führt zur Konvertierung der gesamten Nachricht in das Binärformat (Unicode) und zur Splittung der SMS in Teilnachrichten, sobald sie 70 Zeichen überschreitet. Weiterführende Hinweise finden Sie im Abschnitt [Kodierung, Länge und Transliteration von SMS](#sms-encoding--length-and-transliteration).

**Einfache Zeichen**

<table> 
 <tbody> 
  <tr> 
   <td> @<br /> </td> 
   <td> <img height="21px" src="assets/delta.png" /> <br /> </td> 
   <td> SP<br /> </td> 
   <td> 0<br /> </td> 
   <td> ¡<br /> </td> 
   <td> P<br /> </td> 
   <td> ¿<br /> </td> 
   <td> P<br /> </td> 
  </tr> 
  <tr> 
   <td> £<br /> </td> 
   <td> _<br /> </td> 
   <td> !<br /> </td> 
   <td> 1<br /> </td> 
   <td> A<br /> </td> 
   <td> Q<br /> </td> 
   <td> a<br /> </td> 
   <td> q<br /> </td> 
  </tr> 
  <tr> 
   <td> $<br /> </td> 
   <td> <img height="21px" src="assets/phi.png" /> <br /> </td> 
   <td> "<br /> </td> 
   <td> 2<br /> </td> 
   <td> B<br /> </td> 
   <td> R<br /> </td> 
   <td> b<br /> </td> 
   <td> r<br /> </td> 
  </tr> 
  <tr> 
   <td> ¥<br /> </td> 
   <td> <img height="21px" src="assets/gamma.png" /> <br /> </td> 
   <td> #<br /> </td> 
   <td> 3<br /> </td> 
   <td> C<br /> </td> 
   <td> S<br /> </td> 
   <td> c<br /> </td> 
   <td> s<br /> </td> 
  </tr> 
  <tr> 
   <td> è<br /> </td> 
   <td> <img height="21px" src="assets/delta.png" /> <br /> </td> 
   <td> ¤<br /> </td> 
   <td> 4<br /> </td> 
   <td> D<br /> </td> 
   <td> T<br /> </td> 
   <td> d<br /> </td> 
   <td> t<br /> </td> 
  </tr> 
  <tr> 
   <td> é<br /> </td> 
   <td> <img height="21px" src="assets/omega.png" /> <br /> </td> 
   <td> %<br /> </td> 
   <td> 5<br /> </td> 
   <td> E<br /> </td> 
   <td> U<br /> </td> 
   <td> e<br /> </td> 
   <td> u<br /> </td> 
  </tr> 
  <tr> 
   <td> ù<br /> </td> 
   <td> <img height="21px" src="assets/pi.png" /> <br /> </td> 
   <td> &amp;<br /> </td> 
   <td> 6<br /> </td> 
   <td> F<br /> </td> 
   <td> V<br /> </td> 
   <td> f<br /> </td> 
   <td> v<br /> </td> 
  </tr> 
  <tr> 
   <td> ì<br /> </td> 
   <td> <img height="21px" src="assets/psi.png" /> <br /> </td> 
   <td> '<br /> </td> 
   <td> 7<br /> </td> 
   <td> G<br /> </td> 
   <td> W<br /> </td> 
   <td> g<br /> </td> 
   <td> w<br /> </td> 
  </tr> 
  <tr> 
   <td> ò<br /> </td> 
   <td> <img height="21px" src="assets/sigma.png" /> <br /> </td> 
   <td> (<br /> </td> 
   <td> 8<br /> </td> 
   <td> H<br /> </td> 
   <td> X<br /> </td> 
   <td> h<br /> </td> 
   <td> x<br /> </td> 
  </tr> 
  <tr> 
   <td> Ç<br /> </td> 
   <td> <img height="21px" src="assets/theta.png" /> <br /> </td> 
   <td> )<br /> </td> 
   <td> 9 </td> 
   <td> I<br /> </td> 
   <td> Y<br /> </td> 
   <td> i<br /> </td> 
   <td> y<br /> </td> 
  </tr> 
  <tr> 
   <td> LF<br /> </td> 
   <td> <img height="21px" src="assets/xi.png" /> <br /> </td> 
   <td> *<br /> </td> 
   <td> :<br /> </td> 
   <td> J<br /> </td> 
   <td> Z<br /> </td> 
   <td> j<br /> </td> 
   <td> z<br /> </td> 
  </tr> 
  <tr> 
   <td> Ø<br /> </td> 
   <td> ESC<br /> </td> 
   <td> +<br /> </td> 
   <td> ;<br /> </td> 
   <td> K<br /> </td> 
   <td> Ä<br /> </td> 
   <td> k<br /> </td> 
   <td> ä<br /> </td> 
  </tr> 
  <tr> 
   <td> ø<br /> </td> 
   <td> Æ<br /> </td> 
   <td> ,<br /> </td> 
   <td> &lt;<br /> </td> 
   <td> L<br /> </td> 
   <td> Ö<br /> </td> 
   <td> l<br /> </td> 
   <td> ö<br /> </td> 
  </tr> 
  <tr> 
   <td> CR<br /> </td> 
   <td> æ<br /> </td> 
   <td> -<br /> </td> 
   <td> = </td> 
   <td> M<br /> </td> 
   <td> Ñ<br /> </td> 
   <td> m<br /> </td> 
   <td> ñ<br /> </td> 
  </tr> 
  <tr> 
   <td> Å<br /> </td> 
   <td> ß<br /> </td> 
   <td> .<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> N<br /> </td> 
   <td> Ü<br /> </td> 
   <td> n<br /> </td> 
   <td> ü<br /> </td> 
  </tr> 
  <tr> 
   <td> å<br /> </td> 
   <td> É<br /> </td> 
   <td> /<br /> </td> 
   <td> ?<br /> </td> 
   <td> O<br /> </td> 
   <td> §<br /> </td> 
   <td> o<br /> </td> 
   <td> à<br /> </td> 
  </tr> 
 </tbody> 
</table>

SP: Leerzeichen

ESC: Escape

LF: Zeilenvorschub

CR: Wagenrücklauf

**Doppelt zählende Zeichen**

^ { } [ ~ ] | €

### SMSC-Besonderheiten {#smsc-specifics}

>[!NOTE]
>
>Mithilfe dieser Optionen kann der Connector so angepasst werden, dass nicht standardmäßige (d. h. von der SMPP 3.4-Spezifikation abweichende) SMSC oder spezifische Kodierungsanforderungen unterstützt werden. Konfigurationen dieser Art sollten jedoch nur von erfahrenen Benutzern vorgenommen werden.

Beim SMS-Versand kann Adobe Campaign eine oder mehrere Textkodierungen verwenden. Je nach Kodierung kommen unterschiedliche Zeichensätze zur Anwendung und variiert die Anzahl an zulässigen Zeichen pro SMS.

Das Feld **[!UICONTROL DATA_CODING]**dient in Adobe Campaign dazu, dem SMSC zu signalisieren, welche Kodierung verwendet wird.

>[!NOTE]
>
>Die Entsprechung zwischen dem Wert des **DATA_CODING**-Felds und der tatsächlich verwendeten Kodierung ist standardisiert. Gewisse SMSC besitzen jedoch eine spezifische Entsprechung. In diesem Fall muss Ihr **Adobe-Campaign**-Administrator diese deklarieren. Kontaktieren Sie für weiterführende Informationen Ihren Anbieter.

Die Option **[!UICONTROL Spezifisches Kodierungs-Mapping definieren]**erlaubt die** DATA_CODING **-Deklarierung. Durch Angabe von nur einer Kodierung in der Tabelle wird die Anwendung dieser Kodierung erzwungen.

**Konfiguration**

* Wenn die Option **[!UICONTROL Spezifisches Kodierungs-Mapping definieren]**nicht aktiviert wurde, zeigt der Connector ein Standardverhalten:

   * Er versucht, das GSM-Alphabet zu verwenden und ordnet diesem den Wert **DATA_CODING = 0** zu.
   * Falls die Verwendung des GSM-Alphabets nicht möglich ist, verwendet er **UCS2** und ordnet den Wert **DATA_CODING = 8** zu.
   ![](assets/sms_data_coding.png)

* Wenn die Option **[!UICONTROL Spezifisches Kodierungs-Mapping definieren]**aktiviert wurde, haben Sie die Möglichkeit, die Kodierungen zu definieren, die Sie verwenden möchten, und ihnen im Feld**[!UICONTROL  DATA_CODING]** die entsprechenden Werte zuzuordnen. Adobe Campaign verwendet die Kodierungen in der Reihenfolge ihres Erscheinens in der Liste. Wenn die Verwendung der ersten Kodierung nicht möglich ist, wird die zweite verwendet usw.

   Die Reihenfolge der Deklarierung ist entscheidend. Wir empfehlen Ihnen, die Liste aufsteigend nach den entstehenden **Kosten** zu ordnen, um die Kodierungen zu favorisieren, die eine größere Anzahl von Zeichen pro SMS erlauben.

   Deklarieren Sie nur die Kodierungen, die Sie tatsächlich verwenden möchten. Deklarieren Sie hingegen keine vom SMSC angebotenen Kodierungen in der Liste, die nicht Ihrer Verwendung entsprechen.

   ![](assets/sms_data_coding1.png)

### Automatische Antwort auf MO {#automatic-reply-sent-to-the-mo}

Sie können einem Profil, das auf eine per Campaign gesendete SMS-Nachricht antwortet, eine automatische Nachricht sowie die auszuführende Aktion zurücksenden.

Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/managing-incoming-sms.md).

## SMS-Eigenschaften konfigurieren {#configuring-sms-properties}

Dieser Abschnitt behandelt die Liste von SMS-spezifischen Parametern in den Eigenschaften eines SMS-Versands bzw. einer SMS-Versandvorlage.

Die SMS-spezifischen Versandparameter befinden sich im Abschnitt **[!UICONTROL Senden]**und**[!UICONTROL  Erweiterte Parameter]**.

![](assets/sms_options.png)

* Die Option **[!UICONTROL Von]**erlaubt die Eingabe einer Zeichenkette zur Personalisierung des SMS-Absenders. Es ist der hier eingegebene Name, der auf dem Mobiltelefon des Empfängers als Absender erscheint.

   Bleibt das entsprechende Feld leer, wird die im externen Konto angegebene Anrufernummer verwendet. Sollte auch dort keine Anrufernummer gespeichert sein, wird die Kurzwahlnummer verwendet. The external account specific to SMS delivery is presented in the [Defining an SMS routing](#defining-an-sms-routing) section.

   ![](assets/sms_smpp.png)

   >[!CAUTION]
   >
   >Überprüfen Sie bezüglich der Änderung des Absenders die gültige Rechtslage Ihres Landes. Stellen Sie außerdem sicher, dass Ihr SMS-Provider diese Funktionalität anbietet.

* Die Option **[!UICONTROL Maximale Anzahl an SMS pro Nachricht]**bietet die Möglichkeit, die Anzahl an höchstens zu verwendenden Teilnachrichten (SMS) für eine Nachricht festzulegen. Sollte eine Nachricht diese Anzahl überschreiten, wird sie nicht gesendet.

   >[!CAUTION]
   >
   >Die Verwendung von Personalisierungsfeldern oder bedingtem Text im SMS-Inhalt kann dazu führen, dass die Nachrichtenlänge und somit die Anzahl erforderlicher SMS für die jeweiligen Empfänger variieren. Lesen Sie diesbezüglich auch den Abschnitt [SMS personalisieren](../../channels/using/personalizing-sms-messages.md).

* Im Feld **[!UICONTROL Übermittlungsmodus]**können Sie festlegen, wie die SMS auf dem Mobiltelefon des Empfängers verarbeitet werden:

   * **[!UICONTROL Speicherung auf der SIM-Karte]**: Die Nachricht wird auf der SIM-Karte des Empfängergeräts gespeichert.
   * **[!UICONTROL Speicherung im internen Speicher]**: Die Nachricht wird im internen Speicher des Empfängergeräts gespeichert.
   * **[!UICONTROL Flash]**: Die Nachricht wird auf dem Bildschirm des Empfängergeräts als Benachrichtigung angezeigt und verschwindet, ohne gespeichert zu werden.

