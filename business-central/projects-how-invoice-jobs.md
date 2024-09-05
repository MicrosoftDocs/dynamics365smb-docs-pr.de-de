---
title: 'Erstellen Sie eine Projektverkaufsrechnung, um ein Projekt abzurechnen'
description: 'Beschreibt, wie Sie Debitoren die Ausgaben für ein Projekt in Rechnung stellen können, wenn ein Projekt fortschreitet und sich die Kosten summieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
---
# <a name="invoice-projects"></a>Projekte abrechnen

Im Laufe des Projekts können Projektkosten wie Ressourcenverbrauch, Material oder projektbezogene Einkäufe anfallen. Diese Transaktionen werden im weiteren Verlauf des Projekts auf das Projekt Buch.-Blatt gebucht. Dabei ist es wichtig, dass alle Kosten im Projekt Buch.-Blatt erfasst werden, bevor die Rechnung an den Debitor erstellt wird.
Die Fakturierung kann erfolgen, wenn das Projekt abgeschlossen ist, oder in bestimmten Intervallen während der Projektlaufzeit gemäß eines Fakturierungsplans.

Sie können folgende Rechnungen stellen:

* Mehrere Projekte verwenden ein  **Projekt: Verkaufsrechnung erstellen** Aufgabe.
* Ganze Projekte, einige Projekte innerhalb eines Projekts oder einzelne Projektplanungszeilen mithilfe der entsprechenden Aktion auf den Projektseiten.
* Kombinieren Sie mehrere Projektplanungszeilen aus unterschiedlichen Projekten in einer einzigen Verkaufsrechnung mit der Aktion  **Projektplanungszeilen abrufen**  auf der Seite  **Verkaufsrechnung** .

## <a name="to-create-multiple-project-sales-invoices"></a>So erstellen Sie mehrere Projektverkaufsrechnungen

Sie können eine Rechnung für ein Projekt oder für eine oder mehrere Projektunteraktivitäten für einen Debitor erstellen, wenn entweder die zu fakturierende Arbeit abgeschlossen ist oder das Datum für die Fakturierung basierend auf einem Fakturierungsplan erreicht ist.

Der folgende Ablauf zeigt, wie eine Stapelverarbeitung verwendet wird, um mehrere Projekte zu fakturieren.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Projekt – Verkaufsrechnung erstellen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Legt Filter fest, wenn Sie die Projekte einschränken möchten, die die Stapelverarbeitung verarbeiten soll.
4. Wählen Sie die Schaltfläche **OK**, um die Rechnung zu erstellen.  

Sie können erstellte Rechnungen auf der Seite  **Verkaufsrechnungen**  überprüfen und veröffentlichen.

> [!NOTE]
> Alternativ können Sie einem Kunden eine Rechnung stellen, indem Sie das Projekt auswählen und dann die Aktion  **Projektverkaufsrechnung erstellen**  wählen, oder die Aktion  **Verkaufsrechnung erstellen**  in den Projektaufgaben verwenden.

## <a name="to-create-and-post-project-sales-invoice-from-project-planning-lines"></a>So erstellen und buchen Sie eine Projektverkaufsrechnung aus Projektplanzeilen

Sie können eine Rechnung aus Projektplanungszeilen erstellen, und dabei die Menge des Artikels, der Ressource oder des Sachkontos angeben, die Sie fakturieren möchten.

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie ein entsprechendes Projekt.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. In einer Projektplanungszeile im Feld **In Rechnung zu übertragende Menge** geben Sie die Menge des Artikels, der Ressource, Sachkontoart ein, die fakturiert werden soll.  
5. Wählen Sie die Aktion **Verkaufsrechnung erstellen**.
6. Auf der Seite **In Verkaufsrechnung für Projekt übertragen** geben Sie das Buchungsdatum an und ob Sie eine neue Rechnung erstellen oder diese Rechnung einer bestehenden Rechnung hinzufügen möchten.
7. Wählen Sie die Schaltfläche **OK** aus.  
8. Auf der Seite **Projektplanungszeilen** wählen Sie die Aktion **Verkaufsrechnungen/Gutschrift** aus.

    Die Seite **Verkaufsrechnung** wird geöffnet und zeigt die Menge an, die Sie zum Fakturieren in die Rechnung übertragen haben.
9. Nehmen Sie die zusätzlichen Änderungen vor, und wählen Sie dann die Aktion **Buchen**.

> [!NOTE]  
> Das obige Verfahren dient zum Erstellen, Prüfen und Buchen einer projektbezogenen Verkaufsgutschrift.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Einem Debitoren mehrere Projektaufgaben in Rechnung stellen

Sie können Ihren Rechnungsstellungsprozess vereinfachen, indem Sie eine Rechnung für mehrere Projekte an einen Debitoren senden. Fügen Sie Projektplanungszeilen aus mehreren Projekten auf einmal einer Verkaufsrechnung hinzu. Dieser Vorgang ähnelt dem Erstellen einer Verkaufsrechnung aus einer Projektplanungszeile und der Eingabe eines Werts in das Feld **An Verkaufsrechnungsnr. anfügen**.

Hier ist eine Übersicht über den Prozess.

1. Erstellen Sie einen neuen Verkaufsauftrag, und füllen Sie das Feld **Verk. an Deb.-Nr.** aus Feld Füllen Sie bei Bedarf auch die Felder **Rechnung an Debitor Nr.** und **Währungscode** aus.
2. Klicken Sie im Inforegister **Zeilen** und wählen die Aktion **Projektplanzeilen abrufen**. Auf der Seite **Projektplanzeilen abrufen** werden abrechenbare Projektplanungszeilen aus Projekten für den Verk. an Debitor, die Rechnung an den Debitor und die Rechnungswährung angezeigt, bei denen die in Rechnung zu stellende Menge mehr als null beträgt. 
3. Wählen Sie die Zeilen aus, die Sie der Rechnung hinzufügen möchten, und wählen Sie anschließend **OK** aus.

Wiederholen Sie diese Schritte, wenn Sie einen weiteren Satz Projektplanungszeilen hinzufügen möchten. Sie können die Rechnung oder ihre Zeilen auch löschen und von vorne beginnen.

> [!NOTE]
> Es gibt einige Einschränkungen:
>
> * Die Aktion **Projektplanzeilen abrufen** ist für Verkaufsaufträge oder Verkaufsangebote nicht verfügbar.
> * Sie können nicht nach **Neuer Lief. an Code** oder **Kontaktnr.** filtern Felder.


## <a name="see-also"></a>Siehe auch

[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
