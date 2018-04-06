---
title: Business Central und Power BI Inhaltspakete verbinden | Microsoft Docs
description: Nutzen Sie Einblicke in Business Central mit Power BI und dem Business Central-Inhaltspaket.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a>Power BI mit den Business Central Inhaltspakenten verbinden
Einblicke in Ihre Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Daten zu erhalten ist mit Power BI und dem Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Inhaltspaket sehr einfach. Power BI ruft die Daten ab und erstellt ein Standarddashboard und Berichte auf Grundlage der Daten.

> [!NOTE]  
>  Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen.  
>  Power BI Inhaltpakete benötigen Berechtigungen für die Tabellen, aus denen Daten abgerufen werden. Weitere Einzelheiten auf den Anforderungen werden im Folgenden beschrieben.  

## <a name="how-to-connect"></a>So stellen Sie die Verbindung her
1. Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.  
![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. Im Feld **Dienste** wählen Sie **Abrufen** aus. Dadurch wird ein Fenster mit **AppSource** und **Apps für Power BI Apps** geöffnet.  
![Wählen Sie Inhaltspakete von Onlinediensten aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Wählen Sie **Apps** auf der Registerkarte **Apps für Power BI Apps**, und wählen Sie das Feld **Microsoft Dynamics 365 Business Central** Inhaltspakete, die Sie verwenden möchten, und wählen Sie dann **jetzt abrufen**.  
![Wählen Sie Dynamics 365 Business Central und wählen Sie "Jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Wenn Sie dazu aufgefordert werden, geben Sie in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] den Namen des *Unternehmens* ein. Dies ist nicht der Anzeigename.  
![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Sobald verbunden, werden ein Dashboard, ein Bericht und ein Datensatz automatisch in Ihren Power BI Arbeitsbereich geladen. Wenn abgeschlossen werden die Kacheln die Daten aus dem Konto aktualisieren.
![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Was jetzt?

- [Ändern Sie die Kacheln](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) im Dashboard.  
- [Wählen Sie eine Kachel aus](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.  
- Während Ihr Dataset täglich aktualisiert wird, können Sie den Aktualisierungsplan ändern oder ihn mithilfe von **jetzt aktualisieren** bei Bedarf aktualisieren.

## <a name="system-requirements"></a>Systemanforderungen
Um die Daten [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI zu importieren, müssen Sie Berechtigungen für den Webdiensten haben, um die Daten abzurufen. Die Web Services, die für jedes Inhaltspakete erforderlich sind:

**Microsoft Dynamics 365 Business Central – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Sales**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Jobs**
- Projektübersicht
- Projektplanzeilen
- Projektaufgabenzeilen

**Microsoft Dynamics 365 Business Central – Customers List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard
- Power_BI_Customer_List
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Items List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Artikel
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 Business Central – Vendors List**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Artikel
- SalesDashboard
- Power_BI_Customer_List
- ItemSalesbyCustomer
- Power_BI_Vendor_List
- ExcelTemplateViewCompany

## <a name="web-services"></a>Webdienste
Eine einfache Methode, die Webdienste zu finden ist, in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nach Webdiensten zu suchen. In der Übersicht stellen Sie sicher, dass das Veröffentlichungsfeld für die oben aufgeführten Webdienste markiert wird.

## <a name="troubleshooting"></a>Problembehebung
Das Power BI-Dashboard beruht auf den veröffentlichten Webdiensten, die oben erwähnten werden. Es enthält Daten vom Demomandanten oder von Ihrem eigenen Unternehmen wenn Sie Daten aus der aktuellen Finanzlösung importieren. Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.

### <a name="incorrect-company-name"></a>Ungültiger Unternehmensnamen  
Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben. Unternehmensnamensuche für **Unternehmen** zu suchen. Verwenden Sie das Feld **Name**, wenn Sie den Unternehmensnamen eingeben.

### <a name="incorrect-user-name-and-password"></a>Falscher Benutzername und Kennwort  
Der Benutzername und das Kennwort, die zum Verbinden verwendet werden, sind dieselben, die verwendet werden, um die Verbindung mit Ihrem  Microsoft Office 365 Konto herzustellen.  

Die Inhaltspakete erfordern, dass Sie ein Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben. Nachdem Sie Ihre Anmeldeinformationen eingeben haben, erkennen wir sämtliche Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Tenants, auf die Sie Zugriff haben. Wenn Sie kein lizenziertes oder Probe-Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben, erhalten Sie eine Fehlermeldung.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Der Schlüssel glich keinen Zeilen in der Tabelle
Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle". Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.

## <a name="see-also"></a>Siehe auch
[Erste Schritte mit Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Grundmodelle](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Einrichtungs-Berichterstellugn für [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)  

