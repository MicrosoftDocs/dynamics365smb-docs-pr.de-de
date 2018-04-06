---
title: Daten und das Eingeben von Filterkriterien finden | Microsoft Docs
description: Beschreibt, wie mit Filtern, wie Schnellfilter, gearbeitet wird, um Suchergebnisse zu verfeinern, wenn Sie Daten suchen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="searching-filtering-and-sorting-data"></a>Ermitteln, filternd und Sortieren von Daten
Es gibt mehrere Elemente, wie Sie das tun können und die dabei helfen, Datensätze in einer Liste aufzufinden, festzulegen und zu scannen. Diese umfassen die Sortierung, Suche und Filterung.

Wenn Sie nach Daten, wie Debitorennamen, Adressen oder Produktgruppen suchen möchten, geben Sie Kriterien ein. Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind. Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen. Es gibt zwei Arten zu suchen: mithilfe der Schnellfilter- oder der Spaltenfilter.

## <a name="sorting"></a>Sortieren
Dank der Sortierfunktion können Sie sich schnell und einfach einen Überblick über Ihre Daten verschaffen. Wenn Sie beispielsweise über zahlreiche Debitorenkontakte verfügen, können Sie auswählen, um nach folgenden Kriterien zu sortieren: **Debitorennummer**, **Debitorenbuchungsgruppe**, **Währungscode**, **Länder-/Regionscode** oder **Verkaufssteuer-Registrierung**, um die gewünschte Übersicht zu erhalten.

Um eine Übersicht zu sortieren, können Sie entweder einen Spaltenüberschriftentext um das Menüband zu erweitern und Aufsteigen Absteigend Reihenfolge aus, oder wählen Sie kleine Abstiegpfeil in die Spaltenüberschrift, und wählen Sie dann **Aufsteigend** oder **Absteigend**  

> [!NOTE]  
>   Sortierung wird nicht auf Bilder, BLOB-Felder und FlowFilter unterstützt, die keiner Tabelle angehören.  

## <a name="searching-by-using-the-quick-filter"></a>Suchen mithilfe des Schnellfilters
Sie können allen Seiten Filter hinzufügen, indem Sie Schnellfilter oder erweiterte Filter verwenden. Der Schnellfilter wird aktiviert, indem Sie das Lupensymbol in der oberen rechten Ecke einer Seite auswählen. Diese Filterart wird für die schnelle Eingabe von Kriterien verwendet.

> [!IMPORTANT]  
>   Der Schnellfilter bietet einen einfachen Zugriff auf Filterdaten durch die Eingabe reinen Texts, bietet aber auch zahlreiche Optionen für Suchkriterien. Abhängig davon, ob Sie Freitext oder Text mit Symbolen eingeben, verhält sich der Schnellfilter unterschiedlich.  

* Wenn Sie Freitextangaben in den Suchkriterien eingeben, werden die Suchkriterien als die Groß-/Kleinschreibung nicht beachtend angesehen.  
* Wenn Sie Text mit Symbolen in den Suchkriterien eingeben, werden die Suchkriterien genau wie angegeben interpretiert, und die Groß-/Kleinschreibung wird berücksichtigt.

### <a name="quick-filter-criteria"></a>Schnelle Filterkriterien
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Suchkriterien</TH>
    <TH>Interpretiert als...</TH>
    <TH>Reklamationen...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alle Datensätze, die den Text <b>Mann</b> enthalten und die Groß-/Kleinschreibung nicht beachten.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Alle Datensätze, die den Text <b>se</b> enthalten und die Groß-/Kleinschreibung nicht beachten.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Beginnt mit <b>Man</b> und Groß-/Kleinschreibung beachten</TD>
    <TD>Alle Datensätze, die mit dem Text <b>Mann</b> beginnen.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Exakter Text unter Berücksichtigung der Groß-/Kleinschreibung</TD>
    <TD>Alle Datensätze, die mit <b>Mann</b> genau übereinstimmen.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Beginnt mit, Groß-/Kleinschreibung beachtet</TD>
    <TD>Alle Datensätze, die mit <b>Mann</b> beginnen.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Endet mit, Groß-/Kleinschreibung beachtet</TD>
    <TD>Alle Datensätze, die mit <b>mann</b> enden.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Sie können keinen Platzhalter beim Filtern in Aufzählungsfeldern, wie das Feld **Status** in Verkaufsaufträgen verwenden. Wenn Sie einen Filter für diese Art von Feld eingeben möchten, können Sie den numerischen Wert als Filterparameter eingeben. Beispielsweise im Feld **Status** in einem Verkaufsauftrag, der die Werte **Offen**, **Freigegeben**, **Genehmigung ausstehend** und **Vorauszahlung ausstehend** hat, verwenden Sie die Werte **0**, **1**, **2** und **3**, um für diese Optionen zu filtern. 

## <a name="searching-by-using-column-filters"></a>Suchen mithilfe der Spaltenfiltern
Sie können einen Filter für einen oder mehreren Spalten aus einer Liste hinzufügen. Das Filtern in Spalten ist flexibel und erhöht als den Schnellfilter. 

### <a name="to-add-a-filter-on-a-column"></a>Um einen Filter für eine Spalte hinzufügen
1.  Bevor Sie Filter hinzufügen, wählen Sie ![Anzeigen als Liste](media/ui_show_as_list_icon.png "Anzeigen als linken Listenpfeil"), um die Listenansicht zu ändern.
2. Wählen Sie den Abwärts-Pfeil in die Spaltenüberschrift, und wählen Sie dann **Filter**.
3. Führen Sie einen der folgenden Schritte aus: 
  -  Wählen Sie *...* neben dem Feld, um einen Wert aus einer Liste auszuwählen.
  -  Eingeben von Kriterien in Filtern. Sehen Sie den nächsten Abschnitt für Einzelheiten.
4. Wählen Sie die Schaltfläche **OK** aus.

## <a name="filter-criteria-and-symbols"></a>Filterkriterien und Bildsymbole
Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind. Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen. Die folgende Tabelle enthält die Symbole, die in Filtern verwendet werden können.  
  
> [!IMPORTANT]  
>  Es kann Instanzen geben, in denen diese Feldwerte Symbole enthalten, die Sie filtern möchten. Um dies zu tun, müssen Sie den Filterausdruck berücksichtigt der das Symbol in Anführungszeichen (") enthält. Wenn Sie beispielsweise Datensätzen filtern möchten, die mit dem Text *S&R* beginnen, ist der Filterausdruck **'S&R*'**.  
  
### <a name="-interval"></a>(..) Intervall  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|1100..2100|Nummer 1100 bis 2100|  
|..2500|Bis einschließlich 2500|  
|..31 12 00|Datum bis und einschließlich 31.12.00|  
|P8..|Daten zur Buchhaltungsperiode 8 und folgende|  
|..23|Vom Anfangsdatum bis zum 23. (aktueller Monat, aktuelles Jahr, 23:59:59)|  
|23..|Vom 23-des aktuellen Monats-des aktuellen Jahres 0:00:00 bis zum Ende der Zeit|  
|22..23|Vom 22-des aktuellen Monats-aktuellen Jahres 0:00:00 bis zum 23-des aktuellen Monats-aktuellen Jahres 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) Entweder/oder  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|1200&#124;1300|Nummern mit 1200 oder 1300|  
  
### <a name="-not-equal-to"></a>(<>) Ungleich  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|<>0|Alle Datensätze außer der Nummer Null<br /><br /> Die SQL Server-Option ermöglicht es Ihnen, dieses Symbol mit einem Platzhalterausdruck zu kombinieren. So wird beispielsweise mit "<>A*" Text beschrieben, der nicht mit einem großen A beginnt.|  
  
### <a name="-greater-than"></a>(>) Größer als  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|>1200|Datensatznummern größer als 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Größer oder gleich  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|>=1200|Datensatznummern ab einschließlich 1200 aufwärts|  
  
### <a name="-less-than"></a>(<) Kleiner als  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|<1200|Datensatznummern kleiner als 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Kleiner oder gleich  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|<=1200|Datensatznummern kleiner als oder gleich 1200|  
  
### <a name="-and"></a>(&) Und  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|>200&<1200|Nummern größer 200 und Nummern kleiner 1200.|  
  
### <a name="-an-exact-character-match"></a>(") Eine genaue Zeichenübereinstimmung  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|'man'|Text, der genau übereinstimmt und die Groß-/Kleinschreibung berücksichtigt.|  
  
### <a name="-case-insensitive"></a>(@) Groß-/Kleinschreibung beachten  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|@man*|Text, der mit „Man“ beginnt und die Groß-/Kleinschreibung beachtet.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Beliebig viele unbekannte Zeichen  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|*Co*|Text, der die Zeichenfolge "Co" enthält und die Groß-/Kleinschreibung ist.|  
|*Co|Text, der mit "Co" endet und die Groß-/Kleinschreibung ist.|  
|Co*|Text, der mit "Co" beginnt und die Groß-/Kleinschreibung ist.|  
  
### <a name="-one-unknown-character"></a>(?) Ein unbekannter Buchstabe  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|Hans?n|Text wie "Hansen" oder "Hanson"|  
  
### <a name="combined-format-expressions"></a>Kombinierte Formatausdrücke  
  
|Beispielausdruck|Angezeigte Datensätze|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Alle Datensätze mit der Nummer 5999 oder zwischen 8100 bis 8490.|  
|..1299&#124;1400..|Alle Datensätze mit Nummern kleiner als bzw. gleich 1299 oder mit Nummern größer als bzw. gleich 1400, d. h. alle Datensatznummern außer 1300 bis 1399.|  
|>50&<100|Alle Datensätze mit Nummern größer als 50 und kleiner als 100, d. h. mit Nummern zwischen 51 und 99.|  
 
## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

