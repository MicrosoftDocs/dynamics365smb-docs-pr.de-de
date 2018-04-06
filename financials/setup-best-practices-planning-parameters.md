---
title: "Bewährte Vorgehensweisen einrichten - Planungsparameter | Microsoft Docs"
description: "Das Inforegister **Planung** auf der Artikelkarte ist Mittelpunkt der gesamten Lieferkette des Unternehmens. Das Einstellen eines richtigen Planungsparameters ist für die kosteneffektive Bestandskontrolle und einen sehr guten Debitorenservice sehr wichtig."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a9dfb17b0cbddb3d6b65e8d807dd92990c2ccdc1
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="setup-best-practices-planning-parameters"></a>Bewährte Einrichtungsmethoden: Planungsparameter
Das Inforegister **Planung** auf der Artikelkarte ist Mittelpunkt der gesamten Lieferkette des Unternehmens. Das Einstellen eines richtigen Planungsparameters ist für die kosteneffektive Bestandskontrolle und einen sehr guten Debitorenservice sehr wichtig.  

 Die folgende Tabelle enthält bewährte Methoden zum Einrichten von ausgewählten Planungsparameterfeldern. Für weitere Informationen zu einem Feld klicken Sie auf den Link in der Spalte **Feldeinstellungen**.  

|Feldeinstellungen|Bewährte Vorgehensweisen|Bemerkung|  
|-----------------|-------------------|-------------|  
|Wiederbeschaffungsverfahren||Weitere Informationen finden Sie unter [Bewährte Einrichtungsmethoden: Wiederbeschaffungsverfahren](setup-best-practices-reordering-policies.md).|  
|Reservieren|Wählen Sie **Nie** aus, wenn der Artikel unter Verwendung eines Minimalbestands geplant wird.<br /><br /> Wählen Sie in der Fertigung **Nie** aus, um es dem Planungssystem zu gestatten, alle Bedarfsposten abzudecken.<br /><br /> Wählen Sie **Optional** für Artikel aus, die Sie für Debitoren mit höchster Priorität reservieren wollen.<br /><br /> Wählen Sie **Immer** für nicht eindeutige Artikel aus, wie beispielsweise Artikel des Typs "Sonstiges", die für bestimmte Bedarfsposten eingehend sind.|Reservierungen wirken im Allgemeinen dem Zweck der Planung entgegen, nämlich einem Ausgleich zwischen Bedarf und Vorrat. Daher sollten Artikel, die für die Planung eingerichtet wurden, im Allgemeinen nicht reserviert werden.<br /><br /> Wenn der Benutzer eine Lagerbestandsmenge für zukünftigen Bedarf reserviert, wird die Planungsgrundlage gestört, und der Minimalbestand funktioniert möglicherweise nicht ordnungsgemäß. Selbst wenn der voraussichtliche Lagerbestand im Hinblick auf den Minimalbestand akzeptabel ist, stehen die Mengen möglicherweise aufgrund der Reservierung nicht zur Verfügung.|  
|Toleranzperiode|Legen Sie dies im Hinblick auf die Flexibilität des Lieferanten fest.|Wenn der Lieferant Änderungen in letzter Minute an den Aufträgen akzeptiert, verwenden Sie eine längere Periode. Wenn für den Lieferanten eine feste Planung erforderlich ist, dann halten Sie die Periode so kurz wie möglich.<br /><br /> Informationen zur globalen Einrichtung, siehe [Designdetails: Planungsparameter](design-details-planning-parameters.md).|  
|Toleranzmenge||Informationen zur globalen Einrichtung, siehe [Designdetails: Planungsparameter](design-details-planning-parameters.md).|  
|Lagerbestand berücksichtigen|Wählen Sie dies immer aus, wenn Sie das Los-für-Los-Wiederbeschaffungsverfahren verwenden.|Wählen Sie dies nur in bestimmten Fällen nicht aus, beispielsweise wenn keine Lagerartikel verkäuflich sind.|  
|Sicherh.-Zuschl. Beschaff.-Zt.|Die Einstellung muss zwischen 1D und 6D. liegen.<br /><br /> Legen Sie einen Sicherheitszuschlag zur Beschaffungszeit von mindestens einem Tag fest, um sicherzustellen, dass die Lieferungen an dem Tag verfügbar sind, an dem sie benötigt werden.<br /><br /> Wenn Sie einen neuen Lieferanten verwenden, legen Sie einen längeren Zeitraum fest, bis dessen Liefertreue bekannt ist.<br /><br /> In der Herstellung definieren Sie längere Sicherheitszuschläge zur Beschaffungszeit für wichtige Komponenten.|Vom System geplante Lieferungen, um zu vermeiden, dass am gleichen Tag, an dem Bestand nicht lieferbar ist, Bestand nicht lieferbar ist. Dies kann sich möglicherweise als mehrere Stunden zu spät erweisen, wenn beispielsweise der Bedarf morgens erforderlich ist und die Lieferung am Nachmittag eingeht. **Hinweis:** Das Feld **Sicherh.-Zuschl.-Zt.** verwendet den Basiskalender. Daher bedeutet 14T nicht notwendigerweise zwei Wochen.|  
|Sicherheitsbestand|Verwendung für Artikel mit großen Nachfrageschwankungen.<br /><br /> In der Produktion, Verwendung für wichtige Komponenten.<br /><br /> Verwendung für Artikel, die Servicevereinbarungen unterliegen.|Wenn das Feld **Minimalbestant** nicht ausgefüllt ist, dann dient der Sicherheitsbestand auch als Minimalbestand.|  
|Loskumulierungsperiode|Wenn Sie nur wenige Großaufträge annehmen möchten und einen hohen Lagerbestand akzeptieren, dann legen Sie eine sehr lange Loskumulierungsperiode fest.<br /><br /> Wenn Sie viele kleine Aufträge annehmen möchten und sich einen minimalem Lagerbestand wünschen, dann legen Sie eine kurze Loskumulierungsperiode fest.|Die Loskumulierungsperiode ist im Allgemeinen die längste Periode, in der Sie über Lagerbestand verfügen.|  
|Minimalbestand|Ermitteln Sie den Minimalbestand auf Basis des Anforderungsprofils des Artikels.|Wenn laut historischen Daten während einer Beschaffungszeit von sieben Tagen der durchschnittliche Bedarf des Artikels 100 Einheiten beträgt, kann der Minimalbestand auf 100 festgelegt werden.<br /><br /> Das bedeutet, dass bei einer Abnahme des Lagerbestands auf unter 100 Einheiten das Planungssystem die Wiederbeschaffung des Artikels vorschlägt, da für die Wiederbeschaffung sieben Tage benötigt werden und genügend Einheiten vorhanden sein müssen, um den Bedarf in diesen sieben Tagen zu decken.|  
|Zeitrahmen|Ein leeres Feld bedeutet, dass der Lagerbestand jeden Tag überprüft wird.|Bei täglicher Überprüfung des Lagerbestands ist eine optimale Planung des Minimalbestands sichergestellt. **Hinweis:** Ein Zeitrahmen von 1W bedeutet, dass der Lagerbestand möglicherweise eine Woche bevor ein Beschaffungsauftrag vorgeschlagen wird, unter dem Minimalbestand liegt.|  
|Rundungspräzision|In der teuren Produktion auf 0,00001 festgelegt.|Große Rundungsmengen an Ausschuss oder Materialverbrauch können zu sehr hohen Lagerkosten führen. Es kann daher von Bedeutung sein, die kleinste Rundungspräzision festzulegen, um diese potenziellen Kosten zu minimieren.|  

> [!NOTE]  
>  Die bewährten Methoden zu Planungsparametern auf Artikelkarten gelten auch für dieselben Felder auf Lagerhaltungsdatenkarten.  
>   
>  Wenn Unternehmen den Bedarf an verschiedenen Lagerorten planen, empfiehlt es sich, für jeden Standort Lagerhaltungsdaten festzulegen und den gesamten Bedarf mit einem Wert im Feld **Lagerortcode** zu erstellen. Weitere Informationen finden Sie unter [Designdetails: Bedarf an leerem Lagerort](design-details-demand-at-blank-location.md)  

## <a name="see-also"></a>Siehe auch  
 [Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)   
 [Richten Sie komplexe Anwendungsbereiche mithilfe bewährter Methoden ein](set-up-complex-application-areas-using-best-practices.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

