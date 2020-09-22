---
title: 'Vorgehensweise: Verkaufen von Lagerartikel in Programmfertigungs-Flüssen | Microsoft Docs'
description: Wenn der Montageartikels für die Auftragsmontage eingerichtet ist, dann nimmt der Standard-Verkaufsauftragsprozess an, dass der Artikel nicht auf Lager ist und für den jeweiligen Verkaufsauftrag montiert werden muss. Daher wird ein Montageauftrag automatisch erstellt, wenn Sie den Artikel einer Verkaufsauftragszeile hinzufügen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4386888ed1c4803787938161f8c9e1071dd524e4
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786046"
---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen
Wenn das Feld **Montagerichtlinie** auf der Artikelkarte eines Montageartikels **Auftragsmontage** enthält, dann nimmt der Standard-Verkaufsauftragsprozess an, dass der Artikel nicht auf Lager ist und für den jeweiligen Verkaufsauftrag montiert werden muss. Daher wird ein Montageauftrag automatisch erstellt, wenn Sie den Artikel einer Verkaufsauftragszeile hinzufügen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md). Wenn jedoch ein Teil der Verkaufsauftragsmenge bereits im Lagerbestand verfügbar ist, können Sie die Menge des Montageauftrags verringern, indem Sie das Feld **Menge für Auftragsmontage** auf der Verkaufsauftragszeile ändern.  

Dieses Szenario ist selten, da Auftragsmontageartikel normalerweise immer individuell gefertigt werden und nur eine geringe Möglichkeit dafür besteht, dass sie genau mit den angefragten Spezifikationen auf Lager sind. Wenn ein Mandant jedoch die Auftragsmontagemengen aufgrund von Rücklieferungen oder Stornierungen auf Lager hat, sollten diese Mengen kommissioniert und verkauft werden, bevor weitere Montagen vorgenommen werden.  

> [!NOTE]  
>  Es gibt keine Funktionalität in den Verkaufsaufträgen, die Sie automatisch darauf hinweist oder dabei unterstützt, Montageauftragsmengen, die bereits verfügbar sind, abzuziehen. Stattdessen müssen Sie die Verfügbarkeitsinformationen, wie in der Infobox **VK-Zeilendetails**, überwachen.  

Ähnliche Funktionen sind verfügbar, wenn Sie Montageartikel aus dem Lagerbestand verkaufen und die Menge teilweise oder vollständig nicht verfügbar ist und durch einen Montageauftrag beschafft werden kann. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln und Lagerartikeln zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

> [!NOTE]  
>  Bestimmte Regeln gelten für das Feld **Zu liefern** auf Verkaufsauftragszeilen, die eine Kombination von Auftragsmontagemengen und von Lagermengen enthalten. Weitere Informationen finden Sie im Abschnitt Kombinationsszenarien in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).  

Bei diesem Verfahren ersetzen Sie Auftragsmontagemengen durch Lagerbestandsmengen auf einer Verkaufsauftragszeile. Zu den Schritten gehören das Erkennen dieser Verfügbarkeit, das Abziehen dieser Menge von dem verknüpften Montageauftrag und dann die Reservierung der Lagermenge, um sicherzustellen, dass sie für den Auftrag kommissioniert und geliefert wird.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2.  Erstellen Sie einen Auftrag. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3.  Geben Sie auf einer Verkaufsauftragszeile für einen Auftragsmontageartikel im Feld **Menge** die verlangte Menge ein.  
4.  Sehen Sie in der Infobox **VK-Zeilendetails** nach, ob die gesamte oder ein Teil der verlangten Menge verfügbar ist.  
5.  Ziehen Sie im Feld **Menge für Auftragsmontage** die verfügbare Menge ab, so dass nur die nichtverfügbare Menge gemäß dem Auftrag montiert wird. Das Feld **Reservierte Menge** " wird entsprechend verringert, um zu berücksichtigen, dass der Auftrag-zu-Auftrag-Link oder die Reservierung sich nur auf die zu montierende Menge bezieht.  
6.  Klicken Sie auf dem Inforegister **Zeilen** auf **Funktionen** und wählen Sie dann die Aktion **Reservieren**.  
7.  Wählen Sie auf der Seite **Reservierung** den Artikelposten, der die verfügbaren Mengen enthält, wählen Sie die Option **Von aktueller Zeile reservieren**, und klicken Sie dann auf die Schaltfläche **OK**.  

    Auf der Seite **Verkaufsauftrag** zeigt das Feld **Reservierte Menge** jetzt an, dass die gesamte Auftragpositionsmenge reserviert ist. Das Feld **Menge für Auftragsmontage** spiegelt noch die Untermenge wider, die montiert werden muss.  

8.  Geben Sie den Verkaufsauftrags für die Kommissionierung der Lagerartikel und für die Montage der nicht verfügbaren Artikel frei. Weitere Informationen finden Sie unter [Entnahme von Artikeln](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Das Feld **Lagerplatzcode** auf dem Verkaufsauftrag kann entsprechend dem Feld **P-Code f. Prog.fert.lief.** oder **Von Montagelagerplatzcode** auf der Lagerortkarte ausgefüllt sein. In diesem Fall kann das Feld **Lagerplatzcode** auf der Verkaufsauftragszeile in dieser Kombination aus Auftragsmontage- und Lagermontageartikelmengen falsch sein. Es empfiehlt sich, das Feld **Lagerplatzcode** zu prüfen und sicherzustellen, dass die Platzierung für alle Mengen funktioniert. Alternativ können Sie die beiden verschiedenen Mengen auf separaten Verkaufsauftragszeilen eingeben.  

## <a name="see-also"></a>Siehe auch  
[Montageverwaltung](assembly-assemble-items.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
