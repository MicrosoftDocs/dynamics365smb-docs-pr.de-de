---
title: Anlagenbudgets verwalten
description: 'Die Informationen über Ihre zukünftigen Investitionen, Verkäufe und Abschreibungen von Anlagen, die Ihnen helfen, Budget- und Planungen vorzubereiten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: forecast
ms.search.form: '5610, 5611'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="manage-budgets-for-fixed-assets"></a>Budgets für Anlagen verwalten

Sie können budgetierte Anlagen einrichten. Dadurch haben Sie die Möglichkeit, geplante Anschaffungen und Verkäufe in Berichten zu berücksichtigen.  

Um Ihre budgetierte GuV, die budgetierte Bilanz und Ihr Finanzbudget vorzubereiten, benötigen Sie Informationen über Ihre zukünftigen Investitionen, Verkäufe und Abschreibungen von Anlagen. Diese Informationen erhalten Sie im Bericht **Anlage - Vorschau**. Bevor Sie diesen Bericht ausdrucken, müssen Sie das Budget vorbereiten.  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>So budgetieren Sie die Anschaffungskosten einer Anlage

Um ein Budget vorzubereiten, müssen Sie Anlagenkarten für die Anlagen einrichten, die Sie zukünftig erwerben möchten. Die budgetierten Anlagen werden als normale Anlagen eingerichtet, aber sie müssen so eingerichtet sein, dass sie nicht in der Finanzbuchhaltung buchen.

Wenn Sie Anschaffungskosten buchen, geben Sie die Nummer der budgetierten Anlage im Feld **Plananlagennr.** ein. Dadurch werden Anschaffungskosten mit einem umgekehrten Vorzeichen für die Plananlage gebucht. D. h., dass die Gesamtanschaffungskosten der Plananlage die Differenz zwischen den budgetierten und den tatsächlichen Anschaffungskosten sind.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus, um eine neue Anlagenkarte für die budgetierte Anlage zu erstellen.
3. Wählen Sie das Kontrollkästchen **Plananlage**, um Buchungen in der Finanzbuchhaltung zu vermeiden.
4. Füllen Sie die restlichen Felder aus, weisen Sie ein AfA-Buch zu, und buchen Sie dann die ersten Anschaffungskosten mit der budgetierten Anlage im Feld **Plananlagennr.** Weitere Informationen finden Sie unter [Erwerben von Anlagen](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>So budgetieren Sie Verkäufe von Anlagen

Falls Sie innerhalb der Periode, für die Sie ein Budget erstellen, den Verkauf einer Anlage planen, können Sie Informationen zum Verkaufspreis und zum Verkaufsdatum eingeben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, die verkauft werden soll, und wählen Sie dann die Aktion **AfA-Bücher** aus.
3. Füllen Sie auf der Seite **Anlagen-AfA-Bücher** die Felder **Erwartetes Abgangsdatum** und **Erwarteter Verkaufspreis** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>So zeigen Sie geschätzte Verkaufswerte an

Um sich die geschätzten Verkaufswerte anzeigen zu lassen und den entstehenden Gewinn oder Verlust zu berechnen, können Sie den Bericht **Anlagenvorschau** verwenden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagenvorschau** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="to-budget-depreciation"></a>So budgetieren Sie AfA

Sie können den Bericht **Anlage - Vorschau** zur Kalkulation von zukünftigen Abschreibungen verwenden. Dieser Bericht zeigt den Buchwert und die kumulierte AfA zum Beginn einer gewählten Periode, die Änderungen innerhalb dieser Periode und den Buchwert sowie die kumulierte AfA am Ende der Periode.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagenvorschau** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wenn Sie die Gesamtsummen für alle Anlagen anzeigen möchten, deaktivieren Sie das Kontrollkästchen **Druck pro Anlage**.
4. Lassen Sie das Inforegister **Anlage** leer, damit alle Anlagen einbezogen werden. Geben Sie im Feld **Plananlage** die Einstellung **Nein** an, um Plananlagen auszuschließen, oder geben Sie **Ja** an, um nur Plananlagen anzuzeigen.
5. Wählen Sie die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Überblick über die Anlagenanalyse](fa-analytics-overview.md)   
[Einrichten von Anlagen](fa-setup.md)  
[Finanzen](finance.md)  
[Vorbereitung auf die Verwendung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
