---
title: Sortieren, Durchsuchen und Filtern von Listen | Microsoft Docs
description: Arbeiten Sie effizient in Listen, indem Sie in Ihren Daten suchen, Spalten sortieren und Ergebnis unter Verwendung der leistungsstarken Filtersymbole und Tastenkombinationen neu definieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5c67ea33937ded164626e4c403522a7dc1f3dca0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912571"
---
# <a name="sorting-searching-and-filtering"></a>Sortieren, Durchsuchen und Filtern

Es gibt mehrere Möglichkeiten, wie Sie das tun können und die dabei helfen, Datensätze in einer Liste oder einem Bericht oder XMLport zu scannen, zu suchen und einzugrenzen. Diese umfassen Sortierung, Suche und Filterung. Sie können einige oder alle davon gleichzeitig anwenden, um die Daten schnell zu finden oder zu analysieren.

Für Berichte und XML-Ports können Sie, wie bei Listen, Filter setzen, um abzugrenzen, welche Daten in den Bericht aufgenommen werden sollen oder XMLport, aber Sie können nicht sortieren und suchen.

> [!TIP]
> Wenn Sie Ihre Daten als Kacheln anzeigen, können Sie grundlegender Filterung verwenden und entsprechend suchen. Um den gesamten Satz der leistungsstarken Funktionen zum Sortieren, Suchen und Filtern zu verwenden, wählen Sie das Symbol ![Als Liste anzeigen](media/ui_show_as_list_icon.png "Als Listenpfeil links anzeigen"), um die Datensätze als Liste anzuzeigen.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sortieren

Dank der Sortierfunktion können Sie sich schnell und einfach einen Überblick über Ihre Daten verschaffen. Wenn Sie beispielsweise über zahlreiche Debitorenkontakte verfügen, können Sie auswählen, um nach folgenden Kriterien zu sortieren: **Debitorennummer** , **Debitorenbuchungsgruppe** , **Währungscode** , **Länder-/Regionscode** oder **Verkaufssteuer-Registrierung** , um die gewünschte Übersicht zu erhalten.

Um eine Liste zu sortieren, können Sie entweder eine Spaltenüberschrift auswählen, um zwischen aufsteigender und absteigender Reihenfolge umzuschalten, oder den kleinen Pfeil-nach-Unten auswählen und **Aufsteigend** oder die Aktion **Absteigend** wählen.  

> [!NOTE]  
> Sortierung wird nicht auf Bilder, BLOB-Felder und FlowFilter unterstützt, die keiner Tabelle angehören.  

## <a name="searching"></a>Suchen

<!--## Searching by using the Quick Filter -->
Am Anfang jeder Liste befindet sich eine Aktion ![Suchliste](media/ui-search/search-list.png "Symbol für die Suchliste") **Suchen** , die eine schnelle und einfache Möglichkeit bietet, die Datensätze in einer Liste zu verringern und nur die Datensätze mit den Daten anzuzeigen, die Sie anzeigen möchten.

Zur Suche wählen Sie einfach die Aktion **Suchen** aus und geben dann im Feld den Text ein, nach dem Sie suchen. Sie können Buchstaben, Ziffern und andere Symbole eingeben.

### <a name="fine-tuning-the-search"></a>Feinabstimmung der Suche

Im Allgemeinen versucht die Suche, Text in allen Feldern abzugleichen. Dabei werden zwischen groß und klein geschriebene Zeichen nicht unterschieden (d. h., die Groß-/Kleinschreibung wird nicht beachtet). Text an jeder Stelle im Feld (am Anfang, am Ende oder in der Mitte) wird durchsucht.

Sie können jedoch eine genauere Suche vornehmen, indem Sie die folgenden Sonderzeichen verwenden.

- Um nur Feldwerte zu finden, die dem gesamten Text und der Groß- und Kleinschreibung genau entsprechen, setzen Sie den Text in einfache Anführungszeichen `''` (z. B. `'man'`).

- Um nur Feldwerte zu finden, die mit einem bestimmten Text beginnen und der Groß- und Kleinschreibung entsprechen, setzen Sie `*` hinter den Text (z. B. `man*`).

- Um nur Feldwerte zu finden, die mit einem bestimmten Text enden und der Groß- und Kleinschreibung entsprechen, setzen Sie `*` vor den Text (z. B. `*man`).

- Bei der Anwendung von `''` oder `*` wird die Groß-/Kleinschreibung berücksichtigt. Wenn bei der Suche die Groß-/Kleinschreibung nicht beachtet werden soll, setzten Sie ein `@` vor der Suchtext (zum Beispiel `@man*`).

Die folgende Tabelle enthält einige Beispiele, um zu erläutern, wie Sie die Suche verwenden können.

|Suchkriterien|Findet…|
|---------------|----------|
|`man`<br />oder <br />`Man`|Alle Datensätze mit Feldern, die den Text **man** enthalten, unabhängig der Groß-/Kleinschreibung. Beispielsweise **Mannheim** , **manuell** oder **Roman** . |
|`'Man'`|Alle Datensätze mit Feldern, die nur den Text **Man** enthalten und die Groß-/Kleinschreibung beachten.|
|`Man*`|Alle Datensätze mit Feldern, die mit dem Text <b>Man</b> beginnen und die Groß-/Kleinschreibung beachten. Beispielsweise **Mannheim** , aber nicht **manuell** oder **Roman** .|
|`@Man*`|Alle Datensätze mit Feldern, die mit dem Text **man** beginnen, ungeachtet der Groß-/Kleinschreibung. Beispielsweise **Mannheim** und **manuell** , aber nicht **Roman** .|
|`@*man`|Alle Datensätze, die mit dem Text **man** enden, ungeachtet der Groß-/Kleinschreibung. Beispielsweise **Roman** , aber nicht **Mannheim** oder **manuell** .|

> [!TIP]
> Sie können **F3** drücken, um das Suchfeld zu aktivieren oder zu deaktivieren. Weitere Informationen finden Sie unter [Einrichten von Tastenkombinationen](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Die Suche stimmt nicht mit Werten in Bildern, BLOB-Feldern, FlowFiltern, FlowFields und anderen Feldern überein, die nicht Teil einer Tabelle sind.

## <a name="filtering"></a><a name="filtering"></a>Filterung

Filterung bietet eine erweiterte und vielseitigere Art zum Steuern der in einer Liste angezeigten Datensätze oder diese in einem Bericht oder XMLport anzuzeigen. Es gibt zwei wichtige Unterschiede zwischen Suchen und Filtern, wie in der folgenden Tabelle beschrieben wird.

|| **Suchen** | **Filterung** |
|--|----------|------------|
| **Anwendbare Felder** | Sucht in allen Feldern, die auf der Seite angezeigt werden. | Filtert ein oder mehrere einzelne Felder, wählt aus jedem Feld in der Tabelle aus, einschließlich Feldern, die nicht auf der Seite angezeigt werden. |
| **Zuordnung** | Zeigt Datensätze mit Feldern, die mit dem Suchtext übereinstimmen, ungeachtet der Groß-/Kleinschreibung oder der Position des Texts. | Zeigt Datensätze an, in denen das Feld dem Filter genau entspricht und die Groß-/Kleinschreibung beachtet wird, es sei denn, spezielle Filtersymbole wurden eingegeben.

Filterung ermöglicht es Ihnen, Datensätze für bestimmte Konten oder Debitoren, Daten, Beträge und weitere Informationen anzeigen, indem Filterkriterien angegeben werden. Nur Datensätze, die den Kriterien entsprechen, werden in der Liste angezeigt oder in den Bericht, den Stapeljob oder XMLport aufgenommen. Falls Sie Kriterien für mehrere Felder angeben, werden nur Datensätze angezeigt, die allen Kriterien entsprechen.

Bei Listen werden die Filter in einem Filterbereich angezeigt, der beim Aktivieren links von der Liste angezeigt wird. Für Berichte, Stapeljobs und XML-Ports sind die Filter direkt auf der Anforderungsseite sichtbar.

### <a name="filtering-with-option-fields"></a>Filtern mit Optionsfeldern

Für "normale" Felder, die Daten, Einrichtungsdatum oder Geschäftsdaten enthalten, können Sie Filter festlegen, indem Sie Daten auswählen und Filterwerte eingeben. Mithilfe von Symbolen können Sie erweiterte Filterkriterien definieren. Informationen erhalten Sie unter [Eingeben von Filterkriterien](ui-enter-criteria-filters.md#entering-filter-criteria)

Für Felder vom Typ **Möglichkeit** können Sie einen Filter jedoch nur festlegen, indem Sie eine oder mehrere Optionen aus einer Dropdown-Liste der verfügbaren Optionen auswählen. Ein Beispiel für ein Optionsfeld ist das **Status** Feld auf der **Kundenaufträge** Seite.

> [!NOTE]
> Wenn Sie mehrere Optionen als Filterwert auswählen, wird die Beziehung zwischen den Optionen als *ODER* definiert. Zum Beispiel, wenn Sie das Kontrollkästchen **Öffnen** und **Freigegeben** im **Status** Filterfeld auf der Seite **Kundenaufträge** auswählen, bedeutet dies, dass offene oder freigegebene Kundenaufträge angezeigt werden.

### <a name="setting-filters-on-lists"></a>Festlegen von Filtern in Listen

In Listen legen Sie Filter mithilfe des Filterbereichs fest. Um den Filterbereich für eine Liste anzuzeigen, klicken Sie auf den Dropdown-Pfeil neben dem Namen der Seite und wählen Sie dann die **Filterbereich anzeigen** Aktion. Alternativ können Sie auch **UMSCHALT+F3** drücken.

Um den Filterbereich für eine Spalte in einer Liste anzuzeigen, klicken Sie auf den Dropdown-Pfeil neben dem Namen der Seite und wählen Sie dann die **Filterbereich anzeigen** Aktion. Alternativ können Sie auch **UMSCHALT+F3** drücken. Das Filterfenster wird mit der ausgewählten Spalte geöffnet, die als Filterfeld im Fenster angezeigt wird im Abschnitt **Liste filtern nach** .

Der Filterbereich enthält die aktuellen Filter für eine Liste und ermöglicht es Ihnen, Ihre eigenen benutzerdefinierten Filter für mehrere Felder festzulegen, indem Sie die Aktion **+Filter** auswählen.

 Ein Filterbereich wird in drei Abschnitten aufgeteilt: **Ansichten** , **Liste filtern nach** und **Summen filtern nach** :

- **Ansichten**

  Einige Listen enthalten den Abschnitt **Ansichten** . Ansichten sind Variationen der Liste, die mit Filtern vorkonfiguriert wurden. Sie können so viele Ansichten definieren und speichern, wie Sie möchten, und die Ansichten stehen Ihnen auf jedem Gerät zur Verfügung, auf dem Sie sich dann anmelden. Weitere Informationen finden Sie unter [Speichern und personalisieren von Listenansichten](ui-views.md).

- **Liste filtern nach**

  Hier fügen Sie Filter für bestimmte Felder hinzu, um die Anzahl der angezeigten Datensätze zu verringern. Um einen Filter hinzuzufügen, wählen Sie die **+ Filter** Aktion, geben Sie den Namen des Felds ein, nach dem Sie die Liste filtern möchten, oder wählen Sie ein Feld aus der Dropdown-Liste aus.

- **Summen filtern nach**

  Einige Listen, die berechnete Felder anzeigen, z. B. Beträge und Mengen, enthalten den Abschnitt **Summen filtern nach** , in dem Sie verschiedene Dimensionen anpassen können, die Berechnungen beeinflussen. Um einen Filter hinzuzufügen, wählen Sie die **+ Filter** Aktion, geben Sie den Namen des Felds ein, nach dem Sie die Liste filtern möchten, oder wählen Sie ein Feld aus der Dropdown-Liste aus.

  > [!NOTE]
  > Filter im Abschnitt **Summen filtern nach** werden im Seitenentwurf durch FlowFilter gesteuert. Technischer Informationen finden Sie unter [FlowFilter](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Sie können einen einfachen Filter direkt in einer Liste im Filterbereich festlegen, dh einen Filter, der nur Datensätze mit demselben Wert wie in der ausgewählten Zelle anzeigt. Um eine Zelle in einer Liste anzuzeigen, klicken Sie auf den Dropdown-Pfeil neben dem Namen der Seite und wählen Sie dann die **Filter für diesen Wert anzeigen** Aktion. Alternativ können Sie auch **ALT+F3** drücken.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Festlegen von Filtern in Berichten, Stapeljobs und XML-Ports

Für Berichte und XML-Ports sind die Filter direkt auf der Anforderungsseite sichtbar. Auf der Anforderungsseite werden die zuletzt verwendeten Filter entsprechend Ihrer Auswahl im Feld **Verwenden Sie die Standardwerte von** angezeigt. Weitere Informationen finden Sie unter [Gespeicherte Einstellungen verwenden](ui-work-report.md#SavedSettings).

Der Abschnitt wesentlicher **Filter** zeigt die Standardfilterfelder an, mit denen Sie die Datensätze abgrenzen, die in den Bericht oder XMLport aufgenommen werden sollen. Um einen Filter hinzuzufügen, wählen Sie die **+ Filter** Aktion, geben Sie den Namen des Felds ein, nach dem Sie die Liste filtern möchten, oder wählen Sie ein Feld aus der Dropdown-Liste aus.

In dem **Gesamtsummen filtern nach** Abschnitt können Sie verschiedene Dimensionen anpassen, die die Berechnungen im Bericht oder XMLport beeinflussen. Um einen Filter hinzuzufügen, wählen Sie die **+ Filter** Aktion, geben Sie den Namen des Felds ein, nach dem Sie die Liste filtern möchten, oder wählen Sie ein Feld aus der Dropdown-Liste aus.

## <a name="entering-filter-criteria"></a>Eingeben von Filterkriterien

Sowohl im Filterbereich als auch auf einer Anforderungsseite geben Sie Ihre Filterkriterien in das Feld unter dem Filterfeld ein.

Die Art des Filter-Feldes, das Sie filtern, bestimmt, welche Kriterien Sie eingeben können. Beispielsweise können Sie in einem Feld mit festen Werte nur in diesen Werten filtern. Weitere Informationen über spezielle Filtersymbole finden Sie unter [Filterkriterien](#FilterCriteria) und [Filtertoken](#FilterTokens)

Spalten, die bereits Filter haben, werden durch das Symbol ![Filtersymbol](media/ui-search/filter-icon.png "Filtersymbol") in die Spaltenüberschrift angegeben. Wählen Sie den Dropdownpfeil im Seitentitel und dann **Filter löschen** , um einen Filter zu entfernen.

> [!TIP]
> Beschleunigen Sie die Suche und das Analysieren Ihrer Daten, indem Sie Kombinationen von Tastenkombinationen verwenden. Wählen Sie zum Beispiel ein Feld aus, verwenden Sie **UMSCHALT+ALT+F3** , um diesen Filter dem Filterbereich hinzuzufügen und verwenden Sie **STRG+EINGABETASTE** , um die Zeilen zurückzugeben, wählen Sie ein anderes Feld aus und verwenden Sie **ALT+F3** , um zu diesem Wert zu filtern. Weitere Informationen finden Sie unter [Einrichten von Tastenkombinationen](keyboard-shortcuts.md#KeyboardFilter).

### <a name="filter-criteria-and-symbols"></a><a name="FilterCriteria"> </a>Filterkriterien und Symbole

Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind. Zudem können Sie Sonderzeichen (oder Operatoren) verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen. Die folgende Tabelle enthält die Symbole, die Sie in Filtern verwenden können. Detaillierte Informationen zu Datumsangaben und Uhrzeit finden Sie unter [Arbeiten mit Datumsangaben und Uhrzeit im Kalender](ui-enter-date-ranges.md).

> [!IMPORTANT]  
> Es kann Instanzen geben, in denen diese Feldwerte Symbole enthalten, die Sie filtern möchten. Um dies zu tun, müssen Sie den Filterausdruck berücksichtigt der das Symbol in Anführungszeichen (") enthält. Wenn Sie beispielsweise Datensätzen filtern möchten, die mit dem Text *S&R* beginnen, ist der Filterausdruck `'S&R*'`.

In den folgenden Abschnitten wird die Verwendung der verschiedenen Operatoren beschrieben.

> [!NOTE]
> Wenn ein Filter mehr als 200 Operatoren enthält, gruppiert das System einige Ausdrücke automatisch in Klammern `()` zum Zwecke der Verarbeitung. Dies hat keine Auswirkungen auf den Filter oder die Ergebnisse.  

#### <a name="-interval"></a>(..) Intervall

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`1100..2100`|Nummer 1100 bis 2100|  
|`..2500`|Bis einschließlich 2500|  
|`..12 31 00`|Datum bis und einschließlich 31.12.00|  
|`P8..`|Daten zur Buchhaltungsperiode 8 und folgende|  
|`..23`|Vom Anfangsdatum bis zum 23. (aktueller Monat, aktuelles Jahr, 23:59:59)|  
|`23..`|Vom 23-des aktuellen Monats-des aktuellen Jahres 0:00:00 bis zum Ende der Zeit|  
|`22..23`|Vom 22-des aktuellen Monats-aktuellen Jahres 0:00:00 bis zum 23-des aktuellen Monats-aktuellen Jahres 23:59:59|  

#### <a name="124-eitheror"></a>(&#124;) Entweder/oder

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`1200|1300`|Nummern mit 1200 oder 1300|  

#### <a name="-not-equal-to"></a>(<>) Ungleich  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`<>0`|Alle Datensätze außer der Nummer Null<br /><br /> Die SQL Server-Option ermöglicht es Ihnen, dieses Symbol mit einem Platzhalterausdruck zu kombinieren. So wird beispielsweise mit "<>A*" Text beschrieben, der nicht mit einem großen A beginnt.|  

#### <a name="-greater-than"></a>(>) Größer als  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`>1200`|Datensatznummern größer als 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Größer oder gleich  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`>=1200`|Datensatznummern ab einschließlich 1200 aufwärts|  

#### <a name="-less-than"></a>(<) Kleiner als  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`<1200`|Datensatznummern kleiner als 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Kleiner oder gleich  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`<=1200`|Datensatznummern kleiner als oder gleich 1200|  

#### <a name="-and"></a>(&) Und  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`>200&<1200`|Nummern größer 200 und Nummern kleiner 1200.|  

#### <a name="-an-exact-character-match"></a>(") Eine genaue Zeichenübereinstimmung  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`'man'`|Text, der genau mit „man“ übereinstimmt und die Groß-/Kleinschreibung berücksichtigt.|  

#### <a name="-case-insensitive"></a>(@) Groß-/Kleinschreibung beachten  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`@man*`|Text, der mit „man“ beginnt und die Groß-/Kleinschreibung beachtet.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Beliebig viele unbekannte Zeichen

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`*Co*`|Text, der die Zeichenfolge "Co" enthält und die Groß-/Kleinschreibung ist.|  
|`*Co`|Text, der mit "Co" endet und die Groß-/Kleinschreibung ist.|  
|`Co*`|Text, der mit "Co" beginnt und die Groß-/Kleinschreibung ist.|  

#### <a name="-one-unknown-character"></a>(?) Ein unbekannter Buchstabe  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`Hans?n`|Text wie "Hansen" oder "Hanson"|  

#### <a name="combined-format-expressions"></a>Kombinierte Formatausdrücke  

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Alle Datensätze mit der Nummer 5999 oder zwischen 8100 bis 8490.|  
|`..1299|1400..`|Alle Datensätze mit Nummern kleiner als bzw. gleich 1299 oder mit Nummern größer als bzw. gleich 1400, d. h. alle Datensatznummern außer 1300 bis 1399.|  
|`>50&<100`|Alle Datensätze mit Nummern größer als 50 und kleiner als 100, d. h. mit Nummern zwischen 51 und 99.|  

### <a name="filter-tokens"></a><a name="FilterTokens"> </a>Filtertoken
Wenn Sie Filterkriterien eingeben, können Sie auch Begriffe mit besonderer Bedeutung eingeben, die Filtertoken genannt werden. Nachdem Sie das Token-Wort eingegeben haben, wird das Wort durch den Wert oder die Werte ersetzt, die es darstellt. Dadurch wird das Filtern einfacher, indem die Notwendigkeit verringert wird, auf andere Seiten zu navigieren, um Werte nachzuschlagen, die Sie Ihrem Filter hinzufügen möchten. In den folgenden Tabellen werden einige der Token beschreiben, die Sie als Filterkriterien eingeben können.

> [!TIP]
> Ihre Organisation verwendet möglicherweise benutzerdefinierte Token. Informationen zum verfügbaren kompletten Token-Satz, oder zum Hinzufügen weiterer benutzerdefinierter Token erhalten Sie von Ihren Administrator. Technischer Informationen finden Sie unter [Hinzufügen von Filter-Token](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### <a name="me-or-userid-records-assigned-to-you"></a>(%me oder %userid) Ihnen zugewiesene Datensätze

Verwenden Sie `%me` oder `%userid`, wenn Sie Felder filtern, die die Benutzer-ID, wie das Feld **Benutzer-ID zugewiesen** , enthalten, um alle Datensätze anzuzeigen, die Ihnen zugeordnet werden.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%me`<br />oder<br />`%userid`|Datensätze, die Ihrem Benutzerkonto zugewiesen sind. |  

#### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Debitoren in "Meine Debitoren"

Verwenden Sie `%mycustomers` im Feld Debitoren- **Nr** , um alle Datensätze für Debitoren anzuzeigen, die in der Liste **Meine Debitoren** in Ihrem Rollencenter enthalten sind.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%mycustomers`|Debitoren in **Meine Debitoren** in Ihrem Rollencenter. |  

#### <a name="myitems-items-in-my-items"></a>(%myitems) Artikel in "Meine Artikel"

Verwenden Sie `%myitems` im Feld Artikel- **Nr** , um alle Datensätze für Artikel anzuzeigen, die in der Liste **Meine Artikel** in Ihrem Rollencenter enthalten sind.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%myitems`|Artikel in **Meine Artikel** in Ihrem Rollencenter. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) in "Meine Kreditoren"

Verwenden Sie `%myvendors` im Feld Kreditoren- **Nr** , um alle Datensätze für Kreditoren anzuzeigen, die in der Liste **Meine Kreditoren** in Ihrem Rollencenter enthalten sind.

|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|`%myvendors`|Kreditoren in **Meine Kreditoren** in Ihrem Rollencenter. |  

## <a name="see-also"></a>Siehe auch

[Suchen und Filtern FAQ](ui-search-filter-faq.md)  
[Speichern und personalisieren Sie Listenansichten](ui-views.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
