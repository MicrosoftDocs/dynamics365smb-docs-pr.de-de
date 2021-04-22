---
title: Anlagenabschreibung einrichten
description: Sie geben in einem AfA-Buch an, wie Sie Anlagen abschreiben oder anzeigen möchten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: eb7e0d0d082d8a86ce61b6dffab46ce6248a29d9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782279"
---
# <a name="set-up-fixed-asset-depreciation"></a>Richten Sie eine neue Anlagenkarte ein

Sie können unterschiedliche Abschreibungsmethoden für Bilanzen und Steuern verwenden. Viele Großunternehmen verwenden die lineare Abschreibung in ihren Bilanzen, da dadurch im Allgemeinen höhere Gewinne ausgewiesen werden können. Für Einkommenssteuerzwecke verwenden viele Unternehmen jedoch eine beschleunigte Abschreibungsmethode, wie z. B. die degressive Abschreibung. Sie definieren die Abschreibungsmethode einer Anlage mit dem Feld **Abschreibungsmethode** auf der Seite **Anlagenkarte**. Weitere Informationen zu den verschiedenen Methoden finden Sie unter [Abschreibungsmethoden](fa-depreciation-methods.md).

Sie definieren AfA-Bücher, in denen Sie die verschiedenen Arten, wie die Abschreibungen für unterschiedliche Typen von Anlagen berechnet werden müssen. In jedem AfA-Buch legen Sie individuelle Abschreibungsbedingungen fest. Es ist zum Beispiel möglich, dass eine Anlage in einem Buch über einen Zeitraum von drei Jahren abgeschrieben wird und in einem anderen über fünf Jahre.

Nachdem Sie die erforderlichen AfA-Bücher erstellt haben, müssen Sie jeder Anlage mindestens ein AfA-Buch zuweisen. Ein AfA-Buch, das einer Anlage zugewiesen ist, wird als Anlagen-AfA-Buch bezeichnet. Sie können beliebig viele AfA-Bücher für eine Anlage einrichten.  

## <a name="to-create-a-depreciation-book"></a>So erstellen Sie ein Anlagen-AfA-Buch

In einem AfA-Buch können Sie festlegen, wie eine Anlage abgeschrieben wird. Sie können mehrere AfA-Bücher einrichten, um die verschiedenen Abschreibungsarten zu erleichtern.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **AfA-Bücher** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **AfA-Buch Übersicht** wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Inforegister **AfA-Buchkarte** die Seite nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hinweis: Sie können Anlagentransaktionen auf der Seite **Anlagen Fibu Buch.-Blatt** oder auf der Seite **Anlagen Buch - Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Führen Sie den nächsten Schritt aus, um festzulegen, welche Art von Buch.-Blatt für die verschiedenen Anlagenaktivitäten standardmäßig verwendet wird.
4. Aktivieren Sie im Inforregister **Integration** das Kontrollkästchen für jede Anlagenaktivität, deren Transaktionen Sie mithilfe der Seite **Anlagen Fibu Buch.-Blatt** buchen möchten.
5. Wiederholen Sie die Schritte 2 bis 4 für jede AfA- oder Buchungsmethode, die Sie den Anlagen als AfA-Buch zuweisen möchten.

> [!IMPORTANT]
> Wählen Sie das Feld **Period. AfA runden** zum Runden der berechneten periodischen Abschreibungsbeträge auf ganze Zahlen. Zum Beispiel, wenn Ihr Unternehmen auch die Rechnungsrundung auf ganze Zahlen auf der Seite **Hauptbuch-Setup** verwendet, kann das Runden von Abschreibungsbeträgen auf ganze Zahlen zur Transparenz beitragen.

Wenn Sie beispielsweise ein Anlagevermögen veräußern, in dem im Abschreibungsbuch keine Rundung angegeben ist, die Einrichtung des Hauptbuchs Ihres Unternehmens jedoch eine Rundung erfordert, wird bei der Veräußerung des Anlagevermögens die Fehlermeldung angezeigt, dass ein Betrag gerundet werden muss auf einem Hauptbucheintrag.  

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>So verknüpfen Sie ein AfA-Buchs mit einer Anlage
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Anlage** ein, und wählen Sie dann die entsprechende Verknüpfung.
2. Wählen Sie die Anlage aus, für die Sie ein Anlagen-AfA-Buch einrichten möchten.
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus.
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus.
5. Wählen Sie die Aktion **AfA-Bücher** aus , um eine oder mehrere Anlagen-AfA-Bücher anzugeben.

    > [!NOTE]  
    >   Hinweis: Wenn Sie die manuelle AfA-Methode verwenden, müssen Sie die Abschreibung manuell im Anlagen Fibu Buch.-Blatt eingeben. Die Funktion **AfA berechnen** berücksichtigt keine Anlagen mit der AfA-Methode "Manuell". Sie können diese Methode für Anlagen verwenden, die nicht abgeschrieben werden, wie z. B. Land.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>So weisen Sie ein AfA-Buch mehreren Anlagen mit einer Stapelverarbeitung zu
Falls Sie ein AfA-Buch mit mehreren Anlagen verknüpfen möchten, können Sie die Stapelverarbeitung **Anlagen-AfA-Buch erstellen** verwenden, um die Anwendung die erforderlichen AfA-Bücher automatisch erstellen zu lassen.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Anlage aus, die Sie einrichten möchten und der ein AfA-Buch zugewiesen werden soll, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie auf der Seite **AfA-Buch - Karte** die Aktion **Anlagen-AfA-Bücher erstellen** aus.
4. Füllen Sie auf der Seite **Anlagen-AfA-Buch erstellen** das Fenster **AfA-Buch** aus.
5. Klicken Sie im Feld **Kopieren von Anl.-Nr.** auf den AssistButton, und wählen Sie dann die Nummer der Anlage, die Sie als Basis für das neue AfA-Buch verwenden möchten.

    Wenn Sie dieses Feld ausfüllen, enthalten die Abschreibungsfelder in den neuen Anlagen-AfA-Büchern die gleichen Informationen wie die entsprechenden Felder im Anlagen-AfA-Buch, aus dem Sie kopieren. Lassen Sie dieses Feld leer, wenn Sie neue Anlagen-AfA-Bücher mit leeren Abschreibungsfeldern erstellen möchten.  
6. Im Inforegister **Anlage** können Sie einen Filter setzen, um die Anlagen auszuwählen, für die Sie Anlagen-AfA-Bücher erstellen wollen.
7. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-set-up-depreciation-posting-types"></a>So richten Sie AfA-Buchungsarten ein:
Für jedes AfA-Buch müssen Sie festlegen, wie die verschiedenen Buchungsarten in [!INCLUDE[prod_short](includes/prod_short.md)] verarbeitet werden sollen. Beispielsweise ob Buchungen Soll- oder Habenposten sein sollen und ob die Buchungsart in der AfA-Grundlage enthalten sein soll.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **AfA-Bücher** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, die Sie einrichten möchten und wählen Sie dann die Aktion **Anlagenbuchungsart Einr.** aus.
3. Füllen Sie auf der Seite **Anlagenbuchungsgruppenkarte einrichten** die notwendigen Felder aus.

    > [!NOTE]  
    >   Sie können auf der Seite **Anlagenbuchungsart Einr.** keine Zeilen löschen oder einfügen. Sie können nur die bestehenden Zeilen ändern.

Es wird empfohlen, die Einrichtung von AfA-Büchern, für die bereits Posten gebucht wurden, nicht zu ändern. Änderungen haben keinen Einfluss auf Posten, die bereits gebucht wurden, da andernfalls die Statistik für das AfA-Buch verfälscht würde.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>So richten Sie Standardvorlagen und -Standardstapelverarbeitungen für Anlagen-AfA ein
Sie können für jedes AfA-Buch Vorgaben für Vorlagen und Buch.-Blätter definieren. Sie nutzen diese Standards, um Zeilen aus einem Buch.-Blatt in ein anderes zu kopieren, wenn die Batchaufträge **AfA berechnen** oder **Anlagen indexieren** Buch.-Blattzeilen erstellen oder wenn Anschaffungskosten im Versicherungs Buch.-Blatt doppelt vorhanden sind.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **AfA-Bücher** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, für das Sie die Standardbuch.-Blätter festlegen möchten und wählen Sie dann die Aktion **Anlagen Buch.-Blatt Einr.** aus.  
3. Falls Sie eine Standardeinrichtung für jeden einzelnen Benutzer definieren möchten, wählen Sie die Seite **Benutzer-ID** aus, um über das Fenster **Benutzer** auszuwählen.  
4. Wählen Sie in den anderen Feldern die Buch.-Blattvorlage oder den Buch.-Blattnamen, die standardmäßig verwendet werden müssen.  

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]