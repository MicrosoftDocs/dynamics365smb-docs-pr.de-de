---
title: "Informationen für Kontakte einrichten | Microsoft Docs"
description: "Gliedert die Aufgaben und Informationen, Codes zum Beispiel über Branchen und Geschäftsbeziehungen festzulegen, bevor Sie Kontakte erstellen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: de-de
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Kontakte einrichten
Beim Erstellen von Kontakten können Sie spezifische Informationen wie die Branche, der die Kontaktunternehmen angehören, oder die Geschäftsbeziehung, die mit den Kontakten besteht, eingeben.

Vor dem Erstellen von Kontakten und dem Erfassen von Details zur jeweiligen Geschäftsbeziehung müssen unterschiedliche Codes eingerichtet werden, mit deren Hilfe die Informationen den Kontaktunternehmen und -personen zugeordnet werden. Codes können für Verteiler, Branchen, Geschäftsbeziehungen, Internetfavoriten, Positionen und Verantwortlichkeiten eingerichtet werden.

Sind diese Informationen eingerichtet, gestaltet sich das Erstellen von Kontakten wesentlich organisierter. Dank der Möglichkeit, alle Kontakte auf der Grundlage einer Gruppe zu suchen, wird die Arbeit deutlich effizienter. Die Informationen stehen allen Gruppen innerhalb des Unternehmens zur Verfügung, was eine erfolgreichere Kommunikation mit den Kontakten ermöglicht.

In Verbindung mit dem Einrichten der Kontakte müssen Sie die Geschäftsbeziehung einrichten, die Sie mit Kontakten haben, zum Beispiel Interessent, Bank, Berater und Dienstleister. Weitere Informationen finden Sie unter [Geschäftsbeziehung für Kontakt-Mandanten einrichten](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Einrichten von Branchen für Kontaktunternehmen
Branchen werden verwendet, um die Branche anzugeben, zu der Ihre Kontakte gehören z. B. die Einzelhandelsbranche und die Automobilbranche.

Die Nutzung von Branchen zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Branchenscode. Sie müssen diesen Schritt nur einmal für jede Branche ausführen. Sobald Sie einen Branchencode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

> [!NOTE]  
>   Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.

### <a name="to-define-an-industry-group-code"></a>Branchengruppencode definieren
Der Branchencode definiert die Art oder die Kategorie der Gruppe, z. B. WERBUNG für Werbung oder PRESSE für TV und Radio. Sie können mehrere Branchencodes haben. Um die Branchen zu definieren, verwenden Sie die **Branchen**-Seite.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Branchengruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

### <a name="AssignIndustryGroupContact">Um einem Kontakt eine Branche zuzuordnen:</a>
Sie können Branchen nicht zu Personen zuordnen – nur zu Unternehmen.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Branchen**-Aktion aus. Die Seite **Kontakt Branchen** wird geöffnet.
3. Wählen Sie im Feld **Branchencode** die Branchen aus, die Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Branchen einzurichten. Sie können in dem Fenster Kontaktübersicht ebenfalls Branchen zuordnen, indem Sie denselben Schritten folgen.

Die Anzahl der Branchen, die Sie dem Kontakt zugeordnet haben, wird im Feld **Anzahl Branchen** im Inforegister **Segmentierung** auf der Seite **Kontakt** angezeigt.

Nachdem Sie Ihren Kontakten Branchen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Einrichten von Verteilern für Kontakte
Verteiler werden verwendet, um Kontaktgruppen zu identifizieren, die dieselben Informationen erhalten sollen. Sie können z. B. einen Verteiler für die Kontakte erstellen, denen Sie eine Benachrichtigung über einen Büroumzug schicken möchten.

Die Nutzung von Verteilern zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Verteilercode. Sie müssen diesen Schritt nur einmal für jeden Verteiler ausführen. Sobald Sie einen Verteilercode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

### <a name="to-define-mailing-group-codes"></a>Definieren eines Verteilercodes
Der Verteilercode definiert die Art oder die Kategorie der Gruppe, z. B. UMZUG für einen Büroumzug, oder GESCHENK für ein Geburtstagsgeschenk. Sie können mehrere Branchencodes haben. Um die Branchen zu definieren, verwenden Sie die **Verteiler**-Seite.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versandgruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

### <a name="AssignMailGroupContact">Um einem Kontakt einen Verteiler zuzuordnen:</a>
1. Öffnen Sie den Kontakt.
2. Wählen Sie die **Verteiler**-Aktion aus. Die Seite **Kontakt Verteiler** wird geöffnet.
3. Wählen Sie im Feld **Verteilercode** den Verteiler aus, den Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Verteiler einzurichten. Außerdem können Sie Verteiler auf die gleiche Art in dem Fenster Kontaktübersicht zuordnen.

Die Anzahl der dem Kontakt zugeordneten Verteiler wird im Feld **Anzahl Verteiler** im Abschnitt **Segmentierung** auf der Seite **Kontakt** angezeigt.

Sobald Sie Ihren Kontakten Verteiler zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Einrichten einer alternativen Adresse für einen Kontakt
Sie können Ihren Kontakten alternative Adressen zuordnen, an die Sie manchmal Post und Informationen senden, zum Beispiel an die Urlaubsadresse. Sie können jeder alternativen Adresse einen oder mehrere Datumsbereiche zuordnen, um festzulegen, wann diese Adresse gültig ist.

### <a name="to-assign-an-alternate-address"></a>So ordnen Sie eine alternative Adresse zu
1. Öffnen Sie den Kontakt.
2. Wählen Sie die **Alternative Adresse**-Aktion aus, und wählen Sie dann **Karte**. Die Seite **Alt. Kontaktadressenübersicht** wird geöffnet.
3. Geben Sie eine neue alternative Adresse ein, und füllen Sie die restlichen Felder der Seite **Kontakt alternative Adresse** aus.

Wiederholen Sie diese Schritte, um weitere alternative Adressen einzurichten. Für jede alternative Adresse können Sie eine oder mehrere Gültigkeiten einrichten.

Außerdem können Sie alternative Adressen auf die gleiche Art auf der Seite Kontaktliste zuweisen.

### <a name="to-assign-an-alternate-address-date-range"></a>Um alternative Adressgültigkeiten zuzuordnen
1. Öffnen Sie den Kontakt.
2. Wählen Sie die **Alternative Adresse**-Aktion aus, und wählen Sie dann **Datumsbereich**. Die Seite **Alt. Kontaktadr.-Gültigkeiten** wird geöffnet.
3. Wählen Sie die Aktion **Neu** aus.
4. Im **Alt. Kontaktadresscode**-Feld wählen Sie eine alternative Adresse für diesen Kontakt aus und füllen dann **Startdatum** und **Enddatum** aus.

Wiederholen Sie diese Schritte, um beliebig viele Gültigkeiten einzurichten.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Einrichten von Aufgaben-Verantwortlichkeiten von Kontaktpersonen
Sie können Informationen zu den Verantwortlichkeiten von Kontaktpersonen hinzufügen, um anzuzeigen, wofür eine Kontaktperson innerhalb ihres Unternehmens zuständig ist z. B. IT, Management oder Produktion. Sie können diese Informationen nutzen, wenn Sie Informationen über Ihre Kontakte eingeben.

Die Verwendung von Verantwortlichkeiten zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Verantwortlichkeitscode. Sie müssen diesen Schritt nur einmal für jede Verantwortlichkeit ausführen. Sobald Sie einen Verantwortlichkeitscode haben, können Sie den Code zu den Kontaktpersonen zuweisen.

### <a name="to-define-a-job-responsibility-code"></a>um einen Verantwortlichkeitscode zu definieren
Der Verantwortlichkeitscode definiert die Art oder die Kategorie des Projekts (z. B. MARKETING oder EINKAUFS). Sie können mehrere Verantwortlichkeitscodes haben. Um die Verantwortlichkeit zu definieren, verwenden Sie die **Verantwortlichkeiten**-Seite.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Auftragsverantwortlichkeiten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Kontaktpersonen Verantwortlichkeiten zuordnen
Sie können keine Verantwortlichkeit zu Kontaktunternehmen zuordnen.

1. Öffnen Sie die Kontaktperson.
2. Wählen Sie die **Person**-Aktion aus, und wählen Sie dann die **Verantwortlichkeiten**-Aktion aus. Die Seite **Kontakt Verantwortlichkeiten** wird geöffnet.
3. Wählen Sie im Feld **Verantwortlichkeitscode** die Verantwortlichkeit aus, die Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Verantwortlichkeiten zuzuordnen. Außerdem können Sie Verantwortlichkeiten auf die gleiche Art in der Kontaktübersicht zuordnen.

Die Anzahl der Verantwortlichkeiten, die Sie dem Kontakt zugeordnet haben, wird im Feld **Anzahl Verantwortlichkeit** im Inforegister **Segmentierung** auf der Seite **Kontakt** angezeigt.

Sobald Sie Ihren Kontakten Verantwortlichkeiten zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Einrichten von Position für Kontaktpersonen
Sie können Ihren Kontakten Positionen zuordnen, um zu bestimmen, welche Position sie innerhalb ihres Unternehmens innehaben (beispielsweise Topmanagement). Sie können diese Informationen nutzen, wenn Sie Informationen über Ihre Kontakte eingeben.

Die Nutzung von Positionen zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Positionscode. Sie müssen diesen Schritt nur einmal für jede Position ausführen. Sobald Sie einen Positionscode haben, können Sie den Code zu den Kontaktpersonen zuweisen.

### <a name="to-define-an-organizational-level-code"></a>Um einen Organisationsstufencode zu definieren
Der Positionscode definiert die Art oder die Kategorie der Position (z. B. CEO oder CFO). Sie können mehrere Positionscodes haben. Um die Position zu definieren, verwenden Sie die **Positionen**-Seite.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Organisationsstufen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Um Organisationsstufen einer Kontaktperson zuzuweisen
Sie können Positionen nur zu Kontaktpersonen zuweisen, nicht zu Unternehmen. Sie können jedem Kontakt nur eine Position zuordnen.

1. Öffnen Sie den Kontakt.
2. Wählen Sie im Feld **Positionen** den Code aus, den Sie zuordnen möchten.

Nachdem Sie Ihren Kontakten Positionen zugeordnet haben, können Sie diese Informationen verwenden, um Segmente zu erstellen.

Sobald Sie Ihren Kontakten Verantwortlichkeiten zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Einrichten von Internetfavoriten für Kontaktunternehmen
Sie können Ihren Kontakten Internetfavoriten (z. B. Suchmaschinen und Websites) zuordnen, um anzuzeigen, wo Sie im Internet nach Informationen über die Kontakte suchen möchten. Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.

Die Nutzung von Internetfavoriten zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Internetfavoritencode. Sie müssen diesen Schritt nur einmal für jeden Internetfavoriten ausführen. Sobald Sie einen Internetfavoritencode haben, können Sie den Code zu den Kontaktpersonen zuweisen.

### <a name="to-define-a-web-source-code"></a>um einen Internetfavoritencode zu definieren
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Webressourcen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder **Code**, **Beschreibung** und **URL** aus.

    Geben Sie %1 im Feld **URL** ein, um einen Platzhalter für einen Suchbegriff in der URL einzufügen. Wenn Sie den Internetfavoriten von einer Kontaktkarte aus aktivieren, wird "%1" automatisch durch das Suchwort ersetzt (z. B. den Namen eines Unternehmens), das Sie auf der Seite **Kontakt-Internetfavoriten** eingegeben haben.

Wiederholen Sie diese Schritte, um weitere Internetfavoriten einzurichten.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Um Internetfavoriten zu einem Kontaktunternehmen zuzuordnen
Wenn Sie Internetfavoriten zuordnen, legen Sie fest, welche Suchmaschine und welchen Suchbegriff die Anwendung bei der Suche nach der gewünschten Information verwendet.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Internetfavoriten**-Aktion aus. Die Seite **Kontakt Internetfavoriten** wird geöffnet.
3. Wählen Sie im Feld **Internetfavoritencode** den Internetfavoriten aus, den Sie zuordnen möchten.
4. Geben Sie im Feld **Suchbegriff** den Suchbegriff ein, der bei der Suche nach der Information verwendet werden soll.

Wiederholen Sie diese Schritte, um weitere Internetfavoriten zuzuordnen.

Außerdem können Sie Internetfavoriten auf die gleiche Art auf der Seite **Kontaktübersicht** zuordnen.

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Verkaufschancen verwalten](marketing-manage-sales-opportunities.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

