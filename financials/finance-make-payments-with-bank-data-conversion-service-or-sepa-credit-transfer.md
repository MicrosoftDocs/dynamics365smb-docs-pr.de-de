---
title: "Nehmen Sie Zahlungen mit dem| Microsoft Docs Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor | Microsoft Docs"
description: Verwalten Sie Zahlungen an Ihre Kreditoren, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 0760b5480b3c2de9bc370526bd87da2c9a492d92
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor
Im Fenster **Zahlungsjournal** können Sie Zahlungen an Ihre Kreditoren verarbeiten, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.   

 Um SEPA-Banküberweisungen zu aktivieren, müssen Sie zunächst ein Bankkonto, einen Kreditor und das Fibu Buch.-Blatt anlegen, auf dem das Zahlungsausgangs Buch.-Blatt basiert. Sie bereiten dann Zahlungen an Kreditoren vor, indem Sie das Fenster **Zahlungsjournal** automatisch mit fälligen Zahlungen mit angegebenen Buchungsdaten ausfüllen.  

> [!NOTE]  
>  Wenn Sie geprüft haben, ob die Zahlungen erfolgreich von der Bank verarbeitet wurden, können Sie mit der Buchung der Zahlungsausgangs Buch.-Blattzeilen fortfahren.  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Aktivieren Sie Bankdatenkonvertierungsfunktion, um eine beliebige Bankkontoauszugsdatei in ein Format umzuwandeln, das Sie importieren können, oder um Ihre exportierten Zahlungsdateien in das Format umzuwandeln, das Ihre Bank verlangt.|[Gewusst wie: Einrichten des Bankdatenkonvertierungsservice](bank-how-setup-bank-statement-service.md)|  
|Richten Sie ein Bankkonto, einen Lieferanten und ein Zahlungsbuch für SEPA-Banküberweisung ein.|[So wird's gemacht: SEPA-Kreditübertragungen einrichten](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Füllen Sie das Zahlungsausgangs Buch.-Blatt mit Zeilen für fällige Zahlungen an Kreditoren, mit der Option, Buchungsdaten basierend auf dem Fälligkeitsdatum der zugehörigen Einkaufsbelege einzufügen.|[Verwalten von Verbindlichkeiten](payables-manage-payables.md)|  
|Exportieren von Zahlungsausgangs Buch.-Blattzeilen in eine Datei im SEPA-Banküberweisungsformat.|[Vorgehensweise: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md)|  
|Wenn die elektronische Zahlung erfolgreich von der Bank verarbeitet wird, buchen Sie die Zahlungen.|[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)|  

## <a name="see-also"></a>Siehe auch  
[Gewusst wie: Einrichten des Bankdatenkonvertierungsservice](bank-how-setup-bank-statement-service.md)  
[So wird's gemacht: SEPA-Kreditübertragungen einrichten](finance-how-to-set-up-sepa-credit-transfer.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)   
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Einziehen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)   

