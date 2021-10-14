---
title: Arbeiten mit Power BI-Berichten in Business Central | Microsoft Docs
description: Rufen Sie Erkenntnisse, Business Intelligence und KPIs aus Ihren Business Central-Daten mithilfe von Power BI ab.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: dbe5b2b5fd623d37f144a07b6570f6ee0714f9b9
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588326"
---
# <a name="working-with-power-bi-reports-in-prod_short"></a>Arbeiten mit Power BI-Berichten in [!INCLUDE [prod_short](includes/prod_short.md)]

In diesem Artikel erlernen Sie einige der Grundlagen zum Anzeigen von Power BI-Berichten in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="overview"></a>Matrix

Power BI-Berichte geben Ihnen Einblick in Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten. Verschiedene Seiten in [!INCLUDE [prod_short](includes/prod_short.md)] umfassen einen Power BI-Berichtsteil, in dem Power BI-Berichte angezeigt werden können. Das Rollencenter ist eine typische Seite, auf der Sie einen Power BI-Berichtsteil anzeigen können. Einige Listenseiten, wie z. B. **Artikel**, umfassen außerdem einen Power BI-Teil.

[!INCLUDE [prod_short](includes/prod_short.md)] arbeitet mit dem Power BI-Dienst zusammen. Berichte zur Anzeige in [!INCLUDE [prod_short](includes/prod_short.md)] werden in einem Power BI-Dienst gespeichert. In [!INCLUDE [prod_short](includes/prod_short.md)] können Sie im Power BI-Teil jeden Power BI-Bericht anzeigen, der in Ihrem Power BI-Dienst verfügbar ist. Wenn Sie sich zum ersten Mal bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden und bis zum Herstellen einer Verbindung zu einem Power BI-Dienst sind die Teile leer, wie hier zu sehen ist:

![Power BI-Teil in Business Central.](./media/power-bi-part.png)

## <a name="get-started"></a>Erste Schritte

### <a name="prerequisites"></a>Voraussetzungen

Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] on-premises verwenden, muss es für die Power BI-Integration aktiviert sein. Diese Aufgabe wird normalerweise von einem Administrator ausgeführt. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] on-premises für die Power BI-Integration einrichten](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] online ist bereits für die Integration von Power BI eingerichtet.

### <a name="sign-up-power-bi"></a>Power BI registrieren

Bevor Sie Power BI mit [!INCLUDE[prod_short](includes/prod_short.md)] verwenden können, müssen Sie sich für den Power BI-Service anmelden. Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung Ihre geschäftliche E-Mail-Adresse und Ihr Kennwort.

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Mit Power BI verbinden – nur ein Mal

Wenn Sie sich zum ersten Mal bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden, sehen Sie wahrscheinlich auf einigen Seiten eventuell einen leeren Power BI-Teil. In diesem Fall müssen Sie sich zuerst mit Ihrem Power BI-Konto verbinden. Sobald die Verbindung hergestellt ist, werden Berichte angezeigt. Sie müssen diesen Schritt nur einmal ausführen.

1. Wählen Sie den Link **Erste Schritte mit Power BI** im Teil **Power BI-Berichte** aus.
2. Das unterstützte Setup **Power BI-Berichte in Business Central einrichten** wird gestartet. Wählen Sie **Weiter** aus, um fortzufahren.
3. Auf der Seite **Ihre Power BI-Lizenz überprüfen**. Führen Sie einen der folgenden Schritte aus:

    - Wenn Sie sich noch nicht bei Power BI angemeldet haben, wählen Sie [Zur Power BI-Homepage wechseln](https://powerbi.microsoft.com) aus. Eröffnen Sie ein Konto, kehren Sie dann zu [!INCLUDE[prod_short](includes/prod_short.md)] zurück und beenden Sie die Einrichtung.

    - Wenn Sie bereits eine Lizenz haben, wählen Sie **Weiter** aus.
4. Auf der nächsten Seite [!INCLUDE[prod_short](includes/prod_short.md)] lädt jetzt einen Demo-Bericht auf Power BI hoch. Dies dauert einige Minuten, daher erfolgt dies im Hintergrund. Um das Setup abzuschließen, wählen Sie **Weiter** und dann **Fertig** aus.

Der Verbindungsvorgang beginnt. Während des Vorgangs kommuniziert [!INCLUDE [prod_short](includes/prod_short.md)] mit dem Power BI-Dienst, um festzustellen, ob Sie über ein gültiges Konto und eine gültige Lizenz für Power BI verfügen. Sobald Ihre Lizenz überprüft wurde, wird der Power BI-Standardbericht auf der Seite angezeigt. Wenn dort kein Bericht angezeigt wird, können Sie einen Bericht aus dem Teil auswählen.

> [!TIP]
> Mit [!INCLUDE [prod_short](includes/prod_short.md)] online werden in diesem Schritt automatisch die Power BI-Standardberichte, die in [!INCLUDE [prod_short](includes/prod_short.md)] verwendet werden, in Ihren Power BI-Arbeitsbereich hochgeladen.

#### <a name="from-prod_short-on-premises"></a>Aus [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Das Verbinden mit Power BI erfolgt auf ähnliche Weise wie bei [!INCLUDE [prod_short](includes/prod_short.md)] online. Auf der Seite **AZURE ACTIVE DIRECTORY-DIENSTBERECHTIGUNGEN** werden Sie jedoch möglicherweise aufgefordert, Zugriff auf die Power BI-Dienste zu gewähren. Um den Zugriff zu gewähren, wählen Sie **Azure Services autorisieren** und dann **Akzeptieren** aus.

Sobald die Verbindung hergestellt ist, können Sie auf den Seiten einen Bericht aus dem Power BI-Teil auswählen.

## <a name="working-with-power-bi-reports"></a>Mit Power BI-Berichten arbeiten

### <a name="show-reports-on-list-pages"></a>Berichte auf Listenseiten anzeigen

[!INCLUDE[prod_long](includes/prod_long.md)] umfasst eine Power BI-Infobox auf mehreren Schlüssellistenseiten. Diese Infobox bietet zusätzliche Einblicke in die Daten in der Liste. Während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert. Wenn Sie diesen Teil nicht sehen, wählen Sie in der Aktionsleiste **Aktionen** > **Anzeigen** > **Power BI-Berichte anzeigen/ausblenden** aus.

Informationen zum Erstellen von Berichten für Listenseiten finden Sie unter [Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

### <a name="switch-reports"></a>Berichte wechseln

Ein Power BI-Teil auf einer Seite kann jeden Power BI-Bericht anzeigen, der für Sie verfügbar ist. Um einen anderen Bericht anzuzeigen, wählen Sie oben aus der Dropdown-Befehlsliste die Aktion **Bericht auswählen** aus.  

Die Seite **Power BI-Berichtsauswahl** zeigt eine Liste aller Power BI-Berichte an, auf die Sie Zugriff haben. Diese Liste wird aus einem Ihrer eigenen Arbeitsbereiche oder aus Arbeitsbereichen abgerufen, die mit dem Dienst Power BI für Sie freigegeben wurden. Aktivieren Sie für jeden Bericht, den Sie auf der Startseite anzeigen möchten, das Kontrollkästchen **Aktivieren**. Wählen Sie dann **OK** aus. Sie kehren zur Seite zurück und der zuletzt aktivierte Bericht wird angezeigt. Verwenden Sie die Befehle **Zurück** und **Nächster** aus der Dropdown-Befehlsliste, um zwischen Berichten zu navigieren.  

### <a name="get-more-reports"></a>Weitere Berichte erhalten

Wenn auf der Seite **Power BI-Berichtsauswahl** kein bzw. nicht der gewünschte Bericht angezeigt wird, wählen Sie **Berichte abrufen** aus. Mit dieser Aktion können Sie von den folgenden zwei Orten aus nach Berichten suchen: *Meine Organisation* oder *Dienste*.

- Wählen Sie **Meine Organisation** aus, um zu den Power BI-Diensten zu wechseln. Von hier aus können Sie die Berichte in Ihrer Organisation anzeigen, für die Sie zur Anzeige berechtigt sind. Diese Berichte können Sie dann Ihrem Arbeitsbereich hinzufügen.
- Wählen **Dienstleistungen**, um zum Microsoft AppSource zu gehen, wo Sie Power BI Apps installieren können.  

> [!TIP]
> Falls Sie mit Power BI Desktop arbeiten, können Sie außerdem neue Power BI-Berichte erstellen. Sobald diese Berichte in Ihrem Power BI-Arbeitsbereich veröffentlicht wurden, werden sie auf der Seite **Power BI-Berichtsauswahl** angezeigt.  

### <a name="manage-and-modify-reports"></a>Berichte verwalten und ändern

Im Power BI-Teil können Sie Änderungen an einem Bericht vornehmen. Die von Ihnen vorgenommenen Änderungen werden dann im Power BI-Dienst veröffentlicht. Wenn der Bericht mit anderen Benutzern geteilt wird, können diese die Änderungen ebenfalls sehen, sofern Sie die Änderungen nicht in einem neuen Bericht speichern.

Um einen Bericht zu ändern, wählen Sie die Aktion **Bericht verwalten** aus der Dropdown-Befehlsliste im Power BI-Teil aus. Nehmen Sie dann die gewünschten Änderungen vor. Wenn Sie fertig sind, wählen Sie **Datei** > **Speichern** aus. Wenn es sich um einen geteilten Bericht handelt und Sie die Änderung nicht für alle Benutzer vornehmen möchten, wählen Sie **Speichern unter** aus, damit diese Änderung nicht für alle Benutzer sichtbar ist.

Wenn Sie zum Rollencenter zurückkehren, wird der aktualisierte Bericht angezeigt. Wenn Sie **Speichern unter** verwendet haben, müssen Sie **Bericht auswählen** auswählen und den neuen Bericht anschließend aktivieren, um ihn anzuzeigen.

> [!NOTE]
> Diese Funktion steht mit [!INCLUDE [prod_short](includes/prod_short.md)] on-premises nicht zur Verfügung.

### <a name="upload-reports"></a><a name="upload"></a>Berichte hochladen

Power BI-Berichte können als .pbix-Dateien unter den Benutzern verteilt werden. Wenn .pbix-Dateien vorhanden sind, können Sie diese hochladen und mit allen Benutzern von [!INCLUDE [prod_short](includes/prod_short.md)] teilen. Die Berichte werden in jedem Unternehmen in [!INCLUDE [prod_short](includes/prod_short.md)] geteilt.  

Um einen vorhandenen Bericht hochzuladen, wählen Sie die Aktion **Bericht hochladen** aus der Dropdown-Befehlsliste im Teil **Power BI-Berichte** aus. Suchen Sie dann nach der .pbix-Datei, die den Bericht definiert, den Sie teilen möchten. Sie können den Standardnamen der Datei ändern.  

Nachdem der Bericht in Ihren Power BI-Arbeitsbereich hochgeladen wurde, wird er automatisch in die Power BI-Arbeitsbereiche anderer Benutzer hochgeladen.

> [!NOTE]
> Zum Hochladen eines Berichts benötigen Sie SUPERUSER-Berechtigungen in [!INCLUDE[prod_short](includes/prod_short.md)]. Außerdem ist das Hochladen von Berichten mit [!INCLUDE [prod_short](includes/prod_short.md)] on-premises nicht möglich. Mit der lokalen Version laden Sie Berichte direkt in Ihren Power BI-Arbeitsbereich hoch. Weitere Informationen finden Sie unter [Arbeiten mit [!INCLUDE [prod_short](includes/prod_short.md)]-Daten in Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Probleme beheben

Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.  

### <a name="you-dont-have-a-power-bi-account"></a>Kein Power BI-Konto vorhanden

Es wurde kein Power BI-Konto eingerichtet. Für ein gültiges Power BI-Konto benötigen Sie eine Lizenz und müssen sich zuvor bei Power BI angemeldet haben, um einen Power BI-Arbeitsbereich zu erstellen.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Nachricht: Es sind keine Berichte aktiviert. Wählen Sie „Bericht auswählen“ aus, um eine Liste der anzeigbaren Berichte anzuzeigen.

Diese Meldung wird angezeigt, wenn der Standardbericht nicht in Ihrem Power BI-Arbeitsbereich bereitgestellt werden konnte. Oder er wurde bereitgestellt, aber nicht erfolgreich aktualisiert. Navigieren Sie zum Bericht in Ihrem Power BI-Arbeitsbereich, wählen Sie **Datensatz**, **Einstellungen** aus und aktualisieren Sie die Anmeldedaten manuell. Wenn der Datensatz erfolgreich aktualisiert wurde, navigieren Sie zurück zu [!INCLUDE[prod_short](includes/prod_short.md)] und wählen Sie den Bericht auf der Seite **Berichte auswählen** manuell aus.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>Auf der Seite „Bericht auswählen“ auf einer Listenseite wird kein Bericht angezeigt

Vermutlich enthält der Name des Berichts nicht den Namen der Listenseite. Löschen Sie den Filter, um die vollständige Liste der verfügbaren Power BI-Berichte anzuzeigen.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Power BI-Berichte erstellenl zur Anzeige von [!INCLUDE [prod_long](includes/prod_long.md)]-Daten](across-how-use-financials-data-source-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbeiten mit [!INCLUDE [prod_short](includes/prod_short.md)]-Daten in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI für Verbraucher](/power-bi/consumer/end-user-consumer)  
[Der „neue Look“ des Power BI Service](/power-bi/service-new-look)  
[Schnellstart: Stellen Sie eine Verbindung zu Daten her in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI Dokumentation](/power-bi/)  
[Business Intelligence](bi.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power BI-Datenquelle](across-how-use-financials-data-source-powerbi.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] als Power Apps-Datenquelle](across-how-use-financials-data-source-powerapps.md)  
[Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]