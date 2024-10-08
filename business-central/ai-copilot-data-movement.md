---
title: Copilot-Datenbewegung über geografische Regionen hinweg
description: 'Erfahren Sie, wie Daten, die in Copilot-Features verwendet werden, in Dynamics 365 Business Central über geografische Regionen hinweg verschoben werden, in denen der Azure OpenAI Dienst nicht standardmäßig verfügbar ist.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 04/16/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: 7775
---

# <a name="copilot-data-movement-across-geographies"></a>Copilot-Datenbewegung über geografische Regionen hinweg

Copilot ist in allen unterstützten [Ländern/Regionen von Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) verfügbar. Copilot verwendet jedoch den Microsoft Azure OpenAI-Dienst, der derzeit nur in einigen geografischen Regionen für Business Central verfügbar ist. Das bedeutet, dass, wenn sich Ihre Umgebung an einem anderen Ort befindet, Daten von den Copilot- und generativen KI-Features außerhalb Ihrer geografischen Region übertragen werden müssen und möglicherweise außerhalb Ihrer Compliance-Grenzen verarbeitet und gespeichert werden. Zu den Daten gehören die KI-Eingabeaufforderungen und Ihre Geschäftsdaten, die von Copilot verwendet oder generiert werden. In diesem Fall müssen Sie sich dafür entscheiden, die Datenverschiebung im Azure OpenAI Dienst in einer anderen Region zuzulassen. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Wenn sich Ihre Umgebung in derselben Azure-Region wie der Azure OpenAI-Dienst befindet, wird automatisch eine Verbindung zum Azure OpenAI-Dienst hergestellt. Es gibt keine Option und es ist keine einmalige Konfiguration erforderlich.

> [!NOTE]
> Einzelne Copilot- und generative KI-Features sind möglicherweise nicht in allen Ländern/Regionen von Business Central verfügbar. Wenden Sie sich an den Herausgeber der einzelnen Funktionen, um die Verfügbarkeit zu erfahren.
> 
> Copilot- und generative KI-Features von anderen Herausgebern als Microsoft, z. B. solche, die aus Anpassungen oder AppSource-Apps stammen, die Sie installieren, legen ihre eigenen spezifischen Azure OpenAI Dienstregionen fest. Wenden Sie sich an den Herausgeber der Erweiterung, um zu erfahren, welche regionalen Azure-Dienste von der Erweiterung verwendet werden. 

### <a name="azure-openai-service-geographies"></a>Azure OpenAI Dienstregionen

Die folgende Tabelle zeigt die von Copilot verwendete geografische Region des Azure OpenAI-Dienstes an, basierend auf der Azure-Region einer Business Central-Umgebung. Diese Informationen sind wichtig, wenn Sie entscheiden, ob Sie der standortübergreifenden Datenübermittlung zustimmen. Sie können die Azure-Region für Ihre Umgebung im Business Central Admin Center herausfinden (siehe [Verwalten von Umgebungen im Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Azure-Region der Umgebung| Geografische Region des Azure OpenAI Diensts|Zum Entsperren von Copilot ist eine Administratoraktion erforderlich| 
| - | - | - |
|Asien (Osten, Südosten) |Vereinigte Staaten|Ja|
|Australien (Südosten)| Australien |Nein |
|Brasilien (Süden) |Vereinigte Staaten|Ja|
|Kanada (Mitte, Osten)|Vereinigte Staaten|Ja|
|Europa (Westen, Norden)| Schweden oder Schweiz |Nein\*|
|Frankreich (Mitte, Süden)| Schweden oder Schweiz |Ja|
|Deutschland (Norden, Westen-Mitte)| Schweden oder Schweiz |Ja|
|Indien (Mitte, Süden)|Indien|Nein|
|Japan (Osten, Westen)|Vereinigte Staaten|Ja|
|Korea (Mitte, Süden)|Vereinigte Staaten|Ja|
|Norwegen (Osten, Westen)|Schweden oder Schweiz |Ja|
|Südafrika (Norden, Westen)|Vereinigte Staaten|Ja|
|Schweiz (Norden, Westen) |Schweden oder Schweiz |Ja|
|Vereinigte Arabische Emirate (Norden, Westen)|Vereinigte Staaten|Ja|
|Vereinigtes Königreich (Süden, Westen)|Vereinigtes Königreich|Nein|
|Vereinigte Staaten (Mitte, Osten, Norden-Mitte, Süden-Mitte, Westen) |Vereinigte Staaten|Nein|

\* Für Umgebungen in den Azure-Regionen Westeuropa und Nordeuropa aktiviert Business Central automatisch die Datenverschiebung über geografische Grenzen hinweg, Administrierende können sich jedoch jederzeit dafür entscheiden, sich abzumelden.

> [!NOTE]
> Sobald ein Azure OpenAI Dienst in Ihrer Business Central-Region verfügbar wird, wird Ihre Umgebung automatisch auf die Verwendung des Azure OpenAI Dienstes umgestellt und eine Anmeldung ist weder erforderlich noch möglich.


## <a name="next-steps"></a>Nächste Schritte

Sie stimmen auf der Seite [Copilot- und KI-Funktionen](https://businesscentral.dynamics.com/?page=7775) zu (oder verweigern die Zustimmung), Datenverschiebungen über geografische Regionen hinweg zuzulassen. Weitere Informationen finden Sie unter [Datenverschiebung über geografische Regionen hinweg zulassen](enable-ai.md#allow-data-movement-across-geographies).
