---
title: Wozu dienen Campaign Standard-APIs?
description: Erfahren Sie mehr über Campaign Standard-APIs und deren Verwendung.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: ef045e5d-cd02-44a0-9a1e-d468483a38d9
source-git-commit: 13d419c5fc51845ee14f8a3b288f4c467e0a60d9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Wozu dienen Campaign Standard-APIs {#why-using-campaign-standard-apis}

Adobe Campaign Standard bietet APIs, die es ermöglichen, bestehende Systeme mit der Campaign-Plattform zu integrieren, um Probleme in Echtzeit zu lösen.

Öffentliche Websites wie die Anmelde- oder Abmeldeseite müssen eine Verbindung zu Backend-Systemen herstellen, um Profildaten speichern zu können. Backend-Systeme wie Adobe Campaign erlauben es, Profildaten aufzunehmen und benutzerdefinierte Aktionen dafür auszuführen.

Hier einige Beispiele:

* Online-Registrierung potenzieller Kunden.
* Bestehendes Kundenprofil und Verwaltung der Präferenzen bei der Marketing-Kommunikation.
* Auslösung von ereignisbasierter Transaktionskommunikation – Bestellbestätigung, Buchungsverlauf, Kennwortzurücksetzung usw.
* Auch E-Mail-Kommunikation bei Warenkorbabbruch.

Auf Anmelde-Landingpages können Kunden bzw. potenzielle Kunden ihren Namen und ihre E-Mail-Adresse registrieren. Sobald Campaign Standard die Profildaten und Präferenzen erfasst hat, kann es auf die Interessen der Person abgestimmte Nachrichten versenden.

Diese werden mit folgenden Elementen erstellt:

1. Registrierungsformular mit Campaign-API-Listenern.

   ![Alternativtext](assets/apis_uc1.png)

1. Benutzerdefinierte Aktionen, die je nach Kontrollkästchen ausgeführt werden. Ein Kunde, der &quot;Sonderangebote per E-Mail&quot; auswählt, erhält eine andere, personalisierte E-Mail mit Gutschein als im normalen Registrierungsprozess.

   ![Alternativtext](assets/apis_uc2.png)

1. Ein Profil kann seine Details durch Auswahl des Links &quot;Details aktualisieren&quot; in der E-Mail ändern. Dadurch wird das Profil auf die Seite &quot;Profil- und Präferenzdetails aktualisieren&quot; geleitet. Zur Erledigung des Vorgangs werden die Profildetails (Pkey) an den Campaign-Server weitergeleitet und das Profil abgerufen und dargestellt. Sobald das Profil auf die Schaltfläche &quot;Aktualisieren&quot; klickt, werden die Daten im System aktualisiert (über einen PATCH-Befehl).

   ![Alternativtext](assets/apis_uc3.png)

Es stehen verschiedene Anfragen zur Verfügung, die Ihnen dabei helfen, sich mit den Anfragen der Campaign Standard-APIs vertraut zu machen. Diese Sammlung im JSON-Format besteht aus vordefinierten API-Anfragen, die gängige Anwendungsfälle repräsentieren.

Im folgenden Anwendungsbeispiel werden die Schritte zum Importieren und Verwenden der Sammlung zur Erstellung eines Profils in der Campaign Standard-Datenbank beschrieben.

>[!NOTE]
>
>In unserem Beispiel verwenden wir Postman. Sie können jedoch auch Ihren bevorzugten REST-Client nutzen.

1. Laden Sie die JSON-Sammlung herunter, indem Sie [hier](https://helpx.adobe.com/content/dam/help/en/campaign/kb/working-with-acs-api/_jcr_content/main-pars/download_section/download-1/KB_postman_collection.json.zip) klicken.

1. Öffnen Sie Postman und wählen Sie dann das Menü **Datei** / **Import**.

1. Ziehen Sie die heruntergeladene Datei in das Fenster. Vordefinierte API-Anfragen werden angezeigt und können verwendet werden.

   ![Alternativtext](assets/postman_collection.png)

1. Wählen Sie die Anfrage **Profil erstellen** und aktualisieren Sie dann die POST-Anfrage sowie den Tab **Kopfzeilen** mit Ihren eigenen Daten (&lt;ORGANISATION>, &lt;API_KEY>, &lt;ACCESS_TOKEN>). Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/setting-up-api-access.md).

   ![Alternativtext](assets/postman_uc1.png)

1. Füllen Sie den Tab **Hauptteil** mit den Daten aus, die Sie dem neuen Profil hinzufügen möchten, und klicken Sie dann auf die Schaltfläche **Senden**, um die Anfrage auszuführen.

   ![Alternativtext](assets/postman_uc2.png)

1. Nach dem Erstellen eines Objekts wird diesem ein Primärschlüssel (Pkey) zugeordnet. Er wird in der Antwort auf die Anfrage sowie in anderen Attributen angezeigt.

   ![Alternativtext](assets/postman_uc3.png)

1. Öffnen Sie Ihre Campaign Standard-Instanz und überprüfen Sie, ob das Profil mit allen Daten aus der Payload erstellt wurde.

   ![Alternativtext](assets/postman_uc4.png)
