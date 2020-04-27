---
title: Status der Ressourcen
description: Hier erhalten Sie Informationen über den vom Publikationszustand abhängigen Ressourcenstatus.
page-status-flag: never-activated
uuid: 215c0a2e-27ec-43f3-baac-1eaac7640784
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 85516477-1b95-4273-a0a7-d2cbb9950afd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401

---


# Status der Ressourcen{#resource-statuses}

Je nach Veröffentlichungs- oder Aktivierung-Status können Ressourcen unterschiedliche Status haben.

There are two columns dedicated to displaying these statuses in the **[!UICONTROL Custom resources]** screen.

![](assets/schema_colonne_1.png)

**Publikationsstatus**

* **Entwurf**: Die Ressource wurde neu erstellt oder zurückgesetzt. Um die Datenbanktabellen sowie die entsprechenden APIs zu erstellen, muss die Ressource erneut veröffentlicht werden. Wenn eine Ressource neu entworfen wird, wird sie nach dem Schritt der Veröffentlichung automatisch inaktiv.
* **Initialisierung ausstehend**: Der Benutzer hat die Zurücksetzung der Ressource angefordert. Die Initialisierung erfolgt im Zuge der nächsten Publikation. Es werden mehrere Warnmeldungen angezeigt, die den Benutzer informieren, sowohl bei der Neufassung als auch bei der Vorbereitung der Veröffentlichung.

   Weiterführende Informationen zum Zurücksetzen finden Sie im Abschnitt [Ressource löschen](../../developing/using/deleting-a-resource.md).

   >[!NOTE]
   >
   >The **[!UICONTROL Cancel re-draft]** option is available when the resource that you want to re-draft still contains links through other resources with the &quot;Published&quot; status. Mithilfe dieser Option lässt sich der Initialisierungsprozess umkehren. Die benutzerdefinierten Ressourcen nehmen auf diese Weise ihren ursprünglichen Status an.

* **Publiziert**: Die Ressource wurde publiziert. Wenn die Ressource nach dem letzten Änderungsdatum geändert wurde, wird eine Meldung angezeigt, die Sie auffordert, die Ressource erneut zu veröffentlichen, um die neuesten Änderungen zu berücksichtigen.

Das **[!UICONTROL Do not publish latest modifications]** Feld verhindert, dass Änderungen bei zukünftigen Veröffentlichungen berücksichtigt werden.

Die Konfiguration dieser Option erfolgt im Definitionsbildschirm der benutzerdefinierten Ressource.
