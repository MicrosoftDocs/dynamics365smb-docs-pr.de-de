---
title: "Überblick zu Aufgaben, um Kosten und Umsatz zuzuordnen | Microsoft Docs"
description: Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 31f8d40d5a8cf8d190f4a6cb655f09ca72f3e070
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="allocate-costs-and-income"></a>Kosten und Einkünfte zuteilen
Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen. Für die Verteilung stehen drei unterschiedliche Methoden zur Verfügung:

* Menge
* Prozentsatz (%)
* Betrag

Die Verteilungsfeatures können sowohl in wiederkehrenden Buch.-Blättern als auch in Buch.-Blättern für Anlagen verwendet werden.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Die folgenden Verfahren beschreiben, was bereitgestellt werden muss, um Kosten in einem wiederkehrenden Buch.-Blatt zuzuordnen, indem Verteilungsschlüssel eingerichtet werden. Wenn Verteilungsschlüssel definiert werden, beenden und buchen Sie das Buch.-Blatt wie alle anderen wiederkehrenden Fibu Buch.-Blätter. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)

## <a name="to-set-up-allocation-keys"></a>Einrichten von Verteilungsschlüsseln
Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen. Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrendes Buch-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Fibu Buch.-Blattnamen** den **Buch.-Blattnamen**.
3. Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.
   * Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.
   * Um die Zuordnungen eines vorhandenen Buch.-Blattes zu ändern, wählen Sie das Buch.-Blatt und gehen Sie zum Schritt 7.    
4. Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Buch.-Blatt.
5. Wenn Sie fertig sind, schließen Sie das Fenster. Ein neues, leeres wiederkehrendes Buchungsblatt wird geöffnet.
6. Füllen Sie die Felder in der Zeile aus.
7. Wählen Sie die Aktion **Verteilung** aus.
8. Erstellen Sie für jede Verteilung eine Zeile. Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen. Sie müssen ebenfalls das Feld **Kontonr.** ausfüllen und, wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".
9. Wenn Sie in einer Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet. Diese Beträge haben das gegenteilige Vorzeichen wie der Gesamtbetrag im Feld **Betrag** des wiederkehrenden Buch.-Blattes.
10. Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zum Fenster **Wiederk. Fibu Buch.-Blätter** zurückzukehren. Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.
11. Buchen Sie die Buch.-Blattzeile.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Ändern eines bereits eingerichteten Verteilungsschlüssels
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrendes Buch-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Wiederk. Fibu Buch.-Blatt** das Buch.-Blatt mit der Verteilung aus.
3. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.
4. Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)    
[Journale und Dokumente buchen](ui-post-documents-journals.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

