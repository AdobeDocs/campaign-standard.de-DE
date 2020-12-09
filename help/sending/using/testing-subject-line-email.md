---
solution: Campaign Standard
product: campaign
title: Betreffzeile einer E-Mail testen
description: Erfahren Sie, wie Sie die Betreffzeile einer E-Mail im Email Designer definieren.
audience: sending
content-type: reference
topic-tags: editing-email-content
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '1115'
ht-degree: 100%

---

# Betreffzeile einer E-Mail testen {#testing-a-subject}


## Über die prädiktive E-Mail-Betreffzeile {#about-predictive-subject-line}

Beim Bearbeiten von E-Mails können Sie verschiedene Betreffzeilen ausprobieren und dabei eine jeweilige Einschätzung der Öffnungsrate erhalten, bevor Sie die E-Mail senden.

Diese Funktion ist standardmäßig deaktiviert. Sie wird beim Import des ersten Modells aktiviert. Bei einem Modell handelt es sich um das Ergebnis aus branchenspezifischen Trainingsdatensätzen. Durch Modelle kann das System bei der Unterbreitung neuer Betreffzeilen darauf bezogene Öffnungsraten für E-Mails voraussagen.

>[!NOTE]
>
>Diese Funktion ist ausschließlich für E-Mail-Nachrichten und Datenbanken mit englischen Inhalten verfügbar. Das trainierte Modell riskiert inkonsistent zu sein und fehlerhafte Ergebnisse zu erzeugen, wenn Ihre Instanz E-Mails beinhaltet, deren Inhalt in anderen Sprachen gehalten ist. Die Option zum Testen von Betreffs ist nur dann sichtbar, wenn in Ihrer Instanz bereits ein Modell verfügbar ist.

Weiterführende Informationen zum Importieren von Modellen finden Sie in diesem [Abschnitt](#importing-models).

## Testen der Betreffzeile {#testing-subject-line}

So testen Sie die Betreffzeile:

1. Erstellen Sie eine neue oder öffnen Sie eine bereits existierende E-Mail.
1. Gehen Sie in den Inhalt und geben Sie den Betreff der E-Mail im entsprechenden Eingabefeld ein.
1. Greifen Sie mithilfe der Schaltfläche **[!UICONTROL Betreff testen]** auf das Fenster **[!UICONTROL Testen Sie Ihre Betreffzeile]** zu. Der Betreff lässt sich in diesem Fenster noch anpassen.
1. Wählen Sie das passende Modell aus, das für die Voraussage der Öffnungsrate berücksichtigt werden soll. Es stehen verschiedene Modelle zur Verfügung, die jeweils einer speziellen Branche entsprechen. Weiterführende Informationen zur Verwendung von Modellen finden Sie in diesem [Abschnitt](#importing-models).
1. Klicken Sie auf **[!UICONTROL Testen]**.

Ihr Betreff wird nun analysiert.

>[!NOTE]
>
>Sollte die Betreffzeile zu kurz sein, kann keine Analyse durchgeführt werden und es wird eine Fehlermeldung angezeigt.

Bei der Analyse werden mehrere Indikatoren berechnet und es werden eine Reihe von Tools angezeigt, die Ihnen Anhaltspunkte zur Bearbeitung des Betreffs geben:

* **Erwartete Öffnungsrate**: Diese Grafik zeigt Ihnen, welche Öffnungsrate Sie mit Bezug auf den aktuellen Betreff Ihrer E-Mail erwarten können.
* **Länge des Betreffs**: Dieser Indikator zeigt an, ob der aktuelle Betreff die richtige Länge aufweist, oder ob er ggf. länger oder kürzer sein sollte.
* **Farbig markierte Wörter**: Beim Testen des Betreffs handelt es sich bei grün hervorgehobenen Stellen um die Wörter, die laut Voraussage am meisten zur Steigerung der Öffnungsrate beitragen. Bei rot hervorgehobenen Stellen handelt es sich um die Wörter, die laut Voraussage am wenigsten zur Steigerung der Öffnungsrate beitragen. Beim Hinzufügen oder Löschen von Wörtern im Betreff verschiebt sich von daher auch die Hervorhebung.
* **Kategorien und Wortvorschläge**: Im unteren Teil des Fensters werden eine Reihe für das ausgewählte Modell relevante Kategorien angezeigt. Die prioritär nach Wichtigkeit sortierten Kategorien helfen Ihnen zu erkennen, ob Ihr Betreff Wörter enthält, die einer jeweiligen Kategorie angehören, die in diesem Fall mit einem Häkchensymbol gekennzeichnet ist. Jede Kategorie enthält einen Satz an vorgeschlagenen Wörtern, die Sie in Ihrem Betreff verwenden können, um ihn genauer auf Zielgruppen zuzuschneiden und die Öffnungsrate zu steigern. Diese Wörter werden am meisten innerhalb einer bestimmten Kategorie verwendet.

>[!NOTE]
>
>Personalisierungsfelder und Satzzeichen werden bei der Analyse außen vor gelassen. Bei dynamischen/bedingten Inhalten werden alle Varianten als eine einzige Betreffzeile angesehen.

![](assets/predictive_subject_line_example.png)

## Modelle importieren       {#importing-models}

Auf Ihrem Adobe-Campaign-Server laufen Modelle nicht standardmäßig. Für den Erhalt eines Modells und die Aktivierung der Funktion gibt es zwei Möglichkeiten:

* Sie können ein lokales lernfähiges Modell mithilfe von Daten aus Ihren bisherigen E-Mail-Nachrichten trainieren.
* Sie haben die Möglichkeit, unter Verwendung der Funktion [Package-Import](../../automating/using/managing-packages.md) vortrainierte, für spezifische Branchen entwickelte Modelle zu importieren (Medizin etc.). 

### Trainieren eines lokalen Modells {#training-local-model}

* Wenn Sie bereits Adobe Campaign verwenden, wird das lokale Modell automatisch von in der Vergangenheit von Ihnen gesendeten Nachrichten lernen.
* Neue Adobe-Campaign-Nutzer können aus ihrem alten System/ESP eine CSV-Datei mit den folgenden vier Spalten extrahieren: Datum, Betreff, Öffnungen, Gesendet. Rufen Sie dazu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL E-Mail]** > **[!UICONTROL Betreffzeilenimport]** auf und führen Sie die Schritte auf den daraufhin angezeigten Bildschirmen aus. Importieren Sie nach Hochladen der Betreffs ein lokales Modell, wie weiter unten beschrieben. Das lokale Modell wird automatisch mit den hochgeladenen Daten trainiert.
* Wenn Sie als neuer Adobe Campaign-Nutzer keinen Zugang zu einer CSV-Datei wie der oben beschriebenen haben, können Sie entweder ein [vortrainiertes Modell](#pre-trained-models) verwenden oder solange warten, bis Sie in Ihrem System über ausreichend Versanddaten verfügen, mit deren Hilfe ein lokales lernfähiges Modell trainiert werden kann. Das System bestimmt automatisch, ob Ihr aktueller Datensatz ausreichend Daten zur Erkennung von Mustern und zum Training des lernfähigen Modells enthält.

>[!NOTE]
>
>Es gibt keine bestimmte Anzahl erforderlicher Betreffzeilen zum Trainieren Ihres eigenen Modells. Weiterführende Informationen dazu finden Sie unter [Fehlerbehebung](#troubleshooting).
>
>Ihre Instanz darf nur ein trainiertes Modell enthalten.

So trainieren Sie ein lokales Modell:
1. Laden Sie [hier](https://experience.adobe.com/#/downloads/content/software-distribution/en/campaign.html) das Modell „subjectLineTraining.xml“ herunter und verwenden Sie die Funktion [Package-Import](../../automating/using/managing-packages.md), um es in Ihre Adobe Campaign-Instanz hochzuladen. Das Training des lernfähigen Modells wird automatisch von einem technischen Workflow übernommen.
1. Wenn es das erste Mal ist, dass Sie ein Modell-Training vornehmen möchten, kann ein Administrator im Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** den Start des Workflows **[!UICONTROL SubjectLine Training]** (Betreff-Training-Workflow) erzwingen.
1. Nach dem Hochladen und Training eines lernfähigen Modells wird die Funktion automatisch aktiviert und neben dem für die Betreffzeile Ihrer Nachrichten vorgesehenen Feld wird eine neue Option angezeigt.
1. Der technische Workflow übernimmt dann automatisch das wöchentliche Training Ihres lernfähigen Modells.

### Importieren von vortrainierten Modellen {#pre-trained-models}

Klicken Sie [hier](https://experience.adobe.com/#/downloads/content/software-distribution/en/campaign.html), um auf diese Modelle zuzugreifen. Verwenden Sie die Funktion [Package-Import](../../automating/using/managing-packages.md), um ein Modell in Ihre Adobe Campaign-Instanz hochzuladen.

Folgende gebrauchsfertige Modelle stehen zur Verfügung:

* Kosmetikbranche: subjectInsightCosmetic.xml
* Supermarktbranche: subjectInsightSupermarket.xml
* Medizinbranche: subjectInsightMedical.xml
* Trainierbares Modell: subjectLineTraining.xml

Diese Modelle können nicht trainiert werden.

Nach dem Hochladen eines solchen Modells wird die Funktion automatisch aktiviert und neben dem für die Betreffzeile Ihrer Nachrichten vorgesehenen Feld wird eine neue Option angezeigt.

>[!NOTE]
>
>Der Import und die Erzeugung trainierter Modelle ist Administratoren vorbehalten.

## Fehlerbehebung {#troubleshooting}

Prädiktive Betreffzeile ist ein maschineller Lernprozess, bei dem alle Betreffzeilen, die Sie hochgeladen haben, gemeinsam mit ihren Öffnungsraten berücksichtigt werden. So kann das System bei der Übermittlung neuer Betreffzeilen darauf bezogene Öffnungsraten für E-Mails voraussagen.

Damit Sie Ihr eigenes Modell trainieren können, müssen die Betreffzeilen unabhängig von der Anzahl der Betreffzeilen, die zum Trainieren des Modells verwendet werden, variieren und dürfen keine Duplikate aufweisen.

Die Qualität der Betreffzeilen ist sehr wichtig. Wenn es nicht genügend hochwertige Daten für die Verarbeitung gibt oder alle früheren Betreffzeilen zu ähnlich sind, kann das System das Modell nicht trainieren und Sie erhalten möglicherweise eine Fehlermeldung. Das bedeutet, dass Ihre vorhandenen Datensätze keine zuverlässige Vorhersage ermöglichen.

In diesem Fall sollten Sie die hochgeladenen Daten prüfen und sicherstellen, dass die Betreffzeilen so unterschiedlich sind, dass sich Ihr Modell wirksam trainieren lässt.

<!--Some clients have reported this issue: I have had the subject line training workflow running for about a year now.  It has trained on 883 records and I am still seeing the message "The existing dataset is not enough to generate a model."  I do get an error in the workflow every time it runs "XML-110009 Unable to find the element 'runwf' of path '/' (document with schema 'serverConf')".

For this, campaign takes the subject line as training data and tries to come up with significant enough model to predict open rate with 95% confidence.

The 400 subject line number is mention with at least and is only indicative, model generation will also depend on quality of these lines.

It may happen that even 10k subject lines don't lead to model generation if they are too similar.

It means that it can be case that you don't have enough subject lines to generate the model and it is giving this error.

If you are getting an error/warning message, it means that your existing set of records is not enough for the predictive subject module to give a high confidence suggestion.

Adobe recommends reviewing the data you are uploading as the similarity of the subject lines might be the issue.-->
