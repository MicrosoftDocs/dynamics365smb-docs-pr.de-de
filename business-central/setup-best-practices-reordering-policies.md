---
title: "Bewährte Einrichtungsmethoden: Wiederbeschaffungsverfahren | Microsoft Docs"
description: Das Feld **Nachbestellungs-Richtlinie** auf Artikelkarten umfasst vier verschiedene Planungsmethoden, die bestimmen, wie die einzelnen Planungsparameter interagieren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cb0658a768276835fba44ab1e88e6fac05df5397
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-reordering-policies"></a>Bewährte Einrichtungsmethoden: Wiederbeschaffungsverfahren
Das Feld **Nachbestellungs-Richtlinie** auf Artikelkarten umfasst vier verschiedene Planungsmethoden, die bestimmen, wie die einzelnen Planungsparameter interagieren.  

Eine optimale Grundlage für die Auswahl eines Wiederbeschaffungsverfahrens ist die ABC-Klassifizierung des Artikels. Wenn Sie eine ABC-Klassifizierung für die Bestandskontrolle und die Beschaffungsplanung nutzen, werden Artikel abhängig von ihrem Wert und Volumen im Verhältnis zum Gesamtbestand in drei unterschiedlichen Klassen verwaltet. Die Wert-Volumen-Verteilung der drei Klassen wird in der folgenden Tabelle dargestellt.

|Klasse|Prozent des Gesamtbestandsvolumens|Prozent des Gesamtbestandswerts|
|-----|-----------------------------|----------------------------|
|A|10 - 20|50 - 70|
|B|20|20|
|L|60 - 70|10 - 30|

Die ABC-Klassifizierungs besagt, dass Aufwand und Geld gespart werden können, indem Artikeln mit geringem Wert weniger kontrolliert werden, als Artikeln mit hohem Wert. Die folgenden Abbildung zeigt, welches Wiederbeschaffungsverfahren in [!INCLUDE[d365fin](includes/d365fin_md.md)] für A-, B- und C-Artikel am besten geeignet ist.

![ABC-Klassifizierung](media/abc_classification.png "abc_classification")

Die folgende Tabelle enthält bewährte Methoden für die Auswahl zwischen den vier Richtlinien.  

|Einrichtungsoptionen|Bewährte Vorgehensweisen|Bemerkung|  
|------------------|-------------------|-------------|  
|**Auftrag**|Verwendung für A-Artikel.<br /><br /> Verwendung für Auftragsfertigungsartikel.<br /><br /> In der Produktion, Verwendung für Artikel auf oberster Ebene und für teure Komponenten und Unterbaugruppen.<br /><br /> Verwendung für Artikel, die als Direktlieferungen und Spezialaufträge bezogen werden.<br /><br /> Nicht verwenden, wenn Sie keine automatische Reservierung akzeptieren.|Artikel wie Ledercouchs in einem Möbelgeschäft sind hochwertige Artikel mit niedriger und unregelmäßiger Auftragsgeschwindigkeit, bei denen eine Lagerhaltung inakzeptabel ist oder die erforderlichen Attribute variieren. Das beste Wiederbeschaffungsverfahren ist deshalb eines, bei dem speziell für jeden Bedarf geplant wird.|  
|**Los-für-Los**|Verwendung für B-Artikel.<br /><br /> In der Produktion, Verwendung für Komponenten, die in mehreren Stücklisten auftreten. Dadurch ist sichergestellt, dass Einkaufsbestellungen für den gleichen Debitor zusammengefasst werden, damit bessere Preise ausgehandelt werden können.<br /><br /> Verwendung, wenn Sie bei der Auswahl des Wiederbeschaffungsverfahren nicht sicher sind.|B-Artikel, z. B. Restaurantstühle, haben eine regelmäßige und relative hohe Auftragsgeschwindigkeit, aber auch hohe Frachtkosten. Das beste Wiederbeschaffungsverfahren für B-Artikel ist deshalb eines, das wirtschaftlich ist, indem der Bedarf im Bestellzyklus gebündelt wird.<br /><br /> Bei 80 % der Artikel kann diese Methode verwendet werden.<br /><br /> Kann ohne Planungsparameter erfolgreich verwendet werden.|  
|**Feste Bestellmenge**|Verwendung für C-Artikel.<br /><br /> Zusammenfassen mit Minimalbestandparametern.<br /><br /> In der Produktion, Verwendung für Komponenten auf der niedrigsten Ebene.<br /><br /> Nicht verwenden, wenn der Artikel häufig reserviert wird.|C-Artikel wie Teetassen sind geringwertige Artikel mit hoher und regelmäßiger Auftragsgeschwindigkeit. Das beste Wiederbeschaffungsverfahren für C-Artikel ist deshalb eines, das konstante Verfügbarkeit sicherstellt, indem der Bestand immer über dem Minimalbestand liegt.<br /><br /> Wenn der Benutzer eine Menge für beliebigen, in der Zukunft liegenden Bedarf reserviert, wird die Planungsgrundlage gestört. Selbst wenn der voraussichtliche Lagerbestand im Hinblick auf den Minimalbestand akzeptabel ist, stehen die Mengen möglicherweise aufgrund der Reservierung nicht zur Verfügung.|  
|**Auffüllen auf Maximalbestand**|Verwendung für C-Artikel mit hohen Frachtkosten oder Einschränkungen bei der Lagerhaltung.<br /><br /> Zusammenfassen mit einen oder mehreren Auftragsmodifikationen (minimale/maximale Losgröße oder Losgrößenrundungsfaktor).|C-Artikel wie Teetassen sind geringwertige Artikel mit hoher und regelmäßiger Auftragsgeschwindigkeit. Das beste Wiederbeschaffungsverfahren für C-Artikel ist deshalb eines, das konstante Verfügbarkeit sicherstellt, indem der Bestand immer über dem Minimalbestand, aber unter dem maximalen Lagerbestand liegt.<br /><br /> Um den vorgeschlagenen Auftrag zu ändern, sollten Sie die Bestellmenge auf eine festgelegte maximale Losgröße reduzieren, auf eine minimale Losgröße erhöhen oder aufrunden, werden um einem festgelegten Losgrößenrundungsfaktor zu entsprechen. **Hinweis:**  Bei Verwendung mit einem Minimalbestand bleibt der Lagerbestand zwischen dem Minimalbestand und dem Maximalbestand.|  

## <a name="see-also"></a>Siehe auch  
 [Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)   
 [Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
 [Designdetails: Auftrag](design-details-order.md)   
 [Designdetails: Charge für Charge](design-details-lot-for-lot.md)   
 [Designdetails: Feste Nachbestellmenge](design-details-fixed-reorder-qty.md)   
 [Designdetails: Höchstmenge](design-details-maximum-qty.md)   
 [Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

