---
title: "Erstellen und bearbeiten von benutzerdefinierten Layouts für Berichte und Dokumente | Microsoft Docs"
description: "Sie können jedoch Ihren eigenen benutzerdefinierten Layouts erstellen, die Ihnen ermöglichen, die Darstellung des Berichts zu ändern, wenn dieser angezeigt, gedruckt bzw. gespeichert wird."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 14c2e5340c64e2b302a0bb04c54911888e995136
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-create-and-modify-a-custom-report-or-document-layout"></a>Vorgehensweise: Erstellen und bearbeiten Sie einen benutzerdefinierten Bericht
Standardmäßig haben Berichte ein integriertes Berichtlayout, das entweder ein RDLC-Berichtlayout oder ein Word-Berichtlayout oder beides sein kann. Sie können keine integrierten Layouts ändern. Sie können jedoch Ihren eigenen benutzerdefinierten Layouts erstellen, die Ihnen ermöglichen, die Darstellung des Berichts zu ändern, wenn dieser angezeigt, gedruckt bzw. gespeichert wird. Sie können mehrere benutzerdefinierte Berichtslayouts für den gleichen Bericht erstellen und anschließend das Layout, das durch einen Bericht verwendet wird, nach Bedarf wechseln.

> [!NOTE]  
>   In [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält der Begriff "Bericht" auch für extern bestimmte Dokumente wie Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Um ein benutzerdefiniertes Layout zu erstellen, können Sie entweder eine Kopie eines vorhandenen benutzerdefinierten Layouts erstellen oder ein neues benutzerdefiniertes Layout hinzufügen, das in den meisten Fällen auf einem integrierten Layout basiert. Wenn Sie ein neues kundenspezifisches Layout hinzufügen, können Sie wählen, einen RDLC-Berichtslayouttyp, Word-Berichtslayouttyp oder beide hinzuzufügen. Das neue benutzerdefinierte Layout basiert automatisch auf dem integrierten Layout des Berichts, falls einer verfügbar ist. Wenn für den Typ kein integriertes Layout verfügbar ist, wird ein neues leeres Layout erstellt, das Sie bearbeiten und von Grund auf neu entwerfen müssen. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Manage Report Layouts](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>So erstellen Sie ein benutzerdefiniertes Layout
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Berichtauswahl** ein. Wählen Sie dann den zugehörigen Link aus.

    In dem Fenster **Bericht-Layout-Auswahl** sind alle Berichte aufgelistet, die für das **Unternehmen** verfügbar sind
2. Legen Sie das Feld **Mandant** für den Mandanten fest, für den Sie das Berichtlayout erstellen möchten.
3. Wählen Sie im Fenster **Kundenspezifisches Layout** die Zeile für das benutzerdefinierte Layout, das Sie verwenden möchten, und wählen Sie dann die Schaltfläche OK aus.  
   Das Fenster **Benutzerdefiniertes Berichtslayout** erscheint und alle benutzerdefinierten Layouts, die für den ausgewählten Bericht verfügbar sind, werden angezeigt.
4. Wenn Sie eine Kopie eines vorhandenen benutzerdefinierten Layouts erstellen möchten, wählen Sie das vorhandene benutzerdefinierte Layout in der Liste aus, und dann wählen **Kopieren**.  
   Die Kopie des benutzerdefinierten Layouts erscheint im Fenster **Benutzerdefiniertes Layout** und hat den Begriff *Kopie von* im Feld **Beschreibung**.
5. Wenn Sie ein neues benutzerdefiniertes Layout hinzufügen möchten, das auf einem integrierten Layout basiert, führen Sie Folgendes aus:  
   1. Wählen Sie die Aktion **Neu** aus. Das Fenster **Integriertes Layout für einen Bericht** erscheint. Die Felder **ID** und **Name** werden automatisch ausgefüllt.
   2. Um einen benutzerdefinierten WordBerichtlayouttyp hinzuzufügen, aktivieren Sie das **Word-Layout einfügen**-Kontrollkästchen.
   3. Um einen benutzerdefinierten RDLC-Berichtlayouttyp hinzuzufügen, aktivieren Sie das **RDLC-Layout einfügen**-Kontrollkästchen.
   4. Wählen Sie die Schaltfläche **OK** aus.  
      Die neuen benutzerdefinierten Layouts werden im Fenster **Benutzerdefinierte Berichtlayout** angezeigt. Wenn ein neues Layout auf einem integrierten Layout basiert, erscheinen die Begriffe **Kopie eines integrierten Layouts** im Feld **Beschreibung**. Wenn kein integriertes Layout für den Bericht vorhanden war, erhält das neue Layout die Begriffe **Neues Layout** im Feld **Beschreibung**, was angibt, dass das benutzerdefinierte Layout leer ist.
6. Standardmäßig ist das Feld **Unternehmensname** leer, d. h., dass das benutzerdefiniertes Layout für den Bericht in allen Unternehmen ist verfügbar. Um das benutzerdefinierte Layout nur in einem bestimmten Mandanten zu ändern, wählen Sie die Registerkarte **Bearbeiten**, und geben Sie dann im Feld **Unternehmensnamen** den Namen für den gewünschten Mandanten ein.

Das benutzerdefinierte Layout wurde erstellt. Sie können das benutzerdefinierte Layout jetzt bei Bedarf ändern.

## <a name="ModifyCustomLayout"></a>Ändern eines benutzerdefinierten Layouts
Um ein Berichtslayout vom zu ändern, müssen Sie das Berichtslayout zunächst als Datei an einen Speicherort auf Ihrem Computer oder Netzwerk exportieren und dann das exportierte Dokument in Word öffnen und die gewünschten Änderungen vornehmen. Wenn Sie die Änderungen vorgenommen haben, importieren Sie das Berichtslayout.

### <a name="to-modify-a-custom-layout"></a>Ändern eines benutzerdefinierten Layouts
1.  Sie exportieren ein benutzerdefiniertes Layout aus dem Fenster **Benutzerdefinierte Berichtslayouts**. Wenn dieses Fensters nicht bereits geöffnet wurde, können Sie das Fenster **Auswahl des Berichtslayouts** öffnen, wählen den Bericht, der das Layout hat, das Sie ändern möchten und dann die Aktion **Benutzerdefinierte Layouts** auswählen.  
2.  Im Fenster **Benutzerdefinierte Berichtslayouts** wählen Sie das Layout, das Sie ändern möchten, wählen Sie die **Layout exportieren** Aktion und wählen Sie dann **Speichern** oder **Speichern unter**, um den Berichtslayoutbeleg an einen Speicherort auf Ihrem Computer oder Netzwerk zu speichern aus.  

3.  Öffnen Sie das Berichtslayout, das Sie gespeichert haben, und nehmen Sie die Änderungen vor.

      Wenn Sie ein Word-Layout ändern, öffnen Sie den Layoutbeleg in Word. Für das Bearbeiten von Details, finden Sie im nächsten Abschnitt [Vornehmen von Änderungen am Berichtslayout](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      RDLC-Berichtslayouts sind weiter entwickelter als Word-Berichtslayouts. Weitere Informationen zm Ändern eines RDLC-Berichtslayouts finden Sie unter [RDLC-Berichtslayout gestalten](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Denken Sie daran, nach Abschluss die Änderungen zu speichern.

4.  Kehren Sie zum Fenster **Benutzerdefinierte Berichtslayouts** zurück, das Berichtslayout, die Sie exportiert haben und geändert haben, und wählen die **Layout importieren** Aktion aus.  

5. Im **Importieren**-Dialogfeld **wählen** Sie das Dokument, das das Berichtlayout definiert, und wählen Sie dann **Öffnen**.

##  <a name="MakeChangesToLayout"></a> Durchführen von Änderungen eines bestehenden Berichtslayouts  
Wenn Sie Word-Berichtlayouts bearbeiten, um allgemeine Formatierungs- und Layoutänderungen zu ändern, wie zum Beispiel Änderung der Textschriftarts, Ändern einer Tabelle oder Entfernen eines Datenfelds, können Sie die grundlegenden Bearbeitungsfunktionen von Word verwenden, wie Sie es bei jedem Word-Dokument tun würden.

Wenn Sie ein Word-Berichtslayout von Grund aus neu entwerfen oder neue Datenfelder hinzufügen, dann starten Sie, indem Sie eine Tabelle hinzufügen, die Zeilen und Spalten enthält, die letztendlich die Datenfelder enthalten.

> [!TIP]  
>  Zeigen Sie die Tabellenrasterlinien an, sodass Sie die Grenzen von Tabellenzellen sehen. Denken Sie daran, die Rasterlinien auszublenden, wenn Sie mit der Bearbeitung fertig sind. Um Tabellenrasterlinien ein- oder auszublenden, wählen Sie die Tabelle und wählen Sie anschließend unter **Layout** auf der Registerkarte **Tabelle** die Option **Rasterlinien anzeigen** aus.  

###  <a name="RemoveField"></a> Entfernen der Beschriftungs- und der Datenfelder in Word-Layouts  
 Beschriftung und Datenfelder eines Berichts sind in Inhaltssteuerelementen in Word enthalten. In der folgenden Abbildung wird ein Inhaltssteuerelement dargestellt, wenn es im Word-Dokument ausgewählt ist.  

 ![Inhaltssteuerelement für Feld im Word-Berichtslayout](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Der Name der Bezeichnung oder des Datenfeldes wird im Inhaltssteuerelement angezeigt. In dem Beispiel ist der Name "CompanyAddr1".  

### <a name="to-remove-a-label-or-data-field"></a>Um eine Beschriftung oder ein Datenfeld zu entfernen  

1.  Klicken Sie mit der rechten Maustaste auf das Feld, das Sie entfernen möchten, und wählen Sie **Inhalt des Steuerelements löschen**.  

     Das Inhaltssteuerelement wird entfernt, aber die Feldnamen bleiben als Text erhalten.  

2.  Löschen Sie den verbleibenden Text nach Bedarf.  

### <a name="adding-data-fields"></a>Hinzufügen von Datenfeldern
Datenfelder aus einem Berichtsdataset hinzuzufügen, ist jedoch komplizierter und erfordert einiges Wissen über das Berichtsdataset. Informationen zum Hinzufügen von Feldern für Daten, werden Adressaufkleber, Daten und Bilder [Vorgehensweise: Fügen Sie einem Word-Berichtslayout Felder hinzu](ui-how-add-fields-word-report-layout.md).  


## <a name="see-also"></a>Siehe auch
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Vorgehensweise: Ändern, welches Layout zur Zeit in einem Bericht verwendet wird](ui-how-change-layout-currently-used-report.md)  
[Vorgehensweise: Importieren und Exportieren von einem benutzerdefinierten Bericht](ui-how-import-and-export-report-layout.md)  
[Arbeiten mit Berichten](ui-work-report.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

