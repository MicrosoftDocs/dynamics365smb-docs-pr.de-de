---
title: Montagesbuchungen rückgängig machen
description: 'Erfahren Sie, wie Sie Fehler in einem gebuchten Montageauftrag korrigieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="undo-assembly-posting"></a><a name="undo-assembly-posting"></a>Montagesbuchungen rückgängig machen

Machen Sie die Buchung eines Montageauftrags rückgängig, um einen Fehler zu korrigieren oder eine unerwünschte Buchung zu entfernen.

Wenn Sie einen gebuchten Montageauftrag rückgängig machen, werden im Artikelposten Stornobuchungen erstellt, um die Originaleinträge zu stornieren. Jeder positive Istmeldungsposten für den Montageartikel wird durch einen negativen Istmeldungsposten storniert. Jeder negative Istmeldungsposten für den Montageartikel wird durch einen positiven Istmeldungsposten storniert. Die Fixkostenanwendung wird zwischen den Korrektur- und den Originaleinträgen automatisch erstellt, um die genaue Kostenumkehrung sicherzustellen.  

Wenn Sie einen vollständig gebuchten Montageauftrag rückgängig machen, können Sie den ursprünglichen Auftrag wiederherstellen. Zum Beispiel, um Korrekturen vorzunehmen, bevor Sie es erneut posten.  

Wenn Sie einen teilweise gebuchten Montageauftrag rückgängig machen, werden in allen betroffenen Mengenfeldern, wie die Felder **Montagemenge**, **Verbrauchte Menge** und **Verbleibende Menge**, die Werte wiederhergestellt, die diese vor der Buchung enthielten.  

Um Montageaufträge neu zu erstellen oder wiederherzustellen, muss der Artikel in der ursprünglichen Buchung die folgenden Bedingungen erfüllen:  

* Es ist noch im Inventar. Das heißt, er wurde nicht verkauft oder durch andere ausgehende Transaktionen verbraucht.  
* Er ist nicht reserviert.  
* Er ist an dem Lagerplatz, an dem er ausgegeben wurde.  

Montageaufträge können nur wiederhergestellt werden, wenn die Anzahl und die Reihenfolge der Zeilen im ursprünglichen Montageauftrag nicht geändert wurden.  

> [!TIP]  
> Um Konflikte durch Änderungen in den Zeilen aufzulösen, können Sie die Änderungen in den Zeilen manuell zurücknehmen, bevor Sie den gebuchten Montageauftrag rückgängig machen. Sie können den Montageauftrag buchen und dann neu erstellen, wenn Sie die Buchung rückgängig machen.  

Nachfolgend wird beschrieben, wie gebuchte Montageaufträge rückgängig gemacht, die Artikel enthalten, die für das Lager montiert werden. Um gebuchte Montageaufträge mit Artikeln rückgängig zu machen, die auf Bestellung montiert wurden, verwenden Sie die Aktion **Lieferung rückgängig machen** für die zugehörige gebuchte Lieferung. Um mehr über das Rückgängigmachen von Lieferungen zu erfahren, gehen Sie zu [Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md). Stornieren des gebuchten Montageauftrags erfolgt auf die gleiche Art, wie in diesem Artikel beschrieben.  

## <a name="to-undo-posting-of-an-assembly-order"></a><a name="to-undo-posting-of-an-assembly-order"></a>Um die Buchung eines Montageauftrags rückgängig zu machen

Sie können gebuchte Montageaufträge ganz oder teilweise rückgängig machen.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Gebuchte Montageaufträge** ein und wählen Sie den zugehörigen Link.  

   Für jede Teilbuchung wird ein separater gebuchten Montageauftrag erstellt.  
2. Öffnen Sie den gebuchten Montageauftrag, den Sie stornieren möchten, und wählen Sie dann die Aktion **Montage rückgängig machen** aus.  

    Wenn der gebuchte Montageauftrag mit einem vollständig gebuchten Montageauftrag verknüpft ist, der gelöscht wurde, können Sie den gelöschten Auftrag neu erstellen. Beispielsweise können Sie die Bestellung neu erstellen, weil Sie sie erneut verarbeiten möchten.  
3. Um den Montageauftrag neu zu erstellen, wählen Sie **Ja**. Um die Buchung zu stornieren, ohne den Montageauftrag neu zu erstellen, wählen Sie **Nein**.  

Das Feld **Reserviert** im Montageauftrag wird in **Ja** geändert. Die Montageauftragsbuchung ist nun storniert. Sie können den gesamten Montageauftrag verarbeiten, wenn Sie ihn neu erstellen möchten, oder den offenen Montageauftrag, den Sie in seinen ursprünglichen Zustand zurückversetzt haben.  

> [!NOTE]  
> Um Mengen aus mehreren Teilbuchungen in einem Montageauftrag wiederherzustellen, müssen Sie alle gebuchten Montageaufträge oben rückgängig machen, indem Sie die nachfolgenden Schritte 1 bis 3 durchführen.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md)  
[Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
