---
title: Verwenden des Mehrwertsteuersatz-Änderungstools | Microsoft-Dokumentation
description: Das MwSt.-Satz-Änderungstool verwenden
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 76c6f8902e9661f4f4dbbbf70487a53bf286edb2
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183164"
---
# <a name="use-the-vat-rate-change-tool"></a>Das MwSt.-Satz-Änderungstool verwenden

## <a name="understanding-the-vat-rate-conversion-process"></a>Verstehen des Prozesses der Umrechnung für die MwSt.-Satzänderung  
Die das Mehrwertsteueränderungstool führt Mehrwertsteuersatzkonvertierungen für Masterdaten, Buch.-Blätter und Aufträge auf verschiedene Arten aus. Die ausgewählten Masterdaten und die Buch.-Blätter werden von der neuen Produktbuchungsgruppe oder der MwSt.-Produktbuchungsgruppe aktualisiert. Wenn eine Bestellung vollständig oder teilweise geliefert wurde, behalten die gelieferten Artikel die aktuelle Produktbuchungsgruppe oder MwSt.-Produktbuchungsgruppe. Eine neue Auftragszeile wird für die nicht gelieferten Artikel erstellt und aktualisiert, um aktuelle und neue Produktbuchungsgruppen oder MwSt.-Produktbuchungsgruppen aufeinander auszurichten. Darüber hinaus werden Artikelzu-/-abschlagszuweisungen, Reservierungen und Artikelverfolgungsinformationen entsprechend aktualisiert.  

Es gibt mehrere Elemente, die das Werkzeug nicht konvertiert:

* Verkaufs- oder Einkaufsbestellungen und -rechnungen, in denen Lieferungen gebucht wurden. Diese Belege werden unter Verwendung des aktuellen Mehrwertsteuersatzes gebucht.  
* Belege mit gebuchten Vorauszahlungsrechnungen. Beispielsweise haben Sie Vorauszahlungen auf Rechnungen geleistet oder erhalten, die nicht vollständig erledigt sind, bevor Sie das Mehrwertsteuersatz-Änderungstool verwenden. In diesem Fall gibt es eine Differenz zwischen der MwSt., die fällig ist, und der MwSt., die in den Vorauszahlungen bezahlt wurde, wenn die Rechnung abgeschlossen wird. Das Mehrwertsteuersatz-Änderungstool überspringt diese Belege, und Sie müssen sie manuell aktualisieren.  
* Direktlieferungen oder Spezialaufträge.  
* Verkaufs- oder Einkaufsbestellungen mit Lagerintegration, wenn sie teilweise geliefert oder erhalten werden.  
* Serviceverträge.  

### <a name="to-prepare-vat-rate-change-conversions"></a>So bereiten Sie Mehrwertsteuersatzänderungen vor  
Bevor Sie das Mehrwertsteuersatz-Änderungstool einrichten, müssen Sie die folgenden Vorbereitungen durchführen.

* Wenn Sie Transaktionen haben, die verschiedene Sätze verwenden, müssen sie in verschiedene Gruppen aufgeteilt werden, entweder durch Erstellen neuer Sachkonten für die einzelnen Sätze oder mithilfe von Datenfiltern, um Transaktionen entsprechend dem Satz zu gruppieren.  
* Wenn Sie neue Sachkonten erstellen, müssen Sie auch neue allgemeine Buchungsgruppen erstellen.  
* Um die Anzahl der Belege zu verringern, die konvertiert werden, buchen Sie möglichst viele Belege, und reduzieren Sie nicht gebuchte Belege auf ein Minimum.  
* Sichern von Daten.

### <a name="to-set-up-the-vat-rate-change-tool"></a>So richten Sie das Mehrwertsteuersatz-Änderungstool ein  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Einrichtung der MwSt.-Satzänderung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf den Inforegistern **Masterdaten**, **Buch.-Blätter** und **Belege** einen Buchungsgruppenwert aus der Liste der Optionen für erforderliche Felder aus. Für jede Gruppe können Sie wählen, ob Sie MwSt.-Produktbuchungsgruppen oder allgemeine Produktbuchungsgruppen konvertieren oder beide Werte konvertieren möchten, sofern sie im Masterdatenelement verfügbar sind. Für einige Bereiche können Sie auch einen Filter festlegen, um nur eine Teilmenge von Werten zu konvertieren, z. B. Sachkonten. 

### <a name="to-set-up-product-posting-group-conversion"></a>So richten Sie die Produktbuchungsgruppenkonvertierung ein  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Einrichtung der MwSt.-Satzänderung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Einrichtung der MwSt.-Satzänderung** entweder die Option **Umrech. für MwSt.-Produktbuchungsgruppe** oder **Umrech. für Produktbuchungsgruppe** Aktion.  
3. Geben Sie im Feld **Code ab** die aktuelle Buchungsgruppe ein.  
4. Geben Sie den neuen Standort in dem Feld **Cod zu** ein.  

### <a name="to-perform-vat-rate-change-conversion"></a>So führen Sie eine Umrechnung für die MwSt.-Satzänderung aus  
Sie verwenden das MwSt.-Satz-Änderungstool, um Änderungen im Standard-MwSt.-Satz zu verwalten. Sie führen MwSt.- und Buchungsgruppenkonvertierungen durch, um Mehrwertsteuersätze zu ändern und genaue MwSt.-Abrechnungen zu erstellen. Abhängig von Ihrem Setup werden folgende Änderungen vorgenommen:  

* MwSt.-Buchungsgruppen und Buchungsgruppen werden konvertiert.  
* Änderungen werden in den Sachkonten, den Debitoren, den Kreditoren, den offenen Belegen, den Buch.-Blattzeilen usw. implementiert.  

> [!IMPORTANT]  
>  Bevor Sie die Umrechnung für MwSt.-Satzänderungen ausführen, können Sie die Konvertierung testen. Um dies zu tun, führen Sie die Schritte unten aus, stellen Sie aber sicher, dass Sie die Kontrollkästchen **Konvertierung durchführen** und **Tool zum Ändern des MwSt.-Satzes abgeschlossen** deaktivieren. Während der Testkonvertierung wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MwSt.-Satzänderung** gelöscht und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MwSt.-Satzänderung** ist leer. Nach der Umrechnung wählen Sie auf der Registerkarte Start, in der Gruppe Prozess die Option **Änderungsprotokollposten für MwSt.-Satz** aus, um die Ergebnisse der Umrechnung anzuzeigen. Prüfen Sie jeden Posten, bevor Sie die Umrechnung ausführen. Insbesondere überprüfen Sie Transaktionen, die einen alten Mehrwertsteuersatz verwenden.     

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Änderung des MwSt.-Satzes** ein und wählen Sie dann den Link **Einrichtung der MwSt.-Satzänderung**.  
2. Vergewissern Sie sich, dass Sie bereits die MwSt.-Produktbuchungsgruppen-Umrechnung oder die Produktbuchungsgruppen-Umrechnung eingerichtet haben.  
3. Wählen Sie das Kontrollkästchen **Konvertierung durchführen**.  

    > [!IMPORTANT]  
    >  Deaktivieren Sie das Kontrollkästchen **Tool zum Ändern des MwSt.-Satzes abgeschlossen**. Das Kontrollkästchen wird automatisch aktiviert, wenn die Umrechnung für die MwSt.-Satzänderung abgeschlossen ist.  

4. Wählen Sie die Aktion **Konvertieren** aus.  
5. Nachdem die Konvertierung abgeschlossen ist, wählen Sie die Aktion **Änderungsprotokollposten für MwSt.-Satz**, um die Ergebnisse der Konvertierung anzuzeigen.  

> [!IMPORTANT]  
>  Nachdem die Umrechnung abgeschlossen ist, wird das Feld **Konvertiert** in der Tabelle **Protokollposten für MwSt.-Satzänderung** ausgewählt und das Feld **Konvertierungsdatum** in der Tabelle **Protokollposten für MwSt.-Satzänderung** wird mit dem Umrechnungsdatum ausgefüllt.  
## <a name="see-also"></a>Siehe auch  
[Mehrwertsteuer einrichten](finance-setup-vat.md)  
[Einrichten von unrealisierter Mehrwertsteuer](finance-setup-unrealized-vat.md)      
[Meldung der Mehrwertsteuer an eine Steuerbehörde](finance-how-report-vat.md)  
[Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md)  
[Lokale Funktion in Business Central](about-localization.md)
