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
source-git-commit: 8f47bf0cc1d5f694df1e1829ccd03c72df28d7de

---


# Kampagne (nms:campaign)

## Objektbeschreibung

<table>
               <tr>
                  <th>Name</th>
                  <th>Titel</th>
                  <th>Typ (Länge)</th>
                  <th>Enumeration-Werte</th>
               </tr>
               <tr>
                  <td>Primärschlüssel</td>
                  <td>Wichtigste Ressourcen-ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Aktivitäten</td>
                  <td>Aktivitäten</td>
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
                  <td>desc</td>
                  <td>Beschreibung</td>
                  <td>Zeichenfolge (512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Dauer</td>
                  <td>Kampagnendauer</td>
                  <td>number </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>end</td>
                  <td>Enddatum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>geoUnit (geoUnitBase)</td>
                  <td>Geografische Einheit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>Ist erweiterungsfähige externe Ressource</td>
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
                  <td>orgUnit (orgUnitBase)</td>
                  <td>Organisationseinheit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>programme (programmeBase)</td>
                  <td>Programm</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>Echtzeitberichte</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>start</td>
                  <td>Anfangsdatum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Status</td>
                  <td>Status</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Gestartet - gestartet - 1</li>
                        <li>Bearbeitung - Ausgabe - 0</li>
                        <li>Fertig - Fertig - 2</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>template (campaign)</td>
                  <td>Kampagnenvorlage</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Miniaturansicht</td>
                  <td>Miniaturansicht</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>Kampagne</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
            </table>

## Filter

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
</table>

Nach Zeitraum (nach Zeitraum)

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

Für den jeweiligen Zeitraum geplant (nach Planung)

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