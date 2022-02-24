---
title: 'Designdetails: Artikelverfolgungsdesign | Microsoft Docs'
description: Dieses Thema beschreibt den Entwurf hinter der Artikelverfolgung in  Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: cda50dc7c3a0377c36f7bce4eca9c1c5cb5b093e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185060"
---
# <a name="design-details-item-tracking-design"></a>Designdetails: Artikelverfolgungsdesign
In der ersten Version der Artikelverfolgung in [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60 wurden Seriennummern oder Chargennummern direkt in Artikelposten erfasst. Dieses Design bot vollständige Verfügbarkeitsinformationen und einfache Nachverfolgung von historischen Posten, aber es ermangelte Flexibilität und Funktionen.  

Ab [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00, befand sich die Artikelverfolgungsfunktion in einer separaten Objektstruktur mit verwickelten Links zu den gebuchten Belegen und den Artikelposten. Dieses Design war flexibel und reich an Funktionen, aber Artikelverfolgungsposten wurden nicht vollständig in Verfügbarkeitsberechnungen einbezogen.  

Seit [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 sind Artikelverfolgungsfunktionen mit dem Reservierungssystem integriert, das Reservierung, Auftragsnachverfolgung und Aktionsmessaging verarbeitet. Weitere Informationen finden Sie unter „Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen“ in „Designdetails: Beschaffungsplanung“.  

Dieses neueste Design enthält Artikelverfolgungsposten in der Gesamtverfügbarkeitsberechnung im gesamten System, einschließlich Planungs-, Produktions- und Lagerfunktionen. Der alte Konzept der Verwendung von Serien- und Chargennummern in den Artikelposten wird erneut eingeführt, um den einfachen Zugriff auf historische Daten für Artikelnachverfolgungszwecke zu ermöglichen. In Verbindung mit Artikelnachverfolgungsverbesserungen in [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 wurde das Reservierungssystem auf Nicht.Auftragsnetzwerk-Entitäten erweitert, wie wie Buch.-Blätter, Rechnungen und Gutschriften.  

Mit der Hinzufügung der Serien- oder Chargennummern verarbeitet das Reservierungssystem permanent Artikelattribute sowie periodische Verknüpfungen zwischen Angebot und Nachfrage in Form von Bedarfsverursacherposten und -Reservierungsposten. Ein weitere Eigenschaft der Serien- oder Chargennummern gegenüber herkömmlichen Reservierungsdaten ist die Tatsache, dass diese teilweise oder vollständig gebucht werden können. Daher funktioniert die Tabelle **Reservierungsposten** (T337) jetzt mit einer zugehörigen Tabelle, der Tabelle **Verfolgungsspezifikation** (T336), die das Summieren über aktive und gebuchte Artikelnachverfolgungsmengen hinweg verwaltet und anzeigt. Weitere Informationen finden Sie unter [Designdetails: Aktiv gegen historische Artikelverfolgungsposten](design-details-active-versus-historic-item-tracking-entries.md).  

Das folgende Diagramm illustriert das Design von Artikelverfolgungsfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

![Beispiel für den Fluss der Artikelverfolgung](media/design_details_item_tracking_design.png "Beispiel für den Fluss der Artikelverfolgung")  

Das zentrale Buchungsobjekt wird überarbeitet, um die besondere Subklassifikation einer Belegzeile in Form von Serien- oder Chargennummern zu bearbeiten, und bestimmte Beziehungstabellen werden hinzugefügt, um die 1-zu-viele-Relationen zwischen gebuchten Belegen und deren geteilten Artikelposten bzw. Wertposten zu erstellen.  

Codeunit 22, **Artikelposten – Zeile buchen** teilt jetzt die Buchung nach Artikelverfolgungsnummern, die auf der Belegzeile angegebenen sind. Jede einzelne Artikelverfolgungsnummer auf der Zeile erstellt ihren eigenen Artikelposten für den Artikel. Dies bedeutet, dass die Verknüpfung von der gebuchten Belegzeile zu den entsprechenden Artikelposten jetzt eine Relation von einem zu mehreren ist. Diese Verknüpfung wird von den folgenden Artikelnachverfolgungs-Beziehungstabellen verarbeitet.  

|Feld|Beschreibung|  
|---------------|---------------------------------------|  
|**Artikelpostenverbindung** (T6507)|Inbezugsetzen gelieferter oder erhaltener Zeilen zu Artikelposten|  
|**Wertpostenverbindung** (T6508)|Inbezugsetzen fakturierter Zeilen zu Wertposten|  

Weitere Informationen finden Sie unter [Designdetails: Artikelbuchungsstruktur nachverfolgen](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)
