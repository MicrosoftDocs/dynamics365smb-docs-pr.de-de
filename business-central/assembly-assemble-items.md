---
title: Montageverwaltung | Microsoft Docs
description: Für Unternehmen, die Produkte für ihre Debitoren herstellen, indem sie Komponenten in einfachen Prozessen kombinieren, und die keine Fertigungsfunktionen benötigen, bietet jedoch Funktionen, um Artikel zu montieren, die sich in bestehende Funktionen einfügen, beispielsweise Verkaufs-, Planungs-, Reservierungs- und Lagerfunktionen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 983dbc4ee6f4efb3a710c08916a814a0195fd650
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935923"
---
# <a name="assembly-management"></a>Montageverwaltung
Für Unternehmen, die Produkte für ihre Debitoren herstellen, indem sie Komponenten in einfachen Prozessen kombinieren, und die keine Fertigungsfunktionen benötigen, bietet [!INCLUDE[d365fin](includes/d365fin_md.md)] Funktionen, um Artikel zu montieren, die sich in bestehende Funktionen einfügen, beispielsweise Verkaufs-, Planungs-, Reservierungs- und Lagerfunktionen.  

 Ein Montageartikel wird als verkäuflicher Artikel definiert, der eine Montagestückliste enthält. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

 Montageaufträge sind, genau wie Fertigungsaufträge, interne Aufträge, die verwendet werden, um den Montagevorgang zu verwalten und die Verkaufsanforderungen mit den jeweiligen Lageraktivitäten zu verbinden. Montageaufträge unterscheiden sich von anderen Auftragsarten, da beim Buchen sowohl eine Istmeldung als auch ein Verbrauch vorliegt. Der Montageauftragskopf verhält sich ähnlich zu einer Verkaufsauftragszeile und die Montageauftragszeilen verhalten sich ähnlich zu den Verbrauchs Buch.-Blattzeilen.  

 Um eine Just-In-Time-Logistikstrategie sowie die Möglichkeit, Produkte an Debitorenanfragen anzupassen, zu unterstützen, können Montageaufträge automatisch erstellt und verknüpft werden, sobald die Verkaufsauftragszeile erstellt wird. Die Verknüpfung zwischen dem Verkaufsbedarf und dem Montagezubehör aktiviert Verkaufsauftragsprozessoren, um den Montageartikel während der Verarbeitung anzupassen, Liefertermine entsprechend der Komponentenverfügbarkeit zuzusagen und Istmeldung und Lieferung des gefertigten Artikels direkt aus der Verkaufsauftragsschnittstelle zu buchen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

 In einer Verkaufsauftragszeile können Sie eine Menge verkaufen, die verfügbar ist und die zusammen mit einer Menge, die für den Auftrag montiert werden muss, aus dem Lagerbestand kommissioniert werden muss. Es sind bestimmte Regeln vorhanden, um die Verteilung solcher Mengen zu steuern und sicherzustellen, dass Auftragsmontagemengen bei einer Teillieferung Priorität vor Lagerbestandsmengen haben. Weitere Informationen finden Sie im Abschnitt "Kombinationsszenarien" in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Es sind spezielle Funktionen vorhanden, um den Versand von Auftragsmontagemengen zu steuern. Sobald eine Auftragsmontagemenge für die Lieferung bereitsteht, bucht der zuständige Lagermitarbeiter für die betroffenen Verkaufsauftragszeilen eine Lagerkommissionierung. Dieses wiederum erstellt eine Lagerbestandsumlagerung für die Komponenten, bucht den Montageausstoß und die Verkaufsauftragslieferung. Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in [Artikel mit Lagerkommissionierungen auswählen](warehouse-how-to-pick-items-with-inventory-picks.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Erhalten Sie Informationen zum Unterschied zwischen der Montage von Artikeln direkt vor dem Versand der Verkaufsaufträge und der Montage von Artikeln, die für das Lager bestimmt sind.|[Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Füllen Sie die Felder auf Lagerortkarten und in der Lagereinrichtung aus, um zu definieren, wie der Fluss der Artikel in der Montageabteilung ist.|[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Anpassung eines Montageartikels auf Anforderung eines Debitors während des Vertriebsprozesses, und Umwandlung in einen Verkauf nach der Akzeptanz.|[Angebot eines Auftragsmontageverkaufs](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombinieren von Komponenten, um einen Artikel in einem einfachen Verfahren für einen Auftrag oder das Lager zu erstellen.|[Artikel montieren](assembly-how-to-assemble-items.md)|  
|Verkaufen Sie Montageartikel, die zu dem Zeitpunkt nicht verfügbar sind, indem Sie einen verknüpften Montageauftrag erstellen, um die gesamte oder einen Teil der Verkaufauftragsmenge zu beziehen.|[Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md)|
|Wenn einige Auftragsmontageartikel bereits im Lager vorhanden sind, dann ziehen Sie die Menge von dem Montageauftrag ab und reservieren sie aus dem Lager.|[So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Wenn Sie Montageartikel aus dem Lagerbestand verkaufen und nicht alle Artikel verfügbar sind, können Sie einen Montageauftrag veranlassen, um einen Teil oder die gesamte Verkaufsauftragsmenge liefern zu können.|[So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Wie für jedem anderen Artikel, können Sie auch Rahmenaufträge für benutzerdefinierte Montageartikel erstellen, bevor Sie die tatsächlichen Verkaufsaufträge in regelmäßigen Abständen entsprechend der Rahmenbestellung erstellen.|[Erstellen von Montagerahmenaufträgen](assembly-how-to-create-blanket-assembly-orders.md)|
|Rückgängigmachen eines gebuchten Montageauftrags, beispielsweise wenn der Auftrag mit Fehlern gebucht wurde, die korrigiert werden müssen.|[Montagesbuchungen rückgängig machen](assembly-how-to-undo-assembly-posting.md)|
|Erhalten Sie weitere Informationen zum Unterschied zwischen Montagestücklisten und Fertigungsstücklisten und die entsprechenden Verarbeitungsunterschiede.|[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)|
|Erfahren Sie, wie der Verbrauch für die Montage und den Ausstoß behandelt werden, wenn Sie Montageaufträge buchen, und wie der abgeleitete Artikel und die Ressourcenkosten verarbeitet und in die Finanzbuchhaltung übergeben werden.|[Designdetails: Montageauftragsbuchung](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Siehe auch  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
