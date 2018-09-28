---
title: "Designdetails: Artikelverfolgung und Verfügbarkeit | Microsoft Docs"
description: "Die **Artikelverfolgungszeilen** und **Artikelverlaufs-Zusammenfassung** Fenster stellen dynamische Verfügbarkeitsinformationen für Serien- oder Chargennummern bereit. Der Zweck besteht darin, die Transparenz für Benutzer bei ausgehenden Belegen, wie etwa Verkaufsaufträgen, zu erhöhen, indem ihnen gezeigt wird, welche Seriennummern oder wie viele Einheiten einer Charge derzeit auf anderen offenen Belegen zugewiesen sind. Dadurch wird die Ungewissheit reduziert, die durch doppelte Zuteilung entsteht und den Auftragsbearbeiter wird das Vertrauen vermittelt, dass die Artikelverfolgungsnummern und die Daten, die sie in nicht gebuchten Verkaufsaufträgen versprechen, erfüllt werden können."
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
ms.openlocfilehash: a58bd4ccc8f31ef0d90bf27f3a89e98bcdb56fe4
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-availability"></a>Designdetails: Artikelverfolgungsverfügbarkeit
Die **Artikelverfolgungszeilen** und **Artikelverlaufs-Zusammenfassung** Fenster stellen dynamische Verfügbarkeitsinformationen für Serien- oder Chargennummern bereit. Der Zweck besteht darin, die Transparenz für Benutzer bei ausgehenden Belegen, wie etwa Verkaufsaufträgen, zu erhöhen, indem ihnen gezeigt wird, welche Seriennummern oder wie viele Einheiten einer Charge derzeit auf anderen offenen Belegen zugewiesen sind. Dadurch wird die Ungewissheit reduziert, die durch doppelte Zuteilung entsteht und den Auftragsbearbeiter wird das Vertrauen vermittelt, dass die Artikelverfolgungsnummern und die Daten, die sie in nicht gebuchten Verkaufsaufträgen versprechen, erfüllt werden können. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgungszeilenfenster.](design-details-item-tracking-lines-window.md)  

 Bei Öffnen des Fensters **Artikelnachverfolgungszeilen** werden Daten aus den Tabellen **Artikelposten** und **Reservierungsposten** abgerufen, jedoch ohne Datumsfilter. Wenn Sie das Feld **Seriennr**. oder das Feld **Chargennr**. auswählen, wird das Fenster geöffnet und eine Zusammenfassung der **Artikelverfolgungsinformationen** in der Tabelle **Reservierungsposten** angezeigt. Die Zusammenfassung enthält die folgenden Informationen über jede Serien- oder Chargennummer auf der Artikelverfolgungszeile:  

|Feld|Beschreibung|  
|---------------------------------|---------------------------------------|  
|**Gesamtmenge**|Die Gesamtmenge der aktuell im Lager vorhandenen Chargen- oder Seriennummern.|  
|**Total angeforderte Menge**|Enthält die Gesamtmenge der aktuell angeforderten Chargen- oder Seriennummer in allen Belegen.|  
|**Aktuell ausstehende Menge**|Die Menge, die in der aktuellen Instanz des Fensters **Artikelnachverfolgungszeilen** eingegeben ist, jedoch noch nicht in der Datenbank aufgezeichnet wurde.|  
|**Total verfügbare Menge**|Die Menge der Serien- oder Chargennummer, die für Nachfragen durch den Benutzer verfügbar ist.<br /><br /> Diese Menge wird aus anderen Feldern im Fenster berechnet, wie folgt:<br /><br /> Gesamtmenge (erforderliche Gesamtmenge - Aktuell ausstehende Menge).|  

> [!NOTE]  
>  Sie können die Informationen in der vorangehenden Tabelle anzeigen, indem Sie die Funktion **Einträge auswählen** im Fenster **Artikelnachverfolgungszeile** verwenden.  

 Um die Datenbankleistung beizubehalten, werden Verfügbarkeitsdaten nur einmal aus der Datenbank abgerufen, wenn Sie das **Artikelverfolgungszeilen**-Fenster öffnen und die **Verfügbarkeit aktualisieren**-Funktion im Fenster verwenden.  

## <a name="calculation-formula"></a>Formel  
 Wie in der vorangehenden Tabelle beschrieben, wird die Verfügbarkeit einer bestimmten Serien- oder Chargennummer wie folgt berechnet.  

 gesamte verfügbare Menge = Menge im Lagerbestand - (alle Bedarfsposten + Menge noch nicht in die Datenbank übernommen)  

> [!IMPORTANT]  
>  Diese Formel impliziert dass die Serien- oder Chargennummerenverfügbarkeitsberechnung nur den Lagerbestand berücksichtigt und voraussichtliche Wareneingänge ignoriert. Entsprechend beeinflussen Vorräte, die noch nicht gebucht sind, nicht die Artikelverfolgungsverfügbarkeit, im Gegensatz zur regulären Artikelverfügbarkeit, in der voraussichtliche Wareneingänge enthalten sind.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)

