---
title: Arbeiten mit Power BI-Berichten in Business Central | Microsoft Docs
description: Insight, Business Intelligence und KPIs aus Ihren Business Central Daten einfach beziehen mit der Business Central Anwendung für Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 07/10/2020
ms.author: jswymer
ms.openlocfilehash: 7f28e763cd2a72bda79c088c3a1268e3443f86dc
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697763"
---
# <a name="working-with-power-bi-reports-in-prodshort"></a>Arbeiten mit Power BI-Berichten in [!INCLUDE [prodshort](includes/prodshort.md)]

In diesem Artikel erlernen Sie einige der Grundlagen zum Anzeigen von Power BI-Berichten in [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="overview"></a>Matrix

Power BI-Berichte geben Ihnen Einblick in Ihre [!INCLUDE[prodshort](includes/prodshort.md)]-Daten. Verschiedene Seiten in [!INCLUDE [prodshort](includes/prodshort.md)] umfassen einen Power BI-Berichtsteil, in dem Power BI-Berichte angezeigt werden können. Das Rollencenter ist eine typische Seite, auf der Sie einen Power BI-Berichtsteil anzeigen können. Einige Listenseiten, wie z. B. **Artikel**, umfassen außerdem einen Power BI-Teil.

[!INCLUDE [prodshort](includes/prodshort.md)] arbeitet mit dem Power BI-Dienst zusammen. Berichte zur Anzeige in [!INCLUDE [prodshort](includes/prodshort.md)] werden in einem Power BI-Dienst gespeichert. In [!INCLUDE [prodshort](includes/prodshort.md)] können Sie im Power BI-Teil jeden Power BI-Bericht anzeigen, der in Ihrem Power BI-Dienst verfügbar ist. Wenn Sie sich zum ersten Mal bei [!INCLUDE [prodshort](includes/prodshort.md)] anmelden und bis zum Herstellen einer Verbindung zu einem Power BI-Dienst sind die Teile leer, wie hier zu sehen ist:

![Power BI-Teil in Business Central](./media/power-bi-part.png)

## <a name="prerequisites"></a>Voraussetzungen

Wenn Sie [!INCLUDE[prodshort](includes/prodshort.md)] on-premises verwenden, muss es für die Power BI-Integration aktiviert sein. Diese Aufgabe wird normalerweise von einem Administrator ausgeführt. Weitere Informationen finden Sie unter [[!INCLUDE[prodshort](includes/prodshort.md)] on-premises für die Power BI-Integration einrichten](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prodshort](includes/prodshort.md)] online ist bereits für die Integration von Power BI eingerichtet.

## <a name="get-ready"></a>Vorbereitung

Registrieren Sie sich für den Power BI-Dienst. Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung Ihre geschäftliche E-Mail-Adresse und Ihr Kennwort.

## <a name="connect-to-power-bi---one-time-only"></a>Mit Power BI verbinden – nur ein Mal

Wenn Sie sich zum ersten Mal bei [!INCLUDE [prodshort](includes/prodshort.md)] anmelden, sehen Sie auf einigen Seiten eventuell einen leeren Power BI-Teil, wie in der vorherigen Abbildung gezeigt. In diesem Fall müssen Sie sich zuerst mit Ihrem Power BI-Konto verbinden. Sobald die Verbindung hergestellt ist, werden Berichte angezeigt. Sie müssen diesen Schritt nur einmal ausführen.

Um eine Verbindung zu Power BI herzustellen, wählen Sie die Verknüpfung **Erste Schritte mit Power BI** im Teil **Power BI-Berichte** aus.

Während des Verbindungsvorgangs kommuniziert [!INCLUDE [prodshort](includes/prodshort.md)] mit dem Power BI-Dienst, um festzustellen, ob Sie über ein gültiges Konto und eine gültige Lizenz für Power BI verfügen. Sobald Ihre Lizenz überprüft wurde, wird der Power BI-Standardbericht auf der Seite angezeigt. Wenn dort kein Bericht angezeigt wird, können Sie einen Bericht aus dem Teil auswählen.

> [!TIP]
> Mit [!INCLUDE [prodshort](includes/prodshort.md)] online werden in diesem Schritt automatisch die Power BI-Standardberichte, die in [!INCLUDE [prodshort](includes/prodshort.md)] verwendet werden, in Ihren Power BI-Arbeitsbereich hochgeladen.

##### <a name="from-prodshort-on-premises"></a>Aus [!INCLUDE [prodshort](includes/prodshort.md)] on-premises

Das Verbinden mit Power BI erfolgt auf ähnliche Weise wie bei [!INCLUDE [prodshort](includes/prodshort.md)] online. Auf der Seite **AZURE ACTIVE DIRECTORY-DIENSTBERECHTIGUNGEN** werden Sie jedoch aufgefordert, Zugriff auf die Power BI-Dienste zu gewähren. Um den Zugriff zu gewähren, wählen Sie **Azure Services autorisieren** und dann **Akzeptieren** aus.

Sobald die Verbindung hergestellt ist, können Sie auf den Seiten einen Bericht aus dem Power BI-Teil auswählen.

## <a name="show-power-bi-reports-on-list-pages"></a>Power BI-Berichte auf Listenseiten anzeigen

[!INCLUDE[prodlong](includes/prodlong.md)] umfasst eine Power BI-Infobox auf mehreren Schlüssellistenseiten. Diese Infobox bietet zusätzliche Einblicke in die Daten in der Liste. Während Sie sich zwischen den Zeilen in der Liste bewegen, wird der Bericht für den Eintrag gefiltert und aktualisiert. Wenn Sie diesen Teil nicht sehen, wählen Sie in der Aktionsleiste **Aktionen** > **Anzeigen** > **Power BI-Berichte anzeigen/ausblenden** aus. Weitere Informationen finden Sie unter [Erstellen von Power BI-Berichten zum Anzeigen von Listendaten in [!INCLUDE[prodshort](includes/prodshort.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="select-power-bi-reports"></a>Power BI-Berichte auswählen

Ein Power BI-Teil auf einer Seite kann jeden Power BI-Bericht anzeigen, der für Sie verfügbar ist. Um einen anderen Bericht anzuzeigen, wählen Sie oben aus der Dropdown-Befehlsliste die Aktion **Bericht auswählen** aus.  

Die Seite **Power BI-Berichtsauswahl** zeigt eine Liste aller Power BI-Berichte an, auf die Sie Zugriff haben. Diese Liste wird von Ihrem Power BI Arbeitsplatz abgerufen. Aktivieren Sie für jeden Bericht, den Sie auf der Startseite anzeigen möchten, das Kontrollkästchen **Aktivieren**. Wählen Sie dann **OK** aus. Sie kehren zur Seite zurück und der zuletzt aktivierte Bericht wird angezeigt. Verwenden Sie die Befehle **Zurück** und **Nächster** aus der Dropdown-Befehlsliste, um zwischen Berichten zu navigieren.  

## <a name="get-reports"></a>Berichte abrufen

Wenn auf der Seite **Power BI-Berichtsauswahl** kein bzw. nicht der gewünschte Bericht angezeigt wird, wählen Sie **Berichte abrufen** aus. Mit dieser Aktion können Sie von den folgenden zwei Orten aus nach Berichten suchen: *Meine Organisation*oder *Dienste*.

- Wählen Sie **Meine Organisation** aus, um zu den Power BI-Diensten zu wechseln. Von hier aus können Sie die Berichte in Ihrer Organisation anzeigen, für die Sie zur Anzeige berechtigt sind. Diese Berichte können Sie dann Ihrem Arbeitsbereich hinzufügen.
- Wählen **Dienstleistungen**, um zum Microsoft AppSource zu gehen, wo Sie Power BI Apps installieren können.  

> [!TIP]
> Falls Sie mit Power BI Desktop arbeiten, können Sie außerdem neue Power BI-Berichte erstellen. Sobald diese Berichte in Ihrem Power BI-Arbeitsbereich veröffentlicht wurden, werden sie auf der Seite **Power BI-Berichtsauswahl** angezeigt.  

## <a name="manage-and-modify-reports"></a>Berichte verwalten und ändern

Im Power BI-Teil können Sie Änderungen an einem Bericht vornehmen. Die von Ihnen vorgenommenen Änderungen werden dann im Power BI-Dienst veröffentlicht. Wenn der Bericht mit anderen Benutzern geteilt wird, können diese die Änderungen ebenfalls sehen, sofern Sie die Änderungen nicht in einem neuen Bericht speichern.

Um einen Bericht zu ändern, wählen Sie die Aktion **Bericht verwalten** aus der Dropdown-Befehlsliste im Power BI-Teil aus. Nehmen Sie dann die gewünschten Änderungen vor. Wenn Sie fertig sind, wählen Sie **Datei** > **Speichern** aus. Wenn es sich um einen geteilten Bericht handelt und Sie die Änderung nicht für alle Benutzer vornehmen möchten, wählen Sie **Speichern unter** aus, damit diese Änderung nicht für alle Benutzer sichtbar ist.

Wenn Sie zum Rollencenter zurückkehren, wird der aktualisierte Bericht angezeigt. Wenn Sie **Speichern unter** verwendet haben, müssen Sie **Bericht auswählen** auswählen und den neuen Bericht anschließend aktivieren, um ihn anzuzeigen.

> [!NOTE]
> Diese Funktion steht mit [!INCLUDE [prodshort](includes/prodshort.md)] on-premises nicht zur Verfügung.

## <a name="upload-reports"></a><a name="upload"></a>Berichte hochladen

Power BI-Berichte können als .pbix-Dateien unter den Benutzern verteilt werden. Wenn .pbix-Dateien vorhanden sind, können Sie diese hochladen und mit allen Benutzern von [!INCLUDE [prodshort](includes/prodshort.md)] teilen. Die Berichte werden in jedem Unternehmen in [!INCLUDE [prodshort](includes/prodshort.md)] geteilt.  

Um einen vorhandenen Bericht hochzuladen, wählen Sie die Aktion **Bericht hochladen** aus der Dropdown-Befehlsliste im Teil **Power BI-Berichte** aus. Suchen Sie dann nach der .pbix-Datei, die den Bericht definiert, den Sie teilen möchten. Sie können den Standardnamen der Datei ändern.  

Nachdem der Bericht in Ihren Power BI-Arbeitsbereich hochgeladen wurde, wird er automatisch in die Power BI-Arbeitsbereiche anderer Benutzer hochgeladen.

> [!NOTE]
> Zum Hochladen eines Berichts benötigen Sie SUPERUSER-Berechtigungen in [!INCLUDE[prodshort](includes/prodshort.md)]. Außerdem ist das Hochladen von Berichten mit [!INCLUDE [prodshort](includes/prodshort.md)] on-premises nicht möglich. Mit der lokalen Version laden Sie Berichte direkt in Ihren Power BI-Arbeitsbereich hoch. Weitere Informationen finden Sie unter [Arbeiten mit [!INCLUDE [prodshort](includes/prodshort.md)]-Daten in Power BI](across-working-with-business-central-in-powerbi.md).

## <a name="fixing-problems"></a>Probleme beheben

Wenn etwas schief geht, stellt dieser Abschnitt eine Problemumgehung für die häufigsten Probleme bereit.  

### <a name="you-dont-have-a-power-bi-account"></a>Kein Power BI-Konto vorhanden

Es wurde kein Power BI-Konto eingerichtet. Für ein gültiges Power BI-Konto benötigen Sie eine Lizenz und müssen sich zuvor bei Power BI angemeldet haben, um einen Power BI-Arbeitsbereich zu erstellen.   

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Nachricht: Es sind keine Berichte aktiviert. Wählen Sie „Bericht auswählen“ aus, um eine Liste der anzeigbaren Berichte anzuzeigen.

Diese Meldung wird angezeigt, wenn der Standardbericht nicht in Ihrem Power BI-Arbeitsbereich bereitgestellt werden konnte. Oder er wurde bereitgestellt, aber nicht erfolgreich aktualisiert. Navigieren Sie zum Bericht in Ihrem Power BI-Arbeitsbereich, wählen Sie **Datensatz**, **Einstellungen** aus und aktualisieren Sie die Anmeldedaten manuell. Wenn der Datensatz erfolgreich aktualisiert wurde, navigieren Sie zurück zu [!INCLUDE[prodshort](includes/prodshort.md)] und wählen Sie den Bericht auf der Seite **Berichte auswählen** manuell aus.


## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Power BI-Berichte erstellenl zur Anzeige von [!INCLUDE [prodlong](includes/prodlong.md)]-Daten](across-how-use-financials-data-source-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Arbeiten mit [!INCLUDE [prodshort](includes/prodshort.md)]-Daten in Power BI](across-working-with-business-central-in-powerbi.md)  
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
