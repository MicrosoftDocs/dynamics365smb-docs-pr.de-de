---
title: Einführung in Contoso Coffee-Servicemanagement
description: Dieser Artikel stellt Ihnen die Demonstrationsdaten von Consoso Coffee für das Servicemanagement vor.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Einführung in Contoso Coffee-Servicemanagement

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für Business Central fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Servicemanagementfunktionen in Business Central erlernen können.

Diese App bietet mehrere Elemente, die für die wichtigsten exemplarischen Vorgehensweisen verwendet werden:

- Ressourcen mit zugewiesenen Fertigkeiten
- Elemente, die zum Erstellen von Serviceartikeln konfiguriert sind
- Leihgeräte

> [!IMPORTANT]
> Bevor Sie eines der Szenarien für Contoso Coffee ausführen, buchen Sie alle Buchungsblattzeilen mit Anfangssalden. Weitere Anforderungen finden Sie im Abschnitt [Contoso Coffee-Daten einrichten](#set-up-contoso-coffee-service-management-data).
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Einrichten von Contoso Coffee-Servicemanagementdaten

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Sobald die relevanten Apps installiert sind, gehen Sie zur Seite [Contoso-Demo-Tool](https://businesscentral.dynamics.com/?page=5194) in [!INCLUDE [prod_short](../../includes/prod_short.md)], wählen die Zeile *Servicemodul* aus, und verwenden Sie **Konfigurieren**-Aktion zur Vorbereitung der Module. Die Einstellungen werden in den folgenden Tabellen beschrieben:  

|Feld  |Description  |
|---------|---------|
|**Debitorennr.**  |Der Debitor, der für die Szenarios in Vertriebsvorgängen verwendet werden soll.|
|**Kontonr.**  |Der Lieferant, der für alle Szenarios in Einkaufsvorgängen verwendet werden soll.|
|**Artikel 1 Nr.**  |Der Artikel, der für die Reparatur- und Wartungsszenarien verwendet werden soll.|
|**Nr. von Serviceartikel 1**  |Das Element vom Typ „Service“, das für das Reparaturszenario verwendet werden soll.|
|**Nr. von Serviceartikel 2**  |Das Element vom Typ „Service“, das für das Reparaturszenario verwendet werden soll.|
|**Ressourcennr. 1**  |Gibt die Ressource an, die für Vertragsszenarien verwendet wird.|
|**Ressourcennr. 2**  |Gibt die Ressource an, die für Problemlösungsszenarien verwendet wird.|
|**Servicestandort** |Gibt das Lager an, das Sie für Servicevorgänge verwenden möchten. Der Standardwert ist *MAIN*, Sie können ihn jedoch an Ihre Bedürfnisse anpassen.|

Wenn Sie fertig sind, wählen Sie die Aktion **Demodaten erstellen** aus. Es dauert einige Minuten, der zugrunde liegenden Datenbank die Daten hinzuzufügen, anschließend können Sie die verschiedenen Szenarien jedoch ausführen.  

## <a name="scenarios"></a>Szenarien

Die Lager-Demodaten von Contoso Coffee unterstützen derzeit die folgenden Serviceszenarien für Tests und Schulungen:

1. Erstellen Sie einen Serviceauftrag für eine Ad-hoc-Reparaturanfrage, platzieren und empfangen Sie Kreditgeber, registrieren Sie die Zeit und stellen Sie Kunden eine Rechnung mit [Exemplarische Vorgehensweise für Serviceaufträge für Serviceartikel](service-basic-flow-order.md) aus
2. Erstellen Sie Serviceverträge, generieren Sie Serviceaufträge, stellen Sie Vertragsgebühren in Rechnung und weisen Sie Ressourcen mit [Exemplarische Vorgehensweise für Serviceverträge für Serviceartikel](service-contract-flow.md) zu

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.  

> [!IMPORTANT]
> Diese exemplarischen Vorgehensweisen für Services erfordert, dass die Benutzererfahrung auf der Seite **Unternehmensdaten** auf **Premium** festgelegt ist.


## <a name="see-also"></a>Siehe auch

[Dienst](../../service-service.md)
