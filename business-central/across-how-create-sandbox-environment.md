---
title: Erstellen Sie eine Sandkastenumgebung| Microsoft Docs
description: Erstellen Sie somit eine Umgebung für das Untersuchen, Lernen, Entwickeln und Testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/06/2019
ms.author: solsen
ms.openlocfilehash: 0f8f0f85df89c1d71fc3e114ebd902f2aa85f802
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896109"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a>Erstellen einer Sandkastenumgebung in [!INCLUDE [prodshort](includes/prodshort.md)]

Mit [!INCLUDE [prodshort](includes/prodshort.md)] können Sie auf einfache Weise eine sichere Umgebung schaffen, in der Sie testen, trainieren oder Fehler beheben können, ohne die Arbeitsprozesse oder Geschäftsdaten Ihres Unternehmens zu beeinträchtigen. Eine solche Nichtproduktionsumgebung heißt *Sandbox*. Isoliert von der Produktion ist eine Sandboxumgebung der Ort, um den Dienst sicher zu untersuchen, erfahren, testen und entwickeln, ohne das Risiko des Beeinflussens der Daten und Einstellungen Ihrer Fertigungsumgebungen zur riskieren.  

Ihr Administrator kann Sandboxumgebungen im [Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json) erstellen, aber wenn Sie schnell etwas testen möchten, können Sie eine Sandboxumgebung aus [!INCLUDE [prodshort](includes/prodshort.md)] heraus erstellen.  

> [!NOTE]
> Technisch gesehen unterscheiden sich Sandboxumgebungen stark von Produktionsumgebungen, selbst wenn Ihr Administrator eine Sandbox erstellt, die Produktionsdaten enthält. Sie können keine Sandbox für das Benchmarking verwenden und beispielsweise keinen Datenbankexport anfordern. Wenn Sie eine Sandbox für das Benchmarking erstellen möchten, kann Ihr Administrator im Admin Center eine dedizierte Produktionsumgebung erstellen. Weitere Informationen finden Sie unter [Umgebungstypen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a>So erstellen Sie eine Umgebung in Ihrer [!INCLUDE [prodshort](includes/prodshort.md)]

1. Melden Sie sich bei Ihrer Produktionsinstanz von [!INCLUDE[d365fin](includes/d365fin_md.md)] an.

2. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Sandboxumgebung** ein und wählen Sie dann den verknüpften Link.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Klicken Sie auf die Schaltfläche **Erstellen**.  

    Eine weitere Registerkarte mit [!INCLUDE[d365fin](includes/d365fin_md.md)] wird geöffnet, in der Sie die Einrichtung Ihrer Sandbox-Umgebung abschließen können.

    > [!NOTE]  
    >  Wenn Sie Popupblocker aktiviert haben in Ihrem Browser, bearbeiten sie diese, um URLs der *.businesscentral.dynamics.com-Adresse zu ermöglichen.

Wenn die Sandkastenumgebung bereitsteht, werden Sie zum Begrüßung-Assistenten der Sandkastenumgebung umgeleitet.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Sie können die Schaltfläche **Mehr erfahren** wählen, um Informationen zu Entwicklerszenarien zu erhalten, die Sie in einer Sandboxumgebung ausprobieren können oder wählen Sie die Schaltfläche **Schließen**, um zum Rollencenter Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)] Sandboxinstanz zu gelangen.

Oben im Rollencenters wird eine Benachrichtigung angezeigt, die bestätigt, dass dies eine Sandkastenumgebung ist. Der Typ dieser Umgebung wird in der Titelleiste des Clients anzeigen.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Eine auf diese Weise erstellte Sandbox-Umgebung enthält nur die Standarddemonstrationsdaten für das CRONUS Unternehmen. Keine Daten werden kopiert oder anderswie von der Fertigungsumgebungen während der Sandkastenerstellung transferiert.<br /><br />
> Sie können auch eine Sandbox-Umgebung erstellen, die die Produktionsdaten enthält. Sie müssen dies über die Verwaltungszentrale tun. Weitere Informationen finden Sie unter [Umgebung verwalten](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in der Entwickler- und IT-Profi-Hilfe.

Jederzeit können Sie zur Seite **Sandkastenumgebung** zurückkehren und die Sandkastenumgebung zurücksetzen.

> [!NOTE]  
> Das Zurücksetzen der Sandkastenmgebung, wird sie komplett entfernen und dann wieder erstellt mit den Vorgabe-Demodaten.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Ein Administrator kann den Zugriff für einige Benutzer zur Sandboxumgebung begrenzen oder sogar sperren. Dies kann geschehen, indem die Standardsicherheitsfunktionen des Produkts, wie die Benutzerkarte, die Benutzergruppen und die Berechtigungssätze verwendet werden. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Erweiterte Funktionen der Sandkastenumgebung

Die Sandboxumgebung ist nicht zuletzt deshalb nützlich, weil sie einige nützliche Funktionen enthält.

### <a name="designer"></a>Designerin

In einer Sandboxumgebung finden Sie den **Designer** aktiviert. Sie können Designer aktivieren, indem Sie das Entwurfssymbol ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) auf einer Seite auswählen oder durch Auswahl des Menüelements **Entwurf** im Einstellungsmenü ![Einstellungen](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Aktivieren Sie die erweiterte Benutzererfahrung
Es ist möglich, die erweiterte (vollständige) Funktion eines Sandkastentenants in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu aktivieren, indem Sie das Feld **Erfahrung** auf der Seite **Firmendaten** einrichten.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Nachdem Sie die Funktion erweiterter Funktionalität in einem Sandkastentenant aktiviert haben, erhalten Sie Zugriff auf alle Standardprofile (Rollen) und Rollencenter. Sie können einen Auswertungsmandanten erstellen, der vollständig eingerichtet wird, einschließlich Demodaten und Zugriff in den erweiterten Bereichen des Produkts.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-Testversionen und Abonnements](across-preview.md)  
[Verwalten von Umgebungen im Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
