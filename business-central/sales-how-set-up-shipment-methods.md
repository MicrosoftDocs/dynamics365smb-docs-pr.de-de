---
title: Lieferbedingungen einrichten
description: Sie können eine Code für jede einzelne angebotene Lieferbedingungen einrichten, wie auch die Informationen dazu angeben und die Informationen dazu eingeben.e können Sie einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778572"
---
# <a name="set-up-shipment-methods"></a>Lieferbedingungen einrichten

Lieferbedingungen hängen häufig von den Debitoren, Kreditoren und den Artikeln ab. Wenn der Debitor beispielsweise auf einer Insel lebt, kann er entscheiden, die Artikel immer auf dem Luftweg oder immer auf dem Seeweg geliefert zu bekommen. Einige Debitoren möglicherweise eine Lieferung am nächsten Tag. Einige möchten vielleicht den Auftrag abholen. Sie können auf den Debitoren- und Kreditorenkarten angeben, welche Lieferart gewünscht ist.

In der Tabelle **Lieferbedingungen** richten Sie die Beschreibung und den Code für jede Lieferbedingung ein. Sie können z. B. den Code "FOB" einrichten und im Feld **Beschreibung** können Sie "Frei an Bord" eingeben. Sie können dann den Code im Feld **Lieferbedingungscode** an anderer Stelle in der Anwendung eingeben, z. B. auf der Debitorenkarte. Wenn Sie dann neue Aufträge, Bestellungen, Rechnungen oder Gutschriften erstellen oder buchen, wird das System die Beschreibung einfügen, die zu dem Code gehört. Sie können die Standardbeträge auf dem Beleg je nach Anforderung ändern.

## <a name="to-set-up-a-shipment-method"></a>So richten Sie eine Lieferbedingung ein

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lieferbedingungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Lieferbedingungen** die Aktion **Neu** aus.
3. Geben Sie in der neuen Zeile einen Code und eine Beschreibung für die Lieferbedingung an.

> [!TIP]
> Wenn Sie Incoterms verwenden, richten Sie Versandmethoden ein, um die relevanten Incoterms-Regeln darzustellen.  

## <a name="see-also"></a>Siehe auch

[Zusteller einrichten](sales-how-to-set-up-shipping-agents.md)  
[Um Pakete zu verfolgen](sales-how-track-packages.md)  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterms auf iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]