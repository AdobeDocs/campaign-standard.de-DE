---
title: Über die Integration von Campaign mit Experience Manager
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a1bc9d23163d12517c4501a572fc92aac6aacbc6

---


# Benutzerdefinierte Ressourcen und benutzerdefinierte Dynamics 365-Entitäten für die Kampagne zuordnen

Erfahren Sie, wie Sie benutzerdefinierte Ressourcen und benutzerdefinierte Entitäten im Kontext der Integration von Adobe Campaign Standard und Microsoft Dynamics 365 zuordnen.

## Voraussetzungen

Die neue Version der [Microsoft Dynamics 365-Adobe Campaign Standard-Integration](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md) unterstützt benutzerdefinierte Entitäten.  Dadurch können benutzerdefinierte Entitäten in Dynamics 365 in die entsprechenden benutzerdefinierten Ressourcen in der Kampagne repliziert werden.

Nach der Replizierung können die neuen Daten in den benutzerdefinierten Ressourcen für verschiedene Zwecke verwendet werden, einschließlich Segmentierung und Personalisierung.

>[!CAUTION]
>
>Wenn ein benutzerdefinierter Ressourcendatensatz eine Kampagne persönliche Daten enthält, die auf die Verwendung der Kampagne durch einen Kunden anwendbar sind, sollte dieser Datensatz mit einem entsprechenden Kampagne-Profil-Datensatz verknüpft werden (entweder direkt oder über eine andere benutzerspezifische Ressource), sodass ein datenschutzbezogener Löschvorgang im Profil-Datensatz auch den verknüpften benutzerspezifischen Ressourcendatensatz mit personenbezogenen Daten löschen kann. Die Verknüpfungs- und Löschoptionen zwischen den Entitäten müssen so konfiguriert sein, dass diese kaskadierte Löschung der verknüpften Datensätze aktiviert wird. Personenbezogene Daten sollten nicht in eine benutzerdefinierte Ressource eingegeben werden, die nicht mit dem Profil verknüpft ist.

Eine umfassendere Übersicht über die benutzerspezifischen Ressourcen der Kampagne finden Sie [unter diesem Link](../../developing/using/key-steps-to-add-a-resource.md).

Um die Integration für benutzerdefinierte Entitäten einzurichten, wenden Sie sich an [adobe-support@unifisoftware.com](mailto:adobe-support@unifisoftware.com) , um dies anzufordern.  Unifi erfordert die Namen der benutzerdefinierten Entitätstabellen in beiden Systemen sowie die gewünschten Attributzuordnungen.  Unifi erstellt dann die entsprechenden Aufträge und Zeitpläne.

Ein Beispielanwendungsfall für die Unterstützung benutzerdefinierter Entitäten finden Sie im Abschnitt [Verwendungsfall](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md#UC).

>[!CAUTION]
>
>* Benutzerspezifische Ressourcen, die vor Campaign Standard 19.4 veröffentlicht wurden, **müssen erneut veröffentlicht** werden, damit sie bei der Integration verwendet werden können.
>* Das Erstellen und Bearbeiten benutzerdefinierter Campaign Standard-Ressourcen sind sensible Vorgänge, die nur von erfahrenen Benutzern ausgeführt werden müssen.


## Umsetzung


### Startstatus

Der Kunde verfügt über ein in Dynamics 365 vordefiniertes benutzerdefiniertes Entitätsfahrzeug und ein in Campaign Standard vordefiniertes benutzerdefiniertes Ressourcenfahrzeug.  Der Kunde hat Unifi benutzerdefinierte Entitätszuordnungsdetails zur Verfügung gestellt und Unifi hat die Aufträge und Zeitpläne für die benutzerdefinierte Vehicle-Ressource in Unifi eingerichtet.

|   | Microsoft Dynamics 365 | Adobe Campaign Standard | Hinweise |
|---|---|---|---|
| Entität auf oberster Ebene | Kontakt | Profile | Standardmäßige, sofort einsatzbereite Entitäten |
| Verknüpfte Entität | Fahrzeug - neue benutzerdefinierte Entität | Fahrzeug - neue benutzerdefinierte Ressource | Neue benutzerdefinierte Entitäten |
| Relationstyp | Elternverknüpfung mit N:1 | Ähnlich wie Dynamics 365 - siehe Kampagne weiter unten. |   |

### Konfiguration in Dynamics 365

Die benutzerdefinierten Entitäten in Dynamics 365 können Sie im Dashboard Sales durch Klicken auf die Dropdown-Liste neben Dynamics 365 anzeigen.  Die benutzerdefinierten Entitäten dieses Kunden werden gruppiert unter **[!UICONTROL Extensions]**.

(../assets/SalesDashboard.png)

Fahrzeugdaten können durch Klicken auf die **[!UICONTROL vehicle]** benutzerdefinierte Entität angezeigt werden.  Siehe Liste der Fahrzeuge unten.

(../assets/VehicleCustomEntity.png)

Die Beziehung der **[!UICONTROL vehicle]** Entität zur **[!UICONTROL Contact]** Entität ist nachfolgend dargestellt. **[!UICONTROL Parental]** wurde für die **[!UICONTROL Type of Behavior]** ausgewählt.

(../assets/ContactToVehicle.png)

### Konfiguration im Campaign Standard

In Kampagne können die benutzerdefinierten Ressourcen angezeigt werden, indem Sie **[!UICONTROL Adobe Campaign]** in der oberen linken Ecke auf klicken und dann **[!UICONTROL Client data]** auswählen.

(../assets/ClientDataMenu.png)

### Benutzerdefinierte Ressourcen und benutzerdefinierte Entitäten zuordnen

Die **[!UICONTROL vehicle]** benutzerdefinierte Ressource hätte zuvor vom Kunden vordefiniert werden müssen und sollte in den Client-Daten angezeigt werden. aber wir werden die Schritte zur Erstellung dieser **[!UICONTROL vehicle]** benutzerspezifischen Ressource unten durchgehen.

Klicken Sie auf **[!UICONTROL Adobe Campaign]** in der oberen linken Ecke und dann auf **[!UICONTROL Administration > Development > Custom Resources]**.

(../assets/CustomRes.png)

1. Klicken Sie auf **[!UICONTROL Custom Resources]**.
1. Click the **[!UICONTROL Create]** button.  Dadurch wird ein Popup-Fenster geöffnet.
1. Wählen Sie **[!UICONTROL Create a new resource]** und geben Sie **[!UICONTROL Vehicle]** als Beschriftung und ID ein.
1. Klicks **[!UICONTROL Create]**.

(../assets/CreateAcusRes.png)

Kampagne zeigt dann Datenstrukturen und Linkseiten an.  Sie können sehen, dass mehrere Felder hinzugefügt wurden.

* Die Fahrzeug-ID ist die eindeutige Kennung der **[!UICONTROL Vehicle]** Entität. seine ID muss genau **[!UICONTROL externalId]** wie unten dargestellt sein, damit die Integration funktioniert.
* Assoziiertes Profil ist die ID des Profils, mit dem der Fahrzeugdatensatz verknüpft ist. Wenn dieser Link verknüpft ist, wird er mit dem **[!UICONTROL externalId]** Feld der Tabelle &quot;Profil&quot;verknüpft.
* VIN- und Fahrzeugname sind Felder zur Erfassung von Informationen über das Fahrzeug.

(../assets/CusResConfig.png)

>[!CAUTION]
>
>Jede benutzerdefinierte Ressource muss ein eindeutiges Feld mit der ID externalId (genau) haben.  Dieses Feld wird dem ID-Feld der benutzerdefinierten Ressource in Dynamics 365 zugeordnet (siehe unten).

(../assets/FieldsInDynamics.png)

### Definieren der Identifizierungsschlüssel

Der nächste Schritt besteht darin, die Identifizierungsschlüssel zu definieren.  Erstellen Sie zunächst die Identifizierungsschlüssel, wie unten dargestellt.

(../assets/IDkeys.png)

Wählen Sie im Bildschirm &quot;Schlüsseldefinition&quot;das **[!UICONTROL externalId]** Feld aus.

(../assets/KeyDefinition.png)

>[!CAUTION]
>
>Jede benutzerdefinierte Ressource muss einen Identifizierungsschlüssel mit dem Pfad &quot;externalId&quot;(genau) haben.

### Definieren des Filters

Der nächste Schritt besteht darin, die Filterdefinition anzugeben.

Klicken Sie **[!UICONTROL Filter Definition]** unter **[!UICONTROL Add an element]**.\
Geben Sie der Beschriftung und der ID den Namen **[!UICONTROL ExternalId]**ein.
Klicks **[!UICONTROL Add]**.

(../assets/FilterDefinition.png)

Klicken Sie jetzt auf Bearbeiten für das neu hinzugefügte Filterelement und konfigurieren Sie den Filter für das unten stehende Bild.  Wenn Sie **[!UICONTROL externalId]** in das **[!UICONTROL Parameters]** Feld eingeben und auf das Pluszeichen klicken, wird **[!UICONTROL externalId_parameter]** angezeigt.  Wählen Sie dies als Parameter aus.

(../assets/EditArule.png)

### Link definieren

Als Nächstes geben wir die Verknüpfung der benutzerdefinierten Ressource an.  In diesem Fall haben wir uns dafür entschieden, mithilfe einer **[!UICONTROL Vehicles]** benutzerdefinierten Entität (Quelle) eine Verknüpfung zur Entität (Zielgruppe) des Profils herzustellen **[!UICONTROL 1 cardinality simple link]**.

(../assets/DefineTheLink.png)

1. Wählen Sie im **[!UICONTROL Link definitions]** Bildschirm die Option Löschen: **[!UICONTROL Deleting the target record implies deleting records referenced by the link]**. Wir wählen diese Option, damit beim Löschen eines Profils auch alle mit diesem Profil verknüpften **[!UICONTROL Vehicle]** Datensätze gelöscht werden.
1. Wählen Sie **[!UICONTROL Join Definitions]** in **[!UICONTROL Define specific join conditions]**.
1. Klicken Sie dann auf **[!UICONTROL Add an element]**.

(../assets/LinkConfiguration.png)

Für die gemeinsame Definition geben wir die folgenden Werte ein.

Beachten Sie, dass der **[!UICONTROL @externalId]** Eintrag das Feld externalId der Tabelle Profil und der **[!UICONTROL ProfileExternalId]** Eintrag die ID des entsprechenden Felds in der benutzerspezifischen Ressource Vehikel ist.  Wenn der Wert externalId eines Profil-Datensatzes in das **[!UICONTROL ProfileExternalId]** Feld eines Fahrzeugdatensatzes eingegeben wird, werden die beiden Datensätze miteinander verknüpft.

(../assets/JoinDefinition.png)

Bestätigen Sie die Änderungen und speichern Sie die benutzerdefinierte Entität.

### Veröffentlichen und nach Updates suchen

Der letzte Schritt besteht darin, die benutzerdefinierte Ressource zu veröffentlichen.

1. Klicken Sie **[!UICONTROL Adobe Campaign]** in der oberen linken Ecke auf **[!UICONTROL Administration > Development > Publishing]**.
1. Die Standardoption beibehalten: **[!UICONTROL Determine modifications since the last publication]**.
1. Klicken Sie auf **[!UICONTROL Prepare Publication]** und warten Sie, bis der Vorgang abgeschlossen ist.

(../assets/PublishModifications.png)

Klicken Sie dann auf **[!UICONTROL Publish]** und warten Sie, bis der Vorgang abgeschlossen ist.

(../assets/Publish.png)

### Einführungszeitplan

Wenn der Kunde die Fahrzeugbenutzereinheit bereits in Dynamics 365 ausgefüllt hat und Unifi ihre eigenen Fahrzeugstandortaufträge und -pläne eingerichtet hat, sollte der Kunde in der Lage sein, den Einstiegsplan für die Fahrzeugeinheit zu starten.

(../assets/Schedule.png)

Nach Abschluss des Eingabefelds können die Fahrzeugdaten nun in der neu ausgefüllten **[!UICONTROL Vehicle]** benutzerdefinierten Ressource in der Kampagne angezeigt werden.

(../assets/ACSUpdate.png)

**Verwandte Themen**

* Arbeiten mit Adobe Campaign Standard - Microsoft Dynamics 365
* Wichtige Schritte zum Hinzufügen einer benutzerdefinierten Ressource in der Kampagne
