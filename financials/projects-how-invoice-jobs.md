---
title: Erstellen Sie eine Projekt-Verkaufsrechnung, um ein Projekt zu fakturieren| Microsoft Docs
description: "Beschreibt, wie Kunden für Jobausgaben als Jobfortschritt Rechnung gestellt wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9367dc5875b687b95076efffb3b0df2019332651
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-invoice-jobs"></a>Vorgehensweise: Fakturieren
Im Laufe des Projekts können Projektkosten wie Ressourcenverbrauch, Material oder projektbezogene Einkäufe anfallen. Diese Transaktionen werden im weiteren Verlauf des Projekts auf das Projekt Buch.-Blatt gebucht. Dabei ist es wichtig, dass alle Kosten im Projekt Buch.-Blatt erfasst werden, bevor die Rechnung an den Debitor erstellt wird.

Sie können das gesamte Projekt im Fenster **Projektaufgabenzeilen** fakturieren, oder Sie fakturieren lediglich ausgewählte Vertragszeilen im Fenster **Projektplanzeilen**. Die Fakturierung kann erfolgen, wenn das Projekt abgeschlossen ist, oder in bestimmten Intervallen während der Projektlaufzeit gemäß eines Fakturierungsplans.

> [!NOTE]  
>   Wenn Sie **Verrechenbar** im Feld **Projekt-Zeilenart** auf den Verkaufsbelegen für projektbezogene Einkäufe auswählen, werden Projektplanzeilen, die bereit sind, an den Kunden zu fakturieren, erstellt. Weitere Informationen finden Sie unter [So geht's: Verwalten von Projekt-Material](projects-how-manage-project-supplies.md).

## <a name="to-create-and-post-a-job-sales-invoice"></a>Verkaufsrechnung für ein Projekt erstellen und buchen
Sie können eine Rechnung für ein Projekt oder für eine oder mehrere Projektunteraktivitäten für einen Debitor erstellen, wenn entweder die zu fakturierende Arbeit abgeschlossen ist oder das Datum für die Fakturierung basierend auf einem Fakturierungsplan erreicht ist.

Vom Fenster **Projekte** können Sie keinen Debitor fakturieren, indem Sie das Projekt auswählen, und dann die Aktion **Projekt-Verkaufsrechnung erstellen** auswählen. Der folgende Ablauf zeigt, wie eine Stapelverarbeitung verwendet wird, um mehrere Projekte zu fakturieren.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projektverkaufsrechnungen** erstellen ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Legt Filter fest, wenn Sie die Projekte einschränken möchten, die die Stapelverarbeitung verarbeiten soll.
4. Wählen Sie die Schaltfläche **OK**, um die Rechnung zu erstellen.  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a>Mehrere Projektverkaufsrechnungen aus Projektplanungszeilen erstellen
Sie können eine Rechnung aus Projektplanungszeilen erstellen, und dabei die Menge des Artikels, der Ressource oder des Sachkontos angeben, die Sie fakturieren möchten.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Ein relevantes Projekt öffnen.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. In einer Projektplanungszeile im Feld **In Rechnung zu übertragende Menge** geben Sie die Menge des Artikels, der Ressource, Sachkontoart ein, die fakturiert werden soll.  
5. Wählen Sie die Aktion **Verkaufsrechnung erstellen**.
6. Im Fenster **Projekt-Verkaufsrechnung erstellen** geben Sie das Buchungsdatum an und ob Sie eine neue Rechnung erstellen oder diese Rechnung einer bestehenden Rechnung hinzufügen möchten.
7. Wählen Sie die Schaltfläche **OK** aus.  

    In der Projektplanungszeile im Feld **In Rechnung übertragene Menge** können Sie die Menge anzeigen.
8. Im Fenster **Projektplanungszeilen** wählen Sie Die Aktion **Verkaufsrechnungen/Gutschrift** aus.

    Das Fenster **Verkaufsrechnung** wird geöffnet und zeigt die Menge an, die Sie zum Fakturieren in die Rechnung übertragen haben.  
9. Nehmen Sie die zusätzlichen Änderungen vor, und wählen Sie dann die Aktion **Buchen**.

> [!NOTE]  
>   Das obige Verfahren dient zum Erstellen, Prüfen und Buchen einer projektbezogenen Verkaufsgutschrift.

## <a name="to-calculate-and-post-job-completion-entries"></a>Berechnen und Buchen von Projekt-Abschlussposten
Nachdem alle Aktivitäten für ein Projekt – einschließlich Buchung des Verbrauchs und Fakturierung – abgeschlossen wurden, muss das Projekt aktualisiert werden, damit es den **Status** **Abgeschlossen** erhält. Dann stornieren Sie alle WIPs, die in der Finanzbuchhaltung gebucht wurde.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein offenes Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Feld **Status** **Abgeschlossen**.
4. Folgen Sie den Hilfeschritten, um WIP zu berechnen und zu buchen. Alternativ folgen Sie den Schritten 5 und 6, um dies manuell zu tun.  
5. Wählen Sie die Aktion **WIP berechnen** aus.
6. Geben Sie im Fenster **WIP für Projekt berechnen** die notwendigen Felder ein.  

     Die WIP-Projektposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.  
7. Wählen Sie die Aktion **WIP nach Sachkonten Projekt** aus.
8. Füllen Sie im Fenster **WIP nach Sachkonten Projekt buchen** aus und füllen Sie die Felder wie erforderlich aus.  

     Die WIP-Hauptbuchungsposten, die beim Ausführen der Stapelverarbeitung erstellt wurden, weisen nun ein Häkchen im Feld **Auftrag abgeschlossen** auf, um anzugeben, dass es sich hierbei um Abschlussposten handelt.

## <a name="see-also"></a>Siehe auch
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

