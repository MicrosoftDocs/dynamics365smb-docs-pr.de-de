---
title: Suchkriterien definieren| Microsoft Docs
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Eingeben von Kriterien in Filtern
Wenn Sie nach Daten, wie Debitorennamen, Adressen oder Produktgruppen suchen möchten, geben Sie Kriterien ein. Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind. Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen.

## <a name="searching-using-the-quick-filter"></a>Suchen mithilfe des Schnellfilters
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

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

