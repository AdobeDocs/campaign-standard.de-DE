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
source-git-commit: c7e83d7d5130ce93b880e4835e634dad03504ebb

---


# Saatgutmitglied (nms:seedMember)

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
                  <td>Land (Länder)</td>
                  <td>Land</td>
                  <td>link </td>
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
                  <td>email</td>
                  <td>E-Mail</td>
                  <td>Zeichenfolge (128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>emailRendering</td>
                  <td>E-Mail-Rendering</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>fax</td>
                  <td>Fax</td>
                  <td>Zeichenfolge (32)</td>
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
                  <td>lastModified</td>
                  <td>Letzte Änderung</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>location</td>
                  <td>Standort</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>marketingCloudId</td>
                  <td>ID für Marketing Cloud</td>
                  <td>Zeichenfolge (256)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobileApp</td>
                  <td>Mobile App</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>Mobil</td>
                  <td>Zeichenfolge (32)</td>
                  <td> </td>
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
                  <td>nms_empfänger</td>
                  <td>Profil</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>nms_rtEvent</td>
                  <td>Ereignis</td>
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
                  <td>phone</td>
                  <td>Telefon</td>
                  <td>Zeichenfolge (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>proof</td>
                  <td>Testversand</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>pushNotification</td>
                  <td>Push-Benachrichtigung</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>registrationToken</td>
                  <td>Anmeldetoken</td>
                  <td>Zeichenfolge (256)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sampleData</td>
                  <td>Beispieldaten</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>sms</td>
                  <td>Mobil</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink (state)</td>
                  <td>Bundesland/Kanton</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetData</td>
                  <td>Extension</td>
                  <td>string </td>
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
                  <td>Testprofil</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Falle</td>
                  <td>Falle</td>
                  <td>boolean </td>
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
        <td>string</td>
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

Nach Verwendung (nach Verwendung)

<table>
        <tr>
        <th>Name</th>
        <th>Typ</th>
        </tr>
        <tr>
        <td>Falle</td>
        <td>boolean</td>
        </tr>
        <tr>
        <td>emailRendering</td>
        <td>boolean</td>
        </tr>
        <tr>
        <td>proof</td>
        <td>boolean</td>
        </tr>
    </table>

Testprofil (Profil)

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