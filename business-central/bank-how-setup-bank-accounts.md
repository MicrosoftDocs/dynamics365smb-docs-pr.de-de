---
title: Einrichten von Bankkonten| Microsoft Docs
description: Sie können Bankkonten mit den Auszügen der Bank abstimmen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8bac106f5f75cd5ebdce8b5da392a1e316184144
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783897"
---
# <a name="set-up-bank-accounts"></a>Bankkonten einrichten
In [!INCLUDE[prod_short](includes/prod_short.md)] verwenden Sie Bankkonten, um Ihre Banktransaktionen nachzuvollziehen. Konten können in Mandantenwährung oder in Fremdwährung geführt werden. Nachdem Sie Bankkonten eingerichtet haben, können Sie auch Schecks drucken.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

## <a name="to-set-up-bank-accounts"></a>Bankkonten einrichten:
1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet, geben Sie **Bankkonten** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Bankkonten** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Um das Feld **Saldo** mit einem Eröffnungsbilanz auszufüllen, müssen Sie den Bankposten mit dem entsprechenden Betrag buchen. Sie können dies tun, indem Sie eine Bankkontoabstimmung durchführen. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md). Alternativ können Sie die Eröffnungsbilanz als Teil der allgemeinen Datenerstellung in neuen Unternehmen implementieren, indem Sie den Leitfaden für das unterstützte Setup **Geschäftsdaten migrieren** verwenden. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten
Felder auf dem Inforegister **Transfer** im Fenster **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md) und [Einrichten des Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Bankkonten** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für ein Bankkonto, mit dem Sie Bankdateien exportieren oder importieren, indem Sie den Bankdatenkonvertierungs-Service verwenden.
3. Füllen Sie im Inforegister **Übertrag** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte auf der Seite **Bankkontokarte** Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren. Lesen die Kurzbeschreibungen der Felder sorgfältig durch oder gehen Sie zu den entsprechenden Verfahrensthemen. Für den Export einer Zahlungsdatei für den nordamerikanischen EFT (Electronic Funds Transfer) beispielsweise müssen die Felder **Letzte Rimesseavis-Nr.** und **Transitnr.** ausgefüllt werden. Weitere Informationen finden Sie unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten

Felder auf dem Inforegister **Transfer** auf der Seite **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md) und [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Karte für einen Kreditor, dem Sie Zahlungsbankdateien auf das Bankkonto exportieren möchten.
3. Wählen Sie die **Bankkonten** Aktion aus.
4. Wählen Sie aus der **Liste der Kreditorenbankkonten** das entsprechende Bankkonto aus, oder fügen Sie ein neues Bankkonto hinzu.  
5. Füllen Sie auf der Seite **Kreditoren-Bankkontokarte** im Inforegister **Übertragung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Siehe auch

[Einrichten von Banken](bank-setup-banking.md)  
[Buchungsgruppen einrichten](finance-posting-groups.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]