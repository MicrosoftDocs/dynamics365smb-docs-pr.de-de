---
title: Verkaufen von Auftragsmontageartikeln
description: 'Erfahren Sie, wie Sie ein Element verkaufen, das auf Bestellung montiert wird.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="sell-items-assembled-to-order" />Verkaufen von Auftragsmontageartikeln

Elemente, die für die Programmfertigung festgelegt sind, müssen nicht im Bestand sein und werden erst montiert, wenn sie in einem Verkaufsauftrag enthalten sind. Ein Artikel ist für die Programmfertigung festgelegt, wenn das Feld **Richtlinie zur Programmfertigung** auf der Artikelkarte **Montage auf Bestellung** enthält. Wenn Sie den Artikel in eine Kundenauftragszeile eingeben, wird automatisch ein Montageauftrag erstellt und mit dem Kundenauftrag verknüpft.  

> [!NOTE]  
> Wenn sich die zu montierenden Elemente bereits im Bestand befinden, können Sie diese Menge vom Montageauftrag abziehen und aus dem Bestand reservieren. Erfahren Sie mehr unter [Verkaufen Sie Lagerartikel in Programmfertigungen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Bei diesem Verfahren verarbeiten Sie den verkauf eines Artikels, der gemäß den Spezifikationen montiert wird, die vom Debitor gewünscht werden. Die Schritte umfassen: 

* Erzeugen einer Verkaufsauftragszeile.
* Anpassen des Montageelements durch Bearbeiten seiner Komponenten und Ressourcen.
* Prüfen der Verfügbarkeit, um ein Lieferdatum festzulegen.
* Freigeben des Verkaufsauftrags zur Montage und sofortigen Auslieferung.  

> [!NOTE]  
> Die folgende Vorgehensweise umfasst nicht die Schritte zum Erstellen eines Standard-Kundenauftrags, die vor dem Schritt erfolgen, in dem Sie die Montageposition in eine Verkaufsauftragszeile eingeben. Weitere Informationen zum Erstellen von Verkaufsaufträgen finden Sie unter [Produkte mit einem Kundenverkaufsauftrag erstellen](sales-how-sell-products.md).  

## <a name="to-sell-an-item-that-is-assembled-to-order" />So verkaufen Sie einen Auftragsmontageartikel:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen Auftrag. 
3. Geben Sie im Feld **Nr.** Geben Sie im Feld Nr. einen Artikel ein, der als Auftragsmontageartikel eingerichtet ist.  
4. Geben Sie im Feld **Lagerortcode** den Lagerort an, von dem aus der Artikel verkauft werden wird. Der Montageprozess wird an diesem Lagerort durchgeführt.  
5. Geben Sie im Feld **Menge** ein, wie viele Einheiten zu verkaufen sind.  

    > [!NOTE]  
    >  Wenn eine oder mehrere Komponenten der angeforderten Montage-Artikelmenge nicht verfügbar sind, wird eine Warnseite zur Verfügbarkeit geöffnet. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    Es wird ein Montageauftrag erstellt und mit der Verkaufsauftragszeile verknüpft. Das Fälligkeitsdatum des Montageauftrags ist das Versanddatum der Verkaufsauftragszeile.  

    Die zu verkaufende Menge wird in das Feld **Montagemenge für Auftrag** übernommen, was bedeutet, dass die Einrichtung davon ausgeht, dass Sie die gesamte Menge in der Verkaufszeile montieren werden. Sie können die zu montierende Menge verringern, wenn Sie zum Beispiel wissen, dass einige Artikel bereits verfügbar sind. Weitere Informationen finden Sie unter [Verkauf von Bestandsartikeln in Programmfertigungs-Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Wenn der Kunde ein zusätzliches Element in einem Bausatz wünscht, wählen Sie auf dem Inforegister **Zeilen** die Aktion **Zeile**, wählen Sie die Aktion **Zusammenstellen zur Bestellung** und dann die Aktion **Zeilen zur Programmfertigung**, um die Standard-Montagekomponenten anzuzeigen und zu ändern. Wählen Sie das Feld **Menge für Auftragsmontage** aus.  
7. Auf der Seite **Zusammenstellen zu Programmfertigung** erstellen Sie eine neue Zeile vom Typ **Element** für die zusätzliche Montagekomponente.  

    Sie können die Bestellung auch anpassen, indem Sie die Menge eines Standardelements des Kits erhöhen. Sie können dies tun, indem Sie den Wert im Feld **Komponentenmenge** auf der jeweiligen Montageauftragszeile erhöhen.  

    > [!NOTE]  
    >  Die Seite **Zeilen zur Programmfertigung** enthält nur die grundlegenden Felder zur Anpassung der Komponentenliste, zum Hinzufügen von Positionsnummern oder zur Lösung von Problemen mit der Verfügbarkeit von Komponenten. Um weitere Informationen zur Programmfertigung hinzuzufügen, wie z.B. das Startdatum der Montage, wählen Sie die Aktion **Dokumente anzeigen**. Dadurch wird eine vollständige Ansicht des Montageauftrags angezeigt, der mit der Verkaufsauftragszeile verknüpft ist. Sie können den Inhalt der meisten Felder in der Kopfzeile des Montageauftrags nicht ändern und Sie können die Montageausgabe nicht von dort aus buchen. Sie müssen die Geb. der Verkaufsauftragszeile buchen.  
    >
    >  Bei den verknüpften Montageaufträgen kann nur das Feld **Beginndatum** geändert werden. Durch das Ändern des Startdatums können die Arbeitskräfte in der Montage angeben, dass sie mit der Montage früher als zum Fälligkeitsdatum beginnen. Alle Felder auf den Zeilen des verknüpften Montageauftrags können geändert werden, so dass die Lagermitarbeiter während des Prozesses Verbrauchsdaten eingeben können.  

8. Prüfen Sie Komponentenverfügbarkeitsprobleme und reagieren Sie darauf. Wählen Sie zum Beispiel ein Ersatz-Element aus.  
9. Schließen Sie die Seite **Auftragsmontagezeilen**. Der verknüpfte Montageauftrag ist fertig, und die Arbeitskräfte können mit der Montage der angepassten Artikel beginnen.  
10. Wählen Sie im Verkaufsauftrag die Aktion **Freigeben**, um die Montageabteilung zu benachrichtigen, dass der Montagevorgang begonnen werden kann. Erfahren Sie mehr unter [Elemente montieren](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Bei der Ersetzung von Elementen wird ein Element nicht automatisch durch ein anderes ersetzt, z.B. wenn Sie einen Verkaufsauftrag oder eine Stückliste erstellen. Stattdessen werden Sie gewarnt, dass eine Ersetzung verfügbar ist.

## <a name="see-related-microsoft-trainingtrainingmodulesassemble-to-order-dynamics--business-central" />Siehe zugehörige [Microsoft Schulungen](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
