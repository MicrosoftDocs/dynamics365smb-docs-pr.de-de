---
title: Verwalten von Änderungen des MwSt.-Satzes
description: erfahren Sie, wie Sie das Tool zur Änderung des MwSt.-Satzes für Dynamics 365 Business Central verwenden, um die MwSt.-Sätze auf der Grundlage der lokalen Gesetzgebung zu ändern.
author: andregu
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.workload: na
ms.search.keywords: VAT, VAT rate, posting, tax, value-added tax
ms.date: 06/16/2021
ms.author: andregu
ms.openlocfilehash: 9d90364691e393ddb376b0446d298ba96a92b383
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437391"
---
# <a name="managing-vat-rate-changes"></a>Verwalten von Änderungen des Mehrwertsteuersatzes

Mehrwertsteuersätze können sich je nach lokaler Gesetzgebung ändern. Jede Änderung der Mehrwertsteuer wirkt sich auf Ihre Daten in [!INCLUDE[prod_short](includes/prod_short.md)] aus, unabhängig davon, ob der Mehrwertsteuersatz gesenkt, angehoben oder entfernt wird. Die Mehrwertsteuer ist mit vielen Entitäten in [!INCLUDE[prod_short](includes/prod_short.md)] verbunden, z. B. Kunden, Lieferanten, Artikel, Ressourcen, Artikel Zu-/Abschläge und Sachkonten. Änderungen der Mehrwertsteuersätze erfolgen normalerweise zu einem bestimmten Zeitpunkt. Ab diesem Zeitpunkt müssen Sie die MwSt.-Einrichtung und Buchungsgruppen usw. geändert haben, um sicherzustellen, dass neue Verkaufsaufträge und Einkaufsbestellungen mit dem neuen Mehrwertsteuersatz erstellt werden.

## <a name="changing-vat-rates"></a>Ändern von Mehrwertsteuersätzen

Der optimale Ansatz für die Verwaltung einer Änderung des Mehrwertsteuersatzes besteht darin, offene Bestellungen und andere Dokumente vor dem Datum der Änderung des Mehrwertsteuersatzes vollständig zu buchen und zu schließen, um sicherzustellen, dass diese nicht von der Änderung betroffen sind. Dies ist die sauberste Vorgehensweise, die es Ihnen ermöglicht, neue Bestellungen und Dokumente mit dem neuen Mehrwertsteuersatz zu starten.

Die folgende Methode wird vorgeschlagen, um eine Änderung des Mehrwertsteuersatzes zu verwalten.

1. Buchen und schließen Sie offene Aufträge, Buch.-Blätter und andere Dokumente vor dem Umstellungsdatum vollständig. Sie können bis nach dem Umstellungsdatum warten, solange Sie keine neuen Zeilen hinzufügen und sicherstellen, dass das Gültigkeitsdatum vor dem Umstellungsdatum liegt.  
2. Erstellen Sie die neue MwSt-Einrichtung.  
3. Nehmen Sie die MwSt-Umstellung für Entitäten vor (relevante Debitoren, Kreditoren, Artikel usw.).  
4. Am Umstellungsdatum des Mehrwertsteuersatzes erstellen Sie neue Dokumente, die den neuen Satz verwenden.  


> [!NOTE]  
> Das Tool zum Ändern des MwSt.-Satzes wird derzeit aktualisiert. Die nachfolgend aufgeführten Funktionen stimmen möglicherweise nicht mit den Funktionen in Ihrer Umgebung überein. Das Update wird vor dem 1. Juli 2020 ausgeführt und ist kein regelmäßiges monatliches Update. Stattdessen werden alle Umgebungen automatisch aktualisiert (Hotfix). Wenn dieses Update abgeschlossen ist, wird diese Meldung nicht mehr angezeigt.  

## <a name="the-vat-rate-change-tool"></a>Das Tool zum Ändern des MwSt.-Satzes

Das Tool zum Ändern des MwSt.-Satzes kann die Umrechnung von Mehrwertsteuersätzen für Masterdaten, Buch.-Blätter und Bestellungen in gewissem Umfang unterstützen. Dies ist nützlich, wenn Sie die Mehrwertsteuer für Masterdaten einfacher umrechnen möchten oder Sie über Aufträge verfügen, die Sie nicht vor dem Umstellungsdatum schließen können und die über einen längeren Zeitraum bearbeitet werden und das Umstellungsdatum des Mehrwertsteuersatzes überschreiten. Das angewendete Tool zum Ändern des MwSt.-Satzes unterliegt bestimmten Einschränkungen und Einschränkungen.

## <a name="understanding-the-vat-rate-conversion-process-and-limitations"></a>Verstehen des Prozesses und der Einschränkungen des Tools zum Ändern des MwSt.-Satzes

Das Tool zum Ändern des MwSt.-Satzes führt Mehrwertsteuersatzkonvertierungen für Masterdaten, Buch.-Blätter und Aufträge auf verschiedene Arten aus. Die ausgewählten Masterdaten und die Buch.-Blätter werden von der neuen Produktbuchungsgruppe oder der MwSt.-Produktbuchungsgruppe aktualisiert. Wenn eine Bestellung vollständig oder teilweise geliefert wurde, behalten die gelieferten Artikel die aktuelle Produktbuchungsgruppe oder MwSt.-Produktbuchungsgruppe. Eine neue Auftragszeile wird für die nicht gelieferten Artikel erstellt und aktualisiert, um aktuelle und neue Produktbuchungsgruppen oder MwSt.-Produktbuchungsgruppen aufeinander auszurichten. Darüber hinaus werden Artikelzu-/-abschlagszuweisungen, Konfigurationsvorlagen für Artikel, Reservierungen und Artikelverfolgungsinformationen entsprechend aktualisiert. 

In Auftragspositionen wird der VK-Preis für alle Zeilen des Typs „Artikel“ und „Ressource“ aktualisiert, wenn Preise inkl. Mehrwertsteuer für den Artikel verwendet werden. Bei anderen Positionstypen kann entschieden werden, ob der VK-Preis aktualisiert werden soll oder nicht.

Es gibt mehrere Elemente, die das Werkzeug nicht konvertiert:

* Verkaufs- oder Einkaufsbestellungen und -rechnungen, in denen Lieferungen gebucht wurden. Diese Belege werden unter Verwendung des aktuellen Mehrwertsteuersatzes gebucht.  
* Belege mit gebuchten Vorauszahlungsrechnungen. Beispielsweise haben Sie Vorauszahlungen auf Rechnungen geleistet oder erhalten, die nicht vollständig erledigt sind, bevor Sie das Mehrwertsteuersatz-Änderungstool verwenden. In diesem Fall gibt es eine Differenz zwischen der MwSt., die fällig ist, und der MwSt., die in den Vorauszahlungen bezahlt wurde, wenn die Rechnung abgeschlossen wird. Das Mehrwertsteuersatz-Änderungstool überspringt diese Belege, und Sie müssen sie manuell aktualisieren.  
* Verkaufs- oder Einkaufsbestellungen mit Lagerintegration, wenn sie teilweise geliefert oder erhalten werden.  
* Direktlieferungen
* Spezialaufträge 
* Montageaufträge
* Serviceverträge.  
* Gutschriften
* Reklamationen
* Preise für Artikel (Masterdaten)
* Preise für Verkaufspreise (Masterdaten)
* Geschäftsbuchungsgruppen für Debitoren und Kreditoren

### <a name="to-prepare-vat-rate-change-conversions"></a>So bereiten Sie Mehrwertsteuersatzänderungen vor

Bevor Sie das Mehrwertsteuersatz-Änderungstool einrichten, müssen Sie die folgenden Vorbereitungen durchführen.

* Wenn Sie Transaktionen haben, die verschiedene Sätze verwenden, müssen sie in verschiedene Gruppen aufgeteilt werden, entweder durch Erstellen neuer Sachkonten für die einzelnen Sätze oder mithilfe von Datenfiltern, um Transaktionen entsprechend dem Satz zu gruppieren.  
* Wenn Sie neue Sachkonten erstellen, müssen Sie auch neue allgemeine Buchungsgruppen erstellen.  
* Um die Anzahl der Belege zu verringern, die konvertiert werden, buchen Sie möglichst viele Belege, und reduzieren Sie nicht gebuchte Belege auf ein Minimum.  
* Sichern von Daten.

### <a name="to-set-up-the-vat-rate-change-tool"></a>So richten Sie das Mehrwertsteuersatz-Änderungstool ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einrichtung der MwSt.-Satzänderung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf den Inforegistern **Masterdaten**, **Buch.-Blätter** und **Belege** einen Buchungsgruppenwert aus der Liste der Optionen für erforderliche Felder aus. Für jede Gruppe können Sie wählen, ob Sie MwSt.-Produktbuchungsgruppen oder allgemeine Produktbuchungsgruppen konvertieren oder beide Werte konvertieren möchten, sofern sie im Masterdatenelement verfügbar sind. Für einige Bereiche können Sie auch einen Filter festlegen, um nur eine Teilmenge von Werten zu konvertieren, z. B. Sachkonten. 
3. Wählen Sie auf dem Inforegister **Preise inkl. MwSt** aus, für welche Zeilenarten in Bestellungen Sie VK-Preise aktualisieren möchten. VK-Preise in Zeilen vom Typ „Artikel“ und „Ressource“ werden immer aktualisiert.

### <a name="to-set-up-product-posting-group-conversion"></a>So richten Sie die Produktbuchungsgruppenkonvertierung ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einrichtung der MwSt.-Satzänderung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Einrichtung der MwSt.-Satzänderung** entweder die Option **Umrech. für MwSt.-Produktbuchungsgruppe** oder **Umrech. für Produktbuchungsgruppe** Aktion.  
3. Geben Sie im Feld **Code ab** die aktuelle Buchungsgruppe ein.  
4. Geben Sie den neuen Standort in dem Feld **Cod zu** ein.  

### <a name="to-perform-vat-rate-change-conversion"></a>So führen Sie eine Umrechnung für die MwSt.-Satzänderung aus

Sie verwenden das MwSt.-Satz-Änderungstool, um Änderungen im Standard-MwSt.-Satz zu verwalten. Sie führen MwSt.- und Buchungsgruppenkonvertierungen durch, um Mehrwertsteuersätze zu ändern und genaue MwSt.-Abrechnungen zu erstellen. Abhängig von Ihrem Setup werden folgende Änderungen vorgenommen:  

* MwSt.-Buchungsgruppen und Buchungsgruppen werden konvertiert.  
* Änderungen werden in den Sachkonten, den Debitoren, den Kreditoren, den offenen Belegen, den Buch.-Blattzeilen usw. implementiert.  

> [!IMPORTANT]  
> Bevor Sie die Umrechnung für MwSt.-Satzänderungen ausführen, können Sie die Konvertierung testen. Um dies zu tun, führen Sie die Schritte unten aus, stellen Sie aber sicher, dass Sie die Kontrollkästchen **Konvertierung durchführen** und **Tool zum Ändern des MwSt.-Satzes abgeschlossen** deaktivieren. Während der Testkonvertierung wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MwSt.-Satzänderung** gelöscht und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MwSt.-Satzänderung** ist leer. Nach der Umrechnung wählen Sie auf der Registerkarte Start, in der Gruppe Prozess die Option **Änderungsprotokollposten für MwSt.-Satz** aus, um die Ergebnisse der Umrechnung anzuzeigen. Prüfen Sie jeden Posten, bevor Sie die Umrechnung ausführen. Insbesondere überprüfen Sie Transaktionen, die einen alten Mehrwertsteuersatz verwenden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **MwSt.-Satz-Änderung** ein und wählen Sie dann den Link **Einrichtung der MwSt.-Satzänderung**.  
2. Vergewissern Sie sich, dass Sie bereits die MwSt.-Produktbuchungsgruppen-Umrechnung oder die Produktbuchungsgruppen-Umrechnung eingerichtet haben.  
3. Wählen Sie das Kontrollkästchen **Konvertierung durchführen**.  

    > [!IMPORTANT]  
    >  Deaktivieren Sie das Kontrollkästchen **Tool zum Ändern des MwSt.-Satzes abgeschlossen**. Das Kontrollkästchen wird automatisch aktiviert, wenn die Umrechnung für die MwSt.-Satzänderung abgeschlossen ist.  

4. Wählen Sie die Aktion **Konvertieren** aus.  
5. Nachdem die Konvertierung abgeschlossen ist, wählen Sie die Aktion **Änderungsprotokollposten für MwSt.-Satz**, um die Ergebnisse der Konvertierung anzuzeigen.  

> [!IMPORTANT]  
> Nachdem die Umrechnung abgeschlossen ist, wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MwSt.-Satzänderung** ausgewählt und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MwSt.-Satzänderung** wird mit dem Umrechnungsdatum ausgefüllt.  

## <a name="see-also"></a>Siehe auch

[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)  
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]