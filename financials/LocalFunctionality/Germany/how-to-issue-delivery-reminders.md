---
title: 'Gewusst wie: Lieferbenachrichtigungen ausstellen'
description: "Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können. Vor dem Ausstellen von Lieferbenachrichtigungen können Sie einen Testbericht drucken."
services: project-madeira
documentationcenter: 
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
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: b5a6e59cddd7ac1d22af73f40cd83f2a4a9860d9
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="issue-delivery-reminders"></a>Lieferbenachrichtigung registrieren
Nachdem Sie Lieferbenachrichtigungen erstellt haben, müssen Sie sie registrieren und ausdrucken, sodass Sie Mahnungen an Kreditoren verschicken können. Vor dem Ausstellen von Lieferbenachrichtigungen können Sie einen Testbericht drucken. Weitere Informationen finden Sie unter [Vorgehensweise: Drucken von Testberichten für  Lieferbenachrichtigungen](how-to-print-test-reports-for-delivery-reminders.md).  

Beim Registrieren der Lieferantenbenachrichtigungen erzeugt die Anwendung Lieferantenbenachrichtigungsposten. Die erstellten Posten können Sie dann im Fenster **Registrierten Lieferbenachrichtigungskopfes** anzeigen.  

## <a name="to-issue-delivery-reminders"></a>So registrieren Sie Lieferbenachrichtigungen  

1.  Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben **Lieferbenachrichtigungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Im Fenster **Lieferbenachrichtigungen** wählen Sie die Lieferbenachrichtigungen aus, die Sie registrieren möchten, und wählen die **Bearbeiten** Aktion aus.  
3.  Wählen Sie die Aktion **Ausgeben** aus.  
4.  Füllen Sie im Fenster **Lieferbenachrichtigung** im Inforegister **Option** die erforderlichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Drucken**|Wählen Sie diese Option aus, um die Lieferbenachrichtigungen zu drucken, wenn sie registriert werden.|  
    |**Buchungsdatum ersetzen**|Wählen Sie diese Option aus, um das vorhandene Buchungsdatum für die Lieferbenachrichtigungen zu ersetzen.|  
    |**Buchungsdatum**|Gibt das Buchungsdatum der Lieferbenachrichtigung an.<br /><br /> Dieses Buchungsdatum wird für alle Lieferbenachrichtigungen verwendet, wenn Sie das Kontrollkästchen **Buchungsdatum ersetzen** aktiviert haben. Wenn das Kontrollkästchen **Buchungsdatum ersetzen** deaktiviert ist, wird dieses Datum nur für diejenigen Lieferbenachrichtigungen verwendet, für die kein Buchungsdatum verfügbar ist.|  

5.  Optional wählen Sie im Inforegister **Lieferbenachrichtigungen Kopfzeile** die entsprechenden Filter aus.  

    > [!NOTE]  
    >  Sie können Filter entfernen und allen Lieferbenachrichtigungen gleichzeitig registrieren.  

6.  Wählen Sie die Schaltfläche **OK** aus.  

Sie können das Fenster registrierte Mahnungen anzeigen im Fenster **Registrierte Lieferbenachrichtigungen**. Optional können Sie jetzt eine Lieferbenachrichtigung drucken.  

## <a name="to-view-delivery-reminder-ledger-entries"></a>Um sich detaillierte Lieferbenachrichtigungen anzeigen zu lassen:  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Aufträge** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Bestellung, für die Sie den Mahnungsstatus anzeigen möchten, und wählen die Aktion **Bearbeiten**.  
3.  Wählen Sie die Aktion **Lieferbenachrichtigungs-Einträge** aus.  

Im registrierten Lieferbenachrichtigungskopf-Fenster, können Sie die Lieferbenachrichtigungsposten der ausgewählten Bestellung anzeigen.  

## <a name="see-also"></a>Siehe auch  
 [Lieferbenachrichtigungen](delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md)

