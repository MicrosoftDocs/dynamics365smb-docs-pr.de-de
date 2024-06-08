---
title: Anlagen erwerben
description: 'Sie können Anlagen einrichten, ein AfA-Buch zuweisen und Anlagen-Anschaffungskosten aufzeichnen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="acquire-fixed-assets"></a>Anlagen erwerben

Verwenden Sie die Seite  **Anlagenkarte**, um Informationen zu einem Anlagegegenstand einzugeben. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Sie müssen für jedes Anlagevermögen ein Abschreibungsbuch einrichten und ihm zuweisen, bevor Sie es erwerben können.

Nachdem Sie eine Anlage eingerichtet und ein Abschreibungsbuch zugewiesen haben, müssen Sie die Anlage erwerben. Um eine Anlage zu erwerben, erfassen Sie seine Anschaffungskosten im entsprechenden Sachkonto, Bankkonto oder Kreditor, indem Sie eine Anschaffungstransaktion auf der Seite **Anlagen Fibu Buch.-Blatt** buchen. Sie können die Seite **Unterstützte Anlagenanschaffung** verwenden, um die erforderlichen Fibu Buch.-Blattzeilen automatisch zu erstellen und zu buchen.

Verwenden Sie die Indexierung, um Werte an allgemeine Preisniveauänderungen anzupassen. Mit der Stapelverarbeitung  **Anlagevermögen indexieren**  können Sie die Anschaffungs- und Wiederbeschaffungskosten berechnen.

## <a name="add-a-fixed-asset-to-your-list-of-fixed-assets"></a>Fügen Sie Ihrer Liste der Anlagegüter ein Anlagegut hinzu

Bevor Sie ein Anlagevermögen erwerben können, müssen Sie es Ihrem Anlagevermögen hinzufügen. Es gibt mehrere Möglichkeiten, Ihrer Liste Anlagevermögen hinzuzufügen:

* Geben Sie auf der Seite  **Anlagenkarte**  Informationen zu den Anlagen ein.
* Verwenden Sie die Aktion  **In Excel bearbeiten**, um Ihre Assetliste in ein Arbeitsblatt herunterzuladen, der Liste neue Assets hinzuzufügen und das Update dann zu veröffentlichen [!INCLUDE [prod_short](includes/prod_short.md)].
* Verwenden Sie eine Bestellung, um Vermögenswerte hinzuzufügen.
* Verwenden Sie die Aktion  **Anlagevermögen kopieren** .

Nachdem Sie Ihrer Liste Anlagevermögen hinzugefügt haben, besteht der nächste Schritt darin, es zu erwerben, damit Sie es in Transaktionen verwenden können. Weitere Informationen finden Sie unter  [Erwerb eines Anlagevermögens](#acquire-fixed-assets).

### <a name="add-a-fixed-asset-on-the-fixed-asset-card-page"></a>Fügen Sie auf der Seite „Anlagenkarte“ ein Anlagevermögen hinzu

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie dann bei Bedarf die Felder im Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus. Dieser Schritt weist eine Anlage einem AfA-Buch zu.  
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus. Weitere Informationen finden Sie unter  [So ordnen Sie einem Anlagevermögen ein Abschreibungsbuch zu](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Nachdem Sie die erforderlichen Felder ausgefüllt haben, **können Sie das Anlagevermögen erwerben.** Die Benachrichtigung wird oben auf der Seite angezeigt. Wenn Sie bereit sind, den Vermögenswert jetzt zu erwerben, wählen Sie die Aktion  **Erwerben** . Befolgen Sie die Schritte auf der Seite  **Unterstützter Erwerb von Anlagevermögen**, um den Erwerb abzuschließen. Wenn Sie noch nicht bereit sind, können Sie den Vermögenswert immer noch später erwerben.

### <a name="use-edit-in-excel-to-add-assets"></a>Verwenden Sie „In Excel bearbeiten“, um Assets hinzuzufügen

Wenn Sie zahlreiche Anlagegüter hinzufügen möchten, ist „In Excel bearbeiten“ ein hervorragendes Tool. Das Tool lädt Ihre aktuelle Anlagenliste in ein Arbeitsblatt herunter, das die meisten der auf der Seite „Anlagenkarte“ verfügbaren Felder enthält. Sie können für jedes Asset einige oder alle Felder in einer Zeile ausfüllen und Ihre Änderungen veröffentlichen, um sie Ihrer Liste in  [!INCLUDE [prod_short](includes/prod_short.md)] hinzuzufügen. Wenn Sie nicht alle erforderlichen Felder ausfüllen können, ist das in Ordnung. Sie können sie aktualisieren, [!INCLUDE [prod_short](includes/prod_short.md)] wenn Sie bereit sind.

> [!NOTE]
> Um die Aktion „In Excel bearbeiten“ zu verwenden, muss das  Microsoft Dynamics Office-Add-In installiert sein. Das Add-In stellt die Verbindung zwischen Excel und [!INCLUDE [prod_short](includes/prod_short.md)] her. Weitere Informationen finden Sie unter  [Business Central-Add-In für Excel herunterladen](admin-deploy-excel-addin.md).

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Symbol  :::image type="content" source="media/share-icon.png" alt-text="Diese Seite mit anderen Benutzern oder Apps teilen."::: Symbol und wählen Sie dann  **In Excel bearbeiten**.
3. Öffnen Sie die heruntergeladene Datei und geben Sie Informationen zu den neuen Anlagegütern ein.

   > [!TIP]
   > Die Eingabe einer Kennung in der  **Nr. ist nicht notwendig.** . Wenn Sie Ihr Update veröffentlichen, [!INCLUDE [prod_short](includes/prod_short.md)] weist es eine Kennung basierend auf der Nummernserie zu, die Sie für Anlagevermögen verwenden.

4. Zum Aktualisieren [!INCLUDE [prod_short](includes/prod_short.md)] wählen Sie im **Microsoft Dynamics** Bereich die Option **Veröffentlichen**.

### <a name="add-a-fixed-asset-from-a-purchase-order-or-invoice"></a>Hinzufügen eines Anlagevermögens aus einer Bestellung oder Rechnung

Die folgenden Schritte beschreiben, wie Sie ein Anlagevermögen aus einer Bestellung hinzufügen. Bei einer Einkaufsrechnung sind die Schritte ähnlich.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie  **Neu**, um eine neue Bestellung zu erstellen.
3. Füllen Sie im Inforegister **Allgemein** die notwendigen Felder aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. Wählen Sie auf der Registerkarte  **Zeilen**  im Feld  **Typ**  die Option  **Anlagevermögen** aus.
5. Geben Sie im Feld **Nr.** Wählen Sie im Feld entweder ein vorhandenes Anlagevermögen aus, um eine Ausgabe hinzuzufügen, oder wählen Sie  **Neu**, um ein neues Anlagevermögen hinzuzufügen.
6. Nachdem Sie die Informationen für das neue Anlagegut und die Bestellung eingegeben haben, wählen Sie  **Buchen**.

## <a name="acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal"></a>Erwerben Sie eine Anlage mithilfe eines Anlage-Fibujournals

Im folgenden Verfahren wird die Erfassung durch Erstellen und Buchen der erforderlichen Sachkonto-Journalzeilen für Anlagen beschrieben. Sie können die Buch.-Blattzeilen auch manuell erstellen und buchen. Weitere Informationen finden Sie unter  [Erwerben Sie ein Anlagevermögen mithilfe eines Anlagevermögen-Fibujournals](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
1. Wählen Sie den Vermögenswert aus, den Sie erwerben möchten, und wählen Sie dann die Aktion  **Erwerben** .
1. Befolgen Sie die Schritte auf der Seite  **Unterstützter Erwerb von Anlagevermögen**, um den Erwerb abzuschließen.

> [!NOTE]  
> Sie können Anchaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Anschaffungskosten inklusive MwSt** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

Wenn Sie „Fertig stellen“ **wählen, wird das Feld „Buchwert“** auf der Seite „Anlagenkarte“ **ausgefüllt. Dies gibt an, dass die Anlage zu den angegebenen Anschaffungskosten erworben wurde.**  **·**   

## <a name="to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal"></a>So buchen Sie eine Anlagenanschaffung manuell mit einem Anlagen Fibu Buch.-Blatt

Nachfolgend wird beschrieben, wie eine Anlage manuell erworben wird, indem Zeilen auf der Seite **Anlagen Fibu Buch.-Blatt** erstellt und gebucht werden. Sie können ein Anlagevermögen auch automatisch auf der Seite  **Anlagevermögenskarte**  erwerben, indem Sie die Aktion  **Anlagevermögen erwerben**  auswählen. Weitere Informationen finden Sie unter  [Anlagevermögen erwerben](#acquire-fixed-assets).

> [!NOTE]  
> Sie können Anchaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Betrag** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus Symbol. Geben Sie **Anlagen-Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.
2. auf der Seite **Anlagen Fibu Buch.-Blatt** wählen Sie im Feld **Anlagenbuchungsart** die **Anschaffungskosten** aus.
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.
4. Wählen Sie die Aktion **Buchen**.  

> [!TIP]  
> Wenn Sie das Feld  **Versicherungs-Nr.**  ausfüllen, [!INCLUDE[prod_short](includes/prod_short.md)] werden auch die Anschaffungskosten der Anlage in das Versicherungsdeckungsbuch gebucht. Weitere Informationen finden Sie unter  [Anlagevermögen versichern](fa-how-insure.md).

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>So richten Sie Komponentenlisten für Hauptanlagen ein

Sie können Ihre Anlagen in Hauptanlagen und deren Komponenten gliedern. Beispielsweise haben Sie möglicherweise eine Produktionsmaschine, die aus mehreren Teilen besteht, die Sie auf diese Weise gruppieren möchten.  

Sie müssen das Hauptvermögen und alle seine Komponenten als einzelnes Anlagevermögen einrichten. Nachdem Sie eine Komponentenliste eingerichtet haben, [!INCLUDE[prod_short](includes/prod_short.md)] werden die Felder  **Hauptanlagen/Komponenten**  und  **Komponenten der Hauptanlage**  im Anlagevermögen automatisch ausgefüllt.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage, die die Hauptanlage ist, und wählen die Aktion **Hauptanl. Unteranlagen** aus.
3. auf der Seite **Unteranlagen** wählen Sie **Anlagennr.** aus und wählen Sie die Anlage aus, die Sie als Komponente der Hauptanlage hinzufügen möchten.
4. Schließen Sie die Seite.
5. Wiederholen Sie die Schritte 3 und 4 für jede Unteranlage, die Sie hinzufügen möchten.
6. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlageneinrichtung** ein und wählen Sie dann den entsprechenden Link.
7. Aktivieren Sie den Schalter  **Buchungen in Hauptanlagen zulassen** .

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>So stornieren Sie eine Anschaffungskostenbuchung für eine Anlage

Wenn Ihnen beim Buchen von Anschaffungskosten ein Fehler unterläuft, können Sie den Posten mithilfe der Stapelverarbeitung **Anlagenposten storn.** entfernen und anschließend den korrekten Anschaffungsposten buchen. Die fehlerhaften Posten werden in die Seite **Anlagenstornoposten** übertragen.

Wenn Sie also beispielsweise eine Anschaffung mit dem falschen Datum gebucht haben, müssen Sie sie so schnell wie möglich korrigieren, da das Anlagenbuchungsdatum für viele Berechnungen verwendet wird.

> [!IMPORTANT]  
> Sie können die Aktion  **Transaktionen stornieren**  nicht für Anlagenposten verwenden.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Anlagenposten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Anlagenposten** den/die zu stornierenden Einträge aus.  
3. Wählen Sie das Menü **Aktionen** und dann die Aktion **Posten stornieren** aus.
4. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.
6. Wenn der falsche Posten oder die falschen Posten storniert wurden, können Sie mit dem Buchen der korrekten Anschaffungskosten fortfahren.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>So buchen Sie den Restbetrag zusammen mit den Anschaffungskosten

Der Restwert ist der verbleibende Wert einer Anlage, die nicht mehr verwendet werden kann. Sie können den Restbetrag zusammen mit den Anschaffungskosten buchen. Weitere Informationen finden Sie unter  [Abschreibung oder Amortisierung von Anlagevermögen](fa-how-depreciate-amortize.md).

Sie können den Restwert zusammen mit den Anschaffungskosten aus einem Anlagen Buch.-Blatt buchen.

> [!NOTE]
> Dieser Prozess erfordert möglicherweise, dass Sie die Seite Anlagenbuchhaltung personalisieren, indem Sie das Feld Restwert hinzufügen. Das Feld An wird auf der Seite standardmäßig nicht angezeigt. Weitere Informationen finden Sie unter  [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen-Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Anlagen Buch.-Blätter** erstellen Sie die Anschaffungszeile. Weitere Informationen finden Sie unter  [So buchen Sie eine Anlagenanschaffung manuell mit einem Anlagen-Fibujournal](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. Geben Sie im Feld **Restwert** in der Rechnungszeile den Restwertbetrag als Haben (Betrag mit einem Minuszeichen, z. B. **-** 100) ein.
4. Wählen Sie die Aktion **Buchen**.

> [!NOTE]
> Wenn für ein Anlagevermögen ein Restwert vorhanden ist, wird dieser Wert bei der Abschreibungsbuchung anstelle des Werts im Feld  **Endbuchwert**  auf der Seite  **FA-Abschreibungsbücher**  verwendet. Weitere Informationen finden Sie unter  [So verwalten Sie den Endbuchwert](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Einrichten von Anlagen](fa-setup.md)  
[Entwurfsdetails zu den Auswirkungen der nicht abzugsfähigen Mehrwertsteuer auf Anlagevermögen](design-details-nondeductible-vat.md)  
[Finanzen](finance.md)  
[Vorbereitung auf die Verwendung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
