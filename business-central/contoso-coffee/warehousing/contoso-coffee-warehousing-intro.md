---
title: Einführung in Contoso Coffee
description: 'Übersicht über Szenarien dazu, wie Sie mithilfe von Contoso Coffee-Demodaten die Verwendung von Lagerfunktionen in Business Central erlernen können.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing"></a><a name="introduction-to-contoso-coffee-warehousing"></a>Einführung in Contoso Coffee Lager

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für Business Central fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Lagerfunktionen in Business Central erlernen können. Sie können Lagerfunktionen auf verschiedene Arten konfigurieren, siehe [Übersicht über verschiedene Konfigurationsmöglichkeiten](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Die App bietet drei Standorte, die für unterschiedliche Szenarien optimiert sind:

- **SILBER**  

  Dieser Standort ist für die Verwendung von Lagerorten konfiguriert. Er kann einfach konfiguriert werden, um grundlegende oder erweiterte Unterstützung zu bieten. 

- **GELB**  

  Dieser Standort verwendet die erweiterte Lagerkonfiguration, aber keine Lagerplätze. Er kann neu konfiguriert werden, um grundlegende Konfigurationen zu unterstützen.

- **WEISS**  

  Dieser Standort verwendet die erweiterte Lagerkonfiguration mit gerichteten Einlagerungen und Entnahmen, die erweiterte Regeln für die Bewegung von Artikeln im gesamten Lager ermöglicht.

## <a name="set-up-contoso-coffee-warehousing-data"></a><a name="set-up-contoso-coffee-warehousing-data"></a>Lagerdaten für Contoso Coffee einrichten

Um die Lagerdaten von Contoso Coffee nutzen zu können, müssen Sie zwei Apps im jeweiligen Unternehmen in [!INCLUDE [prod_short](../../includes/prod_short.md)] installieren:  

- **Demo-Dataset für Contoso Coffee**  

    Diese App stellt Demodaten für die Basisanwendung bereit.  
- **Demo-Dataset für Contoso Coffee (Länderkennung)**  

    Diese App fügt länderspezifische Inhalte zusätzlich zur Basisanwendung hinzu.

Fügen Sie die Apps einem leeren Unternehmen in einem kostenpflichtigen Abonnement oder als Teil einer Testversion hinzu. Erstellen Sie beispielsweise ein neues Unternehmen ohne Beispieldaten über das unterstützte Setup **Neues Unternehmen erstellen**, das Sie über die Liste **Unternehmen** öffnen können. Fügen Sie dann die Apps über den [Marktplatz](../../ui-extensions-install-uninstall.md#install) hinzu, wenn sie nicht bereits auf der Seite **Erweiterungsverwaltung** aufgelistet sind.  

Sobald die relevanten Apps installiert sind, wechseln Sie zur Seite [Contoso Coffee-Whse-Demodaten](https://businesscentral.dynamics.com/?page=4761) in [!INCLUDE [prod_short](../../includes/prod_short.md)], und ändern Sie die Standardeinstellungen entsprechend Ihren Anforderungen. Die Einstellungen werden in den folgenden Tabellen beschrieben:  

|Feld  |Beschreibung  |
|---------|---------|
|**Anfangsjahr** |Gibt das erste Jahr an, das Sie für die Contoso Coffee-Demonstrationsdaten verwenden möchten. Je nach Unternehmenseinrichtung ist das Jahr entweder ein Kalenderjahr oder ein Geschäftsjahr.|
|**Lagerort Lagerplatz**  |Der Lagerort, um die Basis-Standort-Szenarien zu nutzen.|
|**Standort Adv. Logistik**  |Der Lagerort, um die einfachen Logistik-Szenarien zu nutzen.|
|**Lagerort gesteuerte Kommissionierung und Entnahme**  |Der Lagerort, um die erweiterten Logistik-Szenarien zu nutzen.|
|**Standort in Zustellung**  |Der Standort, der in Umlagerungsszenarien als Unterwegsort verwendet werden soll.|
|**Debitorennr.**  |Der Kunde, der für die grundlegenden und einfachen Szenarien im Vertrieb verwendet werden soll.|
|**Kreditorennr**  |Der Lieferant, der für alle Szenarios in Einkaufsvorgängen verwendet werden soll.|
|**Hauptartikelnr.**  |Der Artikel, der für alle Szenarios in Vertriebsvorgängen verwendet werden soll.|
|**Artikel 1 Nr.**  |Gibt den Hauptartikel an, der für alle Szenarien verwendet wird.|
|**Artikel 2 Nr.**  |Gibt den Zusatzartikel an, der für alle Szenarien verwendet wird.|
|**Debitorenbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Debitor Allgemeine Geschäftsbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Kreditorenbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren und Kreditoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Kreditor Allgemeine Geschäftsbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren und Kreditoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Inland – MWST-Geschäftsbuchungsgruppe**|Gibt einen Umsatzsteuer-Geschäftscode für Debitoren und Kreditoren zum Buchen der Umsatzsteuer an, wenn die Umsatzsteuer aktiviert ist.|
|**Wiederverkauf - Lagerbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die für Einzelhandelsbuchungen verwendet werden müssen.|
|**Einzelhandel – Produktbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die für Einzelhandelsbuchungen verwendet werden müssen.|
|**MwSt.-Produktbuchungsgrp.**    |Gibt einen Umsatzsteuer-Produktcode für Artikel zum Buchen der Umsatzsteuer an, wenn die Umsatzsteuer aktiviert ist.|
|**Preisfaktor**     |Gibt einen Faktor an, um einen Preis von USD/EUR in die lokale Währung umzurechnen. *1* bedeutet, dass der Preis in jeder Währung gleich ist. Eine höhere Zahl wird verwendet, um den Preis in der Landeswährung zu erhalten. |
|**Rundungspräzision**  |Definiert, wie berechnete Verbrauchsmengen gerundet werden, wenn sie in FA-Verbrauchs Buch.-Blattzeilen eingegeben werden. Mengen kleiner als 0,5 werden abgerundet. Mengen gleich oder größer 0,5 werden aufgerundet.|

Wenn Sie fertig sind, wählen Sie die Aktion **Demodaten erstellen** aus. Es dauert einige Minuten, der zugrunde liegenden Datenbank die Daten hinzuzufügen, anschließend können Sie die verschiedenen Szenarien jedoch ausführen.  

> [!IMPORTANT]
> Wenn Sie die Szenarien ausführen, möchten Sie möglicherweise überprüfen, ob Ihr Benutzer wie für ausgewählte Standorte hinzugefügt wurde. Weitere Informationen finden Sie unter [Lagermitarbeiter einrichten](../../warehouse-how-to-set-up-warehouse-employees.md)

## <a name="scenarios"></a><a name="scenarios"></a>Szenarien

Die Lager-Demodaten von Contoso Coffee unterstützen derzeit die folgenden Lagerort-Szenarien für Tests und Schulungen:

1.  [Exemplarische Vorgehensweise für ein- und ausgehende Flows in Basis-Lagerkonfigurationen](warehouse-basic-flow-putaway-pick.md)
2.  [Exemplarische Vorgehensweise für ein- und ausgehende Flows in gemischten Lagerkonfigurationen](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Exemplarische Vorgehensweise des eingehenden und ausgehenden Flows in der erweiterten Lagerkonfiguration mit gesteuerter Einlagerung und Kommissionierung](warehouse-directed-flow.md)

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Lager einrichten](../../inventory-setup-inventory.md) 
[So richten Sie Standorte ein](../../inventory-how-setup-locations.md) 
[Lagerung](../../warehouse-manage-warehouse.md) 
[Designdetails](../../design-details-warehouse-overview.md) 
