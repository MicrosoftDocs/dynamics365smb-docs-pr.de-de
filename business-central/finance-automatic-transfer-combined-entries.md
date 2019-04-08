---
title: Automatische Übertragung und kombinierte Posten | Microsoft Docs
description: In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798121"
---
# <a name="automatic-transfer-and-combined-entries"></a>Automatische Übertragung und kombinierte Posten
In der Kostenrechnung können Sie Sachposten in eine Kostenart transferieren, indem Sie eine zusammengefasste Buchung verwenden. Sie können angeben, ob eine Kostenart kombinierte Posten im Feld **Kombinierte Einträge** in der Kostenartdefinition erhalten soll. Die drei Optionen werden in der folgenden Tabelle beschrieben.  

|Posten kombinieren|Beschreibung|  
|---------------------|-----------------|  
|"Keine"|Jeder Sachposten wird einzeln in die entsprechende Kostenart umgelagert.|  
|Tag|Sachposten mit dem gleichen Buchungsdatum werden wie ein Posten in die entsprechende Kostenart umgelagert.|  
|Monat|Alle Sachposten im selben Kalendermonat werden wie ein Posten in die entsprechende Kostenart umgelagert.|  

> [!IMPORTANT]  
>  Wenn Sie das Kontrollkästchen **Automatischer Übertrag vom Buch-Blatt** auf der Seite **Kostenrechnung einrichten** aktiviert haben, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] die Kostenrechnung nach jeder Buchung in der Finanzbuchhaltung aktualisiert. Kombinierte Posten sind nicht möglich.  

## <a name="see-also"></a>Siehe auch  
 [Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)   
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
