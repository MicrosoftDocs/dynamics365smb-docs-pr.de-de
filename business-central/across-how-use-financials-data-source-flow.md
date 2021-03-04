---
title: Ihre Daten mit Power Automate verbinden | Microsoft Docs
description: Sie können Business Central als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow erstellen.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f44b727a353208d1b2b8f5d918400de1687acc52
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754542"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>[!INCLUDE[prod_short](includes/prod_short.md)] in einem automatisierten Workflow nutzen

Sie können Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten als Teil eines Workflows in Microsoft Power Automate verwenden.

> [!NOTE]
> Zusätzlich zu Power Automate können Sie die Workflowfunktionalität verwenden in [!INCLUDE[prod_short](includes/prod_short.md)]. Beachten Sie, dass, obwohl es zwei verschiedene Workflowsysteme sind, jede beliebige Workflow-Vorlage, die Sie mit Power Automate erstellen, zur Liste von Workflows in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt wird. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
> Sie müssen ein gültiges Konto bei [!INCLUDE[prod_short](includes/prod_short.md)] und Power Automate haben.  

## <a name="to-add-prod_short-as-a-data-source-in-power-automate"></a>So fügen Sie [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power Automate hinzu

1. In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com) und melden sich dann an.
2. Wählen Sie **Meine Flows** im Menüband oben auf der Seite.
3. Es gibt drei Möglichkeiten, einen Flow zu erstellen. **Mit Vorlage beginnen**, **Mit leerer Vorlage beginnen**, und **Mit Connector beginnen**. Eine Vorlage ist ein vordefinierter Flow, der für Sie erstellt wurde. Um eine Vorlage zu verwenden, aktivieren Sie sie einfach und erstellen eine Verbindung für jeden Dienst, den die Vorlage verwendet. Mit den Optionen **Mit leerer Vorlage beginnen** und **Mit Connector beginnen** können Sie einen neuen Flow komplett neu erstellen.
4. Zum Erstellen aus einer leeren Vorlage wählen Sie auf der Seite **Meine Flows** die Optionen **Mit leerer Vorlage beginnen** im **Automatisierter Flow** aus.
5. Suchen Sie nach **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]** Connector.
6. Definieren Sie einen Namen und wählen Sie den Trigger aus, den Sie für Ihren Flow verwenden möchten.
7. Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[prod_short](includes/prod_short.md)] verfügbaren Trigger aus:  

    *Die Genehmigung für einen Kreditor wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattzeile wird angefordert*,  
    *Wenn ein Datensatz gelöscht wird*,  
    *Wenn ein Datensatz geändert wird*,  
    *Wenn ein Datensatz erstellt wird*,  
    *Wenn ein Datensatz geändert wird*,  
    *Genehmigung von Fibu Buch.-Blattname wird angefordert*,  
    *Die Genehmigung für einen Debitor wird angefordert*,  
    *Die Genehmigung für einen Artikel wird angefordert*,  
    *Die Genehmigung für einen Einkaufsbeleg wird angefordert*, oder  
    *Wenn ein Verkaufsbeleg angefordert wird*.

8. Power Automate fordert Sie auf, eine Umgebung und ein Unternehmen innerhalb Ihres [!INCLUDE[prod_short](includes/prod_short.md)]-Tenants und sämtliche Bedingungen in Ihren Daten, die Sie abhören möchten, auszuwählen.

    > [!NOTE]
    > Der [!INCLUDE[prod_short](includes/prod_short.md)] Connector for Microsoft Dynamics for Power Automate unterstützt mehrere Produktions- und Sandbox-Umgebungen. Wenn Sie nicht mehrere Produktions- oder Sandbox-Umgebungen erstellt haben, ist **Produktion** die einzige verfügbare Option, die Sie auswählen können.  

    Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren Business Central[!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und sind bereit, Ihren Flow zu erstellen.

9. Um aus einer Vorlage zu erstellen, wählen Sie die Option **Mit Vorlage erstellen** aus.
10. Suchen Sie nach **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**-Vorlangen.
11. Aus der Liste der verfügbaren Vorlagen wählen Sie eine der verfügbaren Vorlagen aus und wählen Sie **Erstellen**.  

    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Verkaufsauftrag anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Verkaufsangebot anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Verkaufsrechnung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Verkaufsgutschrift anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Debitoren anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Einkaufsbestellung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Einkaufsrechnung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-EInkaufsgutschrift anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Artikel anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Anbieter anfordern*,  
    *Genehmigungsanforderung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] Fibu Buch.-Blatt*, oder    
    *Genehmigung für Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-Fibu Buch.-Blattzeilen anfordern*.  
12. Power Automate zeigt eine Liste der Dienste an, die in der Flow-Vorlage verwendet werden und versucht, automatisch eine Verbindung zu diesen Diensten herzustellen. Wenn Sie noch keine Verbindung zu einem Dienst hergestellt haben, werden Sie aufgefordert, sich bei jedem Dienst anzumelden, zu dem Sie eine Verbindung herstellen müssen. Neben jedem Dienst wird ein grünes Häkchen angezeigt, sobald eine Verbindung erfolgreich hergestellt wurde. Wählen Sie **Fortsetzen**.
13. Power Automate fordert Sie auf, eine Umgebung und ein Unternehmen innerhalb Ihres [!INCLUDE[prod_short](includes/prod_short.md)]-Tenant auszuwählen. Da jeder Schritt im Flow unabhängig vom darauffolgenden ist, werden Sie möglicherweise aufgefordert, die Umgebung und das Unternehmen mehrmals zu definieren, wenn Sie eine [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate-Vorlage verwenden.

Weitere Informationen finden Sie in der [Power Automate-Dokumentation](/power-automate/getting-started).

## <a name="see-also"></a>Siehe auch

[Erste Schritte](product-get-started.md)  
[Workflow](across-workflow.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Workflows verwalten](across-use-workflows.md)  
[Genehmigungsbenutzereinrichtung](across-how-to-set-up-approval-users.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzen](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]