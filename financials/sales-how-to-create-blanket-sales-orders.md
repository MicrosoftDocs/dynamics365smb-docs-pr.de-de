---
title: "Vorgehensweise: Erstellen von Rahmenaufträgen| Microsoft Docs"
description: "Verwenden Sie Rahmenaufträge, wenn ein Kunde der Abnahme großer Mengen zugestimmt hat, die in mehreren kleineren Lieferungen über einen bestimmten Zeitraum geliefert werden sollen."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 89db93227222d79e535f2d18400330aa30566f2f
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-blanket-sales-orders"></a>Arbeiten mit Rahmenaufträgen
Ein Rahmenauftrag stellt ein Gerüst für eine langfristige Vereinbarung zwischen Ihnen und einem Debitor dar.

Ein Rahmenauftrag wird in der Regel erstellt, wenn sich ein Debitor verpflichtet hat, größere Mengen abzunehmen, die über einen längeren Zeitraum in mehreren kleineren bereitgestellt werden. Häufig decken Rahmenaufträge nur einen bestimmten Artikel ab, für den bestimmte Liefertermine vorgegeben sind. Der Hauptgrund für die Verwendung eines Rahmenauftrags anstelle eines Verkaufsauftrags besteht darin, dass die bei einem Rahmenauftrag eingegebenen Mengen keinen Einfluss auf die Artikelverfügbarkeit haben und daher als Arbeitsvorlage für die Überwachung und Planung verwendet werden können.

In einem Rahmenauftrag kann jede einzelne Lieferung als Auftragszeile eingerichtet werden, die dann zum Zeitpunkt der Lieferung in einen Auftrag umgewandelt werden kann.

Rahmenaufträge werden beispielsweise verwendet, wenn ein Kunde anruft und 1000 Einheiten eines Artikels bestellt, die über den kommenden Monat in Mengen von je 250 Stck. pro Woche geliefert werden sollen.

> [!NOTE]
> Rahmenbestellungen funktionieren auf ähnliche Weise wie Rahmenaufträge. Die Dokumentation enthält keine Rahmenbestellungen.

## <a name="to-create-a-blanket-sales-order"></a>So legen Sie einen Rahmenauftrag an:  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rahmenbestellungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Nehmen Sie im Feld **Auftragsdatum** keine Eingabe vor. Wenn die einzelnen Verkaufsaufträge anhand des Rahmenauftrags erstellt werden, wird als Auftragsdatum des Verkaufsauftrags automatisch das Arbeitsdatum festgelegt.
5. Erstellen Sie im Inforegister **Zeilen** einzelne Zeilen für jede Lieferung. Wenn der Kunde beispielsweise 1.000 Einheiten gleichmäßig auf vier Wochen verteilt erhalten möchte, geben Sie vier separate Zeilen mit jeweils 250 Einheiten ein.   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>So erstellen Sie einen Auftrag aus einem Rahmenauftrag:  

1.  Um einen Auftrag für eine oder mehrere der Zeilen des Montagerahmenauftrags zu erstellen, entfernen Sie die Menge im Feld **Zu liefern** in allen Zeilen, für die zum aktuellen Zeitpunkt KEINE Lieferung gewünscht wird.  
2.  Wenn Sie die Aufträge erstellen möchten, klicken Sie auf **Auftrag erst.** und anschließend auf **Ja**. Sie werden in einer Meldung darüber informiert, dass dem Rahmenauftrag eine Auftragsnummer zugewiesen wurde. Beachten Sie, dass der Rahmenauftrag nicht gelöscht wurde.  
3.  Wählen Sie die Schaltfläche **OK** aus.  
4.  Um die Ergebnisse der vorangehenden Schritte anzuzeigen, wählen Sie auf dem Inforegister **Zeilen** die Option **Aktionen**, wählen Sie Zeile, wählen Sie Nicht gebuchte Zeilen, und wählen Sie dann **Aufträge**.  
5.  Wählen Sie im Fenster **Verkaufszeilen** den entsprechenden Verkaufsauftrag aus. Wählen Sie auf dem Inforegister **Zeilen** die Option Aktionen, wählen Sie Zeile, und wählen Sie dann **Beleg anzeigen**.  

Das folgende gilt für Verkaufsaufträge nach der Erstellung von Rahmenaufträgen:  

- Nachdem der Rahmenauftrag in einen Auftrag umgewandelt wurde, enthält diese sämtliche Zeilen des Rahmenauftrags. Die Mengen der Zeilen, bei denen die Menge im Feld **Zu liefern** gelöscht wurde, werden mit leerem Feld **Menge** angezeigt. Sie können diese Zeilen bearbeiten oder löschen oder unverändert beibehalten.  
- Beachten Sie unbedingt, dass die Menge der Auftragszeile die Menge der zugehörigen Rahmenauftragszeile nicht übersteigen darf. Andernfalls kann der Auftrag nicht gebucht werden.  
- Wenn der Auftrag als geliefert und/oder als fakturiert gebucht wurde, werden die Felder **Menge geliefert** und **Menge fakturiert** auf des zugehörigen Rahmenauftrags automatisch aktualisiert.  
- Die Nummer des Rahmenauftrags und die Zeilennummer werden als Eigenschaften der Auftragszeilen erfasst, wenn diese aus einem Rahmenauftrag erstellt wurden.  
- Wenn Aufträge nicht direkt aus einem Rahmenauftrag erstellt werden, aber dennoch zu diesem gehören, kann eine Verknüpfung zwischen einem Auftrag und einem Rahmenauftrag eingerichtet werden, indem die Nummer des verknüpften Rahmenauftrags im Feld **Rahmenauftragsnr.** in der Auftragszeile eingegeben wird. Lagerdurchlaufzeit" der Einkaufsbestellung.  
- Nachdem der Verkaufsauftrag für die Gesamtmenge einer Rahmenbestellzeile erstellt wurde, kann kein anderer Verkaufsauftrag für dieselbe Zeile erstellt werden. Benutzer können im Feld **Zu liefern** keine Menge eingeben. Wenn in einem Rahmenauftrag jedoch weitere Mengen hinzugefügt werden müssen, kann der Wert im Feld **Menge** erhöht werden, und es können weitere Aufträge erstellt werden.  
- Der fakturierte Rahmenauftrag verbleibt im System, bis er gelöscht wird, und zwar entweder durch Löschen einzelner Rahmenaufträge oder durch Ausführen der Stapelverarbeitung **Erledigte Rahmenauftr. löschen**.  
- Wenn ein Debitor im Anwendungsbereich "Marketing" auch als Kontakt eingerichtet wurde und Sie einen Aktivitätenvorlagencode für Rahmenaufträge im Fenster **Marketing & Vertrieb Einr.** angegeben haben, wird eine Aktivität in der Tabelle "Aktivitätenprotokollposten" aufgezeichnet, wenn Sie **Drucken** auswählen, um die Rahmenaufträge zu drucken.

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a>So zeigen Sie den Status einer Rahmenbestellung an  
Sie können sich den Status einer Rahmenbestellung in dem Fenster **Einkaufsstatistik Rahmenbestellung** anzeigen lassen. Dies kann dann von Bedeutung sein, wenn Sie beginnen, die Bestellung zu fakturieren, die aus der Rahmenbestellung erstellt wurde.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rahmenbestellungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie eine Rahmenbestellung aus, und wählen Sie die **Statistik** Aktion aus.  
3.  Im Fenster **Einkaufsstatistik Rahmenbestellung** finden Sie auf dem Inforegister **Allgemein** zusammengefasste Informationen über die gesamte Bestellung, basierend auf den Gesamtmengen in den verschiedenen **Mengenfeldern** in den Rahmeneinkaufsbestellungszeilen.  

    - Auf dem Inforegister **Fakturierung** finden Sie zusammengefasste Informationen über die Gesamtmenge in den verschiedenen Feldern **Zu fakturieren** in den Einkaufsrahmenbestellungszeilen.  
    - Auf dem Inforegister **Lieferung** werden zusammengefasste Informationen über die Gesamtmenge in den verschiedenen Feldern **Zu liefern** in den Einkaufsrahmenbestellungszeilen angezeigt.  
    - Auf dem Inforegister **Vorauszahlung** werden zusammenfassende Informationen zu den vorab bezahlten Beträgen angezeigt.  
    - Auf dem Inforegister **Kreditor** werden bestimmte grundlegende Informationen über den Kreditor angezeigt.    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Um gebuchte und nicht gebuchte Rahmenbestellungszeilen anzuzeigen   
Die Verknüpfung zwischen dem Rahmenauftrag und dem daraus stammenden Verkaufsauftrag und jeder andere Verkaufsbeleg wird beibehalten, nachdem sie als Liste gebuchter und ungebuchter Verkaufsauftrags- und Rechnungszeilen gebucht wurden.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Rahmenbestellungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Rahmenbestellung, die Sie anzeigen möchten.
3. Sie können nicht gebuchte Posten anzeigen, indem Sie die entsprechende Zeile markieren und dann auf dem Inforegister  Zeilen auf  Aktionen,  **Zeile**,  **Nicht gebuchte Zeilen** klicken. Wählen Sie eine der folgenden Optionen aus.  

    <table>
    <tr>
    <th>Option</th>
    <th>Description</th>
    </tr>
    <tr>
    <td>**Aufträge**</td>
    <td>Gibt mit der ausgewählten Zeile verknüpfte offene Aufträge an.</td>
    </tr>
    <tr>
    <td>**Rechnungen**</td>
    <td>Gibt mit der ausgewählten Zeile verknüpfte offene Rechnungen an. Offene Rechnungen werden durch Eingabe der Nummer des Rahmenauftrags in der Verkaufsrechnungszeile manuell mit einem Rahmenauftrag verknüpft.</td>
    </tr>
    <tr>
    <td>**Reklamationen**</td>
    <td>Gibt mit der ausgewählten Zeile verknüpfte offene Reklamationen an.</td>
    </tr>
    <tr>
    <td>**Gutschriften**</td>
    <td>Gibt mit der ausgewählten Zeile verknüpfte offene Gutschriften an.</td>
    </tr>
    </table>
4.Sie können nicht gebuchte Posten anzeigen, indem Sie die entsprechende Zeile markieren und dann auf dem Inforegister  **Zeilen** auf  Aktionen,  Zeile,  **Gebuchte Zeilen** klicken. Wählen Sie eine der folgenden Optionen aus.  

    <table>
    <tr>
    <th>Option</th>
    <th>Description</th>
    </tr>
    <tr>
    <td>**Lieferungen**</td>
    <td>Mit der ausgewählten Zeile verknüpfte gebuchte Lieferungen.</td>
    </tr>
    <tr>
    <td>**Rechnungen**</td>
    <td>Mit der ausgewählten Zeile verknüpfte gebuchte Rechnungen.</td>
    </tr>
    <tr>
    <td>**Rücksendungen**</td>
    <td>Mit der ausgewählten Zeile verknüpfte gebuchte Rücksendungen.</td>
    </tr>
    <tr>
    <td>**Gutschriften**</td>
    <td>Mit der ausgewählten Zeile verknüpfte gebuchte Gutschriften.</td>
    </tr>
    </table>
5. Klicken Sie im Fenster **Verkaufszeile** auf Zeile, **Beleg anzeigen**, um den Posten anzuzeigen.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

