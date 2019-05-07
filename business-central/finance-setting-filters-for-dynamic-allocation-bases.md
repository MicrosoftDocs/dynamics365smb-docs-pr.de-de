---
title: Setzen von Filtern für dynamische Zuteilungsgrundlagen | Microsoft Docs
description: Die Methode der dynamischen Zuteilung basiert auf veränderbaren Werten. Zum Beispiel die Anzahl der Mitarbeiter in einer Kostenstelle oder die Artikel eines Kostenträgers, die in einem bestimmten Zeitraum verkauft wurden. Es gibt neun vordefinierte Zuteilungsgrundlagen und zwölf dynamische Datumsbereiche. Die verschiedenen Filter werden basierend auf der Zuteilungsgrundlage eingestellt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 35f9a542d57bfe27c9a9ee48f4a41af7071cdd47
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935496"
---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Setzen von Filtern für dynamische Zuteilungsgrundlagen
Die Methode der dynamischen Zuteilung basiert auf veränderbaren Werten. Zum Beispiel die Anzahl der Mitarbeiter in einer Kostenstelle oder die Artikel eines Kostenträgers, die in einem bestimmten Zeitraum verkauft wurden. Es gibt neun vordefinierte Zuteilungsgrundlagen und zwölf dynamische Datumsbereiche. Die verschiedenen Filter werden basierend auf der Zuteilungsgrundlage eingestellt.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Setzen von Filtern für dynamische Zuteilungsgrundlagen  
 Die nachstehende Tabelle zeigt, welche Filter für verschiedene Zuteilungsgrundlagen möglich sind und welche Werte in den Feldern **Filter-Nr.** und **Gruppenfilter** gültig sind. Drücken Sie F1 im Feld **Datenfiltercode**, um detaillierte Beschreibungen zu lesen.  

|**Bemessungsgrundlage**|**Nr. Filter**|**Datumsfiltercode**|**Kostenstellenfilter**|**Kostenträgerfilter**|**Gruppenfilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Sachposten|Sachkonto|Ja|Ja|Ja|N/Z|  
|Finanzbudgetposten|Sachkonto|Ja|Ja|Ja|Finanzbudgetname|  
|Kostenartposten|Einstandspreisberechnung|Ja|Ja|Ja|N/Z|  
|Kostenbudgetposten|Einstandspreisberechnung|Ja|Ja|Ja|Budgetname|  
|Anzahl Mitarbeiter|N/Z|Ja|Ja|Ja|N/Z|  
|Verkaufte Artikel (Menge)|Artikelnr.|Ja|Ja|Ja|Lagerbuchungsgruppe|  
|Erworbene Artikel (Menge)|Artikelnr.|Ja|Ja|Ja|Lagerbuchungsgruppe|  
|Verkaufte Artikel (Betrag)|Artikelnr.|Ja|Ja|Ja|Lagerbuchungsgruppe|  
|Erworbene Artikel (Betrag)|Artikelnummer|Ja|Ja|Ja|Lagerbuchungsgruppe|  

## <a name="see-also"></a>Siehe auch  
[Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)
