---
title: SEPA Direct Debit einrichten | Microsoft Docs
description: Erfahren Sie, wie Sie SEPA Abbuchung in Dynamics 365 for Financials einrichten.
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
ms.openlocfilehash: a5f7a99a3e6bfd9c0146d87af4e3869cda381a67
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-sepa-direct-debit"></a>Vorgehensweise: Einrichten von SEPA-Lastschriften
Im Fenster **Lastschriften**  können Sie Anweisungen in Ihre elektronische Bank exportieren, um eine Lastschrift vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.  

Um das Exportieren von Bankdateiformaten zu aktivieren, die nicht durch die allgemeine oder lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt werden, können Sie eine Datenaustauschdefinition einrichten, indem Sie das  Datenaustauschframework verwenden. Für weitere Informationen, siehe [Gewusst wie: Einrichten des Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

Bevor Sie Debitorenzahlungen elektronisch durch den Export von Lastschriften im SEPA-Lastschriftformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:  

* Richten Sie zunächst das Exportformat der Bankdatei ein, wodurch Ihre Bank beauftragt wird, eine Lastschrift vom Bankkonto des Debitors auf Ihr Bankkonto durchzuführen.  
* Richten Sie die Zahlungsmethode des Debitors ein.  
* Richten Sie das Lastschriftmandat ein, das Ihrer Übereinkunft mit dem Debitor zum Einzug seiner Zahlungen in einem bestimmten Zeitraum entspricht.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Einrichten Ihres Bankkontos für die SEPA-Lastschrift  
1. Geben Sie im Feld **Suchen** **Bankkonten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das Konto, das Sie für das Lastschriftverfahren verwenden möchten.  
3. Wählen Sie im Inforegister **Umlagerung**, im Feld **SEPA-Lastschrift Exportformat** SEPA Lastschrift.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Einrichten der Zahlungsmethode des Debitors für die SEPA-Lastschrift  
1. Geben Sie im Feld **Suchen** einen Wert für **Zahlungsformen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Richten Sie eine Zahlungsmethode ein. Füllen Sie die auf den Lastschrifteinzug bezüglichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|[Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Lastschrift**|Geben Sie an, ob die Zahlungsmethode für den SEPA-Lastschrifteinzug gilt.|  
    |**Zahlungsbedingungscode Lastschrift**|Geben Sie die Zahlungsbedingungen an, wie etwa NICHT ZAHLEN, die auf Verkaufsrechnungen angezeigt werden, die per SEPA-Lastschrift bezahlt werden, um den Debitor darauf hinzuweisen, dass die Zahlung automatisch eingezogen wird. Als Alternative können Sie das Feld leer lassen.|  

    > [!NOTE]  
    >  Geben Sie hier keinen Wert in **Bal. Kontonr.** ein  

4. Wählen Sie die Schaltfläche **OK** aus, um das Fenster **Genehmigungskommentare** zu schließen.  
5. Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
6. Öffnen Sie die Debitorenkarte für den Debitor, der für die SEPA-Lastschriften eingerichtet werden soll.  
7. Wählen Sie das Feld , und wählen Sie dann den **Zahlungsformcode**, den Sie in Schritt 3 angegeben haben.  
8. Wiederholen Sie die Schritte 6 und 7 für alle Debitoren, die Sie für SEPA-Lastschriften einrichten wollen.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Einrichten des Lastschrift-Mandats, entsprechend der Vereinbarung mit dem Debitor  
1. Geben Sie im Feld **Suchen** **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte für den Debitor, der für die SEPA-Lastschriften eingerichtet werden soll.  
3. Wählen Sie die **Bankkonten** Aktion aus.  
4. Wählen Sie im Feld **Debitor-Bankkontenübersicht** das Debitorenbankkonto, das Lastschriften verwenden wird, und wählen Sie dann auf der Registerkarte **Start**, in der Gruppe **Prozess**, **Lastschrift-Mandat**.  
5. Füllen Sie im Fenster Liste der notwendigen **SEPA-Felder** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |[Feld|Beschreibung]|  
    |---------------------------------|---------------------------------------|  
    |**Debitor Bankkontocode**|Gibt das Bankkonto an, aus dem Lastschrifteinzüge abgebucht werden. Dieses Feld wird automatisch ausgefüllt.|  
    |**Gültig ab**|Geben Sie das Datum an, an dem das Lastschrift-Mandat beginnt.|  
    |**Gültig bis**|Geben Sie das Datum an, an dem das Lastschrift-Mandat endet.|  
    |**Datum der Unterschrift**|Geben Sie das Datum an, an dem der Kunde das Lastschrift-Mandat unterzeichnet hat.|  
    |**Zahlungstyp**|Geben Sie an, ob die Übereinkunft mehrere (**Wiederkehrende**) oder einen einzelnen (**Einmalig**) Lastschrifteinzug abdeckt.|  
    |**Erwartete Anzahl Sollbeträge**|Geben Sie an, wie viele Lastschrifteinzüge Sie zu tätigen erwarten. Dieses Feld ist nur relevant, wenn Sie **Wiederkehrend** im Feld **Sequenzart**ausgewählt haben.|  
    |**Sollzähler**|Gibt an, wie viele Lastschrift-Einzüge mit diesem Lastschrift-Mandat durchgeführt wurden. Dieses Feld wird automatisch aktualisiert.|  
    |**Gesperrt**|Geben Sie an, dass Lastschrifteinzüge mit diesem Lastschrift-Mandat nicht durchgeführt werden können.|  

6.  Wiederholen Sie die Schritte 1 bis 5 für alle Debitoren, die für die SEPA-Lastschriften eingerichtet werden sollen.  

 Das Lastschrift-Mandat wird automatisch in das Feld **Lastschrift-Mandat-ID** eingegeben, wenn Sie eine Verkaufsrechnung für den Debitor erstellen, den Sie in Schritt 2 ausgewählt haben. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Siehe auch  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Vorgehensweise: Datenaustauschdefinitionen einrichten](across-how-to-set-up-data-exchange-definitions.md)
[Vorgehensweise: Wiederkehrende Verkaufs- und Einkaufszeilen einrichten](sales-how-work-standard-lines.md)
[Datenaustausch als elektronische Belege](across-data-exchange.md)

