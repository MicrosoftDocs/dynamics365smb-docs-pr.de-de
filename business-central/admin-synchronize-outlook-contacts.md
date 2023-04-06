---
title: Teilen Sie Kontakte zwischen Business Central und Outlook
description: 'Der Service ist in Microsoft 365 integriert, damit Sie Kontakte zwischen Outlook und Business Central freigeben können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
---
# Synchronisieren Sie Kontakte in Business Central mit Kontakten in Microsoft Outlook

Sie können die Kontaktsynchronisierung einrichten, damit Ihre Kontakte in [!INCLUDE[prod_short](includes/prod_short.md)] dieselben Informationen aufweisen wie Ihre Kontakte in Microsoft Outlook. Wenn Sie beispielsweise ein Vertriebsmitarbeiter sind, arbeiten Sie möglicherweise in Outlook und [!INCLUDE[prod_short](includes/prod_short.md)] gleichzeitig. Wenn die Kontakte an beiden Stellen identisch sind, wird die Arbeit einfacher.  

Standardmäßig werden die Kontakte, die Sie synchronisieren, in einem **Business Central**-Ordner in Ihren Favoriten im Ordnerbereich in Outlook gespeichert. Über den Business Central-Ordners können Sie einfacher ermitteln, welche Kontakte Sie synchronisieren. Sie können Filter festlegen, um nur bestimmte Kontakte von [!INCLUDE[prod_short](includes/prod_short.md)] nach Outlook zu synchronisieren. Nachdem Sie die Synchronisierung eingerichtet haben, können Sie die Synchronisierung manuell durchführen oder den Vorgang automatisieren, um die Synchronisierung auf geplanter Basis durchzuführen.  

## Voraussetzungen

- Auf Ihrem Benutzerprofil in [!INCLUDE[prod_short](includes/prod_short.md)] muss Ihr Microsoft 365 E-Mail angegeben sein.

  Sie können diese Einstellung im Abschnitt **Microsoft 365-Authentifizierung** Ihres Benutzerprofils in der Liste **Benutzer** überprüfen.
- Sie haben mit [!INCLUDE[prod_short](includes/prod_short.md)] die Kontaktsynchronisierung wie unter [Die Kontaktsynchronisierung mit Outlook für das lokale Business Central einrichten](admin-contact-sync-setup-onprem.md) beschrieben eingerichtet

## Synchronisierung einrichten

Sie geben an, wie Sie die Synchronisierung der Kontakte mit Outlook einrichten möchten auf der Seite **Exchange Synchronisierung einrichten** in [!INCLUDE[prod_short](includes/prod_short.md)]. 

Auf der Seite **Exchange Synchronisierung einrichten** können Sie die Verbindung mit Exchange überprüfen und die Synchronisierung von Kontakten festlegen. Auf der Seite **Exchange Synchronisierung einrichten** können Sie die Seite **Kontaktsynchronisierung einrichten** öffnen und die Synchronisierung starten. Legen Sie optional einen Filter fest, um anzugeben, welche Kontakte synchronisiert werden sollen. Sie können beispielsweise nach Name, Typ, Unternehmen usw. filtern. Sie können auch den Standardnamen des Ordners in Outlook ändern, mit dem die Kontakte synchronisiert werden sollen.  

Jeder Ihrer Mitarbeiter kann die eigene Exchange-Synchronisierung einrichten und die eigenen Filter für die Synchronisierung von Kontakten einrichten.  

Nachdem Sie die Synchronisierung eingerichtet haben, können Sie Änderungen am Kontakt manuell synchronisieren oder den Vorgang automatisieren, indem Sie einen Projektwarteschlangenposten einrichten. Weitere Informationen zur Automatisierung finden Sie im nächsten Abschnitt dieses Artikels.

### Synchronisierung automatisieren

Sie können einen Projektwarteschlangenposten erstellen, der Kontakte gemäß einem von Ihnen definierten Zeitplan synchronisiert. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md). 

In der folgenden Tabelle sind die Einstellungen auf der Seite **Karte für Aufgabenwarteschlangenposten** aufgelistet, die für die Synchronisierung vorgesehen sind:

|Feld|Einstellung für Kontaktsynchronisierung|
|-----|-----|
|Art des auszuführenden Objekts|Codeunit|
|ID des auszuführenden Objekts|6700|

## Kontakte synchronisieren

Wenn Sie es gewohnt sind, in [!INCLUDE[prod_short](includes/prod_short.md)] mit Kontakten zu arbeiten, ist es für Sie einfach, die Synchronisierung manuell über die Liste **Kontakte** durchzuführen, falls Sie dies wünschen. Es gibt zwei Möglichkeiten, Kontakte zu synchronisieren:

* **Mit Microsoft 365 synchronisieren**

  Synchronisieren Sie alle Änderungen von [!INCLUDE[prod_short](includes/prod_short.md)] nach Microsoft 365, die nach der letzten Synchronisierung durchgeführt wurden, basierend auf dem letzten Änderungsdatum. Außerdem werden neue Kontakte von Microsoft 365 nach [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert. Diese Aktion erfolgt in der Regel schneller als eine vollständige Synchronisierung. 

* **Vollständig mit Microsoft 365 synchronisieren**

  Synchronisieren Sie alle Kontakte in beide Richtungen unabhängig vom letzten Synchronisierungsdatum und der letzten Änderung.  

In beiden Fällen werden nur Kontakte von Outlook synchronisiert, wenn die erforderlichen Felder ausgefüllt sind. Die für die Synchronisierung mit Microsoft 365 erforderlichen Felder sind **Name** und **E-Mail-Adresse**, und der Kontakt muss vom Typ **Person** sein. [!INCLUDE[prod_short](includes/prod_short.md)] ist die Quelle der Kontaktinformationen, sodass die Kontaktinformationen von [!INCLUDE[prod_short](includes/prod_short.md)] gespeichert werden, falls Duplikate vorhanden sind.  

> [!NOTE]
> Wenn Sie einen Kontakt in Outlook löschen, ihn in [!INCLUDE[prod_short](includes/prod_short.md)] jedoch beibehalten, wird der Kontakt bei der nächsten Synchronisierung in Outlook neu erstellt. 

## Siehe auch

[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Kontakte (Personen) in Outlook im Netz verwenden](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]