---
title: DataModel
description: Informationen zum Datenmodell
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 13ad7e616b51ae0fa0804db02f15120a636b7603

---


# Auslieferung (nms:delivery)

## Objektbeschreibung

<table>
               <tr>
                  <th>Name</th>
                  <th>Titel</th>
                  <th>Typ (Länge)</th>
                  <th>Enumeration-Werte</th>
               </tr>
               <tr>
                  <td>FCP</td>
                  <td>Testversand</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Primärschlüssel</td>
                  <td>Wichtigste Ressourcen-ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>abTesting</td>
                  <td>A/B-Test</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advanced</td>
                  <td>Erweiterte Bereitstellung</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>advancedParameters</td>
                  <td>Erweiterte Parameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>aemContents</td>
                  <td>Adobe Experience Manager-Inhalte</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMessage</td>
                  <td>Warnmeldung</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>alertMode</td>
                  <td>Warentyp</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Anlage</td>
                  <td>Angehängte Dateien</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Branding (brandingBase)</td>
                  <td>Marke</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>wideLogs</td>
                  <td>Versandlogs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>buildIn</td>
                  <td>Integriertes Anwendungsobjekt</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>campaign (campaignBase)</td>
                  <td>Kampagne</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cmsAccount (extAccountAEMBase)</td>
                  <td>Adobe Experience Manager-Konto</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Befehle</td>
                  <td>Befehle</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>content</td>
                  <td>Inhalt</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>contentSource</td>
                  <td>Inhaltsquelle</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Adobe Experience Manager - aem - 1</li>
                        <li>Adobe Campaign - campaign - 0</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>contextResourceType</td>
                  <td>Ressourcentyp</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>created</td>
                  <td>Erstellt</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy (userBase)</td>
                  <td>Erstellt von</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>deliveryMode</td>
                  <td>Auslieferungsmodus</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Massengut - Lieferung - 1</li>
                        <li>Mid-Sourcing - midSourcing - 4</li>
                        <li>Beschreibung - beschreibend - 2</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                        <li>Extern - extern - 0</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>deliveryProvider (extAccountBase)</td>
                  <td>Routing</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>desc</td>
                  <td>Beschreibung</td>
                  <td>Zeichenfolge (512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailPreview</td>
                  <td>E-Mail-Vorschau</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>Ausschlusslogs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Ausnahmen</td>
                  <td>Ausschlussgründe</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Ausführung</td>
                  <td>Ausführungsparameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>executeType</td>
                  <td>Ausführungstyp</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Eindeutig - einmalig - 0</li>
                        <li>Fortlaufend - kontinuierlich - 1</li>
                        <li>Nachrichtencenter - messageCenter - 2</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>foreLogs</td>
                  <td>ForecastLog</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit (geoUnitBase)</td>
                  <td>Geografische Einheit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>hasAttachments</td>
                  <td>Anhängen von Dateien</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>icon</td>
                  <td>Symbol</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Transaktionsemail - E-Mail-Blitz - 60</li>
                        <li>Fax - 4</li>
                        <li>Mobil (SMS) - sms - 1</li>
                        <li>Wiederkehrende E-Mail - E-Mail-Aktualisierung - 30</li>
                        <li>Direktwerbung - Papier - 3</li>
                        <li>Telefon - Telefon - 2</li>
                        <li>Sonstige - sonstige - 120</li>
                        <li>Wiederkehrende SMS - smsRefresh - 31</li>
                        <li>Mobilanwendung - pushNotification - 40</li>
                        <li>Transactional SMS - smsLightning - 61</li>
                        <li>E-Mail - E-Mail - 0</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>Ist erweiterungsfähige externe Ressource</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isMaster</td>
                  <td>Master</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isTemplate</td>
                  <td>Vorlage</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Iterationen</td>
                  <td>Sendungen</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>job</td>
                  <td>Vorgang</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>jobLogs</td>
                  <td>Logs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>kpis</td>
                  <td>Indikatoren</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Titel</td>
                  <td>Titel</td>
                  <td>Zeichenfolge (128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastModified</td>
                  <td>Letzte Änderung</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>logicalStatus</td>
                  <td>Ausführungsstatus</td>
                  <td>Enumeration (Zeichenfolge) (255)</td>
                  <td>
                     <ul>
                        <li>In Verarbeitung - begonnen</li>
                        <li>Bearbeitung - Ausgabe - Ausgabe</li>
                        <li>Fertig - fertig - fertig</li>
                        <li>Warnung - Warnung - Warnung</li>
                        <li>Fehler - Fehler - Fehler</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>mailParameters</td>
                  <td>Email-Header-Parameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mainDate</td>
                  <td>Datum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mapping (deliveryMapping)</td>
                  <td>Zielgruppen-Mapping</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>master (deliveryBase)</td>
                  <td>Masterinstanz</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>masterKpis</td>
                  <td>Hauptindikatoren</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>messageType</td>
                  <td>Kanal</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Fax - 4</li>
                        <li>Mobil (SMS) - sms - 1</li>
                        <li>E-Mail - E-Mail - 0</li>
                        <li>Telefon - Telefon - 2</li>
                        <li>Direktwerbung - Papier - 3</li>
                        <li>Mobilanwendung - pushNotification - 40</li>
                        <li>Sonstige - sonstige - 120</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>modifyBy (userBase)</td>
                  <td>Geändert von</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Name</td>
                  <td>Kennung</td>
                  <td>Zeichenfolge (64)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>offerManagement</td>
                  <td>Angebotsverwaltung</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit (orgUnitBase)</td>
                  <td>Organisationseinheit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>parent (deliveryBase)</td>
                  <td>Elternversand</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Priorität</td>
                  <td>Versandpriorität</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Hoch - Hoch - 20</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                        <li>Normal - normal - 10</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>programme (programmeBase)</td>
                  <td>Programm</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Proofs</td>
                  <td>Testsendungen</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotificationPreview</td>
                  <td>Vorschau auf Push-Benachrichtigung</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushnotificationParameters</td>
                  <td>Parameter der Push-Benachrichtigung</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>Echtzeitberichte</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>resourceVersion</td>
                  <td>Ressourcenversion</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>bandMessage</td>
                  <td>Multifunktionsmeldung</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Szenario</td>
                  <td>Bereitstellungsvorlagenparameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Planung</td>
                  <td>Versandplanung</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsParameters</td>
                  <td>SMS-Parameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>smsPreview</td>
                  <td>SMS-Vorschau</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Status</td>
                  <td>Status</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Start ausstehend - startPending - 51</li>
                        <li>Bereitschaftsbereit - fertig - 45</li>
                        <li>Ausstehend wiederholen - erneut versuchenAusstehend - 61</li>
                        <li>Wiederholung ausgeführt - erneut versuchenInProgress - 62</li>
                        <li>Fehlgeschlagen - fehlgeschlagen - 87</li>
                        <li>In Verarbeitung - begonnen - 55</li>
                        <li>Targeting ausstehend - targetPrepPending - 11</li>
                        <li>Personalisierung ausstehend - messagePrepPending - 21</li>
                        <li>Angehalten - angehalten - 75</li>
                        <li>Bearbeitung - Ausgabe - 0</li>
                        <li>Fertig gestellt - fertig - 95</li>
                        <li>Laufende Zählung - targetSelection - 12</li>
                        <li>Nachricht abgeschlossen - messageReady - 25</li>
                        <li>Personalisierung oder Anzahl fehlgeschlagen - Vorbereitungsfehler - 37</li>
                        <li>Gestoppt - annulliert - 85</li>
                        <li>Personalisierung läuft - messageVorbereitung - 22</li>
                        <li>Target ready - targetReady - 15</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                        <li>Laufende Schiedsverfahren - targetArbitration - 13</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>Ziele</td>
                  <td>Zielgruppe des Versands</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>template (deliveryTemplateSummary)</td>
                  <td>Bereitstellungsvorlage</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Miniaturansicht</td>
                  <td>Miniaturansicht der Auslieferung</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>Versand</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>tracking</td>
                  <td>Tracking-Parameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingLogs</td>
                  <td>Trackinglogs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trackingUrls</td>
                  <td>Getrackte URLs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>triggerMessage</td>
                  <td>Transaktionsnachrichtenparameter</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>typology (typologyBase)</td>
                  <td>Typologien</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflow (workflowBase)</td>
                  <td>Targeting-Arbeitsablauf</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>workflowStatus</td>
                  <td>Workflow-Status</td>
                  <td>Enumeration (Zeichenfolge) (255)</td>
                  <td>
                     <ul>
                        <li>In Verarbeitung - begonnen</li>
                        <li>Bearbeitung - Ausgabe - Ausgabe</li>
                        <li>Fertig - fertig - fertig</li>
                        <li>Warnung - Warnung - Warnung</li>
                        <li>Fehler - Fehler - Fehler</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
            </table>

## Filter

Nach Kanaltyp (nach Kanal)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>channel</td>
    <td>enumeration</td>
    </tr>
</table>

Nach Ausführungsart (von ExecutionType)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>executeType</td>
    <td>enumeration</td>
    </tr>
</table>

Nach logischem Status (byLogicalStatus)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>Status</td>
    <td>enumeration</td>
    </tr>
</table>

Nach Name oder Bezeichnung (nach Text)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>text</td>
    <td>string</td>
    </tr>
    <tr>
    <td>mc</td>
    <td>string</td>
    </tr>
</table>

Nach Zeitraum (nach Zeitraum)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>timePeriod</td>
    <td>string</td>
    </tr>
</table>

Nach Zeitraum (nach Startzeitraum)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>timePeriod</td>
    <td>string</td>
    </tr>
</table>

Nach Veröffentlichungsstatus (nach Veröffentlichungsstatus)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>pStatus</td>
    <td>enumeration</td>
    </tr>
</table>

Nach Status (nach Staat)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>Status</td>
    <td>enumeration</td>
    </tr>
</table>

Follow-up-Meldungen (showFollowup)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>Follow</td>
    <td>boolean</td>
    </tr>
</table>

Erweiterte Auslieferungen einschließen (mit Advanced)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>advanced</td>
    <td>boolean</td>
    </tr>
</table>

Einschließlich kontinuierlicher Auslieferungen aus einer heterogenen Liste (mit "Fortlaufend")

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>withContinuous</td>
    <td>boolean</td>
    </tr>
</table>

Proofs einschließen (mit FCP)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>withFCP</td>
    <td>boolean</td>
    </tr>
</table>

Geplant für den jeweiligen Zeitraum (nach Planung)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>date</td>
    </tr>
</table>

Vorhanden während des angegebenen Zeitraums (nach Kalender)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>startDate</td>
    <td>date</td>
    </tr>
    <tr>
    <td>endDate</td>
    <td>date</td>
    </tr>
</table>

Vordefinierte Anzeige anzeigen (showOob)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>oob</td>
    <td>boolean</td>
    </tr>
</table>