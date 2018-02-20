---
title: 'Vorgehensweise: Artikel reservieren | Microsoft Docs'
description: "Sie können Artikel für Verkaufsaufträge, Einkaufsbestellungen und Fertigungsaufträgen reservieren. Sie können Artikel in Lager oder eingehenden in Zeilen der offenen Belegzeile reservieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 61ecdcd1c87d267e19047be5424e1c07e832316a
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="reserve-items"></a>Artikel reservieren
Reservieren Sie Lager oder eingehenden Artikel für Verkaufsaufträge, Bestellungen, Serviceaufträge, Montageaufträge oder Fertigungsaufträge. Sie können Artikel in Lager oder eingehenden in Zeilen der offenen Belegzeile reservieren. Sie führen die Arbeit im Fenster **Reservierungen** aus.

Jede Zeile in **Reservierung**beinhaltet Informationen zu der Art der Zeile (Verkauf, Einkauf, Buchungsblatt) oder der Postenart. Die Zeilen zeigen an, wie viele Artikel von jeder Art von Zeile oder Posten für die Reservierung verfügbar sind.

## <a name="to-reserve-items-for-sales"></a>So reservieren Sie Artikel für Verkäufe:
Nachfolgend wird erläutert, wie Entscheidungsträger als Artikel aus einem Verkaufsauftrag reserviert werden. Die Schritte sind gleich für Einkaufs-, Service- und Montageaufträge.  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Verkaufsaufträge** ein und wählen Sie dann den zugehörigen Link aus.  
2.  Klicken Sie in einem Verkaufsauftrag auf dem Inforegister **Zeilen** auf **Reservieren**. Das Fenster **Reservierung** wird geöffnet.  
3. Wählen Sie in die Zeile, aus der Sie Artikel reservieren möchten.  
4. Wählen Sie eine der folgenden Optionen aus.  

    |**Funktion**|**Beschreibung**|
    |------------------|---------------------|  
    |**Autom. reservieren**|Um die Artikel in dem Fenster **Reservierung** automatisch zu reservieren.|  
    |**Von aktueller Zeile reservieren**|Um die Artikel aus dem Beleg in der Zeile zu reservieren, die Sie ausgewählt haben.|  
    |**Reservierung der aktuellen Zeile stornieren**|Um die Reservierung der Artikel in dem Beleg und in der Zeile, die Sie ausgewählt haben, zu stornieren.|

> [!NOTE]  
>  Falls für den Verkaufsauftrag Artikelverfolgungszeilen vorhanden sind, führt das Reservierungssystem spezielle Schritte durch: Weitere Informationen hierzu finden Sie unter "Chargen- oder Seriennummern reservieren".  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Artikel für FA-Zeilen reservieren  
Sie können Artikel für Erstellungsaufträge reservieren. Sie müssen zwischen Produktionsauftragszeilen, d.h. übergeordnete Artikel und Produktionsauftragskomponenten unterscheiden.

Im weiteren Prozess wird ein fest geplanter Fertigungsauftrag verwendet.   
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus und geben Sie **Feste Auftragsplanung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie den fest geplanten Produktionsauftrag, den Sie für übergeordnete Artikel reservieren möchten.  
3. Wählen Sie die entsprechende FA-Zeilennummer aus.  
4. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus.
5. Wählen Sie im Fenster **Resevierung**die Zeile **Verkaufszeile, Auftrag**, und klicken Sie dann auf Aktionen in der Gruppe Funktion, und wählen Sie **Von aktueller Zeile reservieren**.  

Die Menge, die Sie im fest geplanten Fertigungsauftrag eingetragen haben, ist reserviert.

## <a name="to-reserve-items-for-production-order-components"></a>Artikel für FA-Komponenten reservieren  
Sie können Artikel für Erstellungsaufträge reservieren. Sie müssen zwischen Produktionsauftragszeilen, d.h. übergeordnete Artikel und Produktionsauftragskomponenten unterscheiden.

Im weiteren Prozess wird ein fest geplanter Fertigungsauftrag verwendet.    
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus und geben Sie **Feste Auftragsplanung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie den fest geplanten FA, für den Sie Komponentenartikel reservieren möchten.  
3. Wählen Sie die entsprechende FA-Zeilennummer aus.  
4. Wählen Sie auf dem Inforegister **Zeilen** die Option **Zeile** und dann **Posten** aus.  
5. Wählen Sie die entsprechende Komponentenzeile aus.  
6. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus.  
7. Wählen Sie im Fenster **Resevierung** eine Zeile und wählen **Aus aktueller Zeile reservieren** aus.  

Die Menge, die Sie in der fest geplanten Fertigungskomponentenzeile eingetragen haben, ist nun reserviert.

## <a name="to-change-a-reservation"></a>So ändern Sie eine Reservierung:  
Gelegentlich kann es erforderlich sein, eine Artikelreservierung zu ändern.   
1. Von der Belegzeile, aus der Sie im Inforegister **Zeilen** reserviert haben, wählen Sie die **Reservieren** Aktion aus.  
2. Im Fenster **Reservierung** wählen Sie die **Reservierungsposten** Aktion aus.
3. Klicken Sie in der Zeile **Reservierungseinträge** auf **Menge** aktualisieren auf der Zeile, die Sie ändern möchten.
4. Bestätigen Sie die nachfolgende Meldung, indem Sie die Schaltfläche **OK** auswählen.

## <a name="to-cancel-a-reservation"></a>So stornieren Sie eine Reservierung  
Gelegentlich kann es erforderlich sein, eine Artikelreservierung zu stornieren.   
1. Von der Belegzeile, aus der Sie im Inforegister **Zeilen** reserviert haben, wählen Sie die **Reservieren** Aktion aus.  
2. Im Fenster **Reservierung** wählen Sie die **Reservierungsposten** Aktion aus.  
3.  Im Fenster **Reservierung** wählen Sie die **Reservierung abbrechen** Aktion aus.  
4.  Bestätigen Sie die nachfolgende Meldung, indem Sie die Schaltfläche **OK** auswählen.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>So reservieren Sie eine bestimmte Serien- oder Chargennummer  
Aus ausgehenden Dokumenten für Artikel mit Artikelverfolgung, wie Verkaufsaufträge oder Listen mit Fertigungskomponenten, können Sie bestimmte Serien- oder Chargennummern reservieren. Dies kann beispielsweise relevant sein, wenn Sie Fertigungskomponenten aus einer bestimmten Charge benötigen, um die Konsistenz mit vorhergehenden Fertigungslosen sicherzustellen, oder weil ein Kunde eine bestimmte Seriennummer angefordert hat. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

Dies wird als spezifische Reservierung bezeichnet, da Sie eine Menge von Artikel X reservieren, die zu Charge X gehört. Wenn Sie einfach Mengen von Artikel X reservieren, ist dies eine normale, unspezifische Reservierung. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md).

Das folgende Verfahren basiert auf einer Auftragsabwicklung.    
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie eine Verkaufsauftragszeile für einen Artikel mit Artikelverfolgung.  
3. Weisen Sie dann der Verkaufsauftragszeile Serien- und Chargennummern zu. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).
4. Auf der Verkaufsauftragszeile wählen Sie die Aktion **Reservieren** aus.  
5. Wählen Sie die Schaltfläche **Ja**, um bestimmte Serien- oder Chargennummern zu reservieren.  
6. Wählen Sie im Fenster **Artikelnachverfolgungsliste** die Serien- und Chargennummernkombination aus, die Sie gerade zugewiesen haben.  
7. Wählen Sie die Schaltfläche **OK**, um das Fenster **Reservationen** zu öffnen, in dem nur der Bedarf angezeigt wird, der mit der angegebenen Artikelverfolgungsnummer verbunden ist. Bei nicht-spezifischen Reservierungen für eine der Artikelverfolgungsnummern, die Sie in dieser Zeile angegeben haben, werden Sie über die Menge informiert, die bereits reserviert wurde.  
8. Klicken Sie auf die Aktionen **Automatisch Reservieren**oder **Aus aktueller Zeile reservieren**, um die Reservierung für die speziellen Artikelverfolgungsnummern zu erstellen.

## <a name="see-also"></a>Siehe auch
[Lagerbest](inventory-manage-inventory.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetails: Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

