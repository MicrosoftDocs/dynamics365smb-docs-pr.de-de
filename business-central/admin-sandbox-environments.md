---
title: Sandbox-Umgebungen
description: 'Erfahren Sie, wie Sie Business Central in einer speziellen Umgebung sicher erforschen, erlernen, demonstrieren, entwickeln, Probleme beheben und testen können.'
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sandbox, demo, develop'
ms.date: 12/20/2021
ms.author: solsen
---
# <a name="sandbox-environments-in-"></a>Sandbox-Umgebungen in [!INCLUDE[prod_short](includes/prod_short.md)]

Mit [!INCLUDE[prod_short](includes/prod_short.md)] Online können Sie auf einfache Weise eine sichere Umgebung schaffen, in der Sie testen, trainieren oder Fehler beheben können, ohne die Arbeitsprozesse oder Geschäftsdaten Ihres Unternehmens zu beeinträchtigen. Eine solche Nichtproduktionsumgebung heißt *Sandbox*. Isoliert von der Produktion ist eine Sandboxumgebung der Ort, um den Dienst sicher zu untersuchen, erfahren, testen und entwickeln, ohne das Risiko des Beeinflussens der Daten und Einstellungen Ihrer Fertigungsumgebungen zur riskieren.  

> [!TIP]
> Sind Sie auf diesem Artikel gelandet, nachdem Sie den Namen Ihrer [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebung in der oberen Leiste ausgewählt haben? Derzeit können Sie weder den Namen noch die Umgebung auf diese Weise ändern. Stattdessen müssen Sie Ihren Admin bitten, den Namen zu ändern, oder ihn bitten, den Link zu einer anderen Umgebung freizugeben.

Ihr Administrator verwaltet Sandbox-Umgebungen im [Administration Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Wenn Sie beispielsweise eine Sandbox für das Benchmarking erstellen möchten, kann Ihr Administrator im Admin Center eine dedizierte Umgebung erstellen. Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Produktions- und Sandbox-Umgebungen](/dynamics365/business-central/dev-itpro/administration/environment-types).  

Sie können Sandboxes auch sicher für Schulungen verwenden, z. B. um einem Lernpfad von [Microsoft Schulung](/training/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs) zu folgen, weil es eine sichere Umgebung zum Experimentieren ist. Wenn etwas schief geht, löschen Sie einfach die Sandbox und beginnen von vorne.  

Sobald Sie fertig sind, können Sie die Sandbox über das Admin Center entfernen.  

> [!NOTE]
> Technisch gesehen unterscheiden sich Sandbox-Umgebungen stark von Produktionsumgebungen. Ihr Administrator kann eine Sandbox erstellen, die Produktionsdaten enthält, aber es ist immer noch eine Sandbox, und Sie können beispielsweise keinen Datenbankexport anfordern. Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Sandbox-Umgebungen](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments).

Die Sandboxumgebung ist nicht zuletzt deshalb nützlich, weil sie einige nützliche Funktionen enthält:

* [Erweiterte Benutzeroberfläche](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Designer](#designer)  

## <a name="advanced-user-experience"></a>Erweiterte Benutzeroberfläche

Es ist möglich, die vollständige Funktion der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] in einem Sandbox-Mandant zu aktivieren, indem Sie das Feld **Erfahrung** auf der Seite **Unternehmensinformationen** auf *Premium* festlegen. Suchen Sie die Seite **Unternehmensdaten** im Symbol :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Einstellungen."::: Menü.  

Nachdem Sie die *Premium*-Benutzererfahrung aktiviert haben, erhalten Sie Zugriff auf alle Standardprofile (Rollen) und Rollencenter in der Standardversion. Wenden Sie sich zur Demonstration der Möglichkeiten alternativ an einen Wiederverkaufspartner. Weitere Informationen finden Sie unter [Wie finde ich einen Wiederverkaufspartner?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Vollständige Beispieldaten

In Situationen, in denen Sie zusätzliche Beispieldaten benötigen, wenden Sie sich bitte an Ihren Vertriebspartner.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Designerin

In einer Sandboxumgebung finden Sie den **Designer** aktiviert. Sie können den Designer aktivieren, indem Sie das Symbol ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) auf einer Seite oder durch Auswahl des Menüelements **Design** im Menü ![Einstellungen ](media/ui-experience/settings_icon_small.png) Einstellungen.  

Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Designer verwenden](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) (nur in englischer Sprache).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/admin-online-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]-Testversionen und -Abonnements](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions)  
[Verwalten von Umgebungen im Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Produktions- und Sandbox-Umgebungen](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
