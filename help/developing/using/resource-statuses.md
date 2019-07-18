---
title: Status der Ressourcen
seo-title: Status der Ressourcen
description: Status der Ressourcen
seo-description: Hier erhalten Sie Informationen über den vom Publikationszustand abhängigen Ressourcenstatus.
page-status-flag: nie aktiviert
uuid: 215 c 0 a 2 e -27 ec -43 f 3-baac -1 eaac 7640784
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: about-custom-resources
discoiquuid: 85516477-1 b 95-4273-a 0 a 7-d 2 cbb 9950 afd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Status der Ressourcen{#resource-statuses}

Je nach Publikations- oder Aktivierungszustand weisen Ressourcen verschiedene Status auf.

Im Übersichtsbildschirm der **[!UICONTROL benutzerdefinierten Ressourcen]wird ihr Status standardmäßig in zwei Spalten angezeigt.**

![](assets/schema_colonne_1.png)

**Publikationsstatus**

* **Entwurf**: Die Ressource wurde neu erstellt oder zurückgesetzt. Sie muss publiziert werden, um die Tabellen und Datenbankfelder sowie die entsprechenden API zu erzeugen. Eine zurückgesetzte Ressource wird im Zuge der Publikation automatisch deaktiviert.
* **Initialisierung ausstehend**: Der Benutzer hat die Zurücksetzung der Ressource angefordert. Die Initialisierung erfolgt im Zuge der nächsten Publikation. Warnhinweise bei der Zurücksetzungsanforderung und im Anschluss an die Publikationsvorbereitung machen den Benutzer darauf aufmerksam, das eine Zurücksetzung unwiderruflich ist.

   Weiterführende Informationen zum Zurücksetzen finden Sie im Abschnitt [Ressource löschen](../../developing/using/deleting-a-resource.md).

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Zurücksetzung abbrechen]ist verfügbar, wenn die Ressource, die Sie zurücksetzen möchten, Relationen mit anderen Ressourcen mit dem Status „Publiziert“ aufweist.** Mithilfe dieser Option lässt sich der Initialisierungsprozess umkehren. Die benutzerdefinierten Ressourcen nehmen auf diese Weise ihren ursprünglichen Status an.

* **Publiziert**: Die Ressource wurde publiziert. Wenn eine publizierte Ressource in der Folge geändert wird, fordert ein Hinweis den Benutzer auf, sie erneut zu publizieren, um die Änderungen zu übernehmen.

Durch Aktivierung der Option **[!UICONTROL Letzte Änderungen nicht publizieren]vermeiden Sie, dass Ihre Änderungen bei zukünftigen Publikationen berücksichtigt werden.**

Die Konfiguration dieser Option erfolgt im Definitionsbildschirm der benutzerdefinierten Ressource.
