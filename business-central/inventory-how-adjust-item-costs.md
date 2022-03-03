---
title: Manuelles Anpassen der Kosten von Artikeln
description: Sie können die Bestandsbewertung eines Elements unter Verwendung der FIFO- oder Durchschnittskalkulation manuell anpassen, wenn sich die Kosten von Artikeln ändern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 2d499d22a51b3bea0367acaee0c650fe4dc67ad5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131639"
---
# <a name="adjust-item-costs"></a>Artikelpreise justieren
Die Kosten eines Artikels (Lagerwert), den Sie ein- und später verkaufen, ändert sich im Laufe der Nutzungsdauer, weil beispielsweise Frachtkosten dem Kaufpreis hinzugefügt werden, nachdem Sie den Artikel verkauft haben. Dies ist insbesondere dann wichtig, wenn Sie Waren verkaufen, bevor der Kauf dieser Waren in Rechnung gestellt wurde. Um immer den richtigen Lagerwert zu kennen, müssen Artikelkosten daher regelmäßig reguliert werden. Dadurch ist sichergestellt, dass die Verkaufs- und Gewinnstatistiken auf dem neuesten Stand sind und die finanziellen Kennziffern korrekt sind. Weitere Informationen finden Sie unter [Designdetails: Kostenanpassung](design-details-cost-adjustment.md)

Als Grundregel gilt, dass der Wert im Feld **Einstandspreis** auf der Artikelkarte für Artikel mit der Lagerabgangsmethode "Standard" auf dem festen Einstandspreis basiert. Für Artikel mit anderen Lagerabgangsmethoden basiert er auf der Berechnung des verfügbaren Lagerbestands (fakturierte und Soll-Kosten), dividiert durch den gezählten Lagerbestand. Weitere Informationen finden Sie unter [Einstandspreisberechnung verstehen](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

In [!INCLUDE[prod_short](includes/prod_short.md)], werden Artikelkosten automatisch jedes Mal reguliert, wenn eine Lagertransaktion auftritt, beispielsweise, wenn Sie eine Einkaufsrechnung für einen Artikel buchen.

Sie können eine Funktion verwenden, um die Kosten einer oder mehrerer Artikel manuell anzupassen. Dies ist beispielsweise dann nützlich, wenn Sie wissen, dass Sie die Artikelpreise aufgrund anderer Ursachen als Artikeltransaktionen geändert haben.

Artikelkosten werden durch die FIFO- oder die Durchschnittskostenmethode, abhängig von Ihrer Auswahl im Leitfaden für das unterstützte Setup in **Mein Unternehmen** oder im Feld **Kostenmethode** auf der Artikelkarte unterstützt. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Wenn Sie die FIFO-Kostenmethode verwenden, dass ist der Einstandspreis eines Artikels der tatsächliche Wert jedes Eingangs des Artikels. Bestand wird mit der Annahme bewertet, dass dess erste Artikel im Lager zuerst verkauft wird.

Wenn Sie die Durchschnittskostenmethode verwenden, dass werden die Einstandskosten als Durchschnittskosten nach dem Kauf berechnet. Bestand wird mit der Annahme bewertet, dass aller Bestand gleichzeitig verkauft wird. Für Artikel, die die Lagerabgangsmethode verwenden, können Sie das Feld **Einstandspreis** auf der Artikelkarte wählen, um die Historie von Transaktionen anzuzeigen, denen der durchschnittliche Einstandspreis berechnet wird

Die Kostenregulierungsfunktion verarbeitet nur Wertposten, die noch nicht reguliert wurden. Liegt eine Situation vor, in der geänderte eingehende Kosten an zugehörige ausgehende Posten weitergeleitet werden müssen, werden dafür neue Regulierungswertposten erstellt, die zwar auf den Informationen der ursprünglichen Wertposten basieren, aber den Regulierungsbetrag enthalten. Die Kostenregulierungsfunktion verwendet das Buchungsdatum des ursprünglichen Wertpostens in den Regulierungsposten, es sei denn, das Datum befindet sich in einer geschlossenen Lagerbuchungsperiode. In diesem Fall verwendet die Anwendung das Startdatum der nächsten offenen Lagerbuchungsperiode verwendet. Werden keine Lagerbuchungsperioden verwendet, definiert das Datum im Feld **Buchungen zugel. ab** auf der Seite **Finanzbuchhaltungs-Einrichtung:**, wann der Regulierungsposten gebucht wird.

## <a name="to-adjust-item-costs-manually"></a>So regulieren Sie Artikelpreise manuell
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerreg. fakt. Einst. Preise anpassen** ein, und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Lagerreg. fakt. Einst. Preise** geben Sie an, für welche Artikel die Kosten anzupassen sind.
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Um allgemeine Änderungen in den direkten Einheitskosten durchzuführen:
Wenn Sie die direkten VK-Preise für mehrere Artikel ändern müssen, können Sie die Stapelverarbeitung **Artikelpreise anpassen** verwenden.  

 Der Batchauftrag ändert den Inhalt des Felds **VK-Preis** auf der Artikelkarte. Die Stapelverarbeitung ändert den Inhalt des Felds auf die gleiche Weise für alle Artikel oder ausgewählten Artikel. Hierzu wird der Wert im Feld mit einem von Ihnen angegebenen Korrekturfaktor multipliziert.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikelpreise justieren** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie im Inforegister Optionen im Feld **Feld korrigieren** an, welche Artikel- oder Lagerhaltungsdatenkarte Sie korrigieren möchten.  
3. Geben Sie im Feld **Korrekturfaktor** den Faktor an, mit dem der Wert korrigiert wird. Beispielsweise geben Sie **1,5** ein, um den Wert um 50 % zu erhöhen.  
4. Legen Sie im Inforegister **Artikel** Filter fest, um beispielsweise anzuzeigen, welche Artikel mit der Stapelverarbeitung zu verarbeiten sind.  
5. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="understanding-unit-cost-calculation"></a>Einstandspreisberechnung verstehen
Als Grundregel gilt, dass der Wert im Feld **Einstandspreis** auf der Artikelkarte für Artikel mit der Lagerabgangsmethode "Standard" auf dem festen Einstandspreis basiert. Für Artikel mit anderen Lagerabgangsmethoden basiert er auf der Berechnung des verfügbaren Lagerbestands (fakturierte und Soll-Kosten), dividiert durch den gezählten Lagerbestand.  

 Wie der Inhalt des Feldes **Lagerabgangsmethode** die Berechnung des Einstandspreises für Einkäufe und Verkäufe von Artikeln beeinflusst, wird detaillierter in den folgenden Abschnitten beschrieben.  

## <a name="unit-cost-calculation-for-purchases"></a>Einstandspreisberechnung bei Einkäufen  
 Wenn Sie Artikel einkaufen, kopiert die Anwendung immer den Wert im Feld **Letzte Direkte Kosten** auf der Artikelkarte in das Feld **Einheit Direkte Kosten** in einer Einkaufszeile oder den Stückpreis in einer Artikel Buch.-Blattzeile.  

 Ihre Auswahl im Feld **Kostenermittlungsmethode** hat Einfluss darauf, wie [!INCLUDE[prod_short](includes/prod_short.md)] den Inhalt des Feldes **Einstandspreis** in den Zeilen berechnet.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Lagerabgangsmethode "FIFO", "LIFO", "Ausgewählt" oder "Durchschnitt"  
 [!INCLUDE[prod_short](includes/prod_short.md)] berechnet den Inhalt des Feldes **Einstandspreis NW** in der Einkaufszeile oder den Inhalt des Feldes **Einstandspreis** in der Artikel Buch.-Blattzeile entsprechend dieser Formel:  

 Einstandspreis (MW) = (EK-Preis - (Rabattbetrag / Menge)) x (1 + Indirekte Kosten % / 100) + Gemeinkostensatz  

### <a name="costing-method-standard"></a>Lagerabgangsmethode "Standard"  
 Die Anwendung füllt das Feld **Einstandspreis (MW)** in einer Einkaufszeile oder das Feld **Einstandspreis** in einer Artikel Buch.-Blattzeile, indem sie den Wert des Felds **Einstandspreis** von der Artikelkarte kopiert. Wenn die Lagerabgangsmethode "Standard" ist, basiert dies auf dem Einstandspreis.  

 Wenn Sie den Einkauf buchen, wird der Einstandspreis aus der Einkaufszeile bzw. der Artikel Buch.-Blattzeile in den Rechnungsposten des eingekauften Artikels kopiert, und Sie können ihn in der Postenübersicht des Artikels einsehen.  

### <a name="all-costing-methods"></a>Alle Lagerabgangsmethoden  
 Die Anwendung verwendet immer den Einstandspreis aus der Herkunftsbelegzeile, um den Inhalt des Feldes **Einstandsbetrag (tatsächl.)** oder, falls anwendbar, des Feldes **Einstandsbetrag (erwartet)** zu berechnen, das zu diesem Artikelposten gehört, unabhängig von der Lagerabgangsmethode des Artikels.  

## <a name="unit-cost-calculation-for-sales"></a>Einstandspreisberechnung für Verkäufe  
 Wenn Sie Artikel verkaufen, kopiert die Anwendung den Einstandspreis immer aus dem Feld Einstandspreis der Artikelkarte in die Verkaufszeile oder die Artikel Buch.-Blattzeile.  

 Beim Buchen wird später der Einstandspreis in den Artikelposten der Verkaufsrechnung übernommen; er wird darüber hinaus in den Artikelposten des jeweiligen Artikels angezeigt. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet den Einstandspreis aus der Herkunftsbelegzeile, um den Inhalt des Feldes **Einstandsbetrag (tatsächl.)** oder, falls anwendbar, des Feldes **Einstandsbetrag (erwartet)** in dem Wertposten zu berechnen, der mit diesem Artikelposten verknüpft ist.  

## <a name="see-also"></a>Siehe auch
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]