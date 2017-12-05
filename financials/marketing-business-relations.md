---
title: "Vorbereiten zur Einrichtung von Geschäftsbeziehungscodes für Kontakte | Microsoft Docs"
description: "Geschäftsbeziehungen in Dynamics 365 werden verwendet, um das Marketing zu erleichtern und um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Interessenten, Kunden und Debitoren haben, wie z. B. Bank oder Dienstleister."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: ee7373ae4b58ce0d31bed5fbf853ae8e039833d4
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Einrichten von Geschäftsbeziehungen für Kontaktunternehmen
Sie können Geschäftsbeziehungen verwenden, um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Kontakten haben wie z. B. Interessent, Bank, Berater und Dienstleister usw. pflegen.

Die Nutzung von Geschäftsbeziehungen zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Geschäftsbeziehungscode. Sie müssen diesen Schritt nur einmal für jede Geschäftsbeziehung ausführen. Sobald Sie einen Geschäftsbeziehungscode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

> [!NOTE]  
>   Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.

## <a name="to-define-a-business-relation-code"></a>Definieren eines Geschäftsbeziehungscodes
Der Geschäftsbeziehungscode definiert eine Kategorie oder einen Typ von Geschäftsbeziehung wie BANK oder Gesetz. Sie können mehrere Geschäftsbeziehungscodes haben. Um die Geschäftsbeziehung zu definieren, verwenden Sie das **Geschäftsbeziehungen**-Fenster.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Geschäftsbeziehungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

## <a name="AssignBusRelContact">Um Kontakten Geschäftsbeziehungen zuzuordnen:</a>
Sie können Geschäftsbeziehungen nicht zu Personen zuordnen – nur zu Unternehmen.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Geschäftsbeziehungen**-Aktion aus.

    Das Fenster **Kontakt Geschäftsbeziehungen** wird angezeigt.
3. Wählen Sie im Feld **Geschäftsbeziehungscode** die Geschäftsbeziehung aus, die Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Geschäftsbeziehungen zuzuordnen. Außerdem können Sie Geschäftsbeziehungen auf die gleiche Art in dem Fenster Kontaktübersicht zuordnen.

Die Anzahl der Geschäftsbeziehungen, die Sie dem Kontakt auf der Kontaktkarte zugeordnet haben, wird im Feld **Anzahl Geschäftsbeziehungen** im Abschnitt **Segmentierung** im Fenster **Kontakt** angezeigt.

Nachdem Sie Ihren Kontakten Geschäftsbeziehungen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Siehe auch
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

