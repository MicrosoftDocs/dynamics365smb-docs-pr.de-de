---
title: Siehe Planung mit/ohne Lagerortcodes.
description: In diesem Thema lernen Sie die Produktion und Fertigung, einschließlich der Vorratsplanung, in Business Central kennen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/16/2021
ms.author: edupont
ms.openlocfilehash: fa1b63bb94152c130077907dbe2d4e0d08281f40
ms.sourcegitcommit: acc1871afa889cb699e65b1b318028c05f8e6444
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2021
ms.locfileid: "6635991"
---
# <a name="planning-with-or-without-locations"></a>Siehe Planung mit/ohne Lagerortcodes.
In der Planung mit oder ohne Lagerortcodes in Bedarfszeilen arbeitet das Planungssystem unter diesen Voraussetzungen in geradliniger Weise:  

-   Die Bedarfszeilen enthalten immer Lagerortcodes, und das System verwendet in vollem Umfang Lagerhaltungsdaten, einschließlich der betreffenden Lagerorteinrichtung.  
-   Die Bedarfszeilen enthalten nie Lagerortcodes, und das System verwendet keine Lagerhaltungsdaten oder irgendeine Lagerorteinrichtung (siehe letztes Szenario unten).  

Wenn jedoch die Bedarfszeilen manchmal Lagerortcodes aufweisen und manchmal nicht, folgt das Planungssystem je nach Einrichtung bestimmten Regeln.  

> [!TIP]
> Wenn Sie oft den Bedarf an verschiedenen Lagerorten planen, wird empfohlen, dass Sie die Funktion „Lagerhaltungsdaten“ verwenden.

## <a name="demand-at-location"></a>Bedarf am Lagerort  

Wenn das Planungssystem Bedarf an einem Lagerort (eine Zeile mit einem Lagerortcode) erkennt, verhält es sich in verschiedener Weise, abhängig von drei kritischen Konfigurationswerten.  

Während eines Planungslaufs führt das System der Reihe nach eine Überprüfung auf die drei Konfigurationswerte durch und plant entsprechend:  

1. Gibt es ein Häkchen im Feld **Lagerort notwendig** auf der Seite **Lagereinrichtung**?  

    Falls ja:  

2. Sind Lagerhaltungsdaten für den Artikel vorhanden?  

    Falls ja:  

    Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.  

    Falls nein:  

3. Enthält das Feld **Komponenten von Lagerort** auf der Seite **Produktion Einrichtung** den gewünschten Lagerortcode?  

    Falls ja:  

    Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

    Falls nein:  

    Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los*, Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer. (Artikel mit dem Wiederbeschaffungsverfahren  *Bestellung* verbleiben auf  *Bestellung* sowie auf allen anderen für sie festgelegten Einstellungen.)  

> [!NOTE]  
> Diese Minimalalternative deckt nur den exakten Bedarf ab. Alle definierten Planungsparameter werden ignoriert.  

Siehe Abweichungen in den unten angeführten Szenarien.  

> [!TIP]
> Das **Lagerort notwendig** auf der Seite **Lager Einrichtung** und das Feld **Komponenten von Lagerort** auf der Seite „Produktion Einrichtung“ sind sehr wichtig, um zu steuern, wie das Planungssystem Bedarfspositionen mit/ohne Lagerortcodes verarbeitet.
>
> Für gekauften Fertigungsbedarf (wenn das Planungsmodul nur für die Einkaufsplanung und nicht für die Produktionsplanung genutzt wird), verwendet [!INCLUDE [prod_short](includes/prod_short.md)] denselben Lagerort für Komponenten, der auch im Fertigungsauftrag angegeben ist. Wenn Sie aber dieses Feld ausfüllen, können Sie die Komponenten an einen anderen Lagerort umleiten.
>
> Sie können dies auch für bestimmte Lagerhaltungsdaten festlegen, indem Sie einen anderen Lagerortcode im Feld **Komponenten von Lagerort** auf der Lagerhaltungsdatenkarte auswählen. Beachten Sie jedoch, dass dies selten sinnvoll ist, da die Planungslogik möglicherweise beim Planen für die Lagerhaltungsdaten-Komponente verfälscht wird.

Ein weiteres wichtiges Feld ist das Feld **Maximale Losgröße** auf der Karte **Artikel**. Es gibt eine maximal zulässige Menge für einen Artikelbestellvorschlag an und wird verwendet, wenn der Artikel in einer festen Transporteinheit, wie einem Container, geliefert wird, die Sie beispielsweise vollständig ausnutzen möchten. Sobald ein Auffüllbedarf festgestellt und die Losgröße entsprechend dem festgelegten Wiederbeschaffungsverfahren angepasst wurde, wird die Menge – falls notwendig – verringert, um die maximale Losgröße einzuhalten, die Sie für den Artikel festgelegt haben. Wenn darüber hinaus noch ein Bedarf besteht, werden neue Aufträge berechnet, um diesen zu erfüllen. Sie verwenden Sie dieses Feld im Allgemeinen mit der Produktionsart „Lagerfertigung“.  

## <a name="demand-at-blank-location"></a>Bedarf an "leerer Lagerort"  
Selbst bei markiertem Feld **Lagerort notwendig** erlaubt das System die Erstellung von Bedarfszeilen ohne Lagerortcode – auch als Lagerort *LEER* bezeichnet. Dies stellt für das System eine Abweichung dar, weil mehrere Konfigurationswerte für die Behandlung von Lagerorten optimiert sind, und im Ergebnis erstellt das Planungsmodul für eine solche Bedarfszeile keine Planungszeile. Wenn das Feld **Lagerort notwendig** nicht markiert ist, jedoch andere Konfigurationswerte für den Lagerort vorhanden sind, wird auch dieser Fall als Abweichung betrachtet, und das Planungssystem reagiert mit der Ausgabe der "Minimalalternative":   
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.  

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

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.  

#### <a name="case-14-demand-is-at--blank-location"></a>Fall 1.4: Es besteht Bedarf am Lagerort *LEER*  

Der Artikel wird nicht geplant, weil kein Lagerort in der Bedarfszeile definiert ist.  

### <a name="setup-2"></a>Konfiguration 2:  

-   Lagerort notwendig = *Ja*  
-   Es sind keine Lagerhaltungsdaten vorhanden.  
-   Komponente an Lagerort =  *BLAU*  

#### <a name="case-21-demand-is-at--red-location"></a>Fall 2.1: Es besteht Bedarf am Lagerort  *ROT*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.  

#### <a name="case-22-demand-is-at--blue-location"></a>Fall 2.2: Es besteht Bedarf am Lagerort *BLAU*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

### <a name="setup-3"></a>Konfiguration 3:  

-   Lagerort notwendig = *Nein*  
-   Es sind keine Lagerhaltungsdaten vorhanden.  
-   Komponente an Lagerort =  *BLAU*  

#### <a name="case-31-demand-is-at--red-location"></a>Fall 3.1: Es besteht Bedarf am Lagerort  *ROT*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.  

#### <a name="case-32-demand-is-at--blue-location"></a>Fall 3.2: Es besteht Bedarf am Lagerort *BLAU*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

#### <a name="case-33-demand-is-at--blank-location"></a>Fall 3.3: Es besteht Bedarf am Lagerort  *LEER*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.  

### <a name="setup-4"></a>Konfiguration 4:  

-   Lagerort notwendig = *Nein*  
-   Es sind keine Lagerhaltungsdaten vorhanden.  
-   Komponente an Lagerort =  *LEER*  

#### <a name="case-41-demand-is-at--blue-location"></a>Fall 4.1: Es besteht Bedarf am Lagerort  *BLAU*  

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren =  *Los-für-Los* ( *Bestellung* bleibt  *Bestellung*), Lagerbestand berücksichtigen =  *Ja*, alle anderen Planungsparameter = Leer.  

#### <a name="case-42-demand-is-at--blank-location"></a>Fall 4.2: Es besteht Bedarf am Lagerort  *LEER*  

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

Wie aus dem letzten Szenario ersehen werden kann, besteht die einzige Möglichkeit, ein richtiges Ergebnis für eine Bedarfszeile ohne Lagerortcode zu erhalten, im Deaktivieren aller konfigurierten Werte, die sich auf Lagerorte beziehen. Analog besteht die einzige Möglichkeit, stabile Planungsergebnisse für den Bedarf an den Lagerorten zu erhalten, in der Verwendung von Lagerhaltungsdaten.  

Wenn Sie oft den Bedarf an Lagerorten planen, wird daher empfohlen, dass Sie die Funktion „Lagerhaltungsdaten“ verwenden.  

## <a name="see-also"></a>Weitere Informationen

[Planung](production-planning.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerhaltungsdaten einrichten](inventory-how-to-set-up-stockkeeping-units.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Entwurfsdetails: Vorratsplanung](design-details-supply-planning.md)  
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]