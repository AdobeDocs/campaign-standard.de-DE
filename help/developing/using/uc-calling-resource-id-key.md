---
title: Aufrufen einer Ressource mit einem Composite-Identifizierungsschlüssel
seo-title: Aufrufen einer Ressource mit einem Composite-Identifizierungsschlüssel
description: Aufrufen einer Ressource mit einem Composite-Identifizierungsschlüssel
seo-description: Hier erfahren Sie, wie Sie eine Ressource mit einem Composite-Identifizierungsschlüssel aufrufen.
translation-type: tm+mt
source-git-commit: 8aea0483bcb1b104e5bd2b13426a1ac590c8efaf

---


# Aufrufen einer Ressource mit einem Composite-Identifizierungsschlüssel

In einigen Fällen müssen Sie möglicherweise für eine Ressource einen Identifikationsschlüssel definieren, der aus zwei Feldern besteht. Sobald der Identifizierungsschlüssel konfiguriert wurde, müssen Sie eine Filterdefinition konfigurieren, um die Ressource mit diesem Identifizierungsschlüssel entweder über die Kampagnenstandard-Oberfläche oder über apis aufzurufen.

In this use case, the **Profile** resource has been extended with custom **"CRM ID"** and **"category"** field. Wir erstellen einen Identifikationsschlüssel für die Profilressource, der aus diesen beiden Feldern besteht. Anschließend konfigurieren wir eine Filterdefinition, damit wir mithilfe des Identifizierungsschlüssels auf die Profilressource zugreifen können.

Die Hauptschritte für diesen Nutzungsfall sind:

1. Konfigurieren Sie den Identifikationsschlüssel für die Profilressource basierend auf den beiden Feldern.
1. Konfigurieren Sie die Filterdefinition, um die Profilressource mit dem Identifizierungsschlüssel aufzurufen.
1. Rufen Sie die Profilressource über die Schnittstelle oder über die apis auf.

Verwandte Themen:

* [Ressource erstellen oder erweitern](../../developing/using/creating-or-extending-the-resource.md)
* [Identifizierungsschlüssel definieren](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys)
* [Kampagnenstandard REST apis](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html)

## Schritt 1: Identifizierungsschlüssel konfigurieren

>[!NOTE]
> Global concepts when configuring identification keys are detailed in [this section](../../developing/using/configuring-the-resource-s-data-structure.md#defining-identification-keys).

1. Bevor Sie den Identifizierungsschlüssel konfigurieren, stellen Sie sicher, dass die Ressource mit den gewünschten Feldern erweitert wurde und dass sie veröffentlicht wurde. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../developing/using/creating-or-extending-the-resource.md).

1. Go to the **[!UICONTROL Administration]** / **[!UICONTROL Developement]** / **[!UICONTROL Custom resources]** menu, then open the **[!UICONTROL Profile]** resource.

   ![](assets/uc_idkey1.png)

1. In the **[!UICONTROL Identification keys]** section, click the **[!UICONTROL Create element]** button.

   ![](assets/uc_idkey2.png)

1. Add the two custom "CRM ID" and "Category" fields, then click **[!UICONTROL Confirm]**.

   ![](assets/uc_idkey3.png)

   >[!NOTE]
   > If you want to display the two custom fields in the profile's interface, configure the **[!UICONTROL Screen definition]** tab. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../developing/using/configuring-the-screen-definition.md).

1. Sie können nun die Filterdefinition konfigurieren, um die Ressource mit dem Identifizierungsschlüssel aufzurufen.

## Schritt 2: Filterdefinition konfigurieren

>[!NOTE]
> Global concepts when configuring filter definitions are detailed in [this section](../../developing/using/configuring-filter-definition.md).

1. In the **[!UICONTROL Filter definition]** tab, click **[!UICONTROL Add an element]**, then enter the filter definition's label and ID.

1. Bearbeiten Sie die Eigenschaften der Filterdefinition, um die Regeln zu konfigurieren.

   ![](assets/uc_idkey4.png)

1. Ziehen Sie die Tabelle mit den im Identifizierungsschlüssel verwendeten Feldern per Drag &amp; Drop.

   ![](assets/uc_idkey5.png)

1. Select the first field used in the identification key ("CRM ID"), then activate the **[!UICONTROL Switch to parameters]** option.

   ![](assets/uc_idkey6.png)

1. In the **[!UICONTROL Filter conditions]** section, keep the **[!UICONTROL Equal]** operator, then define the parameter's name and click the plus sign to create it.

   ![](assets/uc_idkey7.png)

   >[!NOTE]
   > Sobald Sie auf die Plusschaltfläche geklickt haben, wird der Parameter des Parameters automatisch generiert. Beachten Sie diese Informationen, da Sie es benötigen, um den Filter aus den apis zu verwenden.

1. Wiederholen Sie die obigen Schritte mit allen Feldern, die den Identifizierungsschlüssel ("Kategorie" ) zusammenstellen, und speichern Sie dann Ihre Änderungen.

   ![](assets/uc_idkey8.png)

1. Die Filterdefinition ist jetzt konfiguriert. Sie können die Ressource veröffentlichen, damit der Filter verfügbar ist.

## Schritt 3: Rufen Sie die Ressource auf Grundlage ihres Identifikators auf.

Sobald der Identifizierungsschlüssel und die Filterdefinition konfiguriert wurden, können Sie die Ressource verwenden, um die Ressource entweder aus der Kampagnenstandardoberfläche oder aus REST-apis aufzurufen.

To use the filter definition from the interface, use a **[!UICONTROL Query]** activity in a workflow (see [this section](../../automating/using/query.md)). Der Filter ist dann im linken Fensterbereich verfügbar.

![](assets/uc_idkey9.png)

Verwenden Sie die unten stehende Syntax, um die Filterdefinition aus Kampagnenstandard-REST-apis zu verwenden:

```
GET /profileAndServicesExt/&lt;resourceName&gt;&lt;filterName&gt;?&lt;param1_parameter&gt;=&lt;value&gt;&&lt;param2_parameter&gt;=&lt;value&gt;
```

In unserem Fall lautet die Syntax, um ein Profil aus der Kategorie "Frühjahr" und mit der CRM-ID" 123456" abzurufen:

```
GET https://mc.adobe.io/&lt;ORGANIZATION&gt;/campaign/profileAndServicesExt/profile/identification_key?category_parameter=spring&crm_id_parameter=123456
```

For more details, refer to [Campaign Standard REST APIs documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#filtering).