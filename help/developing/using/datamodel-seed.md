---
title: DataModel-Testempfänger
description: Informationen zum Datenmodell
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 9b522c84-e296-47c7-9588-2e5ed08ab631
TQID: https://experienceleague.adobe.com/lfD2ncth570TSScQZE3UiO3ikqqxpjf4CVd7PvuAFXs
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 100%

---

# Testempfänger/in (nms:seedMember)

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
                  <td>country (countries)</td>
                  <td>Country</td>
                  <td>link </td>
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
                  <td>email</td>
                  <td>E-Mail</td>
                  <td>string (128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailRendering</td>
                  <td>E-Mail-Rendering</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>fax</td>
                  <td>Fax</td>
                  <td>string (32)</td>
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
                  <td>lastModified</td>
                  <td>Last modified</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>location</td>
                  <td>Location</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>marketingCloudId</td>
                  <td>Marketing Cloud ID</td>
                  <td>string (256)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobileApp</td>
                  <td>Mobile application</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>Mobile</td>
                  <td>string (32)</td>
                  <td> </td>
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
                  <td>nms_recipient</td>
                  <td>Profile</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>nms_rtEvent</td>
                  <td>Event</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>orgUnit (orgUnitBase)</td>
                  <td>Organizational unit</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>phone</td>
                  <td>Telefon</td>
                  <td>string (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>proof</td>
                  <td>Proof</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotification</td>
                  <td>Push notification</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>registrationToken</td>
                  <td>Registration Token</td>
                  <td>string (256)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sampleData</td>
                  <td>Sample data</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sms</td>
                  <td>Mobile</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink (state)</td>
                  <td>State</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetData</td>
                  <td>Extension</td>
                  <td>Zeichenfolge </td>
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
                  <td>Test profile</td>
                  <td>string (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>trap</td>
                  <td>Trap</td>
                  <td>Boolesch </td>
                  <td> </td>
               </tr>
            </table>

## Filter

Nach Ereignistyp (byEventType)

<table>
        <tr>
        <th>Name</th>
        <th>Typ</th>
        </tr>
        <tr>
        <td>eventType</td>
        <td>Zeichenfolge</td>
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

Nach Verwendung (byUsage)

<table>
        <tr>
        <th>Name</th>
        <th>Typ</th>
        </tr>
        <tr>
        <td>trap</td>
        <td>Boolesch</td>
        </tr>
        <tr>
        <td>emailRendering</td>
        <td>Boolesch</td>
        </tr>
        <tr>
        <td>proof</td>
        <td>Boolesch</td>
        </tr>
    </table>

Testprofil (profile)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>seedMember</td>
    <td>link</td>
    </tr>
</table>
