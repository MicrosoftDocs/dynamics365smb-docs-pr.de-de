---
title: Tabelleninformationen anzeigen
description: 'Erfahren Sie, wie Sie Informationen über Datenbanktabellen in Business Central anzeigen können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
---

# <a name="viewing-table-information" />Tabelleninformationen anzeigen

Auf der Seite **8700 Tabelleninformationen** erhalten Sie Informationen über die Anzahl der Datensätze in allen System- und Geschäftstabellen in [!INCLUDE[prod_short](includes/prod_short.md)], und wie viele Daten jede Tabelle enthält.

Diese Informationen sind hilfreich bei der Behebung von Leistungsproblemen, da Sie die Verteilung der Datengröße auf Tabellen anzeigen können.

## <a name="viewing-table-information" />Tabelleninformationen anzeigen

Um diese Seite zu öffnen, wählen Sie das ![Suche nach Seite oder Bericht.](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht") Symbol. Geben Sie **Tabelleninformationen** ein und wählen Sie dann den entsprechenden Link.

In der folgenden Tabelle werden die für jede Tabelle bereitgestellten Informationen beschrieben:

|Spalte|Beschreibung|
|------|-----------|
|Unternehmensname|Name des Unternehmens (sofern zutreffend), zu dem die Tabelle gehört.|
|Tabellenname|Der Name der Tabelle.|
|Tabellennr.|Die ID der Tabelle.|
|Anz. der Datensätze|Die Gesamtzahl der in der Tabelle gespeicherten Datensätze.|
|Datensatzgröße|Die durchschnittliche Datensatzgröße in KB/Datensatz. Der Wert wird nach folgender Formel berechnet: 1024 (Größe)/(Anzahl der Datensätze). |
|Größe (KB)|Wie viel Platz ingesamt die Tabelle in der Datenbank belegt. Dieser Wert stammt aus der Summe der Werte in den Feldern Datengröße und Indexgröße.|
|Datengröße (KB)|Wie viel Platz die Daten in der Tabelle in der Datenbank belegen.|
|Indexgröße (KB)|Wie viel Platz die Tabellenindizes (Schlüssel) in der Datenbank belegen.|
|Komprimierung|Die Art der Komprimierung, **Zeile**, **Seite** oder **Keine**, die auf die Tabelle in der Datenbank angewendet wird. Weitere Informationen finden Sie unter [Datenkomprimierung](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Wenn Sie Daten in einer Tabelle löschen, startet [!INCLUDE[prod_short](includes/prod_short.md)] mehrere Prozesse im Hintergrund, um sicherzustellen, dass alles in Ihrer Datenbank bereinigt wird. Die Werte auf der Seite Tabelleninformationen werden erst aktualisiert, wenn diese Prozesse abgeschlossen sind, was eine Weile dauern kann. Die Wartezeit kann je nach Größe Ihrer Datenbank variieren.

## <a name="see-also" />Siehe auch

[Überprüfen von Seiten](across-inspect-page.md)  
[Artikel zur Leistung für Entwickler](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
