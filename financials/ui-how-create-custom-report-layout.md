---
title: "Vorgehensweise: Erstellen Sie eine Zollerklärung oder ein Dokumentlayout | Microsoft Docs"
description: "Erfahren Sie, wie Sie gestalten können, wie Berichte aussehen"
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 79c1e5c1ea01077e2e5012ba07618760ccf2a4af
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Erstellen Sie einen benutzerdefinierten Bericht
<a id="how-to-create-a-custom-report-or-document-layout" class="xliff"></a>
Standardmäßig haben Berichte ein integriertes Berichtlayout, das entweder ein RDLC-Berichtlayout oder ein Word-Berichtlayout oder beides sein kann. Sie können keine integrierten Layouts ändern. Sie können jedoch Ihren eigenen benutzerdefinierten Layouts erstellen, die Ihnen ermöglichen, die Darstellung des Berichts zu ändern, wenn dieser angezeigt, gedruckt bzw. gespeichert wird. Sie können mehrere benutzerdefinierte Berichtslayouts für den gleichen Bericht erstellen und anschließend das Layout, das durch einen Bericht verwendet wird, nach Bedarf wechseln.

**Hinweis**: In [!INCLUDE[d365fin](includes/d365fin_md.md)], enthält der Begriff "Bericht" auch Externeinfassungsbelege, wie und Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Um ein benutzerdefiniertes Layout zu erstellen, können Sie entweder eine Kopie eines vorhandenen benutzerdefinierten Layouts erstellen oder ein neues benutzerdefiniertes Layout hinzufügen, das in den meisten Fällen auf einem integrierten Layout basiert. Wenn Sie ein neues kundenspezifisches Layout hinzufügen, können Sie wählen, einen RDLC-Berichtslayouttyp, Word-Berichtslayouttyp oder beide hinzuzufügen. Das neue benutzerdefinierte Layout basiert automatisch auf dem integrierten Layout des Berichts, falls einer verfügbar ist. Wenn für den Typ kein integriertes Layout verfügbar ist, wird ein neues leeres Layout erstellt, das Sie bearbeiten und von Grund auf neu entwerfen müssen. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Manage Report Layouts](ui-manage-report-layouts.md).  

## So erstellen Sie ein benutzerdefiniertes Layout
<a id="to-create-a-custom-layout" class="xliff"></a>
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Search for Page or Report icon")und geben **Bericht-Layout-Bereich**. Wählen Sie dann den zugehörigen Link aus.  
   In dem Fenster **Bericht-Layioutabschnitt** sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, das im Fenster Bericht-Layout-Auswahl oben verfügbar ist.
2. Legen Sie das Feld **Mandant** für den Mandanten fest, für den Sie das Berichtlayout erstellen möchten.
3. Wählen Sie im Fenster **Kundenspezifisches Layout** die Zeile für das benutzerdefinierte Layout, das Sie verwenden möchten, und wählen Sie dann die Schaltfläche OK aus.  
   Das Fenster **Benutzerdefiniertes Berichtslayout** erscheint und alle benutzerdefinierten Layouts, die für den ausgewählten Bericht verfügbar sind, werden angezeigt.
4. Wenn Sie eine Kopie eines vorhandenen benutzerdefinierten Layouts erstellen möchten, wählen Sie das vorhandene benutzerdefinierte Layout in der Liste aus, und dann wählen **Kopieren**.  
   Die Kopie des benutzerdefinierten Layouts erscheint im Fenster **Benutzerdefiniertes Layout** und hat den Begriff im Beschreibungsfeld.
5. Wenn Sie ein neues benutzerdefiniertes Layout hinzufügen möchten, das auf einem integrierten Layout basiert, führen Sie Folgendes aus:  
   1. Wählen Sie **Neu** aus. Das Fenster **Integriertes Layout für einen Bericht** erscheint. Die Felder **ID** und **Name** werden automatisch ausgefüllt.
   2. Um einen benutzerdefinierten WordBerichtlayouttyp hinzuzufügen, aktivieren Sie das **Word-Layout einfügen**-Kontrollkästchen.
   3. Um einen benutzerdefinierten RDLC-Berichtlayouttyp hinzuzufügen, aktivieren Sie das **RDLC-Layout einfügen**-Kontrollkästchen.
   4. Wählen Sie die Schaltfläche **OK** aus.  
      Die neuen benutzerdefinierten Layouts werden im Fenster **Benutzerdefinierte Berichtlayout** angezeigt. Wenn ein neues Layout auf einem integrierten Layout basiert, erscheinen die Begriffe **Kopie eines integrierten Layouts** im Feld **Beschreibung**. Wenn kein integriertes Layout für den Bericht vorhanden war, erhält das neue Layout die Begriffe **Neues Layout** im Feld **Beschreibung**, was angibt, dass das benutzerdefinierte Layout leer ist.
6. Standardmäßig ist das Feld **Unternehmensname** leer, d. h., dass das benutzerdefiniertes Layout für den Bericht in allen Unternehmen ist verfügbar. Um das benutzerdefinierte Layout nur in einem bestimmten Mandanten zu ändern, wählen Sie die Registerkarte **Bearbeiten**, und geben Sie dann im Feld **Unternehmensnamen** den Namen für den gewünschten Mandanten ein.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Vorgehensweise: Ändern, welches Layout zur Zeit in einem Bericht verwendet wird](ui-how-change-layout-currently-used-report.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

