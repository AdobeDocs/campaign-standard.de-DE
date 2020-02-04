---
title: Betreffzeile einer E-Mail testen
description: Erfahren Sie, wie Sie die Betreffzeile einer E-Mail im Email Designer definieren.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: ht
source-git-commit: 0bc487606fe3715b20452f3cf8eae52900539a32

---

# Betreffzeile einer E-Mail testen {#testing-a-subject}

So testen Sie die Betreffzeile:

1. Erstellen Sie eine neue oder öffnen Sie eine bereits existierende E-Mail.
1. Gehen Sie in den Inhalt und geben Sie den Betreff der E-Mail im entsprechenden Eingabefeld ein.
1. Greifen Sie mithilfe der Schaltfläche **[!UICONTROL Betreff testen]**auf das Fenster**[!UICONTROL  Testen Sie Ihre Betreffzeile]** zu. Der Betreff lässt sich in diesem Fenster noch anpassen.
1. Wählen Sie das passende Modell aus, das für die Voraussage der Öffnungsrate berücksichtigt werden soll. Es stehen mehrere Modelle zur Verfügung, die jeweils einer speziellen Branche entsprechen.
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

## Modelle importieren  {#importing-models}

Auf Ihrem Adobe-Campaign-Server laufen Modelle nicht standardmäßig. Für den Erhalt eines Modells und die Aktivierung der Funktion gibt es zwei Möglichkeiten:

* Sie können ein lokales lernfähiges Modell mithilfe von Daten aus Ihren bisherigen E-Mail-Nachrichten trainieren:

   * Wenn Sie bereits Adobe Campaign verwenden, wird das lokale Modell automatisch von in der Vergangenheit von Ihnen gesendeten Nachrichten lernen.
   * Neue Adobe-Campaign-Nutzer können aus ihrem alten System/ESP eine CSV-Datei mit den folgenden vier Spalten extrahieren: Datum, Betreff, Öffnungen, Gesendet. Greifen Sie mithilfe des Adobe-Campaign-Logos oben links im Bildschirm und der Schaltflächen **[!UICONTROL Administration]** >**[!UICONTROL  Kanäle]** > **[!UICONTROL E-Mail]** >**[!UICONTROL  Betreffzeilenimport]** auf das entsprechende Menü zu und führen Sie die Schritte auf den daraufhin angezeigten Bildschirmen aus. Importieren Sie nach Hochladen der Betreffs ein lokales Modell, wie weiter unten beschrieben. Das lokale Modell wird automatisch mit den hochgeladenen Daten trainiert.
   * Wenn Sie als neuer Adobe-Campaign-Nutzer keinen Zugang zu einer CSV-Datei wie der oben beschriebenen haben, können Sie entweder ein vortrainiertes Modell verwenden oder solange warten, bis Sie in Ihrem System über ausreichend Versanddaten verfügen, mit deren Hilfe ein lokales lernfähiges Modell trainiert werden kann. Das System bestimmt automatisch, ob Ihr aktueller Datensatz ausreichend Daten zur Erkennung von Mustern und zum Training des lernfähigen Modells enthält.

      >[!NOTE]
      >
      >Es gibt keine bestimmte Anzahl erforderlicher Betreffzeilen zum Trainieren Ihres eigenen Modells. Um es trainieren zu können, müssen die Betreffzeilen unterschiedlich lauten und dürfen keine Dubletten haben. Sind nicht genügend Daten vorhanden, die verarbeitet werden können, ist das System nicht in der Lage, das lernfähige Modell zu trainieren. Ihre Instanz darf nur ein trainiertes Modell enthalten.
   Laden Sie zum Training eines lokalen lernfähigen Modells [hier](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) das Modell subjectLineTraining.xml herunter und verwenden Sie die Funktion [Package-Import](../../automating/using/managing-packages.md), um es in Ihre Adobe-Campaign-Instanz hochzuladen. Das Training des lernfähigen Modells wird automatisch von einem technischen Workflow übernommen.

   Wenn es das erste Mal ist, dass Sie ein Modell-Training vornehmen möchten, kann ein Administrator im Menü **[!UICONTROL Administration]**>**[!UICONTROL  Anwendungskonfiguration]** > **[!UICONTROL Workflows]**den Start des Workflows**[!UICONTROL  SubjectLine Training]** (Betreff-Training-Workflow) erzwingen.

   Nach dem Hochladen und Training eines lernfähigen Modells wird die Funktion automatisch aktiviert und neben dem für die Betreffzeile Ihrer Nachrichten vorgesehenen Feld wird eine neue Option angezeigt.

   Der technische Workflow übernimmt dann automatisch das wöchentliche Training Ihres lernfähigen Modells.

* Sie haben die Möglichkeit, unter Verwendung der Funktion [Package-Import](../../automating/using/managing-packages.md) vortrainierte, für spezifische Branchen entwickelte Modelle zu importieren (Medizin etc.). Diese Modelle sind [hier](https://support.neolane.net/webApp/downloadCenter?__userConfig=psaDownloadCenter) verfügbar und können nicht nachträglich trainiert werden.

   Nach dem Hochladen eines solchen Modells wird die Funktion automatisch aktiviert und neben dem für die Betreffzeile Ihrer Nachrichten vorgesehenen Feld wird eine neue Option angezeigt.

>[!NOTE]
>
>Der Import und die Erzeugung trainierter Modelle ist Administratoren vorbehalten.

Folgende gebrauchsfertige Modelle stehen zur Verfügung:

* Kosmetikbranche: subjectInsightCosmetic.xml
* Supermarktbranche: subjectInsightSupermarket.xml
* Medizinbranche: subjectInsightMedical.xml
* Trainierbares Modell: subjectLineTraining.xml
