---
title: Erste Schritte mit Campaign Standard-APIs
description: Erstellen Sie Integrationen und bauen Sie Ihr eigenes Ökosystem, indem Sie Campaign mit einer Reihe von Technologien verbinden.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: c6968252-a012-4029-bbb8-66f4f693e99b
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '223'
ht-degree: 100%

---

# Erste Schritte mit Campaign Standard-APIs {#get-started-apis}

Mit Campaign Standard-APIs können Sie **Integrationen** für Adobe Campaign Standard erstellen und **Ihr eigenes Ökosystem einrichten**, indem Sie Adobe Campaign Standard mit den von Ihnen verwendeten Technologien verbinden.

Über die Adobe Campaign Standard-APIs erhalten Sie Zugriff auf folgende Funktionen:

<table><tr>
 <td valign="top"><a href="../../api/using/retrieving-profiles.md"><img width="60px" alt="Bedingungen" src="assets/icon_profile.svg"/></a><p><a href="../../api/using/retrieving-profiles.md">Profile</a></p></td>
<td valign="top"><a href="../../api/using/creating-a-service.md"><img width="60px" alt="Bedingungen" src="assets/icon_services.svg"/></a><p><a href="../../api/using/creating-a-service.md">Dienste und Abonnements</a></p></td>
<td valign="top"><a href="../../api/using/interacting-with-custom-resources.md"><img width="60px" alt="Bedingungen" src="assets/icon_customresources.svg"/></a><p><a href="../../api/using/interacting-with-custom-resources.md">Benutzerdefinierte Ressourcen</a></p></td>
<td valign="top"><a href="../../api/using/interacting-with-marketing-history.md"><img width="60px" alt="Bedingungen" src="assets/icon_marketinghistory.svg"/></a><p><a href="../../api/using/interacting-with-marketing-history.md">Marketing-Verlauf</a></p></td>
</tr>
<tr>
<td valign="top"><a href="../../api/using/creating-a-privacy-request.md"><img width="60px" alt="Bedingungen" src="assets/icon_privacy.svg"/></a><p><a href="../../api/using/creating-a-privacy-request.md">Datenschutzverwaltung</a></p></td>
<td valign="top"><a href="../../api/using/managing-transactional-messages.md"><img width="60px" alt="Bedingungen" src="assets/icon_transactionalmessage.svg"/></a><p><a href="../../api/using/managing-transactional-messages.md">Transaktionsnachrichten</a></p></td>
<td valign="top"><a href="../../api/using/controlling-a-workflow.md"><img width="60px" alt="Bedingungen" src="assets/icon_workflows.svg"/></a><p><a href="../../api/using/controlling-a-workflow.md">Workflows</a></p></td>
<td valign="top"><a href="../../api/using/retrieving-an-organizational-unit.md"><img width="60px" alt="Bedingungen" src="assets/icon_units.svg"/></a><p><a href="../../api/using/retrieving-an-organizational-unit.md">Organisationseinheiten</a></p></td>
</tr></table>

>[!NOTE]
>
>Bevor Sie API-Aufrufe ausführen, überprüfen Sie bitte die Volumenbeschränkungen in Ihrer Lizenzvereinbarung. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

Zur Verwendung der Campaign Standard-API benötigen Sie ein Adobe I/O-Konto. Dies ist ein notwendiger erster Schritt zum Kennenlernen der API-Funktionen.
Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/setting-up-api-access.md).

Die APIs, die wir bereitstellen, basieren auf **Standardkonzepten** mit einer REST-Schnittstelle und JSON-Payloads.

>[!NOTE]
>
>Alle Beispiele arbeiten mit Postman; Sie können aber auch Ihren bevorzugten REST-Client nutzen.

Alle Endpunkte werden in dieser Dokumentation mit allgemeinen Konzepten zur Bearbeitung der API, der vollständigen API-Referenz, Codebeispielen und Schnellstartanleitungen ausführlich beschrieben.

Wenn etwas fehlt oder fehlerhaft erscheint, fragen Sie bitte die [Community](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community).
