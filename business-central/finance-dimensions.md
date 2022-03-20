---
title: Arbeiten mit Dimensionen, um Daten einfach zu verfolgen und zu analysieren
description: Sie können Dimensionen nutzen, um Einträge zu kategorisieren, beispielsweise nach Abteilungen oder Projekt, sodass Sie können Daten einfacher verfolgen und analysieren, um gute Geschäftsentscheidungen zu treffen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track, business intelligence
ms.search.form: 408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 494a79283ba7917666e708d9b07acf9523ef15b8
ms.sourcegitcommit: 6d48c1f601ed22b6b0358311baf63c073ab75e64
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2022
ms.locfileid: "8366729"
---
# <a name="working-with-dimensions"></a>Arbeiten mit Dimensionen

Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie auf Dokumenten wie Verkaufsaufträgen verfolgen und analysieren können. Dimensionen können beispielsweise angegeben, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Anstatt beispielsweise separate Hauptbuchkonten für jede Abteilung und jedes Projekt einzurichten, können Sie Dimensionen als Grundlage für die Analyse verwenden und vermeiden, dass Sie einen komplizierten Kontenplan erstellen müssen. Weitere Informationen finden Sie unter [Business Intelligence](bi.md).

Oder Sie richten beispielsweise eine Dimension mit dem Namen *Abteilung* ein und verwenden diese Dimension und einen Dimensionswert, wenn Sie Verkaufsbelege buchen. Dadurch können Sie auch intelligente Geschäfts-Tools verwenden, um zu sehen, welche Abteilung die Artikel verkauft hat. Je mehr Dimensionen Sie einrichten und verwenden, auf desto detaillierteren Berichten können Sie Ihre Geschäftsentscheidungen basieren. Zum Beispiel kann ein einzelner Verkaufsposten Informationen mehrerer Dimensionsinformationen enthalten, wie:  

* Das Konto, auf das der Artikelverkauf gebucht wurde  
* Wo der Artikel verkauft wurde
* Wer ihn verkauft hat
* Die Art des Debitors, die ihn kaufte  

## <a name="analyzing-by-dimensions"></a>Nach Dimensionen analysieren

Dimensionen spielen eine wichtige Rolle in der Business Intelligence, wie auch beim Definieren von Analyseansichten. Weitere Informationen finden Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

> [!TIP]
> Eine schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, können Sie die Aktion **Dimensionsbilder festlegen** im Kontenplan und auf Seiten nach Dimensionen für Einträge filtern verwenden.

> [!NOTE]
> Analyseansichten verwenden oft Daten aus Dimensionen. Wenn Sie feststellen, dass für gebuchte Hauptbucheinträge eine falsche Dimension verwendet wurde, können Sie die Dimensionswerte korrigieren und Ihre Analyseansichten aktualisieren. Dies hilft Ihnen dabei, Ihre Finanzberichte und ‑analysen korrekt zu halten. Weitere Informationen finden Sie unter [Fehlerbehebung und Korrektur von Dimensionen](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting)

## <a name="dimension-sets"></a>Dimensionssätze

<!--we describe what they are, but not their value.-->
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

## <a name="setting-up-dimensions"></a>Einrichtung von Dimensionen

Sie können die Dimensionen und die Dimensionswerte, die Sie verwenden möchten, definieren, um Buch.-Blätter und Belege zu kategorisieren, wie Verkaufsaufträge und Bestellungen einrichten. Sie errichten Dimensionen auf der Seite **Dimensionen**, wo Sie eine Zeile für jede Dimension erstellen, wie *Projekt*, *Abteilung*, *Bereich* und *Verkäufer*.

Sie erstellen auch Einrichtungswerte für Dimensionen. Beispielsweise könnten Werte Abteilungen Ihres Unternehmens darstellen. Dimensionswerte können in einer hierarchischen Struktur eingerichtet werden, die der Struktur des Kontenplans gleicht, sodass die Daten in unterschiedlichen Granularitätsstufen aufgeschlüsselt und Untergruppen von Dimensionswerten summiert werden können. Sie können beliebig viele Dimensionen und Dimensionswerte in Ihrem Mandanten definieren und Sie können eine unbegrenzte Anzahl von Dimensionswerten für jede Dimension festlegen.

Wenn Dimensionen und Werten eingerichtet wurden, können Sie globale und Shortcut-Dimensionen auf Seite **Finanzbuchhaltungs-Einrichtung** definieren, die immer verfügbar sind, um Felder in Buch.-Blattzeilen und Belegzeilen auszuwählen, ohne zuerst die Seite **Dimensionen** öffnen zu müssen. Weitere Informationen finden Sie unter [So richten Sie globale und Shortcut-Dimensionen ein](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale Dimensionen** werden als Filter beispielsweise in Berichten und XMLports und Stapelverarbeitungen verwendet. Sie können nur zwei globale Dimensionen verwenden, also wählen Sie Dimensionen, die Sie häufig verwenden.
* **Shortcutdimensionen** sind verfügbar als Felder in Buch.-Blättern, Belegzeilen und Belegeinträgen. Sie können bis zu acht davon erstellen.  

> [!NOTE]
> Nachdem Sie eine neue Dimension in einem Eintrag verwendet haben, z. B. in einer Zeile oder einem neuen Datensatz, können Sie die Dimension nicht löschen, selbst wenn Sie den Eintrag nicht buchen. Dies ist darauf zurückzuführen, dass [!INCLUDE[prod_short](includes/prod_short.md)] sofort einen Dimensionssatz für die Zeile oder den Datensatz erstellt. Weitere Informationen finden Sie unter [Dimensionssätze](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>So richten Sie Standarddimensionen für Debitoren, Kreditoren und andere Konten ein

Sie können eine Standarddimension für ein bestimmtes Konto einrichten. Die Dimension wird in das Buch.-Blatt oder den Beleg kopiert, wenn Sie die Kontonummer auf der Zeile eingeben, aber Sie können den Code in der Zeile ändern oder löschen, falls erforderlich. Sie können eine Dimension auch erstellen, die für das Buchen eines Postens mit einem speziellen Konto benötigt wird.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Dimensionen** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Dimensionen** wählen Sie die entsprechende Dimension, und wählen die **Kontoart-Standard Dimensionswerte** Aktion aus.  
3. Füllen Sie für jede neue Vorgabedimension, die Sie einrichten möchten, eine eigene Zeile aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Wenn Sie eine Dimension zwar erforderlich machen, ihr aber keinen Standardwert zuordnen möchten, lassen Sie das Feld **Dimensionswertcode** leer, und wählen Sie im Feld **Dimensionswertbuchung** die Option **Code notwendig** aus.  

> [!WARNING]  
> Wenn ein Konto in der Stapelverarbeitung **Wechselkurs anpassen** oder **Lagerkosten in Buch.-Blatt buchen** verwendet wird, wählen Sie nicht **Code zwingend** oder  **Gleicher Code**. Diese Stapelverarbeitungen können keine Dimensionscodes verwenden.  

> [!NOTE]  
> Wenn einem Konto eine andere Vorgabedimension zugewiesen werden muss als die Vorgabedimension, die bereits für die Tabelle eingerichtet wurde, dann müssen Sie eine Vorgabedimension für dieses Konto einrichten. Die Standarddimension für das Konto ersetzt dann die Vorgabedimension für die Tabelle.  

### <a name="to-set-up-default-dimension-priorities"></a>Prioritäten für Standarddimensionen einrichten:

Unterschiedliche Kontoarten, zum Beispiel ein Debitorenkonto und ein Artikelkonto, können unterschiedliche Vorgabedimensionen eingerichtet haben. Als ein Ergebnis kann bei einem Posten mehr als eine Vorgabedimension für eine Dimension vorgeschlagen werden. Um solche Konflikte zu vermeiden, können Sie in den verschiedenen Quellen Prioritätsregeln hinterlegen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Vorgabedimension Prioritäten** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf der Seite **Standarddimensionsprioritäten** im Feld **Herkunftscode** den Herkunftscode für die Postentabelle ein, für die die Prioritäten der Vorgabedimension gelten sollen.  
3. Füllen Sie für jede Vorgabedimensionspriorität, die Sie für den ausgewählten Herkunftscode festlegen möchten, eine eigene Zeile aus.
4. Wiederholen Sie diesen Ablauf für jeden Herkunftscode, für den Sie Vorgabedimensionsprioritäten einrichten möchten.  

> [!IMPORTANT]  
> Wenn Sie zwei Tabellen mit derselben Priorität für denselben Herkunftscode einrichten, wird [!INCLUDE[prod_short](includes/prod_short.md)] immer die Tabelle mit der niedrigsten Tabellen-ID auswählen.  

### <a name="to-set-up-dimension-combinations"></a>Dimensionskombinationen einrichten:

Um das Buchen von Posten mit widersprüchlichen oder irrelevanten Dimensionen zu vermeiden, können Sie bestimmte Kombinationen von Dimensionen sperren oder einschränken. Eine gesperrte Dimensionskombination bedeutet, dass Sie, unabhängig von den Dimensionswerten, nicht beide Dimensionen auf denselben Posten buchen können. Eine beschränkte Dimensionskombination erlaubt Ihnen, beide Dimensionen auf denselben Posten zu buchen, aber nur für bestimmte Kombinationen von Dimensionswerten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Dimensionskombinationen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Dimensionenkombinationen** das Feld für die Dimensionskombination aus und dann eine der folgenden Optionen.  

    |Feld|Description|
    |----------------------------------|---------------------------------------|  
    |**Keine Einschränkungen**|Diese Dimension hat keine Einschränkungen. Alle Dimensionswerte sind erlaubt.|  
    |**Eingeschränkt**|Diese Dimensionskombination hat, abhängig von den Dimensionswerten, die Sie eingeben, Beschränkungen. Sie müssen die Einschränkungen auf der Seite **Dimensionswert Kombinationen** festlegen.|  
    |**Gesperrt**|Diese Dimensionskombination ist nicht erlaubt.|  

3. Wenn Sie die Option **Eingeschränkt** wählen, müssen Sie angeben, welche Dimensionskombinationen gesperrt sind. Hierzu aktivieren Sie das Feld, um die Dimensionskombination zu definieren.  
4. Wählen Sie anschließend die Kombination von Dimensionswerten aus, die gesperrt werden soll, und geben Sie im Feld die Option **Blockiert** an. Wenn kein Wert angegeben ist, ist die Dimensionskombination zulässig. Wiederholen Sie diesen Vorgang, um mehrere Kombinationen zu sperren.  

> [!NOTE]  
> Es werden in den Zeilen und Spalten dieselben Dimensionen angezeigt, deshalb erscheinen alle Dimensionskombinationen zweimal. [!INCLUDE[prod_short](includes/prod_short.md)]automatisch die Einstellung in beiden Feldern an. Sie können in den Feldern im linken Teil des Fensters nichts auswählen, da diese Felder in den Zeilen und Spalten dieselben Dimensionen haben.  
>
> Die gewählte Option wird erst beim Verlassen des Feldes sichtbar.  
>
> Um anstelle des Codes den Namen der Dimension anzeigen zu lassen, wählen Sie das Feld **Spaltennamen anzeigen**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>So richten Sie globale und Shortcut-Dimensionen ein

Globale und Shortcut-Dimensionen können überall in [!INCLUDE[prod_short](includes/prod_short.md)] als Filter verwendet werden, auch in Berichten, Batchaufträgen, Posten und Analyseansichten. Globale und Shortcutdimensionen können immer direkt eingefügt werden, ohne erst die Seite **Dimensionen** zu öffnen. In Buch.-Blattzeilen und Belegzeilen können Sie globale und Shortcutdimensionen in einem Feld der Zeile auswählen. Sie können zwei globale und acht Shortcutdimensionen einrichten. Wählen Sie die Dimensionen, die Sie am häufigsten verwenden.

> [!Important]  
> Das Ändern einer globalen oder Shortcutdimension erfordert, dass alle Posten, die mit der Dimension gebucht werden, aktualisiert werden. Um eine globale Dimension zu ändern, verwenden Sie die Funktion **Globale Dimensionen ändern**, aber dies kann zeitaufwändig sein und sich negativ auf die Leistung auswirken. Außerdem können Tabellen während des Updates gesperrt sein. Daher wählen Sie Ihre globalen und Shortcutdimensionen sorgfältig aus, um sie später nicht ändern zu müssen. Verwenden Sie die Aktion **Dimension ändern**, um eine Verknüpfungsdimension zu ändern. <br /><br />
> Weitere Informationen finden Sie unter [So ändern Sie globale Dimensionen](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Wenn Sie eine globale oder Shortcutdimension hinzufügen oder ändern, werden Sie automatisch abgemeldet und wieder angemeldet, damit der neuen Wert zur Verwendung in der vollständigen Anwendung vorbereitet wird.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder im Inforegister **Dimensionen** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>So ändern Sie globale Dimensionen

Wenn Sie eine globale oder Shortcutdimension ändern, werden alle mit der betreffenden Dimension gebuchten Einträge aktualisiert. Da dieser Prozess zeitaufwändig sein und die Leistung beeinträchtigen kann, stehen zwei verschiedene Modi zur Verfügung, um den Prozess an die Größe der Datenbank anzupassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Hauptbuchhaltung Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Globale Dimensionen ändern** aus.
3. Wählen Sie oben auf der Seite eine der folgenden Optionen aus, um zu definieren, in welchem Modus der Stapelverarbeitungsauftrag ausgeführt wird.

    |Option|Beschreibung|
    |-|-|
    |**Sequenziell**|(Standard) Die gesamte Dimensionsänderung wird in einer Transaktion durchgeführt, wobei alle Einträge auf die Dimensionen zurückgesetzt werden, die sie vor der Änderung hatten.<br /><br />Diese Option wird empfohlen, wenn das Unternehmen relativ wenige gebuchte Posten enthält, die am schnellsten abgeschlossen werden können. Der Prozess sperrt mehrere Tabellen und blockiert andere Benutzer, bis er abgeschlossen ist. Beachten Sie, dass der Prozess in großen Datenbanken in diesem Modus möglicherweise überhaupt nicht abgeschlossen werden kann. Verwenden Sie in diesem Fall die Option **Parallel**.|
    |**Parallel**|Die Dimensionsänderung erfolgt in mehreren Hintergrundsitzungen und der Vorgang wird in mehrere Transaktionen aufgeteilt. Um diese Option zu verwenden, aktivieren Sie die Umschaltung **Parallelverarbeitung**. <br /><br />Wir empfehlen diese Option für große Datenbanken oder Unternehmen mit vielen gebuchten Posten, die am schnellsten abgeschlossen werden können. Beachten Sie, dass bei diesem Modus der Aktualisierungsprozess nicht gestartet wird, wenn mehrere Datenbanksitzungen aktiv sind.|  

4. Geben Sie in den Feldern **Globaler Dimensionscode 1** und/oder **Globaler Dimensionscode 2** die neue(n) Dimension(en) ein. Die aktuellen Dimensionen werden hinter den Feldern grau dargestellt.
5. Führen Sie je nach Modus einen der folgenden Schritte aus:
    * Im Modus **Sequenziell** wählen Sie die **Start** Aktion.
    * Im Modus **Parallel** wählen Sie die **Vorbereiten** Aktion.

    Die Registerkarte **Protokolleinträge** enthält Informationen zu den Dimensionen, die geändert werden.
6. Melden Sie sich von [!INCLUDE[prod_short](includes/prod_short.md)] ab und dann wieder an.
7. Wählen Sie die Aktion **Start** aus, um die Parallelverarbeitung der Dimensionsänderungen zu starten. <!--is this also dependent on the mode?-->

### <a name="example-of-dimension-setup"></a>Beispiel einer Dimensionseinrichtung

Nehmen wir an, dass Ihr Unternehmen Transaktionen auf Grundlage der Organisationsstruktur und der geografische Lagen verfolgen möchte. Sie können zwei Dimensionen auf der Seite **Dimensionen** einrichten.

* **BEREICH**  
* **ABTEILUNG**  

| Code | Name | Code Caption | Filter Caption |
| --- | --- | --- | --- |
| BEREICH |Ursprungs- / Bestimmungsregion |Gebietscode |Filter "Bereich" |
| ABTEILUNG |Abteilung |Abteilungscode |Kostenstellenfilter |

Für **BEREICH** fügen Sie die folgenden Dimensionswerte hinzu:

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

Um die beiden hauptgeografischen Gebiete Amerika und Europa, fügen Sie bei Bedarf Unterkategorien für Bereiche hinzu, indem Sie die Dimensionswerte einrücken. Dadurch können Sie über Verkäufe oder Ausgaben in den Regionen berichten und Summen für die größeren geographischen Gebiete erhalten. Sie können auch wählen, dass Länder oder Regionen als Ihre Dimensionswerte oder Bundesregionen bzw. Städten gewählt werden, abhängig von Ihrem Geschäft.

> [!NOTE]  
> Um eine Hierarchie einzurichten, muss der Code in alphabetischer Reihenfolge sein. Dies umfasst die Codes der standardmäßigen Dimensionswerte in [!INCLUDE[prod_short](includes/prod_short.md)]  

Für **ABTEILUNG** fügen Sie die folgenden Dimensionswerte hinzu:

| Code | Name | Dimensionswertart |
| --- | --- | --- |
| ADMIN |Verwaltung |Standard |
| PROD |Produktion |Standard |
| VERKAUF |Verkauf |Standard |

Mit dieser Einrichtung können Sie Ihre zwei Dimensionen als zwei globalen Dimensionen auf der Seite **Finanzbuchhaltungs-Einrichtung** hinzufügen. Das bedeutet, dass globale Dimensionen als Filter für Sachposten in allen Berichten, Kontenschemata und Stapelverarbeitungen benutzt werden können. Beide globalen Dimensionen stehen auch als Shortcutdimensionen in Buch.-Blattzeilen und Belegköpfen zur Verfügung.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Eine Übersicht der Dimensionen erhalten, die mehrmals verwendet wurden

Auf der Seite **Vorgabedimensionen - Mehrfach** zeigt, wie eine Kontengruppe Dimensionswerte verwendet. Sie können dies tun, indem Sie mehrere Konten markieren und dann die Vorgabedimensionen und Dimensionswerte für alle in der Kontenübersicht markierten Konten angeben. Wenn Sie Vorgabedimensionen für die markierten Konten angeben, wird die Anwendung diese Dimensionen und Dimensionswerte immer vorschlagen, wenn eines dieser Konten angesprochen wird, z.B. in einer Buch.-Blattzeile. Dies vereinfacht das Buchen für den Anwender, da die Anwendung die Dimensionsfelder automatisch ausfüllt. Die Dimensionswerte, die die Anwendung vorschlägt, können geändert werden, z. B. in einer Buch.-Blattzeile.

Die Seite **Vorgabedimensionen - Mehrfach** enthält die folgenden Felder:

|Feld|Description|
|-----|-----------|  
|**Dimensionscode**|Zeigt alle Dimensionen an, die als Vorgabedimensionen für ein oder mehrere der markierten Konten bestimmt wurden. Indem Sie das Feld aktivieren, können Sie eine Liste aller verfügbaren Dimensionen anzeigen. Wenn Sie eine Dimension wählen und OK klicken, wird die gewählte Dimension als Vorgabedimension für alle markierten Konten bestimmt.|
|**Dimensionswertcode**|Zeigt entweder einen einzelnen Dimensionswert oder den Ausdruck (Konflikt) an. Wenn eine Dimensionswert in dem Feld angezeigt wird, dann haben alle markierten Konten denselben Vorgabedimensionswert für eine Dimension. Wenn der Ausdruck (Konflikt) in dem Feld angezeigt wird, dann haben nicht alle markierten Konten denselben Vorgabedimensionswert für eine Dimension. Durch Aktivieren dieses Felds können Sie eine Übersicht aller verfügbaren Dimensionswerte für eine Dimension einsehen. Wenn Sie einen Dimensionswert wählen und OK klicken, wird der gewählte Dimensionswert als Vorgabedimensionswert für alle markierten Konten bestimmt.|
|**Dimensionswertbuchung**|Zeigt entweder eine einzelne Dimensionswertbuchung oder den Ausdruck (Konflikt) an. Wenn eine Dimensionswertbuchungsregel in dem Feld angezeigt wird, dann haben alle markierten Konten dieselbe Dimensionswertbuchungsregel für eine Dimensionswertbuchung. Wenn der Ausdruck (Konflikt) in dem Feld angezeigt wird, dann haben nicht alle markierten Konten dieselbe Dimensionswertbuchungsregel für eine Dimensionswertbuchung. Durch Aktivieren des Felds Dimensionswertbuchung können Sie eine Übersicht der Dimensionswertbuchungsregeln einsehen. Wenn Sie eine Dimensionswertbuchungsregel auswählen und auf die AssistButton klicken, wird die gewählte Dimensionswertbuchungsregel für alle markierten Konten angewendet.|

## <a name="using-dimensions"></a>Dimensionen verwenden

In einem Beleg, z. B. einem Verkaufsauftrag, können Sie Dimensionsinformationen sowohl für eine einzelne Belegzeile als auch für den Beleg selbst hinzufügen. Sie können beispielsweise auf der Seite **Verkaufsauftrag** Dimensionswerte für die ersten beiden Shortcutdimensionen direkt in den Beleg eingeben und weitere Dimensionsinformationen hinzufügen, wenn Sie auf die Schaltfläche **Dimensionen** klicken.  

Wenn Sie stattdessen in einem Buch.-Blatt arbeiten, können Sie auf dieselbe Art und Weise Dimensionsinformationen hinzufügen, wenn Sie Shortcutdimensionen direkt als Felder in Buch.-Blattzeilen eingerichtet haben.  

Sie können Standarddimensionen für Konten oder Kontenarten festlegen, sodass Dimensionen und Dimensionswerte automatisch ausgefüllt werden.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Einsehen von Globalen Dimensionen in Postenseiten

Beachten Sie, dass globale Dimensionen immer vom Unternehmen \- definiert und benannt werden. Um die globalen Dimensionen für das Unternehmen anzuzeigen, öffnen Sie die Seite  **Finanzbuchhaltung Einrichtung**.  

Auf einer Postenseite können Sie sehen, ob für Posten globale Dimensionen vorhanden sind. Die beiden globalen Dimensionen unterscheiden sich von den anderen Dimensionen dadurch, dass Sie diese beiden Dimensionen überall in [!INCLUDE[prod_short](includes/prod_short.md)] als Filter verwenden können.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Kontenplan** die **Ressourcenposten**-Aktion aus.  
3. Setzen Sie einen oder mehrere Filter, um lediglich die relevanten Posten auf der Seite anzuzeigen.  
4. Um alle Dimensionen eines Postens anzuzeigen, wählen Sie den Posten aus, und klicken Sie auf  **Dimensionen**.  

> [!NOTE]  
> Die Seite **Postendimensionen** zeigt die Dimensionen für jeweils einen Posten. Wenn Sie sich durch die Posten bewegen, verändert sich der Inhalt der Seite **Postendimensionen** dementsprechend.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Analysieren von Daten nach Dimensionen](bi-how-analyze-data-dimension.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]