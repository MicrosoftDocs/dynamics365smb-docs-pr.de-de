---
title: Unternehmenskonfigurationen einrichten | Microsoft Docs
description: Der Implementierungsprozess beginnt mit der benötigten Business Central Lösung. Sie bündeln alle diese Informationen in Konfigurationspakete.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e9b54a28c960ccdaa41c16cce237266e8cb43a88
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4745942"
---
# <a name="set-up-company-configuration"></a>Richten Sie eine Unternehmenskonfiguration ein.
Der Implementierungsprozess beginnt mit dem Microsoft-Partner. Dies ist der Partner, der für die Formulierung der Konfigurationsdetails und das Erstellen eines Pakets zuständig ist, dass ein Debitor einfach anwenden kann. Bevor Sie einen neuen Mandanten erstellen, sollten Sie planen, wie dieser konfiguriert wird. Sie müssen an grundlegende Einrichtungsdaten und die Arten der Daten denken, die Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Lösung benötigt. Sie bündeln alle diese Informationen in Konfigurationspakete.

RapidStart Services gibt außerdem die Werkzeuge, die Sie verwenden, um die Stammdaten zu migrieren, beispielsweise Debitoren und Kreditoren.  

Es ist empfehlenswert, dass Sie Konfigurationspakete erstellen, bei denen die meisten Einrichtungstabellen bereits ausgefüllt sind, damit Debitoren nur wenige Einstellungen ändern müssen, nachdem das Paket angewendet wurde. Wenn Sie beispielsweise einen neuen Mandanten erstellen, wird Tabelle 308 **Nr-Serien** und Tabelle 309 **Nr. Serienzeile**  mit einer Reihe von Nummernserien und Startnummern ausgefüllt. Die entsprechenden **Nummernserie**-Felder in den Einrichtungstabellen werden ebenfalls automatisch ausgefüllt. Sie müssen die Nummernserien und andere grundlegende Einrichtungsdaten nicht selbst eingeben. Sie können alle standardmäßigen Daten auch manuell ändern, die mit RapidStart Services verwendet werden, indem Sie das Konfigurationsarbeitsblatt verwenden.  

Die Konfigurationspakete werden für einen vorkonfigurierten Mandanten erstellt. Nachdem Sie einen Mandanten eingerichtet haben, der Ihre Anforderungen erfüllt, können Sie ein Konfigurationspaket erstellen, das alle relevanten Daten von diesem Mandanten enthält. Sie können sie dann verwenden, wenn Sie einen neuen Mandanten erstellen, der auf die gleiche Weise konfiguriert werden soll.  

Um den Import von Stammdaten, wie Debitoren-, und Kreditorinformationen, zu erleichtern, können Sie Konfigurationsvorlagen verwenden. Konfigurationsvorlagen enthalten eine Reihe von Standardeinstellungen, die automatisch den Datensätzen zugeordnet werden, die in [!INCLUDE[prod_short](includes/prod_short.md)] importiert werden.

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Planen Sie eine Mandantenkonfiguration, indem Sie in den Konfigurationsvorschlag ausfüllen.|[So verwalten Sie eine Mandantenkonfiguration in einem Arbeitsblatt](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Erstellen Sie ein Konfigurationspaket, passen Sie ein Paket an, weisen Sie einem Paket Tabellen, zu überprüfen oder Bearbeiten Sie vorhandene Debitorendaten, erstellen Sie den neuen Mandanten und bewegen Sie dann Prüfdaten auf die Fertigungsumgebungen.|[So bereiten Sie ein Konfigurationspaket vofr](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a>Siehe auch  
[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
