---
title: Lagermitarbeiter einrichten
description: Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmäßigen Lagerorten zugeordnet werden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7328, 7348
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 668b34e011ec103689b45bdc864a7e726d4d8082
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141925"
---
# <a name="set-up-warehouse-employees"></a>Lagermitarbeiter einrichten

Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmäßigen Lagerorten zugeordnet werden. Durch diese Benutzereinrichtung werden alle Lageraktivitäten innerhalb der Datenbank nach dem Lagerort des Mitarbeiters gefiltert, sodass der Mitarbeiter lediglich Lageraktivitäten am Standardlagerort ausführen kann. Ein Benutzer kann zusätzlichen, nicht standardmäßigen Lagerorten zugeordnet werden, für die der Mitarbeiter zwar Aktivitätszeilen anzeigen, aber keine Aktivitäten ausführen kann.

## <a name="to-set-up-warehouse-employees"></a>So richten Sie die Lagermitarbeiter ein:  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie das Feld **Benutzer-ID** und dann den Benutzer aus, der als Lagermitarbeiter hinzugefügt werden soll. Wählen Sie die Schaltfläche **OK** aus.  
4. Geben Sie im Feld **Lagerortcode** den Code des Lagerorts ein, an dem der Lagermitarbeiter arbeitet.  
5. Aktivieren Sie das Kontrollkästchen **Standard**, um den Lagerort als einzigen Lagerort zu definieren, an dem der Mitarbeiter Lageraktivitäten ausführen kann.  
6. Wiederholen Sie diese Schritte, um Lagerorten weitere Mitarbeiter zuzuordnen oder um nicht standardmäßige Lagerorte bestehenden Lagermitarbeitern zuzuordnen.  

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerverwaltung einrichten](warehouse-setup-warehouse.md) 
[Montageverwaltung](assembly-assemble-items.md)
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]