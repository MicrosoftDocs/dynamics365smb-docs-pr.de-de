---
title: KI-gestützten Marketingtext für Artikel (Vorschauversion) mit Copilot konfigurieren
description: 'In diesem Artikel wird erläutert, wie Sie eine Copilot-Testversion von Business Central erhalten und Copilot in einer Umgebung aktivieren.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# KI-gestützten Marketingtext für Artikel (Vorschauversion) mit Copilot konfigurieren

[!INCLUDE[ai-preview](includes/ai-preview.md)]

In diesem Artikel wird erläutert, wie Sie die Möglichkeit steuern können, KI-gestützte Marketingtexte für Artikel mit Copilot für Ihr Unternehmen zu erstellen. Diese Aufgabe wird von einem Administrator ausgeführt. Es gibt zwei Anforderungen, die Sie erfüllen müssen, um die Funktion für Benutzende verfügbar zu machen:

- Aktivieren Sie das Feature **Erstellen Sie KI-unterstützte Produktbeschreibungen mit Copilot**.
- Stimmen Sie für Ihre Organisation den Nutzungsbedingungen der [Vorschauversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) und den [Microsoft-Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=521839) zu.

Wenn eine dieser Anforderungen nicht erfüllt ist, steht das Feature nicht zur Verfügung.

## Voraussetzungen

Sie verwenden eine [Vorschauversion](ai-preview-getstarted.md) von Business Central, die für Copilot aktiviert ist. Die Aktivierung von Copilot erfolgt durch einen Administrator. Weitere Informationen finden Sie unter [KI-gestützten Marketingtext für Artikel mit Copilot konfigurieren](enable-ai.md).

## Aktivieren oder deaktivieren Sie das Erstellen von KI-unterstützten Produktbeschreibungen mit Copilot

1. Suchen und öffnen Sie in Business Central die Seite **Funktionsverwaltung**.
2. Legen Sie die Spalte **Aktiviert für** für **Feature-Vorschauversion: Erstellen Sie KI-unterstützte Produktbeschreibungen mit Copilot** auf **Alle Benutzer** fest, um das Feature zu aktivieren, oder auf **Keiner**, um es zu deaktivieren.

   Weitere Informationen zur Funktionsverwaltung im Allgemeinen finden Sie unter [Funktionsverwaltung](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Den Nutzungsbedingungen für die Vorschauversion und den Datenschutzbestimmungen für alle Benutzende zustimmen oder sie ablehnen

1. Suchen Sie in Business Central nach der Seite **Status der Datenschutzhinweise** und öffnen Sie sie.
2. Wählen Sie in der Spalte **Integrationsname** **Azure OpenAI** aus und lesen Sie dann die Ihnen angezeigten Nutzungsbedingungen.
3. Aktivieren Sie in der Zeile **Azure OpenAI** das Kontrollkästchen **Für alle zustimmen**, um zuzustimmen, oder das Kontrollkästchen **Für alle ablehnen**, um abzulehnen.

## Nächste Schritte

Nachdem Sie die Funktion aktiviert und verfügbar gemacht haben, können Sie Copilot für Elemente in Business Central ausprobieren. Gehen Sie zu [Marketingtext zu Artikeln hinzufügen](item-marketing-text.md).  

## Siehe auch

[Überblick über KI-gestützte Marketingtexte für Artikel mit Copilot](ai-overview.md)  
[Mit Copilot Marketingtext für Artikel erstellen](item-marketing-text.md)  
[FAQ zu KI-gestützten Marketingtext für Artikel mit Copilot](ai-faq.md)  
