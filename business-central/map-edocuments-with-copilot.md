---
title: E-Belege mit Copilot Bestellpositionen zuordnen
description: 'Erfahren Sie, wie Sie mit Copilot E-Belege den Bestellpositionen zuordnen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 02/23/2024
ms.custom: bap-template
---

# E-Belege mit Copilot Bestellpositionen zuordnen (Vorschauversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Da Beschaffungsprozesse zunehmend digitalisiert werden, spielt die E-Belegsfunktion in Business Central eine Schlüsselrolle bei der Automatisierung des Empfangs und der Verarbeitung von Kreditorenrechnungen. Copilot kann diesen Prozess unterstützen, indem er die Zuordnung und den Abgleich von Kreditorenrechnungen mit Bestellungen verbessert. Dadurch werden zeitaufwändige Aufgaben reduziert, die normalerweise umfangreiche Such-, Nachschlage- und Dateneingabevorgänge umfassen würden. Der Vorteil wird durch die Tatsache verstärkt, dass sich Kreditorenrechnungen häufig nicht genau auf Bestellungen beziehen. In diesem Fall ist Copilot besser in der Lage, die entsprechenden Bestellungen zu identifizieren. Von den erweiterten Abgleichsfunktionen profitieren insbesondere kleine und mittlere Unternehmen, die eine effiziente Belegverfolgung für Bestellpositionen benötigen. Copilot ist der KI-gestützte Arbeitsassistent, der die Kreativität fördert und die Produktivität von Business Central-Benutzenden verbessert.

> [!IMPORTANT]
> - Dies ist eine produktionsbereite Vorschaufunktion für Produktions- und Sandbox-Umgebungen in allen Länderlokalisierungen, mit Ausnahme von Kanada.
> - Für produktionsbereite Vorschaufunktionen gelten die ergänzenden Nutzungsbedingungen. Weitere Informationen: [Ergänzende Nutzungsbedingungen für die Dynamics 365-Vorschauversion](https://go.microsoft.com/fwlink/?linkid=2105274)
> - KI-generierte Inhalte können fehlerhaft sein.

In der ersten Version der App **E-Beleg** haben wir grundlegende Szenarien für E-Belege für den gesamten Verkaufsprozess vorgestellt. Allerdings besteht Bedarf an Verbesserungen und Automatisierung im Umgang mit den empfangenen Belegen, insbesondere im Rahmen von Einkaufsprozessen. Copilot verfeinert die Verwaltung von E-Belegen im Kaufprozess, insbesondere im Hinblick auf Bestellungen. Mit dem E-Belegs-Framework können Sie die Art des Einkaufsbelegs angeben, das für jeden Kreditoren erstellt werden soll, wenn Sie E-Rechnungen von ihm erhalten. Bisher bestand die einzige Möglichkeit darin, eine Einkaufsrechnung entweder als Beleg oder als Fibu.-Buch.-Blatt zu erstellen.

Sie können jetzt eine vorhandene Bestellung in Business Central mit den in der E-Rechnung erhaltenen Informationen aktualisieren.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->


## Bestellungen ermitteln

Zunächst können Sie die Bestellungen ermitteln, die Sie automatisch zuordnen können.

## Positionen zuordnen

Copilot hilft Ihnen, E-Rechnungszeilen automatisch mit Bestellpositionen abzugleichen und bietet zusätzliche Zuordnungsintelligenz, um die Übereinstimmungen zu verbessern.

Nachdem sie abgeglichen und zugeordnet wurden, aktualisiert Business Central die abgeglichene Bestellung mit den relevanten Empfangsinformationen, um sicherzustellen, dass die richtigen Mengen in den Bestellpositionen eingehen.

## Siehe auch

[Überblick über E-Belege](finance-edocuments-overview.md)  
[E-Belege bei Verkäufen und Einkäufen verwenden](finance-how-use-edocuments.md)  
[Probleme mit Copilot- und KI-Funktionen behandeln](ai-copilot-troubleshooting.md)  
[Häufig gestellte Fragen zur verantwortungsbewussten KI bei Unterstützung bei Bankkontoabstimmung](faqs-bank-reconciliation.md)  
