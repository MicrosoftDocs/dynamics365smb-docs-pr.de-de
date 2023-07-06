---
title: So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen
description: 'Wenn ein Teil eines auf Lager zu montierenden Artikels nicht verfügbar ist, können Sie einen Montageauftrag für die verbleibende Menge erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="sell-assemble-to-order-items-and-inventory-items-together"></a><a name="sell-assemble-to-order-items-and-inventory-items-together"></a><a name="sell-assemble-to-order-items-and-inventory-items-together"></a>So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen

Wenn das Feld **Montagerichtlinie** auf der Artikelkarte eines Montageartikels **Lagermontage** enthält, dann nimmt der Verkaufsauftragsprozess an, dass der Artikel bereits montiert wird und aus dem Lager entnommen werden kann, wenn er verfügbar ist. Daher wird kein Montageauftrag automatisch erstellt und mit der Verkaufsauftragszeile verknüpft. Wenn allerdings ein Teil oder die gesamte Menge nicht verfügbar ist, können Sie einen Montageauftrag für die verbleibende Menge erstellen. Füllen Sie dazu im Feld **Menge für Montageauftrag** auf dem Verkausauftrag die aus. Mit dieser Einstellung können Sie die Auftragsmontage des Artikels durchführen, obwohl er für die Lagermontage eingerichtet ist.  

Sie haben eine ähnliche Flexibilität, wenn Sie Artikel auf Bestellung verkaufen und ein Teil der Menge bereits auf Lager ist. Sie sollten diese Menge vom Montageauftrag abziehen. Weitere Informationen zum Verkauf von Bestandsartikeln finden Sie unter [So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

> [!NOTE]  
> Es gibt Regeln, die für das Feld **Zu liefern** auf Verkaufsauftragszeilen gelgten, die eine Kombination von Auftragsmontagemengen und von Lagermengen enthalten. Weitere Informationen zu den Regeln finden Sie unter [Kombinationsszenarien](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

> [!NOTE]  
> Die folgende Vorgehensweise enthält nicht die Verkaufszeilenschritte, die Sie durchführen müssen, bevor Sie einen Montageauftrag für nicht verfügbare Mengen erstellen können.

## <a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a><a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a><a name="to-sell-assemble-to-order-items-and-inventory-items-together"></a>So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen

1. Geben Sie auf einer Verkaufsauftragszeile für einen Lagermontageartikel im Feld **Menge** eine Menge ein, die den Lagerbestand überschreitet. Die Seite **Verfügbarkeit prüfen** wird angezeigt. Um mehr über die Verfügbarkeit von Artikeln zu erfahren, gehen Sie zu [Verfügbarkeit von Artikeln anzeigen](inventory-how-availability-overview.md).
2. Geben Sie im Feld **Menge für Auftragsmontage** den Wert aus dem Feld **Gesamtmenge** ein.  
3. Nehmen Sie alle Änderungen an den Montagekomponenten vor. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  
4. Geben Sie den Verkaufsauftrags frei, um die Artikel für die Kommissionierung und die Montage der nicht verfügbaren Artikel verfügbar zu machen. Weitere Informationen zu den Standard-Montageschritten finden Sie unter [Artikel montieren](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
> Das Feld **Lagerplatzcode** auf dem Verkaufsauftrag enthält möglicherweise den Wert aus den Feldern **P-Code f. Prog.fert.lief.** oder **Von Montagelagerplatzcode** auf der Lagerortkarte ausgefüllt sein. Wenn dem so ist, ist das Feld **Lagerplatzcode** auf der Verkaufsauftragszeile in dieser Kombination aus Auftragsmontage- und Lagermontageartikelmengen möglicherweise falsch. Es empfiehlt sich, den Lagerplatz im Feld **Lagerplatzcode** zu prüfen und sicherzustellen, dass die Platzierung für alle Mengen funktioniert. Alternativ können Sie die beiden verschiedenen Mengen auf separaten Verkaufsauftragszeilen eingeben.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
