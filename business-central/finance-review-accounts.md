---
title: Sachkonten überprüfen
description: 'Sie können Ihren Fortschritt verfolgen, wenn Sie Beträge in Hauptbuchkonten überprüfen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
---

# Beträge in Sachkonten überprüfen

Möglicherweise haben Sie Hauptbuchkonten, die Sie häufig im Auge behalten. Oder Sie möchten den Überprüfungsprozess am Ende des Monats beschleunigen. Um die Nachverfolgung zu vereinfachen und die Überprüfungen zu beschleunigen, verwenden Sie für jedes Konto die Aktion **Entitäten überprüfen** auf der Seite **Kontenplan** oder **Sachkonto**. 

## Konten für die Überprüfung einrichten

Geben Sie auf der Seite **Sachkontokarte** für jedes Konto an, wie Bewertungen im Feld **Bewertungsrichtlinie** zugelassen werden sollen.

|Richtlinie überprüfen  |Beschreibung  |
|---------|---------|
|"Keine"     | Sie können Einträge für das Konto nicht als überprüft markieren. Verwenden Sie diese Option beispielsweise für Konten wie Verbindlichkeiten, Forderungen und Bankkonten, bei denen es andere Möglichkeiten gibt, ihre Beträge zu überprüfen.        |
|Überprüfung zulassen     | Sie müssen keine Buchungen in eine Überprüfung einbeziehen, und die Beträge der Soll- und Habenbuchungen müssen nicht ausgeglichen werden. Sie entfernen beispielsweise eine Bewertung, wenn Sie einen Fehler gemacht haben.        |
|Überprüfung zulassen und Saldo abgleichen     | Die Gesamtbeträge der Soll- und Habenbuchungen in der Prüfung müssen übereinstimmen. Die Felder **Soll** und **Haben** zeigen diese Beträge und das Feld **Saldo** zeigt die Gesamtsumme. Mit dieser Einstellung können Sie auch eine Bewertung entfernen. Wenn Sie eine Bewertung von einem oder mehreren Einträgen entfernen, müssen die Soll- und Habeneinträge noch ausgeglichen sein.        |

## Einträge als überprüft markieren

Wählen Sie die Einträge aus, die Sie überprüft haben, und verwenden Sie dann die Aktion **Ausgewählte als überprüft festlegen**. Jedes Mal, wenn Sie einen oder mehrere Einträge als überprüft markieren, erhalten die Einträge dieselbe Nummer in der Spalte **Überprüfungs-ID** . Die Überprüfungskennung ist eine praktische Methode, um die Einträge zu verfolgen, die gleichzeitig überprüft wurden. [!INCLUDE [prod_short](includes/prod_short.md)] zeichnet auch den Benutzer auf, der die Überprüfung vorgenommen hat, und wann er sie durchgeführt hat.

Wenn Sie Einträge als überprüft markieren, dies aber bereuen, verwenden Sie die Aktion **Ausgewählte als nicht überprüft festlegen**.

* Wenn dem Konto die Richtlinie Überprüfung zulässig zugewiesen ist, setzt die Aktion die überprüfte Kennung auf 0 zurück und entfernt die Person sowie das Datum und die Uhrzeit der Überprüfung. 
* Wenn die Richtlinie „Überprüfung zulässig und Kontostand abgleichen“ zugewiesen ist, müssen Guthaben und Soll dennoch ausgeglichen sein. Wenn beispielsweise einer der Einträge in einer Bewertung ein Fehler ist, können Sie einen anderen Eintrag mit dem richtigen Wert auswählen. Der Ersatzeintrag muss nicht dieselbe überprüfte Kennung haben.

> [!TIP]
> Eine schnelle Möglichkeit, mehrere Einträge auszuwählen, besteht darin, die Strg- oder Umschalttaste gedrückt zu halten, während Sie die Einträge auswählen. Mit der Strg-Taste können Sie bestimmte Einträge auswählen, und mit der Umschalttaste werden alle Einträge zwischen dem ersten und dem letzten ausgewählten Eintrag ausgewählt.

## Überprüfen Sie Konten mit alten Einträgen

Möglicherweise haben Sie Einträge aus vergangenen Perioden, die Sie bereits überprüft haben oder die einfach nicht überprüft werden müssen. Sie möchten mit der Überprüfung von Einträgen beginnen, z. B. ab Beginn des Jahres oder des Abrechnungszeitraums. Sie können die Posten unverändert lassen. Wenn Sie jedoch Daten in Excel oder im Analysemodus analysieren möchten, markieren Sie die Einträge als überprüft. Weitere Informationen zum Analysieren von Einträgen finden Sie unter [Einträge analysieren](#analyze-entries). Um die Einträge als überprüft zu markieren, fügen Sie im Filterbereich einen Filter hinzu, um nur diese Einträge anzuzeigen, und wählen Sie dann die Aktion **Ausgewählte Einträge als überprüft markieren** aus.

## Einträge filtern

Um ein klareres Bild zu erhalten, gibt es mehrere Möglichkeiten zum Filtern von Einträgen auf der Seite **Hauptbucheinträge prüfen** .

* Verwenden Sie die Aktionen **Überprüfte Einträge anzeigen** und **Überprüfte Einträge ausblenden**, um nur die Einträge anzuzeigen, die Sie überprüft oder nicht überprüft haben. Um die Filter zu löschen, verwenden Sie die Aktion **Alle Einträge anzeigen**.
* Verwenden des Filterbereichs. Sie können beispielsweise nach der Kontonummer filtern oder, wenn Sie ältere Einträge haben und diese alle als überprüft markieren möchten, nach einem Veröffentlichungsdatum.

## Einträge analysieren

Es gibt mehrere Möglichkeiten, die von Ihnen überprüften Hauptbucheinträge zu analysieren.

* Aktivieren Sie beispielsweise den Analysemodus, um Einträge nach ihrer überprüften Kennung zu gruppieren. Weitere Informationen zum Analysemodus finden Sie unter [Listenseitendaten im Analysemodus analysieren](analysis-mode.md).
* Exportieren Sie die Einträge in Excel.

## Weitere Informationen

[Das Hauptbuch und den Kontenplan verstehen](finance-general-ledger.md)  
[Einrichten oder Ändern des Kontenplans](finance-setup-chart-accounts.md)  
