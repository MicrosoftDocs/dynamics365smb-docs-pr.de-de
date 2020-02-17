---
title: Sofortiges Ausgleichen von Einkaufsrechnungen | Microsoft Docs
description: Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/29/2020
ms.author: bholtorf
ms.openlocfilehash: b38f5f97c7b5be46f1d6cd4d1bc898e72060417e
ms.sourcegitcommit: 1c286468697d403b9e925186c2c05e724d612b88
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2020
ms.locfileid: "2999619"
---
# <a name="settle-purchase-invoices-promptly"></a>Einkaufsrechnungen sofort ausgleichen
Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.  

### <a name="to-settle-purchase-invoices-promptly"></a>So gleichen Sie Einkaufsrechnungen sofort aus  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kaufrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3.  Um entweder bar oder per Banktransfer zu bezahlen, geben Sie die Nummer des Sachkontos für Barzahlungen oder die des Bankkontos in dem Feld **Gegenkontonr.** an.  

> [!IMPORTANT]  
>  Die Felder **Gegenkontoart** und **Gegenkontonr.** sind im Rechnungskopf nicht im Standard enthalten. Um die Zahlung einer Rechnung zu buchen, müssen Sie sie mit Hilfe der Designfunktionen einfügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md). 

> [!NOTE]  
>  Wenn Sie häufiger Rechnungen bar bezahlen, ist es sinnvoll, sich eine spezielle Zahlungsform mit einem Gegenkonto einzurichten und diese Methode in dem Feld **Zahlungsform** auf der Kreditorenkarte anzugeben. Die entsprechende Gegenkontonummer wird automatisch auf dem Rechnungskopf eingefügt, wenn Sie eine neue Rechnung erstellen.  

## <a name="see-also"></a>Siehe auch  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
