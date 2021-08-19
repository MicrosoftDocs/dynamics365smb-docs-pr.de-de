---
title: Richten Sie eine Unternehmenskonfiguration ein.
description: Richten Sie als Partner Business Central für Ihren Kunden mit Standard- oder kundenspezifischen Konfigurationen ein, die Sie in Konfigurationspaketen bündeln.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5baef81f22e260fa6f582b536dcf356d3ae25d25
ms.sourcegitcommit: ecbabd2d0fdf2566cea4a05a25b09ff6ca6256c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "6649712"
---
# <a name="set-up-company-configuration"></a>Richten Sie eine Unternehmenskonfiguration ein.
Der Implementierungsprozess beginnt mit dem Microsoft-Partner. Als Partner sind Sie für die Formulierung der Konfigurationsdetails und das Erstellen eines Pakets zuständig ist, das ein Debitor einfach anwenden kann. Bevor Sie einen neuen Mandanten in [!INCLUDE [prod_short](includes/prod_short.md)] online oder on-premises erstellen, sollten Sie planen, wie dieser konfiguriert wird. Sie müssen an grundlegende Einrichtungsdaten und die Arten der Daten denken, die Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Lösung benötigt. Sie bündeln alle diese Informationen in Konfigurationspakete.

RapidStart Services gibt außerdem die Werkzeuge, die Sie verwenden, um die Stammdaten zu migrieren, beispielsweise Debitoren und Kreditoren.  

Es ist empfehlenswert, dass Sie Konfigurationspakete erstellen, bei denen die meisten Einrichtungstabellen bereits ausgefüllt sind, damit Debitoren nur wenige Einstellungen ändern müssen, nachdem das Paket angewendet wurde. Wenn Sie beispielsweise einen neuen Mandanten erstellen, wird Tabelle 308 **Nr-Serien** und Tabelle 309 **Nr. Serienzeile**  mit einer Reihe von Nummernserien und Startnummern ausgefüllt. Die entsprechenden **Nummernserie**-Felder in den Einrichtungstabellen werden ebenfalls automatisch ausgefüllt. Sie müssen die Nummernserien und andere grundlegende Einrichtungsdaten nicht selbst eingeben. Sie können alle standardmäßigen Daten auch manuell ändern, die mit RapidStart Services verwendet werden, indem Sie das Konfigurationsarbeitsblatt verwenden.  

Die Konfigurationspakete werden für einen vorkonfigurierten Mandanten erstellt. Nachdem Sie einen Mandanten eingerichtet haben, der Ihre Anforderungen erfüllt, können Sie ein Konfigurationspaket erstellen, das alle relevanten Daten von diesem Mandanten enthält. Sie können sie dann verwenden, wenn Sie einen neuen Mandanten erstellen, der auf die gleiche Weise konfiguriert werden soll.  

Um den Import von Stammdaten, wie Debitoren-, und Kreditorinformationen, zu erleichtern, können Sie Konfigurationsvorlagen verwenden. Konfigurationsvorlagen enthalten eine Reihe von Standardeinstellungen, die automatisch den Datensätzen zugeordnet werden, die in [!INCLUDE[prod_short](includes/prod_short.md)] importiert werden.

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Planen Sie eine Mandantenkonfiguration, indem Sie das Konfigurationsarbeitsblatt ausfüllen.|[So verwalten Sie eine Mandantenkonfiguration in einem Arbeitsblatt](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|Erstellen Sie ein Konfigurationspaket, passen Sie ein Paket an, weisen Sie einem Paket Tabellen, zu überprüfen oder Bearbeiten Sie vorhandene Debitorendaten, erstellen Sie den neuen Mandanten und bewegen Sie dann Prüfdaten auf die Fertigungsumgebungen.|[So bereiten Sie ein Konfigurationspaket vofr](admin-how-to-prepare-a-configuration-package.md)|

Sie können auch Konfigurationspakete mit Standardkonfigurationen erstellen, die Sie immer wieder verwenden können. Weitere Informationen finden Sie unter [Einrichten von Standard-Unternehmenskonfigurationspaketen](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) in den Entwickler- und Verwaltungsinhalten.  

## <a name="see-also"></a>Weitere Informationen

[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]