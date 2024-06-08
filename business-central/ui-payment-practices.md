---
title: Zahlungsmethodenbericht
description: 'Erfahren Sie, wie Sie ganz einfach den Zahlungsmethodenbericht für Kreditoren und Debitoren erstellen.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
--- 

# <a name="payment-practices-report"></a>Zahlungsmethodenbericht

In einigen Ländern/Regionen sind Unternehmen verpflichtet, die von den örtlichen Behörden festgelegten Zahlungsfristen für ihre Kreditoren zu melden. Dieses Berichte können auf unterschiedlichen Quellen basieren und Kreditoren nach ihrer Größe oder ihren festgelegten Zahlungsbedingungen sortieren, sodass im Hinblick auf die Kreditoren gemäß den Vorgaben der lokalen Behörden Berichte über Folgendes erstellt werden können:  

- Die durchschnittliche vereinbarte Zahlungsperiode.  
- Die durchschnittliche tatsächliche Zahlungsbedingung   
- Der Anteil der Rechnungen, die nach Ablauf der vereinbarten Zahlungsperiode bezahlt werden. 

Benutzende können die Periode auswählen, für die sie eine Berechnung ausführen und Details basierend auf einer von Ihnen gewählten Gruppierung suchen möchten. Für jede dieser Gruppierungen können Sie Einträge mit Quellenangaben finden. 

> [!NOTE]
> Diese Berichterstattung ist bislang nur in einigen Ländern vorgeschrieben, es handelt sich jedoch um eine globale Funktion, die überall verwendet werden kann. Derzeit müssen schwedische Unternehmen mit mindestens 250 Mitarbeitenden dem schwedischen Handelsregister jedes Jahr melden, welche Zahlungsfristen sie für Einkäufe bei kleineren Unternehmen haben. Ähnliche Gesetze gibt es im Vereinigten Königreich, in Australien und Neuseeland.  

## <a name="generate-the-report"></a>Den Bericht generieren

Um den Bericht **Zahlungsmethoden** auszuführen, gehen Sie wie folgt vor:

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungsmethoden** ein und wählen Sie dann den zugehörigen Link. 
2. Wählen Sie **Neu** aus.
3. Geben Sie auf dem Inforegister **Allgemein** Werte in die folgenden Felder ein:

   | Feld | Description |
   |---------|-----------------------------------|
   | Anz. | Legen Sie die Nummer für den Posten oder den Datensatz für den Bericht fest. |
   | Aggregationsart | Geben Sie an, wie Daten aggregiert werden. Wenn Sie die Option **Periode** wählen, basiert der Bericht auf unterschiedlichen Perioden. Wenn Sie jedoch die Option **Unternehmensgröße** wählen, wird der Bericht auf Grundlage der Unternehmensgrößen erstellt, die im Feld **Unternehmensgrößencode** auf der Karte **Kreditor** konfiguriert sind. |
   | Kopfart | Gibt die Quelle für Posten in der Zahlungsmethode an. Sie können Kreditoren, Debitoren oder beides auswählen. |
   | Startdatum | Gibt das Startdatum der Zahlungsmethode an. |
   | Enddatum | Gibt das Enddatum der Zahlungsmethode an. |

> [!NOTE]
> Wenn Sie die Option **Unternehmensgröße** verwenden möchten, müssen Sie zunächst Posten auf der Seite **Unternehmensgrößen** erstellen und diese allen Kreditoren hinzufügen, die Sie mit dieser Methode verfolgen möchten.

4. Nachdem Sie alle Felder in der Kopfzeile ausgefüllt haben, müssen Sie die Aktion **Generieren** ausführen, um Daten in den Zeilen und Statistiken für den ausgewählten Berichtstyp zu generieren.
5. Je nach dem **Aggregationstyp** erhalten Sie unterschiedliche Zeilen. Sie können einige Werte manuell ändern. In diesem Fall werden jedoch jede geänderte Zeile und der gesamte Bericht als **Manuell geändert** gekennzeichnet.
6. Sie können von allen berechneten Feldern aus tiefer vordringen und sehen, wie dieses Ergebnis berechnet wurde, indem Sie die Seite **Zahlungsmethoden-Datenliste** öffnen.
7. Wenn Sie den Beleg drucken möchten, können Sie dies über die Aktion **Drucken** tun.

## <a name="see-also"></a>Siehe auch

[Finanzberichte](finance-reports.md)  
[Analysieren von Finanzberichten in Microsoft Excel](finance-analyze-excel.md)  
[Debitorenberichte und -analysen](receivables-reports.md)  
[Kreditorenberichte und -analysen](payables-reports.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Finanzen](finance.md)  
[Lokale Funktionen – Übersicht](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
