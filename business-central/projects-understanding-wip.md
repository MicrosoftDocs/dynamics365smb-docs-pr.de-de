---
title: WIP-Methoden für die Berechnung und die Ablaufverfolgung berchnen und aufzeichnen | Microsoft Docs.
description: Beschreibt die unterschiedlichen Umlaufbestand (WIP)-Methoden, die verwendet werden können, um Finanzdaten für Projekte zu senden und zu überwachen, die im Umlaufbestand sind.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8d23cd7ca8badf10bc8c734d84b5142d34ad4362
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748818"
---
# <a name="understanding-wip-methods"></a>Verständnis - WIP-Methoden
Im Laufe eines Projekts werden Material sowie Ressourcen und andere Aufwendungen verbraucht und müssen auf das Projekt gebucht werden. Umlaufbestand (WIP) ist eine Funktion, mit der Sie den finanziellen Wert in der Finanzbuchhaltung schätzen können, solange die Projekte noch nicht abgeschlossen sind. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung des Projekts gebucht. Wurden ausschließlich Aufwendungen gebucht, ergibt sich eine inkorrekte Finanzauswertung.

Zum Überwachen des Werts in der Finanzbuchhaltung können Sie die WIP berechnen und den Wert in der Finanzbuchhaltung buchen. Weitere Informationen finden Sie unter [Überwachen des Auftragsfortschritt und der Leistung](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die folgenden Methoden zum Berechnen der Inventur und der Wert der unfertigen Arbeit.

| WIP-Methode | Formel | Berechnungsbeschreibung |
| --- | --- | --- |
| Einstandswert |Realisierte Einnahmen = Fakturierbarer, verrechneter Preis<br /><br /> Erwarteter Einstandsbetrag = Fakturierbarer Gesamtbetrag x geplanter Einstandspreisanteil<br /><br /> WIP-Kosten = (Prozentsatz der Fertigung -In Rechnung gestellt %) x Erwarteter Einstandsbetrag<br /><br /> Prozentsatz der Fertigung = Gesamtverbrauchskosten / Geplante Gesamtkosten<br /> Fakturiert % = Fakturierbarer verrechneter Preis<br /><br /> Verrechenbarer Gesamtpreis der deklarierten Kosten = Verbrauch Gesamtkosten - WIP |Berechnungen vom Typ "Einstandswert" beginnen mit der Berechnung des Werts dessen, was bereitgestellt wurde. Zu diesem Zweck wird ein Anteil des erwarteten Einstandsbetrags (basierend auf dem Prozentsatz der Fertigstellung) herangezogen. Fakturierte Einstandsbeträge werden abgezogen, indem ein Anteil des erwarteten Einstandsbetrags (basierend auf dem fakturierten Prozentsatz) herangezogen wird.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag", "Plan Gesamtpreis" und "Plan Gesamtkosten" eingegeben werden. |
| Vertriebskosten |Realisierte Einnahmen = Fakturierbarer, verrechneter Preis<br /><br /> Deklarierte Kosten = Plan Gesamtkosten x Fakturierter Prozentbetrag<br /><br /> Fakturiert % = Fakturierbarer Rechnungsbetrag / Fakturierbarer Gesamtpreis<br /><br /> (Fakturiert % ist als Spalte in Projektaufgabenzeilen vorhanden)<br /><br /> WIP-Kosten = Verbrauch (Einstandsbetrag) - deaktivierte Kosten |Berechnungen vom Typ "Vertriebskosten" beginnen mit der Berechnung der deklarierten Kosten. Kosten werden proportional auf der Grundlage von "Plan Gesamtkosten" realisiert.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag" und "Plan Gesamtkosten" eingegeben werden. |
| Verkaufswert |Deaktivierte Kosten = Verbrauch (Einstandsbetrag)<br /><br /> Realisierte Einnahmen = Verbrauch (Verkaufspreis) x geplanter Rechnungsanteil<br /><br /> Kosten Zu-/Abschlag % = Fakturierbarer Gesamtbetrag / Plan Gesamtkosten<br /><br /> WIP Verkäufe = deklarierte Verkäufe - Fakturierbarer Rechnungspreis |Bei Berechnungen vom Typ "Verkaufswert" werden die Einnahmen proportional basierend auf "Verbrauch Gesamtkosten" und dem erwarteten Kostenzu-/-abschlagsanteil realisiert.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag" und "Plan Gesamtkosten" eingegeben werden. |
| Prozentsatz der Fertigung |Deaktivierte Kosten = Verbrauch (Einstandsbetrag)<br /><br /> Realisierte Einnahmen = Fakturierbarer Gesamtbetrag x Prozentsatz der Fertigung<br /><br /> Prozentsatz der Fertigung = Gesamtverbrauchskosten / Geplante Gesamtkosten<br /> (Wird in Projektplanungszeilen als "Kosten Abschluss %" angegeben)<br /><br /> WIP Verkäufe = deklarierte Verkäufe - Fakturierbarer Rechnungspreis |Bei Berechnungen vom Typ "Prozentsatz der Fertigung" werden Einnahmen proportional – auf der Grundlage des Prozentsatzes der Fertigstellung, also "Verbrauch" contra "Einstandspreis" – realisiert.<br /><br /> Damit korrekte Ergebnisse erzielt werden können, müssen für das gesamte Projekt Werte für "Fakturierbarer Gesamtbetrag" und "Plan Gesamtkosten" eingegeben werden. |
| Abgeschl. Vertrag |WIP-Betrag = WIP-Einstandsbetrag = Verbrauch (Einstandsbetrag)<br /><br /> WIP-Verkaufsbetrag = Fakturierbarer (Rechnungsbetrag) |Bei der Option "Abgeschl. Vertrag" werden Einnahmen und Kosten erst nach Abschluss des Projekts realisiert. Dies kann nützlich sein, wenn die Schätzungen der Kosten und Einnahmen für das Projekt äußerst unsicher sind.<br /><br /> Der gesamte Verbrauch wird auf das Konto für Kosten nicht abgeschlossener Arbeiten (Aktiva) gebucht, und alle fakturierten Verkäufe werden auf das Konto für fakturierte Verkäufe nicht abgeschlossener Arbeiten (Passiva) gebucht, bis das Projekt abgeschlossen ist. |

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
