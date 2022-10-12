---
title: So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen
description: Wenn ein Teil eines für Montage-to-Stock festgelegten Elements nicht verfügbar ist, haben Sie die Möglichkeit, einen Montageauftrag für die verbleibende Menge zu erstellen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: dafd52a1a2925c0347a455810ad727b8b89706dc
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607256"
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a>So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen

Wenn das Feld **Montagerichtlinie** auf der Artikelkarte eines Montageartikels **Lagermontage** enthält, dann nimmt der Standard-Verkaufsauftragsprozess an, dass der Artikel bereits montiert wird und aus dem Lager entnommen werden kann, wenn er verfügbar ist. Daher wird kein Montageauftrag automatisch erstellt und mit der Verkaufsauftragszeile verknüpft. Wenn jedoch ein Teil oder die gesamte Menge nicht verfügbar ist, dann Sie haben Sie die Flexibilität, einen Montageauftrag für die Restmenge zu erstellen, indem Sie das Feld **Menge für Auftragsmontage** auf der Verkaufsauftragszeile ausfüllen. Auf diese Weise können Sie die Auftragsmontage des Artikels durchführen, obwohl er standardmäßig für die Lagermontage eingerichtet ist.  

Eine ähnliche Flexibilität besteht, wenn Sie nach Auftrag zu montierende Artikel verkaufen und ein Teil der Menge sich im Lagerbestand befindet, die Sie dann von dem Montageauftrag abziehen können. Weitere Informationen finden Sie unter [Verkaufen von Lagerartikeln in Programmfertigungs-Flow](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)  

> [!NOTE]  
>  Bestimmte Regeln gelten für das Feld **Zu liefern** auf Verkaufsauftragszeilen, die eine Kombination von Auftragsmontagemengen und von Lagermengen enthalten. Weitere Informationen finden Sie im Abschnitt Kombinationsszenarien in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).  

> [!NOTE]  
>  Die folgende Vorgehensweise enthält nicht die Standardverkaufszeilenschritte, die Sie durchführen müssen, bevor Sie einen Montageauftrag für nicht verfügbare Mengen erstellen können.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen

1.  Geben Sie auf einer Verkaufsauftragszeile für einen Artikel, der im Lager montiert werden soll, im Feld **Menge** eine Menge ein, die den Lagerbestand überschreitet. Die Seite **Verfügbarkeit prüfen** wird angezeigt. Weitere Informationen finden Sie unter [Die Verfügbarkeit von Artikeln anzeigen](inventory-how-availability-overview.md)
2.  Beachten Sie das Feld **Gesamtmenge** (mit negativem Wert), das Sie im nächsten Schritt bearbeiten werden.  
3.  Geben Sie im Feld **Menge für Auftragsmontage** den Wert aus dem vorherigen Schritt ein.  
4.  Führen Sie alle Änderungen an den Montagekomponenten aus. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  
5.  Fahren Sie mit der Freigabe des Verkaufsauftrags fort, um ihn für die Kommissionierung der Lagerartikel und für die Montage der nicht verfügbaren Artikel vorzubereiten. Weitere Informationen zu Standard-Montageschritten finden Sie unter[ Artikel montieren](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Das Feld **Lagerplatzcode** auf dem Verkaufsauftrag kann entsprechend dem Feld **P-Code f. Prog.fert.lief.** oder dem Feld **Von Montagelagerplatzcode** auf der Lagerortkarte ausgefüllt sein. In diesem Fall kann das Feld **Lagerplatzcode** auf der Verkaufsauftragszeile in dieser Kombination aus Auftragsmontage- und Lagermontageartikelmengen falsch sein. Es empfiehlt sich, das Feld **Lagerplatzcode** zu prüfen und sicherzustellen, dass die Platzierung für alle Mengen funktioniert. Alternativ können Sie die beiden verschiedenen Mengen auf separaten Verkaufsauftragszeilen eingeben.  

## <a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Design Details: Lagerort Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]