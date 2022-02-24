---
title: 'Designdetails: Artikelverfolgungszeilenseite | Microsoft Docs'
description: Lesen, wie der Fluss der Serien- und Chargennummern in Ihrem Lager verwaltet wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 77d53f959d778b3355ad563fede1dfe106ad1ec8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3184964"
---
# <a name="design-details-item-tracking-lines-page"></a>Designdetails – Artikelverfolgungszeilenfenster-Seite
Artikelverfolgungsdatensätze und Reservierungsdatensätze werden im Reservierungssystem erstellt, und ihre Verfügbarkeit wird dynamisch berechnet. Daten, die auf der **Artikelzeilen nachverfolgen**-Seite eingegeben werden, werden in einer temporären Version der Tabelle **Verfolgungsspezifikation** verwaltet. Wenn die Seite geschlossen wird, werden die aktiven Daten in der Tabelle **Reservierungsposten** bestätigt und die historischen Daten werden in der Tabelle **Verfolgungsspezifikation** bestimmt. Weitere Informationen finden Sie unter [Designdetails: Aktiv gegen historische Artikelverfolgungsposten](design-details-active-versus-historic-item-tracking-entries.md).  
  
Auswahllisten von den Feldern **Seriennummer** und **Chargennummer** zeigen eine Verfügbarkeit, die sowohl auf der Tabelle **Artikelposten** als auch der Tabelle **Reservierungsposten** basiert, ohne Datumsfilter. Die Matrix der Mengenfelder im Kopf des Fensters **Artikelnachverfolgungszeile** zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf den Zeilen der Seite eingegeben werden. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine Null **0** in den Feldern **Undefiniert** in der Kopfzeile der Seite angezeigt wird.  
  
Um den Fluss der Serien- und Chargennummern durch das Lager zu koordinieren, sind die folgenden Regeln für die Eingabe von Daten im **Artikelnachverfolgungszeilen**-Seiten vorhanden:  
  
* Für eingehende und ausgehende Artikelverfolgungszeilen können Sie eine Seriennummer, mit oder ohne Chargennummer, nicht mehrmals in derselben Instanz der **Artikelnachverfolgungszeile**-Seiten eingeben. Wenn Sie versuchen, eine Kombination von Serien- oder Chargennummern einzugeben, die bereits auf der Seite vorhanden ist, dann blockiert eine Fehlermeldung die Dateneingabe.  
* Für eingehende Artikelverfolgungszeilen können Sie den zugehörigen Beleg nicht buchen, wenn sich ein Artikel derselben Variante und mit derselben Seriennummer bereits im Lagerbestand befindet. Wenn Sie versuchen, eine positive Zeile für einen Lagerartikel mit derselben Variante und Seriennummer zu buchen, dann blockiert eine Fehlermeldung die Buchung. Für eingehende und ausgehende Artikelverfolgungszeilen auf offenen Belegen können Sie jedoch die gleiche Kombination von Serien- oder Chargennummern haben, die sich auf verschiedene Herkunftsbelegzeilen beziehen, d.h., die in verschiedenen Instanzen des **Artikelnachverfolgungszeilen**-Seiten vorhanden sind, bis der jeweilige Beleg gebucht ist.  
* Wenn der Artikel für die seriennummernspezifische Verfolgung oder die chargennummernspezifische Verfolgung eingerichtet ist, können Sie keine ausgehende Belegzeile erstellen, es sei denn, ein Artikel mit der definierten Serien- oder Chargennummer ist im Bestand vorhanden. Wenn Sie versuchen, einen ausgehenden Beleg Artikel mit einer Serien-/Chargennummer zu buchen, die sich nicht im Bestand befindet, dann blockiert eine Fehlermeldung die Buchung.  
  
Die Regeln für die Eingabe von Daten auf der Seite **Artikelnachverfolgungszeile** unterstützen auch die Kopplungsprinzipien, die die Auftragsnachverfolgung, die Planung und die Reservierung steuern. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung und Reservierungen“.](design-details-item-tracking-and-planning.md)  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)