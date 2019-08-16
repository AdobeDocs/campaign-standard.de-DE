---
title: Personalisierungsfeld einfügen
seo-title: Personalisierungsfeld einfügen
description: Personalisierungsfeld einfügen
seo-description: Hier erfahren Sie, wie Sie Felder aus der Datenbank, beispielsweise den Vornamen eines Profils, in Form von Platzhaltern in Ihren Inhalten verwenden.
page-status-flag: never-activated
uuid: 8f810c7f-2599-4fde-8422-4d261bea7db8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
discoiquuid: bd39406d-aa20-4f91-8fb8-2e4cdf112a85
internal: n
snippet: y
translation-type: ht
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Personalisierungsfeld einfügen{#inserting-a-personalization-field}

Adobe Campaign bietet die Möglichkeit, Felder aus der Datenbank, beispielsweise den Vornamen der Profile, in Form von Platzhaltern in Ihren Inhalten zu verwenden.

>[!NOTE]
>
>In den unten stehenden Bildern sehen Sie, wie Sie einen Link mit [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) einfügen können.

Um ein Personalisierungsfeld einzufügen, gehen Sie folgendermaßen vor:

1. Klicken Sie in einen Textbaustein und wählen Sie dann in der dedizierten Symbolleiste das **[!UICONTROL Personalisierungssymbol]** und danach **[!UICONTROL Personalisierungsfeld einfügen]** aus. Weiterführende Informationen zur Benutzeroberfläche von Email Designer finden Sie [in diesem Abschnitt](../../designing/using/about-email-content-design.md#email-designer-interface).

   ![](assets/email_perso_field_1.png)

1. Wählen Sie das Feld aus, das Sie in den Inhalt der Seite einfügen möchten.

   ![](assets/email_perso_field_2.png)

1. Wählen Sie **[!UICONTROL Bestätigen]**.

Der Name des Felds erscheint daraufhin hervorgehoben im Editor.

![](assets/email_perso_field_3.png)

Der entsprechende Platzhalter wird zum Zeitpunkt der Personalisierung (d. h. bei der Vorschauerzeugung, der E-Mail-Vorbereitung) durch den für das jeweilige Profil gespeicherten Wert aus der Datenbank ersetzt.

>[!NOTE]
>
>Bei von einem Workflow aus erstellten E-Mails stehen außerdem die innerhalb des Workflows berechneten Zusatzdaten in den Personalisierungsfeldern zur Verfügung. Weiterführende Informationen zur Hinzufügung von Zusatzdaten innerhalb von Workflows finden Sie im Abschnitt [Daten anreichern](../../automating/using/targeting-data.md#enriching-data).

