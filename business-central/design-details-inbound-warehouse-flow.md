---
title: Design-Details – Inbound Warehouse Flow
description: 'Erfahren Sie, wie Sie Artikel in Ihrem Lager empfangen, registrieren und eingehenden Quelldokumenten zuordnen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: warehouse
ms.date: 09/18/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designdetails: Eingehender Lagerflow

Der eingehende Fluss in ein Lager beginnt, wenn Artikel im Lager des Unternehmensstandorts ankommen, entweder aus externen Quellen oder von einem anderen Standort des Unternehmens. Sie können physische und nicht vorrätige Artikel erhalten. Weitere Informationen zum Empfang von Nicht-Lagerartikeln finden Sie unter [Nicht-Lagerartikel buchen](#post-non-inventory-items).

Grundsätzlich besteht der Prozess des Eingangs von eingehenden Aufträgen aus zwei Aktivitäten:

* Sie nehmen Artikel an der Rampe entgegen, identifizieren sie, ordnen sie einem Quellbeleg zu und setzen die Eingangsmenge fest.
* Lagern Sie Artikel im Lager ein und notieren Sie den Platz, an dem Sie sie abgelegt haben.

Die Herkunftsbelege für den eingehenden Lagerfluss sind:

* Bestellungen  
* Eingehende Umlagerungsaufträge  
* Verkaufsreklamationen  

> [!NOTE]
> Produktions- und Montage-Ausgabe stellen auch eingehende Herkunftsbelege dar. Weitere Informationen über die Verarbeitung von Fertigungs- und Montage-Ausgabe für interne Prozesse finden Sie unter [Designdetails: Interner Lagerfluss](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Sie Artikel und lagern sie, wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden ein.

|Art|Eingangsprozess|Wareneingang erforderlich|Einlagerung erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Posteinlieferungsschein und die Einlagerung der Auftragszeile|||Keine dedizierte Lageraktivität.|  
|B|Posteinlieferungsschein und Einlagerung aus dem Beleg "Lagereinlagerung"||Aktiviert|Basis: Auftragsbezogene Logistik|  
|U|Posteinlieferungsschein und Einlagerung aus einem Wareneingangsbeleg|Aktiviert||Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Posteinlieferungsschein aus einem Wareneingangsbeleg und Posteinlagerung aus einem Einlagerungsbeleg|Aktiviert|Aktiviert|Erweitert|  

Die Auswahl eines Ansatzes hängt von Ihren Methoden des Unternehmens und dem Niveau der Organisationskomplexität ab. Im Folgenden finden Sie einige Beispiele, die Ihnen bei der Entscheidung helfen könnten.

* In einer Lagerumgebung mit auftragsbezogener Logistik, in der die meisten Lagermitarbeiter direkt mit Auftragsdokumenten arbeiten, können Sie sich für Methode A entscheiden. 
* Ein Lager mit auftragsbezogener Logistik mit einem komplexeren Einlagerungsprozess oder wo Lagermitarbeiter ihre Einlagerungsaktivitäten vom Auftragsdokument trennen, könnte Methode B verwenden.
* Unternehmen, die die Abwicklung mehrerer Bestellungen planen müssen, finden es möglicherweise hilfreich, Wareneingangsbelege zu verwenden, Methoden C und D.  

In den Methoden A, B und C werden der Eingang und die Einlagerung in einem Schritt zusammengefasst, wenn der Beleg als eingegangen gebucht wird. In Methode D wird der Eingang zuerst gebucht, um die Bestandszunahme zu erfassen sowie, dass Artikel zum Verkauf verfügbar sind. Der Lagermitarbeiter registriert die Einlagerung, um die Artikel für die Kommissionierung für ausgehende Aufträge bereitzustellen. 

> [!NOTE]
> Wareneinlagerungen und Lagereinlagerungen klingen zwar ähnlich, sind aber unterschiedliche Dokumente und werden in unterschiedlichen Prozessen verwendet.
> * Die in Methode B verwendete Lagereinlagerung verbucht zusammen mit der Registrierung von Einlagerungsinformationen auch den Eingang des Herkunftsbelegs.
> * Die in Methode D verwendete Lagereinlagerung kann nicht gebucht werden und registriert nur die Einlagerung. Die Registrierung stellt die Artikel für die weitere Bearbeitung zur Verfügung, bucht aber nicht den Beleg. Im Wareneingang erfordert die Lagereinlagerung einen Wareneingang.

## Keine dedizierte Lageraktivität

Die folgenden Artikel enthalten Informationen zum Verarbeiten von Wareneingängen für Herkunftsbelege, wenn Sie keine dedizierten Lageraktivitäten haben.

* [Erfassen eines Einkaufs](purchasing-how-record-purchases.md)
* [Umlagerungsaufträge](inventory-how-transfer-between-locations.md)
* [Verkaufsaufträge für Rücklieferungen verarbeiten](sales-how-process-sales-returns-orders.md)

## Grundlegende Lagerhauskonfigurationen  

In einer Basislagerkonfiguration ist der Schalter **Einlagerung erforderlich** aktiviert, aber der Schalter **Wareneingang erforderlich** auf der Seite **Lagerortkarte** für den Lagerort ist deaktiviert.

Das folgende Diagramm zeigt die eingehenden Lagerflüsse nach Belegtyp im Rahmen der einfachen Logistik an. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Der eingehende Basisfluss in einem Lager.":::

### 1: Geben Sie ein Herkunftsbeleg frei, um eine Anforderung für eine Lagereinlagerung zu erstellen  

Wenn Sie Artikel erhalten, geben Sie den Herkunftsbeleg frei, z. B. eine Bestellung oder einen eingehenden Umlagerungsauftrag. Durch die Freigabe des Belegs werden die Artikel zum Einlagern verfügbar. Sie können auch Lagereinlagerungsbelege für einzelne Auftragszeilen, im Push-Verfahren, basierend auf angegebenen Lagerplätzen und Mengen erstellen, die verarbeitet werden sollen.  

### 2: Erstellen Sie eine Lagereinlagerung  

Auf der Seite **Lagereinlagerung** können Sie im Pull-Verfahren die offenen Herkunftsbelegzeilen basierend auf den eingehenden Lageranfragen abrufen. Im Push-Verfahren können Sie auch Lagereinlagerungszeilen erstellen, wenn Sie den Herkunftsbeleg erstellen.  

### 3: An Lagereinlagerung buchen  

In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllen Sie das Feld **Menge** aus und buchen Sie dann die Lagereinlagerung. Herkunftsbelege, die mit der Einlagerung verknüpft sind, werden als eingegangen gebucht.  

* Positive Artikelposten werden erstellt.
* Lagerposten werden für Lagerplätze erstellt, die bei allen Artikeltransaktionen einen Lagerplatzcode erfordern.
* Die Einlagerungsanforderung wird gelöscht, wenn sie vollständig bearbeitet wurde. Beispielsweise wird das Feld **Menge empfangen**auf der Zeile des eingehenden Herkunftsbelegs aktualisiert.
* Ein Beleg des gebuchten Wareneingangs wird erstellt, der beispielsweise die Einkaufsbestellung und die eingegangenen Artikel angezeigt.  

## Erweiterte Lagerhauskonfigurationen  

Um die erweiterten Lagerkonfiguration zu verwenden, aktivieren Sie den Schalter **Wareneingang erforderlich** auf der Standortkartenseite für den Standort. Der Schalter **Einlagerung erforderlich** ist optional.

Das folgende Diagramm zeigt den eingehenden Lagerfluss nach Belegtyp. Die Nummern im Diagramm entsprechen den Schritten in den Abschnitten, die dem Diagramm folgen.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Der erweiterte eingehende Fluss in einem Lager.":::

### 1: Den Herkunftsbeleg freigeben  

Wenn Sie Artikel erhalten, geben Sie den Herkunftsbeleg frei, z. B. die Bestellung oder einen eingehenden Umlagerungsauftrag. Durch die Freigabe des Belegs werden die Artikel zum Einlagern verfügbar. Die Einlagerung enthält Referenzen zur Herkunftsbelegart und -Nummer.

### 2: Einen Wareneingang erstellen  

Auf der Seite **Wareneingang** rufen Sie die eingehenden Herkunftsbelegzeilen ab. Sie können mehrere Herkunftsbelegzeilen zu einem Wareneingangsbeleg zusammenfassen. Füllen Sie das Feld **Verarbeitungsmenge** aus und wählen Sie die empfangende Zone und den Lagerplatz nach Bedarf aus.  

### 3: Buchen Sie den Wareneingang  

Buchen Sie den Wareneingang, um positive Artikel Buch.-Blattzeilen zu erstellen. Das Feld **Menge empfangen** wird auf der Zeile des eingehenden Herkunftsbelegs aktualisiert.  

Wenn der Schalter **Einlagerung erforderlich** auf der Lagerortkarte nicht aktiviert ist, wird der Prozess hier beendet. Andernfalls werden die Artikel durch die Buchung des eingehenden Herkunftsbelegs zum Einlagern verfügbar gemacht. Die Einlagerung enthält Referenzen zur Herkunftsbelegart und -Nummer.  

### 4: (Optional) Einlagerungsarbeitsblattzeilen generieren

Rufen Sie Einlagerungszeilen im **Einlagerungsarbeitsblatt** basierend auf gebuchten Wareneingängen oder Vorgängen ab, die eine Ausgabe erzeugen. Geben Sie in der einzulagernden Zeile die folgenden Informationen an:

* Die Lagerplätze aus denen Artikel entnommen werden sollen.
* Die Lagerplätze, in die Artikel eingelagert werden.
* Wie viele Einheiten zu bearbeiten sind.

Die Lagerplätze können durch Einrichtung des Lagerorts oder der Ressource vordefiniert werden, die den Vorgang durchgeführt hat.  

Wenn alle Einlagerungen geplant und den Lagermitarbeitern zugeteilt sind, erstellen Sie die Einlagerungsbelege. Vollständig zugeordnete Einlagerungszeilen werden aus dem **Einlagerungsarbeitsblatt** gelöscht.  

> [!NOTE]  
> Wenn der Schalter **Einlagerungsarbeitsblatt** auf der Artikelkarte nicht aktiviert ist, werden Einlagerungsbelege direkt basierend auf den gebuchten Wareneingängen erstellt. In diesem Fall ist dieser Schritt nicht erforderlich.  

### 5: Einen Einlagerungsbeleg erstellen

Erstellen Sie auf der Grundlage des gebuchten Wareneingangs einen Lagereinlagerungsbeleg im Pull-Verfahren. Oder erstellen Sie das Wareneinlagerungsbeleg und weisen Sie es einem Lagermitarbeiter im Push-Verfahren zu.  

### 6: Eine Wareneinlagerung registrieren

In jeder Zeile für Artikel, die kommissioniert oder umgelagert wurden, sei es teilweise oder vollständig, füllen Sie das Feld **Menge** auf der Seite **Kommissionierungsarbeitsblatt** aus und erfassen dann die Lagerbestandsumlagerung.  

* Lagerposten werden für Lagerplätze erstellt, die bei allen Artikeltransaktionen einen Lagerplatzcode erfordern.
* Die Wareneinlagerungszeilen wird gelöscht, wenn sie vollständig bearbeitet wurde.
* Der Einlagerungsbeleg bleibt offen, bis die gesamte Menge des zugehörigen gebuchten Warenzugangs erfasst ist.
* Das Feld **Menge eingelagert** auf den gebuchten Wareneingangsauftragszeilen wird aktualisiert.

## Verwandte Tasks

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

|**Prozess**|**Informationen**|  
|------------|-------------|  
|Empfangen Sie Artikel an Lagerstandorten mit einem Lagerbeleg für die voll- oder teilautomatisierte Lagerverarbeitung.|[Artikel empfangen](warehouse-how-receive-items.md)|
|Lagern Sie Artikel auftragsweise ein, und buchen Sie bei Basis-Lagerkonfigurationen den Eingang in einer Aktivität.|[Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Lagern Sie Artikel ein, die bei mehreren Einkäufen, Verkaufsrücksendungen, Umlagerungsaufträgen in einer erweiterten Lagerkonfiguration ein.|[Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  

## Buchen von Nicht-Bestandsartikeln

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## Siehe auch

[!INCLUDE[footer-include](includes/footer-banner.md)]
