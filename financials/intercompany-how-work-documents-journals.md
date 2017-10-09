---
title: "Buchen Sie Intercompany-Belege und Buch.-Blätter | Microsoft Docs"
description: Verwenden von Intercompanybelegen zum Buchen der Transaktionen zwischen Intercompanypartnern
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: eeb070e1431d55248a762b444c2298281b0a5101
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-intercompany-documents-and-journals"></a>Vorgehensweise: Arbeiten mit Intercompany-Belegen und Buch.-Blättern
Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwendet. Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

Für Verkaufsaufträge und Einkaufsbelege stellt der IC-Partnercode auf den entsprechenden Debitor oder Kreditor sicher, dass alle Aufträge und Rechnungen, die Transaktionen mit diesen Unternehmen generiert haben, entsprechende Belege in dem Partnerunternehmen, werden mit dem Ergebnis des Ausgleichs die richtigen Konten.

Für Intercompany-Buchungszeilen müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Mithilfe von Intercompanybuchungen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren.

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a>Einen Intercompanyauftrag ausfüllen und senden:
Aufträge, Bestellungen und Reklamationen können vor der Buchung gesendet werden. Rechnungen und Gutschriften können jedoch erst gesendet werden, nachdem sie gebucht sind.

Im Folgenden wird beschrieben, wie ein Intercompanyauftrag ausgefüllt und gesendet wird. Die gleichen Schritte gelten auch für Intercompanybestellungen und Reklamationen und Intercompanyrechnungen auf Rechnungen und Gutschriften.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Verkaufsaufträge** ein und wählen dann den zugehörigen Link aus.  
2. Um neue Verkaufsaufträge zu erstellen, wählen Sie **Neu**. Weitere Informationen finden Sie unter [So geht's: Produkte verkaufen](sales-how-sell-products.md)  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Stellt sicher, dass er Kunde ein Intercompany-Partner ist.
5. Um den Verkaufsauftrag zu senden, bevor Sie ihn buchen, wählen Sie die **IC Verkaufsauftrag senden** Aktion aus.

> [!NOTE]
> Wenn Sie Schritt 4 ausführen, wird der Verkaufsauftrag auf den Intercompany-Ausgang verschoben, wo er später gebucht werden kann. Weitere Informationen finden Sie unter [Vorgehensweise: Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## <a name="to-fill-in-and-post-an-intercompany-journal"></a>Intercompany-Buch.-Blätter ausfüllen und buchen:
Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **IC Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Öffnet das entsprechende Fibu Buch.-Blatt Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)
3. Füllen Sie die Felder je nach Bedarf aus.
4. Geben Sie im Feld **IC Partner-Sachkontonr** das IC-Sachkonto ein, auf das der Betrag beim Partnerunternehmen gebucht wird.

    > [!NOTE]
    > Das Feld muss auf einer Zeile mit einem Bank- bzw. Sachkonto im Feld **Kontonr.** oder  **Gegenkontonr.** ausgefüllt werden.  
5. Wählen Sie die Aktion **Buchen** aus.

Die entsprechenden Posten werden im Unternehmen gebucht und ein Buch.-Blatt mit den entsprechenden Posten werden in den Intercompanyausgang erstellt, die Sie an das Partnerunternehmen senden können. Weitere Informationen finden Sie unter [Vorgehensweise: Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md). 

## <a name="see-also"></a>Siehe auch
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

