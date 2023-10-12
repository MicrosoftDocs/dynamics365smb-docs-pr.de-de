---
title: Einführung in Contoso Coffee Project Management
description: Dieser Artikel stellt Ihnen die Demonstrationsdaten von Consoso Coffee für das Auftrags- und Projektmanagement vor.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Einführung in Contoso Coffee-Auftrags- und Projektmanagement

Contoso Coffee ist ein fiktives Unternehmen, das Kaffeemaschinen für Verbraucher und gewerbliche Kunden herstellt. Die **Contoso Coffee**-Apps für Business Central fügen Demodaten hinzu, mit deren Hilfe Sie die Verwendung der Auftrags- und Projektmanagementfunktionen in Business Central erlernen können.

Diese App bietet mehrere Elemente, die für die wichtigsten exemplarischen Vorgehensweisen verwendet werden:

- Ressourcen mit zugewiesenen Fertigkeiten und Zonen
- Elemente, die zum Erstellen von Serviceartikeln konfiguriert sind

> [!IMPORTANT]
> Bevor Sie eines der Szenarien für Contoso Coffee ausführen, buchen Sie alle Buchungsblattzeilen mit Anfangssalden. Weitere Anforderungen finden Sie im Abschnitt [Contoso Coffee-Daten einrichten](#set-up-contoso-coffee-jobs-and-project-management-data).
>
> 
## Einrichten von Contoso Coffee-Auftrags- und Projektmanagementdaten

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Sobald die relevanten Apps installiert sind, wechseln Sie zur Seite [Demodaten für Contoso Coffee-Projekte](https://businesscentral.dynamics.com/?page=4767) in [!INCLUDE [prod_short](../../includes/prod_short.md)], und ändern Sie die Standardeinstellungen entsprechend Ihren Anforderungen. Die Einstellungen werden in den folgenden Tabellen beschrieben:  

|Feld  |Beschreibung  |
|---------|---------|
|**Anfangsjahr** |Gibt das erste Jahr an, das Sie für die Contoso Coffee-Demonstrationsdaten verwenden möchten. Je nach Unternehmenseinrichtung ist das Jahr entweder ein Kalenderjahr oder ein Geschäftsjahr.|
|**Debitorennr.**  |Der Debitor, der für die Szenarios in Vertriebsvorgängen verwendet werden soll.|
|**Artikel 1 Nr.**  |Gibt den Artikel an, der für Vertragsszenarien verwendet wird.|
|**Artikel 2 Nr.**  |Gibt den Artikel an, der für Problemlösungsszenarien verwendet wird.|
|**Nr. von lokaler Ressource 1**  |Gibt die Ressource an, die für Vertragsszenarien verwendet wird.|
|**Nr. von Remote-Ressource 1**  |Gibt die Ressource an, die für Problemlösungsszenarien verwendet wird.|
|**Debitorenbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Debitor Allgemeine Geschäftsbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Inland – Allgemeine Geschäftsbuchungsgruppe**|Gibt einen Geschäftscode für inländische Debitoren und Kreditoren an. Die Geschäftscodes werden verwendet, wenn Transaktionen gebucht werden. |
|**Wiederverkauf - Lagerbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die für Einzelhandelsbuchungen verwendet werden müssen.|
|**Einzelhandel – Produktbuchungsgruppe**    |Gibt einen Code für Artikel oder Ressourcen an, die für Einzelhandelsbuchungen verwendet werden müssen.|
|**MwSt.-Produktbuchungsgrp.**    |Gibt einen Umsatzsteuer-Produktcode für Artikel zum Buchen der Umsatzsteuer an, wenn die Umsatzsteuer aktiviert ist.|
|**Preisfaktor**     |Gibt einen Faktor an, um einen Preis von USD/EUR in die lokale Währung umzurechnen. *1* bedeutet, dass der Preis in jeder Währung gleich ist. Eine höhere Zahl wird verwendet, um den Preis in der Landeswährung zu erhalten. |
|**Rundungspräzision**  |Definiert, wie berechnete Verbrauchsmengen gerundet werden, wenn sie in FA-Verbrauchs Buch.-Blattzeilen eingegeben werden. Mengen kleiner als 0,5 werden abgerundet. Mengen gleich oder größer 0,5 werden aufgerundet.|

Wenn Sie fertig sind, wählen Sie die Aktion **Demodaten erstellen** aus. Es dauert einige Minuten, der zugrunde liegenden Datenbank die Daten hinzuzufügen, anschließend können Sie die verschiedenen Szenarien jedoch ausführen.  

## Siehe auch
