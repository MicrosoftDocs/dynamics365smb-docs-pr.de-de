---
title: "Erstellen Sie Rechnungen für Services | Microsoft Docs"
description: "Erfahren Sie, wie Sie Rechnungen erstellen, sodass Sie für Ihren Service bezahlt werden."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ee0dc8f0f44e9bb62fc87caf85eaf92d438abe6
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-invoices-or-credit-memos"></a>Gewusst wie: Erstellen Sie eine Servicerechnung oder eine Servicegutschrift.
Die einfache Fakturierung von Serviceaufträgen ist ein zentrales Feature von [!INCLUDE[d365fin](includes/d365fin_md.md)] Sie können Debitoren jederzeit eine Rechnung schicken oder in regelmäßigen Abständen Rechnungen erstellen.  
  
Eine direkte Erstellung von Rechnungen ist im Fenster **Servicevertrag** möglich. Das System kann auch so eingerichtet werden, dass ein Servicetechniker im Feld eine Rechnung für den Service erstellen kann, der nicht mit einem Vertrag oder Auftrag verbunden ist.  

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>So fakturieren Sie einen Servicevertrag aus der Seite "Servicevertrag"   
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Servicevertrags-Rechnungen erstellen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie die anzuwendenden Filter ein.  
3. Geben Sie hier das **Buchungsdatum**, das als Buchungsdatum in der erstellten Servicerechnung verwendet werden soll.  
4. Geben Sie im Feld **Fakturierung bis Datum** das Datum ein, bis zu dem Sie Verträge fakturieren möchten. Die Stapelverarbeitung wird Verträge mit den nächsten Rechnungsdaten bis zu diesem Datum berücksichtigen.  
5. Klicken Sie im Feld **Aktion** auf **Rechnungen erstellen**.  
6. Klicken Sie auf **OK**, um die Servicerechnung(en) zu erstellen.  
  
  > [!NOTE]  
  >  Es ist nicht möglich, eine Servicerechnung für einen Servicevertrag zu erstellen, wenn das Feld **Status für Änderungen** den Wert **Offen** hat.  
  
## <a name="to-post-an-invoice-from-a-service-order"></a>So buchen Sie eine Rechnung von einem Serviceauftrag  
Das folgende Verfahren beschreibt, wie der Teil des Service festgelegt wird, der dem Debitor in Rechnung gestellt werden soll.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceaufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie den Serviceauftrag, den Sie öffnen möchten, und öffnen Sie die Auftragskarte.  
3. Wählen Sie die Aktion **Servicezeilen**.  
4. Suchen Sie im nach den entsprechenden Posten, und geben Sie im Feld  **Zu fakturieren** die Mengen an, die Sie dem Debitor in Rechnung stellen möchten.  
  
   > [!NOTE]  
   >  Sie können dem Debitor den erfassten Service entweder teilweise oder insgesamt in Rechnung stellen. Bei einer Gesamtrechnung für den Debitor muss der Wert im Feld **Zu fakturieren** dem Wert im Feld **Menge** entsprechen. Sie können eine Gesamtrechnung zusammen mit einer Gesamtlieferung buchen, und Sie können eine Gesamtrechnung für eine bereits gebuchte Gesamtlieferung buchen, die zuvor weder fakturiert noch verbraucht wurde.  
   >   
   >  Wenn Sie eine Teilrechnung buchen, können Sie die zu fakturierende Menge auf zwei Arten angeben. Wenn Sie den Service mit der Option **Lieferung und Rechnung** buchen möchten, muss der Wert im Feld **Zu fakturieren** dem Wert im Feld **Zu liefern** entsprechen. Wenn Sie eine bereits gebuchte Lieferung fakturieren möchten, darf die zu fakturierende Menge nicht größer als der Wert im Feld **Menge geliefert** sein.  
  
5. Wählen Sie **Buchen** und dann **Rechnung** oder **Liefern und fakturieren** aus. Weitere Informationen zu diesen Optionen, siehe [Servicemanagement buchen](service-service-posting.md).  
  
 Die ausgewählte Servicezeile wird gebucht. Sie können mehrere Servicezeilen gleichzeitig buchen, indem Sie diese auswählen und **Buchen** auswählen. Stellen Sie in diesem Fall sicher, dass Sie alle erforderlichen Informationen in die zu buchenden Zeilen eingegeben haben.  
  
 Wenn Sie den Auftrag mit der Option **Rechnung** buchen, erstellt die Anwendung eine gebuchte Servicerechnung zusammen mit den entsprechenden Posten und aktualisiert die jeweiligen Felder in den Servicezeilen des Auftrags. Darüber hinaus aktualisiert die Anwendung die zuvor gebuchten Lieferungsbelege mit den fakturierten Mengen. Wenn Sie die Buchungsoption **Liefern und fakturieren** wählen, erstellt die Anwendung außerdem eine gebuchte Lieferung.

## <a name="to-create-a-service-invoice-manually"></a>So erstellen Sie eine Servicerechnung manuell  
Wenn Sie einen Serviceauftrag mit der Option **Rechnung** oder **Liefern und fakturieren** buchen, wird automatisch eine Servicerechnung gebucht. Es kann jedoch erforderlich sein, eine Rechnung zu erstellen, die weder mit einem Servicevertrag noch mit einem Serviceauftrag verknüpft ist. In diesem Verfahren wird beschrieben, wie eine Rechnung zu dem Zeitpunkt erstellt wird, zu dem der Debitor den Service erhält.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicerechnung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Servicerechnung.  
3. Füllen Sie die **Felder Nr.** Feld  
  
    > [!NOTE]  
    >  Wenn Sie Nummernserien für Servicerechnungen im Fenster **Service Einrichtung** eingerichtet haben, drücken Sie die Eingabetaste, um die nächste verfügbare Servicerechnungsnummer auszuwählen.  
  
4. Klicken Sie im Feld **Debitorennr.** Feld geben Sie die Kundennummer ein. Wählen Sie den relevanten Debitoren aus der Liste.  
  
    Die Debitorenfelder werden mit Informationen aus der Karte **Debitor** gefüllt.  
  
5. Geben Sie ein Datum in das Feld **Buchungsdatum** ein. Dieses Datum erscheint in den gebuchten Posten. In dieses Feld wird automatisch das aktuelle Arbeitsdatum eingetragen. Sie können dieses Datum jedoch manuell ändern.  
6. Füllen Sie das Feld **Belegdatum** aus. Das hier eingegebene Datum wird auf der gedruckten Rechnung angegeben und zum Berechnen des Fälligkeitsdatums verwendet.  
7. Füllen Sie die Servicezeilen der Rechnung aus. Füllen Sie die Felder **Art**, **Nr.** und **Menge** aus, um Artikel, Ressourcen und Kosten für Servicearbeiten zu erfassen. 

## <a name="to-invoice-posted-shipment-lines"></a>So fakturieren Sie gebuchte Lieferzeilen  
Es kann der Fall sein, dass Sie eine Servicerechnung für einen Service erstellen müssen, der bereits aus einem oder aus mehreren Serviceaufträgen geliefert, aber noch nicht fakturiert oder verbraucht wurde. Sie können die Rechnungszeilen anhand der ausgewählten gebuchten Lieferungszeilen für einen bestimmten Debitor automatisch ausfüllen.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicerechnung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Erstellen Sie Zeilen für gelieferte, aber noch nicht fakturierte Services. Alternativ können Sie die **Lieferzeilen abrufen** Aktion verwenden, um gebuchte Lieferungszeilen der Rechnung hinzuzufügen.  
4. Buchen Sie die Servicerechnung.  
  
 Die gebuchte Servicerechnung sowie die entsprechenden Posten werden erstellt. Die zuvor gebuchten Warenausgangsbelege werden mit den fakturierten Mengen und die entsprechenden Mengen in den Servicezeilen der ursprünglichen Aufträge aktualisiert.  

## <a name="to-create-a-combined-invoice"></a>So erstellen Sie Sammelrechnungen  
Mithilfe dieses Verfahrens können Sie dem Debitor die in verschiedenen Serviceaufträgen enthaltenen Services in Rechnung stellen. Rechnungszeilen werden für Artikel, Ressourcenzeiten oder Kosten, die bereits aus verschiedenen Serviceaufträgen geliefert, aber noch nicht fakturiert wurden, erstellt.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicerechnung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die **Versandzeilen abrufen** Aktion aus. Im Fenster **Servicelieferungszeilen abrufen** werden alle gelieferten, aber noch nicht fakturierten Zeilen für den angegebenen Debitor angezeigt.  
4. Wählen Sie die Zeilen aus, für die der Service fakturiert wird, und Sie dann **OK**, um die Servicelieferungszeilen der Rechnung hinzuzufügen.  

## <a name="to-create-a-service-credit-memo"></a>So erstellen Sie eine Servicegutschrift  
Eine Servicegutschrift wird normalerweise verwendet, wenn ein Debitor einen Artikel zurücksendet. Sie kann aber auch als Entschädigung für einen Debitor und als Korrektur einer fehlerhaften Rechnung verwendet werden.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Servicevertragsgutschriften** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Die Felder **Buchungsdatum** und **Belegdatum** zeigen ein Arbeitsdatum an. Bei Bedarf können Sie dieses ändern.    
4. Geben Sie in die Gutschriftszeilen Informationen über die Artikel ein, die zurückgeschickt oder entfernt wurden, oder die Entschädigung, die Sie dem Debitor gewähren möchten.  

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: So buchen Sie Servicerechnungen](service-how-to-post-service-orders.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Servicebuchung](service-service-posting.md)  

