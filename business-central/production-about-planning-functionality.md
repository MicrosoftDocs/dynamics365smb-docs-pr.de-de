---
title: Info zu Planungsfunktionen
description: Die Planung berücksichtigt sämtliche Bedarfs- und Vorratsdaten, saldiert die Ergebnisse und erstellt Vorschläge zum Ausgleichen des Vorrats, damit der Bedarf erfüllt werden kann.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5430
ms.date: 08/30/2022
ms.author: bholtorf
ms.openlocfilehash: df67568094e76dccbc62b9dbf6d78dc9c0e58caf
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606964"
---
# <a name="about-planning-functionality"></a>Info zu Planungsfunktionen

Das Planungssystem berücksichtigt sämtliche Bedarfs- und Vorratsdaten, saldiert die Ergebnisse und erstellt Vorschläge zum Ausgleichen des Vorrats, damit der Bedarf erfüllt werden kann.  

Weitere Informationen finden Sie unter [Designdetails: Beschaffungsplanung](design-details-supply-planning.md)  

> [!NOTE]  
> Für alle Felder, die in diesem Thema genannt werden, Lesen Sie die QuickInfo, um die Funktion zu erkennen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Bedarf und Vorrat

Planung besteht aus zwei Elementen: Bedarf und Vorrat. Dieses beiden Elemente müssen einander angepasst werden, damit sichergestellt ist, dass der Bedarf rechtzeitig und kostengünstig erfüllt werden kann.  

- Bedarf ist der Oberbegriff für jede Art von Bruttobedarf: beispielsweise Verkaufsauftrag, Serviceauftrag, Komponentenbedarf aus einem Montage- oder Fertigungsauftrag, ausgehende Umlagerung, Rahmenbestellung oder Absatzplanung. Darüber hinaus erlaubt die Anwendung einige technische Arten von Bedarf, - z. B. negative Fertigungsaufträge oder Einkaufsbestellungen, negative Lagerbestände und Einkaufsreklamationen.  
- Vorrat bezieht sich auf jede Art von Beschaffung: beispielsweise Einkaufsbestellung, Montageauftrag, Fertigungsauftrag oder eingehende Umlagerung. Entsprechend kann es negative Verkaufs- oder Serviceaufträge, negativen Komponentenbedarf oder negative Verkaufsreklamationen geben – alle diese Elemente entsprechen ebenfalls einem Vorrat.  

Außerdem hat das Planungssystem die Aufgabe sicherzustellen, dass der Lagerbestand nicht unnötig wächst. Im Fall eines abnehmenden Bedarfs wird das Planungssystem vorschlagen, dass vorhandene Ersatzaufträge zurückgestellt, mengenmäßig verringert oder storniert werden sollten.  

## <a name="planning-calculation"></a>Planungsberechnung

Das Planungssystem wird durch den erwarteten und den tatsächlichen Debitorenbedarf sowie die Wiederbeschaffungsparameter gesteuert. Ein Ausführen der Planungsberechnung bewirkt, dass die Anwendung bestimmte Aktionen ([Ereignismeldungen](production-how-to-run-mps-and-mrp.md#action-messages)) vorschlägt, die sich auf mögliche Beschaffungen von Kreditoren, Umlagerungen zwischen Lagern oder die Fertigung beziehen. Wenn es bereits Ersatzaufträge gibt, könnten die vorgeschlagenen Aktionen so aussehen, dass die Aufträge vergrößert oder schneller erteilt werden sollen, damit den Bedarfsänderungen Rechnung getragen wird.  

Die Basis der Planungsroutine findet sich in der Brutto-Netto-Berechnung. Die Nettobedarfe steuern die voraussichtlichen Freigabemengen, die anhand der Arbeitspläne (Produktionsartikel) oder der Vorlaufzeiten der Artikelkarten (Einkaufsartikel) geplant werden. Voraussichtliche Freigabemengen basieren auf der Planungsberechnung und werden durch die Parameter beeinflusst, die auf den einzelnen Artikelkarten festgelegt sind.  

> [!TIP]
> Das Planungssystem hängt davon ab, wie Ihre Organisation Standorte verwendet. Weitere Informationen finden Sie unter [Planung mit/ohne Lagerortcodes](production-planning-with-without-locations.md).

## <a name="planning-with-manual-transfer-orders"></a>Planung mit manuellen Umlagerungsaufträgen

Wie aus dem Feld **Beschaffungsmethode** auf einer Lagerhaltungsdatenkarte zu ersehen ist, kann das Planungssystem für die Erstellung von Umlagerungsaufträgen zum standortübergreifenden Ausgleichen von Angebot und Nachfrage eingerichtet werden.  

Über solche automatischen Umlagerungsaufträge hinaus werden möglicherweise manchmal allgemeine Umlagerungen von Lagermengen an einen anderen Lagerort erforderlich, unabhängig von der vorhandenen Nachfrage. Zu diesem Zweck würde normalerweise manuell ein Umlagerungsauftrag für die umzulagernde Menge erstellt. Um sicherzustellen, dass das Planungssystem diese manuellen Umlagerungsauftrag nicht verändert, müssen Sie das Feld **Planungsflexibilität** in der /den Umlagerungszeile(n) auf Keine festlegen.  

Wenn hingegen das Planungssystem die Mengen und Daten für Umlagerungsaufträge an die vorhandene Nachfrage anpassen soll, müssen Sie das Feld **Planungsflexibilität** auf den Standardwert Unbeschränkt festlegen.

## <a name="planning-parameters"></a>Planungsparameter

Die Planungsparameter steuern die Beschaffung (wann, wie viel und wie) anhand der verschiedenen Einstellungen auf den Artikelkarten (oder Lagerhaltungsdaten) sowie der Produktionseinrichtung.  

Die folgenden Planungsparameter sind auf der Artikel- oder Lagerhaltungsdatenkarte vorhanden:  

- Toleranzperiode  
- Toleranzmenge  
- Wiederbeschaffungsverfahren  
- Minimalbestand
- Maximalbestand  
- Überlauflevel  
- Zeitrahmen  
- Loskumulierungsperiode  
- Neuplanungsperiode  
- Bestellmenge  
- Sicherh.-Zuschl. Beschaff.-Zt.  
- Sicherheitsbestand  
- Montagerichtlinie  
- Produktionsart  

Die folgenden Auftragsmodifikationen sind auf der Artikel- oder Lagerhaltungsdatenkarte vorhanden:  

- Minimale Losgröße  
- Maximale Losgröße  
- Losgrößenrundungsfaktor  

Zu den globalen Planungseinrichtungsfeldern auf der Seite **Produktion Einrichtung** gehören:  

- Dyn. Stückl.-Ebene berechnen  
- Aktuelle Bedarfsplanung  
- Absatzpl. pro Lagerort verw.  
- Vorg. Sich.-Zuschl. Besch.-Zt.  
- Leerer Überlauflevel  
- Prod.-Prog.Pl./Nettobed. komb.
- Komponenten von Lagerort  
- Standardtoleranzperiode  
- Toleranzmenge  

Weitere Informationen finden Sie unter [Designdetails: Planungsparameter](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Andere wichtige Planungs-Felder

### <a name="planning-flexibility"></a>Planungsflexibilität

In den meisten Beschaffungsaufträgen wie Fertigungsaufträge, können Sie **Unbeschränkt** oder **Keine** im Feld **Planungsflexibilität** auf den Zeilen auswählen.

Gibt an, ob die durch die Fertigungsauftragszeile dargestellte Lieferung bei der Berechnung von Ereignismeldungen vom Planungssystem berücksichtigt wird.
Enthält das Feld die Option **Unbeschränkt**, wird die Zeile beim Berechnen von Ereignismeldungen berücksichtigt. Wenn das Feld die Option **Keine** enthält, ist die Zeile unveränderlich und wird bei der Berechnung von Aktionsmeldungen nicht berücksichtigt.

### <a name="warning"></a>Warnung

Das Feld **Warnung** auf der **Planungsarbeitsblatt** Seite informiert Sie über jede mögliche Planungszeile, die für eine ungewöhnliche Situation mit einen Text erstellt wird, den der Benutzer klicken kann, um weitere Informationen anzuzeigen. Folgende Arten von Warnungen sind verfügbar:

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
> Der Vorrat in Planungszeilen mit Ausnahmewarnungen wird normalerweise nicht gemäß den Planungsparametern geändert. Stattdessen wird vom Planungssystem nur eine Beschaffung vorgeschlagen, um die genaue Bedarfsmenge zu decken. Sie können jedoch die Planung so festlegen, dass bestimmte Planungsparameter für Planungszeilen mit bestimmten Warnungen berücksichtigt werden können. Weitere Informationen finden Sie in der Beschreibung für das Feld **Beachten Sie die Planungsparameter für Ausnahmewarnungen** im Artikel [Führen Sie vollständige Planung, MPS oder MRP aus](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Achtung

Die Achtungswarnung wird in zwei Situationen angezeigt:

- Das geplante Startdatum liegt vor dem Arbeitsdatum.
- Die Planungszeile schlägt vor, eine freigegebene Bestellung oder einen freigegebenen Fertigungsauftrag zu ändern.

> [!NOTE]
> In Planzeilen mit Warnungen ist das Kontrollkästchen **Ereignismeldung akzeptieren** nicht aktiviert, da diese Zeilen vom Planer genauer untersucht werden sollen, bevor der Plan umgesetzt wird.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Planungs‑ und Anforderungsarbeitsblätter

Wie in [Planung](production-planning.md) beschrieben können Sie für die meisten Planungsaktivitäten zwischen zwei Arbeitsblättern wählen, dem Planungsarbeitsblatt und dem Anforderungsarbeitsblatt. Die meisten Prozesse werden anhand des Planungsarbeitsblatts beschrieben. Es gibt jedoch einige Szenarien, in denen das Anforderungsarbeitsblatt bevorzugt wird.

### <a name="requisition-worksheet"></a>Anforderungsarbeitsblatt

Auf der Seite **Anforderungsarbeitsblatt** sind die Artikel aufgelistet, die Sie bestellen möchten. Sie haben folgende Möglichkeiten, um die Artikel in das Arbeitsblatt einzugeben:

- Geben Sie die Artikel manuell in den Vorschlag ein, und füllen Sie die entsprechenden Felder aus.

- Verwenden Sie die Stapelverarbeitung **Plan berechnen**. Diese berechnet eine Planung für Artikel und Lagerhaltungsdaten, die mit dem Dispositonsmethodencode **Einkauf** oder **Umlagerung** eingerichtet wurden. Wenn Sie diese Stapelverarbeitung verwenden, füllt die Anwendung automatisch das Feld **Ereignismeldung** mit einem Vorschlag, wie Sie die Artikel wiederbeschaffen können. Dabei kann es sich z. B. um die Erhöhung der Artikelmenge in einer bestehenden Bestellung oder um die Erstellung einer neuen Bestellung handeln.

- Wenn Sie die Stapelverarbeitung **Plan berechnen** auf der Seite **Planungsarbeitsblatt** zur Berechnung eines Nachschubplans verwendet haben, können Sie die Stapelverarbeitung **Ereignismeldung durchführen** verwenden, um Bestell- und Umlagerungsvorschläge aus dem Planungsarbeitsblatt in das Anforderungsarbeitsblatt zu kopieren. Dies ist dann nützlich, wenn unterschiedliche Anwender für die Abwicklung der Fertigungsaufträge und Einkaufsbestellungen/Umlagerungsaufträge zuständig sind.

- Sie können die Aktion **Direktlieferung** verwenden, um die Anforderungsarbeitsblattszeilen zu füllen. Diese Aktion verwendet die Stapelverarbeitung **Aufträge holen**, um die Verkaufsauftragszeilen zu ermitteln, die für eine Direktlieferung vorgesehen sind.

- Sie können die Aktion **Spezialauftrag** verwenden, um die Anforderungsarbeitsblattszeilen zu füllen. Diese Aktion verwendet die Stapelverarbeitung **Aufträge holen**, um die Verkaufsauftragszeilen zu ermitteln, die für einen Spezialauftrag vorgesehen sind.

Bestellvorschlagszeilen enthalten detaillierte Informationen über die Artikel, die wiederbestellt werden müssen. Sie können die Zeilen bearbeiten und löschen, um Ihren Bestellarbeitsblatt anzupassen, und Sie können die Zeilen auch mit der Stapelverarbeitung **Ereignismeldung durchführen** weiterverarbeiten. 

Einzelheiten zur Planung mit Standorten und Transfers finden Sie unter [Planen mit oder ohne Standorte](production-planning-with-without-locations.md).

> [!TIP]
> Auf den Seiten **Anforderungsarbeitsblatt** oder **Planungsarbeitsblatt** können Sie die Zeilen organisieren, indem Sie nach einem Spaltennamen sortieren. Dies ist auf der Seite Planungsarbeitsblatt besonders nützlich, da sie für mehrstufige Produktionsaufträge verwendet werden kann. Standardmäßig werden Zeilen nach **Art.-Nr.** sortiert. Um Positionen für einen mehrstufigen Auftrag zu gruppieren, sortieren Sie nach **Ref. Best.-Nr.** Feld Auch **MPS-Bestellung** und **Planungsebene** können dabei helfen, die Hierarchie der Zeilen anzuzeigen.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/plan-items-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Entwurfsdetails: Vorratsplanung](design-details-supply-planning.md)  
[Planung](production-planning.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
