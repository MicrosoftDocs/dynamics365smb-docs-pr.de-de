---
title: Regeln für die automatische Anwendung von Zahlungen
description: 'Lesen Sie auf der Seite Regeln für Zahlungsausgleichsvorschriften, wie Sie Regeln für die automatische Anwendung von Zahlungen festlegen können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/03/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Regeln für die automatische Anwendung von Zahlungen einrichten

Auf der Seite **Zahlungsausgleichsvorschriften** richten Sie die Regeln ein, um zu steuern, wie Zahlungstext (bei einer Banktransaktion) automatisch mit dem Text auf zugehörigen offenen (unbezahlten) Rechnungen, Gutschriften oder anderen Einträgen abeglichen wird, wenn Sie die Funktion **Automatisch anwenden** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** verwenden. Weitere Informationen finden Sie unter [Zahlungen mithilfe der automatischen Anwendung abgleichen](receivables-how-reconcile-payments-auto-application.md).

Sie richten neue Regeln zur Zahlungsanwendung ein, indem Sie auswählen, welche Arten von Daten in einer Zahlungsabstimmungsbuch.-Blattzeile mit Daten einem oder mehreren offenen Posten übereinstimmen müssen, bevor die zugehörige Zahlung automatisch auf die offenen Posten angewendet wird. Die Qualität jedes automatischen Ausgleichs wird als Wert zwischen **Niedrig** und **Hoch** im Feld **Übereinstimmungsgenauigkeit** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** entsprechend der Zahlungsausgleichsregel angezeigt, die verwendet wurde.

Jede Reihe auf der Seite **Zahlungsausgleichsregeln** repräsentiert eine Zahlungsausgleichsregel. Regeln werden in der Reihenfolge angewendet, die durch das Feld **Sortierreihenfolge** angegeben ist. Wenn mehrere Regeln gleichzeitig verwendet werden, wird die Übereinstimmungsgenauigkeit der als am höchsten sortierten Regel verwendet.

Die automatische Abstimmungsfunktion basiert auf priorisierten Zuordnungskriterien. Zuerst versucht die Funktion, in priorisierter Reihenfolge, Text in den fünf **Zugehörige Partei**-Feldern einer Buch.-Blattzeile mit Text im Bankkonto, Namen oder Adresse der Debitoren oder der Kreditoren mit unbezahlten Belegen, die offene Posten darstellen, abzugleichen. Anschließend versucht die Funktion, den Text in den Feldern **Transaktionstext** und **Zusätzliche Transaktionsinformationen** in einer Journalzeile mit Text in den Feldern **Externe Dokumentennummer** und **Dokument Nr.** bei offenen Einträgen abzugleichen. Zuletzt versucht die Funktion, den Betrag im Feld **Auszugsbetrag** mit einer Buch.-Blattzeile mit dem entsprechenden Betrag aus offenen Posten abzugleichen.

> [!NOTE]
> Der Textabgleich ist nur für Text mit mehr als vier Zeichen möglich.

Neben den Zuordnungskriterien gilt Folgendes hinsichtlich des Vorzeichens des Zahlungsbetrags:

- Für negative Beträge wird ein Abgleich gegen offene Posten, die Debitorenrechnungen repräsentieren, und dann gegen Kreditorgutschriften vorgenommen.
- Für positive Beträge wird ein Abgleich gegen offene Posten, die Kreditorenrechnungen repräsentieren, und dann gegen Debitorgutschriften vorgenommen.

## So richten Sie eine Zahlungsausgleichsregel ein
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zahlungsausgleichsvorschriften** ein, und wählen Sie dann den zugehörigen Link.
2. Definieren Sie eine neue oder bearbeitete Zahlungsausgleichsregel, indem Sie die Felder in einer Zeile ausfüllen, wie in der folgenden Tabelle beschrieben.

|Feld|Beschreibung|
|-|-|
|**Übereinstimmungsgenauigkeit**|Gibt Ihr Vertrauen in die Ausgleichsregel an, die Sie in der Zeile definieren. <br /></br>Ein Wert, den Sie in diesem Feld angeben, wird im Feld **Übereinstimmungsgenauigkeit** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** entsprechend der Qualität des automatischen Zahlungsausgleichs der Buch.-Blattzeile angezeigt.|
|**Priorität**|Gibt die Priorität der Anwendungsregel in Bezug auf andere Anwendungsregeln an, die als Zeilen auf der Seite **Zahlungsausgleichsvorschriften** definiert sind. 1 stellt die höchste Priorität dar.|
|**Übereinstimmende zugehörige Partei**|Gibt an, wie viel Informationen über den Debitor oder Kreditor (wie Adresse, Ortsname und Bankkontonummer) auf der Zahlungsabstimmungsbuch.-Blattzeile mit Daten in dem offenen Posten übereinstimmen müssen, bevor die Ausgleichsregel verwendet wird, um die Zahlung automatisch mit dem offenen Eintrag auszugleichen.|
|**Belegnr./Ext. Belegnr. abgeglichen**|Gibt an, ob der Text in der Zahlungsabstimmungsbuch.-Blattzeile mit dem Wert im Feld **Belegnr.** oder im Feld **Externe Belegnummer** für den offenen Posten übereinstimmen muss, bevor die Ausgleichsregel zum automatischen Ausgleich der Zahlung des offenen Postens verwendet wird.|
|**Anzahl der Einträge innerhalb der gefundenen Betragstoleranz**|Gibt an, wie viele Posten für einen Debitor oder Kreditor den Betrag einschließlich Zahlungstoleranz übereinstimmen müssen, bevor die Ausgleichsregel verwendet wird, um die Zahlung eines offenen Postens automatisch auszugleichen.|
|**Überprüfung erforderlich**|Gibt an, ob die automatische Zahlungsanwendung für die manuelle Überprüfung durch den Benutzer vor dem Posten empfohlen wird. Durch Auswahl des Felds **Zu überprüfende Zeilen** auf der Seite **Zahlungsantragsjournal** startet eine geführte Erfahrung, bei der Sie problemlos mehrere Anwendungen in einer Sequenz auf der Website **Überprüfung des Zahlungsantrags** überprüfen können.|

In der folgenden Tabelle werden die Standardregeln für Zahlungsanwendungen in [!INCLUDE[prod_short](includes/prod_short.md)] beschrieben.

> [!Important]
> Die Zahlungsausgleichsregeln können anders sein als in Ihrer Implementierung von [!INCLUDE[prod_short](includes/prod_short.md)].

| Übereinstimmungsgenauigkeit | Priorität | Übereinstimmende zugehörige Partei | Belegnr./übereinstimmende ext. Belegnr. | Anzahl gefundener Posten innerhalb Betragstoleranz |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Hoch             | 0        | Vollständig                 | Ja – mehrfach                 | Eine Übereinstimmung                      |
| Hoch             | 2        | Vollständig                 | Ja – mehrfach                 | Mehrere Übereinstimmungen               |
| Hoch             | 3        | Vollständig                 | Ja                            | Eine Übereinstimmung                      |
| Hoch             | 4        | Vollständig                 | Ja                            | Mehrere Übereinstimmungen               |
| Hoch             | 5        | Teilweise             | Ja – mehrfach                 | Eine Übereinstimmung                      |
| Hoch             | 6        | Teilweise             | Ja – mehrfach                 | Mehrere Übereinstimmungen               |
| Hoch             | 7        | Teilweise             | Ja                            | Eine Übereinstimmung                      |
| Hoch             | 8        | Vollständig                 | Nein                             | Eine Übereinstimmung                      |
| Hoch             | 9        | Nein                    | Ja – mehrfach                 | Eine Übereinstimmung                      |
| Hoch             | 10       | Nein                    | Ja – mehrfach                 | Mehrere Übereinstimmungen               |
| Mittel           | 1        | Vollständig                 | Ja – mehrfach                 | Nicht berücksichtigt                 |
| Mittel           | 2        | Vollständig                 | Ja                            | Nicht berücksichtigt                 |
| Mittel           | 3        | Vollständig                 | Nein                             | Mehrere Übereinstimmungen               |
| Mittel           | 4        | Teilweise             | Ja – mehrfach                 | Nicht berücksichtigt                 |
| Mittel           | 5        | Teilweise             | Ja                            | Nicht berücksichtigt                 |
| Mittel           | 6        | Nein                    | Ja                            | Eine Übereinstimmung                      |
| Mittel           | 7        | Nein                    | Ja - mehrfach                   | Nicht berücksichtigt                 |
| Mittel           | 8        | Teilweise             | Nein                             | Eine Übereinstimmung                      |
| Mittel           | 9        | Nein                    | Ja                            | Nicht berücksichtigt                 |
| Gering              | 1        | Vollständig                 | Nein                             | Keine Übereinstimmungen                     |
| Gering              | 2        | Teilweise             | Nein                             | Mehrere Übereinstimmungen               |
| Gering              | 3        | Teilweise             | Nein                             | Keine Übereinstimmungen                     |
| Gering              | 4        | Nein                    | Nein                             | Eine Übereinstimmung                      |
| Gering              | 5        | Nein                    | Nein                             | Mehrere Übereinstimmungen               |

## Siehe auch
[Zahlungen mit automatischem Ausgleich abstimmen](receivables-how-reconcile-payments-auto-application.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
