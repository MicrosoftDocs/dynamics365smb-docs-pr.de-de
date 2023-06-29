---
title: So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen
description: Auftragsmontageartikel werden für Verkaufsaufträge über einen Montageauftrag montiert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="selling-inventory-items-in-assemble-to-order-flows"></a><a name="selling-inventory-items-in-assemble-to-order-flows"></a>Verkauf von Lagerartikeln in Programmfertigungen (Flows)

Wenn das Feld **Montagerichtlinie** auf der Artikelkarte eines Montageartikels **Auftragsmontage** enthält, dann nimmt der Verkaufsauftragsprozess an, dass der Artikel nicht auf Lager ist und für Verkaufsaufträge montiert werden muss. Wenn Sie den Artikel in eine Zeile oder einen Verkaufsauftrag hinzufügen, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] einen Montageauftrag, der mit dem Kundenauftrag verknüpft ist. Weitere Informationen dazu, wie Auftragsmontageartikel verkauft werden, finden Sie unter [Verkauf von Elementen, die auf Bestellung gefertigt wurden](assembly-how-to-sell-items-assembled-to-order.md). Wenn jedoch ein Teil der Verkaufsauftragsmenge bereits im Lagerbestand verfügbar ist, können Sie die Menge des Montageauftrags verringern, indem Sie das Feld **Menge für Auftragsmontage** auf der Verkaufsauftragszeile ändern.  

Es kommt relativ selten vor, dass Unternehmen Bestandsartikel als auf Auftragsmontageartikel verkaufen. Auftragsmontageartikel sind in der Regel kein Standard. Sie werden an die spezifischen Kundenanforderungen angepasst. Aufgrund von Rücksendungen oder Auftragsstornierungen haben Sie jedoch möglicherweise Mengen an auftragsgefertigten Artikeln im Bestand. Diese Mengen sollten kommissioniert und verkauft werden, bevor neue montiert werden.  

> [!NOTE]  
> Um zu prüfen, ob für Montageaufträge bereits auftragsmontierte Artikel verfügbar sind, verwenden Sie die Infobox **Verkaufszeilendetails** im Verkaufsauftrag.  

Sie können ähnliche Dinge tun, wenn Sie Montageartikel aus dem Lager verkaufen und ein Teil oder die gesamte Menge nicht verfügbar ist. Sie können die fehlende Menge über einen Montageauftrag liefern. Weitere Informationen über den Verkauf von Bestands- und Montageartikeln finden Sie unter [Auftragsmontageartikel Bestandartikel zusammen verkaufen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
> Es gibt Regeln, die für das Feld **Zu liefern** auf Verkaufsauftragszeilen gelgten, die eine Kombination von Auftragsmontagemengen und von Lagermengen enthalten. Weitere Informationen zu den Regeln finden Sie unter [Kombinationsszenarien](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Bei diesem Verfahren ersetzen Sie Auftragsmontagemengen durch Lagerbestandsmengen auf einer Verkaufsauftragszeile. Die folgenden Schritte geben einen Überblick:

1. Stellen Sie die Verfügbarkeit fest.
2. Reduzieren dieser Menge aus dem verknüpften Montageauftrag.
3. Reservieren Sie die Bestandsmenge, um sicherzustellen, dass sie für die Bestellung kommissioniert und versendet wird.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a><a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen Auftrag. Weitere Informationen zum Erstellen von Verkaufsaufträgen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md).  
3. Geben Sie auf einer Verkaufsauftragszeile, die einen Auftragsmontageartikel einthält, im Feld **Menge** die Menge ein.  
4. Sehen Sie in der Infobox **VK-Zeilendetails** nach, ob die gesamte oder ein Teil der Menge verfügbar ist.  
5. Ziehen Sie im Feld **Menge für Auftragsmontage** die verfügbare Menge ab, so dass nur die nichtverfügbare Menge gemäß dem Auftrag montiert wird. Das Feld **Reservierte Menge** " wird entsprechend verringert, um zu berücksichtigen, dass der Auftrag-zu-Auftrag-Link oder die Reservierung sich nur auf die zu montierende Menge bezieht.  
6. Klicken Sie auf dem Inforegister **Zeilen** auf **Funktionen** und wählen Sie dann die Aktion **Reservieren**.  
7. Wählen Sie auf der Seite **Reservierung** den Artikelposten, der die verfügbaren Mengen enthält, wählen Sie die Option **Von aktueller Zeile reservieren**, und klicken Sie dann auf die Schaltfläche **OK**.  

    Auf der Seite **Verkaufsauftrag** zeigt das Feld **Reservierte Menge** jetzt an, dass die gesamte Menge für die Auftragszeile reserviert ist. Das Feld **Menge für Auftragsmontage** spiegelt noch die zu montierende Menge wider.  

8. Geben Sie den Verkaufsauftrags frei, um die Artikel für die Kommissionierung und die Montage der nicht verfügbaren Artikel verfügbar zu machen. Weitere Informationen zum Montieren von Artikeln finden Sie unter [Montageartikel](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Das Feld **Lagerplatzcode** auf dem Verkaufsauftrag enthält möglicherweise den Wert aus den Feldern **P-Code f. Prog.fert.lief.** oder **Von Montagelagerplatzcode** auf der Lagerortkarte ausgefüllt sein. Wenn dem so ist, ist das Feld **Lagerplatzcode** auf der Verkaufsauftragszeile in dieser Kombination aus Auftragsmontage- und Lagermontageartikelmengen möglicherweise falsch. Es empfiehlt sich, den Lagerplatz im Feld **Lagerplatzcode** zu prüfen und sicherzustellen, dass die Platzierung für alle Mengen funktioniert. Alternativ können Sie die beiden verschiedenen Mengen auf separaten Verkaufsauftragszeilen eingeben.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
