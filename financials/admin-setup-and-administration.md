---
title: Verwaltungsaufgaben in Dynamics 365 | Microsoft Docs
description: Einige Aufgaben in Dynamics 365 erfordern eine zentrale Administration und Einrichtung. Erfahren, welche das sind und was zu tun ist.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: c7e5efe85dddcc7db84b05879f0c71990167c775
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a>Einrichtung und Verwaltung in Dynamics 365 for Financials
Zentrale Verwaltungsaufgaben werden in der Regel von einer Rolle im Unternehmen ausgeführt. Der Bereich dieser Aufgaben kann von der Größe des Unternehmens und der Verantwortlichkeiten des Administrators abhängig sein. Diese Aufgaben können die Verwaltung von Datenbanksynchronisierung von Projekt- und E-Mail-Warteschlangen, das Einrichten von Benutzern, das Anpassen der Benutzeroberfläche und Verwalten von Verschlüsselungsschlüsseln enthalten.  

Die Eingabe der richtigen Einrichtungswerte ist entscheidend für den Erfolg jeder neuen Geschäftssoftware. [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Einrichtungshandbücher, die Ihnen dabei helfen, Kerndaten einzurichten. Weitere Informationen finden Sie unter [Dynamics 365 for Financials einrichten](setup.md).

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

Ein Superuser oder ein Administrator kann das Daten-Exchange-Framework einrichten, um Benutzern zu ermöglichen, Daten in den Bank- und Lohndateien, beispielsweise für verschiedene Bankmanagementprozesse, zu exportieren und zu importieren.  

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Fügen Sie Benutzer hinzu, und verwalten Sie Berechtigungen und den Zugriff auf Daten.|[Benutzer, Profile und Rollencenter in Dynamics 365 for Financials](admin-users-profiles-roles.md)|  
|Verfolgen aller direkten Änderungen, die von Benutzern an den Daten in der Datenbank vorgenommen werden, um die Quelle von Fehlern und Datenänderungen zu identifizieren|[Änderungen in Dynamics 365 for Financials protokollieren](across-log-changes.md)|  
|Unterstützen Sie Ihre Setupentscheidungen mit Empfehlungen für ausgewählte Felder, von denen bekannt ist, dass Sie die Lösung möglicherweise dazu veranlassen, ineffizient zu arbeiten, wenn sie falsch definiert werden.|[Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)|  
|Sie können Seiten, Codeunits und Abfragen als Webdienste zur Verfügung stellen.|[Vorgehensweise: Veröffentlichen eines Webdiensts](across-how-publish-web-service.md)|  
|Richten Sie einen SMTP-Server so ein, dass die E-Mail-Kommunikation mit Dynamics 365 for Financials aktiviert ist.| [Vorgehensweise: Richten Sie E-Mail Nachricht manuell oder mit der unterstützten Einrichtung ein](madeira-how-setup-email.md)|  
|Eingeben einzelner oder wiederkehrender Anforderungen zum Ausführen von Berichten oder Codeunits|[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)|  
|Verwalten, löschen oder komprimieren von Belegen|[Verwalten von Belegen](admin-manage-documents.md)|  
|Einrichten eines neuen Konzernmandanten mithilfe von Vorlagen|[Neue Unternehmen anlegen in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)|  

## <a name="see-also"></a>Siehe auch
[Geschäftsfunktionen](madeira-business-functionality.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Willkommen bei [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

