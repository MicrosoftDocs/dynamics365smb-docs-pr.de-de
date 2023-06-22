---
title: Erstellen von Rechnungen oder Gutschriften für Serviceleistungen
description: 'Erfahren Sie, wie Sie mit Business Central nahtlos Servicerechnungen und Gutschriften für Ihre Dienstleistungen erstellen können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# <a name="create-service-invoices-or-credit-memos" />Erstellen Sie eine Servicerechnung oder eine Servicegutschrift.
Die einfache Fakturierung von Serviceaufträgen ist ein zentrales Feature von [!INCLUDE[prod_short](includes/prod_short.md)] [!INCLUDE[prod_short](includes/prod_short.md)] kann auch so eingerichtet werden, dass ein Servicetechniker im Feld eine Rechnung für einen Service erstellen kann, der nicht mit einem Vertrag oder Auftrag verbunden ist. Richten Sie [!INCLUDE[prod_short](includes/prod_short.md)] alternativ so ein, dass Sie Serviceverträge regelmäßig in Rechnung stellen. Im Fakturierungsintervall wird für jeden Vertrag festgelegt, wie oft fakturiert wird.

## <a name="to-invoice-several-service-contracts" />So stellen Sie mehrere Serviceverträge in Rechnung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicevertragsrechnungen erstellen** ein, und wählen Sie dann den entsprechenden Link.  
2. Geben Sie die anzuwendenden Filter ein.  
3. Geben Sie hier das **Buchungsdatum**, das als Buchungsdatum in der erstellten Servicerechnung verwendet werden soll.  
4. Geben Sie im Feld **Fakturierung bis Datum** das Datum ein, bis zu dem Sie Verträge fakturieren möchten. Die Stapelverarbeitung wird Verträge mit den nächsten Rechnungsdaten bis zu diesem Datum berücksichtigen.  
5. Klicken Sie im Feld **Aktion** auf **Rechnungen erstellen**.  
6. Klicken Sie auf **OK**, um die Servicerechnung(en) zu erstellen.  
  
Sie können einen Servicevertrag auch direkt auf der Seite **Servicevertrag** fakturieren, wenn das Rechnungsdatum des Vertrages vor dem Arbeitsdatum liegt.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page" />So fakturieren Sie einen Servicevertrag aus der Seite "Servicevertrag"
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceverträge** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Servicevertrag aus, den Sie fakturieren möchten, und öffnen Sie die Vertragskarte.  
3. Wählen Sie die Aktion **Servicerechnung erstellen** aus. 
4. Klicken Sie auf **Ja**, um die Servicerechnungen zu erstellen.  
  
  > [!NOTE]  
  > Es ist nicht möglich, eine Servicerechnung für einen Servicevertrag zu erstellen, wenn das Feld **Status für Änderungen** den Wert **Offen** hat.  

## <a name="to-post-an-invoice-from-a-service-order" />So buchen Sie eine Rechnung von einem Serviceauftrag
Das folgende Verfahren beschreibt, wie der Teil des Service festgelegt wird, der dem Debitor in Rechnung gestellt werden soll.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Serviceauftrag, den Sie öffnen möchten, und öffnen Sie die Auftragskarte.  
3. Wählen Sie die Aktion **Servicezeilen**.  
4. Suchen Sie im nach den entsprechenden Posten, und geben Sie im Feld **Zu fakturieren** die Mengen an, die Sie dem Debitor in Rechnung stellen möchten.  
  
   > [!NOTE]  
   > Sie können dem Debitor den erfassten Service entweder teilweise oder insgesamt in Rechnung stellen. Bei einer Gesamtrechnung für den Debitor muss der Wert im Feld **Zu fakturieren** dem Wert im Feld **Menge** entsprechen. Sie können eine Gesamtrechnung zusammen mit einer Gesamtlieferung buchen, und Sie können eine Gesamtrechnung für eine bereits gebuchte Gesamtlieferung buchen, die zuvor weder fakturiert noch verbraucht wurde.  
   >  
   > Wenn Sie eine Teilrechnung buchen, können Sie die zu fakturierende Menge auf zwei Arten angeben. Wenn Sie den Service mit der Option **Lieferung und Rechnung** buchen möchten, muss der Wert im Feld **Zu fakturieren** dem Wert im Feld **Zu liefern** entsprechen. Wenn Sie eine bereits gebuchte Lieferung fakturieren möchten, darf die zu fakturierende Menge nicht größer als der Wert im Feld **Menge geliefert** sein.  
  
5. Wählen Sie **Buchen** und dann **Rechnung** oder **Liefern und fakturieren** aus. Weitere Informationen zu diesen Optionen, siehe [Servicemanagement buchen](service-service-posting.md).  
  
 Die ausgewählte Servicezeile wird gebucht. Sie können mehrere Servicezeilen gleichzeitig buchen, indem Sie diese auswählen und **Buchen** auswählen. Stellen Sie in diesem Fall sicher, dass Sie alle erforderlichen Informationen in die zu buchenden Zeilen eingegeben haben.  
  
 Wenn Sie den Auftrag mit der Option **Rechnung** buchen, erstellt die Anwendung eine gebuchte Servicerechnung zusammen mit den entsprechenden Posten und aktualisiert die jeweiligen Felder in den Servicezeilen des Auftrags. Darüber hinaus aktualisiert die Anwendung die zuvor gebuchten Lieferungsbelege mit den fakturierten Mengen. Wenn Sie die Buchungsoption **Liefern und fakturieren** wählen, erstellt die Anwendung außerdem eine gebuchte Lieferung.

## <a name="to-create-a-service-invoice-manually" />So erstellen Sie eine Servicerechnung manuell
Wenn Sie einen Serviceauftrag mit der Option **Rechnung** oder **Liefern und fakturieren** buchen, wird automatisch eine Servicerechnung gebucht. Es kann jedoch erforderlich sein, eine Rechnung zu erstellen, die weder mit einem Servicevertrag noch mit einem Serviceauftrag verknüpft ist. In diesem Verfahren wird beschrieben, wie eine Rechnung zu dem Zeitpunkt erstellt wird, zu dem der Debitor den Service erhält.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicerechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Servicerechnung.  
3. Füllen Sie die **Felder Nr.** Feld  
  
    > [!NOTE]  
    >  Wenn Sie Nummernserien für Servicerechnungen auf der Seite **Service Einrichtung** eingerichtet haben, wählen Sie die <kbd>Eingabetaste</kbd>, um die nächste verfügbare Servicerechnungsnummer auszuwählen.  
  
4. Klicken Sie im Feld **Debitorennr.** Feld geben Sie die Debitorennummer ein. Wählen Sie den relevanten Debitoren aus der Liste.  
  
    Die Debitorenfelder werden mit Informationen aus der Karte **Debitor** gefüllt.  
  
5. Geben Sie ein Datum in das Feld **Buchungsdatum** ein. Dieses Datum erscheint in den gebuchten Posten. In dieses Feld wird automatisch das aktuelle Arbeitsdatum eingetragen. Sie können dieses Datum jedoch manuell ändern.  
6. Füllen Sie das Feld **Belegdatum** aus. Das hier eingegebene Datum wird auf der gedruckten Rechnung angegeben und zum Berechnen des Fälligkeitsdatums verwendet.  
7. Füllen Sie die Servicezeilen der Rechnung aus. Füllen Sie die Felder **Art**, **Nr.** und **Menge** aus, um Artikel, Ressourcen und Kosten für Servicearbeiten zu erfassen. 

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders" />So erstellen Sie eine Rechnung, die gebuchte Lieferzeilen aus einem oder mehreren Serviceaufträgen kombiniert
Es kann der Fall sein, dass Sie eine Servicerechnung für einen Service erstellen müssen, der bereits aus einem oder aus mehreren Serviceaufträgen geliefert, aber noch nicht fakturiert oder verbraucht wurde. Sie können die Rechnungszeilen anhand der ausgewählten gebuchten Lieferungszeilen für einen bestimmten Debitor automatisch ausfüllen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicerechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Erstellen Sie Zeilen für gelieferte, aber noch nicht fakturierte Services. Alternativ können Sie die **Lieferzeilen abrufen** Aktion verwenden, um gebuchte Lieferungszeilen der Rechnung hinzuzufügen.  
4. Buchen Sie die Servicerechnung.  
  
 Die gebuchte Servicerechnung sowie die entsprechenden Posten werden erstellt. Die zuvor gebuchten Warenausgangsbelege werden mit den fakturierten Mengen und die entsprechenden Mengen in den Servicezeilen der ursprünglichen Aufträge aktualisiert.  

## <a name="to-create-a-service-credit-memo" />So erstellen Sie eine Servicegutschrift
Eine Servicegutschrift wird normalerweise verwendet, wenn ein Debitor einen Artikel zurücksendet. Sie kann aber auch als Entschädigung für einen Debitor und als Korrektur einer fehlerhaften Rechnung verwendet werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicegutschriften** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Die Felder **Buchungsdatum** und **Belegdatum** zeigen ein Arbeitsdatum an. Bei Bedarf können Sie dieses ändern.    
4. Geben Sie in die Gutschriftszeilen Informationen über die Artikel ein, die zurückgeschickt oder entfernt wurden, oder die Entschädigung, die Sie dem Debitor gewähren möchten.  

## <a name="see-also" />Siehe auch
[So buchen Sie Servicerechnungen](service-how-to-post-service-orders.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Servicebuchung](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
