---
title: Designdetails - Lagerhaus Übersicht | Microsoft Docs
description: Um die physische Bewegung der Artikel auf dieser Zonen- und Lagerplatzebene zu unterstützen, müssen alle Informationen für jede Transaktion oder Umlagerung im Lager nachverfolgt werden. Dies wird in der Tabelle **Lagerplatzposten** verwaltet. Jede Transaktion wird in einem Lagerplatzjournal gespeichert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: f1ecd1324df2433d31ff1480316a9e281ad5c5df
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215678"
---
# <a name="design-details-warehouse-overview"></a>Designdetails: Lagerübersicht
Um die physische Bewegung der Artikel auf dieser Zonen- und Lagerplatzebene zu unterstützen, müssen alle Informationen für jede Transaktion oder Umlagerung im Lager nachverfolgt werden. Dies wird in der Tabelle **Lagerplatzposten** verwaltet. Jede Transaktion wird in einem Lagerplatzjournal gespeichert.  

Logistikbelege und ein Logistik Buch.-Blatt werden verwendet, um Artikelumlagerungen im Lager zu erfassen. Immer wenn ein Artikel im Lager umgelagert, erhalten, eingelagert, kommissioniert, geliefert oder angepasst wird, werden Lagerposten registriert, um die physischen Informationen zu Zone, Lagerplatz und Menge zu speichern.

Die Tabelle **Lagerplatzinhalt** wird verwendet, um alle verschiedenen Dimensionen des Inhalts eines Lagerplatzes pro Artikel zu bearbeiten, wie etwa Mengeneinheit, Höchstmenge oder Mindestmenge. Die Tabelle **Lagerplatzinhalt** enthält auch Flussfelder zu den Lagerplatzposten, Lageranweisungen und Logistik-Buch.-Blattzeilen, wodurch sichergestellt wird, dass die Verfügbarkeit eines Artikels pro Lagerplatz und eines Lagerplatzes für einen Artikel schnell berechnet werden kann. Weitere Informationen finden Sie unter [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md).  

Wenn Artikelbuchungen außerhalb des Lagermoduls auftreten, wird ein Standard-Ausgleichslagerplatz pro Lagerort verwendet, um Lagerplatzposten mit Inventurposten zu synchronisieren. Während der Inventur des Lagers werden jegliche Abweichungen zwischen berechneten und gezählten Mengen am Regulierungslagerplatz erfasst und dann als korrigierende Artikelposten gebucht. Weitere Informationen finden Sie unter [Designdetails: Bestandintegration](design-details-integration-with-inventory.md).  

Die folgenden Abbildung zeigt typische Warenflüsse.  

![Überblick über Lagerprozesse](media/design_details_warehouse_management_overview.png "Überblick über Lagerprozesse")  

## <a name="basic-or-advanced-warehousing"></a>Grundlegende oder erweiterte Lagerhaltung  
Lagerfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)] können in unterschiedlichen Komplexitätsebenen implementiert werden, abhängig von den Prozessen eines Unternehmens und dem Auftragsvolumen. Der wichtigste Unterschied besteht darin, dass Aktivitäten in der einfachen Logistik Auftrag für Auftrag durchgeführt werden, während sie in der erweiterten Logistik für mehrere Aufträge konsolidiert werden.  

 Um zwischen den verschiedenen Komplexitätsebenen zu unterscheiden, verwendet diese Dokumentation zwei allgemeine Bezeichnungen, grundlegende und erweiterte Lagerhaltung. Diese einfache Unterscheidung umfasst mehrere verschiedene Komplexitätsebenen, die durch definierte Produktdetails und Lagerorteinrichtung definiert sind, wobei jede durch unterschiedliche UI-Dokumente unterstützt werden. Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).  

> [!NOTE]  
>  Die höchstentwickelte Ebene der Logistik wird in dieser Dokumentation als „WMS-Installationen“ bezeichnet, da diese Methode die höchstentwickelten Elemente und Logistiksysteme erfordert.  

 Die folgenden verschiedenen UI-Dokumente werden in der einfachen und der erweiterten Logistik verwendet.  

## <a name="basic-ui-documents"></a>Grundlegende UI-Dokumente  

-   **Lagereinlagerung**  
-   **Lagerkommissionierung**  
-   **Lagerbestandsumlagerung**  
-   **Artikel Buch.-Blatt**  
-   **Artikel Umlag. Buch.-Blatt**  
-   (Verschiedene Berichte)  

## <a name="advanced-ui-documents"></a>Erweiterte UI-Dokumente  

-   **Wareneingang**  
-   **Einlagerungsarbeitsblatt**  
-   **Einlagerung**  
-   **Kommissionierarbeitsblatt**  
-   **Kommissionierung**  
-   **Lagerplatzumlagerungsarbeitsblatt**  
-   **Lagerplatzumlagerung**  
-   **Interne Kommissionierung**  
-   **Interne Einlag.-Anforderung**  
-   **Lagerplatz Erst.-Arbeitsblatt**  
-   **Lagerplatzinh. Erst.-Arbeitsblatt**  
-   **Logistik Artikel Buch.-Blatt**  
-   **Umlagerung Logistik Artikel Buch.-Blatt**  
-   (Verschiedene Berichte)  

Weitere Informationen über jeden Beleg finden Sie den entsprechenden Fensterthemen.  

### <a name="terminology"></a>Terminologie  
Um mit den Finanzbegriffen Einkauf und von Verkauf zu entsprechen, verwendet [!INCLUDE[prod_short](includes/prod_short.md)] Lagerdokumentation die folgenden Begriffe für Warenfluss im Lager.  

|Begriff|Description|  
|----------|---------------------------------------|  
|Eingehender Fluss|Artikel, die in den Lagerort eingehen, z.B. Einkäufe und eingehende Umlagerungen.|  
|Interne Flüsse|Artikel, die innerhalb des Lagerorts verschoben werden, wie z.B. Produktionskomponenten und fertiggestellte Artikel.|  
|Ausgehender Warenfluss|Artikel, die aus dem Lagerort ausgehen, z.B. Verkäufe und ausgehende Umlagerungen.|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Logistik](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]