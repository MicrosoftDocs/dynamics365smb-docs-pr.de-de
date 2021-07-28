---
title: Sandkastenumgebung erstellen
description: Erstellen Sie eine Sandbox-„Test“-Umgebung zum sicheren Erforschen, Lernen, Demonstrieren, Entwickeln, Problembehandeln und Testen innerhalb von Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: 2f4ca6a98aac49fa5fea7d8658ef51a9510c97d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437677"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Erstellen einer Sandkastenumgebung in [!INCLUDE[prod_short](includes/prod_short.md)]

Mit [!INCLUDE[prod_short](includes/prod_short.md)] können Sie auf einfache Weise eine sichere Umgebung schaffen, in der Sie testen, trainieren oder Fehler beheben können, ohne die Arbeitsprozesse oder Geschäftsdaten Ihres Unternehmens zu beeinträchtigen. Eine solche Nichtproduktionsumgebung heißt *Sandbox*. Isoliert von der Produktion ist eine Sandboxumgebung der Ort, um den Dienst sicher zu untersuchen, erfahren, testen und entwickeln, ohne das Risiko des Beeinflussens der Daten und Einstellungen Ihrer Fertigungsumgebungen zur riskieren.  

Ihr Administrator verwaltet Sandboxumgebungen im [Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), wenn Sie jedoch schnell einen Test durchführen möchten, können Sie eine Sandboxumgebung über [!INCLUDE[prod_short](includes/prod_short.md)] erstellen. Sobald Sie fertig sind, können Sie die Sandbox über das Admin Center entfernen.  

> [!NOTE]
> Technisch gesehen unterscheiden sich Sandboxumgebungen stark von Produktionsumgebungen, selbst wenn Ihr Administrator eine Sandbox erstellt, die Produktionsdaten enthält. Sie können keine Sandbox für das Benchmarking verwenden und beispielsweise keinen Datenbankexport anfordern. Wenn Sie eine Sandbox für das Benchmarking erstellen möchten, kann Ihr Administrator im Admin Center eine dedizierte Umgebung erstellen. Weitere Informationen finden Sie unter [Produktions- und Sandbox-Umgebungen](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>So erstellen Sie eine Umgebung in Ihrer [!INCLUDE[prod_short](includes/prod_short.md)]

1. Melden Sie sich bei Ihrer Produktionsinstanz von [!INCLUDE[prod_short](includes/prod_short.md)] an.

2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Sandbox-Umgebung** ein, und wählen Sie dann den entsprechenden Link.
    <!-- ![Sandbox Environment Setup.](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Klicken Sie auf die Schaltfläche **Erstellen**.  

    Eine weitere Registerkarte mit [!INCLUDE[prod_short](includes/prod_short.md)] wird geöffnet, in der Sie die Einrichtung Ihrer Sandbox-Umgebung abschließen können.

    > [!NOTE]  
    >  Wenn Sie Popupblocker aktiviert haben in Ihrem Browser, bearbeiten sie diese, um URLs der *.businesscentral.dynamics.com-Adresse zu ermöglichen.

Wenn die Sandkastenumgebung bereitsteht, werden Sie zum Begrüßung-Assistenten der Sandkastenumgebung umgeleitet.
<!-- ![Sandbox Welcome Wizard.](./media/across-sandbox/sandbox-wizard.png) -->

Sie können die Schaltfläche **Mehr erfahren** wählen, um Informationen zu Entwicklerszenarien zu erhalten, die Sie in einer Sandboxumgebung ausprobieren können oder wählen Sie die Schaltfläche **Schließen**, um zum Rollencenter Ihrer [!INCLUDE[prod_short](includes/prod_short.md)] Sandboxinstanz zu gelangen.

Oben im Rollencenters wird eine Benachrichtigung angezeigt, die bestätigt, dass dies eine Sandkastenumgebung ist. Der Typ dieser Umgebung wird in der Titelleiste des Clients anzeigen.
    <!-- ![Sandbox RoleCenter Notification.](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Eine auf diese Weise erstellte Sandbox-Umgebung enthält nur die Standarddemonstrationsdaten für das CRONUS Unternehmen. Keine Daten werden kopiert oder anderswie von der Fertigungsumgebungen während der Sandkastenerstellung transferiert.
>
> Erstellen Sie alternativ eine Sandbox-Umgebung basierend auf Produktionsdaten. Sie müssen dies über die Verwaltungszentrale tun. Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Umgebungen verwalten](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments).  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu.](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Ein Administrator kann den Zugriff für einige Benutzer zur Sandboxumgebung begrenzen oder sogar sperren. Dies kann geschehen, indem die Standardsicherheitsfunktionen des Produkts, wie die Benutzerkarte, die Benutzergruppen und die Berechtigungssätze verwendet werden. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets.](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Erweiterte Funktionen der Sandkastenumgebung

Die Sandboxumgebung ist nicht zuletzt deshalb nützlich, weil sie einige nützliche Funktionen enthält:

* [Erweiterte Benutzeroberfläche](#advanced-user-experience)  
* [Vollständige Beispieldaten](#complete-sample-data)  
* [Designer](#designer)  

### <a name="advanced-user-experience"></a>Erweiterte Benutzeroberfläche

Es ist möglich, die vollständige Funktion der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] in einem Sandbox-Mandant zu aktivieren, indem Sie das Feld **Erfahrung** auf der Seite **Unternehmensinformationen** auf *Premium* festlegen. Suchen Sie die Seite **Unternehmensdaten** im Symbol :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Einstellungen."::: Menü.  

Nachdem Sie die *Premium*-Benutzererfahrung aktiviert haben, erhalten Sie Zugriff auf alle Standardprofile (Rollen) und Rollencenter in der Standardversion. Sie können einen Auswertungsmandanten erstellen, der vollständig eingerichtet wird, einschließlich Demodaten und Zugriff in den erweiterten Bereichen des Produkts. Wenden Sie sich zur Demonstration der Möglichkeiten alternativ an einen Wiederverkaufspartner. Weitere Informationen finden Sie unter [Wie finde ich einen Wiederverkaufspartner?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Vollständige Beispieldaten

In Situationen, in denen Sie zusätzliche Beispieldaten benötigen, wenden Sie sich bitte an Ihren Vertriebspartner.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>So erstellen Sie ein Unternehmen mit vollständigen Beispieldaten in einer Sandbox

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Unternehmen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** und dann **Neues Unternehmen erstellen** aus.  
3. Wählen Sie auf der Seite **Unterstützte Einrichtung zum Erstellen eines Unternehmens** die Option **Weiter** aus.  
4. Geben Sie einen Namen für das neue Unternehmen an, und wählen Sie dann im Feld **Daten und Einrichtung für die ersten Schritte auswählen** die Option **Erweiterte Auswertung - vollständiger Beispieldaten** aus.  
5. Schließen Sie die restlichen Schritte des unterstützten Einrichtungsleitfadens ab.  

Wenn der unterstützte Einrichtungsleitfaden abgeschlossen ist, können Sie das neue Unternehmen mit den vollständigen Beispieldaten erkunden. Weitere Informationen finden Sie unter [Neue Mandanten erstellen in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Designerin

In einer Sandboxumgebung finden Sie den **Designer** aktiviert. Sie können den Designer aktivieren, indem Sie das Symbol ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) auf einer Seite oder durch Auswahl des Menüelements **Design** im Menü ![Einstellungen ](media/ui-experience/settings_icon_small.png) Einstellungen.  

Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Verwenden von Designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) (nur auf Englisch).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]-Testversionen und Abonnements](across-preview.md)  
[Verwalten von Umgebungen im Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
