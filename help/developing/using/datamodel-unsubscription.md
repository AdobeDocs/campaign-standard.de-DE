---
title: DataModel-Abmeldeereignis
description: Informationen zum Datenmodell
audience: developing
content-type: reference
feature: Data Model
role: Developer
level: Experienced
exl-id: 508361d1-6a0b-4476-a058-4162fb3e8d5e
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 100%

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
                  <td>PKey</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>ctx</td>
                  <td>False</td>
                  <td>item</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>email</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>emailFormat</td>
                  <td>False</td>
                  <td>enumeration</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>mobilePhone</td>
                  <td>False</td>
                  <td>string</td>
                  <td>False</td>
               </tr>
               <tr>
                  <td>serverUrl</td>
                  <td>True</td>
                  <td>string</td>
                  <td>False</td>
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
        <td>status</td>
        <td>enumeration</td>
        </tr>
        <tr>
        <td>type</td>
        <td>string</td>
        </tr>
    </table>
