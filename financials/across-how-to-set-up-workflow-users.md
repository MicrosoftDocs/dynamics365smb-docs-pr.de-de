---
title: 'Vorgehensweise: Einrichten von Workflowbenutzern | Microsoft Docs'
description: "Bevor Sie Workflows erstellen können, müssen Sie die Benutzer einrichten, die an Workflows teilnehmen. Dies ist notwendig, um beispielsweise festzulegen, wer eine Benachrichtigung empfangen soll, um auf einen Workflowschritt zu reagieren."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 929cce642a6adccc493c1ce9947ac60662b261d5
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-workflow-users"></a>So wird's gemacht: Einrichten von Workflowbenutzern
Bevor Sie Workflows erstellen können, müssen Sie die Benutzer einrichten, die an Workflows teilnehmen. Dies ist notwendig, um beispielsweise festzulegen, wer eine Benachrichtigung empfangen soll, um auf einen Workflowschritt zu reagieren.  

Im Fenster  **Workflow Benutzergruppen** richten Sie Benutzer unter Workflowbenutzergruppen ein und legen die Reihenfolge von Benutzern in einer Prozessfolge fest, zum Beispiel in einer Genehmigerkette.  

Workflowbenutzer, die als Genehmigungsbenutzer agieren (sowohl Genehmigungsanforderer als auch Genehmiger) müssen auch als Workflowbenutzer im Fenster **Genehmigungsbenutzuer einrichten** eingerichtet werden. [Weitere Informationen finden Sie unter Vorgehensweise: Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)  

> [!NOTE]  
>  Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Genehmiger in einer Genehmigungskette diese genehmigt haben, richten Sie Genehmiger in einer Hierarchie ein. Für Genehmigungstypen **Genehmiger** richten Sie im Fenster **Genehmigungsbenutzereinrichtung** einen Genehmiger ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen**-Fenster fest, und definiert Sie die Hierarchie, indem Sie ansteigende Nummern zu jedem Genehmiger im Feld **Sequenznummer** zuweisen. Feld Weitere Informationen finden Sie unter dem Thema [Vorgehensweise: Genehnigungsbenutzer](across-how-to-set-up-approval-users.md) und in diesem Thema.  
>   
>  Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor mehrere Genehmiger diese genehmigt haben (unabhängig von einer Hierarchie), richten Sie eine flache Workflowbenutzergruppe ein. Legen Sie für den Genehmigertyp **Workflowbenutzergruppe** die Genehmiger oben im **Workflow-Benutzergruppen**-Fenster fest, und weisen Sie jedem Genehmiger unter **Sequenznummer** die gleiche Zahl zu. Feld Weitere Informationen finden Sie in diesem Thema.  

### <a name="to-set-up-a-workflow-user"></a>So richten Sie Workflowbenutzer ein  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflowbenutzergruppen** ein und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus. Das Fenster **Workflow-Genehmigungsgruppe** öffnet sich.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Beschreiben Sie den Workflow im Feld **Beschreibung**.  
5. Füllen Sie im Inforegister **Mitglieder der Workflowbenutzergruppe** die Felder in der ersten Zeile gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Benutzername**|Geben Sie den Benutzer an, der in Workflows einbezogen werden soll.<br /><br /> Der Benutzer muss im Fenster **Benutzereinrichtung** enthalten sein. Weitere Informationen finden Sie unter [So geht's: Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).|  
    |**Reihenfolge**|Geben Sie die Reihenfolge an, in der Workflowbenutzer im Verhältnis zu anderen Benutzern in einen Workflow eingebunden werden. Mit diesem Feld können Sie beispielsweise festlegen, wann ein Benutzer relativ zu anderen Genehmigern genehmigen kann, wenn Sie die Option **Workflow-Benutzergruppe** im Feld **Genehmigungsart** der entsprechenden Workflowreaktion verwenden. **TIPP:** Um zu definieren, dass eine Genehmigungsanforderung nicht genehmigt wird bevor nicht mehrere Genehmiger genehmigt haben (unabhängig von einer Hierarchie), richten Sie eine flache Workflowbenutzergruppe ein. Weisen Sie hieru allen relevanten Genehmigern dieselbe Reihenfolgenummer zu.|  
6. Wiederholen Sie Schritt 5, um weitere Workflowbenutzer zur Benutzergruppe hinzuzufügen.  
7. Wiederholen Sie die Schritte 2 bis 6, um weitere Workflowbenutzergruppen hinzuzufügen.  

## <a name="see-also"></a>Siehe auch  
[Gewusst wie: Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)   
[Einrichten von Workflows](across-set-up-workflows.md)   
[Verwenden von Workflows](across-use-workflows.md)   
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Workflow](across-workflow.md)   

