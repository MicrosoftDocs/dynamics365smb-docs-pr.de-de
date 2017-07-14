---
title: "Vorgehensweise: Ändern, welches Layout zur Zeit in einem Bericht verwendet wird| Microsoft Docs"
description: "Erfahren Sie, wie Sie gestalten können, wie Berichte aussehen."
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
ms.openlocfilehash: c35611a74e981367170bc487a107777d2ba240f2
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Ändern, welches Layout zur Zeit in einem Bericht verwendet wird
<a id="how-to-change-which-layout-is-currently-used-on-a-report" class="xliff"></a>
Ein Bericht kann mit mehreren Berichtlayouts eingerichtet werden, die bei Bedarf ausgewechselt werden können.

Abhängig von den Layouts, die für einen Bericht verfügbar sind, können Sie ein integriertes RDLC-Berichtlayout, ein integriertes Word-Berichtlayout oder ein kundenspezifisches Layout verwenden. Weitere Informationen zu RDLC- und Word-Berichtlayouts, integrierten und benutzerdefinierten Layouts und mehr finden Sie unter [Manage Report Layouts](ui-manage-report-layouts.md).

## Um das Layout ändern, das in einem Bericht verwendet wird
<a id="to-change-the-layout-that-is-used-on-a-report" class="xliff"></a>
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Search for Page or Report icon")und geben **Bericht-Layout-Bereich**. Wählen Sie dann den zugehörigen Link aus.  
   In dem Fenster sind alle Berichte aufgelistet, die für das Unternehmen verfügbar sind, das im Fenster **Bericht-Layout-Auswahl** oben verfügbar ist. Das ausgewählte Layout-Feld gibt das Layout an, das momentan in dem Bericht verwendet wird.
2. Legen Sie das Feld **Unternehmen** oben im Fenster auf das Unternehmen fest, das den Bericht umfasst.
3. Um das Layout, das von einem Bericht verwendet wird, zu ändern, wählen Sie die Zeile für den Bericht aus der Liste, und legen Sie dann das Feld **Ausgewähltes Layout** auf eine der folgenden Optionen fest:
   * RDLC (integriert) verwendet im Bericht das integrierte RDLC-Berichtlayout.
   * Word (integriert) verwendet im Bericht das integrierte Word-Berichtlayout.
   * Benutzerdefiniert, verwendet ein kundenspezifisches Layout im Bericht.  
     Sie können sehen, welche benutzerdefinierten Layouts für den Bericht in der Infobox verfügbar sind. Falls es keine benutzerdefinierten Layouts für den Bericht gibt, müssen Sie zunächst welche erstellen. Wenn Sie diese Option auswählen, gehen Sie zum folgenden Verfahren, um das benutzerdefinierte Layout anzugeben, die Sie verwenden möchten.
     **Hinweis**: Wenn Sie **RDLC (integriert)** oder **Word (integriert)** auswählen und Sie eine Fehlermeldung erhalten, dass der Bericht kein Layout der angegebenen Art hat, müssen Sie eine andere Darstellungsoption auswählen oder ein kundenspezifisches Berichtlayout der Art erstellen, die Sie verwenden möchten.

Wenn Sie ein inztegriertes RDLC- oder Word-Berichtslayout ausgewählt haben, ist keine weitere Aktionen erforderlich, und das Layout wird verwendet, wenn der Bericht zum nächsten Mal ausgeführt wird.

## Um ein kundenspezifisches Layout in einem Bericht festzulegen
<a id="to-specify-a-custom-layout-on-a-report" class="xliff"></a>
1. Sie bestimmen, welches benutzerdefinierte Layout im Bericht aus dem Fenster **Kundenspezifischen Berichtlayout**-verwendet werden soll. Wenn das Fenster **Kundenspezifisches Layout** nicht offen ist, dann wählen Sie im Feld **Berichtlayout-Beschreibung** die Suchschaltfläche aus.
2. Wählen Sie im Fenster **Kundenspezifisches Layout** die Zeile für das benutzerdefinierte Layout, das Sie verwenden möchten, und schließen Sie dann das Fenster.

Sie kehren zum Fenster **Berichtslayout-Auswahl** zurück. Der Name des ausgewählten benutzerdefinierten Layouts wird im Feld **Benutzerdefinierte Beschreibung** angezeigt. Das benutzerdefinierte Layout wird das nächste Mal verwendet, wenn Sie den Bericht ausführen.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

