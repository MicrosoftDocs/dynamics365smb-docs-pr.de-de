---
title: Daten mithilfe von Flow verbinden| Microsoft Docs
description: "Sie können Financials als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow erstellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

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
    ,*Wenn ein Datensatz erstellt wird*  
    ,*Wenn ein Datensatz gelöscht wird*  
    ,*Wenn ein Datensatz geändert wird*  
    *Die Genehmigung für einen Debitor wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattname wird angefordert*,  
    *Genehmigung von Fibu Buch.-Blattzeile wird angefordert*,  
    *Die Genehmigung für einen Artikel wird angefordert*,  
    *Die Genehmigung für einen Einkaufsbeleg wird angefordert*,  
    *Die Genehmigung für einen Verkaufsbeleg wird angefordert* oder  
    *Die Genehmigung für einen Kreditor wird angefordert*.
5. Flow fordert Sie zur Eingabe der Informationen auf, die benötigt werden, um sich mit Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zu verbinden. Wenn Sie eine der folgenden Trigger gewählt haben: *Wenn ein Datensatz erstellt wird*, *Wenn ein Datensatz geändert wird* oder *Wenn ein Datensatz gelöscht wird*, müssen Sie einen Namen und einen Tabellennamen auswählen. Mit jedem anderen Trigger wird nur der Name der Unternehmung benötigt, um zu verbinden.

   Flow zeigt eine Liste der Unternehmungen und Tabellen an, die in [!INCLUDE[d365fin](includes/d365fin_md.md)]verfügbar sind. Diese Tabellen oder Endpunkte stehen für alle Webdienste, die Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.

   Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Finance and Operations, Business edition-Daten verbunden und sind bereit, Ihren Flow zu erstellen. Weitere Informationen finden Sie in der [Flow Dokumentation](https://flow.microsoft.com/documentation/getting-started/).

Bei Problemen mit Microsoft Flow siehe [Problembehandlung Integration mit Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Siehe auch
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)    
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

