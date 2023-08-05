---
title: 'Verkaufsrechnungen erstellen, um einen Auftrag zu fakturieren'
description: 'Beschreibt, wie Sie Debitoren die Ausgaben für einen Auftrag in Rechnung stellen können, wenn ein Projekt fortschreitet und sich die Kosten summieren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 06/22/2021
ms.author: edupont
---
# Fakturieren von Projekten

Im Laufe des Projekts können Projektkosten wie Ressourcenverbrauch, Material oder projektbezogene Einkäufe anfallen. Diese Transaktionen werden im weiteren Verlauf des Projekts auf das Projekt Buch.-Blatt gebucht. Dabei ist es wichtig, dass alle Kosten im Projekt Buch.-Blatt erfasst werden, bevor die Rechnung an den Debitor erstellt wird.

> [!NOTE]
> Sie können auch externe Ressourcen erwerben, die nicht mit einem Auftrag verbunden sind, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen. Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).

Sie können das gesamte Projekt auf der Seite **Projektaufgabenzeilen** fakturieren, oder Sie fakturieren lediglich ausgewählte Vertragszeilen auf der Seite **Projektplanzeilen**. Die Fakturierung kann erfolgen, wenn das Projekt abgeschlossen ist, oder in bestimmten Intervallen während der Projektlaufzeit gemäß eines Fakturierungsplans.

> [!NOTE]  
> Wenn Sie **Verrechenbar** im Feld **Projekt-Zeilenart** auf den Verkaufsbelegen für projektbezogene Einkäufe auswählen, werden Projektplanzeilen, die bereit sind, an den Debitoren zu fakturieren, erstellt. Weitere Informationen finden Sie unter [Verwalten von Projekt-Material](projects-how-manage-project-supplies.md).

Sie können auch einem Unternehmen, das nicht der Endkunde ist, eine Rechnung stellen. Manchmal unterscheidet sich die Partei, für die ein Projekt ist, von der Partei, die die Rechnung bezahlt. Auf der **Projekte**-Seite können Sie den Debitor, der von dem Projekt profitieren wird, in den Feldern **Verk. an** angeben und den Rechnungssteller in den Feldern **Rech. an**. 

## So erstellen Sie mehrere Projektverkaufsrechnungen

Sie können eine Rechnung für ein Projekt oder für eine oder mehrere Projektunteraktivitäten für einen Debitor erstellen, wenn entweder die zu fakturierende Arbeit abgeschlossen ist oder das Datum für die Fakturierung basierend auf einem Fakturierungsplan erreicht ist.

Der folgende Ablauf zeigt, wie eine Stapelverarbeitung verwendet wird, um mehrere Projekte zu fakturieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Job Verkaufsrechnung erstellen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Legt Filter fest, wenn Sie die Projekte einschränken möchten, die die Stapelverarbeitung verarbeiten soll.
4. Wählen Sie die Schaltfläche **OK**, um die Rechnung zu erstellen.  

Sie können erstellte Rechnungen im Fenster **Verkaufsrechnungen** überprüfen und buchen.

> [!NOTE]
> Alternativ können Sie einen Debitor fakturieren, indem Sie das Projekt auswählen und anschließend die Aktion **Projektverkaufsrechnung erstellen** auswählen. 

## So erstellen und buchen Sie eine Projektverkaufsrechnung aus Projektplanzeilen

Sie können eine Rechnung aus Projektplanungszeilen erstellen, und dabei die Menge des Artikels, der Ressource oder des Sachkontos angeben, die Sie fakturieren möchten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine relevante Jobkarte.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. In einer Projektplanungszeile im Feld **In Rechnung zu übertragende Menge** geben Sie die Menge des Artikels, der Ressource, Sachkontoart ein, die fakturiert werden soll.  
5. Wählen Sie die Aktion **Verkaufsrechnung erstellen**.
6. Auf der Seite **Projekt-Verkaufsrechnung erstellen** geben Sie das Buchungsdatum an und ob Sie eine neue Rechnung erstellen oder diese Rechnung einer bestehenden Rechnung hinzufügen möchten.
7. Wählen Sie die Schaltfläche **OK** aus.  
8. Auf der Seite **Projektplanungszeilen** wählen Sie Die Aktion **Verkaufsrechnungen/Gutschrift** aus.

    Die Seite **Verkaufsrechnung** wird geöffnet und zeigt die Menge an, die Sie zum Fakturieren in die Rechnung übertragen haben.
9. Nehmen Sie die zusätzlichen Änderungen vor, und wählen Sie dann die Aktion **Buchen**.

> [!NOTE]  
>   Das obige Verfahren dient zum Erstellen, Prüfen und Buchen einer projektbezogenen Verkaufsgutschrift.

## Siehe verwandte [Microsoft Schulungen](/training/paths/post-job-usage-sales/)

## Siehe auch

[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
