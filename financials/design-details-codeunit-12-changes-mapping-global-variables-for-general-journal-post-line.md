---
title: "Designdetails: Codeunit 12 Änderungen: Zuordnen der globalen Variablen für Fibu Buch.-Blatt-Beitrags-Zeile | Microsoft Docs"
description: "Die folgenden Änderungen werden in dieser Version von Finance and Operations, Business edition  implementiert wurden."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d1199adb2912d88c545cabcc84d5c9bf27b0892a
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="codeunit-12-changes-mapping-global-variables-for-general-journal-post-line"></a>Codeunit 12 Änderungen: Zuordnen der globalen Variablen für Fibu Buch.-Blatt-Beitrags-Zeile
Die folgenden Änderungen wurden in dieser Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] implementiert.  

|**Microsoft Dynamics NAV 2009 R2**|**Microsoft Dynamics NAV 2013 R2**|**Bemerkung**|  
|----------------------------------------|----------------------------------------|-----------------|  
|GLSetup@1009Datensatz 98:|GLSetup@1009Datensatz 98:|Nicht geändert|  
|SalesSetup@1010Datensatz 311:||Geändert zu lokal|  
|PurchSetup@1011Datensatz 312:||Geändert zu lokal|  
|AccountingPeriod@1012Datensatz 50:||Geändert zu lokal|  
|GLAcc@1013Datensatz 15:||Geändert zu lokal|  
|GLEntry@1014Datensatz 17:|GlobalGLEntry@1014Datensatz 17:|Umbenannt|  
|GLEntryTmp@1015 : TEMPORÄRER Datensatz 17;|TempGLEntryBuf@1010 : TEMPORÄRER Datensatz 17;|Umbenannt|  
|TempGLEntryVAT@1016 : TEMPORÄRER Datensatz 17;|TempGLEntryVAT@1016 : TEMPORÄRER Datensatz 17;|Nicht geändert|  
|OrigGLEntry@1017Datensatz 17:||Gelöscht|  
|VATPostingSetup@1019Datensatz 325:||Geändert zu lokal|  
|Cust@1020Datensatz 18:||Geändert zu lokal|  
|Vend@1021Datensatz 23:||Geändert zu lokal|  
|GenJnlLine@1022Datensatz 81:||Geändert zu lokal|  
|GLReg@1029Datensatz 45:|GLReg@1029Datensatz 45:|Nicht geändert|  
|CustPostingGr@1030Datensatz 92:||Geändert zu lokal|  
|VendPostingGr@1031Datensatz 93:||Geändert zu lokal|  
|Currency@1032Datensatz 4:||Geändert zu lokal|  
|AddCurrency@1033Datensatz 4:|AddCurrency@1033Datensatz 4:|Nicht geändert|  
|ApplnCurrency@1034Datensatz 4:||Geändert zu lokal|  
|CurrExchRate@1035Datensatz 330:|CurrExchRate@1035Datensatz 330:|Nicht geändert|  
|VATEntry@1038Datensatz 254:|VATEntry@1038Datensatz 254:|Nicht geändert|  
|BankAcc@1039Datensatz 270:||Geändert zu lokal|  
|BankAccLedgEntry@1040Datensatz 271:||Geändert zu lokal|  
|CheckLedgEntry@1041Datensatz 272:||Geändert zu lokal|  
|CheckLedgEntry2@1042Datensatz 272:||Geändert zu lokal|  
|BankAccPostingGr@1043Datensatz 277:||Geändert zu lokal|  
|GenJnlTemplate@1044Datensatz 80:||Geändert zu lokal|  
|TaxJurisdiction@1045Datensatz 320:||Geändert zu lokal|  
|TaxDetail@1046Datensatz 322:|TaxDetail@1046Datensatz 322:|Nicht geändert|  
|FAGLPostBuf@1047 : TEMPORÄRER Datensatz 5637;||Geändert zu lokal|  
|UnrealizedCustLedgEntry@1084Datensatz 21:|UnrealizedCustLedgEntry@1084Datensatz 21:|Nicht geändert|  
|UnrealizedVendLedgEntry@1085Datensatz 25:|UnrealizedVendLedgEntry@1085Datensatz 25:|Nicht geändert|  
|GLEntryVATEntryLink@1087Datensatz 253:|GLEntryVATEntryLink@1087Datensatz 253:|Nicht geändert|  
|TempVATEntry@1088 : TEMPORÄRER Datensatz 254;|TempVATEntry@1088 : TEMPORÄRER Datensatz 254;|Nicht geändert|  
|ReversedGLEntryTemp@1089 : TEMPORÄRER Datensatz 17;||Verschoben zu Codeunit17|  
|CostAccSetup@1092Datensatz 1108:||Geändert zu lokal|  
|GenJnlCheckLine@1048: Codeunit11;|GenJnlCheckLine@1001Codeunit11;|Nicht geändert|  
|ExchAccGLJnlLine@1049: Codeunit366;||Geändert zu lokal|  
|FAJnlPostLine@1050 : Codeunit 5632;||Geändert zu lokal|  
|SalesTaxCalculate@1051 : Codeunit 398;||Geändert zu lokal|  
|GenJnlApply@1052 : Codeunit 225;||Geändert zu lokal|  
|DimMgt@1053 : Codeunit 408;||Geändert zu lokal|  
|JobPostLine@1028 : Codeunit 1001;||Geändert zu lokal|  
|TransferGlEntriesToCA@1091 : Codeunit 1105;||Geändert zu lokal|  
||PaymentToleranceMgt@1002 : Codeunit 426;|Teil(e) hinzugefügt|  
||AddCurrencyCode@1117: Code[10];|Teil(e) hinzugefügt|  
|FiscalYearStartDate@1054 : Datum;|FiscalYearStartDate@1011 : Datum;|Nicht geändert|  
|NextEntryNo@1055Ganzzahl;|NextEntryNo@1022Ganzzahl;|Nicht geändert|  
|BalanceCheckAmount@1056Dezimal;|BalanceCheckAmount@1056Dezimal;|Nicht geändert|  
|BalanceCheckAmount2@1057Dezimal;|BalanceCheckAmount2@1057Dezimal;|Nicht geändert|  
|BalanceCheckAddCurrAmount@1058Dezimal;|BalanceCheckAddCurrAmount@1058Dezimal;|Nicht geändert|  
|BalanceCheckAddCurrAmount2@1059Dezimal;|BalanceCheckAddCurrAmount2@1059Dezimal;|Nicht geändert|  
|CurrentBalance@1060Dezimal;|CurrentBalance@1060Dezimal;|Nicht geändert|  
|SalesTaxBaseAmount@1061Dezimal;||Geändert zu lokal|  
|TotalAddCurrAmount@1062 Dezimal;|TotalAddCurrAmount@1062 Dezimal;|Nicht geändert|  
|TotalAmount@1063Dezimal;|TotalAmount@1063Dezimal;|Nicht geändert|  
|UnrealizedRemainingAmountCust@1086Dezimal;|UnrealizedRemainingAmountCust@1086Dezimal;|Nicht geändert|  
|UnrealizedRemainingAmountVend@1074Dezimal;|UnrealizedRemainingAmountVend@1074Dezimal;|Nicht geändert|  
|NextVATEntryNo@1064 Ganzzahl;|NextVATEntryNo@1064 Ganzzahl;|Nicht geändert|  
|FirstNewVATEntryNo@1065 Ganzzahl;|FirstNewVATEntryNo@1065 Ganzzahl;|Nicht geändert|  
|NextTransactionNo@1066 Ganzzahl;|NextTransactionNo@1066 Ganzzahl;|Nicht geändert|  
|NextConnectionNo@1067 Ganzzahl;|NextConnectionNo@1067 Ganzzahl;|Nicht geändert|  
|InsertedTempGLEntryVAT@1068 Ganzzahl;|InsertedTempGLEntryVAT@1027 Ganzzahl;|Nicht geändert|  
|LastDocNo@1069: Code[20];|LastDocNo@1023: Code[20];|Nicht geändert|  
|LastLineNo@1070Ganzzahl;||Gelöscht|  
|LastDate@1071 : Datum;|LastDate@1021 : Datum;|Nicht geändert|  
|LastDocType@1072 Rechnung, Zahlung, Gutschrift, Zinsrechnung oder Mahnung.|LastDocType@1025 Rechnung, Zahlung, Gutschrift, Zinsrechnung oder Mahnung.|Nicht geändert|  
|NextCheckEntryNo@1073Ganzzahl;|NextCheckEntryNo@1028Ganzzahl;|Nicht geändert|  
|AddCurrGLEntryVATAmt@1075Dezimal;|AddCurrGLEntryVATAmt@1017Dezimal;|Nicht geändert|  
|CurrencyDate@1076 : Datum;|CurrencyDate@1020 : Datum;|Nicht geändert|  
|CurrencyFactor@1077Dezimal;|CurrencyFactor@1019Dezimal;|Nicht geändert|  
|UseCurrFactorOnly@1078 : Boolean;|UseCurrFactorOnly@1078 : Boolean;|Nicht geändert|  
|NonAddCurrCodeOccured@1079 : Boolean;|NonAddCurrCodeOccured@1079 : Boolean;|Nicht geändert|  
|FADimAlreadyChecked@1080 : Boolean;|FADimAlreadyChecked@1080 : Boolean;|Nicht geändert|  
|AllApplied@1081 : Boolean;||Geändert zu lokal|  
|OverrideDimErr@1018 : Boolean;|OverrideDimErr@1018 : Boolean;|Nicht geändert|  
|JobLine@1036 : Boolean;|JobLine@1036 : Boolean;|Nicht geändert|  
|Prepayment@1037 : Boolean;||Gelöscht|  
|CheckUnrealizedCust@1082 : Boolean;|CheckUnrealizedCust@1082 : Boolean;|Nicht geändert|  
|CheckUnrealizedVend@1083 : Boolean;|CheckUnrealizedVend@1083 : Boolean;|Nicht geändert|  
|GLEntryNo@1090Ganzzahl;|GLEntryNo@1026Ganzzahl;|Nicht geändert|  
||GLSetupRead@1015 : Boolean;|Teil(e) hinzugefügt|  
||AmountRoundingPrecision@1012Dezimal;|Teil(e) hinzugefügt|  
||CrCardTransactionEntryNo@1013Ganzzahl;|Teil(e) hinzugefügt|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Codeunit 12 Änderungen: Änderungen in Fibu Buch.-Blatt-Beitrags-Verfahren](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)

