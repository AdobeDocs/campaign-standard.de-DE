---
title: Generieren einer CSV-Datei für mehrsprachige Push-Benachrichtigung mit Campaign Standard
description: Das Hochladen einer CSV-Datei zum Generieren von Inhalten für die Bereitstellung ist eine Funktion, mit der mehrsprachige Push-Benachrichtigungen unterstützt werden.
page-status-flag: never-activated
uuid: e90f4ec8-14e3-4304-b5fc-bce0ba08a4ef
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: email-messages
discoiquuid: 79231445-1d51-499a-adcf-0c0f6db1cfa3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c6df07dd78de6b15971937d574429d3ba5dc1a15

---


# Erstellen einer CSV-Datei für mehrsprachige Push-Benachrichtigung{#generating-csv-multilingual-push}

Das Hochladen einer CSV-Datei zur Erstellung von Inhalten für die Bereitstellung ist eine Funktion, mit der mehrsprachige Push-Benachrichtigungen unterstützt werden. Das Format der CSV-Datei muss bestimmten Richtlinien entsprechen, damit der Datei-Upload erfolgreich sein kann und somit eine Auslieferung möglich ist. In den folgenden Abschnitten werden das Dateiformat und die damit verbundenen Erwägungen beschrieben.

## Dateiformat {#file-format}

Mehrsprachiges Push erfordert 14 Spalten in der CSV-Datei:

* title
* messageBody
* Ton
* Badge
* deeplinkURI
* Kategorie
* iosMediaAttachmentURL
* androidMediaAttachmentURL
* isContentAvailable
* isMutableContent
* customFields
* Gebietsschema
* Sprache
* silentPush

![](assets/multilingual_push_1.png)

Markieren Sie das CSV-Beispiel, indem Sie auf **[!UICONTROL Download a sample file]** die **[!UICONTROL Manage Content Variants]** Schaltfläche klicken. For more on this, refer to the this [section](../../channels/using/creating-a-multilingual-push-notification.md).

* **title, messageBody, sound, badge, deeplinkURI, category, iosMediaAttachmentURL, androidMediaAttachmentURL**: regelmäßige Push-Nutzdateninhalte. Sie müssen diese Informationen auf ähnliche Weise bereitstellen wie beim Erstellen von Push-Auslieferungen.
* **Benutzerdefinierte Felder**:  Verwenden Sie das JSON-Format für die benutzerdefinierten Felder, z. B. &quot;{&quot;&quot;key1&quot;&quot;:&quot;&quot;value1&quot;&quot;,&quot;&quot;key2&quot;&quot;:&quot;&quot;value2&quot;&quot;}&quot;. In der obigen Beispieldatei finden Sie ein Beispiel für benutzerdefinierte Felder.
* **isContentAvailable**: Flag für Prüfung &quot;Content Available&quot;, Wert 1 bedeutet &quot;true&quot;, Wert 0 bedeutet &quot;false&quot;. Der Standardwert ist 0. Wenn Sie diese Spalte leer lassen, wird der Wert als 0 betrachtet.
* **isMutableContent**: Flag für &quot;Mutable Content&quot;, Wert 1 bedeutet &quot;true&quot;, Wert 0 bedeutet &quot;false&quot;. Der Standardwert ist 0. Wenn Sie diese Spalte leer lassen, wird der Wert als 0 betrachtet.
* **locale**: locale ist das Feld für Sprachvarianten, z. &quot;en_us&quot;für US-Englisch und &quot;fr_fr&quot;für Frankreich-Französisch.
* **Sprache**: Name der Sprache, die mit dem Gebietsschema verknüpft ist. Wenn das Gebietsschema beispielsweise &quot;en_us&quot;lautet, sollte der Name der Sprache &quot;English-United States&quot;lauten.
* **silentPush**: Flag für den Push-Benachrichtigungstyp. Wenn es sich um eine reguläre Push-Benachrichtigung handelt, sollte der Wert 0 betragen. Wenn es sich um einen stillen Push handelt, sollte der Wert 1 betragen. Der Standardwert ist 0. Wenn Sie diese Spalte leer lassen, wird der Wert als 0 betrachtet.

## Einschränkungen und Richtlinien für die Erstellung von CSV-Dateien {#constraints-guideline-csv}

**Der Name jeder Spalte ist festgelegt**.
Sie sollten den Namen der einzelnen Spalten in der CSV-Datei angeben. Wenn Sie keine Spalten für den Inhalt verwenden, lassen Sie sie leer.

**Die Spalten &quot;locale&quot;und &quot;language&quot;sind obligatorisch und der Wert ist für jede Zeile eindeutig.**
Ein leerer Wert für diese Spalte führt zu einem Fehler beim Hochladen der Datei.

**Die Reihenfolge der Spalten ist wichtig**. Die Reihenfolge der Spalten in der hochgeladenen Datei muss dem gleichen Format wie die Musterdatei entsprechen.

**Anführungsspalteninhalt**. Da es sich hierbei um eine CSV-Datei (steht für kommagetrennte Werte) handelt, muss jeder Spalteninhalt, der Komma (,) enthält, zitiert werden. Zum Beispiel &quot;Hallo, Tom!&quot;

**UTF-8-Kodierung ist für internationale Zeichen erforderlich.**

**Wenn Sie die Datei mit einfachem Text generieren, trennen Sie jede Spalte durch &quot;,&quot;.**

**Variante stimmt nicht überein.** Wenn Sie Inhaltsblock verwenden und Zielgruppen mit bestimmten Sprachen ansprechen, müssen Sie jede Zielsprache in Ihrer CSV-Datei auflisten. Andernfalls wird beim Senden der Bereitstellung ein Fehler ausgegeben.

## Einfügen des Felds &quot;Personalisierung&quot;in die CSV-Datei {#personalization-field-csv}

Wenn Sie Personalisierungsfelder verwenden möchten, sollten Sie <span> Tag in die Datei aufnehmen.

Um das Personalisierungsfeld &quot;firstName&quot;in messageBody einzufügen, muss die Nachricht wie folgt lauten:

```
 "Hello <span class="nl-dce-field nl-dce-done"  data-nl-expr="/context/profile/firstName">First name</span>, this is message".
```

Das Feld &quot;firstName&quot;wird wie folgt dargestellt:

```
 <span class="nl-dce-field nl-dce-done" data-nl-expr="/context/profile/firstName">First name</span>
```

Im Bereich gibt es zwei obligatorische Attribute:

* Eine ist eine Klasse, die statisch ist. Unabhängig davon, welches Personalisierungsfeld Sie verwenden möchten, ist es immer class=&quot;nl-dce-field nl-dce-done&quot;.

* Ein weiteres Beispiel ist data-nl-expr, der Pfad des Personalisierungsfelds. Wenn Sie z. B. das Personalisierungsfeld &quot;firstName&quot;aus der Benutzeroberfläche einfügen, lautet der Navigationspfad **[!UICONTROL Context (context)]** > **[!UICONTROL Profile (profile)]** > **[!UICONTROL First name (firstName)]** (siehe Abbildung unten). In diesem Fall lautet der Pfad

   ```
   /context/profile/firstName. data-nl-expr="/context/profile/firstName".
   ```

![](assets/multilingual_push_2.png)

## Gebietsschema- und Sprachnamen {#locale-language-names}

Die folgenden Sprachen werden unterstützt:

| Gebietsschema | Sprache |
|:-:|:-:|
| af_za | Afrikaans - Südafrika |
| sq_al | Albanisch - Albanien |
| ar_dz | Arabisch – Algerien |
| ar_bh | Arabisch – Bahrain |
| ar_iq | Arabisch – Irak |
| ar_il | Arabisch – Israel |
| ar_jo | Arabisch – Jordanien |
| ar_kw | Arabisch – Kuwait |
| ar_lb | Arabisch – Libanon |
| ar_ma | Arabisch – Marokko |
| ar_om | Arabisch – Oman |
| ar_qa | Arabisch – Katar |
| ar_sa | Arabisch – Saudi-Arabien |
| ar_sy | Arabisch - Syrien |
| ar_tn | Arabisch – Tunesien |
| ar_ae | Arabisch – Vereinigte Arab. Emirate |
| ar_ye | Arabisch – Jemen |
| hy_am | Armenisch - Armenien |
| az_az | Aserbaidschanisch - Aserbaidschan |
| be_by | Weißrussisch - Belarus |
| bs_ba | Bosnisch - Bosnien |
| bg_bg | Bulgarisch - Bulgarien |
| ca_es | Katalanisch - Spanien |
| zh_cn | Chinesisch (vereinfacht) – China |
| zh_sg | Chinesisch (vereinfacht) – Singapur |
| zh_hk | Chinesisch (traditionell) - Hongkong SAR of China |
| zh_tw | Chinesisch (traditionell) - Taiwan-Region |
| hr_hr | Kroatisch - Kroatien |
| cs_cz | Tschechisch - Tschechien |
| da_dk | Dänisch - Dänemark |
| nl_be | Niederländisch – Belgien |
| nl_nl | Holländisch – Niederlande |
| en_au | Englisch – Australien |
| en_bz | Englisch - Belize |
| en_ca | Englisch – Kanada |
| en_in | Englisch – Indien |
| en_ie | Englisch – Irland |
| en_jm | Englisch - Jamaika |
| en_nz | Englisch – Neuseeland |
| en_ph | Englisch - Philippinen |
| en_za | Englisch – Südafrika |
| en_tt | Englisch - Trinidad und Tobago |
| en_gb | Englisch – Vereinigtes Königreich |
| en_us | Englisch – USA |
| en_zw | Englisch - Simbabwe |
| et_ee | Estnisch - Estland |
| fi_fi | Finnisch - Finnland |
| fr_be | Französisch – Belgien |
| fr_ca | Französisch – Kanada |
| fr_fr | Französisch – Frankreich |
| fr_lu | Französisch – Luxemburg |
| fr_ch | Französisch – Schweiz |
| de_at | Deutsch – Österreich |
| de_de | Deutsch – Deutschland |
| de_lu | Deutsch – Luxemburg |
| de_ch | Deutsch – Schweiz |
| el_cy | Griechisch – Zypern |
| el_gr | Griechisch – Griechenland |
| gu_in | Gujarati - Indien |
| he_il | Hebräisch - Israel |
| hi_in | Hindi - Indien |
| hu_hu | Ungarisch - Ungarn |
| is_is | Isländisch - Island |
| id_id | Indonesisch - Indonesien |
| it_it | Italienisch – Italien |
| it_ch | Italienisch – Schweiz |
| ja_jp | Japanisch - Japan |
| kn_in | Kannada - Indien |
| kk_kz | Kasachisch - Kasachstan |
| ko_kr | Koreanisch – Südkorea |
| lv_lv | Lettisch - Lettland |
| lt_lt | Litauisch - Litauen |
| mk_mk | Mazedonisch - Mazedonien |
| ms_my | Malaiisch - Malaysia |
| mr_in | Marathi - Indien |
| no_no | Norwegisch - Norwegen |
| pl_pl | Polnisch - Polen |
| pt_br | Portugiesisch – Brasilien |
| pt_pt | Portugiesisch – Portugal |
| pa_in | Pandschabi - Indien |
| ro_md | Rumänisch – Moldawien |
| ro_ro | Rumänisch – Rumänien |
| ru_kz | Russisch - Kasachstan |
| ru_ru | Russisch – Russland |
| ru_ua | Russisch – Ukraine |
| a_in | Sanskrit - Indien |
| sr_ba | Serbisch - Bosnien |
| sr_rs | Serbisch - Serbien |
| sk_sk | Slowakisch - Slowakei |
| sl_si | Slowenisch - Slowenien |
| es_ar | Spanisch – Argentinien |
| es_bo | Spanisch – Bolivien |
| es_cl | Spanisch – Chile |
| es_co | Spanisch – Kolumbien |
| es_cr | Spanisch – Costa Rica |
| es_do | Spanisch – Dominikanische Republik |
| es_ec | Spanisch – Ecuador |
| es_sv | Spanisch – El Salvador |
| es_gt | Spanisch – Guatemala |
| es_hn | Spanisch – Honduras |
| es_mx | Spanisch – Mexiko |
| es_ni | Spanisch – Nicaragua |
| es_pa | Spanisch – Panama |
| es_py | Spanisch – Paraguay |
| es_pe | Spanisch – Peru |
| es_pr | Spanisch – Puerto Rico |
| es_es | Spanisch – Spanien |
| es_uy | Spanisch – Uruguay |
| es_ve | Spanisch – Venezuela |
| sw_ke | Swahili - Kenia |
| sv_fi | Schwedisch – Finnland |
| sv_se | Schwedisch – Schweden |
| ta_in | Tamil - Indien |
| tt_ru | Tatar - Russisch |
| te_in | Telugu - Indien |
| th_th | Thai - Thailand |
| tr_cy | Türkisch – Zypern |
| tr_tr | Türkisch – Türkei |
| uk_ua | Ukrainisch - Ukrainisch |
| ur_in | Urdu – Indien |
| ur_pk | Urdu – Pakistan |
| vi_vn | Vietnamesisch - Vietnam |