---
title: Legen Sie fest, wann und wie Sie Workflow-Benachrichtigungen erhalten möchten
description: Wenn Sie Benutzer in Workflows für Genehmigungen festlegen, können Sie angeben, wie und wann jeder Genehmigungsbenutzer benachrichtigt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 6812fa270066b03fa64a7d8c664ef4df8d28eff0
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102499"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Legen Sie fest, wann und wie Sie Workflow-Benachrichtigungen erhalten möchten
Wenn Sie Genehmigungsbenutzer in Workflows festlegen, in denen jemand Änderungen genehmigen soll, z.B. wenn neue Datensätze erstellt werden oder wenn jemand eine Genehmigung beantragt, müssen Sie angeben, wie und wann der Genehmigungsbenutzer benachrichtigt werden soll. Sie können z.B. festlegen, dass ein Genehmigter sofort eine E-Mail erhält, wenn jemand einen neuen Debitor erstellt. Alternativ können Sie die Zustellung der Benachrichtigungen auch planen, z.B. auf wöchentlicher oder monatlicher Basis.

Sie können auch Ihre Benachrichtigungseinstellungen ändern, indem Sie die Schaltfläche **Benachrichtigungseinstellungen ändern** auf einer beliebigen Benachrichtigung wählen.  

> [!NOTE]
> Benachrichtigungen werden gemäß den Benachrichtigungseinstellungen des Empfängers und nicht des Absenders zugestellt. Dies ist eine wichtige Unterscheidung, da sie bedeutet, dass wenn jemand eine Genehmigung als Teil eines Workflows anfordert, ihre Genehmigung nicht notwendigerweise sofort gesendet wird. Stattdessen wird sie gemäß dem Benachrichtigungszeitplan bereitgestellt, der in den Benachrichtigungseinstellungen des Genehmigers angegeben ist. 

Bevor Sie Benachrichtigungseinstellungen für einen Genehmigungsbenutzer einrichten können, müssen Sie den Benutzer als Genehmigungsbenutzer einrichten. Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md).  

«»Sie können das Layout von E-Mail-Benachrichtigungen festlegen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail anpassen. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).  

> [!NOTE]
> Wenn Sie E-Mail als Benachrichtigungsmethode verwenden möchten, müssen Sie E-Mail sowohl für den Absender als auch für den Empfänger in [!INCLUDE [prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Schritte in Workflows 
Mit vielen Workflowschritten zur Genehmigung werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert. Die entsprechende Reaktion ist, dass eine Benachrichtigung an Benutzer 2 (Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis enthalten, dass Benutzer 2 den Datensatz genehmigt. Die entsprechende Reatkion ist, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit ein Prozess mit dem genehmigten Datensatz gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden. Weitere Informationen finden Sie unter [Workflow](across-workflow.md)  

## <a name="specify-when-and-how-users-receive-notifications"></a>Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Genehmigungsbenutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Zeile für den Benutzer aus, für den Sie Benachrichtigungseinstellungen festlegen möchten, und wählen Sie dann die Aktion **Benachrichtigungseinrichtung** aus.  
3.  Füllen Sie auf der Seite **Benachrichtigung einrichten** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    > [!NOTE]
    > Wenn Sie die Seite **Benachrichtigungseinrichtung** von der Seite **Genehmigungsbenutzereinrichtung** aus öffnen, ist die Einrichtung der Benachrichtigung mit dem Genehmigungsbenutzer verknüpft. Der Genehmiger erhält immer Workflow-Benachrichtigungen entsprechend der Einrichtung dieser Benachrichtigung. Wenn Sie mit Tell Me die Seite **Einrichtung von Benachrichtigungen** öffnen, gilt die Einrichtung von Benachrichtigungen für alle Benutzer.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Benachrichtigungstyp**|Geben Sie an, auf welche Art von Ereignis sich die Benachrichtigung bezieht.<br /><br /> Wählen Sie eine der folgenden Optionen:<br /><br /> -   **Neuer Datensatz** gibt an, dass sich die Benachrichtigung auf einen neuen Datensatz bezieht, zum Beispiel einen Beleg, auf den der Benutzer reagieren muss.<br />-   **Genehmigung** gibt an, dass sich die Benachrichtigung auf eine oder mehrere Genehmigungsanforderungen bezieht.<br />-   **Fällig** gibt an, dass die Benachrichtigung verwendet wird, um Benutzer daran zu erinnern, dass sie bei der Behandlung eines Ereignisses in Verzug sind.|  
    |**Benachrichtigungsmethode**|Geben Sie an, ob die Benachrichtigung als E-Mail oder als internen Hinweis gesendet wird.|

    Sie können das Layout von E-Mail-Benachrichtigungen festlegen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail anpassen. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

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
 [Erstellen und bearbeiten von benutzerdefinierten Berichtslayouts](ui-how-create-custom-report-layout.md)   
 [Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)   
 [Einrichten von Workflows](across-set-up-workflows.md)   
 [Verwenden von Workflows](across-use-workflows.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]