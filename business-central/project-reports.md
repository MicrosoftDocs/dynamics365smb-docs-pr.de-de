---
title: Projektberichte und Analysen
description: Sehen Sie, welche Projektberichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie Ihr Unternehmen im Auge behalten können.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: ff5294df5cdbeaf0054249f017906bfd60ee4bf7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216365"
---
# <a name="project-reports-and-analytics-in-business-central"></a>Projektberichte und Analysen in Business Central

Die Projektberichterstattung in [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht es Projekt- und Geschäftsfachleuten, Einblicke und Statistiken über aktuelle und vergangene Projektaktivitäten zu erhalten.  

## <a name="reports"></a>Berichte

In der folgenden Tabelle werden einige der wichtigsten Berichte in der Projektberichterstattung beschrieben.

|Bericht |Objekt-ID|Beschreibung  |
|---------|---------|---------|
|**Projektanalyse**|1008|Analysiert das jeweilige Projekt anhand der von Ihnen angegebenen Einstellungen. So können Sie beispielsweise einen Bericht erstellen, in dem die bugetierten Preise, Preise für den Verbrauch und fakturierbare Preise aufgeführt sind und die drei Preisgruppen verglichen werden.<br>Verwenden Sie eine Kombination der verfügbaren Felder für **Betrag**, um eine eigene Analyse zu erstellen. Wählen Sie für jedes Feld einen der folgenden Verkaufspreise, Einstandspreise oder DB-Werte aus: Plan, Verbrauch, Vertrag und Fakturiert. <br>Geben Sie an, ob die Währung als Mandantenwährung oder Fremdwährung angegeben werden soll. |
|**Projektplanzeilen**|1006|Dieser Bericht zeigt die verschiedenen Projektplan- und Projektaufgabenzeilen – einschließlich Zeilentyp, Mengen, Mengeneinheit, Gesamtkosten usw.|
|**Budgetvergleich Projekt**|1009|Vergleicht geplante und Verbrauchsbeträge für ausgewählte Projekte. In allen Zeilen des ausgewählten Projekts sind Menge, Einstandsbetrag und Zeilenbetrag angegeben. <br>Der Bericht eignet sich vor allem für abgeschlossene Projekte. Sie können ihn jedoch zu jedem Zeitpunkt innerhalb eines Projekts verwenden.<br>In den USA, Kanada und Mexiko ist dieser Bericht nicht verfügbar. Verwenden Sie stattdessen die Berichte **Budgetvergleich Projekt (Kosten)** (10210) oder **Budgetvergleich Projekt (Preis)** (10211).|
|**Akontovorschlag Projekt**|1011|Zeigt eine Übersicht aller Projekte gruppiert nach Debitor, dem Betrag, der dem Debitor bereits in Rechnung gestellt wurde, und dem Restbetrag, der noch zu berechnen ist, d. h. dem Akontovorschlag, an. <br>In den USA, Kanada und Mexiko ist dieser Bericht nicht verfügbar. Verwenden Sie stattdessen den Bericht **Akontovorschlag Projektkosten** (10219) Bericht.|
|**Projekte pro Debitor**|1012|Zeigt eine Übersicht aller Projekte nach Debitor gruppiert an. Dadurch können Sie für jede **Rechnung an Debitor** den geplanten Verkaufspreis, den Prozentsatz der Fertigung, den fakturierten Verkaufspreis und den Prozentsatz der fakturierten Beträge vergleichen.|
|**Artikel pro Projekt** oder **Projekte pro Artikel**|1013 oder 1014|Eine Übersicht über die verwendeten Artikel in einem Projekt. Je nachdem, mit welchem Bericht Sie sich einen Überblick über die geplanten Artikel für ein Projekt verschaffen möchten, können Sie einen zusätzlichen Filter setzen. Der Bericht zeigt die relevanten Artikel und einen kumulierten Wert über die Kosten.|
|**Projekt – Kontoblatt**|1007|Dieser Bericht gibt Ihnen einen Überblick über die gebuchten Projektaufgaben wie Ressourcen und Artikel. Er enthält detaillierte Informationen zu den Gesamtkosten und Gesamtpreisen sowie Informationen zu Zeilenrabatten usw. Der Bericht zeigt Daten aus den Projektbuchungsposten.|
|**WIP nach Sachposten Projekt**|1010|Zeigt den WIP-Wert für die ausgewählten Projekte im Vergleich zu dem Betrag an, der in die Finanzbuchhaltung gebucht wurde.|




## <a name="tasks"></a>Aufgaben

In den folgenden Artikeln werden einige der wichtigsten Aufgaben zur Analyse des Status Ihres Unternehmens beschrieben:

* [Überwachen des Status und der Leistung](projects-how-monitor-progress-performance.md)  


## <a name="see-also"></a>Siehe auch

[Projektmanagement einrichten](projects-setup-projects.md)  
[Projektmanagement](projects-manage-projects.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
