---
title: Daten mithilfe von Flow verbinden| Microsoft Docs
description: Sie können Business Central als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow erstellen.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 86178bafa806fb8cba531d5b78157437c242d432
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305028"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] in einem automatisierten Workflow nutzen
Sie können Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten als Teil eines Workflows in Microsoft Flow verwenden.

> [!NOTE]
> Zusätzlich zu Microsoft Flow können Sie die Workflowfunktionalität verwenden in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Beachten Sie, dass, obwohl es zwei verschiedene Workflowsysteme sind, eine mit Microsoft Flow erstellte Fluss-Vorlage der Liste von Workflows in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt wird. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
> Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Flow hinzufügen
1. In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com/en-us/) und melden sich dann an.
2. Wählen Sie **Meine Flows** im Menüband oben auf der Seite.
3. Es gibt drei Möglichkeiten, einen Flow zu erstellen. **Mit der Vorlage beginnen**, **Bei Leerzeichen beginnen**, und **Mit einem Connector for Microsoft Dynamics beginnen**. Eine Vorlage ist ein vordefinierter Flow, der für Sie erstellt wurde. Um eine Vorlage zu verwenden, aktivieren Sie sie einfach und erstellen eine Verbindung für jeden Dienst, den die Vorlage verwendet. Mit den Optionen **Ohne Vorlage beginnen** und **Beginnen Sie mit einem Connector for Microsoft Dynamics** können Sie einen neuen Flow komplett neu erstellen.
4. Zum Erstellen aus einer leeren Vorlage wählen Sie auf der Seite **Meine Flows** die Option **Ohne Vorlage neu** erstellen aus und die Option **Automatischer Flow**.
5. Suchen Sie nach **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** Connector.
6. Definieren Sie einen Namen und wählen Sie den Trigger aus, den Sie für Ihren Flow verwenden möchten.
7. Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbaren Trigger aus:  
    
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
     
8. Flow fordert Sie auf, eine Umgebung und ein Unternehmen innerhalb Ihres [!INCLUDE[d365fin](includes/d365fin_md.md)] Tenants und sämtliche Bedingungen in Ihren Daten, die Sie abhören möchten auszuwählen.

> [!NOTE]  
>   Der [!INCLUDE[d365fin](includes/d365fin_md.md)] Connector for Microsoft Dynamics for Microsoft Flow unterstützt mehrere Produktions- und Sandbox-Umgebungen. Wenn Sie nicht mehrere Produktions- oder Sandbox-Umgebungen erstellt haben, ist **Produktion** die einzige verfügbare Option, die Sie auswählen können. 

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Business Central Daten verbunden und sind bereit, Ihren Flow zu bauen.

9. Um aus einer Vorlage zu erstellen, wählen Sie die Option **Mit Vorlage erstellen** aus.
10. Suchen Sie nach **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-Vorlangen.
11. Aus der Liste der verfügbaren Vorlagen wählen Sie eine der verfügbaren Vorlagen aus und wählen Sie **Erstellen**.  

    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsauftrag anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsangebot anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsrechnung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsgutschrift anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Debitoren anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Einkaufsbestellung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Einkaufsrechnung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-EInkaufsgutschrift anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Artikel anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Anbieter anfordern*,  
    *Genehmigungsanforderung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Fibu Buch.-Blatt*, oder    
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Fibu Buch.-Blattzeilen anfordern*.  
12. Flow zeigt eine Liste der in der Flow-Vorlage verwendeten Dienste an und versucht, automatisch eine Verbindung zu diesen Diensten herzustellen. Wenn Sie noch keine Verbindung zu einem Dienst hergestellt haben, werden Sie aufgefordert, sich bei jedem Dienst anzumelden, zu dem Sie eine Verbindung herstellen müssen. Neben jedem Dienst wird ein grünes Häkchen angezeigt, sobald eine Verbindung erfolgreich hergestellt wurde. Wählen Sie **Fortsetzen**.
13. Flow fordert Sie auf, eine Umgebung und eine Unternehmen innerhalb Ihres [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Mandanten auszuwählen. Da jede Schritt im Flow unabhängig vom darauffolgenden ist, werden Sie möglicherweise aufgefordert, die Umgebung und das Unternehmen mehrmals zu definieren, wenn Sie eine [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow-Vorlage verwenden.

Weitere Informationen finden Sie in der [Flow-Dokumentation](/flow/getting-started).

## <a name="see-also"></a>Siehe auch
[Erste Schritte](product-get-started.md)  
[Workflow](across-workflow.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)   
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Workflows verwalten](across-use-workflows.md)  
[Genehmigungsbenutzereinrichtung](across-how-to-set-up-approval-users.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
