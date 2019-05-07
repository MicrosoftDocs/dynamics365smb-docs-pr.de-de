---
title: 'Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen'
description: Die Liste Kreditorenzahlungen zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.
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
ms.openlocfilehash: 932ea1f1452db27cbf13ef6ae6ed133a976b9e1f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "914008"
---
# <a name="print-vendor-payments-list-reports"></a>Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen
Die Liste **Kreditorenzahlungen** zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.  

## <a name="to-print-the-vendor-payments-list-report"></a>Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kreditorenzahlung einrichten** ein und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Sortieren**|Gibt den sortierten Auftrag an. Sie können chronologisch oder nach Kreditor sortieren. Wenn Sie nach Kreditor sortieren, finden Sie eine Zwischensumme für jeden Kreditor. Wenn Sie chronologisch sortieren, finden Sie keine Zwischensummen.|  
    |**Layout**|Gibt die Nummer des Berichtslayouts an.<br /><br /> Die Ergebnisse können in den folgenden Layouts angezeigt werden:<br /><br /> **Standard**<br /> Zeigt die Kreditorennummer und den Kreditorennamen, zusammen mit den Buchungsdetails wie Dokumentennummer und den Betrag in lokaler Währung an.<br /><br /> **FCY-Beträge**<br /> Zeigt die Kreditorennummer, Kreditorennamen, Belegnummer, Zahlungsstatus (O für den Wert Offen, PP. für Teilzahlung und C für geschlossene) an.<br /><br /> **Buchungsinfo**<br /> Zeigt die Kreditorennummer, den Kreditorennamen, die Kostenstelle, das Kostenobjekt, die Benutzer-ID und den Zahlungsbetrag an.|  

 Am Ende des Berichts wir die Anzahl der verarbeiteten Zahlungen angezeigt.  

## <a name="see-also"></a>Siehe auch  
[Zahlungen vornehmen](../../payables-make-payments.md)
