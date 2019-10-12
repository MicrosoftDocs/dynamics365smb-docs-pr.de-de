---
title: 'Designdetails: Charge für Charge | Microsoft Docs'
description: Erfahren Sie, wie die Charge-für-Charge-Rrichtlinie verwendet wird, um die Bestellmenge auf Grundlage von Bedarf abzustimmen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 5669378383d94b33a25a60a882709885e1463a6d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303101"
---
# <a name="design-details-lot-for-lot"></a>Designdetails: Charge für Charge
Die Charge-für-Charge-Richtlinie ist die flexibelste, da das System nur auf tatsächlichen Bedarf reagiert; dazu reagiert sie auf voraussichtlichen Bedarf aus der Planung und auf Rahmenaufträge und gleicht die Auftragsmenge auf der Grundlage des Bedarfs ab. Die Charge-für-Charge-Richtlinie bezieht sich auf A- und B-Artikel, bei denen der bestand angenommen werden kann, jedoch vermieden werden sollte.  

In mancher Hinsicht sieht die Charge-für-Charge-Richtlinie wie die Auftragsrichtlinie aus, sie verfolgt jedoch einen generischen Ansatz für Artikel; sie kann Mengen im Bestand akzeptieren und bündelt Bedarf und den entsprechenden Vorrat in Zeitrahmen, die vom Benutzer definiert werden.  

Das Zeitrahmen wird im Feld **Zeitrahmen** definiert. Die Anwendung arbeitet mit einem minimale Zeitrahmen von einem Tag, da dies die kleinste Zeiteinheit bei Bedarfs- und Vorratsereignissen im System ist (obwohl in der Praxis die Zeiteinheit in Fertigungsaufträgen und Komponentenbedarfen Sekunden sein kann).  

Das Zeitrahmen legt auch Grenzen dafür fest, wann ein vorhandener Beschaffungsauftrag umgeplant werden soll, um einen angegebenen Bedarf zu erfüllen. Wenn der Vorrat innerhalb des Zeitrahmens liegt, wird dieser ein- oder ausgeplant, um den Bedarf zu erfüllen. Wenn er jedoch vor dem Zeitrahmen liegt, verursacht er eine unnötige Anhäufung des Lagerbestandes und sollte storniert werden. Wenn es später liegt, wird stattdessen ein neuer Beschaffungsauftrag erstellt.  

Mit dieser Methode ist es möglich, einen Sicherheitsbestand festzulegen, um mögliche Schwankungen im Vorrat auszugleichen oder plötzlichen Bedarf zu decken.  

Da die Beschaffungsauftragsmenge auf dem tatsächlichen Bedarf basiert, kann es sinnvoll sein, die Auftragsmodifikationen zu verwenden: Aufrunden der Auftragsmenge, um ein angegebenes Auftragsvielfaches zu erreichen (oder eine Einkaufsmengeneinheit), Erhöhen der Auftragsmenge auf eine angegebene Mindestauftragsmenge oder Vermindern der Menge auf die angegebene Auftragshöchstmenge (wodurch zwei oder mehr Vorräte zum Erreichen der insgesamt benötigten Menge erstellt werden).  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
