---
title: Designdetails – Ausgleich von Angebot und Nachfrage
description: 'In diesem Artikel wird beschrieben, wie Sie Ziele priorisieren, indem Sie Angebot und Nachfrage in Einklang bringen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand"></a><a name="design-details-balancing-supply-and-demand"></a><a name="design-details-balancing-supply-and-demand"></a>Designdetails: Ausgleich von Angebot und Nachfrage

Um zu verstehen, wie das Planungssystem funktioniert, ist es wichtig, seine priorisierten Ziele zu verstehen:  

* Jeder Bedarf wird durch ausreichenden Vorrat gedeckt.  
* Jeder Vorrat dient einem bestimmten Zweck.  

Im Allgemeinen werden diese Ziele durch den Ausgleich von Vorrat und Bedarf erreicht.  

## <a name="supply-and-demand"></a><a name="supply-and-demand"></a><a name="supply-and-demand"></a>Angebot und Nachfrage

Der Begriff *Angebot* bezieht sich auf jede Art von positiver oder eingehender Menge, wie z. B.:

* Inventar
* Einkauf
* Montage
* Produktion
* Eingehende Umlagerungen
* Retouren  

Der Begriff *Nachfrage* bezieht sich auf jede Art von Bruttonachfrage, wie z. B.:

* Ein Artikel für einen Verkaufsauftrag
* Eine Komponente für einen Fertigungsauftrag

[!INCLUDE [prod_short](includes/prod_short.md)] lässt auch die Verwendung für technischere Bedarfsarten zu, wie z. B. negative Bestände und Einkaufsreklamationen.

Um die Quellen von Angebot und Nachfrage zu organisieren, ordnet das Planungssystem diese in zwei Zeitskalen an, die Bestandsprofile genannt werden. Ein Profil ist für Bedarfsereignisse vorgesehen, das andere die entsprechenden Vorratsereignisse. Jedes Angebotsereignis stellt eine Entität in einer Bestellung dar, wie z. B.:

* EIne Verkaufsauftragsposition
* Ein Artikelposten
* Eine Fertigungsauftragsposition

Beim Laden von Bestandsprofilen werden die Nachfrage-/Angebotssätze abgeglichen, um einen Vorratsplan zu erzeugen, der die angegebenen Ziele abdeckt.

Lagerbestände und Planungsparameter sind andere Arten von Angebot und Nachfrage. Diese Typen werden einem integrierten Ausgleich unterzogen, um Lagerartikel aufzufüllen. Weitere Informationen finden Sie unter [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a><a name="the-concept-of-balancing-in-brief"></a><a name="the-concept-of-balancing-in-brief"></a>Kurzzusammenfassung des Ausgleichskonzepts

Die Nachfrage kommt von Ihren Kunden. Der Vorrat ist das, was Sie erzeugen und für den Ausgleich entnehmen kann. Das Planungssystem beginnt mit dem Bedarf und verfolgt diesen dann rückwärts bis zum Vorrat.  

Bestandsprofile enthalten Informationen über den Bedarf und den Vorrat, die Mengen und den Zeitpunkt. Diese Profile bilden die beiden Seiten des Ausgleichs.  

Das Ziel der Planung ist es, das Angebot und die Nachfrage eines Artikels auszugleichen, um sicherzustellen, dass das Angebot entsprechend den Planungsparametern und -regeln zum Vorrat passt.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Übersicht über den Ausgleich von Angebot und Nachfrage.":::

## <a name="process-orders-before-the-planning-start-date"></a><a name="process-orders-before-the-planning-start-date"></a><a name="process-orders-before-the-planning-start-date"></a>Aufträge vor dem Planungsstartdatum bearbeiten

Um zu vermeiden, dass ein Angebotsplan unangemessene Vorschläge enthält, plant das Planungssystem in der Zeit vor dem Planungsstartdatum nichts. Für den Zeitraum gilt die folgende Regel:

* Alle Vorräte und der Bedarf vor dem Startdatum des Planungszeitraums werden als Teil des Bestands oder als ausgeliefert betrachtet.  

Das Planungssystem schlägt, mit wenigen Ausnahmen, keine Änderungen an Vorräten im Zeitraum vor und es werden keine Auftragsverfolgungsverknüpfungen für diesen Zeitraum erstellt. Folgendes sind Ausnahmen von dieser Regel:  

* Das Lager, dessen Verfügbarkeit projiziert ist, einschließlich der Summe aus Vorrat und Bedarf im Zeitraum, unter null liegt.  
* Zurückdatierte Aufträge erfordern Seriennummern oder Chargennummern.  
* Der Vorrat-/Bedarfssatz ist über eine Eins-zu-Eins-Richtlinie verknüpft. 

Wenn der anfänglich verfügbare Bestand unter null liegt, schlägt das Planungssystem einen Vorrat am Tag vor der Planungsperiode vor, um die fehlende Menge zu decken. Daher ist der projizierte und verfügbare Bestand immer mindestens Null, wenn die Planung für die zukünftige Periode beginnt. In der Planungszeile für diesen Beschaffungsauftrag wird ein Notfall-Warnsymbol angezeigt, und in der Nachschlagefunktion werden zusätzliche Informationen bereitgestellt.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a><a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a><a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period"></a>Serien- und Chargennummern sowie Auftrag-zu-Auftrag-Verknüpfungen sind vom vorherigen Zeitraum ausgenommen

Wenn Serien- oder Chargennummern erforderlich sind oder eine Auftrag-zu-Auftrag-Verknüpfung besteht, ignoriert das Planungssystem die Regel über die vorherige Periode. Es enthält zurückdatierte Mengen ab dem Startdatum und schlägt möglicherweise Korrekturmaßnahmen vor, wenn Angebot und Nachfrage nicht synchronisiert sind. Diese Nachfrage-Angebots-Sätze müssen übereinstimmen, um sicherzustellen, dass eine bestimmte Nachfrage erfüllt wird.

## <a name="load-inventory-profiles"></a><a name="load-inventory-profiles"></a><a name="load-inventory-profiles"></a>Bestandsprofile laden

Um die Quellen von Angebot und Nachfrage zu organisieren, ordnet das Planungssystem diese in zwei Zeitskalen an, die Bestandsprofile genannt werden.  

Angebot und Nachfrage mit Fälligkeitsdaten am oder nach dem Planungsstartdatum werden in jedes Bestandsprofil geladen. Beim Laden werden die Angebots- und Nachfragetypen nach Gesamtprioritäten sortiert, z. B.:

* Fälligkeitsdatum
* Stücklistenebene
* Lagerort
* Variante

Auftragsprioritäten werden auf die verschiedenen Arten angewendet, um den wichtigsten Bedarf zuerst zu erfüllen. Informationen finden Sie unter [Bestellungen priorisieren](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Die Nachfrage kann auch negativ sein. Negative Nachfrage als Angebot behandeln. Im Gegensatz zum typischen Angebot gilt die negative Nachfrage jedoch als festes Angebot. Das Planungssystem kann ihn berücksichtigen, wird aber keine Änderungen vorschlagen.  

Allgemein betrachtet das Planungssystem alle Vorräte nach dem Planungsstartdatum als zur Bedarfserfüllung veränderbar. Nachdem eine Menge aus einem Beschaffungsauftrag gebucht wird, kann das Planungssystem diese nicht mehr ändern. Die folgenden Aufträge können nicht neu geplant werden:  

* Freigegebene Produktionsaufträge, bei denen ein Verbrauch oder eine Ausgabe gebucht wurde.  
* Montageaufträge, bei denen ein Verbrauch oder eine Ausgabe gebucht wurde.  
* Umlagerungsaufträge, bei denen die Lieferung gebucht wurde.  
* Einkaufsbestellungen, bei denen der Eingang gebucht wurde.  

Neben dem Laden von Angebots- und Nachfragearten werden bestimmte Arten unter Beachtung spezieller Regeln und Abhängigkeiten geladen, die im Folgenden beschrieben werden. In den folgenden Abschnitten dieses Artikels werden diese Regeln und Abhängigkeiten beschrieben.  

### <a name="item-dimensions-are-separated"></a><a name="item-dimensions-are-separated"></a><a name="item-dimensions-are-separated"></a>Artikeldimensionen werden separiert

Der Vorratsplan muss für jede Kombination der Dimensionen des Artikel berechnet werden, z. B. Variante und Lagerplatz. Es müssen nur die Kombinationen berechnet werden, die einen Bedarf und/oder einen Vorrat aufweisen.  

Das Planungssystem sucht nach Kombinationen im Bestandsprofil. Wenn es eine neue Kombination findet, erstellt es einen internen Steuerdatensatz, der die tatsächlichen Informationen zur Kombination enthält. Das Planungssystem fügt dann die SKU als Steuerungsdatensatz (äußere Schleife) ein. Dadurch werden die Planungsparameter entsprechend einer Kombination aus Variante und Lagerplatz festgelegt, und das System kann mit der inneren Schleife fortfahren. 

> [!NOTE]  
> Sie müssen keinen SKU-Datensatz eingeben, wenn Sie eine Nachfrage und/oder ein Angebot für eine bestimmte Kombination von Variante und Lagerort eingeben. Wenn für eine bestimmte Kombination kein SKU-Datensatz vorhanden ist, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] daher einen eigenen temporären SKU-Datensatz auf der Basis der Daten aus dem Artikel. Wenn der Schalter **Lagerplatz obligatorisch** auf der Seite **Bestandseinrichtung** eingeschaltet ist, müssen Sie entweder eine SKU erstellen oder den Schalter **Komponenten am Lagerplatz** einschalten. Weitere Informationen finden Sie unter [Planung mit/ohne Lagerortcodes](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a><a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a><a name="serial-and-lot-numbers-are-loaded-by-specification-level"></a>Serien- und Chargennummern werden nach Spezifikationsstufe geladen

Serien- und Chargennummern werden zusammen mit dem Angebot und der Nachfrage, denen sie zugeordnet sind, in die Bestandsprofile geladen.  

Angebots- und Nachfrageattribute werden nach Auftragspriorität und nach ihrer Spezifikationsstufe geordnet. Da Serien- und Chargennummernübereinstimmungen die Spezifikationsstufe widerspiegeln, wird eine spezifischere Anforderung vor einer weniger spezifischen Anforderung abgeglichen. Eine bestimmte Nachfrage kann beispielsweise eine Chargennummer sein, die für eine Verkaufsposition angegeben ist. Eine weniger spezifische Nachfrage könnte ein Verkauf von einer beliebigen Chargennummer sein.

> [!NOTE]  
> Die einzigen speziellen Priorisierungsregeln für ein Angebot und eine Nachfrage mit Serien- und Chargennummern sind die Spezifikationsstufe, die durch die Kombinationen von Serien- und Chargennummern definiert ist, und das Einrichten der Artikelverfolgung für die betroffenen Artikel.  

Beim Ausgleich betrachtet das Planungssystem Lieferungen mit Serien- und Chargennummern als unflexibel. Das System wird solche Beschaffungsaufträge nicht erhöhen oder neu planen. Die einzige Ausnahme hiervon gilt, wenn sie in einer Auftrag-zu-Auftrag-Beziehung verwendet werden. Weitere Informationen finden Sie unter [Auftrag-zu Auftrag-Verknüpfungen werden nie aufgelöst](#order-to-order-links-are-never-broken). Diese Ausnahme schützt das Angebot davor, mehrere, möglicherweise widersprüchliche Aktionsnachrichten zu erhalten, wenn unterschiedliche Attribute vorliegen. Unterschiedliche Attribute können beispielsweise auftreten, wenn das Angebot eine Sammlung unterschiedlicher Seriennummern aufweist.  

Ein weiterer Grund, warum Lieferungen mit Serien- und Chargennummern unflexibel sind, besteht darin, dass Serien- und Chargennummern oft spät im Prozess zugewiesen werden. Es könnte verwirrend sein, wenn an dieser Stelle Änderungen vorgeschlagen werden.  

Der Seriennummern- und Chargennummernausgleich respektiert die Regel nicht, dass vor dem Planungsstartdatum nichts geplant wird. Wenn Angebot und Nachfrage nicht synchronisiert sind, schlägt das Planungssystem unabhängig vom Startdatum der Planung Änderungen oder neue Aufträge vor.  

### <a name="order-to-order-links-are-never-broken"></a><a name="order-to-order-links-are-never-broken"></a><a name="order-to-order-links-are-never-broken"></a>Auftrag-zu-Auftrag-Verknüpfungen werden nie aufgelöst

Bei der Planung eines Auftrag-zu-Auftrag-Artikels darf das verknüpfte Angebot nur für das verwendet werden, wofür es ursprünglich vorgesehen war. Die verknüpfte Nachfrage darf nicht durch ein anderes beliebigen Angebot gedeckt werden. Dies gilt auch dann, wenn das Angebot aktuell zeitlich und mengenmäßig verfügbar ist. Beispielsweise können Sie keinen Montageauftrag verwenden, der in einem Programmfertigungsszenario mit einem Kundenauftrag verknüpft ist, um eine andere Nachfrage zu decken.  

Bei Auftrag-zu-Auftrag müssen sich Angebot und Nachfrage exakt decken. Das Planungssystem stellt das Angebot sicher. Dies geschieht ohne Berücksichtigung von Auftragsgrößenparametern, Modifikatoren und Mengen im Bestand (mit Ausnahme der Mengen, die sich auf die verknüpften Aufträge beziehen). Aus demselben Grund schlägt das System die Verringerung überschüssiger Vorräte vor, wenn der verknüpfte Bedarf sinkt.  

Dieser Abgleich wirkt sich auch auf das Timing aus. Der durch den Zeitbereich bedingte begrenzte Horizont wird nicht berücksichtigt. Der Vorrat wird neu geplant, wenn sich das Timing des Bedarfs geändert hat. Die Verzögerungszeit wird jedoch beachtet. Sie verhindert, dass Eins-zu-Eins-Vorräte eingeplant werden – außer bei internen Vorräten eines mehrstufigen Produktionsauftrags (Projektauftrag).  

> [!NOTE]  
> Serien- und Chargennummern können auch für Eins-zu-Eins-Bedarf angegeben werden. In diesem Fall wird das Angebot nicht als flexibel betrachtet (wie normalerweise bei Serien- und Chargennummern). In diesem Fall führt das System eine Erhöhung oder Verringerung durch, wenn sich der Bedarf ändert. Wenn ein Bedarf unterschiedliche Serien- und Chargennummern aufweist, z. B. mehr als eine Chargennummer, wird außerdem ein Beschaffungsauftrag für jede Charge vorgeschlagen.  

> [!NOTE]  
> Planungen sollten nicht dazu führen, dass Vorratsaufträge erstellt werden, die durch eine Eins-zu-Eins-Verknüpfung gebunden sind. Wenn die Planung verwendet wird, sollte dies nur zur Generierung des abhängigen Bedarfs in einer Fertigungsumgebung geschehen.

### <a name="component-need-is-loaded-according-to-production-order-changes"></a><a name="component-need-is-loaded-according-to-production-order-changes"></a><a name="component-need-is-loaded-according-to-production-order-changes"></a>Der Komponentenbedarf wird entsprechend den Änderungen der Produktionsaufträge geladen.

Bei der Bearbeitung von Produktionsaufträgen muss das Planungssystem die benötigten Komponenten überwachen, bevor diese in das Bedarfsprofil geladen werden. Komponentenzeilen, die sich aus einem geänderten Produktionsauftrag ergeben, ersetzen die Zeilen des ursprünglichen Auftrags. Die Änderung stellt sicher, dass das Planungssystem keine Planungszeilen für einen Komponentenbedarf dupliziert.  

### <a name="consume-safety-stock"></a><a name="consume-safety-stock"></a><a name="consume-safety-stock"></a>Sicherheitsbestand verbrauchen

Die Sicherheitsbestandsmenge ist ein Angebot, das zum Planungsstartdatum in das Bestandsprofil geladen wird.  

Der Sicherheitsbestand ist eine Bestandsmenge, die festgelegt wird, um Unsicherheiten im Bedarf während der Vorlaufzeit der Wiederbeschaffung zu erfüllen. Er kann jedoch verbraucht werden, um einen Bedarf zu decken. In diesem Fall sorgt das Planungssystem dafür, dass der Sicherheitsbestand schnell ersetzt wird. Das System schlägt einen Beschaffungsauftrag vor, um die Sicherheitsbestandsmenge am Verbrauchsdatum wieder aufzufüllen. In der Planungszeile wird ein Ausnahme-Warnungssymbol angezeigt. Dieses zeigt, dass der Sicherheitsbestand über einen Ausnahmeauftrag für die fehlende Menge teilweise oder vollständig verbraucht wurde.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a><a name="forecast-demand-is-reduced-by-sales-orders"></a><a name="forecast-demand-is-reduced-by-sales-orders"></a>Geplanter Bedarf wird durch Verkaufsaufträge reduziert

Bedarfsplanungen stellen den erwarteten zukünftigen Bedarf dar. Während der tatsächliche Bedarf eingegeben wird, typischerweise in Form von Verkaufsaufträgen für produzierte Artikel, verringert sich die Planungsmenge.

Die Planung selbst wird nicht durch Verkaufsaufträge reduziert. Die geplanten Mengen, die in der Planungsberechnung verwendet werden, werden jedoch um die Verkaufsauftragsmengen reduziert , bevor die verbleibende Mengen, in das Bedarfsprofil eingehen. Für Verkäufe während eines Zeitraums umfasst die Planung sowohl offene Verkaufsaufträge als auch Artikelposten aus versandten Verkäufen. Die Ausnahme von dieser Regel gilt, wenn sie aus einem Rahmenauftrag stammen.  

Sie müssen einen gültigen Planungszeitraum definieren. Das Datum der geplanten Menge definiert den Beginn des Zeitraums, und das Datum der nächsten Planung definiert das Ende des Zeitraums.  

Die Planung für Perioden vor dem Planungszeitraum wird nicht verwendet – unabhängig vom Verbrauch. Die erste interessante Planungszahl ist entweder das Startdatum der Planung oder das nächstgelegene Datum.  

Die Planung kann für verschiedene Bedarfstypen gelten:

* Unabhängiger Bedarf, z. B. Verkaufsaufträge
* Abhängiger Bedarf, z. B. Produktionsauftragskomponenten.

Ein Artikel kann beide Planungsarten verwenden. Während der Planung erfolgt der Verbrauch separat, zuerst für den unabhängigen Bedarf und dann für den abhängigen Bedarf.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a><a name="blanket-order-demand-is-reduced-by-sales-orders"></a><a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Bedarf für Rahmenaufträge wird durch Verkaufsaufträge reduziert

Die Planung wird durch Rahmenverkaufsaufträge ergänzt, um den zukünftigen Bedarf eines bestimmten Debitors festzulegen. Wie bei der (nicht spezifizierten) Planung sollten die tatsächlichen Verkäufe den erwarteten Bedarf in Anspruch nehmen, und die verbleibende Menge sollte in das Bedarfsbestandsprofil eingehen. Der Verbrauch verringert die Menge des Rahmenauftrags nicht.

Die Planungsberechnung umfasst offene Verkaufsaufträge, die mit dieser bestimmten Rahmenauftragszeile verbunden sind, nicht jedoch Gültigkeitszeiträume. Außerdem umfasst sie keine gebuchten Aufträge, da der Buchungsvorgang die ausstehende Rahmenauftragsmenge bereits reduziert hat.

## <a name="prioritize-orders"></a><a name="prioritize-orders"></a><a name="prioritize-orders"></a>Aufträge priorisieren

Innerhalb einer bestimmten SKU hat das angeforderte oder verfügbare Datum die höchste Priorität. Der heutige Bedarf sollte vor dem Bedarf der nächsten Woche erledigt werden. Aber zusätzlich zu dieser Gesamtpriorität unterbreitet das Planungssystem die folgenden Vorschläge gemäß der Auftragsprioritäten:

* Welche Art von Nachfrage Sie zuerst erfüllen sollten.
* Welche Vorratsquelle vor der Anwendung anderer Vorratsquellen angewendet werden sollte.  

Das geladene Angebot und die Nachfrage ergeben ein Profil für geplanten Bestand gemäß den Prioritäten.  

### <a name="priorities-on-the-demand-side"></a><a name="priorities-on-the-demand-side"></a><a name="priorities-on-the-demand-side"></a>Prioritäten auf der Bedarfsseite

1. Bereits geliefert: Artikelsachkontoeintrag  
2. Einkaufsreklamation  
3. Verkaufsauftrag  
4. Serviceauftrag  
5. Produktionskomponentenbedarf  
6. Montageauftragszeile  
7. Ausgehender Umlagerungsauftrag.  
8. Rahmenauftrag (der nicht bereits durch entsprechende Verkaufsaufträge verbraucht wurde)  
9. Planung (die nicht bereits durch andere Verkaufsaufträge verbraucht wurde)  

> [!NOTE]  
> Einkaufsreklamationen sind normalerweise nicht in die Vorratsplanung eingebunden. Sie sollten immer aus der Charge reserviert werden, die retourniert werden soll. Wenn sie nicht reserviert werden, spielen Einkaufsreklamationen eine Rolle bei der Verfügbarkeit und werden hoch priorisiert, um zu vermeiden, dass das Planungssystem eine Bestellung vorschlägt, nur um eine Einkaufsreklamation abzudecken.  

### <a name="priorities-on-the-supply-side"></a><a name="priorities-on-the-supply-side"></a><a name="priorities-on-the-supply-side"></a>Prioritäten auf der Vorratsseite

1. Bereits im Bestand: Artikelsachkontoeintrag (Planungsflexibilität = keine)  
2. Verkaufsreklamationsauftrag (Planungsflexibilität = keine)  
3. Ausgehende Umlagerungsaufträge  
4. Produktionsauftrag  
5. Montageauftrag  
6. Einkaufsbestellung  

### <a name="priority-related-to-the-state-of-supply-and-demand"></a><a name="priority-related-to-the-state-of-supply-and-demand"></a><a name="priority-related-to-the-state-of-supply-and-demand"></a>Priorität bezogen auf den Status von Bedarf und Vorrat

Neben den Prioritäten aus der Art von Angebot und Nachfrage gibt es noch weitere Dinge, die die Planungsflexibilität beeinflussen. Zum Beispiel Lageraktivitäten und der Status der folgenden Bestellungen:

* Verkauf
* Einkauf
* Transfer
* Montage
* Produktion

Der Status dieser Aufträge hat folgende Auswirkungen: 

1. Teilweise bearbeitet (Planungsflexibilität = Keine)  
2. Bereits in Bearbeitung im Lagerort (Planungsflexibilität = keine)  
3. Freigegeben – alle Auftragstypen (Planungsflexibilität = unbegrenzt)  
4. Umgewandelter geplanter Produktionsauftrag (Planungsflexibilität = unbegrenzt)  
5. Geplant/offen – alle Auftragstypen (Planungsflexibilität = unbegrenzt)

## <a name="balancing-supply-with-demand"></a><a name="balancing-supply-with-demand"></a><a name="balancing-supply-with-demand"></a>Abgleich von Angebot und Nachfrage

Das Planungssystem gleicht Angebot und Nachfrage aus, indem es Maßnahmen vorschlägt, um Beschaffungsaufträge zu überarbeiten, die nicht ausgeglichen sind. Dieser Ausgleich erfolgt für jede Kombination aus Variante und Standort.  

Stellen Sie sich vor, dass jedes Bestandsprofil zwei Zeichenfolgen enthält:

* Eine Reihe von Bedarfsereignissen, sortiert nach Datum und Priorität
* Eine entsprechende Kette von Lieferereignissen

Jedes Ereignis verweist auf seinen Herkunftsartstyp und seine Identifizierung. Die Regeln für den Ausgleich des Artikels sind einfach. Die Zuordnung von Angebot und Nachfrage kann wie folgt zu jedem Zeitpunkt im Vorgang geschehen:  

1. Kein Bedarf oder Vorrat für den Artikel => die Planung ist abgeschlossen (oder soll nicht beginnen).  
2. Bedarf existiert, aber es ist kein Vorrat vorhanden=> Vorrat soll vorgeschlagen werden.  
3. Vorrat existiert, aber es ist kein Bedarf vorhanden=> Vorrat soll storniert werden.  
4. Angebot und Nachfrage sind vorhanden => Fragen sollten gestellt und beantwortet werden, bevor [!INCLUDE [prod_short](includes/prod_short.md)] sicherstellen kann, dass das Angebot den Bedarf erfüllen kann.

    Wenn das Timing des Vorrats nicht passt, kann der Vorrat vielleicht wie folgt neu geplant werden:  

    1. Wenn der Vorrat früher als der Bedarf platziert wird, kann der Vorrat vielleicht so ausgeplant werden, dass der Bestand so gering wie möglich ist.  
    2. Wenn der Vorrat später als der Bedarf platziert wird, kann der Vorrat vielleicht vorwärts geplant werden. Andernfalls schlägt das System einen neuen Vorrat vor.  
    3. Wenn der Vorrat den Bedarf an dem Datum erfüllt, kann das Planungssystem untersuchen, ob die Menge des Vorrats den bedarf decken kann.  

    Wenn die Zeitplanung erfolgt ist, kann die bereitzustellende Angebotsmenge wie folgt berechnet werden:  

    1. Wenn die Angebotsmenge kleiner als der Bedarf ist, kann die Vorratsmenge erhöht werden (oder nicht, wenn eine Höchstmengenrichtlinie vorhanden ist).  
    2. Wenn die Angebotsmenge größer als der Bedarf ist, kann die Vorratsmenge verringert werden (oder nicht, wenn eine Mindestmengenrichtlinie vorhanden ist).  

    An dieser Stelle besteht eine dieser beiden Situationen:  

    1. Der aktuelle Bedarf kann abgedeckt werden, in welchem Fall er geschlossen werden kann und die Planung für den folgenden Bedarf begonnen werden kann.  
    2. Das Vorrat hat sein Maximum erreicht, ein Teil der Bedarfsmenge wurde nicht abgedeckt. In diesem Fall kann das Planungssystem den aktuellen Vorrat schließen und mit dem nächsten fortfahren.  

 Der Vorgang beginnt von vorn mit dem folgenden Bedarf und dem folgenden Vorrat oder umgekehrt. Der aktuelle Vorrat kann möglicherweise auch diesen nächsten Bedarf abdecken, oder der aktuelle Bedarf wurde noch nicht vollständig abgedeckt.  

### <a name="rules-for-actions-for-supply-events"></a><a name="rules-for-actions-for-supply-events"></a><a name="rules-for-actions-for-supply-events"></a>Regeln für Aktionen für Vorratsereignisse

Bei Top-down-Berechnungen, bei denen das Angebot die Nachfrage decken muss, wird die Nachfrage als gegeben angenommen. Es liegt außerhalb der Kontrolle des Planungssystems. Das Planungssystem kann jedoch die Angebotsseite verwalten und wird die folgenden Vorschläge unterbreiten:

* Neue Beschaffungsaufträge erstellen
* Vorhandene Bestellungen umplanen oder ihre Mengen ändern
* Lieferaufträge stornieren, die nicht mehr benötigt werden  

Um einen Beschaffungsauftrag aus den Planungsvorschlägen ausschließen, können Sie angeben, dass keine Planungsflexibilität besteht (Planungsflexibilität = Keine). Dann wird überschüssiger Vorrat aus diesem Auftrag verwendet, um Bedarf zu decken, aber keine Aktion wird vorgeschlagen. 

Im Allgemeinen haben alle Vorräte eine Planungsflexibilität, die durch den Zustand der einzelnen vorgeschlagenen Aktionen eingeschränkt ist.  

* **Neu ausplanen**: Das Datum eines vorhandenen Beschaffungsauftrags kann ausgeplant werden, um das Fälligkeitsdatum des Bedarfs zu erfüllen, es sei denn:

  * Es stellt den Lagerbestand dar (immer mit Tag Null).  
  * Es enthält einen Auftrag-zu-Auftrag-Link zu einem anderen Bedarf.  
  * Es liegt außerhalb des Fensters für die Umplanung im Zeitrahmen.
  * Es gibt einen näheren Bestand, der verwendet werden könnte.  
  * Andererseits entscheidet sich der Benutzer möglicherweise zu einer Neuplanung, weil
  * Der Beschaffungsauftrag wurde an einem früheren Datum mit einem anderen Bedarf verbunden.  
  * Das erforderliche Neuplanung ist so minimal, dass sie als geringfügig ansehen wird.  

* **Neu einplanen**: Das Datum eines vorhandenen Beschaffungsauftrags kann eingeplant werden, ausgenommen unter den folgenden Bedingungen:

  * Es wird direkt mit einem anderen Bedarf verknüpft.  
  * Es liegt außerhalb des Fensters für die Umplanung, die vom Zeitrahmen definiert ist.

> [!NOTE]  
> Wenn ein Artikel unter Verwendung eines Meldebestand geplant wird, können Sie den Beschaffungsauftrag neu planen. Dies geschieht häufig in den vorwärtsgeplanten Beschaffungsaufträgen, die durch einen Minimalbestand gestartet werden.

* **Zugangs-Menge**: Die Menge eines vorhandenen Beschaffungsauftrags kann erhöht werden, damit der Bedarf erfüllt werden kann, es sei denn, der Beschaffungsauftrag ist direkt mit einem Bedarf durch einen Auftrag-zu-Auftrag-Link verknüpft.  

> [!NOTE]  
> Obwohl Sie den Beschaffungsauftrag erhöhen können, kann die Erhöhung durch eine maximale Auftragsgröße eingeschränkt sein.  

* **Menge reduzieren**: Ein vorhandener Beschaffungsauftrag mit einem Überschuss im Vergleich zu einem vorhandenen Bedarf kann reduziert werden, damit der Bedarf erfüllt werden kann.  

> [!NOTE]  
> Obwohl die Menge verringert werden kann, ist möglicherweise immer noch Überschuss im Vergleich zum Bedarf vorhanden, und zwar aufgrund einer Mindestauftragsmenge oder eines Auftragsvielfachen. 

* **Abbrechen**: Als spezieller Vorfall der Mengenverminderungsaktion kann der Beschaffungsauftrag storniert werden, wenn er bis auf Null verringert wird. 
* **Neu**: Wenn keine Beschaffungsaufträge vorhanden sind oder ein vorhandener Auftrag nicht geändert werden kann, um die erforderlichen Menge für den Bedarf im angeforderten Fälligkeitsdatum zu erfüllen, wird ein neuer Beschaffungsauftrag vorgeschlagen.  

### <a name="determine-the-supply-quantity"></a><a name="determine-the-supply-quantity"></a><a name="determine-the-supply-quantity"></a>Die Vorratsmenge bestimmen

Sie definieren die Planungsparameter, die die vorgeschlagene Menge eines jeden Beschaffungsauftrags steuern.  

Wenn das Planungssystem die Menge eines neuen Beschaffungsauftrags oder die Mengenänderung in einem bestehenden Auftrag berechnet, kann sich die vorgeschlagene Menge vom tatsächlichen Bedarf unterscheiden.  

Wenn ein Maximalbestand oder feste Auftragsmengen ausgewählt werden, wird die vorgeschlagene Menge möglicherweise erhöht, um diese feste Menge oder den Maximalbestand zu erfüllen. Wenn ein Wiederbeschaffungsverfahren einen Minimalbestand verwendet, wird die Menge mindestens so erhöht, dass der Minimalbestand erreicht wird. 

Die vorgeschlagene Menge kann in dieser Sequenz geändert werden:  

1. Bis zur maximalen Auftragsmenge.  
2. Aufwärts bis zur Mindestbestellmenge.  
3. Aufwärts bis zum nächsten Losgrößenrundungsfaktor.

### <a name="order-tracking-links-during-planning"></a><a name="order-tracking-links-during-planning"></a><a name="order-tracking-links-during-planning"></a>Bedarfsverursacherverknüpfungen bei der Planung

Bei Auftragsnachverfolgung während der Planung ordnet das Planungssystem die Auftragsnachverfolgungsverknüpfungen der Kombinationen von Artikeln, Varianten und Lagerorten neu an. Das System ordnet die Verfolgungslinks aus folgenden Gründen neu an:

* Um die Vorschläge zur Deckung des gesamten Bedarfs zu überprüfen und sicherzustellen, dass alle Lieferaufträge benötigt werden.  
* Die Auftragsverfolgungslinks müssen regelmäßig neu abgeglichen werden.  

Mit der Zeit geraten die Links zur Auftragsverfolgung aus dem Gleichgewicht. Die Links geraten aus dem Gleichgewicht, da das Bedarfsverursachernetzwerk erst dann wiederhergestellt wird, wenn ein Bedarf- oder Vorratsereignis geschlossen ist.

Vor dem Ausgleich des Vorrats nach Bedarf löscht das Planungssystem alle Auftragsnachverfolgungslinks. Während des Ausgleichsvorgangs, wenn ein Bedarfs- oder Zubehörereignis abgeschlossen wird, werden neue Bedarfsverursacherverknüpfungen zwischen Angebot und Nachfrage erstellt.  

> [!NOTE]  
> Das Planungssystem erstellt auch dann ausgeglichene Auftragsverfolgungsverknüpfungen, wenn der Artikel nicht für die dynamische Auftragsverfolgung festgelegt ist.

## <a name="close-balanced-supply-and-demand"></a><a name="close-balanced-supply-and-demand"></a><a name="close-balanced-supply-and-demand"></a>Ausgeglichenes Angebot und Nachfrage schließen

Der Ausgleich des Angebots hat drei mögliche Ergebnisse:

* Die benötigte Menge und das Datum der Bedarfsereignisse werden erfüllt, und die Planung für den Artikel kann geschlossen werden. Das Versorgungsereignis bleibt offen und kann möglicherweise den nächsten Bedarf decken. Wird das Vorratsereignis offen gehalten, kann der Ausgleichsvorgang mit dem aktuellen Vorratsereignis erneut beginnen.  
* Der Beschaffungsauftrag kann nicht geändert werden, um den gesamten Bedarf zu decken. Das Bedarfsereignis ist noch offen, mit einer nicht abgedeckten Menge, die möglicherweise vom nächsten Bedarfsereignis abgedeckt werden. Daher wird das aktuelle Vorratsereignis geschlossen und der Ausgleich mit dem aktuellen Bedarfs- und dem nächsten Vorratsereignis kann erneut beginnen.  
* Der gesamte Bedarf ist abgedeckt und es gibt keinen nächsten Bedarf (oder es gab gar keinen Bedarf). Überschüssiger Vorrat kann vermindert (oder storniert) und dann geschlossen werden. Alle anderen Versorgungsereignisse sollten ebenfalls storniert werden.  

Schließlich erstellt das Planungssystem ein Auftragsnachverfolgungslink zwischen dem Vorrat und dem Bedarf.  

### <a name="create-the-planning-line-suggested-action"></a><a name="create-the-planning-line-suggested-action"></a><a name="create-the-planning-line-suggested-action"></a>Die Planungszeile (vorgeschlagene Aktion) erstellen

Wenn eine der Aktionen **Neu**, **Menge ändern**, **Neu planen**, **Neu planen und Menge ändern** oder **Stornieren** für die Revision des Beschaffungsauftrags vorgeschlagen wird, erstellt das Planungssystem, eine Planung auf dem Planungsarbeitsblatt. Für die Auftragsverfolgung wird die Planungszeile nicht nur erstellt, wenn das Angebotsereignis geschlossen wird, sondern auch, wenn das Bedarfsereignis geschlossen wird. Dies gilt auch dann, wenn das Angebotsereignis noch offen ist und möglicherweise geändert wird, wenn das nächste Bedarfsereignis verarbeitet wird. Die Planungszeile kann erneut geändert werden, wenn sie erstellt wird.

Um die Belastung der Datenbank bei der Abwicklung von Fertigungsaufträgen zu reduzieren, kann die Planungszeile in drei Ebenen gepflegt werden:

* Erstellen Sie nur die Planungszeile mit dem aktuellen Fälligkeitsdatum und der Menge, aber ohne Arbeitsplan und Komponenten.  
* Arbeitsplan einschließen: Der geplante Arbeitsplan umfasst die Berechnung des Start- und Enddatum und -Zeiten. „Arbeitsplan einschließen“ ist anspruchvoll in Bezug auf Datenbankzugriffe. Um das End- und die Fälligkeitsdatum zu bestimmen, kann es notwendig sein, den Arbeitsplan zu berechnen, auch wenn das Vorratsereignis nicht abgeschlossen wurde. Zum Beispiel, wenn Sie eine Vorwärtsterminierung durchführen.  
* Strukturstückliste einschließen: kann kurz vor dem Abschluss des Vorratsereignisses geschehen.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)  
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
