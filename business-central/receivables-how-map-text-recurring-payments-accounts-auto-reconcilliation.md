---
title: Text-zu-Konton-Zuordnung für Wiederk Zahlungen einrichten| Microsoft Docs
description: Verknüpfen Sie Text für Zahlungen mit bestimmten Konten, so dass Zahlungen auf die Konten gebucht werden, wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 01ca3f718ecf469d01d743d1277ce1abc0d6dcde
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193731"
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Zuordnen von Text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung
Im Fenster **Zuordnung Text zu Konto**, das Sie auf der Seite **Zahlungsabstimmungsbuch.-Blatt** öffnen, können Sie schnell Zuordnungen zwischen Text in Zahlungen und bestimmten Soll-, Haben- und Gegenkonten eingeben, sodass solche Zahlungen auf die angegebenen Konten gebucht werden, wenn Sie Zahlungen im Zahlungsabstimmungsbuch.-Blatt buchen.

Ähnliche Funktionen sind vorhanden, um Mehrbeträge auf Zahlungsabstimmungsbuch.-Blattzeilen fallweise abzustimmen. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Zuordnung](receivables-how-reconcile-payments-cannot-apply-auto.md).

Die Zahlungen, die anhand der Text-zu-Kontenzuordnung gebucht wurden, werden nicht auf offene Einträge angewendet, sondern sie werden nur für die angegebenen Konten sowie das Erstellen von Bankposten gebucht. Entsprechend eignet sich die Text-zu-Konto-Zuordnung für wiederkehrende Zahlungseingänge oder Ausgaben wie häufig auftretende Einkäufe von Autobrennstoff, Bankgebühren und Zinsen, die regelmäßig im Bankkontoauszug auftreten und kein zugehöriges Geschäftsdokument benötigen. Weitere Informationen finden Sie im Abschnitt “Beispiel - Text-zu-Konten-Zuordnung für Brennstoff-Ausgaben” in diesem Thema.

> [!NOTE]  
>   Zahlungen auf Abstimmungsbuch.-Blattzeilen werden nur dann für das Buchen entsprechend der Text-zu-Kontenzuordnung festgelegt, wenn die automatische Anwendungsfunktion lediglich ein Abgleichungsvertrauen zwischen **Niedrig**und **Normal** zurückgibt. Wenn die automatische Anwendungsfunktion eine Übereinstimmungsgenauigkeit von "Hoch" liefert, wird die Zahlung eines oder mehrerer offener Posten automatisch angewendet, und die Zahlung wird nicht auf die Konten gebucht, die auf der Seite **Zuordnung Text zu Konto** angegeben wurde. Anders ausgedrückt, ein Abgleichungsvertrauen **Hoch** überschreibt eine Text-zu-Konto-Zuordnung.

In einer Zahlungsabstimmungsbuch.-Blattzeile, in der die Zahlung entsprechend der Text-zu-Kontenzuordnung zur Buchung festgelegt wurde, enthält das Feld **Übereinstimmungsgenauigkeit** **Hoch - Text-Kontozuordnung** und den **Kontenart** und die **Kontennummer**.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Zuordnen von text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Zahlungsabstimmungsbuch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie ein Zahlungsabstimmungsbuch.-Blatt. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).
3. Wählen Sie die Aktion **Text zu Konto zuordnen**. Die Seite **Text zu Konto zuordnen** öffnet sich.
4. Geben Sie im Feld **Text zuordnen** einen beliebigen Text ein, der in Zahlungen auftritt, die Sie an die angegebenen Konten ohne Anwendung auf einen offenen Posten buchen möchten. Sie können bis zu 50 Zeichen eingeben.

    > [!NOTE]  
    >   Wenn keine anderen Zahlungsbelege mit dem jeweiligen Zuordnungstext vorhanden sind, dann erfolgt die Text-Konto-Zuordnung auch, wenn nur ein Teil des Texts auf den Zahlungsbeleg als Zuordnungstext vorhanden ist.
5. In dem Feld **Kreditorennr.** geben Sie den Kreditor ein, bei dem die Zahlungen gebucht werden.
6. Geben Sie im Feld **Herkunftsart Saldo** an, ob die Zahlung auf ein Sachkonto oder auf ein Debitoren- oder Kreditorenkonto gebucht wird.
7. Im Feld **Saldoquellen-Nr.** definieren Sie das Konto, auf das die Zahlung gebucht wird, abhängig von Ihrer Wahl im Feld **Herkunftsart Saldo**.

    > [!NOTE]
    > Verwenden Sie nicht die Felder **Sollkontonr.** und **Habenkontonr.** in Verbindung mit Zahlungsabstimmung. Sie werden nur für eingehende Belege verwendet. Weitere Informationen finden Sie unter [Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md).

8. Wiederholen Sie die Schritte 3 bis 7 für alle Texte auf Zahlungen, die Sie zuordnen möchten, um die entsprechenden Posten direkt, ohne Anwendung, zu buchen.

Beim nächsten Mal, wenn Sie eine Bankkontoauszugsdatei importieren oder die Funktion **Automatisch anwenden** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** wählen, enthalten die Buch.-Blattzeilen für die Zahlungen, die den angegebenen Zuordnungstext enthalten, die zugehörigen Konten im Feld **Kontoart** und **Kontonummer**. Das Feld **Übereinstimmungsgenauigkeit** enthält **Hoch - Text zu Konto Zuordnung**. Dies ist unter der Bedingung der Fall, dass die automatische Anwendungsfunktion nur ein Abgleichungsvertrauen von **Niedrig** oder **Normal** zur Verfügung stellen kann.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Beispiel: Text-zu-Konto-Zuordnung für Brennstoff-Ausgaben
Um die Brennstoffausgaben an Shell-Tankstellen immer in das Sachkonto für Benzin (Konto 8510) zu buchen, füllen Sie eine Zeile auf der Seite **Text-zu-Konto-Zuordnung** wie folgt aus.

| Abbildungstext | Sollkontonr. | Habenkontonr. | Herkunftsart Saldo | Herkunftsnr. Saldo |
| --- | --- | --- | --- | --- |
| Shell |LEER |8510 |Sachkonto |LEER |

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] über Erweiterungen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
