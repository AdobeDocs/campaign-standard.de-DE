---
title: Die wichtigsten Schritte zum Einrichten einer Landingpage
description: Hier erfahren Sie, wie Sie eine Landingpage einrichten.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Die wichtigsten Schritte zum Einrichten einer Landingpage{#main-steps-create-a-landing-page}

## Über die Erstellung von Landingpages

Dies sind die wichtigsten Schritte zum Einrichten einer Landingpage:

![](assets/lp_steps.png)

Auf dieser Seite finden Sie Informationen zu den einzelnen Schritten sowie Hinweise zu den jeweiligen Dokumentationen, denen Sie weitere Details entnehmen können.

## Landingpage-Vorlage konfigurieren{#configure-the-landing-page-template}

Bevor Sie eine Landingpage einrichten, müssen Sie zunächst eine Landingpage-Vorlage entsprechend Ihren Anforderungen konfigurieren. Alle auf dieser Vorlage basierenden Landingpages werden dadurch mit den gewünschten Parametern vorkonfiguriert.

1. Greifen Sie mithilfe des Adobe Campaign-Logos oben links im Bildschirm auf das erweiterte Menü **[!UICONTROL Ressourcen]** &gt; **[!UICONTROL Vorlagen]** &gt; **[!UICONTROL Landingpage-Vorlagen]** zu und duplizieren Sie die gewünschte Vorlage.
1. Geben Sie in den Vorlageneigenschaften die Parameter an, die alle Ihre Landingpages haben müssen. Beispiel: die Zielgruppendimension, die Seitenzugriffsparameter für identifizierte oder nicht identifizierte Besucher, Aktionen, die spezifisch für die Formularüberprüfung durch einen Besucher sind, die im Inhalt zu verwendende Marke/das Logo usw.
1. Speichern Sie Ihre Änderungen.

Weiterführende Informationen zu Landingpage-Vorlagen finden Sie in [diesem Abschnitt](../../channels/using/about-landing-pages.md).

![](assets/lp-steps1.png)

##  Landingpage erstellen und konfigurieren {#create-and-configure-the-landing-page}

Erstellen Sie ausgehend von der im vorangehenden Schritt definierten Vorlage eine neue Landingpage innerhalb des Programms oder der Kampagne Ihrer Wahl.

1. Erstellen Sie die Landingpage auf der Basis der gewünschten Vorlage.
1. Geben Sie die allgemeinen Parameter der Landingpage ein (Titel, Beschreibung usw.).
1. Sie werden anschließend zum Landingpage-Dashboard weitergeleitet. Bearbeiten Sie bei Bedarf die Eigenschaften der Landingpage. Standardmäßig sind die Eigenschaften diejenigen, die in der Landingpage-Vorlage konfiguriert wurden.
Wir empfehlen dringend, aus Gründen der Sicherheit und der Plattform-Leistung in den Eigenschaften der Landingpage ein Ablaufdatum einzurichten. Die Landingpage wird dadurch automatisch am ausgewählten Datum depubliziert. Weiterführende Informationen zu Gültigkeitsparametern finden Sie in [diesem Abschnitt](../../channels/using/sharing-a-landing-page.md#setting-up-validity-parameters).

   ![](assets/lp-steps3.png)

   >[!NOTE]
   >
   >Sollten Sie Änderungen vornehmen, gelten diese nur für die in Bearbeitung befindliche Landingpage. Wenn Sie die Änderungen auf andere Landingpages anwenden möchten, können Sie sie in einer dedizierten Vorlage vornehmen und von dieser Vorlage ausgehend andere Landingpages erstellen.

## Landingpage gestalten {#design-the-landing-page}

Jetzt können Sie den Inhalt der Landingpage definieren. Standardmäßig umfasst die Landingpage drei Seiten, auf die mithilfe der Scroll-Funktion zugegriffen werden kann: die Hauptseite mit dem Inhalt, eine Bestätigungsseite und eine Fehlerseite.

![](assets/lp-steps4.png)

Auf jeder Seite sind standardmäßig mehrere Felder konfiguriert. Bei Bedarf können Sie deren Eigenschaften und Zuordnung bearbeiten.

Sie können auch festlegen, wie sich die Bestätigungsschaltfläche verhält, wenn ein Profil darauf klickt, und den Inhalt entsprechend Ihren Anforderungen personalisieren (Bild, Personalisierungsfelder usw.). So können Sie den Vornamen eines Profils auf der Bestätigungsseite der Landingpage einfügen, um sich für die Registrierung zu bedanken.

Weiterführende Informationen zum Entwurf der Landingpage finden Sie in [diesem Abschnitt](../../channels/using/designing-a-landing-page.md).

## Landingpage testen {#test-the-landing-page}

Wenn die Landingpage fertig ist, können Sie simulieren, wie sie ausgeführt wird und sich verhält, wenn online auf sie zugegriffen wird.

![](assets/lp-steps5.png)

>[!CAUTION]
>
>Landingpage-Tests können nur mit Profilen und nicht mit Testprofilen durchgeführt werden. Wenn das Formular gesendet wird, werden die Daten des ausgewählten Profils aktualisiert. Um zu verhindern, dass echte Profile verändert werden, verwenden Sie ein erfundenes Kundenprofil.

Sollte das während des Tests beobachtete Verhalten zufriedenstellend sein, können Sie nun die Landingpage publizieren und sie damit online verfügbar machen.

Weiterführende Informationen zum Testen einer Landingpage finden Sie in [diesem Abschnitt](../../channels/using/sharing-a-landing-page.md#testing-the-landing-page-).

## Landingpage publizieren {#publish-the-landing-page}

Nach der zufriedenstellenden Ausführung der Tests können Sie unter Verwendung der Schaltfläche **[!UICONTROL Publizieren]** in der Symbolleiste des Dashboards die Landingpage online stellen. Die Kachel "Landingpage-Verfolgung" gibt Ihnen Auskunft über Fortschritt und Status der Publikation.

Durch die Publikation der Landingpage wird diese online verfügbar. Nach ihrer Publikation lässt sich die Landingpage weiterhin aktualisieren: Hierzu müssen Sie sie nach jeder Änderung erneut publizieren. Sie haben außerdem die Möglichkeit, Ihre Landingpage jederzeit zu depublizieren, damit sie nicht länger verfügbar ist.

![](assets/lp-steps6.png)

Nach der Publikation ist Ihre Landingpage zur Nutzung bereit. Sie können nun verschiedene Zugriffsmechanismen definieren, um entweder neue Profile für Ihre Datenbank oder zusätzliche Informationen zu bereits existierenden Profilen hinzuzugewinnen.

Weiterführende Informationen zum Publizieren von Landingpages finden Sie in [diesem Abschnitt](../../channels/using/sharing-a-landing-page.md#publishing-a-landing-page).
