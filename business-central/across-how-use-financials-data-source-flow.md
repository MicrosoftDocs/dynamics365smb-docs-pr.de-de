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
ms.date: 11/20/2019
ms.author: bmeier
ms.openlocfilehash: 24ca66c2d533f4a3e30eb1ebaca817915b95c370
ms.sourcegitcommit: e97e1df1f5d7b1d8af477580960a8737fcea4d16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832022"
---
# <a name="using-includeprodshortincludesprodshortmd-in-an-automated-workflow"></a>[!INCLUDE[prodshort](includes/prodshort.md)] in einem automatisierten Workflow nutzen

Sie können Ihre [!INCLUDE[prodshort](includes/prodshort.md)]-Daten als Teil eines Workflows in Microsoft Power Automate verwenden.

> [!NOTE]
> Zusätzlich zu Power Automate können Sie die Workflowfunktionalität verwenden in [!INCLUDE[prodshort](includes/prodshort.md)]. Beachten Sie, dass, obwohl es zwei verschiedene Workflowsysteme sind, jede beliebige Workflow-Vorlage, die Sie mit Power Automate erstellen, zur Liste von Workflows in [!INCLUDE[prodshort](includes/prodshort.md)] hinzugefügt wird. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
> Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power Automate haben.  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-automate"></a>So fügen Sie [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power Automate hinzu

1. In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com) und melden sich dann an.
2. Wählen Sie **Meine Flows** im Menüband oben auf der Seite.
3. Es gibt drei Möglichkeiten, einen Flow zu erstellen. **Mit Vorlage beginnen**, **Mit leerer Vorlage beginnen**, und **Mit Connector beginnen**. Eine Vorlage ist ein vordefinierter Flow, der für Sie erstellt wurde. Um eine Vorlage zu verwenden, aktivieren Sie sie einfach und erstellen eine Verbindung für jeden Dienst, den die Vorlage verwendet. Mit den Optionen **Mit leerer Vorlage beginnen** und **Mit Connector beginnen** können Sie einen neuen Flow komplett neu erstellen.
4. Zum Erstellen aus einer leeren Vorlage wählen Sie auf der Seite **Meine Flows** die Optionen **Mit leerer Vorlage beginnen** im **Automatisierter Flow** aus.
5. Suchen Sie nach **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]** Connector.
6. Definieren Sie einen Namen und wählen Sie den Trigger aus, den Sie für Ihren Flow verwenden möchten.
7. Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[prodshort](includes/prodshort.md)] verfügbaren Trigger aus:  

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

8. Power Automate fordert Sie auf, eine Umgebung und ein Unternehmen innerhalb Ihres [!INCLUDE[prodshort](includes/prodshort.md)]-Tenants und sämtliche Bedingungen in Ihren Daten, die Sie abhören möchten, auszuwählen.

    > [!NOTE]
    > Der [!INCLUDE[prodshort](includes/prodshort.md)] Connector for Microsoft Dynamics for Power Automate unterstützt mehrere Produktions- und Sandbox-Umgebungen. Wenn Sie nicht mehrere Produktions- oder Sandbox-Umgebungen erstellt haben, ist **Produktion** die einzige verfügbare Option, die Sie auswählen können.  

    Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren Business Central[!INCLUDE [prodshort](includes/prodshort.md)]-Daten verbunden und sind bereit, Ihren Flow zu erstellen.

9. Um aus einer Vorlage zu erstellen, wählen Sie die Option **Mit Vorlage erstellen** aus.
10. Suchen Sie nach **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]**-Vorlangen.
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
12. Power Automate zeigt eine Liste der Dienste an, die in der Flow-Vorlage verwendet werden und versucht, automatisch eine Verbindung zu diesen Diensten herzustellen. Wenn Sie noch keine Verbindung zu einem Dienst hergestellt haben, werden Sie aufgefordert, sich bei jedem Dienst anzumelden, zu dem Sie eine Verbindung herstellen müssen. Neben jedem Dienst wird ein grünes Häkchen angezeigt, sobald eine Verbindung erfolgreich hergestellt wurde. Wählen Sie **Fortsetzen**.
13. Power Automate fordert Sie auf, eine Umgebung und ein Unternehmen innerhalb Ihres [!INCLUDE[prodshort](includes/prodshort.md)]-Tenant auszuwählen. Da jeder Schritt im Flow unabhängig vom darauffolgenden ist, werden Sie möglicherweise aufgefordert, die Umgebung und das Unternehmen mehrmals zu definieren, wenn Sie eine [!INCLUDE[prodshort](includes/prodshort.md)] Power Automate-Vorlage verwenden.

Weitere Informationen finden Sie in der [Power Automate-Dokumentation](/power-automate/getting-started).

## <a name="see-also"></a>Siehe auch

[Erste Schritte](product-get-started.md)  
[Workflow](across-workflow.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[[!INCLUDE[prodlong](includes/prodlong.md)] Workflows verwalten](across-use-workflows.md)  
[Genehmigungsbenutzereinrichtung](across-how-to-set-up-approval-users.md)  
[Einrichten [!INCLUDE[prodshort](includes/prodshort.md)]](setup.md)  
[Finanzen](finance.md)  
