---
title: Verwalten von Projektmitteln
description: 'Beschreibt die verschiedenen Möglichkeiten, den Vorrat und Kauf von Material und Dienstleistungen für Projekte zu verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Verwalten von Projektmitteln

Sie sollten die Verwaltung der Projektmittel für Artikel, Services und Aufwendungen ist ein integraler und wichtiger Bestandteil aller Projekte. Sie können entweder verfügbaren Lagerbestand verwenden oder projektspezifische Einkäufe mithilfe von Bestellungen und/oder Einkaufsrechnungen durchführen. Beispiel: Bei einem Serviceprojekt für einen Computer wird eine neue Festplatte benötigt. Sie erstellen eine Einkaufsrechnung für den Kauf einer neuen Festplatte und erfassen das Projekt, bei dem diese verwendet wird.

Falls für den Verkaufsprozess keine separate Erfassung von physischen Transaktionen erforderlich ist, können Sie einen Verkauf auf der Seite **Fibu Buch.-Blätter Projekt** verarbeiten. Weitere Informationen finden Sie unter [So buchen Sie eine projektbezogene Ausgabe](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## So kaufen Sie Artikel oder Services für ein Projekt

Der folgende Ablauf zeigt, wie eine Einkaufsrechnung zum Kauf von Produkten für ein Projekt verwendet wird. Die gleichen Schritte gelten auch, wenn sie eine Bestellung verwenden.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).
3. Wählen Sie im Feld **Projektnr.** und in den Feldern **Projektaufgabennr.** wählen Sie die Informationen des Projektes aus, für das Sie Artikel oder Services kaufen möchten. Verwenden Sie die Personalisierungstools, wenn ein Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

    Den Wert, den Sie im Feld **Projektzeilenart** auswählen, definiert, ob eine Planungszeile erstellt wird, wenn Sie den Verbrauch eines Artikels buchen. Wenn das Feld **Fakturierbar** enthält, dann werden die Projektplanungszeilen erstellt, die bereit sind, um dem Debitoren in Rechnung zu stellen. Weitere Informationen finden Sie unter [Projekte fakturieren](projects-how-invoice-jobs.md).
4. Wählen Sie die Aktion **Buchen**.

## So zeigen Sie den Wert eines Kaufes für ein Projekt an

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie eine relevante Projektkarte.

    Auf dem Inforegister **Aufgaben** zeigt das Feld **Ausstehende Bestellungen** den gesamten ausstehenden Betrag in Landeswährung, , den gesamten Lagerbestand und die Services für den Kauf von Dokumenten für die Projektaufgabenzeile.  

    Das Feld **Nicht fakturierter Lieferbetrag** zeigt den Wert der Artikel, die mit Verkaufsdokumenten geliefert aber noch nicht fakturiert wurden.  
3. Klicken Sie auf eines der Felder, um die Seite **Verkaufszeilen** zu öffnen. Auf dieser Seite können Sie Informationen aus dem Auftrag nachlesen – einschließlich Informationen zu eingegangenen Artikeln oder Services.

## Projektbezogene Ausgabe buchen

Wenn Sie außerordentliche oder einmalige Projektausgaben verursachen, können Sie die Seite **Projekt Buch.-Blatt** verwenden, um diese direkt auf das Konto des entsprechenden Projekts zu buchen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Fibu Buch.-Blätter Projekt** ein und wählen Sie dann den entsprechenden Link aus.  
2. Erstellen Sie eine neue Zeile, und geben Sie Informationen zur Aufwendung einschließlich Informationen zur **Projektnr.** und zur **Projektaufgabennummer** ein.  
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

## Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
