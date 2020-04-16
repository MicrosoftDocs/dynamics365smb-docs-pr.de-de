---
title: Einrichten von Ressourcenkosten, Preise und Kapazität| Microsoft Docs
description: Um Ressourcen zu verwenden und Projektmanagement zu erleichtern, können Sie Kosten und Preisen für einzelne Ressourcen oder Ressourcengruppen angeben und die die Ressourcenkapazität festlegen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 08e8f00a73b6c03978d8c00b23f36e3f510c43d6
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191139"
---
# <a name="set-up-resources"></a>Ressourcen einrichten
Zur ordnungsgemäßen Verwaltung von Ressourcenaktivitäten ist die Einrichtung von Ressourcen sowie der zugehörigen Kosten und Preise erforderlich. Die projektbezogenen Preise, Rabatte und Kostenfaktorregeln werden auf der Projektkarte eingerichtet. Die Kosten und Preise können für einzelne Ressourcen, für Ressourcengruppen oder für alle verfügbaren Ressourcen des Unternehmens angegeben werden.

Wenn Ressourcen im Rahmen eines Projekts verbraucht oder verkauft werden, werden die zugehörigen Preise/Kosten aus den Informationen abgerufen, die Sie eingerichtet haben.

Der standardmäßige Betrag pro Stunde wird bei der Ressourcenerstellung angegeben. Wird also beispielsweise eine bestimmte Maschine fünf Stunden lang für ein Projekt verwendet, erfolgt die Berechnung des Projekts auf der Grundlage des Betrags pro Stunde.

> [!NOTE]
> Sie können externe Ressourcen kaufen, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen. Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).<br /><br />
> In diesem Fall wird empfohlen, dass Sie solche externen Ressourcen benennen oder gruppieren, um ihren Zweck anzugeben, damit sie nicht mit Ihren internen Ressourcen verwechselt werden.

## <a name="to-set-up-a-resource"></a>So richten Sie eine Ressource ein
Erstellen Sie für jede Ressource eine Karte,die Sie in " Projekte verwenden möchten.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol öffnet, geben Sie **Ressourcen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Eine Ressourcengruppe einrichten
Mehrere Ressourcen können in einer Ressourcengruppe zusammengefasst werden. Alle Kapazitäten und Budgets der einzelnen Ressourcen werden für die Ressourcengruppe aufsummiert. Es ist ebenfalls möglich, Kapazitäten unabhängig von den summierten Werten oder zusätzlich einzugeben.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Ressourcengruppen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-capacity-for-a-resource"></a>So legen Sie die Kapazität für eine Ressource fest
Um zu berechnen wie viel Zeit eine Ressource in Projekten verbringen kann, muss deren Kapazität zuerst als verfügbare Zeit pro Periode im Arbeitskalender eingerichtet werden. Diese Einstellungen werden verwendet, wenn Sie Projektplanungszeilen ausfüllen, die die Ressource enthalten. Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Ressourcen** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf die Aktion **Ressourcenkapazität**.
3. Geben Sie auf der Seite **Ressourcenkapazität** im Feld **Anzeigen nach** die Länge der Periode an, wie beispielsweise **Tag**, die in Spalten im Inforegister **Ressourcenkapazität – Matrix** angezeigt wird.
4. Für jede Ressource in einer Zeile geben Sie für jede Periode in den Spalten die Anzahl von Stunden an, für die die Ressource verfügbar ist.
5. Alternativ, um die wöchentliche Kapazität der Ressource im Detail innerhalb eines Start- und Enddatums anzugeben, wählen Sie die Aktion **Kapazität festlegen** aus.
6. Füllen Sie auf der Seite **Res.-Kapazität Einstellungen** die Felder nach Bedarf aus.
7. Wählen Sie die Aktion **Kapazität aktualisieren** aus. Die Seite **Ressourcenkapazität** wird mit der eingegebenen Kapazität aktualisiert.
8. Schließen Sie die Seite.

## <a name="to-set-up-alternate-resource-costs"></a>Um alternative Ressourcenkosten einzurichten:
Zusätzlich zu den Kosten, die in der Ressourcenkarte angegeben werden, können Sie auch alternative Kosten für jede Ressource einrichten. Wenn z. B. ein Mitarbeiter einen anderen Stundensatz für Überstunden hat, können Sie für diesen Arbeitstyp einen Einstandspreis einrichten. Die alternativen Kosten, die Sie für die Ressource einrichten, übersteuert den Einstandspreis auf der Ressourcenkarte, wenn Sie die Ressource im Ressourcen Buch.-Blatt buchen.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Ressourcen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Ressource, für die das Sie mindestens alternativen Einstandspreis einrichten möchten, und wählen die Aktion **Kosten** aus.  
3. Füllen Sie auf der Seite **Ressourcenkosten** die Felder auf einer Zeile nach Bedarf aus.  
4. Wiederholen Sie Schritt 3 für jeden alternativen Einstandspreis, den Sie einrichten möchten.

**Hinweis**. Wenn Sie einen Ressourcen-EK-Preis einrichten möchten, der für alle Ressourcen und Ressourcengruppen gültig ist, öffnen Sie die Seite **Ressourcen Einst.-Pr.**, und füllen Sie die Felder aus.

## <a name="to-set-up-alternate-resource-prices"></a>Um alternative Ressourcenkosten einzurichten:
Zusätzlich zu den Kosten, die in der Ressourcenkarte angegeben werden, können Sie auch alternative Kosten für jede Ressource einrichten. Diese alternativen Preise können von Bedingungen abhängig sein. D. h. sie können davon abhängen, ob diese Ressource in einem bestimmten Projekt oder für einen bestimmten Arbeitstyp verwendet wird.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Ressourcen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Ressource, für die das Sie mindestens alternativen Einstandspreis einrichten möchten, und wählen die Aktion **Kosten** aus.
3. Füllen Sie auf der Seite **Ressourcenpreise** die Felder auf einer Zeile nach Bedarf aus.
4. Wiederholen Sie Schritt 3 für jeden alternativen Ressourcenpreis, den Sie einrichten möchten.

## <a name="see-also"></a>Siehe auch
[Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)  
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
