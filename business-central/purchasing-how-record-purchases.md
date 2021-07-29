---
title: Käufe mit Einkaufsrechnungen erfassen
description: Beschreibt, wie Sie Bestand, Nicht-Bestandsartikel oder Ressourcen erwerben, indem Sie Einkaufsrechnungen oder Bestellungen erstellen und buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 74c984d1abdd78f4d8af1364b3c8d285297a1cdd
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445501"
---
# <a name="record-purchases-with-purchase-invoices"></a>Käufe mit Einkaufsrechnungen erfassen

Sie erstellen eine Einkaufsrechnung oder Einkaufsbestellung, um die Kosten der Einkäufe zu erfassen und Kreditoren zu verfolgen. Wenn Sie einen Bestand steuern müssen, werden Einkaufsrechnungen und Einkaufsbestellungen auch verwendet, um Lagerbestände dynamisch zu aktualisieren, sodass Sie Ihre Lagerbestandskosten minimieren und besseren Debitorenservice bereitstellen können. Die Einkaufskosten, einschließlich Servicekosten und Bestandswerte, die aus der Buchung von Einkaufsrechnungen resultieren, tragen zu den Gewinnzahlen und anderen finanziellen Kennziffern in Ihrem Rollencenter bei.

## <a name="create-purchase-invoices"></a>Einkaufsrechnungen erstellen

Zusätzlich zum Kauf physischer Artikel (**Bestand** Artikelart), die sich auf die Bestandsbewertung auswirken, können Sie Dienstleistungen kaufen, die durch Zeiteinheiten dargestellt werden. Sie können dies entweder mit der Seite **Dienstleistung** Positionsart oder mit der Seite **Ressource** Zeilenart tun.

> [!NOTE]  
> Sie müssen Einkaufsbestellungen verwenden, wenn es für den Einkaufsprozess erforderlich ist, Teillieferungen einer Bestellmenge zu erfassen, weil beispielsweise die vollständige Menge beim Kreditor nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Einkaufsbestellungen verwenden. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Einkaufsbestellungen genau wie bei Einkaufsrechnungen. Das folgende Verfahren basiert auf einer Einkaufsrechnung. Die Schritte sind für eine Einkaufsbestellung ähnlich.

Wenn Sie die Bestandsartikel erhalten oder wenn die gekaufte Dienstleistung abgeschlossen ist, buchen Sie die Rechnung oder Bestellung, um die Bestands- und Finanzdaten zu aktualisieren und die Zahlung an den Lieferanten gemäß den Zahlungsbedingungen zu aktivieren. Weitere Informationen finden Sie unter [Käufe verbuchen](ui-post-purchases.md) und [Zahlungen vornehmen](payables-make-payments.md).

> [!CAUTION]  
> Buchen Sie die physischen Artikel einer Einkaufsrechnung erst dann, wenn Sie die Artikel erhalten und die endgültigen Kosten des Kaufs, einschließlich aller zusätzlichen Kosten, kennen. Andernfalls werden Ihr Lagerwert und DB-Zahlen möglicherweise falsch sein.

Gibt an, ob die Artikelkarte einen **Bestand**, **Service** und **Nicht-Bestand** ist, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md). Der Kaufsrechnungsprozess ist derselbe für alle drei Artikeltypen.

> [!NOTE]
> Mit dem Zeilentyp **Ressource** Bestellzeile können Sie auch externe Ressourcen einkaufen, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen. Weitere Informationen finden Sie unter [Ressourcen einrichten](projects-how-setup-resources.md).
>
> Um eine gekaufte Ressource zu verwenden, müssen Sie möglicherweise die Kapazität der Ressource festlegen und sie manuell einem Auftrag zuweisen. Durch den Kauf einer Ressource wird ein Ressourcen-Ledger-Eintrag erstellt, jedoch werden die Ressourcen-Sachkonto-Einträge nicht nach Menge und Wert verfolgt, wie dies z.B. bei Artikeln der Fall ist. Wenn eine Mengen- und Wertverfolgung erforderlich ist, sollten Sie die Verwendung anderer Positionsarten in Betracht ziehen.

Sie können die oberen Infoboxen des Einkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Kreditor bereits registriert ist.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-invoice"></a>Erstellen Sie eine neue Einkaufsrechnung.

Im Folgenden wird beschrieben, wie Sie eine Einkaufsrechnung erstellen. Bei einer Bestellung sind die Schritte ähnlich. Der Hauptunterschied besteht darin, dass Bestellungen zusätzliche Felder und Aktionen für die physische Handhabung von Artikeln haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Geben Sie im Feld **Kreditor** den Namen eines vorhandenen Kreditors ein.

    Andere Felder auf der Seite **Einkaufsrechnung** werden nun mit den Standardinformationen vom ausgewählten Kreditor ausgefüllt. Wenn der Kreditor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:

    1. Geben Sie im Feld **Kreditor** den Namen eines neuen Kreditors ein.
    2. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um den neuen Kreditor zu bestätigen.
    3. Auf der Seite **Vorlage für neuen Kreditor wählen** wählen Sie eine Vorlage, auf der die neue Kreditorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.
    4. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Das Feld **Name** ist mit dem Namen des neuen Kreditors vorausgefüllt, den Sie auf der Einkaufsrechnung eingegeben haben.
    5. Fahren Sie fort, die restlichen Felder auf der Kreditorenkarte auszufüllen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](purchasing-how-register-new-vendors.md).  
    6. Wenn Sie die Kreditorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zur Seite **Einkaufsrechnung** zurückzugehen.

    Einige Felder auf der Seite **Einkaufsrechnung** werden mit den Informationen, die Sie in der neuen Kreditorenkarte festgelegt haben, ausgefüllt.
3. Füllen Sie auf der Seite **Einkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Sie sind nun bereit, die Einkaufsrechnungszeilen mit Artikeln oder Ressourcen auszufüllen, die Sie vom Lieferanten gekauft haben.

    > [!NOTE]  
    > Wenn Sie wiederkehrende Einkaufszeilen für den Debitor, wie einen monatlichen Ersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Aktion **Wiederkehrende Einkaufszeilen** abrufen einfügen.
4. Geben Sie im Inforegister **Zeilen** im Feld **Artikelnr.** die Nummer eines Lagerartikels ein oder Service ein.
5. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der eingekauft wird.

    > [!NOTE]  
    > Für Posten vom Typ **Dienstleistung** und für Zeilen vom Typ **Ressource** ist die Menge eine Zeiteinheit, z.B. Stunden, wie im Feld **Mengeneinheit-Code** in der Zeile angegeben.

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **EK-Preis** multipliziert ist mit dem Wert im Feld **Menge** anzuzeigen.

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Kreditorenkarte ausgewählt haben.

    Die Summenfelder unter den Positionen werden automatisch aktualisiert, wenn Sie Positionen erstellen oder ändern, um die Beträge anzuzeigen, die auf die Sachkonten gebucht werden.

    > [!NOTE]
    > In seltenen Fällen können die gebuchten Beträge von dem abweichen, was in den Summenfeldern angezeigt wird. Dies ist in der Regel auf Rundungsrechnungen in Bezug auf Mehrwertsteuer oder Verkaufssteuer zurückzuführen.
    >
    > Um die tatsächlich gebuchten Beträge zu überprüfen, können Sie die **Statistiken**-Seite verwenden, die die Rundungsberechnungen berücksichtigt. Auch wenn Sie die Aktion **Freigabe** auswählen, werden die Summenfelder aktualisiert, sodass sie die Rundungsberechnungen enthalten.

6. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    > [!NOTE]  
    > Wenn Sie Rechnungsrabatte für den Kreditor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Kreditor Rechnungsrabatt** in Prozent eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt** eingefügt.
7. Falls Sie die eingekauften Artikel oder Dienstleistungen erhalten, wählen Sie aus **Buchen**.

Der Kauf wird nun im Bestand, in den Ressourcen-Sachkonten und in den Finanzdokument widergespiegelt, und die Kreditorenzahlung wird aktiviert. Die Einkaufsrechnung wird in der Liste der gebuchten Einkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Einkaufsrechnungen ersetzt.  

## <a name="posted-invoices"></a>Gebuchte Rechnungen

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Sie können eine gebuchte Einkaufsrechnung einfach korrigieren oder stornieren, bevor Sie den Kreditor bezahlen. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn Sie den Kauf früh im Bestellvorgang ändern möchten. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Einkaufsrechnungen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Wenn Sie bereits für Artikel oder Dienstleistungen auf der gebuchten Einkaufsrechnung bezahlt haben, dann müssen Sie eine Einkaufsgutschrift erstellen, um den Einkauf rückgängig zu machen. Weitere Informationen finden Sie unter [Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

[Die Liste **Gebuchte Einkaufsrechnungen** öffnen](https://businesscentral.dynamics.com/?page=146) in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Externe Belegnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Ressourcen einrichten](projects-how-setup-resources.md)  
[Einkäufe buchen](ui-post-purchases.md)  
[Angebotsanforderungen](purchasing-how-request-quotes.md)  
[Einkauf von Artikeln für einen Verkauf](purchasing-how-purchase-products-sale.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Direktlieferungen vorbereiten](sales-how-drop-shipment.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]