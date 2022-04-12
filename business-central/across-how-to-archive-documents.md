---
title: Archivieren von Einkaufs- und Kaufbelegen
description: Sie können Verkaufs- und Kaufaufträge, Angebote, Rücklieferungen und Rahmenaufträge archivieren, sodass Sie den archivierten Beleg verwenden können, um den Beleg, von dem er archiviert wurde, wiederherzustellen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: 2fc414dcd9a8d9c978ee08eb5d19b960fa21a2d9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511841"
---
# <a name="archive-documents"></a>Beleg archivieren
Sie können Verkaufs- und Einkaufsaufträge, Angebote und Rücklieferungen sowie Rahmenaufträge archivieren, beispielsweise weil Sie eine Kopie eines Dokuments zur späteren Wiederverwendung speichern möchten. Sie können ein Verkaufs- oder Einkaufsbeleg mehrmals archivieren, wobei Sie jedes Mal eine andere archivierte Version speichern.

Für archivierte Verkaufsbelege, bei denen das Original noch existiert und nicht gebucht ist, können Sie die Funktion **Wiederherstellen** verwenden, um das Original mit der archivierten Version des Belegs zu überschreiben. Dies ist nützlich, wenn Sie die Inhalte eines Belegs auf einen früheren Zustand wiederherstellen müssen.

Bei archivierten Dokumenten, bei denen das Original gelöscht ist, können Sie den Inhalt nur durch Kopieren der Daten wiederverwenden, z. B. mit der Funktion **Aus Dokument kopieren**.  

## <a name="to-set-up-automatic-document-archiving"></a>So richten Sie die automatische Archivierung von Belegen ein

Sie können die automatische Archivierung von Verkaufs- und Einkaufsbelegen einrichten – beispielsweise Angebote, Rahmenbestellungen und Aufträge – bevor Sie Belege löschen.

Nachfolgend wird beschrieben, wie die automatische Archivierung von Verkaufsbelegen eingerichtet wird. Die Schritte sind für eine Einkaufsdokumente ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie auf der Seite **Einrichtung Debitoren und Verkauf** die Felder aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Speziell für das Feld **Angebote archivieren** wird in der folgenden Tabelle der Unterschied zwischen den Optionen erläutert.

|Option|Beschreibung|
|------|-----------|
|**Nie**| Verkaufsangebote niemals archivieren, wenn sie gelöscht werden.|
|**Frage**|Wählen Sie diese Option, um den Benutzer zu fragen, ob Verkaufsangebote archiviert werden sollen, wenn sie gelöscht werden.|
|**Immer**|Wählen Sie diese Option, um Verkaufsangebote automatisch zu archivieren, wenn sie gelöscht werden.|

## <a name="to-archive-a-sales-order"></a>Verkaufsauftrag archivieren

Nachfolgend wird beschrieben, wie Sie einen Auftrag archivieren Die Schritte für alle Aufträge, Rahmenaufträge, Reklamationen und Angebote sind ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie einen Verkaufsauftrag für Artikel, die Sie archivierne möchten.  
3. Wählen Sie die **Beleg archivieren**-Aktion aus.

Der Auftrag ist archiviert. Sie können sie auf der Seite **Archivierte Verkaufsaufträge** anzeigen.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>So stellen Sie einen nicht gebuchten Verkaufsauftrag aus dem Archiv wieder her

Die folgende Vorgehensweise beschreibt, wie Sie den Inhalt eines archivierten Verkaufsauftrags zum ursprünglichen Verkaufsauftrag zurück bereitstellen. Dies ist nur möglich, wenn das Originaldokument nicht gebucht wurde. Die Schritte sind für alle Aufträge, Rahmenaufträge, Rücklieferungen und Angebote ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsauftragsarchive** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den archivierten Verkaufsauftrag oder eine Version davon aus, die Sie wiederherstellen möchten, und wählen Sie dann die Aktion **Wiederherstellen** aus.  

Die Inhalte des ursprünglichen Auftrags werden durch die der ausgewählten archivierten Version ersetzt.

## <a name="to-delete-archived-sales-orders"></a>Archivierte Auftragsversionen löschen

Nachfolgend wird beschrieben, wie Sie einen archivierten Auftrag löschen. Die Schritte sind für alle anderen archivierten Einkaufs- und Verkaufsbelege ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsauftragsarchive** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Archivierte Verkaufsauftragsarchive löschen** und wählen Sie dann auf der Seite **Archivierte Verkaufsauftragsarchive löschen** die entsprechenden Filter.  
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch

[Nachverfolgen von Belegzeilen](across-how-to-track-document-lines.md)  
[Verkauf](sales-manage-sales.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
