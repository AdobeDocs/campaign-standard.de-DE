---
solution: Campaign Standard
product: campaign
title: DataModel
description: Informationen zum Datenmodell
audience: developing
content-type: reference
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 100%

---


# Abonnementereignis (nms:rtEvent)

## Objektbeschreibung

<table>
    <tr>
        <th>Name</th>
        <th>Titel</th>
        <th>Typ (Länge)</th>
        <th>Auflistungswerte</th>
    </tr>
    <tr>
        <td>PKey</td>
        <td>Main resource ID</td>
        <td>string </td>
        <td> </td>
    </tr>
    <tr>
        <td>ctx</td>
        <td>Event context</td>
        <td>item </td>
        <td> </td>
    </tr>
    <tr>
        <td>email</td>
        <td>Email</td>
        <td>string (128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>emailFormat</td>
        <td>Email format</td>
        <td>enumeration (byte) </td>
        <td>
            <ul>
            <li>Text - text - 1</li>
            <li>HTML - html - 2</li>
            <li>INVALID VALUE - __Invalid_value__ - __Invalid_value__</li>
            <li>Unknown - unknown - 0</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>eventHistoId</td>
        <td>Archived event ID</td>
        <td>integer </td>
        <td> </td>
    </tr>
    <tr>
        <td>mobilePhone</td>
        <td>Mobile number</td>
        <td>string (32)</td>
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

Nach E-Mail (byEmail)

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

Nach Status oder Typ (byStatusOrType)

<table>
        <tr>
        <th>Name</th>
        <th>Typ</th>
        </tr>
        <tr>
        <td>status</td>
        <td>enumeration</td>
        </tr>
        <tr>
        <td>type</td>
        <td>string</td>
        </tr>
    </table>