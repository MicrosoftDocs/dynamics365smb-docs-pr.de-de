---
title: Übersicht über die Zuweisung von Kosten und Einnahmen
description: Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des wiederkehrenden Buch.-Blatts auf verschiedene Konten verteilen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.form: '283, 5629'
ms.date: 02/05/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Wiederkehrende Kosten und Einkünfte zuteilen

Sie können einen Eintrag in einem wiederkehrenden Fibu Buch.-Blatt mehreren Konten zuordnen, wenn Sie das Journal buchen. Weitere Informationen zu wiederkehrenden Fibu Buch.-Blättern finden Sie unter [Mit wiederkehrenden Buchblättern arbeiten](ui-work-general-journals.md#work-with-recurring-journals). 

Für die Verteilung stehen drei unterschiedliche Methoden zur Verfügung:

* Menge
* Prozentsatz (%)
* Betrag

Die Zuteilungsfunktionen funktionieren mit wiederkehrenden Buch.-Blättern und in Anlagen-Buch.-Blättern.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Die folgenden Verfahren beschreiben, was bereitgestellt werden muss, um Kosten in einem wiederkehrenden Buch.-Blatt zuzuordnen, indem Verteilungsschlüssel eingerichtet werden. Wenn Verteilungsschlüssel definiert werden, beenden und buchen Sie das Buch.-Blatt wie alle anderen wiederkehrenden Fibu Buch.-Blätter. Weitere Informationen finden Sie unter [Arbeiten mit Allgemeinen Buch.-Blättern](ui-work-general-journals.md).

## Einrichten von Verteilungsschlüsseln

Die Posten einer Fibu Buch.-Blattzeile lassen sich beim Buchen des Buch.-Blatts auf verschiedene Konten verteilen. Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Wiederk. Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
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

## So ändern Sie einen bereits eingerichteten Zuordnungsschlüssel

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Wiederk. Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Wiederk. Fibu Buch.-Blatt** das Buch.-Blatt mit der Verteilung aus.
3. Wählen Sie die Zeile mit der Verteilung und wählen Sie dann die Aktion **Zuweisungen** aus.
4. Ändern Sie die relevanten Felder und wählen Sie dann **OK** aus.

## Siehe auch

[Jahres- und Periodenabschlüsse](year-close-years-periods.md)  
[Arbeiten mit Fibu-Buch.-Blättern](ui-work-general-journals.md)    
[Journale und Dokumente buchen](ui-post-documents-journals.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]