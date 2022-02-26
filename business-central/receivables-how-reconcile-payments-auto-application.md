---
title: Abstimmen von Zahlungen mithilfe der automatischen Anwendung
description: Beschreibt, wie die automatische Anwendungsfunktion verwendet wird, um Zahlungseingänge Zahlungen oder in ihre entsprechenden offenen Posten anwenden und Zahlungen auszugleichen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a39798d56aa18dffa929d719cecd68a522bde00d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441985"
---
# <a name="reconcile-payments-using-automatic-application"></a>Abstimmen von Zahlungen mithilfe der automatischen Anwendung

Die Seite **Zahlungsabstimmungsbuch.-Blatt** gibt Zahlungen an, entweder eingehend von Debitoren oder ausgehend an Kreditoren, die als Transaktionen in Ihrem Bankkonto oder bei einem Zahlungsverkehr erfasst wurden und die auf ihre entsprechenden unbezahlten Rechnungen und Gutschriften oder andere offene Posten angewendet werden können. Die Zeilen im Journal können durch Importieren eines Kontoauszugs als Bankfeed oder -datei oder durch manuelle Eingabe von Transaktionen, die Sie mit Ihrem Zahlungsdienst tätigen, ausgefüllt werden.

> [!NOTE]
> Die Seite bietet automatisch entsprechende Funktionen an, die für Zahlungen in ihre entsprechenden offenen Postens darstellte eine Zuordnung der Daten in einer Bankkontoauszugszeile (Buch.-Blattzeile) mit Daten auf einer oder mehreren offenen Posten ausgeglichen werden soll. Beachten Sie, dass die vorgeschlagenen automatischen Anwendungen überschrieben können, und Sie können wählen, dass die Anwendung nicht automatisch verwendet wird. Weitere Informationen finden Sie unter Schritt 7.

Ein Zahlungsabstimmungsbuch.-Blatt wird mit einem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] verknüpft, das das elektronischen Bankkonto widerspiegelt, in der die Zahlungsbuchungen erfasst werden. Alle offnen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen.

Sie können Bankgeschäfte als CSV-Bankdateien oder in einem anderen von Ihrer Bank bereitgestellten Format importieren. Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie einen dedizierten Bankintegrationsdienst einrichten und aktivieren und dann Ihr Bankkonto mit den entsprechenden Onlinebankkonten verbinden. Das Zahlungsabstimmungsbuch.-Blatt erkennt dann automatisch Bankfeeds, wenn Sie die Aktion **Import-Bankbuchungen** auswählen. Darüber hinaus können Sie in einem Bankkonto beliebig viele automatisch festgelegt Importe für neue Bankkontoauszugsfeeds jede Stunde festlegen. Transaktionen für Zahlungen, die bereits als ausgeführt und/oder abgestimmt im Fenster Zahlungsabstimmungsbuch.-Blatt gebucht wurden, werden nicht importiert. Sie können hierfür den Dienst Envestnet Yodlee Bank Feeds verwenden, der in einigen Ländern in der Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] vorinstalliert ist. Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md). Alternativ können Sie sich an Ihren Microsoft-Partner wenden, um Hilfe bei der Erfüllung Ihrer Geschäfts- oder Länderanforderungen zu erhalten.

Im Fenster **Text zu Konto zuordnen**, können Sie schnell Zuordnungen zwischen Text in Zahlungen und bestimmten Soll-, Haben- und Gegenkonten eingeben, sodass solche Zahlungen auf die angegebenen Konten gebucht werden, wenn Sie Zahlungen im Zahlungsabstimmungsbuch.-Blatt buchen. Dies ist beispielsweise nützlich für wiederkehrende Zahlungseingänge oder Ausgaben wie häufig auftretende Einkäufe von Autobrennstoff, Bankgebühren und Zinsen, die regelmäßig im Bankkontoauszug auftreten und kein zugehöriges Geschäftsdokument benötigen. (Siehe dazu auch Schritt 10 unten.) Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Journalzeilen haben möglicherweise keine vorgeschlagene Anwendung. Dies kann verschiedene Gründe haben, z. B. ein fehlendes Dokument oder eine Überzahlung durch einen Kunden, sodass nach dem Anwenden der Zahlung auf eine andere Journalzeile ein Überschussbetrag besteht. In solchen Fällen können Sie die Aktion **Differenz auf Konto übertragen** zum Erstellen und Buchen des fehlenden Hauptbucheintrags, z. B. für eine Rückerstattung, auf die die Zahlung angewendet werden soll. (Siehe dazu auch Schritt 11 unten) Weitere Informationen finden Sie unter [Zahlungen abstimmen, die nicht ausgeglichen werden können](receivables-how-reconcile-payments-cannot-apply-auto.md).

Sie verwenden die Funktion **Automatisch anwenden** entweder automatisch, wenn Sie die Bankdatei importieren mit Zahlungstransaktionen, oder wenn Sie sie aktivieren, um Zahlungen auf ihre entsprechenden offenen Posten im Rahmen eines Datenabgleichs in einer Buch.-Blattzeile mit Daten für einen oder mehrere offene Posten anzuwenden. Diese Automatisierung basiert auf Regeln, die Sie auf der Seite **Zahlungsantragsregeln** definieren, auf der Sie auch definieren, ob ein Anwendungsarbeitsblatt überprüft werden muss. Weitere Informationen finden Sie unter [Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md).

In Buch.-Blattzeilen, bei denen eine Zahlung automatisch auf einen oder mehrere offene Posten angewendet wurde, hat das Feld **Übereinstimmungsgenauigkeit** einen Wert zwischen **Niedrig**, **Mittel** und **Hoch**, um die Qualität des Datenabgleichens anzugeben, auf der die vorgeschlagenen Zahlungsanwendung basiert.

Einige Zahlungsanwendungen erfordern Ihre Überprüfung gemäß der verwendeten Übereinstimmungsregel, z. B. Zeilen mit einer Übereinstimmungsgenauigkeit **Niedrig**. Andere Zeilen erfordern Ihre Überprüfung und manuelle Änderung, da in der Zeile ein Wert **Unterschied** enthalten ist. Um einen oder mehrere Zahlungsanträge zu überprüfen, wählen Sie das Feld **Zu überprüfende Zeilen** oder **Zeilen mit Unterschied** unten. Die Seite **Zahlungsausgleichsüberprüfung** wird geöffnet und zeigt alle relevanten Informationen über den Kunden oder Lieferanten, auf den die Zahlung angewendet wird, die übereinstimmenden Details und Aktionen zur Verarbeitung der Zeile, z. B. die Aktion **Anwendung annehmen**. (Siehe Schritte 7 und 8 unten.)

Für jede Buch.-Blattzeile, die ein Zahlung auf der Seite **Zahlungsabstimmungsbuch.-Blatt** darstellt, können Sie die Seite **Zahlungsanwendung** öffnen, um alle offenen Kandidatenposten für die Zahlung anzuzeigen und detaillierte Informationen für jeden Posten zum Datenabgleich anzuzeigen, auf denen eine Zahlungsanwendung basiert. Hier können Sie manuell Zahlungen ausgleichen, oder Zahlungen erneut ausgleichen, die automatisch auf einen falschen offenen Posten angewendet wurden,. (Siehe Schritt 10 unten). Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Sie können den Banktransaktionsimport automatisch starten, wenn Sie die Seite **Zahlungsabstimmungsbuch.-Blatt** für ein bestehendes Buch.-Blatt. öffnen. Nachfolgend wird beschrieben, wie Banktransaktionen auf die Seite **Zahlungsabstimmungsbuch-Blatt** importiert werden, nachdem Sie ein neues Buch.-Blatt erstellt haben.

## <a name="to-reconcile-payments-using-automatic-application"></a>Vorgehensweise zum Abstimmen von Zahlungen mithilfe der automatischen Anwendung
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zahlungsausgangs Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Um in einem neuen Zahlungsabstimmungsbuch.-Blatt zu arbeiten, wählen Sie die Aktion **Neues Buch.-Blatt** aus.
3. Wählen Sie auf der Seite **Bankkontenübersicht** das Bankkonto aus, mit dem Sie eine Verknüpfung erstellen möchten, und klicken Sie anschließend auf **OK**.
   Die Seite **Zahlungsabstimmungsbuch.-Blatt** wird für das ausgewählte Bankkonto vorbereitet geöffnet.
4. Wählen Sie die Aktion **Import-Bankbuchungen** aus.
   Wenn das Bankkonto für das gewählte Buch.-Blatt nicht zum Importieren von Banktransaktionen eingerichtet ist, dann öffnet sich ein Dialogfeld, um Ihnen dabei zu helfen, die entsprechenden Felder einzutragen.
5. Auf der Seite **Datei für den Import auswählen** wählen Sie die Datei aus, die die Banktransaktionen für Zahlungen enthält, die abgestimmt werden sollen, und wählen Sie dann die Schaltfläche **Öffnen**.  
6. Wenn der Envestnet Yodlee Bank Feeds -Service ausgeführt wird, öffnet sich die Seite **Bankkontoauszugs-Filter** automatisch. Geben Sie ein Datumsintervall an, sodass die Bankkontoauszüge importiert werden können.

    Die Seite **Zahlungsabstimmungsbuch-Blatt** enthält Zeilen für die Zahlungen, die Banktransaktionen in der importierten Datei darstellen.

     In Zeilen, bei denen eine Zahlung automatisch auf den zugehörigen offenen Posten angewendet wurde, hat das Feld **Übereinstimmungsgenauigkeit** einen Wert zwischen **Niedrig** und **Hoch**, um die Qualität des Datenabgleichens anzugeben, auf der die vorgeschlagenen Zahlungsanwendung basiert. Darüber hinaus werden die Felder **Kontoname**, **Kontotyp** und **Kontonummer** über den Debitor oder Kreditor ausgefüllt, auf die die Zahlung angewendet wird.

    Die automatischen Anwendungen, die Übereinstimmungsqualitäten und die Frage, ob Linien überprüft werden müssen, werden durch Regeln definiert, die Sie bearbeiten können, um die Ergebnisse anzupassen. Weitere Informationen finden Sie unter [Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md).

7. Zum Überprüfen, Akzeptieren/Entfernen oder manuellen Ändern mehrerer Zahlungsanwendungen, die einen Wert im Feld **Unterschied** haben, wählen Sie die Aktion **Zeilen mit Unterschied** am unteren Rand.

    Die Seite **Überprüfung des Zahlungsantrags** wird geöffnet und zeigt die erste zu überprüfende Anwendung. Die nächste zu überprüfende Anwendung wird auf der Seite angezeigt, während Sie die vorhergehende bearbeiten. Alle relevanten Informationen über den Kunden oder Lieferanten, auf den die Zahlung angewendet wird, die übereinstimmenden Details und Aktionen zur Verarbeitung der Zeile, z. B. die Aktionen **Anwendung annehmen** und **Manuell anwenden**.

8. Um mehrere Zahlungsanwendungen zu überprüfen, zu akzeptieren/zu entfernen oder manuell zu ändern, die gemäß der Zahlungsanwendungsregel überprüft werden sollen, wählen Sie die Aktion **Zu überprüfende Zeilen** am unteren Rand. Die gleiche Erfahrung wie für Schritt 8 beschrieben wird vorgestellt

9. Um eine automatische Anwendung zu ändern, wählen Sie eine Buch.-Blattzeile, und wählen Sie dann **Manuell anwenden** oder Zahlung manuell anwenden auf der Seite **Zahlungsanwendung**. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-review-apply-payments-auto-application.md).

10. Wählen Sie eine nicht ausgeglichene Buch.-Blattzeile für einen wiederkehrende Zahlungseingang oder Ausgabe aus, wie einen Autobenzineinkauf, und wählen Sie dann auf der Registerkarte Start in der Gruppe Anwendungen **Text-zu-Kontenzuordnung** aus. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

    Wenn Sie Ihre manuelle Zuordnung von Zahlungstext zu Konten abgeschlossen haben, wählen Sie die Aktion **Manuell anwenden** aus.

    Wenn eine Text-zu-Konto-Karte eingerichtet wird, enthält die resultierende automatische Zahlungsanwendung **Hoch – Text-zu-Konto-Zuordnung** in dem Feld **Übereinstimmungsgenauigkeit**.

11. Für eine Journalzeile, für die keine Anwendung vorgeschlagen wurde, da kein Ledger-Eintrag vorhanden ist, auf den sie angewendet werden kann, wählen Sie die Aktion **Differenz auf Konto übertragen** zum Erstellen und Buchen des fehlenden Hauptbucheintrags, auf den die Zahlung angewendet werden soll. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-cannot-apply-auto.md).

10. Wenn keine Zeilen mehr überprüft werden müssen und das Feld **Unterschied** in allen Zeilen leer ist, wählen Sie die Aktion **Buchen**, und wählen Sie dann eine der folgenden Optionen:

    - **Buchen von Zahlungen und Abstimmen von Bankkonten** - Um die Zahlung zu buchen und den entsprechenden Bankposten als ausgeglichen zu schließen.
    - **Nur Zahlungen buchen** -, Um nur Zahlungen als übernommen zu buchen aber den entsprechenden Bankposten offen lassen. Erforderlich, dass Sie das Bankkonto abstimmen, zum Beispiel: Weitere Informationen finden Sie unter [Abstimmen von Bankkonten separat](bank-how-reconcile-bank-accounts-separately.md).
    - Um das Ergebnis der Buchung erneut durchzuführen bevor Sie buchen, wählen Sie die **Bericht testen** Aktion. Der Bericht **Bankkontoauszug** wird geöffnet und zeigt die gleichen Felder wie der Kopf der Seite **Bankkonto bstimmen** an.

Wenn Sie das Zahlungsabstimmungsbuch.-Blatt buchen, werden die saldierten offenen Posten geschlossen und die zugehörigen Debitoren-, Kreditoren- oder Sachkonten werden aktualisiert. Für Zahlungen in Buch.-Blattzeilen basierend auf der Text-zu-Kontenzuordnung werden die angegebenen Debitoren-, Kreditoren- und Sachkonten aktualisiert. Für alle Buch.-Blattzeilen werden Bankposten erstellt. Alle offenen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen.

Sie können den Wert im Feld **Saldo auf Bankkonto nach dem Buchen** zusammen mit dem Wert im Feld **Auszug Schluss-Saldo** verwenden, um zu kontrollieren, wenn das Bankkonto basierend auf den gebuchten Zahlungen abgestimmt wird.

> [!NOTE]  
>   Wenn Sie nicht das Bankkonto aus der Seite **Zahlungs-Abstimmungs-Buch.Blatt** abstimmen, müssen Sie das Fenster **Bankkonto-Abstimmung** verwenden. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]