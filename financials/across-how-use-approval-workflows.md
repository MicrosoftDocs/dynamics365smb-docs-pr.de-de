---
title: 'Vorgehensweise: Genehmigungsworkflows nutzen| Microsoft Docs'
description: Gewusst wie. Genehmigungsworkflow verwenden
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
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ed08fdb7f78c9f6c338e287cd4ef42d7ce0cb72c
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie. Genehmigungsworkflow verwenden
<a id="how-to-use-approval-workflows" class="xliff"></a>
Wenn ein Datensatz, wie ein Einkaufsbeleg oder eine Debitorenkarte, von einer Person in Ihrer Organisation genehmigt werden muss, senden Sie eine Genehmigungsanforderung als Teil eines Workflows. Je nachdem, wie der Workflow eingerichtet ist, wird der entsprechende Genehmiger dann benachrichtigt, dass der Datensatz genehmigt werden muss.

Sie richten Genehmigungsworkflows im Fenster **Workflow** ein.

Wesentliche Genehmigungsworkflows für Einkaufsbelege, Verkaufsbelege, Zahlungsausgangs Buch.-Blätter, Debitorenkarten und Artikelkarten können als unterstützte Einrichtung gestartet werden. Weitere Informationen finden Sie unter [Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

**Hinweis**: Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] anpassen](ui-experiences.md).

## So fordern Sie die Genehmigung eines Datensatzes an
<a id="to-request-approval-of-a-record" class="xliff"></a>
Die nächste Aufgabe wird durch einen genehmigenden Benutzer ausgeführt.

1. Wählen Sie im Fenster, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung senden**.
2. Um alle Genehmigungsanforderungen zu sehen, wählen Sie in der oberen rechter Ecke das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Genehmigungsanforderungseingaben** ein und wählen Sie dann den entsprechenden Link aus.

Der Status des Genehmigungspostens wird von **Erstellt** in **Offen** aktualisiert. Der Status des Datensatzes, z. B. einer Einkaufsrechnung wird von **Offen** zu **Ausstehende Genehmigung** aktualisiert und ist für eine Bearbeitung gesperrt, bis alle Genehmiger den Datensatz genehmigt haben.

Wenn der Genehmiger den Datensatz genehmigt hat, ändert sich der Status zu **Freigegeben**. Sie können dann Ihre Aufgaben für diesen Datensatz fortsetzen.

## So stornieren Sie Genehmigungsanforderungen
<a id="to-cancel-requests-for-approval" class="xliff"></a>
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Ein Debitor möchte möglicherweise Änderungen an einem Auftrag vornehmen, nachdem dieser zur Genehmigung übermittelt wurde. In diesem Fall können Sie den Genehmigungsvorgang abbrechen und die notwendigen Änderungen an dem Auftrag durchführen, bevor Sie eine erneute Genehmigung anfordern.

- Wählen Sie im Fenster, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung stornieren**.

Wenn die Genehmigungsanforderung storniert wurde, wird der Status des entsprechenden Genehmigungspostens zu **Storniert** geändert. Der Status des Datensatzes wird von **Ausstehende Genehmigung** in **Offen** aktualisiert. Der Genehmigungsvorgang kann dann von vorne begonnen werden.

## So nehmen Sie geringfügige Änderungen an genehmigten Datensätzen vor
<a id="to-make-minor-changes-to-approved-records" class="xliff"></a>
Wenn Sie eine kleinere Änderung an einem Datensatz vornehmen möchten, nachdem dieser genehmigt wurde, können Sie den Datensatz erneut öffnen, die Änderung vornehmen und den Datensatz dann freigeben. Für kleine Änderungen können Sie dies über die Schaltflächen **Status zurücksetzen** und **Freigeben** tun.

1. Öffnen Sie das Fenster, das den Datensatz, z.B. eine Einkaufsrechnung anzeigt, und wählen dann die Aktion **Status zurücksetzen** aus.

    Das Feld **Belegstatus** wird zu **Offen** geändert.
2. Nehmen Sie die notwendigen Änderungen am Datensatz vor, zum Beispiel das Ändern der Kreditorenadresse.
3. Wählen Sie die Aktion **Freigabe** aus.

Wenn Sie den Quelldatensatz erneut öffnen, bleibt der Status des zugehörigen Genehmigungspostens im Fenster **Genehmigungsposten** auf "Genehmigt".

## So können Sie Genehmigungsanforderungen genehmigen oder ablehnen
<a id="to-approve-or-reject-requests-for-approval" class="xliff"></a>
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Sie können Genehmigungsanforderungen im Fenster **Zu genehmigende Anforderungen** verarbeiten, beispielsweise um mehrere Anforderungen gleichzeitig zu genehmigen. Alternativ können Sie jede Anforderung im entsprechenden Datensatz, wie dem Fenster **Einkaufsrechnung** verarbeiten, indem Sie den Link in der Benachrichtigung auswählen, die Sie erhalten.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anforderungen für Genehmigungen** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie mindestens eine Zeile für den Datensatz (oder die Datensätze) zur Genehmigung oder Ablehnung aus.
3. Wählen Sie die Aktion **Genehmigen**, **Ablehnen**, oder **Delegieren** aus.

Wenn ein Datensatz genehmigt oder abgelehnt wurde, ändert sich der Genehmigungsstatus im Feld **Status** zu **Genehmigt** oder **Abgelehnt**.

Wenn eine Genehmigerhierarchie eingerichtet wurde, bleibt der Datensatzstatus auf **Ausstehende Genehmigung**, bis alle Genehmiger den Datensatz genehmigt haben. Dann ändert sich der Datensatzstatus zu **Freigegeben**.

Gleichzeitig ändert sich der Genehmigungsstatus von **Erstellt** zu **Offen**, sobald eine Genehmigungsanforderung für den Datensatz erstellt wird. Wenn die Anforderung abgelehnt wurde, ändert sich der Genehmigungsstatus zu **Abgelehnt**. Der Status bleibt **Offen** oder **Abgelehnt**, bis alle Genehmiger die Anforderung genehmigt haben.

## So delegieren Sie Genehmigungsanforderungen
<a id="to-delegate-requests-for-approval" class="xliff"></a>
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

Damit verhindert wird, dass sich Belege ansammeln oder anderweitig den Workflow blockieren, können der Genehmiger und der Genehmigungsadministrator eine Genehmigungsanforderung an einen stellvertretenden Genehmiger delegieren. Der Ersatz kann entweder ein festgelegter Ersatz, der direkte Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge). In der Regel nutzen Sie diese Funktion dann, wenn sich ein Genehmiger außer Haus befindet und Anforderungen nicht vor dem Fälligkeitsdatum genehmigen kann.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anforderungen für Genehmigungen** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie mindestens eine Zeile für die Genehmigungsanforderungen aus, die Sie an einen Ersatzgenehmiger delegieren möchten, und wählen Sie dann die Aktion **Delegieren**.

Eine Benachrichtigung zur Genehmigung der Anforderung wird an den stellvertretenden Genehmiger gesendet.

## So verwalten Sie fällige Genehmigungsanforderungen
<a id="to-manage-overdue-approval-requests" class="xliff"></a>
Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.

In regelmäßigen Abständen müssen Sie Genehmigungs-Workflowbenutzer an überfällige Genehmigungsanforderungen erinnern, auf die sie reagieren müssen. Dazu verwenden Sie die Funktion **Fällige Genehmigungsbenachrichtigungen senden**.

Die Funktion **Fällige Genehmigungsbenachrichtigungen senden** ermittelt alle offenen Genehmigungsanforderungen, die zurzeit fällig sind. Jeder Genehmiger, für den mindestens ein fälliger Genehmigungsposten vorhanden ist, erhält eine Benachrichtigung mit der Liste aller fälligen Genehmigungsanforderungen. Die Benachrichtigung wird auch an den Genehmiger und an alle Anforderer der fälligen Genehmigungen gesendet. Dies ist hilfreich, wenn der fällige Genehmigungsposten an einen Stellvertreter delegiert werden muss.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Überfällige Anforderungen für Genehmigungen** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Fenster **Überfällige Genehmigungsanfragen** die Aktion **Überfällige Genehmigungsbenachrichtigungen senden** aus.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Verkauf](sales-manage-sales.md)    
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

