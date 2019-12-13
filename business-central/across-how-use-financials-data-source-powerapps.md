---
title: Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs
description: Sie können Ihre Business Central-Daten als Datenquelle zur Verfügung stellen und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäftsanwendung mithilfe von Power Apps zu erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881000"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Verbinden mit Ihren Business Central-Daten, um eine Geschäftsanwendung mithilfe von Power Apps zu erstellen

Sie können Ihre [!INCLUDE[prodshort](includes/prodshort.md)]-Daten als Datenquelle in Power Apps bereitstellen.  

> [!NOTE]  
> Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und bei Power Apps haben.  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a>So wird [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power Apps hinzugefügt

1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/) gehen und sich dann anmelden.
2. Wählen Sie auf der Startseite die **Apps**, **Erstelle eine App** und **Canvas** um eine neue Canvas-App zu erstellen. Die App ist zur Verwendung auf einem mobilen Gerät vorgesehen, aber Sie können auch wählen, eine eigene Vorlage zu verwenden.

    Der nächste Schritt, um ein Power App zu erstellen ist die Auswahl der Daten. Wählen Sie das Pfeilsymbol aus und wählen Sie dann die Option **Neue Verbindung** in der oberen linken Seite der Seite aus.
3. In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.

    Power Apps verbinden sich mit Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden. Wenn Sie KEIN Administrator Ihrer [!INCLUDE [prodshort](includes/prodshort.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.  

4. Power Apps zeigt eine Liste der *Umgebungen und Unternehmuen* an, die in [!INCLUDE [prodshort](includes/prodshort.md)] verfügbar sind. Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten be finden, zu denen Sie eine Verbindung herstellen möchten. Als Nächstes wird eine Liste der APIs angezeigt. Wählen Sie die **API**, die Sie verbinden möchten.

Diese so genannten Tabellen sind Teil der [!INCLUDE [prodshort](includes/prodshort.md)] API. Sie müssen die Endpunkte nicht selber konfigurieren, der [!INCLUDE [prodshort](includes/prodshort.md)]-Connector für Power Apps macht dies für Sie.  

> [!NOTE]
> Wenn Sie Daten aus anderen Tabellen in Ihrer [!INCLUDE [prodshort](includes/prodshort.md)]-App hinzufügen möchten, dann müssen Sie mit einem Entwickler arbeiten, um eine benutzerdefinierte API in [!INCLUDE [prodshort](includes/prodshort.md)] zu definieren und diese benutzerdefinierte API dann durch einen benutzerdefinierten Connector in Power Apps zu verbrauchen. Weitere Informationen finden Sie unter [Erstellen Sie einen benutzerdefinierten Connector von Grund auf neu](/connectors/custom-connectors/define-blank).  

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE [prodshort](includes/prodshort.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen. Sie können zusätzliche Bildschirme hinzufügen und an weitere Daten von Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] anschließen. Weitere Informationen finden Sie unter [Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen. Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Wenn Sie [!INCLUDE [prodshort](includes/prodshort.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector in Schritt 3 auswählen.  

## <a name="see-also"></a>Siehe auch

[Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
