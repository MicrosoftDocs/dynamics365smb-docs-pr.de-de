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
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: 9cad9c7e2b54506e60af7d38d42f413599a44d01
ms.openlocfilehash: 7b9140611a47b8b823274763731cf000258c681e
ms.contentlocale: de-de
ms.lasthandoff: 04/03/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Power BI mit den Dynamics 365 Business Central-Inhaltspaketen verbinden
Einblicke in Ihre Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Daten zu erhalten ist mit Power BI und dem Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Inhaltspaket sehr einfach. Power BI ruft die Daten ab und erstellt ein Standarddashboard und Berichte auf Grundlage der Daten.

Sie müssen ein gültiges Konto mit Dynamics 365 und Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen, wenn Sie Ihre eigenen Power BI-Berichte erstellen möchten. Power BI Inhaltpakete benötigen Berechtigungen für die Tabellen, aus denen Daten abgerufen werden. Weitere Einzelheiten auf den Anforderungen werden im Folgenden beschrieben.  

## <a name="how-to-connect"></a>So stellen Sie die Verbindung her
1. Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.  
![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Sie können auch aus Dynamics 365 Business Edition heraus beginnen. Im Rollencenter navigieren Sie zu **Berichtsauswahl** im Power BI-Rollencenterteil. Wählen Sie entweder **Service** oder **Mein Unternehmen** im Menüband aus. Wenn eine dieser Aktionen ausgewählt wird, gelangen Sie zu der jeweiligen Dienstgalerie in Power BI oder zu der Dienstbibliothek in Power BI, die zudem so gefiltert ist, dass nur Inhaltspakete zu [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] angezeigt werden.

2. Im Feld **Dienste** wählen Sie **Abrufen** aus. Dadurch wird ein Fenster mit **AppSource** und **Apps für Power BI Apps** geöffnet.  
![Wählen Sie Inhaltspakete von Onlinediensten aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Wählen Sie **Apps** auf der Registerkarte **Apps für Power BI Apps**, wählen Sie das Feld **Microsoft Dynamics 365 Business Central** Inhaltspakete, die Sie verwenden möchten, und wählen Sie dann **jetzt abrufen**.  
![Wählen Sie Dynamics 365 Business Central und wählen Sie "Jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Wenn Sie dazu aufgefordert werden, geben Sie in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] den Namen des *Unternehmens* ein. Dies ist nicht der Anzeigename. Der Name des Unternehmens kann auf der Seite „Unternehmen“ innerhalb Ihrer [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]- Instanz gefunden werden. 
![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Sobald verbunden, werden ein Dashboard, ein Bericht und ein Datensatz automatisch in Ihren Power BI Arbeitsbereich geladen. Wenn abgeschlossen, werden die Kacheln die Daten aus Ihrem [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-Unternehmen aktualisieren.
![Wählen Sie Dynamics 365 Business Central und wählen Sie jetzt abrufen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Was jetzt?

- Versuchen Sie im [Erstellen eine Frage im Q&A-Feld](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) im oberen Bereich des Dashboards.
- [Ändern Sie die Kacheln](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) im Dashboard.  
- [Wählen Sie eine Kachel aus](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.  
- Während Ihr Dataset täglich aktualisiert wird, können Sie den Aktualisierungsplan ändern oder ihn mithilfe von **jetzt aktualisieren** bei Bedarf aktualisieren.

## <a name="system-requirements"></a>Systemanforderungen
Um die Daten [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI zu importieren, müssen Sie Berechtigungen für den Webdiensten haben, um die Daten abzurufen. Die Web Services, die für jedes Inhaltspakete erforderlich sind:

## <a name="role-center-reports"></a>Rollencenterberichte

**Microsoft Dynamics 365 Business Central – CRM**
- Verkaufschancen
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbeschrifungen

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbeschrifungen

**Microsoft Dynamics 365 Business Central – Jobs**
- Projektübersicht
- Projektplanzeilen
- Projektaufgabenzeilen
- Power BI-Berichtsbeschrifungen
- Excel-Vorlage zur Unternehmensansicht

**Microsoft Dynamics 365 Business Central – Sales**
- Verkaufsdashboard
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbeschrifungen

## <a name="list-page-reports"></a>Berichte für Listenseite 

**Microsoft Dynamics 365 Business Central – Customers List**
- Artikel-Statistik nach Debitor
- Power BI - Artikeleinkaufsübersicht
- Power BI - Artikelverkaufsübersicht
- Verkaufsdashboard
- Power BI - Debitorenübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Power BI - Betrag im Hauptbuch - Übersicht
- Power BI - Hauptbuch - Budgetierter Betrag
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen

**Microsoft Dynamics 365 Business Central – Items List**
- Artikel-Statistik nach Debitor
- Power BI - Artikeleinkaufsübersicht
- Power BI - Artikelverkaufsübersicht
- Verkaufsdashboard
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen

**Microsoft Dynamics 365 Business Central – Jobs List**
- Power BI - Projektübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Power BI - Einkaufsübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Power BI - Verkaufsübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI - Artikeleinkaufsübersicht
- Power BI - Artikelverkaufsübersicht
- Power BI - Kreditorenübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbeschrifungen

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
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
[Einrichtungs-Berichterstellugn für [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)  

