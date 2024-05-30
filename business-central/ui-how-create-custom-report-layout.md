---
title: Erstellen und Ändern von angepassten Layouts für Berichte und Belege
description: 'Erfahren Sie, wie Sie angepasste Layouts erstellen, um das Erscheinungsbild eines Berichts beim Anzeigen, Drucken oder Speichern zu personalisieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Legacy) Erstellen und Ändern benutzerdefinierter Berichtslayouts

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Berichte verfügen standardmäßig über ein integriertes Layout. Das Berichtslayout kann entweder ein RDLC-Berichtslayout (Report Definition Language Client Side), ein Microsoft Word Berichtslayout oder beides sein. Sie können zwar die integrierten Layouts nicht ändern, aber Sie können angepasste Layouts erstellen. Ein Bericht kann mehrere benutzerdefinierte Berichtslayouts haben.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] enthält der Begriff „Bericht“ auch für extern bestimmte Dokumente wie Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Um ein benutzerdefiniertes Layout zu erstellen, kopieren Sie entweder ein vorhandenes benutzerdefiniertes Layout, oder fügen Sie ein neues benutzerdefiniertes Layout hinzu. Benutzerdefinierte Layouts basieren häufig auf einem integrierten Layout. Wenn Sie ein neues angepasstes Layout hinzufügen, können Sie wählen, ob Sie entweder einen RDLC- oder einen Word-Berichtslayouttyp oder beides hinzufügen. Das neue angepasste Layout basiert auf dem integrierten Layout für den Bericht, sofern ein solches vorhanden ist. Wenn es kein eingebautes Layout für den Berichtstyp gibt, wird ein neues leeres Layout erstellt. Sie müssen dieses leere Layout von Grund auf ändern und gestalten. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Verwalten von Berichtslayouts](ui-manage-report-layouts.md).  

> [!TIP]
> Verwenden Sie Finanzberichte, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Erfahren Sie mehr unter [Bereiten Sie Finanzberichte mit Finanzdaten und Kontengruppen vor](bi-how-work-account-schedule.md).

Nachdem Sie Ihre benutzerdefinierte Berichtslayouts definiert haben, können Sie sie auf den Seiten „Debitorenkarte“ und „Kreditorenkarte“ auswählen. Die Layouts werden ann verwendet, wenn Sie Dokumente für den Debitor oder Kreditor erstellen. Erfahren Sie mehr unter [Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md).

Sie können auch benutzerdefinierte Berichtslayouts verwenden, um E-Mail-Nachrichten Inhalte hinzuzufügen. Berichtslayouts können Zeit sparen und zur Konsistenz beitragen, indem dieselben Inhalte wiederverwendet werden, wenn Sie mit Ihren Debitoren kommunizieren. Um benutzerdefinierte Berichtslayouts mit E-Mail verwenden zu können, muss der Dateityp für das Layout „Word“ sein. RDLC-Dateityp kann nicht verwendet werden. Erfahren Sie mehr unter [Wiederverwendbare E-Mail-Texte und -Layouts einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Benutzerdefiniertes Layout erstellen

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.

    In dem Feld **Unternehmesname** sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, die auf der Seite **Bericht-Layout-Auswahl** oben verfügbar ist.
2. Wählen Sie im Feld **Unternehmensname** das Unternehmen aus, für das Sie das Berichtlayout erstellen möchten.
3. Wählen Sie im Fenster **Debitorenspezifisches Layout** die Zeile für das benutzerdefinierte Layout, das Sie verwenden möchten, und wählen Sie dann die Schaltfläche OK aus.  

   Die Seite **Benutzerdefiniertes Berichtslayout** erscheint und alle benutzerdefinierten Layouts, die für den ausgewählten Bericht verfügbar sind, werden angezeigt.
4. Wenn Sie eine Kopie eines vorhandenen benutzerdefinierten Layouts erstellen möchten, wählen Sie das vorhandene benutzerdefinierte Layout in der Liste aus, und dann wählen **Kopieren**.  

   Die Kopie des benutzerdefinierten Layouts erscheint auf der Seite **Benutzerdefiniertes Layout** und hat den Begriff *Kopie von* im Feld **Beschreibung**.
5. Wenn Sie ein neues benutzerdefiniertes Layout hinzufügen möchten, das auf einem integrierten Layout basiert, führen Sie Folgendes aus:  
   1. Wählen Sie die Aktion **Neu**. Die Seite **Integriertes Layout für einen Bericht einfügen** erscheint mit den Feldern **ID** und **Name**, die automatisch ausgefüllt werden.
   2. Schalten Sie **Word-Layout einfügen** um, um einen benutzerdefinierten Layouttyp für Word-Berichte hinzuzufügen, ODER schalten Sie **RDLC-Layout einfügen** um, um einen benutzerdefinierten RDLC-Berichtslayouttyp hinzuzufügen.
   4. Wählen Sie die Schaltfläche **OK**.  

    Das neue angepasste Layout erscheint nun auf der Seite **Benutzerdefinierte Berichtslayouts**. Wenn ein neues Layout auf einem integrierten Layout basiert, erscheinen die Begriffe **Kopie eines integrierten Layouts** im Feld **Beschreibung**. Wenn kein integriertes Layout für den Bericht vorhanden war, erhält das neue Layout die Begriffe **Neues Layout** im Feld **Beschreibung**, was angibt, dass das benutzerdefinierte Layout leer ist.
6. Standardmäßig ist das Feld **Unternehmensname** leer, und das benutzerdefiniertes Layout ist für den Bericht in allen Unternehmen verfügbar. Um das benutzerdefinierte Layout nur in einem bestimmten Mandanten zu ändern, wählen Sie die Registerkarte **Bearbeiten**, und geben Sie dann im Feld **Unternehmensnamen** den Namen für den gewünschten Mandanten ein.

Das benutzerdefinierte Layout wurde erstellt und Sie können es nach Belieben ändern.

> [!TIP]
> Sie können die Berichtsergebnisse in eine Microsoft Excel-Datei exportieren, um das komplette Dataset einschließlich aller Spalten, aber ohne das Layout, zu betrachten. Die Excel-Datei kann Ihnen helfen, zu überprüfen, ob der Bericht die erwarteten Daten liefert, oder Probleme zu diagnostizieren. Weitere Informationen finden Sie unter [Analysieren von Berichtsdaten mit Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Ändern eines benutzerdefinierten Layouts

Um ein benutzerdefiniertes Berichtslayout zu ändern, müssen Sie das Berichtslayout zunächst als Datei an einen Lagerort auf Ihrem Computer oder im Netzwerk exportieren. Öffnen Sie dann den exportierten Beleg und nehmen Sie die Änderungen vor. Wenn Sie mit den Änderungen fertig sind, importieren Sie das Berichtslayout.

### <a name="modify-a-custom-layout"></a>Ändern eines benutzerdefinierten Layouts

1. Sie exportieren ein benutzerdefiniertes Layout aus der Seite **Benutzerdefinierte Berichtslayouts**. Wenn diese Seite nicht bereits geöffnet ist, suchen und öffnen Sie die Seite **Auswahl des Berichtslayouts**, wählen Sie den Bericht mit dem Layout, das Sie ändern möchten, und wählen Sie dann die Aktion **Angepasste Layouts**.  
2. Auf der Seite **Benutzerdefinierte Berichtslayouts** wählen Sie das Layout, das Sie ändern möchten, wählen Sie die **Layout exportieren** Aktion und wählen Sie dann **Speichern** oder **Speichern unter**, um den Berichtslayoutbeleg an einen Speicherort auf Ihrem Computer oder Netzwerk zu speichern aus.  
3. Öffnen Sie den Beleg für das Berichtslayout, den Sie gespeichert haben, und nehmen Sie dann die Änderungen vor.

   Wenn Sie ein Word-Layout ändern, öffnen Sie das Layout-Dokument in Word. Erfahren Sie mehr über das Bearbeiten von Word-Berichten unter [Arbeiten mit Word-Layouts](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-Berichtslayouts sind weiter entwickelter als Word-Berichtslayouts. Weitere Informationen zm Ändern eines RDLC-Berichtslayouts finden Sie unter [RDLC-Berichtslayout gestalten](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Denken Sie daran, Ihre Änderungen zu speichern, wenn Sie fertig sind.

4. Kehren Sie zur Seite **Benutzerdefinierte Berichtslayouts** zurück, das Berichtslayout, die Sie exportiert haben und geändert haben, und wählen die **Layout importieren** Aktion aus.  

5. Wählen Sie im Dialogfeld **Importieren** die Aktion **Auswählen**, um das geänderte Berichtslayout-Dokument zu suchen und auszuwählen, und wählen Sie dann **Öffnen**.

> [!IMPORTANT]
> Denken Sie daran, das geänderte Berichtslayout-Dokument zu importieren. Andernfalls wird das neue Berichtslayout nicht verfügbar sein.

<!--
## <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a>Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

### <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a>Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>To remove a label or data field

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### <a name="adding-data-fields"></a>Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-also"></a>Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Ändern Sie das aktuelle Berichtslayout](ui-how-change-layout-currently-used-report.md)  
[Importieren und Exportieren von einem benutzerdefinierten Berichts- oder Beleglayout](ui-how-import-and-export-report-layout.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Bereiten Sie Finanzberichte mit Finanzdaten und Kontengruppen vor](bi-how-work-account-schedule.md)  
[Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
