---
title: QuickBooks-Migrations-Erweiterung verwenden | Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Desktop zu Business Central zu importieren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: e5cb755b6a15070410c42328ccf08b784928f3ca
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798551"
---
# <a name="the-quickbooks-data-migration-extension"></a>Die QuickBooks-Datenmigrationserweiterung
Diese Erweiterung macht es einfach, Debitoren, Kreditoren und Artikel aus QuickBooks in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren. Wenn Ihr Geschäft QuickBooks heute verwendet, können Sie die Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu migrieren.  
Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Datum von QuickBooks Desktop
 
Sie können die folgenden Daten aus QuickBooks Online in Business Central importieren:

- Debitoren  
- Kreditoren  
- Artikel  
- Kontenplan  
- Saldovortragtransaktion in der Finanzbuchhaltung  
- Verfügbare Mengen für Lagerartikel  
- Offene Dokumente für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen  

Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen. Wir aktualisieren keine teilweise bezahlten Beträge. Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500. Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren. Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.

> [!NOTE]
> Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.

## <a name="before-you-start"></a>Bevor Sie beginnen
Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren. Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren. Beispielsweise die Konten, die Sie für Transaktionen buchen:

- Der Verkauf von Artikeln oder Services an einen Debitoren  
- Der Kauf von Waren oder Dienste von einem Kreditor  
- Änderungen in der Finanzbuchhaltung  

Business Central erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden. Überprüfen Sie, ob Sie Kontonummern Ihren Konten in QuickBooks online zugeordnet werden.
Wenn Transaktionen in QuickBooks Steuerbeträge haben, müssen Sie eine MwSt einrichten für Ihre Steuerzuständigkeiten in Business Central, bevor Sie Buchungen durchführen können.

Um die Daten aus der QuickBooks Desktop-Anwendung abzurufen, müssen Sie das Microsoft Daten Exporter Tool herunterladen.  Die Anweisungen für das Werkzeug finden Sie im Datenmigrationsassistenten in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Das Tool stellt eine Verbindung mit Ihrer QuickBooks-Anwendung her und exportiert die anwendbaren Daten in eine .ZIP-Datei.  

> [!NOTE]
> Zurzeit arbeitet das Datenexporteurtool nur mit QuickBooks 2017 und 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Die QuickBooks-Datenmigrations-Erweiterung suchen
Die QuickBooks-Datenmigrationserweiterung ist eingerichtet und vorbereitet, um als integrierter Teil des unterstützten Setups bei der Datenmigration zu helfen. Wenn Sie bereit sind jetzt anzufangen, und die Daten aus QuickBooks exportiert haben, wählen Sie das Symbol ![Glühbirne, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet werden kann](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren"), geben Sie **Unterstützte Einrichtung** ein, und wählen dann den zugehörigen Link aus. Wählen Sie **Migrieren von Geschäftsdaten** und anschließend führen Sie die Schritte im Handbuch aus.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Was tue ich, nachdem ich Daten migriert habe?
Nachdem Sie Daten migriert haben, haben die Transaktionen den Status Nicht gebucht, sodass Sie sie überprüfen und Korrekturen vornehmen können. Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen. Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, gehen Sie zu der Seite Verkaufsrechnungen. Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie zur Seite Zlg.-Ausg. Buch.-Blätter.
Sie sollten mehrere Dinge tun: wenn die Transaktionen in QuickBooks einen Aufschlag oder einen Rabatt bei Beträgen bedeuten, müssen Sie die Beträge manuell den entsprechenden Transaktionen in Business Central hinzufügen, bevor Sie sie buchen.
Wenn Sie MwSt verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MwSt.-Beträge buchen können.
Prüfen Sie die Startkapitale für Konten in der Finanzbuchhaltung. QuickBooks speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.

## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
