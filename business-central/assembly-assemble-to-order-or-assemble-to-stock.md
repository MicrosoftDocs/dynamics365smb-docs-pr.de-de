---
title: Auftragsmontage und Lagermontage verstehen
description: Elemente für die Montage können geliefert werden, indem sie bei der Bestellung montiert werden oder indem sie im Bestand gehalten werden, bis sie auf einem Verkaufsauftrag benötigt werden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: cc5f10097d26859805d9e03691dd1bb02e204a1e
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381564"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Auftragsmontage und Lagermontage verstehen
Montageartikel können in den beiden folgenden Prozessen geliefert werden:  

-   Auftragsmontage  
-   Lagermontage  

## <a name="assemble-to-order"></a>Auftragsmontage  
In der Regel nutzen Sie die *Auftragsmontage* für Artikel, die Sie nicht auf Lager haben möchten, da Sie erwarten, dass diese für Debitorenanfragen angepasst werden müssen, oder weil Sie die Lagerkosten minimieren möchten. Die unterstützenden Funktionen umfassen:  

-   Möglichkeit, Montageartikel anzupassen, wenn ein Verkaufsauftrag entgegengenommen wird.  
-   Übersicht der Verfügbarkeit des Montageartikels und seiner Komponenten.  
-   Möglichkeit, Montagekomponenten sofort zu reservieren, um die Auftragserfüllung sicherzustellen.  
-   Funktion, um die Profitabilität des angepassten Auftrags durch Berechnen des Preises und der Kosten zu ermitteln.  
-   Fibuintegration für das Lager, um die Montage und das Versenden zu vereinfachen.  
-   Möglichkeit der Auftragsmontage im Augenblick der Erstellung eines Verkaufsangebots oder eines Rahmenauftrags.  
-   Möglichkeit, Lagermengen mit Auftragsmontagemengen zu kombinieren.  

Im Auftragsmontageprozess wird der Artikel als Reaktion auf einen Verkaufsauftrag und mit einer direkten Verknüpfung zwischen Montageauftrag und Verkaufsauftrag montiert.  

Wenn Sie einen Auftragsmontageartikel in eine Verkaufszeile eingeben, wird automatisch ein Montageauftrag mit einem Kopf erstellt, der auf der Verkaufszeile basiert und Zeilen enthält, die anhand der Montagestückliste des Artikels durch Multiplikation mit der Bestellmenge erhalten werden. Sie können auf der Seite **Auftragsmontagezeilen** verwenden, um die Zeilen des verknüpften Montageauftrags anzuzeigen und den Montageartikel und das Lieferdatum, das auf der Komponentenverfügbarkeit basiert, anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Obwohl es nicht Teil des Standardprozesses ist, können Sie Lagerbestandsmengen mit den Auftragsmontagemengen verkaufen. Weitere Informationen finden Sie unter [Verkaufen von Lagerartikeln in Programmfertigungs-Flow](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)  

 Um dieses Verfahren auszuführen, muss für das Feld **Montagerichtlinie** auf der Artikelkarte **Auftragsmontage** aktiviert sein.  

## <a name="assemble-to-stock"></a>Lagermontage  
 In der Regel nutzen Sie *Lagerfertigung* für Artikel, die Sie vor dem Verkauf montieren möchten - wie zur Vorbereitung einer Kit-Kampagne - und auf Lager zu halten, bis sie bestellt werden. Diese Artikel sind normalerweise Standardartikel, wie gepackte Kits, die Sie nicht an Debitorenanfragen anpassen.  

 Im Lagerfertigungsvorgang wird der Artikel ohne sofortigen Verkaufsbedarf montiert und ist im Lager als Lagerartikel für den späteren Verkauf oder Verbrauch als Unterbaugruppe verfügbar. Weitere Informationen finden Sie unter [Entnahme von Artikeln](assembly-how-to-assemble-items.md). Ab diesem Punkt kann der Artikel als einzelner Artikel kommissioniert und verarbeitet werden und wird wie ein gefertigter Artikel behandelt.  

 Wenn Sie einen Lagerfertigungsartikel in eine Verkaufszeile eingeben, sieht die Zeile wie jeder andere Zeile eines aus dem Lagerbestand verkauften Artikels aus. Beispielsweise wird die Verfügbarkeit nur für den Montageartikel geprüft.  

> [!NOTE]  
>  Obwohl es nicht Teil des Standardprozesses ist, können Sie einen Artikel für einen Auftrag montieren, auch wenn für diesen die Lagermontage eingerichtet ist. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln und Lagerartikeln zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

 Um dieses Verfahren auszuführen, muss für das Feld **Montagerichtlinie** auf der Artikelkarte **Lagermontage** aktiviert sein.  

## <a name="combination-scenarios"></a>Kombinierte Szenarien  
 Ein allgemeines Prinzip der Montageverwaltung ist, dass Auftragsmontagemengen, wenn sie in einer Verkaufsauftragszeile zusammengefasst sind, vor Lagermengen ausgeliefert werden müssen.  

 Wenn ein Montageauftrag mit einer Verkaufsauftragszeile verknüpft ist, wird der Wert im Feld **Menge für Auftragsmontage** der Verkaufsauftragszeile über das Feld **Montagemenge** im Montageauftragskopf in das Feld **Menge** kopiert. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

 Darüber hinaus wird der Wert im Feld **Menge für Montage** mit dem Feld **Zu liefern** in der Verkaufsauftragszeile verknüpft. Diese Verknüpfung verwaltet die Lieferung von Teil- und vollständigen Montageauftragsmengen. Dies ist erfüllt, wenn die gesamte Verkaufszeilenmenge für einen Auftrag montiert wird und, in kombinierten Szenarien, wenn ein Teil der Verkaufszeilenmenge montiert und ein anderer Teil aus dem Lager geliefert wird. In kombinierten Szenarien haben Sie jedoch bei der Teillieferung zusätzliche Flexibilität, indem Sie das Feld **Menge für Montage** innerhalb der vordefinierten Regeln ändern können, um anzugeben, wie viele Einheiten der Teillieferung aus dem Lagerbestand geliefert werden und wie viele durch Auftragsmontage geliefert werden sollen.  

 Wenn die vollständige Verkaufszeilenmenge nach Auftrag montiert und versendet werden muss, wird der Wert im Feld **Menge für Versand** in das Feld **Menge für Montage** im verknüpften Montageauftrag kopiert, wenn Sie die zu liefernde Menge ändern. Dadurch ist sichergestellt, dass die Menge, die ausgeliefert wird, vollständig von der Auftragsmontagemenge geliefert wird.  

 In den kombinierten Szenarien wird der Gesamtwert in **Menge für Versand** jedoch nicht in das Feld **Menge für Montage** im Montageauftragskopf kopiert. Stattdessen wird der Standardwert in das Feld **Menge für Montage** eingefügt, der entsprechend einer vordefinierten Regel, die sicherstellt, dass Auftragsmontagemengen zuerst geliefert werden, aus dem Feld **Zu liefern** berechnet wird.  

 Wenn Sie von diesem Standard abweichen möchten, weil Sie beispielsweise mehr oder weniger zusammenbauen möchten, als die Menge im Feld **Zu liefern** können Sie das Feld **Menge für Montage** ändern, allerdings nur innerhalb der vordefinierten Regeln, wie unten dargestellt.  

 Ein Beispiel dafür, warum Sie die zu montierende Menge ggf. ändern möchten, wäre, dass Sie Liefer- von Lagermengen teilweise buchen möchten, bevor der Montageausstoß geliefert werden kann.  

 In den folgenden Tabellen werden die Regeln erläutert, die die minimalen und maximalen Werte festlegen, die Sie manuell in das Feld **Menge für Montage** eingeben können, um in einem kombinierten Szenario vom Standardwert abzuweichen. Die Tabelle zeigt ein kombiniertes Szenario, in dem das Feld **Menge für Montage** der verknüpften Verkaufsauftragszeile von 7 in 4 geändert wird, weshalb **Menge für Montage** den Standardwert 4 annimmt.  

- Verkaufszeile

    |                | **Menge** | **Zu liefern** | **Menge für Auftragsmontage** | **Menge geliefert** |
    |----------------|--------------|------------------|-------------------------------|----------------------|
    |**Anfangswert**| 10          | 7                | 7                             | 0                    |
    |**Änderung**      |              | 4                |                               |                      |

- Montageauftragskopf

    |                | **Menge** | **Zu liefern** | **Menge für Auftragsmontage** | **Menge geliefert** |
    |----------------|--------------|------------------|-------------------------------|----------------------|
    |**Anfangswert**| 7           | 7                | 0                             | 7                    |
    |**Änderung**      |              | 4 (standardmäßig eingefügt)|                         |                      |

Basierend auf diesem Beispiel können Sie nur das Feld **Menge für Montage** wie folgt ändern:  

- Die Mindestmenge, die Sie eingeben können, ist 1. Die Mindestmenge, die Sie eingeben können, ist 1. Dies liegt daran, dass Sie mindestens eine Einheit zusammenbauen müssen, damit Sie die vier Einheiten verkaufen können, wenn davon ausgegangen wird, dass die verbleibenden drei im Lager verfügbar sind.  
- Die Höchstmenge, die Sie eingeben können, ist 4. Damit wird sichergestellt, dass Sie nicht mehr als diese Auftragsmontageartikel zusammenbauen, die im Verkauf benötigt werden.  

## <a name="see-also"></a>Siehe auch

[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]