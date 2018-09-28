---
title: "Bewährte Vorgehensweisen für globale Planung einrichten | Microsoft Docs"
description: "Das Inforegister **Planung** im Fenster **Herstellung einrichten** enthält eine Reihe von Feldern, die globale Regeln für die Beschaffungsplanung definieren."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5f9eda3b9bb2482a446370058c7bd4a503dde6ee
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-global-planning-setup"></a>Bewährte Einrichtungsmethoden: Globale Planungseinrichtung
Das Inforegister **Planung** im Fenster **Herstellung einrichten** enthält eine Reihe von Feldern, die globale Regeln für die Beschaffungsplanung definieren.  

 Die folgende Tabelle enthält bewährte Methoden zum Einrichten von ausgewählten globalen Planungsparameterfeldern. Für weitere Informationen zu einem Feld klicken Sie auf den Link in der Spalte **Feldeinstellungen**.  

|Feldeinstellungen|Bewährte Vorgehensweisen|Bemerkung|  
|-----------------|-------------------|-------------|  
|Absatzpl. pro Lagerort verw.|Wählen Sie diese Option aus, wenn Sie für bestimmte Lagerorte eine Planung haben.||  
|Komponenten von Lagerort|Wenn Artikel nicht als Lagerhaltungsdaten definiert sind, wählen Sie den Lagerortcode Ihres Auffülllagerorts aus.|Dies gilt auch, wenn Sie nur den Bestellvorschlag verwenden.|  
|Leerer Überlauflevel|Wählen Sie **Standardberechnung zulassen** wenn Sie von Microsoft Dynamics NAV 5.0 oder frrüher migrieren.|Verwenden Sie dies nur, wenn alle oder einige Artikel den Minimalbestand übersteigen dürfen.|  
|Standardtoleranzperiode|Die Einstellung muss zwischen 1D und 5D liegen.<br /><br /> Bei Neulingen in der Planung in [!INCLUDE[d365fin](includes/d365fin_md.md)] legen Sie eine längere Periode fest.|Wenn Benutzer mit den verschiedenen Gründen für Ereignismeldungen vertraut sind, dann kürzen Sie die Toleranzperiode, um mehr Änderungsvorschläge zu erlauben.|  
|Toleranzmenge|Legen Sie sie zwischen 5 und 20 Prozent der Losgröße des Artikels fest.||  

## <a name="see-also"></a>Siehe auch  
 [Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)   
 [Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

