---
title: Marken
description: Entdecken Sie alle verfügbaren Tools zum Verwalten Ihrer Markenidentitäten.
page-status-flag: never-activated
uuid: d66ac5a2-2ae1-4870-b48e-7f276744ffdd
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: cbb1dcec-3bc6-4013-87fa-27d0e5d32bf8
context-tags: branding,overview;branding,main
internal: n
snippet: y
translation-type: ht
source-git-commit: e18407ab4bf70caa417b16bbc645fd2c6ba1818b
workflow-type: ht
source-wordcount: '1030'
ht-degree: 100%

---


# Marken {#branding}

## Über Markenidentitäten {#about-brand-identity}

Jedes Unternehmen verfügt über Richtlinien bezüglich der Darstellung und technischen Charakteristika seiner Marke. Mit Adobe Campaign können Sie Spezifikationen festlegen, um Ihre Marke Ihren Kunden einheitlich zu präsentieren, von Logos bis hin zu technischen Aspekten, wie E-Mail-Absendern, URLs oder Domains.

Technische Administratoren haben die Möglichkeit, eine oder mehrere Marken zu definieren und auf die Identität der jeweiligen Marken bezogene Parameter zentral anzugeben, z. B.: das Logo der Marke, die Domain der Zugangs-URL zu den Landingpages, Einstellungen zum Nachrichten-Tracking. Mit Adobe Campaign können diese Marken erstellt und mit verschiedenen Nachrichten oder Landingpages verknüpft werden. Diese Konfiguration wird in Vorlagen vorgenommen.

## Marken konfigurieren und verwenden     {#configuring-and-using-brands}

Konfiguration und Verwendung von Marken basieren auf den folgenden Grundprinzipien:

1. Erstellung und Konfiguration der Marke - dieser Vorgang erfordert spezielle Berechtigungen und ist dem technischen Adobe-Campaign-Administrator vorbehalten.
1. Erstellung einer oder mehrerer Versand- und Landingpage-Vorlagen für die Marke. Lesen Sie diesbezüglich auch den Abschnitt [Vorlagen erstellen](../../start/using/marketing-activity-templates.md).
1. Erstellung von auf den Vorlagen basierenden Nachrichten und Landingpages. Lesen Sie diesbezüglich auch die Abschnitte [E-Mails erstellen](../../channels/using/creating-an-email.md) und [Landingpages erstellen](../../channels/using/designing-a-landing-page.md).

>[!IMPORTANT]
>
>Marken können nicht vom Endnutzer erstellt oder geändert werden. Diese Aktionen müssen von einem technischen Adobe-Campaign-Administrator vorgenommen werden. Bei Fragen wenden Sie sich an die Adobe-Kundenunterstützung.
>
>Multibranding kann nicht in Verbindung mit Transaktionsnachrichten verwendet werden. Weiterführende Informationen dazu finden Sie im Abschnitt [Transaktionsnachrichten und Branding](../../channels/using/about-transactional-messaging.md#permissions-and-branding).

Der Zugriff auf Marken erfolgt über das Menü **[!UICONTROL Administration > Instanzenkonfiguration > Markenkonfiguration]**.

Eine neu erstellte Marke ist standardmäßig nur für Benutzer sichtbar, denen der Administrator die entsprechenden Berechtigungen zugewiesen hat.

Eine **Marke** wird durch die folgenden Eigenschaften definiert:

* eine **Identität**, durch die Ihre Marke definiert und personalisiert wird. Dieser Bereich weist folgende Felder auf:

   ![](assets/branding_01.png)

   * **Titel** (in der Benutzeroberfläche sichtbar)
   * **Markenname**
   * **URL** und **Titel** der Marken-Website
   * **Markenlogo**

* **[!UICONTROL In Header-Parameter für ausgehende E-Mails]** kann der Inhalt für die Empfänger Ihrer Kampagnen personalisiert werden. Dieser Bereich weist folgende Felder auf:

   ![](assets/branding_04_header.png)

   * **Absender (E-Mail)** mit der E-Mail-Adresse der Marke.
   * **Absender (Name)** mit dem Namen der Marke.
   * **Antwortadresse (E-Mail)** mit der E-Mail-Adresse, an die der Kunde eine Antwort senden kann.
   * **Antwortadresse (Name)** mit dem Namen der Marke.
   * **Fehler (E-Mail)** mit der E-Mail-Adresse, die im Falle eines Fehlers verwendet werden soll.

   >[!IMPORTANT]
   >
   >Sollten nach der Aktualisierung der E-Mail-Header-Parameter Name und E-Mail-Adresse des Absenders in einer neuen, auf dieser Vorlage basierenden E-Mail nicht geändert sein, überprüfen Sie die erweiterten Parameter der Vorlage.

* **Öffentlicher Webserver** wird sowohl zu Tracking-Zwecken als auch für den Zugriff auf die Landingpage verwendet. Dieser Bereich weist folgende Felder auf:

   ![](assets/configure_branding_04.png)

   * Die **Externe URL des Anwendungsservers**, die verwendet wird, um die verschiedenen erstellten Landingpages zu hosten und darauf zuzugreifen.
   * Die **Externe URL des Tracking-Servers**, die bei den Sendungen als getrackte URL verwendet werden soll.
   * Die **Externe URL des Mirrorseiten-Servers**, die bei Ihren Sendungen als standardmäßige Mirrorseite verwendet werden soll.

   >[!NOTE]
   >
   >Um die Vorschau der Landingpage und das Rendering der Mirrorseite in der Campaign-Benutzeroberfläche anzuzeigen, müssen die URLs für den Anwendungsserver und den Server der Mirrorseite sicher sein. Verwenden Sie in diesem Fall beim Einrichten dieser URLs https:// anstelle von http://.

* **[!UICONTROL In Konfiguration der Tracking-URLs (Web Analytics)]** wird das Tracking der URLs Ihrer Marke konfiguriert.

   Geben Sie hier die zusätzlichen Parameter an, die das Tracking von Links mithilfe externer Systeme, insbesondere Web-Analytics-Tools wie beispielsweise Adobe Analytics oder Google Analytics, ermöglichen.

   ![](assets/branding_05.png)

## Marke einer E-Mail zuweisen     {#assigning-a-brand-to-an-email}

### Marken mit einer Vorlage verknüpfen {#linking-a-brand-to-a-template}

Um die für eine Marke definierten Parameter nutzen zu können, muss sie mit einer Versand- oder Landingpage-Vorlage verknüpft sein. Dafür ist die Erstellung oder Anpassung einer Vorlage erforderlich.

>[!NOTE]
>
>Weiterführende Informationen zur Erstellung von Vorlagen finden Sie im Abschnitt [Vorlagen erstellen](../../start/using/marketing-activity-templates.md).

Nach der Erstellung Ihrer Vorlage können Sie sie mit einer Marke verknüpfen. Gehen Sie wie folgt vor:

1. Greifen Sie mithilfe der Schaltfläche **[!UICONTROL Eigenschaften bearbeiten]** auf die Eigenschaften Ihrer Vorlage zu.

   ![](assets/branding_04.png)

1. Wählen Sie mithilfe der Dropdown-Liste die Marke aus, die Sie mit der Vorlage verknüpfen möchten.

   >[!NOTE]
   >
   >Standardmäßig ist die **[!UICONTROL Standardmarke (branding)]** ausgewählt.

   ![](assets/branding_05.png)

   Verwenden Sie das Symbol **[!UICONTROL Zur Detailansicht des ausgewählten Elements weiterleiten]**, um genauere Informationen zur Markenkonfiguration angezeigt zu bekommen.

   ![](assets/branding_06.png)

1. Bestätigen Sie Ihre Auswahl und speichern Sie die Vorlage.

Ihre Vorlage ist nun mit der Marke verknüpft. Im E-Mail-Editor werden die für die Marke konfigurierten Daten in den Feldern **Standard-E-Mail-Adresse des Absenders**, **Name des Standard-Absenders** oder **Logo** verwendet.

### Anwendungsbeispiel für Branding     {#branding-use-case}

Im folgenden Beispiel geht es um die Erstellung einer neuen Marke zum Thema Reisen und ihre anschließende Verwendung in einer E-Mail.

#### Neue Marke konfigurieren     {#configure-a-new-brand}

>[!IMPORTANT]
>
>Die Markenkonfiguration wird ausschließlich von Adobe verwaltet, da dies spezielle Berechtigungen und technische Einstellungen erfordert.

1. Der Adobe Campaign-Administrator erstellt die Marke unter **[!UICONTROL Administration > Instanzenkonfiguration > Markenkonfiguration]**. Er fügt das Element **Tropenreise** hinzu und konfiguriert die **[!UICONTROL Identität]** sowie die **[!UICONTROL Header-Parameter für ausgehende E-Mails]** der Marke.

   ![](assets/branding_07.png)

1. Anschließend konfiguriert er für den Fall der Verwendung von Landingpages die URL für **Öffentlicher Webserver** und schließlich die Tracking-URLs.

   Das in unserem Beispiel verwendete **Web-Analytics**-Tool ist **Google Analytics**. Der Administrator konfiguriert die Tracking-URLs folgendermaßen:

   ![](assets/branding_12.png)

Die Marke wurde korrekt erstellt und konfiguriert. Sie ist nun zur Verwendung durch Marketingteams verfügbar.

#### Neue Marke implementieren     {#implement-a-new-brand}

Der Versandbeauftragte ist für die Erstellung der Versandvorlagen verantwortlich, in denen die neue Marke verwendet wird. Gehen Sie dazu wie folgt vor:

1. Ausgehend vom erweiterten Menü duplizieren Sie in **[!UICONTROL Ressourcen > Vorlagen > Versandvorlagen]** eine native Vorlage, um daraufhin eine neue Versandvorlage zu konfigurieren.

   ![](assets/branding_08.png)

1. Um diese Vorlage mit der Marke **Tropenreise** zu verknüpfen, bearbeiten Sie die Eigenschaften der Vorlage und wählen Sie die Marke aus der Dropdown-Liste aus.

   ![](assets/branding_09.png)

1. Konfigurieren Sie diese E-Mail-Vorlage entsprechend der Markenidentität.
1. Nach Fertigstellung der Vorlage kann sie gespeichert werden.

   ![](assets/branding_10.png)

   Die Versandvorlage lässt sich nun zur Erstellung von E-Mails verwenden, die an eine Audience gesendet werden.

#### Die neue Marke in einem Versand verwenden     {#use-the-new-brand-in-a-delivery}

Um eine mit einer Marke verknüpfte E-Mail zu erstellen, gehen Sie wie folgt vor:

1. Wählen Sie die Schaltfläche **[!UICONTROL Erstellen]** im Menü **[!UICONTROL Marketingaktivitäten]** aus.

   ![](assets/branding_14.png)

1. Wählen Sie die Aktivität **[!UICONTROL E-Mail]** und dann die mit der neuen Marke verknüpfte Vorlage aus.

   ![](assets/branding_15.png)

1. Ihre E-Mail ist bereits konfiguriert. Sie haben die Möglichkeit, die Informationen der E-Mail zu überprüfen, bevor Sie sie mithilfe von Testprofilen testen und anschließend an Ihre Audience senden.

   ![](assets/branding_16.png)

