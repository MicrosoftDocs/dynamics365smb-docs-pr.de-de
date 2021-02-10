---
title: Erstellen und führen Sie eine Stapelverarbeitung | Microsoft Docs
description: Sie führen Stapelverarbeitungen durch , um Daten zu verarbeiten und Informationen zu aktualisieren, um periodische Buchhaltungsaktivitäten oder Berechnungen durchzuführen.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 04ae13561f44d544d38b04e3a881a0e707b441b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760517"
---
# <a name="run-batch-jobs-and-xmlports"></a>Führen Sie Stapeljobs und XMLports aus
Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**. Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der GuV am Ende eines Geschäftsjahrs. Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.

Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.

Sie können planen, wann ein Stapeljob ausgeführt wird. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

## <a name="to-run-a-batch-job"></a>So führen Sie eine Stapelverarbeitung aus:
1. Um die Anforderungsseite für den entsprechenden Batch-Job zu öffnen, wählen Sie die Seite ![Glühbirne, die das Symbol Tell Me feature](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie den Namen des Batch-Jobs ein und wählen Sie dann den entsprechenden Link.
2. Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.
3. Die Seite kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen. Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.
4. Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.

## <a name="see-also"></a>Siehe auch
[Sortieren, Durchsuchen und Filtern von Listen](ui-enter-criteria-filters.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
