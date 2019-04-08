---
title: 'Designdetails: Die Rolle des Zeitrahmens | Microsoft Docs'
description: Der Zweck dieses Zeitrahmens ist es, Bedarfsereignisse innerhalb des Zeitfensters zu erfassen, um einen gemeinsamen Beschaffungsauftrag zu erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: ff748a192d8d1650a708ab70ec33ccc7bfd53c48
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798480"
---
# <a name="design-details-the-role-of-the-time-bucket"></a>Designdetails: Die Rolle des Zeitrahmens
Der Zweck dieses Zeitrahmens ist es, Bedarfsereignisse innerhalb des Zeitfensters zu erfassen, um einen gemeinsamen Beschaffungsauftrag zu erstellen.  

 Für Wiederbeschaffungsverfahren, die einen Minimalbestand verwenden, können Sie einen Zeitrahmen definieren. Dadurch ist sichergestellt, dass Bedarf innerhalb derselben Periode kumuliert wird, bevor die Auswirkungen auf den voraussichtlichen Lagerbestand geprüft werden, und ob der Minimalbestand unterschritten wurde. Wenn der Minimalbestand überschritten wird, wird ein neuer Beschaffungsauftrag vom Ende der durch den Zeitrahmen definierten Periode vorwärts geplant. Der Zeitrahmen beginnt am geplanten Startdatum.  

 Der Zeitrahmenkonzept spiegelt den manuellen Vorgang des Überprüfens des Lagerbestands auf häufiger Basis anstatt für jede Transaktion. Die Anwender muss die Häufigkeit (den Zeitrahmen) festlegen. Beispielsweise erfasst der Benutzer alle Artikelanforderungen von einem Kreditor, um einen wöchentlichen Auftrag zu platzieren.  

 ![Beispiel des Zeitrahmens in der Planung](media/nav_app_supply_planning_2_reorder_cycle.png "Beispiel des Zeitrahmens in der Planung")  

 Das Zeitrahmen wird im Allgemeinen verwendet, um einen Kaskadeneffekt zu vermeiden. Zum Beispiel eine eine ausgeglichene Zeile von Bedarf und Vorrat, bei der ein frühzeitiger Bedarf storniert oder ein neuer Bedarf erstellt wird. Das Ergebnis würde sein, dass jeder Beschaffungsauftrag (mit Ausnahme des letzten) umgeplant würde.  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Wiederbeschaffungsverfahren](design-details-reordering-policies.md)   
 [Designdetails: Planungsparameter](design-details-planning-parameters.md)   
 [Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
 [Designdetails: Vorratsplanung](design-details-supply-planning.md)
