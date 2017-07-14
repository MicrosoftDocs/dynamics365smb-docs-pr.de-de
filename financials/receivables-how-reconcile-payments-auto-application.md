---
title: 'So geht''s: Abstimmen von Zahlungen mithilfe der automatischen Anwendung | Microsoft Docs'
description: 'Vorgehensweise: Abstimmen von Zahlungen mithilfe der automatischen Anwendung'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 423b141969c131688542cc10bb5361085f247a68
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Abstimmen von Zahlungen mithilfe der automatischen Anwendung
<a id="how-to-reconcile-payments-using-automatic-application" class="xliff"></a>
Das Fenster **Zahlungsabstimmungsbuch.-Blatt** gibt Zahlungen an, entweder eingehend von Debitoren oder ausgehend an Kreditoren, die als Transaktionen in Ihrem Bankkonto erfasst wurden und die auf ihre entsprechenden unbezahlten Rechnungen und Gutschriften oder andere offene Posten angewendet werden können. Die Zeilen im Buch.-Blatt werden ausgefüllt, indem ein Bankkontoauszug als Bankfeed oder -Datei importiert wird.

Ein Zahlungsabstimmungsbuch.-Blatt wird mit einem Bankkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] verknüpft, das das elektronischen Bankkonto widerspiegelt, in der die Zahlungsbuchungen erfasst werden. Alle offnen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen.

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Bankfeeddienst Envestnet Yodlee einrichten und aktivieren und dann Ihr Bankkonto mit den entsprechenden Onlinebankkonten verbinden. Das Zahlungsabstimmungsbuch.-Blatt erkennt dann automatisch Bankfeeds, wenn Sie die Aktion **Import-Bankbuchungen** auswählen. Darüber hinaus können Sie in einem Bankkonto beliebig viele automatisch festgelegt Importe für neue Bankkontoauszugsfeeds jede Stunde festlegen. Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster Zahlungsabstimmungsbuch.-Blatt gebucht wurden, werden nicht importiert. Für weitere Informationen, siehe [So gehts: Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md).

Im Fenster **Text zu Konto zuordnen**, können Sie schnell Zuordnungen zwischen Text in Zahlungen und bestimmten Soll-, Haben- und Gegenkonten eingeben, sodass solche Zahlungen auf die angegebenen Konten gebucht werden, wenn Sie Zahlungen im Zahlungsabstimmungsbuch.-Blatt buchen. Siehe dazu auch Schritt 8. Weitere Informationen finden Sie unter [Vorgehensweise: Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

Ähnliche Funktionen sind vorhanden, um Mehrbeträge auf Zahlungsabstimmungsbuch.-Blattzeilen fallweise abzustimmen. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-cannot-apply-auto.md).

Sie verwenden die Funktion **Automatisch anwenden** entweder automatisch, wenn Sie die Bankdatei importieren mit Zahlungstransaktionen, oder wenn Sie sie aktivieren, um Zahlungen auf ihre entsprechenden offenen Posten im Rahmen eines Datenabgleichs in einer Buch.-Blattzeile mit Daten für einen oder mehrere offene Posten anzuwenden.

In Buch.-Blattzeilen, bei denen eine Zahlung automatisch auf einen oder mehrere offene Posten angewendet wurde, hat das Feld **Passende Werte** einen Wert zwischen Niedrig und Hoch, um die Qualität des Datenabgleichens anzugeben, auf der die vorgeschlagenen Zahlungsanwendung basiert. Darüber hinaus **Kontoart** und **Kontonummer**. Felder werden mit Informationen über den Debitor oder Kreditor, für den die Zahlung gebucht wurde, ergänzt. Wenn Sie eine Text-zu-Konto-Zuordnung eingerichtet haben, kann die automatische Anwendung einen Abgleichungsvertrauenswert von **Hoch - Text-zu-Konto-Zuordnung** ergeben.

Für jede Buch.-Blattzeile, die ein Zahlung im Fenster **Zahlungsabstimmungsbuch.-Blatt** darstellt, können Sie das Fenster **Zahlungsanwendung** öffnen, um alle offenen Kandidatenposten für die Zahlung anzuzeigen und detaillierte Informationen für jeden Posten zum Datenabgleich anzuzeigen, auf denen eine Zahlungsanwendung basiert. Hier können Sie manuell Zahlungen ausgleichen, oder Zahlungen erneut ausgleichen, die automatisch auf einen falschen offenen Posten angewendet wurden,. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-review-apply-payments-auto-application.md).

**Hinweis**: Sie können den Banktransaktionsimport automatisch starten, wenn Sie dafür ein vorhandenes **Zahlungsabstimmungsbuch.-Blatt** im Fenster **Zahlungsabstimmungsbuch.-Blatt** öffnen. Nachfolgend wird beschrieben, wie Banktransaktionen in das Fenster **Zahlungsabstimmungsbuch-Blatt** importiert werden, nachdem Sie ein neues Buch.-Blatt erstellt haben.

## Vorgehensweise zum Abstimmen von Zahlungen mithilfe der automatischen Anwendung
<a id="to-reconcile-payments-using-automatic-application" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Zahlungsabstimmungsbuch.-Blatt** ein und wählen Sie dann den entsprechenden Link aus.
2. Um in einem neuen Zahlungsabstimmungsbuch.-Blatt zu arbeiten, wählen Sie die Aktion **Neues Buch.-Blatt** aus.
3. Wählen Sie im Fenster **Bankkontenübersicht** das Bankkonto aus, mit dem Sie eine Verknüpfung erstellen möchten, und klicken Sie anschließend auf **OK**.
   Das Fenster **Zahlungsabstimmungsbuch.-Blatt** wird für das ausgewählte Bankkonto vorbereitet geöffnet.
4. Wählen Sie die Aktion **Import-Bankbuchungen** aus.
   Wenn das Bankkonto für das gewählte Buch.-Blatt nicht zum Importieren von Banktransaktionen eingerichtet ist, dann öffnet sich ein Dialogfeld, um Ihnen dabei zu helfen, die entsprechenden Felder einzutragen.
5. Im Fenster **Datei für den Import auswählen** wählen Sie die Datei aus, die die Banktransaktionen für Zahlungen enthält, die abgestimmt werden sollen, und wählen Sie dann die Schaltfläche **Öffnen**.  
6. Wenn der Bankkontoauszugs-Service ausgeführt wird, öffnet sich das Fenster **Bankkontoauszugs-Filter** automatisch. Geben Sie ein Datumsintervall an, sodass die Bankkontoauszüge importiert werden können.

    Das Fenster **Zahlungsabstimmungsbuch-Blatt** enthält Zeilen für die Zahlungen, die Banktransaktionen in der importierten Datei darstellen.

    In Zeilen, bei denen eine Zahlung automatisch auf den zugehörigen offenen Posten angewendet wurde, hat das Feld **Übereinstimmungsgenauigkeit** einen Wert zwischen **Niedrig** und **Hoch**, um die Qualität des Datenabgleichens anzugeben, auf der die vorgeschlagenen Zahlungsanwendung basiert. Darüber hinaus **Kontoart** und **Kontonummer**. Felder werden mit Informationen über den Debitor oder Kreditor, für den die Zahlung gebucht wurde, ergänzt.
7. Wählen Sie eine Buch.-Blattzeile, und wählen Sie dann **Manuell anwenden** oder Zahlung manuell anwenden im Fenster **Zahlungsanwendung**. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-review-apply-payments-auto-application.md).

    Wenn Sie den manuellen Ausgleich abgeschlossen haben, enthält das Feld **Übereinstimmungsgenauigkeit** in der Buchzeile, die Sie manuell verarbeitet haben **Akzeptiert**.
8. Wählen Sie eine nicht ausgeglichene Buch.-Blattzeile für einen wiederkehrende Zahlungseingang oder Ausgabe aus, wie einen Autobenzineinkauf, und wählen Sie dann auf der Registerkarte Start in der Gruppe Anwendungen **Text-zu-Kontenzuordnung** aus. Weitere Informationen finden Sie unter [Vorgehensweise: Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Wenn Sie Ihre manuelle Zuordnung von Zahlungstext zu Konten abgeschlossen haben, wählen Sie die Aktion **Manuell anwenden** aus.
10. Wenn Sie sicher sind, dass alle Zahlungen der Buch.-Blattzeilen korrekt angewendet oder zur direkten Buchung festgelegt werden, wählen Sie die Aktion **Buchen** aus.

Wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen, werden die saldierten offenen Posten geschlossen und die zugehörigen Debitoren-, Kreditoren- oder Sachkonten werden aktualisiert. Für Zahlungen in Buch.-Blattzeilen basierend auf der Text-zu-Kontenzuordnung werden die angegebenen Debitoren-, Kreditoren- und Sachkonten aktualisiert. Für alle Buch.-Blattzeilen werden Bankposten erstellt. Alle offenen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen.

Sie können den Wert im Feld **Saldo auf Bankkonto nach dem Buchen** zusammen mit dem Wert im Feld **Auszug Schluss-Saldo** verwenden, um zu kontrollieren, wenn das Bankkonto basierend auf den gebuchten Zahlungen abgestimmt wird.

**Hinweis**: Wenn Sie nicht das Bankkonto aus dem Fenster **Zahlungs-Abstimmungs-Buch.Blatt** abstimmen, müssen Sie das Fenster **Bankkonto-Abstimmung** verwenden. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

