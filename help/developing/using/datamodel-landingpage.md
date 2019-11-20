---
title: DataModel
description: Informationen zum Datenmodell
page-status-flag: never-activated
uuid: 99277e46-e4f7-49a9-ba27-b878780f90da
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-sms-and-push-content
discoiquuid: 6e21db35-daf9-4edb-977a-6ef606db0e4d
context-tags: delivery,smsContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 18d9b33e36db628ef1fc014e4abe6a4a7eef48b3

---


# landingPage (nms:landingPage)

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
         <td>additionalData</td>
         <td>Zusätzliche Daten</td>
         <td>Sammlung </td>
         <td> </td>
      </tr>
      <tr>
         <td>additionalLanguages</td>
         <td>weitere Sprachen</td>
         <td>item </td>
         <td> </td>
      </tr>
      <tr>
         <td>allowNonIdentifiedTarget</td>
         <td>Nicht identifizierte Besucher autorisieren</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>Branding (brandingBase)</td>
         <td>Marke</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>buildIn</td>
         <td>Integriertes Anwendungsobjekt</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>cache</td>
         <td>Cache</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>campaign (campaignBase)</td>
         <td>Kampagne</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>closeLog</td>
         <td>"Einstiegsseite geschlossen"-Protokoll</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>contextResourceType</td>
         <td>ContextResourceType</td>
         <td>string </td>
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
         <td>cryptKey</td>
         <td>AES-Verschlüsselungsschlüssel</td>
         <td>Zeichenfolge (64)</td>
         <td> </td>
      </tr>
      <tr>
         <td>defaultLanguage</td>
         <td>Standardsprache</td>
         <td>Enumeration (Zeichenfolge) (255)</td>
         <td>
            <ul>
               <li>Griechisch - el - el</li>
               <li>Englisch - en - en</li>
               <li>Chinesisch - zh - zh</li>
               <li>Französisch (Frankreich) - fr_FR - fr_FR</li>
               <li>Vietnamesisch - vi</li>
               <li>Portugiesisch (Portugal) - pt_PT - pt_PT</li>
               <li>Italienisch (Italien) - it_IT - it_IT</li>
               <li>Italienisch - it - it</li>
               <li>Niederländisch (Belgien) - nl_BE - nl_BE</li>
               <li>Norwegisch (Norwegen) - no_NO - no_NO</li>
               <li>Niederländisch (Niederlande) - nl_NL - nl_NL</li>
               <li>Arabisch - ar - ar</li>
               <li>Englisch (Vereinigte Staaten) - en_US - en_US</li>
               <li>Irisch - ga - ga</li>
               <li>Tschechisch - cs</li>
               <li>Estnisch - et - et</li>
               <li>Indonesisch - id - id</li>
               <li>Spanisch - es - es</li>
               <li>Russisch - ru - ru</li>
               <li>Niederländisch - nl - nl</li>
               <li>Wallonisch - wa - wa</li>
               <li>Portugiesisch - pt</li>
               <li>Französisch (Belgien) - fr_BE - fr_BE</li>
               <li>Lettisch - lv - lv</li>
               <li>litauisch - lt - lt</li>
               <li>Thailändisch - th - th</li>
               <li>Englisch (Vereinigtes Königreich) - en_GB - en_GB</li>
               <li>Französisch - fr - fr</li>
               <li>Portugiesisch (Brasilien) - pt_BR - pt_BR</li>
               <li>Deutsch - de - de</li>
               <li>Dänisch - da - da</li>
               <li>Finnisch - fi - fi</li>
               <li>Ungarisch - hu - hu</li>
               <li>Schwedisch (Finnland) - sv_FI - sv_FI</li>
               <li>Japanisch - ja - ja</li>
               <li>Hebräisch - er - der</li>
               <li>Koreanisch - ko - ko</li>
               <li>Schwedisch - sv - sv</li>
               <li>Schweden (Schwedisch) - sv_SE - sv_SE</li>
               <li>Slowakisch - sk</li>
               <li>Maltesisch - mt</li>
               <li>Italienisch (Schweiz) - it_CH - it_CH</li>
               <li>Polnisch - pl - pl</li>
               <li>Slowenisch - sl - sl</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>defaultOrigin (Bereitstellung)</td>
         <td>Traffic-Quelle</td>
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
         <td>designLanguage</td>
         <td>Entwurfssprache</td>
         <td>Enumeration (Zeichenfolge) (255)</td>
         <td>
            <ul>
               <li>Griechisch - el - el</li>
               <li>Englisch - en - en</li>
               <li>Chinesisch - zh - zh</li>
               <li>Französisch (Frankreich) - fr_FR - fr_FR</li>
               <li>Vietnamesisch - vi</li>
               <li>Portugiesisch (Portugal) - pt_PT - pt_PT</li>
               <li>Italienisch (Italien) - it_IT - it_IT</li>
               <li>Italienisch - it - it</li>
               <li>Niederländisch (Belgien) - nl_BE - nl_BE</li>
               <li>Norwegisch (Norwegen) - no_NO - no_NO</li>
               <li>Niederländisch (Niederlande) - nl_NL - nl_NL</li>
               <li>Arabisch - ar - ar</li>
               <li>Englisch (Vereinigte Staaten) - en_US - en_US</li>
               <li>Irisch - ga - ga</li>
               <li>Tschechisch - cs</li>
               <li>Estnisch - et - et</li>
               <li>Indonesisch - id - id</li>
               <li>Spanisch - es - es</li>
               <li>Russisch - ru - ru</li>
               <li>Niederländisch - nl - nl</li>
               <li>Wallonisch - wa - wa</li>
               <li>Portugiesisch - pt</li>
               <li>Französisch (Belgien) - fr_BE - fr_BE</li>
               <li>Lettisch - lv - lv</li>
               <li>litauisch - lt - lt</li>
               <li>Thailändisch - th - th</li>
               <li>Englisch (Vereinigtes Königreich) - en_GB - en_GB</li>
               <li>Französisch - fr - fr</li>
               <li>Portugiesisch (Brasilien) - pt_BR - pt_BR</li>
               <li>Deutsch - de - de</li>
               <li>Dänisch - da - da</li>
               <li>Finnisch - fi - fi</li>
               <li>Ungarisch - hu - hu</li>
               <li>Schwedisch (Finnland) - sv_FI - sv_FI</li>
               <li>Japanisch - ja - ja</li>
               <li>Hebräisch - er - der</li>
               <li>Koreanisch - ko - ko</li>
               <li>Schwedisch - sv - sv</li>
               <li>Schweden (Schwedisch) - sv_SE - sv_SE</li>
               <li>Slowakisch - sk</li>
               <li>Maltesisch - mt</li>
               <li>Italienisch (Schweiz) - it_CH - it_CH</li>
               <li>Polnisch - pl - pl</li>
               <li>Slowenisch - sl - sl</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>dynamicService</td>
         <td>Dynamischer Dienst</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>end</td>
         <td>Ablaufdatum</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>errorContextResourceType</td>
         <td>ErrorContextResourceType</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>errorPage</td>
         <td>Fehlerseite</td>
         <td>item </td>
         <td> </td>
      </tr>
      <tr>
         <td>geoUnit (geoUnitBase)</td>
         <td>Geografische Einheit</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>htmlPage</td>
         <td>Seiten</td>
         <td>Sammlung </td>
         <td> </td>
      </tr>
      <tr>
         <td>identificationByUrlParam</td>
         <td>Identifizierung nach URL-Parametern</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>inactiveUrlRedirect</td>
         <td>Umleitungs-URL</td>
         <td>Zeichenfolge (4096)</td>
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
         <td>job</td>
         <td>Vorgang</td>
         <td>Sammlung </td>
         <td> </td>
      </tr>
      <tr>
         <td>jobLogs</td>
         <td>Logs</td>
         <td>Sammlung </td>
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
         <td>loadingFilter (queryFilterBase)</td>
         <td>Laden der Taste</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>loadingFilterMapping</td>
         <td>Parameter des Ladeschlüssels</td>
         <td>Sammlung </td>
         <td> </td>
      </tr>
      <tr>
         <td>logicalStatus</td>
         <td>Ausführungsstatus</td>
         <td>Enumeration (Zeichenfolge) (255)</td>
         <td>
            <ul>
               <li>In Verarbeitung - begonnen</li>
               <li>Bearbeitung - Ausgabe - Ausgabe</li>
               <li>Fertig - fertig - fertig</li>
               <li>Warnung - Warnung - Warnung</li>
               <li>Fehler - Fehler - Fehler</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>messageAction</td>
         <td>Nachricht starten</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>messageActionDelivery (deliveryMCTemplateBase)</td>
         <td>Transaktionsnachricht</td>
         <td>link </td>
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
         <td>orgUnit (orgUnitBase)</td>
         <td>Organisationseinheit</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>prefill</td>
         <td>Besucherdaten im Voraus laden</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>programme (programmeBase)</td>
         <td>Programm</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>publicUrl</td>
         <td>Öffentliche URL</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>publicationDate</td>
         <td>Veröffentlichungsdatum</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>Reconsfilter (queryFilterBase)</td>
         <td>Abstimmschlüssel</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>aushaltsfilterMapping</td>
         <td>Abgleich von Schlüsselparametern</td>
         <td>Sammlung </td>
         <td> </td>
      </tr>
      <tr>
         <td>overviewUpdateStrategy</td>
         <td>Strategie aktualisieren</td>
         <td>Aufzählung (Byte) </td>
         <td>
            <ul>
               <li>Update - UpdateTarget - 1</li>
               <li>Nicht autorisiert - nicht autorisiert - 0</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>service (serviceBase)</td>
         <td>Abonnementdienst</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>specificAction</td>
         <td>Spezifische Maßnahmen</td>
         <td>Aufzählung (Byte) </td>
         <td>
            <ul>
               <li>Blacklist - blackList - 3</li>
               <li>Keine spezifische Aktion - keine - 0</li>
               <li>Rückmeldung - Rückmeldung - 2</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
               <li>Abonnement - Abonnement - 1</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>start</td>
         <td>Bereitstellungsdatum</td>
         <td>date </td>
         <td> </td>
      </tr>
      <tr>
         <td>Status</td>
         <td>Status</td>
         <td>Aufzählung (Byte) </td>
         <td>
            <ul>
               <li>Bearbeiten - Bearbeiten - 0</li>
               <li>Veröffentlichung fehlgeschlagen - fehlgeschlagen - 99</li>
               <li>Geschlossen - geschlossen - 20</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
               <li>Online - geöffnet - 10</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>targetResource</td>
         <td>Zielgruppendimension</td>
         <td>Zeichenfolge (255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>template (landingPage)</td>
         <td>Vorlage der Einstiegsseite</td>
         <td>link </td>
         <td> </td>
      </tr>
      <tr>
         <td>testUrl</td>
         <td>Test-URL</td>
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
         <td>Zeitzone</td>
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
               <li>Serverzeitzone - _server_ - _server_</li>
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
               <li>Standard - _inherit_ - _inherit_</li>
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
               <li>Zeitzone der Datenbank - _wdbc_ - _wdbc_</li>
               <li>(GMT+06:30) Rangoon - Asia_Rangoon - Asia/Rangoon</li>
               <li>(GMT+11:00) Magadan, The Solomon Islands, New Caledonia - Pacific_Guadalcanal - Pacific/Guadalcanal</li>
               <li>(GMT+02:00) Kairo - Afrika_Kairo - Afrika/Kairo</li>
               <li>(GMT+05:00) Iekaterinburg - Asia_Yekaterinburg - Asia/Yekaterinburg</li>
               <li>(GMT+08:00) Irkoutsk - Asia_Irkutsk - Asia/Irkutsk</li>
               <li>(GMT+10:00) Guam, Port Moresby - Pacific_Guam - Pacific/Guam</li>
               <li>(GMT-04:00) Atlantic Standard Time (Kanada) - America_Halifax - America/Halifax</li>
               <li>(GMT) Greenwich meine Zeit - GMT - GMT</li>
               <li>(GMT-04:00) La Paz - America_La_Paz - America/La_Paz</li>
               <li>Zeitzone des Operators - _login_ - _login_</li>
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
         <td>Landingpage</td>
         <td>Zeichenfolge (255)</td>
         <td> </td>
      </tr>
      <tr>
         <td>trackingEnabled</td>
         <td>Antworten protokollieren</td>
         <td>boolean </td>
         <td> </td>
      </tr>
      <tr>
         <td>trackingUrlName</td>
         <td>Tracking-URL-Name</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>Typ</td>
         <td>Typ</td>
         <td>Aufzählung (Byte) </td>
         <td>
            <ul>
               <li>Allgemein - Generika - 0</li>
               <li>Rückmeldung von einem Dienst - Rückmeldung - 3</li>
               <li>Blacklist - blackList - 4</li>
               <li>UNGÜLTIGER WERT - __Invalid_value__ - __Invalid_value__</li>
               <li>Akquise - Akquisition - 1</li>
               <li>Abonnement eines Dienstes - Abonnement - 2</li>
            </ul>
         </td>
      </tr>
      <tr>
         <td>uuid</td>
         <td>Sicherheits-ID</td>
         <td>string </td>
         <td> </td>
      </tr>
      <tr>
         <td>webTrackingEnabled</td>
         <td>Web-Verfolgung aktivieren</td>
         <td>boolean </td>
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
    <td>Status</td>
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

Nach Status (nach Staat)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>Status</td>
    <td>enumeration</td>
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

Erweiterte Einstiegsseiten einschließen (mit Advanced)

<table>
    <tr>
    <th>Name</th>
    <th>Typ</th>
    </tr>
    <tr>
    <td>advanced</td>
    <td>boolean</td>
    </tr>
</table>

Einschließlich kontinuierlicher Auslieferungen aus einer heterogenen Liste (mit "Fortlaufend")

<table>
        <tr>
        <th>Name</th>
        <th>Typ</th>
        </tr>
        <tr>
        <td>withContinuous</td>
        <td>boolean</td>
        </tr>
    </table>

Vorhanden während des angegebenen Zeitraums (nach Kalender)

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

Veröffentlicht während des angegebenen Zeitraums (nach Planung)

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
