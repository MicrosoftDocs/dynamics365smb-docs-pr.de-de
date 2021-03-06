---
title: Produktionsberichte und Analysen
description: Sehen Sie, welche Produktionsberichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie Ihr Unternehmen im Auge behalten können.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 0cacf41f0a055267af5b0ce5a8b68b34d86a1cb5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216361"
---
# <a name="production-reports-and-analytics-in-business-central"></a>Produktionsberichte und Analysen in Business Central

Die Produktionsberichterstattung in [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht es Vertriebs- und Geschäftsfachleuten, Einblicke und Statistiken über aktuelle und vergangene Produktionsaktivitäten zu erhalten.  

## <a name="reports"></a>Berichte

In der folgenden Tabelle werden einige der wichtigsten Berichte in der Produktionsberichterstattung beschrieben.

|Bericht |Objekt-ID|Beschreibung  |
|---------|---------|---------|
|**Strukturstückliste**|99000753|Zeigt eine eingerückte Stückliste für den oder die Artikel, die Sie in den Filtern angeben. Die Stückliste ist über alle Ebenen aufgelöst.|
|**Artikel - Fertigung möglich (Zeit)**|5871|Zeigt, wie fünf verschiedene wichtige Verfügbarkeitsabbildungen sich bei einem Stücklistenartikel im Zeitverlauf ändern. Diese Zahlen ändern sich entsprechend von erwarteten Angebots- und Nachfrageereignissen sowie Lieferungen basierend auf verfügbaren Komponenten, die montiert werden oder gefertigt werden können.<br>Sie können den Bericht verwenden, um zu prüfen, ob Sie einen Verkaufsauftrag für einen Artikel an einem bestimmten Datum erfüllen können, indem Sie seine aktuelle Verfügbarkeit in Verbindung mit den möglichen Mengen anzeigen, die von den Komponenten geliefert werden können, falls ein Montageauftrag gestartet wurde. Der Bericht zeigt, wann und wie viele Einheiten eines Montage- und Fertigungsartikels basierend auf der Komponentenverfügbarkeit und der aktuellen Verfügbarkeit des Artikels erstellt werden können. Dies wird als die Gesamtmenge angezeigt.<br>Die Informationen werden in einem Diagramm angezeigt, in dem jede Verfügbarkeitszahl eine Zeile ist, die entlang der Zeitachse verläuft und sich bei Mengenänderungen nach oben oder unten bewegt. Die Mengenangaben stammen aus dem Modul, das auch die Informationen für das Fenster **Artikelverfügbarkeit nach Stücklistenebene** bereitstellt. |
|**Stückliste – Kostenanteilsverteilung**|5872|Stellt grafisch dar, wie sich die Kosten eines montierten oder gefertigten Artikels durch die zugehörige Stückliste verteilen.<br>Diese Informationen können beispielsweise bei folgenden Entscheidungen hilfreich sein: Ändern von Zulieferbetrieben, Einsatz interner Kapazitäten durch Fremdvergabe bzw. umgekehrt, oder wann die Stückliste eines Artikels überprüft und geändert werden soll.<br>Das erste Diagramm im Bericht zeigt die Aufschlüsselung des Gesamteinstandsbetrags der Komponenten des übergeordneten Artikels und Arbeitsressourcen in fünf verschiedene Kostenanteile an, die grafisch durch verschiedene Farben dargestellt werden.<br>Das Kreisdiagramm mit der Bezeichnung *Nach Material/Arbeit* zeigt die proportionale Verteilung der Material- und Arbeitskosten des übergeordneten Artikels sowie dessen eigene Produktionsgemeinkosten. Der Materialkostenanteil enthält die Materialkosten des Artikels. Der Arbeitskostenanteil enthält Kapazitätskosten, Kapazitätsgemeinkosten und Fremdarbeitskosten. Die Kostenanteile werden je nach Auswahl im Feld **Nur anzeigen** angezeigt.<br>Das Kreisdiagramm mit der Bezeichnung *Nach Direkt/Indirekt* zeigt die proportionale Verteilung der direkten und indirekten Kosten des übergeordneten Artikels. Der direkte Kostenanteil enthält die Material-, Kapazitäts- und Fremdarbeitskosten des Artikels. Der indirekte Kostenanteil enthält Kapazitätsgemeinkosten und Produktionsgemeinkosten.<br>Die Tabelle am Ende des Berichts ist enthalten, wenn Sie das Kontrollkästchen **Details einbeziehen** aktivieren. Sie zeigt ausgewählte Werte aus dem Fenster „Stücklisten-Kostenanteile“ an, und zwar einstufig oder mehrstufig, abhängig von Ihrer Auswahl im Feld **Stücklisten-Kostenanteile**.|
|**Detailkalkulation**|99000756|Zeigt eine Übersicht der Kosten je Artikel mit Berücksichtigung des Ausschusses.|
|**Teileverwendung (Struktur)**|99000757|Zeigt, wo und in welchen Mengen Artikel in Fertigungsstücklisten verwendet werden.<br>Dieser Bericht zeigt die einstufige Verwendung des Artikels. Wenn zum Beispiel „A“ verwendet wird, um Artikel „B“ zu fertigen und „B“ verwendet wird, um Artikel „C“ zu produzieren, zeigt der Bericht Artikel „B“, wenn Sie den Bericht für Artikel „A“ ausführen. Wenn Sie den Bericht für Artikel „B“ ausführen, wird Artikel „C“ in der Verwendung angezeigt.<br>Sie können auch die Seite **Verwendungszeile** direkt über den Artikel aufrufen.|
|**Artikelstücklisten-Vergleichsliste**|99000758|Mit diesem Bericht können Sie ähnliche Endprodukte hinsichtlich der Kosten vergleichen. Sie sehen eine Liste mit allen Komponenten und deren Kosten sowie den benötigten Mengen. Als Berechnungsdatum wird normalerweise das Arbeitsdatum festgelegt. |
|**Produktionsauftragsstatistik**|99000791|Zeigt die verschiedenen Kosten an, die sich für den ausgewählten Fertigungsauftrag angesammelt haben.<br>Der Inhalt des Berichts ist der Seite **FA-Statistik** sehr ähnlich.<br>Für Fertigungsaufträge, die die Produktionsart *Auftragsfertigung* verwenden, zeigt das Fenster nur Material- und Kapazitätskosten von Artikeln auf der höchsten Stücklistenebene an.|
|**Auftragsvorratsliste**|99000780|Zeigt die Fertigungsaufträge, die darauf warten, von den Arbeitsplätzen und Arbeitsplatzgruppen bearbeitet zu werden. Die Kapazität der Arbeitsplatzgruppe oder des Arbeitsplatzes wird angezeigt. Der Bericht enthält Informationen, wie z. B. Start- und Endzeit und Datum sowie die Einsatzmenge je Fertigungsauftrag.|
|**Arbeitsplatzgruppenauslastung** oder **Arbeitsplatzauslastung**|99000783 oder 99000784|Beide Berichte zeigen eine Übersicht der Auslastung einer Arbeit oder eines Arbeitsplatzes. Die Auslastung einer Arbeit/eines Arbeitsplatzes ist die Summe der benötigten Zeiten für alle geplanten und aktuellen Aufträge, die auf der Arbeitsplatzgruppe in der Zeitperiode laufen sollen.|
|**FA-Fehlteilliste**|99000788|Dieser Bericht kann verwendet werden, um alle Komponenten anzuzeigen, die aufgrund von fehlendem Bestand nicht verfügbar sind. Diese Übersicht kann also herangezogen werden, um rechtzeitig zu sehen, ob der Zeitplan für einen geplanten oder freigegebenen Fertigungsauftrag oder die geplante Zeit eingehalten werden kann.|


## <a name="tasks"></a>Aufgaben

In den folgenden Artikeln werden einige der wichtigsten Aufgaben zur Analyse des Status Ihres Unternehmens beschrieben:

* [Auslastung der Arbeit und Arbeitsplätze anzeigen](production-how-to-view-the-load-on-work-centers.md)  
* [Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)

## <a name="see-also"></a>Siehe auch

[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
