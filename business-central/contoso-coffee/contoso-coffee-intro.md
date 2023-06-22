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

# <a name="introduction-to-contoso-coffee-demo-data" />Einführung in die Demodaten für Contoso Coffee

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für Business Central fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Produktionsfunktionen in Business Central erlernen können.  


## <a name="set-up-contoso-coffee-data" />Demodaten für Contoso Coffee einrichten

Um die Demodaten von Contoso Coffee nutzen zu können, müssen Sie zwei Apps im jeweiligen Unternehmen in [!INCLUDE [prod_short](../includes/prod_short.md)] installieren:  

- **Demo-Dataset für Contoso Coffee**  

    Diese App stellt Demodaten für die Basisanwendung bereit.  
- **Demo-Dataset für Contoso Coffee (Länderkennung)**  

    Diese App fügt länderspezifische Inhalte zusätzlich zur Basisanwendung hinzu.

Fügen Sie die Apps einem leeren Unternehmen in einem kostenpflichtigen Abonnement oder als Teil einer Testversion hinzu. Erstellen Sie beispielsweise ein neues Unternehmen ohne Beispieldaten über das unterstützte Setup **Neues Unternehmen erstellen**, das Sie über die Liste **Unternehmen** öffnen können. Fügen Sie dann die Apps über den [Marktplatz](../ui-extensions-install-uninstall.md#install) hinzu, wenn sie nicht bereits auf der Seite **Erweiterungsverwaltung** aufgelistet sind.  

Sie sollten dann Folgendes vervollständigen:
 - Die [Fertigungseinrichtung](manufacturing/contoso-coffee-manufacturing-intro.md) zur Vorbereitung auf die Verwendung der [Fertigungsszenarien](#manufacturing-scenarios)
 - Die [Lagerorteinrichtung](warehousing/contoso-coffee-warehousing-intro.md) zur Vorbereitung auf die Verwendung der [Lagerortszenarien](#warehousing-scenarios)

## <a name="manufacturing-scenarios" />Produktionsszenarien

Die Produktions-Demodaten von Contoso Coffee unterstützen derzeit die folgenden Produktionsszenarien für Tests und Schulungen:

1. [Eine neue Produktionsstücklisten- und Stücklistenversion erstellen](manufacturing/create-new-production-bom-version.md)  
2. [Neuen Arbeitsplan erstellen](manufacturing/create-new-routing.md)  
3. [Neuen fest geplanten Produktionsauftrag erstellen und ändern](manufacturing/create-firm-planned-production-order-change.md)  
4. [Automatisches und manuelles Buchen kombinieren](manufacturing/combine-automatic-manual-flushing.md)  
5. [Auftragsplanung zum Erstellen und Reservieren von Lieferungen verwenden](manufacturing/order-planning-create-reserve-supply.md)  
6. [Fremdarbeitsvorgang einrichten und verarbeiten](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Neue Kapazität einrichten](manufacturing/set-up-new-capacity.md)  
8. [Bedarf für Artikelvarianten mit verschiedenen zugewiesenen Stücklisten prognostizieren](manufacturing/variants.md)  

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.  

> [!IMPORTANT]
> Diese exemplarischen Vorgehensweisen für die Produktion erfordert, dass die Benutzererfahrung auf der Seite **Unternehmensdaten** auf *Premium* festgelegt ist.

## <a name="warehousing-scenarios" />Lagerszenarien

Die Demodaten von Contoso Coffee unterstützen derzeit die folgenden Lagerort-Szenarien für Tests und Schulungen:

1.  Konfigurieren Sie Standardlagerplätze, Empfangen und Einlagern mit Bestandseinlagerung, Kommissionieren und Versenden mit Bestandskommissionierung in auftragsweiser Weise mit [Exemplarische Vorgehensweise des eingehenden und ausgehenden Flows in grundlegenden Lagerortkonfigurationen.](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Empfangen und lagern Sie mehrere eingehende Bestellungen gleichzeitig mit Lagereingang, versenden Sie mehrere Bestellungen gleichzeitig mit Lagerversand, kommissionieren Sie mit Lagerentnahmen mit [Durchführung des ein- und ausgehenden Flows in gemischten Lagerkonfigurationen](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Konfigurieren Sie feste Lagerplätze für Artikelmengeneinheiten, Benutzer-Cross-Docking, um physische Warenbewegungen zu reduzieren, optimieren Sie die Warenplatzierung mit Behälterauffüllung, teilen Sie große Mengeneinheiten in kleinere auf, verteilen Sie die Kommissionierung auf Lagermitarbeiter mit Kommissionierarbeitsblatt mit [Durchführung des ein- und ausgehenden Flusses in der erweiterten Lagerkonfiguration mit gesteuerter Einlagerung und Kommissionierung](warehousing/warehouse-directed-flow.md)

Lesen Sie die Schritte für jedes Szenario im entsprechenden Artikel.
   
## <a name="see-also" />Siehe auch

[Produktion](../production-manage-manufacturing.md)  
[Lagerhaus](../warehouse-manage-warehouse.md)  

