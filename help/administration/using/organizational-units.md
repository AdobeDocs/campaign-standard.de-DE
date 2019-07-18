---
title: Organisationseinheiten
seo-title: Organisationseinheiten
description: Organisationseinheiten
seo-description: Definieren Sie die Zugriffsebene Ihrer Benutzer mithilfe von Organisationseinheiten.
page-status-flag: nie aktiviert
uuid: 8 c 82 ffea-cef 4-4 a 89-b 823-d 8 b 7 bae 1 db 4 f
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Administration
content-type: Referenz
topic-tags: users-and-security
discoiquuid: 6 f 60 c 653-1 d 12-4 d 27-9 bc 8-ce 8 c 19 bca 466
context-tags: Orgunit, overview; Orgunit, main; Geounit, overview; Geounit, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Organisationseinheiten{#organizational-units}

## Über Einheiten {#about-units}

Alle Objekte und Benutzer der Plattform sind einer Organisationseinheit zugeordnet. Diese Einheit bestimmt auf hierarchische Weise die Ansicht von Benutzern. Die geografische Einheit und die Organisationseinheit, denen ein Benutzer zugeordnet wurde, bestimmen das Zugriffsniveau, über das er für die verschiedenen Plattformobjekte verfügt.

>[!CAUTION]
>
>Ein Benutzer, der keiner Einheit zugeordnet wurde, kann keine Verbindung zu Adobe Campaign herstellen. Wenn Sie den Zugriff von Benutzern oder Benutzergruppen einschränken möchten, dürfen sie nicht der Einheit **[!UICONTROL Alle]zugeordnet werden.**

Der Zugriff eines Benutzers auf Objekte übergeordneter Einheiten ist schreibgeschützt. Ein Benutzer verfügt über Lese- und Schreibzugriff auf Objekte seiner Einheit sowie untergeordneter Einheiten. Benutzer haben keinen Zugriff auf Objekte aus Parallelzweigen.

Standardmäßig sind nur die Einheiten **[!UICONTROL Alle]verfügbar.**

Wenn einem Benutzer eine Organisationseinheit zugewiesen wird, wird diese Einheit stets auf die vom Benutzer erstellten Objekte angewendet.

![](assets/user_management_2.png)

>[!NOTE]
>
>Wenn ein Benutzer mehreren Gruppen mit verschiedenen zugeordneten Einheiten angehört, gelten bestimmte Regeln. Weiterführende Informationen finden Sie im Abschnitt [Gruppen und Benutzer verwalten](../../administration/using/managing-groups-and-users.md).

## Einheiten erstellen und verwalten {#creating-and-managing-units}

Mit Organisationseinheiten können Sie Ihre Instanz nach der Organisation filtern, mit der Ihre Benutzer verknüpft sind. Diese Einheit kann eine Region, ein Land oder sogar eine Marke in Ihrer Instanz sein.

Für unser Beispiel haben wir zuvor Sicherheitsgruppen erstellt und dabei zwei Benutzern unterschiedliche Benutzerrollen zugewiesen: Einem Benutzer wurden die Sicherheitsgruppen "Administratoren" und "Geometrixx" zugewiesen und dem anderen Benutzer die Sicherheitsgruppen "Standardbenutzer" und "Geometrixx Clothes". Das vollständige Beispiel finden Sie unter [Sicherheitsgruppe erstellen und Benutzer zuordnen](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users).

Jetzt müssen wir die Organisationseinheiten für die Sicherheitsgruppen "Geometrixx Clothes" und "Geometrixx" erstellen:

1. From Adobe campaign advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Users &amp; security]** &gt; **[!UICONTROL Organizational units]**.
1. Konfigurieren Sie unter Verwendung der Schaltfläche **[!UICONTROL Erstellen]Ihre Organisationseinheit.**

   ![](assets/manage_units_1.png)

1. Ändern Sie den standardmäßigen **[!UICONTROL Titel]** und die **Kennung]in "Geometrixx".[!UICONTROL **
1. Verknüpfen Sie dann diese Einheit mit einer übergeordneten Einheit. In unserem Beispiel wählen wir **[!UICONTROL Alle]**.

   ![](assets/manage_units_2.png)

1. Wählen Sie abschließend **[!UICONTROL Erstellen]aus, um Ihre neue Organisationseinheit einer Sicherheitsgruppe zuzuweisen.**
1. Gehen Sie für die Geometrixx-Clothes-Einheit ebenso vor, beachten Sie jedoch, dass die übergeordnete Einheit die zuvor erstellte Geometrixx-Einheit sein muss.

   ![](assets/manage_units_3.png)

Wie sich die Zuweisung unterschiedlicher Einheiten zu unterschiedlichen Sicherheitsgruppen auswirkt, wird ersichtlich, wenn der Benutzer, der der Administrator- und Geometrixx-Gruppe zugewiesen ist, zwei E-Mail-Vorlagen erstellt. Darin kann er feststellen, worauf der andere Benutzer, der den Standardbenutzern und Geometrixx Clothes zugewiesen ist, zugreifen kann und worauf nicht.

1. From the advanced menu, select **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery Templates]**.
1. Duplizieren Sie eine vorhandene Vorlage und personalisieren Sie sie nach Bedarf. Weiterführende Informationen finden Sie im Abschnitt [Über Vorlagen](../../start/using/about-templates.md).
1. Wählen Sie bei der Erstellung der Vorlage das Symbol **[!UICONTROL Eigenschaften bearbeiten]aus, um Ihrer Vorlage Einheiten zuzuweisen.**

   ![](assets/manage_units_6.png)

1. Wählen Sie im Dropdown-Menü **[!UICONTROL Zugriffsberechtigung]die Organisationseinheit aus.**

   Hier erstellen wir eine Vorlage mit der zuvor generierten Organisationseinheit "Geometrixx".

   ![](assets/manage_units_5.png)

1. Gehen Sie analog vor, um die zweite Vorlage zu erstellen, die der zuvor generierten Organisationseinheit "Geometrixx Clothes" zugeordnet wurde.

Der den Gruppen "Standardbenutzer" und "Geometrixx Clothes" zugewiesene Benutzer kann beide Vorlagen sehen. Wegen der hierarchischen Struktur der Organisationseinheiten besitzt dieser Benutzer Lese- und Schreibrechte für die Vorlage, die mit der Geometrixx-Clothes-Einheit verknüpft ist, und nur Leserechte für die Vorlage, die mit der Geometrixx-Einheit verknüpft ist.

![](assets/manage_units_7.png)

Da die Geometrixx-Clothes-Einheit eine untergeordnete Einheit von Geometrixx ist, erscheint die folgende Nachricht, wenn der Benutzer versucht, die Geometrixx-Vorlage zu verändern:

![](assets/manage_units_8.png)

Mit Organisationseinheiten kann der Zugriff auf verschiedene Funktionen wie etwa Profile eingeschränkt werden. Unser Geometrixx-Clothes-Benutzer könnte beispielsweise im **[!UICONTROL Profile]-Tab auf die Profile in der Organisationseinheit "Geometrixx Clothes" zugreifen und diese verändern.**

Im Gegensatz dazu bestehen für die Organisationseinheit "Geometrixx " nur Leserechte und die folgende Fehlermeldung wird angezeigt, wenn unser Benutzer versucht, ein Profil zu verändern: **[!UICONTROL Sie verfügen nicht über die erforderlichen Rechte, um die Ressource "Profil" mit Kennung "xy" zu ändern]**.

![](assets/manage_units_10.png)

## Profile partitionieren {#partitioning-profiles}

Falls Ihre Organisation die Profile isolieren möchte, die von den einzelnen Marken kontaktiert werden, müssen Sie Ihre Profile nach Organisationseinheiten partitionieren.

Die Felder für die Organisationseinheiten sind in Ihren Profilen standardmäßig nicht verfügbar und müssen hinzugefügt werden.

Auf Profile ohne Organisationseinheiten kann nach Erweiterung der Ressource nicht mehr zugegriffen werden.

>[!CAUTION]
>
>Es empfiehlt sich, diese Option vor dem Importieren von Profilen hinzuzufügen. Falls Sie Ihre Kundendatenbank bereits importiert haben, ist eine Aktualisierung erforderlich, um die Werte für Organisationseinheiten für bereits importierte Profile festzulegen.

1. Greifen Sie mithilfe des Adobe Campaign-Logos oben links im Bildschirm und der Schaltflächen **Administration &gt; Entwicklung &gt; Benutzerdefinierte Ressourcen** auf das entsprechende Menü zu.
1. Wählen Sie die **Profil**-Ressource aus oder erstellen Sie eine neue benutzerdefinierte Ressource, um die Profile zu erweitern.
1. Aktivieren Sie die Option **Zugriffsberechtigungsverwaltung-Felder hinzufügen**, um die Organisationseinheiten in der Erweiterung der **Profil**-Ressource hinzuzufügen.

   ![](assets/user_management_9.png)

1. Wählen Sie **[!UICONTROL Speichern aus]**.
1. Aktualisieren Sie die Struktur durch eine erneute Publikation. Weitere Informationen zur Publikation finden Sie im Abschnitt [Datenstruktur aktualisieren](../../developing/using/data-model-concepts.md).

Das Feld für Organisationseinheiten wird Ihren Profilen im Bereich **[!UICONTROL Zugriffsberechtigung]hinzugefügt.**

![](assets/user_management_10.png)

**Verwandte Themen**:

* [Über Einheiten](../../administration/using/organizational-units.md#about-units)
* [Über die Zugriffsverwaltung](../../administration/using/about-access-management.md)

