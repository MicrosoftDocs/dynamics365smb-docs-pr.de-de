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
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 5482460acb6ce0e92b1d6dbe876b1b64267974ae
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919688"
---
# <a name="creating-a-sandbox-environment-in-prodshort"></a>Erstellen einer Sandkastenumgebung in [!INCLUDE[prodshort](includes/prodshort.md)]

Mit [!INCLUDE[prodshort](includes/prodshort.md)] können Sie auf einfache Weise eine sichere Umgebung schaffen, in der Sie testen, trainieren oder Fehler beheben können, ohne die Arbeitsprozesse oder Geschäftsdaten Ihres Unternehmens zu beeinträchtigen. Eine solche Nichtproduktionsumgebung heißt *Sandbox* . Isoliert von der Produktion ist eine Sandboxumgebung der Ort, um den Dienst sicher zu untersuchen, erfahren, testen und entwickeln, ohne das Risiko des Beeinflussens der Daten und Einstellungen Ihrer Fertigungsumgebungen zur riskieren.  

Ihr Administrator kann Sandboxumgebungen im [Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json) erstellen, aber wenn Sie schnell etwas testen möchten, können Sie eine Sandboxumgebung aus [!INCLUDE[prodshort](includes/prodshort.md)] heraus erstellen.  

> [!NOTE]
> Technisch gesehen unterscheiden sich Sandboxumgebungen stark von Produktionsumgebungen, selbst wenn Ihr Administrator eine Sandbox erstellt, die Produktionsdaten enthält. Sie können keine Sandbox für das Benchmarking verwenden und beispielsweise keinen Datenbankexport anfordern. Wenn Sie eine Sandbox für das Benchmarking erstellen möchten, kann Ihr Administrator im Admin Center eine dedizierte Produktionsumgebung erstellen. Weitere Informationen finden Sie unter [Umgebungstypen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-prodshort"></a>So erstellen Sie eine Umgebung in Ihrer [!INCLUDE[prodshort](includes/prodshort.md)]

1. Melden Sie sich bei Ihrer Produktionsinstanz von [!INCLUDE[d365fin](includes/d365fin_md.md)] an.

2. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Sandboxumgebung** ein und wählen Sie dann den verknüpften Link.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Klicken Sie auf die Schaltfläche **Erstellen** .  

    Eine weitere Registerkarte mit [!INCLUDE[d365fin](includes/d365fin_md.md)] wird geöffnet, in der Sie die Einrichtung Ihrer Sandbox-Umgebung abschließen können.

    > [!NOTE]  
    >  Wenn Sie Popupblocker aktiviert haben in Ihrem Browser, bearbeiten sie diese, um URLs der *.businesscentral.dynamics.com-Adresse zu ermöglichen.

Wenn die Sandkastenumgebung bereitsteht, werden Sie zum Begrüßung-Assistenten der Sandkastenumgebung umgeleitet.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Sie können die Schaltfläche **Mehr erfahren** wählen, um Informationen zu Entwicklerszenarien zu erhalten, die Sie in einer Sandboxumgebung ausprobieren können oder wählen Sie die Schaltfläche **Schließen** , um zum Rollencenter Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)] Sandboxinstanz zu gelangen.

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

Ein Administrator kann den Zugriff für einige Benutzer zur Sandboxumgebung begrenzen oder sogar sperren. Dies kann geschehen, indem die Standardsicherheitsfunktionen des Produkts, wie die Benutzerkarte, die Benutzergruppen und die Berechtigungssätze verwendet werden. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Erweiterte Funktionen der Sandkastenumgebung

Die Sandboxumgebung ist nicht zuletzt deshalb nützlich, weil sie einige nützliche Funktionen enthält.

### <a name="to-enable-the-advanced-user-experience"></a>Aktivieren Sie die erweiterte Benutzererfahrung

Es ist möglich, die vollständige Funktion der Standardversion von [!INCLUDE[d365fin](includes/d365fin_md.md)] in einem Sandbox-Mandant zu aktivieren, indem Sie das Feld **Erfahrung** auf der Seite **Unternehmensinformationen** auf *Premium* festlegen. Suchen Sie die Seite **Unternehmensinformationen** im Menü :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Einstellungssymbol":::.  

Nachdem Sie die *Premium* -Benutzererfahrung aktiviert haben, erhalten Sie Zugriff auf alle Standardprofile (Rollen) und Rollencenter in der Standardversion. Sie können einen Auswertungsmandanten erstellen, der vollständig eingerichtet wird, einschließlich Demodaten und Zugriff in den erweiterten Bereichen des Produkts. Wenden Sie sich zur Demonstration der Möglichkeiten alternativ an einen Wiederverkaufspartner. Weitere Informationen finden Sie unter [Wie finde ich einen Weiterverkaufspartner?](across-faq.md#findpartner).  

### <a name="to-enable-complete-sample-data"></a>So aktivieren Sie vollständige Beispieldaten

In der Sandbox-Umgebung können Sie mit der Option **Erweiterte Auswertung - vollständiger Beispieldaten** auch ein neues Unternehmen erstellen, sodass Sie Schulungen durchführen oder exemplarische Vorgehensweisen durchlaufen können, für die zusätzliche Beispieldaten erforderlich sind, z. B. [Exemplarische Vorgehensweise: Empfang und Einlagerung in Basis-Lagerkonfigurationen](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).  

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>So erstellen Sie ein Unternehmen mit vollständigen Beispieldaten in einer Sandbox

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Unternehmen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** und dann **Neues Unternehmen erstellen** aus.  
3. Wählen Sie auf der Seite **Unterstützte Einrichtung zum Erstellen eines Unternehmens** die Option **Weiter** aus.  
4. Geben Sie einen Namen für das neue Unternehmen an, und wählen Sie dann im Feld **Daten und Einrichtung für die ersten Schritte auswählen** die Option **Erweiterte Auswertung - vollständiger Beispieldaten** aus.  
5. Schließen Sie die restlichen Schritte des unterstützten Einrichtungsleitfadens ab.  

Wenn der unterstützte Einrichtungsleitfaden abgeschlossen ist, können Sie das neue Unternehmen mit den vollständigen Beispieldaten erkunden. Weitere Informationen finden Sie unter [Neue Mandanten erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).  

### <a name="designer"></a>Designerin

In einer Sandboxumgebung finden Sie den **Designer** aktiviert. Sie können Designer aktivieren, indem Sie das Entwurfssymbol ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) auf einer Seite auswählen oder durch Auswahl des Menüelements **Entwurf** im Einstellungsmenü ![Einstellungen](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-Testversionen und Abonnements](across-preview.md)  
[Verwalten von Umgebungen im Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
