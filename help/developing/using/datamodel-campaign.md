---
title: DataModel Campaign
description: Informationen zum Datenmodell
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: a63fe730-a6b2-4ae0-93da-9f8ee7824c9f
TQID: https://experienceleague.adobe.com/ialeaJzsFmhu1if-CTJfg9xLwq6jjA4aA0eXnOT-oyo
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 100%

---

# Kampagne (nms:campaign)

## Objektbeschreibung

<table>
               <tr>
                  <th>Name</th>
                  <th>Titel</th>
                  <th>Typ (Länge)</th>
                  <th>Aufzählungswerte</th>
               </tr>
               <tr>
                  <td>PKey</td>
                  <td>Main resource ID</td>
                  <td>Zeichenfolge </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>activities</td>
                  <td>Activities</td>
                  <td>collection </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>builtIn</td>
                  <td>Built-in application object</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Erstellt</td>
                  <td>Erstellt</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>createdBy (userBase)</td>
                  <td>Created by</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>desc</td>
                  <td>Beschreibung</td>
                  <td>string (512)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>duration</td>
                  <td>Campaign duration</td>
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
                  <td>Geographical unit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isExternal</td>
                  <td>Is external resource</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>isTemplate</td>
                  <td>Template</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>label</td>
                  <td>Titel</td>
                  <td>string (128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>lastModified</td>
                  <td>Last modified</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>logicalStatus</td>
                  <td>Execution status</td>
                  <td>enumeration (string) (255)</td>
                  <td>
                     <ul>
                        <li>In progress - started - started</li>
                        <li>Editing - edition - edition</li>
                        <li>Finished - finished - finished</li>
                        <li>Warning - warning - warning</li>
                        <li>Erroneous - error - error</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>modifiedBy (userBase)</td>
                  <td>Modified by</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>name</td>
                  <td>ID</td>
                  <td>string (64)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit (orgUnitBase)</td>
                  <td>Organizational unit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>program (programBase)</td>
                  <td>Program</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>realtimeReport</td>
                  <td>Realtime Reports</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>start</td>
                  <td>Startdatum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>status</td>
                  <td>Status</td>
                  <td>enumeration (byte) </td>
                  <td>
                     <ul>
                        <li>Started - started - 1</li>
                        <li>Editing - edition - 0</li>
                        <li>Finished - finished - 2</li>
                        <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>template (campaign)</td>
                  <td>Campaign template</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>thumbnail</td>
                  <td>Thumbnail</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>Kampagne</td>
                  <td>string (255)</td>
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
    <td>state</td>
    <td>enumeration</td>
    </tr>
</table>

Nach Name oder Titel (byText)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>text</td>
    <td>Zeichenfolge</td>
    </tr>
</table>

Nach Zeiträumen (byPeriod)

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
    <td>Zeichenfolge</td>
    </tr>
</table>

Nach Status (byState)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>state</td>
    <td>enumeration</td>
    </tr>
</table>

Kontinuierliche Sendungen aus einer heterogenen Liste einschließen (withContinuous)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>withContinuous</td>
    <td>Boolesch</td>
    </tr>
</table>

Für den angegebenen Zeitraum geplant (byPlanning)

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

Im gegebenen Zeitraum präsent (byCalendar)

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
