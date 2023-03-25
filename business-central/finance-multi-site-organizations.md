---
title: Business Central für Unternehmen mit mehreren Standorten und internationalen Organisationen | Microsoft Dokumente
description: 'Business Central bietet Funktionalitäten, die ein Hub-and-Spoke-Geschäftsmodell unterstützen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'hub-and-spoke, multi-site, headquarter, sites'
ms.date: 10/01/2020
ms.author: bholtorf
---

# Business Central für Unternehmen mit mehreren Standorten und internationale Organisationen
Organisationen mit mehreren Standorten verwenden häufig ein Hub-and-Spoke-Geschäftsmodell, bei dem eine übergeordnete Firma oder die Zentrale die gesamten Vorgänge des Unternehmens verwaltet, während jeder Standort als einzelne, unabhängige Entität fungiert. Die Standorte sind oft geografisch verteilt und haben unterschiedliche Anforderungen an den Informationsaustausch mit der Firma in der Zentrale. Außerdem benötigen die Standorte in der Regel nicht den gleichen Grad an Komplexität und haben oft nicht die Ressourcen, um ein großes System zu pflegen.

[!INCLUDE[prod_short](includes/prod_short.md)] bietet kleinen und mittelständischen Unternehmen eine betriebswirtschaftliche Lösung, die einfach zu bedienen und kostengünstig zu warten ist.

In diesem Artikel werden einige der Möglichkeiten vorgestellt, wie [!INCLUDE[prod_short](includes/prod_short.md)] ein Hub-and-Spoke-Geschäftsmodell unterstützt.

## Integration der Firma in der Zentrale und der Standorte

[!INCLUDE[prod_short](includes/prod_short.md)] kann in das Buchhaltungssystem der Hauptfirma integriert werden und gleichzeitig die unterschiedlichen Anforderungen der verschiedenen Standorte erfüllen, unabhängig von Größe, Lagerplatz oder Art des Geschäfts.

Das folgende Diagramm ist ein Beispiel für die Integration verschiedener Standorte mit einer Firma in der Zentrale.

![Diagramm Beschreibung automatisch generiert.](media/multisite-headquarter-sites.png)

## Erfüllen Sie die Bedürfnisse von inländischen und internationalen Standorten

Die geschäftlichen Anforderungen der Standorte unterscheiden sich oft aufgrund ihrer Branche, ihrer Geschäftsmethoden oder ihrer Beziehung zur Firma in der Zentrale. [!INCLUDE[prod_short](includes/prod_short.md)] kann leicht für verschiedene Arten von Unternehmen und Standorten angepasst und erweitert werden. Microsoft AppSource bietet eine Fülle von Apps von Microsoft und unseren Partnern, und Partner können [!INCLUDE[prod_short](includes/prod_short.md)] schnell und mit minimaler Unterbrechung des täglichen Vorgangs bereitstellen.

Für multinationale Unternehmen unterstützt [!INCLUDE[prod_short](includes/prod_short.md)] die lokalen rechtlichen Anforderungen und Geschäftspraktiken.

* Für Onlineversionen gibt es mehr als [40 lokalisierte Länderversionen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json), die Sie als Erweiterungen von Microsoft AppSource installieren können.  
* Für lokale Versionen sind [Länderversionen](/azure/architecture/solution-ideas/articles/business-central) entweder als von Microsoft lokalisierte Versionen oder als von Partnern betriebene Zusatzlokalisierungen verfügbar.

Ein Netzwerk von mehr als 4.000 Microsoft-Partnern weltweit sorgt für lokale Expertise.

| **Business-Anforderung** | **Wie Business Central sie unterstützt** | **Mehr erfahren** |
|-------------------------|-------------------------|-------------------------|
| Schneiden Sie das System auf Ihr Unternehmen zu. | Profitieren Sie von einem System, das von Anfang an für mittelständische Unternehmen konzipiert wurde. | [Übersicht](https://dynamics.microsoft.com/business-central/overview/) |
| Erfüllen Sie gesetzliche Vorschriften und lokale Praktiken. | Erfüllen Sie die lokalen gesetzlichen Anforderungen und Geschäftspraktiken. | [Lokale Funktionalität](about-localization.md) |
| Greifen Sie auf mehrere Firmen von einer einzigen Seite aus zu. | Erhalten Sie schnellen Zugriff auf jede Business Central Firma in Ihrem Unternehmen. | [Unternehmens-Hub](ui-extensions-company-hub.md) |
| Verarbeiten Sie mehrere Sprachen und Währungen. | Die Unterstützung für mehrere Sprachen und Währungen hilft, lokale Anforderungen zu erfüllen. | [Mehrsprachige Funktionalitäten](about-locale-language.md)<br></br>[Mehrere Funktionalitäten für mehrere Währungen](finance-how-setup-additional-currencies.md) |


## Finanzdaten konsolidieren

Ein zentraler Aspekt des Hub-and-Spoke-Geschäftsmodells ist die Möglichkeit für die Firma in der Zentrale und die Standorte, Finanzdaten auszutauschen, auch wenn die Firma in der Zentrale und die Standorte unterschiedliche Systeme, Buchhaltungsstrukturen, Sprachen und Währungen verwenden.

| **Business-Anforderung** | **Wie Business Central sie unterstützt** | **Mehr erfahren** |
|-------------------------|-------------------------|-------------------------|
| Konsolidieren Sie Finanzdaten von Standorten. | Konsolidieren Sie die Finanzdaten von Standorten, unabhängig davon, ob sie Business Central oder eine andere Anwendung ausführen, zu einer einzigen Entität (Firma). | [Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md) |
| Integrieren Sie Buchhaltungsstrukturen. | Übertragen Sie Konsolidierungsdaten aus verschiedenen Buchhaltungsstrukturen in Ihre eigene. Integriertes Dateiformat für F&O (verfügbar mit Wave 2, 2020) | [Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)<br></br>[Hauptbuchkonten für die Konsolidierung vorbereiten](finance-consolidated-company-reporting-setup.md#glacc) |
| Führen Sie Transaktionen in mehreren Währungen durch. | Helfen Sie dabei, dass Abschlüsse in verschiedenen Währungen genau sind und korrekte Wechselkurse verwenden. | [Währungswechselkurse aktualisieren](finance-how-update-currencies.md) |

## Teilen Sie Business Insights mit integrierten Analysen

Richten Sie die Organisation auf Ihre Geschäftsziele aus, indem Sie ein allgemeines Verständnis der aktuellen Realität schaffen. Integrierte Analysen können dazu beitragen, dass alle Mitarbeiter ihre Entscheidungen auf der Grundlage der gleichen Faktenlage treffen.

| **Business-Anforderung** | **Wie Business Central sie unterstützt** | **Mehr erfahren** |
|-------------------------|-------------------------|-------------------------|
| Teilen Sie Insights mit Standorten ohne umfangreiche IT-Unterstützung. | Erstellen Sie KPIs und Business Intelligence Dashboards in Power BI auf der Basis Ihrer Daten. | [Mit Business Central-Daten in Power BI arbeiten](across-working-with-business-central-in-powerbi.md) |
| Entwickeln Sie angepasste Finanzberichte. | Generieren Sie parameterbasierte Finanzberichte. | [Business Intelligence](bi.md) |
| Orientieren Sie sich an den Fakten. | Generieren Sie Berichte, zeigen Sie sie an und teilen Sie sie mit internen und externen Beteiligten. | [Finanzberichte](finance-reports.md) |
| Analysieren Sie Daten in Excel. | Finden Sie Fakten, beheben Sie Probleme und führen Sie Ad-hoc-Analysen in Microsoft Excel durch. | [Analysieren von Finanzberichten in Excel](finance-analyze-excel.md) |


## Daten mithilfe von APIs und XMLports austauschen

APIs und XMLports vereinfachen den Prozess der Verbindung von Instanzen von [!INCLUDE[prod_short](includes/prod_short.md)], einschließlich derjenigen, die für jeden Standort angepasst wurden.

| **Business-Anforderung** | **Wie Business Central sie unterstützt** | **Mehr erfahren** |
|-------------------------|-------------------------|-------------------------|
| Verbinden Sie angepasste Versionen zwischen Standorten und der Firma in der Zentrale. | API-Seiten können jede Darstellung einer Entität offenlegen, einschließlich ihrer Anpassungen. | [Aktivieren von APIs für Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Versionsverwaltung und Sicherheit. | Die APIs verwenden ODataV4, das Versionsverwaltung, Webhooks und Änderungsverfolgung bietet. | [Sicherheit und Schutz](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Posten und Importieren von XML-Dokumenten. | Codeunits können als ungebundene Aktionen ausgesetzt werden, um das Posten und Einbinden von XML-Dokumenten zu unterstützen. Zum Verarbeiten von XML-Dokumenten können XMLports verwendet werden. Ungebundene Aktionen sind auch in der Lage, ein XML- oder JSON-Dokument zu erzeugen. | [XMLport-Objekte](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Erleichtern Sie die Wartung durch elektronischen Datenaustausch. | Eine Lösung für den elektronischen Datenaustausch kann hinzugefügt werden, um als Integrationsschicht zwischen der Firma in der Zentrale und den Standorten zu dienen. | [Data Exchange Framework](across-about-the-data-exchange-framework.md) |
| Tauschen Sie Daten zwischen verschiedenen Systemen aus. | Verwenden Sie XMLports, um XML-Dokumente zu erstellen, die dann zwischen einer Firma in der Zentrale, die ein System verwendet, und Standorten, die Business Central verwenden, ausgetauscht werden können. | [XMLport-Übersicht](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Orchestrieren Sie komplexen Datenaustausch. | Verwenden Sie eine Kombination aus XMLports mit Business Central und Microsoft BizTalk Server, um die speziellen Anforderungen an Ihren Standorten zu erfüllen.</br>Verwenden Sie für komplexe Anforderungen eine Lösung für den elektronischen Datenaustausch auf Basis von BizTalk Server und Commerce Gateway in Business Central in Kombination mit den XMLports. | [Arbeiten mit Berichten, Batchaufträgen und XMLports](ui-work-report.md) |
| Verbinden Sie sich mit Lösungen und Diensten von Drittanbietern. | APIs stellen eine Punkt-zu-Punkt-Verbindung zwischen Business Central und Lösungen und Diensten von Dritt<sup></sup>parteien her. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## Fördern Sie eine effiziente Intercompany-Lieferkette

Standorte benötigen oft Zugriff auf die Lieferkette und die Möglichkeit, bestimmte Aspekte dieser Kette zu verwalten. Zum Beispiel könnten Standorte denselben Kreditor verwenden, aber ihre Anlagen und physischen Lagerplätze separat verwalten.

| **Business-Anforderung** | **Wie Business Central sie unterstützt** | **Mehr erfahren** |
|-------------------------|-------------------------|-------------------------|
| Behandeln Sie bereichsübergreifende Transaktionen wie normale Verkaufs- und Kauf-Transaktionen. | Verwenden Sie firmenübergreifende Buchungen, um Verkaufs- und Kaufbelege sowie Hauptbucheinträge für ganze Workflows zu erstellen, und zwar für mehrere Firmen gleichzeitig, um doppelte Dateneingaben zu vermeiden. | [Verwaltung von firmenübergreifenden Transaktionen](intercompany-manage.md) |
| Verwenden Sie papierlose Prozesse. | Vermeiden Sie die Kalkulation für das Senden, Empfangen und Drucken von Dokumenten. | [Eingehende Belege](across-income-documents.md)<br><br> [Verwalten von Anhängen, Links und Notizen zu Karten und Dokumenten](ui-how-add-link-to-record.md) |

## Reagieren Sie schnell auf neue Geschäftsbedingungen

Die Firma in der Zentrale muss in der Lage sein, schnell auf geschäftliche Veränderungen an jedem Standort zu reagieren. In Kombination mit Power Automate kann [!INCLUDE[prod_short](includes/prod_short.md)] als Frühwarnmechanismus dienen.

![Ein Screenshot eines POSTs in sozialen Medien Beschreibung automatisch generiert.](media/multisite-apps.png)

| **Business-Anforderung** | **Wie Business Central sie unterstützt** | **Mehr erfahren** |
|-------------------------|-------------------------|-------------------------|
| Automatisch E-Mail-Warnungen generieren. | Legen Sie in Power Automate Alarme fest, die E-Mails generieren, um Sie über kritische Geschäftsbedingungen an Standorten oder Partnern in der Lieferkette zu informieren. | [Business Central und Power BI](admin-powerbi.md) |
| Verwenden Sie Standard- oder angepasste Alarme. | Verwenden Sie 12 verschiedene Vorlagen, die für Business Central mitgeliefert werden, oder legen Sie Ihre eigenen Alarme fest, die zu Ihrem Unternehmen passen. | [Business Central in einem automatisierten Workflow verwenden](across-how-use-financials-data-source-flow.md) |

## Weitere Informationen
[Verwaltung von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
