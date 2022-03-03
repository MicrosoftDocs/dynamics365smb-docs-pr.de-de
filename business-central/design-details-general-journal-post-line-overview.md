---
title: Fibu-Buchungszeile - Überblick
description: In diesem Thema werden die Änderungen in Codeunit 12, Gen. B.-Bl.-Zeile, und ist der einzige Ort, an dem Hauptbuch-, MwSt.- und Debitoren- und Kreditorenbuch-Einträge eingefügt werden können.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 2a4d9715f6fdfaef63bf6ac4090bb71d86346e51
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8146696"
---
# <a name="general-journal-post-line-overview"></a>Fibu-Buchungszeile - Überblick

Codeunit 12, **Jnl.-Beitrags-Zeile**, ist das größte Anwendungsobjekt für Sachpostenbuchung und ist der einzige Bereich, um die Finanzbuchhaltung, MwSt. und Debitoren- und Kreditorenposten einzufügen. Diese Codeunit wird auch für Ausgleich-, Ausgleich aufheben- und Zurücksetzen-Arbeitsgänge verwendet.  
  
In Microsoft Dynamics NAV 2013 R2 wurde die Codeunit überarbeitet, da sie mit ca. 7.600 Codezeilen sehr groß geworden war. Die Architektur wurde geändert und die Codeunit vereinfacht uns somit leichter zu verwalten. In dieser Dokumentation werden die Änderungen beschrieben und Informationen bereitgestellt, die Sie für das Upgrade benötigen.  
  
## <a name="old-architecture"></a>Alte Architektur  
Die alte Architektur hatte die folgenden Funktionen:  
  
* Es wurde umfangreicher Gebrauch von globalen Variablen gemacht, wodurch sich die Möglichkeit verborgener Fehler aufgrund der Verwendung von Variablen mit dem falschen Bereich erhöhten.  
* Es gab viele lange Verfahren (mit mehr als 100 Codezeilen), die auch hohe zyklomatische Komplexität haten (das heißt, viele geschachtelte CASE, REPEAT-, IF-Anweisungen), durch die der Code sehr schwierig zu lesen und zu warten wurde.  
* Einige Verfahren, die nur lokal verwendet wurdne und nur lokal verwendet werden sollten, wurden nicht als lokale Variable markiert.  
* Die meisten Verfahren hatten keine Parameter und verwendeten globale Variablen. Einige verwendeten Parameter und setzten globale Variablen durch lokale Variablen außer Kraft.  
* Codeschemata für das Auffinden der Sachkonten und die Erstellung der Finanzbuchhaltung und MwSt.-Posten waren nicht standardisiert und variierten von Ort zu Ort. Darüber gab es viele Codeverdopplung und unterbrochene Symmetrie zwischen Debitoren- und Kreditorencode.  
* Ein großer Teil des Codes in Codeunit 12, in etwa 30 Prozent, bezog sich auf Rabatt- und Toleranzberechnungen, obwohl Diese Funktion in vielen Ländern oder Regionen nicht benötigt werden.  
* Buchen, Ausgleichen, Ausgleich aufheben, Zahlungsrabatt und -Toleranz und Wechselkursregulierung wurden in Codeunit 12 unter Verwendung einer langen Liste von globalen Variablen vereint.  
  
### <a name="new-architecture"></a>Neue Architektur  
In [!INCLUDE[prod_short](includes/prod_short.md)] hat Codeunit 12 die folgenden Verbesserungen:  
  
* Codeunit 12 ist in kleinere Verfahren umgestaltet worden (insgesamt weniger als 100 Codezeilen).  
* Standardisierte Muster für die Suche von Sachkonten wurden implementiert, indem Hilfsfunktionen aus den Buchungsgruppen verwendet wurden.  
* Ein Buchungs-Modul-Framework wurde implementiert, um den Startund das Ende von Transaktionen zu verwalten und die Erstellung auf Sach- und MwSt.-Posten zu isolieren, die Sammlung von MwSt.-Ausgleich und die Berechnung von zusätzlichen Währungsbeträgen.  
* Codeverdopplung ist gelöscht worden.  
* Viele Hilfsfunktionen wurden zu den entsprechenden Debitoren- und Kreditorenpostentabellen übertragen.  
* Die Verwendung von globalen Variablen ist minimiert worden, sodass jedes Verfahren Parameter verwendet und eine eigene Anwendungslogik enthält.  
  
## <a name="see-also"></a>Siehe auch

[Designdetails: Buchungs-Schnittstellenstruktur](design-details-posting-interface-structure.md)  
[Designdetails: Buchungs-Modul-Struktur](design-details-posting-engine-structure.md)  
[Designdetails: Fibu Buch.-Blatt-Beitrags-Zeile (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]