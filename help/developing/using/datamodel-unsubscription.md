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


# Abmeldeereignis (nms:rtEvent)

## Objektbeschreibung

<table>
               <tr>
                  <th>Name</th>
                  <th>Schreibgeschützt</th>
                  <th>Typ</th>
                  <th>Erforderlich</th>
               </tr>
               <tr>
                  <td>Primärschlüssel</td>
                  <td>Falsch</td>
                  <td>string</td>
                  <td>Falsch</td>
               </tr>
               <tr>
                  <td>ctx</td>
                  <td>Falsch</td>
                  <td>item</td>
                  <td>Falsch</td>
               </tr>
               <tr>
                  <td>email</td>
                  <td>Falsch</td>
                  <td>string</td>
                  <td>Falsch</td>
               </tr>
               <tr>
                  <td>emailFormat</td>
                  <td>Falsch</td>
                  <td>enumeration</td>
                  <td>Falsch</td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>Falsch</td>
                  <td>string</td>
                  <td>Falsch</td>
               </tr>
               <tr>
                  <td>serverUrl</td>
                  <td>Wahr</td>
                  <td>string</td>
                  <td>Falsch</td>
               </tr>
            </table>

## Filter

byEmail

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

byStatusOrType

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