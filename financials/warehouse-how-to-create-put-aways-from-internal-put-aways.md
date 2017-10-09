---
title: 'Vorgehensweise: Einlagerungen aus internen Einlagerungsanforderungen erstellen | Microsoft Docs'
description: "Nachdem Artikel eingelagert wurden und bevor sie kommissioniert werden, um einen Fertigungsauftrag oder einen Warenausgang zu bedienen, sind sie im Lager ein Teil des verfügbaren Lagerbestands."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6829c5a67f1121ecc135e1183af78b0e602f8f
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-and-put-away-without-a-source-document"></a>Vorgehensweise: Wählen und setzen Sie die Einlagerung verwendet ohne Herkunftsbeleg
Nachdem Artikel eingelagert wurden und bevor sie kommissioniert werden, um einen Fertigungsauftrag oder einen Warenausgang zu bedienen, sind sie im Lager ein Teil des verfügbaren Lagerbestands.  

In manchen Situationen müssen Artikel vorübergehend aus den Kommissionierlagerplätzen entnommen werden, um z. B. als Vorführartikel in einer Verkaufspräsentation zu dienen. Diese Artikel gehören immer noch dem Unternehmen und sind Teil des Lagerbestands, sind allerdings nicht für die Kommissionierung verfügbar. Sie werden an einem Lagerplatz für spezielle Zweckes erfasst, den Sie für diesen Zweck erstellen. Technisch sind die Artikel im Lager, aber nicht physisch, weil sie sich z. B. in einem Konferenz- oder Präsentationsraum befinden.  

In anderen Situationen benötigt die Produktion möglicherweise unerwartet einige Teile für einen Prozess. Sie können Artikel für die Produktionslagerplätze kommissionieren, indem Sie die interne Kommissionierungsanforderung verwenden. Wenn der Prozess beendet ist und der Artikel fertig gestellt wurde, buchen Sie den Verbrauch der Artikel und leeren den Produktionslagerplatz, wodurch die Menge der Artikel im Lager verringert wird.  

Entsprechend können Artikel ins Lager zurückgegeben werden, um eingelagert zu werden. Es kann sein, dass die Artikel für einen Fertigungsauftrag aus dem Lagerbestand entnommen und dann nicht verwendet wurden. Damit sie wieder Teil des Lagerbestands werden, müssen sie in den Lagerplatz eingelagert werden.  

Mit **Interne Einlag.-Anforderungen** können Sie Einlagerungen auszuführen, ohne einen bestimmten Herkunftsbeleg beziehen zu müssen. Sie können leicht alle benötigten Informationen einrichten, die Sie erstellen müssen, um eine Logistikanweisung zu erstellen (Kommissionierung oder Einlagerung).  

> [!NOTE]  
>  Wenn Sie keine internen Kommissionierungs- und Einlagerungsanforderungen verwenden, können Sie diese Anpassungen vornehmen, indem Sie die Methoden zum Umlagern von Artikeln von Lagerplatz zu Lagerplatz oder zum Buchen von Mengenanpassungen in einem Lagerplatz verwenden.  
>   
>  Wenn der Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet und daher Lagerplatzarten nutzt, können Sie keine Artikel manuell in einen Lagerplatz der Lagerplatzart "Wareneingang" hinein oder aus diesem heraus umlagern, da Artikel in einem Lagerplatz der Art "Wareneingang" als eingelagert registriert werden müssen, bevor sie Teil des verfügbaren Lagerbestands werden.  

## <a name="to-create-an-internal-pick"></a>So erstellen Sie eine interne Kommissionierung  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Interne Kommiss.-Anforderung** ein und wählen den zugehörenden Link aus.  
2.  Füllen Sie die **Felder Nr.** Füllen Sie die Felder **An Lagerplatzcode** im Inforegister **Allgemein** aus. Das Feld **Nach Lagerplatzcode** legt den Lagerplatz fest, aus dem Sie die Artikel entnehmen wollen. Für die Produktion wäre dieser Lagerplatz der Fertigungsbereitstellungslagerplatz oder der Off. Fert.-Ber.-Lagerplatz. Für andere Zwecke müssen Sie einen "Nach Lagerplatzcode" einer Lagerplatzart auswählen, die nicht für Kommissionierungen genutzt werden, am besten einen Warenausgangs-, Zwischen- oder Speziallagerplatz.  
3.  Wählen Sie einen Artikel im Feld **Artikelnr.** und tragen Sie die Mengen ein, die Sie kommissionieren möchten.  
4. Wählen Sie die Aktion **Kommissionierung erstellen** aus. Jetzt ist eine Kommissionieranweisung fertig und kann von einem Lagermitarbeiter ausgeführt werden.  

## <a name="to-create-an-internal-put-away"></a>So erstellen Sie eine interne Einlag.-Anforderung  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Interne Kommiss.-Anforderung** ein und wählen den zugehörenden Link aus.  
2.  Füllen Sie die **Felder Nr.** Füllen Sie die Felder **Lagerplatzcode** im Inforegister **Allgemein** aus. Das Feld **Von Lagerplatzcode** legt den Lagerplatz fest, in dem sich die Artikel befinden, die ins Lager zurückgegeben werden, z. B. aus der Produktion.  
3.  Tragen Sie die Nummern und Mengen in die Zeilen ein.  
4.  Wählen Sie die Aktion **Einlagerung erstellen** aus. Jetzt ist eine Einlagerungsanweisung fertig und kann von einem Lagermitarbeiter ausgeführt werden.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

