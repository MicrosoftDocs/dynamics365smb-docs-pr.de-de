---
title: Ressourcen, Arbeitszeittabellen und Aufgaben einrichten| Microsoft Docs
description: Die Arbeitszeittabellen, um die Zeit zu verfolgen, die für Projekte verwendet wurde und Ressourcen verwendet wurde und halfen Ihnen mit Projektmanagement, der Stellenbesetzung und der Kapazität
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d2efe0d6d630f3548a41e164f0d71cb98fe09240
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253217"
---
# <a name="set-up-time-sheets"></a>Einrichten von Arbeitszeittabellen
Arbeitszeittabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfassen die Zeit in wöchentlichen Schritten von sieben Tagen. Sie verwenden sie, um die Zeit zu verfolgen, die für Projekte verwendet wird, und Sie können sie verwenden, um Ressourcenzeiterfassung um zu erfassen. Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie festlegen, wie sie eingerichtet und konfiguriert werden sollen.

Nachdem Sie eingerichtet haben, wie Ihre Organisation Arbeitszeittabellen verwendet, können Sie angeben, wann und wie Arbeitszeittabellen genehmigt werden. Abhängig von den Anforderungen Ihrer Organisation, können Sie festlegen:

* Einen oder mehrere Benutzer als Arbeitszeittabellenadministrator und Genehmiger für alle Arbeitszeittabellen.
* Ein Arbeitszeittabellengenehmiger für jede Ressource.

Wenn Sie Arbeitszeittabellen eingerichtet haben, können Sie Arbeitszeittabellen für Ressourcen erstellen, sie Projektplanungszeilen zuweisen und Arbeitszeittabellenzeilen buchen. Weitere Informationen finden Sie unter [Verwenden von Arbeitszeittabellen](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Um allgemeine Informationen für Arbeitszeittabellen einzurichten:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Ressourceneinrichtung** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Für das Feld **Arbeitszeittabelle nach Projekt-Genehmigung** wählen Sie eine der folgenden Optionen aus.

| Option | Beschreibung |
| --- | --- |
| **Nie** |Der Benutzer im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** der Ressourcenkarte genehmigt die Arbeitszeittabelle. |
| **Immer** |Der Benutzer im Feld **Verantwortliche Person** der Projektkarte genehmigt die Arbeitszeittabelle. |
| **Nur Arbeitsplätze** |Wenn die Arbeitsplatzzeittabelle mit einem Projekt verknüpft ist, dann genehmigt der Benutzer im Feld **Verantwortliche Person** auf der Projektkarte die Arbeitszeittabelle. Wenn die Arbeitsplatzzeittabelle mit einer Ressource verknüpft ist, dann genehmigt der Benutzer im Feld **Arbeitszeittabelle Genehmiger-Benutzer-ID** auf der Ressourcenkarte die Arbeitszeittabelle. |

## <a name="to-assign-a-time-sheet-administrator"></a>So weisen Sie einen Arbeitszeittabellenadministrator zu:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer einrichten** ein, und wählen dann den zugehörigen Link aus.  
2. Fügen Sie einen neuen Benutzer hinzu, wenn die Benutzerliste nicht die Person enthält, die Arbeitszeittabelleadministrator sein soll. Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).
3. Wählen Sie einen Benutzer aus, der Arbeitszeittabellenadministrator sein soll, und wählen Sie dann das Kontrollkästchen **Arbeitszeittabellen-Administrator** aus.  

> [!TIP]  
>   Es wird empfohlen, nur einen Benutzer als Arbeitszeittabellenadministrator für ein Unternehmen festzulegen. Im folgenden Verfahren richten Sie einen Arbeitszeittabellenbesitzer und - genehmiger ein, wenn der Arbeitszeittabellengenehmiger für jede Ressource zugeordnet ist.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>So legen Sie einen Arbeitszeittabellenbesitzer und -genehmiger fest:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Ressourcen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Ressource, für die Sie die Möglichkeit einrichten möchten, Arbeitszeittabellen zu verwenden, und wählen Sie dann das Kontrollkästchen **Arbeitszeittabelle verwenden**.  
3. Geben Sie im Feld **Arbeitszeittabellenbesitzer-Benutzer-ID** die ID des Besitzers der Arbeitszeittabelle ein. Der Eigentümer kann Bearbeitungszeit auf der Arbeitszeittabelle eingeben und ihn zur Genehmigung senden. Wenn es sich bei der Ressource um eine Person handelt, ist diese Person im Allgemeinen auch der Besitzer.  
4. Geben Sie im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** die ID des Genehmigers der Arbeitszeittabelle ein. Der Genehmiger kann eine Arbeitszeittabelle genehmigen, ablehnen oder erneut öffnen.  

> [!NOTE]  
>   Sie können die ID des Arbeitszeittabellengenehmigers nicht ändern, wenn Arbeitszeittabellen vorhanden sind, die noch nicht verarbeitet wurden und die den Status **Übermittelt** oder **Offen** haben.

## <a name="see-also"></a>Siehe auch
[Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)  
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
