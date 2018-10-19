---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Online auf Business Central zu migrieren
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e9b0a481f16d8f0bc1647640b62a81b3ea441028
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---

# <a name="the-quickbooks-online-data-migration-extension"></a>Die QuickBooks-Online-Datenmigrations-Erweiterung
Diese Erweiterung ist im unterstützten Einrichtungshandbuch **Datenmigration** enthalten, um Ihnen zu helfen, wichtige Geschäftsdaten von QuickBooks in Online zu [!INCLUDE[d365fin](includes/d365fin_md.md)]migrieren. Dies ist beispielsweise dann nützlich, wenn Ihr Unternehmen wächst und Sie sich entschieden haben, Ihre Geschäftsführungs-App zu aktualisieren, indem Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden.

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Welche Daten kann ich von QuickBooks online importieren?
Sie können die folgenden Daten aus QuickBooks online importieren [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Debitoren
* Kreditoren
* Artikel
* Kontenplan
* Saldovortragtransaktion in der Finanzbuchhaltung
* Verfügbare Mengen für Lagerartikel
* Offene Dokumente für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen

Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen. Wir aktualisieren keine teilweise bezahlten Beträge. Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500. Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren. Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.

> [!NOTE]  
>   Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.

## <a name="before-you-start"></a>Bevor Sie beginnen
Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren. Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren. Beispielsweise die Konten, die Sie für Transaktionen buchen:  

* Der Verkauf von Artikeln oder Services an einen Debitoren.
* Der Kauf von Waren oder Dienste von einem Kreditor.  
* Änderungen in der Finanzbuchhaltung.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden. Überprüfen Sie, ob Sie Kontonummern Ihren Konten in QuickBooks online zugeordnet werden.

Wenn Transaktionen in QuickBooks online Steuerbeträge haben, müssen Sie eine MwSt einrichten für Ihre Steuerzuständigkeiten in, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie Buchungen durchführen können.

## <a name="how-do-i-start-using-the-extension"></a>Wie beginne ich, die Erweiterung zu nutzen?
Erste Schritte sind einfach. Sie müssen nur das unterstütze Einrichtungshandbuch **Datenmigration** ausführen. So geht es:

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unterstütztes Setup** ein, und wählen dann **Geschäftsdaten migrieren** aus.
2. Befolgen Sie die Anweisungen für jeden Schritt im unterstützten Anleitungshandbuch.

## <a name="what-do-i-do-after-i-migrate-data"></a>Was tue ich, nachdem ich Daten migriert habe?
Nachdem Sie Daten migriert haben, haben die Transaktionen den Status **Nicht gebucht**, sodass Sie sie überprüfen und Korrekturen vornehmen können. Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen. Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, wechseln Sie ins Fenster **Verkaufsrechnungen**. Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie ins Fenster **Zlg.-Ausg. Buch.-Blätter**.   

Es gibt mehrere Dinge, die Sie durchführen sollten:

* Wenn die Transaktionen in QuickBooks online Markup oder Rabattbeträge aufweisen, müssen Sie die Beträge zu den verwandten Transaktionen manuell hinzufügen, [!INCLUDE[d365fin](includes/d365fin_md.md)] bevor Sie diese buchen.
* Wenn Sie MwSt verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MwSt.-Beträge buchen können.
* Prüfen Sie die Startkapitale für Konten in der Finanzbuchhaltung. QuickBooks online speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.

## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  

