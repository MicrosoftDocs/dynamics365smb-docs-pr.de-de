---
title: Aufgaben im Hintergrund ausführen
description: Konfigurieren Sie die Synchronisierung von Daten zwischen Business Central und Shopify im Hintergrund.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768120"
---
# <a name="run-tasks-in-the-background"></a>Aufgaben im Hintergrund ausführen

Es ist effizient, einige Aufgaben gleichzeitig und automatisiert auszuführen. Sie können solche Aufgaben im Hintergrund ausführen und auch einen Zeitplan festlegen, wann diese Aufgaben automatisch ausgeführt werden sollen. Um Aufgaben im Hintergrund auszuführen, werden zwei Modi unterstützt:

- Manuell ausgelöste Aufgaben werden sofort über **Warteschlangeneinträge** geplant.
- Wiederkehrende Aufgaben werden in **Warteschlangeneinträge** geplant.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Aufgaben im Hintergrund für einen bestimmten Shop ausführen

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie den Namen für den **Shopify-Shop** ein, und wählen Sie den Namen des Shops aus der Liste aus.
2. Wählen Sie den Shop aus, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Aktivieren Sie den Umschalte **Hintergrundsynchronisierungen zulassen**.

Wenn die Synchronisierungsaktion ausgelöst wird, wird nun nicht mehr eine Aufgabe im Vordergrund ausgeführt, sondern Sie werden aufgefordert zu warten. Wenn dieser abgeschlossen ist, können Sie mit der nächsten Aktion fortfahren. Die Aufgabe wird als **Warteschlangenposten** erstellt und startet sofort und ohne Blockierung.

## <a name="to-schedule-recurring-tasks"></a>So planen Sie wiederkehrende Aufgaben

Sie können die folgenden wiederkehrenden Aktivitäten so planen, dass sie automatisiert ausgeführt werden. Weitere Informationen zum Planen von Aufgaben finden Sie unter [Aufgabenwarteschlange](../admin-job-queues-schedule-tasks.md).

|Aufgabe|Objekt|
|------|------------|
|**Aufträge von Shopify synchronisieren**|Bericht 30104 Synchronisierungsaufträge von Shopify|
|**Shopify-Aufträge verarbeiten**|Bericht 30103 Shopify-Verkaufsaufträge erstellen|
|**Lieferungen mit Shopify synchronisieren**|Bericht 30109 Lieferung mit Shopify synchronisieren|
|**Produkte und/oder Preise synchronisieren**|Bericht 30108 Shopify – Produkte synchronisieren|
|**Lagerbestand synchronisieren**|Bericht 30102 Lagerbestand mit Shopify synchronisieren|
|**Bilder synchronisieren**|Bericht 30107 Shopify – Bilder synchronisieren|
|**Debitoren synchronisieren**|Bericht 30100 Shopify – Debiroten synchronisieren|
|**Zahlungen synchronisieren**|Bericht 30105 Shopify – Zahlungen synchronisieren|

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Konnektor für Shopify](get-started.md)  
