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
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
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
3. Im Fenster **My Flows** wählen Sie die Option **Aus Leer erstellen** aus.
4. Aus der Liste der verfügbaren Triggern, wählen Sie einen der [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbaren Trigger aus:  
    *Die Genehmigung für einen Debitor wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattname wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattzeile wird angefordert*,  
    *Die Genehmigung für einen Artikel wird angefordert*,  
    *Die Genehmigung für einen Einkaufsbeleg wird angefordert*,  
    *Die Genehmigung für einen Verkaufsbeleg wird angefordert* oder  
    *Die Genehmigung für einen Kreditor wird angefordert*.
5. Flow fordert Sie auf, den Mandanten innerhalb Ihres Tenants [!INCLUDE[d365fin](includes/d365fin_md.md)] auszuwählen. Da jede Schritt im Flow unabhängig vom darauffolgenden ist, werden Sie möglicherweise aufgefordert, den Mandanten mehrmals zu definieren, wenn Sie eine Vorlage [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden.

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Business Central Daten verbunden und sind bereit, Ihren Flow zu bauen. Weitere Informationen finden Sie in der [Flow Dokumentation](https://flow.microsoft.com/documentation/getting-started/).

Bei Problemen mit Microsoft Flow siehe [Problembehandlung Integration mit Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Siehe auch
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)    
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

