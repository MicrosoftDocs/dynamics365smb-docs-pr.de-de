---
title: "Dimensionssatzposten Übersicht | Microsoft Docs"
description: In diesem Thema wird beschrieben, wie Dimensionssatzposten in Dynamics 365 gespeichert und gebucht werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1113f371caf00b693144d0ea6f74aed49bbbc9df
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="dimension-set-entries-overview"></a>Dimensionssatz-Eintrags-Übersicht
In diesem Thema wird beschrieben, wie Dimensionssatzposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] gespeichert und gebucht werden.  
  
## <a name="dimension-sets"></a>Dimensionssätze  
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  
  
Im folgenden Beispiel wird ein Dimensionssatz gezeigt, der drei Dimensionssatzposten aufweist. Der Dimensionssatz wird durch eine Dimensionssatz-ID, nämlich 108, identifiziert.  
  
|Dimensionssatz-ID|Dimensionscode|Dimensionswertcode|Dimensionswertname|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|BEREICH|70|Nordamerika|  
|108|UNTERNEHMENSGRUPPE|POS1|Start|  
|108|KOSTENSTELLE|VERKAUF|Verkauf|  
  
## <a name="dimension-set-entries"></a>Dimensionssatzposten  
Dimensionssätze werden in der Tabelle als **Dimensionssatzposten** mit derselben Dimensionssatz-ID gespeichert.  
  
![Dimensions-Postenübersicht](media/dimensionentrynav7.png "DimensionEntryNAV7")  
  
Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  
  
Wenn Sie das Fenster **Dimensionssatzeinträge bearbeiten**bearbeiten und schließen, wird eine Prüfung ausgeführt, um festzustellen, ob die Kombination aus Dimensionswerten als Dimensionssatz in der Tabelle existiert. Wenn die Kombination in der Tabelle auftritt, wird die entsprechende Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugeordnet. Andernfalls wird ein neuer Dimensionssatz der Tabelle hinzugefügt, und die neue Dimensionssatz-ID wird der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugeordnet.  
  
## <a name="performance-improvement"></a>Leistungsverbesserung  
Durch das einmalige Speichern von Dimensionssätzen in der Datenbank wird Datenbankplatz beibehalten und die Gesamtleistung verbessert.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md)   
[Designdetails: Tabellenstruktur](design-details-table-structure.md)   
[Designdetails: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
[Designdetails: Codebeispiele von geänderten Mustern in Änderungen](design-details-code-examples-of-changed-patterns-in-modifications.md)   
[Designdetails: Dimensionssatzeinträge](design-details-dimension-set-entries.md)   

