---
title: Legen Sie fest, wann und wie Sie Workflow-Benachrichtigungen erhalten möchten
description: Wenn Sie Benutzer in Workflows für Genehmigungen einrichten, können Sie angeben, wie und wann jeder Genehmigungsbenutzer benachrichtigt wird.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 663, 1500, 1512, 1513,
ms.date: 09/09/2022
ms.author: bholtorf
ms.openlocfilehash: 74387ee5cb8581d8b8e1cce5c1d1c8850cd6c842
ms.sourcegitcommit: 9bba11d474e21711cc8e2afefee8efb473170707
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9763262"
---
# <a name="specify-when-and-how-to-receive-workflow-notifications"></a>Legen Sie fest, wann und wie Sie Workflow-Benachrichtigungen erhalten möchten

Wenn Sie Genehmigungsbenutzer in Workflows festlegen, in denen jemand Änderungen genehmigen soll, z. B. wenn neue Datensätze erstellt werden oder wenn jemand eine Genehmigung anfordert, müssen Sie angeben, wie und wann der Genehmigungsbenutzer benachrichtigt werden soll. Sie können z.B. festlegen, dass ein Genehmigter sofort eine E-Mail erhält, wenn jemand einen neuen Debitor erstellt. Alternativ können Sie die Zustellung der Benachrichtigungen auch so planen, dass sie zurückgehalten und zusammen zugestellt werden, z.B. auf wöchentlicher oder monatlicher Basis.

Sie können auch Ihre Benachrichtigungseinstellungen ändern, indem Sie **Benachrichtigungseinstellungen ändern** auf einer beliebigen Benachrichtigung wählen.  

> [!NOTE]
> Benachrichtigungen werden gemäß den Benachrichtigungseinstellungen des Empfängers und nicht des Absenders zugestellt. Dies ist eine wichtige Unterscheidung, da sie bedeutet, dass wenn jemand eine Genehmigung als Teil eines Workflows anfordert, ihre Genehmigung nicht notwendigerweise sofort gesendet wird. Stattdessen wird sie gemäß dem Benachrichtigungszeitplan bereitgestellt, der in den Benachrichtigungseinstellungen des Genehmigers angegeben ist.

Bevor Sie Benachrichtigungseinstellungen für einen Genehmigungsbenutzer einrichten können, müssen Sie den Benutzer als Genehmigungsbenutzer einrichten. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md).  

> [!NOTE]
> Wenn Sie E-Mail als Benachrichtigungsmethode verwenden möchten, müssen Sie E-Mail sowohl für den Absender als auch für den Empfänger in [!INCLUDE [prod_short](includes/prod_short.md)] einrichten. Erfahren Sie mehr unter [E-Mail einrichten](admin-how-setup-email.md).

## <a name="steps-in-workflows"></a>Schritte in Workflows

Mit vielen Workflowschritten zur Genehmigung werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert. Die entsprechende Reaktion ist, dass eine Benachrichtigung an Benutzer 2 (Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis enthalten, dass Benutzer 2 den Datensatz genehmigt. Die entsprechende Reatkion ist, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit ein Prozess mit dem genehmigten Datensatz gestartet wird. Für Workflowschritte, die Genehmigungen umfassen, ist jede Benachrichtigung an einen Genehmigungsposten gebunden. Erfahren Sie mehr unter [Workflow](across-workflow.md).  

## <a name="specify-when-and-how-approval-users-receive-notifications"></a>Angeben des Zeitpunkts und wie Genehmigungsbenutzer Benachrichtigungen empfangen  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Genehmigungsbenutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Zeile für den Benutzer aus, für den Sie Benachrichtigungseinstellungen festlegen möchten, und wählen Sie dann die Aktion **Benachrichtigungseinrichtung** aus.  
3. Füllen Sie auf der Seite **Workflow-Benachrichtigungseinrichtung** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

   > [!NOTE]
   > Wenn Sie die Seite **Workflow-Benachrichtigungseinrichtung** von der Seite **Genehmigungsbenutzereinrichtung** aus öffnen, ist die Einrichtung der Benachrichtigung mit dem Genehmigungsbenutzer verknüpft. Der Genehmiger erhält immer Workflow-Benachrichtigungen entsprechend der Einrichtung dieser Benachrichtigung. Wenn Sie mit der *Tell Me*-Funktion die Seite **Workflow-Benachrichtigungseinrichtung** öffnen, gilt die Einrichtung von Benachrichtigungen für alle Benutzer.

   |Feld|Description|
   |-----|-----------|
   |**Benachrichtigungstyp**|Geben Sie an, auf welche Art von Ereignis sich die Benachrichtigung bezieht.<br /><br /> Wählen Sie eine der folgenden Optionen:<br /><br /> -   **Neuer Datensatz** gibt an, dass sich die Benachrichtigung auf einen neuen Datensatz bezieht, zum Beispiel einen Beleg, auf den der Benutzer reagieren muss.<br />-   **Genehmigung** gibt an, dass sich die Benachrichtigung auf eine oder mehrere Genehmigungsanforderungen bezieht.<br />-   **Überfällig** gibt an, dass die Benachrichtigung verwendet wird, um Benutzer daran zu erinnern, dass sie bei der Behandlung eines Ereignisses in Verzug sind.|
   |**Benachrichtigungsmethode**|Geben Sie an, ob die Benachrichtigung als E-Mail oder als internen Hinweis gesendet wird.|

   Sie können das Layout von E-Mail-Benachrichtigungen festlegen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail anpassen. Weitere Informationen erhalten Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

   Sie haben nun festgelegt, wie der Benutzer Benachrichtigungen erhält. Geben Sie nun an, wann der Benutzer Benachrichtigungen empfängt.  
4. Wählen Sie die Aktion **Benachrichtigungsplan** aus.  
5. Füllen Sie auf der Seite **Benachrichtigungsplan** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

   |Feld|Description|
   |-----|-----------|
   |**Wiederholung**|Geben Sie das Serienmuster an, nach dem die Benachrichtigungen an den Benutzer gesendet werden.|
   |**Zeit**|Gibt an, zu welcher Uhrzeit Benachrichtigungen an den Benutzer gesendet werden, wenn der Wert im Feld **Wiederholung** nicht **Sofort** lautet.|
   |**Tägliche Häufigkeit**|Geben Sie an, an welchen Tagen der Benutzer Benachrichtigungen erhält, wenn im Feld **Wiederholung** der Wert **Täglich** festgelegt ist.<br /><br /> Wählen Sie **Werktag** aus, um an jedem Werktag Benachrichtigungen zu erhalten. Wählen Sie **Täglich** aus, um an jedem Wochentag, einschließlich Wochenenden, Benachrichtigungen zu erhalten.|
   |**Montag** bis **Sonntag**|Geben Sie an, an welchen Tagen der Benutzer Benachrichtigungen erhält, wenn im Feld **Wiederkehrend** der Wert **Wöchentlich** festgelegt ist.|
   |**Tag des Monats**|Geben Sie an, dass der Benutzer Benachrichtigungen am ersten oder letzten Tag im Monat oder an einem bestimmten Tag im Monat erhält.|
   |**Monatliches Benachrichtigungsdatum**|Geben Sie das Datum an, an dem der Benutzer Benachrichtigungen erhält, wenn im Feld **Datum des Monats** der Wert **Benutzerdefiniert** festgelegt ist.|

## <a name="change-when-and-how-you-receive-notifications"></a>Ändern des Zeitpunkts und der Art des Empfangs von Benachrichtigungen

1. Wählen Sie in einer der Benachrichtigungen, die Sie entweder als E-Mail oder Hinweis erhalten haben, **Benachrichtigungseinstellungen ändern** aus.  
2. Ändern Sie auf der Seite **Workflow-Benachrichtigungseinrichtung** Ihre Benachrichtigungseinstellungen wie in den Schritten 3-5 beschrieben.
   1. Bestätigen Sie, dass die richtige Benachrichtigung unter **Benachrichtigungstyp** ausgewählt ist.
   2. Wählen Sie unten aus, ob Sie eine E-Mail- oder Notizbenachrichtigung erhalten möchten unter dem Feld **Benachrichtigungsmethode**.
   3. Wählen Sie **Benachrichtigungsplan** aus, um die Häufigkeit und Wiederholung zu ändern, in der Benachrichtigungen gesendet werden.

## <a name="see-also"></a>Siehe auch

[Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Einrichten von Genehmigungs-Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
