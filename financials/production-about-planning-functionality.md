---
title: Info zu Planungsfunktionen  | Microsoft Docs
description: "Das Planungssystem berücksichtigt sämtliche Bedarfs- und Vorratsdaten, saldiert die Ergebnisse und erstellt Vorschläge zum Ausgleichen des Vorrats, damit der Bedarf erfüllt werden kann."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0910760881decc98ba1bfa6e8753566316386b2c
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="about-planning-functionality"></a>Info zu Planungsfunktionen
Das Planungssystem berücksichtigt sämtliche Bedarfs- und Vorratsdaten, saldiert die Ergebnisse und erstellt Vorschläge zum Ausgleichen des Vorrats, damit der Bedarf erfüllt werden kann.  

Weitere Informationen finden Sie unter [Designdetails: Beschaffungsplanung](design-details-supply-planning.md)  

> [!NOTE]  
> Für alle Felder, die in diesem Thema genannt werden, Lesen Sie die QuickInfo, um die Funktion zu erkennen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Bedarf und Vorrat  
Planung besteht aus zwei Elementen: Bedarf und Vorrat. Dieses beiden Elemente müssen einander angepasst werden, damit sichergestellt ist, dass der Bedarf rechtzeitig und kostengünstig erfüllt werden kann.  

- Bedarf ist der Oberbegriff für jede Art von Bruttobedarf: beispielsweise Verkaufsauftrag, Serviceauftrag, Komponentenbedarf aus einem Montage- oder Fertigungsauftrag, ausgehende Umlagerung, Rahmenbestellung oder Absatzplanung. Darüber hinaus werden einige technische Arten von Bedarf unterstützt - z. B. negative Fertigungsaufträge oder Einkaufsbestellungen, negative Lagerbestände und Einkaufsreklamationen.  
- Vorrat ist der Oberbegriff für jede Art von Beschaffung: beispielsweise Einkaufsbestellung, Montageauftrag, Fertigungsauftrag oder eingehende Umlagerung. Entsprechend kann es negative Verkaufs- oder Serviceaufträge, negativen Komponentenbedarf oder negative Verkaufsreklamationen geben – alle diese Elemente entsprechen in gewisser Weise ebenfalls einem Vorrat.  

Außerdem hat das Planungssystem die Aufgabe sicherzustellen, dass der Lagerbestand nicht unnötig wächst. Im Fall eines abnehmenden Bedarfs wird das Planungssystem vorschlagen, dass vorhandene Ersatzaufträge zurückgestellt, mengenmäßig verringert oder storniert werden sollten.  

## <a name="planning-calculation"></a>Planungsberechnung  
Das Planungssystem wird durch den erwarteten und den tatsächlichen Debitorenbedarf sowie die Wiederbeschaffungsparameter gesteuert. Ein Ausführen der Planungsberechnung bewirkt, dass bestimmte vorzunehmende Aktionen (Ereignismeldungen) vorgeschlagen werden, die sich auf mögliche Beschaffungen von Kreditoren, Umlagerungen zwischen Lagern oder die Fertigung beziehen. Wenn es bereits Ersatzaufträge gibt, könnten die vorgeschlagenen Aktionen so aussehen, dass die Aufträge vergrößert oder schneller erteilt werden sollen, damit den Bedarfsänderungen Rechnung getragen wird.  

Die Basis der Planungsroutine findet sich in der Brutto-Netto-Berechnung. Die Nettobedarfe steuern die voraussichtlichen Freigabemengen, die anhand der Arbeitspläne (Produktionsartikel) oder der Vorlaufzeiten der Artikelkarten (Einkaufsartikel) geplant werden. Voraussichtliche Freigabemengen basieren auf der Planungsberechnung und werden durch die Parameter beeinflusst, die auf den einzelnen Artikelkarten festgelegt sind.  

## <a name="planning-with-manual-transfer-orders"></a>Planung mit manuellen Umlagerungsaufträgen
Wie aus dem Feld **Beschaffungsmethode** auf einer Lagerhaltungsdatenkarte zu ersehen ist, kann das Planungssystem für die Erstellung von Umlagerungsaufträgen zum standortübergreifenden Ausgleichen von Angebot und Nachfrage eingerichtet werden.  

Über solche automatischen Umlagerungsaufträge hinaus werden möglicherweise manchmal allgemeine Umlagerungen von Lagermengen an einen anderen Lagerort erforderlich, unabhängig von der vorhandenen Nachfrage. Zu diesem Zweck würde normalerweise manuell ein Umlagerungsauftrag für die umzulagernde Menge erstellt. Um sicherzustellen, dass das Planungssystem diese manuellen Umlagerungsauftrag nicht verändert, müssen Sie das Feld **Planungsflexibilität** in der /den Umlagerungszeile(n) auf Keine festlegen.  

Wenn hingegen das Planungssystem die Mengen und Daten für Umlagerungsaufträge an die vorhandene Nachfrage anpassen soll, müssen Sie das Feld **Planungsflexibilität**auf den Standardwert Unbeschränkt festlegen.

## <a name="planning-parameters"></a>Planungsparameter  
Die Planungsparameter steuern die Beschaffung (wann, wie viel und wie) anhand der verschiedenen Einstellungen auf den Artikelkarten (oder Lagerhaltungsdaten) sowie der Produktionseinrichtung.  

Die folgenden Planungsparameter sind auf der Artikel- oder Lagerhaltungsdatenkarte vorhanden:  

-   Toleranzperiode  
-   Toleranzmenge  
-   Wiederbeschaffungsverfahren  
-   Minimalbestand
-   Maximalbestand  
-   Überlauflevel  
-   Zeitrahmen  
-   Loskumulierungsperiode  
-   Neuplanungsperiode  
-   Bestellmenge  
-   Sicherh.-Zuschl. Beschaff.-Zt.  
-   Sicherheitsbestand  
-   Montagerichtlinie  
-   Produktionsart  

Die folgenden Auftragsmodifikationen sind auf der Artikel- oder Lagerhaltungsdatenkarte vorhanden:  

-   Minimale Losgröße  
-   Maximale Losgröße  
-   Losgrößenrundungsfaktor  

Zu den globalen Planungseinrichtungsfeldern im Fenster **Produktion Einrichtung** gehören:  

-   Dyn. Stückl.-Ebene berechnen  
-   Aktuelle Absatzplanung  
-   Absatzpl. pro Lagerort verw.  
-   Vorg. Sich.-Zuschl. Besch.-Zt.  
-   Leerer Überlauflevel  
-   Prod.-Prog.Pl./Nettobed. komb.   
-   Komponenten von Lagerort  
-   Standardtoleranzperiode  
-   Toleranzmenge  

Weitere Informationen finden Sie unter [Designdetails: Planungsparameter](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Andere wichtige Planungs-Felder
### <a name="planning-flexibility"></a>Planungsflexibilität
In den meisten Beschaffungsaufträgen wie Fertigungsaufträge, können Sie **Unbeschränkt** oder **Keine** im Feld **Planungsflexibilität** auf den Zeilen auswählen.

Gibt an, ob die durch die Fertigungsauftragszeile dargestellte Lieferung bei der Berechnung von Ereignismeldungen vom Planungssystem berücksichtigt wird.
Enthält das Feld die Option **Unbeschränkt**, wird die Zeile beim Berechnen von Ereignismeldungen berücksichtigt. Wenn das Feld die Option **Keine** enthält, ist die Zeile unveränderlich und wird bei der Berechnung von Aktionsmeldungen nicht berücksichtigt.

### <a name="warning"></a>Warnung
Das Feld **Warnung** im **Planungsvorschlag** Fenster informiert Sie über jede mögliche Planungszeile, die für eine ungewöhnliche Situation mit einen Text erstellt wird, den der Benutzer klicken kann, um weitere Informationen anzuzeigen. Folgende Arten von Warnungen sind verfügbar:

- Notfall
- Ausnahme
- Achtung
- Notfall

Die Warnung für einen Notfall wird in zwei Situationen angezeigt:

- Der Lagerbestand ist am geplanten Startdatum negativ.
- Es sind rückdatierte Beschaffungs- oder Bedarfsereignisse vorhanden.

Wenn der Lagerbestand eines Artikels am geplanten Startdatum negativ ist, wird vom Planungssystem ein Notfallbeschaffungsauftrag für den negativen Bestand vorgeschlagen, der am geplanten Startdatum eingeht. Im Warnungstext werden das Startdatum und die Menge der Notfallbestellung angegeben.

Belegzeilen mit Fälligkeitsdaten vor dem geplanten Startdatum werden in einem Notfallbeschaffungsauftrag für den Artikel zusammengefasst, der am geplanten Startdatum eingehen soll.

### <a name="exception"></a>Ausnahme
Die Ausnahmewarnung wird angezeigt, wenn der voraussichtlich verfügbare Lagerbestand den Sicherheitsbestand unterschreitet.

Vom Planungssystem wird ein Beschaffungsauftrag vorgeschlagen, um den Bedarf am Fälligkeitsdatum zu decken. In der Warnung werden der Sicherheitsbestand des Artikels und das Datum angegeben, an dem er unterschritten wurde.

Das Unterschreiten des Sicherheitsbestands gilt als Ausnahme, da dieser Zustand nicht eintreten sollte, wenn der Minimalbestand korrekt festgelegt wurde.

> [!NOTE]
> Der Vorrat in Planungszeilen mit Ausnahmewarnungen wird normalerweise nicht gemäß den Planungsparametern geändert. Stattdessen wird vom Planungssystem nur eine Beschaffung vorgeschlagen, um die genaue Bedarfsmenge zu decken. Sie können jedoch die Planung so festlegen, dass bestimmte Planungsparameter für Planungszeilen mit bestimmten Warnungen berücksichtigt werden können. Weitere Informationen finden Sie unter "Respekt-Planungsparameter für Ausnahme-Warnungen" in Plan kalkulieren. Wksh.

### <a name="attention"></a>Achtung
Die Achtungswarnung wird in zwei Situationen angezeigt:

- Das geplante Startdatum liegt vor dem Arbeitsdatum.
- Die Planungszeile schlägt vor, eine freigegebene Bestellung oder einen freigegebenen Fertigungsauftrag zu ändern.

> [!NOTE]
> In Planzeilen mit Warnungen ist das Kontrollkästchen **Ereignismeldung akzeptieren** nicht aktiviert, da diese Zeilen vom Planer genauer untersucht werden sollen, bevor der Plan umgesetzt wird.

## <a name="see-also"></a>Siehe auch  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)  
[Planung](production-planning.md)   
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

