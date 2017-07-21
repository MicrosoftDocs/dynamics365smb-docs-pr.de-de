---
title: Genehmigen und Ablehnen von Belegen im Arbeitsablauf | Microsoft Docs
description: Anfordern, ablehnen oder delegieren einer Genehmigung, beispielsweise einen Einkaufs- oder Verkaufsbeleg, als Teil eines Workflows.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ffeffe725025dc03d2053333f75249679103b6a4
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-use-approval-workflows"></a>Gewusst wie. Genehmigungsworkflow verwenden
Wenn ein Datensatz, wie ein Einkaufsbeleg oder eine Debitorenkarte, von einer Person in Ihrer Organisation genehmigt werden muss, senden Sie eine Genehmigungsanforderung als Teil eines Workflows. Je nachdem, wie der Workflow eingerichtet ist, wird der entsprechende Genehmiger dann benachrichtigt, dass der Datensatz genehmigt werden muss.

Sie richten Genehmigungsworkflows im Fenster **Workflow** ein.

Wesentliche Genehmigungsworkflows für Einkaufsbelege, Verkaufsbelege, Zahlungsausgangs Buch.-Blätter, Debitorenkarten und Artikelkarten können als unterstützte Einrichtung gestartet werden. Weitere Informationen finden Sie unter [Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="to-request-approval-of-a-record"></a>So fordern Sie die Genehmigung eines Datensatzes an
Die nächste Aufgabe wird durch einen genehmigenden Benutzer ausgeführt.

1. Wählen Sie im Fenster, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung senden**.
2. Um alle Genehmigungsanforderungen anzuzeigen, wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus, geben **Genehmigungsanforderungsposten** ein und wählen dann den zugehörigen Link aus.  

Der Status des Genehmigungspostens wird von **Erstellt** in **Offen** aktualisiert. Der Status des Datensatzes, z. B. einer Einkaufsrechnung wird von **Offen** zu **Ausstehende Genehmigung** aktualisiert und ist für eine Bearbeitung gesperrt, bis alle Genehmiger den Datensatz genehmigt haben.

Wenn der Genehmiger den Datensatz genehmigt hat, ändert sich der Status zu **Freigegeben**. Sie können dann Ihre Aufgaben für diesen Datensatz fortsetzen.

## <a name="to-cancel-requests-for-approval"></a>So stornieren Sie Genehmigungsanforderungen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Ein Debitor möchte möglicherweise Änderungen an einem Auftrag vornehmen, nachdem dieser zur Genehmigung übermittelt wurde. In diesem Fall können Sie den Genehmigungsvorgang abbrechen und die notwendigen Änderungen an dem Auftrag durchführen, bevor Sie eine erneute Genehmigung anfordern.

- Wählen Sie im Fenster, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung stornieren**.

Wenn die Genehmigungsanforderung storniert wurde, wird der Status des entsprechenden Genehmigungspostens zu **Storniert** geändert. Der Status des Datensatzes wird von **Ausstehende Genehmigung** in **Offen** aktualisiert. Der Genehmigungsvorgang kann dann von vorne begonnen werden.

## <a name="to-make-minor-changes-to-approved-records"></a>So nehmen Sie geringfügige Änderungen an genehmigten Datensätzen vor
Wenn Sie eine kleinere Änderung an einem Datensatz vornehmen möchten, nachdem dieser genehmigt wurde, können Sie den Datensatz erneut öffnen, die Änderung vornehmen und den Datensatz dann freigeben. Für kleine Änderungen können Sie dies über die Schaltflächen **Status zurücksetzen** und **Freigeben** tun.

1. Öffnen Sie das Fenster, das den Datensatz, z.B. eine Einkaufsrechnung anzeigt, und wählen dann die Aktion **Status zurücksetzen** aus.

    Das Feld **Belegstatus** wird zu **Offen** geändert.
2. Nehmen Sie die notwendigen Änderungen am Datensatz vor, zum Beispiel das Ändern der Kreditorenadresse.
3. Wählen Sie die Aktion **Freigabe** aus.

Wenn Sie den Quelldatensatz erneut öffnen, bleibt der Status des zugehörigen Genehmigungspostens im Fenster **Genehmigungsposten** auf "Genehmigt".

## <a name="to-approve-or-reject-requests-for-approval"></a>So können Sie Genehmigungsanforderungen genehmigen oder ablehnen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Sie können Genehmigungsanforderungen im Fenster **Zu genehmigende Anforderungen** verarbeiten, beispielsweise um mehrere Anforderungen gleichzeitig zu genehmigen. Alternativ können Sie jede Anforderung im entsprechenden Datensatz, wie dem Fenster **Einkaufsrechnung** verarbeiten, indem Sie den Link in der Benachrichtigung auswählen, die Sie erhalten.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen ](media/ui-search/search_small.png "Nach Seite oder Bericht suche")und geben **Zu genehmigende Anforderungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie mindestens eine Zeile für den Datensatz (oder die Datensätze) zur Genehmigung oder Ablehnung aus.
3. Wählen Sie die Aktion **Genehmigen**, **Ablehnen**, oder **Delegieren** aus.

Wenn ein Datensatz genehmigt oder abgelehnt wurde, ändert sich der Genehmigungsstatus im Feld **Status** zu **Genehmigt** oder **Abgelehnt**.

Wenn eine Genehmigerhierarchie eingerichtet wurde, bleibt der Datensatzstatus auf **Ausstehende Genehmigung**, bis alle Genehmiger den Datensatz genehmigt haben. Dann ändert sich der Datensatzstatus zu **Freigegeben**.

Gleichzeitig ändert sich der Genehmigungsstatus von **Erstellt** zu **Offen**, sobald eine Genehmigungsanforderung für den Datensatz erstellt wird. Wenn die Anforderung abgelehnt wurde, ändert sich der Genehmigungsstatus zu **Abgelehnt**. Der Status bleibt **Offen** oder **Abgelehnt**, bis alle Genehmiger die Anforderung genehmigt haben.

## <a name="to-delegate-requests-for-approval"></a>So delegieren Sie Genehmigungsanforderungen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Damit verhindert wird, dass sich Belege ansammeln oder anderweitig den Workflow blockieren, können der Genehmiger und der Genehmigungsadministrator eine Genehmigungsanforderung an einen stellvertretenden Genehmiger delegieren. Der Ersatz kann entweder ein festgelegter Ersatz, der direkte Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). In der Regel nutzen Sie diese Funktion dann, wenn sich ein Genehmiger außer Haus befindet und Anforderungen nicht vor dem Fälligkeitsdatum genehmigen kann.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen ](media/ui-search/search_small.png "Nach Seite oder Bericht suche")und geben **Zu genehmigende Anforderungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie mindestens eine Zeile für die Genehmigungsanforderungen aus, die Sie an einen Ersatzgenehmiger delegieren möchten, und wählen Sie dann die Aktion **Delegieren**.

Eine Benachrichtigung zur Genehmigung der Anforderung wird an den stellvertretenden Genehmiger gesendet.

## <a name="to-manage-overdue-approval-requests"></a>So verwalten Sie fällige Genehmigungsanforderungen
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

In regelmäßigen Abständen müssen Sie Genehmigungs-Workflowbenutzer an überfällige Genehmigungsanforderungen erinnern, auf die sie reagieren müssen. Dazu verwenden Sie die Funktion **Fällige Genehmigungsbenachrichtigungen senden**.

Die Funktion **Fällige Genehmigungsbenachrichtigungen senden** ermittelt alle offenen Genehmigungsanforderungen, die zurzeit fällig sind. Jeder Genehmiger, für den mindestens ein fälliger Genehmigungsposten vorhanden ist, erhält eine Benachrichtigung mit der Liste aller fälligen Genehmigungsanforderungen. Die Benachrichtigung wird auch an den Genehmiger und an alle Anforderer der fälligen Genehmigungen gesendet. Dies ist hilfreich, wenn der fällige Genehmigungsposten an einen Stellvertreter delegiert werden muss.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen ](media/ui-search/search_small.png "Nach Seite oder Bericht suche")und geben **Überfällige Genehmigungsanforderungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Überfällige Genehmigungsanfragen** die Aktion **Überfällige Genehmigungsbenachrichtigungen senden** aus.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)    
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

