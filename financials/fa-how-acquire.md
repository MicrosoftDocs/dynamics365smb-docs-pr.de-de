---
title: 'So geht''s: Anlagen anschaffen| Microsoft Docs'
description: Beschreibt, wie Sie eine Anlage erstellen und erwerben.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a16e62cf56abc7e3250f3406c1603185b26f677b
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Beschaffen von Anlagen
<a id="how-to-acquire-fixed-assets" class="xliff"></a>
Sie müssen für jede Anlage eine Karte mit entsprechenden Informationen zur Anlage einrichten. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Vor der Anschaffung muß für jede Anlage ein AfA-Buch eingerichtet und zugewiesen werden.

Wenn eine Anlage eingerichtet und ein AfA-Buch zugewiesen ist, müssen Sie die Anlage erwerben. Um eine Anlage zu erwerben, erfassen Sie seine Anschaffungskosten im entsprechenden Sachkonto, Bankkonto oder Kreditor, indem Sie eine Anschaffungstransaktion im Fenster **Anlagen Fibu Buch.-Blatt** buchen. Sie können das Fenster **Unterstützte Anlagenanschaffung** verwenden, um die erforderlichen Fibu Buch.-Blattzeilen automatisch zu erstellen und zu buchen.

Der Restwert ist der verbleibende Wert einer Anlage, die nicht mehr verwendet werden kann. Sie können den Restbetrag zusammen mit den Anschaffungskosten buchen. Weitere Informationen finden Sie unter [So geht's: Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md).

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die Anschaffungskosten zu Wiederbeschaffungskosten zu ermitteln.

## So erstellen Sie eine Anlage und erwerben diese automatisch
<a id="to-create-a-fixed-asset-and-acquire-it-automatically" class="xliff"></a>
Nachfolgend wird beschrieben, wie eine Anlage erstellt und erhalten wird, indem Sie das Fenster **Unterstützte Anlagenanschaffung** verwenden, um die entsprechenden Fibu Buch.-Blattzeilen zu erstellen und zu buchen. Sie können die Buch.-Blattzeilen auch manuell erstellen und buchen. Weitere Informationen finden Sie im Abschnitt "Wie Anlagenanschaffungen mit dem Anlagen Fibu Buch.-Blatt manuell gebucht werden".

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen** eingeben und den entsprechenden Link auswählen.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie dann bei Bedarf die Felder im Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus. Dieser Schritt weist eine Anlage einem AfA-Buch zu.  
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus. Weitere Informationen finden Sie im Abschnitt "So weisen Sie ein AfA-Buch einer Anlage zu" [So geht's: Einrichten von Anlagen-AfA-Büchern](fa-how-setup-depreciation.md).

    Wenn alle Felder, die benötigt werden, um eine Anlage zu erwerben, ausgefüllt sind, erscheint oben auf der Seite die Benachrichtigung **Sie sind bereit, die Anlage zu erwerben**.
5. Wählen Sie Aktion **Erwerben** in der Benachrichtigung aus.
6. Befolgen Sie die Schritte im Fenster **Unterstützte Anlagenanschaffung** Fenster, um die automatische Beschaffung der Anlage abzuschließen.

**Hinweis:** Sie können Anschaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Anschaffungskosten inklusive MwSt** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

Wenn Sie **Fertigstellen** auswählen, wird das Feld **Buchwert** im Fenster **Anlagenkarte** ausgefüllt und gibt an, dass die Anlage zu den angegebenen Anschaffungskosten erworben wurde.  

## So richten Sie Komponentenlisten für Hauptanlagen ein
<a id="to-set-up-a-component-list-for-a-main-asset" class="xliff"></a>
Sie können Ihre Anlagen in Hauptanlagen und deren Komponenten gliedern. Sie können dies z. B. für eine Produktionsanlage verwenden, die aus vielen Teilen besteht, die auf diese Weise gruppiert werden sollen.  

Sowohl für die Hauptanlage als auch für die Unteranlagen müssen Anlagenkarten eingerichtet werden. Nachdem Sie eine Komponentenübersicht eingerichtet haben, füllt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch die Felder **Hauptanlage/Komponente** und **Komponente/Hauptanlage** auf den Anlagenkarten aus.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen** eingeben und den entsprechenden Link auswählen.
2. Wählen Sie die Anlage, die die Hauptanlage ist, und wählen die Aktion **Hauptanl. Unteranlagen** aus.
3. Im Fenster **Hauptanl. Unteranlagen** wählen Sie das Feld **Anlagennr**. und wählen dann die Anlage aus, die Sie als Komponente der Hauptanlage hinzufügen möchten.
4. Schließen Sie das Fenster.
5. Wiederholen Sie die Schritte 3 und 4 für jede Unteranlage, die Sie hinzufügen möchten.
6. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen einrichten** eingeben und den entsprechenden Link auswählen.
7. Aktivieren Sie das Kontrollkästchen **Buchen auf Hauptanl. erlaubt**.

## So buchen Sie eine Anlagenanschaffungen mit dem Anlagen Fibu Buch.-Blatt manuell
<a id="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal" class="xliff"></a>
Nachfolgend wird beschrieben, wie eine Anlage manuell erworben wird, indem Zeilen im Fenster **Anlagen Fibu Buch.-Blatt** erstellt und gebucht werden. Sie können eine Anlage auch automatisch erwerben, indem Sie das Fenster **Unterstützte Anlagenanschaffung** verwenden. Weitere Informationen finden Sie unter Schritt 5 im Abschnitt "So erstellen Sie eine Anlage und erwerben diese automatisch".

**Hinweis:** Sie können Anschaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Betrag** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.
2. Im Fenster **Anlagen Fibu Buch.-Blatt** wählen Sie im Feld **Anlagenbuchungsart** die **Anschaffungskosten** aus.
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.
4. Wählen Sie die Aktion **Buchen** aus.  

**Tipp:** Wenn Sie das Feld **Versicherungsnr.** im Anlagen Fibu Buch.-Blatt ausfüllen, während Sie die Anschaffungskosten buchen, bucht [!INCLUDE[d365fin](includes/d365fin_md.md)] die Anschaffungskosten der Anlage auch für die Versicherungsposten. Weitere Informationen finden Sie unter [So geht's: Versichern von Anlagen](fa-how-insure.md).

## So stornieren Sie eine Anschaffungskostenbuchung für eine Anlage
<a id="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset" class="xliff"></a>
Wenn Ihnen beim Buchen von Anschaffungskosten ein Fehler unterläuft, können Sie den Posten mithilfe der Stapelverarbeitung **Anlagenposten storn.** entfernen und anschließend den korrekten Anschaffungsposten buchen. Die fehlerhaften Posten werden in das Fenster **Anlagenstornoposten** übertragen.

Wenn Sie also beispielsweise eine Anschaffung mit dem falschen Datum gebucht haben, müssen Sie sie so schnell wie möglich korrigieren, da das Anlagenbuchungsdatum für viele kritische Berechnungen verwendet wird.

**Wichtig:** Sie können die Funktion **Transaktion stornieren** nicht für Anlagenposten verwenden.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Anlageneintrag löschen** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.
4. Wenn der falsche Posten oder die falschen Posten storniert wurden, können Sie mit dem Buchen der korrekten Anschaffungskosten fortfahren.

Um Posten für mehrere Anlagen gleichzeitig abzubrechen, verwenden Sie die Stapelverarbeitung **Anlagenposten stornieren**.

## So buchen Sie den Restbetrag zusammen mit den Anschaffungskosten
<a id="to-post-the-salvage-value-together-with-the-acquisition-cost" class="xliff"></a>
Sie können den Restwert zusammen mit den Anschaffungskosten aus einem Anlagen Fibu Buch.-Blatt buchen.    

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Anlageneintrag löschen** ein und wählen Sie dann den entsprechenden Link aus.
2. Erstellen Sie eine Anschaffungs-Buch.-Blattzeile. Weitere Informationen finden Sie im Abschnitt "Wie Anlagenanschaffungen mit dem Anlagen Fibu Buch.-Blatt manuell gebucht werden".
3. Geben Sie im Feld **Restwert** in der Rechnungszeile den Restwertbetrag als Haben (mit einem Minuszeichen) ein.
4. Wählen Sie die Aktion **Buchen** aus.

**Hinweis:** Die Buchungsart **Restwert** steht nur im Fenster **Anlagen Buch.-Blatt** zur Verfügung. Sie ist im Fenster **Anlagen Fibu Buch.-Blatt** nicht verfügbar, weil der Restbetrag nie in der Finanzbuchhaltung gebucht wird.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

