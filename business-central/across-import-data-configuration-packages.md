---
title: Verwenden Sie Excel, um in Financials Stammdaten zu importieren | Microsoft Docs
description: "Verwenden Sie das Standardkonfigurationspaket, um Debitorendaten in Excel hinzuzufügen und Daten nach Business Central zu importieren."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets.
Sie können Transaktions-Masterdaten und die Daten aus anderen Finanzsysteme basierend auf dem Standardkonfigurationspaket in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren. Im Fenster **Konfigurationspakete** können Sie mit einem Paket arbeiten, um die Daten zu importieren und zu prüfen, bevor Sie die Paketnummer anwenden.  

> [!NOTE]  
> Konfigurationspakete sind Teil von RapidStart-Services, [!INCLUDE[d365fin](includes/d365fin_md.md)]für der umfangreichen Toolkit für das Einrichten von neuen Lösungen auf Grundlage Geschäftsanforderungen und -Einrichtungsdaten der Debitoren. RapidStart enthält auch Funktionalität für Stammdaten Importieren von Artikeln. Weitere Informationen finden Sie unter [Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

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
-   Lieferbedingungsmethode
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
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Datenmigration](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

