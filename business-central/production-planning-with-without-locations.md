---
title: Siehe Planung mit/ohne Lagerortcodes.
description: 'In diesem Thema lernen Sie die Produktion und Fertigung, einschließlich der Vorratsplanung, in Business Central kennen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: edupont
---
# <a name="planning-with-or-without-locations"></a><a name="planning-with-or-without-locations"></a>Siehe Planung mit/ohne Lagerortcodes.

Bevor Sie mit der Verwendung des Planungsmoduls beginnen, empfehlen wir Ihnen zu entscheiden, ob Sie Standorte verwenden möchten oder nicht. Es gibt zwei einfache Hauptwege:

* Die Bedarfszeilen enthalten immer Lagerortcodes, und das System verwendet in vollem Umfang Lagerhaltungsdaten, einschließlich der betreffenden Lagerorteinrichtung. Erfahren Sie mehr unter [Nachfrage vor Ort](#demand-at-location).  
* Bedarfszeilen enthalten niemals Standortcodes und das System verwendet die Artikelkarte. Informationen dazu sehen Sie im Szenario [Nachfrage an einem "leeren Ort"](#demand-at-blank-location) unten.

## <a name="demand-at-location"></a><a name="demand-at-location"></a>Bedarf am Lagerort

Wenn das Planungssystem Bedarf an einem Lagerort (eine Zeile mit einem Lagerortcode) erkennt, verhält es sich in verschiedener Weise, abhängig von zwei kritischen Konfigurationswerten.  

Während eines Planungslaufs führt das System der Reihe nach eine Überprüfung auf zwei Konfigurationswerte durch und plant entsprechend:  

1. Existiert eine SKU für den Artikel am gewünschten Standort?  

    Falls ja:  

    Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.  

    Falls nein:  

2. Enthält das Feld **Komponenten von Lagerort** auf der Seite **Produktion Einrichtung** den gewünschten Lagerortcode?  

    Falls ja:  

    Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

    Falls nein:  

    Der Artikel wird nach der „minimalen Alternative“ geplant, die den exakten Bedarf deckt. Die Planungsparameter werden wie folgt festgelegt: Wiederbeschaffungsverfahren = *Los-für-Los*, Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer. (Artikel mit dem Wiederbeschaffungsverfahren *Bestellung* verbleiben auf *Bestellung* sowie auf allen anderen für sie festgelegten Einstellungen.)

> [!TIP]
> Wenn Sie oft den Bedarf an verschiedenen Lagerorten planen, wird empfohlen, dass Sie die Funktion „Lagerhaltungsdaten“ verwenden und die Nachfrage an leeren Standorten vermeiden. Erfahren Sie mehr unter [Lagerhaltungsdaten einrichten](inventory-how-to-set-up-stockkeeping-units.md).

Siehe Abweichungen in den [unten angeführten Szenarien](#scenarios).

> [!NOTE]
> Das Feld **Komponenten am Lagerort** auf der Seite **Produktion Einrichtung** ist unerlässlich für die Art der Verarbeitung von Bedarfszeilen durch das Produktionsplanungssystem.
>
> Hinsichtlich des Fertigungsbedarfs verwendet [!INCLUDE [prod_short](includes/prod_short.md)] für Komponenten den Lagerort für Unterkomponenten und Komponenten, der im Fertigungsauftrag angegeben ist. Wenn Sie aber dieses Feld ausfüllen, können Sie die Unterkomponente und Komponenten an einen anderen Lagerort umleiten.
>
> Sie können dies auch für bestimmte Lagerhaltungsdaten festlegen, indem Sie einen anderen Lagerortcode im Feld **Komponenten von Lagerort** auf der Lagerhaltungsdatenkarte auswählen. Beachten Sie jedoch, dass dies selten sinnvoll ist, da die Planungslogik möglicherweise beim Planen für die Lagerhaltungsdaten-Komponente verfälscht wird.

## <a name="demand-at-blank-location"></a><a name="demand-at-blank-location"></a>Nachfrage am „leeren Lagerort“

Wenn das Planungssystem Bedarf an einem leeren Standort (einer Zeile ohne Standortcode) erkennt, wird der Artikel im Allgemeinen gemäß den Planungsparametern auf der Artikelkarte geplant.

Das Feld **Lagerort notwendig** auf der Seite **Lagerort Einrichtung** und das Feld **Komponenten von Lagerort** auf der Seite **Produktion Einrichtung** oder die Lagerhaltungseinheiten sind sehr wichtig, um zu steuern, wie das Planungssystem Bedarfspositionen mit/ohne Lagerortcodes verarbeitet. Wenn eine der folgenden Anweisungen wahr ist, wird der Bedarf am leeren Lagerort als Abweichung gewertet, und das Planungssystem reagiert, indem es die „Minimale Alternative“ ausgibt: Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* (*Auftrag* bleibt *Auftrag*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

* Auf der Seite **Produktion Einrichtung** hat das Feld **Komponenten von Lagerort** einen Wert.
* Eine Lagerhaltungseinheit ist für den geplannten Artikel vorhanden.
* Das **Lagerort Obligatorisch** Feld ist ausgewählt.

## <a name="scenarios"></a><a name="scenarios"></a>Szenarien

Siehe Abweichungen in den unten angeführte Setup-Szenarien.

### <a name="setup-1"></a><a name="setup-1"></a>Konfiguration 1

* Lagerort notwendig = *Ja*  
* SKU ist für *WEST* eingerichtet  
* Komponente an Lagerort =  *EAST*  

#### <a name="case-11-demand-is-at-west-location"></a><a name="case-11-demand-is-at-west-location"></a>Fall 1.1: Es besteht Bedarf am Lagerort *WEST*

Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant (einschließlich möglicher Umlagerungen).

#### <a name="case-12-demand-is-at-east-location"></a><a name="case-12-demand-is-at-east-location"></a>Fall 1.2: Es besteht Bedarf am Lagerort *EAST*

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.

#### <a name="case-13-demand-is-at-north-location"></a><a name="case-13-demand-is-at-north-location"></a>Fall 1.3: Es besteht Bedarf am Lagerort *NORTH*

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

#### <a name="case-14-demand-is-at-blank-location"></a><a name="case-14-demand-is-at-blank-location"></a>Fall 1.4: Es besteht Bedarf am Lagerort *LEER*

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

### <a name="setup-2"></a><a name="setup-2"></a>Konfiguration 2

* Lagerort notwendig = *Ja*  
* Es sind keine Lagerhaltungsdaten vorhanden.  
* Komponente an Lagerort =  *EAST*  

#### <a name="case-21-demand-is-at-west-location"></a><a name="case-21-demand-is-at-west-location"></a>Fall 2.1: Es besteht Bedarf am Lagerort *WEST*

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

#### <a name="case-22-demand-is-at-east-location"></a><a name="case-22-demand-is-at-east-location"></a>Fall 2.2: Es besteht Bedarf am Lagerort *EAST*

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

### <a name="setup-3"></a><a name="setup-3"></a>Konfiguration 3

* Lagerort notwendig = *Nein*  
* Es sind keine Lagerhaltungsdaten vorhanden.  
* Komponente an Lagerort =  *EAST*  

#### <a name="case-31-demand-is-at-west-location"></a><a name="case-31-demand-is-at-west-location"></a>Fall 3.1: Es besteht Bedarf am Lagerort *WEST*

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

#### <a name="case-32-demand-is-at-east-location"></a><a name="case-32-demand-is-at-east-location"></a>Fall 3.2: Es besteht Bedarf am Lagerort *EAST*

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.  

#### <a name="case-33-demand-is-at-blank-location"></a><a name="case-33-demand-is-at-blank-location"></a>Fall 3.3: Es besteht Bedarf am Lagerort *LEER*

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

### <a name="setup-4"></a><a name="setup-4"></a>Konfiguration 4

* Lagerort notwendig = *Nein*  
* Es sind keine Lagerhaltungsdaten vorhanden.  
* Komponente an Lagerort =  *LEER*  

#### <a name="case-41-demand-is-at-east-location"></a><a name="case-41-demand-is-at-east-location"></a>Fall 4.1: Es besteht Bedarf am Lagerort *EAST*

Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = *Los-für-Los* ( *Bestellung* bleibt *Bestellung*), Lagerbestand berücksichtigen = *Ja*, alle anderen Planungsparameter = Leer.

#### <a name="case-42-demand-is-at-blank-location"></a><a name="case-42-demand-is-at-blank-location"></a>Fall 4.2: Es besteht Bedarf am Lagerort *LEER*

Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.

Wie aus dem letzten Szenario ersehen werden kann, besteht die einzige Möglichkeit, ein richtiges Ergebnis für eine Bedarfszeile ohne Lagerortcode zu erhalten, im Deaktivieren aller konfigurierten Werte, die sich auf Lagerorte beziehen. Analog besteht die einzige Möglichkeit, stabile Planungsergebnisse für den Bedarf an den Lagerorten zu erhalten, in der Verwendung von Lagerhaltungsdaten.  

Wenn Sie oft den Bedarf an Lagerorten planen, wird daher empfohlen, dass Sie die Funktion „Lagerhaltungsdaten“ verwenden.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/training/paths/trade-get-started-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

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
