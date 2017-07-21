---
title: "Einkaufs-Artikel oder Services für ein Projekt und Vorräte verwalten| Microsoft Docs"
description: Beschreibt, wie die Bereitstellung und den Einkauf des Materials und Servicearten in Projekten verwaltet wird.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 46cae53022ba5d65a370694c9818f52a7bf45525
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-job-supplies"></a>Vorgehensweise: Verwalten von Projektlieferungen
Die Verwaltung der Projektmittel für Artikel, Services und Aufwendungen ist ein integraler und wichtiger Bestandteil der Ausführung von Projekten. Sie können entweder verfügbaren Lagerbestand verwenden oder projektspezifische Einkäufe mithilfe von Bestellungen und/oder Einkaufsrechnungen durchführen. Beispiel: Bei einem Serviceprojekt für einen Computer wird eine neue Festplatte benötigt. Sie erstellen eine Einkaufsrechnung für den Kauf einer neuen Festplatte und erfassen das Projekt, für das die Festplatte verwendet wird.

Falls für den Verkaufsprozess keine separate Erfassung von physischen Transaktionen erforderlich ist, kann ein Verkauf möglicherweise nur in einer Einkaufsrechnung oder im Fenster **Fibu Buch.-Blatt** verarbeitet werden. Weitere Informationen finden Sie unter [So gehts: Nutzung von Projekten](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Um Artikel oder Services für ein Projekt kaufen
Der folgende Ablauf zeigt, wie eine Einkaufsrechnung zum Kauf von Produkten für ein Projekt verwendet wird. Die gleichen Schritte gelten auch, wenn sie eine Bestellung verwenden.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
3. Im Feld **Projektnummer** und Feld **Projektaufgabennummer** wählen Sie die Informationen des Projektes aus, für das Sie Artikel oder Services kaufen möchten. Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).

    Den Wert, den Sie im Feld **Projektzeilenart** auswählen, definiert, ob eine Planungszeile erstellt wird, wenn Sie den Verbrauch eines Artikels buchen. Wenn das Feld **Fakturierbar** enthält, dann werden die Projektzeilen erstellt, die bereit sind, um dem Kunden in Rechnung zu stellen. Weitere Informationen finden Sie unter [Gewusst wie: Projekte fakturieren](projects-how-invoice-jobs.md).
4. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>So zeigen Sie den Wert eines Kaufes für ein Projekt
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Eine relevante Projektkarte öffnen.

    In der **Registerkarte** Inforegister zeigt das Feld **Ausstehende Bestellungen** den gesamten ausstehenden Betrag in Landeswährung, , den gesamten Lagerbestand und die Services für den Kauf von Dokumenten für die Projektaufgabenzeile.  

    Das Feld **Nicht fakturierter Lieferbetrag** zeigt den Wert der Artikel, die mit Verkaufsdokumenten geliefert aber noch nicht fakturiert wurden.  
3. Klicken Sie auf eines der Felder, um das Fenster **Verkaufszeilen** zu öffnen. In diesem Fenster können Sie Informationen aus der Bestellung nachlesen – einschließlich Informationen zu eingegangenen Artikeln oder Ressourcen.

## <a name="to-post-a-job-related-expense"></a>Projektbezogene Aufwendung buchen
Wenn Sie die außerordentlichen oder einmalige Projektausgaben verursachen, können Sie das Fenster **Projekt Buch.-Blatt** verwenden, um diese direkt auf das Konto des entsprechenden Projekts zu buchen.

1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine neue Zeile, und geben Sie Informationen zur Aufwendung einschließlich Informationen zur **Projektnummer.** und zur **Projektaufgabennummer** ein.  
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

