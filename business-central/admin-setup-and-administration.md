---
title: Verwaltungsaufgaben in Business Central
description: 'Einige Aufgaben in Business Central erfordern eine zentrale Administration und Einrichtung. Erfahren, welche das sind und was zu tun ist.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# <a name="administration-tasks"></a>Verwaltungsaufgaben

Zentrale Verwaltungsaufgaben werden in der Regel von einer Rolle im Unternehmen ausgeführt. Der Bereich dieser Aufgaben kann von der Größe des Unternehmens und der Verantwortlichkeiten des Administrators abhängig sein. Diese Aufgaben können die Verwaltung von Datenbanksynchronisierung von Projekt- und E-Mail-Warteschlangen, das Einrichten von Benutzern, das Anpassen der Benutzeroberfläche und Verwalten von Verschlüsselungsschlüsseln enthalten.  

Die Eingabe der richtigen Einrichtungswerte ist entscheidend für den Erfolg jeder neuen Geschäftssoftware. [!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Einrichtungshandbücher, die Ihnen dabei helfen, Kerndaten einzurichten. Weitere Informationen finden Sie unter [Business Central einrichten](setup.md).

> [!NOTE]
> Sie können die Datenmigrationstools verwenden, um vorhandene Daten zu [!INCLUDE [prod_short](includes/prod_short.md)] Online zu migrieren. Sie können auch in [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Konfigurationspaketen einen neuen Mandanten einrichten, um Bereitstellungszeiten zu verkürzen, die Qualität der Implementierung zu erhöhen, einen wiederholbaren Ansatz für Implementierungen einzuführen, und durch die Automatisierung und Vereinfachung wiederkehrender Prozesse die Produktivität zu erhöhen. Weitere Informationen finden Sie unter [Lokale Daten zu Business Central Online migrieren](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Sie können Ihre Einrichtungsentscheidungen mit einigen allgemeinen Empfehlungen für ausgewählte Einrichtungsfelder unterstützen, von denen bekannt ist, dass Sie die Lösung möglicherweise dazu veranlassen, ineffizient zu arbeiten, wenn sie falsch definiert werden.  

Ein Superuser oder ein Administrator kann das Daten-Exchange-Framework einrichten, um Benutzern zu ermöglichen, Daten in den Bank- und Lohndateien, beispielsweise für verschiedene Bankmanagementprozesse, zu exportieren und zu importieren. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.  

|**Prozess**|**Siehe**|  
|------------|-------------|
|Definieren Sie, wer sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden darf, indem Sie Benutzer im Microsoft 365 Admin Center entsprechend den Produktlizenzen anlegen.|[Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md)|
|Weisen Sie Benutzern Berechtigungen zu, ändern Sie Berechtigungssätze und gruppieren Sie Benutzer für eine einfache Berechtigungsverwaltung.|[Berechtigungen an Benutzer und Gruppen zuweisen](ui-how-users-permissions.md)|
|Fügen Sie Benutzer hinzu, und verwalten Sie Berechtigungen und den Zugriff auf Daten.|[Profile verwalten](admin-users-profiles-roles.md)|
|Verwalten Sie Benutzereinstellungen wie Unternehmen, Rolle, Sprache, Region und Zeitzone.|[Benutzereinstellungen](admin-manage-user-settings-preferences.md)|
|Richten Sie Drucker ein und geben Sie an, welche Berichte auf welchen Druckern gedruckt werden sollen.|[Drucker einrichten](ui-specify-printer-selection-reports.md)|
|Klassifizieren Sie Datenempfindlichkeit für Felder, sodass Sie auf Anforderungen von den Datensubjekten reagieren können, die mit ihren Personendaten verknüpft werden.|[Datensensitivität klassifizieren](admin-classifying-data-sensitivity.md)|
|Antworten Sie auf Anforderungen von den Datensubjekten, die mit Ihren Personendaten verknüpft werden.|[Antworten auf Anforderungen zu Personendaten](admin-responding-to-requests-about-personal-data.md)|
|Einrichten eines neuen Konzernmandanten mithilfe von Vorlagen|[Neue Unternehmen erstellen](about-new-company.md)|
|Verfolgen aller direkten Änderungen, die von Benutzern an den Daten in der Datenbank vorgenommen werden, um die Quelle von Fehlern und Datenänderungen zu identifizieren|[Änderungen protokollieren](across-log-changes.md)|  
|Eingeben einzelner oder wiederkehrender Anforderungen zum Ausführen von Berichten oder Codeunits|[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)|  
|Verwalten, löschen oder komprimieren von Belegen|[Belege löschen](admin-manage-documents.md)|  
|Sie können Seiten, Codeunits und Abfragen als Webdienste zur Verfügung stellen.|[Einen Webdienst veröffentlichen](across-how-publish-web-service.md)|
|Als Teil der Erstellung von Connect Apps zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Lösungen von Drittanbietern über REST-APIs definieren Sie Vorlagen, die verwendet werden, um leere Eigenschaften in einer Entität zu füllen, wenn Sie eine POST-Aktion über eine API erstellen.|[API Vorlagen konfigurieren](admin-configuring-api-template.md)|
|Sie können Daten in [!INCLUDE[prod_short](includes/prod_short.md)] server verschlüsseln, indem Sie neue Verschlüsselungsschlüssel erstellen oder vorhandene importieren, die Sie auf dem Server ausführen.|[Datenverschlüsselung verwalten](admin-manage-data-encryption.md)|
|Dynamics 365 Sales mit [!INCLUDE[prod_short](includes/prod_short.md)] verbinden, um nahtlose Integration zwischen den Kundschaftsbeziehungen und der Auftragsabwicklung zu erhalten.|[Integrieren in Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ändern Sie, welche Felder und Aktionen in der Benutzeroberfläche angezeigt werden, um den Geschäftsprozessen des Unternehmens zu entsprechen, und erweitern Sie die Lösung mit Apps.|[[!INCLUDE[prod_short](includes/prod_short.md)] anpassen](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Verwaltung im Admin Center

Interne und stellvertretende Administratoren haben Zugriff auf das [!INCLUDE [prod_short](includes/prod_short.md)] Admin Center, wo sie [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebungen konfigurieren, überwachen und Fehler beheben können. Die folgende Tabelle beschreibt einige wichtige Aufgaben mit Links zu den Artikeln, die sie beschreiben..  

|**Prozess**|**Siehe**|  
|------------|-------------|
|Informieren Sie sich über die Tools, die Ihnen zur Fehlerbehebung zur Verfügung stehen.|[Technischer Support](/dynamics365/business-central/dev-itpro/technical-support)|
|Überwachen der Nutzung und Beheben von Fehlern in Sitzungen|[Umgebungstelemetrie im Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Verwalten Sie Benutzersitzungen, einschließlich des Abbrechens einer Sitzung, wenn der Benutzer blockiert ist.|[Sitzungen verwalten](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Konfigurieren Sie den Mandanten zum Senden von Telemetriedaten an Azure Application Insights zur besseren Analyse und Fehlerbehebung.|[Senden von Telemetrie an Application Insights aktivieren](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-also"></a>Siehe auch

[Geschäftsfunktionen](across-business-functionality.md)  
[Allgemeine Unternehmensfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
