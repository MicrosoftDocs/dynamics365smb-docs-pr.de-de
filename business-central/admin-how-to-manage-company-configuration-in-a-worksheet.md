---
title: So verwalten Sie eine Mandantenkonfiguration in einem Arbeitsblatt | Microsoft Docs
description: Das Konfigurationsarbeitsblatt ist die zentrale Stelle, an der Sie Ihre Konfigurationsarbeit planen, nachverfolgen und ausführen können. Sie können ein Arbeitsblatt für jeden Mandanten erstellen, mit dem Sie arbeiten, oder ein Standardkonfigurationsarbeitsblatt erstellen, das für die Konfiguration von mehreren identischen Mandanten verwendet werden kann.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3b4be28dda5e01656f8e91fe813c01969115100
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378248"
---
# <a name="manage-company-configuration-in-a-worksheet"></a>So verwalten Sie eine Mandantenkonfiguration in einem Arbeitsblatt
Das Konfigurationsarbeitsblatt ist die zentrale Stelle, an der Sie Ihre Konfigurationsarbeit planen, nachverfolgen und ausführen können. Sie können ein Arbeitsblatt für jeden Mandanten erstellen, mit dem Sie arbeiten, oder ein Standardkonfigurationsarbeitsblatt erstellen, das für die Konfiguration von mehreren identischen Mandanten verwendet werden kann.  

Der erste Schritt zum Vorbereiten eines Konfigurationspakets ist es, einen Mandanten auszuwählen, den Sie bereits eingerichtet und in Hinblick auf die meisten Ihrer Lösungsanforderungen geändert haben. Dieser Mandant dient als Grundlage für Ihre Konfigurationsarbeit mit neuen Mandanten. Im Arbeitsblatt können Sie die Tabellen festlegen, die die Konfiguration steuern und verarbeiten soll. Da die meisten Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] Beziehungen und Abhängigkeiten zu anderen Tabellen haben, sollten Sie diese zugehörigen Tabelle auch nach Bedarf einschließen. Zusammen dienen diese Tabellen dann als die Struktur, um die herum Sie einen neuen Mandanten erstellen. Folgende Schritte unterstützen Sie dabei, die Konfiguration zu verpacken und bereitzustelllen.  

Um Ihnen bei der Nachverfolgung und Überprüfung Ihrer Arbeit zu helfen, verwenden Sie die **Pakettabelle konfigurieren**-Infobox, um Informationen über Datensätze anzuzeigen. Verwenden Sie die Infobox **Zugehörige Tabellen konfigurieren**, um Tabellen-Verhältnisse zu überwachen.  

Die folgenden Verfahren zeigen, wie Tabelleninformationen für die Konfiguration angepasst und addiert werden.  

## <a name="to-open-the-configuration-worksheet"></a>So öffnen Sie das Konfigurationsarbeitsblatt  
1.  Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] den Mandanten, der die Grundlage für die Konfiguration ist, und öffnen Sie dann sein RapidStart Services-Implementierungs-Rollencenter.  
2.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationsarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  

## <a name="to-add-a-table-to-the-worksheet"></a>So fügen Sie dem Arbeitsblatt eine Tabelle hinzu  
1.  Auf der Seite **Config. Arbeitsblatt** wählen Sie die **Liste bearbeiten** Aktion aus.  
2.  Wählen Sie in der ersten Anfragezeile in dem Feld **Art** die Art **Tabelle**.  
4.  Wählen Sie im Feld **ID-Tabelle** die Tabelle aus, die Sie der Konfiguration hinzufügen möchten.  
5.  Geben Sie im Feld **Seiten-ID** die Seiten-ID ein, die mit der Tabelle verknüpft ist. Für Standard-Tabellen wird dieser Wert automatisch ausgefüllt. Für benutzerdefinierte Tabellen müssen Sie die ID zur Verfügung stellen
6.  Geben Sie im Feld **Referenz** die URL einer Seite ein, die Verfahreninformationen oder Anweisungen zu Einrichtung der Tabelle bereitstellt.  
7.  Um beispielsweise verknüpfte Tabellen hinzuzufügen, wählen Sie die **Zugehörige Tabellen abrufen** Aktion.  

    > [!NOTE]  
    > Zugehörige Tabellen werden nicht mit der Aktion **Zugehörige Tabellen abrufen** hinzugefügt, wenn Folgendes zutrifft:
    > - Die Beziehung ist bedingt.  
    > Beispiel: Wenn Sie zugehörige Tabellen für Tabelle **Debitor** erhalten, dann wird die Tabelle **Lagerort** nicht hinzugefügt, da sie nur bedingt mit der Tabelle **Debitor** verknüpft ist, und zwar, wenn das Feld **Lagerortcode** in Tabelle **Debitor** ausgefüllt ist.  
    > - Die verknüpfte Tabelle wird gefiltert.  
    > Beispiel: Ein Feld in der zugehörigen Tabelle hat eine WHERE-Klausel. Der Grund dafür ist, dass die entsprechenden Beziehungsinformationen in der Systemtabelle **Feld** gespeichert werden, die nicht vollständig für die Anwendung zugänglich ist.  
    > Sie müssen solche Areten von Tabellen manuell hinzufügen, indem Sie Schritt 4 in diesem Verfahren befolgen.  

8.  Um die resultierende Liste von Tabellen zu ändern, wählen Sie eine Tabelle aus, die Sie entfernen möchten, und wählen Sie auf der Registerkarte Start die Option **Löschen** aus.  
9. Wiederholen Sie den Schritt für jede Tabelle, die Sie der Konfiguration hinzufügen möchten.  
10. Um doppelte Tabelleninformationen zu entfernen, die aus der **Zugehörige Tabellen abrufen**-Aktion resultieren können, wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktion **Doppelte Zeilen löschen** aus. Hierdurch werden doppelte Tabellen, die denselben Paketcode haben, entfernt.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>So fügen Sie dem Konfigurationsarbeitsblatt mehrere Tabellen hinzu.  
1. Wählen Sie die Aktion **Tabellen abrufen** aus. Das Batchauftragsseite **Tabellenkonfiguration abrufen** wird geöffnet.  
2. Im Inforegister **Optionen** definieren Sie die Arten von Tabellen, die Sie hinzufügen möchten der Konfiguration, wie in der folgenden Tabelle beschrieben an.

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nur mit Daten einschließen**|Aktivieren Sie dieses Kontrollkästchen aus, um nur die Tabellen einzubeziehen, die Daten enthalten. Sie möchten beispielsweise eine Tabelle einschließen, die bereits die typischen Zahlungsbedingungen definiert, die Ihre Lösung unterstützt.|  
    |**Zugehörige Tabellen einschließen**|Aktivieren Sie das Kontrollkästchen, um alle verwandten Tabellen zu berücksichtigen. Wie eine Teilmenge zugehöriger Tabellen hingezufügt wird, finden Sie Schritt 3 in diesem Verfahren.|  
    |**Dimensionstabellen einschließen**|Aktivieren Sie das Kontrollkästchen, um Dimensionstabellen zu berücksichtigen.|  
    |**Nur lizenzierte Tabellen einschließen**|Aktivieren Sie das Kontrollkästchen, um nur die Tabellen einzuschließen, für die die Lizenz, unter der Sie das Arbeitsblatt erstellen, Ihnen den Zugriff erlaubt.|

3. Geben Sie im Inforegister **Objekt** nach Bedarf Filter ein, um die Arten von Tabellen festzulegen, die Sie ein- oder ausschließen möchten.  
4. Wählen Sie die Schaltfläche **OK** aus. [!INCLUDE[prod_short](includes/prod_short.md)] Tabellen werden dem Fenster hinzugefügt. Jeder Eintrag in der Liste hat die Zeilenart **Tabelle**.  
5. Um doppelte Tabelleninformationen zu entfernen, die aus der **Zugehörige Tabellen abrufen**-Aktion resultieren können, wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktion **Doppelte Zeilen löschen** aus. Hierdurch werden doppelte Tabellen, die denselben Paketcode haben, entfernt.  
6. Sie können diesem Arbeitsblatt Tabellen hinzufügen, die zu einer Tabelle gehören, die Sie ausgewählt haben. Überprüfen Sie die Informationen in der Infobox **Zugehörige Tabellen**, um festzustellen, ob es fehlende Tabellen gibt. Um zugehörige Tabellen für eine bestimmte Tabelle hinzuzufügen, wählen Sie die Tabelle in der Übersicht aus, und wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktionen die Option **Zugehörige Tabellen abrufen** aus.  

    > [!NOTE]  
    > Zugehörige Tabellen werden nicht mit der Aktion **Zugehörige Tabellen abrufen** hinzugefügt, wenn Folgendes zutrifft:
    > - Die Beziehung ist bedingt.  
    > Beispiel: Wenn Sie zugehörige Tabellen für Tabelle **Debitor** erhalten, dann wird die Tabelle **Lagerort** nicht hinzugefügt, da sie nur bedingt mit der Tabelle **Debitor** verknüpft ist, und zwar, wenn das Feld **Lagerortcode** in Tabelle **Debitor** ausgefüllt ist.  
    > - Die verknüpfte Tabelle wird gefiltert.  
    > Beispiel: Ein Feld in der zugehörigen Tabelle hat eine WHERE-Klausel. Der Grund dafür ist, dass die entsprechenden Beziehungsinformationen in der virtuellen Tabelle **Feld** gespeichert werden und nicht auf Seiten wie dem Konfigurationsarbeitsblatt für Leistungsgründe verfügbar ist.  
    > Sie müssen zugehörige Tabellen mit solchen komplexen Relationen manuell hinzufügen, indem Sie Schritt 4 im Abschnitt [So fügen Sie dem Arbeitsblatt eine Tabelle hinzu](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet) befolgen.

7. Um die resultierende Liste von Tabellen zu ändern, wählen Sie eine Tabelle aus, die Sie entfernen möchten, und wählen Sie auf der Registerkarte Start die Option **Löschen** aus.  

Verwenden Sie folgende Vorgehensweise, um die zu berücksichtigenden Felder anzugeben. Nachdem Sie diese Angaben gemacht haben, können Sie die Tabelle nach Excel exportieren und die Tabellenstruktur als Vorlage für das Sammeln von Debitorendaten verwenden. Weitere Informationen finden Sie unter [Gewusst wie: Debitorendaten zusammenführen](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>So legen Sie einen Satz von Feldern und Datensätzen für eine Konfigurationstabelle fest.  
1. Wählen Sie eine Konfigurationstabelle aus der Liste und wählen Sie **Liste bearbeiten** aus.  
2. Wählen Sie eine Tabelle, für die Sie Feldinformationen festlegen möchten, und wählen Sie auf der Registerkarte Aktionen in der Gruppe Anzeigen **Felder** aus.  
3. Um nur die Felder auszuwählen die Sie hinzufügen möchten, wählen Sie die **Eingeschlossene löschen** Aktion. Um alle Felder hinzuzufügen, wählen Sie **Eingeschlossene festlegen**.  
4. Um festzulegen, dass die Felddaten nicht bestätigt werden sollen, löschen Sie das Kontrollkästchen **Feld überprüfen** für das Feld.  
5. Wählen Sie die Schaltfläche **OK** aus.  
6. Um einen bestimmten Satz von Datensätzen zu filtern, um ihn im Konfigurationsarbeitsblatt zu berücksichtigen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Anzeigen die Option **Filter**.

Sie können Bereiche von Funktionen und Gruppen von Tabellen im Arbeitsblatt erstellen, um ähnliche Funktionen zusammenzufügen. Sie können sich beispielsweise beim Einrichten des Kontenplans für die Konfiguration dafür entscheiden, eine Gruppe von Buchungstabellen zu erstellen. Üblicherweise werden Bereiche verwendet, um einen Reihe von Tabellen zu gruppieren, die einem Funktionsbereich entsprechen. Jeder Bereich kann Gruppen enthalten. Eine Gruppe kann verwendet werden, um die Tabellen zu organisieren, die eine gemeinsame Bedeutung haben.  

Nachfolgend wird beschrieben, wie Sie Bereichs- und Gruppenbezeichnungen addieren können, nachdem Sie die erste Liste von Tabellen erstellt haben. Nachdem Sie diese Kategorien hinzugefügt haben, können Sie fortfahren und der Liste weiteres hinzufügen und sie zu ändern.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>So kategorisieren und gruppieren Sie Funktionalitäten im Arbeitsblatt.  
1. Fügen Sie am Anfang eines Bereichs eine neue Zeile in das Arbeitsblatt ein.  
2. Wählen Sie im Feld **Zeilenart** die Option **Bereich** aus. Geben Sie im Feld **Namen** einen Namen für das Gebiet ein.  
3. Fügen Sie am Anfang einer Gruppe von Tabelle eine neue Zeile in das Arbeitsblatt ein.  
4. Wählen Sie im Feld **Zeilenart** die Option **Gruppe** aus. Geben Sie im Feld **Namen** einen Namen für das Gebiet ein. Der Gruppenname wird automatisch eingerückt.  
5. Um Tabellen in die entsprechende Kategorie zu verschieben, wählen Sie die Aktion **Nach Oben** oder **Nach Unten** verschieben. Alternativ können Sie eine Arbeitsblattzeile löschen und die Tabelle an der erforderlichen Stelle erneut einfügen.  

Einige [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen sind Standard und die Daten darin ändern sich wahrscheinlich von Implementierung zu Implementierung nicht. Zur Verbesserung Ihrer Debitorenorientierung können Sie diese Tabellen aus dem Arbeitsblatt entfernen, nachdem Sie sie in das Konfigurationspaket eingeschlossen haben. Einmal hinzugefügt, bleiben die Tabellen Teil des Konfigurationspakets.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>So entfernen Sie eine Standardtabelle aus dem Arbeitsblatt.  
Nachdem Sie einem Konfigurationspaket alle erforderlichen Tabellen hinzugefügt haben, legen Sie fest, welche Tabellen keine Debitoraufmerksamkeit erfordern.  
1.  Wählen Sie die Tabellen aus, und löschen Sie sie, indem Sie die **Löschen** Aktion auswählen.  

    > [!NOTE]  
    >  Die Tabellen bleiben im Paket, obwohl sie aus dem Vorschlag gelöscht werden.  

## <a name="to-review-and-customize-existing-database-data"></a>So können Sie vorhandene Datenbank-Daten prüfen und anpassen.
Wenn Sie ein Konfigurationspaket für eine Lösung erstellen, können Sie die verfügbaren Datenbankdaten anzeigen und anpassen, um Ihren Debitoranforderungen entsprechen. Die Datenbanktabelle muss eine zugeordnete Seite haben.  

## <a name="to-customize-data-in-the-database"></a>So passen Sie Daten in der Datenbank an.  

1.  Identifizieren Sie im **Konfigurationsarbeitsblatt** die Tabellen, deren Daten Sie anzeigen oder anpassen möchten.  

    > [!NOTE]  
    >  Stellen Sie sicher, dass jede Tabelle eine Seiten-ID hat, die ihr zugeordnet ist. Für Standard [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen wird dieser Wert automatisch ausgefüllt. Für benutzerdefinierte Tabellen müssen Sie die ID zur Verfügung stellen  

2.  Wählen Sie die **Datenbankdaten** Aktion aus.  

     Das [!INCLUDE[prod_short](includes/prod_short.md)]-Fenster für die Seite wird geöffnet.  

3.  Überprüfen Sie die verfügbaren Informationen. Ändern Sie sie bei Bedarf, indem Sie Datensätze löschen, die nicht relevant sind oder indem Sie neue hinzufügen.

## <a name="see-also"></a>Siehe auch  
[Unternehmenskonfiguration einrichten](admin-set-up-company-configuration.md)  
[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]