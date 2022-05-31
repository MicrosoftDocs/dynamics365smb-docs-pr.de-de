---
title: Excel zum Importieren von Daten nach Business Central verwenden
description: Verwenden Sie das Standardkonfigurationspaket, um Debitorendaten in Excel hinzuzufügen und Daten nach Business Central zu importieren.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 05/10/2022
ms.author: edupont
ms.openlocfilehash: a189f2f10ad9e8f2ab0063987fbafefd4ad1948f
ms.sourcegitcommit: 4853614c85beb347091c5c4c1ea8d974dec887fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740365"
---
# <a name="import-business-data-from-other-finance-systems"></a>Geschäftsdaten aus anderen Finanzsystemen importieren

Wenn Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden, können Sie auswählen, einen leeren Mandanten zu erstellen, sodass Sie Ihre eigenen Daten hochladen und den neuen Projektmandanten in [!INCLUDE[prod_short](includes/prod_short.md)] testen können. Abhängig von der Finanzlösung, die Ihr Unternehmen heute verwendet, können Sie Informationen zu Debitoren, Kreditoren, Lagerbestand und Bankkonten vornehmen.  

Vom Rollencenter aus können Sie eine unterstützte Einrichtung vornehmen, mit der Sie die Daten einer Exceldatei oder aus anderen Formaten übertragen können. Die Art der Dateien, die Sie hochladen können, hängt von den Erweiterungen ab, die verfügbar sind. Beispielsweise können Sie Daten aus QuickBooks hochladen, da [!INCLUDE[prod_short](includes/prod_short.md)] eine Erweiterung umfasst, die die Umwandlung von QuickBooks behandelt. Wenn Sie Daten aus anderen Finanzlösungen migrieren möchten, müssen Sie überprüfen, ob eine Erweiterung für diese Lösung verfügbar ist oder sie aus Excel importieren.  

[!INCLUDE[prod_short](includes/prod_short.md)] umfasst Vorlagen für Debitoren, Kreditoren und Lagerartikel, die Sie zum Anwenden wählen können, wenn Sie Ihre Daten importieren. Um Artikelbilder zu importieren, können Sie eine dedizierte Funktion auf der Seite **Lagereinrichtung** verwenden. Weitere Informationen finden Sie unter [Importieren mehrerer Artikelbilder](inventory-how-import-item-pictures.md).

> [!TIP]  
> Es ist empfehlenswert, dass Sie den Datenmigrationsassistenten nutzen, um die Daten aus Dynamics GP, Dynamics NAV oder QuickBooks zu importieren. Weitere Informationen finden Sie im Verwaltungsinhalt unter [Lokale Daten zu Business Central Online migrieren](/dynamics365/business-central/dev-itpro/administration/migrate-data) oder [QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md).

## <a name="work-with-data-in-excel"></a>Mit Daten in Excel arbeiten

Sie können das Excel-Add-In verwenden, um vorhandene Inhalte zur Verwendung in [!INCLUDE [prod_short](includes/prod_short.md)] vorzubereiten. Weitere Informationen finden Sie unter [Anzeigen und Bearbeiten in Excel von Business Central](across-work-with-excel.md).  

## <a name="import-data-from-configuration-packages"></a>Daten aus den Konfigurationspaketen importieren

Für größere Implementierungsarbeiten können Sie lösungsspezifische Konfigurationspakete erstellen. Weitere Informationen finden Sie unter [Einrichten von Unternehmenskonfigurationspaketen](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (nur in englischer Sprache) in den Verwaltungsinhalten.  

> [!NOTE]  
> Das Arbeiten mit Konfigurationspaketen ist eine erweiterte Funktionalität und wir empfehlen, dass Sie sich an Ihren Vertriebspartner wenden. Weitere Informationen finden Sie unter [Unternehmenskonfigurationspakete einrichten](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (nur in englischer Sprache).

Sie können Transaktions-Masterdaten und die Daten aus anderen Finanzsysteme basierend auf dem Standardkonfigurationspaket in [!INCLUDE[prod_short](includes/prod_short.md)] importieren. Auf der Seite **Konfigurationspakete** können Sie mit einem Paket arbeiten, um die Daten zu importieren und zu prüfen, bevor Sie die Paketnummer anwenden. Sie können beispielsweise das Konfigurationspaket nach Excel exportieren und dort die Daten einrichten. Anschließend können die wieder von Excel importiert werden. Das Paket besteht aus 27 Tabellen, einschließlich Masterdaten wie Debitoren, Kreditoren, Artikel und Konten, andere grundsätzliche Einrichtungstabellen wie Lieferbedingungen und Transaktionstabellen wie Versandkopf und Zeilen.  

Wenn Sie das Standardkonfigurationspaket in Excel exportieren, enthält das generierte Arbeitsblatt ein Arbeitsblatt für jede Tabelle im Paket. Um Ihre Aufgaben zu vereinfachen, können Sie die in Excel integrierten XML-Änderungswerkzeuge nutzen. Sie können die in Excel integrierten Funktionen auch für die Datenformatierung und zum Verschieben von Daten in die richtige Zelle verwenden. Beispielsweise fügen Sie ein leeres Arbeitsblatt hinzu und kopieren Sie die Stammdaten dazu. Verwenden Sie eine Excel-Formel, um Daten im Arbeitsblatt für die Datenumwandlung zwischen den Feldern im exportierten Arbeitsblatt und in den Debitorenstammdaten zuzuordnen. Sobald Sie alle Daten zugeordnet haben, kopieren Sie den Bereich der Daten in das Arbeitsblatt mit der Migrationstabelle.  

> [!IMPORTANT]  
> Ändern Sie nicht die Spalten in den Arbeitsblättern. Wenn sie verschoben, geändert oder gelöscht werden, kann das Arbeitsblatt nicht in [!INCLUDE[prod_short](includes/prod_short.md)] importiert werden.

> [!NOTE]
> Felder vom Typ Blob können nicht mithilfe von Excel exportiert/importiert werden.

### <a name="tables-in-the-default-configuration-package"></a>Tabellen im Standard-Konfigurations-Paket

Das Standardkonfigurationspaket unterstützt die folgenden Tabellen:

- Zahlungsbedingungen
- Debitorenpreisgruppe
- Lieferbedingung
- Verkäufer/Einkäufer
- Ort
- Gegenkonto
- Debitor
- Kreditor
- Option
- Verkaufskopf
- Verkaufszeile
- Einkaufskopf
- Einkaufszeile
- Gen. Buch.-Blattzeile
- Artikel Buch.-Blattzeile
- Debitorenbuchungsgruppe
- Kreditorenbuchungsgruppe
- Lagerbuchungsgruppe
- Einheit
- Gen. Geschäftsbuchungsgrp.
- Gen. Produktbuchungsgruppe
- Buchungsmatrix Einrichtung
- Gebiet
- Artikelkategorie
- Verkaufspreis
- Einkaufspreis

## <a name="see-also"></a>Siehe auch

[Migrieren lokaler Daten zu Business Central Online (nur in englischer Sprache)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Unternehmenskonfigurationpakete einrichten](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)  
[Mehrere Artikelbilder importieren](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]