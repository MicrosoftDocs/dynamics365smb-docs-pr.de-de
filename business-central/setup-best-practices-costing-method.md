---
title: Bewährte Einrichtungsmethoden – Lagerabgangsmethode
description: Die Lagerabgangsmethode auf der Artikelkarte definiert, ob der Kostenfluss eines Artikels erfasst wird und ob ein tatsächlicher oder budgetierter Wert aktiviert wird und in der Kostenberechnung verwendet wird.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 30, 42, 43
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d6b2c19ae98c50854c35a0bff412689d8e2bc38f
ms.sourcegitcommit: 1e6addcd6ecc25489fc17388409989440a210895
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7974921"
---
# <a name="setup-best-practices-costing-method"></a>Bewährte Einrichtungsmethoden – Lagerabgangsmethode

Die **Lagerabgangsmethode** auf der Artikelkarte definiert, ob der Kostenfluss eines Artikels erfasst wird und ob ein tatsächlicher oder budgetierter Wert aktiviert wird und in der Kostenberechnung verwendet wird.  

Die richtige Lagerabgangsmethode entsprechend Art und betrieblichem Umfeld festzulegen, ist wichtig, um wirtschaftliche Bestände sicherzustellen.  

Die folgende Tabelle enthält bewährte Methoden zum Einrichten des **Kostenmethode**-Felds. Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden](design-details-costing-methods.md).  

|Einrichtungsoptionen|Bewährte Vorgehensweisen|Bemerkung|  
|------------------|-------------------|-------------|  
|FIFO|Wird verwendet, wo die Produktkosten stabil sind.<br /><br /> Verwendung für Artikel mit einem begrenzten Haltbarkeitsdatum, da die ältesten Waren verkauft werden müssen, bevor sie ihr Mindesthaltbarkeitsdatum überschreiten.|Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der FIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die ersten Artikel, die im Lager platziert sind, zuerst verkauft werden. **Hinweis:**  Wenn Preise steigen, zeigt die Bilanz größeren Wert. Das bedeutet, dass Steuerverbindlichkeiten zunehmen, aber die Bonität und die Möglichkeit, Kasse zu borgen verbessert sich.|  
|LIFO|Wird verwendet, wo Ebenen von Beständen gleich bleibend im Zeitverlauf erhalten oder erhöht werden.|Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der LIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die letzten Artikel, die im Lager platziert sind, zuerst verkauft werden. **Hinweis:**  Wenn Preise steigen, reduziert sich der Wert in den GuV-Konten. Das bedeutet, dass Steuerverbindlichkeiten abnehmen, aber die Möglichkeit, Kasse zu borgen verschlechtert sich. **Wichtig:** Nicht zugelassen in vielen Ländern/Regionen, da es verwendet werden kann, um den Deckungsbeitrag zu drücken.|  
|Durchschnitt|Wird verwendet, wo die Produktkosten instabil sind.<br /><br /> Wird verwendet wo Bestände angehäuft und zusammen kombiniert werden und nicht unterschieden werden können, wie Chemikalien.|Der Einstandspreis eines Artikels wird, wie der durchschnittliche Einstandspreis, an jedem Zeitpunkt nach einem Kauf berechnet.<br /><br /> Für die Lagerbestandsbewertung wird vorausgesetzt, dass alle Lagerbestände gleichzeitig verkauft werden.|
|Ausgewählt|Verwendung in der Produktion oder Handel von einfach identifizierbaren Artikeln mit sehr hohen Einstandspreis.<br /><br /> Verwendung für Artikel, die ZU-/Abschlägen unterliegen.<br /><br /> Verwendung für Artikel mit Seriennummern.|Der Einstandspreis eines Artikels sind die exakten Kosten, zu denen die bestimmte Einheit empfangen wurden.|
|Standard|Wird verwendet, wo Kostenkontrolle kritisch ist.<br /><br /> Verwendung in der wiederholenden Produktion, die Kosten des Fertigungsmaterials, direkte Arbeit und Produktionsgemeinkosten zu bewerten.<br /><br /> Wird verwendet, wo es Kategorie und Mitarbeiter gibt, um die Vorgaben beizubehalten.|Der Einstandspreis eines Artikels ist voreingestellt basierend auf vorkalkulierten Kosten.<br /><br /> Wenn die Ist-Kosten später realisiert werden, muss der Einstandspreis (fest) auf die Ist-Kosten durch Abweichungswerte reguliert werden.|  

## <a name="see-also"></a>Siehe auch

[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  
[Design Details: Kalkulation des Bestandes](design-details-inventory-costing.md)  
[Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]