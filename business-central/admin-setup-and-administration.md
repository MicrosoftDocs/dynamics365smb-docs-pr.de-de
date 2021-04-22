---
title: Administrative Aufgaben in Business Central | Microsoft Docs
description: Einige Aufgaben in Business Central erfordern eine zentrale Administration und Einrichtung. Erfahren, welche das sind und was zu tun ist.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 13f713756fc1f771243686c549c22f3ce0974b6b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777216"
---
# <a name="administration"></a>Verwaltung

Zentrale Verwaltungsaufgaben werden in der Regel von einer Rolle im Unternehmen ausgeführt. Der Bereich dieser Aufgaben kann von der Größe des Unternehmens und der Verantwortlichkeiten des Administrators abhängig sein. Diese Aufgaben können die Verwaltung von Datenbanksynchronisierung von Projekt- und E-Mail-Warteschlangen, das Einrichten von Benutzern, das Anpassen der Benutzeroberfläche und Verwalten von Verschlüsselungsschlüsseln enthalten.  

Die Eingabe der richtigen Einrichtungswerte ist entscheidend für den Erfolg jeder neuen Geschäftssoftware. [!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Einrichtungshandbücher, die Ihnen dabei helfen, Kerndaten einzurichten. Weitere Informationen finden Sie unter [Business Central einrichten](setup.md).

Ob Sie RapidStart Services verwenden, um Einrichtungswerte zu implementieren, oder diese manuell im neuen Mandanten eingeben, Sie können Ihre Einrichtungsentscheidungen mit allgemeinen Empfehlungen für ausgewählte Einrichtungsfelder unterstützen, von denen bekannt ist, dass Sie die Lösung möglicherweise dazu veranlassen, ineffizient zu arbeiten, wenn sie falsch definiert werden.  

Ein Superuser oder ein Administrator kann das Daten-Exchange-Framework einrichten, um Benutzern zu ermöglichen, Daten in den Bank- und Lohndateien, beispielsweise für verschiedene Bankmanagementprozesse, zu exportieren und zu importieren. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).

> [!NOTE]
> Sie können in [!INCLUDE[prod_short](includes/prod_short.md)] mit RapidStart Services einen neuen Mandanten einrichten. Dies ist ein Werkzeug, das dazu dient, Bereitstellungszeiten zu verkürzen, die Qualität der Implementierung zu erhöhen, einen wiederholbaren Ansatz für Implementierungen einzuführen, und durch die Automatisierung und Vereinfachung wiederkehrender Prozesse die Produktivität zu erhöhen. Weitere Informationen finden Sie unter [Mandanten einrichten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben.  

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Definieren Sie, wer sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden darf, indem Sie Benutzer im Microsoft 365 Admin Center entsprechend den Produktlizenzen erstellen.|[Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md)|
|Weisen Sie Benutzern Berechtigungen zu, ändern Sie Berechtigungssätze und gruppieren Sie Benutzer für eine einfache Berechtigungsverwaltung.|[Berechtigungen an Benutzer und Gruppen zuweisen](ui-how-users-permissions.md)|
|Fügen Sie Benutzer hinzu, und verwalten Sie Berechtigungen und den Zugriff auf Daten.|[Profile verwalten](admin-users-profiles-roles.md)|
|Verwalten Sie Benutzereinstellungen wie Unternehmen, Rolle, Sprache, Region und Zeitzone.|[Benutzereinstellungen](admin-manage-user-settings-preferences.md)|
|Richten Sie Drucker ein und geben Sie an, welche Berichte auf welchen Druckern gedruckt werden sollen.|[Drucker einrichten](ui-specify-printer-selection-reports.md)|
|Klassifizieren Sie Datenempfindlichkeit für Felder, sodass Sie auf Anforderungen von den Datensubjekten reagieren können, die mit ihren Personendaten verknüpft werden.|[Datensensitivität klassieren](admin-classifying-data-sensitivity.md)|
|Antworten Sie auf Anforderungen von den Datensubjekten, die mit Ihren Personendaten verknüpft werden.|[Antworten auf Anforderungen zu Personendaten](admin-responding-to-requests-about-personal-data.md)|
|Einrichten eines neuen Konzernmandanten mithilfe von Vorlagen|[Neue Unternehmen anlegen](about-new-company.md)|
|Verfolgen aller direkten Änderungen, die von Benutzern an den Daten in der Datenbank vorgenommen werden, um die Quelle von Fehlern und Datenänderungen zu identifizieren|[Änderungen protokollieren](across-log-changes.md)|  
|Eingeben einzelner oder wiederkehrender Anforderungen zum Ausführen von Berichten oder Codeunits|[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)|  
|Verwalten, löschen oder komprimieren von Belegen|[Löschen von Belegen](admin-manage-documents.md)|  
|Sie können Seiten, Codeunits und Abfragen als Webdienste zur Verfügung stellen.|[Webdienst veröffentlichen](across-how-publish-web-service.md)|
|Als Teil der Erstellung von Connect Apps zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Lösungen von Drittanbietern über REST-APIs definieren Sie Vorlagen, die verwendet werden, um leere Eigenschaften in einer Entität zu füllen, wenn Sie eine POST-Aktion über eine API erstellen.|[API Vorlagen konfigurieren](admin-configuring-api-template.md)|
|Sie können Daten in [!INCLUDE[prod_short](includes/prod_short.md)] server verschlüsseln, indem Sie neue Verschlüsselungsschlüssel erstellen oder vorhandene importieren, die Sie auf dem Server ausführen.|[Datenverschlüsselung verwalten](admin-manage-data-encryption.md)|
|Dynamics 365 Sales mit [!INCLUDE[prod_short](includes/prod_short.md)] verbinden, um nahtlose Integration zwischen den Kundschaftsbeziehungen und der Auftragsabwicklung zu erhalten.|[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ändern Sie, welche Felder und Aktionen in der Benutzeroberfläche angezeigt werden, um den Geschäftsprozessen des Unternehmens zu entsprechen, und erweitern Sie die Lösung mit Apps.|[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|
|Überwachen Sie die Nutzung, und beheben Sie Fehler in Sitzungen.|[Umgebungstelemetrie im Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Verwalten Sie Benutzersitzungen, einschließlich des Abbrechens einer Sitzung, wenn der Benutzer blockiert ist.|[Verwalten von Sitzungen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Geschäftsfunktionen](across-business-functionality.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]