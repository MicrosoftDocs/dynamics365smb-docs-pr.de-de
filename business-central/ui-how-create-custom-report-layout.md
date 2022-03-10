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
ms.openlocfilehash: 0b4642f6ca4c7701cbb49e8441debccfbd32b9be
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134717"
---
# <a name="create-and-modify-custom-report-layouts"></a>Erstellen und Ändern benutzerdefinierter Berichtslayouts

Standardmäßig haben Berichte ein integriertes Berichtlayout, das entweder ein RDLC-Berichtlayout oder ein Word-Berichtlayout oder beides sein kann. Sie können die integrierten Layouts nicht ändern. Aber Sie können Ihre eigenen angepassten Layouts erstellen, mit denen Sie das Aussehen eines Berichts ändern können, wenn er angezeigt, gedruckt oder gespeichert wird. Sie können mehrere benutzerdefinierte Berichtslayouts für den gleichen Bericht erstellen und anschließend das Layout, das durch einen Bericht verwendet wird, nach Bedarf wechseln.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] enthält der Begriff "Bericht" auch für extern bestimmte Dokumente wie Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Um ein angepasstes Layout zu erstellen, erstellen Sie entweder eine Kopie eines bestehenden angepassten Layouts oder Sie fügen ein neues angepasstes Layout hinzu, das allgemein auf einem eingebauten Layout basiert. Wenn Sie ein neues Debitorenspezifisches Layout hinzufügen, können Sie wählen, einen RDLC-Berichtslayouttyp, Word-Berichtslayouttyp oder beide hinzuzufügen. Das neue benutzerdefinierte Layout basiert automatisch auf dem integrierten Layout des Berichts, falls einer verfügbar ist. Wenn es kein eingebautes Layout für den Typ gibt, wird ein neues leeres Layout erstellt. Sie müssen dieses leere Layout von Grund auf ändern und gestalten. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Verwalten von Berichtslayouts](ui-manage-report-layouts.md).  

> [!TIP]
> Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Mehr Informationen finden Sie in [Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor](bi-how-work-account-schedule.md).

Wenn angepasste Berichtslayouts definiert sind, können Sie diese aus Kunden- und Kreditorenkarten auswählen, um festzulegen, dass die ausgewählten Layouts für Belege verwendet werden, die Sie für den betreffenden Kunden oder Kreditor erstellen. Weitere Informationen finden Sie unter [Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>So erstellen Sie ein benutzerdefiniertes Layout

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Auswahl des Berichtslayouts** ein und wählen Sie dann den entsprechenden Link.

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

1.  Sie exportieren ein benutzerdefiniertes Layout aus der Seite **Benutzerdefinierte Berichtslayouts**. Wenn diese Seite nicht bereits geöffnet ist, suchen und öffnen Sie die Seite **Auswahl des Berichtslayouts**, wählen Sie den Bericht mit dem Layout, das Sie ändern möchten, und wählen Sie dann die Aktion **Angepasste Layouts**.  
2.  Auf der Seite **Benutzerdefinierte Berichtslayouts** wählen Sie das Layout, das Sie ändern möchten, wählen Sie die **Layout exportieren** Aktion und wählen Sie dann **Speichern** oder **Speichern unter**, um den Berichtslayoutbeleg an einen Speicherort auf Ihrem Computer oder Netzwerk zu speichern aus.  

3.  Öffnen Sie den Beleg für das Berichtslayout, den Sie gespeichert haben, und nehmen Sie dann die Änderungen vor.

      Wenn Sie ein Word-Layout ändern, öffnen Sie das Layout-Dokument in Word. Für das Bearbeiten von Details, finden Sie im nächsten Abschnitt [Vornehmen von Änderungen am Berichtslayout](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      RDLC-Berichtslayouts sind weiter entwickelter als Word-Berichtslayouts. Weitere Informationen zm Ändern eines RDLC-Berichtslayouts finden Sie unter [RDLC-Berichtslayout gestalten](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Denken Sie daran, nach Abschluss die Änderungen zu speichern.

4.  Kehren Sie zur Seite **Benutzerdefinierte Berichtslayouts** zurück, das Berichtslayout, die Sie exportiert haben und geändert haben, und wählen die **Layout importieren** Aktion aus.  

5. Wählen Sie im Dialogfeld **Importieren** die Aktion **Auswählen**, um das geänderte Berichtslayout-Dokument zu suchen und auszuwählen, und wählen Sie dann **Öffnen**.

> [!IMPORTANT]
> Denken Sie daran, das geänderte Berichtslayout-Dokument zu importieren. Andernfalls wird das neue Berichtslayout nicht verfügbar sein.

##  <a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a> Erstellen und Ändern von benutzerdefinierten Berichtslayouts

Um allgemeine Formatierungs- und Layoutänderungen vorzunehmen, wie zum Beispiel Ändern der Schriftart, Hinzufügen und Ändern einer Tabelle oder Entfernen eines Datenfelds, können Sie einfach die grundlegenden Bearbeitungsfunktionen von Word verwenden, wie bei anderen Word-Dokumenten.

Wenn Sie ein Word-Berichtslayout von Grund auf neu entwerfen oder neue Datenfelder hinzufügen, dann beginnen Sie mit dem Hinzufügen einer Tabelle, die Zeilen und Spalten enthält, die später die Datenfelder enthalten werden.

> [!TIP]  
> Zeigen Sie die Tabellenrasterlinien an, sodass Sie die Grenzen von Tabellenzellen sehen. Denken Sie daran, die Gitternetzlinien auszublenden, wenn Sie mit der Bearbeitung fertig sind. Um Tabellenrasterlinien ein- oder auszublenden, wählen Sie die Tabelle und wählen Sie anschließend unter **Layout** auf der Registerkarte **Tabelle** die Option **Rasterlinien anzeigen** aus.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Schriftarten aus Gründen der Konsistenz in Word-Layouts einbetten

Um sicherzustellen, dass Berichte immer mit den vorgesehenen Schriftarten angezeigt und gedruckt werden, wo immer Benutzer die Berichte öffnen oder drucken, können Sie die Schriftarten in den Word-Beleg einbetten. Das Einbetten von Schriftarten kann jedoch die Größe der Word-Dateien erheblich erhöhen. Weitere Informationen zur Einbettung von Schriftarten in Word finden Sie unter [Einbetten von Schriftarten in Word, PowerPoint oder Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc)

###  <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a> Entfernen der Beschriftungs- und der Datenfelder in Word-Layouts

 Beschriftung und Datenfelder eines Berichts sind in Inhaltssteuerelementen in Word enthalten. Die folgende Abbildung zeigt ein Steuerelement für Inhalte, wenn es im Word-Beleg ausgewählt ist.  

 ![Inhaltssteuerelement für Feld in Word-Berichtslayout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Der Name der Bezeichnung oder des Datenfeldes wird im Inhaltssteuerelement angezeigt. In dem Beispiel ist der Name "CompanyAddr1".  

### <a name="to-remove-a-label-or-data-field"></a>Um eine Beschriftung oder ein Datenfeld zu entfernen  

1. Klicken Sie mit der rechten Maustaste auf das Feld, das Sie entfernen möchten, und wählen Sie **Inhalt des Steuerelements löschen**.  

     Das Inhaltssteuerelement wird entfernt, aber die Feldnamen bleiben als Text erhalten.  

2. Löschen Sie den verbleibenden Text nach Bedarf.  

### <a name="adding-data-fields"></a>Hinzufügen von Datenfeldern

Datenfelder aus einem Berichtsdataset hinzuzufügen, ist jedoch komplizierter und erfordert einiges Wissen über das Berichtsdataset. Informationen zum Hinzufügen von Feldern für Daten, werden Adressaufkleber, Daten und Bilder [Fügen Sie einem Word-Berichtslayout Felder hinzu](ui-how-add-fields-word-report-layout.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Ändern Sie das aktuelle Berichtslayout](ui-how-change-layout-currently-used-report.md)  
[Importieren und Exportieren von einem benutzerdefinierten Berichts- oder Beleglayout](ui-how-import-and-export-report-layout.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Bereiten Sie Finanzberichte mit Kontenschemata und Kontengruppen vor](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]