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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528462"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[prodlong](includes/prodlong.md)] als Power BI-Datenquelle für das Erstellen von Berichten nutzen

Sie können Ihre [!INCLUDE[prodlong](includes/prodlong.md)]-Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.  

Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI haben. Sie müssen auch [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunterladen. Weitere Informationen finden Sie unter [Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>So fügen Sie [!INCLUDE[prodshort](includes/prodshort.md)] als Datenquelle in Power BI Desktop hinzu

1. In Power BI Desktop im linken Navigationsbereich, wählen Sie **Daten abrufen** aus.
2. Auf der Seite **Daten abrufen** wählen Sie **Onlinedienste** aus, wählen Sie **Microsoft Dynamics 365 Business Central** und dann die Schaltfläche **Verbinden** aus.
3. Power BI zeigt einen Assistenten an, der Sie durch den Verbindungsprozess führt, einschließlich der Anmeldung bei [!INCLUDE[prodshort](includes/prodshort.md)]. Wählen Sie **Anmelden**, und wählen Sie dann das entsprechende Konto. Verwenden Sie dasselbe Konto, mit dem Sie sich bei [!INCLUDE[prodshort](includes/prodshort.md)] anmelden.
4. Klicken Sie auf die Schaltfläche **Verbinden** zum Fortfahren. Der Power BI-Assistent zeigt eine Liste von Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-Umgebungen, Unternehmen und Datenquellen an. Diese Datenquellen repräsentieren alle Webdienste, die Sie ab [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlicht haben.

    Sie können stattdessen auch eine neue Webdienst-URL in [!INCLUDE[prodshort](includes/prodshort.md)] erstellen. Wählen Sie eine der folgenden Methoden:

      - Verwenden Sie die Aktion **Datensatz erstellen** auf der Seite **Webdienste**
      - Verwenden Sie den Leitfaden **Berichte einrichten** Unterstützte Einrichtung
      - Wählen Sie in einer beliebigen Liste die Aktion **Bearbeiten in Excel**

5. Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.
6. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE[prodshort](includes/prodshort.md)] oder andere Daten Ihrem Power BI Datenmodell hinzuzufügen.

> [!NOTE]  
> Sobald Sie sich erfolgreich verbunden haben mit [!INCLUDE[prodshort](includes/prodshort.md)] werden Sie nicht mehr aufgefordert, sich anzumelden.

Sobald die Daten geladen sind, können Sie sie in der rechten Navigation auf der Seite sehen. Sie haben die Verbindung zu Ihren [!INCLUDE[prodshort](includes/prodshort.md)]-Daten erfolgreich hergestellt, und Sie können mit dem Aufbau Ihres Power BI-Berichts beginnen.  

Bevor Sie Ihren Bericht erstellen, empfiehlt es sich, die Microsoft [!INCLUDE[prodshort](includes/prodshort.md)] Designndatei zu importieren.  Die Designdatei erstellt eine Farbpalette, damit Sie Berichte im selben Farbstil erstellen können, wie bei den Microsoft [!INCLUDE[prodshort](includes/prodshort.md)] Anwendungen, ohne benutzerdefinierte Farben für jede Grafik definieren zu müssen.

Weitere Informationen finden Sie in der [Power BI-Dokumentation](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
