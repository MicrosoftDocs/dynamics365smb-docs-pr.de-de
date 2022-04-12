---
title: Eine Firma mit RapidStart Services festlegen
description: Sie können eine neue Firma in Business Central mit RapidStart Services festlegen, um die Produktivität durch Automatisierung und Vereinfachung wiederkehrender Aufgaben zu erhöhen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8610, 8614, 8615, 8620, 8632
ms.date: 03/28/2022
ms.author: edupont
ms.openlocfilehash: b2d3378e9c06221bc91977883a53bba8514c6afc
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518311"
---
# <a name="set-up-a-company-with-rapidstart-services"></a>Ein Unternehmen mit RapidStart Services einrichten

Sie können in [!INCLUDE[prod_short](includes/prod_short.md)] mit RapidStart Services einen neuen Mandanten einrichten. Dies ist ein Werkzeug, das dazu dient, Bereitstellungszeiten zu verkürzen, die Qualität der Implementierung zu erhöhen, einen wiederholbaren Ansatz für Implementierungen einzuführen, und durch die Automatisierung und Vereinfachung wiederkehrender Prozesse die Produktivität zu erhöhen.  

Verwenden Sie diese Funktionen, um Ihr Unternehmen als Wiederverkäufer zu skalieren. Die meisten relevanten Seiten gelten für [!INCLUDE [prod_short](includes/prod_short.md)] Online und On-Premises. Einige Prozesse sind jedoch auf den Zugriff auf Dateien auf der Festplatte angewiesen und zu komplex, um sie für [!INCLUDE [prod_short](includes/prod_short.md)] Online zu verwenden. Für [!INCLUDE [prod_short](includes/prod_short.md)] möchten Sie wahrscheinlich Windows PowerShell verwenden, um Sie bei der Bereitstellung zu unterstützen. Weitere Informationen finden Sie unter [Verwaltung von Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/administration) bzw. [Verwaltung von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).  

RapidStart Services hilft Ihnen dabei, sich einen Überblick über den Einrichtungsprozess Ihres neuen Mandanten zu verschaffen. dazu dient ein Arbeitsblatt, in dem Sie die Tabellen einrichten können, die in Konfigurationsprozessen für neue Mandanten oft verwendet werden. Wenn Sie dies tun, können Sie einen Fragebogen erstellen, um Ihre Debitoren durch die Sammlung von Einrichtungsinformationen zu leiten. Ihre Debitoren haben die Option, anhand des Fragebogens Anwendungsbereiche einzurichten. Sie können auch die Einrichtungsseite direkt öffnen und die Einrichtung dort Vornehmen. Was am wichtigsten ist, RapidStart Services hilft Ihnen als Debitor dabei, den Mandanten mit Standard-Einrichtungsdaten vorzubereiten, die Sie individuell anpassen können. Und schließlich können Sie, wenn Sie RapidStart Services verwenden, vorhandene Kundendaten, etwa eine Liste von Debitoren oder Artikeln, konfigurieren und in den neuen Mandanten übertragen.

Sie können die folgenden Komponenten verwenden, um die Einrichtung eines neuen Mandanten zu beschleunigen:  

- Konfigurations-Assistent  
- Konfigurationsarbeitsblatt  
- Konfigurationspakete  
- Konfigurationsvorlagen  
- Konfigurationsfragebogen  

> [!Note]  
> Es gibt Bereiche von [!INCLUDE[prod_short](includes/prod_short.md)], die Sie manuell einrichten müssen. Dazu gehört das Hinzufügen von Benutzern, die Einrichtung von Buchhaltungsperioden und die Einrichtung von Dimensionen für die Business Intelligence. Weitere Informationen finden Sie unter [Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Erstellen Sie einen neuen Mandanten, und importieren Sie grundlegende Einrichtungsdaten und Vorlagen.|[Richten Sie eine Unternehmenskonfiguration ein](admin-set-up-company-configuration.md)|  
|Stellen Sie das konfigurierte Paket für Ihren Kunden für Implementierung bereit.|[Konfigurationen für neue Unternehmen übernehmen](admin-apply-configuration-to-new-companies.md)|
|Definieren und prüfen Sie die Einrichtung Ihres Kunden für alle Kernbereiche, z. B. Firmendaten, Finanzbuchhaltung, Lagerbestand, Verkauf oder Fertigung.|[Sammeln von Einrichtungswerten für Debitoren](admin-gather-customer-setup-values.md)|  
|Konfigurieren Sie Kern-Stammdatendatensätze, die auf Vorlagen basieren, um die Migrierung vorhandener Debitorendaten vorzubereiten.|[Vorgehensweise: Migrieren von Debitorendaten](admin-use-templates-to-prepare-customer-data-for-migration.md)|  
|Definieren Sie Tabellen und Felder, prüfen Sie vorhandene Debitorendaten, und migrieren Sie die Daten in die [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbank.|[Migrieren von Debitorendaten](admin-migrate-customer-data.md)|
|Bereiten Sie die Wiederverwendung von Unternehmenskonfigurationen in anderen Unternehmen vor (in den Entwickler- und Verwaltungsinhalten).|[Benutzerdefinierte Unternehmenskonfigurationspakete erstellen](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)|
|Finden Sie im RapidStart Services-Toolkit Lösungen für bekannte Probleme.|[Tipps und Tricks: RapidStart Services](admin-tips-and-tricks-rapidstart-services.md)|  

## <a name="see-also"></a>Siehe auch

[Verwaltung](admin-setup-and-administration.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]