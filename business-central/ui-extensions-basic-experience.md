---
title: Basic Experience-Erweiterung | Microsoft Docs
description: Diese Erweiterung ist eine modernisierte Alternative zu Microsoft Dynamics C5.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: e7377d1413e2f1969543374f1b819e6fc8a2a263
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927668"
---
# <a name="the-basic-experience-extension"></a>Die Basic Experience-Erweiterung
Wenn Sie bisher Microsoft Dynamics C5 verwendet haben, können Microsoft-Partner Ihnen beim Übergang zu einer moderneren Lösung helfen, die auf [!INCLUDE[d365fin](includes/d365fin_md.md)] basiert. So können Sie weiterhin dieselben optimierten Funktionen wie in Dynamics C5 nutzen.

Diese Erweiterung ist für kleine Unternehmen gedacht und kann bis zu drei Benutzer unterstützen. Wenn Sie mehr Benutzer benötigen, müssen Sie ein Upgrade auf eine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Lizenz durchführen und diese Erweiterung deinstallieren.

> [!NOTE]
> Ab sofort ist diese Erweiterung nur für Kunden in Dänemark und Island verfügbar. 

## <a name="whats-available"></a>Was ist verfügbar
In der folgenden Tabelle werden die Funktionen beschrieben, die verfügbar sind, wenn Sie die Basic Experience-Erweiterung installieren.

|Bereich  |Funktionalität  |
|---------|---------|
|**Sachposten** |Grundlegende Finanzen, Kontenschemata, Anlagen, Bankverwaltung, Bankabstimmung, Zahlungen, Lastschrift, Dimensionen, mehrere Währungen, Budgets, Workflow, Dokumentverwaltung/OCR, Konsolidierung, unbegrenzte Unternehmen|
|**Debitoren/Vertrieb** |Grundlegende Forderungen, Verkaufsfakturierung, Verkaufsrabatte, Preisberechnung, Umsatzsteuer, Kontaktverwaltung |
|**Verbindlichkeiten/Einkauf** |Grundlegende Verbindlichkeiten, Einkaufsfakturierung |
|**Projektmanagement** |Projekte, Projektpreisberechnung, Arbeitszeitnachweise, Zuweisungen, Aufgaben, Ressourcen |
|**Lager** |Grundlegender Lagerbestand, Artikelersetzungen, Artikelquerverweis |

## <a name="getting-started"></a>Erste Schritte
Diese Erweiterung unterscheidet sich ein wenig von den meisten anderen und Sie benötigen Hilfe von einem Microsoft-Partner, um sie zu installieren und einzurichten. Damit Sie wissen, was Sie erwartet, finden Sie hier eine allgemeine Übersicht darüber, was Ihr Microsoft-Partner für Sie tun wird.

1. Erstellen eines neuen [!INCLUDE[d365fin](includes/d365fin_md.md)]-Mandanten. Dies kann entweder eine Testversion oder eine CSP-Version sein.
2. Fügen Sie mindestens einen Benutzer hinzu, der einer Basic Experience-Lizenz in Ihrem Azure Active Directory-Konto zugewiesen wird.
3. Entfernen Sie alle Unternehmen, einschließlich des Beispielunternehmens Cronus.
4. Erstellen Sie ein neues Unternehmen, das keine Beispieldaten oder Setups enthält.
5. Fügen Sie das **Demo-RapidStart** -Paket hinzu. <!--what does the pockage contain?-->
6. Laden Sie die Basic Experience-Erweiterung von AppSource herunter und installieren Sie sie.

## <a name="migrating-data"></a>Migrieren von Daten
Bringen Sie Ihre Dynamics C5-Daten mit. Nachdem Ihr Microsoft-Partner die Basic Experience-Erweiterung installiert hat, haben Sie eine leere Firma. Eine einfache Möglichkeit, Ihre Daten von Dynamics C5 nach Basic Experience zu verschieben, ist die Verwendung der C5-Datenmigrations-Erweiterung, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] enthalten ist. Die Erweiterung migriert Kunden, Kreditoren, Artikel und Ihre Sachkonten sowie deren Posten.

## <a name="see-also"></a>Siehe auch
[Die C5-Datenmigrations-Erweiterung](ui-extensions-c5-data-migration.md)