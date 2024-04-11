---
title: Copilot- und KI-Funktionen konfigurieren
description: 'In diesem Artikel wird erläutert, wie Sie Copilot in einer Umgebung aktivieren.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 02/27/2024
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# <a name="configure-copilot-and-ai-capabilities"></a>Copilot- und KI-Funktionen konfigurieren

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

In diesem Artikel wird erläutert, wie Sie Copilot und andere KI-Funktionen in Business Central steuern. Diese Aufgabe wird von einem Administrator erledigt. Copilot ist eine Systemfunktion und integraler Bestandteil von Business Central. Ähnlich wie bei den meisten Systemfunktionen gewähren Sie einzelnen Benutzern keinen Zugriff und können Copilot auch nicht ein- oder ausschalten. Copilot bietet jedoch Datenverwaltungskontrollen und die Möglichkeit, einzelne Copilot- und KI-Funktionen für jede Umgebung zu deaktivieren. Abhängig von der Funktion gibt es unterschiedliche Ebenen der Zugriffskontrolle auf KI-Funktionen:

- Datenverschiebung über geografische Regionen hinweg erlauben.

  Diese Aufgabe ist nur erforderlich, wenn sich Ihre Business Central-Umgebung in einer anderen Region befindet als der Azure OpenAI Dienst, den sie verwendet. [Weitere Informationen](#allow-data-movement-across-geographies)

- Aktivieren Sie das Feature auf der Seite **Copilot- und KI-Funktionen**. [Weitere Informationen](#activate-features)

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Wenn eine dieser Anforderungen nicht erfüllt ist, steht das Feature nicht zur Verfügung.-->

## <a name="prerequisites"></a>Voraussetzungen

- Sie verwenden Business Central Online <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Sie verfügen über Administrator- oder Superuserberechtigungen in Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Datenverschiebung über geografische Regionen hinweg zulassen

Diese Aufgabe gilt nur, wenn der Umschalter **Datenverschiebung zulassen** oben auf der Seite **Copilot- und KI-Funktionen** erscheint. Wenn anstelle des Umschalters **Datenverschiebung zulassen** der Link **Wie kann ich meine Copilot-Daten verwalten?** angezeigt wird, überspringen Sie diesen Schritt.

![Zeigt einen Screenshot des Umschalters „Datenverschiebung zulassen“ auf der Seite „Copilot und KI-Fähigkeiten“.](media/allow-data-movement-v2.png)

Der Umschalter **Datenverschiebung zulassen** gibt an, dass sich der Standort Ihrer Business Central-Umgebung – also die Region, in der Daten verarbeitet und gespeichert werden – nicht dieselbe ist wie die von Copilot verwendete Region für den Azure OpenAI-Dienst. Wenn Sie Copilot aktivieren möchten, müssen Sie die Datenverschiebung zwischen Regionen zulassen. Weitere Informationen zur Datenverschiebung finden Sie unter [Copilot-Datenverschiebung über geografische Regionen hinweg](ai-copilot-data-movement.md). 

Um die Datenverschiebung außerhalb Ihrer geografischen Region zuzulassen, gehen Sie wie folgt vor:

1. Suchen Sie in Business Central nach der Seite **Copilot- und KI-Funktionen** und öffnen Sie sie.
1. Aktivieren Sie den Umschalter **Datenverschiebung zulassen**.

   Der Umschalter **Datenverschiebung zulassen** ist für Umgebungen in den Azure-Regionen Westeuropa und Nordeuropa standardmäßig aktiviert.

Sie können die Datenverschiebung abwählen, indem Sie den Umschalter **Datenverschiebung zulassen** ausschalten. Sobald ein Azure OpenAI Dienst in der geografischen Region Ihrer Business Central-Umgebung verfügbar wird, wird Ihre Umgebung automatisch damit verbunden und der Umschalter ist nicht mehr verfügbar.

<!-- Don't review
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->

## <a name="activate-features"></a>Features aktivieren

Alle Copilot- und KI-Funktionen sind standardmäßig aktiv, wenn sie als Vorschauversion verfügbar gemacht werden oder allgemein verfügbar werden. Mit der Seite **Copilot- und KI-Funktionen** können Sie einzelne Features für alle Benutzenden deaktivieren oder wieder aktivieren.

1. Suchen Sie in Business Central nach der Seite **Copilot- und KI-Funktionen** und öffnen Sie sie.

1. Die Seite listet alle verfügbaren Copilot- und KI-bezogenen Features und ihren aktuellen Status auf, der entweder aktiv oder inaktiv sein kann. Die Features sind in zwei Abschnitte unterteilt – ein Abschnitt für Features in der Vorschau und ein anderer für allgemein verfügbare Features. 

   [![Zeigt das Business Central-Rollencenter und die Checkliste für Copilot an](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Um ein Feature zu aktivieren, wählen Sie es in der Liste aus und wählen Sie dann die Aktion **Aktivieren** aus.
   - Um ein Feature zu deaktivieren, wählen Sie es in der Liste aus und wählen Sie dann die Aktion **Deaktivieren** aus. 

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Gewähren von Benutzerzugriff

Copilot- und KI-Funktionen können Funktionen bieten, die für alle Benutzenden in Ihrer Organisation oder für bestimmte Benutzerrollen gedacht sind. Die meisten Copilot- und KI-Funktionen bieten Zugriffskontrolle mithilfe von Berechtigungen und Berechtigungssätzen im Berechtigungsverwaltungssystem von Business Central. [Erfahren Sie mehr über Berechtigungen und Berechtigungssätze](ui-define-granular-permissions.md).

Die folgenden Tabelle zeigen die Berechtigungen, die für die Nutzung der von Business Central bereitgestellten Copilot-Features erforderlich sind.

|Copilot-Features|Erforderliche Berechtigungen|
|-|-|
|Analyseunterstützung|Berechtigungssatz **DATENANALYSE – AUSFÜHREN** oder Ausführungsberechtigung für das Systemobjekt 9640 **Datenanalysemodus zulassen**. Dies sind die gleichen Berechtigungen, die auch für den Zugriff auf den Analysemodus erforderlich sind.|
|Unterstützung bei der Bankkontoabstimmung|Berechtigung auf Seite 7250 **Bankkontoabstimmungs-KI-Vorschlag** und Seite 7252 **Übertr. KI-Vorschlag auf Fibu-Konto**.|
|Chat |Es gibt keine Berechtigungen oder Berechtigungssätze, die den Zugriff auf den Chat auf Benutzerbasis steuern. Wenn der Chat aktiviert ist, steht er allen Benutzenden zur Verfügung.|
|Vorschläge für Marketingtexte |Berechtigung auf Seite 5836 **Copilot-Marketingtext**|

Um den Zugriff auf bestimmte, nicht von Microsoft stammenden Copilot- und KI-Funktionen zu gewähren oder zu verweigern, konsultieren Sie die Dokumentation oder den Herausgeber dieses Features, um herauszufinden, welche Berechtigungen erforderlich sind.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie die Features aktiviert und ihnen zugestimmt haben, können Sie sie ausprobieren. Gehen Sie zu:

- [Marketingtext zu Artikeln hinzufügen](item-marketing-text.md)
- [Daten mit Copilot im Analysemodus analysieren](analysis-assist.md)  
- [Chat mit Copilot](chat-with-copilot.md)
- [Abstimmung mithilfe der Unterstützung bei Bankkontoabstimmung](bank-reconciliation-with-copilot.md)

## <a name="see-also"></a>Siehe auch

[Probleme mit Copilot- und KI-Funktionen beheben](ai-copilot-troubleshooting.md)  
[Häufig gestellte Fragen zur Analyseunterstützung](faqs-analysis-assist.md)  
[Häufig gestellte Fragen zur Unterstützung bei Bankkontoabstimmung](faqs-bank-reconciliation.md)  
[Häufig gestellte Fragen zum Chat mit Copilot](faqs-chat-with-copilot.md)  
[Häufig gestellte Fragen zu Vorschlägen für Marketingtexte](faqs-marketing-text.md)  
[Überblick über Vorschläge für Marketingtexte](ai-overview.md)  
