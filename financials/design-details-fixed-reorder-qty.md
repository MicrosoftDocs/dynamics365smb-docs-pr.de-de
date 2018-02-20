---
title: Designdetails - Feste Nachbestellmenge | Microsoft Docs
description: "Das Richtlinie „Feste Bestellmenge“ bezieht sich auf die Bestandsplanung typischer C-Artikel (niedrige Bestandskosten, geringes Veraltungsrisiko und/oder zahlreiche Artikel). Diese Methode wird normalerweise in Verbindung mit einem Minimalbestand verwendet, der den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels angezeigt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7726a1b5749aa4da14d06d3484ee83668531f84f
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-fixed-reorder-qty"></a>Designdetails: Feste Nachbestellmenge
Das Richtlinie „Feste Bestellmenge“ bezieht sich auf die Bestandsplanung typischer C-Artikel (niedrige Bestandskosten, geringes Veraltungsrisiko und/oder zahlreiche Artikel). Diese Methode wird normalerweise in Verbindung mit einem Minimalbestand verwendet, der den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels angezeigt.  

## <a name="calculated-per-time-bucket"></a>Berechnet pro Zeitrahmen  
 Wenn das Planungssystem erkennt, dass der Minimalbestand einen bestimmten Zeitrahmen (Nachbestellungszyklus) erreicht oder unterschritten hat – oberhalb oder am Minimalbestand am Beginn der Periode bzw. unter oder am Minimalbestand am Ende der Periode –, schlägt es vor, einen neuen Beschaffungsauftrag mit der angegebenen Bestellmenge zu erstellen und ihn vorwärts vom ersten Datum des Endes des Zeitrahmens an zu planen.  

 Das Konzept des Minimalbestands im Zeitrahmen reduziert reduziert die Anzahl der Beschaffungsvorschläge. Dieses spiegelt einen manuellen Vorgang des häufigen Durchgangs durch das Lager wirder, um die tatsächlichen Inhalte in den unterschiedlichen Lagerplätzen zu prüfen.  

## <a name="creates-only-necessary-supply"></a>Erstellt nur erforderlichen Vorrat  
 Bevor ein neuer Beschaffungsauftrag gemacht wird, um einen Minimalbestand einzuhalten, prüft das Planungssystem, ob Vorrat bereits bestellt wurde, um innerhalb der Vorlaufzeit des Artikels einzugehen. Wenn ein vorhandener Beschaffungsauftrag das Problem löst, indem er den voraussichtlichen Lagerbestand auf oder über den Minimalbestand innerhalb der Beschaffungszeit bringt, schlägt die Anwendung keinen neuen Beschaffungsauftrag vor.  

 Beschaffungsaufträge, die speziell erstellt werden, um einen Minimalbestand zu erfüllen, werden aus dem normalen Vorratsausgleich ausgeschlossen und werden auch nachher in keiner Weise geändert. Deshalb gilt: Wenn ein Artikel mithilfe des Minimalbestands abgewickelt werden soll (d.h. nicht mehr aufgefüllt wird), sollten Sie ausstehende Beschaffungsaufträge manuell überprüfen oder die Wiederbeschaffungsrichtlinie Charge für Charge ändern, wodurch das System überflüssigen Vorrat reduziert oder storniert.  

## <a name="combines-with-order-modifiers"></a>Wird mit anderen Auftragsmodifizierern kombiniert  
 Die Auftragsmodifikatoren minimale Auftragsmenge, maximale Auftragsmenge und Auftragsvielfaches sollten keine große Rolle spielen, wenn die feste Nachbestellungsmengenrichtlinie verwendet wird. Das Planungssystem berücksichtigt jedoch diese Modifizierer und vermindert die Menge auf die angegebene Auftragshöchstmenge (und erstellt zwei oder mehr Vorräte, um die Gesamtauftragsmenge zu erreichen), erhöht den Auftrag auf die angegebene Auftragsmindestmenge oder rundet die Auftragsmenge auf, um ein angegebenes Auftragsvielfaches zu erreichen.  

## <a name="combines-with-calendars"></a>Zusammenfassen mit Kalendern  
 Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** in den Feldern **Firmendaten** und **Lagerortkarten** festgelegt werden.  

 Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum. Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.  

## <a name="should-not-be-used-with-forecast"></a>Sollte nicht mit Planung verwendet werden  
 Da der erwartete Bedarf bereits in der Minimalbestandsebene angegeben wird, ist es nicht notwendig, eine Prognose in die Planung eines Artikels mit einem Minimalbestand zu berücksichtigen. Wenn es wichtig ist, den Plan auf einer Planung zu basieren, verwenden Sie die Charge-für-Charge-Richtlinie.  

## <a name="must-not-be-used-with-reservations"></a>Darf nicht mit Reservierungen verwendet werden  
 Wenn der Benutzer eine Menge, etwa eine Menge im Bestand, für einen späteren Bedarf reserviert hat, ist die Grundlage der Planung gestört. Selbst wenn der voraussichtliche Lagerbestand im Hinblick auf den Minimalbestand akzeptabel ist, stehen die Mengen möglicherweise aufgrund der Reservierung nicht zur Verfügung. Die Anwendung versucht möglicherweise, dies auszugleichen, indem es Ausnahmeaufträge erstellt; jedoch empfiehlt es sich, dass das Reservefeld für Artikel, die unter Verwendung eines Minimalbestands geplant werden, auf Nie festgelegt wird.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
 [Designdetails: Höchstmenge](design-details-maximum-qty.md)   
 [Designdetails: Planungsparameter](design-details-planning-parameters.md)   
 [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)

