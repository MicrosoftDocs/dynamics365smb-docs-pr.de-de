---
title: Zinskonditionen einrichten
description: 'Erfahren Sie, wie Sie Business Central einrichten, damit Sie Debitoren über zusätzliche Gebühren informieren können, indem Sie Memos zu Finanzierungskosten senden.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-finance-charge-terms"></a>Zinskonditionen einrichten

Hat ein Debitor nicht bis zum Fälligkeitsdatum gezahlt, können automatisch Zuschläge berechnet und zu den überfälligen Beträgen auf dem Debitorkonto addiert werden. Verwenden Sie Zinsrechnungen, um Debitoren über die Zuschläge zu informieren. Zuerst müssen Sie für jede Zinskondition einen eigenen Code einrichten. Danach können Sie den Code in das Feld Zinskonditionencode auf Debitorenkarten eingeben.  

## <a name="finance-charge-terms"></a>Zinskonditionbestimmung

Sie müssen für jede Berechnung der Finanzierungskosten Finanzierungskostenbedingungen festlegen und diese dann dem Kunden im Feld **Gebührenbedingungen Code** auf der Seite **Debitor** zuweisen.

Zinsrechnungen können entweder auf der Grundlage des Tagessaldos oder des fälligen Saldos berechnet werden.

* Durchschnittlicher Tagessaldo  
  
  Die Anzahl der Tage, die die Zahlung überfällig ist, wird berücksichtigt:  
  *Durchschnittlicher Tagessaldo* - *Belastung* = *Überfälliger Betrag* x *(Überfälliger Betrag / Zinsperiodeo)* x *(Zinssatz/100)*

* Fälliger Saldo  
  
  Bei der Methode Fälliger Saldo stellt die Zinsberechnung einfach einen Prozentsatz des überfälligen Betrags dar:  
  *Methode fälliger Saldo* - *Belastung* = *Überfälliger Betrag* x *(Zinssatz Rate / 100)*

Zusätzlich ist jede Bestimmung in der Tabelle Zinskondition mit einer Untertabelle, der Tabelle Zinsrechnungstext verbunden. Für jeden Zinskonditionencode kann hier ein Vor- und/oder Nachtext hinterlegt werden, der dann auf dem Zinsrechnungsbeleg erscheint.

### <a name="to-set-up-finance-charge-terms"></a>Um Bedingungen für Gebühren festzulegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zinskonditionen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Um mehr als eine Kombination von Mahnmethoden zu verwenden, richten Sie einen Code für jede ein.

    Für jede Zinskondition können Sie individuelle Bedingungen angeben, die zusätzliche Gebühren in Landes- oder Fremdwährung enthalten können. Sie können mehrere Gebühren in Fremdwährungen für jede Bestimmung auf der Seite **Zinskonditionen** einrichten.
4. Wählen Sie die Aktion **Währungen** aus.
5. Auf der Seite **Währungen für Zinskonditionen** können Sie für jeden Begriff einen Währungscode und Gebühren definieren.

    > [!NOTE]  
    > Wenn Sie Zinsrechnungen in Fremdwährungen erstellen, verwendet die Anwendung die Bedingungen für Fremdwährungen, die Sie in dieser Tabelle eingerichtet haben, um Zinsrechnungen zu erstellen. Falls es keine Zinskonditionen für Fremdwährungen gibt, verwendet die Anwendung die MW-Zinskonditionen für die Mandantenwährung auf der Seite **Zinskondition** und rechnet diese in die entsprechende Währung um.

    Für jeden Zinskonditionencode können Sie Texte festlegen, die vor (**Vortext**) oder nach (**Nachtext**) den Posten in der Zinsrechnung ausgedruckt werden sollen.  
6. Wählen Sie die Aktionen **Vortext** oder **Nachtext** entsprechend aus und füllen Sie die Seite **Zinsgebühr** aus.
7. Um zugehörige Werte in das resultierende Zinsgebühr automatisch einzusetzen, geben -Sie die folgenden Platzhaltern im Feld **Text** Feld ein.

|Platzhalter|Wert|  
|-----------------|-----------|  
|%1|Inhalt des Felds **Belegdatum** des Zinsgebührkopfs|  
|%2|Inhalt des Felds **Fälligkeitsdatum** des Zinsgebührkopfs|  
|%3|Inhalt des Felds **Zinssatz** im verknüpften Zinskonditionen|  
|%4|Inhalt des Felds **Restbetrag** des Zinsgebührkopfs|  
|%5|Inhalt des Felds **Zinsbetrag** des Zinsgebührkopfs|  
|%6|Inhalt des Felds **Zusatzgebühr** des Zinsgebührkopfs|  
|%7|Der Gesamtbetrag der Mahnung|  
|%8|Inhalt des Felds **Währungscode** des Zinsgebührkopfs|  
|%9|Inhalt des Felds **Buchungsdatum** des Zinsgebührkopfs|  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/send-memos-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Einrichten von Mahnmethoden, Bestimmungen und Mahntext](finance-setup-reminders.md)  
[Finanzen einrichten](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
