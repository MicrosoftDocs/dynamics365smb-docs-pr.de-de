---
title: Fakturieren von Anmeldungen in Business Central | Microsoft Docs
description: Erfahren Sie, wie Sie Massenrechnungsstellung von Microsoft Bookings in Business Central vornehmen können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9b683fa14801c00904c131ada5bcce1f669c9b2a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751005"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-prod_short"></a>Massenrechnungsstellung für Microsoft Bookings in [!INCLUDE[prod_short](includes/prod_short.md)]
Wenn Ihr Unternehmen die Bookings-App in Microsoft 365 verwendet, können Sie Massenrechnungsstellung für Termine vornehmen. Die Seite **Nicht in Rechnung gestellte Anmeldungen** in [!INCLUDE[prod_short](includes/prod_short.md)] stellt eine Liste der abgeschlossenen Anmeldungen des Mandanten bereit. Auf dieser Seite können Sie schnell die Termine auswählen, die Sie verrechnen wollen und Entwurfsrechnungen für die erbrachten Services erstellen.  

## <a name="connect-to-bookings"></a>Mit Anmeldungen verbinden
Um Ihr [!INCLUDE[prod_short](includes/prod_short.md)] mit Anmeldungen zu verbinden, müssen Sie Ihren Anmeldungsmandanten angeben, was mit Anmeldungen zu synchronisieren ist, und wie oft Sie synchronisieren möchten und welche Vorlage zu verwenden ist. Sie richten diese Daten auf der Seite **Anmeldungs-Synchronisierung einrichten** ein, die Sie auf der Seite **Exchange-Synchronisierungs-Einrichtung** starten können, die Sie unter [Suchen](ui-search.md) finden.  

Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[prod_short](includes/prod_short.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.  

> [!NOTE]
> Die Anmeldungs-App ist dafür ausgelegt, Termine für einzelne Debitoren statt Mandanten zu buchen. Die Synchronisierung mit [!INCLUDE[prod_short](includes/prod_short.md)] wird daher nur Debitorenkontakte mit einen Typ "Person" synchronisieren. Die E-Mail-Adresse ist auch erforderlich, damit der Kontakt synchronisiert wird.  

Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[prod_short](includes/prod_short.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.  

> [!NOTE]
> Nur Artikel des Typs *Service* werden wischen Buchung und [!INCLUDE[prod_short](includes/prod_short.md)]synchronisiert. Die Vorlage, die Sie auf der Seite **Konfigurationsvorlagen** einrichten, sodass Sie diese Seite für die Artikelsynchronisierung verwenden können, muss die Art *Service* haben.

## <a name="invoice-appointments"></a>Termin fakturieren
Wenn es Zeit ist, die Rechnungen über die abgeschlossenen Anmeldungen zu senden, wechseln Sie zur Seite **Nicht fakturierte Anmeldungen**. Abhängig davon, wie oft die Daten synchronisiert werden, ist die Liste lang oder kurz. Sie können Rechnungen für alle Windows-Anmeldungen in der Liste oder für eine Anmeldung nach der anderen erstellen. Sie können eine oder mehrere Posten in der Liste auswählen und nur jene fakturieren.  

Die Unterstützung für die Fakturierung von Terminen von Anmeldungen ist schneller und einfacher als der vollere Workflow für die Arbeit mit Verkaufsangeboten, Verkaufsaufträgen und Verkaufsrechnungen. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md). Sie können wählen, Ihre Services mithilfe von [!INCLUDE[prod_short](includes/prod_short.md)] zu verkaufen oder wählen, Anmeldungen zu nutzen, abhängig von Ihren Geschäftsanforderungen.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]