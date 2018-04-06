---
title: SEPA Direct Debit in Finance and Operations, Business edition | Microsoft Docs einrichten
description: "Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden gemäß dem SEPA-Format einziehen."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cf07a08eebe8bfffc99f7351a96526452728552e
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Einziehen von Zahlungen per Lastschriftverfahren SEPA
Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden gemäß dem SEPA-Format einziehen.  

 Richten Sie zuerst das Exportformat der Bankdatei ein, die Ihrer Bank aufträgt, eine Lastschrift durchführen. Richten Sie dann die Zahlungsmethode des Debitors ein. Richten Sie schließlich das Lastschrift-Mandat ein, die Ihrer Übereinkunft mit dem Kunden zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

 Um die Bank anzuweisen, den Zahlungsbetrag vom Bankkonto des Debitors auf das Bankkonto Ihres Unternehmens zu überweisen, erstellen Sie einen Lastschrifteinzugposten mit Informationen zu Bankkonten, den betroffenen Verkaufsrechnungen und dem Lastschrift-Mandat. Anschließend exportieren Sie eine XML-Datei, die auf dem Einzugseintrag basiert, und senden Sie zur Verarbeitung an Ihre Bank. Alle Zahlungen, die nicht verarbeitet werden konnten, werden Ihnen von Ihrer Bank mitgeteilt, und Sie müssen dann die jeweiligen Lastschrifteinzugsposten manuell ablehnen.  

 Sie können Standarddebitorverkaufscodes mit Informationen zum Lastschrifteinzug und zu Einzugsermächtigungen einrichten. Anschließend können Sie mit der **Standard-Debitorenrechnung erstellen**-Stapelverarbeitung mehrere Verkaufsrechnungen erstellen, die bereits vorab die Einzugsinformationen enthalten. Dies kann manuell oder automatisch durchgeführt werden, je nach dem Zahlungsfälligkeitsdatum.  

 Wenn Ihre Bank Ihnen mitteilt, dass Zahlungen erfolgreich verarbeitet wurden, können Sie die Zahlungseingänge direkt aus dem Fenster **Lastschriftenposten** buchen, oder indem Sie die Zahlungszeilen in das Buch verschieben, in dem Sie Zahlungseingänge buchen, etwa das Fenster **Zahlungseingangs Buch.-Blatt**. Je nach Ihrem Cash-Management-Prozess können Sie auch warten und die Zahlungen lediglich als Teil der Bankabstimmung anwenden.  

> [!NOTE]  
>  Um Zahlungen mithilfe von SEPA-Lastschrift zu erfassen, muss die Währung der Verkaufsrechnung EURO sein.  

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Bereiten Sie Bankkonto-Formate, Zahlungsmethoden und Kundenvereinbarungen für das Lastschriftverfahren SEPA vor.|[Einrichten von SEPA-Lastschriften](finance-how-to-set-up-sepa-direct-debit.md)|  
|Weisen Sie Ihre Bank an, Zahlungsbeträge von den Bankkonten Ihrer Kunden auf das Konto Ihres Unternehmens gemäß Ihrer SEPA-Lastschrift-Einstellung zu überweisen.|[SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Richten Sie Standarddebitorverkaufscodes für Einzugsrechnungen ein, und generieren Sie Verkaufsrechnungen mit Einzugsinformationen, wenn die Rechnungen zur Zahlung fällig sind.|[Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)|  
|Buchen Sie geleistete Zahlungen als SEPA-Lastschriften.|[SEPA-Lastschrifteinzug-Zahlungseingänge buchen](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Siehe auch  
[Verwalten von Forderungen](receivables-manage-receivables.md)

