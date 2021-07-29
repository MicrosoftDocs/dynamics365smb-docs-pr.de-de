---
title: "So geht's: Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen | Microsoft Docs"
description: Erklärt, wie Sie eine Einkaufsgutschrift erstellen und buchemn, wenn Sie Artikel an einen Kreditor zurückgeben möchten oder eingekaufte Services stornieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e43f5c5dd2a785a0268b9cf61794de1f8fa73a9a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445551"
---
# <a name="process-purchase-returns-or-cancellations"></a>Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen

Wenn Sie Artikel an Ihren Kreditor zurückschicken oder Dienstleistungen löschen wollen, die Sie eingekauft haben, können Sie eine Einkaufsgutschrift erstellen und buchen, die die angeforderte Änderung im Hinblick auf die ursprünglichen Einkaufsrechnung angibt. Um korrekte Verkaufsrechnungsinformationen einzuschließen, können Sie die Verkaufsgutschrift direkt aus der gebuchten Verkaufsrechnung erstellen oder neue Verkaufsgutschrift mit der Rechnungsinformationen erstellen.

Wenn Sie mehr Kontrolle für den Rücklieferungsvorgang, die Logistikbelege oder die Artikelbehandlung benötigen, wenn Sie Artikel von mehreren Verkaufsbelegen mit einer Rücklieferung bearbeiten, dann können Sie Verkaufsrückgabeaufträge erstellen. Wenn Sie die Einkaufsreklamation als fakturiert buchen, wird automatisch eine Einkaufsgutschrift erstellt. Weitere Informationen finden Sie unter [Einkaufsreklamation auf einem oder mehreren gebuchten Einkaufsbelegen erstellen](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
> Wenn eine gebuchte Einkaufsrechnung noch nicht bezahlt wurde, können Sie die **Korrigieren** oder **Abbrechen**-Funktionen auf der gebuchten Einkaufsrechnung verwenden, um die entsprechenden Transaktionen automatisch zu stornieren. Diese Funktionen arbeiten nur für nicht geleistete Rechnungen, und sie unterstützen nicht Teil-Reklamationen oder Kündigungen. Sie können auch keine Einkaufsrechnungen korrigieren oder stornieren, die mit Belegen aus mehreren Einkaufsbestellungen gebucht wurden. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Einkaufsrechnungen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Normalerweise erstellen Sie eine Einkaufsgutschrift als Antworten auf eine Gutschrift, die Ihnen von einem Kreditor gesendet wird. Die Einkaufsgutschrift oder die Einkaufsreklamation dient als Ihre interne Dokumentation des Gutschriftsvorgangs zu den Buchhaltungszwecken oder den Versand der einbezogenen Artikel.

Die Änderung mögen mit allen Produkten auf der Rechnung der ursprünglichen Einkaufsrechnung oder nur mit einigen der Produkte, verknüpft werden. Entsprechend können Sie die erhaltenen Artikel teilweise zurückgeben oder Teil-Vergütung von erhaltenen Services. In diesem Fall müssen Sie Informationen in den Zeilen der Verkaufsgutschrift oder der Verkaufsreklamation bearbeiten.

Zusätzlich zur ursprünglich gebuchten Einkaufsrechnung können Sie die Einkaufsgutschrift für andere Einkaufsbelege übernehmen, beispielsweise einer anderen gebuchten Einkaufsrechnung, da der Kreditor auch die Artikel zurücksendet, die mit dieser Rechnung geliefert werden.

Die Gutschriftsbuchung stellt auch jegliche Artikel Zu-/Abschläge wieder her, die dem gebuchten Beleg zugewiesen wurden, sodass die Wertposten des Artikels wieder identisch sind, wie bevor der Artikel Zu-/Abschlag zugewiesen wurde.

## <a name="inventory-costing"></a>Lagerkosten
Um die korrekte Lagerbewertung beizubehalten, möchten Sie üblicherweise zurückgegebene Artikel im Lager zum Einstandspreis, zum dem sie verkauft wurden und nicht mit dem aktuellen Einstandspreis einlagern. Dies wird als Einstandspreisrückverfolgung bezeichnet.

Zwei Funktionen sind vorhanden, um die Einstandspreisrückverfolgung automatisch zuzuweisen.  

|Funktion|Description|  
|------------------|---------------------------------------|  
|Funktion **Zu stornierende gebuchte Belegzeilen abrufen** auf der Seite **Einkaufsreklamation**|Kopiert Zeilen einer oder mehrerer gebuchter Verkaufsbelegzeilen, um den ursprünglichen Auftrag zu stornieren. Weitere Informationen finden Sie unter [Einkaufsreklamation auf einem oder mehreren gebuchten Einkaufsbelegen erstellen](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|**Kopieren aus Dokument** Funktion auf den Seiten **Einkaufsgutschrift** und **Rückgabeauftrag**|Kopiert den Kopf und die Zeilen aus einem gebuchten Beleg, der storniert werden soll.<br /><br /> Erfordert, dass das Kontrollkästchen **Einst.-Pr.-Rückverfolg. notw.** auf der Seite **Kreditoren & Einkauf Einr.** ausgewählt ist.|

Um exakte Einstandspreisstornierung manuell zuzuordnen, müssen Sie das Feld **Ausgegl. von Artikelposten** für alle Rückholbelegzeile Art wählen und dann die Nummer des ursprünglichen Verkaufspostens. Dies verknüpft die Einkaufsgutschrift oder Einkauzfsreklamation mit dem ursprünglichen Einkaufsposten und stellt sicher, dass der Artikel mit dem ursprünglichen Einstandspreis bewertet wird.

Weitere Informationen finden Sie unter [Designdetails: Lagerkosten](design-details-inventory-costing.md).

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Eine neue Einkaufsgutschrift aus einer gebuchte Einkaufsrechnung erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gebuchte Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie das Feld **Gebuchte Einkaufsrechnung**, um die Seite **Korrekturgutschrift erstellen** zu öffnen, und wählen Sie die gebuchte Einkaufsrechnung aus, die Sie stornieren möchten.

    Die meisten Felder im Einkaufsgutschriftskopf werden mit den Informationen aus der gebuchten Einkaufsrechnung ausgefüllt. Sie können alle Felder bearbeiten, zum Beispiel mit neuen Daten, die die Rückholvereinbarung wiedergeben.
3. Bearbeiten Sie Informationen über die Zeilen entsprechend der Vereinbarung, wie die Anzahl der zurückzuerstattenden Artikel oder der gutzuschreibende Betrag.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus.
5. Auf der Seite **Kreditorenposten zuweisen** wählen Sie die Zeile mit dem gebuchten Einkaufsbeleg, die Sie der Einkaufsgutschrift zuordnen möchten, und wählen Sie dann **Zuweisungs-ID festlegen** aus. Die Nummer der Einkaufsgutschrift wird im Feld **Zuweisungs-ID** eingefügt.
6. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, den Sie ausgleichen möchten, wenn dieser kleiner ist als der ursprüngliche Betrag.

    Im unteren Bereich der Seite **Kreditorenposten zuweisen** können Sie den Gesamtbetrag sehen, um alle beteiligten Posten zu stornieren, nämlich wenn der Wert im Feld **Saldo** Null ist.
7. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie die Einkaufsgutschrift buchen, wird sie für die angegebenen Einkaufsbelege angewandt.

    Nachdem Sie die erforderlichen Einkaufsgutschriftszeilen erstellt oder bearbeitet haben, und der Ausgleich einzelner oder mehrerer Posten angegeben wird, können Sie fortfahren, die Einkaufsgutschrift zu buchen.
8. Wählen Sie die Aktion **Buchen** aus.

Die gebuchten Einkaufsrechnungen, auf die Sie die Gutschrift anzuwenden, werden jetzt umgekehrt. Wenn Sie bereits die ursprüngliche Rechnung bezahlt haben, sollte der Kreditor die Zahlung jetzt an Sie jetzt zurückerstatten. Wenn die Gutschrift nur für einen Teil des Produkts auf der ursprünglichen Rechnung gilt, können Sie nur den Restbetrag auf der Rechnung der ursprünglichen Einkaufsrechnung bezahlen, um sie zu schließen.

Die Einkaufsgutschrift wird entfernt und durch einen neuen Beleg in der Liste der gebuchten Einkaufsgutschriften ersetzt.

## <a name="to-create-a-purchase-credit-memo-by-copying-a-posted-purchase-invoice"></a>Erstellt eine neue Einkaufsgutschrift, um eine gebuchte Einkaufsrechnung zurückzusetzen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, um eine neue leere Einkaufsgutschrift zu öffnen.
3. Geben Sie im Feld **Kreditor** den Namen eines vorhandenen Kreditors ein.
4. Wählen Sie die Aktion **Aus Dokument kopieren**.
5. Wählen Sie auf der Seite **Einkaufsbeleg kopieren** im Feld **Dokumenttyp** **Rechnung buchen** aus.
6. Wählen Sie das Feld **Belegnr.**, um die Seite **Geb. Einkaufsrechnungen** zu öffnen, und wählen Sie die gebuchte Einkaufsrechnung aus, die Sie stornieren möchten.
7. Wählen Sie das Kontrollkästchen **Zeilen neu berechnen**, wenn die kopierten gebuchten Einkaufsrechnungszeilen, mit einzelnen Änderungen im Artikelpreis und im Einstandspreis, aktualisiert werden sollen, da die Rechnung gebucht wurde.
8. Wählen Sie die Schaltfläche **OK** aus. Die kopierten Rechnungszeilen werden in die Einkaufsgutschrift eingefügt.
9. Schließen Sie die Einkaufsgutschrift ab, so wie dies unter [Eine neue Einkaufsgutschrift aus einer gebuchte Einkaufsrechnung erstellen](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice) erklärt ist.

## <a name="to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents"></a>Weitere Informationen finden Sie unter „Einkaufsreklamation auf einem oder mehreren gebuchten Einkaufsbelegen erstellen“.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsreklamationen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
4. Im Inforegister **Zeilen** können Sie die Zeilen manuell ausfüllen, oder kopieren Sie Informationen aus anderen Belegen, um die Zeilen automatisch auszufüllen:

    - Die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** können Sie verwenden, um eine oder mehrere gebuchte Belegzeilen aus einem oder mehreren gebuchten Belegen zu kopieren. Diese Funktion ermöglicht Ihnen die exakte Stornierung der Einstandspreise aus der gebuchten Belegzeile. Diese Funktion wird in den folgenden Schritten beschrieben.    
    - Verwenden Sie die Funktion **Aus Dokument kopieren**, um ein vorhandenes Dokument in den Rückgabeauftrag zu kopieren. Verwenden Sie diese Funktion zum Kopieren des gesamten Belegs. Dies kann entweder ein bereits gebuchter oder ein noch nicht gebuchter Beleg sein. Diese Funktion ermöglicht die Einstandspreisrückverfolgung nur dann, wenn die **Einstandspreisrückverfolgung als obligatorisch** auf der Seite **Debitoren & Verkauf Einr.** eingerichtet ist.  

5. So verwenden Sie die Funktion **Zu stornierende Belegzeilen** abrufen
6. Wählen Sie oben auf der Seite **Gebuchte Einkaufsbelegzeilen** das Feld **Nur stornierbare Zeilen anzeigen aus,** wenn Sie nur Zeilen mit Mengen anzeigen möchten, die noch nicht zurückgesendet oder, im Falle von Einkaufszeilen, verkauft oder verbraucht wurden. Wenn eine gebuchte Einkaufsrechnungsmenge beispielsweise bereits zurückgesendet wurde, möchten Sie diese Menge möglicherweise nicht mit einem neuen Einkaufsreklamationsbeleg zurücksenden.

    > [!NOTE]  
    >  Das Feld bezieht sich nur auf gebuchte Liefer- und Rechnungszeilen, nicht auf gebuchte Rücklieferungs- oder Gutschriftzeilen.  

    Klicken Sie links auf der Seite, die verschiedenen Belegarten werden aufgeführt und die Nummer in Klammern steht für die Anzahl der Belege, die von jeder Belegart verfügbar sind.

7. Wählen Sie im Feld **Belegartfilter** die Art der gebuchten Belegzeilen aus, die Sie verwenden möchten.  
8. Wählen Sie die Zeilen aus, die Sie in den neuen Beleg kopieren möchten.  

    > [!NOTE]  
    >  Wenn Sie zum Auswählen aller Zeilen STRG+A verwenden, werden alle Zeilen in dem von Ihnen festgelegten Filter kopiert, jedoch wird der Filter **Nur stornierbare Mengen anzeigen** ignoriert. Angenommen, Sie haben die Zeilen nach einem bestimmten Beleg mit zwei Zeilen gefiltert, von denen eine bereits auf "Zurückgesendet" gesetzt wurde. Auch wenn das Feld **Nur stornierbare Mengen anzeigen** ausgewählt wird, werden beim Drücken von STRG+A zum Kopieren aller Zeilen beide Zeilen kopiert und nicht nur die eine, die noch nicht storniert wurde.  

9. Klicken Sie auf die Schaltfläche **OK**, um die Zeilen in den neuen Beleg zu kopieren.  

    Die folgenden Prozesse werden durchgeführt:  

    - Für gebuchte Belegzeilen der Art **Artikel** wird eine neue Belegzeile erstellt, die eine Kopie der gebuchten Belegzeile ist, und zwar mit der noch nicht stornierten Menge. Das Feld **Ausgegl. von Artikelposten** wird ausgefüllt mit der Nummer des Artikelpostens der gebuchten Belegzeile.  

    - Bei gebuchten Belegzeilen, die nicht von der Art **Artikel** sind, wie z. B. Artikel Zu-/Abschläge, wird eine neue Belegzeile erstellt, die eine Kopie der ursprünglichen gebuchten Belegzeile ist.  

    - Die Anwendung berechnet das Feld **Einstandspreis (MW)** der neuen Zeile anhand der Kosten in den entsprechenden Artikelposten.  

    - Wenn es sich bei dem kopierten Beleg um eine gebuchte Lieferung, einen gebuchten Wareneingang, eine gebuchte Rücksendung oder eine gebuchte Rücklieferung handelt, wird der VK-Preis automatisch anhand der Artikelkarte berechnet.  

    - Wenn es sich bei dem gebuchten Beleg um eine gebuchte Rechnung oder Gutschrift handelt, werden VK-Preis, Rechnungsrabatte und Zeilenrabatte aus der gebuchten Belegzeile kopiert.  

    - Wenn die gebuchte Belegzeile Artikelverfolgungszeilen enthält, wird Feld **Anwendung vom Artikeleintrag** auf der Artikelnachverfolgungszeilen mit den entsprechenden Artikelpostennummern aus den gebuchten Artikelverfolgungszeilen gefüllt.  

     Beim Kopieren aus einer gebuchten Rechnung oder einer gebuchten Gutschrift kopiert die Anwendung alle relevanten Rechnungsrabatte und Zeilenrabatte, die zum Zeitpunkt der Buchung dieses Belegs gelten, von der gebuchten Belegzeile in die neue Belegzeile. Beachten Sie jedoch, dass, wenn die Option **Rechnungsrab. berechnen** auf der Seite **Verkaufs- und Forderungseinrichtung** aktiviert ist, der Rechnungsrabatt neu berechnet wird, wenn Sie die neue Belegzeile buchen. Daher kann es sein, dass der Zeilenbetrag für die neue Zeile sich von dem Zeilenbetrag für die ursprüngliche Belegzeile unterscheidet, je nach der Neuberechnung des Rechnungsrabatts.  

    > [!NOTE]  
    >  Wenn ein Teil der Menge der gebuchten Belegzeile bereits zurückgesendet, verkauft oder verbraucht wurde, wird nur für die Menge, die am Lager verbleibt oder die nicht zurückgesendet wurde, eine Zeile erstellt. Wurde die vollständige Menge der gebuchten Belegzeile bereits storniert, wird keine neue Belegzeile erstellt.  
    >
    >  Wenn der Warenfluss im gebuchten Beleg der gleiche wie der Warenfluss im neuen Beleg ist, wird einfach eine Kopie der ursprünglich gebuchten Belegzeile im neuen Beleg erstellt. Das Feld **Ausgegl. von Artikelposten** wird nicht ausgefüllt, da in diesem Fall eine exakte Einstandspreisstornierung nicht möglich ist. Wenn Sie beispielsweise die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** zum Abrufen einer gebuchten Einkaufsgutschriftzeile für eine neue Einkaufsgutschrift verwenden, wird nur die ursprünglich gebuchte Gutschriftszeile in die neue Gutschrift kopiert.  

10. Auf der Seite **EInkaufsreklamation** im Feld **Reklamationsgrundcode** auf jeder Zeile wählen Sie den Grund für die Reklamation aus.
11. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-create-a-replacement-purchase-order-from-a-purchase-return-order"></a>So erstellen Sie eine Ersatzbestellung anhand von einer Reklamation

Möglicherweise einigen Sie sich mit Ihrem Kreditoren darauf, dass Sie für einen – eventuell beschädigten – Artikel, den Sie bei ihm gekauft haben, eine Entschädigung in Form eines Austauschartikels erhalten. Der Austauschartikel kann derselbe Artikel oder ein anderer sein. Diese Situation kann eintreten, wenn der Lieferant versehentlich den falschen Artikel geliefert hat.  

1.  Auf der Seite **Einkaufsreklamation** für einen aktiven Rückgabevorgang in einer leeren Zeile, erzeugen Sie einen negativen Eintrag für den Austauschartikel, indem Sie einen negativen Betrag in das Feld **Menge** eingeben.  
2. Wählen Sie die **Negative Zeilen übertragen** Aktion aus.  
3. Füllen Sie auf der Seite **Negative Einkaufszeile verschieben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus. Die negative Zeile wird aus der Einkaufsreklamation gelöscht, und eine neue Einkaufsbestellung wird erstellt. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).  

## <a name="to-create-a-purchase-allowance"></a>So erstellen Sie einen Einkaufsnachlass

Falls Sie von einem Kreditor Artikel erhalten, die nicht Ihren Vorstellungen entsprechen, z. B. weil sie die falsche Farbe haben oder beschädigt sind, kann Ihnen der Kreditor einen Rabatt anbieten.  

Sie können diesen reduzierten EK-Preis als Zu-/Abschlag für Artikel in einer Gutschrift oder einer Reklamation buchen und mit der gebuchten Einkaufslieferung verknüpfen. Nachfolgend wird es für eine Einkaufsreklamation erläutert, aber dieselben Schritte gelten für eine Einkaufsgutschrift zu.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu**, um eine neue leere Einkaufsgutschrift zu öffnen.  
3. Füllen Sie den Kopf der Gutschrift mit den Informationen über den Kreditor aus, von dem Sie den Einkaufsnachlass erhalten haben.  
4. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Art** die Option **Zu-/Abschlag (Artikel)**.  
5. Geben Sie im Feld **Nr.** den entsprechenden Chargenwert ein.  

    Sie haben die Möglichkeit, eine spezielle Artikel Zu-/Abschlagsnummer für Einkaufsrabatte einzurichten.  
6. Geben Sie im Feld **Menge** den Wert **1** ein.  
7. Geben Sie in dem Feld **EK-Preis** den Betrag des Einkaufsrabattes an.  
8. Weisen Sie den Einkaufsrabatt den Artikeln als Artikel Zu-/Abschlag in der gebuchten Einkaufslieferung zu. Weitere Informationen finden Sie untert [Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md). Kehren Sie zur Seite **Gutschrift** zurück.

Wenn Sie die Verkaufsreklamation buchen, wird die Wiedereinlagerungsgebühr zu dem entsprechenden Betrag des Verkaufspostens addiert. Auf diese Art können Sie genaue Bestandbewertung führen.  

## <a name="to-combine-return-shipments"></a>So fassen Sie Rücklieferungen zusammen

Wenn Sie mehrere Artikel , für die verschieden Einkaufsreklamationen gelten, an denselben Kreditor zurücksenden möchten, können Sie die Funktion **Sammelrücklieferungen** verwenden.  

Wenn Sie die Artikel liefern, buchen Sie die jeweiligen Einkaufsreklamationen als geliefert und erzeugen damit gebuchte Rücklieferungen.  

Wenn Sie diese Artikel fakturieren möchten, können Sie eine Einkaufsgutschrift anlegen und die gebuchten Rücklieferzeilen automatisch in diesen Beleg kopieren, anstatt jede Einkaufsreklamation einzeln zu fakturieren. Dann können Sie die Einkaufsgutschrift buchen und gleichzeitig alle offenen Einkaufsreklamationen auf einmal fakturieren.  

Wenn Rücklieferungen in einer Gutschrift zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Einkaufsgutschrift erstellt. Das Feld **Menge fakturiert** auf der entstehenden Einkaufsreklamation wird ausgehend von der fakturierten Menge aktualisiert. Die ursprüngliche Einkaufsreklamation wird jedoch nicht gelöscht, auch wenn sie vollständig geliefert und fakturiert wurde, und Sie müssen daher die Einkaufsreklamation manuell löschen.

> [!NOTE]  
> Dieses Verfahren nimmt an, dass mehrere Einkaufsreklamationen für den Kreditor vorliegen, die alle als geliefert gebucht worden sind.     

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsgutschriften** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.  
4. Wählen Sie die **Rücklieferzeilen abrufen** Aktion aus.  
5. Wählen Sie mehrere Rücklieferzeilen aus, die in der Rechnung enthalten sein sollen:  

    Wenn Sie eine falsche Rücklieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Einkaufsgutschrift löschen und die Funktion **Rücklieferzeilen holen** erneut ausführen.  
6. Wählen Sie die Aktion **Buchen** aus.  

### <a name="to-remove-open-purchase-return-orders-after-combined-return-shipment-posting"></a>Offene Einkaufsreklamationen nach kombinierter Rücklieferungsbuchung entfernen  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Erledigte Einkaufsrechnungen-Rücklieferungen löschen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.  
3. Sie können die einzelnen Einkaufsreklamtionen auch manuell löschen.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]