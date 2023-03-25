---
title: Intercompany Belege und Erfassungen posten
description: 'Dieses Thema erklärt, wie Sie Intercompany-Belege oder Erfassungen verwenden, um Transaktionen mit Ihren Intercompany-Partnern zu buchen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '600, 610'
ms.date: 03/09/2022
ms.author: edupont
---
# Arbeiten mit Intercompany-Belegen und Buch.-Blättern
Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwendet. Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

Für Verkaufsaufträge und Einkaufsbelege stellt der IC-Partnercode auf den entsprechenden Debitor oder Kreditor sicher, dass alle Aufträge und Rechnungen, die Transaktionen mit diesen Unternehmen generiert haben, entsprechende Belege in dem Partnerunternehmen, werden mit dem Ergebnis des Ausgleichs die richtigen Konten.

Für Intercompany-Buchungszeilen müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Mithilfe von Intercompanybuchungen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren.

## Einen Intercompanyauftrag ausfüllen und senden:
Aufträge, Bestellungen und Reklamationen können vor der Buchung gesendet werden. Rechnungen und Gutschriften können jedoch erst gesendet werden, nachdem sie gebucht sind.

Im Folgenden wird beschrieben, wie ein Intercompanyauftrag ausgefüllt und gesendet wird. Die gleichen Schritte gelten auch für Intercompanybestellungen und Reklamationen und Intercompanyrechnungen auf Rechnungen und Gutschriften.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Um neue Verkaufsaufträge zu erstellen, wählen Sie **Neu**. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Stellt sicher, dass der Debitor ein Intercompany-Partner ist.
5. Um den Verkaufsauftrag zu senden, bevor Sie ihn buchen, wählen Sie die **IC Verkaufsauftrag senden** Aktion aus.

> [!NOTE]
> Wenn Sie Schritt 4 ausführen, wird der Verkaufsauftrag auf den Intercompany-Ausgang verschoben, wo er später gebucht werden kann. Weitere Informationen finden Sie unter [Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## Intercompany-Buch.-Blätter ausfüllen und buchen:

Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Seit dem 1. Veröffentlichungszyklus 2022 können Sie das Unternehmen für die automatische Erstellung empfangener Intercompany-Transaktionen von Intercompany-Partnern einrichten, die über das Intercompany-Hauptbuch gebucht werden. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompany-Fibu Buch.-Blätter** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnet das entsprechende Fibu Buch.-Blatt. Weitere Informationen finden Sie unter [Arbeiten mit Allgemeinen Buch.-Blättern](ui-work-general-journals.md).
3. Füllen Sie die Felder nach Bedarf aus.
4. Geben Sie im Feld **IC Partner-Sachkontonr** das IC-Sachkonto ein, auf das der Betrag beim Partnerunternehmen gebucht wird.

    > [!NOTE]
    > Das Feld muss auf einer Zeile mit einem Bank- bzw. Sachkonto im Feld **Kontonr.** oder  **Gegenkontonr.** ausgefüllt werden.  
5. Wählen Sie die Aktion **Buchen** aus.

Die entsprechenden Posten werden im Unternehmen gebucht und ein Buch.-Blatt mit den entsprechenden Posten werden in den Intercompanyausgang erstellt, die Sie an das Partnerunternehmen senden können. Weitere Informationen finden Sie unter [Verwalten des IC-Eingangs und Ausgangs](intercompany-how-manage-intercompany-inbox.md).

## Siehe auch

[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]