---
title: 'Vorgehensweise: Entfernen und erneutes Ausgleichen von Artikelpostens | Microsoft Docs'
description: "Sie können bestimmte Artikelausgleichsposten, die bei Lagertransaktionen automatisch erstellt werden, anzeigen und manuell ändern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 12bde7fc508bb29e56ad63d76b526a80b5073f03
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="remove-and-reapply-item-ledger-entries"></a>Entfernen und erneutes Ausgleichen von Artikelposten
Sie können im Fenster **Ausgleichsvorschlag** bestimmte Artikelausgleichsposten, die bei Lagertransaktionen automatisch erstellt werden, anzeigen und manuell ändern.  

Wenn Sie eine Transaktion buchen, in der Artikel in den oder aus dem Lagerbestand verschoben werden, wird ein Artikelausgleich zwischen jedem Lagerzugang und Lagerabgang erstellt. Diese Ausgleiche bestimmen die Richtung für die Kosten von den Waren, die in den Lagerbestand übernommen wurden, zu den Kosten der Waren, die aus dem Lagerbestand herausgenommen wurden. Wegen der Art, in der Einstandspreise berechnet werden, könnte ein fehlerhafter Artikelausgleich zu falschen Durchschnittskosten und zu falschen Einstandspreisen führen. Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".

Der folgende Szenarios erfordern möglicherweise, dass Sie einen Ausgleich rückgängig machen oder Artikelposten erneut ausgleichen:

- Sie haben vergessen, einen festen Ausgleich vorzunehmen.
- Sie haben einen fehlerhaften festen Ausgleich vorgenommen.
- Sie müssen einen Artikel zurücknehmen, für den bereits ein Verkauf ausgeglichen wurde.

Wenn möglich, verwenden Sie einen Beleg, um einen Artikelposten erneut auszugleichen. Wenn Sie beispielsweise eine Einkaufsreklamation für einen Artikel vornehmen müssen, für den bereits ein Verkauf ausgeglichen wurde, können Sie den erneuten Ausgleich vornehmen, indem Sie einfach den Einkaufsreklamationsbeleg in der Einkaufsreklamationszeile im Feld **Ausgleich mit Artikelposten** mit dem richtigen Ausgleich erstellen und buchen. Sie können im Einkaufsreklamationsbeleg die Funktion **Zu stornierende gebuchte Belegzeilen abrufen** oder die Funktion **Beleg kopieren** verwenden, um diesen Vorgang zu vereinfachen. Wenn Sie den Beleg buchen, wird automatisch der Artikelposten erneut ausgeglichen. Weitere Informationen finden Sie unter [Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

Wenn Sie keinen Beleg verwenden können, um erneut auszugleichen, zum Beispiel wenn Sie einen festen Ausgleich korrigieren müssen, verwenden Sie das Fenster **Ausgleichsvorschlag**, um einen Ausgleich zu korrigieren.

> [!Warning]
> Im Folgenden einige wichtige Überlegungen zur Arbeit mit dem Ausgleichsvorschlag:
>     - Sie sollten Ausgleichsposten nicht über einen längeren Zeitraum ohne Ausgleich lassen, da andere Benutzer die Artikel erst bearbeiten können, wenn Sie die Ausgleichsposten erneut ausgeglichen oder das Fenster **Ausgleichsvorschlag** geschlossen haben. Benutzer, die versuchen, Aktionen auszuführen, die einen manuell nicht ausgeglichenen Ausgleichsposten betreffen, erhalten die folgende Fehlermeldung: "Sie können diese Aktion nicht ausführen, da Posten für Artikel XXX im Ausgleichsvorschlag vom Benutzer XXX aufgehoben wird. "
>     - Sie sollten Artikelposten nur außerhalb der Kernarbeitszeiten erneut ausgleichen, um Konflikte mit anderen Benutzern zu vermeiden, die Transaktionen zu den gleichen Artikeln buchen.
>     - Wenn Sie den Ausgleichsvorschlag schließen, führt [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Prüfung durch, um sicherzustellen, dass alle Posten ausgeglichen wurden. Wenn Sie beispielsweise einen Mengenausgleich entfernt, jedoch keinen neuen Ausgleich erstellt haben und den Ausgleichsvorschlag dann schließen, wird ein neuer Ausgleich erzeugt. Dies trägt dazu bei, die Kosten intakt zu halten. Beim Entfernen eines festen Ausgleichs wird jedoch nicht automatisch ein neuer fester Ausgleich erstellt, wenn Sie den Ausgleichsvorschlag schließen. Dies muss manuell erfolgen, indem Sie im Vorschlag einen neuen Ausgleich erstellen.
>     - Es ist möglich, einen oder mehrere Ausgleiche gleichzeitig für einen Posten im Ausgleichsvorschlag zu entfernen. Da der Ausgleich von Posten jedoch den Satz der zum Ausgleich verfügbaren Posten beeinflusst, ist es nicht möglich, einen Ausgleich für mehr als einen Posten gleichzeitig zu erstellen.
>     - In der folgenden Situation kann über den Ausgleichsvorschlag kein Ausgleich erfolgen: Wenn im Lager nicht genügend Menge zum Ausgleich vorhanden ist, kann über den Ausgleichsvorschlag kein Ausgleich vorgenommen werden, wenn Sie versuchen, einen Lagerabgangsposten ohne Artikelverfolgungsinformationen mit einem Lagerzugangsposten mit Artikelverfolgungsinformationen auszugleichen.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Artikelausgleich mit dem Ausgleichsformular entfernen  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Ausgleichsvorschlag** ein und wählen dann den zugehörigen Link aus.  
2. Das Fenster **Ausgleichsvorschlag** wird geöffnet und zeigt bestehende das Artikelposten für alle Artikel an.  
3. Geben Sie im Inforegister **Allgemein** Filter ein, um die Suche nach dem Artikelposten, für den Sie den Ausgleich ändern möchten, zu erleichtern.  
4. Wählen Sie den Artikelposten aus, und wählen Sie die Aktionen **Ausgeglichene Posten**. Das Fenster **Ausgeglichene Posten anzeigen – Ausgeglichene Posten** wird geöffnet und zeigt den/die Artikelposten für den Ausgleich mit dem ausgewählten Posten an.  
5. Wählen Sie den Artikelposten aus, für den Sie den Ausgleich entfernen möchten.  
6. Wählen Sie die Aktion **Ausgleich entfernen** aus. Dadurch wird der Artikelausgleichsposten, der die beiden Artikelposten verknüpft, entfernt und in das Fenster **Ausgleichsposten anzeigen - nicht ausgeglichene Posten** verschoben.  
7. Schließen Sie das Fenster **Ausgeglichene Posten anzeigen – Ausgeglichene Posten**.  

   Für beide Artikelposten wird das jeweilige Feld **Restmenge** um die Menge erhöht, deren Ausgleich aufgehoben wurde. Der entfernte Artikelposten ist jetzt für den erneuten Ausgleich im Fenster **Ausgeglichene Posten anzeigen – Nicht ausgeglichene Posten** verfügbar.  

> [!IMPORTANT]  
>  Sie sollten Ausgleichsposten nicht über einen längeren Zeitraum ohne Ausgleich lassen, da andere Benutzer die Artikel erst bearbeiten können, wenn Sie die Ausgleichsposten erneut ausgeglichen oder das Fenster **Ausgleichsvorschlag** geschlossen haben. Die folgende Fehlermeldung wird angezeigt, wenn Sie versuchen, Aktionen auszuführen, die einen manuell nicht ausgeglichenen Ausgleichsposten betreffen:  
>   
>  **Diese Aktion kann nicht ausgeführt werden, da der Artikel <item> vom Benutzer <user> im Ausgleichsformular aufgehoben wurde.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Artikelausgleich mit dem Ausgleichsformular erneut ausgleichen  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Ausgleichsvorschlag** ein und wählen dann den zugehörigen Link aus.  
2.  Das Fenster **Ausgleichsvorschlag** wird geöffnet und zeigt bestehende das Artikelposten für alle Artikel an.  
3.  Um Posten erneut auszugleichen, die seit dem Öffnen des Ausgleichsvorschlags entfernt wurden, wählen Sie den Artikelposten aus, den Sie erneut ausgleichen möchten. Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Funktionen** die Option **Erneut ausgleichen** aus.  

    > [!NOTE]  
    >  Der erneute Ausgleich mit dem ursprünglichen Saldo erfolgt auch automatisch, wenn Sie das Fenster **Ausgleichsvorschlag** schließen.  
4.  Wählen Sie zum Ausgleich eines verfügbaren offenen Artikelpostens mit einem anderen Posten den entsprechenden Artikelposten aus. Wählen Sie die Aktion **Nicht ausgeglichene Posten** aus. Das Fenster **Ausgleichsposten anzeigen - nicht ausgeglichene Posten** wird geöffnet.  
5.  Wählen Sie einen oder mehrere Artikelposten aus, die Sie für den Posten im Fenster **Ausgleichsvorschlag.** ausgewählten Posten auswählen, und wählen Sie die Schaltfläche **OK**.  

     Es wird ein Artikelausgleichsposten zwischen den beiden Artikelposten erstellt. Das Feld **Restmenge** der beiden Post wird jeweils um die für den Ausgleich verwendete Menge verringert.  

    > [!NOTE]  
    >  Wenn Sie einen Ausgleich ausgewählt haben, mit dem eine Endlosschleife in der Lagerregulierung erzeugt wird, wird der von Ihnen gewünschte Ausgleich nicht vorgenommen. Dies kommt in Fällen vor, in denen mit den ursprünglichen Posten ein negativer Lagerbestand erzeugt wurde. Der Ausgleich wird nicht vorgenommen. Daher müssen Sie einen anderen Posten für den Ausgleich auswählen.  
6.  Wenn in **Lager Einrichtung** das Feld **Automatische Lagerregulierung** auf **Immer** festgelegt ist, wird die Stapelverarbeitung für Kostenregulierung automatisch ausgeführt, nachdem Sie einen erneuten Ausgleich vorgenommen haben. Führen Sie andernfalls den Batchauftrag **Lagerreg. fakt. Einst. Preise** aus, um sicherzustellen, dass alle Kosten auf dem neuesten Stand sind.  

## <a name="see-also"></a>Siehe auch  
[Schließen von offenen Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md)  
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Artikelausgleich](design-details-item-application.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

