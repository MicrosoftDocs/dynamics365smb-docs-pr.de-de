---
title: 'Designdetails: - Zentrale Konzepte des Planungssystems| Microsoft Docs'
description: Die Planungsfunktionen sind in der Stapelverarbeitung enthalten, die zuerst die entsprechenden Artikel und die Periode auswählen, um die Planung zu wählen und dann die Aktion dem Anwender vorschlägt, die er treffen muss, basierend auf der Nachfrage-/Bestandsituation und die Artikelplanungsparameter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ff18b81f71c8d4877c42f614c5ef485a43b2b494
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390674"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Designdetails: Zentrale Konzepte des Planungssystems
Die Planungsfunktionen sind in einer Stapelverarbeitung enthalten, die zuerst die entsprechenden Artikel und die Periode für die Planung auswählt. Dann ruft die Stapelverarbeitung entsprechend der Stücklistenebene jedes Artikels (Stücklistenposition), eine Codeeinheit ab, die einen Beschaffungsplan erstellt, indem Angebot-Nachfrage-Sätze abgegeglichen und dem Benutzer mögliche Aktionen vorgeschlagen werden. Die vorgeschlagenen Aktionen erscheinen als Zeilen im Planungsarbeitsblatt oder Bestellarbeitsblatt.  

![Inhalt der Seite Planungsarbeitsblatt](media/NAV_APP_supply_planning_1_planning_worksheet.png "Inhalt der Seite Planungsarbeitsblatt")  

Der Planer eines Unternehmens, wie etwa ein Einkäufer oder ein Produktionsplaner, ist wahrscheinlich der Benutzer des Planungssystems. Das Planungssystem hilft dem Benutzer durch die Ausführung der umfangreichen aber insgesamt recht einfachen Berechnungen eines Plans. Der Benutzer kann sich dann auf die Lösung der komplizierteren Probleme konzentrieren, wenn keine Standardfälle vorliegen.  

Das Planungssystem wird durch den erwarteten und den tatsächlichen Debitorenbedarf gesteuert, etwa durch Planung und Verkaufsaufträge. Ein Ausführen der Planungsberechnung bewirkt, dass die Anwendung dem Benutzer bestimmte vorzunehmende Aktionen vorschlägt, die sich auf mögliche Beschaffungen von Kreditoren, auf die Montage oder Produktion oder auf Umlagerungen zu anderen Lagern beziehen. Diese vorgeschlagenen Aktionen sind etwa, neue Beschaffungsaufträge, wie Einkaufsbestellung oder Fertigungsaufträge zu erstellen. Wenn es bereits Beschaffungsaufträge gibt, könnten die vorgeschlagenen Aktionen so aussehen, dass die Aufträge vergrößert oder schneller erteilt werden sollen, damit den Bedarfsänderungen Rechnung getragen wird.  

Außerdem hat das Planungssystem die Aufgabe sicherzustellen, dass der Lagerbestand nicht unnötig wächst. Im Fall eines abnehmenden Bedarfs wird das Planungssystem vorschlagen, dass vorhandene Ersatzaufträge zurückgestellt, mengenmäßig verringert oder storniert werden sollten.  

Nettobedarf und Prod.-Programmplanung, Änderungsplanung berechnen und Neuplanung berechnen sind alle Funktionen innerhalb einer Codeeinheit, die die Planungslogik enthält. Die Beschaffungsplanberechnung schließt jedoch verschiedene untergeordnete Systeme mit ein.  

Beachten Sie, dass das Planungssystem keine dedizierte Logik für das Kapazitätsplanieren oder die Feinterminierung umfasst. Deshalb werden solche Planungsarbeiten als separate Disziplin ausgeführt. Der Mangel an direkter Integration zwischen den beiden Bereichen bedeutet auch, dass substanzielle Kapazitäts- oder Zeitplanänderungen erfordern, dass die Planung erneut durchgeführt wird.  

## <a name="planning-parameters"></a>Planungsparameter  
Planungsparameter, die der Benutzer für einen Artikel oder eine Gruppe Elemente einrichtet, steuern die Aktionen, die das Planungssystem in verschiedenen Situationen vorschlägt. Die Planungsparameter werden auf jeder Artikelkarte definiert, um zu steuern, wann, wie viel und wie aufgefüllt werden soll.  

Planungsparameter können für jede mögliche Kombination aus Artikel, Variante und Lagerort auch definiert werden, indem Sie Lagerhaltungsdaten für alle erforderlichen Kombinationen einrichten, und dann einzelne Parameter angeben.  

Weitere Informationen finden Sie unter [Designdetails: Wiederbeschaffungsverfahren behandeln](design-details-handling-reordering-policies.md) und [Designdetails: Planungsparameter](design-details-planning-parameters.md).  

## <a name="planning-starting-date"></a>Planungsdatum ändern  
Um einen Beschaffungsplan zu vermeiden, der offene Aufträge in der Vergangenheit enthält und möglicherweise unmögliche Aktionen vorschlägt, behandelt das Planungssystem alle Daten vor dem Startdatum als fixierte Zone, in der die folgende Sonderregelung gilt:  

Alle Vorräte und Bedarfe vor dem Startdatum der Planungsperiode gelten als Teil des Lagerbestands oder als geliefert.  

Mit anderen Worten: Es nimmt an, dass der Plan für die Vergangenheit gemäß dem vorhandenen Plan ausgeführt wurde.  

Weitere Informationen finden Sie unter [Umgang mit Aufträgen vor dem Planungs-Startdatum](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).  

## <a name="dynamic-order-tracking-pegging"></a>Dynamische Auftragsnachverfolgung (Pegging)  
Die dynamische Auftragsnachverfolgung, die eine simultane Erstellung von Ereignismeldungen im Planungsarbeitsblatt ermöglicht, ist kein Teil des Beschaffungsplanungssystems in [!INCLUDE[prod_short](includes/prod_short.md)]. Dieses Funktion verknüpft in der Echtzeit den Bedarf und die Mengen, die ihn abdecken können, sobald ein neuer Bedarf oder eine Bedarfssicherung erstellt oder geändert wird.  

Wenn beispielsweise der Benutzer einen Verkaufsauftrag eingibt oder ändert, sucht das dynamische Auftragsnachverfolgungssystem sofort nach einem geeigneten Vorrat, um den Bedarf zu decken. Dies kann aus dem Lagerbestand oder aus einem erwarteten Beschaffungsauftrag sein (wie einer Einkaufsbestellung oder einem Fertigungsauftrag). Wenn eine Versorgungsquelle gefunden wird, erstellt das System eine Verknüpfung zwischen dem Bedarf und dem Vorrat, und zeigt sie in schreibgeschützten Seiten an, auf die von den einbezogenen Belegzeilen zugegriffen wird. Wenn ein entsprechender Vorrat nicht gefunden wird, erstellt das dynamische Bedarfsverursachersystem Ereignismeldungen im Planungsarbeitsblatt mit Beschaffungsplanvorschlägen, die den dynamischen Ausgleich widerspiegeln. Entsprechend bietet das dynamische Auftragsnachverfolgungssystem ein sehr grundlegendes Planungssystem, das für den Planer und andere Rollen in der internen Lieferkette hilfreich sein kann.  

Entsprechend kann die dynamische Auftragsnachverfolgung als Tool betrachtet werden, das dem Benutzer hilft, festzulegen, ob Beschaffungsauftragsvorschläge akzeptiert werden sollen. Aus Vorratssicht kann ein Benutzer sehen, welcher Bedarf den Vorrat erstellt hat, und aus Bedarfssicht, welcher Vorrat den Bedarf abdecken soll.  

![Beispiel für eine dynamische Auftragsnachverfolgung](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Beispiel für eine dynamische Auftragsnachverfolgung")  

Weiter Informationen finden Sie unter [Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  

In Unternehmen mit geringem Warenfluss und weniger fortschrittlichen Produktstrukturen kann es angemessen sein, die dynamische Auftragsnachverfolgung als Haupthilfsmittel der Vorratsplanung zu verwenden. In ausgelasteteren Umgebungen sollte jedoch das Planungssystem verwendet werden, um jederzeit einen korrekt saldierten Beschaffungsplan sicherzustellen.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamische Auftragsnachverfolgung vs. Planungssystem  
Auf den ersten Blick kann es schwierig sein, zwischen dem Planungssystem und der dynamischen Auftragsnachverfolgung zu unterscheiden. Beide Funktionen zeigen die Ausgabe im Planungsarbeitsblatt an, wobei sie Aktionen vorschlagen, die der Planer ausführen soll. Diese Ausgabe wird jedoch auf andere Weise erstellt.  

Das Planungssystem behandelt das gesamte Vorrats- und Bedarfsmuster eines bestimmten Artikels auf allen Ebenen der Stücklistenhierarchie entlang der Zeitachse, während die dynamische Auftragsnachverfolgung nur die Situation des Auftrags behandelt, der sie aktiviert hat. Beim Ausgleichen von Bedarf und Angebot erstellt das Planungssystem Verknüpfungen in einem vom Benutzer aktivierten Batchmodus erstellt, während die dynamische Auftragsnachverfolgung die Verknüpfungen automatisch während der Verarbeitung erstellt, wenn der Benutzer einen Bedarf oder eine Bedarfssicherung, wie einen Verkaufsauftrag oder eine Einkaufsbestellung, in die Anwendung eingibt.  

Die dynamische Auftragsnachverfolgung richtet Verknüpfungen zwischen Bedarf und Vorrat ein, wenn Daten eingegeben werden, und zwar jeweils nach der ersten Eingabe. Dieses kann zu Störung in den Prioritäten führen. Beispielsweise kann ein zuerst mit einem Fälligkeitsdatum im nächsten Monat eingegebener Verkaufsauftrag mit dem Vorrat im Bestand verknüpft sein, während der nächste, morgen fällige, Verkaufsauftrag eine Aktionsmeldung auslöst, die besagt, dass zur Abdeckung ein neuer Einkaufsauftrag erstellt werden muss, wie nachfolgend illustriert.  

![Beispiel der Auftragsnachverfolgung in der Beschaffungsplanung 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Beispiel der Auftragsnachverfolgung in der Beschaffungsplanung 1")  

Demgegenüber befasst sich das Planungssystem mit allen Bedarfen und Vorräten für einen bestimmten Artikel, in priorisierter Reihenfolge gemäß Fälligkeitsdaten und Auftragsarten, d.h. auf der Grundlage des Prinzips des ersten Bedarfs. Löscht alle Auftragsnachverfolgungslinks, die dynamisch erstellt wurden und stellt diese gemäß der Fälligkeitsdatumspriorität wieder her. Wenn das Planungssystem ausgeführt wurde, hat es alle gestörten Gleichgewichte zwischen Bedarf und Vorrat gelöst, wie unten für dieselben Daten angezeigt.  

![Beispiel der Auftragsnachverfolgung in der Beschaffungsplanung 2](media/NAV_APP_supply_planning_1_planning_graph.png "Beispiel der Auftragsnachverfolgung in der Beschaffungsplanung 2")  

Nach der Planung bleiben keine Ereignismeldungen in der Ereignismeldungstabelle, da sie durch die vorgeschlagenen Aktionen im Planungsarbeitsblatt ersetzt wurden  

Weitere Informationen finden Sie unter [Auftragsnachverfolgungslinks in der Planung](design-details-balancing-demand-and-supply.md#seriallot-numbers-are-loaded-by-specification-level).  

## <a name="sequence-and-priority-in-planning"></a>Reihenfolge und Priorität in der Planung  
Wenn ein Plan eingerichtet wird, ist die Reihenfolge der Berechnungen wichtig, um die Arbeit innerhalb eines angemessenen Zeitrahmens zu erledigen. Zusätzlich spielt die Priorisierung von Anforderungen und Ressourcen eine wichtige Rolle bei der Erlangung bester Ergebnisse.  

Das Planungssystem in [!INCLUDE[prod_short](includes/prod_short.md)] ist bedarfsgesteuert. Artikel auf hoher Ebene sollten vor Artikeln auf niedriger Ebene geplant werden, der Plan für Artikel auf hoher Ebene weiteren Bedarf für Artikel auf niedriger Ebene generieren könnte. das bedeutet zu, Beispiel, dass die Einzelhandelsstandorte geplant werden sollten, bevor Vertriebsstellen geplant werden, da der Plan für einen Einzelhandelsstandort zusätzlichen Bedarf aus der Vertriebsstelle umfassen kann. Auf einem detaillierten Ausgleich bedeutet dies auch, dass ein Verkaufsauftrag keinen neuen Beschaffungsauftrag auslösen soll, wenn ein bereits freigegebener Beschaffungsauftrag den Verkaufsauftrag abdecken kann. Ebenso sollte ein Lagerartikel mit einer bestimmten Chargennummer nicht zugewiesen werden, um einen generischen Bedarf zu decken, wenn ein anderer Bedarf diese bestimmte Charge benötigt.  

### <a name="item-priority--low-level-code"></a>Artikelpriorität Stücklistenebene  
In einer Produktionsumgebung wird der Bedarf für einen fertigen, verkäuflichen Artikel zu einem abgeleiteten Bedarf für Komponenten, die den produzierten fertigen Artikel enthalten, führen. Die Stücklistenstruktur steuert die Komponentenstruktur und kann mehrere Ebenen von halbfertigen Artikel enthalten. Die Absatzplanung eines Artikels in einer Ebene verursacht abgeleiteten Bedarf für Komponenten auf der nächsten Stufe, und so weiter. Schließlich führt dies zu abgeleitetem Bedarf für Einkaufsartikel. Deshalb plant das Planungssystem für Artikel nach ihrer Rangfolge in der gesamten Stücklistenhierarchie, beginnend mit den fertig gestellten absatzfähigen Artikeln oben und dann abwärts durch die Produktstruktur bis zu den Artikeln unterer Ebenen (nach dem Low-level-Code).  

![Planung für Stücklisten](media/NAV_APP_supply_planning_1_BOM_planning.png "Planung für Stücklisten")  

Die Abbildungen illustrieren, in welcher Reihenfolge das System Vorschläge für Beschaffungsaufträge auf der obersten Ebene macht und, wenn der Benutzer diese Vorschläge akzeptiert, auch für Artikel auf unteren Ebenen.  

Weitere Informationen zu Überlegungen für die Fertigung finden Sie unter [Auslastung der Lagerprofile](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

#### <a name="optimizing-performance-for-low-level-calculations"></a>Optimieren der Leistung für Low-Level-Berechnungen
Low-Level-Codeberechnungen können sich auf die Systemleistung auswirken. Um die Auswirkungen zu verringern, können Sie **Dynamische Low-Level-Codeberechnung** auf der Seite **Produktionseinrichtung** deaktivieren. Wenn Sie das tun, schlägt [!INCLUDE[prod_short](includes/prod_short.md)] vor, dass Sie einen wiederkehrenden Projektwarteschlangenposten erstellen, der die Low-Level-Codes täglich aktualisiert. Sie können sicherstellen, dass das Projekt außerhalb der Arbeitszeit ausgeführt wird, indem Sie eine Startzeit im Feld **Frühestes Startdatum/früheste Startzeit** angeben.

Sie können auch Logik aktivieren, die Low-Level-Codeberechnungen beschleunigt, indem Sie **Low-Level-Codeberechnung optimieren** auf der Seite **Produktionseinrichtung** auswählen. 

> [!IMPORTANT]
> Wenn Sie wählen, die Leistung zu optimieren, wird [!INCLUDE[prod_short](includes/prod_short.md)] neue Berechnungsmethoden verwenden, um Low-Level-Codes zu bestimmen. Wenn Sie eine Erweiterung haben, die sich auf die Ereignisse stützt, die von den alten Berechnungen verwendet wurden, funktioniert die Erweiterung möglicherweise nicht mehr.   

### <a name="locations--transfer-level-priority"></a>Lagerorte / Übertragung-Ebenen-Priorität  
Unternehmen, die an mehr als einem Standort arbeiten, müssen möglicherweise für jeden Standort einzeln planen. Beispielsweise können sich der Sicherheitsbestand eines Artikels und dessen Wiederbeschaffungsrichtlinien sich von einem Lagerort zu einem anderen unterscheiden. In diesem Fall müssen die Planungsparameter pro Artikel und auch pro Lagerort angegeben werden.  

Dies wird durch die Verwendung von Lagerhaltungsdaten unterstützt, in denen einzelne Planungsparameter auf der Lagerhaltungsdatenebene angegeben werden können. Eine SKU kann als ein Artikel an einem bestimmten Lagerort betrachtet werden. Wenn der Benutzer keine SKU für diesen Lagerort definiert hat, verwendet die Anwendung die Parameter, die auf der Artikelkarte eingerichtet wurden. Die Anwendung berechnet einen Plan nur für aktive Lagerorte, d.h., wo sich der bestehende Bedarf oder Vorrat für den jeweiligen Artikel befindet.  

Generell kann jeder Artikel an einem Lagerort bearbeitet werden, der Ansatz der Anwendung zum Lagerortkonzept ist aber sehr streng. Beispielsweise kann ein Verkaufsauftrag an einem Lagerort nicht durch eine vorrätige Menge an einem anderen Lagerort erfüllt werden. Die Menge im Lager muss dem zuerst zu dem Lagerort übertragen werden, der auf dem Verkaufsauftrag angegeben ist.  

![Planung für Lagerhaltungseinheiten](media/NAV_APP_supply_planning_1_SKU_planning.png "Planung für Lagerhaltungseinheiten")  

Weitere Informationen finden Sie unter [Designdetails: Übertragung in der Planung](design-details-transfers-in-planning.md)  

### <a name="order-priority"></a>Auftragspriorität  
In bestimmten Lagerhaltungsdaten zeigt das angeforderte oder verfügbare Datum die höchste Priorität an; mit dem Bedarf des heutigen Tages soll vor dem Bedarf der nächsten Tage verfahren werden. Aber abgesehen von dieser Art Priorität, werden die verschiedene Bedarfs- und Vorratstypen entsprechend der geschäftlichen Wichtigkeit sortiert, sodass Sie entscheiden können, welcher Bedarf vor einem anderen Bedarf erfüllt werden soll. Auf der Zugangsseite teilt die Auftragspriorität mit, welche Versorgungsquelle ausgeglichen werden soll, bevor andere Versorgungsquellen verwendet werden.  

Weitere Informationen finden Sie unter [Priorisieren von Aufträgen](design-details-balancing-demand-and-supply.md#prioritizing-orders).  

## <a name="demand-forecasts-and-blanket-orders"></a>Absatzplanungen und Rahmenaufträge Nachfrage  
Planungen und Absatzplanungen stellen den voraussichtlichen Bedarf dar. Der Rahmenauftrag, der die geplanten Einkäufe eines Debitoren über einen bestimmten Zeitraum hinweg umfasst, dient dazu, die Unsicherheiten des allgemeinen Plans zu reduzieren. Der Rahmenauftrag ist eine benutzerdefinierte Planung , zusätzlich zur nicht-spezifischen Planung, wie nachfolgend erläutert.  

![Planen mit Prognosen](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planen mit Prognosen")  

Weitere Informationen finden Sie im Abschnitt [Planungsbedarf wird durch Verkaufsaufträge reduziert](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## <a name="planning-assignment"></a>Planungszuweisung  
Alle Artikel sollten eingeplant werden, es gibt jedoch keinen Grund, einen Plan für einen Artikel zu berechnen, es sei denn, es gab eine Änderung im Bedarfs- oder Vorratsmuster seit der letzten Berechnung des Plans.  

Wenn der Benutzer einen neuen Verkaufsauftrag eingegeben oder einen vorhandenen geändert hat, gibt es Gründe zur Neuberechnung des Plans. Andere Ursachen beinhalten eine Änderung in der Planung oder im gewünschten Sicherheitsbestand. Das Ändern einer Stückliste durch Hinzufügen oder Entfernen einer Komponente führt wahrscheinlich zur Anzeige einer Änderung, jedoch nur für den Komponentenartikel.  

Das Planungssystem überwacht solche Ereignisse und ordnet die entsprechenden Artikel für die Planung zu.  

Für mehrere Lagerorte findet die Zuweisung auf Artikelebene pro Lagerortkombination statt. Wenn beispielsweise ein Auftrag an nur einem Lagerplatz erstellt wurde, ordnet die Anwendung den Artikel an diesem bestimmten Lagerort der Planung zu.  

Der Grund für die Auswahl von Artikeln für die Planung hat mit der Systemleistung zu tun. Wenn keine Änderung des Bedarf-Vorrat-Musters eines Artikels eingetreten ist, schlägt das Planungssystem keine Aktionen vor. Ohne die Planungs-Zuweisung müsste das System die Berechnungen für alle Artikel ausführen, um herauszufinden, was zu planen ist, wodurch die Systemressourcen belastet würden.  

Die vollständige Liste der Gründe für das Zuweisen eines Artikels für die Planung wird in [Designdetails: Planung von Zuweisungstabellen](design-details-planning-assignment-table.md) bereitgestellt.  

Die Planungsoptionen in [!INCLUDE[prod_short](includes/prod_short.md)] sind:  

-   Neuplanung berechnen – Berechnet alle ausgewählten Artikel, ob dies erforderlich ist oder nicht.  
-   Änderungsplanung berechnen – Berechnet nur die ausgewählten Artikel, bei denen einige Änderung im Bedarf-Vorrat-Muster aufgetreten sind, und die daher zur Planung zugewiesen wurden.  

Einige Benutzer sind der Meinung, dass die Änderungsplanung im Durchgang ausgeführt werden sollte, etwa, wenn Verkaufsaufträge eingegeben werden. Jedoch kann dies verwirrend sein, da die dynamische Auftragsnachverfolgung und das Aktionsmessaging ebenfalls ad hoc berechnet werden. Außerdem bietet [!INCLUDE[prod_short](includes/prod_short.md)] eine Echtzeit-Lieferzusagesteuerung, die beim Buchen von Verkaufsaufträgen Popupwarnungen anzeigt, wenn der Bedarf im bestehenden Beschaffungsplan nicht gedeckt werden kann.  

Zusätzlich zu diesen Fällen plant das Planungssystem nur Artikel, die der Benutzer mit entsprechenden Planungsparametern bereitgestellt hat. Andernfalls wird angenommen, dass der Benutzer die Artikel manuell oder halbautomatisch plant, indem er die Funktion "Auftragsplanung" verwendet.  

Weitere Informationen über die die automatischen Planungsverfahren finden Sie unter [Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  

## <a name="item-dimensions"></a>Artikeldimensionen  
Bedarf und Vorrat können Variantencodes und Lagerortcodes aufweisen, die berücksichtigt werden müssen, wenn das Planungssystem Bedarf und Vorrat ausgleicht.  

Die Anwendung behandelt Varianten- und Lagerortcodes als Artikeldimensionen in einer Verkaufsauftragszeile, Bestandsposten usw. Entsprechend berechnet es einen Plan für jede Kombination aus Variante und Lagerort, als ob die Kombination die Nummer eines eigenen Artikels wäre.  

Anstatt jede theoretische Kombination aus Variante und Lagerort zu berechnen, berechnet die Anwendung einzig die Kombinationen, die tatsächlich in der Datenbank vorhanden sind.  

Weitere Informationen darüber, wie das Planungssystem mit Lagerortcodes umgeht, finden Sie unter [Designdetails: Nachfrage an leeren Standorten](design-details-balancing-demand-and-supply.md).  

## <a name="item-attributes"></a>Artikelattribute  
Abgesehen von allgemeinen Artikeldimensionen, wie Artikelnummer, Variantencode, Lagerortcode und Art des Auftrags, können alle Bedarf und Vorräte zusätzliche Angaben in Form von Serien-/Chargennummern tragen. Das Planungssystem plant diese Attribute in einer bestimmten Weise, je nach der Ebene der Spezifikation.  

Eine Auftrag-zu-Auftrag-Verknüpfung zwischen Bedarf und Vorrat ist eine weitere Art von Attribut, die sich auf das Planungssystem auswirkt.  

### <a name="specific-attributes"></a>Spezifische Attribute.  
Bestimmte On Demand-Attribute sind spezifisch und müssen exakt an einen entsprechenden Vorrat angepasst sein. Die folgenden beiden spezifischen Attribute sind verfügbar:  

-   Erforderliche Serien-/Chargennummern, die bestimmte Anwendung benötigen (das Kontrollkästchen **SN-spezifische Nachverfolgung** oder **Chargenspezifische Nachverfolgung** wird auf der Seite **Artikelnachverfolgungscodekarte** ausgewählt für die Artikelnachverfolgung, die im Artikel verwendet wird.)  
-   Links zu manuell erstellten Beschaffungsaufträgen oder automatisch erstellt für einen speziellen Bedarf (Auftrag-zu-Auftragslinks).  

Für diese Attribute wendet das Planungssystem die folgenden Regeln an:  

-   Bedarf mit bestimmten Attributen kann nur von Vorrat mit entsprechenden Eigenschaften erfüllt werden.  
-   Vorrat mit bestimmten Attributen kann auch Bedarf abdecken, der diese Attribute nicht speziell erfordert.  

Entsprechend gilt: Wenn einen Bedarf für bestimmte Attribute nicht durch Lagerbestand oder geplanten Vorrat gedeckt werden kann, wird vom Planungssystem ein neuer Beschaffungsauftrag vorgeschlagen, um diesen speziellen Bedarf ohne Berücksichtigung von Planungsparametern zu decken.  

### <a name="non-specific-attributes"></a>Unpezifische Attribute  
Serien-/Chargen-nummerierte Artikel ohne bestimmtes Artikelverfolgungssetup können Serien-/Chargennummern tragen, die nicht auf exakt dieselbe Serien-/Chargennummer angewendet werden müssen, sondern auf beliebige Serien-/Chargennummern angewendet werden können. dies gibt dem Planungssystem mehr Freiheit, um beispielsweise einen serialiserten Bedarf einem Vorrat zuzuordnen, üblicherweise im Lagerbestand.  

Bedarf-Vorrat mit Serien-/Chargennummern, spezifisch oder nicht-spezifisch, gilt als hohe Priorität und ist deshalb von der fixierten Zone ausgenommen; dies bedeutet, dass sie Teil der Planung sind, auch wenn sie vor dem Startdatum fällig sind.  

Weitere Informationen finden Sie im Abschnitt [Serien-/Chargennummern werden nach Spezifikationsebene geladen](design-details-balancing-demand-and-supply.md#seriallot-numbers-are-loaded-by-specification-level).

Weitere Informationen darüber, wie das Planungssystem Attribute ausgleicht, finden Sie unter [Serien-/Chargennummern und Auftrag-zu-Auftrag-Links sind von der fixierten Zone ausgenommen](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Auftrag-zu-Auftrag-Verknüpfungen  
In einer Auftragsfertigungsumgebung wird ein Artikel bezogen, montiert oder gefertigt, um einen speziellen Bedarf zu decken. Normalerweise bezieht sich dies auf A-Artikel, und die Motivation für die Auswahl dieser Methode kann es sein, dass der Bedarf selten ist, die Vorbereitungszeit unbedeutend ist, oder die erforderlichen Attribute variieren können.  

Ein weiterer spezieller Fall, bei dem Auftrag-zu-Auftrag-Verknüpfungen verwendet werden, ist der, bei dem ein Montageauftrag in einem Auftragsmontageszenario mit einem Verkaufsauftrag verknüpft wird.  

Auftrag-zu-Auftrag-Links werden zwischen Bedarf und Vorrat in vier Arten angewendet:  

-   Wenn der geplante Artikel das Wiederbeschaffungsverfahren verwendet.  
-   Bei Verwendung der Produktionsart "Auftragsfertigung", um mehrstufige oder projekttypbezogene Fertigungsaufträge (Herstellung benötigter Komponenten im selben Fertigungsauftrag) zu erstellen.  
-   Wenn Sie Fertigungsaufträge für Verkaufsaufträge mit der Verkaufsauftrags-Planungsfunktion erstellen.  
-   Wenn ein Artikel mit einem Auftrag montiert wird. (Montagerichtlinie ist auf Auftragsmontage festgelegt.  

In diesen Instanzen wird vom Planungssystem nur vorgeschlagen, die benötigte Menge zu bestellen. Sobald er erstellt wurde, werden der Einkauf, die Produktion oder der Montageauftrag fortgesetzt, um den entsprechenden Bedarf zu decken. Wenn beispielsweise ein Verkaufsauftrag nach Zeit oder Menge geändert wird, wird das Planungssystem vorschlagen, dass der entsprechende Beschaffungsauftrag entsprechend geändert wird.  

Wenn Auftrag-zuAuftrag-Verknüpfungen vorhanden sind, bezieht das Planungssystem keinen verknüpften Lagerbestand in das Ausgleichsverfahren ein. Es liegt an dem Benutzer einzuschätzen, wenn der verknüpfte Lagerbestand verwendet wird, um anderen oder neuen Bedarf zu decken, und, in diesem Fall, den Beschaffungsauftrag zu löschen oder den verknüpften Vorrat manuell zu reservieren.  

Reservierungen und Auftragsnachverfolgungslinks schlagen fehl, wenn eine Situation unmöglich wird, etwa beim Verschieben eines Bedarfs zu einem Datum, das vor dem des Vorrats liegt. Der Auftrag-zu-Auftrag-Link passt sich allen Änderungen in dem jeweiligen Bedarf oder Vorrat an und wird daher nie unterbrochen.  

## <a name="reservations"></a>Reservierungen  
Das Planungssystem schließt keine reservierten Mengen in die Berechnung ein. Wenn beispielsweise ein Verkaufsauftrag vollständig oder teilweise gegen die Menge im bestand reserviert wurde, kann die reservierte Menge im Bestand nicht verwendet werden, um anderen Bedarf zu decken. Das Planungssystem schließt diesen Bedarf-Vorrat-Satz nicht in seine Berechnung ein.  

Das Planungssystem schließt dennoch reservierte Mengen im Profil des voraussichtlichen Lagerbestands ein, da alle Mengen berücksichtigt werden müssen, wenn bestimmt wird, ob der Minimalbestand überschritten wurde und wie viel nachbestellt werden muss, um den Maximalbestand zu erreichen, aber nicht zu überschreiten. Deshalb führen unnötige Reservierungen zu erhöhten Risiken, dass Lagerbestände zu niedrig sind, da die Planungslogik reservierte Mengen nicht erkennt.  

Die folgende Abbildung zeigt, wie Reservierungen den optimalen Plan behindern können.  

![Planung mit Reservierungen](media/NAV_APP_supply_planning_1_reservations.png "Planung mit Reservierungen")  

Weiter Informationen finden Sie unter [Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  

## <a name="warnings"></a>Warnungen  
Die erste Spalte im Planungsarbeitsblatt ist für die Warnungsfelder. In jeder für eine ungewöhnliche Situation erstellten Planungszeile wird in diesem Feld ein Warnsymbol angezeigt, auf die der Benutzer klicken kann, um weitere Informationen anzuzeigen.  

Der Vorrat in Planungszeilen mit Warnungen wird normalerweise nicht gemäß den Planungsparametern geändert. Stattdessen wird vom Planungssystem nur eine Beschaffung vorgeschlagen, um die genaue Bedarfsmenge zu decken. Sie können jedoch das System so einrichten, dass bestimmte Planungsparameter für Planungszeilen mit bestimmten Warnungen berücksichtigt werden können. Weitere Informationen finden Sie in der Beschreibung dieser Optionen für **Berechnungsplan - Plan Lagerreg.** Stapelauftrag und **Planung berechnen - Bestellarbeitsblatt** Stapelverarbeitung fest.  

Die Warnungsinformationen werden auf der Seite **Planungselemente ohne Bedarfsverursacher** angezeigt, das auch verwendet wird, um Bedarfsverursacherverknüpfungen mit nicht auftragsbezogenen Netzwerkeinheiten anzuzeigen. Folgende Arten von Warnungen sind verfügbar:  

-   Notfall  
-   Ausnahme  
-   Achtung  

![Warnungen im Planungsarbeitsblatt](media/NAV_APP_supply_planning_1_warnings.png "Warnungen im Planungsarbeitsblatt")  

### <a name="emergency"></a>Notfall  
Die Warnung für einen Notfall wird in zwei Situationen angezeigt:  

-   Der Lagerbestand ist am geplanten Startdatum negativ.  
-   Vorgehensweise bei rückdatierten Beschaffungs- oder Bedarfsereignissen.  

Wenn der Lagerbestand eines Artikels am geplanten Startdatum negativ ist, wird vom Planungssystem ein Notfallbeschaffungsauftrag für den negativen Bestand vorgeschlagen, der am geplanten Startdatum eingeht. Im Warnungstext werden das Startdatum und die Menge der Notfallbestellung angegeben. Weitere Informationen finden Sie unter [Umgang mit voraussichtlichem negativem Lagerbestand](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Belegzeilen mit Fälligkeitsdaten vor dem geplanten Startdatum werden in einem Notfallbeschaffungsauftrag für den Artikel zusammengefasst, der am geplanten Startdatum eingehen soll.  

### <a name="exception"></a>Ausnahme  
Die Ausnahmewarnung wird angezeigt, wenn der voraussichtlich verfügbare Lagerbestand den Sicherheitsbestand unterschreitet. Vom Planungssystem wird ein Beschaffungsauftrag vorgeschlagen, um den Bedarf am Fälligkeitsdatum zu decken. In der Warnung werden der Sicherheitsbestand des Artikels und das Datum angegeben, an dem er unterschritten wurde.  

Das Unterschreiten des Sicherheitsbestands gilt als Ausnahme, da dieser Zustand nicht eintreten sollte, wenn der Minimalbestand korrekt festgelegt wurde. Weitere Informationen finden Sie unter [Die Rolle des Wiederbestellpunkts](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Im Allgemeinen gewährleisten außergewöhnliche Bestellarbeitsblätter, dass der voraussichtlich verfügbare Lagerbestand nicht geringer als die Sicherheitsbestandsebene ist. Das bedeutet, dass die vorgeschlagene Menge gerade ausreicht, den Sicherheitsbestand zu umfassen, ohne Planungsparameter zu berücksichtigen. Jedoch in einigen Szenarien werden Auftragsmodifikationen berücksichtigt.  

> [!NOTE]  
>  Das Planungssystem hat möglicherweise den Sicherheitsbestand absichtlich verbraucht und füllt ihn dann sofort auf. Weitere Informationen finden Sie unter [Sicherheitsbestand kann verbraucht werden](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### <a name="attention"></a>Achtung  
Die Achtungswarnung wird in drei Situationen angezeigt:  

-   Das geplante Startdatum liegt vor dem Arbeitsdatum.  
-   Die Planungszeile schlägt vor, eine freigegebene Bestellung oder einen freigegebenen Fertigungsauftrag zu ändern.  
-   Der voraussichtliche Lagerbestand übersteigt das Überlauflevel am Fälligkeitsdatum. Weitere Informationen finden Sie unter [Verbleibenden unter dem Überlauflevel](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  In Planzeilen mit Warnungen ist das Kontrollkästchen **Ereignismeldung akzeptieren** nicht aktiviert, da diese Zeilen vom Planer genauer untersucht werden sollen, bevor der Plan umgesetzt wird.  

## <a name="error-logs"></a>Fehlerprotokolle  
Auf der Anforderungsseite „Plan berechnen“ kann der Benutzer das Feld **Abbrechen und ersten Fehler anzeigen** auswählen, um die Planung anzuhalten, wenn der erste Fehler aufgetreten ist. Gleichzeitig wird eine Meldung angezeigt, die Informationen zu dem Fehler enthält. Gibt es einen Fehler, werden im Planungsarbeitsblatt nur die Planungszeilen angezeigt, die vor dem Fehler erfolgreich erstellt wurden.  

Wenn das Feld nicht aktiviert ist, wird die Stapelverarbeitung „Planung berechnen“ fortgesetzt, bis sie abgeschlossen ist. Fehler unterbrechen die Stapelverarbeitung nicht. Sind Fehler vorhanden, zeigt die Anwendung nach Beendigung der Stapelverarbeitung eine Meldung an, die mitteilt, wie viele Artikel betroffen sind. Danach wird die Seite **Planungsfehlerprotokoll** geöffnet, in dem weitere Informationen zu den Fehlern sowie den Verknüpfungen für die betroffenen Dokumente oder Setupkarten bereitgestellt werden.  

![Fehlermeldungen im Planungsarbeitsblatt](media/NAV_APP_supply_planning_1_error_log.png "Fehlermeldungen im Planungsarbeitsblatt")  

## <a name="planning-flexibility"></a>Planungsflexibilität  
Es ist jedoch nicht immer nützlich, einen vorhandenen Beschaffungsauftrag zu planen, z.B. wenn die Produktion gestartet hat oder zusätzliche Personen an einem bestimmten Tag zur Ausführung der Arbeit abgestellt werden. Um anzugeben ob ein bestehender Auftrag vom Planungssystem geändert werden kann, verfügen alle Beschaffungsauftragszeilen über ein Feld mit zwei Optionen: Unbegrenzt oder Keine. Wenn das Feld auf Keine festgelegt wurde, versucht das Planungssystem nicht, die Beschaffungsauftragszeile zu ändern.  

Das Feld kann vom Benutzer manuell festgelegt werden, in einigen Fällen wird es jedoch automatisch vom System festgelegt. Der Tatsache, dass die Planungsflexibilität vom Benutzer manuell festgelegt werden kann, ist wichtig, da dadurch vereinfacht wird, die Verwendung des Funktion für verschiedene Workflows und Geschäftsszenarien zu ermöglichen.  

Weitere Informationen darüber, wie dieses Feld verwendet wird, finden Sie unter [Designdetails: Umlagerungen von Planung](design-details-transfers-in-planning.md).  

## <a name="order-planning"></a>Auftragsplanung  
Das grundlegende Tool für die Beschaffungsplanung, das durch die Seite **Auftragsplanung** angegeben wird, ist für die manuelle Entscheidungsfindung gedacht. Berücksichtigt keine Planungsparameter und wird daher nicht weiter in diesem Dokument erläutert. Weitere Informationen finden Sie unter [Plan für neuen Nachfrageauftrag nach Auftrag](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
>  Es wird nicht empfohlen, Auftragsplanung zu verwenden, wenn das Unternehmen bereits Planungs- oder Bestellarbeitsblätter verwendet. Die über die Seite erstellten Beschaffungsaufträge **Auftragsplanung** können während der automatisierten Planungsläufe geändert oder gelöscht werden. Dies liegt daran, dass der automatisierte Planungslauf Planungsparameter verwendet und diese möglicherweise vom Benutzer nicht berücksichtigt werden, der den manuellen Plan auf der Seite "Auftragsplanung" erzeugt hat.  

##  <a name="finite-loading"></a>Begrenzte Auslastung  
[!INCLUDE[prod_short](includes/prod_short.md)] ist ein Standard-ERP-System, kein Dispatching- oder Fertigungssteuerungssystem. Planung einer durchführbaren Nutzung von Ressourcen durch Bereitstellung eines Rohschnittzeitplans, jedoch keine automatische Erstellung und Verwaltung von detaillierten Plänen, die auf Prioritäten oder Optimierungsregeln basieren.  

Die vorgesehene Verwendungsweise der Funktion „Begrenzte Kapazität“ ist 1): das Verhindern der Überladung bestimmter Ressourcen und 2): die Sicherstellung, dass keine Kapazität unzugewiesen bleibt, wenn dies die Durchlaufzeit eines Fertigungsauftrags erhöhen könnte. Die Funktion umfasst keine Funktionen oder Optionen zum Priorisieren oder Optimieren von Abläufen, wie etwa in einem Dispatchingsystem. Jedoch kann sie grobe Kapazitätsinformationen zur Verfügung stellen, die, nützlich sind, um Engpässe zu identifizieren und die Überlastung von Ressourcen zu verhindern.  

Beim Planen mit eingeschränkter Kapazität stellt sicher das System sicher, dass keine Ressourcen oberhalb der definierten Kapazität (Grenzbelastung) geladen werden. Dies geschieht, indem jeder Arbeitsgang dem nächsten verfügbaren Zeitfenster zugewiesen wird. Wenn das Zeitfenster nicht ausreicht, um den gesamten Arbeitsgang abzuschließen, wird der Arbeitsgang in zwei Teile aufgeteilt, die in die nächsten verfügbaren Zeitfenster gesetzt werden.  

> [!NOTE]  
>  Im Falle der Teilung des Arbeitsgangs wird die Rüstzeit nur einmal zugeordnet, da davon ausgegangen wird, dass einige manuelle Ausgleiche vorgenommen werden, um den Plan zu optimieren.  

Die Toleranzzeit kann zu Ressourcen hinzugefügt werden, um die Aufteilung von Arbeitsgängen zu minimieren. Dies ermöglicht dem System, Auslastung am letzten möglichen Tag zu planen, indem es den kritischen Auslastungsprozentsatz etwas überschreitet, wenn dies die Anzahl der Arbeitsgänge verringern kann, die aufgeteilt werden.  

Damit ist die Vorstellung der zentralen Konzept in Bezug auf die Beschaffungsplanung in [!INCLUDE[prod_short](includes/prod_short.md)] abgeschlossen. Die folgenden Abschnitte behandeln diese Konzepte eingehender und beschreiben sie im Kontext der zentralen Planungsvorgänge, des Ausgleichs von bedarf und Vorrat sowie der Verwendung von Wiederbeschaffungsrichtlinien.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Umlagerungen in Planung](design-details-transfers-in-planning.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Planungs-Zuordnungstabelle](design-details-planning-assignment-table.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]