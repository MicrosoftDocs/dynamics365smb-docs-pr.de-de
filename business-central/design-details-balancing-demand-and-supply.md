---
title: Designdetails – Ausgleich von Bedarf und Vorrat
description: Um zu verstehen, wie das Planungssystem funktioniert, ist es notwendig, die priorisierten Ziele des Planungssystems zu verstehen, die durch den Ausgleich von Vorrat und Bedarf erreicht werden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: b0ddc9e4a3fbfd4f26633f82f022aa73ba93ada8
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139833"
---
# <a name="design-details-balancing-demand-and-supply"></a>Planungsdetails – Ausgleich von Bedarf und Vorrat
Um die Funktionsweise des Planungssystems zu verstehen, müssen Sie die vorrangigen Zielsetzungen des Planungssystems kennen. Die wichtigste dieser Zielsetzungen ist, die Deckung des Bedarfs durch einen ausreichenden Vorrat zu gewährleisten und Folgendes sicherzustellen:  

- Jeder Bedarf wird durch ausreichenden Vorrat gedeckt.  
- Jeder Vorrat dient einem bestimmten Zweck.  

 Im Allgemeinen werden diese Ziele durch den Ausgleich von Vorrat und Bedarf erreicht.  

## <a name="demand-and-supply"></a>Bedarf und Vorrat
 „Bedarf“ ist der allgemeine Begriff für jede Art von Bruttobedarf, wie z. B. ein Verkaufsauftrag und ein Komponentenbedarf aus einem Produktionsauftrag. Darüber hinaus lässt die Anwendung auch technischere Bedarfsarten zu, wie z. B. negative Bestände und Einkaufsreklamationen.  

  „Vorrat“ ist der allgemeine Begriff für jede Art von positiver oder eingehender Menge, z. B. Bestand, Einkauf, Montage, Produktion oder eingehende Umlagerungen. Darüber hinaus kann auch eine Verkaufsreklamation einen Vorrat darstellen.  

  Um die vielen Quellen von Bedarf und Vorrat zu organisieren, ordnet das Planungssystem diese in zwei Zeitskalen an, die Bestandsprofile genannt werden. Ein Profil enthält Bedarfsereignisse, das andere die entsprechenden Vorratsereignisse. Jedes Ereignis repräsentiert eine Entität des Auftragsnetzwerks, wie z. B. eine Verkaufsauftragszeile, eine Sachkontozeile oder eine Produktionsauftragszeile.  

  Beim Laden von Bestandsprofilen werden die verschiedenen Bedarfs-/Vorratssätze abgeglichen, um einen Vorratsplan zu erzeugen, der die angegebenen Ziele abdeckt.  

  Planungsparameter und Bestände sind andere Arten von Bedarf bzw. Vorrat, die zur Wiederbeschaffung von Lagerartikeln einem integrierten Abgleich unterzogen werden. Weitere Informationen finden Sie unter [Design-Details: Handhabung von Wiederbestellungsrichtlinien](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Kurzzusammenfassung des Ausgleichskonzepts
  Der Bedarf wird von den Debitoren einer Firma bestimmt. Der Vorrat ist das, was die Firma erzeugen und für den Ausgleich entnehmen kann. Das Planungssystem beginnt mit dem unabhängigen Bedarf und verfolgt diesen dann rückwärts bis zum Vorrat.  

   Die Bestandsprofile enthalten Informationen über den Bedarf und den Vorrat, die Mengen und den Zeitpunkt. Diese Profile bilden die beiden Seiten des Ausgleichs.  

   Das Ziel des Planungsmechanismus ist es, den Bedarf und den Vorrat eines Artikels auszugleichen, um sicherzustellen, dass das Angebot entsprechend den Planungsparametern und -regeln zum Vorrat passt.  

   ![Übersicht über den Ausgleich von Vorrat und Bedarf.](media/nav_app_supply_planning_2_balancing.png "Übersicht über den Ausgleich von Vorrat und Bedarf")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Umgang mit Aufträgen vor dem Planungsstarttermin
Um zu vermeiden, dass ein Vorratsplan unausführbare und damit unbrauchbare Vorschläge anzeigt, betrachtet das Planungssystem den Zeitraum bis zum Planungsstartdatum als eingefrorenen Zeitraum, in dem nichts geplant wird. Für den eingefrorenen Zeitraum gilt die folgende Regel:  

Alle Vorräte und der Bedarf vor dem Startdatum des Planungszeitraums werden als Teil des Bestands oder als ausgeliefert betrachtet.  

Dementsprechend schlägt das Planungssystem, mit wenigen Ausnahmen, keine Änderungen an Vorräten im eingefrorenen Zeitraum vor. Es werden keine Auftragsverfolgungsverknüpfungen für diesen Zeitraum erstellt oder gepflegt.  

Die Ausnahmen von dieser Regel sind wie folgt:  

   * Wenn der projizierte verfügbare Bestand, einschließlich der Summe aus Vorrat und Bedarf im eingefrorenen Zeitraum, unter null liegt.  
   * Wenn Seriennummern/Chargennummern für die rückdatierte(n) Bestellung(en) erforderlich sind.  
   * Wenn der Vorrat-/Bedarfssatz über eine Eins-zu-Eins-Richtlinie verknüpft ist.  

Wenn der anfänglich verfügbare Bestand unter null liegt, schlägt das Planungssystem einen Vorrat am Tag vor der Planungsperiode vor, um die fehlende Menge zu decken. Somit ist der projizierte und verfügbare Bestand immer mindestens Null, wenn die Planung für die zukünftige Periode beginnt. In der Planungszeile für diesen Vorrat wird ein Notfall-Warnsymbol angezeigt. In der Nachschlagefunktion werden zusätzliche Informationen bereitgestellt.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serien-/Chargennummern und Eins-zu-Eins-Verknüpfungen sind vom eingefrorenen Zeitraum ausgenommen  
   Wenn Serien-/Chargennummern erforderlich sind oder eine Eins-zu-Eins-Verknüpfung besteht, ignoriert das Planungssystem den eingefrorenen Zeitraum. Es berücksichtigt Mengen, die ab dem Startdatum zurückdatiert sind, und schlägt möglicherweise Korrekturmaßnahmen vor, wenn Bedarf und Vorrat nicht synchronisiert sind. Der betriebswirtschaftliche Grund für dieses Prinzip liegt darin, dass solche festgelegten Bedarfs- und Vorratsmengen übereinstimmen müssen, um sicherzustellen, dass der spezifische Bedarf erfüllt wird.

## <a name="loading-the-inventory-profiles"></a>Laden der Bestandsprofile
Um die vielen Quellen von Bedarf und Vorrat zu organisieren, ordnet das Planungssystem diese in zwei Zeitskalen an, die Bestandsprofile genannt werden.  

Die normalen Bedarfs- und Vorratsarten mit Fälligkeitsdaten am oder nach dem Planungsstartdatum werden in jedes Bestandsprofil geladen. Nach dem Laden werden die verschiedenen Bedarfs- und Vorratsarten nach übergeordneten Prioritäten sortiert, z. B. nach Fälligkeitsdatum, Low-Level-Code, Lagerplatz und Variante. Außerdem werden Auftragsprioritäten auf die verschiedenen Arten angewendet, um sicherzustellen, dass der wichtigste Bedarf zuerst erfüllt wird. Weitere Informationen finden Sie unter [Priorisieren von Aufträgen](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

Wie bereits erwähnt, kann der Bedarf auch negativ sein. Das bedeutet, dass er als Vorrat zu behandeln ist. Im Gegensatz zu den normalen Vorratsarten wird negativer Bedarf jedoch als fester Vorrat betrachtet. Das Planungssystem kann ihn berücksichtigen, wird aber keine Änderungen vorschlagen.  

Allgemein betrachtet das Planungssystem alle Vorräte nach dem Planungsstartdatum als zur Bedarfserfüllung veränderbar. Sobald eine Menge aus einem Vorrat gebucht wird, kann diese jedoch nicht mehr vom Planungssystem geändert werden. Dementsprechend können die folgenden Aufträge nicht neu geplant werden:  

- Freigegebene Produktionsaufträge, bei denen ein Verbrauch oder eine Ausgabe gebucht wurde.  
- Montageaufträge, bei denen ein Verbrauch oder eine Ausgabe gebucht wurde.  
- Umlagerungsaufträge, bei denen die Lieferung gebucht wurde.  
- Einkaufsbestellungen, bei denen der Eingang gebucht wurde.  

Neben dem Laden von Bedarfs- und Vorratsarten werden bestimmte Arten unter Beachtung spezieller Regeln und Abhängigkeiten geladen, die im Folgenden beschrieben werden.  

### <a name="item-dimensions-are-separated"></a>Artikeldimensionen werden separiert  
Der Vorratsplan muss pro Kombination der Dimensionen des Artikel berechnet werden, z. B. Variante und Lagerplatz. Es gibt jedoch keinen Grund, jede theoretische Kombination zu berechnen. Es müssen nur die Kombinationen berechnet werden, die einen Bedarf und/oder einen Vorrat aufweisen.  

Das Planungssystem steuert dies, indem es das Bestandsprofil durchläuft. Wenn eine neue Kombination gefunden wird, erstellt die Anwendung einen internen Datensatz, der die tatsächlichen Kombinationsinformationen enthält. Die Anwendung fügt die SKU als Steuerungsdatensatz (äußere Schleife) ein. Dadurch werden die richtigen Planungsparameter entsprechend einer Kombination aus Variante und Lagerplatz festgelegt, und die Anwendung kann mit der inneren Schleife fortfahren.  

> [!NOTE]  
>  Die Anwendung erfordert bei der Eingabe des Bedarfs und/oder Vorrats für eine bestimmte Kombination von Variante und Lagerplatz keine Eingabe eines SKU-Datensatzes durch den Benutzer. Wenn für eine bestimmte Kombination kein SKU-Datensatz vorhanden ist, erstellt die Anwendung daher ihren eigenen temporären SKU-Datensatz auf der Basis der Daten der Artikelkarte. Wenn auf der Seite „Bestandseinrichtung“ die Option „Lagerplatz erforderlich“ auf „Ja“ festgelegt ist, muss entweder eine SKU erstellt werden oder Komponenten am Lagerplatz müssen auf „Ja“ festgelegt werden. Weitere Informationen finden Sie unter [Planungsdetails: Bedarf an leerem Lagerplatz](design-details-demand-at-blank-location.md).  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serien-/Chargennummern werden nach Spezifikationsstufe geladen  
Attribute in Form von Serien-/Chargennummern werden zusammen mit dem Bedarf und dem Vorrat, denen sie zugeordnet sind, in die Bestandsprofile geladen.  

Bedarfs- und Vorratsattribute werden nach Auftragspriorität sowie nach ihrer Spezifikationsstufe geordnet. Da Serien-/Chargennummernübereinstimmungen die Spezifikationsstufe darstellen, wird der spezifischere Bedarf, wie z. B. eine speziell für eine Verkaufszeile ausgewählte Chargennummer, vor dem weniger spezifischen Bedarf, wie z. B. einem Verkauf aus einer beliebigen Chargennummer, bei der Übereinstimmungssuche bevorzugt.  

> [!NOTE]  
>  Es gibt keine speziellen Priorisierungsregeln für einen Bedarf und Vorrat mit Serien-/Chargennummern, außer der Spezifikationsstufe, die durch die Kombinationen von Serien- und Chargennummern und das Einrichten der Artikelverfolgung für die betroffenen Artikel definiert ist.  

Während des Abgleichs betrachtet das Planungssystem Vorräte mit Serien-/Chargennummern als nicht flexibel. Es wird nicht versuchen, entsprechende Vorräte zu vergrößern oder neu zu planen (es sei denn, sie werden in einer Eins-zu-Eins-Beziehung verwendet). Weitere Informationen unter „Eins-zu-Eins-Beziehungen werden nie aufgelöst“. Dieses Vorgehen schützt den Vorrat davor, mehrere, möglicherweise widersprüchliche Aktionsnachrichten zu erhalten, wenn ein Vorrat unterschiedliche Attribute aufweist – wie z. B. eine Sammlung verschiedener Seriennummern.  

Ein weiterer Grund dafür, dass Vorräte mit Serien-/Chargennummern nicht flexibel sind, ist, dass Serien-/Chargennummern im Allgemeinen so spät im Prozess zugewiesen werden, dass es verwirrend wäre, wenn Änderungen vorgeschlagen werden.  

Der Abgleich von Serien-/Chargennummern berücksichtigt den *eingefrorenen Zeitraum* nicht. Wenn Bedarf und Vorrat nicht synchronisiert sind, schlägt das Planungssystem unabhängig vom Startdatum der Planung Änderungen oder neue Aufträge vor.  

### <a name="order-to-order-links-are-never-broken"></a>Eins-zu-Eins-Verknüpfungen werden nie aufgelöst  
Bei der Planung eines Eins-zu-Eins-Artikels darf der verknüpfte Vorrat nicht für einen anderen Bedarf verwendet werden als den, für den er ursprünglich vorgesehen war. Der verknüpfte Bedarf darf nicht durch einen anderen beliebigen Vorrat gedeckt werden. Dies gilt auch dann, wenn dieser Vorrat aktuell zeitlich und mengenmäßig verfügbar ist. Beispielsweise kann ein Montageauftrag, der in einem Montage-zu-Auftrag-Szenario mit einem Kundenauftrag verknüpft ist, nicht zur Deckung eines anderen Bedarfs verwendet werden.  

Bei Eins-zu-Eins müssen sich Bedarf und Vorrat exakt decken. Das Planungssystem stellt den Vorrat unter allen Umständen sicher. Dies geschieht ohne Berücksichtigung von Auftragsgrößenparametern, Modifikatoren und Mengen im Bestand (mit Ausnahme der Mengen, die sich auf die verknüpften Aufträge beziehen). Aus demselben Grund schlägt das System die Verringerung überschüssiger Vorräte vor, wenn der verknüpfte Bedarf sinkt.  

Dieser Abgleich wirkt sich auch auf das Timing aus. Der durch den Zeitbereich bedingte begrenzte Horizont wird nicht berücksichtigt. Der Vorrat wird neu geplant, wenn sich das Timing des Bedarfs geändert hat. Die Verzögerungszeit wird jedoch beachtet. Sie verhindert, dass Eins-zu-Eins-Vorräte eingeplant werden – außer bei internen Vorräten eines mehrstufigen Produktionsauftrags (Projektauftrag).  

> [!NOTE]  
>  Serien-/Chargennummern können auch für Eins-zu-Eins-Bedarf angegeben werden. In diesem Fall wird der Vorrat nicht standardmäßig als nicht flexibel betrachtet (wie normalerweise bei Serien-/Chargennummern). In diesem Fall führt das System eine Erhöhung/Verringerung durch, wenn sich der Bedarf ändert. Wenn ein Bedarf unterschiedliche Serien-/Chargennummern trägt, z. B. mehr als eine Chargennummer, wird außerdem ein Vorrat pro Charge vorgeschlagen.  

> [!NOTE]  
>  Planungen sollten nicht dazu führen, dass Vorratsaufträge erstellt werden, die durch eine Eins-zu-Eins-Verknüpfung gebunden sind. Wenn die Planung verwendet wird, sollte dies nur zur Generierung des abhängigen Bedarfs in einer Fertigungsumgebung geschehen.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Der Komponentenbedarf wird entsprechend den Änderungen der Produktionsaufträge geladen.  
Bei der Bearbeitung von Produktionsaufträgen muss das Planungssystem die benötigten Komponenten überwachen, bevor diese in das Bedarfsprofil geladen werden. Komponentenzeilen, die sich aus einem geänderten Produktionsauftrag ergeben, ersetzen die des ursprünglichen Auftrags. Dadurch ist sichergestellt, dass das Planungssystem festlegt, dass Planungszeilen für Komponentenbedarf nicht dupliziert werden.  

###  <a name="safety-stock-may-be-consumed"></a><a name="BKMK_SafetyStockMayBeConsumed"></a> Sicherheitsbestand kann verbraucht werden  
Die Sicherheitsbestandsmenge ist in erster Linie eine Bedarfsart und wird daher zum Planungsstartdatum in das Bestandsprofil geladen.  

Der Sicherheitsbestand ist eine Bestandsmenge, die festgelegt wird, um Unsicherheiten im Bedarf während der Vorlaufzeit der Wiederbeschaffung auszugleichen. Er kann jedoch verbraucht werden, wenn eine Entnahme zur Erfüllung eines Bedarfs notwendig ist. In diesem Fall stellt das Planungssystem sicher, dass der Sicherheitsbestand schnell ersetzt wird, indem es einen Vorrat vorschlägt, um die Sicherheitsbestandsmenge zum Zeitpunkt des Verbrauchs wiederzubeschaffen. In dieser Planungszeile wird ein Ausnahme-Warnungssymbol angezeigt. Dieses zeigt dem Planer, dass der Sicherheitsbestand über einen Ausnahmeauftrag für die fehlende Menge teilweise oder vollständig verbraucht wurde.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Geplanter Bedarf wird durch Verkaufsaufträge reduziert  
Die Bedarfsplanung stellt den erwarteten zukünftigen Bedarf dar. Während der tatsächliche Bedarf eingegeben wird, typischerweise in Form von Verkaufsaufträgen für produzierte Artikel, verringert sich die Planungsmenge.  

Die Planung selbst wird durch Verkaufsaufträge nicht reduziert; sie bleibt gleich. Die geplanten Mengen, die in der Planungsberechnung verwendet werden, werden jedoch reduziert (um die Verkaufsauftragsmengen), bevor die verbleibende Menge, falls vorhanden, in das Bedarfsbestandsprofil eingeht. Wenn das Planungssystem die tatsächlichen Verkäufe während einer Periode untersucht, werden sowohl offene Verkaufsaufträge als auch Artikelsachkontoeinträge aus gelieferten Verkäufen berücksichtigt – es sei denn, diese stammen aus einem Rahmenauftrag.  

Ein Benutzer muss einen gültigen Planungszeitraum definieren. Das Datum der geplanten Menge definiert den Beginn des Zeitraums, und das Datum der nächsten Planung definiert das Ende des Zeitraums.  

Die Planung für Perioden vor dem Planungszeitraum wird nicht verwendet – unabhängig vom Verbrauch. Die erste interessante Planungszahl ist entweder die zum Startdatum der Planung oder das nächstgelegene Datum vor dem Startdatum der Planung.  

Die Planung kann für den unabhängigen Bedarf, z. B. für Verkaufsaufträge, oder für den abhängigen Bedarf, z. B. für Produktionsauftragskomponenten (Modulplanung), erfolgen. Ein Artikel kann beide Planungsarten verwenden. Während der Planung erfolgt der Verbrauch separat, zuerst für den unabhängigen Bedarf und dann für den abhängigen Bedarf.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Bedarf für Rahmenaufträge wird durch Verkaufsaufträge reduziert  
Die Planung wird durch den Rahmenverkaufsauftrag ergänzt, um den zukünftigen Bedarf eines bestimmten Debitors festzulegen. Wie bei der (nicht spezifizierten) Planung sollten die tatsächlichen Verkäufe den erwarteten Bedarf in Anspruch nehmen, und die verbleibende Menge sollte in das Bedarfsbestandsprofil eingehen. Auch hier führt der Verbrauch nicht zu einer tatsächlichen Reduzierung des Rahmenauftrags.  

Die Planungsberechnung berücksichtigt offene Verkaufsaufträge, die mit dieser bestimmten Rahmenauftragszeile verbunden sind, nicht jedoch Gültigkeitszeiträume. Sie berücksichtigt auch keine gebuchten Aufträge, da der Buchungsvorgang die ausstehende Rahmenauftragsmenge bereits reduziert hat.

## <a name="prioritizing-orders"></a>Priorisierung von Aufträgen
Innerhalb einer bestimmten SKU stellt das Anforderungs- oder Verfügbarkeitsdatum die höchste Priorität dar; der Bedarf von heute sollte vor dem Bedarf der nächsten Woche gedeckt werden. Zusätzlich zu dieser allgemeinen Priorität schlägt das Planungssystem jedoch auch vor, welche Bedarfsart vor der Deckung eines anderen Bedarfs gedeckt werden sollte. Ebenso schlägt es vor, welche Vorratsquelle vor der Anwendung anderer Vorratsquellen angewendet werden sollte. Dies geschieht entsprechend der Reihenfolge der Prioritäten.  

Der geladene Bedarf und der Vorrat ergeben ein Profil für den geplanten Bestand gemäß den folgenden Prioritäten:  

### <a name="priorities-on-the-demand-side"></a>Prioritäten auf der Bedarfsseite  
1. Bereits geliefert: Artikelsachkontoeintrag  
2. Einkaufsreklamationsauftrag  
3. Verkaufsauftrag  
4. Serviceauftrag  
5. Produktionskomponentenbedarf  
6. Montageauftragszeile  
7. Ausgehender Umlagerungsauftrag  
8. Rahmenauftrag (der nicht bereits durch entsprechende Verkaufsaufträge verbraucht wurde)  
9. Planung (die nicht bereits durch andere Verkaufsaufträge verbraucht wurde)  

> [!NOTE]  
>  Einkaufsreklamationen sind normalerweise nicht in die Vorratsplanung eingebunden. Sie sollten immer aus der Charge reserviert werden, die retourniert werden soll. Wenn sie nicht reserviert werden, spielen Einkaufsreklamationen eine Rolle bei der Verfügbarkeit und werden hoch priorisiert, um zu vermeiden, dass das Planungssystem eine Bestellung vorschlägt, nur um eine Einkaufsreklamation abzudecken.  

### <a name="priorities-on-the-supply-side"></a>Prioritäten auf der Vorratsseite  
1. Bereits im Bestand: Artikelsachkontoeintrag (Planungsflexibilität = keine)  
2. Verkaufsreklamationsauftrag (Planungsflexibilität = keine)  
3. Eingehender Umlagerungsauftrag  
4. Produktionsauftrag  
5. Montageauftrag  
6. Einkaufsbestellung  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Priorität bezogen auf den Status von Bedarf und Vorrat  
Abgesehen von den Prioritäten, die durch die Bedarfs- und Vorratsart gegeben sind, definiert auch der aktuelle Status der Aufträge im Ausführungsprozess eine Priorität. So wirken sich z. B. Lagerortaktivitäten aus. Auch der Status von Verkaufs-, Einkaufs-, Umlagerungs-, Montage- und Produktionsaufträgen wird berücksichtigt:  

1. Teilweise bearbeitet (Planungsflexibilität = Keine)  
2. Bereits in Bearbeitung im Lagerort (Planungsflexibilität = keine)  
3. Freigegeben – alle Auftragstypen (Planungsflexibilität = unbegrenzt)  
4. Umgewandelter geplanter Produktionsauftrag (Planungsflexibilität = unbegrenzt)  
5. Geplant/offen – alle Auftragstypen (Planungsflexibilität = unbegrenzt)

## <a name="balancing-supply-with-demand"></a>Abgleich von Vorrat und Bedarf
Der Kern des Planungssystems besteht im Abgleich von Bedarf und Vorrat. Dazu werden Benutzeraktionen vorgeschlagen, um die Vorratsaufträge im Falle eines Ungleichgewichts zu revidieren. Dieses findet pro Kombination von Variante und Lagerort statt.  

Stellen Sie sich vor, dass jedes Lagerprofil eine Zeichenfolge aus den Bedarfsereignissen (sortiert nach Datum und Priorität) und eine entsprechende Zeichenfolge von Vorratsereignissen enthält. Jedes Ereignis verweist zurück auf seinen Herkunftsartstyp und seine Identifizierung. Die Regeln für den Ausgleich des Artikels sind einfach. Zu jedem Zeitpunkt des Vorgangs können vier Instanzen des Abgleichs von Bedarf und Vorrat auftreten:  

1. Kein Bedarf oder Vorrat für den Artikel => die Planung ist abgeschlossen (oder soll nicht beginnen).  
2. Bedarf existiert, aber es ist kein Vorrat vorhanden=> Vorrat soll vorgeschlagen werden.  
3. Vorrat existiert, aber es ist kein Bedarf vorhanden=> Vorrat soll storniert werden.  
4. Bedarf und Vorrat sind vorhanden => Fragen sollten gestellt und beantwortet werden, bevor das System sicherstellen kann, dass der Bedarf befriedigt wird und der Vorrat ausreicht.  

    Wenn das Timing des Vorrats nicht passt, kann der Vorrat vielleicht wie folgt neu geplant werden:  

    1.  Wenn der Vorrat früher als der Bedarf platziert wird, kann der Vorrat vielleicht so neu ausgeplant werden, dass der Bestand so gering wie möglich ist.  
    2.  Wenn der Vorrat später als der Bedarf platziert wird, kann der Vorrat vielleicht neu eingeplant werden. Andernfalls schlägt das System einen neuen Vorrat vor.  
    3.  Wenn der Vorrat den Bedarf an dem Datum erfüllt, kann das Planungssystem fortfahren, zu untersuchen, ob die Menge des Vorrats den bedarf decken kann.  

    Sobald die Zeitplanung erfolgt ist, kann die entsprechende bereitzustellende Menge wie folgt berechnet werden:  

    1.  Wenn die Vorratsmenge kleiner als der Bedarf ist, ist es möglich, dass die Vorratsmenge erhöht werden kann (oder nicht, wenn Sie durch eine Höchstmengenrichtlinie begrenzt ist).  
    2.  Wenn die Vorratsmenge größer als der Bedarf ist, ist es möglich, dass die Vorratsmenge reduziert werden kann (oder nicht, wenn Sie durch eine Mindestmengenrichtlinie begrenzt ist).  

    An dieser Stelle besteht eine von zwei Situationen:  

    1.  Der aktuelle Bedarf kann abgedeckt werden, in welchem Fall er geschlossen werden kann und die Planung für den folgenden Bedarf begonnen werden kann.  
    2.  Das Vorrat hat sein Maximum erreicht, ein Teil der Bedarfsmenge wurde nicht abgedeckt. In diesem Fall kann das Planungssystem den aktuellen Vorrat schließen und mit dem nächsten fortfahren.  

 Der Vorgang beginnt von vorn mit dem folgenden Bedarf und dem folgenden Vorrat oder umgekehrt. Der aktuelle Vorrat kann möglicherweise auch diesen nächsten Bedarf abdecken, oder der aktuelle Bedarf wurde noch nicht vollständig abgedeckt.  

### <a name="rules-concerning-actions-for-supply-events"></a>Regeln im Hinblick auf Aktionen für Vorratsereignisse  
Wenn das Planungssystem eine top-down Berechnung ausführt, in der der Vorrat den Bedarf erfüllen muss, gilt der Bedarf als entnommen, d.h. es liegt außerhalb des Steuererung des Planungssystems. Jedoch kann die Vorratsseite verwaltet werden. Daher wird vom Planungssystem vorgeschlagen, neue Beschaffungsaufträge zu erstellen, bestehenden neu zu planen und/oder die Bestellmenge zu ändern. Wenn ein vorhandener Beschaffungsauftrag überflüssig wird, schlägt das System dem Benutzer vor, ihn zu stornieren.  

Wenn der Benutzer einen vorhandenen Beschaffungsauftrag aus den Planungsvorschlägen ausschließen möchte, kann er angeben, dass keine Planungsflexibilität besteht (Planungsflexibilität = Keine). Dann wird überschüssiger Vorrat aus diesem Auftrag verwendet, um Bedarf zu decken, aber keine Aktion wird vorgeschlagen.  

Im Allgemeinen haben alle Vorräte eine Planungsflexibilität, die durch den Zustand der einzelnen vorgeschlagenen Aktionen eingeschränkt ist.  

-   **Neu ausplanen**: Das Datum eines vorhandenen Beschaffungsauftrags kann ausgeplant werden, um das Fälligkeitsdatum des Bedarfs zu erfüllen, es sei denn:  

    -   Es stellt den Lagerbestand dar (immer mit Tag Null).  
    -   Es enthält einen Auftrag-zu-Auftrag-Link zu einem anderen Bedarf.  
    -   Es liegt außerhalb der durch den Zeitrahmen definierten, neu geplanten Seite.  
    -   Es gibt einen näheren Bestand, der verwendet werden könnte.  
    -   Andererseits entscheidet sich der Benutzer möglicherweise zu einer Neuplanung, weil  
    -   Der Beschaffungsauftrag wurde bereits an einem früheren Datum mit einem anderen Bedarf verbunden.  
    -   Das erforderliche Neuplanung ist so minimal, dass der Benutzer sie als geringfügig ansehen wird.  

-   **Neu einplanen**: Das Datum eines vorhandenen Beschaffungsauftrags kann eingeplant werden, ausgenommen unter den folgenden Bedingungen:  

    -   Es wird direkt mit einem anderen Bedarf verknüpft.  
    -   Es liegt außerhalb der durch den Zeitrahmen definierten, neu geplanten Seite.  

> [!NOTE]  
>  Wenn ein Artikel unter Verwendung eines Minimalbestands geplant wird, kann der Beschaffungsauftrag immer bei Bedarf geplant werden. Dies ist häufig in den vorwärtsgeplanten Beschaffungsaufträgen, die durch einen Minimalbestand gestartet werden.  

-   **Zugangs-Menge**: Die Menge eines vorhandenen Beschaffungsauftrags kann erhöht werden, damit der Bedarf erfüllt werden kann, es sei denn, der Beschaffungsauftrag ist direkt mit einem Bedarf durch einen Auftrag-zu-Auftrag-Link verknüpft.  

> [!NOTE]  
>  Obwohl es möglich ist, den Beschaffungsauftrag zu erhöhen, kann dies durch eine maximale Auftragsgröße eingeschränkt sein.  

-   **Menge reduzieren**: Ein vorhandener Beschaffungsauftrag mit einem Überschuss im Vergleich zu einem vorhandenen Bedarf kann reduziert werden, damit der Bedarf erfüllt werden kann.  

> [!NOTE]  
>  Obwohl die Menge verringert werden kann, ist möglicherweise immer noch Überschuss im Vergleich zum Bedarf vorhanden, und zwar aufgrund einer Mindestauftragsmenge oder eines Auftragsvielfachen.  

-   **Abbrechen**: Als spezieller Vorfall der Mengenverminderungsaktion könnte der Beschaffungsauftrag storniert werden, wenn er bis auf Null verringert wurde.  
-   **Neu**: Wenn kein Beschaffungsauftrag existiert oder jedoch ein existierender, der nicht geändert werden kann, um der erforderlichen Menge im angeforderten Fälligkeitsdatum zu genügen, wird ein neuer Beschaffungsauftrag vorgeschlagen.  

### <a name="determining-the-supply-quantity"></a>Bestimmen der Vorratsmenge  
Durch den Benutzer definierte Planungsparameter steuern die vorgeschlagene Menge eines jeden Beschaffungsauftrags.  

Wenn das Planungssystem die Menge eines neuen Beschaffungsauftrags oder die Mengenänderung in bestehenden Aufträgen berechnet, kann sich die vorgeschlagene Menge von der tatsächlich benötigten unterscheiden.  

Wenn ein Maximalbestand oder eine feste Auftragsmenge ausgewählt werden, wird die vorgeschlagene Menge erhöht, um diese feste Menge oder den Maximalbestand zu erfüllen. Wenn ein Wiederbeschaffungsverfahren einen Minimalbestand verwendet, wird die Menge mindestens so erhöht, dass der Minimalbestand erreicht wird.  

 Die vorgeschlagene Menge kann in dieser Sequenz geändert werden:  

1. Bis zur maximalen Auftragsmenge (falls vorhanden).  
2. Aufwärts bis zur Mindestbestellmenge.  
3. Aufwärts bis zum nächsten Losgrößenrundungsfaktor. (Im Falle fehlerhafter Einstellungen verstößt dies möglicherweise gegen die maximale Auftragsmenge.)  

### <a name="order-tracking-links-during-planning"></a>Bedarfsverursacherverknüpfungen bei der Planung  
Hinsichtlich des Auftragsnachverfolgung während der Planung ist es wichtig zu erwähnen, dass das Planungssystem die dynamisch erstellten Auftragsnachverfolgungsverknüpfungen für die Artikel-/Varianten-/Lagerortkombinationen neu anordnet.  

Hierfür gibt es zwei Gründe:  

-   Das Planungssystem muss in der Lage sein, seine Vorschläge zu begründen; dass der Gesamtbedarf gedeckt wurde und dass keine Beschaffungsaufträge überflüssig sind.  
-   Dynamisch erstellte Auftragsnachverfolgungslinks müssen regelmäßig nachjustiert werden.  

Im Laufe der Zeit geraten dynamische Bedarfsverursacherverknüpfungen aus der Balance, da das gesamte Bedarfsverursachernetzwerk erst dann wiederhergestellt wird, wenn ein Bedarf- oder Vorratsereignis tatsächlich geschlossen ist.  

Vor dem Ausgleich des Vorrats nach Bedarf löscht die Anwendung alle vorhandenen Auftragsnachverfolgungslinks. Dann während des Ausgleichsvorgangs, wenn ein Bedarfs- oder Zubehörereignis abgeschlossen wird, werden neue Bedarfsverursacherverknüpfungen zwischen Bedarf und Angebot erstellt.  

> [!NOTE]  
>  Das Planungssystem erstellt auch dann ausgeglichene Auftragsverfolgungsverknüpfungen, wenn der Artikel nicht für die dynamische Auftragsverfolgung festgelegt ist (wie oben beschrieben).
## <a name="closing-demand-and-supply"></a>Schließen von Bedarf und Vorrat
Wenn der Vorrat abgeglichen wurde, gibt es drei mögliche Endsituationen:  

* Die benötigte Menge und das Datum der Bedarfsereignisse wurden erfüllt, und die Planung für den Artikel kann geschlossen werden. Das Vorratsereignis ist noch offen und kann möglicherweise den nächsten Bedarf decken, der Ausgleichsvorgang kann daher erneut mit dem aktuellen Vorratsereignis und dem nächsten Bedarf starten.  
* Der Beschaffungsauftrag kann nicht geändert werden, um den gesamten Bedarf zu decken. Das Bedarfsereignis ist noch offen, mit einigen nicht abgedeckten Mengen, die möglicherweise vom nächsten Bedarfsereignis abgedeckt werden. Daher wird das aktuelle Vorratsereignis geschlossen, sodass der Ausgleichsvorgang mit dem aktuellen Bedarfs- und dem nächsten Vorratsereignis erneut beginnen kann.  
* Der gesamte Bedarf ist abgedeckt; es gibt keinen folgenden Bedarf (oder es gab überhaupt keinen Bedarf). Wenn überschüssiger Vorrat vorhanden ist, kann dieser vermindert (oder storniert) und dann geschlossen werden. Es ist möglich, dass zusätzliche Zubehörereignisse weiter entlang der Kette vorhanden sind, und diese sollten ebenfalls annulliert werden.  

Schließlich erstellt das Planungssystem ein Auftragsnachverfolgungslink zwischen dem Vorrat und dem Bedarf.  

### <a name="creating-the-planning-line-suggested-action"></a>Die Planungszeile (vorgeschlagene Aktion) erstellen  
Wenn eine Aktion – Neu, Menge ändern, Neu planen, Neu planen und Menge ändern oder Stornieren – für die Revision des Beschaffungsauftrags vorgeschlagen wird, erstellt das Planungssystem, eine Planung auf dem Planungsarbeitsblatt. Aufgrund der Auftragsnachverfolgung wird die Planungszeile nicht nur erstellt, wenn das Vorratsereignis geschlossen wird, sondern auch, wenn das Nachfrageereignis geschlossen wird, auch wenn das Vorratsereignis möglicherweise noch offen und abhängig von zusätzlichen Änderungen ist, wenn das nächste Nachfrageereignis verarbeitet wird. Dies bedeutet, dass die Planungszeile, wenn sie zuerst erstellt wird, möglicherweise erneut geändert wird.  

Um Datenbankzugriff zu minimieren, wenn Sie Fertigungsaufträge bearbeiten, können Sie die Planungszeile in drei Ebenen verwalten, mit dem Ziel, das am wenigsten anspruchsvolle Bestanderhaltungsniveau auszuführen:  

* Erstellen Sie nur die Planungszeile mit dem aktuellen Fälligkeitsdatum und der Menge, aber ohne Arbeitsplan und Komponenten.  
* Arbeitsplan einschließen: Der geplante Arbeitsplan wird einschließlich Berechnung des Start- und Enddatum und -Zeiten ausgebreitet. Dieses ist anspruchvoll in Bezug auf Datenbankzugriffe. Um das End- und die Fälligkeitsdatum zu bestimmen, kann es notwendig sein, dies zu berechnen, auch wenn das Vorratsereignis nicht abgeschlossen wurde (im Fall der Vorwärtsterminierung).  
* Strukturstückliste einschließen: Dies kann warten bis kurz vor dem Abschluss des Vorratsereignisses.  

Damit sind die Beschreibungen dazu, wie Bedarf und Vorrat vom Planungssystem geladen, priorisiert und ausgeglichen werden, abgeschlossen. Zur Integration mit dieser Vorratsplanungsaktivität muss das System sicherstellen, dass der erforderliche Bestand jedes geplanten Artikel gemäß seinen Richtlinien für die Nachbestellung aufrechterhalten wird.

## <a name="see-also"></a>Weitere Informationen  
 [Entwurfsdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
 [Entwurfsdetails: Handhabung von Richtlinien zur Wiederbestellung](design-details-handling-reordering-policies.md)   
 [Entwurfsdetails: Vorratsplanung](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]