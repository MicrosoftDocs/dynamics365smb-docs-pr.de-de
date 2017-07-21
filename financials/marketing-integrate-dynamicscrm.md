---
title: Verwalten von Kunden, die Dynamics 365 for Sales nutzen| Microsoft Docs
description: "Sie können Dynamics 365 for Sales aus Dynamics 365 for Financials nutzen, um Daten zu verknüpfen und eine nahtlose Integration und Synchronisation der führenden Prozesse sicherzustellen."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2f182d48a3d2c083507564b553fbe22ad7a2e661
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Verwalten Ihrer Debitoren-Verhältnisse mithilfe von Dynamics 365 for Sales in Dynamics 365 for Financials | Microsoft Docs
Wenn Sie 365 Dynamics for Sales für Debitorenverpflichtung verwenden, können Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] für Prozesse und Finanzen verwenden und eine nahtlose Integration in bargeldlose Prozesse haben.

Wenn Ihre Anwendung für die Integration mit Dynamics 365 eingerichtet ist, haben Sie Zugriff auf Umsatzdaten von [!INCLUDE[d365fin](includes/d365fin_md.md)] und in einigen Fällen auf umgekehrte Art. Mit dieser Integration können Sie mit Datentypen, die von beiden Diensten verwendet werden, arbeiten und diese synchronisieren. Dazu zählen etwa Debitoren, Kontakte und Verkaufsinformationen. Außerdem können Sie die Daten an beiden Lagerorten auf dem aktuellen Stand halten.  

> [!NOTE]  
>   In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] ist Dynamics 365 for Sales als Dynamics CRM erwähnt. Der Einfachheit halber verwendet der restliche Teil dieses Artikels die Terminologie, die verwendet wird in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Beispielsweise kann der Verkäufer in Dynamics CRM die Preislisten verwenden aus [!INCLUDE[d365fin](includes/d365fin_md.md)] wenn Sie einen Verkaufsauftrag erstellen. Wenn Artikel in der Verkaufsauftragszeile in Dynamics CRM hinzugefügt werden, sie sind auch in der Lage, den Lagerbestand (Verfügbarkeit) des Artikels anzuzeigen von [!INCLUDE[d365fin](includes/d365fin_md.md)]. Diese Daten dienen als Teil der unterstützten Einrichtung **Dynamics CRM-Verbindungseinrichtung**.  

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.  

## <a name="setting-up-the-connection"></a>Einrichten der Verbindung
Von der Startseite können Sie auf die **Dynamics CRM-Verbindungseinrichtung** unterstützte Einrichtung zugreifen, der Ihnen hilft, den Link einzurichten. Sobald Sie das getan wird, haben Sie eine nahtlose Kopplung der Dynamics CRM Datensätze mit [!INCLUDE[d365fin](includes/d365fin_md.md)] Datensätzen.  

> [!NOTE]  
>   Das folgende berücksichtigt die unterstützte Einrichtung, aber Sie können dieselben Aufgaben im Fenster **CRM-Verbindungseinrichtung** manuell ausführen.

Im unterstützten Einrichtungshandbuch können Sie auswählen, welche Daten zwischen den beiden Services zu synchronisieren sind. Sie können auch festlegen, dass Sie die vorhandene Lösung in Microsoft Dynamics CRM importieren möchten. In diesem Fall müssen Anmeldeinformationen für ein Administratorkonto angeben.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Richten Sie das Benutzerkonto für das Importieren der Lösung ein
Um eine vorhandene Lösung in Dynamics CRM zu importieren, verwendet das Einrichtungshandbuch ein Verwaltungskonto. Dieses Konto muss ein gültiger Benutzer in Dynamics CRM mit den folgenden Sicherheitsrollen sein:

* Systemadministrator  
* Lösungsanpasser  

Weitere Informationen finden Sie unter [Benutzer erstellen und Microsoft Dynamics 365 (online) Sicherheitsrollen zuweisen](https://technet.microsoft.com/library/jj191623.aspx) auf techNet und [Vorgehensweise: Verwalten Sie Benutzer und Berechtigungen](ui-how-users-permissions.md).  

Dieses Konto wird nur bei der Einrichtung verwendet. Sobald die Lösung in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert wurde, wird das Konto nicht mehr erforderlich.

### <a name="setting-up-the-user-account-for-synchronization"></a>Den Benutzer für die Synchronisierung einrichten
Die Integration beruht auf einem freigegebenen Benutzerkonto. In Ihrem Office 365-Abonnement müssen Sie einen dedizierten Benutzer erstellen, der für die Synchronisierung zwischen den beiden Services verwendet wird. Dieses Konto muss bereits ein gültiger Benutzer in Dynamics CRM sein, aber Sie müssen keine Sicherheitsrollen zum Konto zuordnen, da die Einrichtungshilfe dies für Sie konfigurieren wird. Sie müssen dieses Benutzerkonto einmal oder mehrere Male bei der Einrichtung festlegen, abhängig davon, wie viele Synchronisierungen Sie aktivieren möchten. Weitere Informationen finden Sie unter [Benutzer erstellen und Microsoft Dynamics 365 (online) Sicherheitsrollen zuweisen](https://technet.microsoft.com/library/jj191623.aspx) auf techNet.

Wenn Sie die *Artikelverfügbarkeit* aktivieren, muss das Integrationsbenutzerkonto einen Webdienst-Zugangsschlüssel haben. Dies basiert auf zwei Schritten auf der [!INCLUDE[d365fin](includes/d365fin_md.md)] Seite für das Benutzerkonto, Sie müssen Sie die Schaltfläche **Webdienstschlüssel ändern** auswählen und bei der CRM-Verbindungseinrichtung müssen Sie den Benutzer als OData-Webdienstbenutzer angeben.

Wenn Sie *Verkaufsauftragsintegration* aktivieren, müssen Sie einen Benutzer festlegen, der diese Synchronisierung verarbeiten kann - der Integrationsbenutzer oder ein anderes Benutzerkonto.

### <a name="coupling-records"></a>Kopplungsdatensätze
Im unterstützten Einrichtungshandbuch können Sie auswählen, welche Daten zwischen den beiden Services zu synchronisieren sind. Später können Sie die Synchronisierung für bestimmte Arten von Daten einrichten. Dieses wird als *Koppeln* betrachtet und der entsprechende Abschnitt bietet Empfehlungen für das, was Sie berücksichtigen müssen.

Wenn Sie Konten in Dynamics CRM als Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen möchten, müssen Sie die beiden Arten von Datensätzen koppeln. Dies ist nicht sehr kompliziert - öffnen Sie das Fenster **Debitorenübersicht** in [!INCLUDE[d365fin](includes/d365fin_md.md)], es gibt eine Aktion im Menüband, um diese Daten mit Dynamics CRM zu koppeln. Dann legen Sie fest, welche [!INCLUDE[d365fin](includes/d365fin_md.md)] Debitoren den Konten in Dynamics CRM entsprechen.

In bestimmten Bereichen beruht die Funktionalität auf Sie bestimmten Datensätze vor anderen Datensätzen, wie in der folgenden Liste angezeigt:

* Kunden und Konten  
  * Koppelt Verkäufer mit Dynamics CRM Benutzern zuerst  
* Artikel und Ressourcen  
  * Koppelt Maßeinheiten mit Dynamics CRM Einheitengruppe zuerst  
* Artikel und Ressourcenpreise  
  * Koppelt Kundenpreisgruppen mit Dynamics CRM Preisen zuerst  

> [!NOTE]  
>   Wenn Sie Verkaufspreise in Fremdwährungen verwenden, stellen Sie sicher, dass Sie Währungen mit Dynamics CRM Transaktionswährungen koppeln.

Dynamics CRM Verkaufsaufträge hängen von zusätzlichen Informationen wie Debitoren, Maßeinheiten, Währungen, Debitorenpreisgruppen, Artikeln und/oder Ressourcen ab. Damit Verkaufsaufträge in Dynamics CRM nahtlos arbeiten, müssen Sie Debitoren, Maßeinheiten, Währungen, Debitorenpreisgruppen, Artikel und/oder Ressourcen zuerst koppeln.

### <a name="synchronizing-records-fully"></a>Datensätze vollständig synchronisieren
Am Ende der unterstützen Einrichtung können Sie die Aktion **Vollständige Synchronisierung ausführen** auswählen, um die Synchronisierung aller Datensätze mit allen [!INCLUDE[d365fin](includes/d365fin_md.md)] Datensätzen mit allen verknüpften Einträgen in den verbundenen Dynamics CRM-Lösung zu starten. Im Fenster **Überprüfung vollständige CRM-Synchronisierung** wählen Sie die Aktion **Starten** aus. Die Synchronisierung beginnt dann, Aufgaben entsprechend der Abhängigkeiten auszuführen. Beispielsweise werden Währungsdatensätze vor Debitorendatensätze synchronisiert. Die vollständige Synchronisierung wird möglicherweise viel Zeit in Anspruch nehmen und läuft im Hintergrund, damit Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] weiter arbeiten können.

Um den Status aus einzelnen Projekte in einer vollständigen Synchronisierung sicherzustellen, blättern Sie im **Projektwarteschlangenposten-Status** nach unten zum Feld **Um Int. Tabellen-Projekt-Status** oder **Von Int. Tabellen-Projekt-Status** im Fenster **CRM Full Synch. Prüfen**.

Im Fenster **CRM-Verbindungseinrichtung** können Sie Details über sämtliche Synchronisierungen sehen. Von hier können Sie das **Integrationstabellenzuordnungen** Fenster auch öffnen, um Details über die Tabellen in den Finanzverhältnissen und der Dynamics CRM Lösung finden, die synchronisiert werden müssen.

## <a name="see-also"></a>Siehe auch
[Relationship Management](marketing-relationship-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassen der[!INCLUDE[d365fin](includes/d365fin_md.md)]Erfahrung](ui-experiences.md)  
[Vorgehensweise: Verwalten Sie Benutzer und Berechtigungen](ui-how-users-permissions.md)    
[Holen Sie Ihre Organisation und Benutzer zu Dynamics 365 (Online) an Bord](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
