---
title: 'Designdetails – Abläufe für Fertigung, Montage und Aufträge'
description: Erfahren Sie mehr über den Fluss zwischen Lagerplätzen für das Kommissionieren von Komponenten und das Einlagern von Endartikeln für Montage- oder Fertigungs- oder Projektaufträge.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# Abläufe für Fertigung, Montage und Aufträge

Interne Abläufe, wie z. B. das Kommissionieren von Komponenten und das Einlagern von Endprodukten für die Montage-, Projekt- und Fertigungsaufträge, ähneln eingehenden oder ausgehenden Flüssen. Viele der Prozesse könnten Ihnen also bekannt vorkommen. Dieser Artikel enthält Informationen zum Arbeiten mit internen Lagerflüssen mit unterschiedlichen Komplexitätsgraden.

## Übersicht über verschiedene Konfigurationsmöglichkeiten

Sie können Lagerfunktionen auf verschiedene Weise konfigurieren. Es ist wichtig, dass die von Ihnen gewählten Optionen Ihre Prozesse verbessern, ohne Gemeinkosten zu verursachen. Die folgenden Tabellen beschreiben typische Konfigurationen für den Umgang mit physischen Gütern für Fertigungs-, Projekt- und Montageaufträge.

### Eingehender Fluss (Einlagerung)

|Komplexitätsebene|Beschreibung|Einstellungen|Lagerplatzcode|Eingehender Fluss des Fertigungssauftrags|Eingehender Fluss des Montageauftrags|Eingehender Fluss für Projekte|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Keine dedizierte Lageraktivität.|Buchung von Aufträgen und Journalen.||Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Produktions Buch.-Blatt -> Ausgabejournal</br><br/> **HINWEIS**: Sie können die Ausgabe mit **Produktions Buch.-Blatt** veröffentlichen.|Montageauftrag|Einlagern gilt nicht für Projekte|  
|Standard|Auftrag für Auftrag|Einlagerung erforderlich. </br><br/> **HINWEIS**: Obwohl die Einstellung **Einlagerung erforderlich** genannt wird, können Sie weiterhin Ausgänge aus den Herkunftsbelegen an Lagerorten buchen, in denen Sie dieses Kontrollkästchen aktivieren. |Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Fertigungsauftrag -> Lagereinlagerung|Montageauftrag|Einlagern gilt nicht für Projekte|
|Erweitert|Konsolidierte Einlagerungsaktivitäten für mehrere Herkunftsbelege.|Wareneingang erforderlich + Einlagerung erforderlich|Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Fertigungsaufträge -> Ausgabejournal|Montageaufträge -> innere Umlagerungen | Einlagern gilt nicht für Projekte|
|Erweitert|Wie oben + Gezielte Kommissionierungs-/Einlagerungsaktivitäten|Gezielte Kommissionierung und Einlagerung (abhängige Schalter werden automatisch aktiviert)|Notwendig|Wie oben.|Wie oben.| Einlagern gilt nicht für Projekte|

Bei einigen Konfigurationen können Sie keine dedizierten Lagerdokumente verwenden, um Einlagerungen zu registrieren. Wenn Ihr Lagerort jedoch Lagerplätze verwendet, können Sie allgemeine Umlagerungsdokumente verwenden, um produzierte oder montierte Artikel ins Lager zu transportieren. Weitere Informationen finden Sie unter [Interne Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Ausgehender Fluss (Kommissionierung)

|Komplexitätsebene|Beschreibung|Einstellungen|Lagerplatzcode|Ausgehender Fluss des Fertigungsauftrags|Ausgehender Fluss des Montageauftrags|Ausgehender Fluss für Projekte|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Keine dedizierte Lageraktivität.|Buchung von Aufträgen und Journalen.||Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Produktions Buch.-Blatt -> Verbrauchs Buch.-Blatt </br><br/> **HINWEIS**: Sie können den Verbrauch mit einem **Produktions Buch.-Blatt** veröffentlichen.|Montageauftrag|Projekt -> Projekt Buch.-Blatt|  
|Standard|Auftrag für Auftrag|Kommissionierung erforderlich. </br><br/> **HINWEIS**: Obwohl die Einstellung **Kommissionierung erforderlich** genannt wird, können Sie weiterhin Ausgänge aus den Herkunftsbelegen an Lagerorten buchen, in denen Sie dieses Kontrollkästchen aktivieren. <!-- ToDo Test prod output-->|Optional. Gesteuert durch den Schalter **Lagerplatzcode obligatorisch**.|Fertigungsauftrag -> Lagerbestandkommissionierung|Montageauftrag -> Lagerbestandsumlagerung</br><br/>Die **Lagerbestandsumlagerung** kann nur mit Lagerplätzen verwendet werden.|Projekt -> Lagerbestandskommissionierung|
|Erweitert|Konsolidierte Kommissionierungsaktivitäten für mehrere Herkunftsbelege.|Warenausgang erforderlich + Kommissionierung erforderlich|Optional. Gesteuert durch den Schalter Lagerplatzcode obligatorisch|Fertigungsaufträge -> Lagerkommissionierung -> Verbrauchs Buch.-Blatt |Montageaufträge -> Lagerkommissionierung| Projekt(e) -> Lagerkommissionierung -> Projekt Buch.-Blatt |
|Erweitert|Wie oben + Gezielte Kommissionierungs-/Einlagerungsaktivitäten|Gezielte Kommissionierung und Einlagerung (abhängige Schalter werden automatisch aktiviert)|Notwendig|Wie oben.|Wie oben.| Die gezielte Kommissionierung und Einlagerung wird für Projekte nicht unterstützt|

Ähnlich wie beim eingehenden Fluss können einige Konfigurationen keine dedizierten Lagerdokumente verwenden, um Einlagerungen zu registrieren. Wenn Ihr Lagerort Lagerplätze verwendet, können Sie allgemeine Umlagerungsdokumente verwenden, um produzierte oder montierte Artikel umzulagern. Erfahren Sie mehr unter [Artikel umlagern](warehouse-move-items.md).

## Lager ohne dedizierte Lageraktivität

Auch wenn Sie keine dedizierten Lageraktivitäten haben, möchten Sie wahrscheinlich dennoch Dinge wie Verbrauch und Produktionsleistung im Auge behalten. Die folgenden Artikel enthalten Informationen zum Verarbeiten von Belegen für Herkunftsbelege.

* [Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile](production-how-to-register-consumption-and-output.md)
* [Artikel montieren](assembly-how-to-assemble-items.md)
* [Verbrauch oder Nutzung für Aufträge erfassen](projects-how-record-job-usage.md)

## Basislagerhauskonfigurationen

Die ein- und ausgehenden Flüsse in einer Basislagerkonfiguration beinhalten die folgenden Einstellungen auf der Seite **Lagerortkarte** für den Lagerort:

* Aktivieren Sie für den eingehenden Fluss (Einlagerung) den Schalter **Einlagerung erforderlich**, aber deaktivieren Sie den Schalter **Beleg erforderlich** .
* Aktivieren Sie für den ausgehenden Fluss (Kommissionierung) den Schalter **Kommissionierung erforderlich**, aber deaktivieren Sie den Schalter **Lieferung erforderlich** .

### Flüsse zu und von der Produktion in einer Basislagerkonfiguration  

Verwenden Sie **Bestandskommissionierungsdokumente** für die Kommissionierung von Produktionskomponenten im Fluss zur Produktion. Um die von Ihnen hergestellten Produkte einzulagern, verwenden Sie **Lagereinlagerungsbelege**.

Für Standorte, die Lagerplätze verwenden, sind Dokumente für Lagerbestandsumlagerungen besonders nützlich für die Komponentenbuchung. Weitere Informationen darüber, wie der Komponentenverbrauch aus Fert.-Bereitst.- oder Off. Fert.-Ber.-Lagerplätzen gebucht wird, finden Sie unter [Buchungen von Produktionskomponenten in einem Lager](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Lagerbestandsumlagerungen sind wichtige Dokumente, wenn Sie die Buchungsmethode **Kommissionieren + Vorwärts** oder **Kommissionieren + Rückwärts** verwenden. Erfahren Sie mehr unter [Buchungsmethode](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Die Felder **Fert.-Bereitst.-Lagerplatzcode**, **Fert.-Ausgangslagerplatzcode** und **Off. Fert.-Ber.-Lagerpl.-Code** auf der Lagerort oder den Arbeitsplatz/Arbeitsplatzgruppen definieren Standardströme nach und von Fertigungsbereichen.
* Verwalten Sie die Umlagerung produzierter Artikel auf der Seite **Interne Umlagerung** ohne Bezug zu einem Fertigungsauftrag.

### Flüsse zu und von der Montage in einer Basislagerkonfiguration  

Montage-Ausgabe und -verbrauch direkt aus einem Montageauftrag.

> [!NOTE]
> Dokumente für **Lagerkommissionierung** und **Lagereinlagerung** werden für Montageaufträge nicht unterstützt.

Für Lagerorte, die Lagerplätze verwenden:

* Verwenden Sie **Lagerbestandsumlagerungsdokumente** , um Montagekomponenten in den Montagebereich umzulagern.
* Die Felder **Mont.-Bereitst.-Lagerplatzcode**, **Montage-Ausgangslagerplatzcode** auf der Lagerortkarte legen Standardströme nach und von Montagebereichen fest.
* Verwalten Sie die Umlagerung montierter Artikel auf der Seite **Interne Umlagerung** ohne Bezug zu einem Montageauftrag.

[!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Lagermontage- und Auftragsmontage-Flüsse. Weitere Informationen finden Sie unter [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). In Bezug auf die Lagerverwaltung ist die Lagermontage Teil des internen Lagerflusses und die Auftragsmontage ist Teil des ausgehenden Lagerflusses. Erfahren Sie mehr unter [Verarbeitung von Programmfertigung mit kommissionierten Bestandsartikeln](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flüsse für Projektmanagement in einer Basis-Lagerkonfiguration

Verwenden Sie Dokumente für **Lagerbestandskommissionierung** für die Kommissionierung von Auftragskomponenten im Fluss zum Produktionsmanagement.

Für einen Standort, der Lagerplätze verwendet, definiert das Feld **An Projekt Lagerplatzcode** am Lagerort die Standardflüsse zum Projektmanagement.

## Erweiterte Lagerhauskonfigurationen  

Die ein- und ausgehenden Flüsse in einer erweiterten Lagerkonfiguration beinhalten die folgenden Einstellungen auf der Seite **Lagerortkarte** für den Lagerort:

* Aktivieren Sie für den eingehenden Fluss (Einlagerung) die Schalter **Wareneingang erforderlich** und **Einlagerung erforderlich**.
* Aktivieren Sie für den ausgehenden Fluss (Kommissionierung) die Schalter **Versand erforderlich** und **Wareneingang erforderlich**.

### Flüsse zu und von der Produktion in erweiterten Lagerkonfigurationen

Verwenden Sie die Dokumente **Lagerkommissionierung** und die Seite **Kommissionierungsarbeitsblatt** , um Komponenten für die Produktion zu kommissionieren.

Für Lagerorte, die Lagerplätze verwenden:

* **Lagerumlagerungsdokumente** und die Seite **Umlagerungsarbeitsblatt** sind besonders nützlich für die Komponentenbuchung. Weitere Informationen finden Sie unter [Buchungen von Produktionskomponenten im Lager](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Die Felder **Fert.-Bereitst.-Lagerplatzcode**, **Fert.-Ausgangslagerplatzcode** und **Off. Fert.-Ber.-Lagerpl.-Code** auf der Lagerort oder den Arbeitsplatz/Arbeitsplatzgruppen definieren Standardströme nach und von Fertigungsbereichen. 
* Verwalten Sie die Umlagerung produzierter Artikel auf den Seiten **Umlagerungsarbeitsblatt** oder **Whse. Interne Einlagerungen** ohne Bezug zu einem Fertigungsauftrag.

### Flüsse zu und von der Montage in erweiterten Lagerkonfigurationen

Verwenden Sie die Dokumente **Lagerkommissionierung** und die Seite **Kommissionierungsarbeitsblatt** , um Komponenten für die Montage zu kommissionieren.

Für Lagerorte, die Lagerplätze verwenden:

* Die Felder **Mont.-Bereitst.-Lagerplatzcode** und **Montage-Ausgangslagerplatzcode** am Lagerort legen Standardströme nach und von Montagebereichen fest.
* Verwalten Sie die Umlagerung von Montageartikeln auf den Seiten **Umlagerungsarbeitsblatt** oder **Whse. Interne Einlagerungen** ohne Bezug zu einem Montageauftrag.

[!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Lagermontage- und Auftragsmontage-Flüsse. Weitere Informationen finden Sie unter [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Lagermontage ist Teil des internen Lagerflusses und die Auftragsmontage ist Teil des ausgehenden Lagerflusses. Weitere Informationen finden Sie unter [Verwenden von Auftragsmontageartikeln in Warenausgängen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flüsse zum Projektmanagement in erweiterten Lagerkonfigurationen

Verwenden Sie die Dokumente **Lagerkommissionierung** und die Seite **Kommissionierungsarbeitsblatt** im Fluss zum Projektmanagement.

Für Lagerorte, die Lagerplätze verwenden, definiert das Feld **An Projekte Lagerplatzcode** am Lagerort die Standardflüsse zum Projektbereich.

## Weitere Informationen  

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
