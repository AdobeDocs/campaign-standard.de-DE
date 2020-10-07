---
title: Ausdrucksbearbeitung
description: Mit dem Abfrageeditor-Assistenten können Sie erweiterte Ausdrücke definieren.
page-status-flag: never-activated
uuid: a635f999-27ce-41e0-a88c-8a3882e31efe
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: filtering-data
discoiquuid: 4375153c-0621-4d4c-bfcc-66d157f04f6c
context-tags: queryFilter,overview;audience,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 100%

---


# Ausdrucksbearbeitung{#advanced-expression-editing}

## Über die Ausdrucksbearbeitung {#about-advanced-expression-editing}

Die Bearbeitung von Ausdrücken erfolgt durch die manuelle Eingabe von Bedingungen, die in ihrer Gesamtheit eine Regel bilden.

Diese Vorgehensweise ermöglicht die Verwendung fortgeschrittener Funktionen, über die Sie die verwendeten Werte (Datumsangaben, Strings, numerische Felder etc.) bearbeiten können, um spezifische Abfragen zu erstellen.

Es ist auch möglich, bei der Bearbeitung von Ausdrücken Workflow-Ereignisvariablen zu verwenden. Weiterführende Informationen dazu finden Sie im Abschnitt [Aktivitäten mit Ereignisvariablen anpassen](../../automating/using/customizing-workflow-external-parameters.md).

Die Ausdrucksbearbeitung findet in folgenden Fällen Verwendung:

* bei der Erstellung von Abfragen mithilfe der beim Hinzufügen einer Regel verfügbaren Option **[!UICONTROL Erweiterter Modus]**;

   ![](assets/expression_editor_2.png)

* beim Bearbeiten eines Ausdrucks in einem Workflow; beispielsweise beim Hinzufügen von Zusatzdaten in eine Aktivität;
* bei der Erstellung einer Sichtbarkeitsbedingung im HTML-Content-Editor. In diesem Fall handelt es sich um JavaScript-Ausdrücke. Die Verwendung der klassischen fortgeschrittenen Funktionen ist hier nicht möglich.

## Ausdruck bearbeiten  {#edit-an-expression}

Durch die Bearbeitung erweiterter Ausdrücke können Sie manuell Ausdrücke definieren, die Ihren spezifischen Bedürfnissen entsprechen.

Die Ausdrucksbearbeitung kann während der Erstellung einer E-Mail im Audience-Fenster oder während der Workflow-Erstellung in der Abfrage-Aktivität erfolgen.

1. Öffnen Sie den Ausdruckseditor in einem der im Abschnitt [Über die Ausdrucksbearbeitung](../../automating/using/advanced-expression-editing.md#about-advanced-expression-editing) beschriebenen Anwendungskontexte. Der Editor setzt sich aus folgenden Elementen zusammen:

   * Eingabefeld, in dem der Ausdruck erstellt wird;
   * Liste der verfügbaren Felder, die im Ausdruck verwendet werden können und die der Zielgruppendimension der Abfrage entsprechen (siehe auch [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources)).
   * Liste der verfügbaren Funktionen mit verschiedenen Unterkategorien.

   ![](assets/expression_editor_1.png)

1. Bearbeiten Sie den Ausdruck, indem Sie ihn direkt in das entsprechende Feld eingeben, oder unter Zuhilfenahme der verfügbaren Felder und der Funktionsliste.

   Durch einen Doppelklick auf ein Feld oder eine Funktion werden diese an der Stelle des Cursors in das Eingabefeld eingefügt.

   Es ist möglich, Workflow-Ereignisvariablen zur Erstellung eines Ausdrucks zu verwenden. Weiterführende Informationen dazu finden Sie im Abschnitt [Aktivitäten mit Ereignisvariablen anpassen](../../automating/using/customizing-workflow-external-parameters.md).

1. Benennen Sie gegebenenfalls Ihre Regel. Dieser Name erscheint dann anstelle des automatischen Namens im Arbeitsbereich des Abfragetools.

Durch die Bearbeitung eines Ausdrucks können Sie den Audiences-Ausdruck personalisieren und Ihre Population gezielter ansprechen.

**Verwandte Themen:**

* [Syntax von Ausdrücken](../../automating/using/advanced-expression-editing.md#expression-syntax)
* [Funktionsliste](../../automating/using/list-of-functions.md)

## Syntax von Ausdrücken  {#expression-syntax}

### Standardsyntax {#standard-syntax}

Standardausdrücke bestehen aus einer oder mehreren Bedingungen, die die folgende Syntax beachten müssen:

* Jede Bedingung hat die Form **&lt;Wert 1> &lt;Vergleichsoperator> &lt;Wert 2>**, wobei

   * **&lt;Wert 1>** ein Feld oder eine Funktion ist. Das Feld **@created** z. B. steht für das Erstellungsdatum eines Profils, die Funktion **Year(@created)** gibt das Jahr der Erstellung eines Profils aus.
   * **&lt;Vergleichsoperator>** ist einer der im Abschnitt [Vergleichsoperatoren](../../automating/using/advanced-expression-editing.md#comparison-operators) aufgelisteten Operatoren. Der Operator definiert die Art des Vergleichs zwischen **&lt;Wert 1>** und **&lt;Wert 2>**.
   * **&lt;Wert 2>** ein Feld, eine Funktion oder ein manuell angegebener Wert ist.

   >[!NOTE]
   >
   >Die Datentypen von **&lt;Wert 1>** und **&lt;Wert 2>** müssen identisch sein. Wenn **&lt;Wert 1>** beispielsweise ein Datum ist, muss **&lt;Wert 2>** auch ein Datum sein.

* Mithilfe von logischen Operatoren können verschiedene Bedingungen miteinander kombiniert werden.

   * **[!UICONTROL AND]**: erstellt die Schnittmenge aus zwei Bedingungen;
   * **[!UICONTROL OR]**: vereinigt die aus zwei Bedingungen resultierenden Elemente.

Beispiel:

```
Year(@created) = Year(GetDate()) AND Month(@created) = Month(GetDate())
```

In diesem Beispiel werden die Profile ausgegeben, bei denen das Erstellungsdatum mit dem aktuellen Jahr und Monat übereinstimmt.

### JavaScript-Syntax  {#javascript-syntax}

Bei der Definition von Sichtbarkeitsbedingungen in einem Textblock des HTML-Inhaltseditiors sind Ausdrücke mit JavaScript-Syntax zu verwenden.

JavaScript-Ausdrücke bestehen aus einer oder mehreren Bedingungen, die die folgende Syntax beachten müssen:

* Jede Bedingung hat die Form **&lt;Kontext> &lt;Vergleichsoperator> &lt;Wert 2>**, wobei

   * **&lt;Kontext>** einem Feld oder einer Funktion entspricht, die es ermöglichen, den Kontext anzugeben. Beispiel **context.profile.@email** steht für die E-Mail-Adresse eines Profils und **context.profile.firstName.length()** für die Anzahl an Zeichen des Vornamens eines Profils.
   * **&lt;Vergleichsoperator>** ist einer der im Abschnitt [Vergleichsoperatoren](../../automating/using/advanced-expression-editing.md#comparison-operators) aufgelisteten Operatoren. Der Operator definiert die Art des Vergleichs zwischen **&lt;Kontext>** und **&lt;Wert 2>**.
   * **&lt;Wert 2>** ein Feld, eine Funktion oder ein manuell angegebener Wert ist.

   >[!NOTE]
   Die Datentypen von **&lt;Kontext>** und **&lt;Wert 2>** müssen identisch sein. Wenn **&lt;Kontext>** beispielsweise ein Datum ist, muss **&lt;Wert 2>** auch ein Datum sein.

* Mithilfe von logischen Operatoren können verschiedene Bedingungen miteinander kombiniert werden.

   * **[!UICONTROL &amp;&amp;]**: erstellt die Schnittmenge aus zwei Bedingungen;
   * **[!UICONTROL ||]**: vereinigt die aus zwei Bedingungen resultierenden Elemente.

Beispiel:

```
context.profile.age > 21 && context.profile.firstName.length() > 0
```

In diesem Beispiel werden die Profile ausgegeben, die über 21 Jahre alt sind und deren Vorname angegeben ist (das Feld **firstName** enthält mindestens ein Zeichen).

## Vergleichsoperatoren  {#comparison-operators}

Bei manchen Regeln können Sie über den Abfrageeditor einen Wert auswählen.

Bedingung müssen mithilfe eines der folgenden Operatoren mit Werten verknüpft werden.

<table> 
 <thead> 
  <tr> 
   <th> Operator<br /> </th> 
   <th> Standardsyntax<br /> </th> 
   <th> JavaScript-Syntax<br /> </th> 
   <th> Beschreibung<br /> </th> 
   <th> Beispiel<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <span class="uicontrol">Gleich</span> <br /> </td> 
   <td> =<br /> </td> 
   <td> ==<br /> </td> 
   <td> Der erste Wert muss mit dem zweiten identisch sein.<br /> </td> 
   <td> <strong>@lastName = Martin</strong> gibt die Profile aus, deren Nachname exakt 'Martin' ist.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Größer als</span> <br /> </td> 
   <td> &gt;<br /> </td> 
   <td> &gt;<br /> </td> 
   <td> Der erste Wert muss streng größer als der zweite sein.<br /> </td> 
   <td> <strong>@age &gt; 50</strong> gibt alle Profile aus, deren Alter '50' übersteigt, also '51', '52' etc.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Niedriger als</span> <br /> </td> 
   <td> &lt;<br /> </td> 
   <td> &lt;<br /> </td> 
   <td> Der erste Wert muss streng kleiner als der zweite sein.<br /> </td> 
   <td> <strong>@created &lt; DaysAgo(100)</strong> gibt alle Profile aus, die vor weniger als 100 Tagen in der Datenbank erstellt wurden.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Größer oder gleich</span> <br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> &gt;=<br /> </td> 
   <td> Der erste Wert muss größer oder gleich dem zweiten sein.<br /> </td> 
   <td> <strong>@age &gt;= 30</strong> gibt alle Profile im Alter von 30 Jahren und älter aus.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Kleiner oder gleich</span> <br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> &lt;=<br /> </td> 
   <td> Der erste Wert muss kleiner oder gleich dem zweiten sein.<br /> </td> 
   <td> <strong>@age &lt;= 60</strong> gibt alle Profile im Alter von 60 Jahren und jünger aus.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Unterschiedlich </span> <br /> </td> 
   <td> !=<br /> </td> 
   <td> !=<br /> </td> 
   <td> Der erste Wert muss sich vom zweiten unterscheiden.<br /> </td> 
   <td> <strong>@Sprache != Englisch</strong> gibt alle Profile aus, für die im Feld Sprache nicht Englisch angegeben ist.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Enthält</span> <br /> </td> 
   <td> IN<br /> </td> 
   <td> K. A.<br /> </td> 
   <td> Der erste Wert muss den zweiten enthalten.<br /> </td> 
   <td> <strong>@domain IN mail</strong>. Hier werden alle Domains ausgegeben, deren Name den Wert 'mail' enthält. 'gmail.com' z. B. wird also in der Ergebnismenge enthalten sein.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Ist wie</span> <br /> </td> 
   <td> LIKE<br /> </td> 
   <td> K. A.<br /> </td> 
   <td> <span class="uicontrol">Ist wie</span> erzielt ähnliche Ergebnisse wie der Operator <span class="uicontrol">enthält. </span> Er ermöglicht jedoch die Verwendung des Platzhalters <span class="uicontrol">%</span> im gesuchten Wert.<br /> </td> 
   <td> <strong>@lastName LIKE Me%er</strong>. Hier erlaubt die Verwendung des Zeichens <strong>%</strong> die Ausgabe aller Profile mit Nachnamen Meyer, Meier, Meiser etc.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Ist nicht wie</span> <br /> </td> 
   <td> NOT<br /> </td> 
   <td> K. A.<br /> </td> 
   <td> Negative Form des Operators <span class="uicontrol">ist wie</span>. Hier dürfen die ausgegebenen Daten nicht dem angegebenen Wert ähneln. Auch in diesem Fall ist der Platzhalter <span class="uicontrol">%</span> zu verwenden.<br /> </td> 
   <td> <strong>@lastName NOT Schmi%t</strong>. Alle Empfänger mit Nachnamen Schmiedt, Schmidt, Schmitt etc. werden ausgeschlossen.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Ist leer</span> <br /> </td> 
   <td> IS NULL<br /> </td> 
   <td> K. A.<br /> </td> 
   <td> Der erste Wert muss einen Nullwert ausgeben.<br /> </td> 
   <td> <strong>@mobilePhone IS NULL</strong> gibt alle Profile aus, für die keine Mobiltelefonnummer angegeben wurde.<br /> </td> 
  </tr> 
 </tbody> 
</table>

