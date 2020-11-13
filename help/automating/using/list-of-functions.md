---
title: Funktionsliste
description: Der Abfrageeditor bietet die Möglichkeit, fortgeschrittene Funktionen zur Erstellung komplexer Filter zu verwenden.
page-status-flag: never-activated
uuid: fd50fc99-1e7a-479b-beb7-1f246b419d46
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: filtering-data
discoiquuid: 3cdbe962-1c59-4cd8-b29e-36aa2562fac6
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '1942'
ht-degree: 100%

---


# Funktionsliste{#list-of-functions}

## Über Funktionen {#about-functions}

Der Abfrageeditor bietet die Möglichkeit, fortgeschrittene Funktionen zur Erstellung komplexer Filter zu verwenden. Auf diese können Sie in der Palette über das Element **[!UICONTROL Ausdruck]** zugreifen. Weiterführende Hinweise hierzu finden Sie in einem [gesonderten Abschnitt](../../automating/using/advanced-expression-editing.md).

Ziehen Sie das Element in den Workflow-Arbeitsbereich und geben Sie die gewünschte Funktion manuell ein. Unten stehend finden Sie eine Liste der kompatiblen Funktionen.

Je nach gesuchtem Ergebnis und verwendeten Daten stehen verschiedene Arten an Funktionen zur Verfügung:

* Datum-Funktionen
* Geomarketing
* Numerische Funktionen
* Sonstige Funktionen
* Aggregate
* String-Funktionen
* Sortierungs-Funktionen

>[!NOTE]
>
>Es stehen zusätzliche Funktionen in allen Aktivitäten zur Verfügung, die die Verwendung von Ereignisvariablen nach dem Aufruf eines Workflows mit externen Parametern ermöglichen. Weitere Informationen dazu finden Sie in [diesem Abschnitt](../../automating/using/customizing-workflow-external-parameters.md).

## Datumsangaben {#dates}

Die Datumsfunktionen dienen der Manipulation von Datums- oder Uhrzeitwerten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Tagen hinzu<br /> </td> 
   <td> AddDays(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Stunden hinzu<br /> </td> 
   <td> AddHours(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Minuten hinzu<br /> </td> 
   <td> AddMinutes(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Monaten hinzu<br /> </td> 
   <td> AddMonths(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Sekunden hinzu<br /> </td> 
   <td> AddSeconds(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> Fügt dem Datum eine Anzahl an Jahren hinzu<br /> </td> 
   <td> AddYears(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> Gibt nur das Datum aus (mit Uhrzeit = 00:00 Uhr)<br /> </td> 
   <td> DateOnly(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> Gibt die Zahl aus, die dem Tag des Datums entspricht<br /> </td> 
   <td> Day(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> Gibt die Zahl des Tages im Jahr des angegebenen Datums aus.<br /> </td> 
   <td> DayOfYear(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> Gibt das Datum aus, das dem aktuellen Datum abzüglich n Tage entspricht.<br /> </td> 
   <td> DaysAgo(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> Gibt das Datum (Integer JJJJMMTT) aus, das dem aktuellen Datum abzüglich n Tage entspricht.<br /> </td> 
   <td> DaysAgoInt(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> Anzahl von Tagen zwischen zwei Daten<br /> </td> 
   <td> DaysDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> Gibt das Alter in Tagen in Bezug auf ein Datum aus<br /> </td> 
   <td> DaysOld(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> Gibt das aktuelle Systemdatum des Servers aus<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> Gibt die Stunde der im Datum angegebenen Uhrzeit aus<br /> </td> 
   <td> Hour(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Stunden zwischen zwei Daten aus<br /> </td> 
   <td> HoursDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>LocalToUTC</strong><br /> </td> 
   <td> Konvertiert lokales Datum und die Uhrzeit in UTC<br /> </td> 
   <td> LocalToUTC(&lt;Datum&gt;, &lt;Zeitzone&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> Gibt die Minuten der im Datum angegebenen Uhrzeit aus<br /> </td> 
   <td> Minute(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Minuten zwischen zwei Daten aus<br /> </td> 
   <td> MinutesDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> Gibt die Zahl aus, die dem Monat des Datums entspricht<br /> </td> 
   <td> Month(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> Gibt das Datum aus, das dem aktuellen Datum abzüglich n Monate entspricht<br /> </td> 
   <td> MonthsAgo(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Monaten zwischen zwei Daten aus<br /> </td> 
   <td> MonthsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> Gibt das Alter in Monaten in Bezug auf ein Datum aus<br /> </td> 
   <td> MonthsOld(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> Gibt die Sekunden der im Datum angegebenen Uhrzeit aus<br /> </td> 
   <td> Second(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> Gibt das älteste Datum aus </td> 
   <td> Oldest(&lt;Datum&gt;, &lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Sekunden zwischen zwei Daten aus<br /> </td> 
   <td> SecondsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Tagen vom Datum ab<br /> </td> 
   <td> SubDays(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Stunden vom Datum ab<br /> </td> 
   <td> SubHours(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Minuten vom Datum ab<br /> </td> 
   <td> SubMinutes(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Monaten vom Datum ab<br /> </td> 
   <td> SubMonths(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Sekunden vom Datum ab<br /> </td> 
   <td> SubSeconds(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> Zieht die angegebene Anzahl von Jahren vom Datum ab<br /> </td> 
   <td> SubYears(&lt;Datum&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> Konvertiert eine Angabe Datum+Uhrzeit in Datum alleine<br /> </td> 
   <td> ToDate(&lt;Datum + Uhrzeit&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> Konvertiert einen String in Datum+Uhrzeit<br /> </td> 
   <td> ToDateTime(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDateTimeWithTimezone</strong><br /> </td> 
   <td> Konvertiert einen String in Datum+Zeitzone.<br /> Beispiel: ToDateTimeWithTimezone ("2019-02-19 08:09:00", "Asia/Tehran")<br /> </td> 
   <td> ToDateTimeWithTimezone(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> Kürzt die Angabe Datum+Uhrzeit auf Sekunden<br /> </td> 
   <td> TruncDate(@lastModified, &lt;Anzahl Sekunden&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> Kürzt die Angabe Datum+Uhrzeit auf Sekunden<br /> </td> 
   <td> TruncDateTZ(&lt;Datum&gt;, &lt;Anzahl Sekunden&gt;, &lt;Zeitzone&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> Kürzt die Angabe des Datums auf den ersten Tag des Quartals<br /> </td> 
   <td> TruncQuarter(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> Kürzt die Uhrzeitangabe auf Sekunden<br /> </td> 
   <td> TruncTime(&lt;Datum&gt;, &lt;Anzahl Sekunden&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> Kürzt ein Datum auf die Woche<br /> </td> 
   <td> TruncWeek(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> Kürzt die Angabe Datum+Uhrzeit auf den ersten Januar des Jahres<br /> </td> 
   <td> TruncYear(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> Gibt die Zahl des Wochentags in Bezug auf das Datum aus (0=Montag, 6=Sonntag)<br /> </td> 
   <td> WeekDay(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> Gibt die Zahl aus, die dem Jahr des Datums entspricht<br /> </td> 
   <td> Year(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearAndMonth</strong><br /> </td> 
   <td> Gibt Jahr und Monat eines Datums aus<br /> </td> 
   <td> YearAndMonth(&lt;Datum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearsDiff</strong><br /> </td> 
   <td> Gibt die Anzahl von Jahren zwischen zwei Daten aus<br /> </td> 
   <td> YearsDiff(&lt;Enddatum&gt;, &lt;Startdatum&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> Gibt das Alter in Jahren in Bezug auf ein Datum aus<br /> </td> 
   <td> YearsOld(&lt;Datum&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Geomarketing    {#geomarketing}

Die Geomarketing-Funktionen dienen der Manipulation von geografischen Werten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Gibt die Entfernung zwischen zwei durch Längen- und Breitengrad bezeichneten Punkten in Kilometern aus (in Grad).<br /> </td> 
   <td> Distance(&lt;Längengrad A&gt;, &lt;Breitengrad A&gt;, &lt;Längengrad B&gt;, &lt;Breitengrad B&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Numerisch    {#numerical}

Die numerischen Funktionen dienen der Konversion von Text in Zahlen.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Gibt den absoluten Wert einer Zahl aus<br /> </td> 
   <td> Abs(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Gibt die kleinste ganze Zahl aus, die größer oder gleich der angegebenen Zahl ist<br /> </td> 
   <td> Ceil(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Gibt die größte ganze Zahl aus, die kleiner oder gleich der angegebenen Zahl ist<br /> </td> 
   <td> Floor(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Gibt die größere von zwei Zahlen aus<br /> </td> 
   <td> Greatest(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Gibt die kleinere von zwei Zahlen aus<br /> </td> 
   <td> Least(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Gibt den Rest der ganzzahligen Division von n1 durch n2 aus.<br /> </td> 
   <td> Mod(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Gibt das Verhältnis zwischen zwei Werten in Prozent aus<br /> </td> 
   <td> Percent(&lt;Zahl 1&gt;, &lt;Zahl 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Gibt einen Zufallswert aus<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Rundet eine Zahl auf n Dezimalstellen<br /> </td> 
   <td> Round(&lt;Zahl&gt;, &lt;Anzahl Dezimalstellen&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Gibt das Vorzeichen einer Zahl aus<br /> </td> 
   <td> Sign(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Konvertiert einen Integer in einen Real<br /> </td> 
   <td> ToDouble(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Konvertiert einen Real in einen 64-Bit-Integer<br /> </td> 
   <td> ToInt64(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Konvertiert einen Real in einen Integer<br /> </td> 
   <td> ToInteger(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Kürzt n1 auf n2 Dezimalstellen<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Sonstige    {#others}

In dieser Tabelle sind die restlichen verfügbaren Funktionen enthalten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Gibt den Wert 1 aus, wenn die Bedingung wahr ist, sonst den Wert 2<br /> </td> 
   <td> Case(When(&lt;Bedingung&gt;, &lt;Wert 1&gt;), Else(&lt;Wert 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Löscht das Flag aus dem Wert<br /> </td> 
   <td> ClearBit(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Gibt den Wert 2 aus, wenn der Wert 1 gleich null oder leer ist, sonst den Wert 1<br /> </td> 
   <td> Coalesce(&lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Gibt Wert 3 aus, wenn Wert 1 = Wert 2, sonst den Wert 4<br /> </td> 
   <td> Decode(&lt;Wert 1&gt;, &lt;Wert 2&gt;, &lt;Wert 3&gt;, &lt;Wert 4&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Gibt den Wert 1 aus (kann nur als Parameter der 'Case'-Funktion verwendet werden)<br /> </td> 
   <td> Else(&lt;Wert 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extrahiert die Domain einer E-Mail-Adresse<br /> </td> 
   <td> GetEmailDomain(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Ruft die URL des Mirrorseiten-Servers ab<br /> </td> 
   <td> GetMirrorURL(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Gibt den Wert 1 aus, wenn der Ausdruck wahr ist, sonst den Wert 2<br /> </td> 
   <td> Iif(&lt;Bedingung&gt;, &lt;Wert 1&gt;, &lt;Wert 2&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Gibt an, ob das Flag im Wert vorkommt<br /> </td> 
   <td> IsBitSet(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Gibt den Wert 2 aus, wenn der String leer ist, sonst den Wert 3<br /> </td> 
   <td> IsEmptyString(&lt;String&gt;, &lt;Wert 2&gt;, &lt;Wert 3&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Gibt einen Leerstring aus, wenn das Argument gleich null ist<br /> </td> 
   <td> NoNull(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Gibt die Zeilennummer aus<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Setzt das Flag im Wert<br /> </td> 
   <td> SetBit(&lt;Kennung&gt;, &lt;Flag&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen booleschen Wert<br /> </td> 
   <td> ToBoolean(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Gibt den Wert 1 aus, wenn die Bedingung wahr ist, sonst den Wert 2 (kann nur als Parameter der 'Case'-Funktion verwendet werden)<br /> </td> 
   <td> When(&lt;Bedingung&gt;, &lt;Wert 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>newUUID</strong><br /> </td> 
   <td> Gibt eine neue UUID aus<br /> </td> 
   <td> newUUID<br /> </td> 
  </tr> 
 </tbody> 
</table>

## String    {#string}

Die String-Funktionen dienen der Manipulation einer Reihe von Strings.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Gibt an, ob alle Parameter ungleich null und nicht leer sind<br /> </td> 
   <td> AllNonNull2(&lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Gibt an, ob alle Parameter ungleich null und nicht leer sind<br /> </td> 
   <td> AllNonNull3(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Gibt den ASCII-Wert des ersten Zeichens des Strings aus<br /> </td> 
   <td> Ascii(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Gibt das ASCII-Code-Zeichen 'n' aus<br /> </td> 
   <td> Char(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Gibt die Position des Strings 2 im String 1 aus.<br /> </td> 
   <td> Charindex(&lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>DataLength</strong><br /> </td> 
   <td> Gibt die Anzahl der Zeichen in einer Zeichenfolge aus<br /> </td> 
   <td> DataLength(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Gibt die n-te Zeile (beginnend bei 1) des Strings aus<br /> </td> 
   <td> GetLine(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Gibt den dritten Parameter aus, wenn die ersten beiden Parameter den gleichen Wert aufweisen, sonst wird der letzte Parameter ausgegeben.<br /> </td> 
   <td> IfEquals(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Gibt an, ob das als Parameter ausgegebene Memo gleich null ist<br /> </td> 
   <td> IsMemoNull(&lt;Memo&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Konkatenation von zwei als Parameter übergebenen Strings, fügt, wenn nötig, Leerstellen hinzu.<br /> </td> 
   <td> JuxtWords(&lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Konkatenation von drei als Parameter übergebenen Strings, fügt, wenn nötig, Leerstellen hinzu.<br /> </td> 
   <td> JuxtWords3(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Gibt den String linksseitig aufgefüllt aus<br /> </td> 
   <td> LPad(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zeichen&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Gibt die n ersten Zeichen des Strings aus<br /> </td> 
   <td> Left(&lt;String&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Gibt die Länge des Strings aus.<br /> </td> 
   <td> Length(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Gibt den String in Kleinbuchstaben aus<br /> </td> 
   <td> Lower(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Löscht die Leerstellen links vom String<br /> </td> 
   <td> Ltrim(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Gibt eine hexadezimale Darstellung des MD5-Schlüssels eines Strings aus<br /> </td> 
   <td> Md5Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Gibt an, ob das Memo den als Parameter übergebenen String enthält<br /> </td> 
   <td> MemoContains(&lt;Memo&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Gibt den String rechtsseitig aufgefüllt aus<br /> </td> 
   <td> RPad(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zeichen&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Ersetzt in einem String (1. Parameter) alle Vorkommnisse eines bestimmten String-Werts (2. Parameter) durch einen anderen String-Wert (3. Parameter)<br /> </td> 
   <td> Replace(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Gibt die n letzten Zeichen des Strings aus<br /> </td> 
   <td> Right(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Löscht die Leerstellen rechts vom String<br /> </td> 
   <td> Rtrim(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Berechnet den standardmäßigen <strong>SHA256</strong>-Hash für einen bestimmten UTF8-String<br /> </td> 
   <td> Sha256Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha384Digest</strong><br /> </td> 
   <td> Berechnet den standardmäßigen <strong>SHA384</strong>-Hash für einen bestimmten UTF8-String<br /> </td> 
   <td> Sha384Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Berechnet den standardmäßigen <strong>SHA512</strong>-Hash für einen bestimmten UTF8-String<br /> </td> 
   <td> Sha512Digest(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Gibt jedes Wort des Strings beginnend mit einem Großbuchstaben aus<br /> </td> 
   <td> Smart(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extrahiert aus dem String den Teilstring, der mit dem Zeichen n1 beginnt und die Länge n2 aufweist.<br /> </td> 
   <td> Substring(&lt;String&gt;, &lt;Start&gt;, &lt;Länge&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToIntlString</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen String<br /> </td> 
   <td> ToIntlString(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Konvertiert eine Zahl in einen String<br /> </td> 
   <td> ToString(&lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Gibt den String in Großbuchstaben aus<br /> </td> 
   <td> Upper(&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Gibt den Fremdschlüssel einer als erster Parameter übergebenen Relation aus, wenn die beiden anderen Parameter identisch sind<br /> </td> 
   <td> VirtualLink(&lt;Zahl&gt;, &lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Gibt den Fremdschlüssel (Text) einer als erster Parameter übergebenen Relation aus, wenn die beiden anderen Parameter identisch sind<br /> </td> 
   <td> VirtualLinkStr(&lt;String&gt;, &lt;Zahl&gt;, &lt;Zahl&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_aescbcDecrypt</strong><br /> </td> 
   <td> Entschlüsselt einen verschlüsselten Wert im HEX-Format mit dem Präfix "<strong>x</strong>" (1. Parameter) mithilfe eines Schlüssels im HEX-Format (2. Parameter) und eines Initialisierungsvektors im HEX-Format (3. Parameter)<br /> </td> 
   <td> encryption_aescbcDecrypt(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>encryption_aescbcEncrypt</strong><br /> </td> 
   <td> Nutzt den AES-Algorithmus (CBC-Blockmodus) zur Verschlüsselung einer Zeichenfolge (1. Parameter) mit einem Schlüssel (2. Parameter) und einem Initialisierungsvektor (3. Parameter). Der Schlüssel und der Initialisierungsvektor müssen in einer hexadezimalen Darstellung vorliegen (beginnend mit <strong>\x</strong>). Das Ergebnis wird in hexadezimaler Darstellung ohne <strong>\x</strong> dargestellt.<br /> Beachten Sie, dass die Schlüsselgröße 128 Bit, 192 Bit oder 256 Bit (16, 24, 32 hexadezimale Zeichen) betragen kann, wir aber die Verwendung von 256 Bit und einen zufälligen Initialisierungsvektor derselben Länge als Schlüssel empfehlen.<br /> </td> 
   <td> encryption_aescbcEncrypt(&lt;String&gt;, &lt;String&gt;, &lt;String&gt;)<br /> Beispiel: encryption_aescbcEncrypt(johndoe@example.com, "<strong>\x0123456789ABCDEF0123456789ABCDEF</strong>", "<strong>\x0123456789ABCDEFFEDCBA9876543210</strong>")<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Aggregate {#aggregates}

Aggregatfunktionen stehen ausschließlich bei der [Hinzufügung von Zusatzdaten](../../automating/using/query.md#enriching-data) ausgehend von einer **[!UICONTROL Abfrage]**-Aktivität in einem Workflow zur Verfügung.

Die Aggregatfunktionen dienen der Durchführung von Berechnungen zu einer Reihe von Werten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Avg</strong>, Durchschnitt<br /> </td> 
   <td> Gibt den Durchschnittswert einer Spalte vom Typ Zahl aus.<br /> </td> 
   <td> Avg(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Count</strong>, Zählung (ohne NULL)<br /> </td> 
   <td> Zählt die Werte ungleich null einer Spalte.<br /> </td> 
   <td> Count(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>CountAll</strong>, Zählung (alles)<br /> </td> 
   <td> Zählt alle Werte (einschließlich Nullwerte und Dubletten).<br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Countdistinct</strong>, Zählung (unterschiedliche Werte)<br /> </td> 
   <td> Zählt die unterschiedlichen Werte ungleich null einer Spalte.<br /> </td> 
   <td> Countdistinct(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Max</strong>, Maximum<br /> </td> 
   <td> Gibt den Höchstwert einer Spalte vom Typ Zahl, String oder Datum aus.<br /> </td> 
   <td> Max(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Min</strong>, Minimum<br /> </td> 
   <td> Gibt den Mindestwert einer Spalte vom Typ Zahl, String oder Datum aus.<br /> </td> 
   <td> Min(&lt;Wert&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sum</strong>, Summe<br /> </td> 
   <td> Gibt die Summe der Werte einer Spalte vom Typ Zahl aus.<br /> </td> 
   <td> Sum(&lt;Wert&gt;)<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Darstellung    {#representation}

Die Darstellungsfunktionen dienen der Ordnung von Werten.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Name</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
   <td> <strong>Syntax</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Absteigende Sortierung<br /> </td> 
   <td> Desc(&lt;Wert 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Sortiert das Ergebnis innerhalb der Partition<br /> </td> 
   <td> OrderBy(&lt;Wert 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partitioniert das Ergebnis einer Abfrage<br /> </td> 
   <td> PartitionBy(&lt;Wert 1&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Erzeugt eine Zeilennummer in Abhängigkeit von der Tabellenpartition und der Sortierreihenfolge Funktion wird für MySQL nicht unterstützt<br /> </td> 
   <td> RowNum(PartitionBy(&lt;Wert 1&gt;), OrderBy(&lt;Wert 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>

