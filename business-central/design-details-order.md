---
title: Designdetails - Auftrag | Microsoft Docs
description: Dieses Thema enthält Informationen über Auftrag-zu-Auftrag-Links in einer Auftragsfertigungsumgebung.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: 3a0014a80bd4f1f6c786638ddec23a1852c9a635
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239130"
---
# <a name="design-details-order"></a>Designdetails: Auftrag
In einer Auftragsfertigungsumgebung wird ein Artikel bezogen oder gefertigt, um einen speziellen Bedarf zu decken. Normalerweise bezieht sich dies auf A-Artikel, und die Motivation für die Auswahl des Auftragswiederbeschaffungsverfahrens kann es sein, dass der Bedarf selten ist, die Vorbereitungszeit unbedeutend ist, oder die erforderlichen Attribute variieren können.  
  
Das Programm erstellt einen Auftrag-zu-Auftrag-Link, der als vorläufige Verbindung zwischen dem Vorrat, einem Beschaffungsauftrag oder dem Bestand und dem bedarf, der erfüllt werden soll, fungiert.  
  
Abgesehen von der Verwendung der Auftragsrichtlinie, kann die Auftrag-zu-Auftragverknüpfung in folgender Weise verwendet werden:  
  
* Bei Verwendung der Produktionsart "Auftragsfertigung", um mehrstufige oder projekttypbezogene Fertigungsaufträge (Herstellung benötigter Komponenten im selben Fertigungsauftrag) zu erstellen.  
* Wenn die Verkaufsauftrags-Planungsfunktion verwendet wird, um einen Fertigungsauftrag aus einem Verkaufsauftrag zu erstellen.  
  
Selbst wenn ein Produktionsbetrieb sich als Auftragsfertigungsumgebung sieht, kann es am besten sein, ein Charge-für-Charge-Wiederbeschaffungsverfahren zu verwenden, wenn der Artikel reiner Standard ohne Variation der Attribute ist. Deshalb verwendet das System nicht geplanten Lagerbestand und kumuliert nur Verkaufsaufträge mit demselben Lieferdatum oder in einem definierten Zeitrahmen.  
  
## <a name="order-to-order-links-and-past-due-dates"></a>Auftrag-zu-Auftrag-Links und überfällige Datumsangaben  
Anders als die meisten Angebot-Nachfrage Datensätze werden verknüpfte Aufträge vor dem Startdatum vollständig vom System geplant. Der Geschäftsgrund für diese Ausnahme ist, dass bestimmte Bedarf-Vorrat-Sätze bis zur Ausführung synchronisiert werden müssen. Weitere Informationen zu der fixierten Zone, die für die meisten Bedarf-Vorrat-Typen gilt, finden Sie unter [Designdetails: Abwicklung von Aufträgen vor dem Planungs-Startdatum](design-details-dealing-with-orders-before-the-planning-starting-date.md).  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)