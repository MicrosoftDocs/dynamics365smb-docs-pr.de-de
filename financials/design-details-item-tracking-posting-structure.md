---
title: Design Details - Artikelverfolgungs-Buchungsstruktur | Microsoft Docs
description: "Erfahren Sie, wie der Artikelposten als primäre Transportmitteln von Artikelverfolgungsnummern verwendet wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item tracking, posting, inventory
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 72de5863bf2e7c64078a9ca5421202f00f439250
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-posting-structure"></a>Designdetails: Artikelverfolgungs-Buchungsstruktur
Um der Bestandskalkulationsfunktionen zu entsprechen und eine einfachere und robustere Lösung zu erhalten, werden Artikelposten als der primäre Träger von Artikelverfolgungsnummern verwendet.  
  
Artikelverfolgungsnummern auf Auftragsnetzwerkeinheiten und nicht auftragsbezogenen Netzwerkeinheiten werden in der Tabelle **Reservierungsposten** (T337) angegeben. Artikelverfolgungsnummern, die mit den historischen Informationen verknüpft sind, werden direkt aus den Artikelposten abgerufen, die mit der jeweiligen Transaktion verknüpft werden. Das bedeutet, dass Artikelposten die Artikelverfolgungsspezifikationen der gebuchten Auftragszeile widerspiegeln.  
  
Das Fenster **Artikelverfolgungszeilen** ruft die Informationen aus T337 und den Artikelposten ab und zeigt sie in der temporären Tabelle, **Verfolgungsspezifikation** (T336) an. T336 enthält auch die temporären Dateien im **Fenster Artikelverfolgungszeilen** für Artikelverfolgungsmengen, die noch fakturiert werden müssen.  
  
## <a name="one-to-many-relation"></a>1:n-Beziehung  
Die Tabelle **Artikelpostenverbindung**, die verwendet wird, um eine gebuchte Belegzeile mit den entsprechenden Artikelposten zu verknüpfen, besteht aus zwei Hauptteilen:  
  
* Ein Verweis zu der gebuchten Belegzeile, das Feld **Auftragszeilennr.**. Feld  
* Eine Postennummer, die auf einem Artikelposten verweist, das Feld **Artikelposten Lfd. Nr.**.  
  
Die Funktionen des vorhandenen **Lfd. Nr.**- Feldes, das einen Artikelposten mit einer gebuchten Belegzeile verknüpft, bearbeitet die typische Eins-zu-eins-Verknüpfung, wenn keine Artikelverfolgungsnummern auf der gebuchten Belegzeile vorhanden sind. Wenn Artikelverfolgungsnummern vorhanden sind, bleibt das Feld **Lfd. Nr.** leer, und die Eins-zu-viele-Relation wird durch die Tabelle **Artikelpostenverbindung** verarbeitet. Wenn die gebuchte Belegzeile Artikelverfolgungsnummern enthält, sich jedoch nur auf einem einzelnen Artikelposten bezieht, verarbeitet das Feld **Lfd. Nr.** die Verknüpfung, und es wird kein Datensatz in der Tabelle **Artikelpostenverbindung** erstellt.  
  
## <a name="codeunits-80-and-90"></a>Codeunit 80 und 90  
Um die Artikelposten für die Buchung zu teilen, ist der Code in Codeunit 80 und in Codeunit 90 durch Schleifen eingekreist, die durch globale temporäre Datensatzvariablen laufen. Dieser Code ruft Codeeinnheit 22 mit einer Artikel Buch.-Blattzeile auf. Diese Variablen werden initialisiert, wenn Artikelverfolgungsnummern für die Belegzeile vorhanden sind. Um den Code einfach zu halten, wird diese Schleifenstruktur immer verwendet. Wenn keine Artikelverfolgungsnummern für die Belegzeile vorhanden, wird ein einzelner Datensatz eingefügt, und die Schleife wird einmal ausgeführt.  
  
## <a name="posting-the-item-journal"></a>Buchen des Artikel Buch.-Blatts.  
Artikelverfolgungsnummern werden über die Reservierungsposten übertragen, die mit dem Artikelposten verknüpft sind, und der Kreis durch die Artikelverfolgungsnummern erfolgt in Codeunit 22. Das Konzept arbeitet gleich wie wenn eine Artikel Buch.-Blattzeile indirekt verwendet wird, um einen Einkauf oder eine Einkaufsbestellung beispielsweise zu buchen, wenn die Artikel Buch.-Blattzeile direkt verwendet wird. Wenn das Artikel Buch.-Blatt direkt verwendet wird, auf das Feld **Quellzeile ID** der Artikel Buch.-Blattzeile selbst.  
  
## <a name="code-unit-22"></a>Code Unit 22  
Codeunit 80 und 90 durchlaufen den Aufruf von Codeunit 22 während der Rechnungsbuchung von Artikelverfolgungsnummern und während der Fakturierung der vorhandenen Lieferungen oder Wareneingänge.  
  
Während der Mengenbuchung von Artikelverfolgungsnummern ruft Codeunit 22 Artikelverfolgungsnummern aus den Posten in T337 ab, die sich auf die Buchung beziehen. Diese Posten werden direkt in die Artikel Buch.-Blattzeile gesetzt.  
  
Codeunit 22 durchläuft die Artikelverfolgungsnummern und teilt die Posten in die entsprechenden Artikelposten ein, die die Artikelverfolgungsnummern enthalten. Informationen darüber, welche Artikelposten erstellt werden, werden auf T337 zurückgegeben, indem ein temporärer Datensatz T336 verwendet wird, der durch ein Verfahren in Codeunit 22 aufgerufen wird. Dieses Verfahren wird gestartet, wenn Codeunit 22 seine Ausführung beendet, da für diesen Artikel, das Objekt der Codeunit 22 die Informationen enthält. Wenn der temporäre Datensatz T336 abgerufen wird, erstellen Codeunit 80 und 90 Datensätze in der Tabelle **Artikelpostenverbindung**, um die erstellten Artikelposten mit der erstellten Lieferung oder der Lieferzeile zu verknüpfen. Codeunit 80 oder Codeunit 90 konvertiert dann die temporären T336-Datensätze zu realen T336-Datensätzen, die zu der jeweiligen Zeile gehören. Jedoch tritt diese Konvertierung nur auf, wenn die gebuchte Belegzeile nicht gelöscht wird, da sie nur teilweise gebucht wird.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)   
[Designdetails: Artikelverfolgungsdesign](design-details-item-tracking-design.md)
