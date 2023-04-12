---
title: FAQ für technische Details
description: Implementierungsdetails in Bezug auf Shopify Connector
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# FAQ für technische Details

Dieser Artikel beantwortet häufig gestellte Fragen über den Shopify-Konnektor.

## Was ist Shopify?

Shopify ist eine abonnementbasierte Anwendung, die es jedem ermöglicht, einen Onlineshop einzurichten und seine Produkte zu verkaufen. Die Shopify-Plattform bietet Onlinehändlern eine Reihe von Dienstleistungen, wie Zahlungs-, Marketing-, Versand- und Customer Engagement-Tools.

## Was ist der Microsoft Dynamics 365 Business Central Shopify-Konnektor?

Mit dem Shopify-Konnektor können Unternehmen ihren Shopify-Store mit [!INCLUDE[prod_short](../includes/prod_short.md)]verbinden, um die Produktivität Ihres Unternehmens zu maximieren. Mithilfe des Shopify-Konnektors können sie Erkenntnisse aus Ihrem Unternehmen und ihrem Shopify-Onlineshop als eine Einheit verwalten und anzeigen.

### Funktionalitäten

- Unterstützung für mehr als einen Shopify-Shop
  - Jeder Shop verfügt über eine eigene Einrichtung, einschließlich einer Sammlung von Produkten, Standorten zur Bestandsberechnung sowie Preislisten.  
- Bidirektionale Synchronisierung von Artikeln oder Produkten
  - Der Konnektor synchronisiert Bilder, Artikelvarianten, Barcodes, Lieferantenartikelnummern, erweiterte Texte und Tags.  
  - Exportieren Sie Artikelattribute nach Shopify.  
  - Verwenden Sie ausgewählte Debitorenpreisgruppen und Rabatte, um die nach Shopify exportierten Preise zu definieren.  
  - Entscheiden Sie, ob Artikel automatisch erstellt werden können, oder lassen Sie nur Aktualisierungen bestehender Produkte zu.  
- Synchronisierung von Lagerbeständen
  - Wählen Sie einige oder alle verfügbaren Standorte in [!INCLUDE [prod_short](../includes/prod_short.md)] aus.  
  - Aktualisieren Sie die Lagerbestände an mehreren Standorten in Shopify.  
- Bidirektionale Synchronisierung von Debitoren
  - Ordnen Sie Debitoren intelligent per Telefon und E-Mail zu.  
  - Verwenden Sie beim Erstellen von Debitoren länderspezifische Vorlagen, um sicherzustellen, dass die Steuereinstellungen korrekt sind.  
- Aufträge aus Shopify importieren
  - Beziehen Sie Bestellungen ein, die in verschiedenen Vertriebskanälen erstellt wurden, z.B. im Online Store oder **Shopify POS**.
  - Versandkosten, Geschenkgutscheine, Tipps, Versand- und Zahlungsmethoden, Transaktionen und Betrugsrisiko.  
  - Während des Imports können Sie Debitoren automatisch in [!INCLUDE [prod_short](../includes/prod_short.md)] erstellen oder sich dazu entscheiden, diese in Shopify zu verwalten.  
  - Erhalten Sie Auszahlungsinformationen von Shopify Payments.
- Verfolgen Sie Informationen zur Auftragserfüllung
  - Wählen Sie optional, ob Sie Informationen zur Artikelverfolgung von [!INCLUDE [prod_short](../includes/prod_short.md)] nach Shopify übertragen möchten.  

## Warum sind Microsoft und Shopify diese Partnerschaft eingegangen?

[!INCLUDE[prod_short](../includes/prod_long.md)] kooperiert mit Shopify, um unseren Debitoren zu helfen, ein besseres Einkaufserlebnis zu schaffen. Während Shopify Händlern eine benutzerfreundliche Handelslösung zur Verfügung stellt, bietet [!INCLUDE[prod_short](../includes/prod_short.md)] eine umfassende Unternehmensverwaltungslösung für Finanz-, Vertriebs-, Service- und Betriebsteams innerhalb einer einzigen Anwendung. Die nahtlose Verbindung zwischen den beiden Systemen verwenden, um Bestellungen, Bestand und Debitoreninformationen zu synchronisieren, damit Händler Bestellungen schneller ausführen und Debitoren besser bedienen können.

## Für welche Microsoft-Produkte ist der Shopify Konnektor verfügbar?

Diese Funktion ist nur für [!INCLUDE[prod_short](../includes/prod_short.md)] Online, ab Version 20.1, verfügbar. Sie ist nicht für lokale Bereitstellungen verfügbar. Der Konnektor ist für neue Umgebungen vorinstalliert. Organisationen mit bestehenden Umgebungen können den Connector über AppSource herunterladen und installieren. Die Organisation muss sowohl über eine [!INCLUDE [prod_short](../includes/prod_short.md)]-Lizenz als auch über eine Shopify-Lizenz verfügen, um den Konnektor zu verwenden. Weitere Informationen zu unterstützten Ländern, Sprachen und Editionen von [!INCLUDE[prod_short](../includes/prod_short.md)] finden Sie unter [Shopify-Konnektor in AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

Der Shopify Konnektor funktioniert nicht für [App einbetten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), wobei die Client-URL das `https://[application name].bc.dynamics.com` Format hat.

## Welche Unterstützung wird für den Shopify Konnektor angeboten?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

Der Shopify-Konnektor wird durch das aktuelle Supportmodell abgedeckt. Erfahren Sie mehr unter [Technical Support](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (nur in englischer Sprache verfügbar).

Holen Sie sich Hilfe von einem Berater, der den Shopify Konnektor für [!INCLUDE[prod_short](../includes/prod_short.md)] kennt, um Ihre individuellen geschäftsspezifischen Anforderungen zu erfüllen. Suchen Sie unter [Beratungsdienste](https://aka.ms/BCShopifyConsultant).

### Shopify

Um Hilfe zu Shopify zu erhalten, gehen Sie zum [Allgemeines Shopify Help Center](https://help.shopify.com/) oder zum [24/7 Support für Ihren Store als Shopify Händler](https://help.shopify.com/questions#/).

Sie können auch den [Experts Marketplace](https://experts.shopify.com/) erkunden, um die richtigen Experten zu finden, die Dienstleistungen für Shopify-Händler anbieten.

## Diese Funktionen werden aktuell nicht unterstützt, aber wir verfolgen sie und werden sie möglicherweise in der Zukunft hinzufügen

- B2B Funktionen, einschließlich Unternehmen, Preislisten für Unternehmen und Zahlungsbedingungen
- Märkte
  - Mehrere Übersetzungen von Stammdaten. Sie können eine Sprache auswählen, die für den Export von Produktinformationen verwendet werden soll.
  - Preise pro Land/Region. Eine Preisliste ist für die ausgewählte Währung verfügbar. Die Umrechnung in andere Währungen übernimmt Shopify.

## Ist der Shopify Konnektor erweiterbar?

Ja, der Shopify Konnektor ist erweiterbar. Überprüfen Sie GitHub, um auf die [Liste der Erweiterungspunkte](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) zuzugreifen und einige [Beispiele](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md) zu erkunden.

## Ist der Shopify Connector offen für Beitrag

Ja, diese Erweiterung ist offen für Beiträge aus unserer Community. Sie finden den [Quellcode](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) im Repository für Microsoft AL-Anwendungs-Add-Ons.

## Siehe auch

[Erste Schritte mit dem Konnektor für Shopify](get-started.md)  
