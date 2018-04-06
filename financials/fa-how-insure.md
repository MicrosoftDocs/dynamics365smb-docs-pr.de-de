---
title: Anlagen versichern| Microsoft Docs
Description: You can assign a fixed asset to an insurance policy, which is represented by an insurance card.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d5f3ef437e19ec037dc8f81aac6a8d283fc251a5
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="insure-fixed-assets"></a>Versichern von Anlagen
Eine Versicherungspolice für eine Anlage wird durch eine Versicherungskarte angezeigt. Sie können eine Anlage einer Versicherungspolice oder mehreren Anlagen einer Versicherungspolice zuzuordnen.

Sie ordnen einer Anlage einer Versicherungspolice zu, indem Sie sie im Versicherungsposten im Fenster **Versicherungs Buch.-Blatt** buchen.

Zudem können Sie eine Anlage einer Versicherungspolice zuzuordnen und Versicherungsposten erstellen, wenn Sie deren Anschaffungskosten buchen. Sie tun dies, indem Sie Anschaffungskosten aus dem Anlagen Buch.-Blatt buchen und das Feld **Versicherungsnr.** verwenden. Das Kontrollkästchen **Autom. Versicherungsbuchung** im Fenster **Anlageneinrichtung** muss aktiviert sein. Weitere Informationen finden Sie unter "Wie Anlagenanschaffungen mit dem Anlagen Fibu Buch.-Blatt manuell gebucht werden" [Anlagen erwerben](fa-how-acquire.md).

Wenn das Kontrollkästchen **Autom. Versicherungsbuchung** im Fenster **Anlageneinrichtung** nicht ausgewählt ist, werden beim Buchen von Anschaffungen Zeilen im Fenster **Versicherung Buch.-Blatt** erstellt, die Sie dann manuell buchen müssen.

> [!WARNING]  
>   Wenn Sie das Kontrollkästchen **Autom. Versicherungsbuchung** im Fenster **Anlageneinrichtung** auswählen, dann sollte das Versicherungs Buch.-Blatt auf einer Buch.-Blattvorlage ohne Nummernserie basieren. Der Grund dafür ist, dass die eingefügten Belegnummern aus der Buch.-Blattzeile andernfalls einen Konflikt mit der Nummernserie des Versicherungs Buch.-Blattes verursachen. Weitere Informationen über Buch.-Blattvorlagen und Buch.-Blattstapel finden Sie unter [Einrichten allgemeiner Anlagen-Informationen](fa-how-setup-general.md).

Nachdem Sie eine Anlage einer Versicherungspolice zugewiesen haben, wird das Kontrollkästchen **Versichert** auf der Anlagenkarte aktiviert. Wenn Sie die Anlage verkaufen, wird das Kontrollkästchen automatisch deaktiviert.

## <a name="to-create-or-modify-an-insurance-card"></a>So erstellen oder ändern Sie eine Versicherungskarte
Eine Versicherungspolice für eine Anlage muß durch eine Versicherungskarte angezeigt werden.

Wenn Sie Informationen über Änderungen der Deckungssumme erhalten, müssen Sie diese im Fenster **Versicherungskarte** aktualisieren, um sicherzustellen, dass Sie die Versicherungsdeckung korrekt analysieren.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Versicherung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, um eine neue Karte für eine Versicherungspolice zu erstellen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Versicherungspolice, die Sie ändern möchten, und wählen die Aktion **Bearbeiten** aus.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal"></a>So verknüpfen Sie eine Anlage mit einer Versicherungspolice durch Buchen aus einem Versicherungs Buch.-Blatt
Sie verknüpfen eine Anlage mit einer Versicherungspolice, indem Sie sie in den Versicherungsposten buchen.  

Nachfolgend wird beschrieben, wie Sie eine Versicherungs Buch.-Blattzeile manuell erstellen. Wenn das Kontrollkästchen **Autom. Versicherungsbuchung** im Fenster **Anlageneinrichtung** ausgewählt wird, werden Versicherungs Buch.-Blattzeilen automatisch erstellt, wenn Sie Anschaffungskosten buchen. In diesem Fall müssen Sie nur das Buch.-Blatt buchen.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versicherung buchen** ein und wählen den zugehörenden Link aus.  
2. Öffnen Sie das relevante Buch.-Blatt und füllen Sie die Buch.-Blattzeilen nach Bedarf aus.  
3. Um mehrere Anlagen einer Versicherungspolice zuzuweisen, können Sie Buch.-Blattzeilen mit dem gleichen Wert im Feld **Versicherungsnr** und unterschiedliche Werte im Feld **Anlagennr.**  
4. Wählen Sie die Aktion **Buchen** aus.  

    > [!NOTE]  
>   Die Posten aus dem Versicherungs Buch.-Blatt werden nur auf die Versicherungsposten gebucht.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset"></a>So aktualisieren Sie den Versicherungswert einer Anlage
Sie können die Stapelverarbeitung **Indexiere Versicherung** verwenden, um den Wert der versicherten Anlagen zu aktualisieren.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versicherung indexieren** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus.

    > [!NOTE]  
>   Im Feld **Indexzahl** wird eine Senkung um 5 % beispielsweise als "95" eingegeben, während eine Steigerung von 2 % als "102" eingegeben wird.  
3. Wählen Sie die Schaltfläche **OK** aus.  

   Die Stapelverarbeitung berechnet den neuen Betrag als Prozentsatz des gesamten versicherten Wertes aus dem Fenster **Versicherungsstatistik** und erstellt dann eine Zeile im Vers. Buch.-Blatt.  
4. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versicherung buchen** ein und wählen den zugehörenden Link aus.  
5. Öffnen Sie das relevante Versicherungs Buch.-Blatt, prüfen Sie die erstellten Posten und buchen Sie diese dann auf die Versicherungsposten.  

## <a name="to-monitor-insurance-coverage"></a>So überwachen Sie die Versicherungsdeckung
[!INCLUDE[d365fin](includes/d365fin_md.md)] bietet dedizierte Berichte und Statistikfenster, die dazu verwendet werden können, Versicherungspolicen zu analysieren und zu überprüfen, ob Ihre Anlagen über- oder unterversichert sind.  

### <a name="overview-of-insurance-policies"></a>Übersicht der Versicherungspolicen
Gibt einen Überblicks über die Versicherungspolicen durch Drucken des Berichts **Versicherung-Liste**. Der Bericht zeigt die einzelnen Policen und die wichtigsten Felder der Versicherungskarten an.  

### <a name="insurance-coverage"></a>Versicherungsdeckung
Um zu sehen, welche Versicherungspolicen welche Anlagen in welcher Höhe abdecken, können Sie den Bericht **Versicherung – Vers. Summe** ausdrucken oder anzeigen.  

### <a name="overunder-coverage"></a>Unter-/Überversicherung
Folgendermaßen können Sie prüfen, ob Anlagen über- oder unterversichert sind:  

* Das Fenster **Versicherungsstatistik**. Ein positiver Betrag in dem Feld **Über-/Unterversichert** bedeutet, dass die Anlage überversichert ist. Ein negativer Betrag zeigt eine Unterversicherung an.  
* Das Fenster **Anlagenstatistik**. Wählen Sie das Feld **Versicherte Summe**, um das Fenster **Versicherungsposten** anzuzeigen.  
* Der Bericht **Unter-/Überversicherung**.  
* Der Bericht **Versicherungsanalyse**.  

### <a name="uninsured-fixed-assets"></a>Unversicherte Anlagen
Um zu prüfen, ob Sie vergessen haben, eine Anlage einer Versicherungspolice zuzuweisen, können Sie den Bericht **Versicherung - Unvers. Anlagen** drucken oder anzeigen. Dieser Bericht zeigt Anlagen an, für die noch keine Beträge in den Versicherungsposten gebucht wurden.  

## <a name="to-view-insurance-coverage-ledger-entries"></a>So zeigen Sie Versicherungsposten an
Sie können sich die einzelnen Posten anzeigen lassen, die Sie in den Versicherungsposten erstellt haben.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Versicherung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Versicherungspolice aus, und wählen Sie dann die Aktion **Versicherungsposten**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets"></a>So zeigen Sie den gesamten Versicherungswert von Anlagen an:
Ein dediziertes Matrixfenster zeigt die Versicherungswerte jeder Anlage und jeder Versicherungspolice als Ergebnis der versicherungsbezogenen Beträge an, die von Ihnen gebucht wurden.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Versicherung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Versicherungspolice aus, und wählen Sie dann die Aktion **Versicherte Summe pro Anlage**.  
3. Füllen Sie die Felder je nach Bedarf aus.  
4. Wählen Sie die Aktion **Matrix anzeigen** aus.  
5. Um die zu Grunde liegenden Versicherungsposten anzuzeigen, aktivieren Sie einen Wert in der Matrix.  

## <a name="to-correct-insurance-coverage-entries"></a>So korrigieren Sie Versicherungsposten
Wenn eine Anlage der falschen Versicherung zugeordnet wurde, können Sie diese korrigieren, indem Sie zwei Umbuchungsposten aus dem Versicherungs Buch.-Blatt erstellen.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versicherung buchen** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine Buch.-Blattzeile für die Anlage und die korrekte Versicherungspolice, in der der Wert im Feld **Betrag** positiv ist.  
3. Erstellen Sie eine weitere Buch.-Blattzeile für die Anlage und die inkorrekte Versicherungspolice, in der der Wert im Feld **Betrag** negativ ist.  
4. Wählen Sie die Aktion **Buchen** aus.  

Die Verknüpfung der Anlage mit der falschen Versicherung der zweiten Zeile wird aufgehoben und stattdessen eine Verknüpfung mit der richtigen Versicherung aus der ersten Zeile erstellt.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

