---
title: Arbeiten mit Business Central-Daten in Power BI | Microsoft Docs
description: Abrufen von Erkenntnissen, Business Intelligence und KPIs aus Ihren Business Central-Daten mithilfe von Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 07/10/2020
ms.author: jswymer
ms.openlocfilehash: bdcbcb0fa82d799e29cfcdbb034e231635510656
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697766"
---
# <a name="working-with-prodshort-data-in-power-bi"></a>Arbeiten mit [!INCLUDE [prodshort](includes/prodshort.md)]-Daten in Power BI

In diesem Artikel erlernen Sie einige der Grundlagen zum Arbeiten mit Berichten und Dashboards in Power BI, die [!INCLUDE [prodshort](includes/prodshort.md)] als Datenquelle verwenden. Der Artikel beschreibt einige Aspekte, die Ihnen den Einstieg als [!INCLUDE[prodshort](includes/prodshort.md)]-Benutzer erleichtern. Allgemeine Richtlinien und Anweisungen zur Verwendung von Power BI finden Sie unter [Power BI-Dokumentation für Verbraucher](https://review.docs.microsoft.com/en-us/power-bi/consumer).

## <a name="get-ready"></a>Vorbereitung

Registrieren Sie sich für den Power BI-Dienst. Wenn Sie sich noch nicht registriert haben, wechseln Sie zu [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Verwenden Sie bei der Registrierung eine geschäftliche E-Mail-Adresse und Ihr zugehöriges Kennwort.

## <a name="get-started"></a>Erste Schritte

Sobald Sie ein Power BI-Konto erstellt haben, können Sie sich unter [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/) anmelden.

Der Power BI-Dienst hostet alle Berichte, die Ihnen zur Verfügung stehen. Um den Bericht anzuzeigen, wählen Sie **Mein Arbeitsbereich** > **Berichte** aus. Wählen Sie dann einfach den Bericht aus, den Sie anzeigen möchten.

Mit [!INCLUDE[prodshort](includes/prodshort.md)] online stehen Ihnen in Ihrem Arbeitsbereich automatisch eine Reihe von Standardberichten zur Verfügung. Wenn Sie Ihre eigenen Berichte erstellen möchten, können Sie hierfür Power BI Desktop verwenden und die Berichte dann in Ihrem Arbeitsbereich veröffentlichen. Weitere Informationen finden Sie unter [Erste Schritte beim Erstellen von Berichten in Power BI Desktop zur Anzeige von [!INCLUDE [prodlong](includes/prodlong.md)]-Daten](across-how-use-financials-data-source-powerbi.md).

Wenn Sie [!INCLUDE[prodshort](includes/prodshort.md)] on-premises verwenden, müssen Sie mit Power BI Desktop bei Null anfangen. Optional können Power BI-Berichte als Dateien verteilt werden, die Sie hochladen können.

## <a name="get-the-latest-data"></a>Aktuelle Daten beziehen

Jeder Power BI-Bericht basiert auf einem Datensatz, der Daten aus den [!INCLUDE[prodshort](includes/prodshort.md)]-Quellen abruft. Vergewissern Sie sich, dass die Daten in Ihren Power BI-Berichten auf dem Stand der Daten in [!INCLUDE[prodshort](includes/prodshort.md)] sind. Dieses Konzept wird als *Aktualisieren* bezeichnet.  Abhängig davon, wie Ihre Organisation Power BI eingerichtet hat, wird die Aktualisierung möglicherweise nicht automatisch durchgeführt. Es gibt zwei Möglichkeiten, Daten zu aktualisieren: manuell oder über eine geplante Aktualisierung. Die manuelle Aktualisierung erfolgt bei Bedarf. Mit der geplanten Aktualisierung werden die Daten in definierten Zeitintervallen automatisch aktualisiert.

### <a name="refresh-manually"></a>Manuell aktualisieren

Wählen Sie im Navigationsbereich unter **Datensätze** neben dem Datensatz **Weitere Optionen (...)** aus. Wählen Sie dann **Jetzt aktualisieren** aus.

### <a name="schedule-a-refresh"></a>Eine Aktualisierung planen

Wählen Sie im Navigationsbereich unter „Datensätze“ neben dem Datensatz „Weitere Optionen (...)“ aus. Wählen Sie dann **Aktualisierung planen** aus. Geben Sie im Bereich **Aktualisierung planen** die benötigten Informationen ein und wählen Sie **Anwenden** aus.

Weitere Informationen finden Sie unter [Konfigurieren der geplanten Aktualisierung](/power-bi/connect-data/refresh-scheduled-refresh).

## <a name="upload-reports-from-files"></a><a name="upload"></a>Hochladen von Berichten aus Dateien

Power BI-Berichte können als .pbix-Dateien unter den Benutzern verteilt werden. Wenn Sie eine .pbix-Datei haben, können Sie die Datei in einen Arbeitsbereich hochladen. Gehen Sie folgendermaßen vor, um einen Bericht hochzuladen:

1. Wählen Sie in Ihrem neuen Arbeitsbereich **Daten abrufen** aus.

2. Wählen Sie im Feld „Dateien“ die Option **Abrufen** aus.

3. Wählen Sie **Lokale Datei** aus, navigieren Sie zum Speicherort der Datei und wählen Sie **Öffnen** aus.

Weitere Informationen finden Sie unter [Hochladen des Berichts in den Dienst](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Zum Hochladen eines Berichts benötigen Sie einen Arbeitsbereich in einer [Premium-Kapazität](/power-bi/service-premium-what-is). Weitere Informationen finden Sie unter [Premium-Kapazitäten verwalten](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Wenn Sie [!INCLUDE[prodshort](includes/prodshort.md)] online verwenden, können Sie einen Bericht auch aus [!INCLUDE[prodshort](includes/prodshort.md)] hochladen. Weitere Informationen finden Sie unter [Arbeiten mit Power BI-Berichten in [!INCLUDE [prodshort](includes/prodshort.md)] – Berichte hochladen](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Berichte mit anderen teilen

Sobald sich ein Bericht in Ihrem Arbeitsbereich befindet, können Sie ihn mit anderen Personen in Ihrer Organisation teilen.

Um einen Bericht zu teilen, wählen Sie in einer Liste mit Berichten oder in einem geöffneten Bericht **Teilen** aus. Geben Sie im Bereich **Bericht teilen** die vollständigen E-Mail-Adressen für Personen oder Verteilergruppen ein, mit denen Sie den Bericht teilen möchten. Befolgen Sie die Anweisungen auf dem Bildschirm, um das Teilen abzuschließen. Weitere Informationen finden Sie unter [Teilen von Dashboards oder Berichten](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Sie benötigen eine [Power BI Pro-Lizenz](/power-bi/service-features-license-type). Selbiges gilt auch für die Personen, mit denen Sie einen Bericht teilen möchten. Der Inhalt muss sich in einem Arbeitsbereich in einer [Premium-Kapazität](/power-bi/service-premium-what-is) befinden. Weitere Informationen finden Sie unter [Möglichkeiten zur gemeinsamen Nutzung Ihrer Arbeit in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Power BI-Berichte erstellenl zur Anzeige von [!INCLUDE [prodlong](includes/prodlong.md)]-Daten](across-how-use-financials-data-source-powerbi.md)  
[Übersicht über die Power BI-Integrationskomponente und -Architektur für [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Arbeiten mit Power BI-Berichten in [!INCLUDE [prodshort](includes/prodshort.md)]](across-working-with-powerbi.md)  
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
