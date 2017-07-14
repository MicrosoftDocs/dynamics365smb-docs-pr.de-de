---
title: 'Vorgehensweise: Verwalten von Lieferungen | Microsoft Docs'
description: "Beschreibt, wie Material- und Dienstleistungen für Jobs geliefert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f52fa9545b50038c1d28daa164add07915ef2656
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Verwalten von Projektlieferungen
<a id="how-to-manage-job-supplies" class="xliff"></a>
Die Verwaltung der Projektmittel für Artikel, Services und Aufwendungen ist ein integraler und wichtiger Bestandteil der Ausführung von Projekten. Sie können entweder verfügbaren Lagerbestand verwenden oder projektspezifische Einkäufe mithilfe von Bestellungen und/oder Einkaufsrechnungen durchführen. Beispiel: Bei einem Serviceprojekt für einen Computer wird eine neue Festplatte benötigt. Sie erstellen eine Einkaufsrechnung für den Kauf einer neuen Festplatte und erfassen das Projekt, für das die Festplatte verwendet wird.

Falls für den Verkaufsprozess keine separate Erfassung von physischen Transaktionen erforderlich ist, kann ein Verkauf möglicherweise nur in einer Einkaufsrechnung oder im Fenster **Fibu Buch.-Blatt** verarbeitet werden. Weitere Informationen finden Sie unter [So gehts: Nutzung von Projekten](projects-how-record-job-usage.md).

## Um Artikel oder Services für ein Projekt kaufen
<a id="to-purchase-items-or-services-for-a-job" class="xliff"></a>
Der folgende Ablauf zeigt, wie eine Einkaufsrechnung zum Kauf von Produkten für ein Projekt verwendet wird. Die gleichen Schritte gelten auch, wenn sie eine Bestellung verwenden.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Einkaufsrechnungen** eingeben und den entsprechenden Link auswählen.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
3. Im Feld **Projektnummer** und Feld **Projektaufgabennummer** wählen Sie die Informationen des Projektes aus, für das Sie Artikel oder Services kaufen möchten. Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).

    Den Wert, den Sie im Feld **Projektzeilenart** auswählen, definiert, ob eine Planungszeile erstellt wird, wenn Sie den Verbrauch eines Artikels buchen. Wenn das Feld **Fakturierbar** enthält, dann werden die Projektzeilen erstellt, die bereit sind, um dem Kunden in Rechnung zu stellen. Weitere Informationen finden Sie unter [Gewusst wie: Projekte fakturieren](projects-how-invoice-jobs.md).
4. Wählen Sie die Aktion **Buchen** aus.

## So zeigen Sie den Wert eines Kaufes für ein Projekt
<a id="to-view-the-value-of-purchases-for-a-job" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Jobs** ein und wählen Sie dann den entsprechenden Link aus.
2. Eine relevante Projektkarte öffnen.

    In der **Registerkarte** Inforegister zeigt das Feld **Ausstehende Bestellungen** den gesamten ausstehenden Betrag in Landeswährung, , den gesamten Lagerbestand und die Services für den Kauf von Dokumenten für die Projektaufgabenzeile.  

    Das Feld **Nicht fakturierter Lieferbetrag** zeigt den Wert der Artikel, die mit Verkaufsdokumenten geliefert aber noch nicht fakturiert wurden.  
3. Klicken Sie auf eines der Felder, um das Fenster **Verkaufszeilen** zu öffnen. In diesem Fenster können Sie Informationen aus der Bestellung nachlesen – einschließlich Informationen zu eingegangenen Artikeln oder Ressourcen.

## Projektbezogene Aufwendung buchen
<a id="to-post-a-job-related-expense" class="xliff"></a>
Wenn Sie die außerordentlichen oder einmalige Projektausgaben verursachen, können Sie das Fenster **Projekt Buch.-Blatt** verwenden, um diese direkt auf das Konto des entsprechenden Projekts zu buchen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Job Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.  
2. Erstellen Sie eine neue Zeile, und geben Sie Informationen zur Aufwendung einschließlich Informationen zur **Projektnummer.** und zur **Projektaufgabennummer** ein.  
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

