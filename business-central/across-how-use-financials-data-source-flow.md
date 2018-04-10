---
title: Daten mithilfe von Flow verbinden| Microsoft Docs
description: "Sie können Financials als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow erstellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/21/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5d7fa359ee99cd177a445e025ddf8d156c6e2421
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)]in einem automatisierten Workflow nutzen
Sie können die Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Teil eines Workflows in Microsoft Flow verwenden.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Flow hinzufügen
1. In Ihrem Browser navigieren Sie zu [flow.microsoft.com](https://flow.microsoft.com/en-us/) und melden sich dann an.
2. Wählen Sie **My Flows** im Menüband oben auf der Seite.
3. Es gibt zwei Möglichkeiten, einen Flow zu erstellen: **Aus Formularvorlage erstellen** und **Ohne Vorlage neu erstellen**. Eine Vorlage ist ein vordefinierter Flow, der für Sie erstellt wurde.  Um eine Vorlage zu verwenden, aktivieren Sie sie einfach und erstellen eine Verbindung für jeden Dienst, den die Vorlage verwendet. Eine leere Vorlage ermöglicht Ihnen, einen neuen Flow von Grund auf neu zu erstellen. 
4. Zum Erstellen aus einer leeren Vorlage wählen Sie im Fenster **Meine Flows** die Option **Ohne Vorlage neu erstellen** aus.
5. Suchen Sie nach **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** Connector.
6. Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbaren Trigger aus:  
    *Die Genehmigung für einen Debitor wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattname wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattzeile wird angefordert*,  
    *Die Genehmigung für einen Artikel wird angefordert*,  
    *Die Genehmigung für einen Einkaufsbeleg wird angefordert*,  
    *Die Genehmigung für einen Verkaufsbeleg wird angefordert* oder  
    *Die Genehmigung für einen Kreditor wird angefordert*.
7. Flow fordert Sie auf, ein Unternehmen innerhalb Ihres [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tenants und sämtliche Bedingungen in Ihren Daten, die Sie abhören möchten auszuwählen. 

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Business Central Daten verbunden und sind bereit, Ihren Flow zu bauen. 

8. Um einer aus einer Vorlage zu erstellen, wählen Sie die Option **Auf Vorlage erstellen** aus.
9. Suchen Sie nach **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**-Vorlangen. 
10. Aus der Liste der verfügbaren Vorlangen wählen Sie eine der verfügbaren Vorlangen aus:  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsauftrag anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsangebot anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsrechnung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Verkaufsgutschrift anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Kunden anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Einkaufsbestellung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Einkaufsrechnung anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-EInkaufsgutschrift anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Artikel anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Anbieter anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Fibu Buch.-Blattname anfordern*,  
    *Genehmigung für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Fibu Buch.-Blattzeilen anfordern*.  
11. Flow fordert Sie auf, den Mandanten innerhalb Ihres Tenants [!INCLUDE[d365fin_md](includes/d365fin_md.md)] auszuwählen. Da jede Schritt im Flow unabhängig vom darauffolgenden ist, werden Sie möglicherweise aufgefordert, den Mandanten mehrmals zu definieren, wenn Sie eine Vorlage [!INCLUDE[d365fin_md](includes/d365fin_md.md)] verwenden.
12. Die Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Vorlage integriert mit dem Kernworkflowmodul in Microsoft[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Das Bedeutet, wenn Sie eine dieser Vorlagen verwenden, um den Flow zu erstellen, wird ein entsprechender Workflow in Microsoft erstellt [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Informationen finden Sie in der Workflow-Dokumentation für Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

Weitere Informationen finden Sie in der [Flow-Dokumentation](https://docs.microsoft.com/en-us/flow/getting-started).

Bei Problemen mit Microsoft Flow siehe [Problembehandlung Integration mit Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Siehe auch
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)   
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-Workflows verwalten](across-use-workflows.md)  
[Genehmigungsbenutzereinrichtung](across-how-to-set-up-approval-users.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

