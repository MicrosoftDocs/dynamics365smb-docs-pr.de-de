---
title: Änderungen bei der Zuordnung globaler Variablen für die Buchung in Codeunit 12
description: In früheren Versionen wurde Codeunit 12 geändert, um die Leistung beim Posten aus dem allgemeinen Journal zu verbessern. Erfahren Sie mehr über die Änderungen an den globalen Variablen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e31f26510654ff95c27cdc08643f335c546e10f5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776866"
---
# <a name="historical-changes-to-codeunit-12-mapping-global-variables-for-general-journal-post-line"></a>Frühere Änderungen in Codeunit 12: Zuordnen der globalen Variablen für Fibu Buch.-Blatt-Beitrags-Zeile

Die folgenden Änderungen wurden in dieser Version von [!INCLUDE [navnow_md](includes/navnow_md.md)] implementiert.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Bemerkung**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009 : Record 98;|GLSetup@1009 : Record 98;|Nicht geändert|  
|SalesSetup@1010 : Record 311;||Geändert zu lokal|  
|PurchSetup@1011 : Record 312;||Geändert zu lokal|  
|AccountingPeriod@1012 : Record 50;||Geändert zu lokal|  
|GLAcc@1013 : Record 15;||Geändert zu lokal|  
|GLEntry@1014 : Record 17;|GlobalGLEntry@1014 : Record 17;|Umbenannt|  
|GLEntryTmp@1015 : TEMPORARY Record 17;|TempGLEntryBuf@1010 : TEMPORARY Record 17;|Umbenannt|  
|TempGLEntryVAT@1016 : TEMPORARY Record 17;|TempGLEntryVAT@1016 : TEMPORARY Record 17;|Nicht geändert|  
|OrigGLEntry@1017 : Record 17;||Gelöscht|  
|VATPostingSetup@1019 : Record 325;||Geändert zu lokal|  
|Cust@1020 : Record 18;||Geändert zu lokal|  
|Vend@1021 : Record 23;||Geändert zu lokal|  
|GenJnlLine@1022 : Record 81;||Geändert zu lokal|  
|GLReg@1029 : Record 45;|GLReg@1029 : Record 45;|Nicht geändert|  
|CustPostingGr@1030 : Record 92;||Geändert zu lokal|  
|VendPostingGr@1031 : Record 93;||Geändert zu lokal|  
|Currency@1032 : Record 4;||Geändert zu lokal|  
|AddCurrency@1033 : Record 4;|AddCurrency@1033 : Record 4;|Nicht geändert|  
|ApplnCurrency@1034 : Record 4;||Geändert zu lokal|  
|CurrExchRate@1035 : Record 330;|CurrExchRate@1035 : Record 330;|Nicht geändert|  
|VATEntry@1038 : Record 254;|VATEntry@1038 : Record 254;|Nicht geändert|  
|BankAcc@1039 : Record 270;||Geändert zu lokal|  
|BankAccLedgEntry@1040 : Record 271;||Geändert zu lokal|  
|CheckLedgEntry@1041 : Record 272;||Geändert zu lokal|  
|CheckLedgEntry2@1042 : Record 272;||Geändert zu lokal|  
|BankAccPostingGr@1043 : Record 277;||Geändert zu lokal|  
|GenJnlTemplate@1044 : Record 80;||Geändert zu lokal|  
|TaxJurisdiction@1045 : Record 320;||Geändert zu lokal|  
|TaxDetail@1046 : Record 322;|TaxDetail@1046 : Record 322;|Nicht geändert|  
|FAGLPostBuf@1047 : TEMPORARY Record 5637;||Geändert zu lokal|  
|UnrealizedCustLedgEntry@1084 : Record 21;|UnrealizedCustLedgEntry@1084 : Record 21;|Nicht geändert|  
|UnrealizedVendLedgEntry@1085 : Record 25;|UnrealizedVendLedgEntry@1085 : Record 25;|Nicht geändert|  
|GLEntryVATEntryLink@1087 : Record 253;|GLEntryVATEntryLink@1087 : Record 253;|Nicht geändert|  
|TempVATEntry@1088 : TEMPORARY Record 254;|TempVATEntry@1088 : TEMPORARY Record 254;|Nicht geändert|  
|ReversedGLEntryTemp@1089 : TEMPORARY Record 17;||Verschoben zu Codeunit17|  
|CostAccSetup@1092 : Record 1108;||Geändert zu lokal|  
|GenJnlCheckLine@1048 : Codeunit 11;|GenJnlCheckLine@1001 : Codeunit 11;|Nicht geändert|  
|ExchAccGLJnlLine@1049 : Codeunit 366;||Geändert zu lokal|  
|FAJnlPostLine@1050 : Codeunit 5632;||Geändert zu lokal|  
|SalesTaxCalculate@1051 : Codeunit 398;||Geändert zu lokal|  
|GenJnlApply@1052 : Codeunit 225;||Geändert zu lokal|  
|DimMgt@1053 : Codeunit 408;||Geändert zu lokal|  
|JobPostLine@1028 : Codeunit 1001;||Geändert zu lokal|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Geändert zu lokal|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Teil(e) hinzugefügt|  
||AddCurrencyCode@1117 : Code[10];|Teil(e) hinzugefügt|  
|FiscalYearStartDate@1054 : Date;|FiscalYearStartDate@1011 : Date;|Nicht geändert|  
|NextEntryNo@1055 : Integer;|NextEntryNo@1022 : Integer;|Nicht geändert|  
|BalanceCheckAmount@1056 : Decimal;|BalanceCheckAmount@1056 : Decimal;|Nicht geändert|  
|BalanceCheckAmount2@1057 : Decimal;|BalanceCheckAmount2@1057 : Decimal;|Nicht geändert|  
|BalanceCheckAddCurrAmount@1058 : Decimal;|BalanceCheckAddCurrAmount@1058 : Decimal;|Nicht geändert|  
|BalanceCheckAddCurrAmount2@1059 : Decimal;|BalanceCheckAddCurrAmount2@1059 : Decimal;|Nicht geändert|  
|CurrentBalance@1060 : Decimal;|CurrentBalance@1060 : Decimal;|Nicht geändert|  
|SalesTaxBaseAmount@1061 : Decimal;||Geändert zu lokal|  
|TotalAddCurrAmount@1062 : Decimal;|TotalAddCurrAmount@1062 : Decimal;|Nicht geändert|  
|TotalAmount@1063 : Decimal;|TotalAmount@1063 : Decimal;|Nicht geändert|  
|UnrealizedRemainingAmountCust@1086 : Decimal;|UnrealizedRemainingAmountCust@1086 : Decimal;|Nicht geändert|  
|UnrealizedRemainingAmountVend@1074 : Decimal;|UnrealizedRemainingAmountVend@1074 : Decimal;|Nicht geändert|  
|NextVATEntryNo@1064 : Integer;|NextVATEntryNo@1064 : Integer;|Nicht geändert|  
|FirstNewVATEntryNo@1065 : Integer;|FirstNewVATEntryNo@1065 : Integer;|Nicht geändert|  
|NextTransactionNo@1066 : Integer;|NextTransactionNo@1066 : Integer;|Nicht geändert|  
|NextConnectionNo@1067 : Integer;|NextConnectionNo@1067 : Integer;|Nicht geändert|  
|InsertedTempGLEntryVAT@1068 : Integer;|InsertedTempGLEntryVAT@1027 : Integer;|Nicht geändert|  
|LastDocNo@1069 : Code[20];|LastDocNo@1023 : Code[20];|Nicht geändert|  
|LastLineNo@1070 : Integer;||Gelöscht|  
|LastDate@1071 : Date;|LastDate@1021 : Date;|Nicht geändert|  
|LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder';|Nicht geändert|  
|NextCheckEntryNo@1073 : Integer;|NextCheckEntryNo@1028 : Integer;|Nicht geändert|  
|AddCurrGLEntryVATAmt@1075 : Decimal;|AddCurrGLEntryVATAmt@1017 : Decimal;|Nicht geändert|  
|CurrencyDate@1076 : Date;|CurrencyDate@1020 : Date;|Nicht geändert|  
|CurrencyFactor@1077 : Decimal;|CurrencyFactor@1019 : Decimal;|Nicht geändert|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Nicht geändert|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Nicht geändert|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Nicht geändert|  
|AllApplied@1081 : Boolean;||Geändert zu lokal|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Nicht geändert|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Nicht geändert|  
|Prepayment@1037 : Boolean;||Gelöscht|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Nicht geändert|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Nicht geändert|  
|GLEntryNo@1090 : Integer;|GLEntryNo@1026 : Integer;|Nicht geändert|  
||GLSetupRead@1015 : Boolean;|Teil(e) hinzugefügt|  
||AmountRoundingPrecision@1012 : Decimal;|Teil(e) hinzugefügt|  
||CrCardTransactionEntryNo@1013 : Integer;|Teil(e) hinzugefügt|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Codeunit 12 Änderungen: Änderungen in Fibu Buch.-Blatt-Beitrags-Verfahren](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]