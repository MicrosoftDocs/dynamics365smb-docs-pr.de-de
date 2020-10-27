---
title: Arbeiten mit Verkauf Rahmenaufträgen oder Einkaufsbestellung
description: Verwenden Sie Rahmenaufträge, wenn ein Debitor der Abnahme großer Mengen zugestimmt hat, die in mehreren kleineren Lieferungen über einen bestimmten Zeitraum geliefert werden sollen. Gleiches gilt für den Einkauf.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d3202f380da6b58ba30fa301c7ea6a24efb91cf5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925922"
---
# <a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a>Arbeiten mit Verkauf Rahmenaufträgen oder Einkauf Rahmenbestellungen

Ein Rahmenauftrag stellt ein Gerüst für eine langfristige Vereinbarung zwischen Ihnen und einem Debitor dar. In ähnlicher Weise verwenden Sie Einkauf Rahmenbestellungen, um langfristige Vereinbarungen zwischen Ihnen und Ihrem Kreditor zu verwalten.

Ein Rahmenauftrag wird in der Regel erstellt, wenn sich ein Debitor verpflichtet hat, größere Mengen abzunehmen, die über einen längeren Zeitraum in mehreren kleineren bereitgestellt werden. Häufig decken Rahmenaufträge nur einen bestimmten Artikel ab, für den bestimmte Liefertermine vorgegeben sind. Der Hauptgrund für die Verwendung eines Rahmenauftrags anstelle eines Verkaufsauftrags besteht darin, dass die bei einem Rahmenauftrag eingegebenen Mengen keinen Einfluss auf die Artikelverfügbarkeit haben und daher als Arbeitsvorlage für die Überwachung und Planung verwendet werden können.

In einem Rahmenauftrag kann jede einzelne Lieferung als Auftragszeile eingerichtet werden, die dann zum Zeitpunkt der Lieferung in einen Auftrag umgewandelt werden kann.

Rahmenaufträge werden beispielsweise verwendet, wenn ein Debitor anruft und 1000 Einheiten eines Artikels bestellt, die über den kommenden Monat in Mengen von je 250 Stck. pro Woche geliefert werden sollen.

> [!NOTE]
> Rahmenbestellungen funktionieren auf ähnliche Weise wie Rahmenaufträge. Die Dokumentation enthält nur Rahmenverkaufsaufträge.

## <a name="to-create-a-blanket-sales-order"></a>So legen Sie einen Rahmenauftrag an:

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkauf Rahmenauftrag** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Nehmen Sie im Feld **Auftragsdatum** keine Eingabe vor. Wenn die einzelnen Verkaufsaufträge anhand des Rahmenauftrags erstellt werden, wird als Auftragsdatum des Verkaufsauftrags automatisch das Arbeitsdatum festgelegt.
5. Erstellen Sie im Inforegister **Zeilen** einzelne Zeilen für jede Lieferung. Wenn der Debitor beispielsweise 1.000 Einheiten gleichmäßig auf vier Wochen verteilt erhalten möchte, geben Sie vier separate Zeilen mit jeweils 250 Einheiten ein.  

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>So erstellen Sie einen Auftrag aus einem Rahmenauftrag:  

1. Um einen Auftrag für eine oder mehrere der Zeilen des Rahmenauftrags zu erstellen, entfernen Sie die Menge im Feld **Zu liefernde Menge** in allen Zeilen, für die zum aktuellen Zeitpunkt keine Lieferung gewünscht wird.  
2. Wenn Sie bereit sind, Bestellungen zu erstellen, wählen Sie die Aktion **Bestellung erstellen** und wählen Sie dann **Ja** . Sie werden in einer Meldung darüber informiert, dass dem Rahmenauftrag eine Auftragsnummer zugewiesen wurde. Beachten Sie, dass der Rahmenauftrag nicht gelöscht wurde.  
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Um die Ergebnisse der vorangehenden Schritte anzuzeigen, wählen Sie auf dem Inforegister **Zeilen** die Option **Aktionen** , wählen Sie Zeile, wählen Sie Nicht gebuchte Zeilen, und wählen Sie dann **Aufträge** .  
5. Wählen Sie auf der Seite **Verkaufszeilen** den entsprechenden Verkaufsauftrag aus. Wählen Sie auf dem Inforegister **Zeilen** die Option Aktionen, wählen Sie Zeile, und wählen Sie dann **Beleg anzeigen** .  

Das folgende gilt für Verkaufsaufträge nach der Erstellung von Rahmenaufträgen:  

- Nachdem der Rahmenauftrag in einen Auftrag umgewandelt wurde, enthält diese sämtliche Zeilen des Rahmenauftrags. Die Mengen der Zeilen, bei denen die Menge im Feld **Zu liefern** gelöscht wurde, werden mit leerem Feld **Menge** angezeigt. Sie können diese Zeilen bearbeiten oder löschen oder unverändert beibehalten.  
- Beachten Sie unbedingt, dass die Menge der Auftragszeile die Menge der zugehörigen Rahmenauftragszeile nicht übersteigen darf. Andernfalls kann der Auftrag nicht gebucht werden.  
- Wenn der Auftrag als geliefert und/oder als fakturiert gebucht wurde, werden die Felder **Menge geliefert** und **Menge fakturiert** auf des zugehörigen Rahmenauftrags automatisch aktualisiert.  
- Die Nummer des Rahmenauftrags und die Zeilennummer werden als Eigenschaften der Auftragszeilen erfasst, wenn diese aus einem Rahmenauftrag erstellt wurden.  
- Wenn Aufträge nicht direkt aus einem Rahmenauftrag erstellt werden, aber dennoch zu diesem gehören, kann eine Verknüpfung zwischen einem Auftrag und einem Rahmenauftrag eingerichtet werden, indem die Nummer des verknüpften Rahmenauftrags im Feld **Rahmenauftragsnr.** in der Auftragszeile eingegeben wird. Lagerdurchlaufzeit" der Einkaufsbestellung.  
- Nachdem der Verkaufsauftrag für die Gesamtmenge einer Rahmenbestellzeile erstellt wurde, kann kein anderer Verkaufsauftrag für dieselbe Zeile erstellt werden. Benutzer können im Feld **Zu liefern** keine Menge eingeben. Wenn in einem Rahmenauftrag jedoch weitere Mengen hinzugefügt werden müssen, kann der Wert im Feld **Menge** erhöht werden, und es können weitere Aufträge erstellt werden.  
- Der fakturierte Rahmenauftrag verbleibt im System, bis er gelöscht wird, und zwar entweder durch Löschen einzelner Rahmenaufträge oder durch Ausführen der Stapelverarbeitung **Erledigte Rahmenauftr. löschen** .  
- Wenn ein Debitor im Anwendungsbereich "Marketing" auch als Kontakt eingerichtet wurde und Sie einen Aktivitätenvorlagencode für Rahmenaufträge auf der Seite **Marketing & Vertrieb Einr.** angegeben haben, wird eine Aktivität in der Tabelle "Aktivitätenprotokollposten" aufgezeichnet, wenn Sie **Drucken** auswählen, um die Rahmenaufträge zu drucken.

## <a name="to-view-the-status-of-a-blanket-sales-order"></a>So zeigen Sie den Status eines Rahmenauftrags an:  
Sie können sich den Status einer Rahmenbestellung auf der Seite **Auftragssstatistik Rahmenbestellung** anzeigen lassen. Dies kann dann von Bedeutung sein, wenn Sie beginnen, die Bestellung zu fakturieren, die aus der Rahmenverkaufsbestellung erstellt wurde.  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkauf Rahmenauftrag** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie einen Rahmenbestellung aus, und wählen Sie die **Statistik** Aktion aus.  
3.  Auf der Seite **Verkaufsstatistik Rahmenbestellung** finden Sie auf dem Inforegister **Allgemein** zusammengefasste Informationen über die gesamte Bestellung, basierend auf den Gesamtmengen in den verschiedenen **Mengenfeldern** in den Rahmenbestellungszeilen.  

- Auf dem Inforegister **Fakturierung** finden Sie zusammengefasste Informationen über die Gesamtmenge in den verschiedenen Feldern **Zu fakturieren** in den Rahmenverkaufsbestellungszeilen.  
- Auf dem Inforegister **Lieferung** werden zusammengefasste Informationen über die Gesamtmenge in den verschiedenen Feldern **Zu liefern** in den Rahmenverkaufsbestellungszeilen angezeigt.  
- Auf dem Inforegister **Vorauszahlung** werden zusammenfassende Informationen zu den vorab bezahlten Beträgen angezeigt.  
- Auf dem Inforegister **Kreditor** werden bestimmte grundlegende Informationen über den Kreditor angezeigt.    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Um gebuchte und nicht gebuchte Rahmenbestellungszeilen anzuzeigen   
Die Verknüpfung zwischen dem Rahmenauftrag und dem daraus stammenden Verkaufsauftrag und jeder andere Verkaufsbeleg wird beibehalten, nachdem sie als Liste gebuchter und ungebuchter Verkaufsauftrags- und Rechnungszeilen gebucht wurden.  

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Rahmenaufträge** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Rahmenbestellung, die Sie anzeigen möchten.
3. Sie können nicht gebuchte Posten anzeigen, indem Sie die entsprechende Zeile markieren und dann auf dem Inforegister  Zeilen auf  Aktionen,  **Zeile** ,  **Nicht gebuchte Zeilen** klicken. Wählen Sie eine der folgenden Optionen aus.  

    |Option|Description|
    |--|--|
    |**Aufträge**|Gibt mit der ausgewählten Zeile verknüpfte offene Aufträge an.|
    |**Rechnungen**|Gibt mit der ausgewählten Zeile verknüpfte offene Rechnungen an. Offene Rechnungen werden durch Eingabe der Nummer des Rahmenauftrags in der Verkaufsrechnungszeile manuell mit einem Rahmenauftrag verknüpft.|
    |**Reklamationen**|Gibt mit der ausgewählten Zeile verknüpfte offene Reklamationen an.|
    |**Gutschriften**|Gibt mit der ausgewählten Zeile verknüpfte offene Gutschriften an.|

4. Sie können nicht gebuchte Posten anzeigen, indem Sie die entsprechende Zeile markieren und dann auf dem Inforegister  Zeilen auf  Aktionen,  **Zeile** ,  **Nicht gebuchte Zeilen** klicken. Wählen Sie eine der folgenden Optionen aus.  

    |Option|Description|
    |---|----|
    |**Lieferungen**|Mit der ausgewählten Zeile verknüpfte gebuchte Lieferungen.|
    |**Rechnungen**|Mit der ausgewählten Zeile verknüpfte gebuchte Rechnungen.|
    |**Rücksendungen**|Mit der ausgewählten Zeile verknüpfte gebuchte Rücksendungen.|
    |**Gutschriften**|Mit der ausgewählten Zeile verknüpfte gebuchte Gutschriften.|

5.  Klicken Sie auf der Seite **Verkaufszeile** auf Zeile **Beleg anzeigen** , um den Posten anzuzeigen.

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Erstellen von Montagerahmenaufträgen](assembly-how-to-create-blanket-assembly-orders.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
