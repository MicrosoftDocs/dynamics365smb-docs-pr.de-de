---
title: 'Vorgehensweise: Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen | Microsoft Docs'
description: Wenn Sie Benutzer in Genehmigungsworkflows einrichten, müssen Sie auf den Seiten Benachrichtigung einrichten und Benachrichtigungs-Plan angeben, wie und wann jeder Benutzer Benachrichtigungen über Workflowschritte zur Genehmigung erhält. Einzelne Benutzer können ihre Benachrichtigungseinrichtung über die in jeder Benachrichtigung enthaltene Schaltfläche Benachrichtigungseinstellungen ändern auch ändern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 0e389e74e01d6e846d7f045069190fa1c67884fc
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "912992"
---
# <a name="specify-when-and-how-to-receive-notifications"></a>Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen
Wenn Sie Benutzer in Genehmigungsworkflows einrichten, müssen Sie auf den Seiten **Benachrichtigung einrichten** und **Benachrichtigungs-Plan** angeben, wie und wann jeder Benutzer Benachrichtigungen über Workflowschritte zur Genehmigung erhält. Einzelne Benutzer können ihre Benachrichtigungseinrichtung über die in jeder Benachrichtigung enthaltene Schaltfläche **Benachrichtigungseinstellungen ändern** auch ändern.  

 Bevor Sie Benachrichtigungseinstellungen für einen Genehmigungsbenutzer einrichten können, müssen Sie den Benutzer als Genehmigungsbenutzer einrichten. Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)  

 «»Sie können das Layout von E-Mail-Benachrichtigungen festlegen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail anpassen. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen und bearbeiten Sie ein benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-create-custom-report-layout.md).  

 Mit vielen Workflowschritten zur Genehmigung werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert. Die entsprechende Reaktion ist, dass eine Benachrichtigung an Benutzer 2 (Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis enthalten, dass Benutzer 2 den Datensatz genehmigt. Die entsprechende Reatkion ist, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit ein Prozess mit dem genehmigten Datensatz gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden. Weitere Informationen finden Sie unter [Workflow](across-workflow.md)  

## <a name="specify-when-and-how-users-receive-notifications"></a>Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Genehmigungsbenutzer Einrichtung** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Zeile für den Benutzer aus, für den Sie Benachrichtigungseinstellungen festlegen möchten, und wählen Sie dann die Aktion **Benachrichtigungseinrichtung** aus.  
3.  Füllen Sie auf der Seite **Benachrichtigung einrichten** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Benachrichtigungstyp**|Geben Sie an, auf welche Art von Ereignis sich die Benachrichtigung bezieht.<br /><br /> Wählen Sie eine der folgenden Optionen:<br /><br /> -   **Neuer Datensatz** gibt an, dass sich die Benachrichtigung auf einen neuen Datensatz bezieht, zum Beispiel einen Beleg, auf den der Benutzer reagieren muss.<br />-   **Genehmigung** gibt an, dass sich die Benachrichtigung auf eine oder mehrere Genehmigungsanforderungen bezieht.<br />-   **Fällig** gibt an, dass die Benachrichtigung verwendet wird, um Benutzer daran zu erinnern, dass sie bei der Behandlung eines Ereignisses in Verzug sind.|  
    |**Benachrichtigungsmethode**|Geben Sie an, ob die Benachrichtigung als E-Mail oder als internen Hinweis gesendet wird.|

    «»Sie können das Layout von E-Mail-Benachrichtigungen festlegen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail anpassen. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen und bearbeiten Sie ein benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-create-custom-report-layout.md).

    Sie haben nun festgelegt, wie der Benutzer Benachrichtigungen erhält. Geben Sie nun an, wann der Benutzer Benachrichtigungen empfängt.  

4.  Wählen Sie die Aktion **Benachrichtigungsplan** aus.  
5.  Füllen Sie auf der Seite **Benachrichtigungsplan** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Wiederholung**|Geben Sie das Serienmuster an, nach dem der Benutzer Benachrichtigungen erhält.|  
    |**Zeit**|Gibt an, zu welcher Uhrzeit der Benutzer Benachrichtigungen erhält, wenn der Wert im Feld **Wiederholung** nicht **Sofort** lautet.|  
    |**Tägliche Häufigkeit**|Geben Sie an, an welchen Tagen der Benutzer Benachrichtigungen erhält, wenn im Feld **Wiederholung** der Wert **Täglich** festgelegt ist.<br /><br /> Wählen Sie **Werktag** aus, um an jedem Werktag Benachrichtigungen zu erhalten. Wählen Sie **Täglich** aus, um an jedem Wochentag, einschließlich Wochenenden, Benachrichtigungen zu erhalten.|  
    |**Montag** bis **Sonntag**|Geben Sie an, an welchen Tagen der Benutzer Benachrichtigungen erhält, wenn im Feld **Wiederkehrend** der Wert **Wöchentlich** festgelegt ist.|  
    |**Tag des Monats**|Geben Sie an, dass der Benutzer Benachrichtigungen am ersten oder letzten Tag im Monat oder an einem bestimmten Tag im Monat erhält.|  
    |**Monatliches Benachrichtigungsdatum**|Geben Sie das Datum an, an dem der Benutzer Benachrichtigungen erhält, wenn im Feld **Datum des Monats** der Wert **Benutzerdefiniert** festgelegt ist.|  

## <a name="change-when-and-how-you-receive-notifications"></a>Ändern des Zeitpunkts und der Art des Empfangs von Benachrichtigungen  
1.  Wählen Sie in einer der Benachrichtigungen, die Sie entweder als E-Mail oder Hinweis erhalten haben, die Schaltfläche **Benachrichtigungseinstellungen ändern** aus.  
2.  Ändern Sie auf der Seite **Benachrichtigungseinstellungen** Ihre Benachrichtigungseinstellungen wie im vorigen Verfahren beschrieben.  

## <a name="see-also"></a>Siehe auch  
 [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)   
 [Erstellen und bearbeiten Sie einen benutzerdefinierten Bericht](ui-how-create-custom-report-layout.md)   
 [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)   
 [Einrichten von Workflows](across-set-up-workflows.md)   
 [Verwenden von Workflows](across-use-workflows.md)
