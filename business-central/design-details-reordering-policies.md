---
title: Designdetails -Wiederbeschaffungsverfahren | Microsoft Docs
description: Dieses Thema enthält eine Übersicht von Policen für Artikelergänzungen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 4aaef129da953596632b56716eaff2f0c47736f7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798416"
---
# <a name="design-details-reordering-policies"></a>Designdetails: Wiederbeschaffungsrichtlinien
Wiederbeschaffungsrichtlinien definieren, wie viel zu bestellen ist, wenn der Artikel aufgefüllt werden muss. Es gibt verschiedene Wiederbeschaffungsverfahren.  

## <a name="fixed-reorder-qty"></a>Feste Bestellmenge
Das Richtlinie „Feste Bestellmenge“ bezieht sich auf die Bestandsplanung typischer C-Artikel (niedrige Bestandskosten, geringes Veraltungsrisiko und/oder zahlreiche Artikel). Diese Methode wird normalerweise in Verbindung mit einem Minimalbestand verwendet, der den voraussichtlichen Bedarf während der Beschaffungszeit des Artikels angezeigt.  

### <a name="calculated-per-time-bucket"></a>Berechnet pro Zeitrahmen  
 Wenn das Planungssystem erkennt, dass der Minimalbestand einen bestimmten Zeitrahmen (Nachbestellungszyklus) erreicht oder unterschritten hat – oberhalb oder am Minimalbestand am Beginn der Periode bzw. unter oder am Minimalbestand am Ende der Periode –, schlägt es vor, einen neuen Beschaffungsauftrag mit der angegebenen Bestellmenge zu erstellen und ihn vorwärts vom ersten Datum des Endes des Zeitrahmens an zu planen.  

 Das Konzept des Minimalbestands im Zeitrahmen reduziert reduziert die Anzahl der Beschaffungsvorschläge. Dieses spiegelt einen manuellen Vorgang des häufigen Durchgangs durch das Lager wirder, um die tatsächlichen Inhalte in den unterschiedlichen Lagerplätzen zu prüfen.  

### <a name="creates-only-necessary-supply"></a>Erstellt nur erforderlichen Vorrat  
 Bevor ein neuer Beschaffungsauftrag gemacht wird, um einen Minimalbestand einzuhalten, prüft das Planungssystem, ob Vorrat bereits bestellt wurde, um innerhalb der Vorlaufzeit des Artikels einzugehen. Wenn ein vorhandener Beschaffungsauftrag das Problem löst, indem er den voraussichtlichen Lagerbestand auf oder über den Minimalbestand innerhalb der Beschaffungszeit bringt, schlägt die Anwendung keinen neuen Beschaffungsauftrag vor.  

 Beschaffungsaufträge, die speziell erstellt werden, um einen Minimalbestand zu erfüllen, werden aus dem normalen Vorratsausgleich ausgeschlossen und werden auch nachher in keiner Weise geändert. Deshalb gilt: Wenn ein Artikel mithilfe des Minimalbestands abgewickelt werden soll (d.h. nicht mehr aufgefüllt wird), sollten Sie ausstehende Beschaffungsaufträge manuell überprüfen oder die Wiederbeschaffungsrichtlinie Charge für Charge ändern, wodurch das System überflüssigen Vorrat reduziert oder storniert.  

### <a name="combines-with-order-modifiers"></a>Wird mit anderen Auftragsmodifizierern kombiniert  
 Die Auftragsmodifikatoren minimale Auftragsmenge, maximale Auftragsmenge und Auftragsvielfaches sollten keine große Rolle spielen, wenn die feste Nachbestellungsmengenrichtlinie verwendet wird. Das Planungssystem berücksichtigt jedoch diese Modifizierer und vermindert die Menge auf die angegebene Auftragshöchstmenge (und erstellt zwei oder mehr Vorräte, um die Gesamtauftragsmenge zu erreichen), erhöht den Auftrag auf die angegebene Auftragsmindestmenge oder rundet die Auftragsmenge auf, um ein angegebenes Auftragsvielfaches zu erreichen.  

### <a name="combines-with-calendars"></a>Zusammenfassen mit Kalendern  
 Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarten** festgelegt werden.  

 Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum. Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.  

### <a name="should-not-be-used-with-forecast"></a>Sollte nicht mit Planung verwendet werden  
 Da der erwartete Bedarf bereits in der Minimalbestandsebene angegeben wird, ist es nicht notwendig, eine Prognose in die Planung eines Artikels mit einem Minimalbestand zu berücksichtigen. Wenn es wichtig ist, den Plan auf einer Planung zu basieren, verwenden Sie die Charge-für-Charge-Richtlinie.  

### <a name="must-not-be-used-with-reservations"></a>Darf nicht mit Reservierungen verwendet werden  
 Wenn der Benutzer eine Menge, etwa eine Menge im Bestand, für einen späteren Bedarf reserviert hat, ist die Grundlage der Planung gestört. Selbst wenn der voraussichtliche Lagerbestand im Hinblick auf den Minimalbestand akzeptabel ist, stehen die Mengen möglicherweise aufgrund der Reservierung nicht zur Verfügung. Die Anwendung versucht möglicherweise, dies auszugleichen, indem es Ausnahmeaufträge erstellt; jedoch empfiehlt es sich, dass das Reservefeld für Artikel, die unter Verwendung eines Minimalbestands geplant werden, auf Nie festgelegt wird.

## <a name="maximum-qty"></a>Auffüllen auf Maximalbestand
Die Richtlinie der maximalen Menge ist eine Möglichkeit zur Verwaltung des Bestands anhand eines Minimalbestands.  

Alles im Zusammenhang mit der festen Bestellmengenrichtlinie bezieht sich auch auf diese Richtlinie. Der einzige Unterschied ist die Menge des vorgeschlagenen Vorrats. Wenn Sie die Methode Auffüllen auf Maximalbestand verwenden, erfolgt die Definition der Bestellmenge dynamisch auf Basis des voraussichtlichen Lagerbestandes und unterscheidet sich daher normalerweise von Auftrag zu Auftrag.  

### <a name="calculated-per-time-bucket"></a>Berechnet pro Zeitrahmen  
Die Nachbestellungsmenge wird zu dem Zeitpunkt bestimmt (am Ende eines Zeitrahmens), wenn das Planungssystem erkennt, dass der Minimalbestand überschritten wurde. Zu diesem Zeitpunkt misst das System die Lücke von der aktuellen Stufe des voraussichtlichen Lagerbestands bis zum angegebenen Maximalbestand. Dies bildet die Menge, die wiederbestellt werden soll. Die Anwendung überprüft dann, ob Vorrat bereits anderswo bestellt worden, um innerhalb der Beschaffungszeit erhalten zu werden, und falls ja, reduziert es die Menge des neuen Beschaffungsauftrags um bereits bestellte Mengen.  

Die Anwendung stellt sicher, dass der voraussichtliche Lagerbestand mindestens die Minimalbestandsebene erreicht - falls der Benutzer vergessen hat, eine maximale Lagerbestandsmenge anzugeben.  

### <a name="combines-with-order-modifiers"></a>Wird mit anderen Auftragsmodifizierern kombiniert  
Abhängig von den Einstellungen kann es am besten sein, die Methode „Maximale Menge“ mit Auftragsmodifikationen zu kombinieren, um eine Mindestauftragsmenge sicherzustellen, oder sie auf eine ganze Zahl von Einkaufsmengeneinheiten zu runden, bzw. sie in mehrere Chargen aufzuteilen, wie von der maximalen Auftragsmenge definiert.  

### <a name="combines-with-calendars"></a>Zusammenfassen mit Kalendern  
Bevor ein neuer Beschaffungsauftrag vorgeschlagen wird, einen Minimalbestand einzuhalten, überprüft das Planungssystem, ob der Auftrag für einen nicht freien Tag entsprechend dem Kalender geplant ist, die im Feld **Basiskalendercode** auf den Seiten **Firmendaten** und **Lagerortkarten** festgelegt werden.  

Wenn das geplante Datum ein freier Tag ist, verschiebt das Planungssystem die Reihenfolge weiter zum nächsten Arbeitsdatum. Dadurch ergeben sich möglicherweise ein Verkaufsauftrag, der für einen Minimalbestand gilt, aber keinen bestimmten Bedarf abdeckt. Bei solcher Nachfrage ohne Bedarf erstellt das Planungssystem ein zusätzlicher Vorrat.

## <a name="order"></a>Bestellung
In einer Auftragsfertigungsumgebung wird ein Artikel bezogen oder gefertigt, um einen speziellen Bedarf zu decken. Normalerweise bezieht sich dies auf A-Artikel, und die Motivation für die Auswahl des Auftragswiederbeschaffungsverfahrens kann es sein, dass der Bedarf selten ist, die Vorbereitungszeit unbedeutend ist, oder die erforderlichen Attribute variieren können.  

Das Programm erstellt einen Auftrag-zu-Auftrag-Link, der als vorläufige Verbindung zwischen dem Vorrat, einem Beschaffungsauftrag oder dem Bestand und dem bedarf, der erfüllt werden soll, fungiert.  

Abgesehen von der Verwendung der Auftragsrichtlinie, kann die Auftrag-zu-Auftragverknüpfung in folgender Weise verwendet werden:  

* Bei Verwendung der Produktionsart "Auftragsfertigung", um mehrstufige oder projekttypbezogene Fertigungsaufträge (Herstellung benötigter Komponenten im selben Fertigungsauftrag) zu erstellen.  
* Wenn die Verkaufsauftrags-Planungsfunktion verwendet wird, um einen Fertigungsauftrag aus einem Verkaufsauftrag zu erstellen.  

Selbst wenn ein Produktionsbetrieb sich als Auftragsfertigungsumgebung sieht, kann es am besten sein, ein Charge-für-Charge-Wiederbeschaffungsverfahren zu verwenden, wenn der Artikel reiner Standard ohne Variation der Attribute ist. Deshalb verwendet das System nicht geplanten Lagerbestand und kumuliert nur Verkaufsaufträge mit demselben Lieferdatum oder in einem definierten Zeitrahmen.  

### <a name="order-to-order-links-and-past-due-dates"></a>Auftrag-zu-Auftrag-Links und überfällige Datumsangaben  
Anders als die meisten Angebot-Nachfrage Datensätze werden verknüpfte Aufträge vor dem Startdatum vollständig vom System geplant. Der Geschäftsgrund für diese Ausnahme ist, dass bestimmte Bedarf-Vorrat-Sätze bis zur Ausführung synchronisiert werden müssen. Weitere Informationen zu der fixierten Zone, die für die meisten Bedarf-Vorrat-Typen gilt, finden Sie unter [Designdetails: Abwicklung von Aufträgen vor dem Planungs-Startdatum](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Los-für-Los
Die Charge-für-Charge-Richtlinie ist die flexibelste, da das System nur auf tatsächlichen Bedarf reagiert; dazu reagiert sie auf voraussichtlichen Bedarf aus der Planung und auf Rahmenaufträge und gleicht die Auftragsmenge auf der Grundlage des Bedarfs ab. Die Charge-für-Charge-Richtlinie bezieht sich auf A- und B-Artikel, bei denen der bestand angenommen werden kann, jedoch vermieden werden sollte.  

In mancher Hinsicht sieht die Charge-für-Charge-Richtlinie wie die Auftragsrichtlinie aus, sie verfolgt jedoch einen generischen Ansatz für Artikel; sie kann Mengen im Bestand akzeptieren und bündelt Bedarf und den entsprechenden Vorrat in Zeitrahmen, die vom Benutzer definiert werden.  

Das Zeitrahmen wird im Feld **Zeitrahmen** definiert. Die Anwendung arbeitet mit einem minimale Zeitrahmen von einem Tag, da dies die kleinste Zeiteinheit bei Bedarfs- und Vorratsereignissen im System ist (obwohl in der Praxis die Zeiteinheit in Fertigungsaufträgen und Komponentenbedarfen Sekunden sein kann).  

Das Zeitrahmen legt auch Grenzen dafür fest, wann ein vorhandener Beschaffungsauftrag umgeplant werden soll, um einen angegebenen Bedarf zu erfüllen. Wenn der Vorrat innerhalb des Zeitrahmens liegt, wird dieser ein- oder ausgeplant, um den Bedarf zu erfüllen. Wenn er jedoch vor dem Zeitrahmen liegt, verursacht er eine unnötige Anhäufung des Lagerbestandes und sollte storniert werden. Wenn es später liegt, wird stattdessen ein neuer Beschaffungsauftrag erstellt.  

Mit dieser Methode ist es möglich, einen Sicherheitsbestand festzulegen, um mögliche Schwankungen im Vorrat auszugleichen oder plötzlichen Bedarf zu decken.  

Da die Beschaffungsauftragsmenge auf dem tatsächlichen Bedarf basiert, kann es sinnvoll sein, die Auftragsmodifikationen zu verwenden: Aufrunden der Auftragsmenge, um ein angegebenes Auftragsvielfaches zu erreichen (oder eine Einkaufsmengeneinheit), Erhöhen der Auftragsmenge auf eine angegebene Mindestauftragsmenge oder Vermindern der Menge auf die angegebene Auftragshöchstmenge (wodurch zwei oder mehr Vorräte zum Erreichen der insgesamt benötigten Menge erstellt werden).

## <a name="see-also"></a>Siehe auch  
[Designdetails: Planungsparameter](design-details-planning-parameters.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
