---
title: So geben Sie Dimensionen für den Inventurauftrag ein
description: Nachdem Sie einen Inventurauftrag erstellt haben, können Sie Dimensionen für diesen Auftrag eingeben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: 6fee80132614c0eda8159d88342c564b291f3e97
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300187"
---
# <a name="enter-dimensions-for-physical-inventory-orders"></a>So geben Sie Dimensionen für den physischen Inventurauftrag ein
Nachdem Sie einen Inventurauftrag erstellt haben, können Sie Dimensionen für diesen Auftrag eingeben.  

Die Anwendung unterscheidet zwischen Dimensionen für den Inventurauftragskopf und Dimensionen für die Inventurauftragszeilen. Die Dimensionen für den Inventurauftragskopf sind ein Muster für die Dimensionen der Inventurauftragszeilen. Jedes Mal, wenn (manuell oder automatisch) eine neue Inventurauftragszeile erstellt wird, überträgt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] die Dimensionen aus dem Kopf in die neue Zeile.  

Aus diesem Grund sollten die Inventurauftragszeilen erst erstellt werden, nachdem die Dimensionen für den Inventurauftragskopf vollständig eingegeben wurden. Sie können die Dimensionen für jede Inventurauftragszeile manuell ändern. Zum Buchen verwendet [!INCLUDE[d365fin](../../includes/d365fin_md.md)] die Dimensionen der Inventurauftragszeile.  

## <a name="to-enter-dimensions-for-a-physical-inventory-order"></a>So geben Sie Dimensionen für den Inventurauftrag ein  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Inventurauftrag aus, für den Sie eine Inventurerfassung erstellen möchten, klicken Sie auf Aktionen und anschließend auf **Bearbeiten**.  
3.  Wählen Sie die Aktion **Dimensionen** aus.  
4.  Auf der Seite **Dimensionssatzposten bearbeiten** geben Sie die Dimensionen im Inventurauftragskopf ein.  
5.  Erstellen Sie eine neue Inventurauftragszeile, und geben Sie die Artikelnummer ein.  
6.  Wählen Sie die Aktion **Position** und dann die Aktion **Dimensionen**.  
7.  Auf der Seite **Dimensionssatzposten bearbeiten** geben Sie die Dimensionen im Inventurauftragskopf ein.  

## <a name="see-also"></a>Siehe auch  
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)   
 [So buchen Sie physische Inventuraufträge](how-to-post-physical-inventory-orders.md)   
 [Dimensionssatz-Eintrags-Übersicht](../../design-details-dimension-set-entries-overview.md)
