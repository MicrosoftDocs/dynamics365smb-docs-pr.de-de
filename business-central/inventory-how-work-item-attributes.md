---
title: Artikel-Attribute einrichten und Artikeln zuordnen| Microsoft Docs
description: "Beschreibt, wie Artikelattributwerte beispielsweise als Suchbegriffe installiert werden, die als Suchwörter verwendet werden können, und sie Artikeln und Artikelkategorien zuzuweisen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3e099dde3ab51a2757bf42ffd4c3044c8007ee0a
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-item-attributes"></a>Arbeiten mit Artikelattributen
Wenn Debitorenanfragen zu einem Artikel, entweder über Korrespondenz oder über einen integrierten Webshop, gestellt werden, fragen oder suchen sie möglicherweise nach bestimmten Eigenschaften, wie z. B. Höhe und Modelljahr. Um diesen Debitornservice zu bieten, können Sie Ihren Artikeln Artikelattributwerte verschiedener Art zuordnen, die dann bei der Suche nach Artikeln verwendet werden können.

Sie können den Artikelkategorien auch Artikelattribute zuordnen, die dann für die Artikel gelten, die die Artikelkategorien verwenden. Weitere Informationen finden Sie unter [Artikel kategorisieren](inventory-how-categorize-items.md).

> [!Tip]  
> Wenn Sie Bildern mit Artikel verknüpfen, kann die Bildanalyse-Erweiterung Attribute im Bild erkennen und die Attribute vorschlagen, so dass Sie entscheiden können, ob Sie diese zuweisen möchten. Die Erweiterung ist bereit. Sie müssen sie nur aktivieren. Weitere Informationen finden Sie unter [Die Bild-Analyzer-Eweiterung](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>So erstellen Sie Artikelattribute
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Artikelkattribute** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Artikelattribute** die Aktion **Neu** aus.
3. Füllen Sie im Fenster **Artikelattribute** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Wenn Sie im Feld Art **Option** das Feld **Typ** ausgewählt haben, können Sie die Aktion **Artikelattributwerte** wählen, um Werte für die Artikelattribute zu erstellen. Weitere Informationen finden Sie im Abschnitt "So erstellen Sie Werte für Artikelattribute vom Typ Option".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>So erstellen Sie Werte für Artikelattribute vom Typ Option
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Artikelkattribute** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Artikelattribute** ein Artikelattribut vom Typ **Option**, für das Sie Werte erstellen möchten, und wählen Sie dann die Aktion **Artikelattributwerte** aus.
3. Füllen Sie im Fenster **Artikelattributwerte** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>So ordnen Sie Artikelattribute Artikeln zu:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Artikel** den Artikel, dem Sie Artikelattribute zuordnen möchten, und wählen Sie die Aktion **Attribute** aus.
3. Wählen Sie im Fenster **Artikelattributewerte** die Aktion **Neu** aus.
4. Klicken Sie im Feld **Attribute** auf die Schaltfläche "Suchen" und wählen Sie ein bereits vorhandenes Artikelattribut aus. Wählen Sie die Aktion **Neu**, um zuerst ein neues Artikelattribut so zu erstellen, wie es im Abschnitt "So erstellen Sie Artikelattribute" erklärt wird.
5. Geben Sie im Feld **Wert** den Artikelattributwert ein, z. B. "2010" als **Modelljahr**-Attribut.
6. Für Artikelattribute vom Typ **Option** klicken Sie auf die Suchen-Schaltfläche im Feld **Wert** und wählen einen Artikelattributwert aus. Wählen Sie die Aktion **Neu**, um zuerst einen neuen Artikelattributwert so zu erstellen, wie es im Abschnitt "So erstellen Sie Werte für Artikelattribute vom Typ Option" erklärt wird.
7. Wiederholen Sie die Schritte 4 bis 6 für alle Artikelattribute, die Sie dem Artikel zuweisen möchten.

## <a name="to-assign-item-attributes-to-item-categories"></a>So ordnen Sie ein Artikelattribut einer Artikelkategorie zu:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Artikelkategorien** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Artikelkategorie** die Artikelkategorie, der Sie den Artikelattributen zuordnen möchten, und wählen Sie die Aktion **Bearbeiten** aus.
3. Wählen Sie im Fenster **Artikelkategorie-Karte** im Inforegister **Attribute** die Aktion **Neu** aus.
4. Klicken Sie im Feld **Attribute** auf die Schaltfläche "Suchen" und wählen Sie ein bereits vorhandenes Artikelattribut aus. Wählen Sie die Aktion **Neu**, um zuerst ein neues Artikelattribut so zu erstellen, wie es im Abschnitt "So erstellen Sie ein Artikelattribut" erklärt wird.
5. Klicken Sie im Feld **Standardwert** auf die Suchen-Schaltfläche und wählen Sie einen bereits vorhandenen Attributwert aus.
6. Wiederholen Sie die Schritte 4 bis 5 für alle Artikelattribute, die Sie der Artikelkategorie zuweisen möchten.

> [!NOTE]  
>   Artikelattribute für übergeordnete Artikelkategorien werden in untergeordneten Artikelkategorien übernommen. Dies wird durch das Feld **Geerbt von** im Inforegister **Attribute** angegeben. Weitere Informationen finden Sie unter [Artikel kategorisieren](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>So filtern Sie nach Artikelattributen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Attribute** die Aktion **Nach Attributen filtern** aus.
3. Klicken Sie im Fenster **Artikel nach Attributen filtern** die Suchschaltfläche im Feld **Attribute** an, und wählen Sie ein Artikelattribut aus.
4. Klicken Sie im Feld **Wert** auf die Suchen-Schaltfläche und wählen Sie einen Attributwert aus, mit dem Sie die Artikel filtern wollen.

    > [!NOTE]  
    >   Sie können nur direkt Werte für Artikelattribute auswählen, die über feste Werte , wie z. B. Farbe, verfügen. Für Artikelattribute, die variable Werte, wie z. B. Breite haben, müssen Sie den Artikelattributwert festlegen, indem Sie zuerst eine Bedingung auswählen. Siehe dazu auch Schritt 5.
5. Klicken Sie im Feld **Wert** für ein variables Artikelattribut auf die Suchen-Schaltfläche.
6. Wählen Sie im Fenster **Filterwert angeben** im Feld **Bedingung** den Dropdownpfeil aus, und wählen Sie dann eine Bedingung aus.
7. Geben Sie im Feld **Wert** einen Attributwert ein, mit dem Sie die Artikel filtern wollen.

    **Beispiel**: Um Artikel zu filtern deren Beschreibung mit "blau" beginnt, füllen Sie die Felder wie folgt aus: **Attribut** -Feld: Materialbeschreibung, **Bedingung**-Feld: beginnt mit, **Wert**-Feld: blau.
8. Wählen Sie die Schaltfläche **OK** aus.   

Die Artikel im Fenster **Artikel** werden mit den angegebenen Artikelattributwerten gefiltert.

## <a name="see-also"></a>Siehe auch
[Artikel kategorisieren](inventory-how-categorize-items.md)    
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

