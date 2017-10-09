---
title: SEPA Direct Debit in Dynamics 365 | Microsoft Docs
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d9f60bfb92336227e85b0476a856bcc1173c71cd
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="collect-payments-with-sepa-direct-debit"></a>Erfassen von Zahlungen per Lastschriftverfahren SEPA
Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden gemäß dem SEPA-Format einziehen.  

 Richten Sie zuerst das Exportformat der Bankdatei ein, die Ihrer Bank aufträgt, eine Lastschrift durchführen. Richten Sie dann die Zahlungsmethode des Debitors ein. Richten Sie schließlich das Lastschrift-Mandat ein, die Ihrer Übereinkunft mit dem Kunden zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

 Um die Bank anzuweisen, den Zahlungsbetrag vom Bankkonto des Debitors auf das Bankkonto Ihres Unternehmens zu überweisen, erstellen Sie einen Lastschrifteinzugposten mit Informationen zu Bankkonten, den betroffenen Verkaufsrechnungen und dem Lastschrift-Mandat. Anschließend exportieren Sie eine XML-Datei, die auf dem Einzugseintrag basiert, und senden Sie zur Verarbeitung an Ihre Bank. Alle Zahlungen, die nicht verarbeitet werden konnten, werden Ihnen von Ihrer Bank mitgeteilt, und Sie müssen dann die jeweiligen Lastschrifteinzugsposten manuell ablehnen.  

 Sie können Standarddebitorverkaufscodes mit Informationen zum Lastschrifteinzug und zu Einzugsermächtigungen einrichten. Anschließend können Sie mit der **Standard-Debitorenrechnung erstellen**-Stapelverarbeitung mehrere Verkaufsrechnungen erstellen, die bereits vorab die Einzugsinformationen enthalten. Dies kann manuell oder automatisch durchgeführt werden, je nach dem Zahlungsfälligkeitsdatum.  

 Wenn Ihre Bank Ihnen mitteilt, dass Zahlungen erfolgreich verarbeitet wurden, können Sie die Zahlungseingänge direkt aus dem Fenster **Lastschriftenposten** buchen, oder indem Sie die Zahlungszeilen in das Buch verschieben, in dem Sie Zahlungseingänge buchen, etwa das Fenster **Zahlungseingangs Buch.-Blatt**. Je nach Ihrem Cash-Management-Prozess können Sie auch warten und die Zahlungen lediglich als Teil der Bankabstimmung anwenden.  

> [!NOTE]  
>  Um Zahlungen mithilfe von SEPA-Lastschrift zu erfassen, muss die Währung der Verkaufsrechnung EURO sein.  

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Bereiten Sie Bankkonto-Formate, Zahlungsmethoden und Kundenvereinbarungen für das Lastschriftverfahren SEPA vor.|[Vorgehensweise: Einrichten von SEPA-Lastschriften](finance-how-to-set-up-sepa-direct-debit.md)|  
|Weisen Sie Ihre Bank an, Zahlungsbeträge von den Bankkonten Ihrer Kunden auf das Konto Ihres Unternehmens gemäß Ihrer SEPA-Lastschrift-Einstellung zu überweisen.|[Vorgehensweise: SEPA-Lastschrifteinzugsposten erstellen und in eine Bankdatei exportieren](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Richten Sie Standarddebitorverkaufscodes für Einzugsrechnungen ein, und generieren Sie Verkaufsrechnungen mit Einzugsinformationen, wenn die Rechnungen zur Zahlung fällig sind.|[Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)|  
|Buchen Sie geleistete Zahlungen als SEPA-Lastschriften.|[Vorgehensweise: SEPA-Lastschrifteinzug-Zahlungseingänge buchen](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Siehe auch  
[Verwalten von Forderungen](receivables-manage-receivables.md)

