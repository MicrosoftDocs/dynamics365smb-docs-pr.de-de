---
title: Auftragsmontage und Lagermontage verstehen
description: 'Erfahren Sie, wie Sie Artikel für Verkaufsaufträge zusammenstellen oder für zukünftige Verkäufe auf Lager halten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Auftragsmontage und Lagermontage verstehen

Mit [!INCLUDE [prod_short](includes/prod_short.md)] können Sie Montageartikel auf folgende Weisen ausgeben:

* Montage auf Bestellung  
* Auf Lager montieren  

## <a name="assemble-to-order"></a>Montage auf Bestellung

Verwenden Sie den Auftragsmontageprozess für Artikel, die Sie nicht auf Lager haben möchten. Zum Beispiel aus folgenden Gründen:

* Sie passen die Artikel an die Kundenanforderungen an.
* Sie möchten die Kosten für den Lagerbestand minimieren.

Die folgende Liste beschreibt einige der Vorteile des Auftragsmontageprozesses:  

* Montageartikel anpassen, wenn ein Verkaufsauftrag entgegengenommen wird.  
* Übersicht der Verfügbarkeit des Montageartikels und seiner Komponenten.  
* Montagekomponenten sofort reservieren, um die Auftragserfüllung sicherzustellen.  
* Die Profitabilität des angepassten Auftrags durch Berechnen des Preises und der Kosten ermitteln.  
* Fibuintegration für das Lager, um die Montage und das Versenden zu vereinfachen.  
* Auftragsmontage, wenn Sie ein Verkaufsangebot oder einen Rahmenauftrag erstellen.  
* Lagermengen mit Auftragsmontagemengen kombinieren.  

Bei der Auftragsmontage stellen Sie Artikel für einen Kundenauftrag zusammen. Es besteht eine Eins-zu-Eins-Verknüpfung zwischen dem Montageauftrag und dem Verkaufsauftrag.  

Wenn Sie eine Auftragsmontageartikel in eine Kundenauftragszeile eingeben, wird automatisch ein Montageauftrag erstellt. Der Montageauftrag basiert auf der Verkaufszeile, und seine Zeilen basieren auf der Montagestückliste des Artikels. Die Menge der Komponenten in der Montagestückliste wird mit der Bestellmenge multipliziert. Die Seite **Auftragsmontagezeilen** zeigt Details zu den verknüpften Montageauftragszeilen. Die Details können Ihnen dabei helfen, den Montageartikel anzupassen. Das Lieferdatum basiert auf der Verfügbarkeit von Komponenten. Weitere Informationen zur Montage von Artikeln für Verkaufsaufträge finden Sie unter [Verkauf von Elementen, die auf Bestellung gefertigt wurden](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Obwohl es nicht Teil des Standardprozesses ist, können Sie Lagerbestandsmengen und Auftragsmontagemengen mit dem selben Verkaufsauftrag verkaufen. Mehr Informationen zum Kombinieren von Lager- und Auftragsmontageartikeln finden Sie unter [Verkauf von Lagerartikeln in Auftragsmontageflüssen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Um anzugeben, dass ein Artikel im Auftrag montiert wird, wählen Sie im Feld **Montagerichtlinie** auf der Seite **Artikelkarte** für den Artikel **Auftragsmontage** aus.  

## <a name="assemble-to-stock"></a>Auf Lager montieren

Verwenden Sie den Lagermontageprozess für Artikel, die Sie montieren und für zukünftige Verkäufe lagern. Lagermontageartikel sind Standardartikel, wie z. B. verpackte Bausätze, die Sie nicht anpassen. Sie können diese Artikel auch als Unterbaugruppenkomponenten verwenden. Die Artikel werden als einzelne Artikel kommissioniert und verarbeitet und wie ein fertiger Fertigungsartikel behandelt. Weitere Informationen zu Montageartikeln finden Sie unter [Montageartikel](assembly-how-to-assemble-items.md).  

Wenn Sie einen Lagermontageartikel in eine Verkaufszeile angeben, wird der Artikel wie jeder andere aus dem Lagerbestand verkaufter Artikels behandelt. Zum Beispiel prüft [!INCLUDE [prod_short](includes/prod_short.md)] nur die Verfügbarkeit des montierten Artikels und nicht seiner Komponenten.  

> [!NOTE]  
> Obwohl es nicht Teil des Standardprozesses ist, können Sie einen Artikel für einen Auftrag montieren, auch wenn für den Artikel die Lagermontage eingerichtet ist. Weitere Informationen finden Sie unter [So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Um anzugeben, dass ein Artikel für das Lager montiert wird, wählen Sie im Feld **Montagerichtlinie** auf der Seite **Artikelkarte** für den Artikel **Lagermontage** aus.  

## <a name="combination-scenarios"></a>Kombinierte Szenarien

Wenn die Auftragsmontage und Lagermengen auf einem Verkaufsauftrag kombiniert werden, müssen Auftragsmontagemengen zuerst ausgegeben werden.  

Wenn ein Montageauftrag mit einer Verkaufsauftragszeile verknüpft ist, wird der Wert im Feld **Menge für Auftragsmontage** der Verkaufsauftragszeile über das Feld **Montagemenge** im Montageauftrag in das Feld **Menge** kopiert. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

Der Wert im Feld **Menge für Montage** bezieht sich auf das Feld **Zu liefern** auf der Verkaufsauftragszeile. Diese Beziehung verwaltet, wie Sie Teil- und Komplettmengen für die Auftragsmontage versenden:

* Wenn die Komplettmenge auf der Verkaufsauftragszeile nach Auftrag montiert wird
* In kombinierten Szenarien, in denen ein Teil der Menge nach Auftrag montiert wird und ein Teil aus dem Lagerbestand geliefert wird.

Das Kombinationsszenario ermöglicht Flexibilität bei Teillieferungen. Sie können das Feld **Zu montierende Menge** verwenden, um die Menge anzugeben, die teilweise aus dem Bestand und durch Montage auf Bestellung versendet werden soll.  

Wenn die vollständige Verkaufszeilenmenge nach Auftrag montiert und versendet werden muss, wird der Wert im Feld **Menge für Versand** in das Feld **Menge für Montage** im verknüpften Montageauftrag kopiert, wenn Sie die zu liefernde Menge ändern. Dieses Update stellt sicher, dass die Menge, die ausgeliefert wird, vollständig von der Auftragsmontagemenge geliefert wird.  

In den kombinierten Szenarien wird der Gesamtwert in **Menge für Versand** jedoch nicht in das Feld **Menge für Montage** im Montageauftrag kopiert. Stattdessen wird ein Standardwert in das Feld **Menge für Montage** eingefügt. Der Wert errechnet sich aus dem Feld **Zu liefern**, um sicherzustellen, dass die Auftragsmontagemengen zuerst versendet werden.

Um von dem Standard abzuweichen, weil Sie beispielsweise mehr oder weniger zusammenbauen möchten, als die Menge im Feld **Zu liefern** können Sie das Feld **Menge für Montage** innerhalb der vordefinierten Regeln, wie unten dargestellt, ändern.  

Ein Beispiel dafür, warum Sie die zu montierende Menge ggf. ändern möchten, wäre, dass Sie die Lieferung von Lagermengen teilweise buchen möchten, bevor Sie den Montageausgang liefern.  

In den folgenden Tabellen werden die Regeln erläutert, die die minimalen und maximalen Werte festlegen, die Sie manuell in das Feld **Menge für Montage** eingeben können, um in einem kombinierten Szenario vom Standardwert abzuweichen. Die Tabelle zeigt ein kombiniertes Szenario, in dem das Feld **Menge für Montage** der verknüpften Verkaufsauftragszeile von 7 in 4 geändert wird, weshalb **Menge für Montage** den Standardwert 4 annimmt.  

**Verkaufszeile**

|                | **Menge** | **Zu liefern** | **Menge für Auftragsmontage** | **Menge geliefert** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Anfangswert**| 10          | 7                | 7                             | 0                    |
|**Änderung**      |              | 4                |                               |                      |

**Montageauftragskopf**

|                | **Menge** | **Zu liefern** | **Menge für Auftragsmontage** | **Menge geliefert** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Anfangswert**| 7           | 7                | 0                             | 7                    |
|**Änderung**      |              | 4 (standardmäßig eingefügt)|                         |                      |

Basierend auf diesem Beispiel können Sie das Feld **Menge für Montage** wie folgt ändern:  

* Die Mindestmenge, die Sie eingeben können, ist 1. Sie müssen mindestens eine Einheit montieren, damit Sie die vier Einheiten verkaufen können, wenn davon ausgegangen wird, dass die verbleibenden drei im Lager verfügbar sind.  
* Die Höchstmenge, die Sie eingeben können, ist 4. Dieses Limit stellt sicher, dass Sie nicht mehr von dem Artikel montieren, als Sie für den Verkauf benötigen.  

## <a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Mit Montagestücklisten arbeiten](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
