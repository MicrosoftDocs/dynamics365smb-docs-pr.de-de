---
title: Berichte erstellen in Power BI Desktop zur Anzeige von Business Central-Daten | Microsoft Docs
description: Sie können Ihre Daten zur Verfügung stellen als Datenquelle in Power BI und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ce1ce3039758d5991eb3a770713d2f1e273bbe0c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754517"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Power BI-Berichte erstellen zur Anzeige von [!INCLUDE [prod_long](includes/prod_long.md)]-Daten

Sie können Ihre [!INCLUDE[prod_long](includes/prod_long.md)]-Daten zur Verfügung stellen als Datenquelle in Power BI Desktop und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.

Dieser Artikel beschreibt die ersten Schritte zur Verwendung von Power BI Desktop zur Erstellung von Berichten, die [!INCLUDE[prod_long](includes/prod_long.md)]-Daten anzeigen.  Nach dem Erstellen können Sie die Berichte in Ihrem Power BI-Dienst veröffentlichen oder sie mit allen Benutzern in Ihrer Organisation teilen. Sobald sich diese Berichte im Power BI-Dienst befinden, können Sie von Benutzern, die dafür eingerichtet sind, in [!INCLUDE[prod_long](includes/prod_long.md)] angezeigt werden.

## <a name="get-ready"></a>Vorbereitung

- Registrieren Sie sich für den Power BI-Dienst.

    Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung Ihre geschäftliche E-Mail-Adresse und Ihr Kennwort.

- Laden Sie [Power BI Desktop](https://powerbi.microsoft.com/desktop/) herunter.

   Power BI Desktop ist eine kostenlose Anwendung, die Sie auf Ihrem lokalen Computer installieren. Weitere Informationen finden Sie unter [Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Stellen Sie sicher, dass die Daten, die im Bericht enhalten sein sollen, als Webdienst veröffentlicht werden.
    
    Viele Webdienste werden standardmäßig veröffentlicht. Eine einfache Methode, die Webdienste zu finden ist, in *Webdiensten* in [!INCLUDE[prod_short](includes/prod_short.md)] zu suchen. Stellen Sie sicher, dass auf der Seite **Webdienste** das Feld **Veröffentlichen** ausgewählt ist. Hierbei handelt es sich üblicherweise um eine Aufgabe für einen Administrator.
    
    Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

- Für [!INCLUDE[prod_short](includes/prod_short.md)] on-premises benötigen Sie folgende Informationen:

    - Die OData-URL für [!INCLUDE[prod_short](includes/prod_short.md)]. Diese URL hat üblicherweise das Format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, zum Beispiel `https://localhost:7048/BC160/ODataV4`. Bei einer Bereitstellung mit mehreren Mandanten sollte der Mandant in der URL enthalten sein, zum Beispiel `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Einen Benutzernamen und einen Webdienst-Zugriffsschlüssel für ein [!INCLUDE[prod_short](includes/prod_short.md)]-Konto.

      Für das Abrufen von Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] verwendet Power BI die Standardauthentifizierung. Sie benötigen also einen Benutzernamen und einen Webdienst-Zugriffsschlüssel, um eine Verbindung herzustellen. Hierbei kann es sich um Ihr eigenen Benutzerkonto oder um ein Konto Ihrer Organisation handeln, das speziell für diesen Zweck angelegt wurde.

- Laden Sie das [!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema herunter (optional).

    Weitere Informationen finden Sie unter [[!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthema verwenden](#theme) in diesem Artikel.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop hinzufügen

Die erste Aufgabe beim Erstellen von Berichten ist das Hinzufügen von [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop. Sobald die Verbindung hergestellt ist, können Sie mit der Erstellung des Berichts beginnen.

1. Starten Sie Power BI Desktop.
2. Wählen Sie **Daten abrufen** aus.

    Wenn Sie die Option **Daten abrufen** nicht sehen können, wählen Sie das Menü **Datei** und dann den Menüpunkt **Daten abrufen** aus.
2. Wählen Sie auf der Seite **Daten abrufen** die Option **Onlinedienste** aus.
3. Führen Sie im Bereich **Onlinedienste** einen der folgenden Schritte aus:

    1. Wenn Sie eine Onlineverbindung zu [!INCLUDE [prod_short](includes/prod_short.md)] herstellen, wählen Sie **Dynamics 365 Business Central** und dann **Verbinden** aus.
    2. Wenn Sie eine Verbindung zu [!INCLUDE [prod_short](includes/prod_short.md)] on-premises herstellen, wählen Sie **Dynamics 365 Business Central (on-premises)** und dann **Verbinden** aus.

4. Power BI zeigt einen Assistenten an, der Sie durch den Verbindungsprozess führt, einschließlich der Anmeldung bei [!INCLUDE [prod_short](includes/prod_short.md)].

    Wählen Sie für die Onlineverbindung **Anmelden** und dann das entsprechende Konto aus. Verwenden Sie dasselbe Konto, mit dem Sie sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden.
    
    Geben Sie für eine lokale Verbindung die OData-URL für [!INCLUDE[prod_short](includes/prod_short.md)] und optional den Namen des Unternehmens ein. Wenn Sie dazu aufgefordert werden, geben Sie den Benutzernamen und das Kennwort des Kontos ein, mit dem eine Verbindung zu [!INCLUDE[prod_short](includes/prod_short.md)] hergestellt werden soll. Geben Sie in das Feld **Kennwort** den Webdienst-Zugriffsschlüssel ein.

    > [!NOTE]  
    > Sobald Sie sich erfolgreich mit [!INCLUDE[prod_short](includes/prod_short.md)] verbunden haben, werden Sie nicht mehr aufgefordert, sich anzumelden.
    
5. Wählen Sie **Verbinden** aus, um den Vorgang fortzusetzen.

    Der Power BI-Assistent zeigt eine Liste von Microsoft [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebungen, Unternehmen und Datenquellen an. Diese Datenquellen repräsentieren alle Webdienste, die Sie über [!INCLUDE [prod_short](includes/prod_short.md)] veröffentlicht haben.
6. Geben Sie die Daten an, die Sie Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden** aus.
7. Wiederholen Sie die vorherigen Schritte, um zusätzliche [!INCLUDE [prod_short](includes/prod_short.md)] oder andere Daten Ihrem Power BI Datenmodell hinzuzufügen.

Sobald die Daten geladen sind, können Sie sie in der rechten Navigation auf der Seite sehen. Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und können mit dem Erstellen Ihres Power BI-Berichts beginnen.  

> [!TIP]
> Weitere Informationen zur Verwendung von Power BI Desktop finden Sie unter [Erste Schritte mit Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Berichte erstellen, um mit einer Liste verknüpfte Daten anzuzeigen

Sie können Berichte erstellen, die in einer Infobox einer [!INCLUDE [prod_short](includes/prod_short.md)]-Listenseite angezeigt werden. Die Berichte können Daten zu dem in der Liste ausgewählten Datensatz enthalten. Das Erstellen dieser Berichte ist mit dem Erstellen anderer Berichte vergleichbar. Sie müssen jedoch einige Dinge beachten, um sicherzustellen, dass die Berichte wie erwartet angezeigt werden. Weitere Informationen finden Sie unter [Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Verwenden des [!INCLUDE [prod_short](includes/prod_short.md)]-Berichtsthemas (optional)

Bevor Sie Ihren Bericht erstellen, empfiehlt es sich, die [!INCLUDE [prod_short](includes/prod_short.md)]-Designdatei herunterzuladene und zu importieren. Die Designdatei erstellt eine Farbpalette, damit Sie Berichte im Farbstil der [!INCLUDE [prod_short](includes/prod_short.md)]-Anwendungen erstellen können, ohne benutzerdefinierte Farben für jede Grafik definieren zu müssen.

> [!NOTE]
> Diese Aufgabe ist optional. Sie können Ihre Berichte jederzeit erstellen und die Stilvorlage später herunterladen und darauf anwenden.

### <a name="download-the-theme"></a>Herunterladen des Themas

Die Themendatei ist als json-Datei in der Themengalerie der Microsoft Power BI-Community verfügbar. Gehen Sie folgendermaßen vor, um die Themendatei herunterzuladen:

1. Wechseln Sie zu [Themengalerie der Microsoft Power BI-Community für Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
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

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Aktivieren Sie Ihre Geschäftsdaten für Power BI](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzen](finance.md)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]