---
title: "So gehts: Bank-Geldmittel überweisen| Microsoft Docs"
description: "Gewusst wie: Bank-Geldmittel überweisen"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 03/32/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e2e3642d08428367fac1dd5845013e14627fe6ed
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Bank-Geldmittel überweisen
<a id="how-to-transfer-bank-funds" class="xliff"></a>
Manchmal ist es erforderlich, einen Betrag von einem Bankkonto auf ein anderes Bankkonto zu überweisen. Dafür müssen Sie eine Transaktion im Fibu Buch.-Blatt buchen. Die Aufgabe variiert abhängig davon, ob die Bankkonten dieselbe Währung oder unterschiedlichen Währungen verwenden.

## So buchen Sie Überweisungen zwischen Bankkonten mit demselben Währungscode:
<a id="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Neubewertung Journal** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie in einer Buch.-Blattzeile die Felder **Buchungsdatum** und **Belegnr.** aus. Felder.
3. Wählen Sie im Feld **Kontoart** die Option **Bankkonto** aus.
4. Wählen Sie im Feld **Kontonummer** die Bank, von der Sie den Betrag überweisen möchten.
5. Geben Sie im Feld **Betrag** den Betrag ein, der überwiesen werden soll.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Wählen Sie im Feld **Gegenkontonummer** das Bankkonto aus, an das Sie den Betrag überweisen möchten.
8. Buchen Sie das Buch.-Blatt.

## Überweisungen zwischen Bankkonten mit verschiedenen Währungscodes buchen:
<a id="to-post-a-transfer-between-bank-accounts-with-different-currency-codes" class="xliff"></a>
Um Beträge zwischen Bankkonten zu transferieren, die unterschiedliche Währungen verwenden, müssen Sie zwei Fibu Buch.-Blattzeilen buchen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Neubewertung Journal** ein und wählen Sie dann den entsprechenden Link aus.
2. Erstellen Sie zwei Buch.-Bl.-Zeilen und füllen Sie **Buchungsdatum** und **Belegnr.** aus. Felder.
3. Wählen Sie in der ersten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.
4. Wählen Sie im Feld **Kontonummer** das Bankkonto aus, von dem Sie die Beträge überweisen möchten.
5. Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein. Geben Sie die Habenbeträge mit einem Minuszeichen ein. Geben Sie die Sollbeträge ohne ein Minuszeichen ein.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Wählen Sie im Feld **Gegenkontonummer** das Bankkonto aus, an das Sie den Betrag überweisen möchten.
8. Wählen Sie in der zweiten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.
9. Wählen Sie im Feld **Kontonummer** das Bankkonto aus, an das Sie den Betrag überweisen möchten.
10. Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos ein. Geben Sie die Habenbeträge mit einem Minuszeichen ein. Geben Sie die Sollbeträge ohne ein Minuszeichen ein.
11. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.  
12. Wählen Sie im Feld **Gegenkontonummer** das Bankkonto aus, von dem Sie die Beträge überweisen möchten.

    **Hinweis**: Wenn die im Buch.-Blatt verwendeten Wechselkurse von den Wechselkursen im Fenster **Währungswechselkurse** abweichen, geben Sie eine dritte Zeile für den Wechselkursgewinn oder -verlust ein. Geben Sie **Sachkonto** im Feld **Kontoart** ein. Geben Sie die Sachkontonummer für Wechselkursgewinn oder -verlust im Feld **Kontonr.** ein. Feld Geben Sie den Wechselkursgewinn oder - verlust im Feld **Amount** mit oder ohne Minuszeichen jeweils für Soll- und Habenbeträge ein.
13. Buchen Sie die Buch.-Blattzeile.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

