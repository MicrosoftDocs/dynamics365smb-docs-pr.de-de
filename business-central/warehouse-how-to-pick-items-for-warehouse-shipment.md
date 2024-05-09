---
title: Artikel für den Warenausgang kommissionieren
description: 'Erfahren Sie, wie Sie die Belege der Lager-Kommissionierungen verwenden, um Kommissionierinformationen zu erstellen und zu verarbeiten, bevor Sie einen Warenausgang buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# Artikel für den Warenausgang kommissionieren

In [!INCLUDE[prod_short](includes/prod_short.md)] kommissionieren und versenden Sie Artikel wie in der folgenden Tabelle beschrieben, mit einer von vier Methoden.

|Art|Ausgangsprozess|Kommissionierung erforderlich|Warenausgang erforderlich|Komplexitätsgrad (Weitere Informationen unter [Lagermanagementübersicht](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Die Kommissionierung und den Versand aus der Auftragszeile buchen|||Keine dedizierte Lageraktivität.|  
|B|Die Kommissionierung und den Warenausgang aus einem Lagerkommissionierungsbeleg buchen|Aktiviert||Basis: Auftragsbezogene Logistik|  
|U|Die Kommissionierung und den Warenausgang aus einem Warenausgangsbeleg buchen||Aktiviert|Basis: Konsolidierte Eingangs-/Versandbuchung für mehrere Bestellungen.|  
|T|Die Kommissionierung von einem Kommissionierbeleg und buchen Sie den Warenausgang aus einem Warenausgangsbeleg buchen|Aktiviert|Aktiviert|Erweitert|  

Weitere Informationen finden Sie unter [Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).

Dieser Artikel bezieht sich auf die Methode D in der Tabelle. Weitere Informationen zu Versandartikeln finden Sie unter [Versandartikel](warehouse-how-ship-items.md).

Wenn ein Lagerort so eingerichtet wurde, dass die Bearbeitung der Kommissionierung und des Warenausgangs erforderlich ist, verwenden Sie die Kommissionierbelege, um Kommissionierinformationen vor dem Buchen des Warenausgangs zu erstellen und zu bearbeiten.  

Sie können keine Lagerkommissionierbelege von Grund auf erstellen. Kommissionierungen sind Teil eines Workflows, bei dem eine Person, die einen Auftrag bearbeitet, sie im Push-Verfahren erstellt, oder der Lagermitarbeiter sie im Pull-Verfahren erstellt:

- Im Push-Verfahren, bei dem Sie die Aktion **Kommissionierung erstellen** auf der Seite **Warenausgang** verwenden. Wählen Sie die zu kommissionierenden Zeilen und bereiten Sie die Kommissionierungen vor, indem sie beispielsweise angeben, aus welchen Lagerplätzen entnommen und in welche Lagerplätze eingelagert wird, und wie viele Einheiten bewegt werden. Lagerplätze können für den Lagerort oder die Ressource vordefiniert werden.
- In einem Pull-Verfahren, bei der Sie die Aktion **Freigeben** auf der Seite **Warenausgang** verwenden, um die Artikel für die Kommissionierung verfügbar zu machen. Anschließend können Lagermitarbeiter auf der Seite **Kommissionierungsarbeitsblatt** die Aktion **Lagerdokumente abrufen** verwenden, um ihre zugewiesenen Kommissionierungen vorzunehmen.

> [!NOTE]  
> Die Kommissionierung für einen Warenausgang von Artikeln, die für einen Verkaufsauftrag montiert werden, folgt denselben Schritten wie die reguläre Kommissionierung für Warenausgänge, die in diesem Artikel beschrieben ist. Jedoch kann die Anzahl der Kommissionierzeilen für die zu liefernde Menge n:1 sein, da die Kommissionierung für die Komponenten, nicht für den montierten Artikel erfolgt.  
>
> Lagerkommissionierungszeilen werden für den Wert im Feld **Restmenge** in den Zeilen des Montageauftrags erstellt, der mit der Verkaufsauftragszeile verknüpft ist, die geliefert wird. Alle Komponenten werden in einer Aktion kommissioniert. Weitere Informationen finden Sie unter [Verwenden von Auftragsmontageartikeln in Warenausgängen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Weitere Informationen über das Kommissionieren von Komponenten für Montageaufträge, einschließlich von Situationen, in denen Montageartikel nicht mit einer Verkaufslieferung fällig sind, finden Sie unter [Kommissionierung für Fertigung, Montage oder Projekte in erweiterten Lagerkonfigurationen](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## Prüfen Sie, ob Artikel zur Kommissionierung verfügbar sind

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## So erstellen Sie Kommissionierungsdokumente mit dem Kommissionierungsarbeitsblatt in Masse

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kommissionierarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  

2. Wählen Sie die **Logistikbeleg holen** Aktion aus.  

    Die Liste enthält alle Ausgänge, die zur Kommissionierung freigegeben wurden, einschließlich der Ausgänge, für die bereits Kommissionieranweisungen erstellt wurden. Belege mit Kommissionierungszeilen, die bereits vollständig kommissioniert und registriert wurden, werden in dieser Übersicht nicht angezeigt.  
3. Wählen Sie die Warenausgänge, für die Sie eine Kommissionierung vorbereiten möchten.

    > [!NOTE]  
    >  Sollten Sie versuchen, einen Beleg auszuwählen (Warenausgang oder interne Kommissionierung), für den Sie bereits Anweisungen für alle Zeilen erzeugt haben, erhalten Sie eine Meldung, wie die folgende: „es gibt keine Mengen zu bewegen“. Um Lagerkommissionieranweisungen, die Sie bereits erstellt haben, zu einer Kommissionieranweisung zu kombinieren, müssen Sie die einzelnen Kommissionierungen zuerst löschen.

4. Füllen Sie das Feld **Sortiermethode** aus, um die Zeilen zu sortieren.  

    > [!NOTE]  
    >  Die Art und Weise, wie die Zeilen im Arbeitsblatt sortiert sind, überträgt sich nicht automatisch auf die Entnahmeanweisung. Es bestehen jedoch die gleichen Sortier- und Priorisierungsmöglichkeiten der Lagerplätze. Sie können die Zeilenreihenfolge, die Sie im Arbeitsblatt erstellen, leicht neu erstellen, wenn Sie die Kommissionierungsanweisungen erstellen oder indem Sie die Kommissionierungsanweisungen sortieren.

5. Füllen Sie das Feld **Bewegungsmge** entweder manuell oder mithilfe der Aktion **Bewegungsmenge autom. ausfüllen**.  

    Die Seite zeigt die in Cross-Docking-Lagern verfügbaren Mengen an. Diese Informationen sind für die Planung von Arbeitseinsätzen in Cross-Docking-Situationen nützlich ist. [!INCLUDE[prod_short](includes/prod_short.md)] wird immer zuerst eine Entnahme aus einem Cross-Dock-Behälter vorschlagen.
6. Bearbeiten Sie diese Positionen bei Bedarf. Sie können auch Zeilen löschen, um die Kommissionierung effektiverer zu machen. Wenn es z. B. mehrere Zeilen mit Artikeln in Zuordnungslagerplätzen gibt, möchten Sie möglicherweise eine Kommissionierung für alle Zeilen erzeugen, die mit all diesen Zeilen zusammenhängen. Die zugeordneten Artikel werden ausgeliefert (mit anderen Artikeln im Warenausgang) und die Zuordnungslagerplätze haben wieder Platz für neue ankommende Artikel.  

    > [!NOTE]  
    >  Wenn Sie Zeilen löschen, werden sie aus dem Arbeitsblatt gelöscht. Sie werden nicht aus der Kommissionierungsauswahlliste gelöscht.  

7. Wählen Sie die Aktion **Kommissionierung erstellen** aus. Die Seite **Kommissionierung erstellen** wird geöffnet, auf der Sie der von Ihnen erstellten Kommissionierung weitere Informationen hinzufügen können. Geben Sie an, wie Kommissionierungszeilen in den Kommissionierungsbelegen kombiniert werden sollen, indem Sie eine der folgenden Optionen auswählen.  

    |Option|Beschreibung|
    |-|-|
    |Nach Lager. Beleg|Erstellt separate Kommissionierungsbelege für Arbeitsblattzeilen mit demselben Lagerherkunftsbeleg.|
    |Nach Deb./Kred./Lagerort|Erstellen Sie separate Kommissionierungsbelege für jeden Debitor (Verkaufsaufträge), Kreditor (Einkaufsreklamationen) und Lagerort (Umlagerungsaufträge).|
    |Nach Artikel|Erstellen Sie separate Kommissionierungsbelege für jeden Artikel im Kommissionierungs-Arbeitsblatt.|
    |Nach Zone|Erstellen Sie separate Kommissionierungsbelege für jede Zone, aus der Sie Artikel entnehmen werden.|
    |Nach Lagerplatznr.|Erstellen Sie separate Kommissionierungsbelege für jeden Lagerplatz, aus der Sie Artikel entnehmen werden.|
    |Nach Fälligkeitsdatum|Erstellen Sie separate Kommissionierungsbelege für Herkunftsbelege, die das gleiche Fälligkeitsdatum haben.|

    Geben Sie an, wie Kommissionierbelege erstellt werden sollen, indem Sie aus den folgenden Optionen auswählen.

    |Option|Beschreibung|
    |-|-|
    |Max. Anz. der Kommissionierungszeilen|Erstellt Kommissionierbelege, die in jedem Beleg nicht mehr als die angegebene Anzahl von Zeilen haben.|
    |Max. Anz. der Kommissionierungsherkunftsbelege|Erstellt Kommissionierungsbelege, von denen jeder nicht mehr als die angegebene Anzahl von Herkunftsbelegen einschließt.|
    |Zugewiesene Benutzer-ID|Erstellt Kommissionierungsbelege nur für Arbeitsblattzeilen, die dem ausgewählten Lagermitarbeiter zugeordnet sind.|
    |Sortiermethode für Kommissionierzeilen|Wählen Sie aus den verfügbaren Optionen aus, um Zeilen im erstellten Kommissionierungsbeleg zu sortieren.|
    |Gebindeanbruchsfilter verw.|Blendet Gebindeanbruch-Kommissionierungs-Zwischenzeilen aus, wenn eine größeren Maßeinheit in eine kleinere Maßeinheit umgewandelt und vollständig Kommissioniert wird.|
    |Bewegungsmenge nicht ausfüllen|Lässt das Feld Bewegungsmge in den erstellten Kommissionierungszeilen leer.|
    |Kommissionierschein drucken|Druckt die Kommissionierbelege, wenn diese erstellt werden. Sie können auch aus den erstellten Kommissionierungsbelegen drucken.|

8. Wählen Sie **OK** aus. [!INCLUDE [prod_short](includes/prod_short.md)] erstellt die Kommissionierung gemäß Ihrer Auswahl.  

## So kommissionieren Sie Artikel für einen Warenausgang

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lager-Kommissionierungen** ein und wählen Sie dann den zugehörigen Link.  

    Wenn Sie an einer bestimmten Kommissionierung arbeiten möchten, wählen Sie die Kommissionierung in der Liste aus, oder filtern Sie die Liste, um die Kommissionierungen zu finden, die speziell Ihnen zugeordnet wurden. Öffnen Sie die Kommissionierungskarte.  
2. Wenn das Feld **Zugewiesene Benutzer-ID** leer ist, geben Sie gegebenenfalls Ihre ID ein, um sich zu identifizieren.  
3. Kommissionieren Sie die Artikel.  

    Wenn das Lager für die Verwendung von Lagerplätzen eingerichtet wurde, werden die Vorgabelagerplätze der Artikel als Vorschlag für den Entnahmeort verwendet. Die Anweisungen enthalten mindestens zwei separate Zeilen für jede der Aktionen Entnahme und Einlagerung.  

    Wenn das Lager mit gesteuerter Einlagerung und Kommissionierung eingerichtet wurde, werden die Lagerplatzränge verwendet, um die besten Lagerplätze für die Kommissionierung zu berechnen. Diese Lagerplätze werden in den Kommissionierungszeilen vorgeschlagen. Die Anweisungen enthalten mindestens zwei separate Zeilen für jede der Aktionen Entnahme und Einlagerung.  

    * Die erste Zeile mit dem Feld **Entnahme** im Feld **Aktionsart** zeigt an, wo sich die Artikel im Kommissionierungsbereich befinden. Wenn Sie eine große Menge an Artikeln in einer Lieferzeile liefern, müssen Sie möglicherweise die Artikel in mehrere Lagerplätze kommissionieren, damit es eine Zeile der Art Auslagerung für jeden Lagerplatz gibt.
    * Die nächste Zeile, mit **Einlagerung** in der **Aktionsart** zeigt an, wo Sie die Artikel im Lager einlagern müssen. Sie können die Zone und den Lagerplatz in dieser Zeile nicht ändern.

    > [!NOTE]
    > Wenn Sie die Artikel für eine Zeile in mehr als einem Lagerplatz kommissionieren oder platzieren müssen, beispielsweise, da der freie Lagerplatz voll ist, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.
        
    Sie können die Kommissionierzeilen nach verschiedenen Kriterien sortieren, beispielsweise nach Artikel, Regalnummer, Lagerplatz oder Fälligkeitsdatum. Die Sortierung kann helfen, den Einlagerungsprozess zu optimieren, zum Beispiel:

    * Wenn die Entnahme- und Einlagerungszeilen einer Warenausgangszeile nicht direkt aufeinander folgen, Sie dies aber wünschen, sortieren Sie die Zeilen, indem Sie **Artikel** im Feld **Sortiermethode** auswählen.  
    * Wenn Lagerplatzränge das physische Layout des Lagers widerspiegeln, verwenden Sie die Sortiermethode **Lagerplatzrang**, um die Arbeit nach Lagerplatzlagerorten zu organisieren.

  > [!NOTE]  
  > Die Zeilen sind in der Reihenfolge der ausgewählten Kriterien aufsteigend sortiert. Wenn Sie nach Belegen sortieren, erfolgt die Sortierung zunächst nach Belegart basierend auf dem Feld **Quellbeleg der Lageraktivität**. Wenn Sie nach Lieferadresse sortieren, erfolgt die Sortierung zuerst nach Zieltyp basierend auf dem Feld **Lagerzieltyp**.

4. Nachdem Sie die Kommissionierung ausgeführt und die Artikel in den Ausgangsbereich oder den Ausgangslagerplatz eingelagert haben, wählen Sie die Aktionen **Kommissionierung registrieren** aus.  

Sie können die Artikel in den Warenausgang bringen und den Warenausgang, einschließlich dem zugehörigen Herkunftsbeleg, auf der Seite **Warenausgang** buchen. Erfahren Sie mehr unter [Elemente versenden](warehouse-how-ship-items.md).

## Siehe auch

- [Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
- [Verwalten des Lagerbestands](inventory-manage-inventory.md)  
- [Einrichten von Warehouse Management](warehouse-setup-warehouse.md)     
- [Montageverwaltung](assembly-assemble-items.md)    
- [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
