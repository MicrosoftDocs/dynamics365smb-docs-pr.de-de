---
title: Datenbank-Sperren anzeigen
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: abee0f31d66f648f4b0be567d8599b31c536a193
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324102"
---
# <a name="viewing-database-locks"></a>Anzeigen von Datenbank-Sperren

## <a name="about-locks"></a>Über Sperren

Die Datenbanksperre steuert den gleichzeitigen Zugriff mehrerer Benutzer auf dieselben Daten. Um eine Transaktion gegen andere Transaktionen zu schützen, die dieselben Daten ändern, sperrt die erste Transaktion die Daten. Die Sperre bleibt bestehen, bis die Transaktion abgeschlossen ist.

Benutzer können für den Abschluss von Transaktionen mit den gesperrten Daten gesperrt werden. Sie erhalten in der Regel eine Meldung, die den Sperrzustand anzeigt.

## <a name="to-view-database-locks"></a>So zeigen Sie Datenbanksperren an

Wählen Sie das Symbol ![Seite suchen oder Bericht](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht"), geben Sie **Datenbanksperren** ein, und wählen Sie dann den entsprechenden Link.

Die Seite **Datenbanksperren** zeigt eine Momentaufnahme aller aktuellen Datenbanksperren.

Weitere Informationen über Datenbanksperren finden Sie unter [Überwachung von Datenbanksperren](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in der Hilfe für Business Central Entwickler und IT Pro.

## <a name="see-also"></a>Siehe auch

[Datenbanksperren überwachen](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
