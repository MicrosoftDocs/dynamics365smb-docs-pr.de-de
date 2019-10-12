---
title: So erstellen Sie Buch.-Blatt-Eröffnungssalden | Microsoft Docs
description: Business Central enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten mithilfe von Buch.-Blatt-Buchungen einfach übertragen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 837845bfa31217e071d7237591d34eb3a049bad0
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304540"
---
# <a name="create-journal-opening-balances"></a>So erstellen Sie Buch.-Blatt-Eröffnungssalden
[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten auf das Debitorbuch.-Blatt, das Kreditorbuch.-Blatt, das Artikel Buch.-Blatt und das Hauptbuchbuch.-Blatt übertragen.

Der erste Schritt besteht darin, ein Konfigurationspaket zu erstellen, das die Einrichtungstabellen für alle Buch.-Blätter enthält. Nachfolgend wird davon ausgegangen, dass dieser Schritt abgeschlossen ist. Weitere Informationen finden Sie unter [Unternehmenskonfiguration einrichten](admin-set-up-company-configuration.md). Das Verfahren beschreibt die folgenden Schritte, die das Übernehmen des Pakets, das von einem Partner bereitgestellt wird, enthalten.  

Bevor Sie den Buchungsvorgang starten, prüfen Sie, ob Sie in der RapidStart Services-Implementierungs-Rollencenterseite sind, da sie den korrekten Kontext für Ihre Konfigurationsarbeit bereitstellt. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>So übernehmen Sie die Posten in einem Buch.-Blatt für einen neuen Mandanten.  
1. Konfigurieren Sie einen neuen Mandanten und wenden Sie ein Konfigurationspaket darauf an. Weitere Informationen finden Sie unter [So konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Der neue Mandant enthält keine Informationen über Buch.-Blatt-Eröffnungssalden.  

2. Öffnen Sie das Konfigurationsarbeitsblatt, und importieren Sie vorhandene Daten zu Debitoren, Kreditoren, Artikeln, Kreditoren und dem Sachkonto. Weitere Informationen finden Sie unter [Gewusst wie: Kundendaten zusammenführen](admin-migrate-customer-data.md).  
3. Wählen Sie die Aktion **Buch.-Blattzeilen erstellen** aus.  
4. Füllen Sie das Inforegister **Optionen** entsprechend aus und legen Sie nach Bedarf Filter fest. Geben Sie beispielsweise im Feld **Buch.-Blattvorlage** einen Namen ein.  
5. Wählen Sie die Schaltfläche **OK** aus. Die Datensätze stehen jetzt im Buch.-Blatt, die Beträge sind jedoch leer.  
6. Exportieren Sie die Buch.-Blatt-Tabelle in Excel und geben Sie die Buchung und die Gegenkontoinformationen aus den Stammdaten manuell ein.
7. Importieren Sie die Tabelleninformationen in den neuen Mandanten und gleichen Sie sie aus. Die Erfassungspositionen sind für die Buchung bereit.  
8. Wählen Sie im Konfigurationsarbeitsblatt die Buch.-Blattzeile, und wählen Sie in der Registerkarte Aktionen in der Gruppe Anzeigen die Option **Datenbank-Daten** aus.  
9. Überprüfen Sie die Informationen und wählen Sie dann die Schaltfläche **Buchen** aus.  
10. Wiederholen Sie die Schritte, um verschiedene Salden zu importieren und zu buchen.  

## <a name="see-also"></a>Siehe auch  
[Konfigurationen für neue Mandanten übernehmen](admin-apply-configuration-to-new-companies.md)  
[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
