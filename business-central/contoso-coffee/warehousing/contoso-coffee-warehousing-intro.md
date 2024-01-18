---
title: Einführung in Contoso Coffee
description: 'Übersicht über Szenarien dazu, wie Sie mithilfe von Contoso Coffee-Demodaten die Verwendung von Lagerfunktionen in Business Central erlernen können.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Einführung in Contoso Coffee Lager

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für Business Central fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Lagerfunktionen in Business Central erlernen können. Sie können Lagerfunktionen auf verschiedene Arten konfigurieren, siehe [Übersicht über verschiedene Konfigurationsmöglichkeiten](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Die App bietet drei Standorte, die für unterschiedliche Szenarien optimiert sind:

- **SILBER**  

  Dieser Standort ist für die Verwendung von Lagerorten konfiguriert. Er kann einfach konfiguriert werden, um grundlegende oder erweiterte Unterstützung zu bieten. 

- **GELB**  

  Dieser Standort verwendet die erweiterte Lagerkonfiguration, aber keine Lagerplätze. Er kann neu konfiguriert werden, um grundlegende Konfigurationen zu unterstützen.

- **WEISS**  

  Dieser Standort verwendet die erweiterte Lagerkonfiguration mit gerichteten Einlagerungen und Entnahmen, die erweiterte Regeln für die Bewegung von Artikeln im gesamten Lager ermöglicht.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Lagerdaten für Contoso Coffee einrichten

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Sobald die relevanten Apps installiert sind, gehen Sie zur Seite [Contoso-Demo-Tool](https://businesscentral.dynamics.com/?page=5194) in [!INCLUDE [prod_short](../../includes/prod_short.md)], wählen die Zeile *Lagermodul* aus, und verwenden Sie **Konfigurieren**-Aktion zur Vorbereitung der Module. Die Einstellungen werden in den folgenden Tabellen beschrieben:  

|Feld  |Description  |
|---------|---------|
|**Lagerort Lagerplatz**  |Der Lagerort, um die Basis-Standort-Szenarien zu nutzen.|
|**Erweiterter Standort**  |Der Lagerort, um die einfachen Logistik-Szenarien zu nutzen.|
|**Lagerort gesteuerte Kommissionierung und Entnahme**  |Der Lagerort, um die erweiterten Logistik-Szenarien zu nutzen.|
|**Standort in Zustellung**  |Der Standort, der in Umlagerungsszenarien als Unterwegsort verwendet werden soll.|
|**Debitorennr.**  |Der Kunde, der für die grundlegenden und einfachen Szenarien im Vertrieb verwendet werden soll.|
|**Kreditorennr**  |Der Lieferant, der für alle Szenarios in Einkaufsvorgängen verwendet werden soll.|
|**Artikel 1 Nr.**  |Gibt den Hauptartikel an, der für alle Szenarien verwendet wird.|
|**Artikel 2 Nr.**  |Gibt den Zusatzartikel an, der für alle Szenarien verwendet wird.|
|**Artikel 3 Nr.**  |Der Artikel mit Verfolgung.|

Wenn Sie fertig sind, wählen Sie die Aktion **Demodaten erstellen** aus. Es dauert einige Minuten, der zugrunde liegenden Datenbank die Daten hinzuzufügen, anschließend können Sie die verschiedenen Szenarien jedoch ausführen.  

> [!IMPORTANT]
> Wenn Sie die Szenarien ausführen, möchten Sie möglicherweise überprüfen, ob Ihr Benutzer wie für ausgewählte Standorte hinzugefügt wurde. Weitere Informationen finden Sie unter [Lagermitarbeiter einrichten](../../warehouse-how-to-set-up-warehouse-employees.md)

## <a name="scenarios"></a>Szenarien

Die Lager-Demodaten von Contoso Coffee unterstützen derzeit die folgenden Lagerort-Szenarien für Tests und Schulungen:

1.  [Exemplarische Vorgehensweise für ein- und ausgehende Flows in Basis-Lagerkonfigurationen](warehouse-basic-flow-putaway-pick.md)
2.  [Exemplarische Vorgehensweise: Eingehende und ausgehende Abläufe in gemischten Lagerkonfigurationen](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Exemplarische Vorgehensweise des eingehenden und ausgehenden Flows in der erweiterten Lagerkonfiguration mit gesteuerter Einlagerung und Kommissionierung](warehouse-directed-flow.md)

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.  

## <a name="see-also"></a>Siehe auch

[Lager einrichten](../../inventory-setup-inventory.md) 
[So richten Sie Standorte ein](../../inventory-how-setup-locations.md) 
[Lagerung](../../warehouse-manage-warehouse.md) 
[Designdetails](../../design-details-warehouse-overview.md) 
