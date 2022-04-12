---
title: Montagesbuchungen rückgängig machen
description: Es kann vorkommen, dass Sie einen gebuchten Montageauftrag rückgängig machen müssen, z.B. wenn der Auftrag mit Fehlern gebucht wurde, die korrigiert werden müssen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: a485162cb194f7f16ff7c33c3e4a095865d35daf
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520464"
---
# <a name="undo-assembly-posting"></a>Montagesbuchungen rückgängig machen
In einigen Fällen müssen Sie einem gebuchten Montageauftrag rückgängig machen, wenn der Auftrag zum Beispiel mit Fehlern gebucht wurde, die korrigiert werden müssen, oder weil er nicht im ersten Schritt gebucht werden sollte und zurückgenommen werden muss.

Wenn Sie einen gebuchten Montageauftrag rückgängig machen, wird im Artikelposten ein Satz Stornobuchungen erstellt, um die Originaleinträge zu stornieren. Jeder positive Istmeldungsposten für den Montageartikel wird durch einen negativen Istmeldungsposten storniert. Jeder negative Istmeldungsposten für den Montageartikel wird durch einen positiven Istmeldungsposten storniert. Die Fixkostenanwendung wird zwischen den Korrektur- und den Originaleinträgen automatisch erstellt, um die genaue Kostenumkehrung sicherzustellen.  

Wenn Sie einen vollständig gebuchten Montageauftrag rückgängig machen, können Sie auswählen, dass der Montageauftrag im ursprünglichen Zustand neu erzeugt wird, zum Beispiel, um Korrekturen vorzunehmen, bevor Sie ihn wieder buchen. Alternativ können Sie auswählen, dass der Montageauftrag nicht neu erstellt wird.  

Wenn Sie einen teilweise gebuchten Montageauftrag rückgängig machen, werden in allen betroffenen Mengenfeldern, wie die Felder **Montagemenge**, **Verbrauchte Menge** und **Verbleibende Menge**, die Werte wiederhergestellt, die diese vor der entsprechenden Buchung enthielten.  

Um Montageaufträge neu zu erstellen oder wiederherzustellen, müssen für den Montageartikel die folgenden Anforderungen gelten, die in der ursprünglichen Buchung registriert wurden:  

-   Er muss noch im Lager sein, das heißt, er wurde nicht verkauft oder durch andere ausgehende Transaktionen verbraucht.  
-   Er darf nicht reserviert sein.  
-   Er muss an dem Lagerplatz vorhanden sind, an dem er registriert wurde.  

Darüber hinaus können vorhandene Montageaufträge nur wiederhergestellt werden, wenn die Anzahl der Zeilen und die Reihenfolge der Zeilen im ursprünglichen Montageauftrag nicht geändert wurden.  

> [!TIP]  
>  Um Konflikte aufgrund von Zeilenänderungen aufzulösen, können Sie die Änderungen in den Zeilen manuell zurücknehmen, bevor Sie den zugehörigen gebuchten Montageauftrag rückgängig machen. Alternativ können Sie den Montageauftrag vollständig buchen und dann auswählen, dass er neu erstellt wird, wenn Sie die Buchung rückgängig machen.  

Nachfolgend wird beschrieben, wie gebuchte Montageaufträge rückgängig gemacht, in denen Artikel für das Lager montiert werden. Wenn Sie gebuchte Montageaufträge rückgängig machen möchten, in denen die Artikel für einen Auftrag montiert wurden, müssen Sie in der gebuchten Lieferung, die zu dem gebuchten Montageauftrag gehört, die Funktion **Warenausgang stornieren** verwenden. Weitere Informationen finden Sie unter [Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md). Das Stornieren des gebuchten Montageauftrags erfolgt dann automatisch und auf die gleiche Art, wie in diesem Thema beschrieben.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Um die Buchung eines Montageauftrags rückgängig zu machen  
1.  Um einen ganz oder teilweise gebuchten Montage-Auftrag rückgängig zu machen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Gebuchte Montageaufträge** ein und wählen Sie den zugehörigen Link.  

    Die Seite **Gebuchte Montageaufträge** wird geöffnet und zeigt einen oder mehrere gebuchte Montageaufträge an, die über den entsprechenden Montageauftrag gebucht wurden. Für jede Teilbuchung wird ein separater gebuchten Montageauftrag erstellt.  
2.  Öffnen Sie den gebuchten Montageauftrag, den Sie stornieren möchten, und wählen Sie dann die Aktion **Montage rückgängig machen** aus.  

    Wenn der gebuchte Montageauftrag, den Sie stornieren möchten, mit einem vollständig gebuchten Montageauftrag verknüpft ist, der jetzt gelöscht wird, haben Sie die Möglichkeit, diesen neu zu erstellen, um ihn gegebenenfalls erneut zu bearbeiten.  
3.  Wenn Sie den Montageauftrag neu erstellen möchten, wählen Sie die Schaltfläche **Ja**. Um die Buchung zu stornieren, ohne den verknüpften Montageauftrag neu zu erstellen, wählen Sie die Schaltfläche **Nein**.  

Das Feld **Reserviert** im Montageauftragskopf wird in **Ja** geändert. Die Montageauftragsbuchung wird jetzt storniert, und Sie können fortfahren, den gesamten Montageauftrag zu verarbeiten, wenn Sie ihn wiederherstellen möchten, oder den offenen Montageauftrag, den Sie mit dem ursprünglichen Status wiederhergestellt haben.  

> [!NOTE]  
>  Um Mengen aus mehreren Teilbuchungen in einem Montageauftrag wiederherzustellen, müssen Sie alle gebuchten Montageaufträge oben rückgängig machen, indem Sie die nachfolgenden Schritte 1 bis 3 für jeden gebuchten Montageauftrag durchführen.  

## <a name="see-also"></a>Siehe auch  
[Montageverwaltung](assembly-assemble-items.md)  
[Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md)  
[Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md)    
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Bestand](inventory-manage-inventory.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]