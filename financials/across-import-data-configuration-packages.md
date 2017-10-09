---
title: Verwenden Sie Excel, um in Financials Stammdaten zu importieren | Microsoft Docs
description: "Verwenden Sie das Standardkonfigurationspaket, um Debitorendaten in Excel hinzuzufügen und Daten nach Dynamics 365 for Financials zu importieren."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2a38dc36cb9ff609c5582acd489841b20013d4bc
ms.openlocfilehash: 8cf36afea60b089afac8f1c27d126cd19b88ce94
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets.
Sie können Transaktions-Masterdaten und die Daten aus anderen Finanzsysteme basierend auf dem Standardkonfigurationspaket in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren. Im Fenster **Konfigurationspakete** können Sie mit einem Paket arbeiten, um die Daten zu importieren und zu prüfen, bevor Sie die Paketnummer anwenden.  

Wenn Sie mit RapidStart-Services für Microsoft Dynamics vertraut sind, sind Sie außerdem mit Konfigurationspaketen vertraut. Das Standardkonfigurationspaket unterstützt die meisten allgemeinen Arten von Daten, die Sie von einem Legacysystem importieren möchten. Dort können Sie die Daten aus Legacysystem hinzufügen und sie dann entsprechend der Geschäftslogik von [!INCLUDE[d365fin](includes/d365fin_md.md)] festlegen.  

> [!TIP]  
>   Alternativ verwenden Sie den Datenmigrationsassistenten, um die Daten aus QuickBooks oder von Dynamics GP zu importieren. Weitere Informationen finden Sie unter [QuickBooks-Datenmigration](ui-extensions-quickbooks-data-migration.md) oder [Dynamics GP-Datenmigration](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Arbeiten mit Daten in Excel
Wenn Sie das Standardkonfigurationspaket in Excel exportieren, enthält die generierte Arbeitsmappe einen Vorschlag für jede Tabelle im Paket. Um Ihre Aufgaben zu vereinfachen, können Sie die in Excel integrierten XML-Änderungswerkzeuge nutzen. Sie können die in Excel integrierten Funktionen auch für die Datenformatierung und zum Verschieben von Daten in die richtige Zelle verwenden. Beispielsweise fügen Sie einen leeren Vorschlag hinzu und kopieren Sie die Stammdaten dazu. Verwenden Sie eine Excel-Formel, um Daten im Arbeitsblatt für die Datenumwandlung zwischen den Feldern im exportierten Datenblatt und in den Debitorenstammdaten zuzuordnen. Sobald Sie alle Daten zugeordnet haben, kopieren Sie den Bereich der Daten in das Arbeitsblatt mit der Migrationstabelle.  

> [!IMPORTANT]  
>  Ändern Sie nicht die Spalten in den Arbeitsblättern. Wenn sie verschoben, geändert oder gelöscht werden, kann das Arbeitsblatt nicht in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden.

## <a name="tables-in-the-default-configuration-package"></a>Tabellen im Standard-Konfigurations-Paket
Das Standardkonfigurationspaket unterstützt die folgenden Tabellen:

-   Zahlungsbedingungen
-   Debitorenpreisgruppe
-   Lieferbedingung
-   Verkäufer/Einkäufer
-   Ort
-   Gegenkonto
-   Debitor
-   Kreditor
-   Option
-   Verkaufskopf
-   Verkaufszeile
-   Einkaufskopf
-   Einkaufszeile
-   Fibu Buch.-Blattzeile
-   Artikel Buch.-Blattzeile
-   Debitorenbuchungsgruppe
-   Kreditorenbuchungsgruppe
-   Lagerbuchungsgruppe
-   Maßeinheit
-   Geschäftsbuchungsgrp.
-   Produktbuchungsgrp.
-   Buchungsmatrix Einrichtung
-   Gebiet
-   Artikelkategorie
-   Verkaufspreis
-   Einkaufspreis

## <a name="importing-customer-data"></a>So importieren Sie Debitorendaten
Nachdem die Debitorendaten in die Excel-Dateien für die Datenmigration eingegeben wurden, importieren Sie die Dateien in [!INCLUDE[d365fin](includes/d365fin_md.md)] Im Fenster **Konfigurationspakete** importieren Sie die Excel-Datei aus den Daten, und Sie können prüfen, ob die Daten mit [!INCLUDE[d365fin](includes/d365fin_md.md)] übereinstimmen, bevor Sie das Paket anwenden.

## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Datenmigration](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

