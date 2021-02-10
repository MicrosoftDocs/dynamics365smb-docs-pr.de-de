---
title: "So wird's gemacht: Lieferterminzusagen berechnen | Microsoft Docs"
description: Die Funktion "Lieferterminzusagen" ist ein Werkzeug zur Berechnung des frühestmöglichen Datums, an dem ein Artikel zum Versand oder zur Lieferung verfügbar ist. Sie erstellt außerdem Bestellvorschlagszeilen für das Datum, welches Sie akzeptiert haben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 150c5c552e314d17af15968ebcbe57d8e8bc3fc1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758117"
---
# <a name="calculate-order-promising-dates"></a>Lieferterminzusagen-Daten berechnen
Ein Mandant muss in der Lage sein, seine Debitoren über Auftragslieferdaten zu informieren. Die Seite **Lieferzusagenzeilen** ermöglicht Ihnen, dies von einer Verkaufsauftragszeile aus zu tun.  

Auf Grundlage der bekannten und erwarteten Verfügbarkeitstermine eines Artikels berechnet [!INCLUDE[prod_short](includes/prod_short.md)] sofort die Lieferdaten, die dann dem Debitor zugesagt werden können.  

Wenn Sie in einer Verkaufszeile ein gewünschtes Lieferdatum eingeben, wird dieses Datum als Ausgangspunkt für die folgenden Berechnungen verwendet:  

- Gewünschtes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum  
- Geplantes Warenausgangsdatum - Ausgeh. Lagerdurchlaufzeit = Warenausgangsdatum  

Falls die Artikel am Lieferdatum zur Kommissionierung zur Verfügung stehen, kann der Verkaufsvorgang fortgesetzt werden. Falls die Artikel am Lieferdatum nicht zur Kommissionierung zur Verfügung stehen, erscheint eine Warnmeldung die auf diesen Umstand hinweist.  

Wenn Sie kein angefordertes Lieferdatum auf der Verkaufsauftragszeile angeben oder das angeforderte Lieferdatum nicht eingehalten werden kann, wird das früheste Datum, an dem die Artikel verfügbar sind, berechnet. Dieses Datum wird dann im Feld **Versanddatum** auf der Zeile eingegeben, und das Datum, an dem Sie planen, die Artikel zu liefern, sowie das Datum, an dem Sie an den Debitoren ausgeliefert werden, werden anhand der nachfolgenden Formeln berechnet.  

- Warenausgangsdatum + Ausgeh. Lagerdurchlaufzeit = Geplantes Warenausgangsdatum  
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum  

## <a name="about-order-promising"></a>Über Lieferterminzusagen
Die Funktion Lieferzusagen ermöglicht Ihnen, den Versand oder die Lieferung eines Auftrags zu einem bestimmten Datum zuzusagen. Das Datum, zu dem der Artikel verfügbar oder geeignet für eine Zusage ist, wird berechnet und Auftragszeilen für das Datum, welches Sie akzeptiert haben, erstellt. Die Funktion "Lieferterminzusagen" ist ein Werkzeug zur Berechnung des frühestmöglichen Datums, an dem ein Artikel zum Versand oder zur Lieferung verfügbar ist. Sie erstellt außerdem Bestellvorschlagszeilen, falls die Artikel zuerst gekauft werden müssen, für das Datum, welches Sie akzeptiert haben.

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet zwei grundlegende Konzepte:  

- Lieferzusage (Available to promise, ATP)  
- Beschaffungszusage (Capable to promise, CTP)  

### <a name="available-to-promise"></a>Lieferzusage  
"Lieferzusage (Available to promise, ATP)" berechnet die Daten auf der Grundlage des Reservierungssystems. Dabei wird eine Verfügbarkeitsprüfung der nicht reservierten Mengen im Lagerbestand im Hinblick auf die geplante Produktion, Einkäufe, Umlagerungen und Verkaufsreklamationen durchgeführt. Auf Grundlage dieser Informationen berechnet [!INCLUDE[prod_short](includes/prod_short.md)] automatisch das Auslieferungsdatum des Debitorenauftrags, weil die Artikel, entweder im Lagerbestand oder im Rahmen geplanter Wareneingänge, verfügbar sind.  

### <a name="capable-to-promise"></a>Beschaffungszusage  
Beschaffungszusage (CTP) für eine Zusage akzeptiert "Was-wenn", das nur auf Artikelmengen gehört, die nicht im Lagerbestand oder im geplanten Bestellungen sind. Auf Grundlage dieses Szenarios berechnet [!INCLUDE[prod_short](includes/prod_short.md)] das früheste Datum, zu dem der Artikel verfügbar sein kann, wenn er gefertigt werden, bezogen werden oder umgelagert werden muss.

#### <a name="example"></a>Beispiel
Wenn ein Auftrag für 10 Stück besteht und 6 Stück im Lagerbestand oder in geplanten Aufträge verfügbar sind, ist die Fähig-zu-Versprechenberechnung auf Grundlage 4 Stück.

### <a name="calculations"></a>Berechnungen  
Wenn [!INCLUDE[prod_short](includes/prod_short.md)] das Auslieferungsdatum des Debitors berechnet, werden zwei Aufgaben ausgeführt:  

- Berechnung des frühesten Lieferdatums, wenn der Debitor kein bestimmtes Lieferdatum angefragt hat.  
- Prüfung, ob das vom Debitor angefragte oder ihm zugesagte Lieferdatum realistisch ist.  

Wenn der Debitor kein bestimmtes Lieferdatum anfragt, wird das Lieferdatum auf das Arbeitsdatum festgelegt, und die Verfügbarkeit basiert dann auf diesem Datum. Wenn der Artikel im Lagerbestand vorhanden ist, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] den Termin, zu dem der Auftrag geliefert werden kann. Dazu dienen die folgenden Formeln:  

- Geplantes Warenausgangsdatum + Ausgehende Lagerdurchlaufzeit = Geplantes Warenausg.-Datum  
- Geplantes Warenausgangsdatum + Transportzeit = Geplantes Lieferdatum  

[!INCLUDE[prod_short](includes/prod_short.md)] überprüft dann, ob das berechnete Lieferdatum realistisch ist; dazu wird zeitlich rückwärts berechnet, wann der Artikel verfügbar sein muss, um den zugesagten Termin einhalten zu können. Dazu dienen die folgenden Formeln:  

- Geplantes Lieferdatum - Transportzeit = Geplantes Warenausgangsdatum  
- Geplantes Warenausgangsdatum - Ausgehende Lagerdurchlaufzeit + Warenausg.-Datum  

Das Lieferdatum wird für die Verfügbarkeitsprüfung verwendet. Wenn der Artikel an diesem Datum verfügbar ist, bestätigt [!INCLUDE[prod_short](includes/prod_short.md)], dass die angeforderte/zugesagte Lieferung eingehalten werden kann, indem das geplante Lieferdatum auf das angefragte/zugesagte Lieferdatum gesetzt wird. Wenn der Artikel nicht verfügbar ist, wird ein leeres Datum zurückgegeben, und der Auftragsbearbeiter kann die CTP-Funktion verwenden.  

Auf Grundlage neuer Daten und Uhrzeiten werden alle damit verbundenen Daten gemäß den oben aufgeführten Formeln berechnet. Die CTP-Berechnung dauert, gibt jedoch ein präzises Datum an, zu dem der Debitor die Lieferung des Artikels erwarten kann. Die Daten, die per CTP berechnet werden, werden den Fenstern **Geplantes Lieferdatum** und **Frühestmög. Warenausgangsdatum** auf der Seite **Lieferterminzusagenzeilen** angegeben.  

Der Auftragsverarbeiter beendet den CTP-Prozess, indem er die Datumsangaben akzeptiert. Dies bedeutet, dass eine Planungszeile und ein Reservierungsposten für diesen Artikels vor den berechneten Daten erstellt werden, damit sichergestellt ist, dass der Auftrag erfüllt wird.  

Zusätzlich zu den externen Lieferterminzusagen, die Sie auf der Seite **Lieferterminzusagenzeilen** durchführen können, können Sie interne oder externe Lieferdaten für Stücklistenrtikel zusagen. Weitere Informationen finden Sie unter [Die Verfügbarkeit von Artikeln anzeigen](inventory-how-availability-overview.md)

## <a name="to-set-up-order-promising"></a>Lieferterminzusagen einrichten  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lieferterminzusagen-Einrichtung** ein und wählen Sie dann den entsprechenden Link.  
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
4. Geben Sie eine Lieferterminzusagenvorlage im Feld **Lieferterminzusagenvorlage** ein, indem Sie eine Zeile auf der Seite **Bestellvorschlag Vorl.-Übers.** wählen.  
5. Geben Sie im Feld **Lieferterminzusagenvorschlag** einen Vorschlag ein, indem Sie eine Zeile auf der Seite **Bestellvorschlagsnamen** wählen.

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Eingehende Lagerdurchlaufzeit auf der Einrichtungsseite des Bestands eingeben  
Wenn Sie die Lagerdurchlaufzeit bei der Berechnung der Lieferterminzusage in der Einkaufszeile berücksichtigen wollen, können Sie sie als Vorgabewert für das Lager und für Ihren Lagerort einrichten.    
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Bestandseinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Im Inforegister **Allgemein** im Feld **Eingeh. Lagerdurchlaufzeit** geben Sie die Anzahl Tage ein, die die Anwendung bei der Berechnung der Lieferterminzusage berücksichtigen soll.  

> [!NOTE]  
>  Wenn Sie das Feld **Eingeh. Lagerdurchlaufzeit** auf der **Lagerortkarte** für Ihren Lagerort ausgefüllt haben, verwendet die Anwendung den Inhalt dieses Feldes als eingehende Vorgabelagerdurchlaufzeit.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Eingehende Lagerdurchlaufzeit in Lagerortkarten eingeben  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerort** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die relevante Lagerortkarte.  
3.  Im Inforegister **Lager** im Feld **Eingeh. Lagerdurchlaufzeit** geben Sie die Anzahl Tage ein, die bei der Berechnung der Lieferterminzusage berücksichtigt werden soll.  

> [!NOTE]  
>  Wenn Sie das Feld **Eingeh. Lagerdurchlaufzeit** leer lassen, verwendet die Berechnung den Wert auf der Seite **Lager Einrichtung**.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-page"></a>Ausgehende Lagerdurchlaufzeit auf der Einrichtungsseite des Bestands eingeben  
Wenn Sie eine ausgehende Lagerdurchlaufzeit bei der Berechnung der Lieferterminzusage in der Verkaufszeile berücksichtigen möchten, können Sie diese als Vorgabewert für das Lager eingeben.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Bestandseinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Im Inforegister **Allgemein** im Feld **Ausgeh. Lagerdurchlaufzeit** geben Sie die Anzahl Tage ein, die die Anwendung bei der Berechnung der Lieferterminzusage berücksichtigen soll.  

> [!NOTE]  
>  Wenn Sie das Feld **Ausgeh. Lagerdurchlaufzeit** auf der Standortkarte für Ihren Standort ausgefüllt haben, wird der Inhalt dieses Feldes als ausgehende Vorgabelagerdurchlaufzeit verwendet.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Ausgehende Lagerdurchlaufzeit der Logistik in Standortkarten eingeben  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagerorte** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die relevante Lagerortkarte.  
3.  Im Inforegister **Lager** im Feld **Ausgeh. Lagerdurchlaufzeit** geben Sie die Anzahl Tage ein, die bei der Berechnung der Lieferterminzusage berücksichtigt werden soll.  

> [!NOTE]  
>  Wenn Sie das Feld **Ausgeh. Lagerdurchlaufzeit** leer lassen, verwendet die Berechnung den Wert auf der Seite **Lager Einrichtung**.

## <a name="to-make-an-item-critical"></a>Einen Artikel als kritisch kennzeichnen  
Bevor ein Artikel bei der Berechnung der Lieferterminzusage berücksichtigt werden kann, muss er als kritisch markiert werden Diese Einstellungen stellen sicher, dass unkritische Artikel nicht irrelevante Lieferterminzusagen verursachen.   
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die entsprechende Artikelkarte.  
3.  Wählen Sie im Inforegister **Planung** das Feld **Kritisch** aus.  

## <a name="to-calculate-an-order-promising-date"></a>Lieferterminzusagen berechnen  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufsauftrag** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie den relevanten Verkaufsauftrag, und wählen Sie die Verkaufszeilen aus, die die Anwendung berechnen soll.  
3.  Wählen Sie die **Lieferterminzusagen** Aktion aus, und wählen Sie die **Lieferterminzusagenzeilen** Aktion aus.  
4.  Wählen Sie eine Zeile aus, und wählen Sie dann eine der folgenden Optionen aus:  

    - Wählen Sie **Verfügbar für Zusage**, wenn die Anwendung das früheste Verfügbarkeitsdatum des Artikels unter Berücksichtigung des Lagerbestands der geplanten Zugänge und des Bruttobedarfs berechnen soll.  
    - Wählen Sie **Geeignet für Zusage**, wenn Sie wissen, dass der Artikel aktuell nicht an Lager ist und das früheste Datum, zu dem der Artikel durch neue Lagerzugänge verfügbar sein wird, errechnen wollen.  
5.  Wählen Sie die Schaltfläche **Akzeptieren**, um das früheste verfügbare Lieferdatum zu akzeptieren.  

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
