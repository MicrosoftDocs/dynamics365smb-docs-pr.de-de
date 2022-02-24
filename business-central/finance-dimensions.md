---
title: Arbeiten mit Dimensionen | Microsoft Docs
description: Sie können Dimensionen nutzen, um Einträge zu kategorisieren, beispielsweise nach Abteilungen oder Projekt, sodass Sie können Daten einfacher verfolgen und analysieren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 04/14/2020
ms.author: sgroespe
ms.openlocfilehash: d353381c9267e9039d0b4391aa7fdac1c8a3c405
ms.sourcegitcommit: 8a4e66f7fc8f9ef8bdf34595e0d3983df4749376
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262166"
---
# <a name="working-with-dimensions"></a>Arbeiten mit Dimensionen
Um Analyse in Belegen wie Verkaufsaufträgen einfacher durchzuführen, können Sie Dimensionen verwenden. Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie verfolgen und analysieren können. So können Sie beispielsweise Dimensionen einrichten, mit denen angegeben wird, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Dies ermöglicht die Verwendung von Dimensionen anstelle der Einrichtung separater Sachkonten für einzelne Abteilungen und Projekte. Kennzeichnet eine umfangreiche Verkaufschance zur Analyse, ohne dazu einen komplizierten Kontenplan zu erstellen. Weitere Informationen finden Sie unter [Business Intelligence](bi.md).

Oder Sie richten beispielsweise eine Dimension mit dem Namen *Abteilung* ein und verwenden diese Dimension und einen Dimensionswert, wenn Sie Verkaufsbelege buchen. Dadurch können Sie auch intelligente Geschäfts-Tools verwenden, um zu sehen, welche Abteilung die Artikel verkauft hat.
Je mehr Dimensionen Sie einrichten und verwenden, auf desto detaillierteren Berichten können Sie Ihre Geschäftsentscheidungen basieren. Zum Beispiel kann ein einzelner Verkaufsposten mehrere Dimensionsinformationen enthalten, wie:  

* Das Konto, auf das der Artikelverkauf gebucht wurde  
* Wo der Artikel verkauft wurde
* Wer ihn verkauft hat
* Die Art des Debitors, die ihn kaufte  

## <a name="analyzing-by-dimensions"></a>Nach Dimensionen analysieren
Die Funktionalität Dimensionen wird eine wichtige Rolle in der Business Intelligence spielen, wie auch beim Definieren von Analyseansichten. Weitere Informationen finden Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

> [!TIP]
> Als schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, können Sie Summen im Kostenplan und Posten in allen **Posten**-Seiten nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.

## <a name="dimension-sets"></a>Dimensionssätze
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

## <a name="setting-up-dimensions"></a>Einrichtung von Dimensionen
Sie können die Dimensionen und die Dimensionswerte, die Sie verwenden möchten, definieren, um Buch.-Blätter und Belege zu kategorisieren, wie Verkaufsaufträge und Bestellungen einrichten. Sie errichten Dimensionen auf der Seite **Dimensionen**, wo Sie eine Zeile für jede Dimension erstellen, wie *Projekt*, *Abteilung*, *Bereich* und *Verkäufer*.

Sie erstellen auch Einrichtungswerte für Dimensionen. Beispielsweise könnten Werte Abteilungen Ihres Unternehmens darstellen. Dimensionswerte können in einer hierarchischen Struktur eingerichtet werden, die der Struktur des Kontenplans gleicht, sodass die Daten in unterschiedlichen Granularitätsstufen aufgeschlüsselt und Untergruppen von Dimensionswerten summiert werden können. Sie können beliebig viele Dimensionen und Dimensionswerte in Ihrem Mandanten definieren und Sie können eine unbegrenzte Anzahl von Dimensionswerten für jede Dimension festlegen.

Wenn Dimensionen und Werten eingerichtet wurden, können Sie globale und Shortcut-Dimensionen auf Seite **Finanzbuchhaltungs-Einrichtung** definieren, die immer verfügbar sind, um Felder in Buch.-Blattzeilen und Belegzeilen auszuwählen, ohne zuerst die Seite **Dimensionen** öffnen zu müssen. Weitere Informationen finden Sie unter [So richten Sie globale und Shortcut-Dimensionen ein](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale Dimensionen** werden als Filter beispielsweise in Berichten und XMLports und Stapelverarbeitungen verwendet. Sie können nur zwei globale Dimensionen verwenden, also wählen Sie Dimensionen, die Sie häufig verwenden.
* **Shortcutdimensionen** sind verfügbar als Felder in Buch.-Blattzeilen und Belegzeilen. Sie können bis zu sechs davon erstellen.  

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>So richten Sie Standarddimensionen für Debitoren, Kreditoren und andere Konten ein
Sie können eine Standarddimension für ein bestimmtes Konto einrichten. Die Dimension wird in das Buch.-Blatt oder den Beleg kopiert, wenn Sie die Kontonummer auf der Zeile eingeben, aber Sie können den Code in der Zeile ändern oder löschen, falls erforderlich. Sie können eine Dimension auch erstellen, die für das Buchen eines Postens mit einem speziellen Konto benötigt wird.  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Dimensionen** ein und wählen Sie dann den entsprechenden Link.  
2.  Auf der Seite **Dimensionen** wählen Sie die entsprechende Dimension, und wählen die **Kontoart-Standard Dimensionswerte** Aktion aus.  
4.  Füllen Sie für jede neue Vorgabedimension, die Sie einrichten möchten, eine eigene Zeile aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Wenn Sie eine Dimension zwar erforderlich machen, ihr aber keinen Standardwert zuordnen möchten, lassen Sie das Feld **Dimensionswertcode** leer, und wählen Sie im Feld **Dimensionswertbuchung** die Option **Code notwendig** aus.  

> [!WARNING]  
>  Wenn ein Konto in der Stapelverarbeitung **Wechselkurs anpassen** oder **Lagerkosten in Buch.-Blatt buchen** verwendet wird, wählen Sie nicht **Code zwingend** oder  **Gleicher Code**. Diese Stapelverarbeitungen können keine Dimensionscodes verwenden.  

> [!NOTE]  
>  Wenn einem Konto eine andere Vorgabedimension zugewiesen werden muss als die Vorgabedimension, die bereits für die Tabelle eingerichtet wurde, dann müssen Sie eine Vorgabedimension für dieses Konto einrichten. Die Vorgabedimension für das einzelne Konto ersetzt dann die Vorgabedimension für die Tabelle.  

### <a name="to-set-up-default-dimension-priorities"></a>Prioritäten für Standarddimensionen einrichten:  
Unterschiedliche Kontoarten, zum Beispiel ein Debitorenkonto und ein Artikelkonto, können unterschiedliche Vorgabedimensionen eingerichtet haben. Als ein Ergebnis kann bei einem Posten mehr als eine Vorgabedimension für eine Dimension vorgeschlagen werden. Um solche Konflikte zu vermeiden, können Sie in den verschiedenen Quellen Prioritätsregeln hinterlegen.  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Dimensionseigenschaften** ein und wählen Sie dann den entsprechenden Link.  
2.  Geben Sie auf der Seite **Standarddimensionsprioritäten** im Feld **Herkunftscode** den Herkunftscode für die Postentabelle ein, für die die Prioritäten der Vorgabedimension gelten sollen.  
3.  Füllen Sie für jede Vorgabedimensionspriorität, die Sie für den ausgewählten Herkunftscode festlegen möchten, eine eigene Zeile aus.
4.  Wiederholen Sie diesen Ablauf für jeden Herkunftscode, für den Sie Vorgabedimensionsprioritäten einrichten möchten.  

> [!IMPORTANT]  
>  Wenn Sie zwei Tabellen mit derselben Priorität für denselben Herkunftscode einrichten, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] immer die Tabelle mit der niedrigsten Tabellen-ID auswählen.  

### <a name="to-set-up-dimension-combinations"></a>Dimensionskombinationen einrichten:  
Um das Buchen von Posten mit widersprüchlichen oder irrelevanten Dimensionen zu vermeiden, können Sie bestimmte Kombinationen von Dimensionen sperren oder einschränken. Eine gesperrte Dimensionskombination bedeutet, dass Sie, unabhängig von den Dimensionswerten, nicht beide Dimensionen auf denselben Posten buchen können. Eine beschränkte Dimensionskombination erlaubt Ihnen, beide Dimensionen auf denselben Posten zu buchen, aber nur für bestimmte Kombinationen von Dimensionswerten.

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Dimensionskombinationen** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **Dimensionenkombinationen** das Feld für die Dimensionskombination aus und dann eine der folgenden Optionen.  

    |Feld|Description|
    |----------------------------------|---------------------------------------|  
    |**Keine Einschränkungen**|Diese Dimension hat keine Einschränkungen. Alle Dimensionswerte sind erlaubt.|  
    |**Eingeschränkt**|Diese Dimensionskombination hat, abhängig von den Dimensionswerten, die Sie eingeben, Beschränkungen. Sie müssen die Einschränkungen auf der Seite **Dimensionswert Kombinationen** festlegen.|  
    |**Gesperrt**|Diese Dimensionskombination ist nicht erlaubt.|  

3.  Wenn Sie die Option **Eingeschränkt** wählen, müssen Sie angeben, welche Dimensionskombinationen gesperrt sind. Hierzu aktivieren Sie das Feld, um die Dimensionskombination zu definieren.  
4.  Wählen Sie anschließend die Kombination von Dimensionswerten aus, die gesperrt werden soll, und geben Sie im Feld die Option **Blockiert** an. Wenn kein Wert angegeben ist, ist die Dimensionskombination zulässig. Wiederholen Sie diesen Vorgang, um mehrere Kombinationen zu sperren.  

> [!NOTE]  
>  Es werden in den Zeilen und Spalten dieselben Dimensionen angezeigt, deshalb erscheinen alle Dimensionskombinationen zweimal. [!INCLUDE[d365fin](includes/d365fin_md.md)]automatisch die Einstellung in beiden Feldern an. Sie können in den Feldern im linken Teil des Fensters nichts auswählen, da diese Felder in den Zeilen und Spalten dieselben Dimensionen haben.  
>   
>  Die gewählte Option wird erst beim Verlassen des Feldes sichtbar.  
>   
>  Um anstelle des Codes den Namen der Dimension anzeigen zu lassen, wählen Sie das Feld **Spaltennamen anzeigen**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a>So richten Sie globale und Shortcut-Dimensionen ein
Globale und Shortcut-Dimensionen können überall in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Filter verwendet werden, auch in Berichten, Batchaufträgen und Analyseansichten. Globale und Shortcutdimensionen können immer direkt eingefügt werden, ohne erst die Seite **Dimensionen** zu öffnen. In Buch.-Blattzeilen und Belegzeilen können Sie globale und Shortcutdimensionen in einem Feld der Zeile auswählen. Sie können zwei globale und acht Shortcutdimensionen einrichten. Wählen Sie die Dimensionen, die Sie am häufigsten verwenden.

> [!Important]  
> Das Ändern einer globalen oder Shortcutdimension erfordert, dass alle Posten, die mit der Dimension gebucht werden, aktualisiert werden. Diese Aufgabe können Sie mit der Funktion **Globale Dimensionen ändern** ausführen, aber dies kann zeitaufwändig sein und sich negativ auf die Leistung auswirken. Außerdem können Tabellen während des Updates gesperrt sein. Daher wählen Sie Ihre globalen und Shortcutdimensionen sorgfältig aus, um sie später nicht ändern zu müssen. <br /><br />
> Weitere Informationen finden Sie unter [So ändern Sie globale Dimensionen](finance-dimensions.md#to-change-global-dimensions).

> [!Note]
> Wenn Sie eine globale oder Shortcutdimension hinzufügen oder ändern, werden Sie automatisch abgemeldet und wieder angemeldet, damit der neuen Wert zur Verwendung in der vollständigen Anwendung vorbereitet wird.

1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Finanzbuchhaltungs-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder im Inforegister **Dimensionen** aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a>So ändern Sie globale Dimensionen
Wenn Sie eine globale oder Shortcutdimension ändern, werden alle mit der betreffenden Dimension gebuchten Einträge aktualisiert. Da dieser Prozess zeitaufwändig sein und die Leistung beeinträchtigen kann, stehen zwei verschiedene Modi zur Verfügung, um den Prozess an die Größe der Datenbank anzupassen.  

1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Tell Me-Funktion"), geben Sie **Finanzbuchhaltungs-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Globale Dimensionen ändern** aus.
3. Wählen Sie oben auf der Seite eine der folgenden Optionen aus, um zu definieren, in welchem Modus der Stapelverarbeitungsauftrag ausgeführt wird.

    |Option|Beschreibung|
    |-|-|
    |**Sequenziell**|(Standard) Die gesamte Dimensionsänderung wird in einer Transaktion durchgeführt, wobei alle Einträge auf die Dimensionen zurückgesetzt werden, die sie vor der Änderung hatten.<br /><br />Diese Option wird empfohlen, wenn das Unternehmen relativ wenige gebuchte Posten enthält, die am schnellsten abgeschlossen werden können. Der Prozess sperrt mehrere Tabellen und blockiert andere Benutzer, bis er abgeschlossen ist. Beachten Sie, dass der Prozess in großen Datenbanken in diesem Modus möglicherweise überhaupt nicht abgeschlossen werden kann. Verwenden Sie in diesem Fall die Option **Parallel**.|
    |**Parallel**|(Aktivieren Sie das Kontrollkästchen **Parallele Verarbeitung**.) Die Dimensionsänderung erfolgt in mehreren Hintergrundsitzungen, und der Vorgang wird in mehrere Transaktionen aufgeteilt.<br /><br />Diese Option wird für große Datenbanken oder Unternehmen mit vielen gebuchten Posten empfohlen, die am schnellsten abgeschlossen werden können. Beachten Sie, dass bei diesem Modus der Aktualisierungsprozess nicht gestartet wird, wenn mehrere Datenbanksitzungen aktiv sind.|  

4. Geben Sie in den Feldern **Globaler Dimensionscode 1** und/oder **Globaler Dimensionscode 2** die neue(n) Dimension(en) ein. Die aktuellen Dimensionen werden hinter den Feldern grau dargestellt.
5. Wenn Sie den Modus **Sequenziell** ausgewählt haben, wählen Sie die Aktion **Start** aus.
6. Wenn Sie den Modus **Parallel** ausgewählt haben, wählen Sie die Aktion **Vorbereiten** aus.

    Die Registerkarte **Protokolleinträge** enthält Informationen zu den Dimensionen, die geändert werden.
7. Melden Sie sich von [!INCLUDE[d365fin](includes/d365fin_md.md)] ab und dann wieder an.
8. Wählen Sie die Aktion **Start** aus, um die Parallelverarbeitung der Dimensionsänderungen zu starten.

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
>   Um eine Hierarchie einzurichten, muss der Code in alphabetischer Reihenfolge sein. Dies umfasst die Codes der standardmäßigen Dimensionswerte in [!INCLUDE[d365fin](includes/d365fin_md.md)]  

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

Auf einer Postenseite können Sie sehen, ob für Posten globale Dimensionen vorhanden sind. Die beiden globalen Dimensionen unterscheiden sich von den anderen Dimensionen dadurch, dass Sie diese beiden Dimensionen überall in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Filter verwenden können.  

1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie auf der Seite **Kontenplan** die **Ressourcenposten**-Aktion aus.  
3.  Setzen Sie einen oder mehrere Filter, um lediglich die relevanten Posten auf der Seite anzuzeigen.  
4.  Um alle Dimensionen eines Postens anzuzeigen, wählen Sie den Posten aus, und klicken Sie auf  **Dimensionen**.  

> [!NOTE]  
>  Die Seite **Postendimensionen** zeigt die Dimensionen für jeweils einen Posten. Wenn Sie sich durch die Posten bewegen, verändert sich der Inhalt der Seite **Postendimensionen** dementsprechend.

## <a name="troubleshooting-dimensions-errors"></a>Beheben von Dimensionsfehlern
Wenn Sie Belege oder Buch.-Blattzeilen buchen, die Dimensionen enthalten, treten möglicherweise unterschiedliche Fehler auf, die in der Regel auf eine falsche Dimensionseinrichtung oder Zuweisung zurückgehen.

> [!NOTE]
> In der folgenden Liste der möglichen Fehlermeldungen stehen die *%X*-Codes als Ersatzzeichen für die Datenvariablen, die abhängig vom Kontext in der eigentlichen Nachricht in der Benutzeroberfläche enthalten sind. Beispielsweise könnte *%1 %2 ist blockiert.* in der Benutzeroberfläche als "Dimensionscode BEREICH blockiert" angezeigt werden.  

|Problem|Fehlermeldung|Mögliche Lösung|
|-----|-------------|-----------------|
|Blockierte Dimension|%1 %2 ist blockiert.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der blockierten Dimension enthalten und heben Sie die Blockierung auf.<br />- Entfernen Sie die Dimensionssatzposition für die blockierte Dimension.|
|Gelöschte Dimension|%1 %2 kann nicht gefunden werden.|-Erstellen Sie die fehlende Dimension neu.<br />- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der fehlenden Dimension enthalten und fügen Sie sie hinzu.<br />- Entfernen Sie die Dimensionssatzposition für die fehlende Dimension.|
|Blockierter Dimensionswert|%1 %2 - %3 ist gesperrt.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit dem blockierten Dimensionswert enthalten und heben Sie die Blockierung auf.<br />- Entfernen Sie die Dimensionssatzposition für den blockierten Dimensionswert.|
|Gelöschter Dimensionswert|   %1 für %2 fehlt.|-Erstellen Sie den fehlenden Dimensionswert neu.<br />- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit dem fehlenden Dimensionswert enthalten und fügen Sie ihn hinzu.<br />- Entfernen Sie die Dimensionssatzposition für den fehlenden Dimensionswert.|
|Nicht zugelassener Dimensionswert|Dimensionswerttyp für %1 %2 – %3 darf nicht %4 sein.|- Ändern Sie das Feld **Dimensionswerttyp** auf der Seite **Dimensionswerte** zu **Standard** oder **Von-Summe**.<br />- Entfernen Sie die Dimensionssatzposition für den blockierten Dimensionswert.|
|Blockierte Dimensionskombination|Dimensionen %1 und %2 können nicht gleichzeitig verwendet werden.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der blockierten Dimensionskombination enthalten und heben Sie die Blockierung auf.<br />- Ändern Sie eine der konfliktverursachenden Berechtigungssatzzeilen für die Dimensionskombination.|
|Blockierte Dimensionswertkombination|Dimensionskombinationen %1 - %2 und %3 - %4 können nicht gleichzeitig verwendet werden.|- Suchen Sie nicht gebuchte Belege, die den Dimensionssatz mit der blockierten Dimensionswertkombination enthalten und heben Sie die Blockierung auf.<br />- Ändern Sie eine der konfliktverursachenden Berechtigungssatzzeilen für die Dimensionswertkombination.|
|Leerer Dimensionswertcode für Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Code notwendig** enthält.|-Wählen Sie einen %1 für den %2 %3 aus.<br />-Wählen Sie einen %1 für den %2 %3 für %4 %5 aus.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />-Geben Sie einen nicht leeren Dimensionswert für die widersprüchliche Dimension in den Dimensionssatz ein.|
|Falscher Dimensionswertcode für Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Gleicher Code** enthält.|-Wählen Sie einen %1 %2 für den %3 %4 aus.<br />-Wählen Sie einen %1 %2 für den %3 %4 für %5 %6 aus.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />-Geben Sie den erforderlichen Dimensionswert für die widersprüchliche Dimension in den Dimensionssatz ein.|
|Nicht leerer Dimensionswertcode für leere Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Gleicher Code** enthält.|-%1 %2 muss leer sein.<br />-%1 %2 muss für %3 %4 leer sein.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />-Geben Sie einen leeren Dimensionswertcode für die widersprüchliche Dimension in den Dimensionssatz ein.|
|Unerwarteter Dimensionswert für Vorgabedimension, bei der das Feld **Wertbuchung** die Angabe **Kein Code** enthält.|-%1 %2 darf nicht angegeben werden.<br />-%1 %2 darf für %3 %4 nicht angegeben werden.|-Ändern Sie das Feld **Wertbuchung** auf der Seite **Vorgabedimension**.<br />- Entfernen Sie die widersprüchliche Zeile aus dem Dimensionssatz.|

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Analysieren von Daten nach Dimensionen](bi-how-analyze-data-dimension.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
