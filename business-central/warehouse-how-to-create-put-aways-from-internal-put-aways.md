---
title: Einlagerungen aus internen Einlagerungsanforderungen erstellen
description: Nachdem Artikel eingelagert wurden und bevor sie kommissioniert werden, um einen Fertigungsauftrag oder einen Warenausgang zu bedienen, sind sie im Lager ein Teil des verfügbaren Lagerbestands.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d0f91182196aebf9b0123225603ed303cd39e66f
ms.sourcegitcommit: 026484766988b8727649c02fc8990b0646999bf1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5498612"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Wählen und setzen Sie die Einlagerung ohne Herkunftsbeleg
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
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Interne Kommiss.-Anforderung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die **Felder Nr.** Felder **Lagerortcode** und **Nach Lagerplatzcode** im Inforegister **Allgemein**. Das Feld **Nach Lagerplatzcode** legt den Lagerplatz fest, in dem Sie die entnommenen Artikel platzieren wollen. Für die Produktion wäre dieser Lagerplatz der Fertigungsbereitstellungslagerplatz oder der Off. Fert.-Ber.-Lagerplatz. Für andere Zwecke müssen Sie einen „Lagerplatzcode“ einer Lagerplatzart auswählen, die nicht für Kommissionierungen genutzt werden, am besten einen Warenausgangs-, Zwischen- oder Speziallagerplatz.  
4.  Wählen Sie einen Artikel im Feld **Artikelnr.** und tragen Sie die Mengen ein, die Sie kommissionieren möchten.  
5. Wählen Sie die Aktion **Kommissionierung erstellen** aus. Jetzt ist eine Kommissionieranweisung fertig und kann von einem Lagermitarbeiter ausgeführt werden. Alternativ können Sie die Aktion **Veröffentlichung** wählen und Warehouse-Picks mit dem **Picks-Arbeitsblatt** erstellen. Weitere Informationen finden Sie unter [Kommissionierungen im Arbeitsblatt bearbeiten](warehouse-how-to-plan-picks-in-worksheets.md).

## <a name="to-create-an-internal-put-away"></a>So erstellen Sie eine interne Einlag.-Anforderung  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Interne Einlag.-Anforderung** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie den Kopfbereich einer neuen internen Einlagerungsanforderung mindestens mit der **Nummer** und **Lagerortcode** aus.
4. Tragen Sie für jeden Artikel, den Sie ins Lager einlagern möchten, eine Zeile ein. Sie müssen nur die Felder **Artikelnr.** und **Menge** ausfüllen.

  > [!NOTE]  
  > Wenn Sie das Feld **Artikelnr.** auswählen, wird die **Lagerplatzinhaltsübersicht** anstelle der **Artikelübersicht** angezeigt. Dies liegt daran, dass Sie einen Artikel einlagern möchten, der sich in einem bestimmten Lagerplatz befindet – *Lagerplatzinhalt* – und nicht nur einen Artikel. Außerdem wissen Sie bereits, aus welchem Lagerplatz der Artikel entnommen werden soll.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Um die Zeilen mit dem gesamten oder dem gefilterten Lagerplatzinhalt der Lagerplätze des Lagerorts zu füllen, wählen Sie die Aktion **Lagerplatzinhalt abrufen** aus.  
6. Wählen Sie die Aktion **Einlagerung erstellen** aus. Jetzt ist eine Einlagerungsanweisung fertig und kann von einem Lagermitarbeiter ausgeführt werden. Alternativ können Sie die Aktion **Veröffentlichung** wählen und Warehouse-Put-Aways mit dem **Put-Away-Arbeitsblatt** erstellen. Weitere Informationen finden Sie unter [Kommissionierungen im Arbeitsblatt bearbeiten](warehouse-how-to-plan-put-aways-in-worksheets.md).

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
