---
title: Berichte erstellen in Power BI Desktop zur Anzeige von Business Central-Daten | Microsoft Docs
description: Sie können Ihre Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: db872c8049550a497e2ee56a4a62bb69fa6a1854
ms.sourcegitcommit: 1508643075dafc25e9c52810a584b8df1d14b1dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2022
ms.locfileid: "8049848"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Power BI-Berichte erstellen zur Anzeige von [!INCLUDE [prod_long](includes/prod_long.md)]-Daten

Sie können Ihre [!INCLUDE[prod_long](includes/prod_long.md)]-Daten zur Verfügung stellen als Datenquelle in Power BI Desktop und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.

Dieser Artikel beschreibt die ersten Schritte zur Verwendung von Power BI Desktop zur Erstellung von Berichten, die [!INCLUDE[prod_long](includes/prod_long.md)]-Daten anzeigen.  Nach dem Erstellen können Sie die Berichte in Ihrem Power BI-Dienst veröffentlichen oder sie mit allen Benutzern in Ihrer Organisation teilen. Sobald sich diese Berichte im Power BI-Dienst befinden, können Sie von Benutzern, die dafür eingerichtet sind, in [!INCLUDE[prod_long](includes/prod_long.md)] angezeigt werden.

## <a name="get-ready"></a>Vorbereitung

- Registrieren Sie sich für den Power BI-Dienst.

  Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung Ihre geschäftliche E-Mail-Adresse und Ihr Kennwort.

- Laden Sie [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunter.

  Power BI Desktop ist eine kostenlose Anwendung, die Sie auf Ihrem lokalen Computer installieren. Weitere Informationen finden Sie unter [Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Stellen Sie sicher, dass die Daten, die Sie im Bericht haben wollen, als API-Seite verfügbar sind oder als Webdienst veröffentlicht wurden.

  Weitere Informationen finden Sie unter [Daten über API-Seiten oder OData-Webdienste veröffentlichen](admin-powerbi-setup.md#exposedata).

- Für [!INCLUDE[prod_short](includes/prod_short.md)] on-premises benötigen Sie folgende Informationen:

  - Die OData-URL für [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Diese URL hat üblicherweise das Format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, zum Beispiel `https://localhost:7048/BC160/ODataV4`. Bei einer Bereitstellung mit mehreren Mandanten sollte der Mandant in der URL enthalten sein, zum Beispiel `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
  - Einen Benutzernamen und einen Webdienst-Zugriffsschlüssel für ein [!INCLUDE[prod_short](includes/prod_short.md)]-Konto.

    Für das Abrufen von Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] verwendet Power BI die Standardauthentifizierung. Sie benötigen also einen Benutzernamen und einen Webdienst-Zugriffsschlüssel, um eine Verbindung herzustellen. Hierbei kann es sich um Ihr eigenen Benutzerkonto oder um ein Konto Ihrer Organisation handeln, das speziell für diesen Zweck angelegt wurde.

- Laden Sie das [!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema herunter (optional).

  Weitere Informationen finden Sie unter [[!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema verwenden](#theme) in diesem Artikel.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop hinzufügen

Die erste Aufgabe beim Erstellen von Berichten ist das Hinzufügen von [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop. Sobald die Verbindung hergestellt ist, können Sie mit der Erstellung des Berichts beginnen.

1. Starten Sie Power BI Desktop.
2. Wählen Sie **Daten abrufen** aus.

    Wenn Sie die Option **Daten abrufen** nicht sehen können, wählen Sie das Menü **Datei** und dann den Menüpunkt **Daten abrufen** aus.
3. Wählen Sie auf der Seite **Daten abrufen** die Option **Onlinedienste** aus.
4. Führen Sie im Bereich **Onlinedienste** einen der folgenden Schritte aus:

    - Um sich mit [!INCLUDE [prod_short](includes/prod_short.md)] online zu verbinden, wählen Sie **Dynamics 365 Business Central**, dann **Verbinden**.
    - Um sich mit [!INCLUDE [prod_short](includes/prod_short.md)] vor Ort zu verbinden, wählen Sie **Dynamics 365 Business Central (vor Ort)**, dann **Verbinden**.

5. Melden Sie sich bei [!INCLUDE [prod_short](includes/prod_short.md)] an (nur einmalig).

    Wenn Sie sich noch nicht bei [!INCLUDE [prod_short](includes/prod_short.md)] von Power BI Desktop aus angemeldet haben, werden Sie aufgefordert, sich anzumelden.

    - Für [!INCLUDE [prod_short](includes/prod_short.md)] online wählen Sie **Anmelden** und wählen dann das entsprechende Konto. Verwenden Sie dasselbe Konto, mit dem Sie sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden. Wenn Sie fertig sind, wählen Sie **Verbinden**.

    - Für [!INCLUDE [prod_short](includes/prod_short.md)] lokal geben Sie zuerst die OData-URL für [!INCLUDE[prod_short](includes/prod_short.md)] ein und wählen dann **OK**. Wenn Sie dazu aufgefordert werden, geben Sie den Benutzernamen und das Kennwort des Kontos ein, das für die Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden soll. Geben Sie in das Feld **Kennwort** den Webdienst-Zugriffsschlüssel ein. Wenn Sie fertig sind, wählen Sie **Verbinden**.

    > [!NOTE]  
    > Sobald Sie sich erfolgreich mit [!INCLUDE[prod_short](includes/prod_short.md)] verbunden haben, werden Sie nicht mehr aufgefordert, sich anzumelden. [Wie ändere oder lösche ich das Konto, das ich derzeit für die Verbindung mit Business Central von Power BI Desktop verwende?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Sobald die Verbindung hergestellt ist, stellt Power BI Kontakte zum Business Central-Dienst her. Das Fenster **Navigator** erscheint und zeigt die verfügbaren Datenquellen für die Erstellung von Berichten an. Wählen Sie einen Ordner, um ihn zu erweitern und die verfügbaren Datenquellen zu sehen. 

   Diese Datenquellen stellen alle Webdienste und API-Seiten dar, die für [!INCLUDE [prod_short](includes/prod_short.md)] veröffentlicht sind. Die Datenquellen sind nach den Business Central Umgebungen und Firmen gruppiert. Wenn Business Central online ist, hat **Navigator** die folgende Struktur:

    - **Umgebungsname**
      - **Firmenname**
        - **Erweiterte APIs**

          Dieser Ordner listet erweiterte API-Seiten auf, die von Microsoft veröffentlicht wurden, wie die [Business Central Automatisierungs-APIs](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) und [angepasste API-Seiten für Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Custom-API-Seiten sind weiter in Ordnern nach [APIPublisher](/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/business-central/dev-itpro/developer/properties/devenv-apigroup-property) Eigenschaften des API-Seiten-Quellcodes gruppiert.

        - **Standard-APIs v2.0**

          Dieser Ordner listet die API-Seiten auf, die von der [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) bereitgestellt werden.

        - **Webdienste \(veraltet)**

          Dieser Ordner listet Seiten, Codeunits und Abfragen auf, die als Webdienste in Business Central veröffentlicht werden.

    > [!NOTE]
    > Die Struktur für Business Central lokal ist anders, weil es keine API-Seiten unterstützt.

7. Wählen Sie die Datenquelle(n) aus, die Sie zu Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden**.
8. Wenn Sie später weitere Business Central-Daten hinzufügen möchten, können Sie die vorherigen Schritte wiederholen.

Sobald die Daten geladen sind, können Sie sie in der rechten Navigation auf der Seite sehen. Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und können mit dem Erstellen Ihres Power BI-Berichts beginnen.  

> [!TIP]
> Weitere Informationen zur Verwendung von Power BI Desktop finden Sie unter [Erste Schritte mit Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Erstellen von zugänglichen Berichten

Es ist wichtig, dass Ihre Berichte für so viele Personen wie möglich nutzbar sind. Versuchen Sie, die Berichte so zu gestalten, dass sie keine besonderen Anpassungen an die Bedürfnisse verschiedener Benutzer erfordern. Stellen Sie sicher, dass das Design es den Anwendern ermöglicht, Standard-Hilfstechnologien, wie z.B. Bildschirmleser, zu nutzen. Power BI enthält verschiedene Funktionen, Tools und Richtlinien zur Barrierefreiheit, die Ihnen helfen, dieses Ziel zu erreichen. Weitere Informationen finden Sie unter [Gestalten Sie Power BI-Berichte für Barrierefreiheit](/power-bi/create-reports/desktop-accessibility-creating-reports) in der Power BI-Dokumentation.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Berichte erstellen, um mit einer Liste verknüpfte Daten anzuzeigen

Sie können Berichte erstellen, die in einer Infobox einer [!INCLUDE [prod_short](includes/prod_short.md)]-Listenseite angezeigt werden. Die Berichte können Daten zu dem in der Liste ausgewählten Datensatz enthalten. Das Erstellen dieser Berichte ist mit dem Erstellen anderer Berichte vergleichbar. Sie müssen jedoch einige Dinge beachten, um sicherzustellen, dass die Berichte wie erwartet angezeigt werden. Weitere Informationen finden Sie unter [Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Verwenden des [!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthemas (optional)

Bevor Sie Ihren Bericht erstellen, empfiehlt es sich, die [!INCLUDE [prod_short](includes/prod_short.md)]-Designdatei herunterzuladene und zu importieren. Die Designdatei erstellt eine Farbpalette, damit Sie Berichte im Farbstil der [!INCLUDE [prod_short](includes/prod_short.md)]-Anwendungen erstellen können, ohne benutzerdefinierte Farben für jede Grafik definieren zu müssen.

> [!NOTE]
> Diese Aufgabe ist optional. Sie können Ihre Berichte jederzeit erstellen und die Stilvorlage später herunterladen und darauf anwenden.

### <a name="download-the-theme"></a>Herunterladen des Themas

Die Themendatei ist als json-Datei in der Themengalerie der Microsoft Power BI-Community verfügbar. Gehen Sie folgendermaßen vor, um die Themendatei herunterzuladen:

1. Wechseln Sie zu [Themengalerie der Microsoft Power BI Community für Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Wählen Sie den Anhang **Microsoft Dynamics Business Central.json** zum herunterladen aus.

### <a name="import-the-theme-on-a-report"></a>Importieren des Themas in einen Bericht

Nachdem Sie das [!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema heruntergeladen haben, können Sie es in Ihre Berichte importieren. Um das Thema zu importieren, wählen Sie **Ansicht** > **Themen** > **Nach Themen suchen** aus. Weitere Informationen finden Sie unter [Power BI Desktop – Importieren benutzerdefinierter Berichtsthemen](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Veröffentlichen von Berichten

Nachdem Sie einen Bericht erstellt oder geändert haben, können Sie den Bericht in Ihrem Power BI-Dienst veröffentlichen und sogar mit anderen Benutzern in Ihrer Organisation teilen. Nach der Veröffentlichung wird der Bericht in Power BI angezeigt. Der Bericht kann außerdem in [!INCLUDE[prod_short](includes/prod_short.md)] ausgewählt werden.

Um einen Bericht zu veröffentlichen, wählen Sie **Veröffentlichen** auf der Registerkarte **Start** im Menüband oder im Menü **Datei** aus. Wenn Sie beim Power BI-Dienst angemeldet sind, wird der Bericht für diesen Dienst veröffentlicht. Andernfalls werden Sie aufgefordert, sich anzumelden. 

## <a name="distribute-or-share-a-report"></a>Verteilen oder Teilen eines Berichts

Es gibt verschiedene Möglichkeiten, um Berichte an Ihre Mitarbeiter und andere Personen zu senden:

- Verteilen Sie Berichte als .pbix-Dateien.

    Berichte werden auf Ihrem Computer als .pbix-Dateien gespeichert. Sie können die .pbix-Berichtsdatei wie jede andere Datei an Benutzer verteilen. Anschließend können Benutzer die Datei in ihren Power BI-Dienst hochladen. Siehe hierzu [Hochladen von Berichten aus Dateien](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Das Verteilen von Berichten auf diese Weise bedeutet, dass die Daten für Berichte von jedem Benutzer einzeln aktualisiert werden. Dieser Umstand könnte sich auf die Leistung von [!INCLUDE[prod_short](includes/prod_short.md)] auswirken.

- Teilen eines Berichts über Ihren Power BI-Dienst

    Wenn Sie über eine Lizenz für Power BI Pro verfügen, können Sie den Bericht direkt über Ihren Power BI-Dienst mit anderen Benutzern teilen. Weitere Informationen finden Sie unter [Power BI – Teilen von Dashboards oder Berichten](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="fixing-problems"></a>Probleme beheben

### <a name="cannot-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>„Ein Datensatz kann nicht eingefügt werden. Die aktuelle Verbindungsabsicht ist schreibgeschützt“. Fehler beim Verbinden mit der angepassten API-Seite

> **GILT FÜR:** Business Central Online

Ab Februar 2022 werden neue Berichte, die Business Central-Daten verwenden, standardmäßig mit einer schreibgeschützten Replik der Business Central-Datenbank verbunden. In seltenen Fällen, abhängig vom Design der Seite, erhalten Sie eine Fehlermeldung, wenn Sie versuchen, eine Verbindung zur Seite herzustellen und Daten von der Seite abzurufen.

1. Starten Sie Power BI Desktop.
2. Wählen Sie im Menüband **Daten abrufen** > **Onlinedienste**.
3. Im Fenster **Online-Dienste** wählen Sie **Dynamics 365 Business Central** und dann **Verbinden**.
4. Wählen Sie im Fenster **Navigator** den API-Endpunkt, von dem Sie Daten laden möchten.
5. Im Vorschaubereich auf der rechten Seite sehen Sie den folgenden Fehler:

   *Dynamics365BusinessCentral: Anfrage fehlgeschlagen: Der Remote-Server hat einen Fehler zurückgegeben: (400) Fehlerhafte Anfrage. (Ein Datensatz kann nicht eingefügt werden. Die aktuelle Verbindungsabsicht ist schreibgeschützt. CorrelationId: [...])“.*

6. Wählen Sie **Daten transformieren** anstelle von **Laden**, wie Sie es normalerweise tun würden.
7. Wählen Sie im **Power Query-Editor** aus dem Menüband **Erweiterter Editor**.
8. In der Zeile, die mit **Quelle =** beginnt, ersetzen Sie den folgenden Text:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   mit:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Wählen Sie **Erledigt**.
10. Wählen Sie **Schließen & Anwenden** aus dem Menüband, um die Änderungen zu speichern und den Power Query-Editor zu schließen.

## <a name="see-related-training-at-microsoft-learn"></a>Siehe Verwandte Schulungen unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzen](finance.md)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]