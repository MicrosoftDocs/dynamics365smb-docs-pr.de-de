---
title: Export von Positive Pay-Dateien| Microsoft Docs
description: Um sicherzustellen, dass Ihre Bank nur überprüfte Schecks und Beträge freigibt, können Sie ihr eine Positive Pay Datei senden, die die Daten für Kreditoren, Schecks und Zahlungsinformationen enthält.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bf57ec93a7c238ecdfe177f77fc85d2ff8249994
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390627"
---
# <a name="export-a-positive-pay-file"></a>Eine Positive Pay-Datei exportieren
Um sicherzustellen, dass eine Bank nur validierte Schecks und Beträge freigibt, können Sie eine Positive Pay-Datei exportieren, die die relevanten Zahlungsinformationen enthält wie Schecknummer und Zahlungsbetrag, die Sie als Referenz an die Bank senden, wenn Sie Zahlungen verarbeiten.

[!INCLUDE[prod_short](includes/prod_short.md)] wird vorkonfiguriert, um Positive Pay-Dateien an die Bank of America und City Bank zu senden.

## <a name="to-set-up-a-bank-account-for-positive-pay"></a>Um ein Bankkkonto für Positive Pay einzurichten
1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte des Bankkontos, für das Sie Positive Pay nutzen möchten.
3. In dem Feld **Positive Pay-Exportcode** geben Sie POSPAYBANK ein.
4. Schließen Sie die Seite.

## <a name="to-export-a-positive-pay-file"></a>Um eine Positive Pay-Datei zu exportieren
1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Bankkonto aus, für das Sie eine Positive Pay-Datei exportieren möchten.
3. Wählen Sie die Aktion **Positive Pay-Export** aus.

    Die Seite **Positive Pay-Export** wird geöffnet und zeigt Zahlungen an, die über das Bankkonto seit dem letzten Uploaddatum, wie in den Felder **Letztes Upload-Datum** **Letzte Upload-Zeit** angezeigt, geleistet wurden.
4. Im Feld **Upload-Datum trennen** definieren Sie ein Datum, vor dem Zahlungen nicht in der exportierten Datei enthalten sind.
5. Wählen Sie die Aktion **Exportieren** aus.
6. Klicken Sie auf der Seite **Datei exportieren** auf die Schaltfläche **Speichern** und speichern Sie die Datei am gewünschten Speicherort.
7. Laden Sie die Datei in Ihre elektronische Bankseite hoch.
8. Schreiben oder kopieren Sie die Bestätigungsnummer, die angezeigt wird, wenn Sie die Datei erfolgreich hochgeladen haben.

Um exportierte Positive Pay-Datensätze anzuzeigen

1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Bankkonto aus, für das Sie einen Positive Pay-Datei-Export anzeigen möchten.
3. Wählen Sie die Aktion **Positive Pay-Einträge** aus.

    Auf der Seite **Positive Pay-Posten** können Sie alle Positive Pay-Exportdatensätze für das Bankkonto anzeigen.
4. Geben Sie im Feld **Bestätigungsnummer** für jeden Exportdatensatz die Bestätigungsnummer ein, die Sie gerade erhalten, wann der Dateiupload zur Bank ordnungsgemäß durchgeführt wurde.
5. Um die entsprechenden Zahlungszeilen anzuzeigen, wählen Sie die **Positive Pay-Postendetails** Aktion aus.

Um Positive Pay-Dateien erneut zu exportieren

1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Bankkonto aus, für die Sie Positive Pay-Dateien erneut exportieren möchten.
3. Wählen Sie die Aktion **Positive Pay-Einträge** aus.
4. Wählen Sie die Zeile für die Positive Pay Exportdatei aus, die Sie erneut exportieren möchten.
5. Auf der Seite **Positive Pay-Posten** wählen Sie die Aktion **Erneuter Positive Pay-Export in Datei** aus.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit allgemeinen Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]