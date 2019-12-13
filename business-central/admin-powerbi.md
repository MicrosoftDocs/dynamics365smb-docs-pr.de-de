---
title: Aktivieren Sie Ihre Geschäftsdaten für Power BI| Microsoft Docs
description: Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 0750f1724260eb7767757d947f30dcb074ef1aeb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879106"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivieren Sie Ihre Geschäftsdaten für Power BI

Einblicke in Ihre [!INCLUDE[prodshort](includes/prodshort.md)] Daten erhalten ist mit der [!INCLUDE[prodshort](includes/prodshort.md)] Anwendung für Power BI einfach. Power BI ruft Ihre Daten ab und erstellt dann ein vorkonfiguriertes Dashboard und Berichte auf Grundlage dieser Daten.  

Sie müssen ein gültiges Konto bei [!INCLUDE[prodshort](includes/prodshort.md)] und Power BI haben. Zudem müssen Sie [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunterladen, wenn Sie Ihre eigenen Power BI-Berichte erstellen möchten. Power BI Apps benötigen Berechtigungen für die Tabellen, aus denen Daten abgerufen werden. Weitere Einzelheiten auf den Anforderungen werden im Folgenden beschrieben.  

> [!IMPORTANT]
> Die Power BI Apps, die in diesem Artikel beschrieben werden, sind dafür ausgelegt, Azure Active Directory als Autorisierungsmechanismus zu verwenden, sofern nicht anderweitig definiert. Um eine Power BI App zu installieren, müssen Sie auch eine Power BI Pro Lizenz haben.  Sobald die Power BI App installiert ist, kann es mit Benutzern mit jedem Lizenztyp geteilt werden.

[!INCLUDE [prodlong](includes/prodlong.md)] hat folgende Apps für Power BI veröffentlicht:

- [!INCLUDE [prodlong](includes/prodlong.md)] – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](lokal) – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](lokal) – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](lokal) – Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>[!INCLUDE [prodshort](includes/prodshort.md)] Dashboards nutzen in Power BI

Jede App enthält Berichte, die Sie aufrufen können in:

- Wählen Sie eine Darstellung im Dashboard, um einen der Berichte anzuzeigen.  
- Filtern Sie den Bericht oder fügen Sie Felder hinzu, die Sie überwachen möchten.  
- Heften Sie diese benutzerdefinierte Ansicht an das Dashboard an, um sie weiter zu Verfolgen.  
  Sie können Daten auch manuell aktualisieren, und Sie können einen Aktualisierungsplan einrichten. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/refresh-scheduled-refresh).  

Die Apps sind so konzipiert, dass sie mit Daten aller Unternehmen arbeiten, die Sie in Ihrem [!INCLUDE[prodshort](includes/prodshort.md)] haben. Bei der Installation der Power BI App geben Sie einen oder mehrere Parameter an, um eine Verbindung zu Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] herzustellen.  

> [!NOTE]
> Sie können auch Ihre eigenen Berichte und Dashboards in Power BI auf Grundlage Ihrer Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen. Weitere Informationen finden Sie unter [Verbindung Ihrer Geschäftsdaten mit Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Um Ihre Daten in Power BI zu verbinden

1. Öffnen Sie Ihren Browser und navigieren Sie zu https://powerbi.microsoft.com, und melden Sie sich in Ihrem Konto an.
2. Wählen Sie **Daten abrufen** am unteren Rand des linken Navigationsbereich aus.  

    ![Navigieren, um die Daten zu erhalten](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Sie können möglicherweise auch von [!INCLUDE [prodshort](includes/prodshort.md)] aus starten. Navigieren Sie auf Ihrer Homepage zu **Berichtsauswahl** im Power BI Abschnitt. Wählen Sie entweder **Service** oder **Mein Unternehmen** im Menüband aus. Wenn eine dieser Aktionen ausgewählt wird, gelangen Sie zur Organisationsgalerie in Power BI oder zu der Dienstbibliothek in Microsoft AppSource, die zudem so gefiltert wird dass nur Apps zu [!INCLUDE[prodshort](includes/prodshort.md)] anzeigt.

3. Im Feld **Dienste** wählen Sie **Abrufen** aus. Dadurch wird eine Seite mit der **AppSource** und **Apps für Power BI** geöffnet.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Wählen Sie **Apps** auf der Registerkarte **Apps für Power BI**, wählen Sie das Inhaltspaket **Microsoft Dynamics 365 Business Central** App aus, das Sie verwenden möchten, und wählen Sie dann **Jetzt abrufen** aus.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Geben Sie bei entsprechender Aufforderung den Namen des Unternehmens und der Umgebung in Ihr [!INCLUDE[prodshort](includes/prodshort.md)] ein, mit dem Sie eine Verbindung herstellen möchten. Wenn Sie nicht mehrere Umgebungen erstellt haben, geben Sie eine **Produktion** ein. Stellen Sie für den Firmenparameter sicher, dass Sie den Namen und nicht den Anzeigenamen eingeben. Der Name des Unternehmens kann auf der Seite **Unternehmen** innerhalb Ihrer [!INCLUDE[prodshort](includes/prodshort.md)]-Instanz gefunden werden.  

    > [!NOTE]
    > Wenn Sie eine Verbindung mit [!INCLUDE [prodshort](includes/prodshort.md)] lokal herstellen, müssen Sie den *Web Service URL* Parameter angeben. Finden Sie dies in der Seite **Webdienst** in [!INCLUDE [prodshort](includes/prodshort.md)]. Ihre [!INCLUDE [server](includes/server.md)] Instanz muss für die Standardauthentifizierung konfiguriert sein, und Sie müssen einen Benutzer und den Webzugriffsschlüssel dieses Benutzers als Kennwort angeben. Ersetzen Sie im folgenden Beispiel *Myserver:7048* mit Ihrem [!INCLUDE [server](includes/server.md)] Namen und *CRONUS%20US* mit Ihrem Firmennamen.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Sobald die Verbindung hergestellt ist, werden ein Dashboard und Berichte zu Ihrem Power BI Arbeitsplatz hinzugefügt. Wenn abgeschlossen, werden die Kacheln die Daten aus Ihrem [!INCLUDE[prodshort](includes/prodshort.md)]-Unternehmen anzeigen.

    ![Wählen Sie Dynamics 365 Business Central aus, und wählen Sie dann „Jetzt abrufen“ aus](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Was jetzt?

- Versuchen Sie im [Erstellen eine Frage im Q&A-Feld](/power-bi/service-q-and-a-tips) im oberen Bereich des Dashboards.
- [Ändern Sie die Kacheln](/power-bi/service-dashboard-edit-tile) im Dashboard.  
- [Wählen Sie eine Kachel aus](/power-bi/service-dashboard-tiles), um den zu Grunde liegenden Bericht zu öffnen.  
- Standardmäßig ist für Ihr Dataset keine Aktualisierung geplant. Sie können den Aktualisierungszeitplan ändern oder versuchen, ihn bei Bedarf zu aktualisieren mithilfe von **Jetzt aktualisieren**. Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI in [!INCLUDE [prodshort](includes/prodshort.md)]

Ihre Homepage in [!INCLUDE [prodshort](includes/prodshort.md)] kann ein Power BI Steuerelement einschließen, das für die Anzeige konfiguriert werden, um Power BI Berichte auf Ihrer Homepage anzuzeigen.

> [!IMPORTANT]
> Sie müssen ein gültiges Konto bei [!INCLUDE [prodshort](includes/prodshort.md)] und Power BI haben. Wenn Sie Berichte ändern möchten, müssen Sie Power BI Desktop herunterladen. Weitere Informationen finden Sie unter [Business Central als Power BI Datenquelle nutzen](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Beim ersten Login

Wenn Sie sich zum ersten Mal anmelden bei [!INCLUDE [prodshort](includes/prodshort.md)], werden einen leeren Power BI Teil auf Ihrer Homepage bemerken. Um die Berichte anzuzeigen, müssen Sie zuerst eine Verbindung herstellen zu Power BI durch Auswahl der Verknüpfung *Beginnen Sie mit Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)] kommuniziert dann mit dem Power BI Service, um festzustellen, ob Sie ein gültiges Power BI Konto haben. Sobald Ihre Lizenz überprüft wurde, wird der Power BI Standardbericht auf Ihrer Startseite angezeigt.

### <a name="selecting-power-bi-reports"></a>Wählen Sie Power BI Berichte

Die Power BI Steuerung auf Ihrer Homepage kann jeden Power BI Bericht anzeigen. Um einen vorhandenen Bericht anzuzeigen, wählen Sie die Aktion **Bericht wählen** von der Power BI Dropdown-Befehlsliste.  

Die Berichtsauswahlseite zeigt eine Liste aller Power BI Berichte, auf die Sie Zugriff haben. Diese Liste wird von Ihrem Power BI Arbeitsplatz abgerufen. Aktivieren Sie jeden Bericht, den Sie auf der Startseite anzeigen möchten, und wählen Sie dann OK. Sie kehren zu Ihrer Startseite zurück und der zuletzt aktivierte Bericht wird angezeigt. Verwenden Sie in der Dropdown-Befehlsliste den vorherigen und den nächsten Befehl, um zwischen Berichten zu navigieren.  

### <a name="get-reports"></a>Berichte abrufen

Wenn auf der Seite Berichte auswählen keine Berichte angezeigt werden oder der gewünschte Bericht nicht angezeigt wird. Sie können Berichte abrufen von *Meine Organisation* oder von *Dienstleistungen*.
Wählen *Meine Organisation*, um zum Power BI Dienst zu gehen, in dem Sie die Berichte in Ihrer Organisation anzeigen können, zu deren Anzeige Sie berechtigt waren, und die Sie Ihrem Arbeitsbereich hinzufügen können. Wählen *Dienstleistungen*, um zum Microsoft AppSource zu gehen, wo Sie Power BI Apps installieren können.  

Sie können auch neue Power BI Berichte erstellen. Sobald diese Berichte auf Ihrem Power BI Arbeitsbereich veröffentlicht wurden, werden sie auf dieser Seite angezeigt.  

### <a name="managing-reports"></a>Berichte verwalten

In dem Power BI Abschnitt auf Ihrer Homepage können Sie die Aktion **Bericht verwalten** aus der Dropdown-Befehlsliste auswählen, damit Sie den Bericht ändern können, der sich auf das Rollencenter konzentriert hat.  

Änderungen können am Bericht vorgenommen und gespeichert werden.  Alle am Bericht vorgenommenen Änderungen werden für jeden Benutzer geändert, für den dieser Bericht freigegeben ist, da Sie den Bericht ändern, der im Power BI Service gespeichert ist.  

Wenn Sie Ihre Änderungen abgeschlossen haben, wählen Sie Speichern. Wenn es sich um einen freigegebenen Bericht handelt, möchten Sie möglicherweise Speichern unter auswählen, um zu vermeiden, dass diese Änderung für alle Benutzer vorgenommen wird.
Kehren Sie zum Rollencenter zurück, und der aktualisierte Bericht wird angezeigt. Wenn Sie den Befehl Speichern unter ausgeführt haben, müssen Sie die Seite Bericht auswählen öffnen und den neuen Bericht aktivieren.

### <a name="uploading-reports"></a>Berichte werden hochgeladen

Sie können neue Power BI Berichte hochladen und sie mit allen Benutzern Ihrer [!INCLUDE [prodshort](includes/prodshort.md)] teilen. Die Berichte werden in jedem Unternehmen in [!INCLUDE [prodshort](includes/prodshort.md)] geteilt.  

Um einen vorhandenen Bericht hochzuladen, wählen Sie die Aktion **Bericht hochladen** aus der Dropdown-Befehlsliste aus. Anschließend können Sie eine .pbix-Datei hochladen, in der die Berichte definiert sind, die Sie freigeben möchten. Sie können den Standardnamen der Datei ändern.  

Sobald der Bericht hochgeladen wurde in den Power BI Arbeitsbereich, wird er automatisch in den Power BI Arbeitsbereiche aller anderen Benutzer in diesem Unternehmen bei der nächsten Anmeldung bei [!INCLUDE [prodshort](includes/prodshort.md)] hochgeladen.

## <a name="system-requirements"></a>Systemanforderungen

Um die [!INCLUDE[prodshort](includes/prodshort.md)] Daten in Power BI zu importieren, müssen Sie Berechtigungen für die Webdienste haben, um Daten abzurufen. Die Web Services, die für jede Power BI App erforderlich sind enthalten:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Verkaufschancen
- Excel-Vorlage zur Unternehmensansicht-Information
- Power BI-Berichtsbezeichnungen

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Excel-Vorlage zur Unternehmensansicht-Information
- Power BI-Berichtsbezeichnungen

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Artikel-Statistik nach Debitor
- Verkaufsdashboard
- Excel-Vorlage zur Unternehmensansicht
- Power BI-Berichtsbezeichnungen

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] lokal verwenden dieselben Web-Service-Endpunkte wie [!INCLUDE [prodshort](includes/prodshort.md)] online.

## <a name="web-services"></a>Webdienste

Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prodshort](includes/prodshort.md)] zu suchen. Auf der Seite **Webdienst** stellen Sie sicher, dass das Feld **Veröffentlichen** für die oben aufgeführten Webdienste ausgewählt ist.

## <a name="troubleshooting"></a>Problembehebung

Das Power BI-Dashboard beruht auf den veröffentlichten Webdiensten, die oben aufgeführt werden. Es enthält Daten vom Demounternehmen oder von Ihrem eigenen Unternehmen, wenn Sie Daten aus Ihrer aktuellen Finanzlösung importieren. Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.  

### <a name="you-do-not-have-a-power-bi-account"></a>Sie haben kein Power BI Konto

Ein Power BI Konto wurde nicht eingerichtet. Um ein gültiges Power BI Konto zu haben, benötigen eine Lizenz und müssen sich zuvor angemeldet haben Power BI, damit Ihr Power BI Arbeitsbereich erstellt werden kann.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Nachricht: Es sind keine Berichte aktiviert. Wählen Sie „Bericht auswählen“ aus, um eine Liste der anzeigbaren Berichte anzuzeigen.

Diese Meldung wird angezeigt, wenn der Standardbericht nicht auf Ihrem Power BI Arbeitsbereich bereitgestellt werden kann oder der Bericht wurde bereitgestellt, aber nicht erfolgreich aktualisiert. Navigieren Sie in diesem Fall zu dem Bericht in Ihrem Power BI Arbeitsbereich, wählen Sie **Datensatz**, **Einstellungen** und aktualisieren Sie die Berechtigungsnachweise manuell. Wenn der Datensatz erfolgreich aktualisiert wurde, navigieren Sie zurück zu Business Central und wählen Sie den Bericht manuell aus der Liste aus der **Wählen Sie Berichte** Seite. 

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Sie brauchen eine Power BI Pro Lizenz zur Installation der [!INCLUDE [prodshort](includes/prodshort.md)] App in Power BI

Power BI Apps können nur von Benutzern mit einer Power BI Pro Lizenz installiert werden. Sobald die Power BI App installiert ist, können Sie sie mit Benutzern teilen, die keine Power BI Pro Lizenz haben.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>Parameterprüfung fehlgeschlagen. Prüfen Sie, ob alle Parameter gültig sind.

Dieser Fehler zeigt an, dass einer oder mehrere der Parameter ungültig sind.

- Der angegebene Umgebungsparameter entspricht keinem vorhandenen [!INCLUDE [prodshort](includes/prodshort.md)] Produktions- oder Sandbox-Umgebung. 
- Der angegebene Firmenparameter stimmt mit keiner bestehenden [!INCLUDE [prodshort](includes/prodshort.md)] Unternehmung überein. Überprüfen Sie den Unternehmensnamen auf der Seite **Unternehmen** unter [!INCLUDE [prodshort](includes/prodshort.md)].
- Wenn eine Verbindung zu [!INCLUDE [prodshort](includes/prodshort.md)] lokal hergestellt wird. Sie haben eine ungültige URL eingegeben. Sie können die URL auf er Seite **Webdienst** in [!INCLUDE [prodshort](includes/prodshort.md)] überprüfen  
- Ein Port ist nicht geöffnet, damit die Anforderung Ihre Firewall passieren kann.

### <a name="login-failed"></a>Anmeldung fehlgeschlagen

Wenn Sie einen Anmeldung fehlgeschlagen-Fehler erhalten, wenn Sie sich mit Ihren [!INCLUDE [prodshort](includes/prodshort.md)] Anmeldedaten am Dashboard angemeldet haben, kann dies durch eines der folgenden Probleme verursacht werden:

- Das Konto, das Sie verwenden, hat keine Berechtigungen, um die [!INCLUDE [prodshort](includes/prodshort.md)] Daten aus Ihrem Konto zu lesen. Stellen Sie sicher, dass Sie über Berechtigungen für die erforderlichen Daten in [!INCLUDE [prodshort](includes/prodshort.md)] verfügen und versuche es noch mal.
- Sie haben einen anderen Authentifizierungstyp als Standard ausgewählt, wenn Sie eine Verbindung herstellen mit [!INCLUDE [prodshort](includes/prodshort.md)]lokal.
- Sie haben keinen gültigen Benutzernamen oder Passwort eingegeben.

### <a name="incorrect-company-name"></a>Ungültiger Unternehmensname

Ein häufiger Fehler ist, den Unternehmensanzeigenamen anstelle des Unternehmensnamens einzugeben. Unternehmensnamensuche für **Unternehmen** zu suchen. Verwenden Sie das Feld **Name**, wenn Sie den Unternehmensnamen eingeben.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Der Schlüssel glich keinen Zeilen in der Tabelle

Wenn Sie einen nicht gültigen Unternehmensnamen während des Verbindungsvorgangs eingeben, erhalten Sie möglicherweise die Fehlermeldung, "der Schlüssel entsprach keinen Zeilen in der Tabelle". Geben Sie den korrekten Unternehmensnamen an und versuchen Sie die Verbindung erneut.

### <a name="historical-data-appears-to-be-missing"></a>Historische Daten scheinen zu fehlen

Sobald die Power BI App installiert ist und Ihre Daten angezeigt werden in Power BI, werden Sie möglicherweise feststellen, dass nicht alle Ihre Daten angezeigt werden. Die Datensätze werden so gefiltert, dass nur die Daten der letzten 365 Tage zurückgegeben werden. Diese Standardeinstellung dient dazu, die Berichte zu beschleunigen.  

### <a name="i-only-see-data-for-a-single-company"></a>Ich sehe nur Daten für ein einzelnes Unternehmen

Die Power BI App zeigt nur Daten vom [!INCLUDE [prodshort](includes/prodshort.md)] Unternehmen an, das definiert wurde, als die Power BI App installiert wurde. Daten von zusätzlichen Unternehmen können zu den Berichten hinzugefügt werden, indem neue Abfragen hinzugefügt werden, die andere Unternehmen als Datenquelle verwenden.  

## <a name="see-also"></a>Siehe auch

[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der "neue Look" des Power BI Service](/power-bi/service-new-look)  
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
