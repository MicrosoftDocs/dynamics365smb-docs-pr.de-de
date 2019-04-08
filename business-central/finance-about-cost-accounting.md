---
title: Informationen zur Kostenrechnung | Microsoft Docs
description: Kostenrechnung wird verwendet, um Ihnen dabei zu helfen, die Kosten des Betriebs eines Geschäftes zu erkennen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d7eafb21bbcf6c4b446f02b3a33ff6349c2d415d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799018"
---
# <a name="about-cost-accounting"></a>Informationen zur Kostenrechnung
Kostenrechnung wird verwendet, um Ihnen dabei zu helfen, die Kosten des Betriebs eines Geschäftes zu erkennen. Kostenrechnungsinformationen sollen Folgendes analysieren:  

-   Welche Kostenarten fallen beim Betreiben eines Geschäfts an?  
-   Wird fallen die Kosten an?  
-   Wer trägt die Kosten?  

In der Kostenrechnung weisen Sie aktuelle und geplante Kosten für Betrieb, Abteilungen, Produkte und Projekte zu, um die Profitabilität Ihres Unternehmens zu analysieren.  

## <a name="workflow-in-cost-accounting"></a>Workflow der Kostenrechnung  
Kostenrechnung hat folgende Hauptkomponenten:  

-   Kostenarten, Kostenstellen und Kostenträger  
-   Kostenposten und Kosten-Buch.-Blätter  
-   Kostenzuteilungen  
-   Kostenbudgets
-   Kostenberichte  

Das folgende Diagramm zeigt den Workflow der Kostenrechnung.  

![Kostenrechnungsübersicht](media/costaccountingoverview.png "CostAccountingOverview")  

## <a name="cost-types-cost-centers-and-cost-objects"></a>Kostenarten, Kostenstellen und Kostenträger  
Sie definieren Kostenarten, Kostenstellen und Kostenträger, um zu analysieren, worin die Kosten bestehen, woher die Kosten stammen und wer die Kosten trägt.  

Sie definieren einen Kostenartenplan mit einer Struktur und Funktion ähnlich dem Sachkontenplan. Sie können die GuV-Konten des Sachkontos übertragen oder Ihren eigenen Kostenartenplan erstellen.  

Kostenstellen sind Abteilungen und Profiteinheiten, die für die Kosten und die Einnahmen zuständig sind. Häufig sind mehr Kostenstellen in der Kostenrechnung als in jeder Dimension eingerichtet, die im Sachkonto eingerichtet ist. Im Sachkonto werden normalerweise nur die Kostenstellen der ersten Ebene für direkte Kosten und die ursprünglichen Kosten verwendet. In der Kostenrechnung werden zusätzliche Kostenstellen für zusätzliche Zuteilungsebenen erstellt.  

Kostenträger sind Produkte, Produktgruppen oder Services eines Unternehmens. Dies sind die Fertigartikel eines Unternehmens, die die Kosten tragen.  

Sie können Kostenstellen mit Abteilungen und Kostenträger mit Projekten in Ihrem Unternehmen verknüpfen. Sie können jedoch Kostenstellen und Kostenträger mit sämtlichen Dimensionen im Sachkonto verknüpfen und sie mit Zwischensummen und Titeln ergänzen.  

## <a name="cost-entries-and-cost-journals"></a>Kostenposten und Kosten-Buch.-Blätter  
Betriebskosten können aus dem Sachkonto übertragen werden. Sie können die Kostenposten aus dem Sachkonto automatisch auf Kostenposten bei jeder Buchung übertragen. Sie können einen Batchauftrag auch verwenden, um die Sachposten auf die Kostenposten basierend auf täglichen oder monatlichen Sammelbuchungen zu übertragen.  

In Kosten-Buch.-Blättern können Sie Kosten und Aktivitäten buchen, die weder aus dem Sachkonto stammen noch durch Verteilungen erzeugt werden. Beispielsweise können Sie reine Betriebskosten, Inlandsabgaben, Zuordnungen und Korrekturposten einzeln zwischen Kostenarten, Kostenstellen und Kostenträgern oder auf wiederkehrender Basis buchen.  

## <a name="cost-allocations"></a>Kostenzuteilungen  
Zuteilungen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Gemeinkosten werden zuerst auf den Kostenstellen gebucht und zu einem späteren Zeitpunkt auf Kostenträger berechnet. Dies kann beispielsweise in einer Verkaufsabteilung ausgeführt werden, die eine Reihe von Produkten gleichzeitig verkauft. Direkte Kosten sind die Kosten, die einem Kostenträger direkt zugeordnet werden können, zum Beispiel der Materialeinkauf für ein bestimmtes Produkt.  

Die verwendete Zuteilungsgrundlage und die Genauigkeit der Zuteilungsdefinition haben einen Einfluss auf die Ergebnisse aus Kostenzuteilungen. Die Zuteilungsdefinition wird verwendet, um Kosten zuerst von so genannten Vor-Kostenstellen zu den Hauptkostenstellen und dann von Kostenstellen zu Kostenträgern zuzuordnen.  

Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Sie können tatsächliche Werte oder geplante Werte zuordnen, indem Sie die Methode der statischen Verteilung verwenden, die auf einem bestimmten Wert basiert, wie Fläche oder ein eingerichtetes Zuteilungsverhältnis von 5:2:4. Sie können auch tatsächliche Werte oder geplante Werte zuordnen, indem Sie die Methode der dynamischen Verteilung mit neun vordefinierten Zuteilungsgrundlagen und 12 dynamischen Datenbereichen verwenden.  

## <a name="cost-budgets"></a>Kostenbudgets  
Sie können beliebig viele Kostenbudgets erstellen. Sie können das Kostenbudget ins Sachkontobudget kopieren und umgekehrt. Sie können geplante Kosten als Ist-Kosten übertragen.  

## <a name="cost-reporting"></a>Kostenberichte  
Die meisten Berichte und Statistiken basieren auf den gebuchten Kostenposten. Sie können die Sortierung der Ergebnisse einrichten und Filter verwenden, um zu definieren, welche Daten angezeigt werden müssen. Sie können Berichte für eine Kostenaufteilungsanalyse erstellen. Darüber hinaus können Sie die Standard-Kontenschemata verwenden, um festzulegen, wie die Berichte für den Kostenartenplan angezeigt werden sollen.  

## <a name="see-also"></a>Siehe auch  
 [Kostenrechnung](finance-manage-cost-accounting.md)  
 [Finanzen](finance.md)   
 [Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
