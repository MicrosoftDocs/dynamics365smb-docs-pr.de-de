---
title: Intercompany Belege und Erfassungen posten
description: 'Dieses Thema erklärt, wie Sie Intercompany-Belege oder Erfassungen verwenden, um Transaktionen mit Ihren Intercompany-Partnern zu buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals"></a><a name="work-with-intercompany-documents-and-journals"></a>Arbeiten mit Intercompany-Belegen und Buch.-Blättern

Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwenden. Sie können Transaktionen auf Sachkonten buchen, und wenn Sie Intercompany-Bankkonten eingerichtet haben, können Sie auch Bank-zu-Bank-Transaktionen buchen. Weitere Informationen zum Einrichten von Intercompany-Bankkonten finden Sie unter [Angeben der Bankkonten, die für Intercompanypartner verwendet werden sollen](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Sie übertragen die Leitung von Ihrem Postausgang zu Ihrem Partner. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

Für Verkaufsaufträge und Einkaufsbelege stellt der Intercompanypartner auf den entsprechenden Debitor oder Kreditor sicher, dass alle Aufträge und Rechnungen für Transaktionen zwischen den Partnern entsprechende Belege in den Partnerunternehmen erstellen. Die Firmenkonten saldieren korrekt.

Dasselbe gilt für Intercompany-Hauptbuchungszeilen. Sie müssen keine Konten angeben, Sie wählen einfach das Partnerunternehmen aus. In der Partnerfirma werden dann entsprechende Intercompany-Fbu Buch.-Blattzeilen erstellt.

## <a name="fill-in-and-send-an-intercompany-sales-order"></a><a name="fill-in-and-send-an-intercompany-sales-order"></a>Einen Intercompanyauftrag ausfüllen und senden

Aufträge, Bestellungen und Reklamationen können vor der Buchung gesendet werden. Rechnungen und Gutschriften können jedoch erst gesendet werden, nachdem sie gebucht sind.

Im Folgenden wird beschrieben, wie ein Intercompanyauftrag ausgefüllt und gesendet wird. Die gleichen Schritte gelten auch für Intercompanybestellungen und Reklamationen und Intercompanyrechnungen auf Rechnungen und Gutschriften.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Um neue Verkaufsaufträge zu erstellen, wählen Sie **Neu**. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Stellt sicher, dass der Debitor ein Intercompany-Partner ist.
5. Um den Verkaufsauftrag zu senden, bevor Sie ihn buchen, wählen Sie die **IC Verkaufsauftrag senden** Aktion aus.

> [!NOTE]
> Wenn Sie Schritt 5 ausführen, wird der Verkaufsauftrag auf den Intercompany-Ausgang verschoben, wo er später dann gebucht werden kann. Um mehr über den Intercompany-Eingang und -Ausgang zu erfahren, gehen Sie zu [Verwalten Sie den Intercompany-Eingang und -Ausgang](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal"></a><a name="fill-in-and-post-an-intercompany-journal"></a>Intercompany-Buch.-Blätter ausfüllen und buchen

Wenn Sie einen Intercompanybeleg oder eine Buch.-Blattzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Seit dem 1. Veröffentlichungszyklus 2022 können Sie das Unternehmen für die automatische Erstellung empfangener Intercompany-Transaktionen von Intercompany-Partnern einrichten, die über das Intercompany-Hauptbuch gebucht werden. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Intercompany-Fibu Buch.-Blätter** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie das Buch.-Blatt. Weitere Informationen finden Sie unter [Arbeiten mit Allgemeinen Buch.-Blättern](ui-work-general-journals.md).
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Feld **IC Partner-Sachkontonr** das IC-Sachkonto ein, auf das der Betrag beim Partnerunternehmen gebucht wird.

    > [!NOTE]
    > Das Feld muss auf einer Zeile mit einem Bank- bzw. Sachkonto im Feld **Kontonr.** oder **Gegenkontonr.** ausgefüllt werden.  
5. Wählen Sie die Aktion **Buchen**.

Die entsprechenden Posten werden im Unternehmen gebucht und ein Buch.-Blatt mit den entsprechenden Posten werden in den Intercompanyausgang erstellt, die Sie dann an das Partnerunternehmen senden können.

## <a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
