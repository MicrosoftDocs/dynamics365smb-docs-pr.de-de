---
title: Informationen zu Fertigungsaufträgen
description: Erfahren Sie mehr über Produktionsaufträge und wie diese zur Verwaltung der Umwandlung von gekauften Materialien in gefertigte Artikel verwendet werden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-production-orders"></a>Informationen zu Fertigungsaufträgen

Fertigungsaufträge werden dazu verwendet, die Umwandlung von Einkaufsmaterialien in Produktionsartikel zu verwalten. Fertigungsaufträge (Arbeits- oder Werkaufträge) leiten Arbeit durch verschiedene Einrichtungen (Arbeitsplätze oder Arbeitsplatzgruppen) im Fertigungsbereich.  

Bevor sie mit der Produktion fortfahren, führen die meisten Unternehmen eine Beschaffungsplanung aus, in der Regel einmal wöchentlich, um zu berechnen wie viele Fertigungsaufträge und Einkaufsbestellungen auszuführen sind, um den Verkaufsbedarf diese Woche zu erfüllen. Einkaufsbestellungen liefern die Komponenten, die nach der Fertigungsstückliste erforderlich sind, um die Endartikel zu fertigen.

Fertigungsaufträge sind die zentralen Komponenten der Fertigungsfunktionen und enthalten die folgenden Informationen:  

- Produkte, die für die Fertigung geplant sind  
- Materialien, die für die geplanten Fertigungsaufträge erforderlich sind  
- Produkte, die gefertigt wurden  
- Materialien, die bereits ausgewählt wurden  
- Produkte, die in der Vergangenheit gefertigt wurden  
- Materialien, die in früheren Fertigungsvorgängen verwendet wurden  

Fertigungsaufträge sind die Ausgangspunkte für:  

- Planen der zukünftigen Fertigung  
- Überwachen der aktuellen Fertigung  
- Verfolgen der abgeschlossenen Fertigung  

## <a name="production-order-creation"></a>Fertigungsauftrag erstellen

Sie können Fertigungsaufträge auftragsweise manuell auf der Seite **Fertigungsauftrag** erstellen, oder über die Seiten **Verkaufsauftragsplanung** oder **Auftragsplanung** generieren. Sie können auch mehrere Aufträge über die Seite **Planungsarbeitsblatt** erstellen.  

Sie erstellen Fertigungsaufträge anhand der Informationen aus:  

- Artikel  
- Produktionsstücklisten
- Arbeitspläne  
- Arbeitsplätze  
- Arbeitsplatzgruppen  

## <a name="limitations-on-creating-production-orders"></a>Einschränkungen für das Erstellen von Fertigungsaufträgen

Ein Fertigungsauftrag wird automatisch reserviert und zu seinem Ursprung verfolgt, wenn:  

- Er aus dem [Planungsarbeitsblatt](production-how-to-run-mps-and-mrp.md) erstellt wurde  
- Erstellung auf der Seite [Verkaufsuftragsplanung](production-how-to-create-production-orders-from-sales-orders.md)  
- Wurde aus der Seite [Auftragsplanung](production-how-to-plan-for-new-demand.md) erstellt  
- Die Funktion [Neu planen](production-how-to-replan-refresh-production-orders.md) für Fertigungsaufträge verwendet wird  

Weitere Informationen finden Sie unter [Titel-Beziehungen zwischen Bedarf und Vorrat nachverfolgen](production-how-track-demand-supply.md).

Fertigungsaufträge, die auf andere Weise erstellt wurden, werden nicht automatisch reserviert und verfolgt.

## <a name="production-order-status"></a>Fertigungsauftragsstatus

Über den Fertigungsauftragsstatus wird gesteuert, wie sich der Fertigungsauftrag in der Anwendung sich verhält. Form und Inhalt der Produktion werden durch den Status des Auftrags festgelegt. Je nach Status werden die Fertigungsaufträge auf verschiedenen Seiten angezeigt. Sie können den Status eines Fertigungsauftrags nicht manuell ändern. Sie müssen die Funktion **Status ändern** im einzelnen Fertigungsauftrag oder auf der Seite **Fertigungsauftragsstatus ändern** verwenden.  

### <a name="simulated-production-order"></a>Simulierter Fertigungsauftrag

Ein simulierter Fertigungsauftrag ist eindeutig, basierend auf den folgenden Eigenschaften:  

- Wie der Name schon sagt, handelt es sich um eine Simulation, die Sie für Angebote und Kostenkalkulationen verwenden können. Zum Beispiel, wenn die Forschungs- und Entwicklungsabteilung einen Kostenvoranschlag für einen vorgeschlagenen Artikel einholen möchte. Ein simulierter Fertigungsauftrag fungiert als Beispiel eines Fertigungsauftrages.  
- Er hat keinerlei Auswirkungen auf die Planung von Aufträgen. Simulierte Fertigungsaufträge werden weder von einer Planung (Prod.-Programmplanung und Nettobedarf) berücksichtigt, noch wirken sie sich auf eine Planung aus. Außerdem kann ein simulierter Fertigungsauftrag nicht als Vorlage verwendet werden, weil er gelöscht wird, sobald Sie seinen Status geändert haben.  

### <a name="planned-production-order"></a>Geplanter Fertigungsauftrag

Ein geplanter Fertigungsauftrag zeichnet sich durch folgende Eigenschaften aus:  

- Sie können einen geplanten FA automatisch aus einem Verkaufsauftrag erstellen.  
- Ein geplanter Fertigungsauftrag ist wie ein freigegebener Fertigungsauftrag und stellt Informationen für die Kapazitätsplanung bereit, indem er die Kapazitätsanforderungen nach Arbeitsplatz oder Arbeitsplatzgruppe zeigt.  
- Ein geplanter Fertigungsauftrag entspricht der besten Schätzung der zukünftigen Auslastung des Arbeitsplatzes oder der Arbeitsplatzgruppe auf Basis der verfügbaren Informationen. Üblicherweise wird ein geplanter FA aus den Planungsinformationen generiert, er kann aber auch manuell erstellt werden. Da ein geplanter FA während der Generierung späterer Planungsschritte gelöscht wird, ist eine manuelle Erstellung nicht empfehlenswert.  
- Die Generierung eines geplanten FA ergibt eine vorgeschlagene "voraussichtliche Auftragsfreigabe", die die Menge, das Freigabedatum und das Fälligkeitsdatum enthält. Die Logik des Planungssystems basiert auf der Beschaffungsmethode, den Wiederbeschaffungsverfahren und den Auftragsmodifikationen, die im Planungsvorgang für den Nettobedarf festgelegt wurden.  
- Wenn Sie die Auswirkungen eines geplanten FA wissen möchten, sehen Sie sich auf dem Arbeitsplan des geplanten FA die Auslastung für jeden Arbeitsplatz oder jede Arbeitsplatzgruppe an.  

### <a name="firm-planned-production-order"></a>Fest geplanter Fertigungsauftrag

Ein fest geplanter Fertigungsauftrag (FA) ist eindeutig und zeichnet sich durch folgende Eigenschaften aus:  

- Sie können einen fest geplanten FA automatisch aus einem Verkaufsauftrag erstellen.  
- Ein fest geplanter FA fungiert im Planungsschema für einige zukünftige Projekte, die für die Fertigung freigegeben wurden, als Platzhalter.  
- Ein fest geplanter FA kann aus Planungsinformationen generiert oder manuell aus Verkaufsaufträgen erstellt werden. Er wird im weiteren Verlauf der Planung nicht gelöscht.  
- Die Generierung eines fest geplanten FA ergibt eine vorgeschlagene "voraussichtliche Auftragsfreigabe", die die Menge, das Freigabedatum und das Fälligkeitsdatum enthält. Die Logik des Planungssystems basiert auf der Beschaffungsmethode, den Wiederbeschaffungsverfahren und den Auftragsmodifikationen, die im Planungsvorgang für den Nettobedarf festgelegt wurden.  
- Wenn Sie die Auswirkungen eines fest geplanten FA wissen möchten, sehen Sie sich auf dem Arbeitsplan des fest geplanten FA die Auslastung für jeden Arbeitsplatz oder jede Arbeitsplatzgruppe an.  

### <a name="released-production-order"></a>Freigegebener Fertigungsauftrag

Der freigegebene Fertigungsauftrag (FA) ist eindeutig, basierend auf den folgenden Eigenschaften:  

- Sie können einen freigegebenen FA automatisch aus einem Verkaufsauftrag erstellen.  
- Wenn ein Fertigungsauftrag freigegeben wird, heißt dies nicht notwendigerweise, dass Materialien kommissioniert werden oder das Projekt physisch zu seinem ersten Arbeitsgang verschoben wurde.  
- In einem Unternehmen mit Auftragsfertigung kann es üblich sein, einen freigegebenen FA unmittelbar nach Eingang eines Verkaufsauftrags zu erstellen.  
- Der tatsächliche Materialverbrauch und die tatsächlichen Istmeldungen können mit einem freigegebenen FA erfasst werden. Außerdem kann automatisches Buchen von Verbrauch und Istmeldungen nur für freigegebene Fertigungsaufträge erfolgen.  

### <a name="finished-production-order"></a>Beendeter Fertigungsauftrag

Ein beendeter Fertigungsauftrag (FA) ist eindeutig, basierend auf den folgenden Eigenschaften:  

- Ein beendeter FA ist üblicherweise ein FA, dessen Artikel gefertigt ist.  
- Das Beenden eines Fertigungsauftrages ist eine wichtige Aufgabe beim Abschließen der Gesamtkostenbewertung des Artikels, der gefertigt wird. Nach dem Beenden eines Fertigungsauftrages können Sie die Bewertung anpassen und abstimmen.  
- Beendete Fertigungsaufträge werden für die Erstellung von statistischen Berichten sowie als Unterstützung für die Möglichkeit verwendet, eine Rückverfolgung zu anderen Aufträgen (z. B. Verkaufsaufträge, Fertigungsaufträge und Einkaufsbestellungen) auszuführen. Die Möglichkeit, eine Rückverfolgung zu einem beendeten FA auszuführen, versetzt Sie in die Lage, die genaue Historie nachzuvollziehen.  
- Ein beendeter FA kann nicht geändert werden.  

## <a name="production-order-execution"></a>Fertigungsauftrag ausführen

Sobald Sie einen Fertigungsauftrag erstellt und geplant haben, muss er für den Fertigungsbereich freigegeben werden, damit er ausgeführt wird. Während des Ausführens des Auftrags erfassen Sie Folgendes:  

- Die Materialien, die kommissioniert oder verbraucht wurden  
- Die Zeit, die für das Abarbeiten des Auftrags benötigt wurde  
- Die Menge des gefertigten übergeordneten Artikels  

Sie können diese Informationen manuell oder über die automatische Berichterstellung erfassen. Die Methode hängt von der Einrichtung im Feld „Buchungsmethode“ des Artikels und des Arbeitsplatzes ab.  

### <a name="material-consumption"></a>Materialverbrauch

[!INCLUDE [prod_short](includes/prod_short.md)] bietet verschiedene Möglichkeiten zur Erfassung des Materialverbrauchs. Beispielsweise kann es vorteilhaft sein, den Materialverbrauch manuell zu erfassen, weil häufig Komponenten ersetzt werden oder der Ausschuss größer ist als erwartet.  

Der Verbrauch von Materialien kann über das [Verbrauchs Buch.-Blatt](production-how-to-post-consumption.md) verarbeitet werden, kann aber auch automatisch von [!INCLUDE [prod_short](includes/prod_short.md)] erfasst werden. Dies wird als automatische Berichterstellung (Buchen) bezeichnet. Es stehen die Berichtsmethoden „Manuell“, „Vorwärts“ und „Rückwärts“ zur Verfügung.

Die manuelle Verbrauchsberichterstellung verwendet "FA-Verbrauchs Buch.-Blatt", um die Materialkommissionierung anzugeben.  

Bei der Verbrauchsberichterstellung vom Typ "Vorwärts" wird davon ausgegangen, dass die erwarteten Mengen aller Materialien für den gesamten Auftrag bei der Freigabe eines Fertigungsauftrags verbraucht werden, sofern keine Verbindungscodes verwendet werden. Bei Verwendung von Verbindungscodes werden die Materialien, die nach dem Beginn des Fertigungsschrittes verbraucht werden, im „FA-Istmeldungs Buch.-Blatt“ erfasst. Soll der gesamte Fertigungsauftrag vorwärts gebucht werden, müssen die beiden folgenden Bedingungen erfüllt sein:  

- Für jeden Artikel in der Produktionsstückliste der obersten Ebene muss auf seiner Artikelkarte die Buchungsmethode "Vorwärts" ausgewählt sein.  
- Aus der Produktionsstückliste müssen alle Verbindungscodes entfernt worden sein.  

Bei der Verbrauchsberichterstellung vom Typ "Rückwärts" werden die tatsächlichen Mengen aller kommissionierten oder verbrauchten Materialien erfasst, sobald sich der Status eines Fertigungsauftrags in *Beendet* geändert hat und sofern keine Verbindungscodes verwendet werden. Bei Verwendung von Verbindungscodes werden die Materialien verbraucht, nachdem eine Menge des übergeordneten Artikels für den Fertigungsschritt im „FA-Istmeldungs Buch.-Blatt“ erfasst wurde.  

Wird der Fertigungsauftrag aktualisiert, wird die Buchungsmethode von der Artikelkarte kopiert. Da die Buchungsmethode für jede Komponente eines Fertigungsauftrags steuert, wie und wann der Verbrauch erfasst wird, sollten Sie wissen, dass Sie die Buchungsmethode für bestimmte Artikel direkt auf dem „Fertigungsauftrag“ ändern können. Weitere Informationen finden Sie unter [Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).

### <a name="production-output"></a>Fertig produzierte Artikel

[!INCLUDE [prod_short](includes/prod_short.md)] bietet die Möglichkeit, nachzuverfolgen, wie viel Zeit für das Abarbeiten eines Fertigungsauftrags benötigt wurde, nebem dem Erfassen der gefertigten Menge. Mit diesen Informationen können Sie die Fertigungskosten genauer bestimmen. Außerdem kann es sein, dass Hersteller, die ein standardmäßiges Kostenrechnungssystem verwenden, die tatsächlichen Informationen erfassen möchten, damit sie genauere Standards entwickeln können.  

Die Istmeldung kann über das [FA-Istmeldungs Buch.-Blatt](production-how-to-post-output-quantity.md) verarbeitet, jedoch auch automatisch erfasst werden. [!INCLUDE [prod_short](includes/prod_short.md)] kopiert beim Aktualisieren die Buchungsmethode von der Arbeitsplatz- oder Arbeitsplatzgruppenkarte in den FA-Arbeitsplan. Wie beim Materialverbrauch gibt es auch für Istmeldungen die drei Berichterstellungsmethoden „Manuell“, „Vorwärts“ und „Rückwärts“.

Bei der Methode „Manuell“ wird das FA-Verb. Buch.-Blatt verwendet, um die benötigte Zeit und die gefertigte Menge anzugeben.  

Bei der Methode „Vorwärts“ wird die Soll-Menge (und die Zeit) erfasst, die automatisch bei der Freigabe eines Fertigungsauftrags erfasst wird. Verbindungscodes spielen beim „Vorwärts“-Buchen der Soll-Menge (Istmeldungen) keine Rolle.  

Bei der Methode „Rückwärts“ wird die Soll-Menge (und die Zeit) erfasst, die automatisch am Ende eines Fertigungsauftrags erfasst wird. Verbindungscodes spielen beim „Rückwärts“-Buchen der Soll-Menge (Istmeldungen) keine Rolle.  

### <a name="posting-consumption-and-output"></a>Verbrauch und Istmeldungen buchen

Sie können sowohl für Verbrauch als auch für Istmeldungen beliebige Kombinationen aus automatischem Buchen und manuell erfassten Informationen verwenden. Beispielsweise kann es sein, dass Sie Komponenten automatisch mit der Methode „Vorwärts“ buchen, Ausschuss aber weiterhin mit dem FA-Verbrauchs Buch.-Blatt erfassen möchten. In gleicher Weise möchten Sie möglicherweise Istmeldungen automatisch erfassen, aber das FA-Istmeldungs Buch.-Blatt dazu verwenden, Ausschuss des übergeordneten Artikels oder zusätzlich für den Auftrag benötigte Zeit zu erfassen.  

Wenn Sie Verbrauch und Istmeldungen manuell eingeben, müssen Sie die Reihenfolge festlegen, in der diese Informationen erfasst werden sollen. Sie können den Verbrauch zuerst erfassen und zum Eingeben der Istmeldungen eine Schnellmethode verwenden, die auf der erwarteten Menge für die Istmeldungen basiert. Sie können aber auch zuerst die Istmeldungen mit der Funktion **Arbeitsplan auflösen** eingeben. Anschließend müssen Sie den Verbrauch anhand der tatsächlichen Mengen der Istmeldungen erfassen.  

### <a name="production-journal"></a>Produktions Buch.-Blatt

Im [Produktions Buch.-Blatt](production-how-to-register-consumption-and-output.md) werden die Funktionen des FA-Verbrauchs Buch.-Blatts und des FA-Istmeldungs Buch.-Blatts in einem Buchungsblatt kombiniert, auf das direkt vom freigegebenen Fertigungsauftrag aus zugegriffen werden kann.  

Der Sinn des Produktions Buch.-Blatt besteht darin, eine einzelne Oberfläche bereitzustellen, über die Sie den Verbrauch und die Istmeldungen eines Fertigungsauftrags erfassen können.  

Das Produktions Buch.-Blatt hat eine einfache Ansicht und bietet Ihnen folgende Möglichkeiten:  

- Einfaches Erfassen von Istmeldungen und Verbrauch hinsichtlich eines Fertigungsauftrags  
- Verbinden der Komponenten mit Arbeitsgängen  
- Verbinden der tatsächlichen Arbeitsgangsdaten mit den Standardschätzungen in den Arbeitsplanzeilen des Fertigungsauftrags und in den Komponentenzeilen  
- Buchen und Drucken einer Übersicht der registrierten Arbeitsgangsdaten für den Fertigungsauftrag  

Das Produktions Buch.-Blatt erfüllt viele derselben Funktionen wie das FA-Verbrauchs Buch.-Blatt und das FA-Istmeldungs Buch.-Blatt. Abmessungen, Artikelverfolgung und Lagerplatzinhalt werden auf die gleiche Weise behandelt.  

In den folgende Punkten unterscheidet sich das Produktions Buch.-Blatt aber vom FA-Verbrauchs Buch.-Blatt und FA-Istmeldungs Buch.-Blatt:  

- Es wird direkt aus einer Zeile eines freigegebenen Fertigungsauftrags aufgerufen und mit den relevanten Daten voreingestellt.  
- Es versetzt Sie in die Lage, über einen Buchungsmethodenfilter auf dem Buch.-Blatt zu definieren, welche Arten von Komponenten bearbeitet werden sollen.  
- Mengen und Zeiten, die bereits für den Auftrag gebucht wurden, werden im unteren Bereich des Buch.-Blatts als Posten angezeigt.  
- Felder, für die Dateneingaben unwichtig sind, sind leer und nicht editierbar.  
- Der Benutzer kann einrichten, wie fertig gestellte Mengen im Buch.-Blatt voreingestellt werden - beispielsweise kann er festlegen, dass die "Fertig gestellte Menge" für den letzten Arbeitsgang gleich Null sein muss.  
- Sollten Sie versuchen, das Buch.-Blatt zu beenden, ohne die vorgenommenen Buchungen gespeichert zu haben, wird eine Bestätigungsmeldung angezeigt, die Ihnen den Verbleib im Buch.-Blatt ermöglicht.  
- Arbeitsgänge und Komponenten werden zusammen in einer logischen Struktur angezeigt, die einen Überblick über den Fertigungsprozess bereitstellt.  

Im Produktions Buch.-Blatt werden Verbrauchsmengen als negative Artikelposten, fertig gestellte Mengen als positive Posten und benötigte Zeiten als Kapazitätsposten gebucht.  

## <a name="see-also"></a>Siehe auch

[Produktion](production-manage-manufacturing.md)
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
