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


# Profil (nms:empfänger)

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
                  <td>Alter</td>
                  <td>Alter</td>
                  <td>integer </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>appSubscription</td>
                  <td>Abonnements für eine Anwendung</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>birthDate</td>
                  <td>Geburtsdatum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackList</td>
                  <td>Nicht mehr kontaktieren (alle Kanäle)</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListEmail</td>
                  <td>Nicht mehr per E-Mail kontaktieren</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListFax</td>
                  <td>Keine Verbindung mehr</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListMobile</td>
                  <td>Nicht mehr per SMS kontaktieren</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListPhone</td>
                  <td>Keine telefonische Kontaktaufnahme mehr</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListPostalMail</td>
                  <td>Kein Kontakt mehr mit Direktwerbung</td>
                  <td>boolean </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>blackListPushnotification</td>
                  <td>Kein Kontakt mehr mit Push-Benachrichtigung</td>
                  <td>boolean </td>
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
                  <td>cryptedId</td>
                  <td>Verschlüsselte ID</td>
                  <td>string </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusHobbieslink (cusHobbies)</td>
                  <td>CusHobbieslink</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusLastTransactionDate</td>
                  <td>Letztes Transaktionsdatum</td>
                  <td>date </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>cusTransactionslink</td>
                  <td>Transaktionen</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>domain</td>
                  <td>E-Mail-Domäne</td>
                  <td>Zeichenfolge (255)</td>
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
                  <td>emailStatus (addressStatus)</td>
                  <td>Informationen zur E-Mail</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>excludeLogs</td>
                  <td>Ausschlusslogs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>fax</td>
                  <td>Fax</td>
                  <td>Zeichenfolge (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>firstName</td>
                  <td>Vorname</td>
                  <td>Zeichenfolge (30)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>gender</td>
                  <td>Geschlecht</td>
                  <td>Aufzählung (Byte) </td>
                  <td>
                     <ul>
                        <li>Nicht spezifiziert - unbekannt - 0</li>
                        <li>Männlich - 1</li>
                        <li>Weiblich - weiblich - 2</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                     </ul>
                  </td>
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
                  <td>lastName</td>
                  <td>Nachname</td>
                  <td>Zeichenfolge (50)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>location</td>
                  <td>Standort</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>logs</td>
                  <td>Versandlogs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>middleName</td>
                  <td>Zweiter Vorname</td>
                  <td>Zeichenfolge (30)</td>
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
                  <td>phone</td>
                  <td>Telefon</td>
                  <td>Zeichenfolge (32)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Orte</td>
                  <td>Standorte</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>postalAddress</td>
                  <td>Anschrift</td>
                  <td>item </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>salutation</td>
                  <td>Titel</td>
                  <td>Zeichenfolge (20)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>stateLink (state)</td>
                  <td>Bundesland/Kanton</td>
                  <td>link </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>subHisto</td>
                  <td>Abonnementverläufe</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Abonnements</td>
                  <td>Abonnements</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
               <tr>
                  <td>Miniaturansicht</td>
                  <td>Miniaturansicht</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>timeZone</td>
                  <td>Zeitzone</td>
                  <td>Enumeration (Zeichenfolge) (64)</td>
                  <td>
                     <ul>
                        <li>(GMT-02:00) Mittelatlantik - Atlantic_South_Georgia - Atlantic/South_Georgia</li>
                        <li>(GMT+02:00) Amman - Asia_Amman - Asia/Amman</li>
                        <li>(GMT-03:00) Brasi - America_Sao_Paulo - Amerika/Sao_Paulo</li>
                        <li>(GMT+06:00) Astana, Dhaka - Asia_Dhaka - Asia/Dhaka</li>
                        <li>(GMT+06:00) Novossibirsk - Asia_Novosibirsk - Asia/Nowosibirsk</li>
                        <li>(GMT+02:00) Windhoek - Africa_Windhoek - Africa/Windhoek</li>
                        <li>(GMT+04:00) Caucasus, Erevan - Asia_Yerevan - Asia/Yerevan</li>
                        <li>(GMT-04:00) Manaus - America_Manaus - America/Manaus</li>
                        <li>(GMT+03:30) Teheran - Asia_Teheran - Asia/Teheran</li>
                        <li>(GMT+12:00) Auckland, Wellington - Pacific_Auckland - Pacific/Auckland</li>
                        <li>(GMT+02:00) Jerusalem - Asien_Jerusalem - Asien/Jerusalem</li>
                        <li>(GMT+03:00) Moskau, St. Petersburg, Wolgograd - Europa_Moskau - Europa/Moskau</li>
                        <li>(GMT+09:30) Adelaïde - Australia_Adelaide - Australien/Adelaide</li>
                        <li>(GMT+10:00) Canberra, Melbourne, Sydney - Australia_Canberra - Australien/Canberra</li>
                        <li>(GMT+08:00) Perth - Australia_Perth - Australia/Perth</li>
                        <li>(GMT+09:00) Jakoutsk - Asia_Jakutsk - Asia/Jakutsk</li>
                        <li>(GMT-10:00) Hawai - Pacific_Honolulu - Pacific/Honolulu</li>
                        <li>(GMT+04:00) Baku - Asia_Baku - Asia/Baku</li>
                        <li>(GMT+10:00) Wladiwostok - Asien_Wladiwostok - Asien/Wladiwostok</li>
                        <li>(GMT+09:00) Seoul - Asia_Seoul - Asia/Seoul</li>
                        <li>(GMT+01:00) Sarajevo, Skoplje, Sofia, Warschau, Zagreb - Europe_Sarajevo - Europe/Sarajevo</li>
                        <li>(GMT+04:00) Abu Dhabi, Muscat - Asia_Muscat - Asia/Muscat</li>
                        <li>(GMT+08:00) Kuala Lumpur, Singapur - Asia_Kuala_Lumpur - Asia/Kuala_Lumpur</li>
                        <li>(GMT+09:00) Osaka, Sapporo, Tokio - Asia_Tokyo - Asia/Tokyo</li>
                        <li>(GMT+10:00) Brisbane - Australia_Brisbane - Australia/Brisbane</li>
                        <li>(GMT+05:30) Sri Jaywerdenepura - Asia_Colombo - Asia/Colombo</li>
                        <li>(GMT+02:00) Harare, Pretoria - Africa_Harare - Africa/Harare</li>
                        <li>(GMT+08:00) Oulan-Bator - Asia_Ulan_Bator - Asia/Ulan_Bator</li>
                        <li>(GMT-02:00) Greenwich Mean Time minus 2 Stunden - GMT_m2 - ETC/GMT+2</li>
                        <li>(GMT-03:00) Greenwich Mean Time minus 3 Stunden - GMT_m3 - ETC/GMT+3</li>
                        <li>(GMT-01:00) Greenwich Mean Time minus 1 Stunde - GMT_m1 - ETC/GMT+1</li>
                        <li>(GMT-06:00) Greenwich Mean Time minus 6 Stunden - GMT_m6 - ETC/GMT+6</li>
                        <li>(GMT-07:00) Greenwich Mean Time minus 7 Stunden - GMT_m7 - ETC/GMT+7</li>
                        <li>(GMT-04:00) Mittlere Greenwich-Zeit minus 4 Stunden - GMT_m4 - ETC/GMT+4</li>
                        <li>(GMT) Casablanca - Africa_Casablanca - Africa/Casablanca</li>
                        <li>(GMT+05:30) Kalkutta, Chennai, Mumbai, Neu-Delhi - Asien_Kalkutta - Asien/Kalkutta</li>
                        <li>(GMT-11:00) Greenwich Mean Time minus 11 Stunden - GMT_m11 - ETC/GMT+11</li>
                        <li>(GMT-09:00) Greenwich Mean Time minus 9 Stunden - GMT_m9 - ETC/GMT+9</li>
                        <li>(GMT-03:30) Neufundland - Amerika_St_Johns - Amerika/St_Johns</li>
                        <li>(GMT+03:00) Greenwich Mean Time plus 3 Stunden - GMT_p3 - Etc/GMT-3</li>
                        <li>(GMT-04:30) Caracas - America_Caracas - America/Caracas</li>
                        <li>(GMT+01:00) Amsterdam, Berlin, Bern, Rom, Stockholm, Wien - Europa_Berlin - Europa/Berlin</li>
                        <li>(GMT-07:00) Chihuahua, La Paz, Mazatlan - America_Chihuahua - Amerika/Chihuahua</li>
                        <li>(GMT+03:00) Nairobi - Afrika_Nairobi - Afrika/Nairobi</li>
                        <li>(GMT-04:00) Asunción - America_Asuncion - America/Asuncion</li>
                        <li>(GMT+03:00) Bagdad - Asia_Bagdad - Asia/Bagdad</li>
                        <li>(GMT-10:00) Mittlere Greenwich-Zeit minus 10 Stunden - GMT_m10 - ETC/GMT+10</li>
                        <li>(GMT-03:00) Grönland - America_Godthab - Amerika/Godthab</li>
                        <li>(GMT+02:00) Damas - Asia_Damaskus - Asia/Damaskus</li>
                        <li>(GMT-11:00) Samoa - Pacific_Samoa - Pacific/Samoa</li>
                        <li>(GMT-05:00) Bogota, Lima, Quito - America_Bogota - America/Bogota</li>
                        <li>(GMT+01:00) Brüssel, Kopenhagen, Madrid, Paris - Europa_Paris - Europa/Paris</li>
                        <li>(GMT+08:00) Peking, Chongqing, Hong Kong, Urumqi - Asia_Shanghai - Asia/Shanghai</li>
                        <li>(GMT+12:00) Fidji - Pacific_Fiji - Pacific/Fidschi</li>
                        <li>(GMT+02:00) Athen, Istanbul, Minsk - Europa_Athen - Europa/Athen</li>
                        <li>(GMT+04:00) Tiflis - Asia_Tiflis - Asia/Tiflis</li>
                        <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
                        <li>(GMT+05:45) Katmandu - Asia_Katmandu - Asia/Katmandu</li>
                        <li>(GMT-05:00) Indiana (Osten) - America_Indianapolis - Amerika/Indianapolis</li>
                        <li>(GMT-01:00) Kap-Verde-Inseln - Atlantic_Cape_Verde - Atlantic/Kap_Verde</li>
                        <li>(GMT+04:00) Port Louis - Indian_Mauritius - Indian/Mauritius</li>
                        <li>(GMT+08:00) Taipeh - Asia_Taipei - Asia/Taipeh</li>
                        <li>(GMT+06:30) Rangoon - Asia_Rangoon - Asia/Rangoon</li>
                        <li>(GMT+11:00) Magadan, The Solomon Islands, New Caledonia - Pacific_Guadalcanal - Pacific/Guadalcanal</li>
                        <li>(GMT+02:00) Kairo - Afrika_Kairo - Afrika/Kairo</li>
                        <li>(GMT+05:00) Iekaterinburg - Asia_Yekaterinburg - Asia/Yekaterinburg</li>
                        <li>(GMT+08:00) Irkoutsk - Asia_Irkutsk - Asia/Irkutsk</li>
                        <li>(GMT+10:00) Guam, Port Moresby - Pacific_Guam - Pacific/Guam</li>
                        <li>(GMT-04:00) Atlantic Standard Time (Kanada) - America_Halifax - America/Halifax</li>
                        <li>(GMT) Greenwich meine Zeit - GMT - GMT</li>
                        <li>Standard - keine</li>
                        <li>(GMT-04:00) La Paz - America_La_Paz - America/La_Paz</li>
                        <li>(GMT-06:00) Guadalajara, Mexiko, Monterrey - America_Mexico_City - America/Mexico_City</li>
                        <li>(GMT+09:30) Darwin - Australia_Darwin - Australien/Darwin</li>
                        <li>(GMT-05:00) Est (Vereinigte Staaten und Kanada) - America_New_York - America/New_York</li>
                        <li>(GMT-05:00) Greenwich Mean Time minus 5 Stunden - GMT_m5 - ETC/GMT+5</li>
                        <li>(GMT+05:00) Islamabad, Karatschi, Tachkent - Asia_Karatschi - Asia/Karatschi</li>
                        <li>(GMT+03:00) Koweït, Riyad - Asia_Riad - Asia/Riad</li>
                        <li>(GMT-08:00) Mittlere Greenwich-Zeit minus 8 Stunden - GMT_m8 - ETC/GMT+8</li>
                        <li>(GMT-01:00) Die Azoren - Atlantik_Azoren - Atlantik/Azoren</li>
                        <li>(GMT+07:00) Bangkok, Hanoi, Djakarta - Asia_Bangkok - Asia/Bangkok</li>
                        <li>(GMT) Monrovia - Afrika_Monrovia - Afrika/Monrovia</li>
                        <li>(GMT-09:00) Alaska - America_Anchorage - Amerika/Anchorage</li>
                        <li>(GMT+01:00) Belgrad, Bratislava, Budapest, Ljubljana, Prag - Europa_Belgrad - Europa/Belgrad</li>
                        <li>(GMT) Reykjavik - Atlantic_Reykjavik - Atlantic/Reykjavik</li>
                        <li>(GMT+02:00) Bukarest - Europe_Bukarest - Europe/Bukarest</li>
                        <li>(GMT+05:00) Greenwich Mean Time plus 5 Stunden - GMT_p5 - Etc/GMT-5</li>
                        <li>(GMT+04:00) Greenwich Mean Time plus 4 Stunden - GMT_p4 - Etc/GMT-4</li>
                        <li>(GMT+07:00) Greenwich Mean Time plus 7 Stunden - GMT_p7 - Etc/GMT-7</li>
                        <li>(GMT+06:00) Greenwich Mean Time plus 6 Stunden - GMT_p6 - ETC/GMT-6</li>
                        <li>(GMT+01:00) Greenwich Mean Time plus 1 Stunde - GMT_p1 - Etc/GMT-1</li>
                        <li>(GMT-08:00) Pacific (United States and Canada) - America_Los_Angeles - America/Los_Angeles</li>
                        <li>(GMT+02:00) Greenwich Mean Time plus 2 Stunden - GMT_p2 - Etc/GMT-2</li>
                        <li>(GMT+07:00) Krasnoïarsk - Asia_Krasnojarsk - Asia/Krasnojarsk</li>
                        <li>(GMT+09:00) Greenwich Mean Time plus 9 Stunden - GMT_p9 - Etc/GMT-9</li>
                        <li>(GMT+08:00) Greenwich Mean Time plus 8 Stunden - GMT_p8 - ETC/GMT-8</li>
                        <li>(GMT+10:00) Hobart - Australia_Hobart - Australien/Hobart</li>
                        <li>(GMT+13:00) Nuku'alofa - Pacific_Tongatapu - Pacific/Tongatapu</li>
                        <li>(GMT-06:00) Mittelamerika - Amerika_Regina - Amerika/Regina</li>
                        <li>(GMT-03:00) Buenos Aires, Cayenne, Fortaleza - America_Buenos_Aires - America/Buenos_Aires</li>
                        <li>(GMT-07:00) Rocky Mountains (Vereinigte Staaten und Kanada) - America_Denver - America/Denver</li>
                        <li>(GMT+01:00) Zentralafrika - West - Afrika_Luanda - Afrika/Luanda</li>
                        <li>(GMT+02:00) Helsinki, Kiew, Riga, Sofia, Tallinn, Vilnius - Europe_Helsinki - Europa/Helsinki</li>
                        <li>(GMT) Mittlere Greenwich-Zeit: Dublin, Edinburgh, Lissabon, London - Europe_London - Europe/London</li>
                        <li>(GMT-07:00) Arizona - America_Phoenix - America/Phoenix</li>
                        <li>(GMT+02:00) Beirut - Asien_Beirut - Asien/Beirut</li>
                        <li>(GMT+04:30) Kabul - Asia_Kabul - Asia/Kabul</li>
                        <li>(GMT-06:00) Centre (Vereinigte Staaten und Kanada) - America_Chicago - America/Chicago</li>
                        <li>(GMT+11:00) Greenwich Mean Time plus 11 Stunden - GMT_p11 - Etc/GMT-11</li>
                        <li>(GMT+10:00) Greenwich Mean Time plus 10 Stunden - GMT_p10 - Etc/GMT-10</li>
                        <li>(GMT+13:00) Greenwich Mean Time plus 13 Stunden - GMT_p13 - Etc/GMT-13</li>
                        <li>(GMT+12:00) Greenwich Mean Time plus 12 Stunden - GMT_p12 - Etc/GMT-12</li>
                        <li>(GMT-04:00) Santiago - America_Santiago - America/Santiago</li>
                        <li>(GMT-03:00) Montevideo - America_Montevideo - America/Montevideo</li>
                        <li>(GMT-04:00) Cuiaba - America_Cuiaba - Amerika/Cuiaba</li>
                     </ul>
                  </td>
               </tr>
               <tr>
                  <td>title</td>
                  <td>Profil</td>
                  <td>Zeichenfolge (255)</td>
                  <td> </td>
               </tr>
               <tr>
                  <td>tracking</td>
                  <td>Trackinglogs</td>
                  <td>Sammlung </td>
                  <td> </td>
               </tr>
            </table>


## Filter


Geburtstag (Geburtstag)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>includeStart</td>
<td>boolean</td>
</tr>
<tr>
<td>previousUnitsValue</td>
<td>integer</td>
</tr>
<tr>
<td>nextUnitsValue</td>
<td>integer</td>
</tr>
<tr>
<td>endDay</td>
<td>date</td>
</tr>
<tr>
<td>genauigkeit</td>
<td>enumeration</td>
</tr>
<tr>
<td>relativeValue</td>
<td>string</td>
</tr>
<tr>
<td>Monat</td>
<td>date</td>
</tr>
<tr>
<td>operator</td>
<td>enumeration</td>
</tr>
<tr>
<td>includeEnd</td>
<td>boolean</td>
</tr>
<tr>
<td>endMonth</td>
<td>date</td>
</tr>
<tr>
<td>Typ</td>
<td>enumeration</td>
</tr>
<tr>
<td>Tag</td>
<td>date</td>
</tr>
</table>

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

Nach Schlüsseln (byKeysProfile)

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

Nach Name oder E-Mail (von Text)

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

Von statischem Publikum (von StaticAudience)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>Zielgruppe</td>
<td>link</td>
</tr>
</table>

Klickt (hasClickDelivery)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>lieferung</td>
<td>link</td>
</tr>
</table>

Geöffnet (hasOpenDelivery)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>lieferung</td>
<td>link</td>
</tr>
</table>

Profil (Profil)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>profile</td>
<td>link</td>
</tr>
</table>

Received (hasReceivedDelivery)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>lieferung</td>
<td>link</td>
</tr>
</table>

Abonnenten (Abonnenten)

<table>
<tr>
<th>Name</th>
<th>Typ</th>
</tr>
<tr>
<td>service</td>
<td>link</td>
</tr>
</table>