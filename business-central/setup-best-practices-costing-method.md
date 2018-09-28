---
title: "Bewährte Vorgehensweisen einrichten - Kostenmethoden | Microsoft Docs"
description: "Die **Kostenmethode** auf der Artikelkarte legt fest, ob der Kostenfluss des Artikels erfasst ist und ob ein tatsächlicher und budgetierter Wert gebucht und in der Berechnung des Einstandspreises verwendet wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f268c69b4ec5dbc3975392fb174b8d571c08bcb4
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-costing-method"></a>Bewährte Einrichtungsmethoden: Kostenmethode
Die **Kostenmethode** auf der Artikelkarte legt fest, ob der Kostenfluss des Artikels erfasst ist und ob ein tatsächlicher und budgetierter Wert gebucht und in der Berechnung des Einstandspreises verwendet wird.  

 Die richtige Lagerabgangsmethode entsprechend Art und betrieblichem Umfeld festzulegen, ist wichtig, um wirtschaftliche Bestände sicherzustellen.  

 Die folgende Tabelle enthält bewährte Methoden zum Einrichten des **Kostenmethode**-Felds. Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden".](design-details-costing-methods.md)  

|Einrichtungsoptionen|Bewährte Vorgehensweisen|Bemerkung|  
|------------------|-------------------|-------------|  
|FIFO|Wird verwendet, wo die Produktkosten stabil sind.<br /><br /> Verwendung für Artikel mit einem begrenzten Haltbarkeitsdatum, da die ältesten Waren verkauft werden müssen, bevor sie ihr Mindesthaltbarkeitsdatum überschreiten.|Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der FIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die ersten Artikel, die im Lager platziert sind, zuerst verkauft werden. **Hinweis:**  Wenn Preise steigen, zeigt die Bilanz größeren Wert. Das bedeutet, dass Steuerverbindlichkeiten zunehmen, aber die Bonität und die Möglichkeit, Kasse zu borgen verbessert sich.|  
|LIFO|Wird verwendet, wo Ebenen von Beständen gleich bleibend im Zeitverlauf erhalten oder erhöht werden.|Der Einstandspreis eines Artikels ist der tatsächliche Wert jedes Eingangs des Artikels, nach der LIFO-Regel ausgewählt.<br /><br /> In der Lagerbewertung wird angenommen, dass die letzten Artikel, die im Lager platziert sind, zuerst verkauft werden. **Hinweis:**  Wenn Preise steigen, reduziert sich der Wert in den GuV-Konten. Das bedeutet, dass Steuerverbindlichkeiten abnehmen, aber die Möglichkeit, Kasse zu borgen verschlechtert sich. **Wichtig:** Nicht zugelassen in vielen Ländern/Regionen, da es verwendet werden kann, um den Deckungsbeitrag zu drücken.|  
|Durchschnitt|Wird verwendet, wo die Produktkosten instabil sind.<br /><br /> Wird verwendet wo Bestände angehäuft und zusammen kombiniert werden und nicht unterschieden werden können, wie Chemikalien.|Der Einstandspreis eines Artikels sind die exakten Kosten, an denen die bestimmte Einheit empfangen wurden.|  
|Ausgewählt|Verwendung in der Produktion oder Handel von einfach identifizierbaren Artikeln mit sehr hohen Einstandspreis.<br /><br /> Verwendung für Artikel, die ZU-/Abschlägen unterliegen.<br /><br /> Verwendung für Artikel mit Seriennummern.|Der Einstandspreis eines Artikels wird, wie der durchschnittliche Einstandspreis, an jedem Zeitpunkt nach einem Kauf berechnet.<br /><br /> Für Lagerbewertung setzt man voraus, dass alle Bestände gleichzeitig verkauft werden.|  
|Standard|Wird verwendet, wo Kostenkontrolle kritisch ist.<br /><br /> Verwendung in der wiederholenden Produktion, die Kosten des Fertigungsmaterials, direkte Arbeit und Produktionsgemeinkosten zu bewerten.<br /><br /> Wird verwendet, wo es Kategorie und Mitarbeiter gibt, um die Vorgaben beizubehalten.|Der Einstandspreis eines Artikels ist voreingestellt basierend auf vorkalkulierten Kosten.<br /><br /> Wenn die Ist-Kosten später realisiert werden, muss der Einstandspreis (fest) auf die Ist-Kosten durch Abweichungswerte reguliert werden.|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)   
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

