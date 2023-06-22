---
title: Arbeiten mit RDLC-Layouts
description: Erhalten Sie eine Einführung in RDLC-Berichtslayouts.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# <a name="working-with-rdlc-layouts" />Arbeiten mit RDLC-Layouts

RDLC-Layouts basieren auf Layoutdateien für Client-Berichtsdefinitionen (.rdl- oder .rdlc-Dateitypen). Die Designkonzepte für RDLC-Layouts ähneln denen anderer Layouttypen. Das Layout bestimmt, welche Felder angezeigt werden und wie sie angeordnet sind. Allerdings ist der Entwurf von RDLC-Layouts weiter fortgeschritten als bei Word- und Excel-Layouts.

[![Zeigt die unterschiedlichen Elemente eines RDLC-Layouts.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools" />Erforderliche Tools

Um RDL-Layouts zu ändern, können Sie Microsoft SQL Server Report Builder oder Microsoft RDLC Report Designer verwenden.

- Report Builder ist eine eigenständige App, die von Ihnen oder einem Administrator auf Ihrem Computer installiert wird. Bei einer lokalen Installation von Business Central wird Report Builder automatisch mit der Installation von Business Central Server installiert. Weitere Informationen zum Installieren von Report Builder finden Sie unter [Report Builder installieren](/sql/reporting-services/install-windows/install-report-builder) in der SQL Server-Dokumentation.

- RDLC Report Designer ist eine Erweiterung für Visual Studio 2017 und später. Sie können RDLC Report Designer vom [Visual Studio Marktplatz ](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001) herunterladen und installieren.

## <a name="create-and-modify-rdlc-layouts" />RDLC-Lyouts erstellen und ändern

Das Erstellen und Ändern von RDLC-Layouts ist eine anspruchsvolle Aufgabe, die normalerweise von Hauptbenutzern oder Entwicklern ausgeführt wird. Die grundlegenden Konzepte sind nicht spezifisch für Business Central-Berichtslayouts. Aus diesem Grund verweisen wir auf folgende Dokumentation:

- [RDL-Layoutbericht erstellen](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    In diesem Artikel wird erläutert, wie Sie ein RDLC-Berichtslayout aus AL-Code erstellen.

- [Berichte, Berichtsteile und Berichtsdefinitionen](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Dies verlinkt Sie zur SQL Server Reporting Services-Dokumentation für RDL/RDLC. Diese Dokumentation erläutert die Konzepte  
hinter RDL/RDLC und wie man Report Builder verwendet.

> [!NOTE]
> Report Builder erkennt nur den Dateityp .rdl, nicht .rdlc. Aus Business Central exportierte Layoutdateien haben den Dateityp .rdlc. Um dieses Layout in Report Builder zu ändern, benennen Sie den Dateityp also in .rdl um.

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics--business-centralindex" />Siehe verwandte [Microsoft Schulungen](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Siehe auch

[Verwalten von Berichtslayouts](ui-manage-report-layouts.md)  
[Die von einem Bericht verwendeten Layouts festlegen](ui-set-report-layout.md)  
[Erste Schritte beim Erstellen von Berichtslayouts](ui-get-started-layouts.md)  
[Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md)  
[Business Intelligence](bi.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analysieren von Berichtsdaten mit Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
