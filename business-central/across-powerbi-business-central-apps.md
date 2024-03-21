---
title: Business Central-Apps in Power BI verwenden
description: 'Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="use-the--apps-in-power-bi"></a>[!INCLUDE [prod_short](includes/prod_short.md)]-Apps in Power BI verwenden

> **GILT FÜR:** [!INCLUDE [prod_long](includes/prod_long.md)] online 

[!INCLUDE [prod_long](includes/prod_long.md)] veröffentlicht die folgenden Power BI-Apps, die detaillierte Dashboards zum Anzeigen von Daten bereitstellen:

- [!INCLUDE [prod_long](includes/prod_long.md)] – CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Sales

## <a name="overview"></a>Matrix

Jede App enthält mehrere Berichte, die Sie nach Daten durchsuchen können, einschließlich der folgenden Funktionen:

- Wählen Sie eine Darstellung im Dashboard, um einen der Berichte anzuzeigen.  
- Filtern Sie den Bericht oder fügen Sie Felder hinzu, die Sie überwachen möchten.  
- Heften Sie eine benutzerdefinierte Ansicht an das Dashboard an, um sie weiter zu verfolgen.  
  Sie können Daten auch manuell aktualisieren, und Sie können einen Aktualisierungsplan einrichten. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/refresh-scheduled-refresh).  

Die Apps sind so konzipiert, dass sie mit Daten aller Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] arbeiten. Bei der Installation der Power BI App geben Sie einen oder mehrere Parameter an, um eine Verbindung zu Ihrem [!INCLUDE [prod_short](includes/prod_short.md)] herzustellen.  

> [!NOTE]
> Sie können auch Ihre eigenen Berichte und Dashboards in Power BI auf Grundlage Ihrer Daten in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen. Weitere Informationen finden Sie unter [Verbindung Ihrer Geschäftsdaten mit Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Voraussetzungen

Power BI-Apps erfordern Berechtigungen für die Tabellen, aus denen Daten abgerufen werden, und für die Webdienste, die zum Abrufen von Daten verwendet werden. In der folgenden Tabelle sind die erforderlichen Webdienste für jede einzelne Power BI-App aufgeführt:
    
|App|Webdienste |
|--|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Verkaufschancen</li><li>Excel-Vorlage zur Unternehmensansicht-Information</li><li>Power BI-Berichtsbezeichnungen</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Finanzen| <ul><li>PowerBIFinance</li><li>Excel-Vorlage zur Unternehmensansicht-Information</li><li>Power BI-Berichtsbezeichnungen</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Sales| <ul><li>Artikel-Statistik nach Debitor</li><li>Verkaufsdashboard</li><li>Excel-Vorlage zur Unternehmensansicht-Information</li><li>Power BI-Berichtsbezeichnungen</li></ul>|

> [!TIP] 
> Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prod_short](includes/prod_short.md)] zu suchen. Auf der Seite **Webdienst** stellen Sie sicher, dass das Feld **Veröffentlichen** für die oben aufgeführten Webdienste ausgewählt ist. Weitere Informationen finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

## <a name="get-ready"></a>Vorbereitung

Registrieren Sie sich für den Power BI-Dienst. Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung Ihre geschäftliche E-Mail-Adresse und Ihr Kennwort.

## <a name="install-a--app-in-power-bi"></a>Eine [!INCLUDE[prod_short](includes/prod_short.md)]-App in Power BI installieren

1. Öffnen Sie Ihren Browser, navigieren Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com) und melden Sie sich bei Ihrem Konto an.
2. Wählen Sie im Navigationsbereich **Apps**.
    
    Die **Apps** Seite wird angezeigt.

3. Wählen Sie auf der Seite **Apps** in der oberen rechten Ecke der Seite die Option **Apps abrufen** aus.
    
    Die Seite **Power BI Apps** wird geöffnet, auf der Sie nach den Apps suchen können, die für [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sind.

    ![Navigieren Sie zu „Apps abrufen“.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

> [!TIP] 
> Sie können auch auf den **Power BI-Bericht** aus [!INCLUDE [prod_short](includes/prod_short.md)] zugreifen. Navigieren Sie zum Abschnitt Power BI-Berichte und **Wählen Sie Berichte** auf Ihrer Startseite. Wählen Sie entweder **Services** oder **Meine Organisation** aus **Berichte abrufen**. Die Organisationsgalerie in Power BI oder in Microsoft AppSource wird geöffnet, sodass nur Apps angezeigt werden, die sich auf [!INCLUDE[prod_short](includes/prod_short.md)] beziehen.

5. Geben Sie im Feld **Suchen** den Text **Dynamics 365 Business Central** ein.
6. Wählen Sie die App aus, die Sie verwenden möchten, und wählen Sie **Jetzt abrufen** aus. Wählen Sie dann **Installieren** aus.  

    Anschließend ist die App unter **Apps** im Navigationsmenü von Power BI verfügbar.

## <a name="connect-the--app-to-your-data"></a>[!INCLUDE[prod_short](includes/prod_short.md)]-App mit Ihren Daten verbinden

1. Wählen Sie unter **Apps** zuerst die Business Central-App und dann **Verbinden** aus.
2. Wenn Sie dazu aufgefordert werden, geben Sie unter **Unternehmensname** und **Umgebung** Informationen zur [!INCLUDE[prod_short](includes/prod_short.md)]-Instanz ein, zu der Sie eine Verbindung herstellen möchten.

    - Stellen Sie sicher, dass Sie unter **Unternehmensname** den vollständigen Namen und nicht den Anzeigenamen verwenden. Sie finden den Unternehmensnamen auf der Seite **Unternehmen** in [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Falls Sie nicht mehrere Umgebungen erstellt haben, wählen Sie für **Umgebung** die Option **Produktion** aus.

3. Wählen Sie **Weiter** aus.
4. Wählen Sie **Anmelden** aus.
5. Wenn Sie dazu aufgefordert werden, geben Sie den Benutzernamen und das Kennwort für die Anmeldung bei [!INCLUDE[prod_short](includes/prod_short.md)] ein.
6. Sobald die Verbindung hergestellt ist, werden ein Dashboard und Berichte zu Ihrem Power BI Arbeitsplatz hinzugefügt. Wenn abgeschlossen, werden die Kacheln die Daten aus Ihrem [!INCLUDE[prod_short](includes/prod_short.md)]-Unternehmen anzeigen.

    ![Wählen Sie Dynamics 365 Business Central und wählen Sie Jetzt abrufen.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Probleme beheben

Das Power BI-Dashboard basiert auf den veröffentlichten Webdiensten, die oben aufgeführt sind. Es zeigt Daten des Demounternehmens oder Ihres eigenen Unternehmens an, wenn Sie Daten aus Ihrer aktuellen Finanzlösung importieren. Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.  

### <a name="you-dont-have-a-power-bi-account"></a>Kein Power BI-Konto vorhanden

Es wurde kein Power BI-Konto eingerichtet. Für ein gültiges Power BI-Konto benötigen Sie eine Lizenz. Außerdem müssen Sie sich zuvor bei Power BI angemeldet haben, um Ihren Power BI-Arbeitsbereich zu erstellen.  

### <a name="message-there-are-no-enabled-reports-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Nachricht: Es sind keine Berichte aktiviert. Wählen Sie den Bericht aus, um eine Liste der anzeigbaren Berichte anzuzeigen.

Diese Meldung wird angezeigt, wenn der Standardbericht nicht in Ihrem Power BI-Arbeitsbereich bereitgestellt werden konnte. Oder der Bericht wurde bereitgestellt, aber nicht erfolgreich aktualisiert. Bei diesem Problem navigieren Sie zum Bericht in Ihrem Power BI-Arbeitsbereich und wählen dort **Datensatz**, **Einstellungen** aus. Anschließend aktualisieren Sie die Anmeldedaten manuell. Wenn der Datensatz erfolgreich aktualisiert wurde, navigieren Sie zurück zu [!INCLUDE[prod_short](includes/prod_short.md)] und wählen Sie den Bericht auf der Seite **Berichte auswählen** manuell aus.

### <a name="you-need-a-power-bi-pro-license-to-install-the--app-in-power-bi"></a>Sie brauchen eine Power BI Pro Lizenz zur Installation der [!INCLUDE[prod_short](includes/prod_short.md)] App in Power BI

Sie benötigen eine [Power BI Pro-Lizenz](/power-bi/service-features-license-type), um Ihre Inhalte teilen zu können. Selbiges gilt für die Personen, mit denen Sie Ihre Inhalte teilen möchten. Der Inhalt muss sich in einem Arbeitsbereich in einer [Premium-Kapazität](/power-bi/service-premium-what-is) befinden. Weitere Informationen finden Sie unter [Möglichkeiten zur gemeinsamen Nutzung Ihrer Arbeit in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>Parameterprüfung fehlgeschlagen. Prüfen Sie, ob alle Parameter gültig sind.

Dieser Fehler zeigt an, dass einer oder mehrere der Parameter ungültig sind.

- Der angegebene Umgebungsparameter entspricht keiner vorhandenen Produktions- oder -Sandbox-Umgebung von [!INCLUDE[prod_short](includes/prod_short.md)].
- Der angegebene Unternehmensparameter stimmt mit keinem bestehenden Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] überein. Überprüfen Sie den Unternehmensnamen auf der Seite **Unternehmen** unter [!INCLUDE[prod_short](includes/prod_short.md)].
- Falls eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] on-premises hergestellt wurde, haben Sie eine ungültige URL eingegeben. Sie können die URL auf er Seite **Webdienst** in [!INCLUDE[prod_short](includes/prod_short.md)] überprüfen  
- Es ist kein Port geöffnet, über den die Anforderung Ihre Firewall passieren kann.

### <a name="cant-sign-in"></a>Anmeldung nicht möglich

Wenn angezeigt wird, dass die Anmeldung fehlgeschlagen ist, nachdem Sie sich mit Ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzeranmeldeinformationen angemeldet haben, dann liegt wahrscheinlich eines der folgenden Probleme vor:

- Das Konto, das Sie verwenden, hat keine Berechtigungen, um die [!INCLUDE[prod_short](includes/prod_short.md)]-Daten aus Ihrem Konto zu lesen. Stellen Sie sicher, dass Sie über Berechtigungen für die erforderlichen Daten in [!INCLUDE[prod_short](includes/prod_short.md)] verfügen und versuche es noch mal.
- Sie haben einen anderen Authentifizierungstyp als „Standard“ ausgewählt, falls Sie eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] on-premises hergestellt haben.
- Der eingegebene Benutzername oder das Kennwort ist falsch.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Nachricht: Ihre Datenquelle kann nicht aktualisiert werden, da die Anmeldeinformationen ungültig sind. Bitte aktualisieren Sie Ihre Anmeldeinformationen und versuchen Sie es erneut.

Für [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kann das Problem darauf zurückzuführen sein, dass die OData-URL nur für das lokale Netzwerk zugänglich ist.

### <a name="incorrect-company-name"></a>Ungültiger Unternehmensname

Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben. Unternehmensnamensuche für **Unternehmen** zu suchen. Verwenden Sie das Feld **Name**, wenn Sie den Unternehmensnamen eingeben.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Der Schlüssel glich keinen Zeilen in der Tabelle

Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle". Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.

### <a name="historical-data-appears-to-be-missing"></a>Historische Daten scheinen zu fehlen

Sobald die Power BI-App installiert ist und Ihre Daten in Power BI angezeigt werden, stellen Sie möglicherweise fest, dass nicht alle Ihre Daten angezeigt werden. Die Datensätze werden so gefiltert, dass nur die Daten der letzten 365 Tage zurückgegeben werden. Diese Standardeinstellung dient dazu, die Berichte zu beschleunigen.  

### <a name="i-only-see-data-for-a-single-company"></a>Ich sehe nur Daten für ein einzelnes Unternehmen

Die Power BI App zeigt nur Daten vom [!INCLUDE[prod_short](includes/prod_short.md)] Unternehmen an, das definiert wurde, als die Power BI App installiert wurde. Daten von zusätzlichen Unternehmen können zu den Berichten hinzugefügt werden, indem neue Abfragen hinzugefügt werden, die andere Unternehmen als Datenquelle verwenden.  

### <a name="what-now"></a>Was jetzt?

- Versuchen Sie im [Erstellen eine Frage im Q&A-Feld](/power-bi/service-q-and-a-tips) im oberen Bereich des Dashboards.
- [Ändern Sie die Kacheln](/power-bi/service-dashboard-edit-tile) im Dashboard.  
- [Wählen Sie eine Kachel aus](/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.  
- Standardmäßig ist für Ihren Datenbestand keine Aktualisierung geplant. Sie können den Aktualisierungszeitplan ändern oder versuchen, ihn bei Bedarf mithilfe von **Jetzt aktualisieren** zu aktualisieren. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/refresh-scheduled-refresh).

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Mit [!INCLUDE [prod_short](includes/prod_short.md)]-Daten in Power BI arbeiten](across-working-with-business-central-in-powerbi.md)  
[Power BI-Berichte erstellenl zur Anzeige von [!INCLUDE [prod_long](includes/prod_long.md)]-Daten](across-how-use-financials-data-source-powerbi.md)  
[Business Intelligence](bi.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] einrichten](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle verwenden](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] als Power Apps-Datenquelle verwenden](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate verwenden](across-how-use-financials-data-source-flow.md)  
[Power BI Dokumentation](/power-bi/)  
[Was ist Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Einführung in Datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Einführung in Datenflows und Self-Service-Datenvorbereitung](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
