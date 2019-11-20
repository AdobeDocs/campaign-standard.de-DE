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


# Dienst (nms:service)

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
                  <td>cusPrice</td>
                  <td>Preis</td>
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
                  <td>Geschichte</td>
                  <td>Abonnementverläufe</td>
                  <td>Sammlung </td>
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
                  <td>limitedDuration</td>
                  <td>Begrenzte Dauer</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>mainDate</td>
                  <td>Datum</td>
                  <td>Datum (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>messageType</td>
                  <td>Kanal</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Mobil (SMS) - sms - 1</li>
                        <li>E-Mail - E-Mail - 0</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>mode</td>
                  <td>Modus</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Viral - viral - 1</li>
                        <li>Newsletter - Newsletter - 0</li>
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
                  <td>publicLabel</td>
                  <td>Dienstebezeichnung</td>
                  <td>Zeichenfolge (128)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>start</td>
                  <td>Anfangsdatum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subLandingPage (landingPageSubscriptionBase)</td>
                  <td>Einstiegsseite des Abonnements</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subScenario (deliveryMCTemplateBase)</td>
                  <td>Abonnementbestätigung</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subScenarioEventType</td>
                  <td>SubScenarioEventType</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Abonnements</td>
                  <td>Abonnements</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>targetResource</td>
                  <td>Zielgruppendimension</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>template (service)</td>
                  <td>Dienstvorlage</td>
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
                  <td>Dienst</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>unsubLandingPage (landingPageUnsubscriptionBase)</td>
                  <td>Einstiegsseite für das Abonnement</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>unsubScenario (deliveryMCTemplateBase)</td>
                  <td>Abonnementbestätigung</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>unsubScenarioEventType</td>
                  <td>UnsubScenarioEventType</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>validityDuration</td>
                  <td>Gültigkeitsdauer</td>
                  <td>number </td>
                  <td> </td>
               </tr>
            </table>

## Filter

Verfügbar während des angegebenen Zeitraums (nach Planung)

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

Durch Targeting der Ressource (nach TargetResource)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>targetResource</td>
<td>string</td>
</tr>
</table>