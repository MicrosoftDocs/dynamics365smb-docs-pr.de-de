---
title: Arbeiten mit benutzerdefinierten und integrierten Layouts für Berichte und Belege | Microsoft Docs
description: Verwenden Sie Berichtslayouts, um Belege anzupassen beispielsweise um die gewünschten Schriftart, das Logo oder die Seiteneinstellungen von PDF-Dateien zu personalisieren, die Sie den Debitoren senden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 419c6d48d7370f7bcd6dc21c21ed3bd8d3833b00
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195461"
---
# <a name="managing-report-and-document-layouts"></a>Verwaltung von Berichts- und Beleg-Layouts
Ein Berichtlayout steuert Inhalt und Format des Berichts, auch, welche Datenfelder eines Berichtsdatasets im Bericht erscheinen und wie sie angeordnet werden, Text-Format, Bilder und mehr. Von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus können Sie ändern, welches Layout in einem Bericht verwendet wird, ein neues Layout erstellen oder vorhandene Layouts ändern.

> [!NOTE]  
>   In [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält der Begriff "Bericht" auch für extern bestimmte Dokumente wie Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Insbesondere richtet ein Berichtlayout Folgendes ein:

* Die Beschriftungs- und die Datenfelder, die aus dem Dataset des [!INCLUDE[d365fin](includes/d365fin_md.md)]-Berichts einzuschließen sind.
* Das Text-Format, wie Schriftarttyp, Größe und Farbe.
* Das Firmenlogo und seine Position.
* Allgemeine Seiteneinstellungen, wie Seitenränder und Hintergrundbilder.

Ein Bericht kann mit mehreren Berichtlayouts eingerichtet werden, die bei Bedarf ausgewechselt werden können. Sie können ggf. einen der integrierten Berichtlayouts verwenden, oder Sie können angepasste Berichtlayouts erstellen und sie Ihren Berichten nach Bedarf zuordnen. Weitere Informationen finden Sie unter [Erstellen Sie eines benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-create-custom-report-layout.md).

Es gibt zwei Arten Berichtlayouts, die Sie in Berichten verwenden können, Word und RDLC.

## <a name="word-report-layout-overview"></a>Word-Berichtlayout - Übersicht
Ein Word-Berichtlayout basiert auf einem Word-Dokument (DOCX-Datei-Typ). Word-Berichtslayouts ermöglichen es Ihnen, Berichtslayouts zu gestalten, indem Sie Microsoft Word 2013 oder höher verwenden. Ein Word-Berichtslayout bestimmt den Inhalt des Berichts und steuert, wie diese Inhaltselemente angeordnet werden und wie diese aussehen. Ein Word-Berichtlayoutbeleg verwendet normalerweise Tabellen, um Inhalt zu organisieren, wobei die Zellen Datenfelder, Text oder Bilder enthalten können.

 ![Beispiel eines Word-Berichtslayoutbelegs für NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>RDLC-Layout - Übersicht
RDLC-Layouts basieren auf Client-Berichtsdefinitionslayouts (.rdlc- oder .rdl-Dateitypen). Diese Layouts werden erstellt und geändert, indem Sie SQL Server-Bericht-Generator verwenden. Das Entwurfskonzept für RDLC-Layouts ist ähnlich den Word-Layouts, in denen das Layout das Muster des Berichts definiert und die Felder der Dataset bestimmt, die enthalten sein sollen. RDLC-Layouts bieten, verglichen mit Word-Layouts, eine größere Fülle an Funktionen und Gestaltungsmöglichkeiten. Weitere Informationen finden sie unter [RDLC-Berichtslayouts entwwerfen](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Integrierte und benutzerdefinierte Berichtslayouts
[!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst mehrere integrierte Layouts. Integrierte Layouts sind vordefinierte Layouts, die für bestimmte Berichte vorgesehen sind. [!INCLUDE[d365fin](includes/d365fin_md.md)]-Berichte haben ein integriertes Layout entweder als RDLC-Berichtslayout, Word-Berichtslayout oder in einigen Fällen beides. Sie können ein integriertes Berichtslayout aus dem [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht ändern, Sie können sie jedoch als Ausgangspunkt für das Erstellen Ihrer eigenen benutzerdefinierten Berichtslayouts verwenden.

Kundenspezifische Layouts sind Berichtslayouts, die Sie erstellen, um zdie Darstellung eines Berichts zu ändern. Sie erstellen normalerweise ein benutzerdefiniertes Layout basierend auf einem integrierten Layout, aber Sie können es von einer Kopie eines vorhandenen benutzerdefinierten Layouts von Grund auf neu erstellen. Benutzerdefinierete Layouts ermöglichen Ihnen, mehrere Layouts für den gleichen Bericht einzurichten, zwischen denen Sie nach Bedarf wechseln können. Beispielsweise können Sie verschiedene Layouts für jedes [!INCLUDE[d365fin](includes/d365fin_md.md)]-Unternehmen haben, oder Sie können verschiedene Layouts für das gleiche Unternehmen für bestimmte gelegenheiten oder Ereignisse verwenden, wie eine spezielle Kampagne oder eine Feiertagssaison haben.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Angeben, ob ein Word- oder RDLC-Berichtslayout verwendet werden soll
Ein Berichtlayout kann auf einem Word-Dokument oder RDLC-Datei basieren. Die Entscheidung, ob ein Word-Berichtslayout oder RDLC-Berichtslayout verwendet davon, hängt davon ab, wie der generierten Bericht aussehen soll, sowie von Ihren Kenntnissen in Word und dem SQL Server-Bericht-Generator.

Die allgemeinen Entwurfskonzepte für Word- und RDLC-Layouts sind sehr ähnlich. Jedoch hat jede Art bestimmte Design-Funktionalitäten, die beeinflussen, wie der generierte Bericht im [!INCLUDE[d365fin](includes/d365fin_md.md)]erscheint. Das bedeutet, dass derselbe Bericht möglicherweise bei Verwendung eines Word-Berichtslayout möglicherweise anders aussieht als bei einem RDLC-Berichtslayout.

Der Prozess für die Einrichtung von Word-Berichtslayouts und RDLC-Berichtslayouts in Berichten ist derselbe. Der wichtigste Unterschied besteht in der Art, wie die Sie die Layouts ändern. Word-Berichtslayouts sind in der Regel einfacher als RDLC-Berichtslayouts zu erstellen und zu ändern, da Sie Word bereits kennen. RDLC-Berichtslayouts werden geändert, indem Sie den SQL Server-Bericht-Generator verwenden, der für fortgeschrittene Benutzer entwickelt wurde.

Weitere Informationen darüber, wie das Layout, das verwendet wird, geändert werden kann, finden Sie unter [Aktuelles Berichtslayout ändern](ui-how-change-layout-currently-used-report.md).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Benutzerdefinierte Berichtslayouts aktualisieren](ui-update-report-layouts.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Importieren und Exportieren von einem benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-import-and-export-report-layout.md)  
[Spezielle Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit Berichten, Stapelverarbeitungen und XMLports](ui-work-report.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
