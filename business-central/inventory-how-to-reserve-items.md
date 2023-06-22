---
title: Wie Sie Artikel reservieren
description: 'Sie können Artikel für Verkaufsaufträge, Einkaufsbestellungen und Fertigungsaufträgen reservieren. Sie können auch Artikel in Lager oder eingehenden in Zeilen der offenen Belegzeile reservieren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 08/11/2022
ms.author: edupont
---
# <a name="reserve-items" />Artikel reservieren

Reservieren Sie Lager oder eingehenden Artikel für Verkaufsaufträge, Bestellungen, Montageaufträge, Umlagerungsaufträge oder Fertigungsaufträge. Sie können Artikel auch in Lager oder eingehenden in Zeilen der offenen Belegzeile reservieren. Sie tun dies auf der Seite **Reservierung**.

Jede Zeile, die Sie zum Reservieren der Artikel auf der Seite **Reservierung** öffnen, beinhaltet Informationen zu der Art der Zeile (Verkauf, Einkauf, Buchungsblatt) oder der Postenart. Die Zeilen zeigen an, wie viele Artikel von jeder Art von Zeile oder Posten für die Reservierung verfügbar sind.

## <a name="reserve-items-for-sales" />Sie Artikel für Verkäufe reservieren

Nachfolgend wird erläutert, wie Entscheidungsträger als Artikel aus einem Verkaufsauftrag reserviert werden. Die Schritte sind gleich für Einkaufs-, Service-, Umlagerungs- und Montageaufträge.
  
1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Verkaufsauftrag.
3. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus. Die Seite **Reservierung** wird geöffnet.  
4. Wählen Sie in die Zeile, aus der Sie Artikel reservieren möchten.  
5. Wählen Sie eine der folgenden Optionen aus.  

    |**Funktion**|**Beschreibung**|
    |------------------|---------------------|  
    |**Autom. reservieren**|Um die Artikel in dem Fenster **Reservierung** automatisch zu reservieren.|  
    |**Von aktueller Zeile reservieren**|Um die Artikel aus dem Beleg in der Zeile zu reservieren, die Sie ausgewählt haben.|  
    |**Reservierung der aktuellen Zeile stornieren**|Um die Reservierung der Artikel in dem Beleg und in der Zeile, die Sie ausgewählt haben, zu stornieren.|

> [!NOTE]  
> Falls für den Verkaufsauftrag Artikelverfolgungszeilen vorhanden sind, führt das Reservierungssystem spezielle Schritte durch: Weitere Informationen hierzu finden Sie im Abschnitt [So reservieren Sie eine bestimmte Serien- oder Chargennummer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## <a name="reserve-an-item-for-a-production-order-line" />Artikel für FA-Zeilen reservieren

Sie können Artikel für Erstellungsaufträge reservieren. Sie müssen zwischen Produktionsauftragszeilen, d.h. übergeordnete Artikel und Produktionsauftragskomponenten unterscheiden.

Im folgenden Verfahren wird ein fest geplanter Fertigungsauftrag verwendet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Firm Planned Prod. Auftrag** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den fest geplanten Produktionsauftrag, den Sie für übergeordnete Artikel reservieren möchten.  
3. Wählen Sie die entsprechende FA-Zeilennummer aus.  
4. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus.
5. Wählen Sie auf der Seite **Resevierung** die Zeile **Verkaufszeile, Auftrag**, und klicken Sie dann auf Aktionen in der Gruppe Funktion, und wählen Sie **Von aktueller Zeile reservieren**.  

Die Menge, die Sie im fest geplanten Fertigungsauftrag eingetragen haben, ist reserviert.

## <a name="reserve-items-for-production-order-components" />Artikel für FA-Komponenten reservieren

Sie können Artikel für Erstellungsaufträge reservieren. Sie müssen zwischen Produktionsauftragszeilen, d.h. übergeordnete Artikel und Produktionsauftragskomponenten unterscheiden.

Im folgenden Verfahren wird ein fest geplanter Fertigungsauftrag verwendet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Firm Planned Prod. Auftrag** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den fest geplanten FA, für den Sie Komponentenartikel reservieren möchten.  
3. Wählen Sie die entsprechende FA-Zeilennummer aus.  
4. Wählen Sie auf dem Inforegister **Zeilen** die Option **Zeile** und dann **Posten** aus.  
5. Wählen Sie die entsprechende Komponentenzeile aus.  
6. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus.  
7. Wählen Sie auf der Seite **Resevierung** eine Zeile und wählen **Aus aktueller Zeile reservieren** aus.  

Die Menge, die Sie in der fest geplanten Fertigungskomponentenzeile eingetragen haben, ist nun reserviert.

## <a name="change-a-reservation" />Reservierung ändern

Gelegentlich kann es erforderlich sein, eine Artikelreservierung zu ändern.

1. Von der Belegzeile, aus der Sie im Inforegister **Zeilen** reserviert haben, wählen Sie die **Reservieren** Aktion aus.  
2. Auf der Seite **Reservierung** wählen Sie die **Reservierungsposten** Aktion aus.
3. Klicken Sie auf der Seite **Reservierungseinträge** auf **Menge** aktualisieren auf der Zeile, die Sie ändern möchten.
4. Bestätigen Sie die nachfolgende Meldung, indem Sie die Schaltfläche **OK** auswählen.

## <a name="cancel-a-reservation" />Reservierung stornieren

Gelegentlich kann es erforderlich sein, eine Artikelreservierung zu stornieren.

1. Von der Belegzeile, aus der Sie im Inforegister **Zeilen** reserviert haben, wählen Sie die **Reservieren** Aktion aus.  
2. Auf der Seite **Reservierung** wählen Sie die **Reservierungsposten** Aktion aus.  
3. Auf der Seite **Reservierung** wählen Sie die **Reservierungsposten stornieren** Aktion aus.  
4. Bestätigen Sie die nachfolgende Meldung, indem Sie die Schaltfläche **OK** auswählen.  

## <a name="reserve-a-specific-serial-or-lot-number" />Bestimmte Serien- oder Chargennummer reservieren

Aus ausgehenden Dokumenten für Artikel mit Artikelverfolgung, wie Verkaufsaufträge oder Listen mit Fertigungskomponenten, können Sie bestimmte Serien- oder Chargennummern reservieren. Dies kann beispielsweise relevant sein, wenn Sie Fertigungskomponenten aus einer bestimmten Charge benötigen, um die Konsistenz mit vorhergehenden Fertigungslosen sicherzustellen, oder weil ein Debitor eine bestimmte Seriennummer angefordert hat. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

Dies wird als spezifische Reservierung bezeichnet, da Sie eine Menge von Artikel X reservieren, die zu Charge X gehört. Wenn Sie einfach Mengen von Artikel X reservieren, ist dies eine normale, unspezifische Reservierung. Weitere Informationen unter [Designdetails – Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)

Das folgende Verfahren basiert auf einer Auftragsabwicklung.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine Verkaufsauftragszeile für einen Artikel mit Artikelverfolgung.  
3. Weisen Sie dann der Verkaufsauftragszeile Serien- und Chargennummern zu. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).
4. Auf der Verkaufsauftragszeile wählen Sie die Aktion **Reservieren** aus.  
5. Wählen Sie die Schaltfläche **Ja**, um bestimmte Serien- oder Chargennummern zu reservieren.  
6. Wählen Sie auf der Seite **Artikelnachverfolgungsliste** die Serien- und Chargennummernkombination aus, die Sie zugewiesen haben.  
7. Wählen Sie die Schaltfläche **OK**, um die Seite **Reservationen** zu öffnen, in dem nur der Bedarf angezeigt wird, der mit der angegebenen Artikelverfolgungsnummer verbunden ist. Bei nicht-spezifischen Reservierungen für eine der Artikelverfolgungsnummern, die Sie in dieser Zeile angegeben haben, werden Sie über die Menge informiert, die bereits reserviert wurde.  
8. Klicken Sie auf die Aktionen **Automatisch Reservieren** oder **Aus aktueller Zeile reservieren**, um die Reservierung für die speziellen Artikelverfolgungsnummern zu erstellen.

## <a name="see-related-microsoft-trainingtrainingmodulesmanage-outbound-serial-lot-numbers" />Siehe verwandte [Microsoft Schulungen](/training/modules/manage-outbound-serial-lot-numbers/)

## <a name="see-also" />Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetails: Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Arbeiten mit Seriennummern und Chargennummern](inventory-how-work-item-tracking.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
