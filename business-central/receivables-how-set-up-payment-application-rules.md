---
title: Einrichten von Regeln für die automatische Anwendung von Zahlungen
description: Auf der Seite „Zahlungsausgleichsvorschriften“ richten Sie die Regeln ein, um zu steuern, wie Zahlungen/Banktransaktionen automatisch mit ihren entsprechenden offenen Sachposten ausgeglichen werden, wenn Sie die Funktion Automatisch anwenden auf der Seite Zahlungsabstimmungsbuch.-Blatt verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 07/23/2020
ms.author: sgroespe
ms.openlocfilehash: b655032a17aa617ccbaba2ac3dfd5413d4ca4326
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617573"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Einrichten von Regeln für die automatische Anwendung von Zahlungen

Auf der Seite **Zahlungsausgleichsvorschriften** Regeln Sie regeln ein, um zu steuern, wie der Zahlungstext (bei einer Banktransaktion) in den folgenden beiden Prozessen automatisch mit dem Text auf offenen Einträgen abgeglichen wird:

- Gleichen Sie Zahlungen automatisch mit ihren entsprechenden offenen (unbezahlten) Rechnungen, Gutschriften und anderen Einträgen ab, wenn Sie die Funktion **Automatisch anwenden** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** verwenden. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

- Ordnen Sie Banktransaktionen automatisch den zugehörigen internen Bankkontenposten zu, wenn Sie die Aktion **Automatisch abgleichen** auf der Seite **Bankkontoabstimmung** auswählen. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).

Sie richten neue Regeln zur Zahlungsanwendung ein, indem Sie auswählen, welche Arten von Daten in einer Zahlungsabstimmungsbuch.-Blattzeile mit Daten einem oder mehreren offenen Posten übereinstimmen müssen, bevor die zugehörige Zahlung automatisch auf die offenen Posten angewendet wird. Die Qualität jedes automatischen Ausgleichs wird als Wert zwischen **Niedrig** und **Hoch** im Feld **Übereinstimmungsgenauigkeit** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** entsprechend der Zahlungsausgleichsregel angezeigt, die verwendet wurde.

Jede Reihe auf der Seite **Zahlungsausgleichsregeln** repräsentiert eine Zahlungsausgleichsregel. Regeln werden in der Reihenfolge angewendet, die durch das Feld **Sortierreihenfolge** angegeben ist. Wenn mehrere Regeln gleichzeitig verwendet werden, wird die Übereinstimmungsgenauigkeit der als am höchsten sortierten Regel verwendet.

Die automatische Abstimmungsfunktion basiert auf priorisierten Zuordnungskriterien. Zuerst versucht die Funktion, in priorisierter Reihenfolge, Text in den fünf **Zugehörige Partei**-Feldern einer Buch.-Blattzeile mit Text im Bankkonto, Namen oder Adresse der Debitoren oder der Kreditoren mit unbezahlten Belegen, die offene Posten darstellen, abzugleichen. Anschließend versucht die Funktion, den Text in den Feldern **Transaktionstext** und **Zusätzliche Transaktionsinformationen** in einer Journalzeile mit Text in den Feldern **Externe Dokumentennummer** und **Dokument Nr.** bei offenen Einträgen abzugleichen. Zuletzt versucht die Funktion, den Betrag im Feld **Auszugsbetrag** mit einer Buch.-Blattzeile mit dem entsprechenden Betrag aus offenen Posten abzugleichen.

> [!NOTE]
> Der Textabgleich ist nur für Text mit mehr als vier Zeichen möglich.

Neben den Zuordnungskriterien gilt Folgendes hinsichtlich des Vorzeichens des Zahlungsbetrags:

- Für negative Beträge wird ein Abgleich gegen offene Posten, die Debitorenrechnungen repräsentieren, und dann gegen Kreditorgutschriften vorgenommen.
- Für positive Beträge wird ein Abgleich gegen offene Posten, die Kreditorenrechnungen repräsentieren, und dann gegen Debitorgutschriften vorgenommen.

## <a name="to-set-up-a-payment-application-rule"></a>So richten Sie eine Zahlungsausgleichsregel ein
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Zahlungsausgleichsvorschriften** ein, und wählen Sie dann den zugehörigen Link.
2. Definieren Sie eine neue oder bearbeitete Zahlungsausgleichsregel, indem Sie die Felder in einer Zeile ausfüllen, wie in der folgenden Tabelle beschrieben.

|Feld|Beschreibung|
|-|-|
|**Übereinstimmungsgenauigkeit**|Gibt Ihr Vertrauen in die Ausgleichsregel an, die Sie in der Zeile definieren. <br /></br>Ein Wert, den Sie in diesem Feld angeben, wird im Feld **Übereinstimmungsgenauigkeit** auf der Seite **Zahlungsabstimmungsbuch.-Blatt** entsprechend der Qualität des automatischen Zahlungsausgleichs der Buch.-Blattzeile angezeigt.|
|**Priorität**|Gibt die Priorität der Anwendungsregel in Bezug auf andere Anwendungsregeln an, die als Zeilen auf der Seite **Zahlungsausgleichsvorschriften** definiert sind. 1 stellt die höchste Priorität dar.|
|**Übereinstimmende zugehörige Partei**|Gibt an, wie viel Informationen über den Debitor oder Kreditor (wie Adresse, Ortsname und Bankkontonummer) auf der Zahlungsabstimmungsbuch.-Blattzeile mit Daten in dem offenen Posten übereinstimmen müssen, bevor die Ausgleichsregel verwendet wird, um die Zahlung automatisch mit dem offenen Eintrag auszugleichen.|
|**Belegnummer/übereinstimmende ext. Belegnummer**|Gibt an, ob der Text in der Zahlungsabstimmungsbuch.-Blattzeile mit dem Wert im Feld **Belegnr.** oder im Feld **Externe Belegnummer** für den offenen Posten übereinstimmen muss, bevor die Ausgleichsregel zum automatischen Ausgleich der Zahlung des offenen Postens verwendet wird.|
|**Übereinstimmender Betrag einschließlich Toleranz**|Gibt an, wie viele Posten für einen Debitor oder Kreditor den Betrag einschließlich Zahlungstoleranz übereinstimmen müssen, bevor die Ausgleichsregel verwendet wird, um die Zahlung eines offenen Postens automatisch auszugleichen.|

Die folgende Tabelle zeigt, welche Zahlungsausgleichsregeln in der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] eingerichtet sind.

> [!Important]
> Die Zahlungsausgleichsregeln können anders sein als in Ihrer Implementierung von [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Übereinstimmungsgenauigkeit | Priorität | Übereinstimmende zugehörige Partei | Belegnummer/Externe Belegnummer Übereinstimmend | Übereinstimmender Betrag einschließlich Toleranz |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Hoch             | 1        | Vollständig                 | Ja – mehrfach                 | Eine Übereinstimmung                      |
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

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Zahlungen mit automatischem Ausgleich abstimmen](receivables-how-reconcile-payments-auto-application.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
