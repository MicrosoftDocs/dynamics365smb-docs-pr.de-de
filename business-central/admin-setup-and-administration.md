---
title: Administrative Aufgaben in Business Central | Microsoft Docs
description: Einige Aufgaben in Business Central erfordern eine zentrale Administration und Einrichtung. Erfahren, welche das sind und was zu tun ist.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: c5b76a434403da0d472b1e1fa9430d40ff082220
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "924451"
---
# <a name="administration"></a>Verwaltung
Zentrale Verwaltungsaufgaben werden in der Regel von einer Rolle im Unternehmen ausgeführt. Der Bereich dieser Aufgaben kann von der Größe des Unternehmens und der Verantwortlichkeiten des Administrators abhängig sein. Diese Aufgaben können die Verwaltung von Datenbanksynchronisierung von Projekt- und E-Mail-Warteschlangen, das Einrichten von Benutzern, das Anpassen der Benutzeroberfläche und Verwalten von Verschlüsselungsschlüsseln enthalten.  

Die Eingabe der richtigen Einrichtungswerte ist entscheidend für den Erfolg jeder neuen Geschäftssoftware. [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Einrichtungshandbücher, die Ihnen dabei helfen, Kerndaten einzurichten. Weitere Informationen finden Sie unter [Business Central einrichten](setup.md).

Ob Sie RapidStart Services verwenden, um Einrichtungswerte zu implementieren, oder diese manuell im neuen Mandanten eingeben, Sie können Ihre Einrichtungsentscheidungen mit allgemeinen Empfehlungen für ausgewählte Einrichtungsfelder unterstützen, von denen bekannt ist, dass Sie die Lösung möglicherweise dazu veranlassen, ineffizient zu arbeiten, wenn sie falsch definiert werden.  

Ein Superuser oder ein Administrator kann das Daten-Exchange-Framework einrichten, um Benutzern zu ermöglichen, Daten in den Bank- und Lohndateien, beispielsweise für verschiedene Bankmanagementprozesse, zu exportieren und zu importieren.

> [!NOTE]
> Sie können in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit RapidStart Services einen neuen Mandanten einrichten, einem Werkzeug, das dazu dient, Bereitstellungszeiten zu verkürzen, die Qualität der Implementierung zu erhöhen, einen wiederholbaren Ansatz für Implementierungen einzuführen, und durch die Automatisierung und Vereinfachung wiederkehrender Prozesse die Produktivität zu erhöhen. Weitere Informationen finden Sie unter [Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Fügen Sie Benutzer hinzu, und verwalten Sie Berechtigungen und den Zugriff auf Daten.|[Benutzer, Profile und Rollencenter verstehen](admin-users-profiles-roles.md)|  
|Zuweisen von Benutzerberechtigungen, ändern von Zugriffsrechtsätzen und Gruppenbenutzerberechtigungen.|[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)|
|Klassifizieren Sie Datenempfindlichkeit für Felder, sodass Sie auf Anforderungen von den Datensubjekten reagieren können, die mit ihren Personendaten verknüpft werden.|[Datensensitivität klassieren](admin-classifying-data-sensitivity.md)|
|Antworten Sie auf Anforderungen von den Datensubjekten, die mit Ihren Personendaten verknüpft werden.|[Antworten auf Anforderungen zu Personendaten](admin-responding-to-requests-about-personal-data.md)|
|Einrichten eines neuen Konzernmandanten mithilfe von Vorlagen|[Neue Unternehmen anlegen](about-new-company.md)|
|Verfolgen aller direkten Änderungen, die von Benutzern an den Daten in der Datenbank vorgenommen werden, um die Quelle von Fehlern und Datenänderungen zu identifizieren|[Änderungen protokollieren](across-log-changes.md)|  
|Eingeben einzelner oder wiederkehrender Anforderungen zum Ausführen von Berichten oder Codeunits|[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)|  
|Verwalten, löschen oder komprimieren von Belegen|[Löschen von Belegen](admin-manage-documents.md)|  
|Sie können Seiten, Codeunits und Abfragen als Webdienste zur Verfügung stellen.|[Webdienst veröffentlichen](across-how-publish-web-service.md)|
|Als Teil der Erstellung von Verbindungs-Apps zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Drittanbieterlösungen durch REST APIs definieren Sie Vorlagen, die verwendet werden, um leere Eigenschaften einer Einheit zu füllen, wenn Sie eine BUCHUNGS-Aktion über ein API erstellen.|[API Vorlagen konfigurieren](admin-configuring-api-template.md)|
|Sie können Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] server verschlüsseln, indem Sie neue Verschlüsselungsschlüssel erstellen oder vorhandene importieren, die Sie auf dem Server ausführen.|[Datenverschlüsselung verwalten](admin-manage-data-encryption.md)|
|Verbinden Sie Dynamics 365 for Sales mit [!INCLUDE[d365fin](includes/d365fin_md.md)], um nahtlose Integration zwischen Kundschaftsbeziehungen und Auftragsabwicklung im Interessent-zu-Geld-Prozess zu erhalten.|[Integrieren in Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Ändern Sie, welche Felder und Aktionen in der Benutzeroberfläche angezeigt werden, um den Geschäftsprozessen des Unternehmens zu entsprechen, und erweitern Sie die Lösung mit Apps.|[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)|

## <a name="see-also"></a>Siehe auch
[Geschäftsfunktionen](across-business-functionality.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Erste Schritte](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
