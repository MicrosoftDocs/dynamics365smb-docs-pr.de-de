---
title: "Einrichten von Branchengruppen für Kontaktunternehmen| Microsoft Docs"
description: Beschreibt, wie eine Branche definiert und diese einem Kontaktunternehmen, beispielsweise Einzelhandelsbranche, oder der Automobilindustrie zuweist.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f1927938bc7e882902d8f609242c529e0ba29cd1
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a>Einrichten von Branchen für Kontaktunternehmen
Branchen werden verwendet, um die Branche anzugeben, zu der Ihre Kontakte gehören z. B. die Einzelhandelsbranche und die Automobilbranche.

Die Nutzung von Branchen zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Branchenscode. Sie müssen diesen Schritt nur einmal für jede Branche ausführen. Sobald Sie einen Branchencode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

> [!NOTE]  
>   Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.

## <a name="to-define-an-industry-group-code"></a>Branchengruppencode definieren
Der Branchencode definiert die Art oder die Kategorie der Gruppe, z. B. WERBUNG für Werbung oder PRESSE für TV und Radio. Sie können mehrere Branchencodes haben. Um die Branchen zu definieren, verwenden Sie das **Branchen**-Fenster.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Branchengruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

## <a name="AssignIndustryGroupContact">Um einem Kontakt eine Branche zuzuordnen:</a>
Sie können Branchen nicht zu Personen zuordnen – nur zu Unternehmen.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Branchen**-Aktion aus. Das Fenster **Kontakt Branchen** wird geöffnet.
3. Wählen Sie im Feld **Branchencode** die Branchen aus, die Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Branchen einzurichten. Sie können in dem Fenster Kontaktübersicht ebenfalls Branchen zuordnen, indem Sie denselben Schritten folgen.

Die Anzahl der Branchen, die Sie dem Kontakt zugeordnet haben, wird im Feld **Anzahl Branchen** im Inforegister **Segmentierung** im Fenster **Kontakt** angezeigt.

Nachdem Sie Ihren Kontakten Branchen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Siehe auch
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

