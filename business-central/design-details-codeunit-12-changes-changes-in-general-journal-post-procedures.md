---
title: 'Designdetails: Codeunit 12 Änderungen: Änderungen in Fibu Buch.-Blatt-Beitrags-Verfahren | Microsoft Docs'
description: Die folgenden Änderungen wurden in dieser Version von  Business Central implementiert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5f27bb652009c740066dfa0ef3659bb9e53cfb0e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307348"
---
# <a name="codeunit-12-changes-changes-in-general-journal-post-procedures"></a>Codeunit 12 Änderungen: Änderungen in Fibu Buch.-Blatt-Beitrags-Verfahren
Die folgenden Änderungen wurden in dieser Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] implementiert.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Bemerkung**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GetGLReg|GetGLReg|Aktualisiert|  
|RunWithCheck|RunWithCheck|Aktualisiert|  
|RunWithoutCheck|RunWithoutCheck|Aktualisiert|  
|Code|Code|Aktualisiert|  
||PostGenJnlLine|Teil(e) hinzugefügt|  
||InitAmounts|Teil(e) hinzugefügt|  
||InitLastDocDate|Teil(e) hinzugefügt|  
|InitVAT|InitVAT|Aktualisiert|  
|PostVAT|PostVAT|Aktualisiert|  
|InsertVAT|InsertVAT|Aktualisiert|  
|SummarizeVAT|SummarizeVAT|Aktualisiert|  
|InsertSummarizedVAT|InsertSummarizedVAT|Aktualisiert|  
|PostGLAcc|PostGLAcc|Aktualisiert|  
|PostCust|PostCust|Aktualisiert|  
|PostVend|PostVend|Aktualisiert|  
|PostBankAcc|PostBankAcc|Aktualisiert|  
|PostFixedAsset|PostFixedAsset|Aktualisiert|  
|PostICPartner|PostICPartner|Aktualisiert|  
|InitCodeUnit|StartPosting|Aktualisiert|  
||ContinuePosting|Teil(e) hinzugefügt|  
|FinishCodeunit|FinishPosting|Aktualisiert|  
||PostUnrealizedVAT|Teil(e) hinzugefügt|  
||CheckPostUnrealizedVAT|Teil(e) hinzugefügt|  
||ExchangeAccounts|Teil(e) hinzugefügt|  
|InitGLEntry|InitGLEntry|Aktualisiert|  
||InitGLEntryVAT|Teil(e) hinzugefügt|  
||InitGLEntryVATCopy|Teil(e) hinzugefügt|  
|InsertGLEntry|InsertGLEntry|Aktualisiert|  
||CreateGLEntry|Teil(e) hinzugefügt|  
||CreateGLEntryBalAcc|Teil(e) hinzugefügt|  
||CreateGLEntryVAT|Teil(e) hinzugefügt|  
||CreateGLEntryVATCollectAdj|Teil(e) hinzugefügt|  
||CreateGLEntryFromVATEntry|Teil(e) hinzugefügt|  
||UpdateCheckAmounts|Teil(e) hinzugefügt|  
|ApplyCustLedgEntry|ApplyCustLedgEntry|Aktualisiert|  
||CalcPmtDiscPossible|Teil(e) hinzugefügt|  
||CalcPmtTolerancePossible|Teil(e) hinzugefügt|  
|CalcPmtTolerance|CalcPmtTolerance|Aktualisiert|  
|CalcPmtDisc|CalcPmtDisc|Aktualisiert|  
|CalcPmtDiscIfAdjVAT|CalcPmtDiscIfAdjVAT|Aktualisiert|  
|CalcPmtDiscTolerance|CalcPmtDiscTolerance|Aktualisiert|  
||CalcPmtDiscVATBases|Teil(e) hinzugefügt|  
||CalcPmtDiscVATAmounts|Teil(e) hinzugefügt|  
||InsertPmtDiscVATForVATEntry|Teil(e) hinzugefügt|  
||InsertPmtDiscVATForGLEntry|Teil(e) hinzugefügt|  
|CalcCurrencyApplnRounding|CalcCurrencyApplnRounding|Aktualisiert|  
|FindAmtForAppln|FindAmtForAppln|Aktualisiert|  
|CalcCurrencyUnrealizedGainLoss|CalcCurrencyUnrealizedGainLoss|Aktualisiert|  
|CalcCurrencyRealizedGainLoss|CalcCurrencyRealizedGainLoss|Aktualisiert|  
|CalcApplication|CalcApplication|Aktualisiert|  
|CalcRemainingPmtDisc|CalcRemainingPmtDisc|Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CalcAmtLCYAdjustment|CalcAmtLCYAdjustment|Teil(e) hinzugefügt|  
|InitNewCVLedgEntry|InitFromGenJnlLine|Verschoben zu Tabelle 383 Det. Deb.-/Kred.-Postenpuffer|  
|InitOldCVLedgEntry|CopyFromCVLedgEntryBuf|Verschoben zu Tabelle 383 Det. Deb.-/Kred.-Postenpuffer|  
|InsertDtldCVLedgEntry|InsertDtldCVLedgEntry|Verschoben zu Tabelle 383 Det. Deb.-/Kred.-Postenpuffer|  
||InitBankAccLedgEntry|Teil(e) hinzugefügt|  
||InitCheckLedgEntry|Teil(e) hinzugefügt|  
||InitCustLedgEntry|Teil(e) hinzugefügt|  
||InitVendLedgEntry|Teil(e) hinzugefügt|  
||InsertDtldCustLedgEntry|Teil(e) hinzugefügt|  
||InsertDtldVendLedgEntry|Teil(e) hinzugefügt|  
|CustUnrealizedVAT|CustUnrealizedVAT|Aktualisiert|  
|CustPostApplyCustLedgEntry|CustPostApplyCustLedgEntry|Aktualisiert|  
||PrepareTempCustLedgEntry|Teil(e) hinzugefügt|  
|UnapplyCustLedgEntry|UnapplyCustLedgEntry|Aktualisiert|  
|TransferCustLedgEntry|CopyFromGenJnlLine|Verschoben zu Tabelle 21 Debitorenposten|  
|PostDtldCustLedgEntries|PostDtldCustLedgEntries|Aktualisiert|  
||PostDtldCustLedgEntry|Teil(e) hinzugefügt|  
||PostDtldCustLedgEntryUnapply|Teil(e) hinzugefügt|  
||GetDtldCustLedgEntryAccNo|Teil(e) hinzugefügt|  
|ZeroTransNoDtldCustLedgEntries|SetZeroTransNo|Verschoben zu Tabelle 379 Detaillierte Debitorenposten|  
|AutoEntrForDtldCustLedgEntries||Umgestaltet zu PostDtldCustLedgEntryUnapply|  
|CustUpdateDebitCredit|UpdateDebitCredit|Verschoben zu Tabelle 379 Detaillierte Debitorenposten|  
|ApplyVendLedgEntry|ApplyVendLedgEntry|Aktualisiert|  
||PrepareTempVendLedgEntry|Teil(e) hinzugefügt|  
|VendPostApplyVendLedgEntry|VendPostApplyVendLedgEntry|Aktualisiert|  
|UnapplyVendLedgEntry|UnapplyVendLedgEntry|Aktualisiert|  
|TransferVendLedgEntry|CopyFromGenJnlLine|Verschoben zu Tabelle 25 Kreditorenposten|  
|PostDtldVendLedgEntries|PostDtldVendLedgEntries|Aktualisiert|  
||PostDtldVendLedgEntry|Teil(e) hinzugefügt|  
||PostDtldVendLedgEntryUnapply|Teil(e) hinzugefügt|  
||GetDtldVendLedgEntryAccNo|Teil(e) hinzugefügt|  
||PostDtldCVLedgEntry|Teil(e) hinzugefügt|  
||PostDtldCustVATAdjustment|Teil(e) hinzugefügt|  
||PostDtldVendVATAdjustment|Teil(e) hinzugefügt|  
|ZeroTransNoDtldVendLedgEntries|SetZeroTransNo|Verschoben zu Tabelle 380 Detaillierte Kreditorenposten|  
|AutoEntrForDtldVendLedgEntries||Refactored to PostDtldVendLedgEntryUnapply|  
|VendUpdateDebitCredit|UpdateDebitCredit|Verschoben zu Tabelle 380 Detaillierte Kreditorenposten|  
|VendUnrealizedVAT|VendUnrealizedVAT|Aktualisiert|  
||PostUnrealVATEntry|Teil(e) hinzugefügt|  
||PostApply|Teil(e) hinzugefügt|  
|PostUnrealVATByUnapply|PostUnrealVATByUnapply|Aktualisiert|  
||PostUnapply|Teil(e) hinzugefügt|  
||InsertDtldCustLedgEntryUnapply|Teil(e) hinzugefügt|  
||InsertDtldVendLedgEntryUnapply|Teil(e) hinzugefügt|  
||InsertTempVATEntry|Teil(e) hinzugefügt|  
||ProcessTempVATEntry|Teil(e) hinzugefügt|  
||UpdateCustLedgEntry|Teil(e) hinzugefügt|  
||UpdateVendLedgEntry|Teil(e) hinzugefügt|  
|UpdateCalcInterest|UpdateCalcInterest|Aktualisiert|  
|UpdateCalcInterest2|UpdateCalcInterest2|Aktualisiert|  
|GLCalcAddCurrency|GLCalcAddCurrency|Aktualisiert|  
|HandleAddCurrResidualGLEntry|HandleAddCurrResidualGLEntry|Aktualisiert|  
|CalcLCYToAddCurr|CalcLCYToAddCurr|Aktualisiert|  
|CalcAddCurrFactor||Gelöscht|  
|GetCurrencyExchRate|GetCurrencyExchRate|Aktualisiert|  
|ExchAmount|ExchangeAmount|Verschoben zu Tabelle 330 Währungswechselkurs|  
|ExchangeAmtLCYToFCY2|ExchangeAmtLCYToFCY2|Aktualisiert|  
|CalcAddCurrForUnapplication|CalcAddCurrForUnapplication|Aktualisiert|  
|CheckNonAddCurrCodeOccurred|CheckNonAddCurrCodeOccurred|Aktualisiert|  
|CheckCalcPmtDisc||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CheckCalcPmtDiscCVCust||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CheckCalcPmtDiscCust||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CheckCalcPmtDiscGenJnlCust||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CheckCalcPmtDiscCVVend||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CheckCalcPmtDiscVend||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|CheckCalcPmtDiscGenJnlVend||Verschoben zu Codeunit 426 Zahlungstoleranz-Verwaltung|  
|Reverse|Reverse|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|ReverseCustLedgEntry|ReverseCustLedgEntry|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|ReverseVendLedgEntry|ReverseVendLedgEntry|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|ReverseBankAccLedgEntry|ReverseBankAccLedgEntry|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|ReverseVAT|ReverseVAT|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|SetReversalDescription|SetReversalDescription|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|ApplyCustLedgEntryByReversal|ApplyCustLedgEntryByReversal|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|ApplyVendLedgEntryByReversal|ApplyVendLedgEntryByReversal|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
|PostPmtDiscountVATByUnapply|PostPmtDiscountVATByUnapply|Verschoben zu Codeunit 17 Gen. Jnl.-Post Reverse|  
||CheckDimComb|Hinzugefügt in Codeunit 17 Gen. Jnl.-Post Reverse|  
||CopyCustLedgEntry|Hinzugefügt in Codeunit 17 Gen. Jnl.-Post Reverse|  
||CopyVendLedgEntry|Hinzugefügt in Codeunit 17 Gen. Jnl.-Post Reverse|  
||CopyBankAccLedgEntry|Hinzugefügt in Codeunit 17 Gen. Jnl.-Post Reverse|  
|HandlDtlAddjustment|HandleDtldAdjustment|Aktualisiert|  
|CollectAddjustment|CollectAdjustment|Aktualisiert|  
|SetOverDimErr|SetOverDimErr|Aktualisiert|  
|PostJob|PostJob|Aktualisiert|  
|InsertVATEntriesFromTemp|InsertVATEntriesFromTemp|Aktualisiert|  
|CaptureOrRefundCreditCardPmnt|CaptureOrRefundCreditCardPmnt|Aktualisiert|  
|UpdateDOPaymentTransactEntry|UpdateDOPaymentTransactEntry|Aktualisiert|  
|ABSMin|ABSMin|Aktualisiert|  
|GetApplnRoundPrecision|GetApplnRoundPrecision|Aktualisiert|  
|CheckDimValueForDisposal|CheckDimValueForDisposal|Aktualisiert|  
|CalculateCurrentBalance|CalculateCurrentBalance|Aktualisiert|  
|IncludeVATAmount||Verschoben zu Tabelle 81 Gen. Buch.-Blattzeile|  
|CalcVATAmountFromVATEntry|CalcVATAmountFromVATEntry|Aktualisiert|  
||TotalVATAmountOnJnlLines|Teil(e) hinzugefügt|  
||SetGLRegReverse|Teil(e) hinzugefügt|  
||GetGLSetup|Teil(e) hinzugefügt|  
||ReadGLSetup|Teil(e) hinzugefügt|  
||CheckSalesExtDocNo|Teil(e) hinzugefügt|  
||CheckPurchExtDocNo|Teil(e) hinzugefügt|  
||CheckGLAccDimError|Teil(e) hinzugefügt|  
||GetCurrency|Teil(e) hinzugefügt|  
||PostDtldAdjustment|Teil(e) hinzugefügt|  
||GetNextEntryNo|Teil(e) hinzugefügt|  
||GetNextTransactionNo|Teil(e) hinzugefügt|  
||GetNextVATEntryNo|Teil(e) hinzugefügt|  
||IncrNextVATEntryNo|Teil(e) hinzugefügt|  
||IsNotPayment|Teil(e) hinzugefügt|  
||IsTempGLEntryBufEmpty|Teil(e) hinzugefügt|  
||IsVATAdjustment|Teil(e) hinzugefügt|  
||IsVATExcluded|Teil(e) hinzugefügt|  
||UpdateDimensions|Teil(e) hinzugefügt|  
||UpdateDimensionsFromCustLedgEntry|Teil(e) hinzugefügt|  
||UpdateDimensionsFromVendLedgEntry|Teil(e) hinzugefügt|  
||UpdateTotalAmounts|Teil(e) hinzugefügt|  
||CreateGLEntriesForTotalAmounts|Teil(e) hinzugefügt|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Codeunit 12 Änderungen: Zuordnen der globalen Variablen für Fibu Buch.-Blatt-Beitrags-Zeile](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)
