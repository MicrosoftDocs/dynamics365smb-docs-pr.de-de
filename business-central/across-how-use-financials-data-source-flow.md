---
title: Power Automate-Flows in Business Central verwenden
description: 'Richten Sie Power Automate-Flows zum Erstellen ode Ändern von Business Central-Daten ein, und verwenden Sie sie.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 10/10/2022
ms.custom: bap-template
---
# <a name="use-power-automate-flows-in-"></a><a name="use-power-automate-flows-in-"></a>Power Automate-Flows in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden

Mit [!INCLUDE[prod_short](includes/prod_short.md)] erhalten Sie eine Lizenz für Microsoft Power Automate. Mit dieser Lizenz können Sie Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten als Teil eines Workflows in Microsoft Power Automate verwenden. Sie erstellen Flows und stellen über den [!INCLUDE [prod_short](includes/prod_short.md)]-Konnektor eine Verbindung zu Ihren Daten aus internen und externen Quellen her.

Power Automate-Flows werden durch Ereignisse ausgelöst, z.B. wenn ein Datensatz erstellt, geändert oder gelöscht wurde. Sie können auch nach einem benutzerdefinierten Zeitplan oder bei Bedarf ausgeführt werden.

> [!NOTE]
> Administratoren können den Zugriff auf Power Automate einschränken. Wenn Sie feststellen, dass Sie keinen Zugriff auf einige oder alle der in diesem Artikel beschriebenen Funktionen haben, wenden Sie sich an Ihren Admin. Wenn Sie erfahren möchten, wie Sie als Admin den Zugriff auf Power Automate festlegen können, lesen Sie [Einrichten der Power Automate-Integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Zusätzlich zu Power Automate können Sie die Vorlagen für Genehmigungsworkflow in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Obwohl es zwei verschiedene Workflowsysteme sind, wird jede Vorlage für Genehmigungsworkflows, die Sie mit Power Automate erstellen, der Liste von Workflows in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Erfahren Sie mehr unter [Workflows](across-workflow.md).

## <a name="about-power-automate-flows"></a><a name="about-power-automate-flows"></a>Über Power Automate Flows

Power Automate ist ein Dienst, mit dem Sie automatisierte Workflows (oder Flows) zwischen Apps und Diensten erstellen können, wie [!INCLUDE[prod_short](includes/prod_short.md)]. Power Automate Flows erfordern wenig oder gar keine Programmierkenntnisse. Sie können mit einer Vielzahl von Ereignissen und Reaktionen verknüpft werden, z.B:

- Änderungen eines Datensatzes
- Aktualisierungen externer Dateien
- Eingestellte Dokumente
- Verschiedene Dienste von Microsoft und Drittanbietern, wie Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps, und mehr.

Es gibt drei verschiedene Cloud-Flow-Typen, mit denen Sie arbeiten können:

|Flow-Typ|Description|
|---------|-----------|
|Automatisiert|Dieser Flow-Typ wird automatisch durch ein Ereignis ausgeführt. In [!INCLUDE[prod_short](includes/prod_short.md)] könnte ein Ereignis sein, wenn ein Datensatz oder ein Dokument erstellt, geändert oder gelöscht wird. So kann z.B. eine neue Verkaufsrechnung einen Flow für eine Genehmigungsanfrage auslösen, für die je nach Antwort des Genehmigers unterschiedliche Ereignisse festgelegt werden können. Bei einer negativen Antwort werden eine Benachrichtigung und eine E-Mail an den Genehmigungsanfragenden gesendet. Eine positive Antwort aktualisiert gleichzeitig eine Excel-Tabelle, die sich in einem SharePoint-Ordner befindet, und sendet ein Update an einen Teams-Chat. Automatisierte Flows können sowohl durch interne als auch durch externe Ereignisse in [!INCLUDE[prod_short](includes/prod_short.md)] gestartet werden.|
|Terminiert|Diese Art von Flows wird ebenfalls automatisch ausgeführt, allerdings periodisch zu einem bestimmten Datum und einer bestimmten Uhrzeit. |
|Sofort |Dieser Flow-Typ wird bei Bedarf ausgeführt, d.h. der Benutzer muss ihn manuell über eine Schaltfläche oder Aktion in einer anderen App oder einem anderen Gerät, in diesem Fall dem [!INCLUDE[prod_short](includes/prod_short.md)]-Client, ausführen. Instant Flows funktionieren ähnlich wie Batch-Verknüpfungen, führen mehrere langwierige Schritte mit ein paar Tastendrücken aus und werden von bestimmten Seiten oder Tabellen aus gestartet. Beispielsweise kann ein Flow eine Schaltfläche zum Aktionsmenü auf der Seite **Anbieter** hinzufügen, um Zahlungen an einen Lieferanten zu blockieren und gleichzeitig anpassbare E-Mails an den Kontakt des Lieferanten und die Einkäufer Ihres Unternehmens zu senden sowie den Kontakt in Outlook zu aktualisieren. |

## <a name="power-automate-features"></a><a name="power-automate-features"></a>Power Automate-Funktionen

Sie können sich alle Power Automate Flows ansehen, die Ihnen derzeit zur Verfügung stehen, indem Sie sich bei [Power Automate](https://powerautomate.com) anmelden und **Meine Flows** aus der Navigationsleiste auf der linken Seite auswählen. Hier finden Sie alle Flows, die Sie bereits selbst erstellt haben, sowie Flows, die Ihnen von einem Admin oder einem Mitarbeiter zur Verfügung gestellt wurden.

- Direktflows werden auch für die direkte Ausführung von den meisten Listen-, Karten- und Dokumentseiten in [!INCLUDE[prod_short](includes/prod_short.md)] zur Verfügung gestellt. Sie finden die Direktflows in der Aktionsgruppe **Automatisieren** in der Aktionsleiste der Seiten. Um einen Flow auszuführen, wählen Sie ihn aus und befolgen Sie die angezeigten Anweisungen. Mehr dazu erfahren Sie in den folgenden Abschnitten.
 
- Bei automatisierten Flows in [!INCLUDE[prod_short](includes/prod_short.md)] müssen Sie nichts tun, es sei denn, Sie möchten sie ändern oder deaktivieren. Andernfalls funktionieren sie einfach, wenn sie ausgelöst werden. 
<!--

## <a name="automated-flows"></a><a name="automated-flows"></a>Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows"></a><a name="run-instant-flows"></a>Sofortige Flows ausführen

Direktflows öffnen sich innerhalb von [!INCLUDE [prod_short](includes/prod_short.md)] online, so dass Sie im Kontext des Geschäftsprozesses bleiben können, in dem Sie sich gerade befinden. Sie können einen Instant Flow aus den meisten Listen, Karten oder Dokumenten ausführen.

1. Wählen Sie in der Aktionsleiste **Automatisieren** und wählen Sie dann einen Flow aus der Liste der verfügbaren Flows unter der Aktion **Power Automate**.

    :::image type="content" source="media/power-automate-action-intro.png" alt-text="Zeigt die Aktion Automatisieren in der Aktionsleiste mit erweiterten Aktionen an.":::

    Auf einigen Seiten ist **Automatisieren** unter **Weitere Optionen (...)** verschachtelt. 
2. Füllen Sie im Bereich **Ausführen des Flows** alle erforderlichen Felder aus und wählen Sie dann **Fortfahren**, um den Flow auszuführen.

> [!NOTE]
> Wenn Sie das Element **Automatisieren** zum ersten Mal verwenden, sehen Sie möglicherweise nur die Aktion **Gestartet mit Power Automate**. Sie sehen diese Aktion, weil Sie dem Datenschutzhinweis für Microsoft Power Automate nicht zugestimmt haben. Um fortzufahren, wählen Sie **Beginnen Sie mit Power Automate** und folgen Sie den Anweisungen, um zuzustimmen oder zu widersprechen.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Zeigt das Element Automatisieren in der Aktionsleiste an.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows"></a><a name="create-edit-and-manage-flows"></a>Flows erstellen, bearbeiten und verwalten

Das Erstellen neuer Flows, das Ändern und Verwalten bestehender Flows (wie das Ein- oder Ausschalten) können Sie direkt in Power Automate vornehmen. Einige dieser Aufgaben können Sie jedoch von [!INCLUDE[prod_short](includes/prod_short.md)] aus starten:

- Um einen sofortigen Flow aus einer Liste, einer Karte oder einer Dokumentseite zu erstellen, wählen Sie **Automatisieren** > **Flow erstellen**.
- Um Power Automate von einer Liste, Karte oder Dokumentenseite aus zu öffnen, wählen Sie **Automatisieren** > **Flows verwalten**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Diese Aufgaben werden normalerweise von einem Admin oder Superuser erledigt. Die Aufgaben erfordern ein breiteres Wissen über die Geschäftsprozesse in [!INCLUDE[prod_short](includes/prod_short.md)]. Weitere Informationen finden Sie unter [Power Automate-Integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview), [Direktflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) und [Power Automate-Flows verwalten](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows).
<!-- 

## <a name="add-more-automated-flows-and-instant-flows"></a><a name="add-more-automated-flows-and-instant-flows"></a>Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## <a name="create-and-manage-power-automate-flows"></a><a name="create-and-manage-power-automate-flows"></a>Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/use-power-automate/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Problembehandlung für automatisierte [!INCLUDE[prod_short](includes/prod_short.md)]-Workflows](across-flow-troubleshoot.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Workflows](across-workflow.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] einrichten](setup.md)  
[Finanzen](finance.md)  
[Power Automate-Flows verwalten](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Schalten Sie Direktflows ein](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
A
