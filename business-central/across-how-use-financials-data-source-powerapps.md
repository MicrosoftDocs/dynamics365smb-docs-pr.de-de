---
title: 'Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs'
description: 'Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe von Power Apps zu erstellen.'
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe von Power Apps zu erstellen

Sie können die [!INCLUDE[prod_short](includes/prod_short.md)] Daten als Datenquelle in Power Apps bereitstellen.  

> [!TIP]  
> Business Central bietet jetzt Entwicklungs- und Betriebsunterstützung für Power Platform in AL-Go sowie Beispiele, die Ihnen den Einstieg in die Erstellung Ihrer eigenen Apps mit Power Apps erleichtern. Diese Funktionen befinden sich derzeit in der Vorschau. Weitere Informationen finden Sie unter [Business Central und Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) in der Hilfe für Entwickler und IT-Profis.

## Voraussetzungen

Sie müssen ein gültiges Konto bei [!INCLUDE[prod_short](includes/prod_short.md)] und Power Apps haben.  

## [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power Apps hinzufügen

Mit diesen Schritten wird eine Business Central-Tabelle, wie Kunden oder Artikel, als Datenquelle einer Power Apps-App hinzugefügt.

1. Gehen Sie in Ihrem Browser zu [powerapps.microsoft.com](https://powerapps.microsoft.com/) und melden Sie sich dann an.
2. Wählen Sie im Navigationsbereich auf der linken Seite **+ Erstellen** und dann **Weitere Datenquellen** auf der Seite **App erstellen** aus.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. In der Liste **Verbindungen** werden alle bestehenden Datenverbindungen angezeigt, die Sie haben.

   - Wenn bereits eine **Business Central**-Verbindung besteht, wählen Sie diese aus und wählen Sie dann **Erstellen** aus.

   - Wenn Sie keine Business Central-Verbindung sehen, wählen Sie **+ Neue Verbindung** aus, suchen Sie danach und wählen Sie **Business Central** und dann **Erstellen** aus.

   > [!NOTE]
   > Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector auswählen.  
  
4. Power Apps stellt eine Verbindung zu Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] her. Melden Sie sich mit den gültigen Benutzernamen und Kennwort von Business Central an. Wenn Sie kein Administrator Ihrer [!INCLUDE[prod_short](includes/prod_short.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.  
5. Sobald Sie angemeldet sind, zeigt Power Apps eine Liste der *Umgebungen und Unternehmen* an, die in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sind. Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten befinden, zu denen Sie eine Verbindung herstellen möchten, z. B. *PRODUKTION - Mein Unternehmen*.  
6. Als Nächstes wird eine Liste der Tabellen angezeigt, die als Teil der API für Ihre Umgebung bereitgestellt werden. Wählen Sie die Tabelle aus, zu der Sie eine Verbindung herstellen möchten, und wählen Sie dann **Verbinden** aus.

Diese sogenannten Tabellen werden von [!INCLUDE[prod_short](includes/prod_short.md)] Connector für Power Apps als Endpunkte bereitgestellt.  

> [!NOTE]
> Wenn Sie Daten aus anderen Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] in Ihre Anwendung aufnehmen möchten, müssen Sie mit einem Entwickler zusammenarbeiten, um eine benutzerdefinierte API in [!INCLUDE[prod_short](includes/prod_short.md)] zu definieren.  

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen. Sie können immer weitere Bildschirme hinzufügen und erhalten eine Verbindung zu weiteren Daten. Weitere Informationen finden Sie unter [Erstellen einer Canvas-App aus einem Beispiel in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen. Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## Siehe auch

[Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importieren von Geschäftsdaten aus anderen Finance-Systemen](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
