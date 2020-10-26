---
title: Lieferkettenplanung | Microsoft Docs
description: Vorbereiten eines ausführlichen ausführbaren Plan und der Montageplan für Verkäufe und Produktionsbedarf.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 565b12c884ebc144174307a6d6dd893915d042cb
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919063"
---
# <a name="planning"></a>Planung

Die Produktionsschritte, die ausgeführt werden müssen, um das Ausgangsmaterial zu Fertigerzeugnissen zu verarbeiten, müssen – abhängig von Volumen und Art der Produkte – täglich oder wöchentlich geplant werden. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügt über Features zum Erfüllen des erwarteten und tatsächlichen Bedarfs von Verkauf und Produktion sowie über Verteilungsplanungsfeatures, die die Verwendung von Lagerhaltungsdaten und Umlagerungen zwischen Lagerorten ermöglichen.

> [!NOTE]
> Dieses Thema beschreibt die Planung für Unternehmen, die mit der Fertigung oder Montageverwaltung zu tun haben, wenn die resultierenden Beschaffungsaufträge entweder Produktion, Montage, Umlagerung oder Einkaufsbestellungen sein können. Die Hauptschnittstelle für diese Planungsarbeiten ist die Seite **Planungsvorschlag**
>
> [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt auch Beschaffungsplanung für Großhandelsmandanten, in denen Beschaffungsaufträge und die resultierende Umlagerung nur Einkaufsbestellungen sein können. Die für diese Hauptschnittstelle Planungsarbeiten ist die **Bestellvorschlag** Seite, die indirekt in diesem Thema beschrieben wird, während die meisten Planungsfunktionalität auf beide Vorschläge gehört.

Planung kann als die Vorbereitung der erforderlichen Beschaffungsaufträge in den Einkaufs-, Montage- oder Fertigungsabteilungen zur Erfüllung des Bedarfs angesehen werden. Weitere Informationen finden Sie unter [Einkauf](purchasing-manage-purchasing.md), [Montageverwaltung](assembly-assemble-items.md) und [Produktion](production-manage-manufacturing.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben.  

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Erhalten einer kurzen Einführung, wie das Planungssystem verwendet werden kann, um Nachfrage zu erkennen und zu priorisieren und einen ausgewogenen Beschaffungsplan vorzuschlagen,.|[Info zu Planungsfunktionen](production-about-planning-functionality.md)|
|Erläutert, wie das Planungssystem arbeitet und wie die Algorithmen angepasst werden, um Planungsbedingungen in verschiedenen Umgebungen zu erfüllen.|[Designdetails: Vorratsplanung](design-details-supply-planning.md)|
|Erhalten von Informationen zur Planungslogikabweichung zwischen dem Bedarf an Lagerplätzen gemäß den Einstellungen der Lagerhaltungsdaten und dem Bedarf ohne Lagerortcodes|[Planung mit/ohne Lagerortcodes](production-planning-with-without-locations.md)|
|Prognostizieren den Fertigungsbedarf, der durch erwartete Verkaufs- und Fertigungskomponenten dargestellt wird.|[Bedarfsplanung erstellen](production-how-to-create-a-forecast.md)|  
|Automatisches exaktes Erstellen von Fertigungsaufträgen auf der Grundlage von Aufträgen, um den exakten Bedarf der Auftragszeile abzudecken|[Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:](production-how-to-create-production-orders-from-sales-orders.md)|
|Direktes Erstellen eines Projektfertigungsauftrags auf der Grundlage eines mehrzeiligen Auftrags, bei dem es sich um Fertigungsprojekt handelt|[Projektaufträge planen](production-how-to-plan-project-orders.md)|
|Manuelles Planen für Verkaufs- oder Fertigungsbedarf pro einzelner Stücklistenebene mithilfe der Seite **Auftragsplanung**|[Planung der Bestellung eines neuen Bedarfs von Auftrag](production-how-to-plan-for-new-demand.md)|
|Verwenden Sie die Seite **Planungsvorschlag** , um die Felder Prod.-Programmplanung und Nettobedarfsoptionen auszuführen, einen oder ausführlichen Beschaffungsplans auf hoher Ebene in allen Artikelebenen automatisch zu erstellen.|[Führen Sie eine vollständige Planung, Prod.-Programmplanung oder Nettobedarf aus](production-how-to-run-mps-and-mrp.md)|
|Nutzen Sie die Seite **Anforderungsarbeitsblatt** zum automatischen Erstellen eines ausführlichen Beschaffungsplans, um den Bedarf für Artikel zu decken, die ausschließlich per Einkauf oder Umlagerung beschafft werden.|[Anforderungsarbeitsblatt](production-about-planning-functionality.md#requisition-worksheet)|  
|Initiieren oder Aktualisieren eines Fertigungsauftrags in Form grobterminierter Arbeitsgänge im Produktionsplan|[Neugestaltungs- oder direkt Aktualisierung von Fertigungsaufträgen](production-how-to-replan-refresh-production-orders.md)|
|Berechnen Sie Arbeits- oder Arbeitsplatzkalender aufgrund von Planungsänderungen.|[Einen Arbeitsplatzgruppenkalender berechnen](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist|[Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat.](production-how-track-demand-supply.md)|
|Anzeigen des voraussichtlich verfügbaren Lagerbestands eines Artikels in verschiedenen Ansichten und Anzeigen des beeinflussenden Bruttobedarfs sowie der beeinflussenden geplanten Auftragseingänge und anderer Ereignisse im Laufe der Zeit|[Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)|  
<!--|Wählen Sie Planungsaktivitäten wie ändern oder hinzufügen von Planungsvorschlagszeilen, in einer grafischen Ansicht des Beschaffungsplans aus.|[Ändern von Planungsvorschlägen in einer grafischen Ansicht](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|-->

## <a name="see-also"></a>Siehe auch

[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)  
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
