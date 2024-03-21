---
title: "Designdetails\_– Artikelverfolgungsdesign"
description: 'In diesem Thema wird das Design der Artikelverfolgung in Business Central beschrieben, wenn diese über Produktversionen hinweg ausgereift ist.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-item-tracking-design"></a>Designdetails: Artikelverfolgungsdesign

Artikelverfolgung in [!INCLUDE[prod_short](includes/prod_short.md)] begann mit [!INCLUDE [navnow_md](includes/navnow_md.md)]. Die Artikelverfolgungsfunktion befindet sich in einer separaten Objektstruktur mit komplexen Links zu gebuchten Dokumenten und Artikelposten und ist in das Reservierungssystem integriert, das Reservierung, Auftragsverfolgung und Aktionsnachrichten verwaltet. Weitere Informationen finden Sie unter [Designdetails: Reservierung, Auftragsnachverfolgung und Aktionsmeldungen](design-details-reservation-order-tracking-and-action-messaging.md) in den Beschaffungsplanungsdetails.  

Dieses Design enthält Artikelverfolgungsposten in der Gesamtverfügbarkeitsberechnung im gesamten System, einschließlich Planungs-, Produktions- und Lagerfunktionen. Serien- und Chargennummern in den Artikelposten werden angewendet, um den einfachen Zugriff auf historische Daten für Artikelnachverfolgungszwecke zu ermöglichen. Mit dem Veröffentlichungszyklus 1 von 2021 enthält die Artikelverfolgung in [!INCLUDE [prod_short](includes/prod_short.md)] Paketnummern.  

Mit der Hinzufügung der Serien-, Chargen‑ und Paketnummern verarbeitet das Reservierungssystem permanent Artikelattribute sowie periodische Verknüpfungen zwischen Angebot und Nachfrage in Form von Bedarfsverursacherposten und -Reservierungsposten. Ein weitere Eigenschaft der Serien- oder Chargennummern gegenüber herkömmlichen Reservierungsdaten ist die Tatsache, dass diese teilweise oder vollständig gebucht werden können. Daher funktioniert die Tabelle **Reservierungsposten** (T337) jetzt mit einer zugehörigen Tabelle, der Tabelle **Verfolgungsspezifikation** (T336), die das Summieren über aktive und gebuchte Artikelnachverfolgungsmengen hinweg verwaltet und anzeigt. Weitere Informationen finden Sie unter [Designdetails: Aktiv gegen historische Artikelverfolgungsposten](design-details-active-versus-historic-item-tracking-entries.md).  

Das folgende Diagramm illustriert das Design von Artikelverfolgungsfunktionen in [!INCLUDE[prod_short](includes/prod_short.md)].  

![Beispiel für einen Item Tracking Flow.](media/design_details_item_tracking_design.png "Beispiel für den Fluss der Artikelverfolgung")  

Das zentrale Buchungsobjekt wird überarbeitet, um die besondere Subklassifikation einer Belegzeile in Form von Serien- oder Chargennummern zu bearbeiten, und bestimmte Beziehungstabellen werden hinzugefügt, um die 1-zu-viele-Relationen zwischen gebuchten Belegen und deren geteilten Artikelposten bzw. Wertposten zu erstellen.  

Codeunit 22, **Artikelposten – Zeile buchen** teilt jetzt die Buchung nach Artikelverfolgungsnummern, die auf der Belegzeile angegebenen sind. Jede einzelne Artikelverfolgungsnummer auf der Zeile erstellt ihren eigenen Artikelposten für den Artikel. Dies bedeutet, dass die Verknüpfung von der gebuchten Belegzeile zu den entsprechenden Artikelposten jetzt eine Relation von einem zu mehreren ist. Diese Verknüpfung wird von den folgenden Artikelnachverfolgungs-Beziehungstabellen verarbeitet.  

|Feld|Beschreibung|  
|---------------|---------------------------------------|  
|**Artikelpostenverbindung** (T6507)|Inbezugsetzen gelieferter oder erhaltener Zeilen zu Artikelposten|  
|**Wertpostenverbindung** (T6508)|Inbezugsetzen fakturierter Zeilen zu Wertposten|  

Weitere Informationen finden Sie unter [Designdetails: Artikelbuchungsstruktur nachverfolgen](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Siehe auch

[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
