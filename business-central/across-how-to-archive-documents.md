---
title: Einkaufs- und Verkaufsbelege archivieren | Microsoft Docs
description: "Sie können auch Aufträge oder Bestellungen, Angebote, Reklamationen und Rahmenaufträge archivieren, und Sie können den archivierten Beleg verwenden, um den Beleg neu zu erstellen, dass er aus archiviert wurde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Beleg archivieren
Sie können auch Aufträge oder Bestellungen, Angebote, Reklamationen und Rahmenaufträge archivieren, und Sie können den archivierten Beleg verwenden, um den Beleg neu zu erstellen, dass er aus archiviert wurde.

## <a name="to-set-up-automatic-document-archiving"></a>So richten Sie die automatische Archivierung von Belegen ein  
Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Angebote, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.

Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird. Die Schritte sind für eine Einkaufsdokumente ähnlich.
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Debit&oren && Verkauf Einr.** ein und wählen dann den zugehörigen Link aus.
2. Füllen Sie im Feld **Debitoren & Verkauf Einr.** die folgenden Felder aus:

|Feld|Description|
|-----|-----------|
|**Angebote archivieren**|**Nie**, wenn die Verkaufsangebote beim Löschen niemals archiviert werden sollen. **Frage**, wenn der Benutzer aufgefordert werden soll, auszuwählen, ob Verkaufsangebote beim Löschen archiviert werden sollen. **Immer**, wenn Verkaufsangebote beim Löschen automatisch archiviert werden sollen.|
|**Info zu Rahmenaufträgen**|Wählen Sie diese Option aus, um Rahmenaufträge bei jedem Löschen automatisch zu archivieren.|
|**Arch. Bestellungen und Reklamationen**|Wählen Sie diese Option aus, um Verkaufsaufträge bei jedem Löschen automatisch zu archivieren.|

## <a name="to-archive-a-sales-order"></a>Verkaufsauftrag archivieren
Nachfolgend wird beschrieben, wie Sie einen Auftrag archivieren Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie archivierne möchten.  
3.  Wählen Sie die **Beleg archivieren**-Aktion aus.

Der Auftrag ist archiviert. Sie können sie im Fenster **Archivierte Aufträge** anzeigen. Von hier aus können Sie es verwenden, um den Verkaufsauftrag neu zu erstellen, der archiviert wurde.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Einen Auftrag aus Posten neu erstellen
Nachfolgend wird beschrieben, wie Sie einen Auftrag neu erstellen. Die Schritte für Einkaufsreklamationen, Serviceaufträge und ausgehende Umlagerungsaufträge sind ähnlich.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Auftrag archivieren** ein. Wählen Sie dann den zugehörigen Link aus.
2.  Wählen Sie den zu archivierenden Verkaufsauftrag aus, klicken Sie auf Aktionen und anschließend auf **Wiederherstellen**.  

Der Verkaufsauftrag wird im  **Verkaufsaufträge** Fenster erstellt und hinzugefügt.

## <a name="to-delete-archived-sales-orders"></a>Archivierte Auftragsversionen löschen
Nachfolgend wird beschrieben, wie Sie einen archivierten Auftrag löschen. Die Schritte sind für alle anderen archivierten Einkaufs- und Verkaufsbelege ähnlich.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Archivierte Rahmenbestellungen löschen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Im Fenster **Archivierte Auftragsversionen löschen** wählen Sie den entsprechenden Filter aus.  
3.  Wählen Sie die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Nachverfolgen von Belegzeilen](across-how-to-track-document-lines.md)  
[Verkauf](sales-manage-sales.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

