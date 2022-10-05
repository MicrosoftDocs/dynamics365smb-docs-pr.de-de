---
title: Problembehandlung für automatisierte Workflows
description: Erfahren Sie, wie Sie Probleme mit der Verbindung zwischen Business Central und Power Automate beheben, wenn Sie einen automatisierten Workflow erstellen.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,
ms.date: 08/04/2022
ms.author: edupont
ms.openlocfilehash: 42b9a61f40afda0a50d6c6ec86d9984e53ae9ffb
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585918"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Problembehandlung für automatisierte [!INCLUDE[prod_short](includes/prod_short.md)]-Workflows

Wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] mit Power Automate verbinden, um automatisierte Workflows zu erstellen, werden möglicherweise Fehlermeldungen angezeigt. Dieser Artikel enthält Lösungsvorschläge für auftretende Probleme.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flow wird nicht für alle erstellten oder geänderten Datensätze ausgeführt

### <a name="problem"></a>Problem

Wenn ein Ereignis viele Datensätze erstellt oder ändert, wird der Flow für einige oder alle Datensätze nicht ausgeführt.

### <a name="possible-cause"></a>Mögliche Ursache

Derzeit ist die Anzahl der Datensätze, die ein Flow verarbeiten kann, begrenzt. Wenn mehr als 100 Datensätze innerhalb von 30 Sekunden erstellt oder geändert werden, wird der Flow nicht ausgelöst.

> [!NOTE]
> Für Entwickler erfolgt die Flow-Auslösung über Webhook-Benachrichtigungen, und diese Einschränkung ist darauf zurückzuführen, wie der Business Central-Konnektor `collection`-Benachrichtigungen handhabt. Weitere Informationen finden Sie unter [Mit Webhooks in Dynamics 365 Business Central arbeiten](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) in der Hilfe für Entwickler und die Verwaltung.

## <a name="entity-set-not-found-error"></a>Fehler „Entitätenmenge nicht gefunden“

### <a name="problem"></a>Problem

Beim Erstellen eines neuen Power Automate-Flows mit einem [!INCLUDE[prod_short](includes/prod_short.md)]-Genehmigungstrigger wie *Die Genehmigung für einen Einkaufsbeleg wird angefordert* erhalten Sie möglicherweise eine ähnliche Fehlermeldung wie die folgende:

`Entity set not found: \<name\>`

Der Platzhalter `\<name\>` ist der Dienstname des fehlenden Webdienstes, z. B. *workflowWebhookSubscriptions* oder *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Mögliche Ursache

Die Verwendung von Power Automate für Ihre Genehmigungen erfordert, dass bestimmte Seiten- und Codeunit-Objekte als Webdienste veröffentlicht werden. Standardmäßig werden die meisten erforderlichen Objekte als Webdienste veröffentlicht. In einigen Fällen wurde Ihre Umgebung jedoch möglicherweise so angepasst, dass diese Objekte nicht mehr veröffentlicht werden.

### <a name="fix"></a>Beheben

Gehen Sie zur Seite **Webdienste**, und stellen Sie sicher, dass die folgenden Objekte als Webdienste veröffentlicht sind. Für jedes Objekt sollte ein Eintrag in der Liste vorhanden sein, mit aktiviertem Kontrollkästchen **Veröffentlicht**.  

| Objekttyp | Objekt-ID | Objektname | Dienstname |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Seite | 6408 | workflowCustomers | workflowCustomers |
| Seite | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Seite | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Seite | 6409 | workflowItems | workflowItems |
| Seite | 6405 | Entität „EK-Belegzeilen“ | workflowPurchaseDocumentLines |
| Seite | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Seite | 6403 | Entität „VK-Belegzeilen“ | workflowSalesDocumentLines |
| Seite | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Seite | 6410 | workflowVendors | workflowVendors |
| Seite | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Der Wert **Dienstname** muss genau wie in der Tabelle angegeben sein. Ändern oder übersetzen Sie den Dienstnamen nicht.

Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

## <a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/learn/modules/use-power-automate/).

## <a name="see-also"></a>Siehe auch

[Power Automate-Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)verwenden  
[Workflow](across-workflow.md)  
[Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Schalten Sie Direktflows ein](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Power Automate-Flows verwalten](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
