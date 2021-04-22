---
title: Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen | Microsoft Docs
description: Beschreibt, wie eine Verkaufsgutschrift erstellt, eine Reklamation, Stornierung oder eine Vergütung für Artikel oder Dienstleistungen verarbeitet wird, für Sie eine Zahlung erhalten haben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b5f6daba9251dad73b8924312e35a5cb1474bdb3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778697"
---
# <a name="process-sales-returns-or-cancellations"></a>Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen
Wenn Ihr Debitor Artikel zurückschicken oder Dienstleistungen löschen will, die Sie verkauft haben, können Sie eine Einkaufsgutschrift erstellen und buchen, die die angeforderte Änderung im Hinblick auf die ursprünglichen Einkaufsrechnung angibt. Um korrekte Verkaufsrechnungsinformationen einzuschließen, können Sie die Verkaufsgutschrift direkt aus der gebuchten Verkaufsrechnung erstellen oder neue Verkaufsgutschrift mit der Rechnungsinformationen erstellen.

Wenn Sie mehr Kontrolle für den Rücklieferungsvorgang, die Logistikbelege oder die Artikelbehandlung benötigen, wenn Sie Artikel von mehreren Verkaufsbelegen mit einer Rücklieferung bearbeiten, dann können Sie Verkaufsrückgabeaufträge erstellen. Eine Verkaufsreklamation löst automatisch die zugehörige Verkaufsgutschrift sowie andere Dokumente wie Verkaufsauftrag für Ersatzlieferungen aus, sofern erforderlich. Weitere Informationen finden Sie unter [Verkaufsreklamation auf einem oder mehreren gebuchten Verkaufsbelegen erstellen](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).

> [!NOTE]  
>   Wenn eine gebuchte Verkaufsrechnung noch nicht bezahlt wurde, können Sie die Funktionen **Korrigieren** oder **Abbrechen** auf der gebuchten Verkaufsrechnung verwenden, um die entsprechenden Transaktionen automatisch zu stornieren. Diese Funktionen gehen nur für nicht geleistete Rechnungen, und sie unterstützen nicht Teil-Reklamationen oder Stornierungen. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Verkaufsrechnungen](sales-how-correct-cancel-sales-invoice.md).

Eine Rücklieferungs- oder eine Vergütung kann sich nur auf einige der Artikel oder der Services in der ursprünglichen Verkaufsrechnung beziehen. In diesem Fall müssen Sie Informationen in den Zeilen der Verkaufsgutschrift oder der Verkaufsreklamation bearbeiten. Wenn Sie die Verkaufsgutschrift oder Verkaufsreklamationen buchen, werden die Verkaufsbelege, die von Änderungen betroffen sind rückgängig gemacht und eine Rückerstattung für den Debitor wird erstellt. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).  

Zusätzlich zur ursprünglich gebuchten Verkaufsrechnung können Sie die Verkaufsgutschrift für andere Verkaufsbelege übernehmen, beispielsweise einer anderen gebuchten Verkaufsrechnung, da der Debitor auch die Artikel zurücksendet, die mit dieser Rechnung geliefert werden.

Sie können die gebuchte Verkaufsgutschrift an den Debitor senden, um die Rücksendung oder Stornierung zu bestätigen und mitzuteilen, dass der zugehörige Wert erstattet werden wird, wenn zum Beispiel Artikel zurückgegeben werden oder eine Service-Stornierung vereinbart wurde.

Die Gutschriftsbuchung stellt auch jegliche Artikel Zu-/Abschläge wieder her, die dem gebuchten Beleg zugewiesen wurden, sodass die Wertposten des Artikels wieder identisch sind, wie bevor der Artikel Zu-/Abschlag zugewiesen wurde.

> [!NOTE]
> Die Buchhaltungsaspekte von Retouren, wie z. B. die Zahlungen an Debitoren als Rückerstattung, wird als Buchhaltungsarbeit betrachtet und hier nicht beschrieben. Weitere Informationen finden Sie unter [Kreditoren verwalten](payables-manage-payables.md).

## <a name="inventory-costing"></a>Lagerkosten
Um die korrekte Lagerbewertung beizubehalten, möchten Sie üblicherweise zurückgegebene Artikel im Lager zum Einstandspreis, zum dem sie verkauft wurden und nicht mit dem aktuellen Einstandspreis einlagern. Dies wird als Einstandspreisrückverfolgung bezeichnet.

Zwei Funktionen sind vorhanden, um die Einstandspreisrückverfolgung automatisch zuzuweisen.   

|Funktion|Description|  
|------------------|---------------------------------------|  
|Funktion **Zu stornierende gebuchte Belegzeilen abrufen** auf der Seite **Verkaufsreklamation**|Kopiert Zeilen einer oder mehrerer gebuchter Verkaufsbelegzeilen, um den ursprünglichen Auftrag zu stornieren. Weitere Informationen finden Sie unter [Verkaufsreklamation auf einem oder mehreren gebuchten Verkaufsbelegen erstellen](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|**Kopieren aus Dokument** Funktion auf den Seiten **Umsatzgutschrift** und **Rücksendeauftrag**|Kopiert den Kopf und die Zeilen aus einem gebuchten Beleg, der storniert werden soll.<br /><br /> Erfordert, dass das Kontrollkästchen **Einst.-Pr.-Rückverfolg. notw.** auf der Seite **Debitoren und Verkauf Einr.** ausgewählt ist.|

Um exakte Einstandspreisstornierung manuell zuzuordnen, müssen Sie das Feld **Ausgegl. von Artikelposten** für alle Rückholbelegzeile Art wählen und dann die Nummer des ursprünglichen Verkaufspostens. Dies verknüpft die Verkaufsgutschrift oder Verkaufsreklamation mit dem ursprünglichen Verkaufsposten und stellt sicher, dass der Artikel mit dem ursprünglichen Einstandspreis bewertet wird.

Weitere Informationen finden Sie unter [Designdetails: Lagerkosten](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen.
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **Gebuchte Verkaufsrechnungen** ein und wählen Sie den entsprechenden Link.  
2. Wählen Sie das Feld **Gebuchte Verkaufsrechnung**, um die Seite **Korrekturgutschrift erstellen** zu öffnen, und wählen Sie die gebuchte Verkaufsrechnung aus, die Sie stornieren möchten.

    Der Verkaufsgutschriftskopf enthält einige Informationen aus der gebuchten Verkaufsrechnung. Sie können alle Felder bearbeiten, zum Beispiel mit neuen Daten, die die Rückholvereinbarung wiedergeben.  
3. Bearbeiten Sie Informationen über die Zeilen entsprechend der Vereinbarung, wie die Anzahl der zurückzuerstattenden Artikel oder der gutzuschreibende Betrag.
4. Wählen Sie die Aktion **Posten ausgleichen...** aus.
5. Auf der Seite **Debitorenposten zuweisen** wählen Sie die Zeile mit dem gebuchten Verkaufsbeleg, die Sie der Verkaufsgutschrift zuordnen möchten, und wählen Sie dann **Zuweisungs-ID festlegen** aus.

    Die Kennzeichnung der Verkaufsgutschrift wird im Feld **Zuweisungs-ID** angezeigt.
6. Geben Sie in jeder Zeile im Feld **Anzuwendender Betrag** den Betrag ein, den Sie ausgleichen möchten, wenn dieser kleiner ist als der ursprüngliche Betrag.  

    Im unteren Bereich der Seite **Debitorenposten zuweisen** können Sie den Gesamtbetrag sehen, um alle beteiligten Posten zu stornieren, nämlich wenn der Wert im Feld **Saldo** Null ist.
7. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie die Verkaufsgutschrift buchen, wird sie für die angegebenen gebuchten Verkaufsrechnungen angewandt.

    Nachdem Sie die erforderlichen Verkaufsgutschriftszeilen erstellt ober bearbeitet haben, und der Ausgleich einzelner oder mehrerer Posten angegeben wird, können Sie fortfahren, die Verkaufsgutschrift zu buchen.   
8. Wählen Sie die Aktion **Buchen und Senden** aus.  

Das Dialogfeld **Buchungs- und Sendebestätigung** wird geöffnet und zeigt die bevorzugte Sendemethode für den Debitor an. Sie können die Sendemethode ändern, indem Sie die Schaltfläche vom Feld **Beleg senden an** auswählen. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

Die gebuchten Verkaufsdokumente für die entsprechende Gutschrift werden nun storniert und eine Erstattung der Zahlung kann für den Debitor erstellt werden. Die Verkaufsgutschrift wird entfernt und durch einen neuen Beleg in der Liste der gebuchten Verkaufsgutschriften ersetzt.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen.
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell me-Funktion") aus, geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Neu**, um eine neue leere Verkaufsgutschrift zu öffnen.
3. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.
4. Wählen Sie die Aktion **Aus Dokument kopieren**.
5. Wählen Sie auf der Seite **Verkaufsbeleg kopieren** im Feld **Dokumenttyp** **Rechnung buchen** aus.
6. Wählen Sie das Feld **Belegnr.**, um die Seite **Geb. Verkaufsrechnungen** zu öffnen, und wählen Sie die gebuchte Verkaufsrechnung aus, die Sie stornieren möchten.
7. Wählen Sie das Kontrollkästchen **Zeilen neu berechnen**, wenn die kopierten gebuchten Verkaufsrechnungszeilen, mit einzelnen Änderungen im Artikelpreis und im Einstandspreis, aktualisiert werden sollen, da die Rechnung gebucht wurde.
8. Wählen Sie die Schaltfläche **OK** aus. Die kopierten Rechnungszeilen werden in die Verkaufsgutschrift eingefügt.
9. Schließen Sie die Verkaufsgutschrift ab, so wie dies unter [Erstellt eine neue Verkaufsgutschrift, um eine gebuchte Verkaufsrechnung zurückzusetzen](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice) erklärt ist.

## <a name="to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Weitere Informationen finden Sie unter „Verkaufsreklamation auf einem oder mehreren gebuchten Verkaufsbelegen erstellen“.
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsreklamationen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.
4. Im Inforegister **Zeilen** können Sie die Zeilen manuell ausfüllen, oder kopieren Sie Informationen aus anderen Belegen, um die Zeilen automatisch auszufüllen:

    - Die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** können Sie verwenden, um eine oder mehrere gebuchte Belegzeilen aus einem oder mehreren gebuchten Belegen zu kopieren. Diese Funktion ermöglicht Ihnen die exakte Stornierung der Einstandspreise aus der gebuchten Belegzeile. Diese Funktion wird in den folgenden Schritten beschrieben.    
    - Verwenden Sie die Funktion **Aus Dokument kopieren**, um ein vorhandenes Dokument in den Rückgabeauftrag zu kopieren. Verwenden Sie diese Funktion zum Kopieren des gesamten Belegs. Dies kann entweder ein bereits gebuchter oder ein noch nicht gebuchter Beleg sein. Diese Funktion ermöglicht die Einstandspreisrückverfolgung nur dann, wenn die **Einstandspreisrückverfolgung als obligatorisch** auf der Seite **Debitoren & Verkauf Einr.** eingerichtet ist.  

5. So verwenden Sie die Funktion **Zu stornierende Belegzeilen** abrufen
6. Wählen Sie oben auf der Seite **Gebuchte Verkaufsbelegzeilen** das Feld **Nur stornierbare Zeilen anzeigen aus,** wenn Sie nur Zeilen mit Mengen anzeigen möchten, die noch nicht zurückgesendet oder, im Falle von Einkaufszeilen, verkauft oder verbraucht wurden. Wenn eine gebuchte Verkaufsrechnungsmenge beispielsweise bereits zurückgesendet wurde, möchten Sie diese Menge möglicherweise nicht mit einem neuen Verkaufsreklamationsbeleg zurücksenden.

    > [!NOTE]  
    >  Das Feld bezieht sich nur auf gebuchte Liefer- und Rechnungszeilen, nicht auf gebuchte Rücklieferungs- oder Gutschriftzeilen.

    Klicken Sie links auf der Seite, die verschiedenen Belegarten werden aufgeführt und die Nummer in Klammern steht für die Anzahl der Belege, die von jeder Belegart verfügbar sind.

7. Wählen Sie im Feld **Belegartfilter** die Art der gebuchten Belegzeilen aus, die Sie verwenden möchten.  
8. Wählen Sie die Zeilen aus, die Sie in den neuen Beleg kopieren möchten.  

    > [!NOTE]  
    >  Wenn Sie zum Auswählen aller Zeilen STRG+A verwenden, werden alle Zeilen in dem von Ihnen festgelegten Filter kopiert, jedoch wird der Filter **Nur stornierbare Mengen anzeigen** ignoriert. Angenommen, Sie haben die Zeilen nach einem bestimmten Beleg mit zwei Zeilen gefiltert, von denen eine bereits auf "Zurückgesendet" gesetzt wurde. Auch wenn das Feld **Nur stornierbare Mengen anzeigen** ausgewählt wird, werden beim Drücken von STRG+A zum Kopieren aller Zeilen beide Zeilen kopiert und nicht nur die eine, die noch nicht storniert wurde.  

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

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>So erstellen Sie einen Austauschverkaufsauftrag von einer Verkaufsreklamation aus:
Möglicherweise entscheiden Sie, einen Debitoren für einen Artikel, den Sie ihm verkauft haben, zu entschädigen, indem Sie ihm den Artikel ersetzen. Sie können diesen Austausch mit demselben oder einem anderen Artikel vornehmen. Diese Situation könnte eintreten, wenn Sie dem Kunden z. B. versehentlich einen falschen Artikel geliefert haben.  

1. Auf der Seite **Einkaufsreklamation** für einen aktiven Rückgabevorgang in einer leeren Zeile, erzeugen Sie einen negativen Eintrag für den Austauschartikel, indem Sie einen negativen Betrag in das Feld **Menge** eingeben.  
2. Wählen Sie die **Negative Zeilen übertragen** Aktion aus.
3. Füllen Sie auf der Seite **Negative Verkaufszeile verschieben** die Felder nach Bedarf aus.
4. Wählen Sie die Schaltfläche **OK** aus. Wenn Sie diese Stapelverarbeitung ausführen, wird die negative Zeile (für den Austauschartikel) aus der Verkaufsreklamation gelöscht und auf einer neuen **Verkaufsauftrag**-Seite eingefügt. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>So erstellen Sie reklamationsbezogene Belege aus einer Verkaufsreklamation
Lassen Sie alle relevanten Verkaufsreklamationsbelege automatisch erstellen, z. B. eine Einkaufsreklamation, eine Ersatzbestellung oder einen neuen Verkaufsauftrag. Dies ist beispielsweise in Fällen nützlich, in denen Sie Artikel mit den Garantien bearbeiten möchten, die von Kreditoren bereitgestellt werden.

1. Auf der Seite **Verkaufsreklamation** für einen aktiven Rückgabevorgang wählen Sie die Aktion **Reklamationsbez. Belege erstellen** aus.
2. Geben Sie im **Kreditorennr.** Feld die Nummer des Kreditors ein, wenn Sie Kreditorenbelege automatisch erstellen möchten.
3. Wenn ein Artikel an den Kreditor zurückgeliefert werden muss, aktivieren Sie das Kontrollkästchen **Eink.-Reklamation erstellen**.
4. Wenn ein Artikel beim Kreditor bestellt werden muss, aktivieren Sie das Kontrollkästchen **Bestellung erstellen**.
5. Wenn ein Auftrag für eine Ersatzlieferung erstellt werden muss, aktivieren Sie das Kontrollkästchen **Verkaufsauftrag erstellen**.

## <a name="to-create-a-restock-charge"></a>So legen Sie eine Wiedereinlagerungsgebühr an
Möglicherweise entscheiden Sie sich dazu, Ihren Debitoren mit einer Wiedereinlagerungsgebühr zu belasten, um die Bearbeitungskosten für die Rücksendung des Artikels abzudecken. Diese Situation könnte z. B. eintreten, wenn der Debitor aus Versehen den falschen Artikel bestellt hatte oder seine Meinung geändert hat, nachdem er den Artikel erhalten hat.

Sie können diesen herabgesetzten Preis als Zu-/Abschlag (Artikel) in einer Gutschrift oder einer Reklamation buchen und ihn der gebuchten Lieferung zuordnen. Nachfolgend wird es für eine Verkaufsreklamation erläutert, aber dieselben Schritte gelten für eine Verkaufsgutschrift zu.

1. Öffnen Sie die Seite **Verkaufsreklamation** für einen aktiven Rückgabevorgang.
2. Geben Sie eine neue Zeile ein, und wählen Sie **Zu-/Abschlag (Artikel)** im Feld **Art**.  
3. Füllen Sie die Felder für jede mögliche Artikelzuschlagszeile aus. Weitere Informationen finden Sie untert [Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md).  

Wenn Sie die Verkaufsreklamation buchen, wird die Wiedereinlagerungsgebühr zu dem entsprechenden Betrag des Verkaufspostens addiert. Auf diese Art können Sie genaue Bestandbewertung führen.  

## <a name="to-create-a-sales-allowance"></a>So erstellen Sie einen Verkaufsrabatt
Sie können einem Debitoren eine Gutschrift mit einem Preisnachlass ausstellen, wenn der Debitor leicht beschädigte Artikel erhalten hat oder die Artikel zu spät geliefert wurden.  
Sie können diesen herabgesetzten Preis als Zu-/Abschlag (Artikel) in einer Gutschrift oder einer Reklamation buchen und ihn der gebuchten Lieferung zuordnen. Nachfolgend wird es für eine Verkaufsreklamation erläutert, aber dieselben Schritte gelten für eine Verkaufsgutschrift.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsgutschriften** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Neu**, um eine neue leere Verkaufsgutschrift zu öffnen.
3. Füllen Sie den Kopf der Gutschrift mit den entsprechenden Informationen über den Debitor aus, dem Sie den Verkaufsrabatt gewähren möchten.  
4. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Art** die Option **Zu-/Abschlag (Artikel)**.  
5.  Geben Sie im Feld **Nr.** den entsprechenden Chargenwert ein.  
     Vielleicht möchten Sie eine spezielle Artikel Zu-/Abschlagsnummer erstellen, um Verkaufsrabatte abzudecken.  
6.  Geben Sie im Feld **Menge** den Wert **1** ein.  
7.  Geben Sie im Feld **VK-Preis** den Betrag des Verkaufsrabattes ein.  
8.  Den Verkaufsrabatt können Sie als Zu-/Abschlag (Artikel) den Artikeln in der gebuchten Lieferung zuweisen. Weitere Informationen finden Sie untert [Verwenden von Artikelzuschlägen für zusätzliche Kosten](payables-how-assign-item-charges.md). Kehren Sie zur Seite **Gutschrift** zurück.  

Wenn Sie die Verkaufsreklamation buchen, wird die Wiedereinlagerungsgebühr zu dem entsprechenden Betrag des Verkaufspostens addiert. Auf diese Art können Sie genaue Bestandbewertung führen.

## <a name="to-combine-return-receipts"></a>Sammelgutschrift für Reklamationen kombinieren
Sie können Rücksendungen zusammenfassen, wenn Ihr Debitor mehrere Artikel zurücksendet, die durch mehrere Verkaufsreklamationen abgedeckt werden.  

Wenn Sie die Artikel in Ihrem Lager erhalten, buchen Sie die entsprechende Verkaufsreklamation als geliefert. Dadurch erzeugen Sie gebuchte Rücksendungen. Dies erstellt gebuchte Rücksendungen.  

Wenn Sie bereit sind, an den Debitoren zu fakturieren, können Sie eine Verkaufsgutschrift anlegen und die gebuchten Rücksendungszeilen automatisch in diesen Beleg kopieren, anstatt jede Verkaufsreklamation einzeln zu fakturieren. Dann können Sie die Verkaufsgutschrift buchen und einfach alle offenen Verkaufsreklamationen auf einmal fakturieren.  

Um Rücksendungen zusammenzufassen, muss das Kontrollkästchen **Sammelversand** auf der Seite **Debitorenkarte** aktiviert sein.  

### <a name="to-manually-combine-return-receipts"></a>So werden Rücksendungen manuell zusammengefasst:  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsgutschrift** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus.  
4. Wählen Sie die **Rücklieferzeilen abrufen** Aktion aus.  
5. Wählen Sie die Rücksendungszeilen aus, die Sie in die Gutschrift einschließen möchten:  

    -   Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.  

    -   Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**.  

6.  Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Gutschrift löschen und die Funktion **Rücksendungszeilen holen** erneut ausführen.  
7.  Buchen Sie die Rechnung.  

### <a name="to-automatically-combine-return-receipts"></a>So werden Rücksendungen automatisch zusammengefasst  
Sie können Rücksendungen automatisch zusammenfassen und haben zudem die Möglichkeit, Gutschriften automatisch zu buchen, indem Sie die Stapelverarbeitung **Sammelgutschrift für Rekl.** verwenden.  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Sammelgutschrift für Rekl.** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Sammelgutschrift für Rekl.** füllen Sie die Felder aus, um die relevanten Rücksendungen auszuwählen.
3. Wählen Sie das Feld **Gutschriften buchen** aus. Wenn nicht, müssen Sie die ausgefüllten Einkaufsgutschriften manuell buchen.
4.  Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>So werden eingegangene und fakturierte Reklamationen entfernt:  
Wenn Rücksendungen auf diese Weise fakturiert werden, bleiben die Rücksendungsaufträge, von denen ausgehend die Rücksendungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.  

Wenn Rücksendungen in einer Gutschrift zusammengefasst und gebucht werden, wird für die gutgeschriebenen Zeilen eine gebuchte Verkaufsgutschrift erstellt. Das Feld **Menge fakturiert** auf der entstehenden Verkaufsreklamation wird ausgehend von der fakturierten Menge aktualisiert.   
1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Erledigte Verkaufsreklamationen löschen** ein und wählen Sie dann den entsprechenden Link aus.  
2.  Wählen Sie im Feld **Kontonummer** Filterfeld an, welche Verkaufsaufträge zu löschen sind.  
3.  Wählen Sie die Schaltfläche **OK** aus.  

Sie können die einzelnen Verkaufsaufträge auch manuell löschen.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]