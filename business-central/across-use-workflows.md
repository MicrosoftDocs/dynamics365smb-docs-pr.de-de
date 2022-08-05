---
title: Verwenden von Workflows
description: Sie können Workflows festlegen und verwenden, die Geschäftsprozessaufgaben wie das automatische Buchen oder das Anfordern und Genehmigen neuer Datensätze miteinander verbinden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 4f66b334df678ff27e094858dd0cec44c1bb8e75
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130226"
---
# <a name="use-workflows"></a>Workflows verwenden

Ein Workflow ist eine Sequenz von Aufgaben, die durch eine Aktion, eine Bedingung oder eine Regel ausgelöst wird. Workflows werden in der Regel implementiert, um Geschäftslogik in eine Organisation zu integrieren, wie z. B. die Trennung von Aufgaben, die Vereinheitlichung von Prozessen oder die Erhöhung von Vertrauen und Verantwortung.  

Die Workflows sind so konzipiert, dass sie Anfragen zur Genehmigung eines neuen Wertes erstellen, während der alte Wert beibehalten wird, falls die Anfrage nicht genehmigt wird. Der neue Wert wird erst dann implementiert, wenn die letzte Anforderung genehmigt ist.  

Die Geschäftslogik könnte die Genehmigung von sein:

- Neue Stammdaten wie Sachkonten, Debitoren, Kreditor oder Artikel
- Änderungen an Feldern in bestehenden Datensätzen, die sensible Informationen enthalten, wie z.B. **Kreditor Bankkontonr.** oder **Kunde Kreditlimit**
- Änderungen an Feldern in bestehenden Datensätzen, die geschäftskritische Informationen enthalten, z.B. **Artikel VK-Preise**
- Neue Benutzer oder Änderungen an Benutzerberechtigungen
- Kauf Belege
- Verkaufsbelege
- Eingehende Belege
- Finance Erfassungen vor der Buchung

Die folgende Abbildung zeigt ein Beispiel für einen Workflow mit sequentieller Genehmigung, ausgelöst durch einen Benutzer. Durch das Auslösen des Workflows wird ein Genehmigungsantrag für den ersten Genehmiger erstellt.  

![Illustration eines Workflows mit sequentieller Genehmigung.](media/Workflows/approval-flow.png)

In diesem Beispiel muss die Anfrage vom ersten Genehmiger genehmigt werden, bevor die Anfrage an den nächsten Genehmiger weitergeleitet wird. Wenn die Anfrage nicht vom ersten Genehmiger genehmigt wird, wird die Anfrage nie an den nächsten Genehmiger weitergeleitet.  

Der Arbeitsplan ab dem ersten Auslösen des Workflows kann je nach Art der Genehmigung variieren.  

Die folgende Abbildung zeigt eine parallele Genehmigung, die durch den Benutzer ausgelöst wird. Durch das Auslösen des Workflows wird ein Genehmigungsantrag an alle Genehmiger gleichzeitig gesendet.  

![Illustration eines Workflows mit paralleler Genehmigung.](media/Workflows/approval-flow-2.png)

Der Workflow ist jedoch erst dann genehmigt, wenn alle Anträge von den Genehmigenden genehmigt wurden, wie in der folgenden Abbildung dargestellt:  

![Illustration eines abgelehnten Workflows mit paralleler Genehmigung.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Es ist nicht möglich, einen Workflow mit mehreren Genehmigern zu erstellen und zu erwarten, dass der gesamte Workflow genehmigt wird, nachdem die erste Anfrage genehmigt wurde. Alle Anträge müssen genehmigt werden, damit der Workflow genehmigt werden kann.

Sie können Workflows festlegen und verwenden, die von verschiedenen Benutzern ausgeführte Geschäftsprozessaufgaben miteinander verbinden. Es ist auch möglich, denselben Workflow mehr als einmal zu erstellen. Jeder Workflow kann durch ein Ereignis mit unterschiedlichen Filtern ausgelöst werden. Dies ist nützlich, wenn eine Genehmigungsanfrage in einer Abteilung von einem Genehmiger genehmigt werden muss, während Genehmigungsanfragen in anderen Abteilungen von einem anderen Genehmiger genehmigt werden müssen. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

Bevor Sie beginnen können, Workflows zu verwenden, müssen Sie Workflowbenutzer einrichten, die Workflows erstellen, möglicherweise Codeanpassung berücksichtigen und angeben, wie Benutzer Benachrichtigungen empfangen sollen. Weitere Informationen erhalten Sie unter [Workflows einrichten](across-set-up-workflows.md).  

> [!NOTE]  
> Typische Workflowschritte drehen sich um Benutzer, die Genehmigungen für Aufgaben anfordern, und Genehmiger, die Genehmigungsanforderungen annehmen oder ablehen. Daher beschäftigen sich viele Themen in Bezug auf die Verwendung von Workflows mit Genehmigungen.  

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.  

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Richten Sie einen Workflow ein, der gestartet wird, wenn das erste Einstiegspunktereignis auftritt.|[Aktivieren von Workflows](across-how-to-enable-workflows.md)|  
|Anforderung der Genehmigung einer Aufgabe, Akzeptieren oder Delegieren von Genehmigungen oder Ablehnen von Genehmigungen, und Senden oder Anzeigen von Genehmigungsbenachrichtigungen.|[Artikelgenehmigungsworkflow verwenden](across-how-use-approval-workflows.md)|  
|Erstellen Sie Workflowschritte, die einen bestimmten Datensatztyp für die Verwendung vor einem bestimmten Ereignis einschränken (beispielsweise, bevor der Datensatz genehmigt wird).|[Zulassen und Einschränken des Verbrauchs eines Datensatzes](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Zeigen Sie Workflowschrittinstanzen mit dem Status **Abgeschlossen** an.|[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)|  
|Löschen Sie einen Workflow, den Sie mit Gewissheit nicht mehr verwenden werden.|[Löschen eines Workflows](across-how-to-delete-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Siehe auch

[Einrichten von Workflows](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]