---
title: Über den Datenimport und -export
description: Hier erfahren Sie über die Möglichkeiten, mit Adobe Campaign Daten zu importieren und zu exportieren.
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
feature: Workflows
role: Data Architect
level: Experienced
exl-id: 208e8629-c3e2-4f36-bae7-46ffc3f56a1b
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 100%

---

# Über den Datenimport und -export{#about-data-import-and-export}

Je nach Ihren Anforderungen haben Sie mehrere Möglichkeiten, Daten mit Adobe Campaign zu importieren und exportieren:

* **Packages**: Packages sind XML-Dateien, mit denen Konfigurationen und Datensätze von einer Adobe-Campaign-Instanz zur einer anderen transferiert werden können. Auch Systemaktualisierungen werden mit Package-Importen durchgeführt.
* **Listen**: Alle Listenfenster können konfiguriert und die angezeigten Daten können in eine Datei exportiert werden.
* **Workflows**: Hier erfolgt der Import von Daten über Dateien, mit denen die Datenbank aktualisiert oder E-Mails gesendet werden können. Sie können auch Daten auswählen und in Dateien exportieren. Workflows sind die beste Möglichkeit, regelmäßige Aktualisierungen, wie etwa Profilimporte, automatisch durchzuführen.

   * Die Aktivität **[!UICONTROL Datei laden]** erlaubt den Import von strukturierten Dateidaten, um diese in Adobe Campaign verwenden zu können. Die importierten Daten werden nur vorübergehend gespeichert und erfordern die Verwendung einer weiteren Workflow-Aktivität, um definitiv in die Adobe Campaign-Datenbank integriert zu werden. Weiterführende Informationen zur Verwendung der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/load-file.md).
   * Die **[!UICONTROL Dateiübertragung]** dient dem Empfang und Versand von Dateien. Sie ermöglicht es zudem, das Vorhandensein von Dateien zu testen und die in Adobe Campaign enthaltenen Dateien aufzulisten. Sie können diese Aktivität vor der Aktivität **[!UICONTROL Datei laden]** verwenden, um die Datei von einer externen Quelle abzurufen. Weiterführende Informationen zur Verwendung der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/transfer-file.md).

Bei der Erstellung von Importprozessen empfiehlt es sich, Workflow-Vorlagen zu verwenden, die Sie nach Ihren Bedürfnissen anpassen können. Weiterführende Informationen zum Einrichten einer Workflow-Vorlage zum Importieren von Daten finden Sie in [diesem Anwendungsbeispiel](../../automating/using/creating-import-workflow-templates.md).

Adobe Campaign bietet auch eine einfache Möglichkeit, regelmäßige Importe durch die Erstellung von **Importvorlagen** durchzuführen. Importvorlagen sind Workflow-Vorlagen, die über ein spezielles Fenster abrufbar sind. Nach ihrer Erstellung muss der Benutzer, der den Import durchführt, nur mehr die zu importierende Datei in einer vereinfachten Ansicht hochladen.

**Verwandte Themen**:

* [Datenimport mit Importvorlagen](../../automating/using/importing-data-with-import-templates.md)
* [Importvorlagen konfigurieren](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates)
* [Package-Verwaltung](../../automating/using/managing-packages.md)
