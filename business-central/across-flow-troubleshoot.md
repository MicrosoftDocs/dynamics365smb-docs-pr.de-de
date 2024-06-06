---
title: Probleme bei automatisierten Workflows beheben
description: 'Erfahren Sie, wie Sie Probleme mit der Verbindung zwischen Business Central und Power Automate beheben, wenn Sie einen automatisierten Workflow erstellen.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 12/13/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---

# <a name="troubleshoot-your--automated-workflows"></a>Probleme mit automatisierten [!INCLUDE[prod_short](includes/prod_short.md)] Workflows beheben

Wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] mit Power Automate verbinden, um automatisierte Workflows zu erstellen, werden möglicherweise Fehlermeldungen angezeigt. Dieser Artikel enthält Lösungsvorschläge für auftretende Probleme.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flow wird nicht für alle erstellten oder geänderten Datensätze ausgeführt

### <a name="problem"></a>Problem

Wenn ein Ereignis viele Datensätze erstellt oder ändert, wird der Flow für einige oder alle Datensätze nicht ausgeführt.

### <a name="possible-cause"></a>Mögliche Ursache

Derzeit ist die Anzahl der Datensätze, die ein Flow verarbeiten kann, begrenzt. Wenn mehr als 1000 Datensätze innerhalb von 30 Sekunden erstellt oder geändert werden, wird der Flow nicht ausgelöst.

> [!NOTE]
> Für Entwickler erfolgt die Flow-Auslösung über Webhook-Benachrichtigungen, und diese Einschränkung ist darauf zurückzuführen, wie der Business Central-Konnektor `collection`-Benachrichtigungen handhabt. Weitere Informationen finden Sie unter [Mit Webhooks in Dynamics 365 Business Central arbeiten](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) in der Hilfe für Entwickler und die Verwaltung.

## <a name="the-response-from-the-business-central-service-is-too-large-error"></a>Fehler „Die Antwort des Business Central-Diensts ist zu groß“

### <a name="problem-1"></a>Problem

Bei Verwendung einer Aktion, die mit Datensätzen interagiert (z. B. *Datensatz erstellen [V3]* und *Datensatz abrufen [V3]*) zeigt Power Automate möglicherweise einen Fehler ähnlich diesem an:

`The response from the Business Central service is too large`

### <a name="possible-cause-1"></a>Mögliche Ursache

Auch wenn in Business Central keine Beschränkung für die Größe der von APIs zurückgegebenen Datensätze festgelegt ist, kann der Dynamics 365 Business Central Connector für Power Automate nur Datensätze bis zu 8 MB verarbeiten.

Alle von Microsoft bereitgestellten Business Central-APIs geben Datensätze unter diesem Grenzwert zurück, von Partnern bereitgestellte APIs jedoch möglicherweise nicht. Wenn die Fehlermeldung „Die Antwort des Business Central-Dienstes ist zu groß“ angezeigt wird, wenden Sie sich an den Partner, der die von Ihnen verwendete API erstellt hat.

## <a name="entity-set-not-found-error"></a>Fehler „Entitätenmenge nicht gefunden“

### <a name="problem-2"></a>Problem

Beim Erstellen eines neuen Power Automate-Flows mit einem [!INCLUDE[prod_short](includes/prod_short.md)]-Genehmigungstrigger wie *Die Genehmigung für einen Einkaufsbeleg wird angefordert* erhalten Sie möglicherweise eine ähnliche Fehlermeldung wie die folgende:

`Entity set not found: \<name\>`

Der Platzhalter `\<name\>` ist der Dienstname des fehlenden Webdienstes, z. B. *workflowWebhookSubscriptions* oder *workflowPurchaseDocumentLines*.

### <a name="possible-cause-2"></a>Mögliche Ursache

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

## <a name="see-also"></a>Siehe auch

[Power Automate-Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)verwenden  
[Workflow](across-workflow.md)  
[Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Schalten Sie Direktflows ein](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Power Automate-Flows verwalten](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
