---
title: Marketingkampagnen in Financials einrichten | Microsoft Docs
description: "Beschreibt, wie Sie Marketingkampagnen in Dynamics 365 for Financials einrichten und durchführen können"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# Verwaltung von Marketingkampagnen
<a id="managing-marketing-campaigns" class="xliff"></a>
Der Einsatz eines fundierten Marketingplans ermöglicht das Erkennen, Gewinnen und Binden von Debitoren. Ein Marketingplan setzt sich aus mehreren Kampagnen und anderen Aktivitäten rund um Ihre Verkaufs- und Marketingaktivitäten zusammen. Beim Planen einer Kampagne müssen Sie entscheiden, welche Kontakte Sie ansprechen möchten, welche Art von Kampagne (beispielsweise Messe oder Direktwerbung) Sie erstellen möchten und welche Verkäufer die einzelnen Aufgaben ausführen sollen.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## Einzelkampagne definieren
<a id="defining-individual-campaigns" class="xliff"></a>
Damit eine Kampagne erstellt werden kann, müssen *Codes für den Kampagnenstatus* eingerichtet werden. Diese Codes vereinfachen das Verwalten der Kampagnen, indem der Kampagne ein Status zugeordnet wird. So können Sie den aktuellen Status der Kampagne sowie den nächsten Schritt der Kampagne ablesen, während die einzelnen Phasen einer Kampagne durchlaufen werden. Sie können Kampagnenstatuscodes im Fenster **Kampagnenstatus** einrichten.

Für jede Kampagne, die Sie nachverfolgen möchten, kann eine *Kampagnenkarte* erstellt werden. Auf diesen Kampagnenkarten finden Sie auch allgemeine Informationen zu den Kampagnen.
Sie können Kampagnenposten löschen, z. B. wenn der Posten eine Aktion speichert, die storniert wurde. Es können nur stornierte Kampagnenposten gelöscht werden.

### Auswählen der Zielgruppe
<a id="selecting-the-target-audience" class="xliff"></a>
Nachdem eine Kampagne erstellt wurde, können Sie mit dem Erstellen von Segmenten für die Kampagnen beginnen und das Zielsegment festlegen. Weitere Informationen finden Sie unter [Segmente verwalten](marketing-segments.md).

### Erfassen von Rabattprozentsätzen
<a id="registering-discount-percentages" class="xliff"></a>
Nachdem Sie Ihre Kampagne eingerichtet haben, entschieden haben, welche Segmente die Kampagne umfassen soll, und das Start- und Enddatum festgelegt haben, erfassen Sie den Rabattprozentsatz, den der Debitor auf die einzelnen Artikel in den Zeilen des Fensters **Verkaufszeilenrabatt** erhält. Sie können die Verkaufspreise der einzelnen Artikel in den Zeilen im Fenster **Verkaufspreise** auch erfassen. Sie können auf beide Fenster von der Kampagnenkarte zugreifen.

 Nachdem Sie die Verkaufspreise/Zeilenrabatte sowie die Segmente auf der Kampagnenkarte eingerichtet haben, müssen Sie sie aktivieren, so dass die Kampagnenpreise/Rabatte in den Zeilen wiedergegeben werden.

> [!NOTE]  
>  Um die Verkaufspreise/Zeilenrabatte zu aktivieren, müssen Sie das gesamte Segment oder nur einzelne Kontakte für die Kampagne markieren. Wenn die Verkaufspreise/Zeilenrabatte für alle Kontakte des Segments gelten sollen, wählen Sie im Fenster **Segment** auf dem Inforegister **Kampagne** das Feld **Kampagnenziel** aus.
Wenn die Verkaufspreise/Zeilenrabatte nicht für alle Kontakte des Segments gelten sollen, können Sie das Feld **Kampagnenziel** für die relevanten Kontakte. Wenn Sie dieses Feld nicht sehen, können Sie es zur Ansicht hinzuzufügen. Weitere Informationen finden Sie unter [Benutzer-Personalisierung](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## Siehe auch
<a id="see-also" class="xliff"></a>
[Kontakte verwalten](marketing-contacts.md)  
[Verwalten von Segmenten](marketing-segments.md)  
[Verkaufschancen verwalten](marketing-manage-sales-opportunities.md)  
[Arbeiten mit Financials](ui-work-product.md)  

