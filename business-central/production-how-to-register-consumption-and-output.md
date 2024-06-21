---
title: Verbrauchsausgabe für Produktauftrag registrieren
description: 'Dieses Thema erklärt, wie Sie den Verbrauch und die Ausgabe für eine freigegebene Fertigungsauftrags-Zeile registrieren, die auf der Seite Fertigungsjournal angezeigt wird.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a>Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile

Diese Ausführungsaufgabe wird auf der Seite **Produktions Buch.-Blatt** ausgeführt. In diesem Buchungsblatt werden die Funktionen des separaten FA-Verbrauchs Buch.-Blatts und des FA-Istmeldungs Buch.-Blatts in einem Buchungsblatt kombiniert. Auf das kombinierte Buchungsblatt wird direkt von einem freigegebenen Fertigungsauftrag aus zugegriffen. Es dient hauptsächlich dazu, den Verbrauch von Komponenten, die Menge der gefertigten Endartikel und die für die Arbeitsgänge aufgewendete Zeit manuell zu buchen. Die Werte werden als Posten unter dem freigegebenen Fertigungsauftrag gebucht. Verbrauchsmengen werden als negative Artikelposten gebucht, fertig gestellte Mengen werden als positive Posten gebucht, und die aufgewendeten Zeiten werden als Kapazitätsposten gebucht. Solche gebuchten Posten können auch unten im Buchungsblatt als Ist-Mengen angezeigt werden.  

> [!NOTE]  
> Da die Verbrauchsdaten gemeinsam mit den Istmeldungsdaten verwendet werden, bietet dieses Protokoll eine Möglichkeit zum Anzeigen verknüpfter Komponenten und Arbeitsgänge in einer logischen Prozessstruktur. Die Komponenten werden unter dem jeweils zugehörigen Arbeitsgang eingerückt. Dazu ist es erforderlich, dass Sie Verbindungscodes verwenden.  

> [!NOTE]  
> Komponenten ohne Verbindungscodes werden im Buchungsblatt zuerst aufgeführt.  

## <a name="to-register-consumption-and-output"></a>Verbrauch und Istmeldungen registrieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Geben Sie im Symbol **Freigegebene Prod. Orders** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie eine freigegebene FA-Zeile, die zur Registrierung bereitsteht. Klicken Sie auf dem Inforegister **Zeilen** auf die Aktion **Zeilen** und klicken Sie dann auf **Produktions Buch.-Blatt**.  

    Die Seite **Produktions-Buch.-Blatt** wird geöffnet, mit Buchungsblattzeilen für den Fertigungsauftrag entsprechend den Seiten **FA-Komponente** und **FA-Arbeitsplan**. Diese Zeilen stammen aus der Fertigungsstückliste und dem Arbeitsplan, die dem Artikel zugewiesen wurden, der gefertigt wird. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-create-routings.md).  

3. Geben Sie im Feld **Buchungsdatum** ganz oben im Buchungsblatt ein Buchungsdatum ein, das auf alle Zeilen angewendet wird. Standardmäßig wird das Arbeitsdatum eingegeben. Das Feld soll dazu dienen, schnell die Buchungsdaten in allen Zeilen anzugleichen, falls dies erforderlich ist.  

    > [!NOTE]  
    >  Ein Buchungsdatum, das in einzelne Zeilen eingegeben wird, setzt dieses Feld außer Kraft.  

4. Im Feld **Buchungsmethodenfilter** ganz oben im Protokoll können Sie auswählen, ob auch der Verbrauch und die Istmeldungen angezeigt werden, die gemäß den jeweils für den Artikel und die Ressource definierten Buchungsmethoden automatisch gebucht werden. Weitere Informationen finden Sie unter [Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).

5. Geben Sie anschließend die entsprechenden Mengen in den veränderbaren Feldern für Verbrauch und/oder Istmeldungen ein.  
  
    In jeder Art von Zeilen des Buchungsblatts werden nur die relevanten Felder angezeigt. Der Rest ist leer und schreibgeschützt.  

    Beim Öffnen des Buchungsblatts sind die zu buchenden Mengen voreingestellt. Wenn bisher nichts gebucht wurde, werden in allen Mengenfeldern standardmäßig die erwarteten Mengen angezeigt, die aus dem Fertigungsauftrag übernommen wurden. Wenn Teilbuchungen vorgenommen wurden, werden in den Mengenfeldern der Zeilen die Restmengen angezeigt. Die bereits für den Auftrag gebuchten Mengen und Zeiten werden unten im Buchungsblatt als Ist-Posten angezeigt.  

    Für die Mengen im Feld **Fertig gestellte Menge** können Sie festlegen, welche Werte beim ersten Öffnen des Protokolls als Voreinstellung angezeigt werden. Dies erfolgt auf der Seite **Produktion Einrichtung** auf dem Inforegister **Allgemein** im Feld **Vordef. fertig gest. Menge**.

    > [!NOTE]  
    >  Nur mit der fertig gestellten Menge für die letzte Protokollzeile vom Postenart **Istmeldung** beim Buchen des Protokolls der Lagerbestand angepasst wird. Achten Sie deshalb darauf, dass Sie das Protokoll nicht mit der erwarteten fertig gestellten Menge als Voreinstellung in der letzten Istmeldungszeile buchen, solange nicht alle Endartikel tatsächlich gefertigt wurden.  

6. Wählen Sie das Feld **Beendet** in den Istmeldungszeilen, um anzugeben, dass der Arbeitsgang beendet ist. Dieses Feld ist mit dem Feld **Arbeitsplanstatus** in einem Arbeitsgang eines Fertigungsauftrags verbunden.  
7. Klicken Sie auf **Buchen**, um die eingegebenen Mengen zu registrieren und das Buchungsblatt zu schließen.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    Wenn Werte zu buchen übrig bleiben, enthält das Buchungsblatt beim nächsten Öffnen diese verbleibenden Werte. Gebuchte Werte werden als tatsächliche Werte unten auf dem Buchungsblatt angezeigt.  

    > [!NOTE]  
    >  Wenn ein im Verbrauch befindlicher Artikel gesperrt ist, werden vom Buchungsblatt keine Verbrauchsmengen für diesen Artikel gebucht. Wenn ein Arbeitsplatz oder eine Arbeitsplatzgruppe gesperrt ist, werden vom Buchungsblatt keine fertig gestellten Mengen oder Prozesszeiten für die fragliche Istmeldungszeile gebucht.  

    > [!NOTE]  
    > Wenn Sie das Buchungsblatt schließen, ohne eine Buchung vorzunehmen, gehen die Änderungen verloren.  

> [!WARNING]  
> Die Seite **Produktions Buch.-Blatt** kann nicht von zwei Benutzern gleichzeitig verwendet werden. Das bedeutet, wenn Benutzer 2 die Seite öffnet und Daten eingibt, wenn Benutzer 1 bereits auf der Seite arbeitet, dann verliert möglicherweise Benutzer 2 Daten, wenn Benutzer 1 die Seite schließt.  

## <a name="see-also"></a>Siehe auch

[Produktion](production-manage-manufacturing.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
