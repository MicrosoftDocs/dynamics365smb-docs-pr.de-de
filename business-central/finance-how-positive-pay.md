---
title: Positive Pay-Dateien exportieren
description: 'Um sicherzustellen, dass Ihre Bank nur überprüfte Schecks und Beträge freigibt, können Sie ihr eine Positive Pay Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'check, clearing'
ms.search.form: '1231, 1232, 1233, 1234'
ms.date: 04/01/2021
ms.author: edupont
---
# Eine Positive Pay-Datei exportieren
Um sicherzustellen, dass eine Bank nur validierte Schecks und Beträge freigibt, können Sie eine Positive Pay-Datei exportieren, die die relevanten Zahlungsinformationen enthält wie Schecknummer und Zahlungsbetrag, die Sie als Referenz an die Bank senden, wenn Sie Zahlungen verarbeiten.

[!INCLUDE[prod_short](includes/prod_short.md)] wird vorkonfiguriert, um Positive Pay-Dateien an die Bank of America und City Bank zu senden.

## Um ein Bankkkonto für Positive Pay einzurichten
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte des Bankkontos, für das Sie Positive Pay nutzen möchten.
3. In dem Feld **Positive Pay-Exportcode** geben Sie POSPAYBANK ein.
4. Schließen Sie die Seite.

## Um eine Positive Pay-Datei zu exportieren
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Bankkonto aus, für das Sie eine Positive Pay-Datei exportieren möchten.
3. Wählen Sie die Aktion **Positive Pay-Export** aus.

    Die Seite **Positive Pay-Export** wird geöffnet und zeigt Zahlungen an, die über das Bankkonto seit dem letzten Uploaddatum, wie in den Felder **Letztes Upload-Datum** **Letzte Upload-Zeit** angezeigt, geleistet wurden.
4. Im Feld **Upload-Datum trennen** definieren Sie ein Datum, vor dem Zahlungen nicht in der exportierten Datei enthalten sind.
5. Wählen Sie die Aktion **Exportieren** aus.
6. Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern** und speichern Sie die Datei am gewünschten Speicherort.
7. Laden Sie die Datei in Ihre elektronische Bankseite hoch.
8. Schreiben oder kopieren Sie die Bestätigungsnummer, die angezeigt wird, wenn Sie die Datei erfolgreich hochgeladen haben.

Um exportierte Positive Pay-Datensätze anzuzeigen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Bankkonto aus, für das Sie einen Positive Pay-Datei-Export anzeigen möchten.
3. Wählen Sie die Aktion **Positive Pay-Einträge** aus.

    Auf der Seite **Positive Pay-Posten** können Sie alle Positive Pay-Exportdatensätze für das Bankkonto anzeigen.
4. Geben Sie im Feld **Bestätigungsnummer** für jeden Exportdatensatz die Bestätigungsnummer ein, die Sie gerade erhalten, wann der Dateiupload zur Bank ordnungsgemäß durchgeführt wurde.
5. Um die entsprechenden Zahlungszeilen anzuzeigen, wählen Sie die **Positive Pay-Postendetails** Aktion aus.

Um Positive Pay-Dateien erneut zu exportieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Bankkonto aus, für die Sie Positive Pay-Dateien erneut exportieren möchten.
3. Wählen Sie die Aktion **Positive Pay-Einträge** aus.
4. Wählen Sie die Zeile für die Positive Pay Exportdatei aus, die Sie erneut exportieren möchten.
5. Auf der Seite **Positive Pay-Posten** wählen Sie die Aktion **Erneuter Positive Pay-Export in Datei** aus.

## Weitere Informationen
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]