---
title: Einführung in die Demodaten für Contoso Coffee
description: 'Übersicht über Szenarien dazu, wie Sie mithilfe von Contoso Coffee-Demodaten die Verwendung von Produktionsfunktionen in Business Central erlernen können.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Einführung in die Demodaten für Contoso Coffee

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

Die Fertigungsaktivitäten für alle Szenarien verwenden den Standort *NORD*.  

> [!IMPORTANT]
> Bevor Sie eines der Szenarien für Contoso Coffee ausführen, buchen Sie alle Buchungsblattzeilen mit Anfangssalden. Weitere Anforderungen finden Sie im Abschnitt [Contoso Coffee-Daten einrichten](#set-up-contoso-coffee-data).

## Demodaten für Contoso Coffee einrichten

Um die Demodaten von Contoso Coffee nutzen zu können, müssen Sie zwei Apps im jeweiligen Unternehmen in [!INCLUDE [prod_short](../includes/prod_short.md)] installieren:  

- **Demo-Dataset für Contoso Coffee**  

    Diese App stellt Demodaten für die Basisanwendung bereit.  
- **Demo-Dataset für Contoso Coffee (Länderkennung)**  

    Diese App fügt länderspezifische Inhalte zusätzlich zur Basisanwendung hinzu.

Fügen Sie die Apps einem leeren Unternehmen in einem kostenpflichtigen Abonnement oder als Teil einer Testversion hinzu. Erstellen Sie beispielsweise ein neues Unternehmen ohne Beispieldaten über das unterstützte Setup **Neues Unternehmen erstellen**, das Sie über die Liste **Unternehmen** öffnen können. Fügen Sie dann die Apps über den [Marktplatz](../ui-extensions-install-uninstall.md#install) hinzu, wenn sie nicht bereits auf der Seite **Erweiterungsverwaltung** aufgelistet sind.  

Sobald die relevanten Apps installiert sind, wechseln Sie zur Seite [Contoso Coffee-Demodaten](https://businesscentral.dynamics.com/?page=4760) in [!INCLUDE [prod_short](../includes/prod_short.md)], und ändern Sie die Standardeinstellungen entsprechend Ihren Anforderungen. Die Einstellungen werden in den folgenden Tabellen beschrieben:  

|Feld  |Beschreibung  |
|---------|---------|
|**Anfangsjahr** |Gibt das erste Jahr an, das Sie für die Contoso Coffee-Demonstrationsdaten verwenden möchten. Je nach Unternehmenseinrichtung ist das Jahr entweder ein Kalenderjahr oder ein Geschäftsjahr.|
|**Produktionsstandort** |Gibt das Lager an, das Sie für Produktionsvorgänge verwenden möchten. Der Standardwert ist *NORD*, Sie können ihn jedoch an Ihre Bedürfnisse anpassen.|
|**Unternehmenstyp**    |Gibt an, ob das aktuelle Unternehmen Mehrwertsteuer oder Verkaufssteuer melden muss. |
|**Inland – Allgemeine Geschäftsbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren und Kreditoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Kapazität – Produktbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die zum Buchen von Kapazität verwendet werden müssen.|
|**Einzelhandel – Produktbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die für Einzelhandelsbuchungen verwendet werden müssen.|
|**Rohmaterial – Produktbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die zum Buchen von Rohmaterial verwendet werden müssen. |
|**Basis-MwSt.-Code**    |Gibt eine bestehende MwSt.-Produktgruppe an, die für Artikel verwendet werden soll.|
|**Fertiger Code**    |Gibt eine bestehende MwSt.-Produktgruppe an, die für fertige Artikel verwendet werden soll.|
|**Preisfaktor**     |Gibt einen Faktor an, um einen Preis von USD/EUR in die lokale Währung umzurechnen. *1* bedeutet, dass der Preis in jeder Währung gleich ist. Eine höhere Zahl wird verwendet, um den Preis in der Landeswährung zu erhalten. |
|**Rundungspräzision**  |Definiert, wie berechnete Verbrauchsmengen gerundet werden, wenn sie in FA-Verbrauchs Buch.-Blattzeilen eingegeben werden. Mengen kleiner als 0,5 werden abgerundet. Mengen gleich oder größer 0,5 werden aufgerundet.|

Wenn Sie fertig sind, wählen Sie die Aktion **Demodaten erstellen** aus. Es dauert einige Minuten, der zugrunde liegenden Datenbank die Daten hinzuzufügen, anschließend können Sie die verschiedenen Szenarien jedoch ausführen.  

## Szenarien

Die Demodaten von Contoso Coffee unterstützen derzeit die folgenden Szenarien für Tests und Schulungen:

1. [Neue Versionen von Fertigungsstücklisten und Stücklisten erstellen](create-new-production-bom-version.md)  
2. [Neuen Arbeitsplan erstellen](create-new-routing.md)  
3. [Neuen fest geplanten Fertigungsauftrag erstellen und ändern](create-firm-planned-production-order-change.md)  
4. [Automatisches und manuelles Buchen kombinieren](combine-automatic-manual-flushing.md)  
5. [Auftragsplanung zum Erstellen und Reservieren von Lieferungen verwenden](order-planning-create-reserve-supply.md)  
6. [Fremdarbeitsvorgang einrichten und verarbeiten](set-up-process-subcontracting-operation.md)  
7. [Neue Kapazität einrichten](set-up-new-capacity.md)  
8. [Bedarf für Artikelvarianten mit verschiedenen zugewiesenen Stücklisten prognostizieren](variants.md)  

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.  

> [!IMPORTANT]
> Diese exemplarischen Vorgehensweisen erfordern, dass die Benutzererfahrung auf der Seite **Unternehmensdaten** auf *Premium* festgelegt ist.

## Siehe auch

[Produktion](../production-manage-manufacturing.md)  
[Produktionsberichte und Analysen in Business Central](../production-reports.md)  
