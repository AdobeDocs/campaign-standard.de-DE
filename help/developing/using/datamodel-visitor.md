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
source-git-commit: 6263623a5a8999c475255709a7d0150437e68c0b

---


# Besucher (nms:visitor)

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
        <td>comment</td>
        <td>Referrer-Kommentar</td>
        <td>Zeichenfolge (255)</td>
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
        <td>Lieferung (Lieferung)</td>
        <td>Versand</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>deliveryId</td>
        <td>ID der letzten Auslieferung</td>
        <td>integer </td>
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
        <td>externalId</td>
        <td>Externe Kennung</td>
        <td>Zeichenfolge (64)</td>
        <td> </td>
    </tr>
    <tr>
        <td>firstName</td>
        <td>Vorname</td>
        <td>Zeichenfolge (30)</td>
        <td> </td>
    </tr>
    <tr>
        <td>forwardUrl</td>
        <td>Weiterleitungs-URL</td>
        <td>Zeichenfolge (255)</td>
        <td> </td>
    </tr>
    <tr>
        <td>geoUnit (geoUnitBase)</td>
        <td>Geografische Einheit</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>lastModified</td>
        <td>Letzte Änderung</td>
        <td>date </td>
        <td> </td>
    </tr>
    <tr>
        <td>lastName</td>
        <td>Nachname</td>
        <td>Zeichenfolge (50)</td>
        <td> </td>
    </tr>
    <tr>
        <td>modifyBy (userBase)</td>
        <td>Geändert von</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>orgUnit (orgUnitBase)</td>
        <td>Organisationseinheit</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>Herkunft</td>
        <td>Ursprung</td>
        <td>Aufzählung (Byte) </td>
        <td>
            <ul>
            <li>Nicht definiert - nicht definiert - 0</li>
            <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Empfänger (Empfänger)</td>
        <td>Identifiziertes Profil</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>empfängerId</td>
        <td>Profilkennung</td>
        <td>integer </td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerEmail</td>
        <td>Verweisende E-Mail</td>
        <td>Zeichenfolge (128)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerFirstName</td>
        <td>Vorname der verweisenden Stelle</td>
        <td>Zeichenfolge (30)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerId</td>
        <td>Referrer-ID</td>
        <td>integer </td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerLastName</td>
        <td>Nachname der verweisenden Stelle</td>
        <td>Zeichenfolge (50)</td>
        <td> </td>
    </tr>
    <tr>
        <td>referrerRcp (Empfänger)</td>
        <td>Referrer</td>
        <td>link </td>
        <td> </td>
    </tr>
    <tr>
        <td>title</td>
        <td>Titel</td>
        <td>Zeichenfolge (255)</td>
        <td> </td>
    </tr>
</table>

## Filter

Nachname, Vorname oder E-Mail-Adresse (von Text)</p>

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