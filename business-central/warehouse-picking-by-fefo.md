---
title: So aktivieren Sie die Kommissionierung nach FEFO | Microsoft Docs
description: FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ae07bc4f1d9f348f08f591e5e4341938ec4b5f16
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382204"
---
# <a name="enable-picking-items-by-fefo"></a>Aktiveren der Kommissionierung von Artikeln nach FEFO
FEFO (First-Expired-First-Out) ist eine Sortiermethode, durch die sichergestellt ist, dass die ältesten Artikel mit den frühesten Ablaufdatumsangaben zuerst kommissioniert werden.  

 Diese Funktionen arbeiten nur, wenn die folgenden Kriterien erfüllt sein:  

-   Der Artikel muss eine Serien-/Chargennummer haben.  
-   Bei der Einrichtung des Artikelverfolgungscodes des Artikels muss das Feld **Seriennr.-Verf. Lager** oder das Feld **Chargennr.-Verf. Lager** ausgewählt werden.  
-   Der Artikel muss mit einem Ablaufdatum im Lager gebucht werden.  
-   Das Kontrollkästchen **Kommissionierung erforderlich** auf der Lagerortkarte muss aktiviert sein.  
-   Das Kontrollkästchen **Gemäß FEFO kommissionieren** auf der Lagerortkarte muss aktiviert sein.  
-   Das Kontrollkästchen **Kommissionierung erforderlich** muss auf der Lagerortkarte aktiviert sein.  

 Wenn alle Kriterien erfüllt sein, werden zu kommissionierenden Artikel mit Serien-/Chargennummern bei allen in Kommissionierungen und Lagerplatzumlagerungen mit dem ältesten zuerst sortiert. Ausgenommen sind Artikel mit SN-spezifischer oder chargenspezifischer Verfolgung.  

> [!NOTE]  
> Wenn einige serien-/chargennummerierte Artikel eine spezifische Verfolgung verwenden, werden diese zuerst berücksichtigt und danach werden die verbleibenden unspezifischen Serien-/Chargennummern gemäß FEFO aufgelistet.
<br /><br />
Weisen zwei Artikel mit Serien-/Chargennummer dasselbe Ablaufdatum aufweisen, wählt die Anwendung den Artikel mit der niedrigeren Serien- oder Chargennummer aus.
<br /><br />
Werden Artikel mit Serien-/Chargennummer an Lagerorten kommissioniert, die für die gesteuerte Einlagerung und Kommissionierung eingerichtet sind, werden bei der FEFO-Methode lediglich Mengen aus Lagerplätzen vom Typ *Kommissionierung* kommissioniert.  
<br /><br />
Die Aktivierung der Umlagerungen nach FEFO erfolgt entweder auf der Seite **Lagerbestandsumlagerung** oder auf der Seite **Lagerplatzumlagerungsvorschlag**, indem das Feld **Von Lagerplatz** leer gelassen wird.  
<br /><br />
Wenn das Feld **Fixes Ablaufdatum** ausgewählt ist, werden nur Artikel, die nicht abgelaufen sind, in die Kommissionierung einbezogen. Dies gilt auch dann, wenn Sie die Kommissionierung gemäß FEFO nicht verwenden.

## <a name="see-also"></a>Siehe auch  
[Kommissionieren von Artikeln](warehouse-pick-items.md)   
[Um Artikel für den Warenausgang zu kommissionieren](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Artikel mit der Lagerkommissionierung kommissionieren](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]