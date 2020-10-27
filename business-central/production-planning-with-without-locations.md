---
title: Siehe Planung mit/ohne Lagerortcodes  | Microsoft Docs
description: Die Planung mit oder ohne Lagerortcodes unter diesen Voraussetzungen in geradliniger Weise ist wichtig zu verstehen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2cf9c34434136578b6ab31841c5bb7f69f72ae18
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921467"
---
# <a name="planning-with-or-without-locations"></a>Siehe Planung mit/ohne Lagerortcodes.
In der Planung mit oder ohne Lagerortcodes in Bedarfszeilen arbeitet das Planungssystem unter diesen Voraussetzungen in geradliniger Weise:  

-   Die Bedarfszeilen enthalten immer Lagerortcodes, und das System verwendet in vollem Umfang Lagerhaltungsdaten, einschließlich der betreffenden Lagerorteinrichtung.  
-   Die Bedarfszeilen enthalten nie Lagerortcodes, und das System verwendet keine Lagerhaltungsdaten oder irgendeine Lagerorteinrichtung (siehe letztes Szenario unten).  

Wenn jedoch die Bedarfszeilen manchmal Lagerortcodes aufweisen und manchmal nicht, folgt das Planungssystem je nach Einrichtung bestimmten Regeln.  

## <a name="demand-at-location"></a>Bedarf am Lagerort  
Wenn das Planungssystem Bedarf an einem Lagerort (eine Zeile mit einem Lagerortcode) erkennt, verhält es sich in verschiedener Weise, abhängig von drei kritischen Konfigurationswerten.  

Während eines Planungslaufs führt das System der Reihe nach eine Überprüfung auf die drei Konfigurationswerte durch und plant entsprechend:  

1.  Ist das Feld **Lagerort notwendig** mit einem Häkchen markiert?  

    Falls ja:  

2.  Sind Lagerhaltungsdaten für den Artikel vorhanden?  

    Falls ja:  

    Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.  

    Falls nein:  

3.  Enthält das Feld **Komponenten von Lagerort** den angeforderen Lagerortcode?  

    Falls ja:  

    Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

    Falls nein:  

    Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* , Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer. (Artikel mit dem Wiederbeschaffungsverfahren  *Bestellung* verbleiben auf  *Bestellung* sowie auf allen anderen für sie festgelegten Einstellungen.)  

> [!NOTE]  
>  Diese Minimalalternative deckt nur den exakten Bedarf ab. Alle definierten Planungsparameter werden ignoriert.  

Siehe Abweichungen in den unten angeführten Szenarien.  

## <a name="demand-at-blank-location"></a>Bedarf an "leerer Lagerort"  
Selbst bei markiertem Feld **Lagerort notwendig** erlaubt das System die Erstellung von Bedarfszeilen ohne Lagerortcode – auch als Lagerort *LEER* bezeichnet. Dies stellt für das System eine Abweichung dar, weil mehrere Konfigurationswerte für die Behandlung von Lagerorten optimiert sind, und im Ergebnis erstellt das Planungsmodul für eine solche Bedarfszeile keine Planungszeile. Wenn das Feld **Lagerort notwendig** nicht markiert ist, jedoch andere Konfigurationswerte für den Lagerort vorhanden sind, wird auch dieser Fall als Abweichung betrachtet, und das Planungssystem reagiert mit der Ausgabe der "Minimalalternative":   
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt *Bestellung* ), Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer.  

Siehe Abweichungen in den unten angeführte Setup-Szenarien.  

### <a name="setup-1"></a>Konfiguration 1:  

-   Lagerort notwendig = *Ja*  
-   Lagerhaltungsdaten sind für  *ROT* eingerichtet  
-   Komponente an Lagerort =  *BLAU*  

#### <a name="case-11-demand-is-at--red-location"></a>Fall 1.1: Es besteht Bedarf am Lagerort  *ROT*  

Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant (einschließlich möglicher Umlagerungen).  

#### <a name="case-12-demand-is-at--blue-location"></a>Fall 1.2: Es besteht Bedarf am Lagerort *BLAU*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

#### <a name="case-13-demand-is-at--green-location"></a>Fall 1.3: Es besteht Bedarf am Lagerort  *GRÜN*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung* ), Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer.  

#### <a name="case-14-demand-is-at--blank-location"></a>Fall 1.4: Es besteht Bedarf am Lagerort *LEER*  

Der Artikel wird nicht geplant, weil kein Lagerort in der Bedarfszeile definiert ist.  

### <a name="setup-2"></a>Konfiguration 2:  

-   Lagerort notwendig = *Ja*  
-   Es sind keine Lagerhaltungsdaten vorhanden.  
-   Komponente an Lagerort =  *BLAU*  

#### <a name="case-21-demand-is-at--red-location"></a>Fall 2.1: Es besteht Bedarf am Lagerort  *ROT*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung* ), Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer.  

#### <a name="case-22-demand-is-at--blue-location"></a>Fall 2.2: Es besteht Bedarf am Lagerort *BLAU*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

### <a name="setup-3"></a>Konfiguration 3:  

-   Lagerort notwendig = *Nein*  
-   Es sind keine Lagerhaltungsdaten vorhanden.  
-   Komponente an Lagerort =  *BLAU*  

#### <a name="case-31-demand-is-at--red-location"></a>Fall 3.1: Es besteht Bedarf am Lagerort  *ROT*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung* ), Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer.  

#### <a name="case-32-demand-is-at--blue-location"></a>Fall 3.2: Es besteht Bedarf am Lagerort *BLAU*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

#### <a name="case-33-demand-is-at--blank-location"></a>Fall 3.3: Es besteht Bedarf am Lagerort  *LEER*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung* ), Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer.  

### <a name="setup-4"></a>Konfiguration 4:  

-   Lagerort notwendig = *Nein*  
-   Es sind keine Lagerhaltungsdaten vorhanden.  
-   Komponente an Lagerort =  *LEER*  

#### <a name="case-41-demand-is-at--blue-location"></a>Fall 4.1: Es besteht Bedarf am Lagerort  *BLAU*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung* ), Lagerbestand berücksichtigen =  *Ja* , alle anderen Planungsparameter = Leer.  

#### <a name="case-42-demand-is-at--blank-location"></a>Fall 4.2: Es besteht Bedarf am Lagerort  *LEER*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

Wie aus dem letzten Szenario ersehen werden kann, besteht die einzige Möglichkeit, ein richtiges Ergebnis für eine Bedarfszeile ohne Lagerortcode zu erhalten, im Deaktivieren aller konfigurierten Werte, die sich auf Lagerorte beziehen. Analog besteht die einzige Möglichkeit, stabile Planungsergebnisse für den Bedarf an den Lagerorten zu erhalten, in der Verwendung von Lagerhaltungsdaten.  

Wenn Sie häufig den Bedarf an Lagerorten planen müssen, empfiehlt sich daher dringend die Verwendung der Funktion Lagerhaltungsdaten.  

## <a name="see-also"></a>Siehe auch
[Planung](production-planning.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Vorratsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
