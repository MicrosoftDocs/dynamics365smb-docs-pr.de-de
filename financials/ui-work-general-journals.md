---
title: "Arbeiten mit Fibu Buch.-Blättern | Microsoft Docs"
description: "Vorgehensweise: Arbeit mit Fibu-Buch.-Blättern"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Arbeiten mit Fibu Buch.-Blättern
<a id="working-with-general-journals" class="xliff"></a>
Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt. Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.

[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält auch nichtfinanzielle Buch.-Blätter, beispielsweise das Artikel Buch.-Blatt und das Inventur Buch.-Blatt, doch diese Buch.-Blätter sind nicht auf der Benutzeroberfläche sichtbar.

Die in ein Buch.-Blatt eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Buch.-Blatt befinden. Durch Buchen des Buch.-Blatts werden die Informationen in Posten auf Konten übertragen und können nicht mehr geändert werden. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten.

## Buch-Blattvorlagen und -namen
<a id="journal-templates-and-batches" class="xliff"></a>
Es gibt mehrere Fibu Buch.-Blattvorlagen. Jede Buch.-Blattvorlage wird durch ein spezifisches Fenster mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie das Fenster **Zahlungs-Abstimmungs-Buch.-Blatt**, um Bankzahlungen und das Fenster **Zahlungsausgangs Buch.-Blatt** zu verarbeiten, um Ihre Kreditoren zu bezahlen.

**Hinweis**: Wenn Sie Zahlungsdateien an Ihre Bank aus dem Zahlungsausgangs Buch.-Blatt exportieren, müssen Sie das Kontrollkästchen **Zahlungsexport erlauben** für den Buch.-Blattnamen auswählen, der im Fenster **Fibu Buch.-Blattnamen** angezeigt wird. Weitere Informationen finden Sie unter [So gehts: Zahlungen in eine Bankdatei exportieren](payables-how-export-payments-bank-file.md).

Sie können zu jeder Buch.-Blattvorlage mehrere Buch.-Blattnamen als Buch-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungsausgangsbuch erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat.

Ein Beispiel einer persönlichen Einstellungen, die Sie in Ihrem Fibu Buch.-Stapel festlegen können, ist es, mit der Systemhilfe die Betrag-Felder auszufüllen. Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Buch.-Blattzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter [ [!INCLUDE[d365fin](includes/d365fin_md.md)] Werte vorschlagen lassen](ui-let-system-suggest-values.md).

## Hauptkonten und Gegenkonten
<a id="main-accounts-and-balancing-accounts" class="xliff"></a>
Wurden Standardgegenkonten für die Buch.-Blattnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Feld Sie müssen auch das Feld **Kontonr.**ausfüllen, Feld und **Gegenkonto-Nummer** Feld manuell. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

**Hinweis**: Die MwSt. für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MwSt.-Prozentsätze verwendet werden können.

## Wiederkehrende Buch.-Blätter
<a id="recurring-journals" class="xliff"></a>
Bei einem wiederkehrenden Buch.-Blatt handelt es sich um ein Fibu Buch.-Blatt mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig mit geringen oder keinen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Vorgehensweise: Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern](ui-how-use-allocation-keys-general-journals.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

