---
title: An-/Abmeldedienst
description: Mithilfe der An-/Abmeldedienst-Aktivität lassen sich Profile gesammelt für Dienste an- bzw. von Diensten abmelden.
page-status-flag: never-activated
uuid: 56637024-15ab-4145-9c48-3fbd27ab8af8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 74a6df0e-fd85-4404-a42c-9a7406512717
context-tags: setOfService,workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9048e11fe063707e1c6b5a86de095f72d22800c1

---


# An-/Abmeldedienst{#subscription-services}

## Beschreibung {#description}

![](assets/wf_subscription.png)

The **[!UICONTROL Subscription Services]** activity allows you to take profiles in mass and subscribe them to a service or unsubscribe them from a service.

>[!CAUTION]
>
>Wenn An-/Abmeldungen im Rahmen eines Workflows verwaltet werden, empfangen die an- bzw. abgemeldeten Profile nicht die verschiedenen in den Diensteigenschaften definierten Bestätigungs-E-Mails.

## Anwendungskontext {#context-of-use}

The **[!UICONTROL Subscription Services]** activity is the only Adobe Campaign functionality which allows multiple profiles to be subscribed to or to be unsubscribed from a service in a single action.

Sie können diese Aktivität beispielsweise im Anschluss an eine Zielgruppenbestimmung oder den Import einer Datei mit identifizierten Daten verwenden.

Wenn dies in den entsprechenden Spalten der Datei spezifiziert wird, können Sie mithilfe dieser Aktivität auch die gewünschte Aktion auswählen (anmelden oder abmelden) sowie den Dienst, auf den sich die Aktion bezieht.

## Konfiguration {#configuration}

1. Drag and drop a **[!UICONTROL Subscription Services]** activity into your workflow.
1. Schließen Sie ihn nach weiteren Zielgruppenbestimmungs-Aktivitäten an, wie beispielsweise nach einer Abfrage oder einer auf einen Import folgenden Abstimmung.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Select the **[!UICONTROL Service]** for which you would like to manage the subscriptions using one of the following options:

   * **[!UICONTROL Select a specific service]**: wählen Sie einen Dienst manuell aus.
   * **[!UICONTROL Select services from the inbound transition]**: der Dienst in der eingehenden Transition angegeben ist. Beispielsweise können Sie eine Datei importieren, in der der zu verwaltende Dienst für jede Zeile spezifiziert wird. Wenn Sie diese Option wählen, muss zuvor eine Verknüpfung zwischen den Daten und der Ressource **Dienst** erstellt worden sein, wie in [diesem Beispiel](#example--updating-multiple-subscription-statuses-from-a-file) erläutert wird.

      Der Dienst, bei dem der Vorgang ausgeführt werden soll, wird dann für jeden Datensatz dynamisch ausgewählt.

1. Select the **[!UICONTROL Operation type]** to execute using one of the following options:

   * **[!UICONTROL Select a specific operation type]**: manuell auswählen, ob Sie **[!UICONTROL Subscribe]** oder **[!UICONTROL Unsubscribe]** Profil möchten.
   * **[!UICONTROL Select an operation type from a path of inbound transition]**: Wählen Sie die Spalte der eingehenden Daten aus, die den Vorgang für jeden Datensatz angibt.

      In dieser Spalte muss der Vorgang als &quot;Boolesch&quot; oder &quot;Integer&quot; angegeben werden. Mit **0** melden Sie einen Datensatz ab und mit **1** melden Sie ihn an.

      In case the values contained in an imported file do not match the above requirements, you can still use the [Remapping of values](../../automating/using/load-file.md#column-format) option available in the **[!UICONTROL Load file]** activity.

1. Wenn die eingehenden Daten eine Spalte enthalten, die dem Abonnementdatum des Profils für den Dienst entspricht, wählen Sie sie aus. Sie können sie leer lassen. In diesem Fall wird aber kein Abonnementdatum bei der Durchführung des Workflows eingerichtet.
1. Definieren Sie den Ursprung des Abonnements. You can set it to one of the fields of the inbound data or to a constant value of your choice by checking the **[!UICONTROL Set a constant as origin]** option. Sie können diese Option auch leer lassen. In diesem Fall wird aber kein Ursprung bei der Durchführung des Workflows festgelegt.
1. Sie können bei Bedarf eine ausgehende Transition erzeugen. In diesem Fall sind die Daten der ausgehenden Transition mit denen der eingehenden Transition identisch.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

   Ihr Workflow kann nun ausgeführt werden. Nach der Ausführung können Sie die an- bzw. abgemeldeten Profile in der Detailansicht des Dienstes einsehen.

## Beispiel: Profile bei einem spezifischen Dienst nach dem Import einer Datei anmelden {#example--subscribing-profiles-to-a-specific-service-after-importing-a-file}

In diesem Beispiel wird dargestellt, wie man eine Datei mit Profilen importiert, um diese für einen existierenden Dienst anzumelden. Auf den Dateiimport muss eine Abstimmungsaktivität folgen, damit die importierten Daten als Profile identifiziert werden können. Um sicherzustellen, dass sich keine Dubletten in der Datei befinden, wird eine Deduplizierung auf die Daten angewendet.

Der Workflow stellt sich folgendermaßen dar:

![](assets/subscription_activity_example1.png)

* A **[!UICONTROL Load file]** activity loads the profile file and defines the structure of the imported columns.

   In unserem Beispiel weist die geladene Datei das .csv-Format auf und enthält folgende Daten:

   ```
   lastname;firstname;email;birthdate;subdate
   jackman;megan;megan.jackman@testmail.com;07/08/1975;10/08/2017
   phillips;edward;phillips@testmail.com;09/03/1986;10/08/2017
   weaver;justin;justin_w@testmail.com;11/15/1990;10/08/2017
   martin;babeth;babeth_martin@testmail.net;11/25/1964;10/08/2017
   reese;richard;rreese@testmail.com;02/08/1987;11/08/2017
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989;11/08/2017
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992;11/08/2017
   grimes;daryl;daryl_890@testmail.com;12/06/1979;12/08/2017
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971;12/08/2017
   ```

   ![](assets/subscription_activity_example2.png)

* A **[!UICONTROL Reconciliation]** activity identifies the data from the file as belonging to the profile dimension of the Adobe Campaign database. Only the **[!UICONTROL Identification]** tab is configured. Durch ihn lassen sich die Daten der Datei über die E-Mail-Adresse der Profile identifizieren.

   ![](assets/subscription_activity_example3.png)

* A **[!UICONTROL Deduplication]** based on the **email** field of the temporary resource (resulting from the reconciliation) identifies any duplicates. Sollten die aus der Datei importierten Daten Dubletten enthalten, wird die Anmeldung für einen Dienst für alle Datensätze fehlschlagen.

   ![](assets/subscription_activity_example5.png)

* A **[!UICONTROL Subscription Services]** activity lets you select the service to which the profiles must be subscribed, the field corresponding to the subscription date, and the origin of the subscription.

   ![](assets/subscription_activity_example4.png)

## Beispiel: Mehrere Abonnementstatus über eine Datei aktualisieren {#example--updating-multiple-subscription-statuses-from-a-file}

Dieses Beispiel zeigt, wie eine Datei mit Profilen importiert wird und ihre Anmeldungen bei mehreren in der Datei spezifizierten Diensten durchgeführt werden. Auf den Dateiimport muss eine Abstimmungsaktivität folgen, damit die importierten Daten als Profile mit einer Verknüpfung zu Diensten identifiziert werden können. Um sicherzustellen, dass sich keine Dubletten in der Datei befinden, wird eine Deduplizierung auf die Daten angewendet.

Der Workflow stellt sich folgendermaßen dar:

![](assets/subscription_activity_example1.png)

* A **[!UICONTROL Load file]** activity loads the profile file and defines the structure of the imported columns.

   In unserem Beispiel weist die geladene Datei das .csv-Format auf und enthält folgende Daten:

   ```
   lastname;firstname;email;birthdate;service;operation
   jackman;megan;megan.jackman@testmail.com;07/08/1975;SVC2;sub
   phillips;edward;phillips@testmail.com;09/03/1986;SVC3;unsub
   weaver;justin;justin_w@testmail.com;11/15/1990;SVC3;sub
   martin;babeth;babeth_martin@testmail.net;11/25/1964;SVC3;unsub
   reese;richard;rreese@testmail.com;02/08/1987;SVC3;sub
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989;SVC3;sub
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992;SVC4;sub
   grimes;daryl;daryl_890@testmail.com;12/06/1979;SVC3;unsub
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971;SVC2;sub
   ```

   ![](assets/subscription_example_load_file.png)

   Der Vorgang wird in der Datei als &quot;sub&quot; oder &quot;unsub&quot; spezifiziert. Vom System wird ein **boolescher** Wert oder eine **Integer** erwartet, der/die angibt, welcher Vorgang ausgeführt werden soll: Mit &quot;0&quot; wird eine Abmeldung vorgenommen und mit &quot;1&quot; eine Anmeldung. Um diesen Anforderungen zu entsprechen, wird eine Neukodifizierung der Werte im Detail der Spalte &quot;Vorgang&quot; durchgeführt.

   ![](assets/subscription_example_remapping.png)

   Wenn in Ihrer Datei der Vorgang bereits mit &quot;0&quot; und &quot;1&quot; spezifiziert ist, müssen Sie diese Werte nicht erneut kodifizieren. Only make sure that the column is processed as a **Boolean** or **Integer** in the **[!UICONTROL Column definition]** tab.

* A **[!UICONTROL Reconciliation]** activity identifies the data from the file as belonging to the profile dimension of the Adobe Campaign database. Through the **[!UICONTROL Identification]** tab, the **email** field of the file is matched to the **email** field of the profile resource.

   ![](assets/subscription_activity_example3.png)

   In the **[!UICONTROL Relations]** tab, a link is created with the service resource to allow the **service** field of the file to be recognized. In unserem Beispiel werden die Werte mit dem **name**-Feld der Dienst-Ressource abgestimmt.

   ![](assets/subscription_example_service_relation.png)

* A **[!UICONTROL Deduplication]** based on the **email** field of the temporary resource (resulting from the reconciliation) identifies duplicates. Die Eliminierung von Dubletten ist wichtig, da andernfalls die Anmeldung für einen Dienst für alle Daten fehlschlägt.

   ![](assets/subscription_activity_example5.png)

* A **[!UICONTROL Subscription Services]** identifies the services to update as coming from the transition, through the link created in the **[!UICONTROL Reconciliation]** activity.

   The **[!UICONTROL Operation type]** is identified as coming from the **operation** field of the file. Hier können nur die Felder &quot;Boolesch&quot; oder &quot;Integer&quot; ausgewählt werden. If the column of your file that contains the operation to perform does not appear in the list, make sure that you have correctly set your column format in the **[!UICONTROL Load file]** activity, as explained earlier in this example.

   ![](assets/subscription_activity_example_from_file.png)

