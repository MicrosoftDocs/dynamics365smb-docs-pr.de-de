---
title: "Vorbereiten zur Einrichtung von Versandgruppen für Kontakte | Microsoft Docs"
description: "Beschreibt die Nutzung von Verteilern für Kontakte in Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fc29f5a6238373db3e862058eb327398e624882e
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Einrichten von Verteilern für Kontakte
<a id="setting-up-mailing-groups-for-contacts" class="xliff"></a>
Verteiler werden verwendet, um Kontaktgruppen zu identifizieren, die dieselben Informationen erhalten sollen. Sie können z. B. einen Verteiler für die Kontakte erstellen, denen Sie eine Benachrichtigung über einen Büroumzug schicken möchten.

Die Nutzung von Verteilern zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Verteilercode. Sie müssen diesen Schritt nur einmal für jeden Verteiler ausführen. Sobald Sie einen Verteilercode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

## Definieren eines Verteilercodes
<a id="defining-mailing-group-codes" class="xliff"></a>
Der Verteilercode definiert die Art oder die Kategorie der Gruppe, z. B. UMZUG für einen Büroumzug, oder GESCHENK für ein Geburtstagsgeschenk. Sie können mehrere Branchencodes haben. Um die Branchen zu definieren, verwenden Sie das **Verteiler**-Fenster.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Verteilergruppen** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

## <a name="AssignMailGroupContact">Um einem Kontakt einen Verteiler zuzuordnen:</a>
1. Öffnen Sie den Kontakt.
2. Wählen Sie die **Verteiler**-Aktion aus. Das Fenster **Kontakt Verteiler** wird geöffnet.
3. Wählen Sie im Feld **Verteilercode** den Verteiler aus, den Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Verteiler einzurichten. Außerdem können Sie Verteiler auf die gleiche Art in dem Fenster Kontaktübersicht zuordnen.

Die Anzahl der dem Kontakt zugeordneten Verteiler wird im Feld **Anzahl Verteiler** im Abschnitt **Segmentierung** im Fenster **Kontakt** angezeigt.

Sobald Sie Ihren Kontakten Verteiler zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Vorgehensweise: Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## Siehe auch
<a id="see-also" class="xliff"></a>
[Kontaktunternehmenerstellen](marketing-create-contact-companies.md)  
[Kontaktpersonen erstellen](marketing-create-contact-persons.md)  
[Arbeiten mit Financials](ui-work-product.md)

