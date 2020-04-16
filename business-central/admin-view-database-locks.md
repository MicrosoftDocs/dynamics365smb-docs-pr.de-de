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
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196380"
---
# <a name="viewing-database-locks"></a>Anzeigen von Datenbank-Sperren

## <a name="about-locks"></a>Über Sperren

Die Datenbanksperre steuert den gleichzeitigen Zugriff mehrerer Benutzer auf dieselben Daten. Um eine Transaktion gegen andere Transaktionen zu schützen, die dieselben Daten ändern, sperrt die erste Transaktion die Daten. Die Sperre bleibt bestehen, bis die Transaktion abgeschlossen ist.

Benutzer können für den Abschluss von Transaktionen mit den gesperrten Daten gesperrt werden. Sie erhalten in der Regel eine Meldung, die den Sperrzustand anzeigt.

## <a name="to-view-database-locks"></a>So zeigen Sie Datenbanksperren an

Wählen Sie das Symbol ![Seite suchen oder Bericht](media/ui-search/search_small.png "Suchen Sie nach dem Symbol Seite oder Bericht"), geben Sie **Datenbanksperren** ein, und wählen Sie dann den entsprechenden Link.

Die Seite **Datenbanksperren** zeigt eine Momentaufnahme aller aktuellen Datenbanksperren.

Weitere Informationen über Datenbanksperren finden Sie unter [Überwachung von Datenbanksperren](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in der Hilfe für Business Central Entwickler und IT Pro.

## <a name="see-also"></a>Siehe auch

[Datenbanksperren überwachen](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
