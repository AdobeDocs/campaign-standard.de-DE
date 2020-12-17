---
solution: Campaign Standard
product: campaign
title: Einschränkungen bei Transaktionsnachrichten
description: Erfahren Sie mehr über die wichtigsten Empfehlungen und Einschränkungen für Transaktionsnachrichten in Adobe Campaign Standard.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: 0092ad11314fab232663f558ca6635b8fcc03133
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 83%

---


# Best Practices und Einschränkungen bei Transaktionsnachrichten {#transactional-messaging-limitations}

<img src="assets/do-not-localize/icon_concepts.svg" width="60px">

In diesem Abschnitt werden die Best Practices und Einschränkungen Liste, die Sie vor dem Erstellen von Transaktionsnachrichten beachten sollten.

<!--For more on transactional messages, including on how to configure and create them, see [Getting started with transactional messaging](../../channels/using/getting-started-with-transactional-msg.md).-->

## Berechtigungen {#permissions}

Nur Benutzer mit der Rolle [Administration](../../administration/using/users-management.md#functional-administrators) können Transaktionsereignisse konfigurieren und auf Transaktionsnachrichten zugreifen.

## Konfiguration und Publikation von Ereignissen {#design-and-publication}

Bei der Konfiguration und Publikation von Transaktionsereignissen können manche Schritte nicht mehr rückgängig gemacht werden. Achten Sie bitte auf folgende Einschränkungen:

* Die für Transaktionsnachrichten verfügbaren Kanäle sind: **[!UICONTROL E-Mail]**, **[!UICONTROL Mobil (SMS)]** und **[!UICONTROL Push-Benachrichtigung]**.
* Für jede Ereigniskonfiguration kann jeweils nur ein Kanal verwendet werden. Siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event).
* Nach der Erstellung des Ereignisses lässt sich der Kanal nicht mehr ändern. Deshalb müssen Sie den Mechanismus festlegen, über den eine Nachricht im Fall einer erfolglosen Sendung über einen anderen Kanal mit einem Workflow gesendet werden kann. Siehe [Workflow-Daten und -Prozesse](../../automating/using/get-started-workflows.md).
* Nach der Erstellung des Ereignisses können Sie die Zielgruppendimension (**[!UICONTROL Echtzeit-Ereignis]** or **[!UICONTROL Profil]**) nicht mehr ändern. Siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event).
* Es ist nicht möglich, eine Publikation rückgängig zu machen, Sie können aber ein Ereignis depublizieren: Dadurch wird der Zugriff auf das Ereignis und die damit verknüpften Transaktionsnachrichten gesperrt. Siehe [Ereignis depublizieren](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).
* Die einzige Transaktionsnachricht, die mit einem Ereignis verknüpft werden kann, ist die Nachricht, die automatisch beim Publizieren dieses Ereignisses erstellt wird. Siehe [Vorschau erstellen und Ereignis publizieren](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

## Anzahl der Transaktionsnachrichten {#transactional-message-number}

Die Anzahl der veröffentlichten Transaktionsnachrichten kann erhebliche Auswirkungen auf Ihre Plattform haben. Um eine optimale Leistung zu erzielen, sollte die Anzahl der veröffentlichten Transaktionsnachrichten unter 100 bleiben. Um dies sicherzustellen, machen Sie die Veröffentlichung oder das Löschen nicht verwendeter Transaktionsnachrichten rückgängig. Siehe [Rückgängigmachen der Veröffentlichung einer Transaktionsnachricht](../../channels/using/publishing-transactional-message.md#unpublishing-a-transactional-message) und [Löschen einer Transaktionsnachricht](../../channels/using/publishing-transactional-message.md#deleting-a-transactional-message).

Um eine optimale Leistung zu gewährleisten, können Sie auch die Veröffentlichung oder das Löschen nicht verwendeter Ereignis rückgängig machen. Wenn Sie die Veröffentlichung eines Ereignisses rückgängig machen oder löschen, wird auch die Veröffentlichung oder Löschung der entsprechenden Transaktionsnachricht(n) sowie deren Versand und Trackinglogs (sofern vorhanden) rückgängig gemacht. Siehe [Rückgängigmachen der Veröffentlichung eines Ereignisses](../../channels/using/publishing-transactional-event.md#unpublishing-an-event) und [Löschen eines Ereignisses](../../channels/using/publishing-transactional-event.md#deleting-an-event).

## Personalisierung          {#personalization}

Die Möglichkeiten zur Personalisierung eines Nachrichteninhalts hängt vom Typ der Transaktionsnachricht ab. Unten finden Sie die Spezifikationen.

### Ereignisbasierte Transaktionsnachrichten

* Die Personalisierungsinformationen stammen von den im Ereignis selbst enthaltenen Daten. Siehe [Konfiguration ereignisbasierter Transaktionsnachrichten](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages).
* Sie können in einer Ereignis-Transaktionsnachricht **keine** Inhaltsbausteine für **[!UICONTROL Abmelde-Links]** verwenden.
* Beim ereignisbasierten Transaktionsnachrichtenversand sollen ausschließlich die Daten verwendet werden, die im gesendeten Ereignis der Personalisierung von Empfängern und Nachrichteninhalten dienen. Der Inhalt Ihrer Transaktionsnachricht lässt sich jedoch durch die Verwendung von in der Adobe-Campaign-Datenbank enthaltenen Informationen anreichern. Siehe [Ereignisse anreichern](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) und [Transaktionsnachrichten personalisieren](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).
* Da Ereignis-Transaktionsnachrichten keine Profilinformationen enthalten, sind sie nicht mit Ermüdungsregeln kompatibel (auch nicht, wenn sie mit Profilen angereichert werden). 

### Profilbasierte Transaktionsnachrichten  

* Die Personalisierungsinformationen können von den im Ereignis enthaltenen Daten oder von den abgestimmten Profildaten stammen. Siehe [Konfiguration profilbasierter Transaktionsnachrichten](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) und [Besonderheiten profilbasierter Transaktionsnachrichten](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities).
* Sie **können in einer Profil-Transaktionsnachricht** Inhaltsbausteine für **[!UICONTROL Abmelde-Links]** verwenden. Siehe [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block).
* Ermüdungsregeln sind mit Profil-Transaktionsnachrichten kompatibel. Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md).

### Produktlisten

Beachten Sie, dass Produktlisten nur in **E-Mail-Transaktionsnachrichten** verfügbar sind. Siehe [Produktlisten in Transaktionsnachrichten verwenden](../../channels/using/editing-transactional-message.md#using-product-listings-in-a-transactional-message).

## Branding {#permissions-and-branding}

Beim [Branding](../../administration/using/branding.md) bieten Transaktionsnachrichten weniger Flexibilität als Standardnachrichten. Adobe empfiehlt, alle in Transaktionsnachrichten verwendeten Marken mit der Organisationseinheit **[!UICONTROL Alle]**[ zu verknüpfen](../../administration/using/organizational-units.md). Weiterführende Informationen dazu finden Sie in der unten stehenden Erläuterung.

Bei der Bearbeitung einer Transaktionsnachricht können Sie sie mit einer Marke verknüpfen, um einige Parameter automatisch einzufügen, wie z. B. den Markennamen oder das Markenlogo. In den Eigenschaften der Transaktionsnachricht ist standardmäßig die **[!UICONTROL Standardmarke]** ausgewählt.

![](assets/message-center_branding.png)

Alle in einer Transaktionsnachricht verwendeten Objekte (einschließlich der Marke) müssen in der Organisationseinheit **[!UICONTROL Message Center]** sichtbar sein, d. h. diese Objekte müssen sich in der Organisationseinheit **[!UICONTROL Message Center]** oder **[!UICONTROL Alle]** befinden.

Wenn aber die in den Nachrichteneigenschaften ausgewählte Marke mit einer anderen Organisationseinheit als **[!UICONTROL Message Center]** oder **[!UICONTROL Alle]** verknüpft ist, tritt ein Fehler auf und die Transaktionsnachricht kann nicht gesendet werden.

Deshalb müssen Sie im Fall von Multibranding bei Transaktionsnachrichten alle Marken entweder mit der Organisationseinheit **[!UICONTROL Message Center]** oder **[!UICONTROL Alle]** verknüpfen.

## Transaktionsnachrichten exportieren und importieren {#exporting-and-importing-transactional-messages}

* Um eine Transaktionsnachricht zu exportieren, müssen Sie bei der [Erstellung des Package-Exports](../../automating/using/managing-packages.md#creating-a-package) die entsprechende Ereigniskonfiguration einbeziehen.
* Nachdem die Transaktionsnachricht [in einem Package importiert wurde](../../automating/using/managing-packages.md#importing-a-package), wird sie nicht mehr in der Liste der Transaktionsnachrichten angezeigt. [Publizieren](../../channels/using/publishing-transactional-event.md) Sie die Ereigniskonfiguration, um die damit verbundene Transaktionsnachricht verfügbar zu machen.
