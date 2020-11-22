---
solution: Campaign Standard
product: campaign
title: Datenschutzanfragen
description: Erfahren Sie, wie Sie Datenschutzanforderungen in Adobe Campaign Standard verwalten
audience: start
content-type: reference
topic-tags: discovering-the-interface
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1829'
ht-degree: 36%

---


# Managing Privacy requests {#privacy-requests}

For a general presentation on Privacy Management, refer to [this section](../../start/using/privacy-management.md).

Diese Informationen gelten für DSGVO, CCPA, PDPA und LGPD. Weitere Informationen zu diesen Verordnungen finden Sie in [diesem Abschnitt](../../start/using/privacy-management.md#privacy-management-regulations).

The opt-out for the Sale of Personal Information, which is specific to CCPA, is explained in [this section](#sale-of-personal-information-ccpa).

>[!IMPORTANT]
>
>Ab Version 19.4 wird die Verwendung der Campaign-API und -Benutzeroberfläche für Zugriffs- und Löschanfragen nicht mehr unterstützt. Für alle GDPR-, CCPA-, PDPA- oder LGPD Access- und Delete-Anforderungen müssen Sie die Integrationsmethode des [Privacy Core Service](#create-privacy-request) verwenden.

## Datenschutzanforderungen {#about-privacy-requests}

Um Ihnen die Datenschutzbereitschaft zu erleichtern, ermöglicht Ihnen Adobe Campaign die Bearbeitung von Zugriffs- und Löschanfragen. Das **Zugriffsrecht** und das **Recht auf Vergessen** (Löschungsanfrage) werden in [diesem Abschnitt](../../start/using/privacy-management.md#right-access-forgotten)beschrieben.

Um diese Anforderungen auszuführen, müssen Sie die Integration des **Datenschutz-Core-Service** verwenden. Datenschutzanforderungen, die vom Datenschutz-Core-Service an alle Experience Cloud-Lösungen gesendet werden, werden automatisch von der Kampagne über einen dedizierten Arbeitsablauf verarbeitet.

### Voraussetzungen {#prerequesites}

Adobe Campaign Angebots Data Controllers-Tools zum Erstellen und Verarbeiten von Datenschutzanforderungen für in Adobe Campaign gespeicherte Daten. Für den Kontakt mit den betroffenen Personen ist jedoch der Datenverantwortliche allein zuständig (über E-Mail, Kundenunterstützung oder ein Web-Portal).

Als Datenverantwortlicher sind Sie daher außerdem verpflichtet, die Identität der betroffenen Person zu überprüfen, die die Anfrage stellt, und sicherzustellen, dass die dem Anfragenden übermittelten Daten zur betroffenen Person gehören.

>[!NOTE]
>
>Weitere Informationen zu personenbezogenen Daten und zu den verschiedenen Entitäten, die Daten verwalten (Datenverantwortlicher, Auftragsverarbeiter und betroffene Person), finden Sie unter [Personenbezogene Daten und Personas](../../start/using/privacy.md#personal-data).

### Namensräume {#namesspaces}

Bevor Sie Datenschutzanforderungen erstellen, müssen Sie den zu verwendenden Namensraum definieren. Der Namespace ist der Schlüssel, anhand dessen die Identität der betroffenen Person in der Adobe Campaign-Datenbank identifiziert wird. Standardmäßig sind zwei Namespaces verfügbar: E-Mail und Mobiltelefon. Wenn Sie einen anderen Namespace benötigen (z. B. ein benutzerdefiniertes Profilfeld) führen Sie diese Schritte aus.

Also refer to this [tutorial](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/namespaces-for-privacy-requests.html?lang=en#privacy) on how to create a namespace.

>[!NOTE]
>
>Wenn Sie mehrere Namensraum verwenden, müssen Sie pro Namensraum eine Datenschutzanforderung erstellen.

1. Klicken Sie im Bildschirm oben links auf das Adobe Campaign-Logo und verwenden Sie dann die Schaltflächen **[!UICONTROL Administration]** > **[!UICONTROL Namensräume]**.

   ![](assets/privacy-namespaces.png)

1. Wählen Sie in der Liste der Namensräume die Option **[!UICONTROL Erstellen]**.

   ![](assets/privacy-namespace-create.png)

1. Geben Sie einen **[!UICONTROL Titel]** ein.

   ![](assets/privacy-namespace-label.png)

1. If you want to use an existing identity service namespace, choose **[!UICONTROL Map from Identity Namespace Service]** and select a namespace from the **[!UICONTROL Identity Service Namespaces]** list.

   ![](assets/privacy-map-from-namespace.png)

   If you want to create a new namespace in **[!UICONTROL Identity Service]** and map it in Campaign, select **[!UICONTROL Create new]** and enter a name in the **[!UICONTROL Identity namespace name]** field.

   ![](assets/privacy-create-new-namespace.png)

   Weitere Informationen zu Identitäts-Namensräumen finden Sie in der Dokumentation zur [Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=en) .

1. Ein Identitätsdienst-Namensraum wird einem Namensraum in der Kampagne zugeordnet. Sie müssen angeben, wie der Namensraum in der Kampagne abgeglichen werden soll.

   Wählen Sie ein Zielgruppen-Mapping aus (**[!UICONTROL Empfänger]**, **[!UICONTROL Echtzeit-Ereignis]** oder **[!UICONTROL Abonnements für eine Anwendung]**). Wenn Sie mehrere Zielgruppen-Mappings verwenden möchten, müssen Sie pro Zielgruppen-Mapping einen Namespace erstellen.

   ![](assets/privacy-namespace-target-mapping.png)

1. Wählen Sie den **[!UICONTROL Abstimmschlüssel]**. Das ist das Feld, das zur Identifikation des Datensubjekts in der Adobe Campaign-Datenbank herangezogen wird.

   ![](assets/privacy-namespace-reconciliation-key.png)

1. Wählen Sie **[!UICONTROL Erstellen]** aus. Sie können jetzt Datenschutzanforderungen auf Grundlage Ihres neuen Namensraums erstellen. Wenn Sie mehrere Namensraum verwenden, müssen Sie pro Namensraum eine Datenschutzanforderung erstellen.

### Creating a Privacy request {#create-privacy-request}

>[!IMPORTANT]
>
>The **Privacy Core Service** integration is the method you should use for all Access and Delete requests.
>
>Ab Version 19.4 wird die Verwendung der Campaign-API und -Benutzeroberfläche für Zugriffs- und Löschanfragen nicht mehr unterstützt. Verwenden Sie den Privacy Core Service für alle DSGVO-, CCPA-, PDPA- oder LGPD-Zugriffs- und Loschanfragen.

Mit der Integration des Datenschutzkerns können Sie Ihre Datenschutzanforderungen in einem Kontext mit mehreren Lösungen durch einen einzigen JSON-API-Aufruf automatisieren. Datenschutzanforderungen, die vom Datenschutz-Core-Service an alle Experience Cloud-Lösungen gesendet werden, werden automatisch von der Kampagne über einen dedizierten Arbeitsablauf verarbeitet.

Refer to the [Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en) documentation to learn how to create Privacy requests from the Privacy Core Service.

Jeder Hauptdienstauftrag zum Datenschutz wird in Kampagne in mehrere Datenschutzanfragen aufgeteilt, je nachdem, wie viele Namensraum verwendet werden, eine Anforderung, die einem Namensraum entspricht. Außerdem kann ein Auftrag auf mehreren Instanzen ausgeführt werden. Daher werden für einen Auftrag mehrere Dateien erstellt. Wenn sich eine Anfrage beispielsweise auf zwei Namespaces bezieht und drei Instanzen betrifft, werden insgesamt sechs Dateien gesendet. Eine Datei pro Namespace und Instanz.

The pattern for a file name is : `<InstanceName>-<NamespaceId>-<ReconciliationKey>.xml`

* **InstanceName**: der Name der Campaign-Instanz
* **NamespaceId**: Identitätsdienst-Namensraum-ID des verwendeten Namensraums
* **Abstimmschlüssel**: verschlüsselter Abstimmschlüssel

### Liste der Ressourcen {#list-of-resources}

When performing a Delete or Access Privacy request, Adobe Campaign searches all the Data Subject&#39;s data based on the **Reconciliation** value in all the resources that have a link to the profiles resource (own type).

Im Folgenden finden Sie die Liste der vordefinierten Ressourcen, die bei der Ausführung von Datenschutzanforderungen berücksichtigt werden:

* Profile (recipient)
* Versandlogs der Profile (broadLogRcp)
* Trackinglogs der Profile (trackingLogRcp)
* Versandlogs (App-Abonnements) (broadLogAppSubRcp)
* Trackinglogs (App-Abonnements) (trackingLogAppSubRcp)
* App-Abonnements (appSubscriptionRcp)
* Abonnementverlauf der Profile (subHistoRcp)
* Profilanmeldungen (subscriptionRcp)
* Besucher (visitor)

Wenn Sie benutzerdefinierte Ressourcen erstellt haben, für die eine Relation zur Profilressource (Typ „own“) besteht, werden auch diese berücksichtigt. Wenn Sie beispielsweise eine Transaktionen-Ressource haben, für die eine Relation mit der Profilressource vorhanden ist und eine Transaktionendetails-Ressource, für die eine Relation mit der Transaktionen-Ressource besteht, werden beide berücksichtigt.

Weitere Informationen zum Ändern benutzerdefinierter Ressourcen finden Sie in [diesem Tutorial](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/custom-resources-for-privacy-requests.html?lang=en#privacy).

Wählen Sie zu diesem Zweck in der benutzerdefinierten Ressource die Option **[!UICONTROL Das Löschen des Zieldatensatzes zieht das Löschen der durch die Relation referenzierten Datensätze nach sich]** aus:

1. Der Zugriff auf das entsprechende Menü erfolgt über das Adobe Campaign-Logo oben links im Bildschirm. Verwenden Sie dann die Schaltflächen **[!UICONTROL Administration]** > **[!UICONTROL Entwicklung]** > **[!UICONTROL Benutzerdefinierte Ressourcen]**.

1. Wählen Sie eine benutzerdefinierte Ressource aus, für die eine Relation zur Profilressource (Typ &quot;own&quot;) besteht.

1. Click the **[!UICONTROL Links]** section.

1. For each link, click the pencil icon (**[!UICONTROL Edit properties]**).

1. Wählen Sie im Bereich **[!UICONTROL Verhalten beim Löschen/Duplizieren]** die Option **[!UICONTROL Das Löschen des Zieldatensatzes zieht das Löschen der durch die Relation referenzierten Datensätze nach sich]** aus.

   ![](assets/privacy-cus-resource-option.png)

### Status von Datenschutzanfragen {#privacy-request-statuses}

Hier sind die verschiedenen Status für Datenschutzanforderungen:

* **[!UICONTROL Neu]** / **[!UICONTROL Erneuter Versuch steht aus]**: Durchführung läuft, der Workflow hat die Anfrage noch nicht verarbeitet.
* **[!UICONTROL Verarbeitungsvorgang läuft]** / **[!UICONTROL Erneuter Versuch läuft]**: Der Workflow verarbeitet gerade die Anfrage.
* **[!UICONTROL Löschen steht aus]**: Der Workflow hat alle zu löschenden Empfängerdaten identifiziert.
* **[!UICONTROL Löschvorgang läuft]**: Der Workflow führt gerade die Löschung durch.
   <!--**[!UICONTROL Delete Confirmation Pending]** (Delete request in 2-steps process mode): the workflow has processed the Access request. Manual confirmation is requested to perform the deletion. The button is available for 15 days.-->
* **[!UICONTROL Beendet]**: Die Verarbeitung der Anfrage wurde ohne Fehler abgeschlossen.
* **[!UICONTROL Fehler]**: beim Workflow ist ein Fehler aufgetreten. The reason is displayed in the list of Privacy requests in the **[!UICONTROL Request status]** column. For example, **[!UICONTROL Error data not found]** means that no recipient data matching the Data Subject&#39;s **[!UICONTROL Reconciliation value]** has been found in the database.

### Deaktivieren des zweistufigen Prozesses {#disabling-two-step-process}

Der zweistufige Prozess wird vom Privacy Core Service nicht unterstützt.

>[!IMPORTANT]
>
>Bevor Sie die Privacy Core Service-Integration zur Verwaltung Ihrer Datenschutzanfragen verwenden, müssen Sie den zweistufigen Prozess für Löschanfragen über die Campaign Standard-Benutzeroberfläche deaktivieren.

Wenn diese Option nicht deaktiviert wird, bleiben alle mit dem Privacy Core Service verwalteten Löschanfragen im Status &quot;Ausstehend&quot; und werden nicht abgeschlossen.

Standardmäßig ist der zweistufige Prozess aktiviert.

Um diesen Modus zu ändern, klicken Sie auf Eigenschaften **** bearbeiten, in der oberen rechten Ecke des Bildschirms **[!UICONTROL Datenschutzanforderungen]** und deaktivieren Sie dann die Option 2-Schritte-Prozess **** aktivieren.

![](assets/privacy-disable-2-step-process.png)

## Opt-out aus dem Verkauf von personenbezogenen Daten (CCPA) {#sale-of-personal-information-ccpa}

The **California Consumer Privacy Act** (CCPA) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

Die Konfiguration und Verwendung von Zugriffs- und Löschanforderungen gelten sowohl für GDPR- als auch für CCPA-Anforderungen. In diesem Abschnitt wird das Opt-out für den Verkauf personenbezogener Daten vorgestellt, das speziell für CCPA gilt.

In addition to the [Consent management](../../start/using/privacy-management.md#consent-management) tools provided by Adobe Campaign, you have the possibility to track whether a consumer has opted-out for the Sale of Personal Information.

Ein Verbraucher entscheidet über Ihr System, dass er nicht zulässt, dass seine persönlichen Daten an Dritte verkauft werden. In Adobe Campaign können Sie diese Informationen speichern und nachverfolgen.

>[!NOTE]
>
>Sie können das Opt-out über die Kampagne-Oberfläche und über die API nutzen. Sie können sie nicht über den Datenschutzzentrale-Dienst verwenden.

>[!IMPORTANT]
>
>Es liegt in Ihrer Verantwortung als Datenkontrolleur, die Anfrage des Datenbetreibers zu empfangen und die Daten der Anfrage für CCPA zu verfolgen. Als Technologieanbieter bieten wir nur eine Möglichkeit zum Ausschluss. Weitere Informationen zu Ihrer Rolle als Datenverantwortlicher finden Sie unter [Persönliche Daten und Personen](../../start/using/privacy.md#personal-data).

### Voraussetzungen für benutzerdefinierte Tabellen {#ccpa-prerequisite}

Starting 19.4, the **[!UICONTROL CCPA Opt-Out]** field is provided out-of-the-box in the Campaign interface and API. Standardmäßig ist das Feld für die **[!UICONTROL Standard-Profilressource]** verfügbar.

Wenn Sie eine benutzerdefinierte Profilressource verwenden, müssen Sie die Ressource erweitern und das Feld hinzufügen. We recommend that you use a different name than the out-of-the-box field, for example:  **[!UICONTROL Opt-Out for CCPA]** (optoutccpa). Wenn ein neues Feld erstellt wird, wird es automatisch von der Campaign-API unterstützt.

For more detailed information on how to extend the profile resource, see [this section](../../developing/using/extending-the-profile-resource-with-a-new-field.md).

>[!NOTE]
>
>Das Ändern von Ressourcen ist ein sensibler Vorgang, der nur von erfahrenen Benutzern ausgeführt werden muss.

1. Gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Entwicklung]** > **[!UICONTROL Benutzerspezifische Ressourcen]**. Klicken Sie auf die Ressource für das benutzerdefinierte Profil. For more on extending a resource, see [this section](../../developing/using/creating-or-extending-the-resource.md).

   ![](assets/privacy-ccpa-extend-cus.png)

1. Klicken Sie auf **[!UICONTROL Hinzufügen Feld]** oder **[!UICONTROL Element]** erstellen, fügen Sie die Beschriftung und ID hinzu und wählen Sie den **[!UICONTROL booleschen]** Typ. Verwenden Sie für den Namen **Ausschluss für CCPA**. Für die ID verwenden Sie: **optOutCcpa**.

   ![](assets/privacy-ccpa-extend-field.png)

1. Fügen Sie auf der Registerkarte &quot; **[!UICONTROL Bildschirmdefinition]** &quot;unter &quot;Konfiguration **[!UICONTROL des]** Detailbildschirms&quot;das Feld hinzu und wählen Sie &quot; **[!UICONTROL Eingabefeld]**&quot;aus. Dadurch wird das Feld in der Liste der Profile und den Details verfügbar.  For more on configuring the screen definition, see [this section](../../developing/using/configuring-the-screen-definition.md).

   ![](assets/privacy-ccpa-extend-screen.png)

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Publishing]**, prepare the publication and publish the modifications. For more on publishing a resource, see [this section](../../developing/using/updating-the-database-structure.md).

   ![](assets/privacy-ccpa-extend-pub.png)

1. Vergewissern Sie sich, dass das Feld in den Details eines Profils verfügbar ist. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#usage).

### Verwendung {#usage}

Es liegt in der Verantwortung des Datenkontrolleurs, den Wert des Feldes auszufüllen und die CCPA-Richtlinien und -Regeln für den Datenverkauf zu befolgen.

Um die Werte auszufüllen, können mehrere Methoden verwendet werden:

* Verwenden der Benutzeroberfläche der Kampagne durch Bearbeiten der Details des Empfängers (siehe unten)
* Using the Campaign Privacy API (see the [API documentation](../../api/using/managing-ccpa-opt-out.md))
* Über einen Workflow zum Datenimport

Sie sollten dann sicherstellen, dass Sie niemals personenbezogene Daten von Profilen, die sich gegen diese Regelung entschieden haben, an Dritte verkaufen.

1. Bearbeiten Sie auf der Benutzeroberfläche der Kampagne ein Profil, um den Abmeldestatus zu ändern.

   ![](assets/privacy-ccpa-profile-opt-out.png)

1. When the value of the field is **[!UICONTROL True]**, the information is displayed on the profile&#39;s details.

   ![](assets/privacy-ccpa-profile-opt-out-true.png)

1. Sie können die Liste &quot;Profil&quot;so konfigurieren, dass die Spalte &quot;Op-out&quot;angezeigt wird. Informationen zum Konfigurieren von Listen finden Sie in [diesem Abschnitt](../../start/using/customizing-lists.md).

   ![](assets/privacy-ccpa-profile-configure-list.png)

1. Sie können auf die Spalte klicken, um Empfänger gemäß den Ausschluss-Informationen zu sortieren.

   ![](assets/privacy-ccpa-profile-sorting.png)
