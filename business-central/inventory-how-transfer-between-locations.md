---
title: Artikel zwischen Lagerorten transferieren
description: 'Erfahrten Sie, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Buch.-Blatt mit oder den Umlagerungsaufträgen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# <a name="transfer-inventory-between-locations"></a>Lagerbestand zwischen Lagerplätzen umlagern

Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen. Sie können auch das Einkaufs-Buch.-Blatt verwenden.

> [!NOTE]
> Um Artikel umzulagern, müssen Sie Lagerplätze und Umlagerungsrouten einrichten. Weitere Informationen zum Einrichten von Standorten finden Sie unter  [Standorte einrichten](inventory-how-setup-locations.md). Sie können keine Umlagerungsaufträge für *leere* Lagerorte verwenden.

## <a name="transfer-orders"></a>Umlagerungsaufträge

Sie können eine ausgehende Umlagerung von einem Lagerplatz senden und eine eingehende Umlagerung am Ziel empfangen. Sie können:

* Verfolgen Sie eine Menge während des Transports.
* Definieren Sie Kalender, Arbeitspläne sowie eingehende und ausgehende Bearbeitungszeiten für die Datumsberechnung und -planung. Weitere Informationen zur Planung finden Sie unter [Info zu Planungsfunktionen](production-about-planning-functionality.md).
* Verwenden Sie unterschiedliche Lagerfunktionen für eingehende und ausgehende Lagerorte.
* Verwenden Sie Umlagerungsaufträge für direkte Umlagerungen mit einigen Einschränkungen.

## <a name="item-reclassification-journals"></a>Buch.-Blätter für die Neuklassifizierung von Artikeln

Verwenden Sie die Seite **Artikel Umlag. Buch.-Blätter** für Folgendes:

* Direkte Umlagerung von Artikeln zwischen Lagerorten
* Verschieben Sie Artikel zwischen Behältern. Weitere Informationen zum Übertragen von Artikeln zwischen Behältern finden Sie unter  [Ungeplantes Verschieben von Artikeln in grundlegenden Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Ändern Sie eine Chargen- oder Seriennummer in eine neue Chargen- oder Seriennummer. Weitere Informationen zur Neuklassifizierung von Serien- und Chargennummern finden Sie unter [Serien- oder Chargennummern neu klassifizieren](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Ändern Sie das Ablaufdatum in ein neues Datum.
* Klassifizieren Sie Artikel von einem leeren Lagerort an einem tatsächlichen Lagerort neu.
* Erstellen Sie Lagereinträge, wenn Sie keine Lageraktivitäten verwalten.

## <a name="to-transfer-items-with-a-transfer-order"></a>So lagern Sie Artikel mit einem Umlagerungsauftrag um

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Umlagerungsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Umlagerungsauftrag** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Wenn Sie die Felder **Umlag. in Code**, **Zustellercode** und **Zustellertransportartencode** auf der Seite **Umlagerungsroutenspezifikation** ausgefüllt haben, als Sie die Umlagerungsrouten zwischen diesen Lagerorten eingerichtet haben, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.

    Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.

3. Es gibt mehrere Wege, die Zeilen auszufüllen:

    |Option  |Beschreibung  |
    |---------|---------|
    |Manuell     | Füllen Sie auf dem Inforegister **Zeilen** eine Zeile für einen Artikel aus oder verwenden Sie die Aktion **Elemente auswählen**, um mehrere auszuwählen Artikel.        |
    |Automatisch     | * Wählen Sie die Aktion **Lagerplatz-Inhalt abrufen** aus, um vorhandene Elemente aus einem bestimmten Fach am Standort auszuwählen.<br><br>* Wählen Sie **Belegzeilen abrufen** aus, um Elemente auszuwählen, die gerade am Transfer-von-Standort angekommen sind.        |

    Sie können die Artikel nun versenden.
4. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.

    Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen Die Überweisungsauftragspositionen sind dieselben wie im Auslieferungszustand und können nicht bearbeitet werden.
5. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.

### <a name="undo-a-transfer-shipment"></a>Ein Umlagerungsversand rückgängig machen

Wenn Sie in einem gebuchten Transportauftrag einen Mengenfehler finden, können Sie die Menge problemlos korrigieren, solange die Lieferung nicht eingeht. Auf der Seite  **Gebuchte Transfersendung**  werden mit der Aktion  **Sendung rückgängig machen**  Korrekturzeilen wie folgt erstellt:

* Der Wert im Feld **Verschickte Menge** auf dem Verkaufsauftrag wird um die Menge verringert, die Sie rückgängig gemacht haben.
* Der Wert im Feld **Verschickte Menge** auf dem Verkaufsauftrag wird um die Menge verringert, die Sie rückgängig gemacht haben.
* Das Kontrollkästchen **Korrektur** ist für die Zeilen aktiviert.

Wenn die Menge in einem Lagerversand versendet wurde, wird im gebuchten Lagerversand eine Korrekturzeile erstellt.

Um die Korrektur abzuschließen, öffnen Sie den Umlagerungsauftrag erneut, geben Sie die richtige Menge ein und buchen Sie dann den Auftrag. Wenn Sie Lagerversand verwenden, um den auftrag zu versenden, erstellen und buchen Sie einen neuen Warenausgang.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Buchen Sie mehrere Umlagerungsaufträge in einem Stapel

Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen in einer Charge buchen.

1. 1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Umlagerungsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Aufträge übertragen** die zu buchenden Aufträge aus.
3. Geben Sie im Feld **Nr.** öffnen Sie das Kontextmenü und wählen Sie **Mehr auswählen**.
4. Wählen Sie das Kontrollkästchen für die Zeilen für jeden Auftrag, den Sie buchen möchten.
5. Wählen Sie die Aktion  **Buchen**  und anschließend  **Stapel buchen**.
6. Füllen Sie auf der Seite **Chargen-Umlagerungsauftrag** die Felder nach Bedarf aus.

   > [!TIP]
    > Für Umlagerungsaufträge, die einen Transitstandort verwenden, können Sie entweder **Versenden** oder **Empfangen** auswählen. Wiederholen Sie diesen Schritt, wenn Sie beides tun müssen. Bei Bestellungen, bei denen **Direktbuchung** aktiviert ist, funktionieren beide Optionen auf die gleiche Weise und buchen die Bestellung vollständig.

7. Wählen Sie **OK** aus.
8. Um mögliche Probleme anzuzeigen, öffnen Sie die Seite **Fehlermeldungsregister** .

    > [!NOTE]
    > Das Buchen mehrerer Dokumente kann einige Zeit dauern und andere Benutzer blockieren. Erwägen Sie die Aktivierung der Hintergrundbuchung. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](/dynamics365/business-central/admin-job-queues-schedule-tasks)

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Planen Sie einen Auftragswarteschlangeneintrag, um mehrere Dokumente in einem Stapel zu veröffentlichen

Alternativ können Sie die Auftragswarteschlange verwenden, um die Veröffentlichung zu einem Zeitpunkt zu planen, der für Ihre Organisation günstig ist. Beispielsweise kann es für Ihre Geschäft sinnvoll sein, bestimmte Routinen dann auszuführen, wenn ein Großteil der Dateneingaben für einen Arbeitstag abgeschlossen wurde.

Der folgende Ablauf zeigt, wie Sie den Bericht **Stapelbuchung von Verkaufsaufträgen** so festlegen, dass direkte Umlagerungen automatisch an Wochentagen um 16:00 Uhr gebucht werden. Diese Zeit ist nur ein Beispiel. Die Schritte sind für die anderen unterstützten Dokumente gleich.  

1. Suchen Sie die Seite für **Aufgabenwarteschlangeneinträge** und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu**.  
3. Wählen Sie im Feld **Auszuführender Objekttyp** die Option **Bericht** aus.  
4. Wählen Sie im Feld **Auszuführende Objekt-ID** **5707, Stapelbuchung von Verkaufsaufträgen** aus.
5. Aktivieren Sie das Kontrollkästchen **Berichtsanforderungsseite**.
6. Wählen Sie auf der Anforderungsseite **Chargen-Buchung-Übertragungsaufträge** die Option **Versenden** aus und filtern Sie nach **Direktübertragung** und wählen Sie dann **OK**.

   > [!IMPORTANT]
   > Es ist wichtig, Filter zu setzen. Andernfalls wird [!INCLUDE [prod_short](includes/prod_short.md)] alle Dokumente veröffentlichen, auch wenn sie noch nicht fertig sind. Ziehen Sie in Betracht, für das Feld **Status** einen Filter für den Wert **Freigegeben** zu setzen, sowie einen Filter für das Feld **Buchungsdatum** für den Wert **Heute**. Weitere Informationen zu Filter finden Sie unter [Sortieren, Suchen und Filtern](/dynamics365/business-central/ui-enter-criteria-filters).

7. Wählen Sie alle Kontrollkästchen von **Montags ausführen** bis **Freitags ausführen**.
8. In dem Feld **Startzeit** geben Sie **16:00 Uhr** ein.
9. Wählen Sie die Aktion **Status auf bereit festlegen** aus.

### <a name="comparison-of-different-settings-for-transfer-orders"></a>Vergleich verschiedener Einstellungen für Transportaufträge

Sie können Transportaufträge in verschiedenen Modi buchen, mit oder ohne Transportort. Deaktivieren Sie den Schalter  **Direktüberweisung**  und Auswählen den temporären Standort im Feld  **Unterwegscode**  auf der Seite  **Überweisungsauftrag** . Wenn Sie die Lieferung eines Umlagerungsauftrags buchen, der den Lagerort „Unterwegs“ verwendet, sind die Artikel in der Zeile an einem Ihrer Lagerorte nicht mehr verfügbar, da sie sich im Transport befinden. Direktbuchung stellt sicher, dass kein Standort während des Transports verwendet wird und dass Versand und Empfang gleichzeitig erfolgen. Das genaue Verhalten von Direktbuchung kann je nach dem im Feld  **Direkte Umbuchung**  auf der Seite  **Lagereinrichtung**  ausgewählten Wert unterschiedlich sein.

In der folgenden Tabelle werden die Unterschiede zwischen den Kombinationen beschrieben.

|Fähigkeit|Das Feld  **Direktüberweisung**  ist auf der Seite  **Überweisungsauftrag**  deaktiviert.|**Direkte Überweisung** ist auf der Seite  **Überweisungsauftrag** aktiviert.</br>**Direkte Umbuchung** ist auf der Seite  **Lagereinrichtung** auf  **Direkte Umbuchung** eingestellt.|**Direkte Überweisung** ist auf der Seite  **Überweisungsauftrag** aktiviert.</br>**Direkte Umbuchung** ist auf der Seite  **Lagereinrichtung** auf  **Empfang und Versand**  eingestellt.|
|---|---|---|---|
|Standort während des Transports verwenden|Ja|Nein|Nein|
|Kann Quittung ohne Versand posten.</br>Kann den  **Empfang rückgängig machen** verwenden.|Ja|Nein|Nein|
|Teilbuchung|Ja|Nein|Ja|
|Artikelposten|4:</br>Transfer vom Ab-Standort,</br>Transfer zu In-Transit,</br>Transfer von In-Transit,</br>Transfer zum Zielort.|2:</br>Transfer vom Ab-Standort,</br>Transfer zum Zielort.|4:</br>Transfer vom Ab-Standort,</br>Übertragen auf *leer*,</br>Überweisung von *leer*,</br>Transfer zum Zielort.|
|Eingestellte Dokumente|Versendete Transfersendung,</br>Überweisungsbeleg gebucht.|Gebuchte Direktüberweisung|Versendete Transfersendung,</br>Überweisungsbeleg gebucht.|
|Reservierung: Ein- und Ausreise|Ja|Ja|Ja|
|Artikelgebühren – dem gebuchten Überweisungsbeleg zuordnen|Ja|Nein|Ja|
|Lagerabwicklung|Vollständig|Nein|Begrenzt, (siehe unten|

Lagerabwicklungsmatrix für die Konfiguration:  **Direktübertragung**  ist auf der Seite  **Transferauftrag**  aktiviert und  **Direktübertragungsbuchung**  ist auf der Seite  **Lagereinrichtung**  auf  **Direktübertragung**  eingestellt.

|Von \ Bis|An: Kein Lagerumschlag|An: Lagerschein|An: Lagereinlagerung|Nach: Gezielte Einlagerung und Kommissionierung|
|-|-|-|-|-|
|**Von: Kein Lagerumschlag**|0|Nicht unterstützt|1, 4|Nicht unterstützt|
|**Von: Lagerversand**|1, 2|Nicht unterstützt|1,2,4|Nicht unterstützt|
|**Von: Lagereinlagerung**|1, 3|Nicht unterstützt|1,3,4|Nicht unterstützt|
|**Von: Gezielte Einlagerung und Kommissionierung**|2|Nicht unterstützt|2|Nicht unterstützt|

Die Zahlen in den Zellen zeigen die unterstützten Buchungsoptionen.

1. Buchen aus Überweisungsauftrag. Bei manchen Kombinationen müssen Sie möglicherweise das Feld  **Zu versendende Menge**  ausfüllen.
2. Erstellen und buchen Sie einen Lagerversand.
3. Erstellen und buchen Sie eine Lagerkommissionierung.
4. Erstellen und buchen Sie eine Lagereinlagerung. Bei manchen Kombinationen müssen Sie möglicherweise das Feld  **Zu versendende Menge**  ausfüllen.

Unabhängig von der Methode werden die Versand- und Empfangstransaktionen durchgeführt. Sie können beispielsweise einen Transportauftrag von einem Standort, der eine Kommissionierung erfordert, zu einem Standort erstellen, der eine Einlagerung erfordert. Sie können die Lagereinlagerung erstellen und buchen. Außerdem werden sowohl die Versand- als auch die Empfangstransaktionen erstellt. Sie können solche Belege auch aus einem Transportauftrag oder einer Lagerkommissionierung heraus buchen.  

Weitere Informationen zur Lagerverwaltung finden Sie unter  [Übersicht zur Lagerverwaltung](design-details-warehouse-management.md).

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Element Reclass. Erfassungen** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Umlagerungs Buch.-Blatt** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.

    > [!NOTE]  
    > Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.
4. Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.
5. Wählen Sie die Aktion **Buchen**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]


## <a name="see-also"></a>Siehe auch

[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Lagerorte einrichten](inventory-how-setup-locations.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Angezeigte Features ändern](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
