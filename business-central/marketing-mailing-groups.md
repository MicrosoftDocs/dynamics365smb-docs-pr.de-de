---
title: "Versandgruppen für Kontakte einrichten| Microsoft Docs"
description: Einrichten von Verteilern zum Identifizieren von Kontaktgruppen, denen die gleichen Informationen zugehen sollen, z. B. Marketingkampagnen oder Promotionen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a7b9c39b1f213bf2b09ee24e3e6172df027e042c
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Einrichten von Verteilern für Kontakte
Verteiler werden verwendet, um Kontaktgruppen zu identifizieren, die dieselben Informationen erhalten sollen. Sie können z. B. einen Verteiler für die Kontakte erstellen, denen Sie eine Benachrichtigung über einen Büroumzug schicken möchten.

Die Nutzung von Verteilern zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Verteilercode. Sie müssen diesen Schritt nur einmal für jeden Verteiler ausführen. Sobald Sie einen Verteilercode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

## <a name="to-define-mailing-group-codes"></a>Definieren eines Verteilercodes
Der Verteilercode definiert die Art oder die Kategorie der Gruppe, z. B. UMZUG für einen Büroumzug, oder GESCHENK für ein Geburtstagsgeschenk. Sie können mehrere Branchencodes haben. Um die Branchen zu definieren, verwenden Sie das **Verteiler**-Fenster.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versandgruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

## <a name="AssignMailGroupContact">Um einem Kontakt einen Verteiler zuzuordnen:</a>
1. Öffnen Sie den Kontakt.
2. Wählen Sie die **Verteiler**-Aktion aus. Das Fenster **Kontakt Verteiler** wird geöffnet.
3. Wählen Sie im Feld **Verteilercode** den Verteiler aus, den Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Verteiler einzurichten. Außerdem können Sie Verteiler auf die gleiche Art in dem Fenster Kontaktübersicht zuordnen.

Die Anzahl der dem Kontakt zugeordneten Verteiler wird im Feld **Anzahl Verteiler** im Abschnitt **Segmentierung** im Fenster **Kontakt** angezeigt.

Sobald Sie Ihren Kontakten Verteiler zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Siehe auch
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  
[Kontaktpersonen erstellen](marketing-create-contact-persons.md)  
[Arbeiten mit  Business Central](ui-work-product.md)

