---
title: Artikel zwischen Lagerorten transferieren
description: 'Erfahrten Sie, wie vom Bestand von einem Bereich oder von einem Lager an einen anderen Ort umgebucht wird, entweder mit dem Umlagerungs Buch.-Blatt mit oder den Umlagerungsaufträgen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
---
# Lagerbestand zwischen Lagerplätzen umlagern

Sie können Bestandsartikel zwischen Lagerplätzen umlagern, indem Sie Umlagerungsaufträge erstellen. Sie können auch das Einkaufs-Buch.-Blatt verwenden.

> [!NOTE]
> Um Artikel umzulagern, müssen Sie Lagerplätze und Umlagerungsrouten einrichten. Weitere Informationen zum Einrichten von Lagerorten finden Sie unter [Lagerorte einrichten](inventory-how-setup-locations.md). Sie können keine Umlagerungsaufträge für *leere* Lagerorte verwenden.

## Umlagerungsaufträge

Sie können eine ausgehende Umlagerung von einem Lagerplatz senden und eine eingehende Umlagerung am Ziel empfangen. Sie können:

* Eine Menge in Transit nachverfolgen
* Definieren Sie Kalender, Arbeitspläne sowie eingehende und ausgehende Bearbeitungszeiten für die Datumsberechnung und -planung. Weitere Informationen zur Planung finden Sie unter [Info zu Planungsfunktionen](production-about-planning-functionality.md).
* Verwenden Sie unterschiedliche Lagerfunktionen für eingehende und ausgehende Lagerorte.
* Mit einigen Einschränkungen können Sie Umlagerungsaufträge für direkte Umlagerungen verwenden.

## Buch.-Blätter für die Neuklassifizierung von Artikeln

* Einfache, direkte Umlagerung von Artikeln zwischen Lagerorten.
* Lagern Sie Artikel zwischen Lagerplätzen um. Weitere Informationen zum Umlagern von Artikeln zwischen Lagerplätzen finden Sie unter [Ungeplanmte Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Ändern Sie eine Chargen- oder Seriennummer in eine neue Chargen- oder Seriennummer. Weitere Informationen zur Neuklassifizierung von Serien- und Chargennummern finden Sie unter [Serien- oder Chargennummern neu klassifizieren](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Ändern Sie das Ablaufdatum auf ein neues Datum.
* Klassifizieren Sie Artikel von einem *leeren* Lagerort an einem tatsächlichen Lagerort neu.
* Lageraktivitäten werden nicht verwaltet. Lagereinträge werden erstellt.

## So lagern Sie Artikel mit einem Umlagerungsauftrag um

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Umlagerungsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Umlagerungsauftrag** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Wenn Sie die Felder **Umlag. in Code**, **Zustellercode** und **Zustellertransportartencode** auf der Seite **Umlagerungsroutenspezifikation** ausgefüllt haben, als Sie die Umlagerungsrouten zwischen diesen Lagerorten eingerichtet haben, werden die entsprechenden Felder im Umlagerungsauftrag automatisch ausgefüllt.

    Wenn Sie das Feld **Zustellertransportarten** ausfüllen, wird das Zugangsdatum am Ziellagerplatz berechnet, indem Sie die Transportzeit der Zustellertransportart zum Lieferdatum hinzuaddieren.

3. Um die Zeilen auszufüllen, geben Sie sie entweder manuell ein oder wählen Sie eine der folgenden Optionen unter der Aktion **Funktionen** aus:

    * Wählen Sie die Aktion **Bin-Inhalt abrufen** aus, um vorhandene Elemente aus einem bestimmten Fach am Standort auszuwählen.
    * Wählen Sie **Belegzeilen abrufen** aus, um Elemente auszuwählen, die gerade am Transfer-von-Standort angekommen sind.

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel auszuliefern.
4. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Warenausgang**, und wählen Sie dann die Schaltfläche **OK** aus.

    Die Artikel befinden sich jetzt in der Umlagerung zwischen den angegebenen Lagerplätzen, entsprechend der angegebenen Umlagerungsroute.

    Als Lagermitarbeiter am vom Umlagerungsort fahren sie fort, die Artikel zu empfangen Die Überweisungsauftragspositionen sind dieselben wie im Auslieferungszustand und können nicht bearbeitet werden.
5. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Eingang**, und wählen Sie dann die Schaltfläche **OK** aus.

## So lagern Sie Artikel mit dem Artikel Umlag. Buch.-Blatt um

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Reclass. Erfassungen** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Umlagerungs Buch.-Blatt** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Geben Sie im Feld **Lagerortcode** den Lagerplatz ein, an dem die Artikel aktuell gelagert sind.

    > [!NOTE]  
    > Um Artikel umzulagern die keinen Lagerortcode haben, belassen Sie das Feld **Lagerortcode** leer.
4. Im Feld **Neuer Lagerortcode** geben Sie den Lagerplatz ein, an den Sie die Artikel umlagern möchten.
5. Wählen Sie die Aktion **Buchen**.

## Siehe verwandte [Microsoft Schulungen](/training/modules/transfer-items/)

## Siehe auch

[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Einrichten von Lagerorten](inventory-how-setup-locations.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
