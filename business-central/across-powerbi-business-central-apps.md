---
title: Verwenden von Business Central-Apps in Power BI| Microsoft Docs
description: Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 292f78f16b77940fa16a6ffc25bd79dbca0684e3
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915860"
---
# <a name="using-the-prodshort-apps-in-power-bi"></a>[!INCLUDE [prodshort](includes/prodshort.md)]-Apps in Power BI verwenden

> **GILT FÜR:** [!INCLUDE [prodlong](includes/prodlong.md)] online 

[!INCLUDE [prodlong](includes/prodlong.md)] veröffentlicht die folgenden Power BI-Apps, die detaillierte Dashboards zum Anzeigen von Daten bereitstellen:

- [!INCLUDE [prodlong](includes/prodlong.md)] – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Sales

## <a name="overview"></a>Matrix

Jede App enthält mehrere Berichte, die Sie nach Daten durchsuchen können, einschließlich der folgenden Funktionen:

- Wählen Sie eine Darstellung im Dashboard, um einen der Berichte anzuzeigen.  
- Filtern Sie den Bericht oder fügen Sie Felder hinzu, die Sie überwachen möchten.  
- Heften Sie eine benutzerdefinierte Ansicht an das Dashboard an, um sie weiter zu verfolgen.  
  Sie können Daten auch manuell aktualisieren, und Sie können einen Aktualisierungsplan einrichten. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/refresh-scheduled-refresh).  

Die Apps sind so konzipiert, dass sie mit Daten aller Unternehmen in [!INCLUDE[prodshort](includes/prodshort.md)] arbeiten. Bei der Installation der Power BI App geben Sie einen oder mehrere Parameter an, um eine Verbindung zu Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] herzustellen.  

> [!NOTE]
> Sie können auch Ihre eigenen Berichte und Dashboards in Power BI auf Grundlage Ihrer Daten in [!INCLUDE[prodshort](includes/prodshort.md)] erstellen. Weitere Informationen finden Sie unter [Verbindung Ihrer Geschäftsdaten mit Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Voraussetzungen

Power BI-Apps erfordern Berechtigungen für die Tabellen, aus denen Daten abgerufen werden, und für die Webdienste, die zum Abrufen von Daten verwendet werden. In der folgenden Tabelle sind die erforderlichen Webdienste für jede einzelne Power BI-App aufgeführt:
    
|App | Webdienste|
|----|-------------|
|[!INCLUDE[prodshort](includes/prodshort.md)] – CRM| <ul><li>Verkaufschancen</li><li>Excel-Vorlage zur Unternehmensansicht-Information</li><li>Power BI-Berichtsbezeichnungen</li></ul>|
|[!INCLUDE[prodshort](includes/prodshort.md)] – Finanzen| <ul><li>PowerBIFinance</li><li>Excel-Vorlage zur Unternehmensansicht-Information</li><li>Power BI-Berichtsbezeichnungen</li></ul>|
|[!INCLUDE[prodshort](includes/prodshort.md)] – Sales| <ul><li>Artikel-Statistik nach Debitor</li><li>Verkaufsdashboard</li><li>Excel-Vorlage zur Unternehmensansicht-Information</li><li>Power BI-Berichtsbezeichnungen</li></ul>|

> [!TIP]
> Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prodshort](includes/prodshort.md)] zu suchen. Auf der Seite **Webdienst** stellen Sie sicher, dass das Feld **Veröffentlichen** für die oben aufgeführten Webdienste ausgewählt ist. Weitere Informationen finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

## <a name="get-ready"></a>Vorbereitung

Registrieren Sie sich für den Power BI-Dienst. Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung Ihre geschäftliche E-Mail-Adresse und Ihr Kennwort.

## <a name="install-a-prodshort-app-in-power-bi"></a>Eine [!INCLUDE[prodshort](includes/prodshort.md)]-App in Power BI installieren

1. Öffnen Sie Ihren Browser, navigieren Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com) und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.  

    ![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Sie können möglicherweise auch von [!INCLUDE [prodshort](includes/prodshort.md)] aus starten. Navigieren Sie auf Ihrer Homepage zu **Berichtsauswahl** im Power BI Abschnitt. Wählen Sie entweder **Service** oder **Mein Unternehmen** im Menüband aus. Die Organisationsgalerie in Power BI oder in Microsoft AppSource wird geöffnet. Sie wird gefiltert, sodass nur Apps angezeigt werden, die sich auf [!INCLUDE[prodshort](includes/prodshort.md)] beziehen.

3. Im Feld **Dienste** wählen Sie **Abrufen** aus.

    Dieser Schritt öffnet die Seite **Power BI-Apps** , auf der Sie nach Power BI-Apps suchen können, die in **AppSource** verfügbar sind.  

4. Geben Sie im Feld **Suchen** den Text **Dynamics 365 Business Central** ein.
5. Wählen Sie die App aus, die Sie verwenden möchten, und wählen Sie **Jetzt abrufen** aus. Wählen Sie dann **Installieren** aus.  

    Anschließend ist die App unter **Apps** im Navigationsmenü von Power BI verfügbar.

## <a name="connect-the-prodshort-app-to-your-data"></a>[!INCLUDE[prodshort](includes/prodshort.md)]-App mit Ihren Daten verbinden

1. Wählen Sie unter **Apps** zuerst die Business Central-App und dann **Verbinden** aus.
2. Wenn Sie dazu aufgefordert werden, geben Sie unter **Unternehmensname** und **Umgebung** Informationen zur [!INCLUDE[prodshort](includes/prodshort.md)]-Instanz ein, zu der Sie eine Verbindung herstellen möchten.

    - Stellen Sie sicher, dass Sie unter **Unternehmensname** den vollständigen Namen und nicht den Anzeigenamen verwenden. Sie finden den Unternehmensnamen auf der Seite **Unternehmen** in [!INCLUDE[prodshort](includes/prodshort.md)]. 
    - Falls Sie nicht mehrere Umgebungen erstellt haben, wählen Sie für **Umgebung** die Option **Produktion** aus.

3. Wählen Sie **Weiter** aus.
4. Wählen Sie **Anmelden** aus.
5. Wenn Sie dazu aufgefordert werden, geben Sie den Benutzernamen und das Kennwort für die Anmeldung bei [!INCLUDE[prodshort](includes/prodshort.md)] ein.
6. Sobald die Verbindung hergestellt ist, werden ein Dashboard und Berichte zu Ihrem Power BI Arbeitsplatz hinzugefügt. Wenn abgeschlossen, werden die Kacheln die Daten aus Ihrem [!INCLUDE[prodshort](includes/prodshort.md)]-Unternehmen anzeigen.

    ![Wählen Sie Dynamics 365 Business Central aus, und wählen Sie dann „Jetzt abrufen“ aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Probleme beheben

Das Power BI-Dashboard basiert auf den veröffentlichten Webdiensten, die oben aufgeführt sind. Es zeigt Daten des Demounternehmens oder Ihres eigenen Unternehmens an, wenn Sie Daten aus Ihrer aktuellen Finanzlösung importieren. Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.  

### <a name="you-dont-have-a-power-bi-account"></a>Kein Power BI-Konto vorhanden

Es wurde kein Power BI-Konto eingerichtet. Für ein gültiges Power BI-Konto benötigen Sie eine Lizenz. Außerdem müssen Sie sich zuvor bei Power BI angemeldet haben, um Ihren Power BI-Arbeitsbereich zu erstellen.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Nachricht: Es sind keine Berichte aktiviert. Wählen Sie „Bericht auswählen“ aus, um eine Liste der anzeigbaren Berichte anzuzeigen.

Diese Meldung wird angezeigt, wenn der Standardbericht nicht in Ihrem Power BI-Arbeitsbereich bereitgestellt werden konnte. Oder der Bericht wurde bereitgestellt, aber nicht erfolgreich aktualisiert. Bei diesem Problem navigieren Sie zum Bericht in Ihrem Power BI-Arbeitsbereich und wählen dort **Datensatz** , **Einstellungen** aus. Anschließend aktualisieren Sie die Anmeldedaten manuell. Wenn der Datensatz erfolgreich aktualisiert wurde, navigieren Sie zurück zu [!INCLUDE[prodshort](includes/prodshort.md)] und wählen Sie den Bericht auf der Seite **Berichte auswählen** manuell aus.

### <a name="you-need-a-power-bi-pro-license-to-install-the-prodshort-app-in-power-bi"></a>Sie brauchen eine Power BI Pro Lizenz zur Installation der [!INCLUDE[prodshort](includes/prodshort.md)] App in Power BI

Sie benötigen eine [Power BI Pro-Lizenz](/power-bi/service-features-license-type), um Ihre Inhalte teilen zu können. Selbiges gilt für die Personen, mit denen Sie Ihre Inhalte teilen möchten. Der Inhalt muss sich in einem Arbeitsbereich in einer [Premium-Kapazität](/power-bi/service-premium-what-is) befinden. Weitere Informationen finden Sie unter [Möglichkeiten zur gemeinsamen Nutzung Ihrer Arbeit in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>Parameterprüfung fehlgeschlagen. Prüfen Sie, ob alle Parameter gültig sind.

Dieser Fehler zeigt an, dass einer oder mehrere der Parameter ungültig sind.

- Der angegebene Umgebungsparameter entspricht keiner vorhandenen Produktions- oder -Sandbox-Umgebung von [!INCLUDE[prodshort](includes/prodshort.md)].
- Der angegebene Unternehmensparameter stimmt mit keinem bestehenden Unternehmen in [!INCLUDE[prodshort](includes/prodshort.md)] überein. Überprüfen Sie den Unternehmensnamen auf der Seite **Unternehmen** unter [!INCLUDE[prodshort](includes/prodshort.md)].
- Falls eine Verbindung mit [!INCLUDE[prodshort](includes/prodshort.md)] on-premises hergestellt wurde, haben Sie eine ungültige URL eingegeben. Sie können die URL auf er Seite **Webdienst** in [!INCLUDE[prodshort](includes/prodshort.md)] überprüfen  
- Es ist kein Port geöffnet, über den die Anforderung Ihre Firewall passieren kann.

### <a name="cant-sign-in"></a>Anmeldung nicht möglich

Wenn angezeigt wird, dass die Anmeldung fehlgeschlagen ist, nachdem Sie sich mit Ihren [!INCLUDE[prodshort](includes/prodshort.md)]-Benutzeranmeldeinformationen angemeldet haben, dann liegt wahrscheinlich eines der folgenden Probleme vor:

- Das Konto, das Sie verwenden, hat keine Berechtigungen, um die [!INCLUDE[prodshort](includes/prodshort.md)]-Daten aus Ihrem Konto zu lesen. Stellen Sie sicher, dass Sie über Berechtigungen für die erforderlichen Daten in [!INCLUDE[prodshort](includes/prodshort.md)] verfügen und versuche es noch mal.
- Sie haben einen anderen Authentifizierungstyp als „Standard“ ausgewählt, falls Sie eine Verbindung mit [!INCLUDE[prodshort](includes/prodshort.md)] on-premises hergestellt haben.
- Der eingegebene Benutzername oder das Kennwort ist falsch.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Nachricht: Ihre Datenquelle kann nicht aktualisiert werden, da die Anmeldeinformationen ungültig sind. Bitte aktualisieren Sie Ihre Anmeldeinformationen und versuchen Sie es erneut.

Für [!INCLUDE[prodshort](includes/prodshort.md)] on-premises kann das Problem darauf zurückzuführen sein, dass die OData-URL nur für das lokale Netzwerk zugänglich ist.

### <a name="incorrect-company-name"></a>Ungültiger Unternehmensname

Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben. Unternehmensnamensuche für **Unternehmen** zu suchen. Verwenden Sie das Feld **Name** , wenn Sie den Unternehmensnamen eingeben.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Der Schlüssel glich keinen Zeilen in der Tabelle

Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle". Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.

### <a name="historical-data-appears-to-be-missing"></a>Historische Daten scheinen zu fehlen

Sobald die Power BI-App installiert ist und Ihre Daten in Power BI angezeigt werden, stellen Sie möglicherweise fest, dass nicht alle Ihre Daten angezeigt werden. Die Datensätze werden so gefiltert, dass nur die Daten der letzten 365 Tage zurückgegeben werden. Diese Standardeinstellung dient dazu, die Berichte zu beschleunigen.  

### <a name="i-only-see-data-for-a-single-company"></a>Ich sehe nur Daten für ein einzelnes Unternehmen

Die Power BI App zeigt nur Daten vom [!INCLUDE[prodshort](includes/prodshort.md)] Unternehmen an, das definiert wurde, als die Power BI App installiert wurde. Daten von zusätzlichen Unternehmen können zu den Berichten hinzugefügt werden, indem neue Abfragen hinzugefügt werden, die andere Unternehmen als Datenquelle verwenden.  

### <a name="what-now"></a>Was jetzt?

- Versuchen Sie im [Erstellen eine Frage im Q&A-Feld](/power-bi/service-q-and-a-tips) im oberen Bereich des Dashboards.
- [Ändern Sie die Kacheln](/power-bi/service-dashboard-edit-tile) im Dashboard.  
- [Wählen Sie eine Kachel aus](/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.  
- Standardmäßig ist für Ihren Datenbestand keine Aktualisierung geplant. Sie können den Aktualisierungszeitplan ändern oder versuchen, ihn bei Bedarf mithilfe von **Jetzt aktualisieren** zu aktualisieren. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/refresh-scheduled-refresh).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Arbeiten mit [!INCLUDE [prodshort](includes/prodshort.md)]-Daten in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI-Berichte erstellenl zur Anzeige von [!INCLUDE [prodlong](includes/prodlong.md)]-Daten](across-how-use-financials-data-source-powerbi.md)  
[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der „neue Look“ des Power BI Service](/power-bi/service-new-look)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI Dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Power Apps-Datenquelle](across-how-use-financials-data-source-powerapps.md)  
[Verwenden von [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
