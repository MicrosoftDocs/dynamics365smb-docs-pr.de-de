---
title: Einrichten von Mahnmethoden, Bestimmungen und Mahntext
description: Lernen Sie, wie Business Central eingerichtet wird, so dass Sie eine Mahnung an einen Debitoren wegen einer fälligen Zahlung senden können und wie der Zahlung wegen des Verzugs Zuschläge oder Gebühren hinzugefügt werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: 1bef0a7598846f0ea3fe74b03bbef70bb5c940ef
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035381"
---
# <a name="set-up-reminder-terms-and-levels"></a>Einrichten von Mahnmethoden, Bestimmungen und Mahntext

Mithilfe von Mahnungen können Debitoren auf überfällige Beträge aufmerksam gemacht werden. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a>Mahnbestimmungen

Bei Debitoren mit überfälligen Zahlungen muss entschieden werden, wann und auf welche Weise eine Mahnung gesendet wird. Darüber hinaus können ggf. Gebühren oder Zinsen erhoben werden. Sie können eine beliebige Anzahl an Lieferanmahnungsmethoden einrichten.  

> [!NOTE]
> Wenn Sie Zinsen auf überfällige Zahlungen berechnen möchten, können Sie das auch bei der Mahnungserstellung. Möchten Sie die Zinsen dagegen nur berechnen und Ihre Debitoren darüber in Kenntnis setzen, ohne eine Mahnung zu senden, sollten Sie [Zinsrechnungen](finance-setup-finance-charges.md) verwenden. Weitere Informationen finden Sie unter [Erinnerungen](receivables-collect-outstanding-balances.md#reminders) oder [Finanzierungskosten](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="to-set-up-reminder-terms"></a>So richten Sie Mahnmethoden ein:

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun") Symbol öffnet, geben Sie **Mahnmethoden** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

## <a name="reminder-levels"></a>Mahnstufen

Für jeden Lieferanmahnungsmethodencode können beliebig viele Lieferanmahnungsstufen definiert werden. Bei der ersten Erstellung einer Mahnung für einen Debitor werden die Einstellungen der Stufe 1 verwendet. Beim Registrieren der Mahnung wird die Stufennummer in den erstellten Mahnposten erfasst und mit den jeweiligen Debitorenposten verknüpft. Ist eine erneute Mahnung erforderlich, werden alle Mahnposten überprüft, die mit offenen Debitorenposten verknüpft sind, um die höchste Stufennummer zu ermitteln. In der neuen Mahnung werden dann die Bedingungen für die nächsthöhere Stufennummer verwendet.

Werden mehr Mahnungen erstellt als definierte Stufen vorhanden sind, werden die Bedingungen der höchsten Stufe verwendet. Die Anzahl der erstellbaren Mahnungen wird in den Mahnmethoden durch das Feld **Max. Anzahl Mahnungen** begrenzt.

### <a name="to-set-up-reminder-levels"></a>So richten Sie Mahnstufen ein:

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun") Symbol öffnet, geben Sie **Mahnmethoden** ein und wählen Sie dann den entsprechenden Link.  
2. Klicken Sie auf der Seite **Mahnmethoden** in die Zeile mit der Methode, für die Sie Stufen anlegen möchten, und wählen Sie dann die Aktion **Stufen**.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Die Einstellung des Felds **Zinsen berechnen** legt fest, ob bei der Erinnerung Zinsen für die Erinnerung angezeigt werden. Das Feld **Zinsen buchen** auf der Seite **Erinnerungsbestimmungen** bestimmen, ob die berechneten Zinsen auf Sachkonten und Debitorenkonten gebucht werden müssen.
    >
    > Um anzuzeigen, dass Zinsen berechnet werden sollen, wählen Sie das Feld **Zinsen berechnen**.

    Geben Sie optional für jede Erinnerungsstufe zusätzliche Gebühren sowohl in MW als auch in Fremdwährung an. Sie können mehrere Gebühren in Fremdwährungen für jeden Code auf der Seite **Mahnstufen** einrichten.  

    Die zusätzlichen Gebühren können auf drei verschiedene Arten berechnet werden, die durch den Wert des Feld **Hinzufügen. Gebührenberechnungsart** definiert werden.  

    - **Fixiert**

        Die Gebühren werden auf der Grundlage der Werte der Felder **Zusätzliche Gebühr** in der Zeile für die Erinnerungsebene selbst berechnet.  
    - **Single Dynamic**

        Die Gebühren werden auf der Grundlage der Werte der Felder **Zusätzliche Gebühr einrichten** in der Zeile für die Erinnerungsebene selbst berechnet.
    - **Akkumulierte Dynamik**

        Die Gebühren werden auf der Grundlage der Werte der Felder **Zusätzliche Gebühr einrichten** in der kombinierten Zeile für die Erinnerungsebene selbst berechnet.

4. Wählen Sie die Aktion **Währungen** aus.
5. Auf der Seite **Währungen für Mahnstufen festlegen** können Sie für jeden Mahnstufencode und die dazugehörende Mahnstufe Fremdwährungsinformationen hinterlegen, die aus einem Währungscode und einer Gebühr bestehen.

    > [!NOTE]  
    > Wenn Sie Mahnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um Mahnungen zu erstellen. Falls keine Mahnkonditionen für Fremdwährungen eingerichtet wurden, verwendet die Anwendung die Mahnkonditionen für die Mandantenwährung auf der Seite **Mahnstufe** und rechnet diese in die entsprechende Währung um.

    Jede Mahnstufe kann mit Text versehen werden, der entweder vor (**Vortext**) oder nach (**Nachtext**) den Mahnposten gedruckt wird.

6. Wählen Sie die Aktionen **Anfangstext** oder **Endtext** entsprechend aus und füllen Sie die Seite **Mahntext** aus.
7. Um zugehörige Werte in das resultierende Mahntext automatisch einzusetzen, geben -Sie die folgenden Platzhaltern im Feld **Text** Feld ein.  

    |Platzhalter|Wert|  
    |-----------------|-----------|  
    |%1|Inhalt des Felds **Belegdatum** des Mahnungskopfs|  
    |%2|Inhalt des Felds **Fälligkeitsdatum** des Mahnungskopfs|  
    |%3|Inhalt des Felds **Zinssatz** im verknüpften Zinskonditionen|  
    |%4|Inhalt des Felds **Restbetrag** des Mahnungskopfs|  
    |%5|Inhalt des Felds **Zinsbetrag** des Mahnungskopfs|  
    |%6|Inhalt des Felds **Zusatzgebühr** des Mahnungskopfs|  
    |%7|Der Gesamtbetrag der Mahnung|  
    |%8|Inhalt des Felds **Mahnstufe** des Mahnungskopfs|  
    |%9|Inhalt des Felds **Währungscode** des Mahnungskopfs|  
    |%10|Inhalt des Felds **Buchungsdatum** des Mahnungskopfs|  
    |%11|Der Unternehmensname.|  
    |%12|Inhalt des Felds **Zusatzgebühr pro Zeile** des Mahnungskopfs|  

    Wenn Sie beispielsweise schreiben **%9 %7 fällig am %2.**, dann enthält die Mahnung den folgenden Text: **Sie schulden 1.200,50 MW, fällig am 02-02-2014**.

    > [!NOTE]
    > Das Fälligkeitsdatum wird entsprechend der von Ihnen eingegebenen Datumsformel berechnet. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).

Geben Sie nach der Einrichtung der Mahnmethoden (mit zusätzlichen Stufen und Text) auf jeder Debitorenkarte einen der Codes ein. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Siehe auch

[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Zinskonditionen einrichten](finance-setup-finance-charges.md)  
[Finanzen einrichten](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]