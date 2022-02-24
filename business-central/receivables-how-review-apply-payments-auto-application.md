---
title: Prüfen Sie automatisch übernommene Zahlungen, und wenden Sie Zahlungen manuell erneut an | Microsoft Docs
description: Nachdem Zahlungen automatisch ausgeglichen sind, können Sie alle Posten für eine Zahlung manuell überprüfen und diejenigen erneut ausgleichen, die fehlerhaft ausgeglichen wurden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e37d9ab5aae53ef0e6af6e04a0d94077569e62a3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191955"
---
# <a name="review-or-apply-payments-manually-after-automatic-application"></a>Zahlungen manuell zuordnen oder überprüfen nach der automatischen Zuordnung.
Für jede Buch.-Blattzeile, die ein Zahlung auf der Seite **Zahlungsabstimmungsbuch.-Blatt** darstellt, können Sie die Seite **Zahlungsanwendung** öffnen, um alle offenen Kandidatenposten für die Zahlung anzuzeigen und detaillierte Informationen für jeden Posten zum Datenabgleich anzuzeigen, auf denen eine Zahlungsanwendung basiert. Hier können Sie manuell Zahlungen ausgleichen, oder Zahlungen erneut ausgleichen, die automatisch auf einen falschen offenen Posten angewendet wurden,. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]  
>   Wenn das Bankkonto, für das Sie Zahlungen abstimmen, für die Mandantenwährung eingerichtet ist, zeigt die Seite **Zahlungsanwendung** alle offenen Posten in Mandantenwährung, einschließlich offener Posten für Belege, die ursprünglich in Fremdwährungen fakturiert wurden. Zahlungen, die mit Posten mit umgerechneten Währungen ausgeglichen wurden, werden daher aufgrund von möglicherweise verschiedenen Wechselkursen, die von der Bank bzw. [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden, möglicherweise mit anderen Beträgen als im ursprünglichen Beleg gebucht.

Daher empfiehlt es sich, dass Sie nach Fremdwährungscodes im Feld **Fremdwährungscode** auf der Seite **Zahlungsanwendung** suchen, um zu überprüfen, ob Anwendungen auf umgerechneten Währungen basieren. Um den Originalbelegbetrag in Fremdwährung zu überprüfen und den verwendeten Wechselkurs anzuzeigen, aktivieren Sie das Feld **Auf Eintragsnr. anwenden** und wählen dann das Dropdown-Menü, um die Seite **Debitorenposen** oder **Kreditorenposten** zu öffnen.

Gewinn-und-Verlust-Ausgleich, der aufgrund der Fakturierung des Projekts erforderlich ist, wird nicht automatisch durch [!INCLUDE[d365fin](includes/d365fin_md.md)]verarbeitet.

> [!NOTE]  
>   Sie können Posten mit einem anderen Vorzeichen als dem Vorzeichen der Zahlung nicht ausgleichen. Um beispielsweise sowohl eine Gutschrift mit negativem Vorzeichen als auch die zugehörige Rechnung mit positivem Vorzeichen abzuschließen, müssen Sie zuerst die Gutschrift mit der Rechnung ausgleichen und dann die Zahlung mit der Rechnung mit dem reduzierten Restbetrag ausgleichen.

> [!WARNING]  
>   **Warnung:** Falls Sie Skonti verwenden, und wenn das Fälligkeitsdatum vor dem Zahlungsfälligkeitsdatum ist, wird das Feld Verbleibender Betrag inkl. Rabatt auf der Seite **Zahlungsanwendung** verwendet. Ansonsten wird der Wert aus dem Feld **Verbleibender Betrag** verwendet. Wenn die Zahlung mit einem verbilligten Betrag nach dem Zahlungsfälligkeitsdatum geleistet wurde oder der Totalbetrag bezahlt wurde, aber ein Skonto gewährt wurde, wird der Betrag nicht abgeglichen.

> [!NOTE]  
>   Sie können eine Zahlung nur mit einem Konto ausgleichen. Wenn die Anwendung auf mehrere offene Posten aufteilen möchten, zum Beispiel, um eine Pauschalzahlung auszugleichen, müssen die offenen Posten für das gleiche Konto sein. Weitere Informationen finden Sie in den Schritten 7 und 8 dieses Themas.

## <a name="to-review-or-apply-payments-after-automatic-application"></a>Vorgehensweise: Überprüfen oder Ausgleichen von Zahlungen nach automatischer Anwendung
1. Wählen Sie das Symbol ![Glühbirne , die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Zahltungsabstimmungserfassungen** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie das Zahlungsabstimmungsbuch.-Blatt für ein Bankkonto, für das Sie Zahlungen abstimmen möchten. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).
3. Auf der Seite **Zahlungsabstimmungsbuch.-Blatt** wählen Sie eine Zahlung, die Sie mit einem oder mehreren offenen Posten manuell anwenden oder überprüfen möchten und wählen dann **Manuell Anwenden** aus.
4. Aktivieren Sie das Kontrollkästchen **Angewendet** für die Position mit dem offenen Eintrag aus, auf den die Zahlung angewendet werden soll.
5. Der Zahlungsbetrag, der auch im Feld **Transaktionsbetrag** auf der Seite **Zahlungszuordnung** angezeigt wird, wird im Feld **Zugeordneter Betrag** angezeigt wird, aber Sie können das Feld bearbeiten, wenn Sie zum Beispiel den Betrag auf mehrere offene Posten anwenden möchten.
6. Um einen Teil des bezahlten Betrag in einem anderen offenen Posten für das Konto auszugleichen, beispielsweise um eine Pauschalzahlung auszugleichen, aktivieren Sie das Kontrollkästchen **Zugeordnet** für die Position. Der Ausgleichsbetrag wird automatisch von dem Transaktionsbetrag abgezogen, um die Verteilung in den beiden offenen Posten widerzuspiegeln.
7. Um einen Teil einer Zahlung mit einem oder mehreren offenen Posten zu übernehmen die nicht in der Datenbank vorhanden sind, erstellen Sie eine neue Zeile unter der Zeile für das gleiche Konto. Geben Sie im Feld **Zugeordneter Betrag** den Betrag ein, der der neuen Zeile zugeordnet werden soll und passen Sie dann das Feld **Zugeordneter Betrag** auf der bestehenden Zeile an.
8. Wiederholen Sie Schritt 5, 6 oder 7 für andere offene Posten, auf die Sie einen vollständige Zahlung oder Teilzahlung anwenden möchten.
9. Wenn Sie eine Zahlungs-Anwendung überprüft oder manuell auf einen oder mehrere offene Posten angewendet haben, wählen **Anwendung akzeptieren** aus.

Das Fenster **Zugeordnete Zahlung** wird geschlossen und auf der Seite **Zahlungsabstimmungsbuch.-Blatt** wird der Wert im Feld **Übereinstimmungsgenauigkeit** auf **Zugeordnet** geändert, um Ihnen mitzuteilen, dass Sie die Zahlung überprüft oder manuell angewendet haben.

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
