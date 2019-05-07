---
title: Lieferbenachrichtigungen
description: Lieferbenachrichtigung werden verwendet, um überfällige Kreditorenlieferungen zu verfolgen und um  Kreditoren an überfällige Lieferungen zu erinnern.
ms.service: dynamics365-business-central
documentationcenter: ''
author: SorenGP
services: project-madeira
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f957c5f19171126c50770e6dce60e90b8437f09c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "941324"
---
# <a name="delivery-reminders"></a>Lieferbenachrichtigungen
Lieferbenachrichtigung werden verwendet, um überfällige Kreditorenlieferungen zu verfolgen und um  Kreditoren an überfällige Lieferungen zu erinnern. Um Lieferbenachrichtigung zu erstellen, müssen Sie Folgendes einrichten:  

- Lieferbenachrichtigungsbestimmungen  

    Lieferbenachrichtigungsbestimmungen werden durch einen Code identifiziert, der Kreditoren zugewiesen werden muss. Wenn mehr als eine Kombination der Einstellungen verwendet werden soll, müssen Sie für jede Kombination einen eigenen Code einrichten. Sie können eine beliebige Anzahl an Lieferbenachrichtigungsbestimmungen einrichten.  

- Lieferbenachrichtigungsstufen  

    Für jede Lieferbenachrichtigungsbestimmung müssen Sie Lieferbenachrichtigungsebenen definieren. Diese Stufen legen fest, wie häufig Lieferbenachrichtigung für eine bestimmte Methode erstellt werden können. Stufe 1 ist die erste Lieferbenachrichtigung, die Sie für eine überfällige Lieferung erstellen. Stufe 2 ist die zweite Lieferbenachrichtigung und so weiter. Wenn Lieferbenachrichtigungen erstellt werden, werden die Anzahl von Mahnungen, die zuvor erzeugt wurden und die aktuelle Nummer verwendet, um Methoden anzuwenden.  

- Lieferbenachrichtigungstextnachrichten  

    Für jede Lieferbenachrichtigungstextnachricht müssen Sie Lieferbenachrichtigungsebenen definieren. Es gibt zwei Arten von Lieferbenachrichtigungstexten: Vortexte und Nachtexte. Die Vortextnachricht wird unter dem Kopfabschnitt gedruckt, vor der Liste der Posten, die zur Mahnung markiert sind. Die Nachtextnachricht wird nach dieser Liste gedruckt.  

Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminder-terms-levels-and-text.md).  

Nach dem Einrichten der Lieferbestimmungen müssen die Lieferbenachrichtigungsbestimmungscodes den Kreditoren zuweisen. Weitere Informationen finden Sie unter [Vorgehensweise: Zuweisen von Lieferbenachrichtigungen zu Kreditoren](how-to-assign-delivery-reminder-codes-to-vendors.md).  

Lieferbenachrichtigung können manuell oder automatisch erstellt werden. Sie können die Stapelverarbeitung **Lieferbenachrichtigung erstellen** verwenden, um Lieferbenachrichtigungen automatisch zu erstellen. Dieser Batchauftrag ermöglicht es Ihnen, die Bestellungen auszuwählen, für die Lieferbenachrichtigungen erstellt werden müssen. Weitere Informationen finden Sie unter [Lieferbenachrichtigungen erstellen](how-to-issue-delivery-reminders.md).  

Sie können Belege auch in Bezug auf Bestellzeilen und Verkaufsauftragszeilen nachverfolgen.  

[!INCLUDE[d365fin](../../includes/d365fin_md.md)] stellt die folgenden Berichte bereit:  

- **Registrierte Lieferbenachrichtigung** -, Um die Lieferbenachrichtigung für Kreditoren anzuzeigen.  
- **Lieferbenachrichtigung - Test** -, Um die Lieferbenachrichtigung zu prüfen, bevor Sie diese registrieren.  

Weitere Informationen finden Sie unter [Vorgehensweise: Drucken von Testberichten für  Lieferbenachrichtigungen](how-to-print-test-reports-for-delivery-reminders.md).  

## <a name="see-also"></a>Siehe auch  
 [Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md)   
 [Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text](how-to-set-up-delivery-reminder-terms-levels-and-text.md)   
 [So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [So erstellen Sie Lieferanmahnungen](how-to-generate-delivery-reminders.md)   
 [So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md)   
 [Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md)   
 [So drucken Sie Testberichte vor dem Registrieren von Lieferanmahnungen](how-to-print-test-reports-for-delivery-reminders.md)
