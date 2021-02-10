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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c4549492e118d1b4367e89f2b0169f43ba7f8393
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748243"
---
# <a name="create-special-orders"></a>Spezialaufträge erstellen
Sie können einen Spezialauftrag für einen bestimmten Katalogartikel erstellen, der an einen bestimmten Debitoren geliefert werden soll. Ihr Kreditor liefert den Artikel an Ihr Lager und Sie können den Artikel dann an Ihren Debitoren weiterleiten, entweder unabhängig von anderen Artikeln oder zusammen mit anderen Artikeln in einem anderen Auftrag.  

Spezialaufträge setzen voraus, dass die Bestellung und der Verkaufsauftrag verknüpft sind, um sicherzustellen, dass der bestimmte Katalogartikel entnommen und an den Debitor geliefert wird.  

Bevor Sie diese Funktion verwenden können, müssen Sie die Karten für den Debitor, den Kreditor und die Artikel in dem Auftrag erstellen.  

## <a name="to-create-a-special-order"></a>So erstellen Sie Spezialaufträge:  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsauftrag** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**. Erstellen Sie einen  Verkaufsauftrag für den Artikel, und füllen Sie diesen aus. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3.  Geben Sie auf dem Inforegister **Zeilen** die Verkaufszeile ein. Wählen Sie im Feld **Einkaufscode** einen Einkaufscode mit einem Häkchen im Feld **Spezialauftrag** aus .

    Sie müssen nun aus einem Bestellvorschlag eine Bestellung erstellen.  
4. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Arbeitsblatt zur Genehmigung** ein, und wählen Sie dann den entsprechenden Link.  
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
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
