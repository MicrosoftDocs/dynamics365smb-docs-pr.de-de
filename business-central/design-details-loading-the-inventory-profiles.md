---
title: 'Designdetails: Laden der Bestands-Profile | Microsoft Docs'
description: Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5b47a898b7e1d574abaf521e917f780fd105c4a8
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-loading-the-inventory-profiles"></a>Designdetails: Laden der Bestands-Profile
Um die vielen Quellen von Nachfrage und Angebot zu sortieren, organisiert das Planungssystem sie auf zwei Zeitachsen, die Bestandsprofile genannt werden.  

 Die normalen Typen von Bedarf und Vorrat mit Fälligkeitsdaten auf oder nach dem Planungsstartdatum werden in die Bestandsprofile geladen. Wenn sie geladen werden, werden die verschiedenen Bedarf- und Vorrattypen entsprechend allgemeinen Prioritäten, wie Fälligkeitsdatum, Stücklistenebenen, Lagerort und Variante sortiert. Darüber hinaus werden Auftragsprioritäten auf verschiedene Arten angewendet, um sicherzustellen, dass der wichtigste Bedarf zuerst erfüllt wird. Weitere Informationen finden Sie unter [Designdetails: Aufträge priorisieren](design-details-prioritizing-orders.md).  

 Wie bereits erwähnt, kann Bedarf auch negativ sein. Das bedeutet, dass es als Vorrat behandelt werden sollte, jedoch anders als die normalen Vorratstypen, gilt negativer Bedarf als fester Vorrat. Das Planungssystem kann dies berücksichtigen, schlägt aber keine Änderungen dafür vor.  

 Im Allgemeinen berücksichtigt das Planungssystem alle Beschaffungsaufträge nach dem Startdatum als änderbar, um den Bedarf zu erfüllen. Sobald eine Menge von einem Beschaffungsauftrag gebucht wurde, kann sie jedoch vom Planungssystem nicht mehr geändert werden. Entsprechend können die folgenden verschiedenen Aufträge nicht neu geplant werden:  

-   Freigegebene Fertigungsaufträge, bei denen Verbrauch oder Ausgabe gebucht wurde.  

-   Montageaufträge, bei denen Verbrauch oder Ausgabe gebucht wurde.  

-   Umlagerungsaufträge, in denen Lieferung gebucht wurde.  

-   Einkaufsbestellungen, in denen der Wareneingang gebucht wurde.  

 Abgesehen vom Laden von Bedarf- und Vorrattypen werden bestimmte Typen im Hinblick auf besondere Regeln und Abhängigkeiten geladen, die nachfolgend beschrieben werden.  

## <a name="item-dimensions-are-separated"></a>Artikeldimensionen sind aufgeteilt  
 Der Beschaffungsplan muss pro Kombination der Artikeldimensionen, wie Variante und Lagerort berechnet werden. Es gibt jedoch keinen Grund, eine theoretische Kombination zu berechnen. Nur jene Kombinationen, die einen Bedarf ausführen und/oder Bedarfsposten müssen berechnet werden.  

 Das Planungssystem steuert dies, indem es das Bestandsprofil durchläuft. Wenn eine neue Kombination gefunden wird, erstellt die Anwendung einen internen Steuerdatensatz, der die tatsächlichen Kombinationsinformationen enthält. Das Programm fügt die SKU als Steuerdatensatz oder externe Schleife ein. Als Ergebnis werden die richtigen Planungsparameters entsprechend einer Kombination aus Variante und Lagerort gesetzt, und die Anwendung kann an die inneren Schleife übergehen.  

> [!NOTE]  
>  Das Programm verlangt nicht, dass der Benutzer einen SKU-Datensatz eingibt, wenn ein Bedarf und/oder ein Vorrat für eine bestimmte Kombination von Variante und Lagerort eingegeben wird. Wenn Lagerhaltungsdaten für eine angegebene Kombination nicht vorhanden sind, erstellt die Anwendung einen eigenen temporären Lagerhaltungsdatendatensatz basierend auf den Artikelkartendaten. Wenn „Lagerort erforderlich“ im Bestandseinrichtungsfenster auf „Ja“ gesetzt ist, muss entweder eine SKU erstellt werden, oder „Komponenten am Lagerort“ muss auf „Ja“ gesetzt werden. Weitere Informationen finden Sie unter [Designdetails: Bedarf an leerem Lagerort](design-details-demand-at-blank-location.md)  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serien-/Chargennummern werden durch die Spezifikations-Ebene geladen  
 Attribute in Form von Serien-/Chargennummern werden in die Bestandsprofile zusammen mit dem Bedarf und dem Vorrat geladen, denen sie zugeordnet sind.  

 Bedarfs- und Vorratsattribute werden nach Auftragspriorität sowie nach Spezifikationsebene angeordnet. Da Serien-/Chargennummernübereinstimmungen die Ebene der Spezifikation widerspiegeln, gilt: Der spezifischere Bestand, wie etwa eine Chargennummer, die speziell nach Verkaufszeile ausgewählt wurde, sucht eine Übereinstimmung vor einem weniger spezifischen Bestand, etwa einem Verkauf aus einer beliebigen ausgewählten Chargennummer.  

> [!NOTE]  
>  Es gibt keine dedizierten Prioritisierungsregeln für serien-/chargennummerierten Bedarf und Vorrat, außer den Ebenen der Spezifikation, die durch ihre Kombinationen von Serien- und der Chargennummern und die Artikelverfolgungseinrichtung der einbezogenen Artikel definiert sind.  

 Während des Ausgleichs betrachtet das Planungssystem Vorrat mit Serien-/Chargennummern als nicht flexibel und versucht nicht, diese Beschaffungsaufträge zu erhöhen oder umzuplanen (sofern sie nicht in einer Auftrag-zu-Auftrag-Beziehung verwendet werden). Vgl. Auftrag-zu-Auftrags-Link werden nie unterbrochen). Diese schützt das Vorrat davor, mehrere und möglicherweise widersprüchliche Ereignismeldungen zu erhalten, wenn eine Bedarfssicherung unterschiedliche Attribute hat, etwa eine Sammlung verschiedener Seriennummern.  

 Ein weiterer Grund dafür, dass Serien-/Chargen-nummerierter Vorrat unflexibel ist, besteht darin, dass Serien-/Chargennummern allgemein so spät im Prozess zugewiesen werden, dass Änderungsvorschläge verwirrend wären.  

 Der Ausgleich der Serien-/Chargennummern berücksichtigt nicht die [Fixierte Zone](design-details-dealing-with-orders-before-the-planning-starting-date.md). Wenn Bedarf und Vorrat nicht synchronisiert sind, schlägt das Planungssystem Änderungen vor oder neue Aufträge, unabhängig vom Startdatum der Planung.  

## <a name="order-to-order-links-are-never-broken"></a>Auftrag-zu-Auftrag-Links werden nie unterbrochen.  
 Wenn ein Auftrag-zu-Auftrag-Artikel geplant wird, darf der verknüpfte Vorrat nicht für einen anderen Bedarf verwendet werden, als den, für den er ursprünglich gedacht war. Der verknüpfte Bedarf sollte nicht durch einen anderen zufälligen Vorrat abgedeckt werden, selbst wenn er in der derzeitigen Situation nach Zeit und Menge verfügbar ist. Beispielsweise kann ein Montageauftrag, der mit einem Verkaufsauftrag in einem Auftragsfertigungsszenario verknüpft ist, nicht verwendet werden, um anderen Bedarf zu decken.  

 Auftrag-zu-Auftrag-Bedarfe und Angebot müssen sich genau ausgleichen. Das Planungssystem stellt den Vorrat unter allen Umständen sicher, ohne Auftragsdimensionierungsparameter, -modifizierer oder Mengen im Bestand (ausgenommen Mengen im Zusammenhang mit den verknüpften Aufträgen) zu berücksichtigen. Aus dem gleichen Grund schlägt das System die Minderung überschüssigen Vorrats vor, wenn der verknüpfte Bedarf vermindert wird.  

 Dieser Ausgleich beeinflusst auch die zeitliche Steuerung. Der begrenzte Zeitraum, der durch den Zeitrahmen gewährt wird, wird nicht berücksichtigt; der Vorrat wird neu geplant, wenn die zeitliche Steuerung des Bedarfs geändert wurde. Es wird jedoch die Toleranzzeit berücksichtigt und Auftrag-zu-Auftrag-Vorrat wird nicht ausgeplant, ausgenommen interner Vorrat eines mehrstufigen Fertigungsauftrags (Projektauftrag).  

> [!NOTE]  
>  Serien-/Chargennummern können auch auf Auftrag-zu-Auftrag-Bedarfen angegeben werden. In diesem Fall gilt der Vorrat nicht standardmäßig als inflexibel, wie dies normalerweise der Fall ist für Serien-/Chargennummern. In diesem Fall erhöht/mindert das System gemäß den Änderungen des Bedarfs. Darüber hinaus gilt: Wenn ein Bedarf variierende Serien-/Chargennummern enthält (etwa mehr als eine Chargennummer), wird ein Beschaffungsauftrag pro Charge vorgeschlagen.  

> [!NOTE]  
>  Planungen sollten nicht dazu führen, dass Beschaffungsaufträge erstellt werden, die durch eine Auftrag-zu-Auftrag-Verknüpfung gebunden sind. Wenn der Plan verwendet wird, sollte er nur als Generator des abhängigen Bedarfs in einer Produktionsumgebung verwendet werden.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Der Komponentenbedarf wird gemäß den Fertigungsauftragsänderungen geladen  
 Wenn es Fertigungsaufträge bearbeitet, muss das Planungssystem die benötigten Komponenten überwachen, bevor es sie in das Anforderungsprofil lädt. Komponentenzeilen, die aus einem ergänzten Fertigungsauftrag resultieren, ersetzen die des ursprünglichen Auftrags. Dadurch ist sichergestellt, dass das Planungssystem festlegt, dass Planungszeilen für Komponentenbedarf nicht dupliziert werden.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a>Sicherheitsbestand kann verbraucht werden  
 Der Sicherheitsbestand ist hauptsächlich ein Bedarfstyp und wird daher am Planungsstartdatum in das Bestandsprofil geladen.  

 Der Sicherheitsbestand ist eine Bestandsmenge, die beiseite gelegt wird, um Ungewissheiten beim Bedarf während der Beschaffungszeit zu kompensieren. Jedoch kann er verbraucht werden, wenn es erforderlich ist, ihn zur Deckung eines Bedarfs zu verwenden. In diesem Fall wird durch das Planungssystem sichergestellt, dass der Sicherheitsbestand schnell ersetzt wird, indem am Datum des Verbrauchs ein Ausnahmebeschaffungsauftrag zum Auffüllen des Sicherheitsbestands vorgeschlagen wird. In dieser Planungszeile wird das Symbol für eine Ausnahmewarnung angezeigt, durch das der Planer darauf aufmerksam gemacht wird, dass der Sicherheitsbestand teilweise oder vollständig aufgrund eines Ausnahmeauftrags für die Fehlteile verbraucht wurde.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Planungsbedarf wird durch Verkaufsaufträge reduziert  
 Der Produktionsplan drückt den erwarteten künftigen Bedarf aus. Während der Eingabe des tatsächlichen Bedarfs, üblicherweise als Verkaufsaufträge für Fertigungsartikel, verbraucht er die Planung.  

 Die Planung selbst wird durch Verkaufsaufträge nicht reduziert; sie bleibt unverändert. Jedoch werden die geplanten Mengen, die in der Planungsberechnung verwendet werden, reduziert (über die Verkaufsauftragsmengen), bevor die eventuelle Restmenge in das Bedarfsbestandsprofil eingeht. Wenn das Planungssystem tatsächliche Verkäufe für eine Periode prüft, schließt dies sowohl Verkaufsaufträge als auch Artikelposten von gelieferten Verkäufen ein, es sei denn, sie ergeben sich aus einem Rahmenauftrag.  

 Ein Benutzer muss eine gültige Planungsperiode definieren. Das Datum auf der Planungsmenge definiert den Anfang der Periode, und das Datum auf der nächsten Planung definiert das Ende der Periode.  

 Die Planung für Zeiträume vor der Planungsperiode wird nicht verwendet, unabhängig davon, ob sie verbraucht wurde oder nicht. Die erste interessante Planungszahl ist entweder das Datum auf oder möglichst nahe vor dem Planungsstartdatum.  

 Die Planung kann für unabhängigen Bedarf, wie etwa Verkaufsaufträge, oder abhängigen Bedarf, wie etwa FA-Komponenten (Modul Planung) gelten. Ein Artikel kann beide Planungsarten haben. Während der Planung findet der Verbrauch separat statt, zuerst für unabhängigen Bedarf und dann für abhängigen Bedarf.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Der Rahmenauftragsbedarf wird durch Verkaufsaufträge reduziert  
 Die Planung wird durch den Rahmenauftrag als Mittel zur Angabe des zukünftigen Bedarfs von einem bestimmten Kunden ergänzt. Wie mit dem (unspezifizierten) Plan sollte der tatsächliche Verkauf den voraussichtlichen Bedarf verbrauchen, und die restliche Menge sollte in das Bedarfsbestandsprofil eingehen. Wieder reduziert der Verbrauch nicht tatsächlich den Rahmenauftrag.  

 Die Planungsberechnung berücksichtigt offene Verkaufsaufträge, die mit dieser bestimmten Rahmenauftragszeile verbunden sind, nicht jedoch Gültigkeitszeiträume. Es berücksichtigt auch nicht gebuchte Aufträge, da das Buchungsverfahren bereits die ausstehende Rahmenauftragsmenge reduziert hat.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
 [Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)   
 [Designdetails: Planungsparameter](design-details-planning-parameters.md)

