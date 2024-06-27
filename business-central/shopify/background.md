---
title: Aufgaben im Hintergrund und wiederkehrend ausführen
description: Konfigurieren Sie die Synchronisierung von Daten zwischen Business Central und Shopify im Hintergrund.
ms.date: 05/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
ms.custom: bap-template
---

# <a name="run-tasks-in-the-background"></a>Aufgaben im Hintergrund ausführen

Es ist effizient, einige Aufgaben gleichzeitig und automatisiert auszuführen. Sie können solche Aufgaben im Hintergrund ausführen und auch einen Zeitplan festlegen, wann diese Aufgaben automatisch ausgeführt werden sollen. Um Aufgaben im Hintergrund auszuführen, werden zwei Modi unterstützt:

- Manuell ausgelöste Aufgaben werden sofort über **Aufgabenwarteschlangenposten** geplant.
- Wiederkehrende Aufgaben werden in **Aufgabenwarteschlangenposten** eingeplant.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Aufgaben im Hintergrund für einen bestimmten Shop ausführen

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie **Shopify Shop** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie die Synchronisierung im Hintergrund ausführen möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** ein.

Wenn die Synchronisierungsaktion beginnt, wird nicht mehr eine Aufgabe im Vordergrund ausgeführt, sondern Sie werden aufgefordert zu warten. Ist diese abgeschlossen, können Sie mit der nächsten Aktion fortfahren. Die Aufgabe wird als **Aufgabenwarteschlangeneintrag** erstellt und startet sofort.

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
|**Unternehmen synchronisieren**|Bericht 30114 Shopify – Unternehmen synchronisieren (B2B)|
|**Zahlungen synchronisieren**|Bericht 30105 Shopify – Zahlungen synchronisieren|
|**Kataloge synchronisieren**|Bericht 30115 Shopify – Kataloge synchronisieren (B2B)|
|**Kataglogpreise synchronisieren**|Bericht 30116 Shopify – Katalogpreise synchronisieren (B2B)|

> [!NOTE]
> Einige Elemente werden möglicherweise durch mehrere Aufgaben aktualisiert. Wenn Sie zum Beispiel Bestellungen importieren, importiert und aktualisiert das System eventuell je nach der Einstellung auf der Seite **Shopify Shop-Karte** auch Debitor- und/oder Produktdaten. Denken Sie daran, die gleiche Kategorie der Auftragswarteschlange zu verwenden, um Konflikte zu vermeiden.
>
> Verwenden Sie die Aktion **Berichtsanforderungsseite**, um Filter zu definieren. Sie können beispielsweise festlegen, dass Sie Aufträge nur importieren, wenn der Status **Vollständig bezahlt** lautet.

Weitere Aufgaben, die hilfreich sein können, um die Weiterverarbeitung von Verkaufsbelegen zu automatisieren:

- Bericht 297 Batchbuchung Verkaufsrechnungen
- Bericht 296 Batchbuchung Verkaufsaufträge

Sie können **Shopify Bestellnr.** verwenden Feld zum Identifizieren von Verkaufsdokumenten, die aus Shopify importiert wurden.

Um mehr über das Verbuchen von Verkaufsaufträgen in einem Stapel zu erfahren, gehen Sie zu [So erstellen Sie einen Auftragswarteschlangeneintrag für die Stapelverbuchung von Verkaufsaufträgen](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="to-check-the-status-of-synchronization"></a>Den Status von Synchronisierungen überprüfen

Im Rollencenter **Geschäftsführer** bietet der Abschnitt **Shopify Aktivitäten** mehrere Hinweise, die Ihnen helfen können, schnell zu erkennen, ob Probleme mit dem Shopify-Konnektor vorliegen.

- **Nicht zugeordnete Debitoren**: Der Shopify-Debitor wird importiert, ist aber nicht mit einem entsprechenden Debitorenposten in [!INCLUDE [prod_short](../includes/prod_short.md)] verbunden.
- **Nicht zugeordnete Produkte**: Das Shopify Produkt wird importiert, ist aber nicht mit einem entsprechenden Artikelposten in [!INCLUDE [prod_short](../includes/prod_short.md)] verbunden.
- **Unverarbeitete Aufträge**: Shopify-Aufträge werden importiert, aber es werden keine Verkaufsbelege in [!INCLUDE [prod_short](../includes/prod_short.md)] erstellt, was häufig daran liegt, dass Produkte oder Debitoren nicht zugeordnet sind.
- **Unverarbeitete Lieferungen**: Die gebuchten Verkaufslieferungen, die aus Shopify-Aufträgen stammen, werden nicht mit Shopify synchronisiert.
- **Fehler bei Lieferungen**: Der Shopify-Konnektor konnte gebuchte Verkaufslieferungen nicht mit Shopify synchronisieren.
- **Synchronisierungsfehler**: Es gibt fehlgeschlagene Aufgabenwarteschlangenposten im Zusammenhang mit der Synchronisierung mit Shopify.

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Shopify-Konnektor](get-started.md)  
