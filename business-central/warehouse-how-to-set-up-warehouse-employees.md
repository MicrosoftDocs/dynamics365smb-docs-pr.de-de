---
title: Lagermitarbeiter einrichten
description: 'Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmäßigen Lagerorten zugeordnet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# Lagermitarbeiter einrichten

Sie müssen jeden Benutzer, der Lagertätigkeiten ausführt, als Lagermitarbeiter einrichten und ihm einen Standardlagerort zuweisen. [!INCLUDE [prod_short](includes/prod_short.md)] filtert Lageraktivitäten zum Standardstandort des Mitarbeiters. Sie können nur die Lagertätigkeiten am Standort ausführen. Sie können einem Benutzer anderen Standorten zuweisen. Sie können auf diese Standorte zugreifen, aber keine Aktivitäten dort ausführen.

## So richten Sie die Lagermitarbeiter ein:  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie das Feld **Benutzer-ID** und dann den Benutzer aus, der als Lagermitarbeiter hinzugefügt werden soll. Wählen Sie die Schaltfläche **OK** aus.  
4. Geben Sie im Feld **Lagerortcode** den Code des Lagerorts ein, an dem der Lagermitarbeiter arbeitet.  
5. Aktivieren Sie die Umschaltung **Standard**, um den Lagerort als einzigen Lagerort zu definieren, an dem der Mitarbeiter Lageraktivitäten ausführen kann.  
6. Wiederholen Sie diese Schritte, um Lagerorten weitere Mitarbeiter zuzuordnen oder um andere Lagerorte bestehenden Lagermitarbeitern zuzuordnen.  

> [!TIP]
> Sie können auch die Aktion **Mich als Lagermitarbeiter hinzufügen** verwenden, um sich schnell zur Liste der Lagermitarbeiter hinzuzufügen. Dies ist beispielsweise nützlich, wenn Sie die Funktionen testen.

## Siehe verwandte [Microsoft Schulungen](/training/modules/get-started-warehouse-management/)

## Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
