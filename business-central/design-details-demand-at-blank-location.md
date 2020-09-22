---
title: 'Designdetails: Bedarf und Vorrat | Microsoft Docs'
description: Dieses Thema erläutert das Konzept der Nachfrage, welches der allgemeine Begriff ist für jede Art Brutto-Bedarf, wie beispielsweise für Verkaufsauftrags und Komponentenbedarf aus einem Fertigungsauftrag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a14f3da6a919f4e5a8066a4205ceb71f2dcee505
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788021"
---
# <a name="design-details-demand-at-blank-location"></a>Designdetails: Bedarf an leerem Lagerort
Wenn ein Benutzer ein Bedarfsereignis erstellt, wie eine Verkaufsauftragszeile, erlaubt es das Programm dem Benutzer, manchmal einen Lagerortcode anzugeben und andere Male nicht, das heißt, es muss ein leerer Lagerort verwendet werden.

In der Bedarfsplanung mit oder ohne Lagerortcodes arbeitet das Planungssystem unter diesen Voraussetzungen in geradliniger Weise:

- Bedarfszeilen enthalten immer Lagerortcodes, und das System verwendet in vollem Umfang Lagermengeneinheiten, einschließlich der betreffenden Lagerorteinrichtung.
- Bedarfszeilen enthalten nie Lagerortcodes, und das System verwendet keine Lagermengeneinheiten oder irgendeine Lagerorteinrichtung (siehe letztes Szenario im folgenden Abschnitt).

Wenn jedoch Bedarfsereignisse manchmal Lagerortcodes aufweisen und manchmal nicht, folgt das Planungssystem je nach Einrichtung bestimmten Regeln.

## <a name="demand-at-location"></a>Bedarf am Lagerort
Wenn das Planungssystem Bedarf an einem Lagerort erkennt, verhält es sich in unterschiedlicher Weise, abhängig von drei kritischen Einrichtungswerten. Während eines Planungslaufs führt das System der Reihe nach eine Überprüfung auf drei Konfigurationswerte durch und plant entsprechend.

1. Ist das Feld **Lagerort notwendig** mit einem Häkchen markiert?

    Falls ja:

2. Sind Lagerhaltungsdaten für den Artikel vorhanden?

    Falls ja:

    Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.

    Falls nein:

3. Enthält das Feld Komponenten von Lagerort den angeforderen Lagerortcode?

  Falls ja:

  Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.

  Falls nein:

  Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los, Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer, Artikel mit dem Wiederbeschaffungsverfahren = Bestellung verwendet weiterhin Auftrag zusammen mit den anderen Einstellungen.

> [!NOTE]
> Die Ausnahmeplanungseinrichtung, die als letzte Reaktion in Schritt 3 ausgegeben wird, wird nachfolgend als „minimale Alternative“ bezeichnet. Diese Planungseinrichtung deckt nur den exakten Bedarf ab, und alle anderen Planungsparameter werden ignoriert.

Informationen zu Variationen dieser Planungslogik finden Sie unten im Szenarienabschnitt.

## <a name="demand-at-blank-location"></a>Bedarf unter „Leerer Lagerort“
Selbst bei ausgewähltem Feld **Lagerort notwendig** erlaubt das System die Erstellung von Bedarfszeilen ohne Lagerortcode, auch als „Leerer Lagerort“ bezeichnet. Dies stellt für das System eine Abweichung dar, weil mehrere Konfigurationswerte für die Behandlung von Lagerorten optimiert sind, und im Ergebnis erstellt das Planungsmodul für eine solche Bedarfszeile keine Planungszeile.

Wenn das Feld **Lagerort notwendig** nicht aktiviert ist, jedoch einer der Standortsetupwerte vorhanden ist, gilt dies auch als eine Abweichung, und das Planungssystem reagiert, indem es die „Minimale Alternative“ verwendet: Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

## <a name="scenarios"></a>Szenarien
Die folgenden Szenarien beschreiben Variationen des Bedarfs am leeren Lagerort und wie das Planungssystem zur „minimale Alternative“ aufgelöst wird.

### <a name="setup-1"></a>Konfiguration 1:
Lagerort notwendig = Ja

Lagerhaltungsdaten sind für ROT eingerichtet

Komponenten in Lagerort = BLAU

#### <a name="case-11-demand-is-at-red-location"></a>Fall 1.1: Es besteht Bedarf am Lagerort ROT
Der Artikel wird gemäß den Planungsparametern auf der Lagerhaltungsdatenkarte geplant.

#### <a name="case-12-demand-is-at-blue-location"></a>Fall 1.2: Es besteht Bedarf am Lagerort BLAU
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

#### <a name="case-13-demand-is-at-green-location"></a>Fall 1.3: Es besteht Bedarf am Lagerort GRÜN
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

#### <a name="case-14-demand-is-at-blank-location"></a>Fall 1.4: Es besteht Bedarf am Lagerort LEER
Der Artikel wird nicht geplant, weil kein Lagerort in der Bedarfszeile definiert ist.

### <a name="setup-2"></a>Konfiguration 2:
Lagerort notwendig = Ja

Es sind keine Lagerhaltungsdaten vorhanden.

Komponenten in Lagerort = BLAU

#### <a name="case-21-demand-is-at-red-location"></a>Fall 2.1: Es besteht Bedarf am Lagerort ROT
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

#### <a name="case-22-demand-is-at-blue-location"></a>Fall 2.2: Es besteht Bedarf am Lagerort BLAU
Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.

### <a name="setup-3"></a>Konfiguration 3:
Lagerort notwendig = Nein

Es sind keine Lagerhaltungsdaten vorhanden.

Komponenten in Lagerort = BLAU

#### <a name="case-31-demand-is-at-red-location"></a>Fall 3.1: Es besteht Bedarf am Lagerort ROT
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

#### <a name="case-32-demand-is-at-blue-location"></a>Fall 3.2: Es besteht Bedarf am Lagerort BLAU
Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.

#### <a name="case-33-demand-is-at-blank-location"></a>Fall 3.3: Es besteht Bedarf am Lagerort LEER
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

### <a name="setup-4"></a>Konfiguration 4:
Lagerort notwendig = Nein

Es sind keine Lagerhaltungsdaten vorhanden.

Komponente an Lagerort = LEER

#### <a name="case-41-demand-is-at-blue-location"></a>Fall 4.1: Es besteht Bedarf am Lagerort BLAU
Der Artikel wird anhand dieser Kriterien geplant: Wiederbeschaffungsverfahren = Los-für-Los (Auftrag bleibt Auftrag), Lagerbestand berücksichtigen = Ja, alle anderen Planungsparameter = Leer.

#### <a name="case-42-demand-is-at-blank-location"></a>Fall 4.2: Es besteht Bedarf am Lagerort LEER
Der Artikel wird gemäß den Planungsparametern auf der Artikelkarte geplant.

Wie aus dem letzten Szenario ersehen werden kann, besteht die einzige Möglichkeit, ein richtiges Ergebnis für eine Bedarfszeile ohne Lagerortcode zu erhalten, im Deaktivieren aller Einrichtungswerte, die sich auf Lagerorte beziehen. Analog besteht die einzige Möglichkeit, stabile Planungsergebnisse für den Bedarf an den Lagerorten zu erhalten, in der Verwendung von Lagerhaltungsdaten. Wenn Unternehmen häufig den Bedarf an Lagerorten planen müssen, empfiehlt sich daher dringend die Verwendung des Moduls Lagerhaltungsdaten.

## <a name="see-also"></a>Siehe auch  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)   
[Designdetails: Vorratsplanung](design-details-supply-planning.md)
