---
title: Design-Details – Buchungsstruktur für die Artikelverfolgung
description: 'Erfahren Sie, wie Sie Sachkonto-Einträge als primären Spediteur für Artikelverfolgungsnummern in der Buchungsstruktur für die Artikelverfolgung verwenden können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-item-tracking-posting-structure"></a>Designdetails: Artikelverfolgungs-Buchungsstruktur
Um der Bestandskalkulationsfunktionen zu entsprechen und eine einfachere und robustere Lösung zu erhalten, werden Artikelposten als der primäre Träger von Artikelverfolgungsnummern verwendet.  
  
Artikelverfolgungsnummern auf Auftragsnetzwerkeinheiten und nicht auftragsbezogenen Netzwerkeinheiten werden in der Tabelle **Reservierungsposten** (T337) angegeben. Artikelverfolgungsnummern, die mit den historischen Informationen verknüpft sind, werden direkt aus den Artikelposten abgerufen, die mit der jeweiligen Transaktion verknüpft werden. Das bedeutet, dass Artikelposten die Artikelverfolgungsspezifikationen der gebuchten Auftragszeile widerspiegeln.  
  
Die Seite **Artikelverfolgungszeilen** ruft die Informationen aus T337 und den Artikelposten ab und zeigt sie in der temporären Tabelle, **Verfolgungsspezifikation** (T336) an. T336 enthält auch die temporären Dateien im **Fenster Artikelverfolgungsseiten** für Artikelverfolgungsmengen, die noch fakturiert werden müssen.  
  
## <a name="one-to-many-relation"></a>1:n-Beziehung
Die Tabelle **Artikelpostenverbindung**, die verwendet wird, um eine gebuchte Belegzeile mit den entsprechenden Artikelposten zu verknüpfen, besteht aus zwei Hauptteilen:  
  
* Ein Verweis zu der gebuchten Belegzeile, das Feld **Auftragszeilennr.**. Feld  
* Eine Postennummer, die auf einem Artikelposten verweist, das Feld **Artikelposten Lfd. Nr.**.  
  
Die Funktionen des vorhandenen **Lfd. Nr.**- Feldes, das einen Artikelposten mit einer gebuchten Belegzeile verknüpft, bearbeitet die typische Eins-zu-eins-Verknüpfung, wenn keine Artikelverfolgungsnummern auf der gebuchten Belegzeile vorhanden sind. Wenn Artikelverfolgungsnummern vorhanden sind, bleibt das Feld **Lfd. Nr.** leer, und die Eins-zu-viele-Relation wird durch die Tabelle **Artikelpostenverbindung** verarbeitet. Wenn die gebuchte Belegzeile Artikelverfolgungsnummern enthält, sich jedoch nur auf einem einzelnen Artikelposten bezieht, verarbeitet das Feld **Lfd. Nr.** die Verknüpfung, und es wird kein Datensatz in der Tabelle **Artikelpostenverbindung** erstellt.  
  
## <a name="codeunits-80-sales-post--and-90-purch-post"></a>Codeunits 80 (Verkaufsbuchung) und 90 (Einkaufsbuchung)
Um die Artikelposten für die Buchung zu teilen, ist der Code in Codeunit 80 und in Codeunit 90 durch Schleifen eingekreist, die durch globale temporäre Datensatzvariablen laufen. Dieser Code ruft Codeeinnheit 22 mit einer Artikel Buch.-Blattzeile auf. Diese Variablen werden initialisiert, wenn Artikelverfolgungsnummern für die Belegzeile vorhanden sind. Um den Code einfach zu halten, wird diese Schleifenstruktur immer verwendet. Wenn keine Artikelverfolgungsnummern für die Belegzeile vorhanden, wird ein einzelner Datensatz eingefügt, und die Schleife wird einmal ausgeführt.  
  
## <a name="posting-the-item-journal"></a>Buchen des Artikel Buch.-Blatts.
Die Übertragung der Artikelverfolgungsnummern erfolgt über die Reservierungseinträge, die sich auf den Artikelposten beziehen und die Schleife durch die Artikelverfolgungsnummern erfolgt in Codeunit 22 (Artikelposten-Buchungszeile). Das Konzept arbeitet gleich wie wenn eine Artikel Buch.-Blattzeile indirekt verwendet wird, um einen Einkauf oder eine Einkaufsbestellung beispielsweise zu buchen, wenn die Artikel Buch.-Blattzeile direkt verwendet wird. Wenn das Artikel Buch.-Blatt direkt verwendet wird, auf das Feld **Quellzeile ID** der Artikel Buch.-Blattzeile selbst.  
  
## <a name="code-unit-22--item-jnl-post-line"></a>Codeeinheit 22 (Artikelbuchungszeile)
Die Codeunits 80 (Verkauf-Buchen) und 90 (Einkauf-Buchen) schleifen den Aufruf der Codeunit 22 (Artikelposten-Buchungszeile) während der Rechnungsbuchung von Artikeltrackingnummern und während der Rechnungsstellung vorhandener Lieferungen oder Wareneingänge.  
  
Während der Mengenbuchung von Artikelverfolgungsnummern ruft die Codeunit 22 (Artikelposten-Buchungszeile) Artikelverfolgungsnummern aus den Einträgen in T337 (Reservierungseintrag) ab, die sich auf die Buchung beziehen. Diese Posten werden direkt in die Artikel Buch.-Blattzeile gesetzt.  
  
Codeunit 22 (Artikelposten – Buchungszeile) durchläuft die Artikelverfolgungsnummern und teilt die Buchung in die entsprechenden Artikelposten auf, die die Artikelverfolgungsnummern tragen. Informationen darüber, welche Artikelposten erstellt werden, werden an T337 (Reservierungsposten) zurückgegeben, indem ein temporärer T336-Datensatz verwendet wird, der von einer Prozedur in Codeunit 22 aufgerufen wird. Dieses Verfahren wird gestartet, wenn Codeunit 22 seine Ausführung beendet, da für diesen Artikel, das Objekt der Codeunit 22 die Informationen enthält. Wenn der temporäre T336-Datensatz abgerufen wird, erstellen die Codeunits 80 (Verkaufsbuchung) und 90 (Einkaufsbuchung) Datensätze in der Tabelle  **Artikeleintragsrelation**, um die erstellten Artikelposten der erstellten Liefer- oder Empfangszeile zu verknüpfen. Die Codeunits 80 (Verkaufsbuchung) und 90 (Einkaufsbuchung) konvertieren dann die temporären T336-Datensätze (Tracking-Spezifikation) in echte T336-Datensätze (Tracking-Spezifikation), die sich auf die betreffende Zeile beziehen. Jedoch tritt diese Konvertierung nur auf, wenn die gebuchte Belegzeile nicht gelöscht wird, da sie nur teilweise gebucht wird.  
  
## <a name="see-also"></a>Siehe auch
[Designdetails: Artikelnachverfolgung](design-details-item-tracking.md)   
[Designdetails: Artikelverfolgungsdesign](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
