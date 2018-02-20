---
title: "Berichterstattung für Finance and Operations, Business edition in Power BI | Microsoft Docs einrichten"
description: "Sie können Ihre Daten in Financials als Datenquelle in Power BI bereitstellen und leistungsstarke Berichte über den Zustand des Geschäftes erstellen."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 056761b398737bd052b68488756198051f0cdb9a
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] Power BI als Datenquelle für das Erstellen von Berichten nutzen
Sie können Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand des Geschäftes erstellen.  

> [!NOTE]  
> Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Um [!INCLUDE[d365fin](includes/d365fin_md.md)] als Datenquelle in Power BI Desktop hinzufügen
1. In Power BI Desktop im linken Navigationsbereich, wählen Sie **Daten abrufen** aus.
2. Im Fenster **Daten abrufen** wählen Sie **Onlineservices** aus, wählen Sie **Dynamics 365 for Finance and Operations, Business edition** und dann die Schaltfläche **Verbinden**aus.
3. Power BI zeigt einen Assistenten an, der Sie durch den [Verbindungsvorgang](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md) führt. Der erste Schritt besteht darin, sich beim Service anzumelden. Wählen Sie **Anmelden** und wählen Sie das Konto aus, bei dem Sie sich anmelden möchten. Dieses sollte das gleiche Konto sein, bei dem Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden.
4. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. Der Power BI Assistent zeigt eine Liste der [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen und Datenquellen an. Diese Datenquelle ist für alle Webdienste, die Sie von jeder Unternehmung in [!INCLUDE[d365fin](includes/d365fin_md.md)] veröffentlicht haben.
5. Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.
6. Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.
7. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten Ihrem Power BI Datenmodell hinzuzufügen.

> [!NOTE]  
> Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Sie nicht mehr aufgefordert, sich anzumelden.

Sobald die Daten geladen sind, erscheinen Sie in der rechten Navigation auf der Seite. Zu diesem Zeitpunkt haben Sie erfolgreich Ihre Finance and Operations, Business edition-Daten verbunden und sind bereit, Ihren Power BI Bericht zu erstellen. Weitere Informationen finden Sie in der [Power BI Dokumentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finanzen](finance.md)  
[Power BI mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md) verbinden  

