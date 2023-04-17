---
title: 'Verwenden Sie die Daten, um eine App zu erstellen| Microsoft Docs'
description: 'Sie können Daten aus Business Central zur Verfügung stellen und eine OData URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe von Power Apps zu erstellen.'
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2023
ms.author: jswymer
---
# Verknüpfung mit Business Central, um eine Geschäfts-App mithilfe von Power Apps zu erstellen

Sie können die [!INCLUDE[prod_short](includes/prod_short.md)] Daten als Datenquelle in Power Apps bereitstellen.  

> [!TIP]  
> Die zusätzliche Power Apps Dokumentation und unsere Power App-Beispiele, die während der [!INCLUDE[prod_short](includes/prod_short.md)] Einführungsveranstaltung vorgestellt wurden, werden später im Jahr 2023, Zyklus 1, hier veröffentlicht. Lesen Sie mehr unter [Erste Schritte mit weiteren Power Automate Beispielvorlagen und Power Apps](/dynamics365/release-plan/2023wave1/smb/dynamics365-business-central/get-started-more-sample-power-automate-templates-power-apps).

## Voraussetzungen

Sie müssen ein gültiges Konto bei [!INCLUDE[prod_short](includes/prod_short.md)] und Power Apps haben.  

## [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power Apps hinzufügen

1. In Ihrem Browser navigieren und zu [powerapps.microsoft.com](https://powerapps.microsoft.com/) gehen und sich dann anmelden.
2. Wählen Sie auf der Homepage im Abschnitt **Beginn von Daten** die Kachel **Andere Datenquellen** aus.  

    Dieser Schritt öffnet Power Apps Studio. Bei der ersten Anmeldung müssen Sie das Land/die Region angeben.  
3. In der Liste der verfügbaren Verbindungscodes wählen Sie **Business Central** und dann die Schaltfläche **Erstellen** aus.

    Power Apps verbinden sich mit Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Anmeldeinformationen, mit denen Sie sich anmelden. Wenn Sie kein Administrator Ihrer [!INCLUDE[prod_short](includes/prod_short.md)] sind, müssen Sie sich möglicherweise bei einem anderen Konto anmelden.  

4. Power Apps zeigt eine Liste der *Umgebungen und Unternehmungen* an, die in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sind. Wählen Sie die Umgebung und das Unternehmen aus, in der sich die Daten befinden, zu denen Sie eine Verbindung herstellen möchten, z. B. *PRODUKTION - Mein Unternehmen*.  

5. Als Nächstes wird eine Liste der Tabellen angezeigt, die als Teil der API für Ihre Umgebung bereitgestellt werden. Wählen Sie die Tabelle aus, zu der Sie eine Verbindung herstellen möchten, und wählen Sie dann **Verbinden** aus.

Diese sogenannten Tabellen werden von [!INCLUDE[prod_short](includes/prod_short.md)] Connector für Power Apps als Endpunkte bereitgestellt.  

> [!NOTE]
> Wenn Sie Daten aus anderen Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] in Ihre Anwendung aufnehmen möchten, müssen Sie mit einem Entwickler zusammenarbeiten, um eine benutzerdefinierte API in [!INCLUDE[prod_short](includes/prod_short.md)] zu definieren.  

Zu diesem Zeitpunkt haben Sie erfolgreich Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und sind bereit, Ihre Power App zu erstellen. Sie können weitere Bildschirme hinzufügen und an weitere Daten von Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] anschließen. Weitere Informationen finden Sie unter [Erstellen einer Canvas-App aus einem Beispiel in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Wenn Sie Ihre App entworfen und erstellt haben, können Sie diese mit Ihre Kollegen teilen. Weitere Informationen finden Sie unter [Speichern und veröffentlichen Sie eine Canvas-App in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verbinden möchten, müssen Sie den **Business Central (lokal)** Connector in Schritt 3 auswählen.  

## Siehe verwandte [Microsoft Schulungen](/training/paths/power-apps-power-automate-business-central/)

## Siehe auch

[Erstellen Sie eine Canvas-App aus einer Vorlage in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importieren von Geschäftsdaten aus anderen Finance-Systemen](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Erste Schritte mit dem Entwickeln von Verbindungs-Apps für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
