---
title: Basic Experience-Erweiterung | Microsoft Docs
description: Diese Erweiterung ist eine modernisierte Alternative zu Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 11/10/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Die Basic Experience-Erweiterung

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Wenn Sie bisher Microsoft Dynamics C5 verwendet haben, können Microsoft-Partner Ihnen beim Übergang zu einer moderneren Lösung helfen, die auf [!INCLUDE[prod_short](includes/prod_short.md)] basiert. So können Sie weiterhin dieselben optimierten Funktionen wie in Dynamics C5 nutzen.

Diese Erweiterung ist für kleine Unternehmen gedacht und kann bis zu drei Benutzer unterstützen. Wenn Sie mehr Benutzende benötigen, müssen Sie ein Upgrade auf eine [!INCLUDE[prod_short](includes/prod_short.md)]-Lizenz durchführen und diese Erweiterung deinstallieren.

> [!NOTE]
> Derzeit ist diese Erweiterung nur für Kunden in Dänemark und Island verfügbar.

## Was ist verfügbar

In der folgenden Tabelle werden die Funktionen beschrieben, die verfügbar sind, wenn Sie die Basic Experience-Erweiterung installieren.

|Region  |Funktionalität  |
|---------|---------|
|**Sachposten** |Grundlegende Finanzen, Finanzberichte, Anlagen, Bankverwaltung, Bankabstimmung, Zahlungen, Lastschrift, Dimensionen, mehrere Währungen, Budgets, Workflow, Dokumentverwaltung/OCR, Konsolidierung, unbegrenzte Unternehmen|
|**Debitoren/Vertrieb** |Grundlegende Forderungen, Verkaufsfakturierung, Verkaufsrabatte, Preisberechnung, Umsatzsteuer, Kontaktverwaltung |
|**Kreditoren/Einkauf** |Grundlegende Verbindlichkeiten, Einkaufsfakturierung |
|**Projektmanagement** |Projekte, Projektpreisberechnung, Arbeitszeitnachweise, Zuweisungen, Aufgaben, Ressourcen |
|**Lager** |Grundlegender Lagerbestand, Artikelersetzungen, Artikelquerverweis |

## Erste Schritte

Diese Erweiterung unterscheidet sich ein wenig von den meisten anderen und Sie benötigen Hilfe von einem Microsoft-Partner, um sie zu installieren und einzurichten. Damit Sie wissen, was Sie erwartet, finden Sie hier eine allgemeine Übersicht darüber, was der Microsoft-Partner tut.

1. Erstellen eines neuen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten. Dies kann entweder eine Testversion oder eine Cloud Solution Provider (CSP)-Version sein.
2. Fügen Sie mindestens einen Benutzer hinzu, der einer Basic Experience-Lizenz in Ihrem Microsoft Entra-Konto zugewiesen wird.
3. Entfernen Sie alle Unternehmen, einschließlich des Beispielunternehmens Cronus.
4. Erstellen Sie ein neues Unternehmen, das keine Beispieldaten oder Einrichtungen enthält.
5. Fügen Sie das **Demo-RapidStart**-Paket hinzu. <!--what does the package contain?-->
6. Laden Sie die Basic Experience-Erweiterung von AppSource herunter und installieren Sie sie.

## Migrieren von Daten

Bringen Sie Ihre Dynamics C5-Daten mit. Nachdem Ihr Microsoft-Partner die Basic Experience-Erweiterung installiert hat, haben Sie ein leeres Unternehmen. Eine einfache Möglichkeit, Ihre Daten von Dynamics C5 nach Basic Experience zu verschieben, ist die Verwendung der C5-Datenmigrations-Erweiterung, die in [!INCLUDE[prod_short](includes/prod_short.md)] enthalten ist. Die Erweiterung migriert Kunden, Kreditoren, Artikel und Ihre Sachkonten sowie deren Posten.

## Siehe auch

[Die C5-Datenmigrations-Erweiterung](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
