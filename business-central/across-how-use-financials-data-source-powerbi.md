---
title: Berichterstellung für Business Central in Power BI einrichten | Microsoft Docs
description: Sie können Ihre Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: ca4c27eaa1fe66e9bee678d6ec197fee7b928bdd
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798962"
---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] als Power BI-Datenquelle für das Erstellen von Berichten nutzen
Sie können Ihre [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.  

Sie müssen ein gültiges Konto bei [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] und Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen.  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>So fügen Sie [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] als Datenquelle in Power BI Desktop hinzu
1. In Power BI Desktop im linken Navigationsbereich, wählen Sie **Daten abrufen** aus.
2. Auf der Seite **Daten abrufen** wählen Sie **Onlinedienste** aus, wählen Sie **Microsoft Dynamics 365 Business Central** und dann die Schaltfläche **Verbinden** aus.
3. Power BI zeigt einen Assistenten an, der Sie durch den [Verbindungsvorgang](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md) führt. Sie werden aufgefordert, sich beim Service anzumelden. Wählen Sie **Anmelden** und wählen Sie das Konto aus, bei dem Sie sich anmelden möchten. Dieses sollte das gleiche Konto sein, bei dem Sie sich bei [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] anmelden.
4. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. Der Power BI-Assistent zeigt eine Liste der Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-Unternehmen und Datenquellen an. Diese Datenquelle ist für alle Webdienste, die Sie von jedem Unternehmen in Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] veröffentlicht haben.
5. Sie können einen neuen Webdienst URL in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.
6. Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.
7. Wiederholen Sie die vorherigen Schritte, um zusätzliche Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] oder andere Daten Ihrem Power BI-Datenmodell hinzuzufügen.

> [!NOTE]  
> Sobald Sie sich erfolgreich mit Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] verbunden haben, werden Sie nicht mehr aufgefordert, sich anzumelden.

Sobald die Daten geladen sind, erscheinen Sie in der rechten Navigation auf der Seite. Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Daten verbunden und sind bereit, Ihren Power BI-Bericht zu erstellen. 

Bevor Sie Ihren Bericht erstellen, empfiehlt es sich, die Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Designdatei zu importieren.  Die Designdatei erstellt eine Farbpalette, damit Sie Berichte im selben Farbstil erstellen können, wie bei den Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Inhaltspacks, ohne benutzerdefinierte Farben für jede Grafik definieren zu müssen.

Weitere Informationen finden Sie in der [Power BI-Dokumentation](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finanzen](finance.md)  
[Verbinden von Power BI mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
