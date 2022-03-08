---
title: Einrichten des Benutzerkontos für die Integration in Dynamics 365 for Sales | Microsoft Docs
description: Erfahren Sie, wie die Benutzerkonten eingerichtet werden, die die Apps zum Austausch von Daten verwenden, und die Mitarbeiter nutzen, um auf Daten in den Apps zuzugreifen und diese Daten zu synchronisieren.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0f59324e41695e35e09a2dd970492acb3a8dba58
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726882"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Einrichten des Benutzerkontos für die Integration in Dynamics 365 for Sales
Dieser Artikel bietet eine Übersicht darüber, wie die Benutzerkonten eingerichtet werden, die erforderlich sind, um [!INCLUDE[d365fin](includes/d365fin_md.md)] in [!INCLUDE[crm_md](includes/crm_md.md)] zu integrieren.  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Einrichten des Admininstratorbenutzerkontos im Verkauf
Sie müssen Ihr Administratorbenutzerkonto für [!INCLUDE[d365fin](includes/d365fin_md.md)] als Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] hinzufügen und dann den Benutzer zum Administrator in [!INCLUDE[crm_md](includes/crm_md.md)] befördern. Das Administratorbenutzerkonto muss auch die Rolle des Systemanpassers und mindestens eine andere nicht administrative Benutzerrolle, z. B. Vertriebsmanager, in [!INCLUDE[crm_md](includes/crm_md.md)] haben.

## <a name="setting-up-the-user-account-for-the-integration"></a>Einrichten des Benutzerkontos für die Integration
Sie müssen ein spezifisches Benutzerkonto in Ihrem Office 365-Abonnement erstellen, das sowohl [!INCLUDE[d365fin](includes/d365fin_md.md)] als auch [!INCLUDE[crm_md](includes/crm_md.md)] verwenden können, um Daten zu synchronisieren. Dieses Benutzerkonto muss in der Lage sein, sich bei [!INCLUDE[crm_md](includes/crm_md.md)] anzumelden, was bedeutet, dass dieser Benutzer eine Lizenz für [!INCLUDE[crm_md](includes/crm_md.md)] benötigt und mindestens eine Sicherheitsrolle in [!INCLUDE[crm_md](includes/crm_md.md)] zugewiesen werden muss, wie [hier](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account) beschrieben wird. Weitere Informationen darüber, wie Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt werden, finden Sie unter [Verwalten von Sicherheit, Benutzern und Teams](http://go.microsoft.com/fwlink/?LinkID=616518). Nachdem die Verbindung eingerichtet ist, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] dem Benutzerkonto die Sicherheitsrollen zuweisen, die sie benötigen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und dieses Konto kann auf [ nicht interaktiven Zugriffsmodus](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) festgelegt werden in [!INCLUDE[crm_md](includes/crm_md.md)]

![Der Leitfaden für das unterstützte Setup zeigt den Ort, an dem die Anmeldeinformationen für die Synchronisierung eingegeben werden](media/sync-user-setup.png "Assistentenseite für die Visualisierung des unterstützten Setups zeigt den Ort, an dem die Anmeldeinformationen für die Synchronisierung eingegeben werden")

> [!IMPORTANT]  
> Verwenden Sie nicht das Administratorkonto für [!INCLUDE[crm_md](includes/crm_md.md)] für die Synchronisierung. Dadurch wird die Synchronisierung unterbrochen.
> Um die konstante Synchronisierung zu vermeiden, werden auch Änderungen an den Daten, die durch das Integrationsbenutzerkonto vorgenommen werden, nicht synchronisiert. <!--What changes would this account make?--> Nachdem die Verbindung hergestellt wurde, empfehlen wir, den Zugriffsmodus für das Benutzerkonto für die Integration auf einen nicht interaktiven Modus in [!INCLUDE[crm_md](includes/crm_md.md)] festzulegen. Weitere Informationen finden Sie unter [Erstellen eines nicht interaktiven Benutzerkontos](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Einrichten von Konten für Verkäufer
Sie müssen Benutzerkonten in [!INCLUDE[crm_md](includes/crm_md.md)] für die Verkäufer von [!INCLUDE[d365fin](includes/d365fin_md.md)]. Um das zu vereinfachen, bietet das Microsoft 365 Admin Center eine Excel-Vorlage, die Sie verwenden können. Wählen Sie auf der Seite **Aktive Benutzer** die Option **Mehr** und dann **Mehrere Benutzer importieren** aus. Wählen Sie **CSV-Datei nur mit Kopfzeilen herunterladen** aus und geben Sie dann die Informationen für die Verkäufer ein. Um ein Beispiel anzusehen, wählen Sie **CSV-Datei mit Kopfzeilen und Beispielbenutzerinformationen herunterladen** aus. Nachdem Sie die Informationen über die Benutzer eingeben, besteht der nächste Schritt im Importvorgang darin, den Benutzern Lizenzen zu dem Dynamics 365 Customer Engagement-Plan zuzuweisen.  

Nachdem Sie die Benutzer importiert und ihnen Lizenzen für Dynamics 365 Customer Engagement zugewiesen haben, müssen Sie die Benutzer der Rolle **Verkäufer** in [!INCLUDE[crm_md](includes/crm_md.md)] zuweisen.

![Koppeln von Verkäufern mit Benutzern in Dynamics 365 for Sales](media/couple-salespeople.png "Visualisierung des Koppelns von Verkäufern mit Benutzern in Dynamics 365 for Sales")

## <a name="minimum-permissions-for-user-accounts-in-crm_md"></a>Mindestberechtigungen für Benutzerkonten in [!INCLUDE[crm_md](includes/crm_md.md)]
Wenn Sie die Integrationslösung installieren, werden die Berechtigungen für das Benutzerkonto für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)] konfiguriert. Wenn diese Berechtigungen geändert werden, müssen Sie sie möglicherweise zurücksetzen. Sie können dies tun, indem Sie die Integrationslösung neu installieren oder manuell zurücksetzen. In den folgenden Tabellen sind die Mindestberechtigungen für die Benutzerkonten in [!INCLUDE[crm_md](includes/crm_md.md)] aufgeführt.

### <a name="integration-administrator"></a>Integrationsadministrator
In der folgenden Tabelle werden die Mindestberechtigungen für jede Registerkarte für jede Sicherheitsrolle angezeigt, die für den Administratorbenutzer erforderlich ist.

##### <a name="customization"></a>Anpassung
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Modellgesteuerte App|Global|||Lesen|
|Plugin-Montage|Global|Lesen|Lesen|Lesen|
|Plugin-Typ|Global|Lesen|Lesen|Lesen|
|Verbindungen|Global|||Lesen|
|SDK-Meldung|Global|Lesen|Lesen|Lesen|
|SDK-Nachrichtenverarbeitungsschritt|Global|Lesen|Lesen|Lesen|
|SDK-Nachrichtenverarbeitungsschrittbild|Global|Lesen|Lesen|Lesen|
|System von|Global|||Schreiben|

##### <a name="custom-entities"></a>Benutzerdefinierte Entitäten
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Business Central Kontostatistiken|Global|Lesen|Lesen|Lesen|
|Business Central Verbindung|Global|Erstellen, Lesen, Schreiben, Löschen|Erstellen, Lesen, Schreiben, Löschen|Erstellen, Lesen, Schreiben, Löschen|
|Buchungskonfiguration|Global|||Schreiben|

#### <a name="integration-user"></a>Integrationsbenutzer
In der folgenden Tabelle werden die Mindestberechtigungen für jede Registerkarte für jede Sicherheitsrolle angezeigt, die für den Integrationsbenutzer erforderlich ist.

##### <a name="core-records"></a>Zentrale Datensätze
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Konto|Global|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an, Zuweisen|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an, Zuweisen|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an, Zuweisen|
|Aktionskarte|Global||Lesen|Lesen|
|Verbindung|Global|Lesen|Lesen|Lesen|
|Kontakt|Global|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|
|Hinweis|Global|||Erstellen, Lesen, Schreiben, Anhängen löschen, Zuweisen|
|Verkaufschance|Global||Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|
|Buchung|Global|||Erstellen, Lesen, Anhängen an|
|Benutzeroberfläche der Entität|Benutzer|Erstellen, Lesen, Schreiben|Erstellen, Lesen, Schreiben|Erstellen, Lesen, Schreiben|

##### <a name="sales"></a>Verkauf
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Fakturieren|Global|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|
|Bestellung|Global|Lesen, Schreiben, Anhängen an|Lesen, Schreiben, Anhängen an|Lesen, Schreiben, Anhängen, Anhängen an, Zuweisen|
|Produkt|Global|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|
|Eigenschaft|Global|Lesen|Lesen|Lesen|
|Eigenschaftsverband|Global|Lesen|Lesen|Lesen|
|Eigenschaftsoptionssatzelement|Global|Lesen|Lesen|Lesen|
|Angebot|Global|Lesen|Lesen|Lesen|

##### <a name="service"></a>Dienst
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Anfrage|Global|Lesen|Lesen|Lesen|

##### <a name="business-management"></a>Geschäftsführung
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Währung|Global|Erstellen, Lesen, Schreiben|Erstellen, Lesen, Schreiben|Erstellen, Lesen, Schreiben|
|Organisation|Global|Lesen Schreiben|Lesen Schreiben|Lesen Schreiben|
|Sicherheitsrolle|Global|||Lesen|
|Benutzer|Global|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen, Anhängen an|
|Benutzereinstellungen|Global|Erstellen, Lesen, Schreiben, Löschen, Anhängen an|Erstellen, Lesen, Schreiben, Löschen, Anhängen an|Erstellen, Lesen, Schreiben, Löschen, Anhängen an|
|Im Namen eines anderen Benutzers handeln|Global|Ja|Ja|Ja|

##### <a name="customization"></a>Anpassung
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Feld|Global||Lesen|Lesen|
|Plugin-Montage|Global|Lesen|Lesen|Lesen|
|Plugin-Typ|Global|Lesen|Lesen|Lesen|
|SDK-Meldung|Global|Lesen|Lesen|Lesen|
|SDK-Nachrichtenverarbeitungsschritt|Global|Lesen|Lesen|Lesen|
|Webressourcen|Global|Lesen|Lesen|Lesen|

##### <a name="custom-entities"></a>Benutzerdefinierte Entitäten
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Bankkontostatistik|Global|Erstellen, Lesen, Schreiben, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen an|
|Dynamics 365 Business Central Verbindung|Global|Lesen|Lesen|Lesen|

### <a name="product-availability-user"></a>Produktverfügbarkeitnutzer
Sie können es Verkäufern ermöglichen, Inventarebenen für die von ihnen verkauften Artikel anzuzeigen, indem Sie ihnen die in der folgenden Tabelle beschriebenen Berechtigungen erteilen.

##### <a name="custom-entities"></a>Benutzerdefinierte Entitäten
|Sicherheitsrolle|Zugriffsebene|Dynamics NAV 2018 und früher|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Bankkontostatistik|Global|Erstellen, Lesen, Schreiben, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen an|Erstellen, Lesen, Schreiben, Anhängen an|
|Dynamics 365 Business Central Verbindung|Global|Lesen|Lesen|Lesen|

## <a name="see-also"></a>Siehe auch  
[Integrieren in Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
