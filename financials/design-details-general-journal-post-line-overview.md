---
title: "Fibu-Buchungszeile - Überblick | Microsoft Docs"
description: "Dieses Thema enthält Änderungen für Codeunit 12, **Jnl.-Beitrags-Zeile**, welche das größte Anwendungsobjekt für Sachpostenbuchung ist und der einzige Bereich, um in der Finanzbuchhaltung MwSt. und Debitoren- und Kreditorenposten einzufügen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 77fa52505dc586dc11ca89e53f6eec75042d3606
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="general-journal-post-line-overview"></a>Fibu-Buchungszeile - Überblick
Codeunit 12, **Jnl.-Beitrags-Zeile**, ist das größte Anwendungsobjekt für Sachpostenbuchung und ist der einzige Bereich, um die Finanzbuchhaltung, MwSt. und Debitoren- und Kreditorenposten einzufügen. Diese Codeunit wird auch für Ausgleich-, Ausgleich aufheben- und Zurücksetzen-Arbeitsgänge verwendet.  
  
Während die Codeunit in jeder Version in den letzten zehn Jahre verbessert wurde, blieb die Architektur im Wesentlichen unverändert. Die Codeunit wurde mit ungefähr 7.600 Codezeilen sehr umfangreich. Mit dieser Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] wird die Architektur geändert und die Codeunit wurde einfacher und leichter zu verwalten. Diese Dokumentation stellt die Änderungen vor und enthält Informationen, die Sie für das Upgrade benötigen.  
  
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
In [!INCLUDE[d365fin](includes/d365fin_md.md)] hat Codeunit 12 die folgenden Verbesserungen:  
  
* Codeunit 12 ist in kleinere Verfahren umgestaltet worden (insgesamt weniger als 100 Codezeilen).  
* Standardisierte Muster für die Suche von Sachkonten wurden implementiert, indem Hilfsfunktionen aus den Buchungsgruppen verwendet wurden.  
* Ein Buchungs-Modul-Framework wurde implementiert, um den Startund das Ende von Transaktionen zu verwalten und die Erstellung auf Sach- und MwSt.-Posten zu isolieren, die Sammlung von MwSt.-Ausgleich und die Berechnung von zusätzlichen Währungsbeträgen.  
* Codeverdopplung ist gelöscht worden.  
* Viele Hilfsfunktionen wurden zu den entsprechenden Debitoren- und Kreditorenpostentabellen übertragen.  
* Die Verwendung von globalen Variablen ist minimiert worden, sodass jedes Verfahren Parameter verwendet und eine eigene Anwendungslogik enthält.  
  
## <a name="see-also"></a>Siehe auch  
[Designdetails: Buchungs-Schnittstellenstruktur](design-details-posting-interface-structure.md)   
[Designdetails: Buchungs-Modul-Struktur](design-details-posting-engine-structure.md)

