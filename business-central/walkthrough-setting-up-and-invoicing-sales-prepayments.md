---
title: 'Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen | Microsoft Docs'
description: "Vorauszahlungen sind Zahlungen, die vor der finalen Fakturierung fakturiert und auf einen Vorauszahlungsauftrag (Einkauf oder Verkauf) gebucht werden. Sie können z. B. eine Anzahlung vor der Auftragsfertigung von Artikeln oder eine Zahlung vor der Lieferung an einen Debitoren verlangen. Mithilfe der Vorauszahlungsfunktion von Business Central können Sie Anzahlungen von Debitoren fakturieren und einfordern oder Anzahlungen an Kreditoren leisten. Somit können Sie sicherstellen, dass alle Zahlungen mit einer Rechnung ausgeglichen werden."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab76136c7f28e322bbc3b52a0fec354c6c13f3ff
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen
Vorauszahlungen sind Zahlungen, die vor der finalen Fakturierung fakturiert und auf einen Vorauszahlungsauftrag (Einkauf oder Verkauf) gebucht werden. Sie können z. B. eine Anzahlung vor der Auftragsfertigung von Artikeln oder eine Zahlung vor der Lieferung an einen Debitoren verlangen. Mithilfe der Vorauszahlungsfunktion von [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Anzahlungen von Debitoren fakturieren und einfordern oder Anzahlungen an Kreditoren leisten. Somit können Sie sicherstellen, dass alle Zahlungen mit einer Rechnung ausgeglichen werden.  

 Die Vorauszahlungsanforderungen können für einen Debitor, einen Kreditor, für alle Artikel oder für ausgewählte Artikel definiert werden. Nach dem Festlegen der erforderlichen Einstellungen können Vorauszahlungsrechnungen für den berechneten Vorauszahlungsbetrag auf der Grundlage von Aufträgen und Bestellungen generiert werden. Die Standardbeträge auf der Rechnung können Sie je nach Anforderung ändern. Sie haben zum Beispiel auch die Möglichkeit zum Senden weiterer Vorauszahlungsrechnungen, für den Fall, dass dem Auftrag weitere Artikel hinzugefügt wurden.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
 In dieser exemplarischen Vorgehensweise werden folgende Szenarios behandelt:  

-   Einrichten von Vorauszahlungen  
-   Erstellen eines Auftrags, der eine Vorauszahlung erfordert  
-   Erstellen einer Vorauszahlungsrechnung  
-   Korrigieren der Vorauszahlungsanforderungen für einen Auftrag  
-   Ausgleichen von Vorauszahlungen für einen Auftrag  
-   Fakturieren des Endbetrags für einen Auftrag mit Vorauszahlung  

### <a name="roles"></a>Rollen  
 Diese exemplarische Vorgehensweise umfasst Aufgaben für folgende Rollen:  

-   Debitorenbetreuerin (Heike)  
-   Auftragsbearbeiterin (Martha)  
-   Debitorenadministrator (Peter)  

## <a name="story"></a>Hintergrund  
 Heike ist eine Debitorenbetreuerin. In dieser wird festgelegt, welche Debitoren eine Anzahlung leisten müssen, bevor Artikel hergestellt oder geliefert werden. Heike hat [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet, um Vorauszahlungen automatisch zu berechnen.  

 Marta ist eine Verkaufsauftragsbearbeiterin. Wenn ein Debitor eine telefonische Bestellung tätigt, gibt sie die Auftragsdaten in das System ein, während sie mit dem Debitoren telefoniert. Auf diese Weise lassen sich Preise und Zahlungsbedingungen sofort absprechen, und sie hat die Möglichkeit, den Auftrag noch während des Gesprächs mit dem Debitoren anzupassen.  

 Peter arbeitet in der Debitorenabteilung, wo er Rechnungen und Zahlungen bucht.  

 In diesem Szenario richtet Heike basierend auf der Kreditgeschichte Vorauszahlungsanforderungen für den Debitoren Blütenhaus GmbH ein. Sie informiert Martha, wie Aufträge dieses Debitoren gehandhabt werden sollen.  

 Wenn der Debitor anruft, verhandelt Martha mit ihm, bis sie eine Vereinbarung erreichen. Sie kann dann wählen, die Vorauszahlung auf mehrere unterschiedliche Arten zu berechnen.  

 Nachdem Martha die Vorauszahlungsrechnung gesendet hat, bestellt der Debitor einen weiteren Artikel. Martha aktualisiert den Auftrag und erstellt eine zweite Vorauszahlungsrechnung.  

 Peter erfasst die Zahlung des Debitoren und gleicht sie mit den Rechnungen aus. Anschließend sendet er die endgültige Rechnung.  

## <a name="setting-up-prepayments"></a>Einrichten von Vorauszahlungen  
 Die Debitorenbetreuerin Heike richtet das System zur Verarbeitung von Vorauszahlungen für Debitoren ein.  

-   Heike entscheidet sich, für Vorauszahlungen die gleichen Nummernserien zu verwenden wie für die Fakturierung von Verkaufsaufträgen.  
-   Heike richtet das Programm so ein, dass die Notwendigkeit von Vorauszahlungen vor der endgültigen Fakturierung eines Auftrags überprüft wird.  
-   Heike legt Standardwerte für den erforderlichen Vorauszahlungsprozentsatz für bestimmte Artikel und Debitoren fest.  

In den folgenden Verfahren wird beschrieben, wie Sie Heikes Aufgaben ausführen:  

#### <a name="to-set-up-number-series-for-prepayments"></a>So richten Sie Nummernserien für Vorauszahlungen ein  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitoren & Verkauf einrichten** ein, und wählen dann den zugehörigen Link aus.  
2.  Erweitern Sie im Fenster **Verkauf und Erhalt Einr.** das Inforegister **Nummerierung**.  
3.  Vergewissern Sie sich, dass die Nummernserien für gebuchte Vorauszahlungsrechnungen im Feld **Geb. Vorauszahlungs-Rechnungsnr.** und gebuchte Verkaufsrechnungen (**Gebuchte Rechnungsnummern**) sowie die Nummernserien für gebuchte Vorauszahlungsgutschriften (**Geb. Vorauszahlungs-Gutschriftennr.**) und gebuchte Gutschriften (**Gebuchte Gutschriftennr.**) übereinstimmen.  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Lieferungen für nicht geleistete Vorauszahlung sperren  
1.  Aktivieren Sie im Fenster **Debitoren & Verkauf Einr.** auf dem Inforegister **Allgemein** die Option **Vorauszahlung beim Buchen prüfen**.

    Jetzt können Sie einen Auftrag mit nicht bezahltem Vorauszahlungsbetrag nicht liefern oder in Rechnung stellen.  

Heike legt standardmäßig fest, dass für den Debitoren 20000 eine Anzahlung in Höhe von 30 % für alle Aufträge fakturiert werden muss. Daher gibt sie einen Standardvorauszahlungsprozentsatz in der Debitorenkarte ein.  

Heike legt fest, dass für alle Debitoren eine Anzahlung in Höhe von 20 % für den Artikel 1100 fakturiert werden muss. Debitor 20000 verfügt über eine schlechte Zahlungsvergangenheit Daher verlangt sie vom Debitoren 20000 eine Vorauszahlung von 40 % für die Artikel 1100. Im folgenden Beispiel wird gezeigt, wie Sie standardmäßige Vorauszahlungsprozentsätze einrichten.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>So weisen Sie Debitoren und Artikeln Standardvorauszahlungsprozentsätze zu  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitor** ein, und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie das Kartenfenster für Debitor 20000 (Selangorian).
3.  Geben Sie im Feld **Vorauszahlung %** den Wert **30** ein.  
4.  Wählen Sie die Schaltfläche **OK**, um die Debitorenkarte zu schließen.  
5.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
6.  Öffnen Sie die Karte für Debitor 1100.
7.  Wählen Sie die **Vorauszahlungsprozentsätze** Aktion aus.  
8.  Füllen Sie im Fenster **Verkaufsvorauszahlungs-Prozentsätze** zwei Zeilen wie folgt aus.  

    |**Verkaufsart**|**Verkaufscode**|**Artikelnr.**|**Vorauszahlung %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Debitor**|**20000**|**1100**|**40**|  
    |**Alle Debitoren**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Abhängig von Ihrem Land/Ihrer Region müssen Sie einen Steuergruppencode in dem Inforegister **Fakturierung** für Artikel ebenfalls angeben 1000 und 1100 angeben.  

9. Schließen Sie alle Fenster.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Ein Konto für Verkaufsvorauszahlung in der allgemeinen Buchungsmatrix angeben  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Allgemeine Buchungseinrichtung** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Zeile, in der das Feld **Geschäftsbuchungsgruppe** zu **EXPORT** und das Feld **Produktbuchungsgruppe** zu **EINZELHANDEL** festgelegt wurde, und wählen Sie dann auf der Registerkarte Start in der Gruppe Verwalten die Option **Bearbeiten** aus.  
3.  Geben Sie im Fenster **Buchungsmatrixkarte Einricht.** im Inforegister Verkauf im Feld **Verkaufsvorauszahlungs-Konto**das gewünschte Konto an.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Erstellen eines Auftrags, der eine Vorauszahlung erfordert  
 Im folgenden Szenario erstellt Susan aus der Auftragsabwicklung einen Auftrag, während sie mit einem Debitoren spricht. Die Artikel, die der Debitor bestellt, erfordern eine Vorauszahlung, und der Debitor hat in der Vergangenheit einige Male zu spät gezahlt. Daher wurde Martha angewiesen, einen festen Betrag von 2.000 als Vorauszahlung auf dem Auftrag zu benötigen.  

Der Debitor fragt an, 35 % bezahlen zu dürfen; dem kann Martha zustimmen. Daher ändert sie den Auftrag.  

Martha erstellt die Vorauszahlungsrechnung und sendet sie an den Debitoren.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>So erstellen Sie einen Verkaufsauftrag mit einer Vorauszahlung  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Wählen Sie im Feld **Verk. an Deb.-Nr.** Feld **20000**auswählen  
5.  Akzeptieren Sie die angezeigte Warnung zum fälligen Saldo.  
6.  Füllen Sie zwei Verkaufszeilen mit den folgenden Informationen aus.  

    |**Typ**|**Nr.**|**Menge**|  
    |--------------|-------------|------------------|  
    |**Artikel**|**1000**|**1**|  
    |**Artikel**|**1100**|**1**|

    Die Vorauszahlungsfelder in der Verkaufszeile sind standardmäßig ausgeblendet und müssen daher angezeigt werden.  

7. Vergewissern Sie sich, dass das Feld **Vorauszahlung %** in der Zeile mit dem Artikel **1000** den Wert **30** enthält. Der Standardwert wurde aus dem Verkaufskopf von der Debitorenkarte übernommen.  

    Das Feld **Vorauszahlung %** in der Zeile mit dem Artikel **1100** enthält **40**. Dies ist der Prozentsatz, den Sie im Fenster **Verkaufsvorauszahlungs-Prozentsätze** für den Artikel **1100** und den Debitoren **20000** eingegeben haben.  

    Weitere Informationen finden Sie unter [Einrichten von Vorauszahlungen](finance-set-up-prepayments.md).  
8. Wählen Sie die Aktion **Statistik** aus.  
9. Im Inforegister **Vorauszahlung** enthält das Feld **Vorauszahlungszeilenbetrag ohne MwSt.** den Wert **1.560**. Wenn Sie jetzt eine Vorauszahlungsrechnung für den Auftrag erstellen, wird dieser Betrag in der Rechnung angezeigt.  

    In diesem Szenario wurde Martha angewiesen, eine Gesamtvorauszahlung in Höhe von 2000 für den Auftrag vorzuschlagen.  

    > [!IMPORTANT]  
    >  Abhängig von Ihrem Land/Ihrer Region trifft der nächste Schritt möglicherweise nicht zu.  
10. Ändern Sie den Betrag im Feld **Vorauszahlungszeilenbetrag ohne MwSt.** in **2000**, und schließen Sie dann das Fenster.  
11. Überprüfen Sie das Feld **Vorauszahlung %** in den Verkaufszeilen. Der Wert wurde neu berechnet und lautet nun **40.81625**.  

    Die erneute Berechnung beinhaltet alle Zeilen mit einem Vorauszahlungsprozentsatz größer 0.  

    Jetzt fragt der Debitor, ob der Vorauszahlungsprozentsatz auf 35 % festgelegt werden kann. Da Marthas Vorgesetzter genehmigt die Änderung.  

12. Erweitern Sie im Fenster **Verkaufsauftrag** das Inforegister **Vorauszahlung** und geben **35** ein.  
13. In der Warnung, die erscheint, wählen Sie die Schaltfläche **Ja**. Eine Rate von 35 % wird als Vorauszahlungsprozentsatz für den gesamten Auftrag angewendet.  
14. Überprüfen Sie dann, ob die Zeilen entsprechend aktualisiert wurden.  

## <a name="creating-a-prepayment-invoice"></a>Erstellen einer Vorauszahlungsrechnung  
Nachdem sie die korrekten Vorauszahlungswerte im Auftrag eingegeben hat, erstellt Martha die Vorauszahlungsrechnung und sendet sie an den Debitoren.  

#### <a name="to-create-a-prepayment-invoice"></a>So erstellen Sie eine Vorauszahlungsrechnung  

1.  Im Fenster **Verkaufsauftrag** wählen Sie die Aktion **Vorauszahlungsrechnung buchen** aus.  

> [!NOTE]  
>  Martha wählt **Vorauszahlungsrechnung buchen und drucken** und sendet die Rechnung an den Debitoren.  

## <a name="creating-an-additional-prepayment-invoice"></a>Erstellen einer weiteren Vorauszahlungsrechnung  
Am folgenden Tag, ruft der Debitor Martha an, und nimmt Änderungen am Auftrag vor. Der Debitor möchte zwei Exemplare des Artikels 1100. Martha öffnet und aktualisiert die Bestellung, und dann erstellt sie eine zweite Vorauszahlungsrechnung auf dem Auftrag und sendet sie an den Debitoren.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>So erstellen Sie eine weitere Vorauszahlungsrechnung  

1.  Im Fenster **Verkaufsauftrag** wählen Sie die Aktion **Wieder öffnen** aus.  
2.  Geben Sie in der Zeile für den Artikel **1100** im Feld **Menge** den Wert **2** ein.  

    Rollen Sie, um die Vorauszahlungsfelder anzuzeigen. Das Feld **Vorauszahlungszeilenbetrag ohne. MwSt.** enthält jetzt **630**, und das Feld **Fakt. Vorauszahlungsbetrag ohne MwSt.** enthält **315**. Dieses bedeutet, dass ein zusätzlicher Vorauszahlungsbetrag vorhanden ist, der noch nicht fakturiert wurde.  
3.  Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Buchen** **Vorauszahlung**, und wählen Sie dann **Vorauszahlungsrechnung buchen**, um eine Rechnung für den zusätzlichen Vorauszahlungsbetrag zu buchen.  

## <a name="applying-the-prepayments"></a>Ausgleichen der Vorauszahlungen  
Der Debitor bezahlt den Vorauszahlungsbetrag und Peter, der in der Debitorenabteilung arbeitet, registriert die Zahlung und gleicht sie mit den Vorauszahlungsrechnungen aus.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>So gleichen Sie eine Zahlung mit den Vorauszahlungsrechnungen aus  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Buch.-Blätter für den Zahlungseingang** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie ein Buchhaltungsprotokoll mit den folgenden Informationen aus.  

    |Name des Felds|Eingabe|  
    |----------------|-----------|  
    |**Belegart**|**Zahlung**|  
    |**Kontoart**|**Debitor**|  
    |**Kontonummer**|**20000**|  
3. Wählen Sie die Aktion **Posten ausgleichen...** aus.  
4.  Im Fenster **Debitorenpostenausgleich** wählen Sie die erste Vorauszahlungsrechnung und dann auf der Registerkarte Start in der Gruppe Vorgang die Option **Ausgleichs-ID setzen** aus.  
5.  Wiederholen Sie den vorherigen Schritt für die zweite Vorauszahlung.  
6.  Wählen Sie die Schaltfläche **OK** aus.  

    Das Betragsfeld enthält jetzt die Summe der beiden Vorauszahlungsrechnungen.  

7.  Buchen Sie die Buch.-Blattzeile.  

## <a name="invoicing-the-remaining-amount"></a>Fakturieren des Restbetrags  
Peter wurde darüber informiert, dass die Artikel im Auftrag geliefert wurden und der Auftrag fakturiert werden kann. Peter erstellt die Rechnung für den Auftrag.  

#### <a name="to-invoice-the-remaining-amount"></a>So fakturieren Sie den Restbetrag  
1. Öffnen Sie den Verkaufsauftrag.  
2. Wählen Sie die Aktion **Liefern und fakturieren**, und klicken Sie anschließend auf die Schaltfläche **OK**.  

> [!NOTE]  
>  Normalerweise wurde die Lieferung bereits von der Versandabteilung gebucht.  

Peter kann die Historie anzeigen, um sicherzustellen, dass die Verkaufsrechnung wie beabsichtigt erstellt wurde.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Gebuchte Verkaufsrechnungen** ein, und wählen dann den zugehörigen Link aus.  

## <a name="next-steps"></a>Nächste Schritte  
In dieser Demonstration wurde beschrieben, wie Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] zur Verarbeitung von Vorauszahlungen einrichten. Das Einrichten von standardmäßigen Vorauszahlungsprozentsätzen für Debitoren und Artikel wurde erläutert, und Sie haben erfahren, dass zum Berechnen der Vorauszahlungen für einen Auftrag verschiedene Methoden zur Auswahl stehen. Sie haben versucht, dem Auftrag einen Gesamtvorauszahlungsbetrag zuzuweisen, und haben den Vorauszahlungsbetrag vom Programm als Prozentsatz des gesamten Auftrags berechnen lassen.  

Zudem wurden das Buchen einer Vorauszahlungsrechnung, Erstellen einer zweiten Vorauszahlungsrechnung bei einer Änderung des Auftrags und das Buchen der endgültigen Rechnung für den Restbetrag erläutert.  

Die Vorauszahlungsfunktion in [!INCLUDE[d365fin](includes/d365fin_md.md)] erleichtert das Einrichten und Anwenden von Vorauszahlungsregeln für Debitoren und Artikel und ermöglicht es Ihnen, jede Zahlung für eine Rechnung zu buchen.  

## <a name="see-also"></a>Siehe auch  
[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)

