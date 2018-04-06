---
title: 'Designdetails: Integration mit dem Lagerbestand | Microsoft Docs'
description: Der Logistik-Anwendungsbereich und der Lager-Anwendungsbereich interagieren miteinander im physischen Bestand und in der Bestands- und Lageranpassung.
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
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a>Designdetails: Integration mit dem Lagerbestand
Der Logistik-Anwendungsbereich und der Lager-Anwendungsbereich interagieren miteinander im physischen Bestand und in der Bestands- und Lageranpassung.  
  
## <a name="physical-inventory"></a>Inventur  
 Das **Logistik-Inventur-Buch.-Blatt**-Fenster wird mit dem **Inventur Buch.-Blatt**-Fenster für alle erweiterten Lagerorte verwendet. Der Bestand auf Lagerplatzebene wird berechnet, und eine gedruckte Liste wird für den Lagermitarbeiter bereitgestellt. Die Liste zeigt, welche Artikel an welchen Lagerplätzen gezählt werden müssen.  
  
 Der Lagermitarbeiter gibt die gezählte Menge im **Logistik-Inventur-Buch.-Blatt** Fenster ein und bucht das Buch.-Blatt.  
  
 Wenn die gezählte Menge größer als die Menge auf der Buch.-Blattzeile ist, wird eine Umlagerung für diese Differenz aus dem Standard-Ausgleichslagerplatz zum gezählten Lagerplatz gebucht. Dieses erhöht die Menge im gezählten Lagerplatz und vermindert die Menge im Standard-Ausgleichslagerplatz.  
  
 Wenn die gezählte Menge geringer als die Menge auf der Buch.-Blattzeile ist, wird eine Umlagerung für diese Differenz aus dem gezählten Lagerplatz zum Standard-Ausgleichslagerplatz gebucht. Dieses reduziert die Menge im gezählten Lagerplatz und erhöht die Menge im Standard-Ausgleichslagerplatz.  
  
 In erweiterten Lagerfunktionskonfigurationen wird der Wert im Feld **Menge (berechnet)** aus den Artikelposten einbezogen und der Wert im Feld **Menge (Phys. Lagerbestand)** aus den Lagerplatzposten ohne Ausgleichslagerplatzinhalt abgerufen. Das Feld **Menge** gibt die Differenz zwischen den ersten beiden Feldern an, die dem Inhalt des Regulierungslagerplatzes entsprechen sollte.  
  
 Wenn Sie das Inventur Buch.-Blatt buchen, werden der Lagerbestand und der Ausgleichslagerplatz aktualisiert.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Lagerplatz-Ausgleich mit dem Artikelposten  
 Sie verwenden das Fenster **Artikel Buch.-Blatt** und die Funktion **Ausgleich berechnen**, um den Lagerbestand im Artikelposten in Übereinstimmung mit einem Ausgleich anzupassen, der für die Artikelmenge in einem Lagerplatz vorgenommen wurde. Um eine Verbindung zwischen den Lagerbestand und der Logistik zu erstellen, müssen Sie einen Vorgabe-Ausgleichslagerplatz pro Lagerort festlegen.  
  
 Der Standard-Regulierungslagerplatz registriert Artikel im Lager, wenn Sie einen Zugang für den Bestand buchen. Wenn Sie jedoch einen Lagerabgang buchen, wird die Menge am Lagerplatz ebenfalls verringert. In beiden Fällen werden Artikelposten und Lagerposten erstellt.  
  
> [!NOTE]  
>  Der Ausgleichslagerplatz ist nicht in der Verfügbarkeitsberechnung enthalten.  
  
 Wenn Sie den Lagerplatzinhalt anpassen wollen, können Sie das Logistik Artikel-Buch.-Blatt verwenden, von dem Sie die Artikelnummer, den Zonencode, den Lagerplatzcode und die Menge angeben können, die Sie anpassen möchten.  
  
 Wenn Sie eine positive Menge eingeben und die Zeile buchen, wird der Bestand an dem Lagerplatz erhöht, und die Menge des Standard-Ausgleichslagerplatzes wird entsprechend vermindert.  
  
## <a name="see-also"></a>Siehe auch  
 [Designdetails: Logistik](design-details-warehouse-management.md)   
 [Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md)
