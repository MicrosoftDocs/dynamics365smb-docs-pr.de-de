---
title: Basic Experience-Erweiterung | Microsoft Docs
description: Diese Erweiterung ist eine modernisierte Alternative zu Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1ddb4468bda648b0368551ecb8cdbc6167cf4778
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381672"
---
# <a name="the-basic-experience-extension"></a>Die Basic Experience-Erweiterung
Wenn Sie bisher Microsoft Dynamics C5 verwendet haben, können Microsoft-Partner Ihnen beim Übergang zu einer moderneren Lösung helfen, die auf [!INCLUDE[prod_short](includes/prod_short.md)] basiert. So können Sie weiterhin dieselben optimierten Funktionen wie in Dynamics C5 nutzen.

Diese Erweiterung ist für kleine Unternehmen gedacht und kann bis zu drei Benutzer unterstützen. Wenn Sie mehr Benutzer benötigen, müssen Sie ein Upgrade auf eine [!INCLUDE[prod_short](includes/prod_short.md)]-Lizenz durchführen und diese Erweiterung deinstallieren.

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

1. Erstellen eines neuen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten. Dies kann entweder eine Testversion oder eine CSP-Version sein.
2. Fügen Sie mindestens einen Benutzer hinzu, der einer Basic Experience-Lizenz in Ihrem Azure Active Directory-Konto zugewiesen wird.
3. Entfernen Sie alle Unternehmen, einschließlich des Beispielunternehmens Cronus.
4. Erstellen Sie ein neues Unternehmen, das keine Beispieldaten oder Setups enthält.
5. Fügen Sie das **Demo-RapidStart**-Paket hinzu. <!--what does the pockage contain?-->
6. Laden Sie die Basic Experience-Erweiterung von AppSource herunter und installieren Sie sie.

## <a name="migrating-data"></a>Migrieren von Daten
Bringen Sie Ihre Dynamics C5-Daten mit. Nachdem Ihr Microsoft-Partner die Basic Experience-Erweiterung installiert hat, haben Sie eine leere Firma. Eine einfache Möglichkeit, Ihre Daten von Dynamics C5 nach Basic Experience zu verschieben, ist die Verwendung der C5-Datenmigrations-Erweiterung, die in [!INCLUDE[prod_short](includes/prod_short.md)] enthalten ist. Die Erweiterung migriert Kunden, Kreditoren, Artikel und Ihre Sachkonten sowie deren Posten.

## <a name="see-also"></a>Siehe auch
[Die C5-Datenmigrations-Erweiterung](ui-extensions-c5-data-migration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]