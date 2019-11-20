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


# Abonnementereignis (nms:rtEvent)

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
        <td>ctx</td>
        <td>Ereigniskontext</td>
        <td>item </td>
        <td> </td>
    </tr>
    <tr>
        <td>email</td>
        <td>E-Mail</td>
        <td>Zeichenfolge (128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>emailFormat</td>
        <td>Email-Format</td>
        <td>Aufzählung (Byte) </td>
        <td>
            <ul>
            <li>Text - Text - 1</li>
            <li>HTML - html - 2</li>
            <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
            <li>unbekannt - unbekannt - 0</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>eventHistoId</td>
        <td>Archivierte Ereignis-ID</td>
        <td>integer </td>
        <td> </td>
    </tr>
    <tr>
        <td>mobilePhone</td>
        <td>Mobilnummer</td>
        <td>Zeichenfolge (32)</td>
        <td> </td>
    </tr>
    <tr>
        <td>serverUrl</td>
        <td>ServerUrl</td>
        <td>string </td>
        <td> </td>
    </tr>
</table>

## Filter

per E-Mail (per E-Mail)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>email</td>
    <td>string</td>
    </tr>
</table>

Nach Status oder Typ (nach StatusOrType)

<table>
        <tr>
        <th>Name</th>
        <th>Typ</th>
        </tr>
        <tr>
        <td>Status</td>
        <td>enumeration</td>
        </tr>
        <tr>
        <td>Typ</td>
        <td>string</td>
        </tr>
    </table>