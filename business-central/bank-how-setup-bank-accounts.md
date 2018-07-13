---
title: Einrichten von Bankkonten| Microsoft Docs
description: "Sie können Bankkonten mit den Auszügen der Bank abstimmen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 68a618ff528589ce9b72a2441cbf3a442cbbb0d8
ms.contentlocale: de-de
ms.lasthandoff: 06/01/2018

---
# <a name="set-up-bank-accounts"></a>Bankkonten einrichten
In [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden Sie Bankkonten, um Ihre Banktransaktionen nachzuvollziehen. Konten können in Mandantenwährung oder in Fremdwährung geführt werden. Nachdem Sie Bankkonten eingerichtet haben, können Sie auch Schecks drucken.

## <a name="to-set-up-bank-accounts"></a>Bankkonten einrichten:
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Bankkonten** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Um das Feld **Saldo** mit einem Eröffnungsbilanz auszufüllen, müssen Sie den Bankposten mit dem entsprechenden Betrag buchen. Sie können dies tun, indem Sie eine Bankkontoabstimmung durchführen. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md). Alternativ können Sie die Eröffnungsbilanz als Teil der allgemeinen Datenerstellung in neuen Unternehmen implementieren, indem Sie das unterstützte Setup **Geschäftsdaten migrieren** verwenden. Weitere Informationen finden Sie unter [Erste Schritte](product-get-started.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten
Felder auf dem Inforegister **Transfer** im Fenster **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [Einrichten des Bankdatenkonvertierungsdienstes](bank-how-setup-bank-data-conversion-service.md) und [Einrichten des Envestnet Yodlee Bankfeed-Diensts](bank-how-setup-bank-statement-service.md).

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Karte für ein Bankkonto, mit dem Sie Bankdateien exportieren oder importieren, indem Sie den Bankdatenkonvertierungs-Service verwenden.
3. Füllen Sie im Inforegister **Übertrag** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte im Fenster **Bankkontokarte** Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren. Lesen die Kurzbeschreibungen der Felder sorgfältig durch oder gehen Sie zu den entsprechenden Verfahrensthemen. Für den Export einer Zahlungsdatei für den nordamerikanischen EFT (Electronic Funds Transfer) beispielsweise müssen die Felder **Letzte Rimesseavis-Nr.** und **Transitnr.** ausgefüllt werden. Weitere Informationen finden Sie unter [Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Um Ihre Bankkonten zum Importieren und Exportieren von Bankdateien einzurichten
Felder auf dem Inforegister **Transfer** im Fenster **Bankkontenkarte** beziehen sich auf den Import und den Export von Bankfeeds und Dateien. Weitere Informationen finden Sie unter [Einrichten des Bankdatenkonvertierungsdientes](bank-how-setup-bank-data-conversion-service.md) und [Einrichten einer Exportzahlung an eine Bankdatei](payables-how-export-payments-bank-file.md).

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Karte für einen Kreditor, dem Sie Zahlungsbankdateien auf das Bankkonto exportieren möchten.
3. Wählen Sie die **Bankkonten** Aktion aus.
3. Füllen Sie im Fenster **Kreditoren-Bankkontokarte** im Inforegister **Übertragung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Siehe auch
[Einrichten von Banken](bank-setup-banking.md)  
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

