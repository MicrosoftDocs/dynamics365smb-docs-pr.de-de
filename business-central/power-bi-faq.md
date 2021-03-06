---
title: Power BI FAQ
description: Erhalten Sie Antworten auf einige typische Fragen zur Arbeit mit Power BI und Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 939b280e631113d3196f6fbbc90d9bf19b9fc408
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025833"
---
# <a name="power-bi--faq"></a>Power BI FAQ

Dieser Artikel beantwortet einige typische Fragen zur Arbeit mit Power BI und [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Allgemein](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Ich habe in Business Central einen Bericht für mein Rollencenter ausgewählt. Wenn ich später online Änderungen an den Darstellungen des Berichts vornehme, wird das Rollencenter dann automatisch mit meinen Änderungen aktualisiert?

Ja, da die Berichte von Power BI eingebettet sind.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Sind die Business Central Apps für Power BI in anderen Sprachen als Englisch verfügbar?

Anzahl Diese Apps sind derzeit nur in Englisch verfügbar.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Sobald ein Bericht in meinem powerbi.com Arbeitsbereich veröffentlicht ist, kann ich sein pbix herunterladen? 

Ja. Weitere Informationen finden Sie unter [Herunterladen eines Berichts vom Dienst Power BI auf Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Kann ich die Apps als pbix-Dateien herunterladen? 

Anzahl Derzeit bieten wir den Download von pbix-Dateien für die offiziellen Power BI-Apps nicht an, da diese auf AppSource veröffentlicht werden.

## <a name="license"></a>[Lizenz](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Benötige ich eine Power BI Pro-Lizenz, um Berichte zu veröffentlichen? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Anzahl Eine Pro-Lizenz ist nicht erforderlich, um Berichte zu veröffentlichen. Die normale (kostenlose) Power BI-Lizenz ist ausreichend. Weitere Informationen finden Sie unter [Power BI-Lizenzierung](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Gibt es etwas, was ich mit der kostenlosen Lizenz nicht tun kann?

Sie können keine Berichte freigeben oder die Business Central Apps für Power BI installieren. Ansonsten lässt die kostenlose Lizenz zu, dass Sie fast alle Variationen von Diagrammen und Berichten erstellen können.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Wenn jemand einen Bericht mit einer anderen Person teilt, dann braucht diese Person eine Pro-Lizenz, um den Bericht zu sehen. Gibt es Pläne, diese Funktionalität auch mit der kostenlosen Lizenz zu ermöglichen?

Wir haben keine Kontrolle über dieses Erfordernis. Diese Anforderung ist durch Power BI festgelegt. Weitere Informationen finden Sie unter [Freigeben von Power BI-Dashboards und -Berichten für Mitarbeiter und andere](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Designer](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Funktioniert der Konnektor mit API-Seiten?

Noch nicht. Aber ab Juni 2021 wird der neue Power BI-Konnektor sowohl Business Central-Webdienste als auch API-Seiten unterstützen. Weitere Informationen finden Sie unter [Aktivieren Sie den Power BI-Konnektor, um mit Business Central APIs zu arbeiten, statt nur mit Webdiensten](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Ist es möglich zu wählen, aus welcher Business Central Umgebung die Daten für Power BI geholt werden sollen, z. B. aus einer Sandbox oder einer Produktionsumgebung? 

Ja. Das kann einfach gewählt werden. Wenn Sie sich über den Konnektor mit Business Central verbinden, müssen Sie die Umgebung und den Namen der Firma auswählen.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Kann ich Daten aus mehreren Produktionsumgebungen desselben Mandanten zusammenführen?

Ja. In Power BI führen Sie einfach den Vorgang „Daten abrufen“ erneut aus und wählen die gewünschte Umgebung aus.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Welche Seiten in Business Central haben den Power BI Berichtsteil?  

Derzeit gibt es einige ausgewählte Seiten, die eine FactBox mit einem **Power BI-Berichte**-Teil zur Anzeige eines Reports haben. 

Auf Listenseiten wird der **Power BI Berichte**-Teil gefiltert, um Berichte anzuzeigen, die sich auf die Daten in der Liste beziehen. Hier sind die Seiten vom Typ Liste, die den **Power BI-Berichte**-Teil enthalten:

|Seiten-ID|Name|
|-------|----|
|22|Debitor-Liste|
|27|Kreditor-Liste|
|31|Artikelübersicht|
|9305|Verkaufsauftragsliste|
|9308|Einkaufsrechnungen|

Hier sind weitere Seiten, die den größeren, nicht gefilterten **Power BI Berichte** Teil enthalten:

|Seiten-ID|Name|
|-------|----|
|1156|Firma Detail|
|4013|Intelligente Cloud Insights |
|9006|Auftragsverarbeiter-Rollencenter|
|9008|Logistik Basis-Rollenzentrum|
|9010|Produktionsplaner-Rollencenter|
|9015|Job Projekt Manager RC|
|9016|Service Disponent Rollencenter|
|9022|Business Manager Rollencenter|
|9024|Sicherheit Admin-Rollencenter|
|9026|Vertrieb und Beziehungen Mgr. RC|
|9027|Buchhalter-Rollencenter|

> [!TIP]
> Wir haben im Moment nicht vor, es zu allen Listenseiten hinzuzufügen. Sie können jedoch eine einfache Seitenerweiterung erstellen, die den **Power BI-Berichte** Teil in einer FactBox hinzufügt. Weitere Informationen finden Sie unter [Hinzufügen von Power BI Berichtsteilen zu Seiten](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) in der Hilfe für Entwickler und IT Pro.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Gibt es eine Möglichkeit, ein Dataset aus Business Central zu filtern, *bevor* ich es in Power BI ziehe, anstatt danach Filter anzuwenden?

Um größere Datasets zu filtern, ist es am einfachsten, einen Filter auf Ihren Power BI-Bericht festzulegen, indem Sie direkt die Power Query-Formel bearbeiten. Die meisten der Filter, die Sie auf diese Weise festlegen, werden durch das Falten der Abfrage an Business Central weitergegeben. Siehe [Inkrementelle Aktualisierung für Datasets](/power-bi/admin/service-premium-incremental-refresh).

Es gibt derzeit keine Möglichkeit, einen Filter für die Webservice-Daten von Business Central aus festzulegen. Wenn Ihre Anwendung einen Filter aus Business Central heraus festlegen muss, müssen Sie zu diesem Zweck eine angepasste Business Central App erstellen.

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>Für die Einbettung von Berichten in Business Central Seiten ist es im Moment nur möglich, Berichte aus *Mein Arbeitsbereich* in Power BI zu erhalten. Gibt es Pläne, es möglich zu machen, sie aus angepassten Arbeitsbereichen zu erhalten?

Ja. Wir haben es in unseren Plänen, Unterstützung für gemeinsame Arbeitsbereiche hinzuzufügen, aber wir haben noch keinen Zeitplan, den wir Ihnen geben können.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Gibt es neben der Verwendung einer Abfrage in Power BI eine andere Möglichkeit, Daten aus Business Central-Tabellen abzurufen, die keine zugehörige Seite haben? Zum Beispiel, wie die *Element-Attribute-Wert-Zuordnung* Tabelle.

Anzahl Im Moment nicht.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Sind veröffentlichte Abfragen schneller zu verwenden als veröffentlichte Seiten?

Wenn es um Webdienste geht, sind veröffentlichte Abfragen in der Regel schneller als entsprechende veröffentlichte Seiten. Der Grund dafür ist, dass Abfragen für das Lesen von Daten optimiert sind und keine teuren Auslöser wie OnAfterGetRecord enthalten.

Wenn der neue Konnektor im Juni 2021 verfügbar ist, sollten Sie lieber API-Seiten verwenden als Abfragen, die als Webservices veröffentlicht werden.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-developer-have-to-create-a-custom-query"></a>Gibt es eine Möglichkeit für einen Endbenutzer, einen Webservice mit einer Spalte zu erstellen, die sich in einer Business Central-Tabelle befindet, aber nicht in einer Seite? Oder muss der Entwickler eine angepasste Abfrage erstellen? 

Noch nicht. Aber wenn der neue Konnektor im Juni 2021 verfügbar ist, kann ein Entwickler eine neue API-Seite erstellen, um diese Anforderung zu erfüllen. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Kann ich eine Power BI-Verbindung zu einem schreibgeschützten Datenbankserver von Business Central online herstellen? 

Anzahl Aber wir haben diese Funktion auf unserer langfristigen Roadmap. 

## <a name="performance"></a>[Leistung](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Ist es schneller, Daten über API-Seiten abzurufen als über Webdienste?

Ja. Unsere Tests zeigen, dass API-Seiten bis zu 25 % performanter sind als Webdienste.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Ist ein Mirror auf der Azure SQL Database-Instanz geplant, mit dem ich mich direkt verbinden kann?

Anzahl Im Moment nicht. Sie können nur über APIs mit Business Central kommunizieren.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Das Laden von Daten aus Business Central-Webdiensten scheint langsam zu sein. Gibt es eine Möglichkeit, Daten direkt aus der SQL-Datenbanktabelle abzurufen?

Anzahl Ein direkter Zugriff auf die Datenbank ist nicht möglich, aber der Wechsel zu API-Seiten (wenn der neue Konnektor verfügbar ist) wird eine große Hilfe sein.

## <a name="advanced"></a>[Erweitert](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Gibt es Pläne für den Power BI-Konnektor, die Funktionen zur inkrementellen Aktualisierung im Power BI-Service zu unterstützen?

Ja. Das ist auf unserer Roadmap.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Wenn eine Business Central Lösung vor Ort keinen Zugriff auf das Internet hat, kann ich dann trotzdem Power BI verwenden?
<!-- todo: please explain this one-->

Ja. In diesem Fall verwenden Sie Power BI Desktop lokal und verbinden sich mit dem Business Central vor Ort. Sobald Sie verbunden sind, können Sie Berichte erstellen und anzeigen, aber Sie können sie nicht mit dem Power BI-Dienst veröffentlichen. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Ist es geplant, die Online-Datenbanken von Business Central so zu replizieren, dass sie für schreibgeschützte SQL-Abfragen zugänglich sind? Diese Funktionalität würde eine inkrementelle Aktualisierung unterstützen und wäre viel schneller als APIs oder Webservices.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. Wir haben diese Funktion auf unserer langfristigen Roadmap. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Wenn ich Azure Data Factory verwende, um Daten von Business Central zu erhalten und sie auf Power BI zu konsumieren, wird das zu einer Leistungssteigerung beitragen? 

Ja. Dieses erweiterte Szenario wird Business Central helfen, performant zu bleiben, da der Zugriff auf die Daten über die Azure Data Factory erfolgen würde.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Gibt es Pläne, Power BI Bereitstellungspipelines zu unterstützen oder eine Möglichkeit, Bereitstellungspipelines für PBI-Berichte zu erstellen, ähnlich wie bei Erweiterungen? Oder vielleicht sogar eine einfache API im Business Admin-Center? 

Wir schauen uns diese Funktion an. Power BI bietet reichhaltige APIs, um das Bereitstellen von Berichten zu steuern. Weitere Informationen finden Sie unter [Einführung in Bereitstellungs-Pipelines](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>Ich habe die Vorschau des neuen Konnektors ausprobiert, der im Juni 2021 live sein wird. Ich sehe einige Werte wie „_x0020_“ beim Verbinden mit API v2.0. Was sind diese Werte?

Mit der kommenden Version des Konnektors Power BI können Sie sich mit den Business Central API-Seiten verbinden, einschließlich API v2.0. Diese Seiten enthalten ein paar Felder, die auf [AL Enum-Objekten](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums) basieren. Felder, die auf AL Enum-Objekten basieren, müssen konsistente und immer gleiche Namen haben, damit die Filter im Bericht immer funktionieren &mdash; unabhängig von der Sprache oder dem Betriebssystem, das Sie verwenden. Aus diesem Grund werden die Felder, die auf AL Enums basieren, nicht übersetzt und so kodiert, dass alle Sonderzeichen, einschließlich des Leerzeichens, vermieden werden. Insbesondere wird jedes Mal, wenn es eine leere Option im AL Enum-Objekt gibt, diese in „_x0020_“ kodiert. Sie können immer eine Transformation auf Power BI anwenden, wenn Sie einen anderen Wert für diese Felder anzeigen möchten, z. B. „Leer“.


---

## <a name="see-also"></a>Siehe auch

[Power BI Lizenzierung](admin-powerbi-setup.md#license)
[Business Central und Power BI Einführung](admin-powerbi.md)  
[Power BI Integration Übersicht](admin-powerbi-overview.md)  
[Aktivierung von Power BI in Business Central](admin-powerbi-setup.md)  
[Arbeiten mit Power BI-Berichten in Business Central](across-working-with-powerbi.md)  
[Arbeiten mit Business Central-Daten in Power BI](across-working-with-business-central-in-powerbi.md)  
[Erstellung von Power BI-Berichten zur Anzeige von Business Central-Daten](across-how-use-financials-data-source-powerbi.md)    
[Power BI Dokumentation](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]