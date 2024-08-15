---
title: So reservieren Sie Artikel
description: 'Erfahren Sie mehr über die Reservierung von Artikeln für Verkaufsaufträge, Bestellungen und Produktionsaufträge.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 05/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Artikel reservieren

Reservieren Sie Lager oder eingehenden Artikel für Verkaufsaufträge, Bestellungen, Montageaufträge, Umlagerungsaufträge oder Fertigungsaufträge. Sie können Artikel auch in Lager oder eingehenden in Zeilen der offenen Belegzeile reservieren. Sie tun dies auf der Seite **Reservierung**.

Jede Zeile, die Sie zum Reservieren der Artikel auf der Seite **Reservierung** öffnen, beinhaltet Informationen zu der Art der Zeile (Verkauf, Einkauf, Buchungsblatt) oder der Postenart. Die Zeilen zeigen an, wie viele Artikel von jeder Art von Zeile oder Posten für die Reservierung verfügbar sind.

> [!TIP]
> Basierend auf den Mengen, die Sie im Lagerbestand reserviert haben, zeigt [!INCLUDE [prod_short](includes/prod_short.md)] einen Status der Dokumente an, sodass Sie schnell über den nächsten Schritt informiert sind. Beispielsweise um anzugeben, dass Sie einen Kundenauftrag versenden oder mit der Arbeit an einem Projekt, einer Montage oder einem Produktionsauftrag beginnen können. Der Status trägt auch dazu bei, das Risiko versehentlicher Teillieferungen oder Verzögerungen aufgrund fehlender Bestände für Produktions- und Montageaufträge zu verringern.
>
> Das Feld **Reserviert aus Bestand** kann Ihnen helfen zu verstehen, ob Sie für eine bestimmte Bestellung oder Bestellposition versenden oder kommissionieren können. Für Positionen ist das Feld „Reserviert aus Bestand“ in Infoboxen verfügbar. Um auf die Informationen zur gesamten Bestellung zuzugreifen, befindet sich das Feld auf der Seite **Statistiken**.

## Sie Artikel für Verkäufe reservieren

Nachfolgend wird erläutert, wie Entscheidungsträger als Artikel aus einem Verkaufsauftrag reserviert werden. Die Schritte sind gleich für Einkaufs-, Service-, Umlagerungs- und Montageaufträge.
  
1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Verkaufsauftrag.
3. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus. Die Seite **Reservierung** wird geöffnet.  
4. Wählen Sie in die Zeile, aus der Sie Artikel reservieren möchten.  
5. Wählen Sie eine der folgenden Optionen aus.  

    |**Funktion**|**Beschreibung**|
    |------------------|---------------------|  
    |**Autom. reservieren**|Um die Artikel in dem Fenster **Reservierung** automatisch zu reservieren.|  
    |**Von aktueller Zeile reservieren**|Um die Artikel aus dem Beleg in der Zeile zu reservieren, die Sie ausgewählt haben.|  
    |**Reservierung der aktuellen Zeile stornieren**|Um die Reservierung der Artikel in dem Beleg und in der Zeile, die Sie ausgewählt haben, zu stornieren.|

> [!NOTE]  
> Falls für den Verkaufsauftrag Artikelverfolgungszeilen vorhanden sind, führt das Reservierungssystem spezielle Schritte durch: Weitere Informationen hierzu finden Sie im Abschnitt [So reservieren Sie eine bestimmte Serien- oder Chargennummer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## Artikel für FA-Zeilen reservieren

Sie können Artikel für Erstellungsaufträge reservieren. Sie müssen zwischen Produktionsauftragszeilen, d.h. übergeordnete Artikel und Produktionsauftragskomponenten unterscheiden.

Im folgenden Verfahren wird ein fest geplanter Fertigungsauftrag verwendet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Firm Planned Prod. Auftrag** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den fest geplanten Produktionsauftrag, den Sie für übergeordnete Artikel reservieren möchten.  
3. Wählen Sie die entsprechende FA-Zeilennummer aus.  
4. Wählen Sie auf der Registerkarte  **Zeilen**  in der Gruppe  **Funktionen**  die Aktion  **Reservieren**  aus.
5. Markieren Sie auf der Seite  **Reservierung**  die Verkaufszeile und die Auftragszeile und wählen Sie dann die Aktion  **Aus aktueller Zeile reservieren** .  

Die Menge, die Sie im fest geplanten Fertigungsauftrag eingetragen haben, ist reserviert.

## Artikel für FA-Komponenten reservieren

Sie können Artikel für Erstellungsaufträge reservieren. Sie müssen zwischen Produktionsauftragszeilen, d.h. übergeordnete Artikel und Produktionsauftragskomponenten unterscheiden.

Im folgenden Verfahren wird ein fest geplanter Fertigungsauftrag verwendet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Firm Planned Prod. Auftrag** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den fest geplanten FA, für den Sie Komponentenartikel reservieren möchten.  
3. Wählen Sie die entsprechende FA-Zeilennummer aus.  
4. Wählen Sie auf dem Inforegister **Zeilen** die Option **Zeile** und dann **Posten** aus.  
5. Wählen Sie die entsprechende Komponentenzeile aus.  
6. Wählen Sie auf dem Inforegister **Zeilen** das Feld **Reservieren** aus.  
7. Wählen Sie auf der Seite **Resevierung** eine Zeile und wählen **Aus aktueller Zeile reservieren** aus.  

Die Menge, die Sie in der fest geplanten Fertigungskomponentenzeile eingetragen haben, ist nun reserviert.

## Reservieren Sie Artikel in großen Mengen

Verwenden Sie die Seite **Reservierungsarbeitsblatt**, um eingehende Waren in großen Mengen zu reservieren und zuzuordnen. Mithilfe von Massenreservierungen können Sie beispielsweise sicherstellen, dass für Ihre Verkaufs- und Produktionsaufträge Mengen verfügbar sind. Sie können mehrere Chargen für unterschiedliche Zwecke haben. Beispielsweise können Sie Produktionsaufträge wöchentlich zuweisen, diese jedoch täglich für den Verkauf reservieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Reservierungsarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion  **Nachfrage abrufen**  aus. Die Seite  **Anfrage zur Reservierung abrufen**  wird geöffnet.
1. Geben Sie auf der Seite  **Zu reservierenden Bedarf abrufen**  die Art des Bedarfs an, den Sie aus dem verfügbaren Bestand reservieren möchten.
1. Füllen Sie die Filter nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
1. Optional: Um die Elemente sofort zuzuordnen, wählen Sie die Aktion **Zuordnen**.
1. Wählen Sie auf der Seite **Zuordnungsrichtlinie** eine Richtlinie für jeden Schritt aus.

   |Zuordnungsrichtlinie  |Description  |
   |---------|---------|
   |Grundlegend (keine Konflikte)     | Weist einem Bedarf Bestand zu, wenn keine Konflikte vorliegen und der Bedarf vollständig gedeckt werden kann. Beispiel: Sie haben Kundenauftrag A mit einer Menge von 10 und einen Auftrag mit einer Menge von 7. Wenn Sie 20 Stück auf Lager haben, erhalten beide Bedarfe die volle Menge. Wenn Ihr Bestand 12 beträgt, wird kein Bestand zugeteilt. Sie müssen die Menge manuell zuteilen.        |
   |Zu gleichen Teilen    | Verteilt den verfügbaren Bestand gleichmäßig auf die Nachfrage. Beispiel: Sie haben einen Kundenauftrag mit einer Menge von 10 und einen Auftrag mit einer Menge von 7. Wenn Ihr Lagerbestand 20 beträgt, erhalten beide Bedarfe die volle Menge. Wenn Ihr Bestand 12 beträgt, erhalten beide Nachfragen 6.        |
   |Nach Debitorenpriorität|Verteilung basierend auf dem Feld **Priorität** auf der Seite **Debitorenkarte**. Bei geringen Lagerbeständen beliefert Business Central zuerst die Kundschaft mit höherer Priorität.|

6. Um alle Zeilen zu reservieren, bei denen **Akzeptieren** aktiviert ist, wählen Sie die Aktion **Reservierung vornehmen** aus.
    
## Reservierung ändern

Sie können eine Artikelreservierung ändern.

1. Von der Belegzeile, aus der Sie im Inforegister **Zeilen** reserviert haben, wählen Sie die **Reservieren** Aktion aus.  
2. Auf der Seite **Reservierung** wählen Sie die **Reservierungsposten** Aktion aus.
3. Klicken Sie auf der Seite **Reservierungseinträge** auf **Menge** aktualisieren auf der Zeile, die Sie ändern möchten.
4. Bestätigen Sie die nachfolgende Meldung, indem Sie die Schaltfläche **OK** auswählen.

## Reservierung stornieren

Sie können eine Artikelreservierung abbrechen.

1. Von der Belegzeile, aus der Sie im Inforegister **Zeilen** reserviert haben, wählen Sie die **Reservieren** Aktion aus.  
2. Wählen Sie auf der Seite  **Reservierung**  die Aktion  **Reservierungseinträge**  auf dem Inforegister  **Zeilen**  aus.  
3. Auf der Seite **Reservierung** wählen Sie die **Reservierungsposten stornieren** Aktion aus.  
4. Bestätigen Sie die nachfolgende Meldung, indem Sie die Schaltfläche **OK** auswählen.  

## Bestimmte Serien- oder Chargennummer reservieren

Aus ausgehenden Dokumenten für Artikel mit Artikelverfolgung, wie Verkaufsaufträge oder Listen mit Fertigungskomponenten, können Sie bestimmte Serien- oder Chargennummern reservieren. Die Reservierung bestimmter Serien- oder Chargennummern kann beispielsweise in den folgenden Situationen nützlich sein:

* Wenn Sie Produktionskomponenten aus einer bestimmten Charge benötigen, um die Konsistenz mit früheren Produktionschargen sicherzustellen.
* Weil ein Kunde eine bestimmte Seriennummer angefordert hat. 

Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).

Dieses Vorgehen wird als spezifische Reservierung bezeichnet, weil Sie von der Menge des Artikels X reservieren, die zu Charge X gehört. Wenn Sie dagegen nur von der Menge des Artikels X reservieren, handelt es sich lediglich um eine normale, nicht spezifische Reservierung. Weitere Informationen unter [Designdetails – Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)

Das folgende Verfahren basiert auf einer Auftragsabwicklung.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine Verkaufsauftragszeile für einen Artikel mit Artikelverfolgung.  
3. Weisen Sie dann der Verkaufsauftragszeile Serien- und Chargennummern zu. Weitere Informationen finden Sie unter [Arbeiten mit Serien- und Chargennummern](inventory-how-work-item-tracking.md).
4. Auf der Verkaufsauftragszeile wählen Sie die Aktion **Reservieren** aus.  
5. Wählen Sie die Schaltfläche **Ja**, um bestimmte Serien- oder Chargennummern zu reservieren.  
6. Wählen Sie auf der Seite **Artikelnachverfolgungsliste** die Serien- und Chargennummernkombination aus, die Sie zugewiesen haben.  
7. Wählen Sie die Schaltfläche **OK**, um die Seite **Reservationen** zu öffnen, in dem nur der Bedarf angezeigt wird, der mit der angegebenen Artikelverfolgungsnummer verbunden ist. Bei nicht-spezifischen Reservierungen für eine der Artikelverfolgungsnummern, die Sie in dieser Zeile angegeben haben, werden Sie über die Menge informiert, die bereits reserviert wurde.  
8. Klicken Sie auf die Aktionen **Automatisch Reservieren** oder **Aus aktueller Zeile reservieren**, um die Reservierung für die speziellen Artikelverfolgungsnummern zu erstellen.

## Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designdetails: Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Arbeiten mit Seriennummern und Chargennummern](inventory-how-work-item-tracking.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
