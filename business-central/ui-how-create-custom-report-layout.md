---
title: Erstellen und Ändern von angepassten Layouts für Berichte und Belege
description: Erfahren Sie, wie Sie angepasste Layouts erstellen, um das Erscheinungsbild eines Berichts beim Anzeigen, Drucken oder Speichern zu personalisieren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d629b2639325b95ab90db8aaf8ac9a3e5d51fc33
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511441"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>(Legacy) Erstellen und Ändern benutzerdefinierter Berichtslayouts

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Standardmäßig haben Berichte ein integriertes Berichtlayout, das entweder ein RDLC-Berichtlayout oder ein Word-Berichtlayout oder beides sein kann. Sie können die integrierten Layouts nicht ändern. Aber Sie können Ihre eigenen angepassten Layouts erstellen, mit denen Sie das Aussehen eines Berichts ändern können, wenn er angezeigt, gedruckt oder gespeichert wird. Sie können mehrere benutzerdefinierte Berichtslayouts für den gleichen Bericht erstellen und anschließend das Layout, das durch einen Bericht verwendet wird, nach Bedarf wechseln.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] enthält der Begriff "Bericht" auch für extern bestimmte Dokumente wie Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Um ein angepasstes Layout zu erstellen, erstellen Sie entweder eine Kopie eines bestehenden angepassten Layouts oder Sie fügen ein neues angepasstes Layout hinzu, das allgemein auf einem eingebauten Layout basiert. Wenn Sie ein neues Debitorenspezifisches Layout hinzufügen, können Sie wählen, einen RDLC-Berichtslayouttyp, Word-Berichtslayouttyp oder beide hinzuzufügen. Das neue benutzerdefinierte Layout basiert automatisch auf dem integrierten Layout des Berichts, falls einer verfügbar ist. Wenn es kein eingebautes Layout für den Typ gibt, wird ein neues leeres Layout erstellt. Sie müssen dieses leere Layout von Grund auf ändern und gestalten. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Verwalten von Berichtslayouts](ui-manage-report-layouts.md).  

> [!TIP]
> Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Mehr Informationen finden Sie in [Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor](bi-how-work-account-schedule.md).

Wenn angepasste Berichtslayouts definiert sind, können Sie diese aus Kunden- und Kreditorenkarten auswählen, um festzulegen, dass die ausgewählten Layouts für Belege verwendet werden, die Sie für den betreffenden Kunden oder Kreditor erstellen. Weitere Informationen finden Sie unter [Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>So erstellen Sie ein benutzerdefiniertes Layout

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.

    In dem Feld **Unternehmesname** sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, die auf der Seite **Bericht-Layout-Auswahl** oben verfügbar ist.
2. Legen Sie das Feld **Mandant** für den Mandanten fest, für den Sie das Berichtlayout erstellen möchten.
3. Wählen Sie im Fenster **Debitorenspezifisches Layout** die Zeile für das benutzerdefinierte Layout, das Sie verwenden möchten, und wählen Sie dann die Schaltfläche OK aus.  

   Die Seite **Benutzerdefiniertes Berichtslayout** erscheint und alle benutzerdefinierten Layouts, die für den ausgewählten Bericht verfügbar sind, werden angezeigt.
4. Wenn Sie eine Kopie eines vorhandenen benutzerdefinierten Layouts erstellen möchten, wählen Sie das vorhandene benutzerdefinierte Layout in der Liste aus, und dann wählen **Kopieren**.  

   Die Kopie des benutzerdefinierten Layouts erscheint auf der Seite **Benutzerdefiniertes Layout** und hat den Begriff *Kopie von* im Feld **Beschreibung**.
5. Wenn Sie ein neues angepasstes Layout hinzufügen möchten, das auf einem integrierten Layout basiert, führen Sie die folgenden Schritte aus:  
   1. Wählen Sie die Aktion **Neu**. Die Seite **Integriertes Layout für einen Bericht** erscheint. Die Felder **ID** und **Name** werden automatisch ausgefüllt.
   2. Um einen benutzerdefinierten WordBerichtlayouttyp hinzuzufügen, aktivieren Sie das **Word-Layout einfügen** Kontrollkästchen.
   3. Um einen benutzerdefinierten RDLC-Berichtlayouttyp hinzuzufügen, aktivieren Sie das **RDLC-Layout einfügen** Kontrollkästchen.
   4. Wählen Sie die Schaltfläche **OK**.  

    Das neue angepasste Layout erscheint nun auf der Seite **Benutzerdefinierte Berichtslayouts**. Wenn ein neues Layout auf einem integrierten Layout basiert, erscheinen die Begriffe **Kopie eines integrierten Layouts** im Feld **Beschreibung**. Wenn kein integriertes Layout für den Bericht vorhanden war, erhält das neue Layout die Begriffe **Neues Layout** im Feld **Beschreibung**, was angibt, dass das benutzerdefinierte Layout leer ist.
6. Standardmäßig ist das Feld **Unternehmensname** leer, d. h., dass das benutzerdefiniertes Layout für den Bericht in allen Unternehmen ist verfügbar. Um das benutzerdefinierte Layout nur in einem bestimmten Mandanten zu ändern, wählen Sie die Registerkarte **Bearbeiten**, und geben Sie dann im Feld **Unternehmensnamen** den Namen für den gewünschten Mandanten ein.

Das benutzerdefinierte Layout wurde erstellt. Sie können das benutzerdefinierte Layout jetzt bei Bedarf ändern.

> [!TIP]
> Sie können die Berichtsergebnisse in eine Excel-Datei exportieren, um das komplette Dataset einschließlich aller Spalten, aber ohne das Layout, zu betrachten. Die Excel-Datei kann Ihnen helfen, zu überprüfen, ob der Bericht die erwarteten Daten liefert, oder Probleme zu diagnostizieren. Weitere Informationen finden Sie unter [Analysieren von Berichtsdaten mit Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Ändern eines benutzerdefinierten Layouts

Um ein Berichtslayout zu ändern, müssen Sie das Berichtslayout zunächst als Datei an einen Lagerort auf Ihrem Computer oder im Netzwerk exportieren. Öffnen Sie dann den exportierten Beleg und nehmen Sie die Änderungen vor. Wenn Sie mit den Änderungen fertig sind, importieren Sie das Berichtslayout.

### <a name="to-modify-a-custom-layout"></a>Ändern eines benutzerdefinierten Layouts

1. Sie exportieren ein benutzerdefiniertes Layout aus der Seite **Benutzerdefinierte Berichtslayouts**. Wenn diese Seite nicht bereits geöffnet ist, suchen und öffnen Sie die Seite **Auswahl des Berichtslayouts**, wählen Sie den Bericht mit dem Layout, das Sie ändern möchten, und wählen Sie dann die Aktion **Angepasste Layouts**.  
2. Auf der Seite **Benutzerdefinierte Berichtslayouts** wählen Sie das Layout, das Sie ändern möchten, wählen Sie die **Layout exportieren** Aktion und wählen Sie dann **Speichern** oder **Speichern unter**, um den Berichtslayoutbeleg an einen Speicherort auf Ihrem Computer oder Netzwerk zu speichern aus.  
3. Öffnen Sie den Beleg für das Berichtslayout, den Sie gespeichert haben, und nehmen Sie dann die Änderungen vor.

   Wenn Sie ein Word-Layout ändern, öffnen Sie das Layout-Dokument in Word. Details zum Bearbeiten finden Sie unter [Mit Word-Layouts arbeiten](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   RDLC-Berichtslayouts sind weiter entwickelter als Word-Berichtslayouts. Weitere Informationen zm Ändern eines RDLC-Berichtslayouts finden Sie unter [RDLC-Berichtslayout gestalten](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Denken Sie daran, nach Abschluss die Änderungen zu speichern.

4. Kehren Sie zur Seite **Benutzerdefinierte Berichtslayouts** zurück, das Berichtslayout, die Sie exportiert haben und geändert haben, und wählen die **Layout importieren** Aktion aus.  

5. Wählen Sie im Dialogfeld **Importieren** die Aktion **Auswählen**, um das geänderte Berichtslayout-Dokument zu suchen und auszuwählen, und wählen Sie dann **Öffnen**.

> [!IMPORTANT]
> Denken Sie daran, das geänderte Berichtslayout-Dokument zu importieren. Andernfalls wird das neue Berichtslayout nicht verfügbar sein.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Ändern Sie das aktuelle Berichtslayout](ui-how-change-layout-currently-used-report.md)  
[Importieren und Exportieren von einem benutzerdefinierten Berichts- oder Beleglayout](ui-how-import-and-export-report-layout.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]