---
title: CNIL-Anleitung zu E-Mail-Tracking-Pixeln
description: Erfahren Sie mehr über die aktualisierten CNIL-Anleitungen zu E-Mail-Tracking-Pixeln und den Adobe Campaign Standard-Steuerelementen, die Ihre Compliance-Bemühungen unterstützen können.
audience: administration
role: Admin
level: Experienced
hide: true
source-git-commit: 75f1f4ad8f7173f4601c9cff1ea93bf4092f274d
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 0%

---


# Grundlegendes zur aktualisierten CNIL-Anleitung zu E-Mail-Tracking-Pixeln {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**Auf dieser Seite:** Erfahren Sie mehr über die CNIL-Empfehlung vom April 2026 zu E-Mail-Tracking-Pixeln und entdecken Sie die Adobe Campaign Standard-Steuerelemente - Tracking-Aktivierung, Tracking auf Link-Ebene, Einverständnisdatenmodell, Opt-out-Mechanismen und Reporting -, die Ihre Compliance-Bemühungen unterstützen können.

>[!ENDSHADEBOX]

Dieser Beitrag dient nur zu Informationszwecken. Es ist keine Rechtsberatung und garantiert nicht, dass Sie das geltende Recht einhalten. Die unten beschriebenen Adobe Campaign Standard-Produktfunktionen sind Bausteine, die eine konforme Implementierung unterstützen können, wenn sie entsprechend konfiguriert und betrieben werden. Jeder Kunde ist für die Feststellung und Erfüllung seiner Verpflichtungen nach geltendem Recht verantwortlich.

## Übersicht {#overview}

Am 14. April 2026 veröffentlichte die *Commission nationale de l&#39;informatique et des libertés* (CNIL), Frankreichs Datenschutzbehörde, eine [Empfehlung zur Verwendung von Tracking-Pixeln in E-Mails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). In der Anleitung wird klargestellt, wann eine Zustimmung erforderlich ist, und die Bedeutung ordnungsgemäßer Zustimmungspraktiken für das E-Mail-Pixel-Tracking hervorgehoben. Diese Richtlinie könnte sich auf die Versandpraktiken von Entitäten auswirken, die E-Mails an Abonnenten mit Sitz in Frankreich versenden.

CNIL räumte Unternehmen ab dem Datum der Empfehlung einen Zeitraum von drei Monaten ein, um ihre E-Mail-Empfänger („Benutzer„) über das Vorhandensein der Tracking-Pixel, ihren Zweck und das Recht der Benutzer auf Opt-out zu informieren. Während dieser Übergangsphase wird von den Kunden erwartet, dass sie die Benutzer über das Pixel-Tracking informieren und ihnen bei Bedarf ein Opt-out anbieten. CNIL wird voraussichtlich nach dem 14. Juli 2026 mit Durchsetzungsmaßnahmen beginnen.

Während die CNIL und andere Regulierungsbehörden die Leitlinien zur Verfolgung von Pixeln und damit zusammenhängenden Problemen erläutern, wird Adobe weiterhin Aktualisierungen überwachen und Kunden über die technischen Funktionen von Adobe-Produkten informieren, die E-Mail-Marketing, einschließlich Adobe Campaign Standard, unterstützen.

Adobe-Programme zur Ausführung von E-Mail-Marketing, einschließlich Adobe Journey Optimizer, Journey Optimizer B2B, Adobe Campaign und Marketo Engage, bieten Steuerelemente, mit denen Kunden das Öffnungs-Tracking auf Versand- oder E-Mail-Ebene verwalten können. Kunden sind dafür verantwortlich, ihre eigenen Compliance-Verpflichtungen gemäß den geltenden CNIL-Richtlinien und anderen Gesetzen zu bestimmen, aber diese Funktionen können die Bemühungen um die Einhaltung von Kundenrichtlinien unterstützen.

### Was ist ein E-Mail-Tracking-Pixel? {#tracking-pixel}

Ein E-Mail-Tracking-Pixel ist ein 1 x 1 transparentes Bild, das in die HTML einer E-Mail eingebettet ist. Wenn der E-Mail-Client des Empfängers dieses Bild lädt, pingt das Pixel einen Server, der Daten wie Zeitstempel, Gerätetyp, E-Mail-Client und manchmal eine IP-Adresse als ungefähren Speicherort aufzeichnet. Dieses Protokoll wird dann an den Datensatz eines Empfängers gebunden, sodass Marketing-Experten sehen können, ob eine E-Mail geöffnet wird.

### Kunden-Support {#support}

Kunden, die Unterstützung bei der Implementierung der oben beschriebenen Änderungen benötigen, können mit ihrem bestehenden Adobe-Ökosystem interagieren. Wenden Sie sich bei technischen Fragen zu den Funktionen von Adobe, auf die verwiesen wird, an Ihren Customer Success Manager oder technischen Kundenbetreuer.

## Adobe Campaign Standard-Funktionen im Zusammenhang mit dem E-Mail-Tracking {#acs-functionality}

Kunden können die nativen Tracking-, Schema- und Personalisierungsmechanismen von Adobe Campaign Standard verwenden, um bei der Konfiguration der Architektur auf bestimmte Elemente einzugehen.

### E-Mail-Klassifizierung {#email-classification}

Erweitern Sie die Versandvorlage mit einem benutzerdefinierten Feld, das den Typ der E-Mail angibt (Authentifizierung, Nur Zustellbarkeit, Transaktion, Marketing mit Einverständnis, B2B-Akquise). In Campaign Standard können Versandvorlagen benutzerdefinierte Felder enthalten, die in die Reporting- und Workflow-Logik einfließen. Diese Klassifizierung bestimmt, welches Tracking für jeden Versand geeignet ist.

[Erfahren Sie, wie Sie Versandvorlagen erstellen und verwenden](../../channels/using/creating-an-email.md)

### Einverständnisdatenmodell {#consent-data-model}

Erweitern Sie die Profilressource über den benutzerdefinierten Ressourcenmechanismus von Campaign Standard (**Administration > Entwicklung > Benutzerdefinierte Ressourcen**), um zweckbezogene Einverständniskennzeichnungen, Einverständniszeitstempel und das Datum des zuletzt geöffneten Fensters (nur Datum - keine Zeitkomponente) zu verwenden. Eine separate benutzerdefinierte Ressource, die mit dem Profil verknüpft ist, erfasst das Ereignisprotokoll „Nur anhängen“-Einverständnis, das den individuellen Einverständnisnachweis unterstützt. Da auf Campaign Standard-Landingpages direkt in Profilfelder geschrieben werden kann, ist der aktuelle Einverständnisstatus nativ verwaltbar. Das Einverständnisprotokoll wird über die Adobe Campaign Standard REST-API (`/profileAndServicesExt`) geschrieben, sobald eine Voreinstellung übermittelt wurde.

[Erfahren, wie eine Ressource erstellt oder erweitert wird](../../developing/using/creating-or-extending-the-resource.md)

[Erfahren Sie, wie Sie über die API mit benutzerdefinierten Ressourcen interagieren können](../../api/using/interacting-with-custom-resources.md)

### Pixelemission {#pixel-emission}

Adobe Campaign Standard steuert das Tracking auf Versandebene über den Umschalter **[!UICONTROL Tracking aktivieren]** in den Eigenschaften des Versands oder der Vorlage. Bei Sendungen, bei denen das offene Tracking nicht rechtmäßig ist (E-Mails, die nur zur Authentifizierung aufgefordert werden), ist dieser Umschalter deaktiviert. Bei Sendungen, bei denen eine Pixelemission pro Zweck angemessen ist, besteht ein Ansatz darin, das standardmäßig automatisch eingefügte Pixel zu deaktivieren und Inhaltsblöcke zu verwenden, die bedingte 1×1-getrackte Bildelemente enthalten - einen pro Zweck - wobei jedem Bild eine URL-Kategorie zugewiesen wird (`PIX_DELIV`, `PIX_PERF`, `PIX_PROFILE`, `PIX_FRAUD`) und nur angezeigt wird, wenn das entsprechende Einverständnis des Empfängers wahr ist.

[Informationen zum Konfigurieren von E-Mail-Tracking-Parametern](configuring-email-channel.md#tracking-parameters)

[Erfahren Sie, wie Sie in der E-Mail-Designer getrackte URLs verwalten](../../designing/using/links.md#about-tracked-urls)

[Erfahren Sie, wie Inhaltsbausteine hinzugefügt werden](../../designing/using/personalization.md#adding-a-content-block)

### Entzug {#withdrawal}

Fügen Sie jeder E **Mail-Fußzeile einen Link** Tracker-Einstellungen verwalten“ hinzu, der sich vom Abmelde-Link unterscheidet. Der Link verweist auf eine Campaign Standard-Landingpage, die über den `recipientId`- oder `urlSubscription` authentifiziert wurde. Der Empfänger bzw. die Empfängerin aktiviert bzw. deaktiviert die Einverständniskennzeichnungen für einzelne Zwecke und sendet sie. Nach der Bestätigung wird bei einem kleinen Aufruf an die Campaign Standard-REST-API das Widerrufereignis in das Einverständnisprotokoll geschrieben. In der Empfehlung wird darauf hingewiesen, dass dieser Link selbst von der Tracking-Anforderung sicherheitsausgenommen ist.

[Erfahren Sie, wie Sie Opt-in- und Opt-out-Landingpages einrichten](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages)

[Erste Schritte mit Landingpages](../../channels/using/getting-started-with-landing-pages.md)

### Nachweis der Zustimmung {#consent-proof}

Jede Einverständnisänderung - Erfassung bei der Anmeldung, Aktualisierung auf der Seite „Voreinstellungen“, Ablauf - erstellt eine Zeile in der benutzerdefinierten Ressource des Einverständnisprotokolls, die den Wortlaut des Versionscodes, den Zeitstempel der Erfassung, die Quelle und den Umfang enthält. Dieses Protokoll kann über den Campaign Standard-Explorer abgefragt, über die REST-API verfügbar gemacht und über einen geplanten Workflow zur DPO-Überprüfung exportiert werden.

[Erfahren Sie, wie Sie über die API mit benutzerdefinierten Ressourcen interagieren können](../../api/using/interacting-with-custom-resources.md)

### Governance bei erneuten Anfragen {#re-solicitation}

Ein benutzerdefiniertes `cusLastPixelRefusalDate` im Profil in Kombination mit einer Typologieregel, die Profile ausschließt, bei denen sich dieses Feld innerhalb eines bestimmten Zeitraums befindet, verhindert die erneute Abfrage von Empfängern, die in diesem Zeitraum abgelehnt haben. Ein geplanter Workflow verwaltet die Ablaufzeiten von Kundeneinverständnissen, indem veraltete Datensätze markiert und Ablaufereignisse in das Einverständnisprotokoll geschrieben werden.

[Erfahren Sie, wie Sie mit Typologieregeln arbeiten](../../sending/using/about-typology-rules.md)

[Erfahren Sie, wie Sie Typologieregeln verwalten](../../sending/using/managing-typology-rules.md)

### Reporting {#reporting}

Dynamische Berichte in Campaign Standard basieren auf URL-Kategorien und Profildimensionen. Die über der Oberfläche in dynamische Berichte eingeführten zweckbezogenen URL-Kategorien bilden neue Dimensionen, mit denen Benutzende Daten nach Zweck aufteilen und darauf klicken können. Die Unterscheidung zwischen einverstandenem und nicht einverstandenem Tracking ist nativ sichtbar, sobald die URL-Kategorien vorhanden sind.

[Erfahren Sie mehr über die ersten Schritte mit dynamischen Berichten](../../reporting/using/about-dynamic-reports.md)

[Erfahren Sie mehr über Tracking-Indikatoren](../../reporting/using/tracking-indicators.md)
