---
title: Genehmigen und Ablehnen von Belegen im Arbeitsablauf | Microsoft Docs
description: Anfordern, ablehnen oder delegieren einer Genehmigung, beispielsweise einen Einkaufs- oder Verkaufsbeleg, als Teil eines Workflows.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 09/28/2021
ms.author: edupont
ms.openlocfilehash: 55e7861d479ee5d4415ca776f969b722464ddcc3
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531917"
---
# <a name="use-approval-workflows"></a>Artikelgenehmigungsworkflow verwenden

Wenn ein Datensatz, wie ein Einkaufsbeleg oder eine Debitorenkarte, von einer Person in Ihrer Organisation genehmigt werden muss, senden Sie eine Genehmigungsanforderung als Teil eines Workflows. Je nachdem, wie der Workflow eingerichtet ist, wird der entsprechende Genehmiger dann benachrichtigt, dass der Datensatz genehmigt werden muss.

Sie richten Genehmigungsworkflows auf der Seite **Workflow** ein. Außerdem müssen Sie auf der Seite **Genehmigungsbenutzereinrichtung** die Genehmigungsbenutzer festlegen, einschließlich aller relevanten Betragsgrenzen. Weitere Informationen erhalten Sie unter [Workflows einrichten](across-set-up-workflows.md).  

Neben der Genehmigung von Workflows, wie in diesem Artikel beschrieben, können Sie auch verschiedene andere Aufgaben für Workflows ausführen. Weitere Informationen finden Sie unter [Workflows verwenden](across-use-workflows.md).

Wesentliche Genehmigungsworkflows für Einkaufsbelege, Verkaufsbelege, Zahlungsausgangs Buch.-Blätter, Debitorenkarten und Artikelkarten können als Leitfaden gestartet werden. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).

## <a name="to-request-approval-of-a-record"></a>So fordern Sie die Genehmigung eines Datensatzes an

Die nächste Aufgabe wird durch einen genehmigenden Benutzer ausgeführt.

1. Wählen Sie auf der Seite, auf der der Datensatz angezeigt wird, die Aktion **Genehmigungsantrag senden**.
2. Um alle Ihre Genehmigungs-Anforderungen zu sehen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Genehmigungsanforderungsposten** ein, und wählen Sie dann den zugehörigen Link.  

Der Status des Genehmigungspostens wird von **Erstellt** in **Offen** aktualisiert. Der Status des Datensatzes, z. B. einer Einkaufsrechnung wird von **Offen** zu **Ausstehende Genehmigung** aktualisiert und ist für eine Bearbeitung gesperrt, bis alle Genehmiger den Datensatz genehmigt haben.

Wenn alle erforderlichen Genehmiger den Datensatz genehmigt haben, ändert sich der Status in **Freigegeben**. Sie können dann Ihre Aufgaben für diesen Datensatz fortsetzen.

## <a name="to-cancel-requests-for-approval"></a>So stornieren Sie Genehmigungsanforderungen

Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Ein Debitor möchte möglicherweise Änderungen an einem Auftrag vornehmen, nachdem dieser zur Genehmigung übermittelt wurde. In diesem Fall können Sie den Genehmigungsvorgang abbrechen und die notwendigen Änderungen an dem Auftrag durchführen, bevor Sie eine erneute Genehmigung anfordern.

- Wählen Sie auf der Seite, auf der der Datensatz angezeigt wird, die Aktion **Genehmigungsanfrage stornieren**.

Wenn die Genehmigungsanforderung storniert wurde, wird der Status des entsprechenden Genehmigungspostens zu **Storniert** geändert. Der Status des Datensatzes wird von **Ausstehende Genehmigung** in **Offen** aktualisiert. Der Genehmigungsvorgang kann dann von vorne begonnen werden.

## <a name="to-approve-or-reject-requests-for-approval"></a>So können Sie Genehmigungsanforderungen genehmigen oder ablehnen

Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Sie können Genehmigungsanforderungen auf der Seite **Zu genehmigende Anforderungen** verarbeiten, beispielsweise um mehrere Anforderungen gleichzeitig zu genehmigen. Alternativ können Sie jede Anforderung im entsprechenden Datensatz, wie der Seite **Einkaufsrechnung** verarbeiten, indem Sie den Link in der Benachrichtigung auswählen, die Sie erhalten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zu genehmigende Anforderungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie mindestens eine Zeile für den Datensatz (oder die Datensätze) zur Genehmigung oder Ablehnung aus.
3. Wählen Sie die Aktion **Genehmigen**, **Ablehnen**, oder **Delegieren** aus.

Wenn ein Datensatz genehmigt oder abgelehnt wurde, ändert sich der Genehmigungsstatus im Feld **Status** zu **Genehmigt** oder **Abgelehnt**.

Wenn eine Genehmigerhierarchie eingerichtet wurde, bleibt der Datensatzstatus auf **Ausstehende Genehmigung**, bis alle Genehmiger den Datensatz genehmigt haben. Dann ändert sich der Datensatzstatus zu **Freigegeben**.

Gleichzeitig ändert sich der Genehmigungsstatus von **Erstellt** zu **Offen**, sobald eine Genehmigungsanforderung für den Datensatz erstellt wird. Wenn die Anforderung abgelehnt wurde, ändert sich der Genehmigungsstatus zu **Abgelehnt**. Der Status bleibt **Offen** oder **Abgelehnt**, bis alle Genehmiger die Anforderung genehmigt haben.

## <a name="to-delegate-requests-for-approval"></a>So delegieren Sie Genehmigungsanforderungen

Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Damit verhindert wird, dass sich Belege ansammeln oder anderweitig den Workflow blockieren, können der Genehmiger und der Genehmigungsadministrator eine Genehmigungsanforderung an einen stellvertretenden Genehmiger delegieren. Der Ersatz kann entweder ein festgelegter Ersatz, der direkte Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). In der Regel nutzen Sie diese Funktion dann, wenn ein Genehmiger nicht verfügbar oder Anforderungen nicht vor dem Fälligkeitsdatum genehmigen kann.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Zu genehmigende Anforderungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie mindestens eine Zeile für die Genehmigungsanforderungen aus, die Sie an einen Ersatzgenehmiger delegieren möchten, und wählen Sie dann die Aktion **Delegieren**.

Eine Benachrichtigung zur Genehmigung der Anforderung wird an den stellvertretenden Genehmiger gesendet.

## <a name="to-manage-overdue-approval-requests"></a>So verwalten Sie fällige Genehmigungsanforderungen

Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

In regelmäßigen Abständen müssen Sie Genehmigungs-Workflowbenutzer an überfällige Genehmigungsanforderungen erinnern, auf die sie reagieren müssen. Verwenden Sie die Funktion **Fällige Genehmigungsbenachrichtigungen senden**, um Benutzer zu erinnern.

Die Funktion **Fällige Genehmigungsbenachrichtigungen senden** ermittelt alle offenen Genehmigungsanforderungen, die zurzeit fällig sind. Jeder Genehmiger, für den mindestens ein fälliger Genehmigungsposten vorhanden ist, erhält eine Benachrichtigung mit der Liste aller fälligen Genehmigungsanforderungen. Die Benachrichtigung wird auch an den Genehmiger und an alle Anforderer der fälligen Genehmigungen gesendet. Dieser letzte Schritt ist hilfreich, wenn der fällige Genehmigungsposten an einen Stellvertreter delegiert werden muss.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Überfällige Genehmigungsanfragen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Überfällige Genehmigungsanfragen** die Aktion **Überfällige Genehmigungsbenachrichtigungen senden** aus.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/use-approval-workflows/)

## <a name="see-also"></a>Siehe auch

[Einrichten von Genehmigten Benutzern](across-how-to-set-up-approval-users.md)  
[Verkauf](sales-manage-sales.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
