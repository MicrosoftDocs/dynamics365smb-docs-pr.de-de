---
title: 'Vorgehensweise: Montagebuchung stornieren | Microsoft Docs'
description: In einigen Fällen müssen Sie einem gebuchten Montageauftrag rückgängig machen, wenn der Auftrag zum Beispiel mit Fehlern gebucht wurde, die korrigiert werden müssen, oder weil er nicht im ersten Schritt gebucht werden sollte und zurückgenommen werden muss.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 11041ebb7c7154eed6959a99ec5b100c73ccd8c6
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880760"
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
1.  Um einen teilweise oder vollständig gebuchten Montageauftrag rückgängig zu machen, wählen Sie das Symbol ![Glühlampe, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, und geben Sie **Gebuchte Montageaufträge** ein und wählen den zugehörigen Link aus.  

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
[Lagerbestand](inventory-manage-inventory.md)  
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
