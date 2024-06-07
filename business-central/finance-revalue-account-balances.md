---
title: Finanzbuchhaltungssalden neu bewerten
description: 'Erfahren Sie, wie Sie Finanzbuchhaltungssalden neu bewerten, bevor Sie Ihre Finanzauswertungen erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# <a name="revalue-general-ledger-account-balances"></a>Finanzbuchhaltungssalden neu bewerten

Wenn Sie Sachkonten verwenden, um Bilanzposten in Fremdwährungen zu erfassen, sollten Sie die Kontosalden neu bewerten, bevor Sie Finanzauswertungen erstellen. Währungswechselkurse ändern sich häufig und eine Neubewertung hilft, Ihre Finanzauswertungen genauer zu gestalten.

## <a name="set-up-revaluations"></a>Neubewertungen einrichten

Sie richten jedes Konto, das Sie in Neubewertungen einbeziehen möchten, auf der Seite **Finanzbuchhaltungskontokarte** ein. Sie können auswählen, ob Neubewertungsanpassungen auf Konten für realisierte oder nicht realisierte Gewinne/Verluste gebucht werden sollen. Das Buchen von Gewinnen und Verlusten im Rahmen einer Währungskursanpassung erfolgt gemäß der normalen Buchungsroutine. Sie tun dies beispielsweise für jede Einstellung auf der Seite **Währungen**. Weitere Informationen zu Wechselkursanpassungen finden Sie unter [Währungswechselkurse aktualisieren](finance-how-update-currencies.md).

Um Fehler zu minimieren, können Sie im Feld **Buchung in Ursprungswährung** eine Überprüfung für die Währungen einrichten, die Sie für Buchungen auf einzelnen Finanzbuchhaltungskonten zulassen möchten:

* Alle Währungen (leer)
* Mehrere Währungen
* Gleiche Währung
* Lokale Währung

## <a name="run-a-revaluation"></a>Neubewertung ausführen

Um die Beträge in der Fremdwährung für Finanzbuchhaltungskontosalden in der lokalen Währung neu zu bewerten, verwenden Sie auf der Seite **Kontenplan** die Aktion **Neubewertung der Finanzbuchhaltungswährung**, um einen Stapelverarbeitungsauftrag zu starten. Der Stapelverarbeitungsauftrag erstellt Anpassungsposten in dem von Ihnen ausgewählten Buch.-Blatt. Wenn Sie die Posten buchen, passen Sie den Saldo für das Konto in der lokalen (LW) an. Finanzbuchhaltungkontosalden, die immer in LW angezeigt werden, spiegeln jetzt die Änderungen der Währungen wider, in denen Posten gebucht wurden. Durch diese Neubewertung können Sie mit weniger Aufwand genauere Finanzauswertungen erstellen.

Wenn Sie eine Berichtswährung (AW) verwenden, verfügen die Finanzbuchhaltungskontoneubewertungsposten über einen AW-Betrag. Der Betrag entspricht nur dem LW-Betrag dieser Posten, nicht dem AW-Saldo auf dem Finanzbuchhaltungskonto. Wenn Sie die AW-Kurse anpassen, nachdem Sie die Anpassungen gebucht haben, führen Sie die Wechselkursanpassung noch einmal durch, um alle Hauptbuchposten anzupassen.

> [!IMPORTANT]
> Die Neubewertung von Finanzbuchhaltungskonten erfüllt möglicherweise nicht alle Anforderungen für Transaktions- und Anlagenregistrierungen, die eine Neubewertung erfordern. Zum Beispiel für Finanzinstrumente, Wertpapiere, Leasingobjekte oder wenn Sie sie für bestimmte oder große Transaktions- oder Anlagenvolumina verwenden. Wir empfehlen Ihnen, mit Ihrem Wirtschaftsprüfer zu besprechen, ob Sie das Feature nutzen können und wenn ja, wie Sie es nutzen sollten. Wenn Sie zum Beispiel für ein Konto gemischte Währungen zulassen oder wenn Sie für jede Anlage, den Sie verfolgen möchten, ein separates Konto führen müssen.

> [!NOTE]
> Bei der Neubewertung besteht nicht die Möglichkeit, Posten anzuwenden oder die Anwendung aufzuheben, wie dies bei Debitoren- und Kreditorenposten der Fall ist. Anpassungen erfolgen auf Basis des Saldos pro Währung.

## <a name="revaluate-accounts-vs-customer-and-vendor-exchange-rate-adjustments"></a>Neubewertung von Konten im Vergleich zu Wechselkursanpassungen für Debitoren und Kreditoren

Die Neubewertung vereinfacht die Anpassung der Finanzbuchhaltungskontosalden. Das Feature bewertet den Saldo pro Währung und Finanzbuchhaltungskonto neu, ähnlich wie Sie es bei Anpassungen von Finanzbuchhaltungskonten tun, die mit Bankkonten verknüpft sind. Wenn Sie zur Nachverfolgung mehrerer Anlagen ein Finanzbuchhaltungskonto verwenden, sollten Sie stattdessen die Verwendung eines Kreditoren- oder Debitorenkontos in Erwägung ziehen.

> [!NOTE]
> Die Neubewertung von Finanzbuchhaltungskonten erfüllt möglicherweise nicht alle Anforderungen für Transaktions- und Anlagenregistrierungen, die eine Neubewertung erfordern. Zum Beispiel für Finanzinstrumente, Wertpapiere, Leasingobjekte oder wenn Sie sie für bestimmte oder große Transaktions- oder Anlagenvolumina verwenden. Wir empfehlen Ihnen, mit Ihrem Wirtschaftsprüfer zu besprechen, ob Sie das Feature nutzen können und wenn ja, wie Sie es nutzen sollten. Wenn Sie zum Beispiel für ein Konto gemischte Währungen zulassen oder wenn Sie für jede Anlage, den Sie verfolgen möchten, ein separates Konto führen müssen.

Die folgenden Beispiele veranschaulichen den Unterschied zwischen der Verwendung eines Finanzbuchhaltungskontos und der Verwendung eines Kreditorenkontos zur Verfolgung des Saldos zweier monetärer Anlagen, die eine Fremdwährung verwenden.

**Verwenden Sie ein Finanzbuchhaltungskonto**: Wenn Sie ein Finanzbuchhaltungskonto verwenden, um entweder mehrere Anlagen (z. B. Darlehen oder materielle Anlagen) in derselben Währung oder einzelne Teiltransaktionen für dieselbe Anlage ebenfalls in derselben Währung nachzuverfolgen, wird bei der Finanzbuchhaltungskontoneubewertung ein Posten pro Neubewertung für die Währung erstellt. Das bedeutet, dass Sie die Anpassungen, die sich auf einzelne Anlagen oder einzelne Transaktionen für dieselbe Anlage beziehen, nicht nachverfolgen können.

**Verwenden Sie ein Kreditorenkonto**: Wenn Sie mehrere Anlagen als Kreditoren einrichten und Transaktionen auf diese buchen, entweder in derselben oder in verschiedenen Währungen, erhalten Sie eine Anpassung pro Währung und Kreditor. Wenn Sie alternativ den Umschalter **Buchung pro Posten** im Auftragswarteschlangenposten **Währungswechselkurs anpassen** aktivieren, erhalten Sie für jeden einzelnen Kreditorenposten einen Anpassungsposten.

Dieser Unterschied ist wichtig, wenn Sie beurteilen, ob die Finanzbuchhaltungskontoneubewertung die richtige Funktion für Ihre Berichtsanforderungen ist.

> [!TIP]
> Wir empfehlen Ihnen, Ihre Buchhaltung oder Wirtschaftsprüfung zu fragen, welche Kontoart für Ihr Unternehmen am besten geeignet ist. Möglicherweise gibt es auch eine App für [!INCLUDE [prod_short](includes/prod_short.md)] auf [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central), die genau zu Ihren Geschäftsszenarien passt.

## <a name="see-also"></a>Siehe auch

[Beträge in Sachkonten überprüfen](finance-review-accounts.md)  
[Das Hauptbuch und den Kontenplan verstehen](finance-general-ledger.md)  
