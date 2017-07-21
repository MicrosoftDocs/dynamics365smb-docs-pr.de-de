---
title: "Verkaufsaufträge und Lagerplanungserweiterung verwenden, um das Lager zu verwalten | Microsoft Docs"
description: "Diese Erweiterung hilft Ihnen, Verkäufe zu planen und eine klare Übersicht über erwartete fehlende Lagerbestände zu erhalten und hilft Ihnen sogar dabei, Lagerauffüllungsanfragen an Verkäufer zu stellen."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a0cac0236611c90d3d1fdf1bae9deaaeb235b540
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a>Geplanter voraussichtlicher Verkauf und Lagerbestand für Dynamics 365 for Financials
Lagerverwaltung ist ein Austausch zwischen Serviceabteilung und Verwaltung der Kosten. Auf der einen Seite benötigt ein niedriger Bestand weniger Betriebskapital, andererseits führen fehlende Lagerbestände evtl. zu entgangenen Verkäufen. Die Erweiterung "Geplanter voraussichtlicher Verkauf und Lagerbestand" sagt potenzielle Verkäufe anhand der historischen Daten voraus und gibt eine klare Übersicht über erwartete fehlende Lagerbestände. Auf Grundlage der Planung helfen die Erweiterungen dabei, Beschaffungsanfragen an Ihre Kreditoren zu stellen und Zeit zu spraren.  

## <a name="setting-up-forecasting"></a>Einrichten der Planung
In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist die Verknüpfung zu [Cortana-Intelligenz](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) bereits eingerichtet. Sie können jedoch die Planung konfigurieren, um eine andere Art von Periode zu erfassen, zum Beispiel von der Planung nach Monaten auf die Planung nach Quartal. Sie können außerdem die Anzahl von Perioden zur Berechnung der Planung festlegen, abhängig davon, wie differenziert die Planung sein soll. Wir empfehlen, dass Sie die Planung nach Monaten und über einen Zeitraum von 12 Monaten prognostizieren.  

## <a name="using-the-forecasts"></a>Planungen verwenden
Die Erweiterung verwendet Cortana Intelligence, um künftige Verkäufe basierend auf dem Verkaufsverlauf vorauszusagen und so fehlenden Lagerbestand zu vermeiden. Wenn Sie beispielsweise einen Artikel im Fenster **Artikel** auswählen, zeigt das Diagramm im Bereich **Artikelplanung** die geschätzten Verkäufe dieses Artikels in der kommenden Periode an. Auf diese Weise können Sie sehen, ob der Artikel evtl. in Kürze nicht mehr am Lager sein wird.  

Sie können auch die Erweiterung verwenden, um vorzuschlagen, wann der Lagerbestand aufgefüllt werden soll. Wenn Sie beispielsweise eine Einkaufsbestellung für Fabrikam erstellen, da Sie deren neuen Schreibtischstuhl kaufen möchten, wird die Erweiterung "Geplanter voraussichtlicher Verkauf und Lagerbestand" vorschlagen, dass Sie ebenfalls den LONDON-Schreibtischstuhl wiedereinlagern, den Sie üblicherweise von diesem Kreditor kaufen. Der Grund dafür ist, dass die Erweiterung vorausplant, dass der LONDON-Schreibtischstuhl in den kommenden zwei Monaten nicht mehr am Lager verfügbar sein wird und Sie bereits jetzt mehr Stühle bestellen sollten.  

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  

