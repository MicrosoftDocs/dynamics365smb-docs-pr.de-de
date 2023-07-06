---
title: Finanzinformationen Schnellstart
description: 'Bereiten Sie Ihr Unternehmen auf das Geschäft vor, indem Sie die Finanzinformationen in Business Central einrichten.'
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a>Finanzinformationen Schnellstart

Nach Eingabe grundlegender Unternehmensinformationen in[!INCLUDE[prod_short](includes/prod_short.md)], ist einer der nächsten Schritte das Ausfüllen des Finanzteils. Sie tun dies nicht nur, um Zahlungen zu erhalten oder zu leisten, sondern auch um die Nummern Ihres Unternehmens ordnungsgemäß zu verwalten und zu melden.

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Der Kontenplan

Der Kontenplan (COA) bietet einen Überblick über die Finanzen des Unternehmens und listet Konten in strukturierten Gruppen wie Vermögenswerte, Verbindlichkeiten, Einnahmen, Herstellungskosten und Ausgaben auf. [!INCLUDE[prod_short](includes/prod_short.md)] umfasst einen Standardkontenplan, den Sie an Ihre Buchhaltungspraktiken anpassen können.

## <a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a>Die Kontenpläne einrichten

Das folgende Video zeigt Ihnen, wie Sie den Kontenplan in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a>Dem Kontenplan ein Konto hinzufügen

So fügen Sie ein Konto hinzu, das nicht standardmäßig in [!INCLUDE[prod_short](includes/prod_short.md)] enthalten ist – zum Beispiel Gartendienste. Folgen Sie einfach diesen Schritten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"). Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Sachkontokarte** die Aktion **Neu** aus.
3. Geben Sie die folgenden Daten in den entsprechenden Feldern im Inforegister **Allgemein** ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Feld | Daten |
   | --- | --- |
   | **Nr.** | 61250 |
   | **Name** | Gartendienste |
   | **GuV/Bilanz** | Gewinn- und Verlustrechnung |
   | **Kontokategorie** | Ausgabe |
   | **Kontounterkategorie** | Ausgaben für Reparaturen und Instandhaltung |
   | **Soll/Haben** | Beide |
   | **Kontoart** | Buchen |

4. Geben Sie auf dem Inforegister **Buchung** die folgenden Informationen ein:

   | Feld | Daten |
   | --- | --- |
   | **Buchungsart** | Einkauf |
   | **Geschäftsbuchungsgruppe** | Inland |
   | **Produktbuchungsgruppe** | Dienstleistungen |

5. Füllen Sie auf der Seite **Sachkontokarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a>Verschaffen Sie sich einen Überblick über den Kontenplan

Wenn Sie ein kompaktere Ansicht des Kontenplans benötigen, z. B. ohne Spalten für Buchungskreise, Buchungsart oder Kostenart, listet die **Übersicht Kontenplan** die wichtigsten Informationen für jedes Konto in einer kleineren Tabelle auf. Darüber hinaus können Sie Gruppen reduzieren oder erweitern, um die darin enthaltenen Konten auszublenden.

Um die Übersicht anzuzeigen, wählen Sie die Aktion **Übersicht Kontenplan** auf der Seite **Kontenplan** oder suchen Sie mit nach der Funktion ![Glühbirne, die die Tell Me-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?").

Erfahren Sie mehr über den Kontenplan und das Hauptbuch unter [Das Hauptbuch und den Kontenplan verstehen](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a>Bankkonten einrichten

Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)] registrieren Bankgeschäfte und sind mit Eintragungen im Kontenplan verbunden. Das folgende Video zeigt Ihnen, wie Sie Bankkonten einrichten.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Bankkonten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Bankkonten** die Aktion **Neu** aus.
3. Geben Sie im Feld **Nr.** Feld, eine Kennung wie *B010* wird automatisch eingetragen, wenn für Bankkonten eine Nummernkreisliste eingestellt ist. Wenn nicht, geben Sie eine eindeutige Kombination ein.

   Das Feld unterscheidet sich vom Feld **Bankkonto Nr.**, das auch im **Allgemein** Inforegister verfügbar ist.
4. Füllen Sie auf der Seite **Bankkontokarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Die Kontenpläne einrichten](finance-setup-chart-accounts.md)  
[Bankkonten einrichten](bank-how-setup-bank-accounts.md)  
[Berichte ausführen und drucken](ui-work-report.md)  
[Business Central Schnellstarts](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
