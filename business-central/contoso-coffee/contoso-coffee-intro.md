---
title: Einführung in die Demodaten für Contoso Coffee
description: 'Übersicht über Szenarien dazu, wie Sie mithilfe von Contoso Coffee-Demodaten die Verwendung von Produktionsfunktionen in Business Central erlernen können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# Einführung in die Demodaten für Contoso Coffee

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für [!INCLUDE [prod_short](../includes/prod_short.md)] fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Produktionsfunktionen in [!INCLUDE [prod_short](../includes/prod_short.md)] erlernen können.  

## Demodaten für Contoso Coffee einrichten

[!INCLUDE [contoso-coffee-app-install](contoso-coffee-app-install.md)].

Wenn die Apps installiert sind, verwenden Sie auf der Seite **Demo-Tool für Contoso** die Aktion **Konfigurieren**, um die folgenden Module vorzubereiten. Sie können wählen, ob alle verfügbaren Daten, einschließlich Einrichtungs- und Produktionsdaten, oder nur Einrichtungsdaten installiert werden sollen.

 - Das **Allgemeine Modul** zur Vorbereitung allgemeiner Einstellungen, die für [!INCLUDE [prod_short](../includes/prod_short.md)] erforderlich sind. Zum Beispiel Dinge wie Zahlenreihen. 

Die Einstellungen werden in den folgenden Tabellen beschrieben:  

|Feld  |Description  |
|---------|---------|
|**Anfangsjahr** |Gibt das erste Jahr an, das Sie für die Contoso Coffee-Demonstrationsdaten verwenden möchten. Je nach Unternehmenseinrichtung ist das Jahr entweder ein Kalenderjahr oder ein Geschäftsjahr.|
|**Länder-/Regionscode**|Gibt einen Land/Regionscode für inländische Debitoren und Kreditoren an.|
|**Unternehmenstyp**    |Gibt an, ob das aktuelle Unternehmen Mehrwertsteuer oder Verkaufssteuer melden muss. |
|**Preisfaktor**     |Gibt einen Faktor an, um einen Preis von USD/EUR in die lokale Währung umzurechnen. *1* bedeutet, dass der Preis in jeder Währung gleich ist. Eine höhere Zahl wird verwendet, um den Preis in der Landeswährung zu erhalten. |
|**Rundungsgenauigkeit**  |Gibt die Rundungsgenauigkeit an, mit der Sie die Demodaten erstellen möchten.|

 - Das [Fertigungsmodul](manufacturing/contoso-coffee-manufacturing-intro.md) zur Vorbereitung auf die Verwendung der [Produktionsszenarien](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - Das [Lagerortmodul](warehousing/contoso-coffee-warehousing-intro.md) zur Vorbereitung auf die Verwendung der [Lagerortszenarien](warehousing/contoso-coffee-warehousing-intro.md#scenarios).
 - Das [Servicemodul](service/contoso-coffee-service-intro.md) zur Vorbereitung auf die Verwendung der [Serviceszenarien](service/contoso-coffee-service-intro.md#scenarios).

Nachdem Sie die Module konfiguriert haben, die Sie ausprobieren möchten, wählen Sie die Aktion **Generieren**, um Demonstrationsdaten für sie zu erstellen.

## Siehe auch

[Fertigung](../production-manage-manufacturing.md)  
[Lagerfunktionen](../warehouse-manage-warehouse.md)  
[Dienst](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

