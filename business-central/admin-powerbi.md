---
title: Business Central und Power BI-Inhaltspakete | Microsoft Docs
description: Einblicke, Business Intelligence und KPIs aus Ihren Business Central-Daten zu beziehen, ist einfach mit Power BI und den Business Central-Inhaltspaketen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: f51de349c4b13eaabd185cdb728d59006dfe6db6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "916374"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivieren Sie Ihre Geschäftsdaten für Power BI
Einblicke in Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten zu erhalten zu erhalten, ist mit Power BI und den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Inhaltspaketen sehr einfach. Power BI ruft Ihre Daten ab und erstellt dann ein vorkonfiguriertes Dashboard und Berichte auf Grundlage dieser Daten.  

Sie müssen ein gültiges Konto mit Dynamics 365 und mit Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) herunterladen, wenn Sie Ihre eigenen Power BI-Berichte erstellen möchten. Power BI-Inhaltspakete benötigen Berechtigungen für die Tabellen, aus denen Daten abgerufen werden. Weitere Einzelheiten auf den Anforderungen werden im Folgenden beschrieben.  

Microsoft hat folgende Inhaltspakete veröffentlicht:

| App | Description |
| --- | --- |
| Microsoft Business Central | Gewährt ein Dashboard mit Schlüsselfinanzdaten im Zeitverlauf, z.B. Umsatz von Ausgaben, Deckungsbeiträgen % und Geldumlauf.|
| Microsoft Business Central - CRM | Gewährt ein Dashboard mit Schlüsseldaten zu Verkaufschancen und Kontakten.  |
| Microsoft Business Central - Sales | Gewährt ein Dashboard mit Schlüsseldaten zu Verkaufschancen und Bestand. |

## <a name="using-the-dashboards"></a>Dashboards nutzen
Jedes Inhaltspaket enthält Berichte, die Sie aufrufen können in:

* Wählen Sie eine Darstellung im Dashboard, um einen der Berichte anzuzeigen.  
* Filtern Sie den Bericht oder fügen Sie Felder hinzu, die Sie überwachen möchten.  
* Heften Sie diese benutzerdefinierte Ansicht an das Dashboard an, um sie weiter zu Verfolgen.  
  Sie können Daten auch manuell aktualisieren, und Sie können einen Aktualisierungsplan einrichten. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Das Inhaltspaket ist vorkonfiguriert, um mit Umsatzdaten und Finanzdaten aus dem Demounternehmen zu arbeiten, das Sie erhalten, wenn Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden. Wenn Sie die Apps in Power BI installieren und Sie eine Verbindung zu Ihren eigenen Daten herstellen, funktionieren einige Berichte möglicherweise nicht, da sie auf Daten beruhen, über die Ihr Unternehmen nicht verfügt. In diesen Fällen können Sie den Bericht von Ihrem Dashboard einfach entfernen.  

> [!NOTE]  
>   Sie können auch Ihre eigenen Berichte und Dashboards in Power BI auf Grundlage Ihrer Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen. Weitere Informationen finden Sie unter [Verbindung Ihrer Geschäftsdaten mit Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>So stellen Sie die Verbindung her
1. Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.  
![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Sie könne möglicherweise auch von Dynamics 365 Business Edition aus starten. Im Rollencenter navigieren Sie zu **Berichtsauswahl** im Power BI-Rollencenterteil. Wählen Sie entweder **Service** oder **Mein Unternehmen** im Menüband aus. Wenn eine dieser Aktionen ausgewählt wird, gelangen Sie zur Organisationsgalerie in Power BI oder zu der Dienstbibliothek in Power BI, die zudem so gefiltert wird dass nur Inhaltspakete zu [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] angezeigt werden.

2. Im Feld **Dienste** wählen Sie **Abrufen** aus. Dadurch wird eine Seite mit der **AppSource** und **Apps für Power BI-Apps** geöffnet.  
![Wählen Sie Inhaltspakete von Onlinediensten aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Wählen Sie **Apps** auf der Registerkarte **Apps für Power BI-Apps**, wählen Sie das Inhaltspaket **Microsoft Dynamics 365 Business Central** aus, das Sie verwenden möchten, und wählen Sie dann **Jetzt abrufen** aus.  
![Wählen Sie Dynamics 365 Business Central aus, und wählen Sie dann „Jetzt abrufen” aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Wenn Sie dazu aufgefordert werden, geben Sie in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] den Namen des *Unternehmens* ein. Dies ist nicht der Anzeigename. Der Name des Unternehmens kann auf der Seite „Unternehmen“ innerhalb Ihrer [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]- Instanz gefunden werden.  
![Wählen Sie Dynamics 365 Business Central aus, und wählen Sie dann „Jetzt abrufen” aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Sobald verbunden, werden ein Dashboard, ein Bericht und ein Dataset automatisch in Ihren Power BI-Arbeitsbereich geladen. Wenn abgeschlossen, werden die Kacheln die Daten aus Ihrem [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-Unternehmen aktualisieren.
![Wählen Sie Dynamics 365 Business Central aus, und wählen Sie dann „Jetzt abrufen” aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Was jetzt?

- Versuchen Sie im [Erstellen eine Frage im Q&A-Feld](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) im oberen Bereich des Dashboards.
- [Ändern Sie die Kacheln](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) im Dashboard.  
- [Wählen Sie eine Kachel aus](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.  
- Während Ihr Dataset täglich aktualisiert wird, können Sie den Aktualisierungsplan ändern oder ihn mithilfe von **jetzt aktualisieren** bei Bedarf aktualisieren.

## <a name="system-requirements"></a>Systemanforderungen
Um die [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-Daten in Power BI zu importieren, müssen Sie Berechtigungen für die Webdienste haben, um Daten abzurufen. Die Web Services, die für jedes Inhaltspakete erforderlich sind:

## <a name="role-center-reports"></a>Rollencenterberichte

**Microsoft Dynamics 365 Business Central – CRM**
- Verkaufschancen
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central – Jobs**
- Projektübersicht
- Projektplanzeilen
- Projektaufgabenzeilen
- Power BI-Berichtsbezeichnungen
- Excel-Vorlage zur Unternehmensansicht

**Microsoft Dynamics 365 Business Central - Sales**
- Verkaufsdashboard
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbezeichnungen

## <a name="list-page-reports"></a>Berichte für Listenseite

**Microsoft Dynamics 365 Business Central – Customers List**
- Artikel-Statistik nach Debitor
- Power BI-Artikeleinkaufsübersicht
- Power BI-Artikelverkaufsübersicht
- Verkaufsdashboard
- Power BI-Debitorenübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Power BI-Sachkontobetragsübersicht
- Power BI – budgetierter Betrag des Sachkontos
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central – Items Listt**
- Artikel-Statistik nach Debitor
- Power BI-Artikeleinkaufsübersicht
- Power BI-Artikelverkaufsübersicht
- Verkaufsdashboard
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central – Jobs List**
- Power BI-Projekte-Übersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Power BI-Einkaufsübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Power BI-Verkaufsübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen


**Microsoft Dynamics 365 Business Central – Vendors List**
- Power BI-Artikeleinkaufsübersicht
- Power BI-Artikelverkaufsübersicht
- Power BI-Kreditorenübersicht
- ExcelTemplateViewCompany
- Power BI-Berichtsbezeichnungen

## <a name="web-services"></a>Webdienste
Eine einfache Methode, die Webdienste zu finden ist, in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nach Webdiensten zu suchen. In der Übersicht stellen Sie sicher, dass das Veröffentlichungsfeld für die oben aufgeführten Webdienste markiert wird.

## <a name="troubleshooting"></a>Problembehebung
Das Power BI-Dashboard beruht auf den veröffentlichten Webdiensten, die oben aufgeführt werden. Es enthält Daten vom Demounternehmen oder von Ihrem eigenen Unternehmen, wenn Sie Daten aus Ihrer aktuellen Finanzlösung importieren. Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.

### <a name="incorrect-company-name"></a>Ungültiger Unternehmensnamen  
Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben. Unternehmensnamensuche für **Unternehmen** zu suchen. Verwenden Sie das Feld **Name**, wenn Sie den Unternehmensnamen eingeben.

### <a name="incorrect-user-name-and-password"></a>Falscher Benutzername und Kennwort  
Der Benutzername und das Kennwort, die zum Verbinden verwendet werden, sind dieselben, die verwendet werden, um die Verbindung mit Ihrem Microsoft Office 365-Konto herzustellen.  

Die Inhaltspakete erfordern, dass Sie ein Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben. Nachdem Sie Ihre Anmeldeinformationen eingeben haben, erkennen wir sämtliche Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Tenants, auf die Sie Zugriff haben. Wenn Sie kein lizenziertes oder Probe-Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Konto haben, erhalten Sie eine Fehlermeldung.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Der Schlüssel glich keinen Zeilen in der Tabelle
Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle". Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.

## <a name="see-also"></a>Siehe auch
[Erste Schritte mit Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Grundlegende Konzepte](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI Datenquelle](across-how-use-financials-data-source-powerapps.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] in Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
