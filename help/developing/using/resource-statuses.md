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
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Status der Ressourcen{#resource-statuses}

Je nach Publikations- oder Aktivierungszustand weisen Ressourcen verschiedene Status auf.

Im Übersichtsbildschirm der **[!UICONTROL benutzerdefinierten Ressourcen]** wird ihr Status standardmäßig in zwei Spalten angezeigt.

![](assets/schema_colonne_1.png)

**Publikationsstatus**

* **Entwurf**: Die Ressource wurde neu erstellt oder zurückgesetzt. Sie muss publiziert werden, um die Tabellen und Datenbankfelder sowie die entsprechenden API zu erzeugen. Eine zurückgesetzte Ressource wird im Zuge der Publikation automatisch deaktiviert.
* **Initialisierung ausstehend**: Der Benutzer hat die Zurücksetzung der Ressource angefordert. Die Initialisierung erfolgt im Zuge der nächsten Publikation. Warnhinweise bei der Zurücksetzungsanforderung und im Anschluss an die Publikationsvorbereitung machen den Benutzer darauf aufmerksam, das eine Zurücksetzung unwiderruflich ist.

   Weiterführende Informationen zum Zurücksetzen finden Sie im Abschnitt [Ressource löschen](../../developing/using/deleting-a-resource.md).

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Zurücksetzung abbrechen]** ist verfügbar, wenn die Ressource, die Sie zurücksetzen möchten, Relationen mit anderen Ressourcen mit dem Status „Publiziert“ aufweist. Mithilfe dieser Option lässt sich der Initialisierungsprozess umkehren. Die benutzerdefinierten Ressourcen nehmen auf diese Weise ihren ursprünglichen Status an.

* **Publiziert**: Die Ressource wurde publiziert. Wenn eine publizierte Ressource in der Folge geändert wird, fordert ein Hinweis den Benutzer auf, sie erneut zu publizieren, um die Änderungen zu übernehmen.

Durch Aktivierung der Option **[!UICONTROL Letzte Änderungen nicht publizieren]** vermeiden Sie, dass Ihre Änderungen bei zukünftigen Publikationen berücksichtigt werden.

Die Konfiguration dieser Option erfolgt im Definitionsbildschirm der benutzerdefinierten Ressource.
