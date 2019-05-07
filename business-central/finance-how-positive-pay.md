---
title: Export von Positive Pay-Dateien| Microsoft Docs
description: Um sicherzustellen, dass Ihre Bank nur überprüfte Schecks und Beträge freigibt, können Sie ihr eine Positive Pay Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c2a3a1e94eaa5fee747ce52726765ff1f9401bb2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "915407"
---
# <a name="export-a-positive-pay-file"></a>Eine Positive Pay-Datei exportieren
Um sicherzustellen, dass eine Bank nur validierte Schecks und Beträge freigibt, können Sie eine Positive Pay-Datei exportieren, die die relevanten Zahlungsinformationen enthält wie Schecknummer und Zahlungsbetrag, die Sie als Referenz an die Bank senden, wenn Sie Zahlungen verarbeiten.

[!INCLUDE[d365fin](includes/d365fin_md.md)] wird vorkonfiguriert, um Positive Pay-Dateien an die Bank of America und City Bank zu senden.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Um ein Bankkkonto für Positive Pay einzurichten
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte des Bankkontos, für das Sie Positive Pay nutzen möchten.
3. In dem Feld **Positive Pay-Exportcode** geben Sie POSPAYBANK ein.
4. Schließen Sie die Seite.

## <a name="to-export-a-positive-pay-file"></a>Um eine Positive Pay-Datei zu exportieren
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das Bankkonto aus, für das Sie eine Positive Pay-Datei exportieren möchten.
3. Wählen Sie die Aktion **Positive Pay-Export** aus.

    Die Seite **Positive Pay-Export** wird geöffnet und zeigt Zahlungen an, die über das Bankkonto seit dem letzten Uploaddatum, wie in den Felder **Letztes Upload-Datum** **Letzte Upload-Zeit** angezeigt, geleistet wurden.
4. Im Feld **Upload-Datum trennen** definieren Sie ein Datum, vor dem Zahlungen nicht in der exportierten Datei enthalten sind.
5. Wählen Sie die Aktion **Exportieren** aus.
6. Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern** und speichern Sie die Datei am gewünschten Speicherort.
7. Laden Sie die Datei in Ihre elektronische Bankseite hoch.
8. Schreiben oder kopieren Sie die Bestätigungsnummer, die angezeigt wird, wenn Sie die Datei erfolgreich hochgeladen haben.

Um exportierte Positive Pay-Datensätze anzuzeigen

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das Bankkonto aus, für das Sie einen Positive Pay-Datei-Export anzeigen möchten.
3. Wählen Sie die Aktion **Positive Pay-Einträge** aus.

    Auf der Seite **Positive Pay-Posten** können Sie alle Positive Pay-Exportdatensätze für das Bankkonto anzeigen.
4. Geben Sie im Feld **Bestätigungsnummer** für jeden Exportdatensatz die Bestätigungsnummer ein, die Sie gerade erhalten, wann der Dateiupload zur Bank ordnungsgemäß durchgeführt wurde.
5. Um die entsprechenden Zahlungszeilen anzuzeigen, wählen Sie die **Positive Pay-Postendetails** Aktion aus.

Um Positive Pay-Dateien erneut zu exportieren

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Bankkonten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das Bankkonto aus, für die Sie Positive Pay-Dateien erneut exportieren möchten.
3. Wählen Sie die Aktion **Positive Pay-Einträge** aus.
4. Wählen Sie die Zeile für die Positive Pay Exportdatei aus, die Sie erneut exportieren möchten.
5. Auf der Seite **Positive Pay-Posten** wählen Sie die Aktion **Erneuter Positive Pay-Export in Datei** aus.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
