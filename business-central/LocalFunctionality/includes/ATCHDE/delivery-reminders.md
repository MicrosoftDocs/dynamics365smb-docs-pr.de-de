---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fe306d5fd0f6878e016adc28036c026730d69552
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747553"
---
Lieferanmahnungen werden verwendet, um überfällige Kreditorenlieferungen zu verfolgen und um Kreditoren an überfällige Lieferungen zu erinnern. Um Lieferbenachrichtigung zu erstellen, müssen Sie Folgendes einrichten:

- Lieferbenachrichtigungsbestimmungen  

    Lieferbenachrichtigungsbestimmungen werden durch einen Code identifiziert, der Kreditoren zugewiesen werden muss. Wenn mehr als eine Kombination der Einstellungen verwendet werden soll, müssen Sie für jede Kombination einen eigenen Code einrichten. Sie können eine beliebige Anzahl an Lieferbenachrichtigungsbestimmungen einrichten.  

- Lieferbenachrichtigungsstufen  

    Für jede Lieferbenachrichtigungsbestimmung müssen Sie Lieferbenachrichtigungsebenen definieren. Diese Stufen legen fest, wie häufig Lieferbenachrichtigung für eine bestimmte Methode erstellt werden können. Stufe 1 ist die erste Lieferbenachrichtigung, die Sie für eine überfällige Lieferung erstellen. Stufe 2 ist die zweite Lieferbenachrichtigung und so weiter. Wenn Lieferbenachrichtigungen erstellt werden, werden die Anzahl von Mahnungen, die zuvor erzeugt wurden und die aktuelle Nummer verwendet, um Methoden anzuwenden.  

- Lieferbenachrichtigungstextnachrichten  

    Für jede Lieferbenachrichtigungstextnachricht müssen Sie Lieferbenachrichtigungsebenen definieren. Es gibt zwei Arten von Lieferbenachrichtigungstexten: Vortexte und Nachtexte. Die Vortextnachricht wird unter dem Kopfabschnitt gedruckt, vor der Liste der Posten, die zur Mahnung markiert sind. Die Nachtextnachricht wird nach dieser Liste gedruckt.  

Nach dem Einrichten der Lieferbestimmungen, -stufen und -texte, müssen Sie den Kreditoren die entsprechenden Lieferanmahnungscodes zuweisen.  

Lieferbenachrichtigung können manuell oder automatisch erstellt werden. Sie können den Batchauftrag **Lieferanmahnung erstellen** zum automatischen Erstellen von Lieferanmahnungen verwenden, um so die Bestellungen auswählen zu können, für die Lieferanmahnungen erstellt werden müssen.  

Sie können Belege auch in Bezug auf Bestellzeilen und Verkaufsauftragszeilen nachverfolgen.  

[!INCLUDE[prod_short](../../../includes/prod_short.md)] stellt die folgenden Berichte bereit:  

- **Registrierte Lieferbenachrichtigung** -, Um die Lieferbenachrichtigung für Kreditoren anzuzeigen.  
- **Lieferbenachrichtigung - Test** -, Um die Lieferbenachrichtigung zu prüfen, bevor Sie diese registrieren.  
