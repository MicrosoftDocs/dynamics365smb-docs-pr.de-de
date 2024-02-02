---
title: Probleme mit Copilot- und KI-Funktionen behandeln
description: 'Erfahren Sie, wie Sie häufige Probleme beheben, die bei der Arbeit mit Copilot- und KI-Funktionen in Business Central auftreten können.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 11/15/2023
ms.custom: bap-template
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Probleme mit Copilot- und KI-Funktionen behandeln

Copilot ist eine KI-gestützte Funktion in Business Central, die Sie bei verschiedenen Aufgaben wie der Erstellung von Marketingtexten und dem Abgleich von Bankkonten unterstützt. Wenn Sie Probleme mit Copilot oder anderen KI-Funktionen haben, kann Ihnen dieser Artikel dabei helfen, häufige Probleme zu identifizieren und zu beheben.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot erscheint nicht auf Seiten

Wenn Copilot-Funktionalität, wie die Aktion **Mit Copilot entwerfen** für Marketingtextvorschläge oder die Aktion **Mit Copilot abgleichen** für die Unterstützung bei Bankkontoabstimmung, nicht wie erwartet auf einer Seite angezeigt wird, überprüfen Sie Folgendes:

- Wenn die Funktion unter „Funktionsverwaltung“ gesteuert wird, stellen Sie sicher, dass sie aktiviert ist. [Weitere Informationen finden Sie unter Funktionsverwaltung](admin-feature-management.md).

- Stellen Sie sicher, dass die Funktionalität nicht durch die Personalisierung verdeckt wird. [Weitere Informationen zur Personalisierung](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot erscheint auf Seiten, aber Sie erhalten eine Fehlermeldung, dass es nicht aktiviert ist

Wenn Sie versuchen, Copilot zu verwenden, und eine Fehlermeldung wie **Copilot ist für \[Feature\] leider nicht aktiviert** erhalten, müssen Sie einige Dinge überprüfen:

- Stellen Sie zunächst sicher, dass das Feature auf der Seite **Copilot- und KI-Funktionen** aktiviert ist. [Erfahren Sie mehr über die Aktivierung von Copilot- und KI-Funktionen](enable-ai.md#activate-features). 
- Stellen Sie als Nächstes sicher, dass die Datenschutzerklärung für die Azure OpenAI-Integration nicht auf **Für alle nicht zustimmen** eingestellt ist. Wenn dies der Fall ist, ändern Sie es in **Für alle zustimmen**. [Erfahren Sie mehr über Datenschutzhinweise](privacy-notices-status.md).

## <a name="see-also"></a>Siehe auch

[Copilot- und KI-Funktionen konfigurieren](enable-ai.md)  
[Vorschläge für Marketingtexte mit Copilot](ai-overview.md)  
[Bankkontoabstimmung mit Copilot](bank-reconciliation-with-copilot.md)  
