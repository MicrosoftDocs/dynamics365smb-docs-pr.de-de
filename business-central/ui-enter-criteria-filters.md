---
title: Sortieren, Durchsuchen und Filtern von Listen | Microsoft Docs
description: Arbeiten Sie effizient in Listen, indem Sie in Ihren Daten suchen, Spalten sortieren und Ergebnis unter Verwendung der leistungsstarken Filtersymbole und Tastenkombinationen neu definieren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: c6eb9465d07b702e545347cad5acf0a42f01d1de
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799007"
---
# <a name="sorting-searching-and-filtering-lists"></a>Sortieren, Durchsuchen und Filtern von Listen
Es gibt mehrere Möglichkeiten, wie Sie das tun können und die dabei helfen, Datensätze in einer Liste zu scannen, zu suchen und einzugrenzen. Diese umfassen die Sortierung, Suche und Filterung. Sie können einige oder alle davon gleichzeitig anwenden, um die Daten schnell zu finden oder zu analysieren.

> [!TIP]
> Wenn Sie Ihre Daten als Kacheln anzeigen, können Sie grundlegender Filterung verwenden und entsprechend suchen. Um den gesamten Satz der leistungsstarken Funktionen zum Sortieren, Suchen und Filtern zu verwenden, wählen Sie ![Anzeigen als Liste](media/ui_show_as_list_icon.png "Anzeigen als Listenpfeil links")- Symbol aus, um ihn als Liste anzuzeigen.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortieren
Dank der Sortierfunktion können Sie sich schnell und einfach einen Überblick über Ihre Daten verschaffen. Wenn Sie beispielsweise über zahlreiche Debitorenkontakte verfügen, können Sie auswählen, um nach folgenden Kriterien zu sortieren: **Debitorennummer**, **Debitorenbuchungsgruppe**, **Währungscode**, **Länder-/Regionscode** oder **Verkaufssteuer-Registrierung**, um die gewünschte Übersicht zu erhalten.

Um eine Liste zu sortieren, können Sie entweder eine Spaltenüberschrift auswählen, um zwischen aufsteigender und absteigender Reihenfolge umzuschalten, oder den kleinen Pfeil-nach-Unten auswählen und **Aufsteigend** oder **Absteigend** wählen.  

> [!NOTE]  
>   Sortierung wird nicht auf Bilder, BLOB-Felder und FlowFilter unterstützt, die keiner Tabelle angehören.  

## <a name="searching"></a>Suchen
<!--## Searching by using the Quick Filter --> Am Anfang jeder Liste befindet sich ein ![Suchliste](media/ui-search/search-list.png "Suchenlistensymbol") **Suchen**-Symbol, das eine schnelle und einfache Möglichkeit bietet, die Datensätze in einer Liste zu verringern und nur die Datensätze mit den Daten anzuzeigen, die Sie anzeigen möchten.

Zur Suche wählen Sie einfach das Suchsymbol aus und geben dann im Feld den Text ein, nach dem Sie suchen. Sie können Buchstaben, Ziffern und andere Symbole eingeben.

### <a name="fine-tune-the-search"></a>Abstimmen der Suche
Grundsätzlich versucht die Suche Treffer im Text aller Feldern zu finden. Dabei werden zwischen groß und klein geschriebene Zeichen nicht unterschieden (d. h., die Groß-/Kleinschreibung wird nicht beachtet). Text an jeder Stelle im Feld (am Anfang, am Ende oder in der Mitte) wird durchsucht.

Sie können jedoch eine genauere Suche vornehmen, indem Sie die folgenden Sonderzeichen verwenden:

- Um nur Feldwerte zu finden, die dem gesamten Text und der Groß- und Kleinschreibung genau entsprechen, setzen Sie den Text in einfache Anführungszeichen `''` (z. B. `'man'`).

- Um nur Feldwerte zu finden, die mit einem bestimmten Text beginnen und der Groß- und Kleinschreibung entsprechen, setzen Sie `*` hinter den Text (z. B. `man*`).

- Um nur Feldwerte zu finden, die mit einem bestimmten Text enden und der Groß- und Kleinschreibung entsprechen, setzen Sie `*` vor den Text (z. B. `*man`).

- Bei der Anwendung von `''` oder `*` wird die Groß-/Kleinschreibung berücksichtigt. Wenn bei der Suche die Groß-/Kleinschreibung nicht beachtet werden soll, setzten Sie ein `@` vor der Suchtext (zum Beispiel `@man*`).

Die folgende Tabelle enthält einige Beispiele, um zu erläutern, wie Sie die Suche verwenden können.


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|Suchkriterien|Findet…|
|---------------|----------|
|`man`<br />oder <br />`Man`|Alle Datensätze mit Feldern, die den Text **man** enthalten, unabhängig der Groß-/Kleinschreibung. Beispielsweise **Mannheim**, **manuell** oder **Roman**. |
|`'Man'`|Alle Datensätze mit Feldern, die nur den Text **Man** enthalten und die Groß-/Kleinschreibung beachten.|
|`Man*`|Alle Datensätze mit Feldern, die mit dem Text <b>Man</b> beginnen und die Groß-/Kleinschreibung beachten. Beispielsweise **Mannheim**, aber nicht **manuell** oder **Roman**.|
|`@Man*`|Alle Datensätze mit Feldern, die mit dem Text **man** beginnen, ungeachtet der Groß-/Kleinschreibung. Beispielsweise **Mannheim** und **manuell**, aber nicht **Roman**.|
|`@*man`|Alle Datensätze, die mit dem Text **man** enden, ungeachtet der Groß-/Kleinschreibung. Beispielsweise **Roman**, aber nicht **Mannheim** oder **manuell**.|

> [!TIP]
> Sie können F3 drücken, um das Suchfeld zu aktivieren oder zu deaktivieren. Weitere Informationen finden Sie unter [Einrichten von Tastenkombinationen](keyboard-shortcuts.md#KeyboardFilter).

## <a name="filtering"></a>Filterung
Filterung bietet eine erweiterte und vielseitigere Art zum Steuern der in einer Liste angezeigten Datensätze. Es gibt zwei wichtige Unterschiede zwischen Suchen und Filtern, wie in der folgenden Tabelle beschrieben wird.

|| **Suchen** | **Filterung** |
|--|----------|------------|
| **Anwendbare Felder** | Sucht in allen Feldern, die auf der Seite angezeigt werden. | Filtert ein oder mehrere einzelne Felder, wählt aus jedem Feld in der Tabelle aus, einschließlich Feldern, die nicht auf der Seite angezeigt werden. |
| **Zuordnung** | Zeigt Datensätze mit Feldern, die mit dem Suchtext übereinstimmen, ungeachtet der Groß-/Kleinschreibung oder der Position des Texts. | Zeigt Datensätze an, in denen das Feld dem Filter genau entspricht und die Groß-/Kleinschreibung beachtet wird, es sei denn, spezielle Filtersymbole wurden eingegeben.

Filterung ermöglicht es Ihnen, Datensätze für bestimmte Konten oder Debitoren, Daten, Beträge und weitere Informationen anzeigen, indem Filterkriterien angegeben werden. Nur mit den Kriterien übereinstimmende Datensätze werden angezeigt. Falls Sie Kriterien für mehrere Felder angeben, werden nur Datensätze angezeigt, die allen Kriterien entsprechen.

### <a name="working-in-the-filter-pane"></a>Arbeiten im Filterbereich
Der Filterbereich enthält die aktuellen Filter für eine Liste und ermöglicht es Ihnen, Ihre eigenen benutzerdefinierten Filter für mehrere Felder festzulegen. Die folgenden Abbildung zeigt einen Beispielsfilterbereich für eine Verkaufsangebotsliste.

![Filterbereichsübersicht ](media/filter-pane-overview.png "Filtersymbol")

Um den Filterbereich anzuzeigen, verwenden Sie die Tastenkombination **UMSCHALT+F3** . Bei Listen innerhalb des Rollencenters können Sie diesen Nach-Unten-Pfeil neben dem Seitentitel in der Navigationsleiste über die Liste auswählen und dann **Filterbereich anzeigen** auswählen.

![Filterbereich anzeigen](media/open-filter-pane.png "Filterbereich anzeigen")

Ein Filterbereich wird in drei Abschnitten aufgeteilt: **Ansichten**, **Liste filtern nach** und **Summen filtern nach**:

- **Ansichten**

  Einige Listen enthalten den Abschnitt **Ansichten**. Ansichten sind Variationen der Liste, die mit Filtern vorkonfiguriert wurden. Um zu einer anderen Ansicht Ihrer Liste zu wechseln, wählen Sie einfach einen anderen Link aus. Sie können Filter einer Ansicht vorübergehend ändern. Die Änderungen werden aber nicht permanent gespeichert.

- **Liste filtern nach**

  Im Abschnitt **Liste filtern nach** fügen Sie Filter für bestimmte Felder hinzu, um die Anzahl der angezeigten Datensätze zu verringern. Um einen Filter hinzuzufügen, wählen Sie **+ Filter** aus, wählen Sie das zu filternde Feld aus jedem Feld in der Tabelle aus und geben Sie dann Filterkriterien in das Feld ein.

- **Summen filtern nach**

  Einige Listen, die berechnete Felder anzeigen, z. B. Beträge und Mengen, enthalten den Abschnitt **Summen filtern nach**, in dem Sie verschiedene Dimensionen anpassen können, die Berechnungen beeinflussen. Beispielsweise können Sie Ihren Kontenplan schnell analysieren, indem Sie die Beträge eines bestimmten Zeitraums filtern, oder Sie können die Summen der Verkaufsaufträge nur eines bestimmten Lagers ansehen.

  Um einen Filter hinzuzufügen, wählen Sie **+ Filter** aus, wählen Sie eine der vordefinierten Dimensionen aus und fügen Sie dann die Filterkriterien im Feld hinzu.

  > [!NOTE]
  > Filter im Abschnitt **Summen filtern nach** werden im Seitenentwurf durch FlowFilter gesteuert. Technischer Informationen finden Sie unter [FlowFilter](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Eingeben von Filterkriterien im Filterbereich
Zum Auswählen eines zu filternden Felds führen Sie eine der folgenden Schritte aus:
  - Im Filterbereich wählen Sie **+ Feld** aus. Geben Sie den Namen des Feldes ein, das Sie filtern möchten, oder wählen Sie ein Feld aus dem Menü aus, das alle Felder in der Tabelle anzeigt.

  - In einer Spaltenüberschrift wählen Sie unten Nach-Unten-Pfeil aus und wählen dann **Filtern…** aus. Dadurch wird der Filterbereich geöffnet und dem Filterbereich eine Spalte hinzugefügt.

Sie können jetzt Ihre Filterkriterien im Feld eingeben oder auswählen. Die Art des Feldes, das Sie filtern, bestimmt, welche Kriterien Sie eingeben können. Beispielsweise können Sie in einem Feld mit festen Werte nur in diesen Werten filtern. Weitere Informationen über spezielle Filtersymbole finden Sie unter [Filterkriterien](#FilterCriteria) und [Filtertoken](#FilterTokens)

Spalten, die bereits Filter haben, werden durch das ![Filtersymbol](media/ui-search/filter-icon.png "Filtersymbol") in die Spaltenüberschrift angegeben. Um einen Filter zu entfernen, klicken Sie auf die Spaltenüberschrift und, wählen Sie **Filter löschen** aus.


### <a name="entering-filter-criteria-without-the-filter-pane"></a>Eingeben von Filterkriterien ohne Filterbereich
Sie können Filter einfach direkt in der Liste auswählen, ohne den Filterbereich verwenden zu müssen.
Wenn ein Feld in einer Zeile ausgewählt ist, verwenden Sie die Tastenkombination **ALT+F3**, um nur die Datensätze mit demselben Wert anzuzeigen. Sie können ein anders Feld auswählen und dieselbe Tastenkombination erneut verwenden, um Ihrer Filter weiter zu verfeinern. Wenn das ausgewählte Feld bereits gefiltert wird, wird der Filter über **ALT+F3** gelöscht.

> [!TIP]
> Beschleunigen Sie die Suche und das Analysieren Ihrer Daten, indem Sie Kombinationen von Tastenkombinationen verwenden. Wählen Sie zum Beispiel ein Feld aus, verwenden Sie **UMSCHALT+ALT+F3**, um diesen Filter dem Filterbereich hinzuzufügen und verwenden Sie **STRG+EINGABETASTE**, um die Zeilen zurückzugeben, wählen Sie ein anderes Feld aus und verwenden Sie **ALT+F3**, um zu diesem Wert zu filtern.
Weitere Informationen finden Sie unter [Einrichten von Tastenkombinationen](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"></a>Filterkriterien und Bildsymbole
Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind. Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen. Die folgende Tabelle enthält die Symbole, die in Filtern verwendet werden können. Detaillierte Informationen zu Datumsangaben und Uhrzeit finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeit im Kalender](ui-enter-date-ranges.md).

> [!IMPORTANT]  
>  Es kann Instanzen geben, in denen diese Feldwerte Symbole enthalten, die Sie filtern möchten. Um dies zu tun, müssen Sie den Filterausdruck berücksichtigt der das Symbol in Anführungszeichen (") enthält. Wenn Sie beispielsweise Datensätzen filtern möchten, die mit dem Text *S&R* beginnen, ist der Filterausdruck `'S&R*'`.  

### <a name="-interval"></a>(..) Intervall

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`1100..2100`|Nummer 1100 bis 2100|  
|`..2500`|Bis einschließlich 2500|  
|`..12 31 00`|Datum bis und einschließlich 31.12.00|  
|`P8..`|Daten zur Buchhaltungsperiode 8 und folgende|  
|`..23`|Vom Anfangsdatum bis zum 23. (aktueller Monat, aktuelles Jahr, 23:59:59)|  
|`23..`|Vom 23-des aktuellen Monats-des aktuellen Jahres 0:00:00 bis zum Ende der Zeit|  
|`22..23`|Vom 22-des aktuellen Monats-aktuellen Jahres 0:00:00 bis zum 23-des aktuellen Monats-aktuellen Jahres 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Entweder/oder  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`1200|1300`|Nummern mit 1200 oder 1300|  

### <a name="-not-equal-to"></a>(<>) Ungleich  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`<>0`|Alle Datensätze außer der Nummer Null<br /><br /> Die SQL Server-Option ermöglicht es Ihnen, dieses Symbol mit einem Platzhalterausdruck zu kombinieren. So wird beispielsweise mit "<>A*" Text beschrieben, der nicht mit einem großen A beginnt.|  

### <a name="-greater-than"></a>(>) Größer als  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`>1200`|Datensatznummern größer als 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Größer oder gleich  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`>=1200`|Datensatznummern ab einschließlich 1200 aufwärts|  

### <a name="-less-than"></a>(<) Kleiner als  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`<1200`|Datensatznummern kleiner als 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Kleiner oder gleich  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`<=1200`|Datensatznummern kleiner als oder gleich 1200|  

### <a name="-and"></a>(&) Und  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`>200&<1200`|Nummern größer 200 und Nummern kleiner 1200.|  

### <a name="-an-exact-character-match"></a>(") Eine genaue Zeichenübereinstimmung  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`'man'`|Text, der genau mit „man“ übereinstimmt und die Groß-/Kleinschreibung berücksichtigt.|  

### <a name="-case-insensitive"></a>(@) Groß-/Kleinschreibung beachten  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`@man*`|Text, der mit „man“ beginnt und die Groß-/Kleinschreibung beachtet.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Beliebig viele unbekannte Zeichen

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`*Co*`|Text, der die Zeichenfolge "Co" enthält und die Groß-/Kleinschreibung ist.|  
|`*Co`|Text, der mit "Co" endet und die Groß-/Kleinschreibung ist.|  
|`Co*`|Text, der mit "Co" beginnt und die Groß-/Kleinschreibung ist.|  

> [!NOTE]  
>   Sie können `*` nicht beim Filtern in Optionsfeldern (Enumerationen) verwenden, wie das Feld **Status** in Verkaufsaufträgen. Wenn Sie einen Filter für diese Art von Feld eingeben möchten, können Sie den numerischen Wert als Filterparameter eingeben. Beispielsweise im Feld **Status** in einem Verkaufsauftrag, der die Werte **Offen**, **Freigegeben**, **Genehmigung ausstehend** und **Vorauszahlung ausstehend** hat, verwenden Sie die Werte `0`, `1`, `2` und `3`, um für diese Optionen zu filtern.

### <a name="-one-unknown-character"></a>(?) Ein unbekannter Buchstabe  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`Hans?n`|Text wie "Hansen" oder "Hanson"|  

### <a name="combined-format-expressions"></a>Kombinierte Formatausdrücke  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Alle Datensätze mit der Nummer 5999 oder zwischen 8100 bis 8490.|  
|`..1299|1400..`|Alle Datensätze mit Nummern kleiner als bzw. gleich 1299 oder mit Nummern größer als bzw. gleich 1400, d. h. alle Datensatznummern außer 1300 bis 1399.|  
|`>50&<100`|Alle Datensätze mit Nummern größer als 50 und kleiner als 100, d. h. mit Nummern zwischen 51 und 99.|  


## <a name="FilterTokens"> </a> Filtertoken
Wenn Sie Filterkriterien eingeben, können Sie auch Begriffe mit besonderer Bedeutung eingeben, die Filtertoken genannt werden. Nachdem Sie das Token-Wort eingegeben haben, wird das Wort durch den Wert oder die Werte ersetzt, die es darstellt. Dadurch wird das Filtern einfacher, indem die Notwendigkeit verringert wird, auf andere Seiten zu navigieren, um Werte nachzuschlagen, die Sie Ihrem Filter hinzufügen möchten. In den folgenden Tabellen werden einige der Token beschreiben, die Sie als Filterkriterien eingeben können.

> [!TIP]
> Ihre Organisation verwendet möglicherweise benutzerdefinierte Token. Informationen zum verfügbaren kompletten Token-Satz, oder zum Hinzufügen weiterer benutzerdefinierter Token erhalten Sie von Ihren Administrator. Technischer Informationen finden Sie unter [Hinzufügen von Filter-Token](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens)


### <a name="me-or-userid-records-assigned-to-you"></a>(%me oder %userid) Ihnen zugewiesene Datensätze

Verwenden Sie `%me` oder `%userid`, wenn Sie Felder filtern, die die Benutzer-ID, wie das Feld **Benutzer-ID zugewiesen**, enthalten, um alle Datensätze anzuzeigen, die Ihnen zugeordnet werden.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%me`<br />oder<br />`%userid`|Datensätze, die Ihrem Benutzerkonto zugewiesen sind. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Debitoren in "Meine Debitoren"

Verwenden Sie `%mycustomers` im Feld Debitoren-**Nr**, um alle Datensätze für Debitoren anzuzeigen, die in der Liste **Meine Debitoren** in Ihrem Rollencenter enthalten sind.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%mycustomers`|Debitoren in **Meine Debitoren** in Ihrem Rollencenter. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Artikel in "Meine Artikel"

Verwenden Sie `%myitems` im Feld Artikel-**Nr**, um alle Datensätze für Artikel anzuzeigen, die in der Liste **Meine Artikel** in Ihrem Rollencenter enthalten sind.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%myitems`|Artikel in **Meine Artikel** in Ihrem Rollencenter. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) in "Meine Kreditoren"

Verwenden Sie `%myvendors` im Feld Kreditoren-**Nr**, um alle Datensätze für Kreditoren anzuzeigen, die in der Liste **Meine Kreditoren** in Ihrem Rollencenter enthalten sind.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%myvendors`|Kreditoren in **Meine Kreditoren** in Ihrem Rollencenter. |  


## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Fragen zum Suchen und Filtern](ui-search-filter-faq.md)
