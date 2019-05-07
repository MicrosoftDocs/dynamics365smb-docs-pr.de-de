---
title: Verwenden Sie Excel, um in Business Central Daten zu importieren | Microsoft Docs
description: Verwenden Sie das Standardkonfigurationspaket, um Debitorendaten in Excel hinzuzufügen und Daten nach Business Central zu importieren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 0d31e710c0b5d9e1dfa63c9c653b740fdcc12f11
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926532"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Geschäftsdaten aus anderen Finanzsystemen importieren
Wenn Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden, können Sie auswählen, einen leeren Mandanten zu erstellen, sodass Sie Ihre eigenen Daten hochladen und den neuen Projektmandanten in [!INCLUDE[d365fin](includes/d365fin_md.md)] testen können. Abhängig von der Finanzlösung, die Ihr Unternehmen heute verwendet, können Sie Informationen zu Debitoren, Kreditoren, Lagerbestand und Bankkonten vornehmen.  

Vom Rollencenter aus können Sie eine unterstützte Einrichtung vornehmen, mit der Sie die Daten einer Exceldatei oder aus anderen Formaten übertragen können. Die Art der Dateien, die Sie hochladen können, hängt von den Erweiterungen ab, die verfügbar sind. Beispielsweise können Sie Daten aus QuickBooks hochladen, da [!INCLUDE[d365fin](includes/d365fin_md.md)] eine Erweiterung umfasst, die die Umwandlung von QuickBooks behandelt. Wenn Sie Daten aus anderen Finanzlösungen migrieren möchten, müssen Sie überprüfen, ob eine Erweiterung für diese Lösung verfügbar ist oder sie aus Excel importieren.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst Vorlagen für Debitoren, Kreditoren und Lagerartikel, die Sie zum Anwenden wählen können, wenn Sie Ihre Daten importieren.

Sie können Transaktions-Masterdaten und die Daten aus anderen Finanzsysteme basierend auf dem Standardkonfigurationspaket in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren. Auf der Seite **Konfigurationspakete** können Sie mit einem Paket arbeiten, um die Daten zu importieren und zu prüfen, bevor Sie die Paketnummer anwenden.  

> [!TIP]  
> Alternativ verwenden Sie den Datenmigrationsassistenten, um die Daten aus QuickBooks oder von Dynamics GP zu importieren. Weitere Informationen finden Sie unter [QuickBooks-Datenmigration](ui-extensions-quickbooks-data-migration.md) oder [Dynamics GP-Datenmigration](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> Für umfangreichere Implementierungsarbeiten können Sie RapidStart Services nutzen für [!INCLUDE[d365fin](includes/d365fin_md.md)], der ein umfangreiches Toolkit für das Einrichten von neuen Lösungen auf Grundlage von Geschäftsanforderungen und -Einrichtungsdaten der Debitoren ist. RapidStart Services enthält auch Funktionalität für Stammdaten Importieren von Artikeln. Weitere Informationen finden Sie unter [Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

Um Artikelbilder zu importieren, können Sie eine dedizierte Funktion auf der Seite **Lagereinrichtung** verwenden. Weitere Informationen finden Sie unter [Importieren mehrerer Artikelbilder](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Importieren von Daten aus den Konfigurations-Paketen
[!INCLUDE[d365fin](includes/d365fin_md.md)] umfasst ein Konfigurationspaket, das Sie dann in Excel exportieren und dort die Daten einrichten können. Anschließend können die wieder von Excel importiert werden. Das Paket besteht aus 27 Tabellen, einschließlich Masterdaten wie Debitoren, Kreditoren, Artikel und Konten, andere grundsätzliche Einrichtungstabellen wie Versandarten und Transaktionstabellen wie Versandkopf und Zeilen.  

> [!NOTE]  
>   Das Arbeiten mit Konfigurationspaketen ist eine erweiterte Funktionalität und wir empfehlen, dass Sie sich an Ihren Administrator wenden. [Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets](across-import-data-configuration-packages.md)

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

## <a name="see-also"></a>Siehe auch
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP Datenmigration](ui-extensions-dynamicsgp-data-migration.md)  
[Mehrere Artikelbilder importieren](inventory-how-import-item-pictures.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
