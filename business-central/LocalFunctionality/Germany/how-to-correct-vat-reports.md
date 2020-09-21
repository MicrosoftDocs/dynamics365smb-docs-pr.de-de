---
title: Vorgehensweise beim Korrigieren von MwSt.-Berichten
description: Wenn Sie einen Korrektur-MwSt-Bericht übermitteln müssen oder einen übermittelten MwSt-Bericht löschen müssen, müssen Sie einen neuen MwSt-Bericht erstellen. Entsprechend der Gesetzgebung muss ein Korrekturbericht innerhalb eines Monats nach dem ursprünglichen Bericht übermittelt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a672780e1db93b07cfae55dc5d006a9f66751d3e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778616"
---
# <a name="correct-vat-reports"></a>Zu korrigierender MwSt.-Bericht
Wenn Sie einen Korrektur-MwSt-Bericht übermitteln müssen oder einen übermittelten MwSt-Bericht löschen müssen, müssen Sie einen neuen MwSt-Bericht erstellen. Entsprechend der Gesetzgebung muss ein Korrekturbericht innerhalb eines Monats nach dem ursprünglichen Bericht übermittelt werden.  

Wenn Sie einen Korrekturbericht erstellen, enthält die Erklärung zwei Zeilenarten pro korrigierter Zeile. In einer Zeilenart, „Stornierung“, wird der Basiswert der MwSt. als Stornierung aufgezeichnet. Alle anderen Informationen bleiben dieselben und können nicht bearbeitet werden. In einer neuen Zeile, Korrekturtyp, können Sie nach Bedarf Korrekturen am MwSt.-Betrag vornehmen. Bei der Aktion **Zeilen vorschlagen** wird jedoch der richtige Betrag, basierend auf den Filtern und gebuchten Belegen, vorgeschlagen. Sie können die **USt-IdNr.** nicht korrigieren oder ändern. Jede Periode, die korrigiert wird, benötigt ihren eigenen Korrekturbericht.  

Bei der Aktion **Zeilen vorschlagen**, werden die zu meldenden Werte neu berechnet. Die Aktion **Zeilen korrigieren** wird verwendet, um manuelle Änderungen vorzunehmen. Sie können die Auswirkungen der zwei Aktionen kombinieren, um den Bericht zu korrigieren.  

**Beispielkorrekturszenarien**  

1.  Wenn Sie zusätzliche MwSt-Posten buchen, nachdem Sie den Standardbericht im Berichtszeitraum übermitteln, wählen Sie **Zeilen vorschlagen** in der Gruppe **Verarbeiten** aus, um die aktualisierten Beträge zu erhalten.  

    > [!NOTE]  
    >  Wenn Sie den Betrag für einen Debitor oder Keditor manuell geändert haben, wird dieser Betrag überschrieben, wenn zusätzliche MwSt-Posten gebucht werden. Aktualisieren Sie den Betrag entsprechend.  

2.  Wenn Sie den Betrag einer Berichtszeile ändern möchten, die bereits übermittelt wurde und keine neuen MwSt-Posten gebucht werden, wählen Sie **Zeilen korrigieren** in der Gruppe Verarbeiten aus. Wählen Sie auf der Seite **MwST-Berichtszeilen** die zu korrigierenden Lieferzeilen aus, und klicken Sie auf **OK**.  

    Für jeden Posten werden zwei Zeilen angezeigt: Stornierung oder Korrektur. Sie können jetzt den Betrag der Korrekturzeile ändern.  

    > [!NOTE]  
    >  Die Aktion **Zeilen korrigieren** schlägt den Betrag nicht vor, der auf MwSt-Posten basiert. Wenn Sie neue MwSt-Posten für den Debitor oder Kreditor haben, verwenden Sie stattdessen **Zeilen vorschlagen**.  

3.  Wenn Sie die falschen Filter verwendet haben, wie beispielsweise die falsche MwSt-Produktbuchungsgruppe, wählen Sie **Zeilen vorschlagen** in der Gruppe Verarbeiten aus, und legen Sie dann die Filter nach Bedarf fest.  

    **Zeilen vorschlagen** erstellt Posten, um die Differenz zwischen den Filter zu widerzuspiegeln.  

    > [!NOTE]  
    >  Wenn die aktualisierten Filter einen Debitor oder einen Kreditor ausschließen, erstellt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] eine Stornierungszeile für den vorherigen berichteten Betrag und einen Korrekturposten mit Betrag 0.

## <a name="to-correct-a-vat-report"></a>So wird ein MwSt-Bericht korrigiert  

1.  Erstellen Sie einen neuen MwSt-Bericht. Weitere Informationen finden Sie unter [MwSt-Berichte erstellen](how-to-create-vat-reports.md).  
2.  Füllen Sie die Felder im Inforegister **Allgemein** aus, und legen Sie das Feld **MwSt-Berichtstyp** auf „Korrigiert“ fest.  
3.  In der **Originalberichtsnr.** Feld, wählen Sie den Bericht aus, die Sie korrigieren möchten. Sie können nur Berichte vom Typ „Standard“ auswählen, die als „Übermittelt“ markiert sind.  
4.  Erstellen Sie Ihre Korrektur-MwSt-Berichts-Zeilenposten.  

    Wählen Sie die Aktion **Mahnungszeile vorschlagen**. Legen Sie die Filter gemäß Bedarf fest.  

    In jeder Zeile können Sie einen Drilldown zu den Beträgen durchführen, um anzuzeigen, aus welchen MwSt-Posten sich der Betrag zusammensetzt. Ändern Sie den Betrag nach Bedarf. Sie können die **USt-IdNr.** jedoch nicht bearbeiten.  

5.  Wenn die **Vorschlagszeilen** Aktion keine Vorschläge bietet, die Beträge zu korrigieren, die erforderlich sind, verwenden Sie die Aktion**Zeilen korrigieren**, um Stornierungs- und Korrekturzeilen für den Debitor oder Kreditor einzufügen.  
6.  Fahren Sie mit dem MwSt-Berichterstellungsprozess fort und geben Sie den Bericht frei.  

## <a name="see-also"></a>Siehe auch  
 [Richten Sie die MwSt.-Berichte ein.](how-to-set-up-vat-reports.md)
