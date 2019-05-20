---
title: Designdetails - Maximale Menge | Microsoft Docs
description: Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 857a01bac28d85a35668f3aa01e8807a6f6dc845
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239153"
---
# <a name="design-details-maximum-qty"></a>Designdetails: Höchstmenge
Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.  

 Alles im Zusammenhang mit der festen Bestellmengenrichtlinie bezieht sich auch auf diese Richtlinie. Der einzige Unterschied ist die Menge des vorgeschlagenen Vorrats. Wenn Sie die Methode Auffüllen auf Maximalbestand verwenden, erfolgt die Definition der Bestellmenge dynamisch auf Basis des voraussichtlichen Lagerbestandes und unterscheidet sich daher normalerweise von Auftrag zu Auftrag.  

## <a name="calculated-per-time-bucket"></a>Berechnet pro Zeitrahmen  
 Die Nachbestellungsmenge wird zu dem Zeitpunkt bestimmt (am Ende eines Zeitrahmens), wenn das Planungssystem erkennt, dass der Minimalbestand überschritten wurde. Zu diesem Zeitpunkt misst das System die Lücke von der aktuellen Stufe des voraussichtlichen Lagerbestands bis zum angegebenen Maximalbestand. Dies bildet die Menge, die wiederbestellt werden soll. Die Anwendung überprüft dann, ob Vorrat bereits anderswo bestellt worden, um innerhalb der Beschaffungszeit erhalten zu werden, und falls ja, reduziert es die Menge des neuen Beschaffungsauftrags um bereits bestellte Mengen.  

 Die Anwendung stellt sicher, dass der voraussichtliche Lagerbestand mindestens die Minimalbestandsebene erreicht - falls der Benutzer vergessen hat, eine maximale Lagerbestandsmenge anzugeben.  

## <a name="combines-with-order-modifiers"></a>Wird mit anderen Auftragsmodifizierern kombiniert  
 Abhängig von den Einstellungen kann es am besten sein, die Methode „Maximale Menge“ mit Auftragsmodifikationen zu kombinieren, um eine Mindestauftragsmenge sicherzustellen, oder sie auf eine ganze Zahl von Einkaufsmengeneinheiten zu runden, bzw. sie in mehrere Chargen aufzuteilen, wie von der maximalen Auftragsmenge definiert.  

## <a name="combines-with-calendars"></a>Zusammenfassen mit Kalendern  
 Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarten** festgelegt werden.  

 Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum. Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
 [Designdetails: Planungsparameter](design-details-planning-parameters.md)   
 [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)
