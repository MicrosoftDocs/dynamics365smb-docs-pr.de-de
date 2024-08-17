---
title: 'Konstruktionsdetails – Abläufe für Produktion, Montage und Projekte'
description: 'Erfahren Sie mehr über die Abläufe zwischen Lagerplätzen für das Kommissionieren von Komponenten und das Einlagern von Endartikeln für Montage-, Produktions- oder Projektaufträge.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/12/2024
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-projects"></a>Abläufe für Produktion, Montage und Projekte

Interne Abläufe, wie z. B. das Kommissionieren von Komponenten und das Einlagern von Endprodukten für Montage-, Projekt- und Produktionsaufträge, ähneln eingehenden oder ausgehenden Flüssen. Viele der Prozesse dürften Ihnen bekannt vorkommen. Dieser Artikel enthält Informationen zum Arbeiten mit internen Lagerflüssen mit unterschiedlichen Komplexitätsgraden.

## <a name="overview-of-different-configuration-options"></a>Übersicht über verschiedene Konfigurationsmöglichkeiten

Sie können Lagerfunktionen auf verschiedene Weise konfigurieren. Es ist wichtig, dass die von Ihnen gewählten Optionen Ihre Prozesse verbessern, ohne Gemeinkosten zu verursachen. Die folgenden Tabellen beschreiben typische Konfigurationen für den Umgang mit physischen Gütern für Produktions-, Projekt- und Montageaufträge.

### <a name="inbound-flow-put-away"></a>Eingehender Fluss (Einlagerung)

|Komplexitätsebene|Beschreibung|Einstellungen|Lagerplatzcode|Eingehender Fluss des Fertigungssauftrags|Eingehender Fluss des Montageauftrags|Eingehender Fluss für Projekte|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Keine dedizierte Lageraktivität.|Buchung von Aufträgen und Journalen.||Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Produktions Buch.-Blatt -> Ausgabejournal</br><br/> **HINWEIS**: Sie können die Ausgabe mit **Produktions Buch.-Blatt** veröffentlichen.|Montageauftrag|Die Einlagerung ist nicht anwendbar für Projekte|  
|Basis|Auftrag für Auftrag|Lagerabwicklung der Produktionsausgabe: Lagereinlagerung. </br><br/> **HINWEIS**: An Orten, an denen Sie diese Einstellungen aktiviert haben, können Sie weiterhin Ausgaben direkt aus den Quelldokumenten veröffentlichen. |Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Fertigungsauftrag -> Lagereinlagerung|Montageauftrag|Die Einlagerung ist nicht anwendbar für Projekte|
|Erweitert|Konsolidierte Einlagerungsaktivitäten für mehrere Herkunftsbelege.|Keine dedizierten Einstellungen|Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Fertigungsaufträge -> Ausgabejournal|Montageaufträge -> innere Umlagerungen | Die Einlagerung ist nicht anwendbar für Projekte|
|Erweitert|Wie oben, plus gesteuerte Kommissionier-/Einlagerungsaktivitäten|Gezielte Kommissionierung und Einlagerung (abhängige Umschalter werden automatisch aktiviert)|Obligatorisch|Wie oben|Wie oben| Die Einlagerung ist nicht anwendbar für Projekte|

Bei einigen Konfigurationen ist die Verwendung dedizierter Lagerdokumente zum Erfassen von Einlagerungen nicht möglich. Wenn Ihr Lagerort jedoch Lagerplätze verwendet, können Sie allgemeine Umlagerungsdokumente verwenden, um produzierte oder montierte Artikel ins Lager zu transportieren. Erfahren Sie mehr unter [Artikel umlagern](warehouse-move-items.md).

### <a name="outbound-flow-pick"></a>Ausgehender Fluss (Kommissionierung)

|Komplexitätsebene|Description|Einstellungen|Lagerplatzcode|Ausgehender Fluss des Fertigungsauftrags|Ausgehender Fluss des Montageauftrags|Ausgehender Fluss für Projekte|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Keine dedizierte Lageraktivität.|Buchung von Aufträgen und Buch.-Blättern.||Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Produktions Buch.-Blatt -> Verbrauchs Buch.-Blatt </br><br/> **HINWEIS**: Sie können den Verbrauch mit einem **Produktions Buch.-Blatt** veröffentlichen.|Montageauftrag|Projekt -> Projekt-Buch.-Blatt|  
|Basis|Auftrag für Auftrag|Produktion, Montage, Projekte: Lagerkommissionierung, Lagerbewegung </br><br/> **HINWEIS**: An Standorten, an denen Sie diese Einstellungen aktiviert haben, können Sie den Verbrauch weiterhin direkt aus den Quellbelegen buchen.|Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Fertigungsauftrag -> Lagerbestandkommissionierung|Montageauftrag -> Lagerbestandsumlagerung</br><br/>Die **Lagerbestandsumlagerung** kann nur mit Lagerplätzen verwendet werden.|Projekt -> Lagerkommissionierung|
|Erweitert|Konsolidierte Kommissionierungsaktivitäten für mehrere Herkunftsbelege.|Produktion, Montage, Projekte: Lagerkommissionierung|Optional. Gesteuert durch den Schalter Lagerplatzcode obligatorisch|Fertigungsaufträge -> Lagerkommissionierung -> Verbrauchs Buch.-Blatt |Montageaufträge -> Lagerkommissionierung| Projekt(e) -> Lagerkommissionierung -> Projekt-Buch.-Blatt |
|Erweitert|Wie oben + Gezielte Kommissionierungs-/Einlagerungsaktivitäten|Gezielte Kommissionierung und Einlagerung (abhängige Umschalter werden automatisch aktiviert)|Obligatorisch|Wie oben|Wie oben| Gezielte Kommissionierung und Einlagerung werden für Projekte nicht unterstützt|

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Lager ohne dedizierte Lageraktivität

Auch wenn Sie keine dedizierten Lageraktivitäten verwenden, möchten Sie möglicherweise Dinge wie Verbrauch und Produktionsleistung verfolgen. Die folgenden Artikel enthalten Informationen zum Verarbeiten von Belegen für Herkunftsbelege.

* [Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile](production-how-to-register-consumption-and-output.md)
* [Artikel montieren](assembly-how-to-assemble-items.md)
* [Verbrauch oder Nutzung für Projekt erfassen](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Basislagerhauskonfigurationen

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Flüsse zu und von der Produktion in einer Basislagerkonfiguration

Die ein- und ausgehenden Flüsse in einer Basislagerkonfiguration beinhalten die folgenden Einstellungen auf der Seite **Lagerortkarte** für den Lagerort:

* Für den Eingangsfluss (Einlagerung) im Feld  **Produktionsausgangs-Lagerabwicklung**  Auswählen **Lagereinlagerung**.
* Für den ausgehenden Fluss (Kommissionierung) im Feld  **Produktionsverbrauch – Lagerabwicklung**  Auswählen **Lagerkommissionierung/-bewegung**.

Verwenden Sie **Bestandskommissionierungsdokumente** für die Kommissionierung von Produktionskomponenten im Fluss zur Produktion. Um die von Ihnen hergestellten Produkte einzulagern, verwenden Sie **Lagereinlagerungsbelege**.

Für Standorte, die Lagerplätze verwenden, sind Dokumente für Lagerbestandsumlagerungen besonders nützlich für die Komponentenbuchung. Weitere Informationen darüber, wie der Komponentenverbrauch aus Fert.-Bereitst.- oder Off. Fert.-Ber.-Lagerplätzen gebucht wird, finden Sie unter [Buchungen von Produktionskomponenten in einem Lager](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerbestandsumlagerungen sind wichtige Dokumente, wenn Sie die Buchungsmethode **Kommissionieren + Vorwärts** oder **Kommissionieren + Rückwärts** verwenden. Erfahren Sie mehr unter [Buchungsmethode](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Die Felder **Fert.-Bereitst.-Lagerplatzcode**, **Fert.-Ausgangslagerplatzcode** und **Off. Fert.-Ber.-Lagerpl.-Code** auf der Lagerort oder den Arbeitsplatz/Arbeitsplatzgruppen definieren Standardströme nach und von Fertigungsbereichen.
* Verwalten Sie die Umlagerung produzierter Artikel auf der Seite **Interne Umlagerung** ohne Bezug zu einem Fertigungsauftrag.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Flüsse zu und von der Montage in einer Basislagerkonfiguration

Der ausgehende Fluss in einer grundlegenden Lagerkonfiguration umfasst die folgenden Einstellungen auf der Seite  **Standort Karte**  für den Standort:

* Für den ausgehenden Fluss (Kommissionierung) im Feld  **Assembly-Verbrauchslagerabwicklung**  Auswählen **Lagerbewegung**.

Verwenden Sie  **Lagerbewegungsdokumente**, um Montagekomponenten im Montagefluss auszuwählen. Montage-Ausgabe und -verbrauch direkt aus einem Montageauftrag.

> [!NOTE]
> Dokumente für **Lagerkommissionierung** und **Lagereinlagerung** werden für Montageaufträge nicht unterstützt.

Für Lagerorte, die Lagerplätze verwenden:

* Verwenden Sie **Lagerbestandsumlagerungsdokumente** , um Montagekomponenten in den Montagebereich umzulagern.
* Die Felder **Mont.-Bereitst.-Lagerplatzcode**, **Montage-Ausgangslagerplatzcode** auf der Lagerortkarte legen Standardströme nach und von Montagebereichen fest.
* Verwalten Sie die Umlagerung montierter Artikel auf der Seite **Interne Umlagerung** ohne Bezug zu einem Montageauftrag.

[!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Lagermontage- und Auftragsmontage-Flüsse. Weitere Informationen finden Sie unter [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). In Bezug auf die Lagerverwaltung ist die Lagermontage Teil des internen Lagerflusses und die Auftragsmontage ist Teil des ausgehenden Lagerflusses. Erfahren Sie mehr unter [Verarbeitung von Programmfertigung mit kommissionierten Bestandsartikeln](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Flüsse für Projektmanagement in einer Basis-Lagerkonfiguration

Der ausgehende Fluss in einer grundlegenden Lagerkonfiguration umfasst die folgenden Einstellungen auf der Seite  **Standort Karte**  für den Standort:

* Für den ausgehenden Fluss (Kommissionierung) im Feld  **Projektverbrauchs-Lagerabwicklung**  Auswählen **Lagerkommissionierung**.

Verwenden Sie Belege für **Lagerkommissionierung** für die Kommissionierung von Projektkomponenten im Fluss zum Projektmanagement.

Für einen Lagerort, der Lagerplätze verwendet, legt das Feld **An Projekt Lagerplatzcode** am Lagerort die Standardflüsse zum Projektmanagement fest.

## <a name="advanced-warehouse-configurations"></a>Erweiterte Lagerhauskonfigurationen

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Flüsse zu und von der Produktion in erweiterten Lagerkonfigurationen

Der ausgehende Fluss in einer erweiterten Lagerkonfiguration umfasst die folgenden Einstellungen auf der Seite  **Standort Karte**  für den Standort:

* Für den ausgehenden Fluss (Kommissionierung) im Feld  **Produktionsverbrauch – Lagerabwicklung**  Auswählen **Lagerkommissionierung (optional)**  oder  **Lagerkommissionierung (obligatorisch)**.

Verwenden Sie die Dokumente **Lagerkommissionierung** und die Seite **Kommissionierungsarbeitsblatt** , um Komponenten für die Produktion zu kommissionieren.

> [!NOTE]
> **Lagereinlagerungsdokumente** werden für die Produktionsausgabe nicht unterstützt.

Für Lagerorte, die Lagerplätze verwenden:

* **Lagerumlagerungsdokumente** und die Seite **Umlagerungsarbeitsblatt** sind besonders nützlich für die Komponentenbuchung. Weitere Informationen finden Sie unter [Buchungen von Produktionskomponenten im Lager](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Die Felder **Fert.-Bereitst.-Lagerplatzcode**, **Fert.-Ausgangslagerplatzcode** und **Off. Fert.-Ber.-Lagerpl.-Code** auf der Lagerort oder den Arbeitsplatz/Arbeitsplatzgruppen definieren Standardströme nach und von Fertigungsbereichen. 
* Verwalten Sie die Umlagerung produzierter Artikel auf den Seiten **Umlagerungsarbeitsblatt** oder **Whse. Interne Einlagerungen** ohne Bezug zu einem Fertigungsauftrag.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Flüsse zu und von der Montage in erweiterten Lagerkonfigurationen

Der ausgehende Fluss in einer erweiterten Lagerkonfiguration umfasst die folgenden Einstellungen auf der Seite  **Standort Karte**  für den Standort:

* Für den ausgehenden Fluss (Kommissionierung) im Feld  **Montage-Verbrauchslagerabwicklung**  Auswählen **Lagerkommissionierung (optional)**  oder  **Lagerkommissionierung (obligatorisch)**. 

Verwenden Sie die Dokumente **Lagerkommissionierung** und die Seite **Kommissionierungsarbeitsblatt** , um Komponenten für die Montage zu kommissionieren.

> [!NOTE]
> **Lagereinlagerungsbelege** werden für Montageaufträge nicht unterstützt.

Für Lagerorte, die Lagerplätze verwenden:

* Die Felder **Mont.-Bereitst.-Lagerplatzcode** und **Montage-Ausgangslagerplatzcode** am Lagerort legen Standardströme nach und von Montagebereichen fest.
* Verwalten Sie die Umlagerung von Montageartikeln auf den Seiten **Umlagerungsarbeitsblatt** oder **Whse. Interne Einlagerungen** ohne Bezug zu einem Montageauftrag.

[!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Lagermontage- und Auftragsmontage-Flüsse. Weitere Informationen finden Sie unter [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Lagermontage ist Teil des internen Lagerflusses und die Auftragsmontage ist Teil des ausgehenden Lagerflusses. Weitere Informationen finden Sie unter [Verwenden von Auftragsmontageartikeln in Warenausgängen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Flüsse zum Projektmanagement in erweiterten Lagerkonfigurationen

Der ausgehende Fluss in einer erweiterten Lagerkonfiguration umfasst die folgenden Einstellungen auf der Seite  **Standort Karte**  für den Standort:

* Für den ausgehenden Fluss (Kommissionierung) im Feld  **Projektverbrauch – Lagerabwicklung**  Auswählen **Lagerkommissionierung (optional)**  oder  **Lagerkommissionierung (obligatorisch)**.

Verwenden Sie die Dokumente **Lagerkommissionierung** und die Seite **Kommissionierungsarbeitsblatt** im Fluss zum Projektmanagement.

Für Lagerorte, die Lagerplätze verwenden, legt das Feld **An Projekte Lagerplatzcode** am Lagerort die Standardflüsse zum Projektbereich fest.

## <a name="see-also"></a>Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
