---
title: "Gewusst wie: Zeiblätter einrichten | Microsoft Docs"
description: "Beschreibt, wie das System für die Nutzung von Arbeitszeittabellen für die Verwaltung von Projektnen vorbereitet wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: aa93e7fe867893c52e3b3973a58ea8a43291c1b1
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# Gewusst wie: Einrichten von Arbeitszeittabellen
<a id="how-to-set-up-time-sheets" class="xliff"></a>
Arbeitszeittabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfassen die Zeit in wöchentlichen Schritten von sieben Tagen. Sie verwenden sie, um die Zeit zu verfolgen, die für Projekte verwendet wird, und Sie können sie verwenden, um Ressourcenzeiterfassung um zu erfassen. Bevor Sie Arbeitszeittabellen verwenden können, müssen Sie festlegen, wie sie eingerichtet und konfiguriert werden sollen.

Nachdem Sie eingerichtet haben, wie Ihre Organisation Arbeitszeittabellen verwendet, können Sie angeben, wann und wie Arbeitszeittabellen genehmigt werden. Abhängig von den Anforderungen Ihrer Organisation, können Sie festlegen:

* Einen oder mehrere Benutzer als Arbeitszeittabellenadministrator und Genehmiger für alle Arbeitszeittabellen.
* Ein Arbeitszeittabellengenehmiger für jede Ressource.

Wenn Sie Arbeitszeittabellen eingerichtet haben, können Sie Arbeitszeittabellen für Ressourcen erstellen, sie Projektplanungszeilen zuweisen und Arbeitszeittabellenzeilen buchen. Weitere Informationen finden Sie unter [Vorgehensweise: Verwenden von Arbeitszeittabellen](projects-how-use-time-sheets.md).

## Um allgemeine Informationen für Arbeitszeittabellen einzurichten:
<a id="to-set-up-general-information-for-time-sheets" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Ressourcen einrichten** ein und wählen Sie dann den entsprechenden Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Für das Feld **Arbeitszeittabelle nach Projekt-Genehmigung** wählen Sie eine der folgenden Optionen aus.

| Option | Beschreibung |
| --- | --- |
| **Nie** |Der Benutzer im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** der Ressourcenkarte genehmigt die Arbeitszeittabelle. |
| **Immer** |Der Benutzer im Feld **Verantwortliche Person** der Projektkarte genehmigt die Arbeitszeittabelle. |
| **Nur Arbeitsplätze** |Wenn die Arbeitsplatzzeittabelle mit einem Projekt verknüpft ist, dann genehmigt der Benutzer im Feld **Verantwortliche Person** auf der Projektkarte die Arbeitszeittabelle. Wenn die Arbeitsplatzzeittabelle mit einer Ressource verknüpft ist, dann genehmigt der Benutzer im Feld **Arbeitszeittabelle Genehmiger-Benutzer-ID** auf der Ressourcenkarte die Arbeitszeittabelle. |

## So weisen Sie einen Arbeitszeittabellenadministrator zu:
<a id="to-assign-a-time-sheet-administrator" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **MwSt-Benutzereinrichtung** eingeben und den entsprechenden Link auswählen.  
2. Fügen Sie einen neuen Benutzer hinzu, wenn die Benutzerliste nicht die Person enthält, die Arbeitszeittabelleadministrator sein soll. Weitere Informationen finden Sie im Abschnitt "Benutzer erstellen" [Für das Geschäft bereit sein](ui-get-ready-business.md).  
3. Wählen Sie einen Benutzer aus, der Arbeitszeittabellenadministrator sein soll, und wählen Sie dann den **Arbeitszeittabellen-Administrator** aus. Kontrollkästchen aktivieren.  

**Hinweis**: Es wird empfohlen, nur einen Benutzer als Arbeitszeittabellenadministrator für ein Unternehmen festzulegen. Im folgenden Verfahren richten Sie einen Arbeitszeittabellenbesitzer und - genehmiger ein, wenn der Arbeitszeittabellengenehmiger für jede Ressource zugeordnet ist.  

## So legen Sie einen Arbeitszeittabellenbesitzer und -genehmiger fest:
<a id="to-assign-a-time-sheets-owner-and-approver" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Ressourcen** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Ressource, für die Sie die Möglichkeit einrichten möchten, Arbeitszeittabellen zu verwenden, und wählen Sie dann das Kontrollkästchen **Arbeitszeittabelle verwenden**.  
3. Geben Sie im Feld **Arbeitszeittabellenbesitzer-Benutzer-ID** die ID des Besitzers der Arbeitszeittabelle ein. Der Eigentümer kann Bearbeitungszeit auf der Arbeitszeittabelle eingeben und ihn zur Genehmigung senden. Wenn es sich bei der Ressource um eine Person handelt, ist diese Person im Allgemeinen auch der Besitzer.  
4. Geben Sie im Feld **Arbeitszeittabellengenehmiger-Benutzer-ID** die ID des Genehmigers der Arbeitszeittabelle ein. Der Genehmiger kann eine Arbeitszeittabelle genehmigen, ablehnen oder erneut öffnen.  

**Hinweis**: Sie können die ID des Arbeitszeittabellengenehmigers nicht ändern, wenn Arbeitszeittabellen vorhanden sind, die noch nicht verarbeitet wurden und die den Status Übermittelt oder **Übermittelt** oder **Offen** haben.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)  
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

