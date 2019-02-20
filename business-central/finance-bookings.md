---
title: Fakturieren von Anmeldungen in  Business Central | Microsoft Docs
description: "Erfahren Sie, wie Sie Massenrechnungsstellung von Microsoft Bookings in Business Central vornehmen können."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 01/07/2019
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: a98027c3ef3171491f84197897f93cbed4e288c2
ms.openlocfilehash: 65542f3855eff3a5ed117bff3247adbf05def6e2
ms.contentlocale: de-de
ms.lasthandoff: 01/07/2019

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a>Massenrechnungen für Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn Ihr Unternehmen die Anmeldungs-App in Office 365 verwendet, können Sie Massenrechnungsstellung für Termine vornehmen. Die Seite **Nicht in Rechnung gestellte Anmeldungen** in [!INCLUDE[d365fin](includes/d365fin_md.md)] stellt eine Liste der abgeschlossenen Anmeldungen des Mandanten bereit. Auf dieser Seite können Sie schnell die Termine auswählen, die Sie verrechnen wollen und Entwurfsrechnungen für die erbrachten Services erstellen.  

## <a name="connect-to-bookings"></a>Mit Anmeldungen verbinden
Um Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Anmeldungen zu verbinden, müssen Sie Ihren Anmeldungsmandanten angeben, was mit Anmeldungen zu synchronisieren ist, und wie oft Sie synchronisieren möchten und welche Vorlage zu verwenden ist. Sie richten diese Daten auf der Seite **Anmeldungs-Synchronisierung einrichten** ein, die Sie auf der Seite **Exchange-Synchronisierungs-Einrichtung** starten können, die Sie unter [Suchen](ui-search.md) finden.  

Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.  

> [!NOTE]
> Die Anmeldungs-App ist dafür ausgelegt, Termine für einzelne Debitoren statt Mandanten zu buchen. Die Synchronisierung mit [!INCLUDE[d365fin](includes/d365fin_md.md)] wird daher nur Debitorenkontakte mit einen Typ "Person" synchronisieren. Die E-Mail-Adresse ist auch erforderlich, damit der Kontakt synchronisiert wird.  

Wenn Sie beispielsweise Debitoren zwischen Anmeldungen und [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren möchten, müssen Sie die Standardvorlage angeben, die sie verwenden möchten, um neue Debitoren basierend auf den [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren in Ihrem Anmeldungsmandanten hinzuzufügen.  

> [!NOTE]
> Nur Artikel des Typs *Service* werden wischen Buchung und [!INCLUDE[d365fin](includes/d365fin_md.md)]synchronisiert. Die Vorlage, die Sie auf der Seite **Konfigurationsvorlagen** einrichten, sodass Sie diese Seite für die Artikelsynchronisierung verwenden können, muss die Art *Service* haben.

## <a name="invoice-appointments"></a>Termin fakturieren
Wenn es Zeit ist, die Rechnungen über die abgeschlossenen Anmeldungen zu senden, wechseln Sie zur Seite **Nicht fakturierte Anmeldungen**. Abhängig davon, wie oft die Daten synchronisiert werden, ist die Liste lang oder kurz. Sie können Rechnungen für alle Windows-Anmeldungen in der Liste oder für eine Anmeldung nach der anderen erstellen. Sie können eine oder mehrere Posten in der Liste auswählen und nur jene fakturieren.  

Die Unterstützung für die Fakturierung von Terminen von Anmeldungen ist schneller und einfacher als der vollere Workflow für die Arbeit mit Verkaufsangeboten, Verkaufsaufträgen und Verkaufsrechnungen. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md). Sie können wählen, Ihre Services mithilfe von [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verkaufen oder wählen, Anmeldungen zu nutzen, abhängig von Ihren Geschäftsanforderungen.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  

