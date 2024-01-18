---
title: Einführung in Contoso Coffee Produktion
description: 'Übersicht über Szenarien dazu, wie Sie mithilfe von Contoso Coffee-Demodaten die Verwendung von Produktionsfunktionen in Business Central erlernen können.'
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a>Einführung in Contoso Coffee Produktion

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für Business Central fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Produktionsfunktionen in Business Central erlernen können.  

Die App bietet vier Produkte, die für unterschiedliche Szenarien optimiert sind:

- **SP-SCM1009 Airpot**  

  Dieses Produkt ist eine Stückliste (BOM) mit einer Unterkomponente, **Arbeitsplan**. Verwenden Sie es, um den Standardproduktionsfluss zu demonstrieren. Er wird mit alternativen Arbeitsplänen eingerichtet, mit denen Sie verschiedene Szenarien demonstrieren können, an denen Subunternehmer beteiligt sind. Die Kostenmethode ist *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Dieses Produkt erfordert eine Artikelverfolgung und verfügt über eine Komponente, die ebenfalls eine Artikelverfolgung voraussetzt. Die Methode der Kalkulation ist *Spezifisch*.  

- **SP-SCM1004 Autodrip**  

  Dieses Produkt ist eine Stückliste mit einer Unterkomponente, **Arbeitsplan**. Wir empfehlen es, um die verschiedenen Buchungsmethoden für Komponenten und für den Betrieb zu demonstrieren. Die Kostenmethode ist *Standard*.

- **SP-SCM1006 AutoDripLite**

  Dieses Produkt hat drei Varianten und drei Stücklisten, die Lagerhaltungsdaten zugeordnet werden können. Das Produkt verwendet das Konzept der Phantomstückliste. Die Kostenmethode ist *Standard*.

Die Fertigungsaktivitäten für alle Szenarien verwenden den Standort *MAIN*.  

> [!IMPORTANT]
> Bevor Sie eines der Szenarien für Contoso Coffee ausführen, buchen Sie alle Buchungsblattzeilen mit Anfangssalden. Weitere Anforderungen finden Sie im Abschnitt [Contoso Coffee-Daten einrichten](#set-up-contoso-coffee-manufacturing-data).

## <a name="set-up-contoso-coffee-manufacturing-data"></a>Contoso Coffee-Produktionsdaten

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Feld  |Description  |
|---------|---------|
|**Produktionsstandort** |Gibt das Lager an, das Sie für Produktionsvorgänge verwenden möchten. Der Standardwert ist *MAIN*, Sie können ihn jedoch an Ihre Bedürfnisse anpassen.|


Wenn Sie fertig sind, wählen Sie die Aktion **Demodaten erstellen** aus. Es dauert einige Minuten, der zugrunde liegenden Datenbank die Daten hinzuzufügen, anschließend können Sie die verschiedenen Szenarien jedoch ausführen.  

## <a name="scenarios"></a>Szenarien

Die Produktions-Demodaten von Contoso Coffee unterstützen derzeit die folgenden Szenarien für Tests und Schulungen:

1. [Neue Versionen von Fertigungsstücklisten und Stücklisten erstellen](create-new-production-bom-version.md)  
2. [Neuen Arbeitsplan erstellen](create-new-routing.md)  
3. [Erstellen und Ändern fest geplanter Fertigungsaufträge](create-firm-planned-production-order-change.md)  
4. [Automatisches und manuelles Buchen kombinieren](combine-automatic-manual-flushing.md)  
5. [Auftragsplanung zum Erstellen und Reservieren von Lieferungen verwenden](order-planning-create-reserve-supply.md)  
6. [Fremdarbeitsvorgang einrichten und verarbeiten](set-up-process-subcontracting-operation.md)  
7. [Neue Kapazität einrichten](set-up-new-capacity.md)  
8. [Bedarf für Artikelvarianten mit verschiedenen zugewiesenen Stücklisten prognostizieren](variants.md)  

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.  

> [!IMPORTANT]
> Diese exemplarischen Vorgehensweisen erfordern, dass die Benutzererfahrung auf der Seite **Unternehmensdaten** auf *Premium* festgelegt ist.

## <a name="see-also"></a>Siehe auch

[Produktion](../../production-manage-manufacturing.md)  
[Produktionsberichte und Analysen in Business Central](../../production-reports.md)  
