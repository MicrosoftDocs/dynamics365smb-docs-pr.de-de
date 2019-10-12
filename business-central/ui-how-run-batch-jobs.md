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
ms.date: 10/01/2019
ms.author: solsen
ms.openlocfilehash: 2387356fd3e80e5020b4d2e4857280dd4b99788a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315204"
---
# <a name="run-batch-jobs-and-xmlports"></a>Führen Sie Stapeljobs und XMLports aus
Bei einer Stapelverarbeitung handelt es sich um einen Vorgang, bei dem Daten stapelweise verarbeitet werden, beispielsweise bei der Stapelverarbeitung **Wechselkurs regulieren**. Es stehen Stapelverarbeitungen für periodische Buchhaltungsaktivitäten zur Verfügung, beispielsweise zum Abschließen der GuV am Ende eines Geschäftsjahrs. Viele Stapelverarbeitungen dienen zum Ausführen von Berechnungsaufgaben – beispielsweise zum Berechnen von Zuschlägen, Wechselkursregulierungen oder VK-Preisen.

Eine Stapelverarbeitung gleicht einem Bericht, die Ergebnisse der Stapelverarbeitung werden jedoch zur direkten Aktualisierung der Informationen verwendet, anstatt diese lediglich auszugeben.

Sie können planen, wann ein Stapeljob ausgeführt wird. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

## <a name="to-run-a-batch-job"></a>So führen Sie eine Stapelverarbeitung aus:
1. Zum Öffnen der Anforderungsseite für die relevanten Stapelverarbeitung wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie den Namen der Stapelverarbeitung ein, und wählen dann den zugehörigen Link aus.
2. Ist für die Stapelverarbeitung ein Inforegister vom Typ **Optionen** verfügbar, füllen Sie die Felder aus, um die Stapelverarbeitung zu konfigurieren.
3. Die Seite kann mehrere Inforegister mit Filtern enthalten, mit denen sich die in die Stapelverarbeitung einzubeziehenden Daten einschränken lassen. Sie können Kriterien in die vorgeschlagenen Filter eingeben oder weitere Filter hinzufügen.
4. Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.

## <a name="see-also"></a>Siehe auch
[Sortieren, Durchsuchen und Filtern von Listen](ui-enter-criteria-filters.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
