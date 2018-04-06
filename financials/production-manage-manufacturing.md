---
title: "Ausführen der Produktion aus | Microsoft Docs"
description: "Nach der Ausgabe des Materials kann mit den eigentlichen Fertigungsarbeitsgängen begonnen werden. Diese können dann in der Reihenfolge ausgeführt werden, die im FA-Arbeitsplan definiert ist."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: e358e505977e2229ad7f7338fb22e0d8075b0aa9
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="manufacturing"></a>Produktion
Nach der Ausgabe des Materials kann mit den eigentlichen Fertigungsarbeitsgängen begonnen werden. Diese können dann in der Reihenfolge ausgeführt werden, die im FA-Arbeitsplan definiert ist.  

Ein aus Systemsicht wichtiger Aspekt beim Ausführen der Produktion ist das Buchen der Istmeldung in die Datenbank, um den Status zu melden, sowie das Aktualisieren des Lagerbestands mit den fertig gestellten Artikeln. Istmeldungsbuchungen können manuell, also durch Ausfüllen und Buchen von Buch.-Blattzeilen nach Ausführen von Fertigungsarbeitsgängen, vorgenommen werden. Alternativ können die Buchungen auch mithilfe der Buchungsmethode "Rückwärts" gebucht werden. In diesem Fall wird der Materialverbrauch automatisch zusammen mit der Istmeldung gebucht, wenn der Status des Fertigungsauftrags zu "Beendet" geändert wird.  

Als Alternative zum Stapelbuchungsblatt für die Istmeldungsbuchung mehrerer Fertigungsaufträge können Sie das Fenster **Produktions Buch.-Blatt** verwenden, um Verbrauch und/oder Istmeldung für eine Fertigungsauftragszeile zu buchen.

Bevor Sie mit der Fertigung von Artikeln beginnen können, müssen Sie Mehreres einrichten, wie beispielsweise Arbeitsplatzgruppen, Arbeitspläne und Fertigungsstücklisten. Weitere Informationen finden Sie unter [Einrichten von Produktion](production-configure-production-processes.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Verstehen Sie, wie Fertigungsaufträge arbeiten.|[Info zu Fertigungsaufträgen](production-about-production-orders.md)|
|Manuelles Erstellen von Produktionsaufträgen.|[Fertigungsauftrag erstellen](production-how-to-create-production-orders.md)|
|Lagern Sie alle oder ausgewählte Arbeitsgänge im Fertigungsauftrag an einen Subunternehmer aus.|[Fertigung durch Fremdarbeitsvertrag](production-how-to-subcontract-manufacturing.md)|
|Erfassen und Buchen der fertig gestellten Menge – zusammen mit Materialverbrauch und Zeitaufwand – für eine einzelne freigegebene Fertigungsauftragszeile.|[Verbrauch und Ausgabe für den freigegebenen Fertigungsauftrag buchen.](production-how-to-register-consumption-and-output.md)|  
|Stapelbuchung der Komponenten pro Arbeitsgang in einem Buch.-Blatt, die verschiedene Fertigungsaufträge verarbeiten kann.|[Buchen Sie den Verbrauch über Stapelverarbeitung.](production-how-to-post-consumption.md)|
|Stapelbuchung der Komponenten pro Arbeitsgang in einem Buch.-Blatt, die verschiedene Fertigungsaufträge verarbeiten kann, buchen.|[Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen](production-how-to-post-output-quantity.md)|  
|Buchen der Anzahl von Artikeln, die in den einzelnen abgeschlossenen Arbeitsgängen gefertigt wurden und nicht als fertig gestellte Menge, sondern als Ausschussmaterial betrachtet werden|[Buchen Sie Ausschuss](production-how-to-post-scrap.md)|
|Anzeigen der Fertigungsbereichsauslastung aufgrund geplanter und freigegebener Fertigungsaufträge.|[Anzeigen der Auslastung der Arbeitsplätze und Arbeitsplatzgruppen](production-how-to-view-the-load-on-work-centers.md)|      
|Buchen verbrauchter Kapazitäten, die keinem Fertigungsauftrag zugeordnet sind (beispielsweise Wartungsarbeiten), mithilfe des Fensters **Kapazitäts Buch.-Blatt**|[Kapazität buchen](production-how-to-post-capacities.md)|  
|Berechnen und Regulieren der Kosten für gefertigte Artikel und verbrauchte Komponenten zur finanziellen Abstimmung|[Info zu Kosten des beendeten Auftrags](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Siehe auch  
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

