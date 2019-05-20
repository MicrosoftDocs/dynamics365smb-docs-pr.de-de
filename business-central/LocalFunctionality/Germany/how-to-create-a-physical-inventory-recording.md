---
title: So erstellen Sie eine physische Inventurerfassung
description: Nachdem Sie einen Inventurauftrag und die zugehörigen Zeilen erstellt haben, können Sie eine neue Inventurauftragserfassung für diese Inventur erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: d46e5fa0f80cc5df4f6bd296282a780e7e45d97b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246765"
---
# <a name="create-a-physical-inventory-recording"></a>So erstellen Sie eine physische Inventurerfassung
Nachdem Sie einen Inventurauftrag und die zugehörigen Zeilen erstellt haben, können Sie eine neue Inventurauftragserfassung für diese Inventur erstellen.  

Sie können manuell eine physische Inventurerfassung erstellen. Dies erweist sich ggf. als nützlich, wenn die Verwendung von Inventurlisten nicht erforderlich ist und/oder wenn die Lagerbestandsdaten mithilfe eines Scanners ermittelt werden. Sie können eine Inventurerfassung auch dann manuell erstellen, wenn der zugehörige Inventurauftrag keine Zeilen aufweist. Nach Abschluss der Inventurerfassung erzeugt die Anwendung die erforderlichen Inventurauftragszeilen automatisch. Dies kann beispielsweise bei permanenten Inventuren nützlich sein.  

In den meisten Fällen verwenden Sie jedoch einen Batchauftrag, um Lagerbestand zu erfassen. Basierend auf der Inventurerfassung können Sie eine Liste drucken, um die Inventur durchzuführen und die Ergebnisse zu notieren. Anschließend können die Ergebnisse vom Papier in die Inventurerfassungszeilen übertragen werden.  

## <a name="to-create-a-physical-inventory-recording"></a>So erstellen Sie eine Inventurerfassung  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Inventurauftrag aus, für den Sie eine Inventurerfassung erstellen möchten, klicken Sie auf Aktionen und anschließend auf **Bearbeiten**.  
3.  Um eine Inventurerfassung zu erstellen, wählen Sie die Aktion **Neue Erfassung erstellen** aus.  
4.  Füllen Sie auf der Seite **Neue Inventurerfassung erst.** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nur nicht erfasste Zeilen**|Wählen Sie diese Option aus, um nur dann eine neue Inventurerfassungszeile zu generieren, falls die Daten in keiner anderen Inventurerfassungszeile vorhanden sind.|  
    |**Erfassung ohne Auftrag erlaubt**|Wählen Sie diese Option aus, um eine neue Inventurerfassungszeile zu generieren.|  

5.  Klicken Sie auf die Schaltfläche **OK**, um den Batchauftrag zu starten.  
6.  Wählen Sie die Aktion **Aufzeichnung** aus. Die Seite "Inventurerfassung" wird angezeigt. Wählen Sie die neu erstellte Inventurerfassung aus.  

    Sie können nun die Inventurliste basierend auf den Daten der aktuellen Inventurerfassung drucken.  

7.  So weisen Sie die **Inventurerfassungsaufzeichnung** zu.  
8.  Auf der Seite **Phys. Invt. Erfassung** legen Sie die entsprechenden Filter fest, und wählen Sie die Schaltfläche **Drucken** aus oder wählen Sie die Schaltfläche **Vorschau** aus.  

    Optional können Sie die Funktion Physische Stabelverarbeitungs-Inventur verwenden, um die Serien- oder Chargennummern zu erfassen.  

9. Auf der Seite **Physische Inventurerfassung** wählen Sie die Inventurerfassungszeile aus, wählen Sie **Funktionen** und dann **Zeile kopieren**.  
10. Auf der Seite **Physische Inventurerfassung kopieren** geben Sie die Anzahl der Kopien an, die von der ausgewählten Zeile erstellt werden sollen, und wählen Sie dann die Schaltfläche **OK** aus.  

Sie können die gedruckte physische Inventurerfassung verwenden, um die tatsächliche Menge des am angegebenen Lagerort verfügbaren Artikels zu aktualisieren. Zum Abschließen des Erfassungsprozesses muss das Kontrollkästchen **Erfasst** für alle Inventurerfassungszeilen aktiviert werden.  

Damit ersichtlich ist, dass die Inventurerfassung abgeschlossen wurde, muss der **Status** im Inventurerfassungskopf mithilfe der entsprechenden Funktion auf **Beendet** gesetzt werden. Weitere Informationen finden Sie unter [Führen Sie physische Inventuren aus](how-to-finish-a-physical-inventory-recording.md).  

## <a name="to-complete-a-physical-inventory-recording"></a>So schließen Sie eine Inventurerfassung ab  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventur durchführen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Inventurauftrag aus, den Sie fertig stellen möchten und klicken Sie auf **Bearbeiten**.  
3.  Geben Sie auf der Seite **Inventurerfassung** im Inforegister **Zeilen** im Feld **Menge** für jede Zeile die tatsächliche Artikelmenge ein.  
4.  Aktivieren Sie für jede Zeile das Kontrollkästchen **Erfasst**.  
5.  Füllen Sie im Inforegister **Allgemein** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Erfasst von**|Die Person, von der der Lagerbestand erfasst wurde.|  
    |**Erfassungsdatum**|Das Datum, an dem die Inventur erfasst wurde.|  
    |**Erfassungszeit**|Die Zeit, zu der die Inventur erfasst wurde.|  

 Sie können die Inventur jetzt beenden. Weitere Informationen finden Sie unter [Führen Sie physische Inventuren aus](how-to-finish-a-physical-inventory-recording.md).  

## <a name="see-also"></a>Siehe auch  
 [Inventurerfassung – Inventurzählung](physical-inventory-recording-counting-physical-inventory.md)   
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)   
 [Berechnen der verfügbaren Menge für einen Inventurauftrag](how-to-calculate-quantity-on-hand-for-a-physical-inventory-order.md)   
 [So schließen Sie eine Inventurerfassung ab](how-to-finish-a-physical-inventory-recording.md)
