---
title: "Verwalten, löschen oder komprimieren von Belegen | Microsoft Docs"
description: "Speichern Sie die historischen Daten oder löschen Sie sie."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 60438f0b6f0d5da60925b5b9c309cc359a8422e3
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Verwalten von Belegen
Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

## <a name="delete-documents"></a>Belege löschen
Es kann gelegentlich erforderlich sein, erledigte Einkaufsbestellungen zu löschen, die noch nicht gelöscht wurden. [!INCLUDE[d365fin](includes/d365fin_md.md)] überprüft, ob Sie die gelöschten Bestellungen vollständig fakturiert haben. Sie können keine Bestellungen löschen, die noch nicht vollständig geliefert und fakturiert wurden.  

Reklamationen werden üblicherweise gelöscht, nachdem sie fakturiert wurden. Wenn Sie eine Rechnung buchen, wird sie in das Fenster **Geb. Einkaufsgutschrift** übertragen. Ist das Kontrollkästchen **Rücklieferung bei Gutschrift** im Fenster **Kreditoren & Einkauf Einr.** aktiviert, wird sie auch in das Fenster **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Rahmenbestellungen werden nicht gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben. Sie können erledigte Rahmenbestellungen mit Hilfe der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.  

Verrechnete Serviceaufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten im Fenster **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann im Fenster **Gebuchte Servicerechnung** angezeigt werden.  

Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern im Fenster **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

## <a name="see-also"></a>Siehe auch  
[Einrichten und Verwaltung in Finance and Operations, Business edition](admin-setup-and-administration.md)  

