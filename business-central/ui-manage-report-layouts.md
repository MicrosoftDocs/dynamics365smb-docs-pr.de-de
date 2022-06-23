---
title: Verwaltung von Berichts- und Beleg-Layouts
description: Verwenden Sie Berichtslayouts, um Belege anzupassen beispielsweise um die gewünschten Schriftart, das Logo oder die Seiteneinstellungen von PDF-Dateien zu personalisieren, die Sie den Debitoren senden.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: fa615d3e0753b7f1aa9cd602168a393849765079
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950225"
---
# <a name="report-and-document-layouts-overview"></a>Berichts- und Beleg-Layouts – Überblick

Ein Berichtlayout steuert Inhalt und Format des Berichts, auch, welche Datenfelder eines Berichtsdatasets im Bericht erscheinen und wie sie angeordnet werden, Text-Format, Bilder und mehr. Von [!INCLUDE[prod_short](includes/prod_short.md)] aus können Sie ändern, welches Layout in einem Bericht verwendet wird, ein neues Layout erstellen oder vorhandene Layouts ändern.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] enthält der Begriff "Bericht" auch für extern bestimmte Dokumente wie Verkaufsrechnungen und Bestellungbestätigungen, die Sie den Debitoren als PDF-Dateien senden.

Sie können auchBerichtslayouts verwenden, um E-Mail-Nachrichten Inhalte hinzuzufügen. Berichtslayouts können beispielsweise Zeit sparen und zur Konsistenz beitragen, indem dieselben Inhalte wiederverwendet werden, wenn Sie mit Ihren Debitoren kommunizieren. Um benutzerdefinierte Berichtslayouts mit E-Mail verwenden zu können, muss der Dateityp für das Layout „Word“ sein. Der Dateityp „RDLC“ kann nicht verwendet werden. Weitere Informationen finden Sie unter [Wiederverwendbare E-Mail-Texte und -Layouts einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="introduction"></a>Einführung

Insbesondere richtet ein Berichtlayout folgende Dinge ein:

* Die Beschriftungs- und die Datenfelder, die aus dem Dataset des [!INCLUDE[prod_short](includes/prod_short.md)]-Berichts einzuschließen sind.
* Das Text-Format, wie Schriftarttyp, Größe und Farbe.
* Das Firmenlogo und seine Position.
* Allgemeine Seiteneinstellungen, wie Seitenränder und Hintergrundbilder.

Ein Bericht kann mit mehreren Berichtlayouts eingerichtet werden, die bei Bedarf ausgewechselt werden können. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Es gibt zwei wichtige Aspekte von Berichtslayouts, die beeinflussen, wie Sie damit arbeiten: der *Layouttyp* und die *Layout-Quelle*. Der Layouttyp gibt die Art der Datei an, auf der das Layout basiert. Die Layoutquelle gibt die Herkunft des Layouts an.

## <a name="layout-types"></a>Layouttypen

Es gibt vier Arten Layouts, die Sie in Berichten verwenden können: Word, RDLC, Excel und extern.

### <a name="word"></a>Word

Word-Layouts basieren auf Word-Dokumenten (DOCX-Dateityp). Mit Word-Layouts können Sie Berichtslayouts entwerfen, indem Sie Microsoft Word verwenden. Ein Word-Layout bestimmt den Inhalt des Berichts und steuert, wie diese Inhaltselemente angeordnet werden und wie diese aussehen. Ein Word-Layoutbeleg verwendet normalerweise Tabellen, um Inhalt zu organisieren, wobei die Zellen Datenfelder, Text oder Bilder enthalten können.

[![Beispiel für einen Word-Berichtslayout-Dokument für Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Weitere Informationen finden Sie unter [Mit Word-Layouts arbeiten](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a>Excel

Excel-Layouts basieren auf Microsoft Excel-Arbeitsmappen (.xlsx-Dateityp). Damit können Sie Berichte erstellen, indem Sie vertraute Excel-Funktionen zum Zusammenfassen, Analysieren und Präsentieren von Daten mit Tools wie Formeln, PivotTables, PivotCharts und mehr verwenden.

[![Zeigt ein Beispiel für ein Excel-Layout.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Weitere Informationen finden Sie unter [Mit Excel-Layouts arbeiten](ui-excel-report-layouts.md).

### <a name="rdlc"></a>RDLC

RDLC-Layouts basieren auf Layoutdateien für Client-Berichtsdefinitionen (.rdl- oder .rdlc-Dateitypen). Diese Layouts werden erstellt und geändert, indem Sie SQL Server Report Builder oder Microsoft RDLC Report Designer verwenden. Das Designkonzept für RDLC-Layouts ähnelt Word-Layouts, bei denen das Layout bestimmt, welche Felder angezeigt werden und wie sie angeordnet sind. Allerdings ist der Entwurf von RDLC-Layouts weiter fortgeschritten als bei Word-Layouts.

[![Zeigt ein Beispiel für ein RDLC-Layout.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Weitere Informationen finden Sie unter [Mit RDLC-Layouts arbeiten](ui-rdlc-report-layouts.md).

### <a name="external"></a>Extern

Ein externer Layouttyp bezieht sich auf einen erweiterten Typ, der speziell für bestimmte Berichte entwickelt wurde. Die Berichte und die Layouts selbst werden in der Regel von Partnern und nicht von Microsoft bereitgestellt. Der tatsächliche Dateityp des Layouts variiert je nach Anbieter.

Weitere Informationen finden Sie unter [Entwickeln eines benutzerdefinierten Berichts-Renders](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources"></a>Layoutquellen

Zusätzlich zum Typ werden Layouts basierend auf ihrer Quelle oder Herkunft weiter in drei Kategorien unterteilt.

* Erweiterungslayouts

   Erweiterungslayouts sind Layouts, die Teil einer Erweiterung sind, die in der Umgebung installiert wurde. Diese Layouts sind typischerweise Standardlayouts, die beispielsweise von Microsoft in der Basisanwendung bereitgestellt werden. Oder es könnten Layouts sein, die in Erweiterungen anderer Softwareanbieter enthalten sind. Erweiterungslayouts erkennen Sie auf der **Berichtslayouts**-Seite, da der Name der Erweiterung und der Herausgeber in der **Erweiterung**-Spalte angezeigt werden.

* Benutzerdefinierte Layouts

   Die andere Quelle für Layouts ist der Endbenutzer. Innerhalb von Business Central kann ein Benutzer mit den entsprechenden Berechtigungen auf verschiedene Arten neue Layouts hinzufügen. Sie könnten beispielsweise mit einem vorhandenen Erweiterungslayout oder einem anderen benutzerdefinierten Layout beginnen. Auf der Seite **Berichtslayouts** ist die **Erweiterung**-Spalte bei benutzerdefinierten Layouts leer.

   Weitere Informationen finden Sie unter [Erstel Schritte mit der Erstellung von Berichtslayouts](ui-get-started-layouts.md).

* Benutzerdefinierte Layouts

  Benutzerdefinierte Layouts sind auch Layouts, die von Benutzern erstellt werden. Der Unterschied besteht darin, dass diese Layouts auf der Legacy **Benutzerdefinierte Berichtslayouts**-Seite erstellt werden, und sie können nur vom Typ Word und RDLC sein. Sie können zwar weiterhin benutzerdefinierte Layouts erstellen, diese werden jedoch zugunsten benutzerdefinierter Layouts eingestellt.

  Weitere Informationen finden Sie unter [(Legacy) Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).

Informationen, die Ihnen bei der Entscheidung helfen, welcher Typ für Sie am besten geeignet ist, finden Sie unter[ Entscheiden, welche Art von Layout Sie möchten](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Beachten Sie unbedingt, dass Sie Erweiterungslayouts nicht vom Business Central-Client aus ändern können. Beispielsweise ist es Ihnen nicht gestattet, den Namen oder Typ des Layouts zu ändern oder es hochzuladen und durch eine andere Version zu ersetzen. Wenn Sie es versuchen, erhalten Sie eine Fehlermeldung. Sie müssen stattdessen ein benutzerangepasstes oder benutzerdefiniertes Layout basierend auf dem Erweiterungslayout erstellen.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Benutzerdefinierte Berichtslayouts aktualisieren](ui-update-report-layouts.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Importieren und Exportieren von einem benutzerdefinierten Berichts- oder Dokumentenlayout](ui-how-import-and-export-report-layout.md)  
[Spezielle Beleglayouts für Debitoren und Kreditoren definieren](ui-define-customer-vendor-document-layouts.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]