---
title: Aufgaben im Hintergrund und wiederkehrend ausführen
description: Konfigurieren Sie die Synchronisierung von Daten zwischen Business Central und Shopify im Hintergrund.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 4a67f6fc58fb8b158563ce58baab55e7fda2ccb1
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728599"
---
# <a name="run-tasks-in-the-background"></a>Aufgaben im Hintergrund ausführen

Es ist effizient, einige Aufgaben gleichzeitig und automatisiert auszuführen. Sie können solche Aufgaben im Hintergrund ausführen und auch einen Zeitplan festlegen, wann diese Aufgaben automatisch ausgeführt werden sollen. Um Aufgaben im Hintergrund auszuführen, werden zwei Modi unterstützt:

- Manuell ausgelöste Aufgaben werden sofort über **Aufgabenwarteschlangenposten** geplant.
- Wiederkehrende Aufgaben werden in **Aufgabenwarteschlangenposten** eingeplant.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Aufgaben im Hintergrund für einen bestimmten Shop ausführen

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") , geben Sie den Namen für den **Shopify-Shop** ein, und wählen Sie den Namen des Shops aus der Liste aus.
2. Wählen Sie den Shop, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Aktivieren Sie das Kontrollkästchen **Hintergrundsynchronisationen zulassen**.

Wenn die Synchronisierungsaktion ausgelöst wird, wird nun nicht mehr eine Aufgabe im Vordergrund ausgeführt, sondern Sie werden aufgefordert zu warten. Wenn dieser abgeschlossen ist, können Sie mit der nächsten Aktion fortfahren. Die Aufgabe wird als **Aufgabenwarteschlangenposten** erstellt und startet sofort, ohne zu blockieren.

## <a name="to-schedule-recurring-tasks"></a>So planen Sie wiederkehrende Aufgaben

Sie können die folgenden wiederkehrenden Aktivitäten so planen, dass sie automatisiert ausgeführt werden. Erfahren Sie mehr über die Planung von Aufgaben unter [Auftragswarteschlange](../admin-job-queues-schedule-tasks.md).

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

> [!NOTE]
> Einige Elemente können durch mehrere Aufgaben aktualisiert werden, z.B. wenn Sie Bestellungen importieren. Je nach Einstellung in der **Shopify Shop Card** importiert und aktualisiert das System auch Debitor- und/oder Produktdaten. Denken Sie daran, die gleiche Kategorie der Auftragswarteschlange zu verwenden, um Konflikte zu vermeiden.

## <a name="see-also"></a>Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)  
