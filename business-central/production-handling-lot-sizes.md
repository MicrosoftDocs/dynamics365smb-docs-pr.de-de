---
title: Umgang mit Losgrößen
description: In diesem Thema werden verschiedene Möglichkeiten zum Umgang mit Losgrößen beschrieben.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="handling-lot-sizes-in-production"></a>Umgang mit Losgrößen in der Produktion
In Bezug auf die Menge korreliert die Anzahl der Artikel, die Sie in einem Produktionsvorgang produzieren, möglicherweise nicht mit dem Verkauf. Sie können beispielsweise Hunderte von Artikeln in einem einzigen Los produzieren, aber jeden Artikel einzeln verkaufen. Wenn Sie Ihre Produktionswege und Stücklisten konfigurieren, sollten Sie einige Nuancen in Bezug auf die Losgrößen berücksichtigen. In diesem Thema wird beschrieben, wie sich Losgrößen auf Kostenberechnungen und Ressourcenplanung auswirken.

## <a name="units-of-measure-in-production-bill-of-materials"></a>Einheiten in der Stückliste
Obwohl Sie die Basiseinheit (UOM) für einen Artikel angeben, verwendet Ihre Stückliste möglicherweise eine andere UOM für das fertige Produkt. Beispielsweise könnte die Basis-Stückliste für einen Artikel PCS sein, Ihre Stückliste könnte jedoch eine Palette oder Tonne erfordern. Dies ist praktisch, wenn Ihre Maschinen oder Rohkomponenten die Menge bestimmen. Zum Beispiel möchten Sie wahrscheinlich kein einziges Muffin backen, da es schwierig ist, eine Portion eines Eies zu verwenden. Stattdessen backen Sie eine Menge Muffins, um den Abfall zu reduzieren. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a>Losgröße auf Arbeitsgänge
Aus Routing-Sicht können Sie für Arbeitsgänge eine Losgröße angeben, um sie an die Kapazität der Maschinen anzupassen, die die Artikel produzieren. Die Bearbeitungszeit für Arbeitsgänge wird proportional zur Losgröße reduziert. 

Dies funktioniert gut, wenn die Menge in einem Fertigungsauftrag ein Faktor für die Losgröße auf der Route ist. Wenn Ihr Backblech beispielsweise 10 Muffins aufnehmen kann, sollten Sie 10, 20, 30 usw. backen und nicht 5 oder 15.  Dies ist viel weniger ein Problem, wenn Sie mit großen Mengen arbeiten.

Die Losgröße ist auch in Fertigungsumgebungen beliebt, in denen die Ausgabe als Menge gemessen wird, die Sie während eines festgelegten Zeitraums herstellen können. Wenn beispielsweise das Volumen pro 9-Stunden-Schicht 25000 Kubikfuß beträgt, können Sie die Laufzeit auf 9 Stunden und die Losgröße auf 25000 einstellen.
Die Fertigungsauftragsmenge wird weniger wichtig, da im Fertigungsauftrag die Laufzeit als Laufzeit/Losgröße berechnet wird, um die Laufzeit pro Stück zu erhalten.
 
> [!NOTE]
> Der in der Losgröße definierte Wert hat keinen Einfluss auf die im Feld **Aufbauzeit** des Arbeitsgangs definierte Zeit. Die Einrichtung wird nur einmal durchgeführt, selbst wenn mehrere Lose vorhanden sind. Zum Beispiel, damit Sie den Ofen für die zweite Menge Muffins nicht erwärmen müssen. Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a>Losgrößen für Artikel und Lagereinheiten
Für Arbeitspläne definierte Losgrößen stimmen nicht mit Losgrößen für Artikel oder Lagereinheiten überein. Diese Werte werden für einen anderen Zweck verwendet und wirken sich nicht auf die Produktionskapazität aus. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a>Losgröße für Artikel und Lagereinheiten
Bei Artikeln und Lagereinheiten haben Losgrößen folgende Auswirkungen auf die Kostenberechnung und die Lieferplanung:

* Wenn Sie **Kosten inkl. Einrichtung** für die Standardkostenberechnung auf der Seite **Produktionseinrichtung** aktivieren, werden die Kosten für die Einrichtung zu den Standardkosten addiert. Wenn Sie eine Losgröße angeben, werden die Einrichtungskosten für den Routing-Vorgang entsprechend einer Losgröße reduziert. Wenn Ihre auf der Artikelkarte festgelegte Losgröße beispielsweise 10 beträgt und das Erhitzen des Ofens 15 Minuten dauert, werden die Kosten für den Strom für die 10 Muffins als ungefähr 1,5 Minuten zugewiesen. 

> [!NOTE]
> Die Einrichtungskosten werden aus Sicht der Standardkosten- und Kapazitätszuweisung unterschiedlich behandelt. Wenn die produzierte Menge nicht mit der auf der Artikelkarte definierten Losgröße übereinstimmt, führt dies zu Abweichungen. Weitere Informationen finden Sie unter [Lagerbestandkosten verwalten](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Bei der Lieferplanung funktioniert die Losgrößeneinstellung für Artikel mit dem **Standarddämpfer%** auf der Seite **Produktionseinrichtung**. [!INCLUDE[prod_short](includes/prod_short.md)] ignoriert Änderungen der Nachfrage, die unter dem Toleranzprozentsatz liegen, und erstellt keine Planungsvorschläge. Zum Beispiel ist 15 im Feld Standardtoleranz% angegeben, und wir haben einen Produktionsauftrag für 20 Muffins, um 20 Gäste zu verpflegen, aber ein Gast kann nicht teilnehmen. [!INCLUDE[prod_short](includes/prod_short.md)] ignoriert den einzelnen nicht anwesenden Gast, da er nur 10% der auf dem Artikel definierten Losgröße 10 entspricht. Wenn es jedoch zwei Gäste nicht schaffen, [!INCLUDE[prod_short](includes/prod_short.md)] wird vorgeschlagen, dass wir die Bestellmenge reduzieren, da zwei 20% der Losgröße entspricht. Weitere Informationen zur Planung finden Sie unter [Planung](production-planning.md).

## <a name="see-also"></a>Siehe auch
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Arbeiten mit Produktionsgsloseinheiten](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Routings erstellen](production-how-to-create-routings.md)  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
