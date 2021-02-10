---
title: 'Vorgehensweise: Lieferbedingungen einrichten in | Microsoft Docs'
description: Sie können eine Code für jede einzelne angebotene Lieferbedingungen einrichten, wie auch die Informationen dazu angeben und die Informationen dazu eingeben.e können Sie einen Code für jeden Zusteller anlegen und Informationen dazu eingeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f1916724c995f875d15b931e919d07d2253dcdb1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748294"
---
# <a name="set-up-shipment-methods"></a>Lieferbedingungen einrichten
Lieferbedingungen nennt man auch Incoterms; sie hängen oft ab vom Artikel, den Debitoren und den Kreditoren Wenn der Debitor beispielsweise auf einer Insel lebt, kann er entscheiden, die Artikel immer auf dem Luftweg oder immer auf dem Seeweg geliefert zu bekommen. Einige Debitoren möglicherweise eine Lieferung am nächsten Tag. Einige möchten vielleicht den Auftrag abholen. Sie können auf den Debitoren- und Kreditorenkarten angeben, welche Lieferart gewünscht ist.

In der Tabelle **Lieferbedingungen** richten Sie die Beschreibung und den Code für jede Lieferbedingung ein. Sie können z. B. den Code "FOB" einrichten und im Feld **Beschreibung** können Sie "Frei an Bord" eingeben. Sie können dann den Code im Feld **Lieferbedingungscode** an anderer Stelle in der Anwendung eingeben, z. B. auf der Debitorenkarte. Wenn Sie dann neue Aufträge, Bestellungen, Rechnungen oder Gutschriften erstellen oder buchen, wird das System die Beschreibung einfügen, die zu dem Code gehört. Sie können die Standardbeträge auf dem Beleg je nach Anforderung ändern.

## <a name="to-set-up-a-shipment-code"></a>So richten Sie einen Lieferbedingungscode ein
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lieferbedingungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Lieferbedingungen** die Aktion **Neu** aus.
3. Geben Sie in der neuen Zeile einen Code und eine Beschreibung für die Lieferbedingung an.

## <a name="see-also"></a>Siehe auch
[Incoterms](https://iccwbo.org/resources-for-business/incoterms-rules)  
[Zusteller einrichten](sales-how-to-set-up-shipping-agents.md)  
[Um Pakete zu verfolgen](sales-how-track-packages.md)    
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
