---
title: Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs
description: Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe PowerApps zu erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540269"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe PowerApps zu erstellen
Sie können die Daten [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in PowerApps bereitstellen.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] mit PowerApps haben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Als [!INCLUDE[d365fin](includes/d365fin_md.md)] Datenquelle in PowerApps hinzufügen
1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) gehen und sich dann anmelden.
2. Auf der Homepage wählen Sie die Vorlage **Beginn von Daten**, um eine neue Canvas-App zu erstellen. Die App ist zur Verwendung auf einem mobilen Gerät vorgesehen, aber Sie können auch wählen, eine eigene Vorlage zu verwenden.

    Der nächste Schritt, um ein PowerApp zu erstellen ist die Auswahl der Daten. Wählen Sie das Pfeilsymbol aus und wählen Sie dann die Option **Neue Verbindung** in der oberen linken Seite der Seite aus.
3. In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.

    PowerApps verbinden sich mit Ihrem[!INCLUDE [prodshort](includes/prodshort.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden. Wenn Sie KEIN Administrator Ihrer [!INCLUDE [prodshort](includes/prodshort.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.  

4. Wenn Sie mehr als ein Unternehmen in Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] haben, müssen Sie das Unternehmen auswählen, mit dem Sie sich verbinden möchten. Dann zeigt PowerApps eine Liste der *Tabellen* an, die von [!INCLUDE [prodshort](includes/prodshort.md)] verfügbar sind. Diese so genannten Tabellen sind Teil der [!INCLUDE [prodshort](includes/prodshort.md)] API. Sie müssen die Endpunkte nicht selber konfigurieren, der [!INCLUDE [prodshort](includes/prodshort.md)] Connector für PowerApps macht dies für Sie.  

    Wenn Sie Daten aus anderen Tabellen in Ihrer [!INCLUDE [prodshort](includes/prodshort.md)] App hinzufügen möchten, dann müssen Sie mit einem Entwickler arbeiten, um benutzerdefinierte API in [!INCLUDE [prodshort](includes/prodshort.md)] zu definieren und diese benutzerdefinierte API durch einen benutzerdefinierten Connector in PowerApps zu verbrauchen. Weitere Informationen finden Sie unter [Erstellen Sie einen benutzerdefinierten Connector von Grund auf neu](/connectors/custom-connectors/define-blank).  

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE [prodshort](includes/prodshort.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen. Sie können zusätzliche Bildschirme hinzufügen und an weitere Daten von Ihrem  [!INCLUDE [prodshort](includes/prodshort.md)] anschließen. Weitere Informationen finden Sie unter [Erstellen Sie eine Canvas-App aus einer Vorlage in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen. Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Wenn Sie [!INCLUDE [prodshort](includes/prodshort.md)] lokal verbinden möchten, müssen Sie den**Business Central (lokal)** Connector in Schritt 3 auswählen.  

## <a name="see-also"></a>Siehe auch

[Erstellen Sie eine Canvas-App aus einer Vorlage in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
