---
title: Verkaufsaufträge und Lagerplanungserweiterung verwenden, um das Lager zu verwalten | Microsoft Docs
description: Diese Erweiterung hilft Ihnen, Verkäufe zu planen und eine klare Übersicht über erwartete fehlende Lagerbestände zu erhalten und hilft Ihnen sogar dabei, Lagerauffüllungsanfragen an Verkäufer zu stellen.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 3ae36c5cb7f1738bded3947c99c197221a621f07
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "799048"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>Die Verkaufs- und Bestandprognosen-Erweiterung
Lagerverwaltung ist ein Austausch zwischen Serviceabteilung und Verwaltung der Kosten. Auf der einen Seite benötigt ein niedriger Bestand weniger Betriebskapital, andererseits führen fehlende Lagerbestände evtl. zu entgangenen Verkäufen. Die Erweiterung "Geplanter voraussichtlicher Verkauf und Lagerbestand" sagt potenzielle Verkäufe anhand der historischen Daten voraus und gibt eine klare Übersicht über erwartete fehlende Lagerbestände. Auf Grundlage der Planung helfen die Erweiterungen dabei, Beschaffungsanfragen an Ihre Kreditoren zu stellen und Zeit zu spraren.  

## <a name="setting-up-forecasting"></a>Einrichten der Planung
In [!INCLUDE[d365fin](includes/d365fin_md.md)] ist die Verknüpfung zu [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) bereits eingerichtet. Sie können jedoch die Planung konfigurieren, um eine andere Art von Periode zu erfassen, zum Beispiel von der Planung nach Monaten auf die Planung nach Quartal. Sie können außerdem die Anzahl von Perioden zur Berechnung der Planung festlegen, abhängig davon, wie differenziert die Planung sein soll. Wir empfehlen, dass Sie die Planung nach Monaten und über einen Zeitraum von 12 Monaten prognostizieren.  

## <a name="using-the-forecasts"></a>Planungen verwenden
Die Erweiterung verwendet Cortana Intelligence, um künftige Verkäufe basierend auf dem Verkaufsverlauf vorauszusagen und so fehlenden Lagerbestand zu vermeiden. Wenn Sie beispielsweise einen Artikel auf der Seite **Artikel** auswählen, zeigt das Diagramm im Bereich **Artikelplanung** die geschätzten Verkäufe dieses Artikels in der kommenden Periode an. Auf diese Weise können Sie sehen, ob der Artikel evtl. in Kürze nicht mehr am Lager sein wird.  

Sie können auch die Erweiterung verwenden, um vorzuschlagen, wann der Lagerbestand aufgefüllt werden soll. Wenn Sie beispielsweise eine Einkaufsbestellung für Fabrikam erstellen, da Sie deren neuen Schreibtischstuhl kaufen möchten, wird die Erweiterung "Geplanter voraussichtlicher Verkauf und Lagerbestand" vorschlagen, dass Sie ebenfalls den LONDON-Schreibtischstuhl wiedereinlagern, den Sie üblicherweise von diesem Kreditor kaufen. Der Grund dafür ist, dass die Erweiterung vorausplant, dass der LONDON-Schreibtischstuhl in den kommenden zwei Monaten nicht mehr am Lager verfügbar sein wird und Sie bereits jetzt mehr Stühle bestellen sollten.  

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
