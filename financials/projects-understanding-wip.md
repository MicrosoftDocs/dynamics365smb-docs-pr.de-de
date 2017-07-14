---
title: WIP-Methoden verstehen| Microsoft Docs
description: "Beschreibt die unterschiedlichen WIP-Methoden, die verwendet werden können, um Finanzdaten für Projekte zu senden und zu überwachen, die im Umlaufbestand sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d6f82b3eb086b53be8a091e7a805c745a74ac10f
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Verständnis - WIP-Methoden
<a id="understanding-wip-methods" class="xliff"></a>
[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt die folgenden Methoden zum Berechnen der Inventur und der Wert der unfertigen Arbeit.

| WIP-Methode | Formel | Berechnungsbeschreibung |
| --- | --- | --- |
| Einstandswert |Realisierte Einnahmen = Fakturierbarer, verrechneter Preis<br /><br /> Erwarteter Einstandsbetrag = Fakturierbarer Gesamtbetrag x geplanter Einstandspreisanteil<br /><br /> WIP-Kosten = \((Prozentsatz der Fertigung -In Rechnung gestellt %)\) x Erwarteter Einstandsbetrag<br /><br /> Prozentsatz der Fertigung = Gesamtverbrauchskosten / Geplante Gesamtkosten<br /> Fakturiert % = Fakturierbarer verrechneter Preis<br /><br /> Verrechenbarer Gesamtpreis der deklarierten Kosten = Verbrauch Gesamtkosten - WIP |Berechnungen vom Typ "Einstandswert" beginnen mit der Berechnung des Werts dessen, was bereitgestellt wurde. Zu diesem Zweck wird ein Anteil des erwarteten Einstandsbetrags (basierend auf dem Prozentsatz der Fertigstellung) herangezogen. Fakturierte Einstandsbeträge werden abgezogen, indem ein Anteil des erwarteten Einstandsbetrags (basierend auf dem fakturierten Prozentsatz) herangezogen wird.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag", "Plan Gesamtpreis" und "Plan Gesamtkosten" eingegeben werden. |
| Vertriebskosten |Realisierte Einnahmen = Fakturierbarer, verrechneter Preis<br /><br /> Deklarierte Kosten = Plan Gesamtkosten x Fakturierter Prozentbetrag<br /><br /> Fakturiert % = Fakturierbarer Rechnungsbetrag / Fakturierbarer Gesamtpreis<br /><br /> \(Fakturiert % ist als Spalte in Projektaufgabenzeilen vorhanden\)<br /><br /> WIP-Kosten = Verbrauch (Einstandsbetrag) - deaktivierte Kosten |Berechnungen vom Typ "Vertriebskosten" beginnen mit der Berechnung der deklarierten Kosten. Kosten werden proportional auf der Grundlage von "Plan Gesamtkosten" realisiert.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag" und "Plan Gesamtkosten" eingegeben werden. |
| Verkaufswert |Deaktivierte Kosten = Verbrauch (Einstandsbetrag)<br /><br /> Realisierte Einnahmen = Verbrauch (Verkaufspreis) x geplanter Rechnungsanteil<br /><br /> Kosten Zu-/Abschlag % = Fakturierbarer Gesamtbetrag / Plan Gesamtkosten<br /><br /> WIP Verkäufe = deklarierte Verkäufe - Fakturierbarer Rechnungspreis |Bei Berechnungen vom Typ "Verkaufswert" werden die Einnahmen proportional basierend auf "Verbrauch Gesamtkosten" und dem erwarteten Kostenzu-/-abschlagsanteil realisiert.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag" und "Plan Gesamtkosten" eingegeben werden. |
| Prozentsatz der Fertigung |Deaktivierte Kosten = Verbrauch (Einstandsbetrag)<br /><br /> Realisierte Einnahmen = Fakturierbarer Gesamtbetrag x Prozentsatz der Fertigung<br /><br /> Prozentsatz der Fertigung = Gesamtverbrauchskosten / Geplante Gesamtkosten<br /> \(Wird in Projektplanungszeilen als "Kosten Abschluss %" angegeben\)<br /><br /> WIP Verkäufe = deklarierte Verkäufe - Fakturierbarer Rechnungspreis |Bei Berechnungen vom Typ "Prozentsatz der Fertigung" werden Einnahmen proportional – auf der Grundlage des Prozentsatzes der Fertigstellung, also "Verbrauch" contra "Einstandspreis" – realisiert.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag" und "Plan Gesamtkosten" eingegeben werden. |
| Abgeschl. Vertrag |WIP-Betrag = WIP-Einstandsbetrag = Verbrauch \(Gesamtkosten\)<br /><br /> WIP-Verkaufsbetrag = Fakturierbarer \(Rechnungsbetrag\) |Bei der Option "Abgeschl. Vertrag" werden Einnahmen und Kosten erst nach Abschluss des Projekts realisiert. Dies kann nützlich sein, wenn die Schätzungen der Kosten und Einnahmen für das Projekt äußerst unsicher sind.<br /><br /> Der gesamte Verbrauch wird auf das Konto für Kosten nicht abgeschlossener Arbeiten \(Aktiva\) gebucht, und alle fakturierten Verkäufe werden auf das Konto für fakturierte Verkäufe nicht abgeschlossener Arbeiten \(Passiva\) gebucht, bis das Projekt abgeschlossen ist. |

## Siehe auch
<a id="see-also" class="xliff"></a>
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

