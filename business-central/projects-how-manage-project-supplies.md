---
title: Verwalten von Projektlieferungen
description: 'Beschreibt die verschiedenen Möglichkeiten, den Vorrat und Kauf von Material und Dienstleistungen für Aufträge zu verwalten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="manage-job-supplies"></a>Verwalten von Projektlieferungen
Die Verwaltung der Projektmittel für Artikel, Services und Aufwendungen ist ein integraler und wichtiger Bestandteil der Ausführung von Projekten. Sie können entweder verfügbaren Lagerbestand verwenden oder projektspezifische Einkäufe mithilfe von Bestellungen und/oder Einkaufsrechnungen durchführen. Beispiel: Bei einem Serviceprojekt für einen Computer wird eine neue Festplatte benötigt. Sie erstellen eine Einkaufsrechnung für den Kauf einer neuen Festplatte und erfassen das Projekt, für das die Festplatte verwendet wird.

Falls für den Verkaufsprozess keine separate Erfassung von physischen Transaktionen erforderlich ist, kann ein Verkauf möglicherweise nur in einer Einkaufsrechnung oder auf der Seite **Fibu Buch.-Blatt** verarbeitet werden. Weitere Informationen finden Sie unter [So buchen Sie eine auftragsbezogene Ausgabe](projects-how-manage-project-supplies.md#to-post-a-job-related-expense).

## <a name="to-purchase-items-or-services-for-a-job"></a>Um Artikel oder Services für ein Projekt kaufen
Der folgende Ablauf zeigt, wie eine Einkaufsrechnung zum Kauf von Produkten für ein Projekt verwendet wird. Die gleichen Schritte gelten auch, wenn sie eine Bestellung verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
3. In den Feldern **Projektnr.** und**Projektaufgabennr.** wählen Sie die Informationen des Projektes aus, für das Sie Artikel oder Services kaufen möchten. Verwenden Sie die Personalisierungstools, wenn ein Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

    Den Wert, den Sie im Feld **Projektzeilenart** auswählen, definiert, ob eine Planungszeile erstellt wird, wenn Sie den Verbrauch eines Artikels buchen. Wenn das Feld **Fakturierbar** enthält, dann werden die Projektzeilen erstellt, die bereit sind, um dem Debitoren in Rechnung zu stellen. Weitere Informationen finden Sie unter [Verkaufsrechnungen](projects-how-invoice-jobs.md).
4. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>So zeigen Sie den Wert eines Kaufes für ein Projekt
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine relevante Auftragskarte.

    In der **Registerkarte** Inforegister zeigt das Feld **Ausstehende Bestellungen** den gesamten ausstehenden Betrag in Landeswährung, , den gesamten Lagerbestand und die Services für den Kauf von Dokumenten für die Projektaufgabenzeile.  

    Das Feld **Nicht fakturierter Lieferbetrag** zeigt den Wert der Artikel, die mit Verkaufsdokumenten geliefert aber noch nicht fakturiert wurden.  
3. Klicken Sie auf eines der Felder, um die Seite **Verkaufszeilen** zu öffnen. Auf dieser Seite können Sie Informationen aus dem Auftrag nachlesen – einschließlich Informationen zu eingegangenen Artikeln oder Ressourcen.

## <a name="to-post-a-job-related-expense"></a>Projektbezogene Aufwendung buchen
Wenn Sie die außerordentlichen oder einmalige Projektausgaben verursachen, können Sie die Seite **Projekt Buch.-Blatt** verwenden, um diese direkt auf das Konto des entsprechenden Projekts zu buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Job-Hauptbuch.-Erfassungen** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine neue Zeile, und geben Sie Informationen zur Aufwendung einschließlich  **Projektnr.** und **Projektaufgabennr.** ein.  
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Weitere Informationen
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
