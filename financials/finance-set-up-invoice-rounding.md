---
title: Einrichten der Rechnungsrundung | Microsoft Docs
description: "Sie können Rechnungsbeträge beim Erstellen von Rechnungen runden. Darüber hinaus muss die Rechnungsrundung möglicherweise aufgrund lokaler Vorgaben oder üblicher Vorgehensweisenauf eine bestimmte Weise erfolgen – beispielsweise auf einen Betrag, der durch 0,05 teilbar ist."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-invoice-rounding"></a>Einrichten der Rechnungsrundung
Wenn Sie beim Erstellen von Rechnungen Rechnungsbeträge runden müssen, können Sie die automatische Rundungsfunktion verwenden. Nach dem Runden einer Rechnung wird eine zusätzliche Zeile mit dem Rundungsbetrag eingefügt, die zusammen mit den anderen Rechnungszeilen gebucht wird.

> [!NOTE]  
>  Aufgrund gesetzlicher Vorgaben oder üblicher Vorgehensweisen muss die Rechnungsrundung möglicherweise auf eine bestimmte Weise erfolgen – beispielsweise auf einen Betrag, der durch 0,05 teilbar ist.  
  
Zum Verwenden der automatischen Rechnungsrundung müssen folgende Aktionen ausgeführt werden:  
  
* Geben Sie die Sachkonten zum Buchen der Rundungsdifferenzen an.  
* Richten Sie Regeln für das Runden von Rechnungen in Mandanten- und Fremdwährung an.  
* Aktivieren Sie die Funktion.  
  
> [!NOTE]  
>  Zusätzlich zu den Rechnungsrundungsfeatures besteht auch die Möglichkeit, Beträge in Rechnungen mithilfe der Stückpreisrundung und der Betragsrundung zu runden.  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Sachkonten für Rechnungsrundungsdifferenzen einrichten
Um die automatische Rundungsfunktion zu nutzen, müssen Sie Sachkonten einrichten, auf die Rundungsdifferenzen gebucht werden. Bevor Sie dies tun können, müssen Sie die MwSt.-Produktbuchungsgruppen einrichten. Weitere Informationen finden Sie unter [MwSt. einrichten](finance-setup-vat.md).  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Sachkonten für Rechnungsrundungsdifferenzen einrichten:  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kontenplan** ein und wählen dann den zugehörigen Link aus.  
2. Richten Sie das Konto im Fenster **Kontenplan** ein, und benennen Sie es mit **Rechnungsrundung** oder mit einem ähnlichen Namen. [!INCLUDE[d365fin](includes/d365fin_md.md)]Die Anwendung verwendet den Kontonamen als Text in gerundeten Rechnungen.  
3. Abhängig davon, ob Sie Mehrwertsteuer oder Verkaufssteuer verwenden, wählen Sie in den Feldern **Steuer-Produktbuchungsgruppe** oder **MwSt.-Produktbuchungsgruppe** eine Buchungsgruppe für Rundungsbeträge aus. Es empfiehlt sich, eine neuen Gruppencode einzurichten, der für die Rechnungsrundung verwendet werden kann.
4. Lassen Sie die Felder **Buchungsart** und **Steuer-Produktbuchungsgruppe** oder **MwSt.-Produktbuchungsgruppe** leer. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
Jetzt können Sie das Rechnungsrundungskonto den Buchungsgruppen auf der Seite **Kreditorenbuchungsgruppen** zuordnen.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Rundungsregeln für Fremdwährungen und lokale Währungen einrichten
Damit Sie die automatische Rechnungsrundungsfunktion verwenden können, müssen Sie Rundungsregeln für Fremdwährungen und lokale Währungen einrichten.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Einrichten von Rundungsregeln für Fremdwährungen  
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.  
2. Füllen Sie auf der Seite **Währungen** die Fremdwährung aus, um die **Währungskarte** zu öffnen, und füllen Sie dann die Felder **Betragsrundungspräzision**, **Stückpreisrundungspräzision**, **Rechnungsrundungspräzision** und **Rechnungsrundungsmethode** aus.
  
### <a name="to-set-up-rounding-for-your-local-currency"></a>Einrichten der Rundung für Ihre lokale Währung
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Finanzbuchhaltungs-Einrichtung:** ein und wählen dann den zugehörigen Link aus.  
2. Füllen Sie auf der Seite **Finanzbuchhaltungs-Einrichtung:** auf dem Inforegister **Allgemein** die Felder **Rechnungsrundungspräz.** und **Rechnungsrundungsmethode** aus.  

## <a name="activate-the-invoice-rounding-function"></a>Aktivieren der Rechnungsrundungsfunktion  
Damit die Anwendung Einkaufs- und Verkaufsrechnungen automatisch gerundet werden, müssen Sie die Rechnungsrundungsfunktion aktivieren. Beachten Sie, dass Sie die Rechnungsrundung einzeln für Verkaufsrechnungen und Einkaufsrechnungen aktivieren können.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debitoren & Verkauf Einrichtung** oder **Kreditoren & Einkauf Einrichtung** ein und wählen dann den zugehörigen Link aus.  
2. Markieren Sie im Inforegister **Allgemein** das Kontrollkästchen **Rechnungsrundung**.  
  
## <a name="see-also"></a>Siehe auch  
[Verkaufsrechnung](sales-how-invoice-sales.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)
