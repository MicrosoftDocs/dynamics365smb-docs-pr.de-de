---
title: Element-Referenzen verwenden
description: 'Richten Sie Referenzen zwischen den Beschreibungen, Einheiten und Varianten ein, die Sie und Ihr Kreditor oder Debitor für einen Artikel verwenden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: edupont
---
# Element-Referenzen verwenden

Wenn Sie Artikel kaufen oder verkaufen, für die Sie und Ihr Kreditor oder Debitor unterschiedliche Bedingungen verwenden, können Sie eine Referenz zwischen Ihren Bedingungen für die Artikel und den Bedingungen einrichten, die der Debitor oder Kreditor dieses Artikels verwendet. Auf diese Weise wird die Artikelbezeichnung, die Einheit oder der Variantencode des Kreditors oder Debitors beim Ausfüllen des Formulars automatisch in die entsprechenden Dokumente eingefügt **Artikel-Referenz-Nr.** Feld eingetragen.  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Nicht alle Unternehmen verwenden Artikelreferenzen. Wir haben die zugehörigen Felder und Aktionen standardmäßig ausgeblendet, um das Durcheinander auf den Seiten zu minimieren. Wenn Sie sich entscheiden, sie zu verwenden, können Sie auf der Seite **Lagerbestandseinrichtung** das Feld **Artikelreferenzen verwenden** aktivieren. Nachdem Sie die Artikelreferenzen aktiviert haben, sind die Felder und Aktionen auf den Seiten Artikelkarte, Lieferantenkarte und Kundenkarte sowie in Einkaufs- und Verkaufsbelegen verfügbar.
>
> In Versionen vor dem 2. Veröffentlichungszyklus 2021 kann Ihr Administrator die Funktion *Längere Artikelreferenzen schreiben* auf der Seite [Funktionsverwaltung](https://businesscentral.dynamics.com/?page=2610) aktivieren (der Link erfordert, dass Sie einen [!INCLUDE [prod_short](includes/prod_short.md)]-Mandanten haben) aktivieren. Die Verwendung von Referenzen ändert sich nicht, aber die Namen von Dingen wie Seiten und Schaltflächen ändern sich. Aus der Seite **Artikelquerverweisposten** wird beispielsweise die Seite **Artikelreferenzposten**.

## So beginnen Sie mit der Verwendung von Artikelreferenzen

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Wählen Sie das Symbol :::image type="icon" source="media/ui-search/search_small.png" border="false"::: aus, und geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Feld **Artikelreferenzen verwenden**.

## Artikelreferenzen einrichten

1. Wählen Sie das Symbol :::image type="icon" source="media/ui-search/search_small.png" border="false"::: aus, und geben Sie **Artikel** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte eines Elements, für das Sie eine Referenz erstellen möchten.
3. Wählen Sie die Aktion **Artikelverweise**.

     Wenn Sie die Aktion **Artikelverweise** nicht finden können, wählen Sie die Option zum Anzeigen weiterer Optionen und suchen Sie sie dann unter **Verwandt** > **Artikel**.
  
4. Füllen Sie in einer neuen Zeile auf der Seite **Element-Referenz-Einträge** die erforderlichen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Das folgenden Verfahren beschreibt, wie Sie Artikelreferenzen für eine Bestellung angeben. Die gleichen Schritte gelten auch für andere Verkaufs- und Einkaufsbelege.  

## So geben Sie die Artikelbeschreibung eines Kreditors auf einem Beleg ein

1. Wählen Sie das Symbol :::image type="icon" source="media/ui-search/search_small.png" border="false"::: aus, geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie eine Bestellung für den Kreditor, für den Sie im vorherigen Verfahren einen Artikelbezug festgelegt haben.
3. Erstellen Sie eine Kauf-Zeile für den Artikel, für den Sie in der vorherigen Vorgehensweise einen Artikelbezug festgelegt haben.
4. Im Feld **Artikelreferenz-Nr.** und wählen Sie die entsprechende Artikelreferenz aus und wählen dann die Schaltfläche **OK**.

Das Feld **Beschreibung** in der Zeile wird mit der Artikelbeschreibung des Kreditors überschrieben, wie sie auf dem Eintrag für die Artikelreferenz festgelegt wurde. Enthält die Artikelreferenz einen Variantencode oder eine Einheit, werden diese Werte ebenfalls in den Beleg übernommen.  

## Weitere Informationen

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]