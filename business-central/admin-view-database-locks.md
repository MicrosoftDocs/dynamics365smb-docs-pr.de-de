---
title: Datenbank-Sperren anzeigen
description: Erfahren Sie, wie Sie Informationen über Datenbanksperren direkt über die Clientschnittstelle in Business Central anzeigen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 640608b810f3ad9812decc493ad4e35bcc316f98
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388149"
---
# <a name="viewing-database-locks"></a>Anzeigen von Datenbank-Sperren

Die Datenbanksperre steuert den gleichzeitigen Zugriff mehrerer Benutzer auf dieselben Daten. Um eine Transaktion gegen andere Transaktionen zu schützen, die dieselben Daten ändern, sperrt die erste Transaktion die Daten. Die Sperre bleibt bestehen, bis die Transaktion abgeschlossen ist.

Benutzer können für den Abschluss von Transaktionen mit den gesperrten Daten gesperrt werden. Sie erhalten in der Regel eine Meldung, die den Sperrzustand anzeigt.

## <a name="to-view-database-locks"></a>So zeigen Sie Datenbanksperren an

Wählen Sie das Symbol ![Seite suchen oder Bericht](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht"), geben Sie **Datenbanksperren** ein, und wählen Sie dann den entsprechenden Link.

Die Seite **Datenbanksperren** zeigt eine Momentaufnahme aller aktuellen Datenbanksperren.

Weitere Informationen über Datenbanksperren finden Sie unter [Überwachung von Datenbanksperren](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in der Hilfe für Business Central Entwickler und IT Pro.

## <a name="see-also"></a>Siehe auch

[Datenbanksperren überwachen](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]