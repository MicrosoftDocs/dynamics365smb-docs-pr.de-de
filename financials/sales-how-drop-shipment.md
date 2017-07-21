---
title: "Erstellen Sie einen Verkaufsauftrag, der mit einer Einkaufsbestellung für eine direkte Lieferung verknüpft ist| Microsoft Docs"
description: "Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-make-drop-shipments"></a>So geht's: Direktlieferungen erstellen
Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.

Wenn ein Verkaufsauftrag für Direktlieferung markiert wird und Sie eine Bestellung erstellen, in der der Debitor im Feld **Verk. an Deb.-Nr.** angegeben wird, können Sie die beiden Belege verknüpfen und somit den Kreditor anweisen, direkt an den Kunden zu versenden.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung
Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel, außer dass Sie in der Verkaufsauftragszeile angeben müssen, dass für den Verkauf Direktlieferung benötigt wird.

1. Legen Sie einen Verkaufsauftrag für einen Artikel an. Weitere Informationen finden Sie unter [So geht's: Produkte verkaufen](sales-how-sell-products.md)
2. Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**. Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>So erstellen Sie Bestellungen für Direktlieferungen:
Um eine Direktlieferung für den Artikel, der verkauft werden soll, vorzubereiten, erstellen Sie eine normale Bestellung, außer dass Sie in der Bestellung angeben müssen, dass direkt an den Debitoren geliefert wird, nicht an Sie selbst.

1. Erstellen Sie eine Bestellung. Füllen Sie keines dieser Felder in den Zeilen aus. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
2. Wählen Sie im Feld **Verk. an Deb.-Nr.** den Debitor aus, an die Sie verkaufen.
3. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
4. Im Fenster **Verkaufsübersicht** wählen Sie den Auftrag, den Sie im Abschnitt "So erstellen Sie einen Verkaufsauftrag für Direktlieferung" vorbereitet haben.
5. Wählen Sie die Schaltfläche **OK** aus.

Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.

Sie können nun den Kreditor anweisen, die Artikel an Ihren Kunden zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>So zeigen Sie den verknüpften Auftrag aus der Bestellung an
* Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.

## <a name="to-post-a-drop-shipment"></a>So buchen Sie eine Direktlieferung:
Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen. Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.

1. Alternativ wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsauftrag** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie den Verkaufsauftrag, den Sie im Abschnitt "So erstellen Sie einen Verkaufsauftrag für Direktlieferung" erstellt haben.
3. Geben Sie im Feld **Zu liefern** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.
4. Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.
5. Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.

## <a name="see-also"></a>Siehe auch
[Gewusst wie: Produkte verkaufen](sales-how-sell-products.md)  
[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Verkauf](sales-manage-sales.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

