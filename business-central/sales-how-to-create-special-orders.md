---
title: 'So geht es: Besondere Aufträge herstellen | Microsoft Docs'
description: Sie können einen Spezialauftrag für einen bestimmten Katalogartikel erstellen, der an einen bestimmten Debitoren geliefert werden soll. Ihr Kreditor liefert den Artikel an Ihr Lager und Sie können den Artikel dann an Ihren Debitoren weiterleiten, entweder unabhängig von anderen Artikeln oder zusammen mit anderen Artikeln in einem anderen Auftrag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7f3e023ce290e59c6fda88d62bb7abffd83853bb
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251584"
---
# <a name="create-special-orders"></a>Spezialaufträge erstellen
Sie können einen Spezialauftrag für einen bestimmten Katalogartikel erstellen, der an einen bestimmten Debitoren geliefert werden soll. Ihr Kreditor liefert den Artikel an Ihr Lager und Sie können den Artikel dann an Ihren Debitoren weiterleiten, entweder unabhängig von anderen Artikeln oder zusammen mit anderen Artikeln in einem anderen Auftrag.  

Spezialaufträge setzen voraus, dass die Bestellung und der Verkaufsauftrag verknüpft sind, um sicherzustellen, dass der bestimmte Katalogartikel entnommen und an den Debitor geliefert wird.  

Bevor Sie diese Funktion verwenden können, müssen Sie die Karten für den Debitor, den Kreditor und die Artikel in dem Auftrag erstellen.  

## <a name="to-create-a-special-order"></a>So erstellen Sie Spezialaufträge:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus. Erstellen Sie einen  Verkaufsauftrag für den Artikel, und füllen Sie diesen aus. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3.  Geben Sie auf dem Inforegister **Zeilen** die Verkaufszeile ein. Wählen Sie im Feld **Einkaufscode** einen Einkaufscode mit einem Häkchen im Feld **Spezialauftrag** aus .

    Sie müssen nun aus einem Bestellvorschlag eine Bestellung erstellen.  
4. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Einlagerungsvorschlag** ein, und wählen dann den zugehörigen Link aus.  
5. Wählen Sie die Aktion **Spezialauftrag** aus, und dann die Aktion **Auftrag holen**.  
6.  Auf der Seite **Aufträge holen** werden Ergebnisse angezeigt, wobei **Belegnr.** die Verkaufsauftragsnummer ist. Wählen Sie die Schaltfläche **OK** aus. Es wird eine Bestellvorschlagszeile für den Artikel erstellt.  
7.  Wählen Sie in der Bestellvorschlagszeile im Feld **Ereignismeldung** die Option **Neu** aus.  
8.  Auf der Seite **Bestellauftrags-Arbeitsblatt** wählen Sie **Aktionsnachricht ausführen**. Auf der Seite **Ereignismeld. durchf. - Best.** wird geöffnet. Wählen Sie die Schaltfläche **OK** aus.  

    Es erscheint eine Meldung, dass die Einkaufsbestellungen erstellt wurden. Wählen Sie die Schaltfläche **OK**.  

Eine als Spezialauftrag für einen Verkaufsauftrag erstellte Bestellung wird vom Planungssystem berücksichtigt, da es Nachfrage und Angebot ausgleicht. Die Bestellung (Angebot) bleibt also auch dann mit dem Auftrag (Nachfrage) verknüpft, wenn sich mit der Bestellung eine frühere Nachfrage decken ließe. Weitere Informationen finden Sie unter [Designdetails: Behandlungs-Wiederbeschaffungsverfahren](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Sie können die Spezialauftragsfunktion nicht verwenden, wenn der Artikel bereits reserviert ist. Stellen Sie daher für Artikel, die im Rahmen von Spezialaufträgen verkauft werden, sicher, dass das Feld **Reserve** auf der Artikelkarte nicht auf **Immer** gesetzt ist.  

## <a name="see-also"></a>Siehe auch  
[Arbeiten mit Katalogartikeln](inventory-how-work-nonstock-items.md)  
[Verkauf](sales-manage-sales.md)  
[Direktlieferungen machen](sales-how-drop-shipment.md)   
[Designdetails: Wiederbeschaffungsverfahren](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
