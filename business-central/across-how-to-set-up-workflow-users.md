---
title: 'Vorgehensweise: Einrichten von Workflowbenutzern | Microsoft Docs'
description: Bevor Sie Workflows erstellen können, müssen Sie die Benutzer einrichten, die an Workflows teilnehmen. Dies ist notwendig, um beispielsweise festzulegen, wer eine Benachrichtigung empfangen soll, um auf einen Workflowschritt zu reagieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87cba590a76c1b14d97351b4b0fd2f2f64d49705
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921122"
---
# <a name="set-up-workflow-users"></a>Einrichten von Workflowbenutzern

Bevor Sie Workflows erstellen können, müssen Sie die Benutzer einrichten, die an Workflows teilnehmen. Dies ist notwendig, um beispielsweise festzulegen, wer eine Benachrichtigung empfangen soll, um auf einen Workflowschritt zu reagieren.  

Auf der Seite  **Workflow Benutzergruppen** richten Sie Benutzer unter Workflowbenutzergruppen ein und legen die Reihenfolge von Benutzern in einer Prozessfolge fest, zum Beispiel in einer Genehmigerkette.  

Workflowbenutzer, die als Genehmigungsbenutzer agieren (sowohl Genehmigungsanforderer als auch Genehmiger) müssen auch als Workflowbenutzer auf der Seite **Genehmigungsbenutzuer einrichten** eingerichtet werden. Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)  

> [!NOTE]  
> Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Genehmiger in einer Genehmigungskette diese genehmigt haben, richten Sie Genehmiger in einer Hierarchie ein. Für Genehmigungstypen **Genehmiger** richten Sie auf der Seite **Genehmigungsbenutzereinrichtung** einen Genehmiger ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen** -Fenster fest, und definiert Sie die Hierarchie, indem Sie ansteigende Nummern zu jedem Genehmiger im Feld **Sequenznummer** zuweisen. Feld eingetragen. Weitere Informationen finden Sie unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md) und im folgenden Abschnitt.  
>
> Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Genehmiger diese genehmigt haben (unabhängig von einer Hierarchie), richten Sie eine flache Workflowbenutzergruppe ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen** -Fenster fest, und weisen Sie jedem Genehmiger unter **Sequenznummer** die gleiche Zahl zu. Feld eingetragen. Weitere Informationen finden Sie im folgenden Abschnitt.  

## <a name="to-set-up-a-workflow-user"></a>So richten Sie Workflowbenutzer ein

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Workflow-Benutzergruppen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus. Die Seite **Workflow-Genehmigungsgruppe** öffnet sich.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Beschreiben Sie den Workflow im Feld **Beschreibung** .  
5. Füllen Sie im Inforegister **Mitglieder der Workflowbenutzergruppe** die Felder in der ersten Zeile gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Benutzername**|Geben Sie den Benutzer an, der in Workflows einbezogen werden soll.<br /><br /> Der Benutzer muss auf der Seite **Benutzereinrichtung** enthalten sein. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).|  
    |**Reihenfolge**|Geben Sie die Reihenfolge an, in der Workflowbenutzer im Verhältnis zu anderen Benutzern in einen Workflow eingebunden werden. Mit diesem Feld können Sie beispielsweise festlegen, wann ein Benutzer relativ zu anderen Genehmigern genehmigen kann, wenn Sie die Option **Workflow-Benutzergruppe** im Feld **Genehmigungsart** der entsprechenden Workflowreaktion verwenden. **TIPP:** Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor nicht mehrere Genehmiger genehmigt haben (unabhängig von einer Hierarchie), richten Sie eine flache Workflowbenutzergruppe ein. Weisen Sie hieru allen relevanten Genehmigern dieselbe Reihenfolgenummer zu.|  
6. Wiederholen Sie Schritt 5, um weitere Workflowbenutzer zur Benutzergruppe hinzuzufügen.  
7. Wiederholen Sie die Schritte 2 bis 6, um weitere Workflowbenutzergruppen hinzuzufügen.  

## <a name="see-also"></a>Siehe auch

[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)  
[Einrichten von Workflows](across-set-up-workflows.md)  
[Verwenden von Workflows](across-use-workflows.md)  
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]