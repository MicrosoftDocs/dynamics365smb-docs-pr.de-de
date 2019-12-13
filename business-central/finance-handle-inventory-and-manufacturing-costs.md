---
title: Verarbeiten von Lager- und Fertigungskosten | Microsoft Docs
description: Obgleich viele der Kostenberechnungsfunktionen in untergeordneten Prozessen ohne Benutzereingriff ausgedrückt werden (beispielsweise Postenausgleich und automatische Lagerregulierung), sind eine Reihe von Feldern, Seiten und Berichten für Benutzer konzipiert, die die Kosten von Artikeln oder Arbeitsgängen direkt oder indirekt verwalten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8eceae6e325d4b5c1cf5cc4b0ba509c4624dd9f4
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879776"
---
# <a name="handling-inventory-and-manufacturing-costs"></a>Verarbeiten von Lager- und Fertigungskosten
Obgleich viele der Kostenberechnungsfunktionen in untergeordneten Prozessen ohne Benutzereingriff ausgedrückt werden (beispielsweise Postenausgleich und automatische Lagerregulierung), sind eine Reihe von Feldern, Seiten und Berichten für Benutzer konzipiert, die die Kosten von Artikeln oder Arbeitsgängen direkt oder indirekt verwalten.  

 Das Zuordnen von Artikelzu-/-abschlägen zu Einkaufsbelegen ist ein Beispiel für eine indirekte Kostenberechnungsaufgabe. Das Aktualisieren des Einstandspreises von Produktionsstücklistenartikeln ist ein Beispiel für eine direktere Kostenberechnungsaufgabe.  

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Aufgabe**|**Siehe**|  
|------------|-------------|  
|Periodisches oder automatisches Aktualisieren des Einstandspreises von Artikeln, um Kostenänderungen bei eingehenden Posten (beispielsweise Posten für Einkäufe oder gefertigte Artikel) an die zugehörigen ausgehenden Posten (beispielsweise Verbrauch oder Umlagerung) weiterzugeben|[Artikelpreise justieren](inventory-how-adjust-item-costs.md)|  
|Verschaffen eines Überblicks über die Dynamik des durchschnittlichen Einstandspreises, um Entscheidungen zur Preisgestaltung zu treffen oder Kostenschwankungen nachzugehen, die auf Dateneingabefehler zurückzuführen sind|[Neue Artikel registrieren](inventory-how-register-new-items.md)|  
|Erstellen des festen Einstandspreises eines Fertigungsartikels durch Eingeben der drei Kostenelemente: Materialkosten, Kapazitätskosten und Fremdarbeiterkosten|[Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)|  
|Berechnen des Einstandspreises eines Stücklistenartikels auf der Grundlage der Einstandspreise der zugrundeliegenden Komponenten|[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)|  
|Abschließen des Kostenberechnungs-Lebenszyklus eines gefertigten Artikels durch Regulieren der Kosten sowie Abstimmen der Wertposten mit der Finanzbuchhaltung|[Info zu Kosten des beendeten Auftrags](finance-about-finished-production-order-costs.md)|  
|Ändern des Werts eines Artikels im Lagerbestand oder des Werts eines Artikelpostens (beispielsweise einer Einkaufstransaktion)|[Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md)|
|Manuelles Rückgängigmachen eines Artikelausgleichs oder erneutes Ausgleichen von Artikelposten, die durch die Anwendung erstellt wurden|[Artikelposten entfernen und erneut ausgleichen](finance-how-to-remove-and-reapply-item-entries.md)|  
|Sie können das Feld **Eintrag anwenden** im Buch.-Blatt verwenden, um manuell einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen.|[Schließen von offenen Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Siehe auch  
[Lagerkosten Verwalten](finance-manage-inventory-costs.md)
[Designdetails: Lagerkosten](design-details-inventory-costing.md)
