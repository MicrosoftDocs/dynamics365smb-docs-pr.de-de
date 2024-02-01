---
title: 'MwSt.-Berichte korrigieren [DE]'
description: 'Wenn Sie einen Korrektur-MwSt-Bericht übermitteln müssen oder einen übermittelten MwSt-Bericht löschen müssen, müssen Sie einen neuen MwSt-Bericht erstellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 26101
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="correct-vat-reports-in-the-german-version"></a>MwSt.-Berichte korrigieren in der deutschen Version

Wenn Sie einen Korrektur-MwSt-Bericht übermitteln müssen oder einen übermittelten MwSt-Bericht löschen müssen, müssen Sie einen neuen MwSt-Bericht erstellen. Entsprechend der Gesetzgebung muss ein Korrekturbericht innerhalb eines Monats nach dem ursprünglichen Bericht übermittelt werden.  

Wenn Sie einen Korrekturbericht erstellen, enthält die Erklärung zwei Zeilenarten pro korrigierter Zeile. In einer Zeilenart, „Stornierung“, wird der Basiswert der MwSt. als Stornierung aufgezeichnet. Alle anderen Informationen bleiben dieselben und können nicht bearbeitet werden. In einer neuen Zeile, Korrekturtyp, können Sie nach Bedarf Korrekturen am MwSt.-Betrag vornehmen. Bei der Aktion **Zeilen vorschlagen** wird jedoch der richtige Betrag, basierend auf den Filtern und gebuchten Belegen, vorgeschlagen. Sie können die **USt-IdNr.** nicht korrigieren oder ändern. Jede Periode, die korrigiert wird, benötigt ihren eigenen Korrekturbericht.  

Bei der Aktion **Zeilen vorschlagen**, werden die zu meldenden Werte neu berechnet. Die Aktion **Zeilen korrigieren** wird verwendet, um manuelle Änderungen vorzunehmen. Sie können die Auswirkungen der zwei Aktionen kombinieren, um den Bericht zu korrigieren.  

## <a name="example-corrections-scenarios"></a>Beispielszenarien für Korrekturen

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
    >  Wenn die aktualisierten Filter einen Debitor oder einen Kreditor ausschließen, erstellt [!INCLUDE[prod_short](../../includes/prod_short.md)] eine Stornierungszeile für den vorherigen berichteten Betrag und einen Korrekturposten mit Betrag 0.

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
 [Richten Sie die MwSt.-Berichte ein](how-to-set-up-vat-reports.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
