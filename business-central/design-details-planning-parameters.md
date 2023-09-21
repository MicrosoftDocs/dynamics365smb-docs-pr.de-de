---
title: Designdetails – Planungsparameter
description: 'In diesem Artikel werden die verschiedenen Planungsparameter beschrieben, die Sie verwenden können, und wie sie sich auf das Planungssystem auswirken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
---
# Designdetails: Planungsparameter

Dieser Artikel beschreibt die Planungsparameter, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden können.  

Wie das Planungssystem Artikelzubehör steuert, wird durch verschiedene Einstellungen auf den Seiten **Artikelkarte**, **SKU** und **Produktion Einrichtung** bestimmt. In der folgenden Tabelle wird erläutert, wie die Planung diese Einstellungen verwendet.  

|Zweck|Einstellungen|
|-------------|---------------|
|Festlegen, ob der Artikel geplant ist|Wiederbeschaffungsverfahren = Leer|
|Definieren Sie, wann neu bestellt werden soll|Zeitrahmen<br /><br /> Minimalbestand<br /><br /> Sicherh.-Zuschl. Beschaff.-Zt.|
|Definieren Sie, wie viel neu bestellt werden soll|Sicherheitsbestand<br /><br /> Wiederbeschaffungsverfahren:<br /><br /> -   Feste Bestellmenge und Bestellmenge<br />-   Auffüllen auf Maximalbestand plus Maximalbestand<br />-   Bestellung<br />-   Los-für-Los|
|Optimieren des Zeitpunktes und der Menge bei einer Neubestellung|Neuplanungsperiode<br /><br /> Loskumulierungsperiode<br /><br /> Toleranzperiode|
|Ändern Sie die Beschaffungsaufträge|Minimale Losgröße<br /><br /> Maximale Losgröße<br /><br /> Losgrößenrundungsfaktor|
|Abgrenzen des geplanten Artikels|Produktionsart:<br /><br /> -  Lagerfertigung<br />- Auftragsfertigung|

## Festlegen, ob der Artikel geplant ist  

Um einen Artikel oder eine SKU in den Planungsprozess einzubeziehen, müssen Sie ihm ein Wiederbeschaffungsverfahren zuweisen. Andernfalls muss die Planung manuell erfolgen, beispielsweise mithilfe der Funktion „Auftragsplanung“.  

## Definieren Sie, wann neu bestellt werden soll  

Nachbestellungsvorschläge werden generell nur freigegeben, wenn die voraussichtliche verfügbare Menge unter eine bestimmten Menge gefallen ist. Die Menge hängt vom Meldebestand ab. Andernfalls ist sie Null. Null kann angepasst werden, indem ein Sicherheitsbestand eingegeben wird. Wenn Sie einen Sicherheitszuschlag zur Beschaffungszeit festlegen, wird der Vorschlag in der Periode vor dem erforderlichen Fälligkeitsdatum gemacht.  

Das Feld **Zeitrahmen** wird von Meldebestandrichtlinien verwendet (**Feste Bestellmenge** und **Auffüllen auf Maximalbestand**). Die Lagerebene wird infolgedessen nach jedem Zeitrahmen überprüft. Der erste Zeitrahmen beginnt am Planungsstartdatum.  

> [!NOTE]  
> Wenn Zeitrahmen berechnet werden, ignoriert das Planungssystem Arbeitskalender, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarte** festgelegt werden.  

Auf der Seite **Produktion Einrichtung** sollten Sie den Standardsicherheitszuschlag zur Beschaffungszeit von mindestens auf einen Tag gesetzt werden. Das Fälligkeitsdatum des Bedarfs ist möglicherweise bekannt, nicht jedoch die Fälligkeitsuhrzeit. Die Planung erfolgt rückwärts, um den Bruttobedarf zu decken. Wenn Sie keinen Sicherheitszuschlag zur Beschaffungszeit festlegen, kommt die Ware möglicherweise zu spät an, um den Bedarf zu decken.  

Die Felder **Neuplanungsperiode**, **Loskumulierungsperiode** und **Toleranzperiode** spielen auch beim Festlegen des Meldebestands eine Rolle. Weitere Informationen finden Sie unter [Optimieren des Zeitpunktes und der Menge bei einer Neubestellung](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder).  

## Definieren Sie, wie viel neu bestellt werden soll

Wenn das Planungssystem die Notwendigkeit einer Neubestellung erkennt, bestimmt das Wiederbeschaffungsverfahren, wann und wie viel bestellt werden soll.  

Unabhängige vom Wiederbeschaffungsverfahrens folgt das Planungssystem normalerweise dieser Logik:  

1. Die Menge des Bestellarbeitsblatts wird berechnet, um den Mindestlagerbestand des Artikels zu erfüllen. Dies ist normalerweise der Sicherheitsbestand. Wenn nichts angegeben ist, ist der minimale Lagerbestand Null.  
2. Wenn der voraussichtlich verfügbare Lagerbestand den Sicherheitsbestand unterschreitet, wird ein rückwärts-geplanter Beschaffungsauftrag vorgeschlagen. Die Auftragsmenge füllt mindestens den Sicherheitsbestand und kann durch den Bruttobedarf innerhalb des Zeitrahmens, durch die Wiederbeschaffungsrichtlinie oder die Auftragsmodifikatoren erhöht werden.  
3. Wenn der voraussichtliche Lagerbestand den Minimalbestand (berechnet aus den aggregierten Änderungen innerhalb des Zeitrahmens) erreicht oder unterschreitet und über dem Sicherheitsbestand liegt, wird ein vorwärtsgeplanter Ausnahmeauftrag vorgeschlagen. Sowohl der zu erfüllende Bruttobedarf, als auch das Wiederbeschaffungsverfahren bestimmen die Bestellmenge. Mindestens entspricht die Bestellmenge dem Minimalbestand.  
4. Wenn mehr Bruttobedarf vor dem Fälligkeitsdatum des vorwärts geplanten Auftragsvorschlag besteht und dieser Bedarf den derzeit geplanten voraussichtlich verfügbaren Lagerbestand unter den Sicherheitsbestand bringt, wird die Auftragsmenge entsprechend erhöht. Die vorgeschlagene Beschaffungsauftrag wird dann vom Fälligkeitsdatum dieses Grobbedarfs, der den Sicherheitsbestand unterschritten hätte, rückwärts geplant.  
5. Wenn das Feld **Zeitrahmen** nicht ausgefüllt ist, wird nur der Bruttobedarf am gleichen Fälligkeitsdatum hinzugefügt.  

### Wiederbeschaffungsverfahren  

Die folgenden Wiederbeschaffungsverfahren beeinflussen die Menge, die nachbestellt wird. Weitere Informationen zu Wiederbeschaffungsverfahren finden Sie unter [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md).  

|Wiederbeschaffungsverfahren|Description|  
|-----------------------|---------------------------------------|  
|**Feste Bestellmenge**|Mindestens ist die Bestellmenge gleich der Nachbestellmenge. Sie können die Menge erhöhen, um den Bedarf oder die gewünschte Lagerebene zu erfüllen. Dieses Wiederbeschaffungsverfahren wird normalerweise mit einem Minimalbestand verwendet.|  
|**Auffüllen auf Maximalbestand**|Die Auftragsmenge wird so berechnet, das sie den Maximalbestand erfüllt. Wenn Mengenmodifizierer verwendet werden, kann der Maximalbestand verletzt werden. Es ist nicht empfehlenswert, den Zeitrahmen zusammen mit maximaler Menge zu verwenden. Das Zeitrahmen wird normalerweise überschrieben. Dieses Wiederbeschaffungsverfahren wird normalerweise mit einem Minimalbestand verwendet.|  
|**Auftrag**|Die Auftragsmenge wird so berechnet, dass jedes Bedarfsereignis erfüllt wird, und der Bedarf-Vorrat-Satz bleibt bis zur Ausführung verknüpft. Planungsparameter werden nicht berücksichtigt.|  
|**Los-für-Los**|Die Menge wird berechnet, um die Summe des Bedarfs abzudecken, der im Zeitrahmen fällig wird.|  

## Optimieren des Zeitpunktes und der Menge bei einer Neubestellung  

Ein Planner kann Planungsparameter genau abstimmen, um Neuplanungsvorschläge einzuschränken, Bedarf zu akkumulieren (dynamische Bestellmenge), oder um unwichtige Planungsaktionen zu vermeiden. Die folgenden Felder helfen bei der Optimierung, wann und wie viel nachzubestellen ist.  

|Feld|Description|  
|---------------------------------|---------------------------------------|  
|**Neuplanungsperiode**|Dieses Feld bestimmt, ob die Ereignismeldung einen bestehenden Auftrags neu planen oder diesen stornieren und einen neuen Auftrag erstellen soll. Der bestehende Auftrag wird innerhalb einer Neuplanungsperiode vor dem aktuellen Vorrat und bis zu einer Neuplanungsperiode nach dem aktuellen Vorrat neu geplant.<br><br>**Hinweis:** Dieser Parameter funktioniert nur mit dem **Los-für-Los**-Wiederbeschaffungsverfahren.|  
|**Loskumulierungsperiode**|Mit dem Wiederbeschaffungsverfahren „Los-für-Los“ wird dieses Feld verwendet, um mehrere Bedarfsposten in einem Beschaffungsauftrag zusammenzufassen. Ab dem ersten geplanten Vorrat werden alle Bedarfsposten in der folgenden Loskumulierungsperiode in einen Beschaffungsauftrag zusammengefasst, der am Tag des ersten Bedarfs aufgeben wird. Ein Bedarfsposten, der außerhalb der Loskumulierungsperiode liegt, wird nicht durch den Beschaffungsauftrag abgedeckt.|  
|**Toleranzperiode**|Dieses Feld wird verwendet, um kleinere Neuplanungen für vorhandenen Bedarf rechtzeitig zu vermeiden. Ändert das Lieferdatum, bis eine Toleranzperiode ab dem Lieferdatum keine Ereignismeldungen mehr generiert.<br /><br /> Die Toleranzperiode definiert eine Zeitspanne, die das Planungssystem nicht vorschlagen soll, um bestehende Beschaffungsaufträge in der Neuplanung vorzuverlegen. Dies schränkt die Anzahl der geringfügigen Neuplanungen für vorhandenen Bedarf auf ein späteres Datum ein, wenn dieses neue Datum innerhalb der Toleranzperiode liegt.<br /><br /> Deshalb ist ein positives Delta zwischen dem vorgeschlagenen neuen Lieferdatum und dem ursprünglichen Lieferdatum immer größer als die Toleranzperiode.|  

> [!NOTE]
> Beim Wiederbeschaffungsverfahren Los-für-Los muss der Wert des Felds **Loskumulierungsperiode** dem Wert des Felds **Toleranzperiode** entsprechen oder größer als dieser sein. Andernfalls wird die Toleranzperiode während der Planungsroutine reduziert, um der Loskumulierungsperiode zu entsprechen.  

Die Terminierung für die Neuplanungsperiode, die Toleranzperiode und die Loskumulierungsperiode basiert auf einem Lieferdatum. Das Zeitrahmen basiert auf dem Planungsstartdatum, wie in der folgenden Abbildung gezeigt.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Zeitrahmen-Elemente.":::

In den folgenden Beispielen stellen die schwarzen Pfeile vorhandenen Bedarf (aufwärts) und Bedarf dar (abwärts). Rote, grüne und orange Pfeile sind Planungsvorschläge.  

**Beispiel 1**: Das geänderte Datum liegt außerhalb der Neuplanungsperiode, wodurch der bestehende Vorrat storniert wird. Ein neuer Vorrat wird vorgeschlagen, um den Bedarf in der Loskumulierungsperiode zu decken.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Neuplanungs- und Loskumulierungsperiode":::

**Beispiel 2**: Das geänderte Datum liegt innerhalb der Neuplanungsperiode, wodurch der bestehende Vorrat neu geplant wird. Ein neuer Vorrat wird vorgeschlagen, um den Bedarf außerhalb der Loskumulierungsperiode zu decken.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Neuplanungsperiode, Loskumulierungsperiode und neu planen.":::

**Beispiel 3**: Es gibt einen Bedarf in der Toleranzperiode, und die Vorratsmenge in der Loskumulierungsperiode entspricht der Vorratsmenge. Der nächste Bedarf wird aufgedeckt, und ein neuer Vorrat wird vorgeschlagen.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Toleranzperiode und Loskumulierungsperiode":::

**Beispiel 4**: Es gibt einen Bedarf in der Toleranzperiode und der Vorrat bleibt auf dem selben Datum. Allerdings deckt die aktuelle Angebotsmenge nicht den Bedarf in der Loskumulierungsperiode. Es wird eine Mengenänderungsaktion für den bestehenden Beschaffungsauftrag vorgeschlagen.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Toleranzperiode, Loskumulierungsperiode und Änderungsmenge":::

**Vorgabewerte**: Der Vorgabewert des **Zeitrahmen**-Feldes und der drei Nachbestellungsperiodenfelder ist leer. Für alle Felder mit Ausnahme des Felds **Toleranzperiode** bedeutet dies 0D (Null Tage). Wenn das Feld **Toleranzperiode** leer ist, wird der Wert im Feld **Standardtoleranzperiode** auf der Seite **Produktion Einrichtung** verwendet.  

## Ändern Sie die Beschaffungsaufträge  

Wenn die Menge des Bestellarbeitsblatts berechnet wurde, können eine oder mehrere der Auftragsmodifikationen ihn anpassen. Beispielsweise ist die maximale Auftragsgröße größer als oder gleich der minimale Auftragsgröße, die größer als oder gleich dem Auftragsvielfachen ist.  

Die Menge wird verringert, wenn sie die maximale Auftragsmenge übersteigt. Dann wird sie erhöht, wenn sie unter der Mindestbestellgröße liegt. Schließlich wird sie aufgerundet, sodass sie einem angegebenen Auftragsvielfachen entspricht. Alle Restmengen verwenden die gleichen Regulierungen, bis der Gesamtbedarf in Bestellarbeitsblätter umgewandelt wurde.  

## Abgrenzen des Artikels  

Das Feld **Produktionsart** auf der Seite **Artikelkarte** legt fest, welche anderen Bestellungen die Nettobedarfberechnung vorschlägt.  

Wenn die Option **Lagerfertigung** verwendet wird, betreffen die Aufträge nur den Artikel.  

Wenn die Option **Auftragsfertigung** verwendet wird, analysiert das Planungssystem die Fertigungsstückliste des Artikels und erstellt verknüpfte Vorschlagszeilen für diejenigen Artikel auf untergeordneter Ebene, die auch als Auftragsfertigung definiert werden. Dieses wird fortgesetzt, solange Auftragsfertigungsartikel in den absteigenden Stücklistenstrukturen vorhanden sind.

## Verwenden von Stücklistenebenen, um den abgeleiteten Bedarf zu verwalten

Verwenden Sie Stücklistenebenen, um den abgeleiteten Bedarf an Komponenten bis zu den unteren Ebenen der Stückliste weiterzuführen. Weitere Informationen zu Stücklistenebenen finden Sie unter [Artikelpriorität/Stücklistenebene](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

Jedem Teil in der Erzeugnisstruktur wird eine Stücklistenebene zugeordnet. Das oberste Fertigprodukt wird mit der Ebene 0 gekennzeichnet. Je größer die Ebenennummer, desto tiefer ist der Artikel in der Hierarchie. Fertigprodukte haben z. B. die Ebene 0, Baugruppen, die als Teile in die Montage des Produkts eingehen, haben die Ebenen 1, 2, 3 und so weiter. Das Ergebnis ist die mit den Bedarfen koordinierte Planung von Baugruppen aller Artikel mit einer höheren Ebenennummer. Wenn Sie einen Plan berechnen, wird die Stückliste im Planungsvorschlag entfaltet und der Bruttobedarf für die Ebene 0 geht ein in die Bruttobedarfe für die nächste Planungsebene.

Verwenden Sie auf der Seite **Produktion Einrichtung** den Umschalter **Dyn. Stückl.-Ebene berechnen**, um anzugeben, ob sofort Stücklistenebenen für jede Komponente in der Produktstruktur zugewiesen und berechnet werden sollen. Wenn Sie große Mengen an Daten haben, kann sich diese Funktion negativ auf die Leistung der Anwendung auswirken (zum Beispiel bei der automatischen Kostenanpassung). Beachten Sie, dass diese Funktion nicht rückwirkend arbeitet. Deshalb ist es empfehlenswert, diese Funktion bereits im Vorfeld zu verwenden.

Als Alternative zur automatischen Berechnung, die bei aktiviertem Kontrollkästchen dynamisch erfolgt, können Sie im Menü **Produktion** den Batchauftrag **Stücklistenebene berechnen** ausführen, indem Sie auf **Produktentwicklung** und anschließend auf **Stücklistenebene berechnen** klicken.

> [!IMPORTANT]
> Wenn Sie den Umschalter **Dyn. Stückl.-Ebene berechnen** nicht einschalten, dann müssen Sie den Stapelverarbeitungsauftrag **Stücklistenebene berechnen** ausführen, bevor Sie den Beschaffungsplan berechnen (den Stapelverarbeitungsauftrag **Planung berechnen**).  

> [!NOTE]
> Auch wenn Sie das ausgewählte Feld **Dyn. Stückl.-Ebene berechnen** einschalten, werden die Stücklistenebenen nicht dynamisch geändert, wenn eine übergeordnete Stückliste gelöscht wird oder als nicht zertifiziert festgelegt wird. Dieser Fall macht das Hinzufügen neuer Artikel zum Ende der Produktstruktur eventuell schwierig, da unter Umständen die maximale Anzahl von Stücklistenebenen überschritten wird. Daher können Sie bei umfangreichen Produktstrukturen, bei denen das Limit für die Stücklistenebenen erreicht wird, häufig die Stapelverarbeitung **Stücklistenebene berechnen** auszuführen, um die Struktur beizubehalten.  

## Siehe auch  

[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)  
[Designdetails: Ausgleich von Nachfrage und Angebot](design-details-balancing-demand-and-supply.md)  
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]