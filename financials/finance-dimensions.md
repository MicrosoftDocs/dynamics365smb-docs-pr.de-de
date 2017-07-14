---
title: Dimensionen | Microsoft Docs
description: Dimensionen verwenden, um Daten zu analysieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Dimensionen
<a id="dimensions" class="xliff"></a>
Um Analyse in Belegen wie Verkaufsaufträgen einfacher durchzuführen, können Sie Dimensionen verwenden. Dimensionen sind Attribute und Werte, die Posten kategorisieren, sodass Sie sie verfolgen und analysieren können. So können Sie beispielsweise Dimensionen einrichten, mit denen angegeben wird, aus welchem Projekt oder aus welcher Abteilung ein Posten stammt.  

Dies ermöglicht die Verwendung von Dimensionen anstelle der Einrichtung separater Sachkonten für einzelne Abteilungen und Projekte. Kennzeichnet eine umfangreiche Verkaufschance zur Analyse, ohne dazu einen komplizierten Kontenplan zu erstellen.  

Oder Sie richten beispielsweise eine Dimension mit dem Namen *Abteilung* ein und verwenden diese Dimension und einen Dimensionswert, wenn Sie Verkaufsbelege buchen. Dadurch können Sie auch intelligente Geschäfts-Tools verwenden, um zu sehen, welche Abteilung die Artikel verkauft hat.
Je mehr Dimensionen Sie einrichten und verwenden, auf desto detaillierteren Berichten können Sie Ihre Geschäftsentscheidungen basieren. Zum Beispiel kann ein einzelner Verkaufsposten mehrere Dimensionsinformationen enthalten, wie:  

* Das Konto, auf das der Artikelverkauf gebucht wurde  
* Wo der Artikel verkauft wurde
* Wer ihn verkauft hat
* Die Art des Debitors, die ihn kaufte  

Das bedeutet, dass Sie beliebig viele maßgeschneiderte Finanzaufstellungen erstellen können.  

**Hinweis**: Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen].

## Dimensionen verwenden
<a id="using-dimensions" class="xliff"></a>
In einem Beleg, z. B. einem Verkaufsauftrag, können Sie Dimensionsinformationen sowohl für eine einzelne Belegzeile als auch für den Beleg selbst hinzufügen. Sie können beispielsweise im Fenster **Verkaufsauftrag** Dimensionswerte für die ersten beiden Shortcutdimensionen direkt in den Beleg eingeben und weitere Dimensionsinformationen hinzufügen, wenn Sie auf die Schaltfläche **Dimensionen** klicken.  

Wenn Sie stattdessen in einem Buch.-Blatt arbeiten, können Sie auf dieselbe Art und Weise Dimensionsinformationen hinzufügen, wenn Sie Shortcutdimensionen direkt als Felder in Buch.-Blattzeilen eingerichtet haben.  

Sie können Standarddimensionen für Konten oder Kontenarten festlegen, sodass Dimensionen und Dimensionswerte automatisch ausgefüllt werden.  

## Dimensionssätze
<a id="dimension-sets" class="xliff"></a>
Ein Dimensionssatz ist eine eindeutige Kombination von Dimensionswerten. Er wird als Dimensionssatzposten in die Datenbank gespeichert. Jeder Dimensionssatzposten stellt einen einzelnen Dimensionswert dar. Der Dimensionssatz wird durch eine allgemeine Dimensionssatz-ID identifiziert, die jedem Dimensionssatzposten zugewiesen wird, der zum Dimensionssatz gehört.  

Wenn Sie eine neue Buch.-Blattzeile, einen Belegkopf oder eine Belegzeile erstellen, können Sie eine Kombination von Dimensionswerten angeben. Anstatt jeden Dimensionswert explizit in der Datenbank zu speichern, wird eine Dimensionssatz-ID der Buch.-Blattzeile, dem Belegkopf oder der Belegzeile zugewiesen, um den Dimensionssatz anzugeben.  

## Siehe auch
<a id="see-also" class="xliff"></a>
[Finanzen](finance.md)  
[Einrichtung von Dimensionen](finance-setup-dimensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

