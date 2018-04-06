---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: "FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc45bf06ab5d12cf393d48b7b1c295db28f56b3b
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="enable-picking-items-by-fefo"></a>Aktiveren der Kommissionierung von Artikeln nach FEFO
FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.  

 Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:  

-   Der Artikel muss eine Serien-/Chargennummer haben.  
-   Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-spezifische Verf.** oder das Feld **Chargennr.-spezifische Verf.** aktiviert werden.  
-   Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.  
-   Das Kontrollkästchen **Kommissionierung erforderlich** auf der Lagerortkarte muss aktiviert sein.  
-   Das Kontrollkästchen **Gemäß FEFO kommissionieren** auf der Lagerortkarte muss aktiviert sein.  
-   Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.  

 Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.  

> [!NOTE]  
>  Wenn einige serien-/chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.  

 Weisen zwei Artikel mit Serien-/Chargennummer dasselbe Ablaufdatum aus, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus. Sind die Serien- oder Chargennummern identisch, wählt die Anwendung den Artikel aus, der zuerst registriert wurde.  

> [!NOTE]  
>  -   Werden Artikel mit Serien-/Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.  
> -   Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder im Fenster **Lagerbestandsumlagerung** oder im Fenster **Lagerplatzumlagerungsvorschlag**, indem das Feld **Von Lagerplatz** leer gelassen wird.  
> -   Wenn das Feld **Fixes Ablaufdatum** ausgewählt ist, werden nur Artikel, die nicht abgelaufen sind, in die Kommissionierung einbezogen. Dies gilt auch dann, wenn Sie die Kommissionierung gemäß FEFO nicht verwenden.  

## <a name="see-also"></a>Siehe auch  
[Kommissionieren von Artikeln](warehouse-pick-items.md)   
[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

