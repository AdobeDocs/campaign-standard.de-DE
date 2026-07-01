---
title: Problem mit Signaturen getrackter URLs
description: Problem mit Signaturen getrackter URLs
hide: true
exl-id: 8c2725a8-2c3a-448a-8c04-c0c2a5950574
TQID: https://experienceleague.adobe.com/6R8s1OkdU0TWD2Qo1DnI33T-FsiV4kVNkn942k0o5-Q
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: e267777274122de6dc8badc2d6b8dfdaa20c5fb2
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 100%

---

# Problem mit Signaturen getrackter URLs {#tracked-urls}

Nach den jüngsten Änderungen können von Campaign gesendete getrackte URLs fehlschlagen. Postfächer, bei denen spezielle Sicherheits-Tools verwendet werden, die sich auf Links auswirken und den Mechanismus für URL-Signaturen verändern, können hiervon stärker betroffen sein.

Adobe hat daher beschlossen, den Signaturmechanismus für Tracking-Links zu deaktivieren. Mit diesem Verfahren werden alle Tracking-Links repariert.

Es gilt zu beachten, dass der Fehler bei Abmelde-Links ebenso auftreten kann wie bei allen anderen Links. Die Auftrittshäufigkeit ist dabei von Host zu Host unterschiedlich, beträgt jedoch weniger als 1 %.

**Sind Sie betroffen?**

Davon sind einige Campaign Standard-Benutzer betroffen, da der Signaturmechanismus zum Tracking von Links in E-Mails mit [Campaign Standard 20.4](release-notes-2020.md#release-20-4-october-2020) im Oktober 2020 eingeführt wurde und standardmäßig für alle Kunden aktiviert ist.

**Wie wird die Aktualisierung durchgeführt?**

Adobe wird in Kürze gemeinsam mit Ihnen Ihre Konfiguration aktualisieren. Sie werden eine E-Mail mit dem Zeitplan für Ihr Upgrade erhalten.

**Wie wirkt sich das aus?**

Für den Wartungsvorgang ist eine Stillstandszeit von maximal 25 Minuten einzuplanen. Während dieser funktionieren Versand, Tracking-Links und API-Aufrufe nicht.

Nach Abschluss der Aktualisierung funktionieren alle Links wieder ordnungsgemäß.

>[!NOTE]
>
>Wenden Sie sich bei Fragen zu diesen Änderungen an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html).
