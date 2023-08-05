---
title: Ihre Buchungen in Business Central in Rechnung stellen
description: 'In diesem Thema lernen Sie, wie Sie in Microsoft Bookings Business Central Massenfakturierung durchführen können.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: edupont
---
# Massenrechnungsstellung für Microsoft Bookings in [!INCLUDE[prod_short](includes/prod_short.md)]

Wenn Ihr Unternehmen die Anmeldungs-App in Microsoft 365 verwendet, können Sie Massenrechnungsstellung für Termine vornehmen. Die Seite **Nicht fakturierte Buchungen** in [!INCLUDE[prod_short](includes/prod_short.md)] stellt eine Liste der abgeschlossenen Buchungen des Unternehmens bereit. Auf dieser Seite können Sie schnell die Termine auswählen, die Sie verrechnen wollen und Entwurfsrechnungen für die erbrachten Services erstellen.  

## Mit Anmeldungen verbinden

Um Ihr [!INCLUDE[prod_short](includes/prod_short.md)] mit Anmeldungen zu verbinden, müssen Sie Ihren Anmeldungsmandanten angeben, was mit Anmeldungen zu synchronisieren ist, und wie oft Sie synchronisieren möchten und welche Vorlage zu verwenden ist. Sie richten diese Daten auf der Seite **Anmeldungs-Synchronisierung einrichten** ein, die Sie auf der Seite **Exchange-Synchronisierungs-Einrichtung** starten können, die Sie unter [Suchen](ui-search.md) finden.  

Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[prod_short](includes/prod_short.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.  

> [!NOTE]
> Die Anmeldungs-App ist dafür ausgelegt, Termine für einzelne Debitoren statt Mandanten zu buchen. Bei der Synchronisierung mit [!INCLUDE[prod_short](includes/prod_short.md)] werden daher nur Debitorenkontakte vom Typ *Person* synchronisiert. Die E-Mail-Adresse ist auch erforderlich, damit der Kontakt synchronisiert wird.  

Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[prod_short](includes/prod_short.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.  

> [!NOTE]
> Nur Artikel des Typs *Service* werden wischen Buchung und [!INCLUDE[prod_short](includes/prod_short.md)]synchronisiert. Die Vorlage, die Sie auf der Seite **Konfigurationsvorlagen** einrichten, sodass Sie diese Seite für die Artikelsynchronisierung verwenden können, muss die Art *Service* haben.

## Termin fakturieren

Wenn es an der Zeit ist, die Rechnungen über die abgeschlossenen Buchungen zu senden, wechseln Sie zur Seite **Nicht fakturierte Buchungen**. Abhängig davon, wie oft die Daten synchronisiert werden, ist die Liste lang oder kurz. Sie können Rechnungen für alle Windows-Anmeldungen in der Liste oder für eine Anmeldung nach der anderen erstellen. Sie können eine oder mehrere Posten in der Liste auswählen und nur jene fakturieren.  

Die Unterstützung für die Fakturierung von Terminen von Anmeldungen ist schneller und einfacher als der vollere Workflow für die Arbeit mit Verkaufsangeboten, Verkaufsaufträgen und Verkaufsrechnungen. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md). Sie können wählen, Ihre Services mithilfe von [!INCLUDE[prod_short](includes/prod_short.md)] zu verkaufen oder wählen, Anmeldungen zu nutzen, abhängig von Ihren Geschäftsanforderungen.  

> [!NOTE]
> Im Mai 2022 wurde ein Problem bei der Integration in Buchungen erkannt. Derzeit erfordert die Synchronisierung von Buchungen mit [!INCLUDE [prod_short](includes/prod_short.md)] die manuelle Verknüpfung der Rechnungen mit Debitoren in [!INCLUDE [prod_short](includes/prod_short.md)].

## Siehe auch

[Finanzen](finance.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]