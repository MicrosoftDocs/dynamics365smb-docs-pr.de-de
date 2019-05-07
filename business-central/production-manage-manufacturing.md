---
title: Ausführen der Produktion aus | Microsoft Docs
description: Nach der Ausgabe des Materials kann mit den eigentlichen Fertigungsarbeitsgängen begonnen werden. Diese können dann in der Reihenfolge ausgeführt werden, die im FA-Arbeitsplan definiert ist.
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
ms.openlocfilehash: 57fef211c6e0336edca60985757626c23932a3ae
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "911931"
---
# <a name="manufacturing"></a>Produktion
> [!NOTE]
> Die Funktionalität, die in diesem Thema und in Vorthemen beschrieben, handelt in der Benutzeroberfläche nur angezeigt, wenn Sie die **Premium** haben. Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).

Nach der Ausgabe des Materials kann mit den eigentlichen Fertigungsarbeitsgängen begonnen werden. Diese können dann in der Reihenfolge ausgeführt werden, die im FA-Arbeitsplan definiert ist.  

Ein aus Systemsicht wichtiger Aspekt beim Ausführen der Produktion ist das Buchen der Istmeldung in die Datenbank, um den Status zu melden, sowie das Aktualisieren des Lagerbestands mit den fertig gestellten Artikeln. Istmeldungsbuchungen können manuell, also durch Ausfüllen und Buchen von Buch.-Blattzeilen nach Ausführen von Fertigungsarbeitsgängen, vorgenommen werden. Alternativ können die Buchungen auch mithilfe der Buchungsmethode "Rückwärts" gebucht werden. In diesem Fall wird der Materialverbrauch automatisch zusammen mit der Istmeldung gebucht, wenn der Status des Fertigungsauftrags zu "Beendet" geändert wird.  

Als Alternative zum Stapelbuchungsblatt für die Istmeldungsbuchung mehrerer Fertigungsaufträge können Sie die Seite **Produktions Buch.-Blatt** verwenden, um Verbrauch und/oder Istmeldung für eine Fertigungsauftragszeile zu buchen.

Bevor Sie mit der Fertigung von Artikeln beginnen können, müssen Sie Mehreres einrichten, wie beispielsweise Arbeitsplatzgruppen, Arbeitspläne und Fertigungsstücklisten. Weitere Informationen finden Sie unter [Einrichten von Produktion](production-configure-production-processes.md).

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Verstehen Sie, wie Fertigungsaufträge arbeiten.|[Info zu Fertigungsaufträgen](production-about-production-orders.md)|
|Manuelles Erstellen von Produktionsaufträgen.|[Fertigungsauftrag erstellen](production-how-to-create-production-orders.md)|
|Lagern Sie alle oder ausgewählte Arbeitsgänge im Fertigungsauftrag an einen Subunternehmer aus.|[Fertigung durch Fremdarbeitsvertrag](production-how-to-subcontract-manufacturing.md)|
|Erfassen und Buchen der fertig gestellten Menge – zusammen mit Materialverbrauch und Zeitaufwand – für eine einzelne freigegebene Fertigungsauftragszeile.|[Verbrauch und Ausgabe für den freigegebenen Fertigungsauftrag buchen.](production-how-to-register-consumption-and-output.md)|  
|Stapelbuchung der Komponenten pro Arbeitsgang in einem Buch.-Blatt, die verschiedene Fertigungsaufträge verarbeiten kann.|[Buchen Sie den Verbrauch über Stapelverarbeitung.](production-how-to-post-consumption.md)|
|Stapelbuchung der Komponenten pro Arbeitsgang in einem Buch.-Blatt, die verschiedene Fertigungsaufträge verarbeiten kann, buchen.|[Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen](production-how-to-post-output-quantity.md)|
|Machen Sie die Ausgabe rückgängig, zum Beispiel aufgrund eines Dateneingabefehlers und eines falschen Betrags.  |[Gebuchte fertig gestellte Menge stornieren](production-how-to-reverse-output-posting.md)|  
|Buchen der Anzahl von Artikeln, die in den einzelnen abgeschlossenen Arbeitsgängen gefertigt wurden und nicht als fertig gestellte Menge, sondern als Ausschussmaterial betrachtet werden|[Buchen Sie Ausschuss](production-how-to-post-scrap.md)|
|Anzeigen der Fertigungsbereichsauslastung aufgrund geplanter und freigegebener Fertigungsaufträge.|[Anzeigen der Auslastung der Arbeitsplätze und Arbeitsplatzgruppen](production-how-to-view-the-load-on-work-centers.md)|      
|Buchen verbrauchter Kapazitäten, die keinem Fertigungsauftrag zugeordnet sind (beispielsweise Wartungsarbeiten), mithilfe der Seite **Kapazitäts Buch.-Blatt**|[Kapazität buchen](production-how-to-post-capacities.md)|  
|Berechnen und Regulieren der Kosten für gefertigte Artikel und verbrauchte Komponenten zur finanziellen Abstimmung|[Info zu Kosten des beendeten Auftrags](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Siehe auch  
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
