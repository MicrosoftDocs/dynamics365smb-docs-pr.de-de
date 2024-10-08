---
title: Kommissionierung für interne Arbeitsgänge in erweiterter Lagerkonfigurationen
description: 'Wenn Ihre Standorte Kommissionierung und Versand verwenden, kommissionieren Sie Komponenten für Produktion, Montage und Projektaktivitäten auf der Seite „Lagerkommissionierung“.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 08/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="pick-for-production-assembly-or-projects-in-advanced-warehouse-configurations"></a>Kommissionieren für Produktion, Montage oder Projekte in erweiterten Lagerkonfigurationen

Wie Sie Komponenten für die Produktion, Projekte oder Montageaufträge kommissionieren, hängt davon ab, wie Ihr Lager als Standort eingerichtet ist. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).

Verwenden Sie in einer erweiterten Lagerkonfiguration für den ausgehenden Fluss (Kommissionierung) auf der Seite  **Standort Karte**  für den Standort die folgenden Einstellungen:

* Produktion, im Feld  **Produktionsverbrauch – Lagerabwicklung**, Auswählen **Lagerkommissionierung (optional)**  oder  **Lagerkommissionierung (obligatorisch)**.
* Montage, im Feld  **Montageverbrauch Lagerabwicklung**, Auswählen **Lagerkommissionierung (optional)**  oder  **Lagerkommissionierung (obligatorisch)**.
* Projektmanagement, im Feld  **Projektverbrauch – Lagerabwicklung**, Auswählen **Lagerkommissionierung (optional)**  oder  **Lagerkommissionierung (obligatorisch)**.

Wenn für den Lagerort eine Kommissionierung erforderlich ist, erstellen und verarbeiten Sie Kommissionierinformationen mithilfe von Kommissionierbelegen, bevor Sie die Verwendung oder den Verbrauch von Komponenten buchen.  

Sie können keine Lagerkommissionierbelege von Grund auf erstellen. Kommissionierungen sind Teil eines Workflows, bei dem eine Person, die einen Auftrag bearbeitet, sie im Push-Verfahren erstellt, oder der Lagermitarbeiter sie im Pull-Verfahren erstellt:

- Im Push-Verfahren, bei dem Sie die Aktion **Kommissionierung erstellen** auf der Seite **Produktionsauftrag**, **Montageauftrag**, **Projektkarte**. Wählen Sie die zu kommissionierenden Zeilen und bereiten Sie die Kommissionierungen vor, indem sie beispielsweise angeben, aus welchen Lagerplätzen entnommen und in welche Lagerplätze eingelagert wird, und wie viele Einheiten bewegt werden. Lagerplätze können für den Lagerort oder die Ressource vordefiniert werden.
- Im Pull-Verfahren, bei dem Sie **Produktionsauftrag**, **Montageauftrag**, **Projektkarte** für das Lager freigeben, wodurch die Artikel für die Entnahme verfügbar gemacht werden. Anschließend können Lagermitarbeiter auf der Seite **Kommissionierungsarbeitsblatt** die Aktion **Lagerdokumente abrufen** verwenden, um ihre zugewiesenen Kommissionierungen vorzunehmen.

Um Komponenten für Herkunftsbelege im Pull-Verfahren zu kommissionieren oder zu verschieben, müssen Sie das Herkunftsbeleg freigeben, um es für die Entnahme bereit zu machen. Die Freigabe von Herkunftsbelegen für interne Arbeitsgänge geschieht auf die folgenden Arten.  

|Herkunftsbeleg|Freigabeverfahren|  
|---------------------|--------------------|  
|Produktionsauftrag|Ändern Sie den Auftragsstatus auf Freigegeben, oder erstellen Sie gleich einen freigegebenen Fertigungsauftrag.|  
|Montageauftrag|Änderung des Status in "Freigegeben".|
|Projekte | Ändern Sie den Status auf „Offen“ oder erstellen Sie sofort ein Projekt mit dem Status „Offen“.|  

## <a name="production"></a>Fertigung

Verwenden Sie **Lagerkommissionierungsdokumente** für die Kommissionierung von Produktionskomponenten im Fluss zur Produktion.

Für einen Lagerort, der Lagerplätze verwendet, um Artikel in offenem Lagerplätze im Fertigungsbereich zu verschieben, können Sie die folgenden Methoden verwenden:

* Befolgen Sie für einen Lagerort, der gesteuertes Einlagern und Kommissionieren verwendet, die Schritte im Artikel [Artikel in erweiterten Lagerkonfigurationen verschieben](warehouse-how-to-move-items-in-advanced-warehousing.md).
* Befolgen Sie für andere Lagerorte die Schritte im Artikel [Interne Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## <a name="assembly"></a>Montage

Verwenden Sie **Lagerentnahme**-Dokumente, um Montagekomponenten zum Montagebereich zu bewegen.

[!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Lagermontage und Auftragsmontage-Typen von Montageflüssen. Weitere Informationen zur Auftragsmontage im ausgehenden Lagerfluss finden Sie unter [Handhabung von Auftragsmontageartikeln in Lagerlieferungen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Projektmanagement

Verwenden Sie  **Lagerkommissionierungs** Dokumente, um Projektkomponenten im Ablauf zum Projektmanagement zu kommissionieren.

> [!NOTE]
> Projekte unterstützen keine erweiterten Konfigurationen, bei denen die Option  **Gezielte Kommissionierung und Einlagerung**  aktiviert ist.

## <a name="check-whether-items-are-available-for-picking"></a>Prüfen Sie, ob Artikel zur Kommissionierung verfügbar sind

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>So erstellen Sie Kommissionierungsdokumente mit dem Kommissionierungsarbeitsblatt in Masse

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kommissionierarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Logistikbeleg holen** Aktion aus.  

    In der Liste werden die freigegebenen Produktions-, Projekt- und Montageaufträge angezeigt, die an die Kommissionierfunktion weitergeleitet wurden. Zu den Aufträgen zählen auch solche, für die bereits Kommissionieranweisungen erstellt wurden. Belege mit Kommissionierungszeilen, die bereits kommissioniert und registriert wurden, werden in dieser Übersicht nicht angezeigt.  
3. Wählen Sie die Aufträge, für die Sie eine Kommissionierung vorbereiten möchten.

    > [!NOTE]  
    > Wenn Sie einen Beleg auswählen, das bereits Anweisungen für alle Zeilen enthält, informiert Sie [!INCLUDE [prod_short](includes/prod_short.md)] darüber, dass nichts zu bearbeiten ist. Um die bereits erstellten Kommissionierungsanweisungen in einer Kommissionierungsanweisung zu kombinieren, müssen Sie zunächst die einzelnen Kommissionierungen löschen.

4. Füllen Sie das Feld **Sortiermethode** aus, um die Zeilen nach Wunsch zu sortieren.  

    > [!NOTE]  
    > Die Art und Weise, wie die Zeilen im Arbeitsblatt sortiert sind, überträgt sich nicht automatisch auf die Entnahmeanweisung. Es sind jedoch die gleichen Sortierwerkzeuge verfügbar, zusammen mit der Lagerplatzrangfolge. Sie können die Reihenfolge der Zeilen, die Sie im Arbeitsblatt erstellen, leicht neu erstellen, wenn Sie die Kommissionierungsanweisungen erstellen oder indem Sie die Kommissionierungsanweisungen sortieren.

5. Füllen Sie das Feld **Bewegungsmenge** aus. Wählen Sie die **Bewegungsmenge autom. ausfüllen** Aktion aus, oder füllen Sie die Felder manuell aus.  

    Die Seite zeigt die in Cross-Docking-Lagern verfügbaren Mengen an, was für die Planung von Arbeitseinsätzen in Cross-Docking-Situationen nützlich ist. [!INCLUDE[prod_short](includes/prod_short.md)] wird immer zuerst eine Entnahme aus einem Cross-Dock-Behälter vorschlagen.

6. Bearbeiten Sie diese Positionen bei Bedarf manuell. Sie können auch einige der Zeilen löschen, um die Kommissionierung effektiverer zu machen. Wenn es z. B. mehrere Zeilen mit Artikeln in Zuordnungslagerplätzen gibt, möchten Sie möglicherweise eine Kommissionierung für alle Zeilen erzeugen, die mit all diesen Zeilen zusammenhängen. Die Crossdocking-Artikel werden mit anderen Artikeln im Herkunftsbeleg kommissioniert und die Crossdocking-Lagerplätze haben wieder Platz für neue ankommende Artikel.

    > [!NOTE]  
    >  Die Zeilen werden nur aus diesem Arbeitsblatt gelöscht, nicht aus der Kommissionierungsauswahlliste.  

7. Wählen Sie die Aktion **Kommissionierung erstellen** aus. Die Seite **Kommissionierung erstellen** wird geöffnet, auf der Sie der Auswahl weitere Informationen hinzufügen können.  

    Geben Sie an, wie Kommissionierungszeilen in den Kommissionierungsbelegen kombiniert werden sollen, indem Sie eine der folgenden Optionen auswählen.  

    |Option|Beschreibung|
    |-|-|
    |Nach Lager. Beleg|Erstellt separate Kommissionierungsbelege für Arbeitsblattzeilen mit demselben Lagerherkunftsbeleg.|
    |Nach Deb./Kred./Lagerort|Erstellt separate Kommissionierbelege für jeden Kunden (jedes Projekt)|
    |Nach Artikel|Erstellt separate Kommissionierungsbelege für jeden Artikel im Kommissionierungs-Arbeitsblatt.|
    |Nach Zone|Erstellt separate Kommissionierungsbelege für jede Zone, aus der Sie die Artikel entnehmen.|
    |Nach Lagerplatznr.|Erstellt separate Kommissionierungsbelege für jeden Lagerplatz, von dem Sie die Artikel entnehmen.|
    |Nach Fälligkeitsdatum|Erstellt separate Kommissionierungsbelege für Herkunftsbelege, die das gleiche Fälligkeitsdatum haben.|

    Verwenden Sie die folgenden Optionen, um anzugeben, wie die Kommissionierbelege erstellt werden sollen.  

    |Option|Description|
    |-|-|
    |Max. Anz. der Kommissionierungszeilen|Erstellt Kommissionierbelege, die in jedem Beleg nicht mehr als die angegebene Anzahl von Zeilen haben.|
    |Max. Anz. der Kommissionierungsherkunftsbelege|Erstellt Kommissionierungsbelege, die bis zu der angegebene Anzahl von Herkunftsbelegen einschließt.|
    |Zugewiesene Benutzer-ID|Erstellt Kommissionierungsbelege nur für Arbeitsblattzeilen, die dem ausgewählten Lagermitarbeiter zugeordnet sind.|
    |Sortiermethode für Kommissionierzeilen|Wählen Sie aus den verfügbaren Optionen aus, um Zeilen im erstellten Kommissionierungsbeleg zu sortieren.|
    |Gebindeanbruchsfilter verw.|Blendet Gebindeanbruch-Kommissionierungszeilen aus, wenn eine größeren Einheit in eine kleinere Einheit umgewandelt und kommissioniert wird.|
    |Bewegungsmenge nicht ausfüllen|Lässt das Feld **Bewegungsmge** auf den erstellten Kommissionierungszeilen leer.|
    |Kommissionierschein drucken|Druckt die Kommissionierbelege, wenn diese erstellt werden. Sie können auch aus den erstellten Kommissionierungsbelegen drucken.|

8. Wählen Sie die Schaltfläche **OK**.  

## <a name="to-pick-items-for-a-production-order-assembly-order-or-project"></a>So kommissionieren Sie Artikel für einen Fertigungsauftrag, einen Montageauftrag oder ein Projekt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kommissionierungen** ein und wählen Sie dann den zugehörigen Link.  

    Wenn Sie an einer bestimmten Kommissionierung arbeiten möchten, wählen Sie die Kommissionierung in der Liste aus, oder filtern Sie die Liste, um die Kommissionierungen zu finden, die Ihnen zugeordnet wurden. Öffnen Sie die Kommissionierungskarte.  
2. Wenn das Feld **Zugewiesene Benutzer-ID** leer ist, geben Sie gegebenenfalls Ihre ID ein, um sich zu identifizieren.  
3. Kommissionieren Sie die Artikel.  

    Wenn das Lager für die Verwendung von Lagerplätzen eingerichtet wurde, werden die Vorgabelagerplätze der Artikel als Vorschlag für den Entnahmeort verwendet. Die Anweisungen enthalten mindestens zwei separate Zeilen für jede der Aktionen Entnahme und Einlagerung.  

    Betriebsbereiche wie Produktionshallen verfügen möglicherweise über einen Standardlagerplatz für die benötigten Komponenten. Wenn dies der Fall ist, wird der Standard-Lagerplatzcode zum Lagerentnahmedokument hinzugefügt, um anzugeben, wo die Artikel abgelegt werden sollen. Weitere Informationen finden Sie in den QuickInfos zu den Feldern  **Beginn-Produktionslagerplatzcode**,  **Beginn-Montagelagerplatzcode** und  **Beginn-Projektlagerplatzcode** .

    Wenn das Lager mit gesteuerter Einlagerung und Kommissionierung eingerichtet wurde, werden die Lagerplatzränge verwendet, um die besten Lagerplätze für die Kommissionierung zu berechnen. Diese Lagerplätze werden in den Kommissionierungszeilen vorgeschlagen. Die Anweisungen enthalten mindestens zwei separate Zeilen für jede der Aktionen Entnahme und Einlagerung.  

    * Die erste Zeile mit dem Feld **Entnahme** im Feld **Aktionsart** zeigt an, wo sich die Artikel im Kommissionierungsbereich befinden. Wenn Sie eine große Menge an Artikeln in einer Lieferzeile liefern, müssen Sie möglicherweise die Artikel in mehrere Lagerplätze kommissionieren, damit es eine Zeile der Art Auslagerung für jeden Lagerplatz gibt.
    * Die nächste Zeile, mit **Einlagerung** in der **Aktionsart** zeigt an, wo Sie die Artikel im Lager einlagern müssen. Sie können die Zone und den Lagerplatz in dieser Zeile nicht ändern.

    > [!NOTE]
    > Wenn Sie die Artikel für eine Zeile in mehr als einem Lagerplatz kommissionieren oder platzieren müssen, beispielsweise, da der freie Lagerplatz voll ist, verwenden Sie die Aktion **Zeile aufteilen** im Inforegister **Zeilen**. Die Aktion erstellt eine Zeile für die zu bearbeitende Restmenge.

      Sie können die Kommissionierzeilen nach verschiedenen Kriterien sortieren, beispielsweise nach Artikel, Regalnummer, Lagerplatz oder Fälligkeitsdatum. Die Sortierung kann helfen, den Einlagerungsprozess zu optimieren, zum Beispiel:

    * Wenn die Zeilen der Art Entnahme und Einlagerung einer Warenausgangszeile nicht direkt aufeinander folgen, Sie dies aber wünschen, sortieren Sie die Zeilen, indem Sie **Artikel** im Feld **Sortiermethode** auswählen.  
    * Wenn Lagerplatzränge das physische Layout des Lagers widerspiegeln, verwenden Sie die Sortiermethode **Lagerplatzrang**, um die Arbeit nach Lagerplatzlagerorten zu organisieren.

  > [!NOTE]  
  > Die Zeilen sind in der Reihenfolge der ausgewählten Kriterien aufsteigend sortiert. Wenn Sie nach Belegen sortieren, erfolgt die Sortierung zunächst nach Belegart basierend auf dem Feld **Quellbeleg der Lageraktivität**. Wenn Sie nach Lieferadresse sortieren, erfolgt die Sortierung zuerst nach Zieltyp basierend auf dem Feld **Lagerzieltyp**.

4. Nachdem Sie die Artikel kommissioniert und im Produktions-, Montage- oder Projektbereich bzw. Lagerplatz platziert haben, wählen Sie die Aktion  **Kommissionierung registrieren**  aus.  

    Sie können nun die Artikel in den entsprechenden Bereich bringen und die Verwendung oder den Verbrauch der kommissionierten Komponenten buchen, indem Sie die Verbrauchserfassung, den Montageauftrag oder die Projekterfassung buchen. Die folgenden Artikel bieten weitere Informationen:

    * [Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile](production-how-to-register-consumption-and-output.md)
    * [Artikel montieren](assembly-how-to-assemble-items.md)
    * [Verbrauch oder Nutzung für Projekt erfassen](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Buchung von Produktionskomponenten in einer erweiterten Lagerkonfiguration

Die Buchungsmethoden beeinflussen den Fluss der Komponenten in der Produktion. Weitere Informationen finden Sie unter [Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md). Abhängig von der gewählten Buchungsmethode können Sie Komponenten für die Produktion auf folgende Weise kommissionieren:

* Verwenden Sie ein **Lagerenkommissionierungs**-Dokument , um die Kommissionierung für Artikel aufzuzeichnen, die die **Manuelle** Buchungsmethode verwenden. Den Verbrauch müssen Sie separat anmelden. Weitere Informationen finden Sie unter [Produktionsverbrauch mit Stapelverarbeitung buchen](production-how-to-post-consumption.md).
* Verwenden Sie ein **Lagerkommissionierungs**-Dokument , um die Kommissionierung für Artikel aufzuzeichnen, die die Buchungsmethode **Kommissionnieren + vorwärts**, **Kommissionieren + rückwärts** verwenden. Der Verbrauch der Komponenten erfolgt automatisch, wenn Sie entweder den Status des Produktionsauftrags ändern oder einen Vorgang starten oder beenden. Alle benötigten Komponenten müssen verfügbar sein. Andernfalls stoppt das Buchen geleerten Verbrauchs für diese Komponente.
* Verwenden Sie einen **Lagerplatzumlagerungs**-Beleg ohne eine Referenz, um einen Herkunftsbeleg oder andere Methoden, um die Umlagerung von Komponenten aufzuzeichnen, die die Buchungsmethode **Vorwärts** oder **Rückwärts** verwenden. Komponenten werden automatisch verbraucht, wenn Sie sie entweder den Status des Produktionsauftrags ändern oder einen Vorgang starten oder beenden. Alle benötigten Komponenten müssen verfügbar sein. Andernfalls stoppt das Buchen geleerten Verbrauchs für diese Komponente. Erfahren Sie mehr unter [Artikel umlagern](warehouse-move-items.md).

### <a name="example"></a>Beispiel

Sie haben einen Fertigungsauftrag für 15 STÜCK des Artikels SP-SCM1004. Einige der Artikel auf der Komponentenliste müssen manuell in ein Verbrauchsjournal gebucht werden. Andere Artikel können mit der Buchungsmethode **Kommissionieren + Rückwärts** entnommen und automatisch gebucht werden.  

Die folgenden Schritte beschreiben die entsprechenden Aktionen, die von verschiedenen Personen genutzt werden, und die entsprechende Reaktion:  

1. Der Fertigungsbereichsvorgesetzte gibt den Fertigungsauftrag frei. Artikel mit der Buchungsmethode **Vorwärts** und keiner Arbeitsplanverknüpfung werden vom Off. Fert.-Ber.-Lagerplatz. abgezogen.  
2. Der Fertigungsbereichsvorgesetzte wählt die Aktion **Kommissionierung erstellen** auf dem Fertigungsauftrag aus. Ein Lager-Kommissionierbeleg wird für die Kommissionierung von Artikel mit den Buchungsmethoden **Manuell**, **Kommiss. + Rückwärts** und **Kommiss. + Vorwärts** erstellt. Diese Artikel werden in den Fert.-Bereitst.-Lagerplatzcode aufgeführt.  
3. Der Lagermanager weist einem Lagermitarbeiter die Kommissionierungen zu.  
4. Der Lagermitarbeiter kommissioniert die Artikel aus den jeweiligen Lagerplätzen und platziert sie im Fert.-Bereitst.-Lagerplatzcode oder in dem Lagerplatz. Der Lagerplatz kann der Lagerplatz eine Arbeitsplatzgruppe oder eines Arbeitsplatzes sein.
5. Der Lagermitarbeiter registriert die Kommissionierung. Die Menge wird vom Kommissionierlagerplatz zum Verbrauchslagerplatz transferiert. Das Feld **Menge kommissioniert** auf der Komponentenliste für alle kommissionierten Artikel wird aktualisiert.

    > [!NOTE]  
    >  Nur die kommissionierte Menge kann verbraucht werden.  
6. Der Maschinist informiert den Produktionsleiter, dass die Endartikel fertig sind.
7. Der Fertigungsleiter verwendet das Verbrauchs Buch.-Blatt oder das Produktions Buch.-Blatt, um den Verbrauch von Komponenten zu buchen, die ein der Buchungsmethoden **Manuell** verwenden.
8. Der Fertigungsleiter verwendet die Ausgabeerfassung oder die Produktionserfassung, um die Istmeldung zu buchen. Die Menge der Komponentenartikel, die die Buchungsmethoden **Kommissionieren + Vorwärts** oder **Kommissionieren + Rückwärts** mit Arbeitsplanlinks verwenden, wird vom Fert.-Bereitst.-Lagerplatz abgezogen.
9. Der Produktionsleiter ändert den Status des Fertigungsauftrags zu **Beendet**. Die Menge der Komponenten, die die Buchungsmethode **Rückwärts** verwenden, wird vom Off. Fert.-Ber.-Lagerplatz.abgezogen, und die Menge der Komponenten, die die Buchungsmethode **Kommiss. + Rückwärts** verwenden wird vom Fert.-Bereitst.-Lagerplatz abgezogen und kein Arbeitsplanlink wird vom Fert.-Bereitst.-Lagerplatzcode abgezogen.  

Die folgende Abbildung zeigt, wann das Feld **Lagerplatzcode** auf der Komponentenliste entsprechend Ihrer Lagerort- oder Arbeitsplatzeinrichtung gefüllt wird.  

:::image type="content" source="media/binflow.png" alt-text="Übersicht, wann und wie das Feld Lagerplatz ausgefüllt wird.":::

## <a name="make-to-order-mto-production-components-in-an-advanced-warehouse-configuration"></a>Produktionskomponenten der Auftragsfertigung in einer erweiterten Lagerkonfiguration

In Szenarien, in denen ein produzierter Artikel aus Rohmaterialien und Halbfertigerzeugnissen besteht und die Produktionsrichtlinie auf **Auftragsfertigung** eingestellt ist, wird die Lagerkommissionierung für diese Halbfertigkomponenten demselben Fertigungsauftrag hinzugefügt, wobei das Feld **Planungsebenennr.** ausgefüllt ist. Es wird erwartet, dass die Halbfertigerzeugnisse sofort zum Verbrauch verfügbar sind und nicht kommissioniert werden müssen. Daher werden sie nicht in den Lagerkommissionierbeleg aufgenommen. Die erstellten Lagerkommissionierungen umfassen nur Rohstoffe für Fertig- und Halbfertigerzeugnisse.

Wenn jedoch Halbfertigerzeugnisse auf Lager sind, schlägt das Planungssystem vor, diese zu verbrauchen, anstatt die gesamte Menge zu produzieren. Angenommen, für die Produktion eines Artikels werden fünf Halbfertigkomponenten benötigt, von denen jedoch drei bereits auf Lager sind. In diesem Fall werden in den Fertigungsauftragskomponenten fünf Halbfertigerzeugnisse aufgeführt, jedoch nur zwei davon im selben Fertigungsauftrag als separate Fertigungsauftragszeile produziert.
Eine solche Konfiguration ist nicht mit der Lagerkommissonierung kompatibel und Sie müssen, je nach der Häufigkeit, entweder die Produktionsrichtlinie für solche Halbfertigerzeugnisse auf **Auftragsfertigung** ändern oder die Komponentenzeile des Fertigungsauftrags manuell aufteilen, wenn Sie die zuvor produzierten Halbfertigerzeugnisse kommissionieren müssen.


## <a name="see-also"></a>Siehe auch

- [Verwalten des Lagerbestands](inventory-manage-inventory.md)  
- [Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
- [Montageverwaltung](assembly-assemble-items.md)  
- [Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
- [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
