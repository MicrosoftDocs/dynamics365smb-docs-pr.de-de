---
title: So legen Sie Workflow-Benutzer fest
description: 'Bevor Sie Workflows erstellen können, müssen Sie die Benutzer, die daran teilnehmen, auf der Einrichtungsseite für Benutzergenehmigungen einrichten.'
author: brentholtorf
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '1533,'
ms.date: 05/31/2023
ms.author: bholtorf
---
# <a name="set-up-a-sequence-of-workflow-users" />Sequenz von Workflow-Benutzern einrichten

Bevor Sie Genehmigungsworkflows erstellen können, müssen Sie die Benutzer einrichten, die Anforderungen und ihre Genehmiger übermitteln. Beispielsweise können Sie festlegen, wer eine Benachrichtigung empfangen soll, um auf einen Workflowschritt zu reagieren. Sie richten Teilnehmer an Genehmigungsworkflows auf der Seite **Genehmigungsbenutzereinrichtung** ein. Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md).

Sie können auf der Seite **Workflow-Benutzergruppen** angeben, wo ein Teilnehmer an einem Genehmigungsworkflow beteiligt ist, indem Sie im Feld **Sequenznummer** eine Zahl eingeben Feld Sie können beispielsweise festlegen, dass Benutzer in einer sequenziellen Reihenfolge interagieren, beispielsweise in einer Genehmigerkette. Sie können auch eine flache Liste von Genehmigern angeben, indem Sie dieselbe Nummer eingeben. Im letzteren Fall muss nur einer der Genehmiger eine Anforderung genehmigen.

[!INCLUDE [workflow-requestor-approver](includes/workflow-requestor-approver.md)]

## <a name="to-set-up-a-workflow-user-group" />So richten Sie eine Workflow-Benutzergruppe ein

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Workflow-Benutzergruppen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**. Die Seite **Workflow-Genehmigungsgruppe** öffnet sich.  
3. Geben Sie im Feld **Code** maximal 20 Zeichen ein, um den Workflow zu identifizieren.  
4. Beschreiben Sie den Workflow im Feld **Beschreibung**.  
5. Füllen Sie im Inforegister **Mitglieder der Workflowbenutzergruppe** die Felder in der ersten Zeile gemäß der Beschreibung in der folgenden Tabelle aus.  

   |Feld|Description|
   |-----|-----------|
   |**Benutzername**|Geben Sie den Benutzer an, der in einem Workflow einbezogen werden soll.<br /><br /> Der Benutzer muss auf der Seite **Benutzereinrichtung** enthalten sein. Weitere Informationen erhalten Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).|
   |**Reihenfolge**|Geben Sie die Reihenfolge an, in der Workflowbenutzer im Verhältnis zu anderen Benutzern in einen Workflow eingebunden werden. Mit diesem Feld können Sie beispielsweise angeben, wann ein Benutzer relativ zu anderen Genehmigern genehmigen kann, indem Sie die Option **Workflow-Benutzergruppe** im Feld **Genehmigungsart** der entsprechenden Workflowreaktion verwenden.| 

6. Wiederholen Sie Schritt 5, um weitere Workflowbenutzer zur Workflowbenutzergruppe hinzuzufügen.  

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## <a name="see-also" />Siehe auch

[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
