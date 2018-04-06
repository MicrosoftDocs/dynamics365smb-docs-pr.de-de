---
title: 'Gewusst wie: Lieferbenachrichtigungen manuell erstellen'
description: "Mahnt Ihre Debitoren wegen überfälliger Lieferung."
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
ms.openlocfilehash: 58c1bfc1d5922a0274eca74d31e3365727eac1e4
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
<<<<<<< HEAD:financials/LocalFunctionality/Germany/how-to-create-delivery-reminders-manually.md
# <a name="create-delivery-reminders-manually"></a>So erstellen Sie Lieferanmahnungen manuell
<a name="in-included365finincludesd365finmdmd-you-can-create-delivery-reminders-when-a-purchase-has-not-been-delivered-as-expected-you-can-create-a-single-delivery-reminder-manually-or-you-can-generate-delivery-reminders-for-all-overdue-deliveries-for-more-information-see-generate-delivery-remindershow-to-generate-delivery-remindersmd"></a>In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde. Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen. Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-generate-delivery-reminders.md).
=======
# <a name="create-delivery-reminders-manually"></a>So erstellen Sie Lieferanmahnungen manuell
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], können Sie Lieferbenachrichtigungen erstellen, wenn eine Bestellung nicht wie erwartet geliefert wurde. Sie können eine einzelne Lieferbenachrichtigung manuell erstellen oder Sie können Lieferbenachrichtigungen für alle überfälligen Lieferungen erstellen. Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-generate-delivery-reminders.md).
>>>>>>> refs/remotes/origin/Update13:archive/LocalFunctionality/Germany/how-to-create-delivery-reminders-manually.md

> [!NOTE]
> Um Lieferanmahnungen zu erstellen, müssen Sie die Lieferanmahnungseigenschaften einrichten. Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-set-up-delivery-reminders.md).

## <a name="to-create-a-delivery-reminder-manually"></a>So erstellen Sie Lieferantenbenachrichtigungen manuell  

1.  Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben **Lieferbenachrichtigungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie im Fenster **Lieferbenachrichtigung** im Inforegister **Allgemein** die erforderlichen Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Die eindeutige Kennnummer für die Lieferbenachrichtigung.|  
    |**Kreditorennr**|Gibt die Nummer des Kreditors an, für den Sie eine Lieferbenachrichtigung buchen möchten.<br /><br /> Wenn Sie die Kreditorennummer auswählen, werden **Name**, **Adresse**, **PLZ Code/Ort** und **Kontakt** Felder automatisch ausgefüllt.|  
    |**Buchungsdatum**|Gibt das Buchungsdatum der Lieferbenachrichtigung an. Dieses Datum wird in alle Lieferbenachrichtigung kopiert.|  
    |**Belegdatum**|Gibt das Dokumentdatum der Lieferbenachrichtigung an. Dieses Datum wird auch verwendet, um das Fälligkeitsdatum der Lieferbenachrichtigung zu bestimmen. Sie können das Buchungsdatum bei Bedarf ändern.|  
    |**Mahnstufe**|Lieferbenachrichtigungsstufe. Dieser Wert basiert auf der Anzahl von Lieferbenachrichtigung, die bereits gesendet wurden. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).|  
    |**Mahnmethodencode**|Gibt den Lieferbenachrichtigungscode für den Kreditor an.|  
    |**Fälligkeitsdatum**|Gibt das Fälligkeitsdatum der Lieferbenachrichtigung an.|  

4.  Wählen Sie die Aktion **Mahnungszeile vorschlagen**.  

    Wenn es überfällige Lieferungen vom angegebenen Kreditor gibt, werden diese der Lieferbenachrichtigung hinzugefügt.  

5.  Wählen Sie die Schaltfläche **OK** aus.  

    Lieferbenachrichtigung wurde erstellt. So können die Lieferbenachrichtigungen ausgeben und erstellen.  

## <a name="see-also"></a>Siehe auch  
 [Lieferbenachrichtigungen](delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md)   
 [Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md)   
 [Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md)   
 [So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen](how-to-print-test-reports-for-delivery-reminders.md)

