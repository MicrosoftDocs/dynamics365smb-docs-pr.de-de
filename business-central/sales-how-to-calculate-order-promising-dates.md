---
title: Datumsangaben für Lieferterminzusagen berechnen
description: 'Die Funktion "Lieferterminzusagen" ist ein Werkzeug zur Berechnung des frühestmöglichen Datums, an dem ein Artikel zum Versand oder zur Lieferung verfügbar ist.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Datumsangaben für Lieferterminzusagen berechnen

Ein Mandant muss in der Lage sein, seine Debitoren über Auftragslieferdaten zu informieren. Die Seite **Lieferzusagenzeilen** ermöglicht Ihnen dies über einen Verkaufsauftrag.  

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet die Versand- und Liefertermine auf der Grundlage der bekannten und erwarteten Verfügbarkeitsdaten eines Artikels, die Sie den Kunden zusagen können.  

Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet:  

- Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum  
- Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum  

Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden. Falls die Artikel am Lieferdatum nicht zur Kommissionierung zur Verfügung stehen, erscheint eine Warnmeldung die auf diesen Umstand hinweist.  

Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet. Dieses Datum wird dann im Feld **Versanddatum** auf der Zeile eingegeben, und das Datum, für das Sie die Lieferung der Artikel einplanen, sowie das Datum, an dem sie an den Debitor ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.  

- Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum  
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum  

## Über Lieferterminzusagen

Die Funktion Lieferzusagen ermöglicht Ihnen, den Versand oder die Lieferung eines Auftrags zu einem bestimmten Datum zuzusagen. Das Datum, zu dem der Artikel verfügbar oder geeignet für eine Zusage ist, wird berechnet und Auftragszeilen für das Datum, welches Sie akzeptiert haben, erstellt. Die Funktion "Lieferterminzusagen" ist ein Werkzeug zur Berechnung des frühestmöglichen Datums, an dem ein Artikel zum Versand oder zur Lieferung verfügbar ist. Sie erstellt außerdem Bestellarbeitsblattszeilen, falls die Artikel für die von Ihnen akzeptierten Daten zuerst bezogen oder gefertigt werden müssen.

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet zwei grundlegende Konzepte:  

- Lieferzusage (Available to promise, ATP)  
- Beschaffungszusage (Capable to promise, CTP)  

### Verfügbar für Zusage

"Lieferzusage (Available to promise, ATP)" berechnet die Daten auf der Grundlage des Reservierungssystems. Dabei wird eine Verfügbarkeitsprüfung der nicht reservierten Mengen im Lagerbestand im Hinblick auf die geplante Produktion, Einkäufe, Umlagerungen und Verkaufsreklamationen durchgeführt. Auf der Grundlage dieser Informationen berechnet [!INCLUDE[prod_short](includes/prod_short.md)] das Lieferdatum der Kundenbestellung, weil die Artikel entweder im Bestand oder auf geplanten Aufträgen verfügbar sind.  

### Verfügbarkeitszusage

Die Verfügbarkeitszusage (CTP) geht von einem „Was-wenn“-Szenario aus, das nur für Artikelmengen gilt, die nicht im Lagerbestand oder im geplanten Bestellungen sind. Auf Grundlage dieses Szenarios berechnet [!INCLUDE[prod_short](includes/prod_short.md)] das früheste Datum, zu dem der Artikel verfügbar sein kann, wenn er gefertigt, eingekauft oder umgelagert werden muss.

#### Beispiel

Wenn eine Bestellung über 10 Stück vorliegt und 6 Stück im Bestand oder auf geplanten Zugängen verfügbar sind, dann basiert die Berechnung der Verfügbarkeitszusage auf 4 Stück.

### Berechnungen

Wenn [!INCLUDE[prod_short](includes/prod_short.md)] das Auslieferungsdatum des Debitors berechnet, werden zwei Aufgaben ausgeführt:  

- Berechnung des frühesten Lieferdatums, wenn der Debitor kein bestimmtes Lieferdatum angefragt hat.  
- Prüfung, ob das vom Debitor angefragte oder ihm zugesagte Lieferdatum realistisch ist.  

Wenn der Debitor kein bestimmtes Lieferdatum anfragt, wird das Lieferdatum auf das Arbeitsdatum festgelegt, und die Verfügbarkeit basiert dann auf diesem Datum. Wenn der Artikel im Lagerbestand vorhanden ist, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] den Termin, zu dem der Auftrag geliefert werden kann. Dazu dienen die folgenden Formeln:  

- Geplantes Warenausgangsdatum + Ausgehende Lagerdurchlaufzeit = Geplantes Warenausg.-Datum  
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum  

[!INCLUDE[prod_short](includes/prod_short.md)] überprüft dann, ob das berechnete Lieferdatum realistisch ist; dazu wird zeitlich rückwärts berechnet, wann der Artikel verfügbar sein muss, um den zugesagten Termin einhalten zu können. Dazu dienen die folgenden Formeln:  

- Geplantes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum  
- Geplantes Warenausgangsdatum - Ausgehende Lagerdurchlaufzeit + Warenausg.-Datum  

Das Lieferdatum wird für die Verfügbarkeitsprüfung verwendet. Wenn der Artikel zu diesem Datum verfügbar ist, bestätigt [!INCLUDE[prod_short](includes/prod_short.md)], dass die angeforderte/zugesagte Lieferung eingehalten werden kann, indem das geplante Lieferdatum auf das angeforderte/zugesagte Lieferdatum festgelegt wird. Wenn der Artikel nicht verfügbar ist, wird ein leeres Datum zurückgegeben, und der Auftragsbearbeiter kann die CTP-Funktion verwenden.  

Auf Grundlage neuer Daten und Uhrzeiten werden alle damit verbundenen Daten gemäß den oben aufgeführten Formeln berechnet. Die CTP-Berechnung dauert, gibt jedoch ein präzises Datum an, zu dem der Debitor die Lieferung des Artikels erwarten kann. Die Daten, die per CTP berechnet werden, werden den Fenstern **Geplantes Lieferdatum** und **Frühestmög. Warenausgangsdatum** auf der Seite **Lieferterminzusagenzeilen** angegeben.  

Der Auftragsverarbeiter beendet den CTP-Prozess, indem er die Datumsangaben akzeptiert. Dies bedeutet, dass eine Planungszeile und ein Reservierungsposten für diesen Artikels vor den berechneten Daten erstellt werden, damit sichergestellt ist, dass der Auftrag erfüllt wird.  

Zusätzlich zu den externen Lieferterminzusagen, die Sie auf der Seite **Lieferterminzusagenzeilen** durchführen können, können Sie interne oder externe Lieferdaten für Stücklistenrtikel zusagen. Weitere Informationen finden Sie unter [Die Verfügbarkeit von Artikeln anzeigen](inventory-how-availability-overview.md)

## Lieferterminzusagen einrichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lieferterminzusagen Einr.** ein, und wählen Sie dann den zugehörigen Link.  
2. Geben Sie eine Zahl und einen Zeiteinheitencode in das Feld **Verschiebung (Zeit)** ein. Wählen Sie einen der folgenden Codes aus.  

    |Code|Beschreibung|  
    |----------|-----------------|  
    |**T**|Kalendertag|  
    |**a**|Woche|  
    |**M**|Monat|  
    |**Q**|Quartal|  
    |**J**|Jahr|  

    "3w" bedeutet zum Beispiel, dass die Verschiebung drei Wochen beträgt. Stellen Sie ein "l" vor einen dieser Codes, um die jeweils laufende Zeiteinheit anzugeben. Wenn Sie zum Beispiel als Basis für die Verschiebung den aktuellen Monat verwenden möchten, geben Sie **lm** ein.  
3. Geben Sie in das Feld **Lieferterminzusagennummern** eine Nummernserie ein, indem Sie eine Zeile aus der Liste auf der Seite **Nummernserien** wählen.  
4. Geben Sie eine Lieferterminzusagenvorlage im Feld **Lieferterminzusagenvorlage** ein, indem Sie eine Zeile auf der Seite **Bestellarbeitsblatt Vorl.-Übers.** wählen.  
5. Geben Sie im Feld **Lieferterminzusagenvorschlag** einen Vorschlag ein, indem Sie eine Zeile auf der Seite **Bestellarbeitsblattsnamen** wählen.

### Eingehende und ausgehende Lagerumschlagszeiten in der Lieferterminzusage

Wenn Sie die Lagerumschlagszeit in die Berechnung der Lieferterminzusage in der Einkaufszeile einbeziehen möchten, können Sie auf der Seite **Bestandseinrichtung** eine Standardumschlagszeit für Verkaufs- und Einkaufsbelege angeben. Sie können auch auf der Seite **Standortkarte** spezifische Zeiten für jeden Ihrer Standorte eingeben. 

#### So geben Sie Standard-Handlingszeiten für eingehende und ausgehende Lager für Einkaufs- und Verkaufsbelege ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie auf der Seite **Allgemein** in den Feldern **Eingehende Lagerbearbeitungszeit** und **Ausgehende Lagerbearbeitungszeit** die Anzahl der Tage ein, die Sie in die Berechnung der Lieferterminzusagen einbeziehen möchten.  

#### So geben Sie eingehende und ausgehende Lagerbearbeitungszeiten für Standorte ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Lagerort** ein und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie die relevante Lagerortkarte.  
3.  Geben Sie auf dem Inforegister **Lager** in den Feldern **Eingehende Lagerbearbeitungszeiten** und **Ausgehende Lagerbearbeitungszeiten** die Anzahl der Tage ein, die Sie in die Berechnung der Lieferterminzusagen einbeziehen möchten.  

> [!NOTE]  
>  Wenn Sie bei der Erstellung einer Bestellung im Feld **Versand an** auf dem Inforegister **Versand und Zahlung** die Option **Lagerplatz** und anschließend im Feld **Lagerplatzcode** einen Lagerplatz auswählen, verwenden die Felder **Ausgehende Lagerbearbeitungszeit** und **Eingehende Lagerbearbeitungszeit** die für den Lagerplatz angegebene Bearbeitungszeit. Für Verkaufsaufträge gilt dasselbe, wenn Sie im Feld **Lagerortcode** einen Lagerort auswählen. Wenn für den Lagerort keine Bearbeitungszeit angegeben ist, bleiben die Felder **Ausgehende Lagerbearbeitungszeit** und **Eingehende Lagerbearbeitungszeit** leer. Wenn Sie das Feld **Lagerortcode** auf Belegen für Einkauf und Verkauf leer lassen, wird die auf der Seite **Bestandseinrichtung** angegebene Bearbeitungszeit verwendet.

## Einen Artikel als kritisch kennzeichnen

Bevor ein Artikel bei der Berechnung der Lieferterminzusage berücksichtigt werden kann, muss er als kritisch markiert werden Diese Einstellungen stellen sicher, dass nicht kritische Artikel nicht irrelevante Lieferterminzusagen verursachen.   
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie die betreffende Elementkarte.  
3.  Wählen Sie im Inforegister **Planung** das Feld **Kritisch** aus.  

## Lieferterminzusagen berechnen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsauftrag** ein und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie den relevanten Verkaufsauftrag, und wählen Sie die Verkaufszeilen aus, die die Anwendung berechnen soll.  
3.  Wählen Sie die **Lieferterminzusagen** Aktion aus, und wählen Sie die **Lieferterminzusagenzeilen** Aktion aus.  
4.  Wählen Sie eine Zeile aus, und wählen Sie dann eine der folgenden Optionen aus:  

    - Wählen Sie **Verfügbar für Zusage**, wenn die Anwendung das früheste Verfügbarkeitsdatum des Artikels unter Berücksichtigung des Lagerbestands der geplanten Zugänge und des Bruttobedarfs berechnen soll.  
    - Wählen Sie **Geeignet für Zusage**, wenn Sie wissen, dass der Artikel aktuell nicht an Lager ist und das früheste Datum, zu dem der Artikel durch neue Lagerzugänge verfügbar sein wird, errechnen wollen.  
5.  Wählen Sie die Schaltfläche **Akzeptieren**, um das früheste verfügbare Lieferdatum zu akzeptieren.  

## Siehe auch

[Verkauf](sales-manage-sales.md)  
[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
