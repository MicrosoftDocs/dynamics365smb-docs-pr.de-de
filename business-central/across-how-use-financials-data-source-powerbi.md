---
title: Berichte für Business Central in Power BI verwenden | Microsoft Docs
description: Sie können Ihre Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 01/13/2020
ms.author: edupont
ms.openlocfilehash: a069fb7df3738b1f42aa2ddc86ce95144c39daff
ms.sourcegitcommit: ead69ebe5b29927876a4fb23afb6c066f8854591
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2020
ms.locfileid: "2952842"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE [prodlong](includes/prodlong.md)] als Power BI-Datenquelle für das Erstellen von Berichten nutzen

Sie können Ihre [!INCLUDE[prodlong](includes/prodlong.md)]-Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.  

Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunterladen. Weitere Informationen finden Sie unter [Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>So fügen Sie [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power BI Desktop hinzu

1. In Power BI Desktop im linken Navigationsbereich, wählen Sie **Daten abrufen** aus.
2. Auf der Seite **Daten abrufen** wählen Sie **Onlinedienste** aus, wählen Sie **Microsoft Dynamics 365 Business Central** und dann die Schaltfläche **Verbinden** aus.
3. Power BI zeigt einen Assistenten an, der Sie durch den Verbindungsvorgang führt. Sie werden aufgefordert, sich beim [!INCLUDE [prodshort](includes/prodshort.md)] anzumelden. Wählen Sie **Anmelden** und wählen Sie das Konto aus, bei dem Sie sich anmelden möchten. Dieses sollte das gleiche Konto sein, bei dem Sie sich bei [!INCLUDE [prodshort](includes/prodshort.md)] anmelden.
4. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. Der Power BI Assistent zeigt eine Liste der Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] Umgebungen, Unternehmen und Datenquellen an. Diese Datenquelle ist für alle Webdienste, die Sie von jedem Tenant/Unternehmen in Microsoft [!INCLUDE [prodshort](includes/prodshort.md)] veröffentlicht haben.
5. Sie können einen neuen Webdienst URL in [!INCLUDE [prodshort](includes/prodshort.md)] erstellen, indem Sie die **Erstellen Dataset** Aktion der Seite **Webdienste** nutzen, indem Sie die unterstütze Hilfe **Bericht einrichten** verwenden oder die Aktion **Bearbeiten in Excel** in einer beliebigen Liste wählen.
6. Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.
7. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE [prodshort](includes/prodshort.md)] oder andere Daten Ihrem Power BI Datenmodell hinzuzufügen.

> [!NOTE]  
> Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE [prodshort](includes/prodshort.md)] werden Sie nicht mehr aufgefordert, sich anzumelden.

Sobald die Daten geladen sind, erscheinen Sie in der rechten Navigation auf der Seite. Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren Microsoft [!INCLUDE [prodshort](includes/prodshort.md)] Daten verbunden und sind bereit, Ihren Power BI Bericht zu erstellen.  

Bevor Sie Ihren Bericht erstellen, empfiehlt es sich, die Microsoft [!INCLUDE [prodshort](includes/prodshort.md)] Designndatei zu importieren.  Die Designdatei erstellt eine Farbpalette, damit Sie Berichte im selben Farbstil erstellen können, wie bei den Microsoft [!INCLUDE [prodshort](includes/prodshort.md)] Anwendungen, ohne benutzerdefinierte Farben für jede Grafik definieren zu müssen.

Weitere Informationen finden Sie in der [Power BI-Dokumentation](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-related-training-at-microsoft-learnlearnmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
