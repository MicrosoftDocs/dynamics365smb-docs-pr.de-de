---
title: Problembehandlung und Korrektur von Dimensionen
description: 'Erfahren Sie, wie Sie typische Dimensionsfehler beheben und Dimensionen korrigieren können, nachdem sie in gebuchten Transaktionen verwendet wurden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="troubleshooting-and-correcting-dimensions"></a>Problembehandlung und Korrektur von Dimensionen

Finanzberichte und Analyseansichten stützen sich oft auf Daten aus Dimensionen. Trotz der vorhandenen Sicherheitsvorkehrungen passiert manchmal ein Fehler, der zu Ungenauigkeiten führen kann. In diesem Artikel werden einige der typischen Fehler beschrieben und es wird erklärt, wie Sie Dimensionszuordnungen auf gebuchten Transaktionen korrigieren können, damit die Finanzberichte korrekt sind.

## <a name="troubleshooting-dimensions-errors"></a>Beheben von Dimensionsfehlern

Beim Buchen von Belegen oder Buchungsblattzeilen, die Dimensionen enthalten, können verschiedene Fehler auftreten. Sie hängen jedoch in der Regel mit einer falschen Dimensionseinrichtung oder -zuweisung zusammen.

> [!NOTE]
> In der folgenden Liste der möglichen Fehlermeldungen stehen die *%X*-Codes als Ersatzzeichen für die Datenvariablen, die abhängig vom Kontext in der eigentlichen Nachricht in der Benutzeroberfläche enthalten sind. Beispielsweise könnte *%1 %2 ist blockiert.* in der Benutzeroberfläche als "Dimensionscode BEREICH blockiert" angezeigt werden.  

|Problem|Fehlermeldung|Mögliche Lösung|
|-----|-------------|-----------------|
|Blockierte Dimension|%1 %2 ist blockiert.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der blockierten Dimension enthalten und heben Sie die Blockierung auf.<br />- Entfernen Sie die Dimensionssatzposition für die blockierte Dimension.|
|Gelöschte Dimension|%1 %2 kann nicht gefunden werden.|-Erstellen Sie die fehlende Dimension neu.<br />- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der fehlenden Dimension enthalten und fügen Sie sie hinzu.<br />- Entfernen Sie die Dimensionssatzposition für die fehlende Dimension.|
|Blockierter Dimensionswert|%1 %2 - %3 ist gesperrt.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit dem blockierten Dimensionswert enthalten und heben Sie die Blockierung auf.<br />- Entfernen Sie die Dimensionssatzposition für den blockierten Dimensionswert.|
|Gelöschter Dimensionswert|    %1 für %2 fehlt.|-Erstellen Sie den fehlenden Dimensionswert neu.<br />- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit dem fehlenden Dimensionswert enthalten und fügen Sie ihn hinzu.<br />- Entfernen Sie die Dimensionssatzposition für den fehlenden Dimensionswert.|
|Nicht zugelassener Dimensionswert|Dimensionswerttyp für %1 %2 – %3 darf nicht %4 sein.|- Ändern Sie das Feld **Dimensionswerttyp** auf der Seite **Dimensionswerte** zu **Standard** oder **Von-Summe**.<br />- Entfernen Sie die Dimensionssatzposition für den blockierten Dimensionswert.|
|Blockierte Dimensionskombination|Dimensionen %1 und %2 können nicht gleichzeitig verwendet werden.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der blockierten Dimensionskombination enthalten und heben Sie die Blockierung auf.<br />- Ändern Sie eine der konfliktverursachenden Berechtigungssatzzeilen für die Dimensionskombination.|
|Blockierte Dimensionswertkombination|Dimensionskombinationen %1 - %2 und %3 - %4 können nicht gleichzeitig verwendet werden.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der blockierten Kombination an Dimensionswerten enthalten und heben Sie die Blockierung auf.<br />- Ändern Sie eine der konfliktverursachenden Berechtigungssatzzeilen für die Kombination an Dimensionswerten.|
|Leerer Dimensionswertcode für Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Code notwendig** enthält.|-Wählen Sie einen %1 für den %2 %3 aus.<br />-Wählen Sie einen %1 für den %2 %3 für %4 %5 aus.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />- Geben Sie einen nicht leeren Dimensionswert für die den Konflikt verursachende Dimension in den Dimensionssatz ein.|
|Falscher Dimensionswertcode für Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Gleicher Code** enthält.|-Wählen Sie einen %1 %2 für den %3 %4 aus.<br />-Wählen Sie einen %1 %2 für den %3 %4 für %5 %6 aus.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />-Geben Sie den erforderlichen Dimensionswert für die widersprüchliche Dimension in den Dimensionssatz ein.|
|Nicht leerer Dimensionswertcode für leere Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Gleicher Code** enthält|-%1 %2 muss leer sein.<br />-%1 %2 muss für %3 %4 leer sein.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />-Geben Sie einen leeren Dimensionswertcode für die widersprüchliche Dimension in den Dimensionssatz ein.|
|Unerwarteter Dimensionswert für Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Kein Code** enthält.|-%1 %2 darf nicht angegeben werden.<br />-%1 %2 darf für %3 %4 nicht angegeben werden.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />- Entfernen Sie die widersprüchliche Zeile aus dem Dimensionssatz.|
|Eine Dimensionskorrektur wird nicht korrekt abgeschlossen.||Wählen Sie **Zurücksetzen** aus. um die Korrektur auf einen Entwurfszustand zurückzusetzen. Dadurch werden die Änderungen zurückgesetzt und Sie können die Korrektur erneut ausführen.|

## <a name="changing-dimension-assignments-after-posting"></a>Dimensionszuweisungen nach dem Buchen ändern

Wenn Sie feststellen, dass bei gebuchten Sachposten eine falsche Dimension verwendet wurde, können Sie die Dimensionswerte korrigieren und Ihre Analyseansichten aktualisieren. Die Korrektur hilft, dass Ihre Finanzberichte und Analysen korrekt bleiben.

> [!IMPORTANT]
> Die Funktionen zum Korrigieren von Dimensionen sind nur dazu gedacht, die Genauigkeit der Finanzberichte zu unterstützen. Dimensionskorrekturen beziehen sich nur auf die Sachbucheinträge. Sie ändern nicht die Dimensionen, die den Einträgen in anderen Sachkonten für dieselbe Transaktion zugeordnet sind. Es besteht eine Diskrepanz zwischen den Dimensionen, die im Hauptbuch und den Nebenbüchern zugeordnet sind.

### <a name="setting-up-dimension-corrections"></a>Dimensionskorrekturen einrichten

Beim Einrichten von Dimensionskorrekturen sind zwei Dinge zu beachten:

* Gibt es Dimensionen, bei denen Sie nicht zulassen möchten, dass sie von anderen geändert werden? Geben Sie auf der Seite **Dimensionskorrektureinstellungen** die Dimensionen an, die Sie für Änderungen blockieren möchten.
* Wer darf Dimensionen ändern? Weisen Sie die **D365 DIM-KORREKTUR** Erlaubnis Benutzern zu, damit Personen Änderungen vornehmen können. Mit den Berechtigungen können sie Dimensionskorrekturen erstellen, ausführen und bei Bedarf rückgängig machen. Sie können auch blockierte Dimensionen angeben. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Eine Dimension korrigieren

Sie können einen oder mehrere Hauptbucheinträge manuell auswählen oder Filter verwenden, um Sätze von Einträgen auszuwählen. Bei Bedarf können Sie auch Dimensionen hinzufügen oder löschen. 

1. Verwenden Sie eine der folgenden Seiten, um eine Dimensionskorrektur zu starten:

    * Auf der Seite **Sachpostenjournalnr.**, indem Sie ein Register auswählen und dann die Aktion **Dimensionen korrigieren** auswählen. Diese Aktion startet eine Korrektur für die Posten im ausgewählten Journal.
    * Auf der Seite **Sachposten**, indem Sie die Aktion **Dimensionskorrektur** auswählen. 

2. Geben Sie im Feld **Beschreibung** die Informationen zur Veränderung ein. Andere Personen verwenden diese Informationen möglicherweise später, um zu verstehen, was getan wurde.
3. Wählen Sie im Inforegister **Ausgewählte Posten** die entsprechenden Einträge aus.

    > [!IMPORTANT]
    > Wenn Sie eine Auswahl ändern, werden die Werte im Inforegister **Dimensionskorrekturänderungen** zurückgesetzt. Wählen Sie daher immer die Einträge aus, bevor Sie Dimensionswertänderungen angeben.

   Die Optionen werden in der folgenden Tabelle beschrieben.

   |Option  |Beschreibung  |
   |---------|---------|
   |Zugehörige Posten hinzufügen     |Fügen Sie Sachkonteneinträge hinzu, die sich im selben Sachkontenregister befinden.|   
   |Nach Filter hinzufügen     |Verwenden Sie Filterkriterien, wenn Sie Sachbucheinträge hinzufügen.|
   |Manuelle Auswahl     |Wählen Sie bestimmte Sachkonteneinträge aus.         |
   |Nach Dimensionen hinzufügen     |Filtern Sie Sachkonteneinträge nach Dimensionen.         |
   |Posten entfernen     |Heben Sie Sachposten auf.         |
   |Auswahlkriterien verwalten     |Behalten Sie den Auswahlprozess im Auge und machen Sie die Auswahl bei Bedarf rückgängig.         |

4. Wählen Sie im Inforegister **Dimensionskorrekturänderungen** die Dimension aus, die Sie im Feld **Dimensionscode** ändern möchten und der neue Wert im Feld **Neuer Dimensionswertcode**.
5. Um die Korrektur zu bestätigen, wählen Sie **Dimensionsänderungen überprüfen** aus. Weitere Informationen finden Sie unter [Dimensionskorrekturen validieren](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Wählen Sie **Ausführen** aus.

### <a name="validating-dimension-corrections"></a>Dimensionskorrekturen überprüfen

Bevor Sie eine Korrektur ausführen, sollten Sie diese zuerst validieren. Die Validierung prüft auf Einschränkungen bei der Wertbuchung für die Sachkonten, Einschränkungen für Dimensionen und ob die Dimensionswerte blockiert sind. Während der Validierung wird der Status der Korrektur auf **Validierung in Bearbeitung** gesetzt. Nachdem Sie eine Korrektur validiert haben, wird das Ergebnis im Feld **Überprüfungsstatus** angezeigt. Wenn Fehler gefunden wurden, können Sie die Aktion **Fehler anzeigen** verwenden, um sie zu untersuchen. Nachdem Sie einen Fehler behoben haben, müssen Sie die Aktion **Erneut öffnen** zum Ausführen der Korrektur oder einer neuen Validierung verwenden.

Sie können eine Korrektur entweder sofort ausführen oder für eine spätere Ausführung planen. Wenn Sie Korrekturen an einem großen Datensatz ausführen, empfehlen wir, die Ausführung außerhalb der Geschäftszeiten zu planen. Weitere Informationen finden Sie unter [Dimensionskorrekturen bei großen Datensätzen](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Eine Korrektur rückgängig machen

Wenn Ihnen nach dem Korrigieren einer Dimension das, was Sie sehen, nicht gefällt, können Sie die Aktion **Rückgängig machen** zum Zurücksetzen des vorherigen Werts verwenden. Sie können jedoch nur die letzte Korrektur rückgängig machen. Bevor Sie eine Korrektur rückgängig machen, können Sie die Änderungen überprüfen, die sich aus dem Rückgängigmachen ergeben. Die Prüfung ist beispielsweise nützlich, wenn sich die Dimensionsbeschränkungen nach der Korrektur geändert haben.

Wenn die Aktion „Rückgängig“ nicht verfügbar ist, z. B. weil Sie viele Korrekturen vorgenommen haben, können Sie die Aktion **In Entwurf kopieren** verwenden, um eine neue Korrektur für dieselben Einträge zu starten.

### <a name="dimension-corrections-on-large-data-sets"></a>Dimensionskorrekturen bei großen Datenmengen

Seien Sie vorsichtig, wenn Sie große Sätze von Einträgen korrigieren, z. B. Sets mit mehr als 10.000 Einträgen. Wenn Sie können, empfehlen wir, dass Sie die Filter verwenden, um die Korrekturen für kleinere Datensätze auszuführen. Es ist auch eine gute Idee, Korrekturen außerhalb der normalen Geschäftszeiten durchzuführen. 

### <a name="use-analysis-views-with-dimension-corrections"></a>Analyseansichten mit Dimensionskorrekturen verwenden

Wenn **Bei Buchung aktualisieren** für eine Analyseansicht aktiviert ist, kann [!INCLUDE[prod_short](includes/prod_short.md)] die Ansicht aktualisieren, wenn Belege und Buch.-Blätter gebucht werden. Sie können Ansichten auch mit dieser Einstellung aktualisieren, die mit Ergebnissen von Dimensionskorrekturen aktiviert ist. Aktivieren Sie dazu den Umschalter **Analyseansichten aktualisieren**. Das Aktualisieren von Analyseansichten kann sich auf die Leistung auswirken, insbesondere bei großen Datenmengen. Wir empfehlen daher, die Analyseansichten nur bei kleinen Datenmengen zu aktualisieren.  

### <a name="viewing-historical-dimension-corrections"></a>Historische Dimensionskorrekturen anzeigen

Wenn ein Sachposten korrigiert wurde, können Sie die Änderung mithilfe der Aktion **Verlauf der Dimensionskorrekturen** untersuchen.

### <a name="handling-incomplete-corrections"></a>Umgang mit unvollständigen Korrekturen

Wenn eine Korrektur nicht abgeschlossen ist, wird auf der Korrekturkarte eine Warnung angezeigt. In diesem Fall können Sie die Aktion **Zurücksetzen** verwenden, um die Korrektur auf einen Entwurfsstatus zurückzusetzen und die Änderungen rückgängig zu machen. Sie können die Korrektur dann erneut ausführen.

> [!NOTE]
> Das Zurücksetzen einer unvollständigen Korrektur wirkt sich nicht auf Aktualisierungen der Analyseansichten aus, da diese am Ende des Korrekturprozesses erfolgen.

### <a name="use-cost-accounting-with-corrected-gl-entries"></a>Kostenrechnung mit korrigierten Sachposten verwenden

Nachdem Sie die Dimensionen korrigiert haben, sind Ihre Daten für die Kostenrechnung nicht mehr synchron. Die Kostenrechnung verwendet Dimensionen, um Beträge für Kostenstellen und Kostenträger zu aggregieren und Kostenzuteilungen durchzuführen. Das Ändern der Dimensionen für Sachpostet bedeutet wahrscheinlich, dass Sie Ihre Kostenrechnungsmodelle erneut ausführen sollten. Je nach den aktualisierten Daten und der Einrichtung Ihrer Kostenrechnungsfunktionen müssen Sie möglicherweise Folgendes tun:

* Löschen Sie nur einige Kostenjournale und führen Sie die Zuteilungen erneut aus.
* Löschen Sie alles und führen Sie alle Ihre Modelle erneut aus.

Sie müssen manuell ermitteln, wo sich Korrekturen an Dimensionen auf die Kostenrechnung auswirken und wo Aktualisierungen erforderlich sind. [!INCLUDE[prod_short](includes/prod_short.md)] bietet dafür derzeit keine automatisierte Option.

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
