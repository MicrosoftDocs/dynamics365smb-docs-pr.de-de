---
title: So erstellen Sie Buch.-Blatt-Eröffnungssalden | Microsoft Docs
description: Business Central enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten mithilfe von Buch.-Blatt-Buchungen einfach übertragen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e1d936901f1a42991895c9e4b797a3238a24710
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378273"
---
# <a name="create-journal-opening-balances"></a>So erstellen Sie Buch.-Blatt-Eröffnungssalden

[!INCLUDE[prod_short](includes/prod_short.md)] enthält mehrere Stapelverarbeitungsaufträge, die bereitgestellt werden, um die Übertragung von vorhandenen Kontosalden auf einen neu konfigurierten Mandanten zu unterstützen. Sie können diese Daten auf das Debitorbuch.-Blatt, das Kreditorbuch.-Blatt, das Artikel Buch.-Blatt und das Hauptbuchbuch.-Blatt übertragen.

Der erste Schritt besteht darin, ein Konfigurationspaket zu erstellen, das die Einrichtungstabellen für alle Buch.-Blätter enthält. Nachfolgend wird davon ausgegangen, dass dieser Schritt abgeschlossen ist. Weitere Informationen finden Sie unter [Unternehmenskonfiguration einrichten](admin-set-up-company-configuration.md). Das Verfahren beschreibt die folgenden Schritte, die das Übernehmen des Pakets, das von einem Partner bereitgestellt wird, enthalten.  

Bevor Sie den Buchungsvorgang starten, prüfen Sie, ob Sie die Verwaltungsrollencenterseite verwenden, da sie den korrekten Kontext für Ihre Konfigurationsarbeit bereitstellt. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>So übernehmen Sie die Posten in einem Buch.-Blatt für einen neuen Mandanten.

1. Konfigurieren Sie einen neuen Mandanten und wenden Sie ein Konfigurationspaket darauf an. Weitere Informationen finden Sie unter [So konfigurieren Sie einen Mandanten mit dem RapidStart-Assistenten](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Der neue Mandant enthält keine Informationen über Buch.-Blatt-Eröffnungssalden.  

2. Öffnen Sie das Konfigurationsarbeitsblatt, und importieren Sie vorhandene Daten zu Debitoren, Kreditoren, Artikeln, Kreditoren und dem Sachkonto. Weitere Informationen finden Sie unter [Gewusst wie: Kundendaten zusammenführen](admin-migrate-customer-data.md).  

    Jetzt haben Sie die Masterdaten eingerichtet. Als Nächstes fügen Sie die Eröffnungssalden hinzu. In den folgenden Schritten wird beschrieben, wie Sie Buch.-Blattzeilen für Sachkonten erstellen. Gleiches gilt jedoch für die Erstellung von Buch.-Blattzeilen für Debitoren, Kreditoren und Artikel.  
3. Wählen Sie beispielsweise die Aktion **Buch.-Blattzeilen erstellen** aus.  
4. Füllen Sie das Inforegister **Optionen** entsprechend aus und legen Sie nach Bedarf Filter fest. Geben Sie beispielsweise im Feld **Buch.-Blattvorlage** einen Namen ein.  
5. Wählen Sie die Schaltfläche **OK** aus. Die Datensätze stehen jetzt im Buch.-Blatt, die Beträge sind jedoch leer.  
6. Exportieren Sie die Buch.-Blatt-Tabelle in Excel und geben Sie die Buchung und die Gegenkontoinformationen aus den Stammdaten manuell ein.
7. Importieren Sie die Tabelleninformationen in den neuen Mandanten und gleichen Sie sie aus. Die Erfassungspositionen sind für die Buchung bereit.  
8. Wählen Sie im Konfigurationsarbeitsblatt die Buch.-Blattzeile, und wählen Sie in der Registerkarte Aktionen in der Gruppe Anzeigen die Option **Datenbank-Daten** aus.  
9. Überprüfen Sie die Informationen und wählen Sie dann die Schaltfläche **Buchen** aus.  
10. Wiederholen Sie die Schritte, um verschiedene Salden zu importieren und zu buchen.  

> [!TIP]
> Sie können dieselben Stapeljobs verwenden, um Eröffnungssalden hinzuzufügen, wenn Sie einen neuen Debitor oder Kreditor registrieren, mit dem Sie zuvor Geschäfte gemacht haben, bei dem Sie jedoch nicht registriert sind [!INCLUDE [prod_short](includes/prod_short.md)]. Suchen Sie einfach nach der entsprechenden Aufgabe und wählen Sie dann den entsprechenden Link.

## <a name="see-also"></a>Siehe auch

[Konfigurationen für neue Unternehmen übernehmen](admin-apply-configuration-to-new-companies.md)  
[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]