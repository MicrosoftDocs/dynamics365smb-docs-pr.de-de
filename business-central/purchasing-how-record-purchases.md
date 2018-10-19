---
title: "Erstellen einer Einkaufsrechnung und erfassen von Einkäufe | Microsoft Docs"
description: Beschreibt, wie man Artikel oder Dienstleistungen durch das Erstellen und Buchen von Einkaufsrechnungen oder Bestellungen kauft.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a96947c07cf86159f767ffcdf85564ee2b4366d8
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="record-purchases"></a>Erfassen eines Einkaufs
Sie erstellen eine Einkaufsrechnung oder Einkaufsbestellung, um die Kosten der Einkäufe zu erfassen und Kreditoren zu verfolgen. Wenn Sie einen Bestand steuern müssen, werden Einkaufsrechnungen und Einkaufsbestellungen auch verwendet, um Lagerbestände dynamisch zu aktualisieren, sodass Sie Ihre Lagerbestandskosten minimieren und besseren Debitorenservice bereitstellen können. Die Einkaufskosten, einschließlich Servicekosten und Bestandswerte, die aus der Buchung von Einkaufsrechnungen resultieren, tragen zu den Gewinnzahlen und anderen finanziellen Kennziffern in Ihrem Rollencenter bei.

> [!NOTE]  
>   Sie müssen Einkaufsbestellungen verwenden, wenn es für den Einkaufsprozess erforderlich ist, Teillieferungen einer Bestellmenge zu erfassen, weil beispielsweise die vollständige Menge beim Kreditor nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Einkaufsbestellungen verwenden. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Einkaufsbestellungen genau wie bei Einkaufsrechnungen. Das folgende Verfahren basiert auf einer Einkaufsrechnung. Die Schritte sind für eine Einkaufsbestellung ähnlich.

Wenn Sie den Lagerartikel erhalten haben oder die erworbene Dienstleistung abgeschlossen ist, buchen Sie die Einkaufsrechnung oder-bestellung, um Lagerbestands- und Finanzdatensätze zu aktualisieren und Zahlungen für den Kreditor entsprechend der Zahlungsbedingungen zu aktivieren. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).

> [!CAUTION]  
>   Buchen Sie keine Einkaufsrechnung, bevor Sie die Produkte erhalten und die abschließenden Einkaufskosten kennen, einschließlich aller zusätzlichen Gebühren. Andernfalls werden Ihr Lagerwert und DB-Zahlen möglicherweise falsch sein.

Sie können eine gebuchte Einkaufsrechnung einfach korrigieren oder stornieren, bevor Sie den Kreditor bezahlen. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn Sie den Kauf früh im Bestellvorgang ändern möchten. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Einkaufsrechnungen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Wenn Sie bereits für Artikel auf der gebuchten Einkaufsrechnung bezahlt haben, müssen Sie eine Einkaufsgutschrift erstellen, um den Einkauf zu stornieren. Weitere Informationen finden Sie unter [Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

Gibt an, ob die Artikelkarte einen **Bestand**, **Service** und **Nicht-Bestand** ist, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md). Der Kaufsrechnungsprozess ist derselbe für alle drei Artikeltypen.

Sie können die oberen Infoboxen des Einkaufsangebotes auf zwei Arten ausfüllen, abhängig davon, ob der Kreditor bereits registriert ist.

## <a name="to-create-a-purchase-invoice"></a>Erstellen Sie eine neue Einkaufsrechnung.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufrechnung** ein, und wählen dann den zugehörigen Link aus.  
2. Geben Sie im Feld **Kreditor** den Namen eines vorhandenen Kreditors ein.

    Andere Felder im Fenster **Einkaufsrechnung** werden nun mit den Standardinformationen vom ausgewählten Kreditor ausgefüllt. Wenn der Kreditor noch nicht erfasst wurde, dann führen Sie die folgenden Schritte durch:
3. Geben Sie im Feld **Kreditor** den Namen eines neuen Kreditors ein.
4. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um den neuen Kreditor zu bestätigen.
5. Im Fenster **Vorlage für neuen Kreditor wählen** wählen Sie eine Vorlage, auf der die neue Kreditorenkarte basieren soll, und dann wählen Sie die Schaltfläche **OK**.
6. Eine neue Debitorenkarte wird geöffnet, vorausgefüllt mit Informationen auf der ausgewählten Debitorenvorlage. Das Feld **Name** wird mit dem neuen Namen des Kreditors vorab ausgefüllt, den Sie in der Einkaufsrechnung eingegeben haben.
7. Fahren Sie fort, die restlichen Felder auf der Kreditorenkarte auszufüllen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](purchasing-how-register-new-vendors.md).  
8. Wenn Sie die Kreditorenkarte abgeschlossen haben, wählen Sie die Schaltfläche **OK**, um zum Fenster **Einkaufsrechnung** zurückzugehen.

    Einige Felder im Fenster **Einkaufsrechnung** werden mit den Informationen, die Sie in der neuen Kreditorenkarte festgelegt haben, ausgefüllt.
9. Füllen Sie im Fenster **Einkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Sie können jetzt die Einkaufssrechnungszeilen mit Lagerartikeln oder Services auszufüllen, die Sie von Ihrem Kreditor gekauft haben.

    > [!NOTE]  
    >   Wenn Sie wiederkehrende Einkaufszeilen für den Debitor, wie einen monatlichen Ersatzauftrag, eingerichtet haben, können Sie diese Zeilen auf der Rechnung durch Auswählen der Aktion **Wiederkehrende Einkaufszeilen** abrufen einfügen.
10. Geben Sie im Inforegister **Zeilen** im Feld **Artikelnr.** die Nummer eines Lagerartikels ein oder Service ein.
11. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der eingekauft wird.

    > [!NOTE]  
    >   Für Artikel des Typs **Service** ist die Menge eine Zeiteinheit wie Stunden, wie im Feld **Einheit des Messcodes** der Zeile angegeben.

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **EK-Preis** multipliziert ist mit dem Wert im Feld **Menge** anzuzeigen.

    Der Preis und der Zeilenbetrag auf den Verkaufsrechnungszeilen werden mit oder ohne MwSt. angezeigt je nachdem, was Sie im Feld **Preis inklusive Mehrwertsteuer** auf der Kreditorenkarte ausgewählt haben.
12. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

    > [!NOTE]  
    >   Wenn Sie Rechnungsrabatte für den Kreditor eingerichtet haben, wird der angegebene Prozentwert automatisch in das Feld **Kreditor Rechnungsrabatt** in Prozent eingetragen, sobald die Kriterien erfüllt sein, und der entsprechende Betrag wird im Feld **Rechnungsbetrag mit Rabatt** eingefügt.
13. Falls Sie die eingekauften Artikel oder Dienstleistungen erhalten, wählen Sie aus **Buchen**.

Der Einkauf ist nun im Bestand und in den Finanzdatensätzen reflektiert, und die Lieferantenzahlung ist aktiviert. Die Einkaufsrechnung wird in der Liste der gebuchten Einkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Einkaufsrechnungen ersetzt.

## <a name="see-also"></a>Siehe auch
[Einkauf](purchasing-manage-purchasing.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Angebotsanforderungen](purchasing-how-request-quotes.md)  
[Einkauf von Produkten für einen Verkauf](purchasing-how-purchase-products-sale.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Direktlieferungen vorbereiten](sales-how-drop-shipment.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

