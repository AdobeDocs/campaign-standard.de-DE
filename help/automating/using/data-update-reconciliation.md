---
title: Datenaktualisierung mittels Abstimmung
description: Das folgende Beispiel zeigt einen Workflow zur Erstellung einer Profil-Audience, die direkt aus einer importierten Datei mit neuen Kunden erzeugt wird.
page-status-flag: never-activated
uuid: 7884db8c-1717-4724-be15-3b0b32ccc071
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: cb8c43f4-9cdd-4e85-99a4-004b36b336aa
context-tags: reconciliation,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 100%

---


# Datenaktualisierung mittels Abstimmung {#data-update-reconciliation}

Das folgende Beispiel zeigt einen Workflow zur Erstellung einer Profil-Audience, die direkt von einer importierten Datei mit neuen Kunden ausgeht. Er setzt sich aus folgenden Aktivitäten zusammen:

![](assets/identification_example2.png)

* [Datei laden](../../automating/using/load-file.md) zum Laden und Erkennen der Daten der zu importierenden Datei. Die importierte Datei enthält folgende Daten:

   ```
   lastname;firstname;email;dateofbirth
   jackman;megan;megan.jackman@testmail.com;07/08/1975
   phillips;edward;phillips@testmail.com;09/03/1986
   weaver;justin;justin_w@testmail.com;11/15/1990
   martin;babeth;babeth_martin@testmail.net;11/25/1964
   reese;richard;rreese@testmail.com;02/08/1987
   cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
   xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
   grimes;daryl;daryl_890@testmail.com;12/06/1979
   tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
   ```

* [Abstimmung](../../automating/using/reconciliation.md) zur Zuordnung jeder Spalte der geladenen Datei zu einer Spalte der Profildimension. Die nicht identifizierbaren Datensätze der Datei (fehlende Daten, inkompatible Datentypen etc.) werden zur Wahrung der Integrität der endgültigen Audience-Daten ignoriert.

   ![](assets/identification_example1.png)

* Aktivität [Audience-Speicherung](../../automating/using/save-audience.md) zum Speichern der Profil-Audience.

   ![](assets/identification_example3.png)
