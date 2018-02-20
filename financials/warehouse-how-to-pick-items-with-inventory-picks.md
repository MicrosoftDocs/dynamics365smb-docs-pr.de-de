---
title: 'So wird''s gemacht: Artikel mit der Lagerkommissionierung kommissionieren | Microsoft Docs'
description: "Wenn ein Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie Lagerkommissionierbelege, um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7e5d30ec5775030c523b73f90490428531f49fec
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="pick-items-with-inventory-picks"></a>Artikel mit der Lagerkommissionierung kommissionieren
Wenn Ihr Lagerort so eingerichtet wurde, dass Kommissionierung erforderlich ist, jedoch Warenausgang nicht erforderlich ist, verwenden Sie das Fenster **Lagerkommissionierung**, um Kommissionier- und Warenausgangsinformationen für Ihre Herkunftsbelege zu erfassen und zu buchen. Der ausgehende Herkunftsbeleg kann ein Verkaufsauftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag oder ein Fertigungsauftrag sein, dessen Komponenten zum Kommissionieren bereitstehen.

> [!NOTE]  
> Komponenten für Montageaufträge können nicht mit Lagerkommissionierungen kommissioniert oder gebucht werden. Verwenden Sie stattdessen das Fenster **Lagerbestandsumlagerung**. Weitere Informationen finden Sie in[Umlagern von Komponenten in einen Arbeitsgangbereich in den grundlegenden Lagerfunktionen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

>  Bei der Kommissionierung und Lieferung von Verkaufszeilenmengen, die auftragsbezogen montiert werden, müssen Sie bestimmte Regeln einhalten, wenn sie die Lagerkommissionierzeilen erstellen. Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in Lagerkommissionierungen".  

Sie können eine Lagerkommissionierung auf drei Arten erstellen:  

- Erstellen Sie die Kommissionierung in zwei Schritten, indem Sie zuerst eine Lagerkommissionierung anfordern, indem Sie den Herkunftsbeleg freigeben. Dies signalisiert dem Lager, dass der Herkunftsbeleg für die Kommissionierung bereit ist. Die Lagereinkommissionierung kann dann im Fenster **Lagereinlagerung** erstellt werden, die auf dem Herkunftsbeleg basiert.  
- Erstellen Sie die Lagerkommissionierung direkt vom Herkunftsbeleg aus.  
- Sie können für mehrere Herkunftsbelege gleichzeitig Lagerkommissionierungen erstellen, indem Sie einen Batchauftrag verwenden.  

## <a name="to-request-an-inventory-pick-by-releasing-the-source-document"></a>So fordern Sie eine Lagerkommissionierung durch Freigabe des Herkunftsbelegs an  
Bei Verkaufsaufträgen, Einkaufsreklamationen und ausgehenden Umlagerungsaufträgen erstellen Sie die erwartete Lagerbewegung, indem Sie den Auftrag freigeben. Nachfolgend wird erläutert, wie dies mit einem Verkaufsauftrag erreicht wird.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus, geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Verkaufsauftrag, den Sie freigeben möchten, und wählen Sie die **Freigeben** Aktion aus.

Bei Fertigungsaufträgen erzeugen Sie die erwartete Lagerbewegung für das Kommissionieren der Komponenten automatisch (dies wird *Vorwärtsbuchen* genannt), wenn der Status des Fertigungsauftrags in **Freigegeben** geändert wird oder wenn der freigegebene Fertigungsauftrag erstellt wird. Weitere Informationen finden Sie unter [Kommissionierung für die Produktion oder Montage](warehouse-how-to-pick-for-production.md).

Nachdem die erwartete Lagerbewegung erzeugt wurde, kann ein Lagermitarbeiter, der der Kommissionierung von Artikeln zugewiesen wurde, sehen, dass der Herkunftsbeleg zur Kommissionierung bereitsteht, und einen neuen Kommissionierbeleg auf Grundlage der erwarteten Lagerbewegung aus erstellen.  

## <a name="to-create-an-inventory-pick-based-on-the-source-document"></a>So erstellen Sie eine Lagerkommissionierung auf Grundlage des Herkunftsbelegs
Nachdem die Anforderung erstellt wurde, kann der Lagermitarbeiter eine neue Lagerkommissionierung auf Grundlage des freigegebenen Herkunftsbelegs erstellen.
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerkommissionierung** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Herkunftsbeleg** die Art des Herkunftsbelegs aus, auf dem die Kommissionierung basiert.  
4. Wählen Sie im Feld **Herkunftsnr.** den Herkunftsbeleg aus.  
5. Oder wählen Sie die Aktion **Herkunftsbeleg holen** aus, um den Beleg aus einer Liste von ausgehenden Herkunftsbelegen auszuwählen, die zur Kommissionierung am Lagerort bereit sind.  
6. Wählen Sie die Schaltfläche **OK**, um die Kommissionierungszeilen gemäß dem ausgewählten Herkunftsbeleg auszufüllen.  

## <a name="to-create-an-inventory-pick-from-the-source-document"></a>Eine Lagerkommissionierung vom Herkunftsbeleg aus erstellen  
1.  Im Herkunftsbeleg, der ein Auftrag, eine Einkaufsreklamation, ein ausgehender Umlagerungsauftrag oder ein Fertigungsauftrag sein kann, klicken Sie auf die Aktion **Lagerbelege erstellen**.
2.  Aktivieren Sie das Kontrollkästchen **Lagerkomm. erst.**  
3.  Wählen Sie die Schaltfläche **OK** aus. Eine neue Lagerkommissionierung wird erstellt.

## <a name="to-create-multiple-inventory-picks-with-a-batch-job"></a>Mehrere Lagerkommissionierungen mit einem Batchauftrag erstellen  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerbelege erstellen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Verwenden Sie im Inforegister **Erwartete Lagerbewegung** die Felder **Herkunftsbeleg** und **Herkunftsnr.**, um Filter auf bestimmte Arten von Belegen oder Bereiche von Belegnummern zu setzen. Beispielsweise können Sie Kommissionierungen nur für Verkaufsaufträge erstellen.  
3. Aktivieren Sie im Inforegister **Optionen** das Kontrollkästchen **Lagerkomm. erst.** aus.
4. Wählen Sie die Schaltfläche **OK** aus. Die angegebenen Lagerkommissionierungen werden erstellt.

> [!NOTE]  
>  Bei der Kommissionierung und Lieferung von Verkaufszeilenmengen, die auftragsbezogen montiert werden, sollten Sie bestimmte Regeln einhalten, wenn sie die Lagerkommissionierzeilen erstellen. Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in Lagerkommissionierungen".  
>   
>  In den Basis-Lagerkonfigurationen werden Artikel, die nach Verkaufsauftrag montiert werden, aus dem entsprechenden Verkaufsauftrag kommissioniert, wie in diesem Thema erläutert. Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in Lagerkommissionierungen" in der Lagerkommissionierung.  

## <a name="to-record-the-inventory-picks"></a>So erfassen Sie die Lagerkommissionierungen  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerkommissionierung** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie im Feld **Lagerplatzcode** auf den Kommissionierungszeilen wird der Lagerplatz der Kommissionierung entsprechend des Standardlagerplatzes des Artikels vorgeschlagen. Sie können – falls erforderlich – in diesem Fenster den Lagerplatz ändern.  
3. Führen Sie die Kommissionierung durch und geben Sie die Informationen über die tatsächlich eingelagerte Menge in das Feld **Bewegungsmenge** ein.

    Wenn es erforderlich ist, die Artikel einer Zeile aus mehr als einem Lagerplatz zu kommissionieren, beispielsweise, da sie im designierte Lagerplatz nicht verfügbar sind, verwenden Sie die Funktion **Zeile aufteilen** im Inforegister **Zeilen**. Weitere Informationen über das Aufteilen von Zeilen finden Sie unter [Aufteilen von Lageraktivitätszeilen](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Wenn Sie die Kommissionierung durchgeführt haben, wählen Sie die **Buchen** Aktion aus.    

Der Buchungsvorgang bucht die Lieferung der Herkunftsbelegzeilen, die kommissioniert wurden. Bei Fertigungsaufträgen wird durch den Buchungsvorgang der Verbrauch gebucht. Wenn der Lagerort Lagerplätze verwendet, erzeugt der Buchungsvorgang darüber hinaus Lagerplatzposten, um die Mengenänderungen in den Lagerplätzen zu buchen.  

## <a name="to-delete-inventory-pick-lines"></a>Lagerkommissionierzeilen löschen  
Wenn Artikel in der Lagerkommissionierung nicht verfügbar sind, können Sie die Lagerkommissionierzeilen normalerweise löschen, nachdem Sie sie gebucht haben, und dann den Lagerkommissionierungsbeleg löschen. Der Herkunftsbeleg, beispielsweise ein Verkaufsauftrag oder ein Fertigungsauftrag, enthält dann restliche Artikel zum Kommissionieren, die später durch eine neue Lagerkommissionierung erhalten werden können, wenn die Artikel verfügbar werden.  

> [!WARNING]  
>  Dieser Prozess ist nicht möglich, wenn Serien-/Chargennummern im Herkunftsbeleg angegeben werden. Wenn beispielsweise eine Verkaufsauftragszeile eine Serien-/Chargennummer enthält, wird diese Artikelverfolgungsspezifikationen gelöscht, wenn eine Lagerkommissionierungszeile für die Serien-/Chargennummer gelöscht wird.  
>   
>  Wenn Lagerkommissionierzeilen Serien-/Chargennummern haben, die nicht verfügbar sind, dürfen Sie die entsprechenden Zeilen nicht löschen. Stattdessen müssen Sie das Feld **Qualitätshandhabung** in null ändern, die tatsächlichen Kommissionierungen buchen und den Lagerkommissionierungsbeleg dann löschen. Dadurch ist sichergestellt, dass die Lagerkommissionierzeilen für diese Serien-/Chargennummern später aus dem Verkaufsauftrag wiederhergestellt werden können.  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Verarbeiten von Auftragsmontageartikel mit Lagerkommissionierungen
Das Fenster **Lagerkommissionierung** wird auch verwendet, um für Verkäufe zu kommissionieren und zu liefern, in denen Artikel montiert werden müssen, bevor sie geliefert werden können. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).

Die zu liefernden Artikel sind an einem Lagerplatz erst dann tatsächlich vorhanden, wenn sie zusammengestellt und als Ausstoß für einen Lagerplatz im Montagebereich gebucht wurden. Das bedeutet, dass das Kommissionieren von Auftragsmontageartikeln zur Lieferung einem speziellen Ablauf folgt. Von einem Lagerplatz bringen Lagermitarbeiter die Montageartikel zur Versandstelle und buchen dann die Lagerkommissionierung. Die gebuchte Lagerkommissionierung bucht dann den Montageausstoß, den Komponentenverbrauch und die Verkaufslieferung.

Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] einrichten, um eine automatische Lagerbestandsumlagerung zu erstellen, wenn die Lagerkommissionierung für die Montageartikel erstellt wird. Um dies zu aktivieren, müssen Sie das Feld **Umlagerungen automatisch erstellen** im Fenster **Montageeinrichtung** auswählen. Weitere Informationen finden Sie in[Umlagern von Komponenten in einen Arbeitsgangbereich in den grundlegenden Lagerfunktionen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerkommissionierzeilen für Verkaufsartikel werden je nachdem, ob keine, einige oder alle Verkaufspositionsmengen auf Bestellung gefertigt werden, auf unterschiedliche Weise erstellt.

Bei regulären Verkäufen, wo Sie Lagerkommissionierungen verwenden, um Liefer- und Lagermengen zu buchen, wird eine Verkaufsauftragszeile, oder mehre, wenn der Artikel in verschiedenen Lagerplätzen platziert ist, erstellt für jede Verkaufszeile. Diese Kommissionierzeile basiert auf der Menge im Feld **Zu liefern**.

In Auftragsmontageverkäufen, bei denen die gesamte Menge aus der Verkaufsauftragszeile montiert wird, wird eine Lagerkommissionierzeile für diese Menge erstellt. Das bedeutet, dass der Wert im Feld "Menge für Montage" dem Wert im Feld **Zu liefern** entspricht. Das Feld **Auftragsmontage** wird in der Zeile ausgewählt.

Wenn ein Montageausgabefluss für den Lagerort eingerichtet wird, wird der Wert im Feld **LP-Code f. Prog.fert.lief.** oder der Wert im Feld **Montage-Ausgangslagerplatzcode** in dieser Reihenfolge in das Feld **Lagerplatzcode** in der Lagerkommissionierzeile eingefügt.

Wenn kein Lagerplatzcode in der Verkaufsauftragszeile angegeben wird und kein Montageausgabefluss für den Lagerort eingerichtet wird, bleibt das Feld **Lagerplatzcode** in der Lagerkommissionierzeile leer. Der Lagermitarbeiter muss das Fenster **Lagerplatzinhalte** öffnen und den Lagerort auswählen, in dem die Montageartikel montiert werden.

In Kombinationsszenarien in denen ein Teil der Menge zunächst montiert werden muss und andere aus dem Lager kommissioniert werden müssen, werden mindestens zwei Lagerkommissionierzeilen erstellt. Eine Kommissionierzeile ist für die Programmfertigungsmenge. Die andere Kommissionierzeile hängt davon ab, welche Lagerplätze die Restmenge aus dem Lagerbestand erfüllen können. Lagerplatzcodes in den beiden Zeilen werden auf verschiedene Weise ausgefüllt, wie für die beiden verschiedenen Verkaufsarten beschrieben. Weitere Informationen finden Sie im Abschnitt "Kombinationsszenarien" in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

