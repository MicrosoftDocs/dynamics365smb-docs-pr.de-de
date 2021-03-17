---
title: 'Designdetails: Planungsparameter | Microsoft Docs'
description: Dieses Thema beschreibt die verschiedenen Planungsparameter, die Sie in Business Central verwenden können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 10a1e22092e8e18e5b1a71f7d2aa90f0ad2879a9
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390799"
---
# <a name="design-details-planning-parameters"></a>Designdetails: Planungsparameter
Dieses Thema beschreibt die verschiedenen Planungsparameter, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden können.  

Die Art, in der das Planungssystem Artikelzubehör steuert, wird durch verschiedene Einstellungen auf den Artikelkarten oder den Lagerhaltungsdaten und Einstellungen in der Produktionseinrichtung bestimmt. Die nachstehende Tabelle zeigt, wie diese Parameter für die Planung verwendet werden.  

|Zweck|Parameter|  
|-------------|---------------|  
|Definieren Sie, ob der Artikel geplant werden soll|Wiederbeschaffungsverfahren = Leer|  
|Definieren Sie, wann neu bestellt werden soll|Zeitrahmen<br /><br /> Minimalbestand<br /><br /> Sicherh.-Zuschl. Beschaff.-Zt.|  
|Definieren Sie, wie viel neu bestellt werden soll|Sicherheitsbestand<br /><br /> Wiederbeschaffungsverfahren:<br /><br /> -   Feste Bestellmenge und Bestellmenge<br />-   Auffüllen auf Maximalbestand plus Maximalbestand<br />-   Bestellung<br />-   Los-für-Los|  
|Optimieren des Zeitpunktes und der Menge bei einer Neubestellung|Neuplanungsperiode<br /><br /> Loskumulierungsperiode<br /><br /> Toleranzperiode|  
|Ändern Sie die Beschaffungsaufträge|Minimale Losgröße<br /><br /> Maximale Losgröße<br /><br /> Losgrößenrundungsfaktor|  
|Abgrenzen des geplanten Artikels|Produktionsart:<br /><br /> -   Lagerfertigung<br />-   Auftragsfertigung|  

## <a name="define-if-the-item-will-be-planned"></a>Definieren Sie, ob der Artikel geplant werden soll  
Um einen Artikel/SKU in den Planungsprozess einzuschließen, muss er über ein Wiederbeschaffungsverfahren verfügen, andernfalls muss es manuell geplant werden, beispielsweise mit der Funktion "Auftragsplanung".  

## <a name="define-when-to-reorder"></a>Definieren Sie, wann neu bestellt werden soll  
Nachbestellungsvorschläge werden generell nur freigegeben, wenn die voraussichtliche verfügbare Menge unter eine bestimmten Menge gefallen ist. Diese Menge wird durch den Minimalbestand definiert. Andernfalls ist sie Null. Null kann angepasst werden, indem ein Sicherheitsbestand eingegeben wird. Wenn der Benutzer einen Sicherheitszuschlag zur Beschaffungszeit festgelegt hat, führt dies dazu, dass der Vorschlag in der Periode vor dem erforderlichen Fälligkeitsdatum gemacht wird.  

Das Feld **Zeitrahmen** wird von Minimalbestandrichtlinien verwendet (**Feste Bestellmenge** und **Maximalbestand**), bei denen der bestand nach jedem Zeitrahmen geprüft wird. Der erste Zeitrahmen beginnt am Planungsstartdatum.  

> [!NOTE]  
>  Wenn Zeitrahmen berechnet werden, ignoriert das Planungssystem sämtliche Arbeitskalender, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarte** festgelegt werden.  

Die Standardsicherheitsbeschaffungszeit auf der Seite **Herstellung einrichten** sollte mindestens auf einen Tag gesetzt werden. Das Fälligkeitsdatum des Bedarfs ist möglicherweise bekannt, nicht jedoch die Fälligkeitsuhrzeit. Die Planung plant rückwärts, um den Bruttobedarf zu decken, und, wenn kein Sicherheitszuschlag zur Beschaffungszeit definiert ist, können die Waren zu spät eintreffen, um den Bedarf zu decken.  

Drei zusätzlich Wiederbestell-Periodenfelder **Neuplanungsperiode**, **Loskumulierungsperiode** und **Toleranzperiode** spielen auch eine Rolle beim Definieren der Wiederbestellung. Weitere Informationen finden Sie unter [Optimieren des Zeitpunktes und der Menge bei einer Neubestellung](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## <a name="define-how-much-to-reorder"></a>Definieren Sie, wie viel neu bestellt werden soll  
Wenn das Planungssystem die Notwendigkeit einer Neubestellung erkennt, wird das ausgewählte Wiederbeschaffungsverfahren verwendet, um zu ermitteln, wann und wie viel bestellt werden soll.  

Unabhängige vom Wiederbeschaffungsverfahrens folgt das Planungssystem normalerweise dieser Logik:  

1. Die Menge des Bestellvorschlags wird berechnet, um den angegebenen minimalen Bestand des Artikels zu erfüllen; dies ist normalerweise der Sicherheitsbestand. Wenn nichts angegeben ist, ist der minimale Lagerbestand Null.  
2. Wenn der voraussichtlich verfügbare Lagerbestand den Sicherheitsbestand unterschreitet, wird ein rückwärts-geplanter Beschaffungsauftrag vorgeschlagen. Die Auftragsmenge füllt mindestens den Sicherheitsbestand und kann durch den Bruttobedarf innerhalb des Zeitrahmens, durch die Wiederbeschaffungsrichtlinie oder die Auftragsmodifikatoren erhöht werden.  
3. Wenn der voraussichtliche Lagerbestand den Minimalbestand (berechnet aus den aggregierten Änderungen innerhalb des Zeitrahmens) erreicht oder unterschreitet und über dem Sicherheitsbestand liegt, wird ein vorwärtsgeplanter Ausnahmeauftrag vorgeschlagen. Sowohl der zu erfüllende Bruttobedarf, als auch das Wiederbeschaffungsverfahren bestimmen die Bestellmenge. Mindestens entspricht die Bestellmenge dem Minimalbestand.  
4. Wenn mehr Grobbedarf vor dem Fälligkeitsdatum des vorwärts geplanten Auftragsvorschlag besteht und dieser Bedarf den derzeit geplanten voraussichtlich verfügbaren Lagerbestand unter den Sicherheitsbestand bringt, wird die Auftragsmenge entsprechend erhöht. Die vorgeschlagene Beschaffungsauftrag wird dann vom Fälligkeitsdatum dieses Grobbedarfs, der den Sicherheitsbestand unterschritten hätte, rückwärts geplant.  
5. Wenn das Feld **Zeitrahmen** nicht ausgefüllt ist, wird nur der Bruttobedarf am gleichen Fälligkeitsdatum hinzugefügt.  

     Drei zusätzlich Wiederbestell-Periodenfelder **Neuplanungsperiode**, **Loskumulierungsperiode** und **Toleranzperiode** spielen auch eine Rolle beim Definieren der Wiederbestellung. Weitere Informationen finden Sie unter [Optimieren des Zeitpunktes und der Menge bei einer Neubestellung](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

### <a name="reordering-policies"></a>Wiederbeschaffungsverfahren  
Die folgenden Wiederbeschaffungsrichtlinien beeinflussen die Menge, die nachbestellt wird.  

|Wiederbeschaffungsverfahren|Beschreibung|  
|-----------------------|---------------------------------------|  
|**Feste Bestellmenge**|Mindestens ist die Bestellmenge gleich der Nachbestellmenge. Kann erhöht werden, um den Bedarf oder die gewünschte Lagerebene zu erfüllen. Dieses Wiederbeschaffungsverfahren wird normalerweise mit einem Minimalbestand verwendet.|  
|**Auffüllen auf Maximalbestand**|Die Auftragsmenge wird so berechnet, das sie den Maximalbestand erfüllt. Wenn Mengenmodifizierer verwendet werden, kann der Maximalbestand verletzt werden. Es ist nicht empfehlenswert, den Zeitrahmen zusammen mit maximaler Menge zu verwenden. Das Zeitrahmen wird normalerweise überschrieben. Dieses Wiederbeschaffungsverfahren wird normalerweise mit einem Minimalbestand verwendet.|  
|**Auftrag**|Die Auftragsmenge wird so berechnet, dass jedes Bedarfsereignis erfüllt wird, und der Bedarf-Vorrat-Satz bleibt bis zur Ausführung verknüpft. Planungsparameter werden nicht berücksichtigt.|  
|**Los-für-Los**|Die Menge wird berechnet, um die Summe des Bedarfs abzudecken, der im Zeitrahmen fällig wird.|  

##  <a name="optimize-when-and-how-much-to-reorder"></a>Optimieren des Zeitpunktes und der Menge bei einer Neubestellung  
Um einen rationalen Beschaffungsplan zu erhalten, kann ein Planer Planungsparameter genau abstimmen, um Neuplanungsvorschläge einzuschränken, Bedarf zu akkumulieren (dynamische Nachbestellmenge), oder um unwichtige Planungsaktionen zu vermeiden. Die folgenden Nachbestellungsperiodenfelder helfen bei der Optimierung, wann und wie viel nachzubestellen ist.  

|Feld|Beschreibung|  
|---------------------------------|---------------------------------------|  
|**Neuplanungsperiode**|Dieses Feld wird verwendet, um zu ermitteln, ob die Ereignismeldung einen bestehenden Auftrags neu planen oder diesen stornieren und einen neuen Auftrag erstellen soll. Der bestehende Auftrag wird innerhalb einer Neuplanungsperiode vor dem aktuellen Vorrat und bis zu einer Neuplanungsperiode nach dem aktuellen Vorrat neu geplant.|  
|**Loskumulierungsperiode**|Mit dem Wiederbeschaffungsverfahren „Los-für-Los“ wird dieses Feld verwendet, um mehrere Bedarfsposten in einem Beschaffungsauftrag zusammenzufassen. Ab dem ersten geplanten Vorrat werden alle Bedarfsposten in der folgenden Loskumulierungsperiode in einen Beschaffungsauftrag zusammengefasst, der am Tag des ersten Bedarfs aufgeben wird. Ein Bedarfsposten, der außerhalb der Loskumulierungsperiode liegt, wird nicht durch den Beschaffungsauftrag abgedeckt.|  
|**Toleranzperiode**|Dieses Feld wird verwendet, um kleinere Neuplanungen für vorhandenen Bedarf rechtzeitig zu vermeiden. Ändert das Lieferdatum, bis eine Toleranzperiode ab dem Lieferdatum keine Ereignismeldungen mehr generiert.<br /><br /> Die Toleranzperiode definiert eine Zeitspanne, die das Planungssystem nicht vorschlagen soll, um bestehende Beschaffungsaufträge in der Planung vorzuverlegen. Dies schränkt die Anzahl der geringfügigen Neuplanungen für vorhandenen Bedarf auf ein späteres Datum ein, wenn dieses neue Datum innerhalb der Toleranzperiode liegt.<br /><br /> Deshalb ist ein positives Delta zwischen dem vorgeschlagenen neuen Lieferdatum und dem ursprünglichen Lieferdatum immer größer als die Toleranzperiode.|  
> [!NOTE]
> Beim Wiederbeschaffungsverfahren Los-für-Los muss der Wert des Felds **Loskumulierungsperiode** dem Wert des Felds **Toleranzperiode** entsprechen oder größer als dieser sein. Andernfalls wird die Toleranzperiode während der Planungsroutine automatisch reduziert, um der Loskumulierungsperiode zu entsprechen.  

Die Terminierung für die Neuplanungsperiode, die Toleranzperiode und die Loskumulierungsperiode basiert auf einem Lieferdatum. Das Zeitrahmen basiert auf dem Planungsstartdatum, wie in der folgenden Abbildung gezeigt.  

![Zeitrahmenelemente](media/supply_planning_5_time_bucket_elements.png "Zeitbereich-Elemente")  

In den folgenden Beispielen stellen die schwarzen Pfeile vorhandenen Bedarf (aufwärts) und Bedarf dar (abwärts). Rote, grüne und orange Pfeile sind Planungsvorschläge.  

**Beispiel 1**: Das geänderte Datum liegt außerhalb der Neuplanungsperiode, wodurch der bestehende Vorrat storniert wird. Ein neuer Vorrat wird vorgeschlagen, um den Bedarf in der Loskumulierungsperiode zu decken.  

![Neuplanungsperiode und Losakkumulationsperiode](media/supply_planning_5_recheduling_period_lot_accumulation_period.png "Neuplanungsperiode und Losakkumulationsperiode")  

**Beispiel 2**: Das geänderte Datum liegt innerhalb der Neuplanungsperiode, wodurch der bestehende Vorrat neu geplant wird. Ein neuer Vorrat wird vorgeschlagen, um den Bedarf außerhalb der Loskumulierungsperiode zu decken.  

![Neuplanungsperiode, Losakkumulationsperiode und Neuplanung](media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png "Neuplanungsperiode, Losakkumulationsperiode und Umplanung")  

**Beispiel 3**: Es gibt einen Bedarf in der Toleranzperiode, und die Vorratsmenge in der Loskumulierungsperiode entspricht der Vorratsmenge. Der nächste Bedarf wird aufgedeckt, und ein neuer Vorrat wird vorgeschlagen.  

![Toleranzperiode und Lotakkumulationsperiode](media/supply_planning_5_dampener_period_lot_accumulation_period.png "Toleranzperiode und Losakkumulationsperiode")  

**Beispiel 4**: Es gibt einen Bedarf in der Toleranzperiode, und der Vorrat bleibt auf dem selben Datum. Die derzeitige Vorratsmenge reicht jedoch nicht aus, um den Bedarf in der Loskumulierungsperiode zu decken; daher wird eine Mengenänderungsaktion für den vorhandenen Beschaffungsauftrag empfohlen.  

![Toleranzperiode, Losakkumulationsperiode und Änderungsmenge](media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png "Toleranzperiode , Losakkumulationsperiode und Änderungsmenge")  

**Vorgabewerte**: Der Vorgabewert des **Zeitrahmen**-Feldes und der drei Nachbestellungsperiodenfelder ist leer. Für alle Felder mit Ausnahme des Felds **Toleranzperiode** bedeutet dies 0D (Null Tage). Wenn das Feld **Toleranzperiode** leer ist, wird der Wert im Feld **Standardtoleranzperiode** auf der Seite **Produktion Einrichtung** verwendet.  

## <a name="modify-the-supply-orders"></a>Ändern Sie die Beschaffungsaufträge  
Wenn die Menge des Bestellvorschlags berechnet wurde, können eine oder mehrere der Auftragsmodifikationen ihn anpassen. Beispielsweise ist die maximale Auftragsgröße größer als oder gleich der minimale Auftragsgröße, die größer als oder gleich dem Auftragsvielfachen ist.  

Die Menge wird verringert, wenn sie die maximale Auftragsmenge übersteigt. Dann wird sie erhöht, wenn sie unter der Mindestbestellgröße liegt. Schließlich wird sie aufgerundet, sodass sie einem angegebenen Auftragsvielfachen entspricht. Alle Restmengen verwenden die gleichen Regulierungen, bis der Gesamtbedarf in Bestellvorschläge umgewandelt wurde.  

## <a name="delimit-the-item"></a>Abgrenzen des Artikels  
Die Option **Produktionsart** definiert, welche zusätzlichen Aufträge die Nettobedarfsberechnung vorschlagen wird.  

Wenn die Option **Lagerfertigung** verwendet wird, betreffen die Aufträge nur den jeweiligen Artikel.  

Wenn die Option **Auftragsfertigung** verwendet wird, analysiert das Planungssystem die Fertigungsstückliste des Artikels und erstellt zusätzliche verknüpfte Vorschlagszeilen für diejenigen Artikel auf untergeordneter Ebene, die auch als Auftragsfertigung definiert werden. Dieses wird fortgesetzt, solange Auftragsfertigungsartikel in den absteigenden Stücklistenstrukturen vorhanden sind.  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]