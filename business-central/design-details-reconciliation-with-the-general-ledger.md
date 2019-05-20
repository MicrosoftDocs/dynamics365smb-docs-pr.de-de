---
title: 'Designdetails: Abgleich mit der Finanzbuchhaltung | Microsoft Docs'
description: Dieses Thema beschreibt die Abstimmung mit der Fibu, wenn Sie Lagertransaktionen buchen, z. B.  Verkaufslieferungen, Fertigerzeugnisse oder negative Anpassungen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, reconciliation, general ledger, inventory
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2cb3e743dfd28e96a404209f086caa3f9e84be6c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241689"
---
# <a name="design-details-reconciliation-with-the-general-ledger"></a>Designdetails: Abgleich mit der Finanzbuchhaltung
Wenn Sie Lagertransaktionen buchen, z. B. Verkaufslieferungen, Einkaufsrechnungen, Fertigprodukte aus der Produktion oder Abgängen, werden die Mengen- und die Wertänderungen des Lagerbestandes in den Artikelposten bzw. in den Wertposten festgehalten. Verkaufslieferungen, Einkaufsrechnungen, Fertigprodukte aus der Produktion oder Abgänge, werden die Mengen- und die Wertänderungen des Lagerbestandes in den Artikelposten bzw. in den Wertposten festgehalten.  

Es gibt zwei Möglichkeiten, Inventurposten mit der Finanzbuchhaltung abzustimmen:  

* Manuell, indem die Stapelverarbeitung **Lagerreg. buchen** ausgeführt wird.  
* Automatisch, bei jeder Buchung einer Lagertransaktion.  

## <a name="post-inventory-cost-to-gl-batch-job"></a>Buchen der Stapelverarbeitung "Lagerregulierung buchen"  
Wenn Sie diesen **Lagerreg. buchen** Batchauftrag ausführen, werden auf Basis der Wertposten allgemeine Hauptbuchungsposten erstellt. Sie können Sachposten für die einzelnen Wertposten summieren oder Sachposten für jede Kombination aus Buchungsdatum, Lagerortcode, Lagerbuchungsgruppe, Geschäftsbuchungsgruppe und Produktbuchungsgruppe erstellen.  

Die Buchungsdaten der Sachposten werden auf das Buchungsdatum des entsprechenden Wertpostens gesetzt, außer wenn der Wertposten in eine geschlossene Buchhaltungsperiode fällt. In diesem Fall wird der Wertposten übersprungen, und Sie müssen entweder die Finanzbuchhaltung-Einrichtung oder die Benutzereinrichtung ändern, um Buchungen in dem Datumsbereich zu ermöglichen.  

Während Sie die Stapelverarbeitung **Lagerreg. buchen** ausführen, könnten Sie auf Fehler treffen, die ihre Ursache in fehlender Einrichtung oder nicht kompatibler Dimensionseinrichtung haben. Wenn die Stapelverarbeitung auf Fehler in der Dimensionseinrichtung stößt, setzt sie diese Fehler außer Kraft und verwendet die Dimensionen des Wertpostens. Bei anderen Fehlern überspringt die Stapelverarbeitung das Buchen der Wertposten und listet die Fehler am Ende des Berichts im Abschnitt **Übersprungene Artikel**auf. Um diese Artikel buchen zu können, müssen Sie zunächst die Fehler beheben. Wenn Sie eine Liste der Fehler anzeigen möchten, bevor Sie die Stapelverarbeitung **Lagerreg. buchen** ausführen, führen Sie den Bericht  Lagereinstandspreise buchen - Test aus. In dem Testbericht werden alle Fehler aufgelistet, die während der Testbuchung aufgetreten sind. Sie können die Fehler dann beheben und die Stapelverarbeitung zum Buchen der Lagerregulierung ausführen, ohne dass Posten übersprungen werden.  

## <a name="automatic-cost-posting"></a>Automatische Kostenbuchung  
Um einzurichten, dass Kostenbuchung in der Finanzbuchhaltung automatisch ausgeführt wird, wenn Sie eine Lagertransaktion buchen, wählen Sie das **Kosten automatisch buchen**-Kontrollkästchen auf der Seite **Bestand einrichten** aus. Das Buchungsdatum des Sachpostens ist das gleiche wie das Buchungsdatum des Artikelpostens.  

## <a name="account-types"></a>Kontoarten  
Während der Abstimmung werden Bestandswerte zum Bestandskonto auf der Bilanz gebucht. Der gleiche Betrag, aber mit umgekehrtem Vorzeichen, wird in das entsprechende Gegenkonto gebucht. Normalerweise ist das Gegenkonto ein GuV-Konto. Wenn Sie direkte Kosten im Zusammenhang mit Verbrauch oder Ausgabe buchen, ist das Gegenkonto jedoch ein Bilanzkonto. Die Art des Artikelpostens und des Wertpostens bestimmt, auf welches Sachkonto gebucht wird.  

Die Postenart gibt an, in welches Sachkonto die Buchung vorgenommen werden soll. Dieses wird entweder durch das Vorzeichen der Menge im Artikelposten oder der bewerteten Menge im Wertposten bestimmt, da die Mengen immer das gleiche Vorzeichen haben. Beispielsweise beschreibt ein Verkaufsposten mit einer positiven Menge eine Bestandsabnahme durch einen Verkauf, und ein Verkaufsposten mit negativer Menge beschreibt eine Bestandszunahme durch eine Verkaufsreklamation.  

### <a name="example"></a>Beispiel  
Das folgende Beispiel zeigt eine Fahrradkette, die aus eingekauften Gliedern gefertigt ist. In diesem Beispiel wird gezeigt, wie die verschiedenen Sachkontoarten in einem typischen Szenario verwendet werden.  

Das Kontrollkästchen **Erwartete Soll-Kosten**, die auf der Seite **Lager-Einrichtung** ausgewählt ist und die folgenden Einstellungen werden festgelegt.  

Die nachstehende Tabelle zeigt, wie das Glied auf der Artikelkarte eingerichtet wird.  

|Feld einrichten|Wert|  
|-----------------|-----------|  
|**Lagerabgangsmethode**|Standard|  
|**Einstandspreis (fest)**|MW 1,00|  
|**Gemeinkostensatz**|MW 0,02|  

Die nachstehende Tabelle zeigt, wie die Kette auf der Artikelkarte eingerichtet wird.  

|Feld einrichten|Wert|  
|-----------------|-----------|  
|**Lagerabgangsmethode**|Standard|  
|**Einstandspreis (fest)**|MW 150,00|  
|**Gemeinkostensatz**|MW 25,00|  

Die nachstehende Tabelle zeigt, wie der Arbeitsplatz auf der Arbeitsplatzkarte eingerichtet wird.  

|Feld einrichten|Wert|  
|-----------------|-----------|  
|**EK-Preis**|MW 2,00|  
|**Neue indirekte Kosten in Prozent**|10|  

##### <a name="scenario"></a>Szenario  
1. Die Benutzer kauft 150 Glieder und bucht die Einkaufsbestellung als erhalten. (Einkauf)  
2. Der Benutzer bucht die Einkaufsbestellung als fakturiert. Dies erstellt einen zuzuordnenden Gemeinkostenbetrag von MW, 3,00 und einen Abweichungsbetrag MW 18,00. (Einkauf)  

    1. Die Interimskonten werden gelöscht. (Einkauf)  
    2. Die direkten Kosten werden gebucht. (Einkauf)  
    3. Die indirekten Kosten werden berechnet und gebucht. (Einkauf)  
    4. Die Einkaufsabweichung wird berechnet und gebucht (nur für Standardkostenartikel). (Einkauf)  
3. Die Benutzer verkauft eine Kette und bucht den Verkaufsauftrag als geliefert. (Verkauf)  
4. Der Benutzer bucht die Verkaufsbestellung als fakturiert. (Verkauf)  

    1. Die Interimskonten werden gelöscht. (Verkauf)  
    2. Kosten der verkauften Waren (COGS) werden gebucht. (Verkauf)  

        ![Ergebnisse aus den Verkäufen, die zu GL-Konten gebucht werden](media/design_details_inventory_costing_3_gl_posting_sales.png "Ergebnisse aus den Verkäufen, die zu GL-Konten gebucht werden")  
5. Der Benutzer bucht einen Verbrauch von 150 Gliedern, der die Anzahl der Links ist, die verwendet werden, um eine Kette herzustellen. (Materialverbrauch)  

    ![Ergebnisse aus den Materialien, die zu GL-Konten gebucht werden](media/design_details_inventory_costing_3_gl_posting_material.png "Ergebnisse aus den Materialien, die zu GL-Konten gebucht werden")  
6. Diese Arbeitsplatzgruppe brauchte 60 Minuten, um die Kette herzustellen. Der Benutzer bucht die Verarbeitungskosten. (Verbrauch, Kapazität)  

    1. Die direkten Kosten werden gebucht. (Verbrauch, Kapazität)  
    2. Die indirekten Kosten werden berechnet und gebucht. (Verbrauch, Kapazität)  

        ![Ergebnisse aus den Kapazitäten, die zu GL-Konten gebucht werden](media/design_details_inventory_costing_3_gl_posting_capacity.png "Ergebnisse aus den Kapazitäten, die zu GL-Konten gebucht werden")  
7. Der Benutzer bucht die Soll-Kosten einer Kette. (Istmeldung)  
8. Der Benutzer beendet den Fertigungsauftrag und führt die Stapelverarbeitung **Kostenanpassung Artikeleinträge** aus. (Istmeldung)  

    1. Die Interimskonten werden gelöscht. (Istmeldung)  
    2. Die direkten Kosten werden vom WIP-Konto zum Bestandskonto übertragen. (Istmeldung)  
    3. Die indirekten Kosten (Gemeinkosten) werden vom Konto für indirekte Kosten zum Bestandskonto übertragen. (Istmeldung)  
    4. Dadurch ergibt sich ein Abweichungsbetrag von MW 157,00. Abweichungen werden nur für Standardkosntenartikel berechnet. (Istmeldung)  

        ![Ergebnisse aus den Ergebnissen, die zu GL-Konten gebucht werden](media/design_details_inventory_costing_3_gl_posting_output.png "Ergebnisse aus den Ergebnissen, die zu GL-Konten gebucht werden")  

        > [!NOTE]  
        >  Der Einfachheit halber wird nur ein Abweichungskonto angezeigt. Real existieren fünf verschiedene Konten:  
        >   
        >  * Materialabweichung  
        >  * Kapazitätsabweichung  
        >  * Abweichung Kapazitätsgemeinkosten  
        >  * Fremdarbeitskostenabweichung  
        >  * Prod.-Gemeinkostenabw.  

9. Der Benutzer bewertet die Kette um von MW 150,00 auf MW 140,00. (Regulierung/Neubewertung/Rundung/Umlagerung)  

    ![Ergebnisse aus den Anpassungen, die zu GL-Konten gebucht werden](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Ergebnisse aus den Anpassungen, die zu GL-Konten gebucht werden")  

Weitere Informationen über das Verhältnis zwischen den Kontotypen und den verschiedenen Arten von Wertposten finden Sie unter [Designdetails. Konten in der Finanzbuchhaltung](design-details-accounts-in-the-general-ledger.md)  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
[Designdetails: Soll-Kosten-Buchen](design-details-expected-cost-posting.md)   
[Designdetails: Kostenregulierung](design-details-cost-adjustment.md)
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
