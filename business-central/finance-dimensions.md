---
title: Arbeiten mit Dimensionen zum Verfolgen und Analysieren von Daten
description: 'Verwenden Sie Dimensionen, um Einträge zu kategorisieren, z.B. nach Abteilung oder Projekt, damit Sie Daten leichter verfolgen und analysieren können, um gute Geschäftsentscheidungen zu treffen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 08/08/2024
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---

# <a name="work-with-dimensions"></a>Arbeiten mit Dimensionen

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Anstatt also für jede Abteilung und jedes Projekt separate Sachkonten einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und müssen keinen komplizierten Kontenplan erstellen. Erfahren Sie mehr unter [Business Intelligence](bi.md).

Ein weiteres Beispiel ist die Festlegung einer Dimension mit dem Namen *Abteilung*, die Sie dann beim Buchen von Verkaufsbelegen verwenden. Auf diese Weise können Sie Business Intelligence Tools verwenden, um zu sehen, welche Abteilung welche Artikel verkauft hat. Je mehr Dimensionen Sie verwenden, desto detaillierter sind die Berichte, auf die Sie Ihre Geschäftsentscheidungen stützen. Ein einziger Verkaufseintrag kann nämlich Informationen aus mehreren Dimensionen enthalten, wie z.B.:  

* Das Konto, auf das der Verkauf des Artikels gebucht wurde.  
* Wo das Element verkauft wurde.
* Wer ihn verkauft hat.
* Welcher Kunde ihn gekauft hat.

## <a name="analyze-by-dimensions"></a>Analysieren nach Dimensionen

Dimensionen spielen eine wichtige Rolle in der Business Intelligence, wie auch beim Definieren von Analyseansichten. Erfahren Sie mehr unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

> [!TIP]
> Eine schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, ist die Aktion **Dimensionsfilter festlegen**, mit der Sie Summen im Kontenplan und auf Buchungsseiten nach Dimensionen filtern können.

> [!NOTE]
> Analyseansichten verwenden oft Daten aus Dimensionen. Wenn Sie feststellen, dass bei gebuchten Sachkontenbuchungen eine falsche Dimension verwendet wurde, können Sie die Dimensionswerte korrigieren und Ihre Analyseansichten aktualisieren. Dies trägt dazu bei, dass Ihre Finanzberichte und Analysen korrekt bleiben. Erfahren Sie mehr unter [Problembehandlung und Korrektur von Dimensionen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets"></a>Dimensionen-Sets

Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Sie werden als Dimensionssatz-Einträge in der Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Außerdem wird jedes Dimensionen-Set und jeder Dimensionen-Set-Eintrag darin durch eine allgemeine Dimensionen-Set-ID identifiziert.  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

## <a name="set-up-dimensions"></a>Dimensionen einrichten

Sie können Dimensionen und Dimensionswerte definieren, um Erfassungen und Dokumente wie Verkaufsaufträge und Bestellungen zu kategorisieren. Sie errichten Dimensionen auf der Seite **Dimensionen**, wo Sie eine Zeile für jede Dimension erstellen, wie *Projekt*, *Abteilung*, *Bereich* und *Verkäufer*.

Sie erstellen auch Einrichtungswerte für Dimensionen. Nehmen wir an, die Werte repräsentieren die Abteilungen Ihrer Firma. Die Werte der Dimensionen können in einer hierarchischen Struktur festgelegt werden, die dem Kontenplan ähnelt. Das bedeutet, dass die Daten in verschiedene Granularitätsebenen aufgeschlüsselt werden können und Teilmengen von Dimensionswerten summiert werden können. Sie können beliebig viele Dimensionen und Dimensionswerte in Ihrem Mandanten definieren und Sie können eine unbegrenzte Anzahl von Dimensionswerten für jede Dimension festlegen.

Wenn die Dimensionen und Werte festgelegt sind, können Sie auf der Seite **Hauptbuchhaltung Einrichtung** globale und Verknüpfungsdimensionen definieren. Diese Dimensionen stehen Ihnen dann jederzeit zur Auswahl als Felder in Buchungsblattzeilen, Belegzeilen und Sachkonteneinträgen zur Verfügung, ohne dass Sie die Seite **Dimensionen** öffnen müssen. Mehr dazu erfahren Sie im Abschnitt [Zum Festlegen von globalen Dimensionen und Verknüpfungen](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale Dimensionen** werden als Filter beispielsweise in Berichten und XMLports und Stapelverarbeitungen verwendet. Sie können nur zwei globale Dimensionen verwenden. Wählen Sie daher Dimensionen aus, die Sie häufig verwenden.
* **Shortcutdimensionen** sind verfügbar als Felder in Buch.-Blättern, Belegzeilen und Belegeinträgen. Sie können bis zu acht davon erstellen.  

> [!NOTE]
> Nachdem Sie eine neue Dimension in einem Eintrag verwendet haben, z. B. in einer Zeile oder einem neuen Datensatz, können Sie die Dimension nicht löschen, selbst wenn Sie den Eintrag nicht buchen. Dies ist darauf zurückzuführen, dass [!INCLUDE[prod_short](includes/prod_short.md)] sofort einen Dimensionssatz für die Zeile oder den Datensatz erstellt. Weitere Informationen finden Sie im Abschnitt [Dimensions-Sets](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>So richten Sie Standarddimensionen für Debitoren, Kreditoren und andere Konten ein

Sie können eine Standarddimension für ein bestimmtes Konto einrichten. Die Dimension wird in das Journal oder den Beleg kopiert, wenn Sie die Kontonummer in eine Zeile eingeben, aber Sie können den Code in der Zeile löschen oder ändern, falls erforderlich. Sie können auch eine Dimension für die Buchung einer Buchung auf einem bestimmten Kontotyp verlangen. > 

> [!NOTE]
> Standarddimensionsprioritäten eröffnen sich für Szenarien in Verkäufen und Einkäufen, denen Sie besondere Aufmerksamkeit schenken sollten. Wenn Sie standardmäßige Dimensionsprioritäten für Verkaufs- und Einkaufsbelege verwenden, betrachtet [!INCLUDE [prod_short](includes/prod_short.md)] die Dimensionen in der Kopfzeile immer als vom Debitor oder Kreditor stammend. Dies gilt für Dimensionen, die Sie manuell oder standardmäßig festlegen, und ist besonders relevant, wenn Sie Standarddimensionen für Standorte und Artikel, aber nicht für Debitoren oder Kreditoren verwenden.
>
> **Beispiel**
>
> Sie haben ein Szenario mit den folgenden Dimensionseinstellungen:
>
> * Ein Kunde ohne Standarddimensionen
> * Ein Artikel mit ADM als Dimensionswert für die Dimension DEPARTMENT
> * Ein Lagerort mit PROD als Dimensionswert für die Dimension DEPARTMENT
> * Standarddimensionsprioritäten sind als Debitor > Artikel > Lagerort festgelegt
>
> Wenn Sie in diesem Szenario einen neuen Beleg erstellen, werden Dimensionen wie folgt verwendet:
>
> * Wenn Sie einen neuen Beleg erstellen und einen Lagerort hinzufügen, ist der Standardwert für neue Zeilen PROD. Wenn Sie Zeilen mit Artikeln hinzufügen, behält [!INCLUDE [prod_short](includes/prod_short.md)] PROD bei, da es aus der Kopfzeile des Belegs stammt.
>
> * Wenn Sie einen neuen Beleg erstellen und Elemente mit dem ADM-Dimensionswert hinzufügen und dann eine Position in der Kopfzeile des Belegs angeben, fragt [!INCLUDE [prod_short](includes/prod_short.md)], ob Sie die vorhandenen Zeilen überschreiben möchten, da ein Konflikt besteht.
>
> Wir empfehlen Ihnen, Ihre standardmäßige Dimensionseinrichtung, Dimensionsprioritäten und die Reihenfolge, in der Sie Daten in Belege eingeben, zu testen.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Dimensionen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Dimensionen** die entsprechende Dimension aus und wählen Sie dann die Aktion **Kontotyp Standarddim**.  
3. Füllen Sie für jede neue Vorgabedimension eine eigene Zeile aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Wenn Sie eine Dimension benötigen, aber der Dimension keinen Standardwert zuweisen möchten, lassen Sie das Feld **Dimensionswertcode** leer und wählen Sie dann **Code obligatorisch** im Feld **Wertbuchung**.  

> [!WARNING]  
> Wenn ein Konto in einem Batchauftrag **Wechselkurse anpassen** oder **Lagerkosten ins Hauptbuch buchen** verwendet wird, wählen Sie nicht **Code obligatorisch** oder **Gleicher Code**. Diese Stapelverarbeitungen können keine Dimensionscodes verwenden.  

> [!NOTE]  
> Wenn ein Konto eine andere Dimension haben muss als die Standarddimension, die der Kontoart zugewiesen ist, müssen Sie eine neue Standarddimension für das Konto festlegen. Die Standarddimension für das Konto ersetzt dann die Vorgabedimension für die Tabelle.  

### <a name="to-set-up-default-dimension-priorities"></a>Prioritäten für Standarddimensionen einrichten:

Verschiedene Kontotypen, wie z.B. ein Kundenkonto und ein Artikelkonto, können unterschiedliche Standarddimensionen haben. Folglich kann ein Eintrag mehr als eine vorgeschlagene Standarddimension haben. Um solche Konflikte zu vermeiden, können Sie in den verschiedenen Quellen Prioritätsregeln hinterlegen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Vorgabedimension Prioritäten** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Vorgabedimension Prioritäten** geben Sie in das Feld **Herkunftscode** den Herkunftscode für die Eintragstabelle ein, für die die Prioritäten der Vorgabedimensionen gelten sollen.  
3. Füllen Sie für jede Vorgabedimension Prioritäten, die Sie für den ausgewählten Quellcode wünschen, eine Zeile aus.
4. Wiederholen Sie den Vorgang für jeden Quellcode, für den Sie Vorgabedimensions Prioritäten festlegen möchten.  

> [!IMPORTANT]  
> Wenn Sie zwei Tabellen mit der gleichen Priorität für denselben Quellcode festlegen, wird mit [!INCLUDE[prod_short](includes/prod_short.md)] immer die Tabelle mit der niedrigsten Tabellen-ID ausgewählt.  

### <a name="to-set-up-dimension-combinations"></a>Dimensionskombinationen einrichten:

Um das Buchen von Posten mit widersprüchlichen oder irrelevanten Dimensionen zu vermeiden, können Sie bestimmte Kombinationen von Dimensionen sperren oder einschränken. Eine gesperrte Dimensionskombination bedeutet, dass Sie unabhängig von den Dimensionswerten nicht beide Dimensionen auf denselben Eintrag buchen können. Im Gegensatz dazu bedeutet eine eingeschränkte Dimensionskombination, dass Sie beide Dimensionen auf denselben Eintrag buchen können, allerdings nur für bestimmte Kombinationen von Dimensionswerten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Dimensionskombinationen** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Dimensionskombinationen** wählen Sie das gewünschte Feld für die Dimensionskombination aus den folgenden Optionen.  

    |Feld|Description|
    |----------------------------------|---------------------------------------|  
    |**Keine Einschränkungen**|Diese Dimension hat keine Einschränkungen. Alle Dimensionswerte sind erlaubt.|  
    |**Eingeschränkt**|Diese Dimensionskombination hat, abhängig von den Dimensionswerten, die Sie eingeben, Beschränkungen. Sie müssen die Einschränkungen auf der Seite **Dimensionswert Kombinationen** festlegen.|  
    |**Gesperrt**|Diese Dimensionskombination ist nicht zulässig.|  

3. Wenn Sie die Option **Eingeschränkt** wählen, müssen Sie angeben, welche Dimensionskombinationen gesperrt sind. Wählen Sie dazu das Feld, in dem Sie die Kombination der Dimensionswerte definieren.  
4. Wählen Sie anschließend die Kombination von Dimensionswerten aus, die gesperrt werden soll, und geben Sie im Feld die Option **Blockiert** an. Ein leeres Feld bedeutet, dass die Dimensionswertkombination zugelassen ist. Wiederholen Sie diesen Vorgang, um mehrere Kombinationen zu sperren.  

> [!NOTE]  
> Die gleichen Dimensionen werden sowohl in den Zeilen als auch in den Spalten angezeigt, d.h. alle Dimensionskombinationen erscheinen zweimal. [!INCLUDE[prod_short](includes/prod_short.md)] zeigt automatisch die Einstellung in beiden Feldern an. In den Feldern von links oben und unten können Sie nichts auswählen, da diese Felder sowohl in den Zeilen als auch in den Spalten dieselbe Dimension aufweisen.  
>
> Die gewählte Option wird erst beim Verlassen des Feldes sichtbar.  
>
> Um anstelle des Codes den Namen der Dimension anzeigen zu lassen, wählen Sie das Feld **Spaltennamen anzeigen**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>So richten Sie globale und Shortcut-Dimensionen ein

Globale und Shortcut-Dimensionen können überall in [!INCLUDE[prod_short](includes/prod_short.md)] als Filter verwendet werden, auch in Berichten, Batchaufträgen, Posten und Analyseansichten. Globale Dimensionen und Verknüpfungen können direkt eingefügt werden, ohne dass Sie die Seite **Dimensionen** öffnen müssen. In Buch.-Blattzeilen und Belegzeilen können Sie globale und Shortcutdimensionen in einem Feld der Zeile auswählen. Sie können zwei globale und acht Shortcutdimensionen einrichten. Wählen Sie die Dimensionen, die Sie am häufigsten verwenden.

> [!IMPORTANT]
> Wenn Sie eine globale oder Verknüpfungsdimension ändern, müssen alle Einträge, die mit dieser Dimension gebucht wurden, aktualisiert werden. Um eine globale Dimension zu ändern, können Sie die Funktion **Globale Dimensionen ändern** verwenden, aber das kann zeitaufwändig sein, die Leistung beeinträchtigen und die Tabellen können während der Aktualisierung gesperrt sein. Stellen Sie sicher, dass Sie Ihre globalen und Verknüpfungsdimensionen sorgfältig auswählen, damit Sie sie später nicht ändern müssen. Verwenden Sie die Aktion **Dimension ändern**, um eine Verknüpfungsdimension zu ändern.
>
> Mehr dazu erfahren Sie im Abschnitt [Zum Ändern globaler Dimensionen](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Wenn Sie eine globale oder Verknüpfungsdimension hinzufügen oder ändern, werden Sie automatisch ab- und wieder angemeldet, so dass der neue Wert für die Verwendung vorbereitet ist.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder im Inforegister **Dimensionen** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>So ändern Sie globale Dimensionen

Wenn Sie eine globale oder verkürzte Dimension ändern, werden alle mit dieser Dimension gebuchten Einträge aktualisiert. Da dieser Prozess zeitaufwändig sein und die Leistung beeinträchtigen kann, stehen zwei verschiedene Modi zur Verfügung, um den Prozess an die Größe der Datenbank anzupassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Globale Dimensionen ändern** aus.
3. Wählen Sie oben auf der Seite einen der beiden folgenden Modi, um den Batchauftrag auszuführen.

    |Option|Description|
    |-|-|
    |**Sequenziell**|(Standard) Die gesamte Dimensionsänderung wird in einer Transaktion durchgeführt, wobei alle Einträge auf die Dimensionen zurückgesetzt werden, die sie vor der Änderung hatten.<br /><br />Diese Option empfiehlt sich, wenn die Firma nur relativ wenige gebuchte Einträge hat. In diesem Fall dauert der Batchauftrag am wenigsten lange. Der Vorgang sperrt mehrere Tabellen und blockiert andere Benutzer, bis es Fertig ist. Beachten Sie, dass bei großen Datenbanken der Vorgang in diesem Modus möglicherweise nicht abgeschlossen wird. Verwenden Sie in diesem Fall die Option **Parallel**.|
    |**Parallel**|Die Dimensionsänderung erfolgt in mehreren Hintergrundsitzungen und der Vorgang wird in mehrere Transaktionen aufgeteilt. Um diese Option zu verwenden, aktivieren Sie die Umschaltung **Parallelverarbeitung**. <br /><br />Diese Option empfehlen wir für große Datenbanken oder Unternehmen mit zahlreichen Einträgen, da sie die kürzeste Zeit in Anspruch nimmt. Beachten Sie, dass in diesem Modus der Aktualisierungsvorgang nicht gestartet wird, wenn mehr als eine aktive Datenbanksitzung vorhanden ist.|  

4. Geben Sie in den Feldern **Globaler Dimensionscode 1** und/oder **Globaler Dimensionscode 2** die neue(n) Dimension(en) ein. Die aktuellen Dimensionen werden hinter den Feldern grau dargestellt.
5. Führen Sie je nach Modus einen der folgenden Schritte aus:
    * Im Modus **Sequenziell** wählen Sie die **Start** Aktion.
    * Im Modus **Parallel** wählen Sie die **Vorbereiten** Aktion.

    Die Registerkarte **Protokolleinträge** ist mit Informationen über die zu ändernden Dimensionen gefüllt.
6. Melden Sie sich von [!INCLUDE[prod_short](includes/prod_short.md)] ab und dann wieder an.
7. Wählen Sie die Aktion **Start**, um die parallele Verarbeitung der Änderungen an den Dimensionen zu beginnen.

### <a name="example-of-dimension-setup"></a>Beispiel für die Einrichtung von Dimensionen

Nehmen wir an, Ihre Firma möchte Transaktionen auf der Grundlage der Organisationsstruktur und der geografischen Standorte verfolgen. Zu diesem Zweck legen Sie auf der Seite **Dimensionen** zwei Dimensionen fest:

* **BEREICH**  
* **ABTEILUNG**  

| Code | Name | Code Caption | Filter Caption |
| --- | --- | --- | --- |
| BEREICH |Ursprungs- / Bestimmungsregion |Gebietscode |Filter "Bereich" |
| ABTEILUNG |Abteilung |Abteilungscode |Kostenstellenfilter |

Für **AREA** fügen Sie die folgenden Dimensionen hinzu:

| Code | Name | Dimensionswertart |
| --- | --- | --- |
| 10 |Amerika |Von-Summe |
| 20 |Nordamerika |Standard |
| 30 |Pazifik |Standard |
| 40 |Südamerika |Standard |
| 50 |Amerika, gesamt |Bis-Summe |
| 60 |Europa |Von-Summe |
| 70 |EU |Standard |
| 80 |Nicht-EU |Standard |
| 90 |Europa, gesamt |Bis-Summe |

Um die beiden hauptgeografischen Gebiete Amerika und Europa, fügen Sie bei Bedarf Unterkategorien für Bereiche hinzu, indem Sie die Dimensionswerte einrücken. So können Sie über Umsätze oder Spesen in Regionen berichten und Summen für die größeren geografischen Gebiete erhalten. Sie können auch Länder, Regionen, Landkreise oder Städte als Dimensionswerte verwenden, je nach Ihrem Geschäft.

> [!NOTE]  
> Um eine Hierarchie einzurichten, muss der Code in alphabetischer Reihenfolge sein. Dazu gehören auch die Codes der in [!INCLUDE[prod_short](includes/prod_short.md)] angegebenen Dimensionswerte.  

Für **ABTEILUNG** fügen Sie die folgenden Dimensionswerte hinzu:

| Code | Name | Dimensionswertart |
| --- | --- | --- |
| ADMIN |Verwaltung |Standard |
| PROD |Produktion |Standard |
| VERKAUF |Verkauf |Standard |

Mit dieser Einrichtung können Sie Ihre beiden Dimensionen als die beiden globalen Dimensionen auf der Seite **Hauptbuchhaltung Einrichtung** hinzufügen. Das bedeutet, dass Sie BEREICH und ABTEILUNG als Filter für Hauptbuch-Einträge sowie in allen Berichten verwenden können. Beide globalen Dimensionen stehen auch als Shortcutdimensionen in Buch.-Blattzeilen und Belegköpfen zur Verfügung.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Einen Überblick über mehrfach verwendete Dimensionen erhalten

Die Seite **Standarddimensionen-Mehrfach** gibt an, wie eine Gruppe von Konten Dimensionen und Dimensionswerte verwendet. Sie können dies festlegen, indem Sie mehrere Konten markieren und dann die Standarddimensionen und Dimensionswerte für diese Konten festlegen. Danach schlägt die Anwendung diese Dimensionen und Dimensionswerte immer dann vor, wenn eines dieser Konten verwendet wird, z.B. in einer Buchungsblattzeile. Dies vereinfacht das Buchen für den Anwender, da die Anwendung die Dimensionsfelder automatisch ausfüllt. Beachten Sie jedoch auch, dass die vorgeschlagenen Dimensionen z.B. in einer Buchungsblattzeile geändert werden können.

Die Seite **Vorgabedimensionen - Mehrfach** enthält die folgenden Felder:

|Feld|Description|
|-----|-----------|  
|**Dimensionscode**|Zeigt alle Dimensionen an, die als Standarddimensionen für ein oder mehrere markierte Konten definiert sind. Wenn Sie dieses Feld auswählen, sehen Sie eine Liste aller verfügbaren Dimensionen. Wenn Sie eine Dimension auswählen, wird diese Dimension als Standarddimension für alle markierten Konten definiert.|
|**Dimensionswertcode**|Zeigt entweder einen einzelnen Dimensionswert oder den Ausdruck (Konflikt) an. Wenn eine Dimensionswert in dem Feld angezeigt wird, dann haben alle markierten Konten denselben Vorgabedimensionswert für eine Dimension. Wenn in dem Feld der Begriff (Konflikt) angezeigt wird, dann haben nicht alle markierten Konten denselben Standardwert für eine Dimension. Wenn Sie das Feld **Dimensionscode** auswählen, sehen Sie eine Liste aller verfügbaren Dimensionswerte für eine Dimension. Wenn Sie einen Dimensionswert auswählen, wird dieser als Standard-Dimensionswert für alle markierten Konten definiert.|
|**Dimensionswertbuchung**|Zeigt entweder eine einzelne Dimensionswertbuchung oder den Ausdruck (Konflikt) an. Wenn eine Dimensionswertbuchungsregel in dem Feld angezeigt wird, dann haben alle markierten Konten dieselbe Dimensionswertbuchungsregel für eine Dimensionswertbuchung. Wenn in dem Feld der Begriff (Konflikt) angezeigt wird, gilt nicht für alle markierten Konten die gleiche Buchungsregel für einen Dimensionswert. Wenn Sie das Feld **Wertbuchung** auswählen, sehen Sie eine Liste der Wertbuchungsregeln für eine Dimension. Wenn Sie eine Wertbuchungsregel auswählen, wird diese auf alle markierten Konten angewendet.|

## <a name="use-dimensions"></a>Dimensionen verwenden

In einem Beleg, z. B. einem Verkaufsauftrag, können Sie Dimensionsinformationen sowohl für eine einzelne Belegzeile als auch für den Beleg selbst hinzufügen. So könnten Sie auf der Seite **Verkaufsauftrag** Dimensionswerte für die ersten beiden Verknüpfungsdimensionen der einzelnen Verkaufszeilen eingeben und dann weitere Dimensionsinformationen hinzufügen, wenn Sie die Schaltfläche **Dimensionen** wählen.  

Wenn Sie stattdessen in einem Buch.-Blatt arbeiten, können Sie auf dieselbe Art und Weise Dimensionsinformationen hinzufügen, wenn Sie Shortcutdimensionen direkt als Felder in Buch.-Blattzeilen eingerichtet haben.  

Sie können auch Standarddimensionen für Konten oder Kontoarten festlegen, so dass Dimensionen und Dimensionswerte automatisch ausgefüllt werden.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Einsehen von Globalen Dimensionen in Postenseiten

Globale Dimensionen sind immer firmenbezogen und nach Unternehmen benannt. Um die globalen Dimensionen für das Unternehmen anzuzeigen, öffnen Sie die Seite **Finanzbuchhaltung Einrichtung**.

Auf einer Postenseite können Sie sehen, ob für Posten globale Dimensionen vorhanden sind. Die beiden globalen Dimensionen unterscheiden sich von Ihren anderen Dimensionen, da Sie sie als Filter an beliebiger Stelle in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden können.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Kontenplan** die **Ressourcenposten**-Aktion aus.  
3. Um nur Einträge zu sehen, die relevant sind, legen Sie einen oder mehrere Filter auf der Seite fest.  
4. Um alle Dimensionen für einen Eintrag zu sehen, markieren Sie den Eintrag und wählen Sie dann die Aktion **Dimensionen**.  

> [!NOTE]  
> Auf der Seite **Sachkonto Dimensionen** werden die Dimensionen für jeweils einen Sachkontoeintrag angezeigt. Sie werden sehen, dass sich der Inhalt der Seite **Sachkonto Dimensionen** entsprechend ändert, wenn Sie durch die Ledgereinträge blättern.

## <a name="see-also"></a>Siehe auch

[Business Intelligence](bi.md)    
[Finanzen](finance.md)    
[Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
