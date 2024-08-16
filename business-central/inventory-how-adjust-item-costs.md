---
title: Manuell Anpassen die Kosten der Artikel
description: 'Sie können die Bestandsbewertung eines Elements unter Verwendung der FIFO- oder Durchschnittskalkulation anpassen, wenn sich die Kosten von Artikeln ändern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 07/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Artikelpreise anpassen

Die Kosten eines Artikels (Lagerwert), den Sie ein- und später verkaufen, ändert sich im Laufe der Nutzungsdauer, weil beispielsweise Frachtkosten dem Kaufpreis hinzugefügt werden, nachdem Sie den Artikel verkaufen. Dies ist insbesondere dann wichtig, wenn Sie Waren verkaufen, bevor der Kauf dieser Waren in Rechnung gestellt wurde. Um immer den richtigen Lagerwert zu kennen, sollten Sie die Artikelkosten regelmäßig regulieren. Durch die korrekten Kosten ist sichergestellt, dass die Verkaufs- und Gewinnstatistiken auf dem neuesten Stand sind und die finanziellen Kennziffern korrekt sind. Weitere Informationen finden Sie unter [Designdetails: Kostenanpassung](design-details-cost-adjustment.md)

Der Wert im Feld **Einstandspreis** auf der Artikelkarte für Artikel mit der Lagerabgangsmethode „Standard“ basiert auf dem festen Einstandspreis. Für Artikel mit anderen Lagerabgangsmethoden basiert der Wert auf der Berechnung des verfügbaren Lagerbestands (fakturierte und Soll-Kosten), dividiert durch den gezählten Lagerbestand. Weitere Informationen finden Sie unter [Einstandspreisberechnung verstehen](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

In [!INCLUDE[prod_short](includes/prod_short.md)], werden Artikelkosten automatisch jedes Mal reguliert, wenn eine Lagertransaktion auftritt, beispielsweise, wenn Sie eine Einkaufsrechnung für einen Artikel buchen.

Sie können die Kosten einer oder mehrerer Artikel manuell anpassen. Manuelle Anpassungen sind hilfreich, wenn Sie wissen, dass die Artikelkosten aufgrund anderer Ursachen als Artikeltransaktionen geändert werden.

Artikelkosten werden durch die FIFO- oder die Durchschnittskostenmethode, abhängig von Ihrer Auswahl im Leitfaden für das unterstützte Setup in **Mein Unternehmen** oder im Feld **Kostenmethode** auf der Artikelkarte unterstützt. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).  

Bei der FIFO-Kostenbewertungsmethode ist der Einstandspreis eines Artikels der tatsächliche Wert jedes Eingangs des Artikels. Bestand wird mit der Annahme bewertet, dass der erste Artikel im Lager zuerst verkauft wird.

Wenn Sie die Durchschnittskostenmethode verwenden, dass werden die Einstandskosten als Durchschnittskosten nach dem Kauf berechnet. Bestand wird mit der Annahme bewertet, dass aller Bestand gleichzeitig verkauft wird. Für Artikel, die die Lagerabgangsmethode verwenden, können Sie das Feld **Einstandspreis** auf der Artikelkarte wählen, um die Historie von Transaktionen anzuzeigen, denen der durchschnittliche Einstandspreis berechnet wird

Die Kostenregulierung verarbeitet nur Wertposten, die nicht reguliert werden. In einer Situation, in der geänderte Eingangskosten an zugehörige Ausgangsposten weitergeleitet werden müssen, werden neue Anpassungswertposten erstellt. Die Regulierungswerteinträge basieren auf den Informationen in den ursprünglichen Werteinträgen, enthalten jedoch den Anpassungsbetrag. Die Kostenregulierungsfunktion verwendet das Buchungsdatum des ursprünglichen Wertpostens in den Regulierungsposten, es sei denn, das Datum befindet sich in einer geschlossenen Lagerbuchungsperiode. In diesem Fall verwendet die Anwendung das Startdatum der nächsten offenen Lagerbuchungsperiode verwendet. Werden keine Lagerbuchungsperioden verwendet, definiert das Datum im Feld **Buchungen zugel. ab** auf der Seite **Finanzbuchhaltungs-Einrichtung:**, wann der Regulierungsposten gebucht wird.

## So regulieren Sie Artikelpreise manuell

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerreg. fakt. Einst. Preise anpassen** ein, und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Lagerreg. fakt. Einst. Preise** geben Sie an, für welche Artikel die Kosten anzupassen sind.
3. Wählen Sie die Schaltfläche **OK** aus.

## Um allgemeine Änderungen in den direkten Einheitskosten durchzuführen:

Wenn Sie die direkten VK-Preise für mehrere Artikel ändern müssen, können Sie die Stapelverarbeitung **Artikelpreise anpassen** verwenden.  

Der Batchauftrag ändert den Inhalt des Felds **VK-Preis** auf der Artikelkarte. Die Stapelverarbeitung ändert den Inhalt des Felds auf die gleiche Weise für alle Artikel oder ausgewählten Artikel. Hierzu wird der Wert im Feld mit einem von Ihnen angegebenen Korrekturfaktor multipliziert.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Artikelpreise justieren** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie im Inforegister Optionen im Feld **Feld korrigieren** an, welche Artikel- oder Lagerhaltungsdatenkarte Sie korrigieren möchten.  
3. Geben Sie im Feld **Korrekturfaktor** den Faktor an, mit dem der Wert korrigiert wird. Beispielsweise geben Sie **1,5** ein, um den Wert um 50 %% zu erhöhen.  
4. Legen Sie im Inforegister **Artikel** Filter fest, um beispielsweise anzuzeigen, welche Artikel mit der Stapelverarbeitung zu verarbeiten sind.  
5. Wählen Sie die Schaltfläche **OK** aus.  

## Einstandspreisberechnung verstehen

Der Wert im Feld **Einstandspreis** auf der Artikelkarte für Artikel mit der Lagerabgangsmethode „Standard“ basiert auf dem festen Einstandspreis. Für Artikel mit anderen Lagerabgangsmethoden basiert der Wert auf der Berechnung des verfügbaren Lagerbestands (fakturierte und Soll-Kosten), dividiert durch den gezählten Lagerbestand.  

Wie der Inhalt des Feldes **Lagerabgangsmethode** die Berechnung des Einstandspreises für Einkäufe und Verkäufe von Artikeln beeinflusst, wird detaillierter in den folgenden Abschnitten beschrieben.  

## Einstandspreisberechnung bei Einkäufen  

Wenn Sie Artikel einkaufen, wird der Wert im Feld **EK-Preis (neuester)** auf der Artikelkarte in das Feld **EK-Preis** einer Einkaufszeile oder in die Zeile **Stückpreis** einer Artikel Buch.-Blattzeile kopiert.  

Ihre Auswahl im Feld **Kostenermittlungsmethode** hat Einfluss darauf, wie [!INCLUDE[prod_short](includes/prod_short.md)] den Inhalt des Feldes **Einstandspreis** in den Zeilen berechnet.  

### FIFO, LIFO, ausgewählte oder durchschnittliche Lagerabgangsmethoden  

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet die folgende Formel, um die Inhalte des Feldes **Einstandspreis NW** in der Einkaufszeile oder den Inhalt des Feldes **Einstandspreis** in der Artikel Buch.-Blattzeile zu berechnen:  

Einstandspreis (MW) = (EK-Preis - (Rabattbetrag / Menge)) x (1 + Indirekte Kosten % / 100) + Gemeinkostensatz  

### Lagerabgangsmethode „Standard“  

Die Anwendung füllt das Feld **Einstandspreis (MW)** in einer Einkaufszeile oder das Feld **Einstandspreis** in einer Artikel Buch.-Blattzeile, indem sie den Wert des Felds **Einstandspreis** von der Artikelkarte kopiert. Wenn Sie die Lagerabgangsmethode „Standard“ verwenden, basiert der Wert auf dem Einstandspreis.  

Wenn Sie einen Einkauf buchen, wird der Einstandspreis aus der Einkaufszeile bzw. der Artikel Buch.-Blattzeile in den Rechnungsposten des eingekauften Artikels kopiert. Er wird in der Postenübersicht des Artikels angezeigt.  

### Alle Lagerabgangsmethoden  

Der Einstandspreis aus der Herkunftsbelegzeile wird verwendet, um den Wert im Feld **Einstandsbetrag (tatsächl.)** oder, falls anwendbar, im Feld **Einstandsbetrag (erwartet)** zu berechnen, der mit diesem Artikelposten verknüpft ist. Die Kosten werden unabhängig von der Lagerabgangsmethode des Artikels in die Berechnung einbezogen.  

## Einstandspreisberechnung für Verkäufe  

Wenn Sie Artikel verkaufen, kopiert die Anwendung den Einstandspreis immer aus dem Feld **Einstandspreis** der Artikelkarte in die Verkaufszeile oder die Artikel Buch.-Blattzeile.  

Beim Buchen wird später der Einstandspreis in den Artikelposten der Verkaufsrechnung kopiert; er wird darüber hinaus in den Artikelposten des jeweiligen Artikels angezeigt. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet den Einstandspreis aus der Herkunftsbelegzeile, um den Inhalt des Feldes **Einstandsbetrag (tatsächl.)** oder, falls anwendbar, des Feldes **Einstandsbetrag (erwartet)** in dem Wertposten zu berechnen, der mit diesem Artikelposten verknüpft ist.  

## Preisregulierungen von Artikeln verfolgen

Artikelkosten können sich aus vielen Gründen ändern, daher ist es wichtig, dass Sie die Kostenanpassungen im Auge behalten können. Verwenden Sie die Seite **Lagerkostenregulierung**, um den Kostenregulierungsprozess zu verwalten und zu überwachen. Auf dieser Seite werden Artikel zusammen mit ihren Kostenparametern und dem Kostenregulierungsstatus angezeigt. Sie können die Liste filtern, um sich auf Elemente zu konzentrieren, die angepasst werden müssen oder die vom Kostenanpassungsprozess ausgeschlossen sind. Weitere Informationen zum Verfolgen von Kostenanpassungen finden Sie unter [Preisregulierungen von Artikeln verfolgen](finance-track-inventory-costs.md).

## Siehe auch

[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Bestand](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]