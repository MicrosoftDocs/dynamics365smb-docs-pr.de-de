---
title: Verwalten, löschen oder komprimieren von Belegen | Microsoft Docs
description: Speichern Sie die historischen Daten oder löschen Sie sie.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 7f0024f54979a563e885242d7160bc2b615493a5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1246630"
---
# <a name="manage-documents"></a>Verwalten von Belegen
Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

## <a name="delete-documents"></a>Belege löschen
Es kann gelegentlich erforderlich sein, erledigte Einkaufsbestellungen zu löschen, die noch nicht gelöscht wurden. [!INCLUDE[d365fin](includes/d365fin_md.md)] überprüft, ob Sie die gelöschten Bestellungen vollständig fakturiert haben. Sie können keine Bestellungen löschen, die noch nicht vollständig geliefert und fakturiert wurden.  

Reklamationen werden üblicherweise gelöscht, nachdem sie fakturiert wurden. Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Geb. Einkaufsgutschrift** übertragen. Ist das Kontrollkästchen **Rücklieferung bei Gutschrift** im Fenster **Kreditoren & Einkauf Einr.** aktiviert, wird sie auch auf die Seite **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Rahmenbestellungen werden nicht gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben. Sie können erledigte Rahmenbestellungen mit Hilfe der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.  

Verrechnete Serviceaufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten auf der Seite **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.  

Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern von der Seite **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

## <a name="see-also"></a>Siehe auch  
[Verwaltung](admin-setup-and-administration.md)  
