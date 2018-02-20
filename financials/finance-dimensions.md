---
title: Arbeiten mit Dimensionen | Microsoft Docs
description: "Sie können Dimensionen nutzen, um Einträge zu kategorisieren, beispielsweise nach Abteilungen oder Projekt, sodass Sie können Daten einfacher verfolgen und analysieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f9a6d577138fcffa338ce51f0abaa45c63c520f7
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

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
> Als schnelle Möglichkeit, Transaktionsdaten nach Dimensionen zu analysieren, können Sie Summen im Kostenplan und Posten in allen **Posten**-Fenstern nach Dimensionen filtern. Suchen Sie nach der Aktion **Dimensionsfilter festlegen**.

## <a name="dimension-sets"></a>Dimensionssätze
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

## <a name="setting-up-dimensions"></a>Einrichtung von Dimensionen
Sie können die Dimensionen und die Dimensionswerte, die Sie verwenden möchten, definieren, um Buch.-Blätter und Belege zu kategorisieren, wie Verkaufsaufträge und Bestellungen einrichten. Sie errichten Dimensionen im Fenster **Dimensionen**, wo Sie eine Zeile für jede Dimension erstellen, wie *Projekt*, *Abteilung*, *Bereich* und *Verkaufsperson*.

Sie erstellen auch Einrichtungswerte für Dimensionen. Beispielsweise könnten Werte Abteilungen Ihres Unternehmens darstellen. Dimensionswerte können in einer hierarchischen Struktur eingerichtet werden, die der Struktur des Kontenplans gleicht, sodass die Daten in unterschiedlichen Granularitätsstufen aufgeschlüsselt und Untergruppen von Dimensionswerten summiert werden können. Sie können beliebig viele Dimensionen und Dimensionswerte in Ihrem Mandanten definieren und Sie können eine unbegrenzte Anzahl von Dimensionswerten für jede Dimension festlegen.

Sie können mehrere globale und Shortcutdimensionen einrichten:  

* **Globale Dimensionen** werden als Filter (beispielsweise in Berichten und Stapelverarbeitungen verwendet). Sie können nur zwei globale Dimensionen verwenden, also wählen Sie Dimensionen, die Sie häufig verwenden.
* **Shortcutdimensionen** sind verfügbar als Felder in Buch.-Blattzeilen und Belegzeilen. Sie können bis zu sechs davon erstellen.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Standarddimensionen für Debitoren, Kreditoren und andere Konten einrichten
Sie können eine Standarddimension für ein bestimmtes Konto einrichten. Die Dimension wird in das Buch.-Blatt oder den Beleg kopiert, wenn Sie die Kontonummer auf der Zeile eingeben, aber Sie können den Code in der Zeile ändern oder löschen, falls erforderlich. Sie können eine Dimension auch erstellen, die für das Buchen eines Postens mit einem speziellen Konto benötigt wird.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Dimensionen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Im Fenster **Dimensionen** wählen Sie die entsprechende Dimension, und wählen die **Kontoart-Standard Dimensionswerte** Aktion aus.  
4.  Füllen Sie für jede neue Vorgabedimension, die Sie einrichten möchten, eine eigene Zeile aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Wenn Sie eine Dimension zwar erforderlich machen, ihr aber keinen Standardwert zuordnen möchten, lassen Sie das Feld **Dimensionswertcode** leer, und wählen Sie im Feld **Dimensionswertbuchung** die Option **Code notwendig** aus.  

> [!WARNING]  
>  Wenn ein Konto in der Stapelverarbeitung **Wechselkurs anpassen** oder **Lagerkosten in Buch.-Blatt buchen** verwendet wird, wählen Sie nicht **Code zwingend** oder  **Gleicher Code**. Diese Stapelverarbeitungen können keine Dimensionscodes verwenden.  

> [!NOTE]  
>  Wenn einem Konto eine andere Vorgabedimension zugewiesen werden muss als die Vorgabedimension, die bereits für die Tabelle eingerichtet wurde, dann müssen Sie eine Vorgabedimension für dieses Konto einrichten. Die Vorgabedimension für das einzelne Konto ersetzt dann die Vorgabedimension für die Tabelle.  

### <a name="to-set-up-default-dimension-priorities"></a>Prioritäten für Standarddimensionen einrichten:  
Unterschiedliche Kontoarten, zum Beispiel ein Debitorenkonto und ein Artikelkonto, können unterschiedliche Vorgabedimensionen eingerichtet haben. Als ein Ergebnis kann bei einem Posten mehr als eine Vorgabedimension für eine Dimension vorgeschlagen werden. Um solche Konflikte zu vermeiden, können Sie in den verschiedenen Quellen Prioritätsregeln hinterlegen.  

1.  Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Symbol Seite oder Bericht suchen") und geben **Standard-Dimensionsprioritäten** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Geben Sie im Fenster **Standarddimensionsprioritäten** im Feld **Herkunftscode** den Herkunftscode für die Postentabelle ein, für die die Prioritäten der Vorgabedimension gelten sollen.  
3.  Füllen Sie für jede Vorgabedimensionspriorität, die Sie für den ausgewählten Herkunftscode festlegen möchten, eine eigene Zeile aus.
4.  Wiederholen Sie diesen Ablauf für jeden Herkunftscode, für den Sie Vorgabedimensionsprioritäten einrichten möchten.  

> [!IMPORTANT]  
>  Wenn Sie zwei Tabellen mit derselben Priorität für denselben Herkunftscode einrichten, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] immer die Tabelle mit der niedrigsten Tabellen-ID auswählen.  

### <a name="to-set-up-dimension-combinations"></a>Dimensionskombinationen einrichten:  
Um das Buchen von Posten mit widersprüchlichen oder irrelevanten Dimensionen zu vermeiden, können Sie bestimmte Kombinationen von Dimensionen sperren oder einschränken. Eine gesperrte Dimensionskombination bedeutet, dass Sie, unabhängig von den Dimensionswerten, nicht beide Dimensionen auf denselben Posten buchen können. Eine beschränkte Dimensionskombination erlaubt Ihnen, beide Dimensionen auf denselben Posten zu buchen, aber nur für bestimmte Kombinationen von Dimensionswerten.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Dimensionen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Dimensionenkombinationen** das Feld für die Dimensionskombination aus und dann eine der folgenden Optionen.  

    |Feld|Description|
    |----------------------------------|---------------------------------------|  
    |**Keine Einschränkungen**|Diese Dimension hat keine Einschränkungen. Alle Dimensionswerte sind erlaubt.|  
    |**Eingeschränkt**|Diese Dimensionskombination hat, abhängig von den Dimensionswerten, die Sie eingeben, Beschränkungen. Sie müssen die Einschränkungen im Fenster **Dimensionswert Kombinationen** festlegen.|  
    |**Gesperrt**|Diese Dimensionskombination ist nicht erlaubt.|  

3.  Wenn Sie die Option **Eingeschränkt** wählen, müssen Sie angeben, welche Dimensionskombinationen gesperrt sind. Hierzu aktivieren Sie das Feld, um die Dimensionskombination zu definieren.  
4.  Wählen Sie anschließend die Kombination von Dimensionswerten aus, die gesperrt werden soll, und geben Sie im Feld die Option **Blockiert** an. Wenn kein Wert angegeben ist, ist die Dimensionskombination zulässig. Wiederholen Sie diesen Vorgang, um mehrere Kombinationen zu sperren.  

> [!NOTE]  
>  Es werden in den Zeilen und Spalten dieselben Dimensionen angezeigt, deshalb erscheinen alle Dimensionskombinationen zweimal. [!INCLUDE[d365fin](includes/d365fin_md.md)]automatisch die Einstellung in beiden Feldern an. Sie können in den Feldern im linken Teil des Fensters nichts auswählen, da diese Felder in den Zeilen und Spalten dieselben Dimensionen haben.  
>   
>  Die gewählte Option wird erst beim Verlassen des Feldes sichtbar.  
>   
>  Um anstelle des Codes den Namen der Dimension anzeigen zu lassen, wählen Sie das Feld **Spaltennamen anzeigen**.

### <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Eine Übersicht der Dimensionen erhalten, die mehrmals verwendet wurden
Das Fenster **Vorgabedimensionen - Mehrfach** zeigt, wie eine Kontengruppe Dimensionswerte verwendet. Sie können dies tun, indem Sie mehrere Konten markieren und dann die Vorgabedimensionen und Dimensionswerte für alle in der Kontenübersicht markierten Konten angeben. Wenn Sie Vorgabedimensionen für die markierten Konten angeben, wird die Anwendung diese Dimensionen und Dimensionswerte immer vorschlagen, wenn eines dieser Konten angesprochen wird, z. B. in einer Buch.-Blattzeile. Dies vereinfacht das Buchen für den Anwender, da die Anwendung die Dimensionsfelder automatisch ausfüllt. Die Dimensionswerte, die die Anwendung vorschlägt, können geändert werden, z. B. in einer Buch.-Blattzeile.

Das Fenster **Vorgabedimensionen - Mehrfach** enthält die folgenden Felder:
|Feld|Description|
|----------------------------------|---------------------------------------|  
|**Dimensionscode**|Zeigt alle Dimensionen an, die als Vorgabedimensionen für ein oder mehrere der markierten Konten bestimmt wurden. Indem Sie das Feld aktivieren, können Sie eine Liste aller verfügbaren Dimensionen anzeigen. Wenn Sie eine Dimension wählen und OK klicken, wird die gewählte Dimension als Vorgabedimension für alle markierten Konten bestimmt.|
|**Dimensionswertcode**|Zeigt entweder einen einzelnen Dimensionswert oder den Ausdruck (Konflikt) an. Wenn eine Dimensionswert in dem Feld angezeigt wird, dann haben alle markierten Konten denselben Vorgabedimensionswert für eine Dimension. Wenn der Ausdruck (Konflikt) in dem Feld angezeigt wird, dann haben nicht alle markierten Konten denselben Vorgabedimensionswert für eine Dimension. Durch Aktivieren dieses Felds können Sie eine Übersicht aller verfügbaren Dimensionswerte für eine Dimension einsehen. Wenn Sie einen Dimensionswert wählen und OK klicken, wird der gewählte Dimensionswert als Vorgabedimensionswert für alle markierten Konten bestimmt.|
|**Dimensionswertbuchung**|Zeigt entweder eine einzelne Dimensionswertbuchung oder den Ausdruck (Konflikt) an. Wenn eine Dimensionswertbuchungsregel in dem Feld angezeigt wird, dann haben alle markierten Konten dieselbe Dimensionswertbuchungsregel für eine Dimensionswertbuchung. Wenn der Ausdruck (Konflikt) in dem Feld angezeigt wird, dann haben nicht alle markierten Konten dieselbe Dimensionswertbuchungsregel für eine Dimensionswertbuchung. Durch Aktivieren des Felds Dimensionswertbuchung können Sie eine Übersicht der Dimensionswertbuchungsregeln einsehen. Wenn Sie eine Dimensionswertbuchungsregel auswählen und auf die AssistButton klicken, wird die gewählte Dimensionswertbuchungsregel für alle markierten Konten angewendet.|

### <a name="example-of-dimension-setup"></a>Beispiel einer Dimensionseinrichtung
Nehmen wir an, dass Ihr Unternehmen Transaktionen auf Grundlage der Organisationsstruktur und der geografische Lagen verfolgen möchte. Sie können zwei Dimensionen im Fenster **Dimensionen** einrichten.

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
| 2.0 |Nordamerika |Standard |
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

Mit dieser Einrichtung fügen Sie dann Ihre zwei Dimensionen als zwei globalen Dimensionen im Fenster **Finanzbuchhaltung Einrichtung** hinzu. Das bedeutet, dass globale Dimensionen als Filter für Sachposten in allen Berichten, Kontenschemata und Stapelverarbeitungen benutzt werden können. Beide globalen Dimensionen stehen auch als Shortcutdimensionen in Buch.-Blattzeilen und Belegköpfen zur Verfügung.  

## <a name="using-dimensions"></a>Dimensionen verwenden
In einem Beleg, z. B. einem Verkaufsauftrag, können Sie Dimensionsinformationen sowohl für eine einzelne Belegzeile als auch für den Beleg selbst hinzufügen. Sie können beispielsweise im Fenster **Verkaufsauftrag** Dimensionswerte für die ersten beiden Shortcutdimensionen direkt in den Beleg eingeben und weitere Dimensionsinformationen hinzufügen, wenn Sie auf die Schaltfläche **Dimensionen** klicken.  

Wenn Sie stattdessen in einem Buch.-Blatt arbeiten, können Sie auf dieselbe Art und Weise Dimensionsinformationen hinzufügen, wenn Sie Shortcutdimensionen direkt als Felder in Buch.-Blattzeilen eingerichtet haben.  

Sie können Standarddimensionen für Konten oder Kontenarten festlegen, sodass Dimensionen und Dimensionswerte automatisch ausgefüllt werden.

## <a name="to-view-global-dimensions-in-ledger-entry-windows"></a>Globale Dimensionen in Postenfenstern anzeigen:  
Beachten Sie, dass globale Dimensionen immer vom Unternehmen \- definiert und benannt werden. Um die globalen Dimensionen für das Unternehmen anzuzeigen, öffnen Sie das Fenster  **Finanzbuchhaltung Einrichtung**.  

In einem Postenfenster können Sie sehen, ob für Posten globale Dimensionen vorhanden sind. Die beiden globalen Dimensionen unterscheiden sich von den anderen Dimensionen dadurch, dass Sie diese beiden Dimensionen überall in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Filter verwenden können.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Fenster **Kontenplan** die **Ressourcenposten**-Aktion aus.  
3.  Setzen Sie einen oder mehrere Filter, um lediglich die relevanten Posten anzuzeigen.  
4.  Um alle Dimensionen eines Postens anzuzeigen, wählen Sie den Posten aus, und klicken Sie auf  **Dimensionen**.  

> [!NOTE]  
>  Das Fenster **Postendimensionen** zeigt die Dimensionen für jeweils einen Posten. Wenn Sie sich durch die Posten bewegen, verändert sich der Inhalt des Fensters **Postendimensionen** dementsprechend.  

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Analysieren von Daten nach Dimensionen](bi-how-analyze-data-dimension.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

