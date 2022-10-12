---
title: Power Automate-Flows in Business Central verwenden
description: Richten Sie Power Automate-Flows zum Erstellen ode Ändern von Business Central-Daten ein, und verwenden Sie sie.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 5fe089c0330a8d2b7a71f4907212665722d27d38
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606521"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Power Automate-Flows in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden

Sie können Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten als Teil eines Workflows in Microsoft Power Automate verwenden. Erstellen Sie Ihre eigenen Flows, und stellen Sie eine Verbindung mit Ihren Daten aus externen und internen Quellen mit dem [!INCLUDE [prod_short](includes/prod_short.md)]-Konnektor her.

> [!NOTE]
> Sie müssen ein gültiges Konto bei [!INCLUDE[prod_short](includes/prod_short.md)] und Power Automate haben.  

> [!TIP]
> Zusätzlich zu Power Automate können Sie die Vorlagen für Genehmigungsworkflow in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Obwohl es zwei verschiedene Workflowsysteme sind, wird jede Vorlage für Genehmigungsworkflows, die Sie mit Power Automate erstellen, der Liste von Workflows in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Erfahren Sie mehr unter [Workflows](across-workflow.md).

Power Automate-Flows werden durch Ereignisse wie das Erstellen, Ändern oder Löschen von Datensätzen und Dokumenten ausgelöst (automatisierte Flows). Die Flows können auch nach einem benutzerdefinierten Zeitplan (geplante Flows) oder nach Bedarf (sofortige Flows) ausgeführt werden.

## <a name="power-automate-features-in-prod_short"></a>Power Automate-Features in [!INCLUDE[prod_short](includes/prod_short.md)]

Flows erweitern die integrierten Funktionen für Genehmigungsworkflows, die in [!INCLUDE[prod_short](includes/prod_short.md)] verfügbar sind ohne dass Programmierkenntnisse erforderlich sind, und können mit einer Vielzahl von Ereignissen und Reaktionen verknüpft werden, z. B. Datensatzänderungen, Aktualisierungen externer Dateien, veröffentlichte Dokumente sowie verschiedene Dienste von Microsoft und Drittanbietern wie Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps, und mehr.

So kann beispielsweise eine neue Verkaufsrechnung einen Workflow für eine Genehmigungsanfrage auslösen, für die je nach Antwort des Genehmigers unterschiedliche Ereignisse festgelegt werden können. Bei einer negativen Antwort werden eine Benachrichtigung und eine E-Mail an den Genehmigungsanfragenden gesendet. Eine positive Antwort aktualisiert gleichzeitig eine Excel-Tabelle, die sich in einem SharePoint-Ordner befindet, und sendet ein Update an einen Teams-Chat.

Instant Flows funktionieren ähnlich wie Batch-Verknüpfungen, führen mehrere langwierige Schritte mit ein paar Tastendrücken aus und werden von bestimmten Seiten oder Tabellen aus gestartet. Beispielsweise kann ein Flow eine Schaltfläche zum Aktionsmenü auf der Seite **Anbieter** hinzufügen, um Zahlungen an einen Lieferanten zu blockieren und gleichzeitig anpassbare E-Mails an den Kontakt des Lieferanten und die Einkäufer Ihres Unternehmens zu senden sowie den Kontakt in Outlook zu aktualisieren.

## <a name="automated-workflows"></a>Automatisierte Workflows

Mit Power Automate können Sie Geschäftsabläufe direkt intern erstellen und sich auf Citizen Developer verlassen. Automatisierte Workflows können sowohl durch interne als auch externe Ereignisse in [!INCLUDE[prod_short](includes/prod_short.md)] gestartet werden, und auch so eingestellt werden, dass sie regelmäßig ausgeführt werden. Erfahren Sie mehr und erhalten Sie Anweisungen zum Erstellen von Workflows im Artikel [Richten Sie automatisierte Workflows ein](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) im Verwaltungsinhalt.

## <a name="instant-flows"></a>Direktflows

[!INCLUDE [prod_short](includes/prod_short.md)] kann einen Power Automate Flow von den meisten Listen-, Karten- und Dokumentenseiten aus ausführen. Sobald der Administrator [!INCLUDE [prod_short](includes/prod_short.md)] mit Power Automate verbunden hat, werden alle von Ihrer Organisation hinzugefügten Flows angezeigt, wenn Sie die Aktion **Automatisieren** auf den entsprechenden Seiten auswählen. Direktflows werden ausgeführt, ohne [!INCLUDE [prod_short](includes/prod_short.md)] zu verlassen. Weitere Informationen finden Sie unter [Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) im Verwaltungsinhalt.

Diese Direkt-Workflows werden auf einer Seite in [!INCLUDE [prod_short](includes/prod_short.md)] Online geöffnet, damit Sie im Kontext des Geschäftsprozesses bleiben, in dem Sie sich gerade befanden. Wählen Sie die Aktion **Automatisieren**, die auf einigen Seiten unter dem Menü **Weitere Optionen** zu finden ist. Suchen Sie sie, wählen Sie den Menüpunkt **Power Automate** und dann den entsprechenden Link aus, um den Workflow auszulösen. Die Verknüpfung zu Power Automate ist bereits eingerichtet.

Bei den meisten Flows müssen Sie ein oder zwei Felder ausfüllen, bevor Sie die Aktion **Flow ausführen** ausführen.

> [!TIP]
> Wenn die Aktion **Automatisieren** nicht angezeigt wird, wurde [!INCLUDE [prod_short](includes/prod_short.md)] wahrscheinlich noch nicht für die Verwendung von Power Automate eingerichtet. Erfahren Sie mehr von Ihrem Administrator.

## <a name="add-more-automated-flows-and-instant-flows"></a>Weitere automatisierte Flows und Direkt-Flows hinzufügen

Sie können Flows auf der Website [powerautomate.microsoft.com](https://powerautomate.microsoft.com) erstellen. Wenn Ihr Administrator jedoch die Funktion zum Ausführen von Power Automate-Flows aus [!INCLUDE [prod_short](includes/prod_short.md)] online aktiviert hat, können Sie mit dem Erstellen eines Flows über die Aktion **Automatisieren** auf den entsprechenden Seiten, die unter dem Menü **Mehr Optionen** je nach Seite zu finden sind. Wählen Sie die das Menüelement **Power Automate** und dann **Flow erstellen** aus. Power Automate wird dann in einer neuen Browserregisterkarte geöffnet, und Sie werden automatisch angemeldet.

Sie können Mustervorlagen finden, die Sie an Ihr Unternehmen und alle verfügbaren Trigger-Ereignisse anpassen können, indem Sie [!INCLUDE [prod_short](includes/prod_short.md)] und externe Tools verwenden. Wählen Sie dazu das Menü **Connectors** auf der Power Automate-Website. Weitere Informationen zu verfügbaren Vorlagen und Auslösern finden Sie unter [Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) im Verwaltungsinhalt.

## <a name="manage-automated-workflows"></a>Automatisierte Workflows verwalten

Sie können neue Flows erstellen oder vorhandene Power Automate-Flows in [!INCLUDE [prod_short](includes/prod_short.md)] auf der Seite **Power Automate-Flows verwalten** verwalten. Erfahren Sie mehr im Artikel [Verwalten von Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) im Inhalt der Administration.

Sie können auf der Seite **Workflows** in [!INCLUDE[prod_short](includes/prod_short.md)] die verfügbaren Power Automate-Workflows verwalten. Die Seite listet sowohl die integrierte Genehmigung und Power Automate-Workflows, mit Optionen für letztere zum Aktivieren/Deaktivieren, Löschen und Anzeigen des Workflows auf der Power Automate-Website.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/use-power-automate/)

## <a name="see-also"></a>Siehe auch

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
