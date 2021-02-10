---
title: Genehmigen und Ablehnen von Belegen im Arbeitsablauf | Microsoft Docs
description: Anfordern, ablehnen oder delegieren einer Genehmigung, beispielsweise einen Einkaufs- oder Verkaufsbeleg, als Teil eines Workflows.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 044b09cb2dced1100665a6d5705f6e43672b5f12
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754592"
---
# <a name="use-approval-workflows"></a>Artikelgenehmigungsworkflow verwenden
Wenn ein Datensatz, wie ein Einkaufsbeleg oder eine Debitorenkarte, von einer Person in Ihrer Organisation genehmigt werden muss, senden Sie eine Genehmigungsanforderung als Teil eines Workflows. Je nachdem, wie der Workflow eingerichtet ist, wird der entsprechende Genehmiger dann benachrichtigt, dass der Datensatz genehmigt werden muss.

Sie richten Genehmigungsworkflows auf der Seite **Workflow** ein. Weitere Informationen erhalten Sie unter [Workflows einrichten](across-set-up-workflows.md).

Neben der Genehmigung von Workflows, wie in diesem Thema beschrieben, können Sie auch verschiedene andere Aufgaben für Workflows ausführen. Weitere Informationen erhalten Sie unter [Workflows verwenden](across-use-workflows.md).

Wesentliche Genehmigungsworkflows für Einkaufsbelege, Verkaufsbelege, Zahlungsausgangs Buch.-Blätter, Debitorenkarten und Artikelkarten können als Leitfaden gestartet werden. Weitere Informationen finden Sie unter [Erste Schritte](product-get-started.md).

## <a name="to-request-approval-of-a-record"></a>So fordern Sie die Genehmigung eines Datensatzes an
Die nächste Aufgabe wird durch einen genehmigenden Benutzer ausgeführt.

1. Wählen Sie auf der Seite, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung senden**.
2. Um alle Ihre Genehmigungsanfragen zu sehen, wählen Sie die Funktion ![Glühbirne, die das Symbol Tell Me feature](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") öffnet, geben Sie **Genehmigungsanfrageeinträge** ein und wählen Sie dann den entsprechenden Link.  

Der Status des Genehmigungspostens wird von **Erstellt** in **Offen** aktualisiert. Der Status des Datensatzes, z. B. einer Einkaufsrechnung wird von **Offen** zu **Ausstehende Genehmigung** aktualisiert und ist für eine Bearbeitung gesperrt, bis alle Genehmiger den Datensatz genehmigt haben.

Wenn der Genehmiger den Datensatz genehmigt hat, ändert sich der Status zu **Freigegeben**. Sie können dann Ihre Aufgaben für diesen Datensatz fortsetzen.

## <a name="to-cancel-requests-for-approval"></a>So stornieren Sie Genehmigungsanforderungen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Ein Debitor möchte möglicherweise Änderungen an einem Auftrag vornehmen, nachdem dieser zur Genehmigung übermittelt wurde. In diesem Fall können Sie den Genehmigungsvorgang abbrechen und die notwendigen Änderungen an dem Auftrag durchführen, bevor Sie eine erneute Genehmigung anfordern.

- Wählen Sie auf der Seite, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung stornieren**.

Wenn die Genehmigungsanforderung storniert wurde, wird der Status des entsprechenden Genehmigungspostens zu **Storniert** geändert. Der Status des Datensatzes wird von **Ausstehende Genehmigung** in **Offen** aktualisiert. Der Genehmigungsvorgang kann dann von vorne begonnen werden.

## <a name="to-approve-or-reject-requests-for-approval"></a>So können Sie Genehmigungsanforderungen genehmigen oder ablehnen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Sie können Genehmigungsanforderungen auf der Seite **Zu genehmigende Anforderungen** verarbeiten, beispielsweise um mehrere Anforderungen gleichzeitig zu genehmigen. Alternativ können Sie jede Anforderung im entsprechenden Datensatz, wie der Seite **Einkaufsrechnung** verarbeiten, indem Sie den Link in der Benachrichtigung auswählen, die Sie erhalten.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Genehmigungsanfragen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie mindestens eine Zeile für den Datensatz (oder die Datensätze) zur Genehmigung oder Ablehnung aus.
3. Wählen Sie die Aktion **Genehmigen**, **Ablehnen**, oder **Delegieren** aus.

Wenn ein Datensatz genehmigt oder abgelehnt wurde, ändert sich der Genehmigungsstatus im Feld **Status** zu **Genehmigt** oder **Abgelehnt**.

Wenn eine Genehmigerhierarchie eingerichtet wurde, bleibt der Datensatzstatus auf **Ausstehende Genehmigung**, bis alle Genehmiger den Datensatz genehmigt haben. Dann ändert sich der Datensatzstatus zu **Freigegeben**.

Gleichzeitig ändert sich der Genehmigungsstatus von **Erstellt** zu **Offen**, sobald eine Genehmigungsanforderung für den Datensatz erstellt wird. Wenn die Anforderung abgelehnt wurde, ändert sich der Genehmigungsstatus zu **Abgelehnt**. Der Status bleibt **Offen** oder **Abgelehnt**, bis alle Genehmiger die Anforderung genehmigt haben.

## <a name="to-delegate-requests-for-approval"></a>So delegieren Sie Genehmigungsanforderungen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Damit verhindert wird, dass sich Belege ansammeln oder anderweitig den Workflow blockieren, können der Genehmiger und der Genehmigungsadministrator eine Genehmigungsanforderung an einen stellvertretenden Genehmiger delegieren. Der Ersatz kann entweder ein festgelegter Ersatz, der direkte Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). In der Regel nutzen Sie diese Funktion dann, wenn sich ein Genehmiger außer Haus befindet und Anforderungen nicht vor dem Fälligkeitsdatum genehmigen kann.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Genehmigungsanfragen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie mindestens eine Zeile für die Genehmigungsanforderungen aus, die Sie an einen Ersatzgenehmiger delegieren möchten, und wählen Sie dann die Aktion **Delegieren**.

Eine Benachrichtigung zur Genehmigung der Anforderung wird an den stellvertretenden Genehmiger gesendet.

## <a name="to-manage-overdue-approval-requests"></a>So verwalten Sie fällige Genehmigungsanforderungen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

In regelmäßigen Abständen müssen Sie Genehmigungs-Workflowbenutzer an überfällige Genehmigungsanforderungen erinnern, auf die sie reagieren müssen. Dazu verwenden Sie die Funktion **Fällige Genehmigungsbenachrichtigungen senden**.

Die Funktion **Fällige Genehmigungsbenachrichtigungen senden** ermittelt alle offenen Genehmigungsanforderungen, die zurzeit fällig sind. Jeder Genehmiger, für den mindestens ein fälliger Genehmigungsposten vorhanden ist, erhält eine Benachrichtigung mit der Liste aller fälligen Genehmigungsanforderungen. Die Benachrichtigung wird auch an den Genehmiger und an alle Anforderer der fälligen Genehmigungen gesendet. Dies ist hilfreich, wenn der fällige Genehmigungsposten an einen Stellvertreter delegiert werden muss.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Überfällige Genehmigungsanfragen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Überfällige Genehmigungsanfragen** die Aktion **Überfällige Genehmigungsbenachrichtigungen senden** aus.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)    
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
