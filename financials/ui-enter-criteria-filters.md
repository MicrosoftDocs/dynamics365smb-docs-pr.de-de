---
title: Eingeben von Kriterien in Filtern| Microsoft Docs
description: Erfahren, wie Filter in Financials arbeiten.
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
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1a94e2ead59a40081920a0b11ed545a895d89910
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Eingeben von Kriterien in Filtern
<a id="entering-criteria-in-filters" class="xliff"></a>
Wenn Sie nach Daten, wie Debitorennamen, Adressen oder Produktgruppen suchen möchten, geben Sie Kriterien ein. Beim Eingeben von Filterkriterien können alle Ziffern und Buchstaben verwendet werden, die auch normalerweise im Feld zulässig sind. Zudem können Sie Sonderzeichen verwenden, um eine zusätzliche Filterung der Ergebnisse zu erreichen.

## Suchen mithilfe des Schnellfilters
<a id="searching-using-the-quick-filter" class="xliff"></a>
Sie können allen Seiten Filter hinzufügen, indem Sie Schnellfilter oder erweiterte Filter verwenden. Der Schnellfilter wird aktiviert, indem Sie das Lupensymbol in der oberen rechten Ecke einer Seite auswählen. Diese Filterart wird für die schnelle Eingabe von Kriterien verwendet.

**Wichtig**: Der Schnellfilter bietet einen einfachen Zugriff auf Filterdaten durch die Eingabe reinen Texts, bietet aber auch zahlreiche Optionen für Suchkriterien. Abhängig davon, ob Sie Freitext oder Text mit Symbolen eingeben, verhält sich der Schnellfilter unterschiedlich.  

* Wenn Sie Freitextangaben in den Suchkriterien eingeben, werden die Suchkriterien als die Groß-/Kleinschreibung nicht beachtend angesehen.  
* Wenn Sie Text mit Symbolen in den Suchkriterien eingeben, werden die Suchkriterien genau wie angegeben interpretiert, und die Groß-/Kleinschreibung wird berücksichtigt.

### Schnelle Filterkriterien
<a id="quick-filter-criteria" class="xliff"></a>
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

**Hinweis**: Sie können keinen Platzhalter beim Filtern in Aufzählungsfeldern, wie das Feld **Status** in Verkaufsaufträgen verwenden. Wenn Sie einen Filter für diese Art von Feld eingeben möchten, können Sie den numerischen Wert als Filterparameter eingeben. Beispielsweise im Feld **Status** in einem Verkaufsauftrag, der die Werte **Offen**, **Freigegeben**, **Genehmigung ausstehend** und **Vorauszahlung ausstehend** hat, verwenden Sie die Werte **0**, **1**, **2** und **3**, um für diese Optionen zu filtern.  

## Siehe auch
<a id="see-also" class="xliff"></a>
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

