---
title: QuickBooks Online Datenmigration-Erweiterung
description: 'Beschreibt, wie die Erweiterung verwendet wird, um Debitoren, Kreditoren, Artikel und Konten aus QuickBooks Online zu Business Central zu migrieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'extension, migrate, data, QuickBooks, import'
ms.search.form: '1830,'
ms.date: 06/24/2021
ms.author: bholtorf
---

# <a name="the-quickbooks-online-data-migration-extension" />Die QuickBooks Online-Datenmigrations-Erweiterung

Diese Erweiterung ist im unterstützten Einrichtungshandbuch **Datenmigration** enthalten, um Ihnen zu helfen, wichtige Geschäftsdaten von QuickBooks Online zu [!INCLUDE[prod_short](includes/prod_short.md)] zu migrieren. Dies ist beispielsweise dann nützlich, wenn Ihr Unternehmen wächst und Sie sich entschieden haben, Ihre Geschäftsführungs-App zu aktualisieren, indem Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] verwenden.

## <a name="what-data-can-i-import-from-quickbooks-online" />Welche Daten kann ich von QuickBooks Online importieren?

Sie können die folgenden Daten von QuickBooks Online in [!INCLUDE[prod_short](includes/prod_short.md)] importieren:  

* Debitoren
* Kreditoren
* Artikel
* Kontenplan
* Saldovortragtransaktion in der Finanzbuchhaltung
* Verfügbare Mengen für Lagerartikel
* Offene Dokumente für Debitoren und Kreditoren, wie beispielsweise Rechnungen, Gutschriften und Zahlungen

Es migrieren nur Gesamtbeträge auf Einkaufs- und Verkaufsbelegen. Wir aktualisieren keine teilweise bezahlten Beträge. Wenn ein Debitor 300 von insgesamt 500 Dollar einer Verkaufsrechnung bezahlt hat, migrieren wir die vollständigen 500. Wenn Sie Teilzahlungen erhalten, müssen Sie diese manuell aktualisieren, entweder, vor oder nach dem Sie Daten migrieren. Es ist empfehlenswert, ausstehende Transaktionen anzuwenden, bevor Sie migrieren, das ist einfacher danach.

> [!NOTE]  
> Wir migrieren keine Einkaufsbestellungen oder Verkaufsaufträge.

## <a name="before-you-start" />Bevor Sie beginnen

Ein wichtiger Teil des Migrationsvorgangs ist es, Konten anzugeben, um Transaktionen zu migrieren. Es ist empfehlenswert, diese Zuordnung zu planen, bevor Sie Daten migrieren. Beispielsweise die Konten, die Sie für Transaktionen buchen:  

* Der Verkauf von Artikeln oder Services an einen Debitoren.
* Der Kauf von Waren oder Dienste von einem Kreditor.  
* Änderungen in der Finanzbuchhaltung.  

[!INCLUDE[prod_short](includes/prod_short.md)] erfordert, dass Sachkonten die Kontonummern haben, die ihm zugeordnet werden. Überprüfen Sie, ob Kontonummern Ihren Konten in QuickBooks Online zugeordnet wurden.

Wenn Transaktionen in QuickBooks Online Steuerbeträge haben, müssen Sie ein Steuerkonto für Ihre Steuerzuständigkeiten in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, bevor Sie Buchungen durchführen können.

## <a name="how-do-i-start-using-the-extension" />Wie beginne ich, die Erweiterung zu nutzen?

Erste Schritte sind einfach. Sie müssen nur das unterstütze Einrichtungshandbuch **Datenmigration** ausführen. So geht es:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Unterstützte Einrichtung** ein, und wählen Sie dann **Geschäftsdaten migrieren**.
2. Befolgen Sie die Anweisungen für jeden Schritt im unterstützten Anleitungshandbuch.

## <a name="what-do-i-do-after-i-migrate-data" />Was tue ich, nachdem ich Daten migriert habe?

Nachdem Sie Daten migriert haben, haben die Transaktionen den Status **Nicht gebucht**, sodass Sie sie überprüfen und Korrekturen vornehmen können. Um die Transaktionen zu überprüfen, wechseln Sie zur Seite in der Sie normalerweise suchen müssen. Beispielsweise um nicht gebuchten Verkaufsrechnungen zu überprüfen, gehen Sie zu der Seite **Verkaufsrechnungen**. Um Zahlungsausgangs Buch.-Blätter zu überprüfen, wechseln Sie zur Seite **Zlg.-Ausg. Buch.-Blätter**.  

Es gibt mehrere Dinge, die Sie durchführen sollten:

* Wenn die Transaktionen in QuickBooks Online Aufschläge oder Rabattbeträge aufweisen, müssen Sie die Beträge manuell zu den verwandten Transaktionen in [!INCLUDE[prod_short](includes/prod_short.md)] hinzufügen, bevor Sie diese buchen.
* Wenn Sie MwSt verwenden, können Sie eine Geschäftsbuchungsgruppe und eine Produktbuchungsgruppe "Buchungsmatrix Einrichtung" hinzufügen, sodass Sie MwSt.-Beträge buchen können.
* Prüfen Sie die Startkapitale für Konten in der Finanzbuchhaltung. QuickBooks Online speichert nicht den aktuellen Saldo für alle Konten, daher müssen Sie möglicherweise Startkapitale korrigieren.

## <a name="see-related-microsoft-trainingtrainingmodulesmigrate-data-dynamics--business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/migrate-data-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Importieren von Geschäftsdaten aus anderen Finance-Systemen](across-import-data-configuration-packages.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe von Erweiterungen](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
