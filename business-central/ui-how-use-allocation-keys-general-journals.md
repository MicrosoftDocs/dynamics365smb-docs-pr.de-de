---
title: Verwenden von Verteilungsschlüsseln in Fibu Buch.-Blättern
description: Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.search.form: '283, 284'
ms.date: 06/29/2021
ms.author: edupont
---
# <a name="use-allocation-keys-in-general-journals"></a><a name="use-allocation-keys-in-general-journals"></a><a name="use-allocation-keys-in-general-journals"></a>Zuordnungsschlüssel in Allgemeinen Buch.-Blättern verwenden
Sie können einen Eintrag in einem Allgemeinen Journal mehreren verschiedenen Konten zuordnen, wenn Sie das Journal buchen. Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.

## <a name="to-set-up-allocation-keys"></a><a name="to-set-up-allocation-keys"></a><a name="to-set-up-allocation-keys"></a>Einrichten von Verteilungsschlüsseln
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Wiederk. Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Fibu Buch.-Blattnamen** den **Buch.-Blattnamen**.
3. Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.
   * Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.
   * Um die Zuordnungen eines vorhandenen Buch.-Blattes zu ändern, wählen Sie das Buch.-Blatt und gehen Sie zum Schritt 7.    
4. Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Buch.-Blatt.
5. Wenn Sie fertig sind, schließen Sie die Seite. Ein neues, leeres wiederkehrendes Buchungsblatt wird geöffnet.
6. Füllen Sie die Felder in der Zeile aus.
7. Wählen Sie die Aktion **Verteilung** aus.
8. Erstellen Sie für jede Verteilung eine Zeile. Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen. Sie müssen ebenfalls das Feld **Kontonr.** ausfüllen und, wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".
9. Wenn Sie in einer Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet. Diese Beträge haben das gegenteilige Vorzeichen wie der Gesamtbetrag im Feld **Betrag** des wiederkehrenden Buch.-Blattes.
10. Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zur Seite **Wiederk. Fibu Buch.-Blätter** zurückzukehren. Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.
11. Buchen Sie die Buch.-Blattzeile.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>So ändern Sie einen bereits eingerichteten Zuordnungsschlüssel
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Wiederk. Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Wiederk. Fibu Buch.-Blatt** das Buch.-Blatt mit der Verteilung aus.
3. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.
4. Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Dokumente und Buch.-Blatt verbuchen](ui-post-documents-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
