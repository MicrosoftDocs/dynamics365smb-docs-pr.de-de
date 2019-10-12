---
title: Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs
description: Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe von PowerApps zu erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305023"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe von PowerApps zu erstellen
Sie können die [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten als Datenquelle in PowerApps bereitstellen.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto bei [!INCLUDE[d365fin](includes/d365fin_md.md)] und PowerApps haben.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>So fügen Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in PowerApps hinzu
1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) gehen und sich dann anmelden.
2. Wählen Sie auf der Startseite die **Apps**, **Erstelle eine App** und **Canvas** um eine neue Canvas-App zu erstellen. Die App ist zur Verwendung auf einem mobilen Gerät vorgesehen, aber Sie können auch wählen, eine eigene Vorlage zu verwenden.

    Der nächste Schritt, um ein PowerApp zu erstellen ist die Auswahl der Daten. Wählen Sie das Pfeilsymbol aus und wählen Sie dann die Option **Neue Verbindung** in der oberen linken Seite der Seite aus.
3. In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.

    PowerApps PowerApps verbinden sich mit Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden. Wenn Sie KEIN Administrator Ihrer [!INCLUDE [prodshort](includes/prodshort.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.  

4.  PowerApps zeigt eine Liste der *Umgebungen und Unternehmungen* an, die in [!INCLUDE [prodshort](includes/prodshort.md)] verfügbar sind. Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten be finden, zu denen Sie eine Verbindung herstellen möchten. Als Nächstes wird eine Liste der APIs angezeigt. Wählen Sie die **API**, die Sie verbinden möchten.

Diese so genannten Tabellen sind Teil der [!INCLUDE [prodshort](includes/prodshort.md)] API. Sie müssen die Endpunkte nicht selber konfigurieren, der [!INCLUDE [prodshort](includes/prodshort.md)] Connector für PowerApps macht dies für Sie.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE [prodshort](includes/prodshort.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen. Sie können zusätzliche Bildschirme hinzufügen und an weitere Daten von Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] anschließen. Weitere Informationen finden Sie unter [Erstellen Sie eine Canvas-App aus einer Vorlage in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen. Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Wenn Sie [!INCLUDE [prodshort](includes/prodshort.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector in Schritt 3 auswählen.  

## <a name="see-also"></a>Siehe auch

[Erstellen Sie eine Canvas-App aus einer Vorlage in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
