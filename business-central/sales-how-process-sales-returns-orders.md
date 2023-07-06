---
title: Verkaufsaufträge Rücklieferung verarbeiten
description: 'Beschreibt, wie Sie einen Verkaufsauftrag erstellen, um eine Rückgabe, Stornierung oder Rückerstattung für Artikel oder Dienstleistungen zu verarbeiten, für die Sie eine Zahlung erhalten haben.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: edupont
---
# <a name="process-sales-return-orders"></a><a name="process-sales-return-orders"></a><a name="process-sales-return-orders"></a>Verkaufsaufträge Rücklieferung verarbeiten

Wenn Sie mehr Steuerelemente für den Rücklieferungsprozess benötigen, z.B. Lagerbelege für die Artikelabwicklung oder eine bessere Übersicht beim Empfang von Artikeln aus mehreren Verkaufsbelegen mit einer Rücklieferung, dann können Sie Verkaufsreklamationen erstellen. Ein Rücklieferungsauftrag gibt automatisch die zugehörige Verkaufsgutschrift und andere rücklieferungsbezogene Belege aus, wie z.B. einen Ersatzverkaufsauftrag, falls erforderlich.

Zusätzlich zur ursprünglich gebuchten Verkaufsrechnung können Sie die Verkaufsgutschrift für andere Verkaufsbelege übernehmen, beispielsweise einer anderen gebuchten Verkaufsrechnung, da der Debitor auch die Artikel zurücksendet, die mit dieser Rechnung geliefert werden.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a><a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a><a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Erstellen Sie einen Verkaufsauftrag für eine Rücklieferung auf der Grundlage eines oder mehrerer gebuchter Belege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsreklamationen** ein und wählen Sie den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
4. Im Inforegister **Zeilen** können Sie die Zeilen manuell ausfüllen, oder kopieren Sie Informationen aus anderen Belegen, um die Zeilen automatisch auszufüllen:

    - Die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** können Sie verwenden, um eine oder mehrere gebuchte Belegzeilen aus einem oder mehreren gebuchten Belegen zu kopieren. Diese Funktion ermöglicht Ihnen die exakte Stornierung der Einstandspreise aus der gebuchten Belegzeile. Diese Funktion wird in den folgenden Schritten beschrieben.    
    - Verwenden Sie die Funktion **Aus Dokument kopieren**, um ein vorhandenes Dokument in den Rückgabeauftrag zu kopieren. Verwenden Sie diese Funktion zum Kopieren des gesamten Belegs. Dies kann entweder ein bereits gebuchter oder ein noch nicht gebuchter Beleg sein. Diese Funktion ermöglicht die Einstandspreisrückverfolgung nur dann, wenn die **Einstandspreisrückverfolgung** als obligatorisch auf der Seite **Debitoren & Verkauf Einr.** eingerichtet ist.  

5. Wählen Sie die Aktion **Verarbeiten** und dann die Aktion **Getragene Belegzeilen zum Stornieren**.
6. Wählen Sie oben auf der Seite **Gebuchte Verkaufsbelegzeilen** das Feld **Nur stornierbare Zeilen anzeigen aus,** wenn Sie nur Zeilen mit Mengen anzeigen möchten, die noch nicht zurückgesendet oder, im Falle von Einkaufszeilen, verkauft oder verbraucht wurden. Wenn eine gebuchte Verkaufsrechnungsmenge beispielsweise bereits zurückgesendet wurde, möchten Sie diese Menge möglicherweise nicht mit einem neuen Verkaufsreklamationsbeleg zurücksenden.

    > [!NOTE]  
    >  Das Feld bezieht sich nur auf gebuchte Liefer- und Rechnungszeilen, nicht auf gebuchte Rücklieferungs- oder Gutschriftzeilen.

    Klicken Sie links auf der Seite, die verschiedenen Belegarten werden aufgeführt und die Nummer in Klammern steht für die Anzahl der Belege, die von jeder Belegart verfügbar sind.

7. Wählen Sie im Feld **Belegartfilter** die Art der gebuchten Belegzeilen aus, die Sie verwenden möchten.  
8. Wählen Sie die Zeilen aus, die Sie in den neuen Beleg kopieren möchten.  

    > [!NOTE]  
    >  Wenn Sie zum Auswählen aller Zeilen <kbd>STRG</kbd>+<kbd>A</kbd> verwenden, werden alle Zeilen in dem von Ihnen festgelegten Filter kopiert, jedoch wird der Filter **Nur stornierbare Mengen anzeigen** ignoriert. Angenommen, Sie haben die Zeilen nach einem bestimmten Beleg mit zwei Zeilen gefiltert, von denen eine bereits auf "Zurückgesendet" gesetzt wurde. Auch wenn das Feld **Nur stornierbare Mengen** anzeigen ausgewählt wird, werden beim Drücken von <kbd>STRG</kbd>+<kbd>A</kbd> zum Kopieren aller Zeilen beide Zeilen kopiert und nicht nur die eine, die noch nicht storniert wurde.  

9. Klicken Sie auf die Schaltfläche **OK**, um die Zeilen in den neuen Beleg zu kopieren.  

    Die folgenden Prozesse werden durchgeführt:  

    -   Für gebuchte Belegzeilen der Art **Artikel** wird eine neue Belegzeile erstellt, die eine Kopie der gebuchten Belegzeile ist, und zwar mit der noch nicht stornierten Menge. Das Feld **Ausgegl. von Artikelposten** wird ausgefüllt mit der Nummer des Artikelpostens der gebuchten Belegzeile.  

    -   Bei gebuchten Belegzeilen, die nicht von der Art **Artikel** sind, wie z. B. Artikel Zu-/Abschläge, wird eine neue Belegzeile erstellt, die eine Kopie der ursprünglichen gebuchten Belegzeile ist.  

    -   Die Anwendung berechnet das Feld **Einstandspreis (MW)** der neuen Zeile anhand der Kosten in den entsprechenden Artikelposten.  

    -   Wenn es sich bei dem kopierten Beleg um eine gebuchte Lieferung, einen gebuchten Wareneingang, eine gebuchte Rücksendung oder eine gebuchte Rücklieferung handelt, wird der VK-Preis automatisch anhand der Artikelkarte berechnet.  

    -   Wenn es sich bei dem gebuchten Beleg um eine gebuchte Rechnung oder Gutschrift handelt, werden VK-Preis, Rechnungsrabatte und Zeilenrabatte aus der gebuchten Belegzeile kopiert.  

    -   Wenn die gebuchte Belegzeile Artikelverfolgungszeilen enthält, wird Feld **Anwendung vom Artikeleintrag** auf der Artikelnachverfolgungszeilen mit den entsprechenden Artikelpostennummern aus den gebuchten Artikelverfolgungszeilen gefüllt.  

     Beim Kopieren aus einer gebuchten Rechnung oder einer gebuchten Gutschrift kopiert die Anwendung alle relevanten Rechnungsrabatte und Zeilenrabatte, die zum Zeitpunkt der Buchung dieses Belegs gelten, von der gebuchten Belegzeile in die neue Belegzeile. Beachten Sie jedoch, dass, wenn die Option **Rechnungsrab. berechnen** auf der Seite **Verkaufs- und Forderungseinrichtung** aktiviert ist, der Rechnungsrabatt neu berechnet wird, wenn Sie die neue Belegzeile buchen. Daher kann es sein, dass der Zeilenbetrag für die neue Zeile sich von dem Zeilenbetrag für die ursprüngliche Belegzeile unterscheidet, je nach der Neuberechnung des Rechnungsrabatts.  

     > [!NOTE]  
     >  Wenn ein Teil der Menge der gebuchten Belegzeile bereits zurückgesendet, verkauft oder verbraucht wurde, wird nur für die Menge, die am Lager verbleibt oder die nicht zurückgesendet wurde, eine Zeile erstellt. Wurde die vollständige Menge der gebuchten Belegzeile bereits storniert, wird keine neue Belegzeile erstellt.  
     >   
     >  Wenn der Warenfluss im gebuchten Beleg der gleiche wie der Warenfluss im neuen Beleg ist, wird einfach eine Kopie der ursprünglich gebuchten Belegzeile im neuen Beleg erstellt. Das Feld **Ausgegl. von Artikelposten** wird nicht ausgefüllt, da in diesem Fall eine exakte Einstandspreisstornierung nicht möglich ist. Wenn Sie beispielsweise die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** zum Abrufen einer gebuchten Verkaufsgutschriftzeile für eine neue Verkaufsgutschrift verwenden, wird nur die ursprünglich gebuchte Gutschriftszeile in die neue Gutschrift kopiert.  

10. Auf der Seite **Verkaufsreklamation** im Feld **Reklamationsgrundcode** auf jeder Zeile wählen Sie den Grund für die Reklamation aus.
11. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a><a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a><a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>So erstellen Sie einen Austauschverkaufsauftrag von einer Verkaufsreklamation aus:
Möglicherweise entscheiden Sie, einen Debitoren für einen Artikel, den Sie ihm verkauft haben, zu entschädigen, indem Sie ihm den Artikel ersetzen. Sie können diesen Austausch mit demselben oder einem anderen Artikel vornehmen. Diese Situation könnte eintreten, wenn Sie dem Kunden z. B. versehentlich einen falschen Artikel geliefert haben.  

1. Auf der Seite **Einkaufsreklamation** für einen aktiven Rückgabevorgang in einer leeren Zeile, erzeugen Sie einen negativen Eintrag für den Austauschartikel, indem Sie einen negativen Betrag in das Feld **Menge** eingeben.  
2. Wählen Sie die **Negative Zeilen übertragen** Aktion aus.
3. Füllen Sie auf der Seite **Negative Verkaufszeile verschieben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie diese Stapelverarbeitung ausführen, wird die negative Zeile (für den Austauschartikel) aus der Verkaufsreklamation gelöscht und auf einer neuen **Verkaufsauftrag**-Seite eingefügt. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a><a name="to-create-return-related-documents-from-a-sales-return-order"></a><a name="to-create-return-related-documents-from-a-sales-return-order"></a>So erstellen Sie reklamationsbezogene Belege aus einer Verkaufsreklamation
Lassen Sie alle relevanten Verkaufsreklamationsbelege automatisch erstellen, z. B. eine Einkaufsreklamation, eine Ersatzbestellung oder einen neuen Verkaufsauftrag. Dies ist beispielsweise in Fällen nützlich, in denen Sie Artikel mit den Garantien bearbeiten möchten, die von Kreditoren bereitgestellt werden.

1. Auf der Seite **Verkaufsreklamation** für einen aktiven Rückgabevorgang wählen Sie die Aktion **Reklamationsbez. Belege erstellen** aus.
2. Geben Sie im **Kreditorennr.** Feld die Nummer des Kreditors ein, wenn Sie Kreditorenbelege automatisch erstellen möchten.
3. Wenn ein Artikel an den Kreditor zurückgeliefert werden muss, aktivieren Sie das Kontrollkästchen **Eink.-Reklamation erstellen**.
4. Wenn ein Artikel beim Kreditor bestellt werden muss, aktivieren Sie das Kontrollkästchen **Bestellung erstellen**.
5. Wenn ein Auftrag für eine Ersatzlieferung erstellt werden muss, aktivieren Sie das Kontrollkästchen **Verkaufsauftrag erstellen**.

## <a name="to-create-a-restock-charge"></a><a name="to-create-a-restock-charge"></a><a name="to-create-a-restock-charge"></a>So legen Sie eine Wiedereinlagerungsgebühr an
Möglicherweise entscheiden Sie sich dazu, Ihren Debitoren mit einer Wiedereinlagerungsgebühr zu belasten, um die Bearbeitungskosten für die Rücksendung des Artikels abzudecken. Diese Situation könnte z. B. eintreten, wenn der Debitor aus Versehen den falschen Artikel bestellt hatte oder seine Meinung geändert hat, nachdem er den Artikel erhalten hat.

Sie können diesen herabgesetzten Preis als Zu-/Abschlag (Artikel) in einer Gutschrift oder einer Reklamation buchen und ihn der gebuchten Lieferung zuordnen. Im Folgenden wird dies für einen Verkaufsreklamationsauftrag beschrieben, aber die gleichen Schritte gelten auch für eine Verkaufsgutschrift.

1. Öffnen Sie die Seite **Verkaufsreklamation** für einen aktiven Rückgabevorgang.
2. Geben Sie eine neue Zeile ein, und wählen Sie **Zu-/Abschlag (Artikel)** im Feld **Art**.  
3. Füllen Sie die Felder für jede mögliche Artikelzuschlagszeile aus. Weitere Informationen finden Sie untert [Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md).  

Wenn Sie die Verkaufsreklamation buchen, wird die Wiedereinlagerungsgebühr zu dem entsprechenden Betrag des Verkaufspostens addiert. Auf diese Art können Sie genaue Bestandbewertung führen.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
