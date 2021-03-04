---
title: Buchen Sie Intercompany-Belege und Buch.-Blätter | Microsoft Docs
description: Verwenden von Intercompanybelegen zum Buchen der Transaktionen zwischen Intercompanypartnern
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 338c5dce8ae2011bb36ad126d4926635a86d3e95
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746391"
---
# <a name="work-with-intercompany-documents-and-journals"></a>Arbeiten mit Intercompany-Belegen und Buch.-Blättern
Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwendet. Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

Für Verkaufsaufträge und Einkaufsbelege stellt der IC-Partnercode auf den entsprechenden Debitor oder Kreditor sicher, dass alle Aufträge und Rechnungen, die Transaktionen mit diesen Unternehmen generiert haben, entsprechende Belege in dem Partnerunternehmen, werden mit dem Ergebnis des Ausgleichs die richtigen Konten.

Für Intercompany-Buchungszeilen müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Mithilfe von Intercompanybuchungen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Einen Intercompanyauftrag ausfüllen und senden:
Aufträge, Bestellungen und Reklamationen können vor der Buchung gesendet werden. Rechnungen und Gutschriften können jedoch erst gesendet werden, nachdem sie gebucht sind.

Im Folgenden wird beschrieben, wie ein Intercompanyauftrag ausgefüllt und gesendet wird. Die gleichen Schritte gelten auch für Intercompanybestellungen und Reklamationen und Intercompanyrechnungen auf Rechnungen und Gutschriften.  

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Um neue Verkaufsaufträge zu erstellen, wählen Sie **Neu**. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Stellt sicher, dass der Debitor ein Intercompany-Partner ist.
5. Um den Verkaufsauftrag zu senden, bevor Sie ihn buchen, wählen Sie die **IC Verkaufsauftrag senden** Aktion aus.

> [!NOTE]
> Wenn Sie Schritt 4 ausführen, wird der Verkaufsauftrag auf den Intercompany-Ausgang verschoben, wo er später gebucht werden kann. Weitere Informationen finden Sie unter [Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Intercompany-Buch.-Blätter ausfüllen und buchen:
Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Intercompany Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnet das entsprechende Fibu Buch.-Blatt Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder je nach Bedarf aus.
4. Geben Sie im Feld **IC Partner-Sachkontonr** das IC-Sachkonto ein, auf das der Betrag beim Partnerunternehmen gebucht wird.

    > [!NOTE]
    > Das Feld muss auf einer Zeile mit einem Bank- bzw. Sachkonto im Feld **Kontonr.** oder  **Gegenkontonr.** ausgefüllt werden.  
5. Wählen Sie die Aktion **Buchen** aus.

Die entsprechenden Posten werden im Unternehmen gebucht und ein Buch.-Blatt mit den entsprechenden Posten werden in den Intercompanyausgang erstellt, die Sie an das Partnerunternehmen senden können. Weitere Informationen finden Sie unter [Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## <a name="see-also"></a>Siehe auch
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]