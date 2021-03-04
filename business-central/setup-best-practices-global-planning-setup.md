---
title: Bewährte Vorgehensweisen für globale Planung einrichten | Microsoft Docs
description: Das Inforegister "Planung" auf der Seite "Herstellung einrichten" enthält eine Reihe von Feldern, die globale Regeln für die Beschaffungsplanung definieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f70e720cd8639038f7c06de7f6b2f338652e8e4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757767"
---
# <a name="setup-best-practices-global-planning-setup"></a>Bewährte Einrichtungsmethoden: Globale Planungseinrichtung
Das Inforegister **Planung** auf der Seite **Herstellung einrichten** enthält eine Reihe von Feldern, die globale Regeln für die Beschaffungsplanung definieren.  

 Die folgende Tabelle enthält bewährte Methoden zum Einrichten von ausgewählten globalen Planungsparameterfeldern. Für weitere Informationen zu einem Feld klicken Sie auf den Link in der Spalte **Feldeinstellungen**.  

|Feldeinstellungen|Bewährte Vorgehensweisen|Bemerkung|  
|-----------------|-------------------|-------------|  
|Absatzpl. pro Lagerort verw.|Wählen Sie diese Option aus, wenn Sie für bestimmte Lagerorte eine Planung haben.||  
|Komponenten von Lagerort|Wenn Artikel nicht als Lagerhaltungsdaten definiert sind, wählen Sie den Lagerortcode Ihres Auffülllagerorts aus.|Dies gilt auch, wenn Sie nur den Bestellvorschlag verwenden.|  
|Leerer Überlauflevel|Wählen Sie **Standardberechnung zulassen** wenn Sie von Microsoft Dynamics NAV 5.0 oder frrüher migrieren.|Verwenden Sie dies nur, wenn alle oder einige Artikel den Minimalbestand übersteigen dürfen.|  
|Standardtoleranzperiode|Die Einstellung muss zwischen 1D und 5D liegen.<br /><br /> Bei Neulingen in der Planung in [!INCLUDE[prod_short](includes/prod_short.md)] legen Sie eine längere Periode fest.|Wenn Benutzer mit den verschiedenen Gründen für Ereignismeldungen vertraut sind, dann kürzen Sie die Toleranzperiode, um mehr Änderungsvorschläge zu erlauben.|  
|Toleranzmenge %|Legen Sie sie zwischen 5 und 20 Prozent der Losgröße des Artikels fest.||  

## <a name="see-also"></a>Siehe auch  
 [Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)   
 [Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]