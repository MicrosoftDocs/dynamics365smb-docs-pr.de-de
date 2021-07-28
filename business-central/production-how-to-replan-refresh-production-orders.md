---
title: Neugestaltungs- oder direkt Aktualisierung von Fertigungsaufträgen
description: In diesem Thema wird beschrieben, wie Sie Produktionsaufträge neu planen und Produktionsaufträge direkt aktualisieren können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 5e8543d64c1ecfea1f554f13f753743684d1f463
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440378"
---
# <a name="replan-or-refresh-production-orders-directly"></a>Produktionsaufträge direkt umplanen oder auffrischen
Die Funkion **Neu Planen** wird in der Regel nach dem Hinzufügen bzw. Ändern von Komponenten ausgeführt, aus denen sich zugrunde liegende Fertigungsaufträge zusammensetzen. Mit dieser Planungsfunktion werden Änderungen berechnet, die an Komponenten und Arbeitsgängen vorgenommen werden. Dabei werden Artikel auf niedrigeren Ebenen der Fertigungsstückliste berücksichtigt, für die ggf. neue Fertigungsaufträge erstellt werden.  

Auf der Grundlage der vorgenommenen Änderungen an den Komponenten und Arbeitsgängen wird von der Funktion Neu planen der neue Bedarf für den Fertigungsauftrag berechnet und geplant.  

Die Funktion **Aktualisieren** für Fertigungsaufträge wird normalerweise verwendet, nachdem Sie Folgendes getan haben:

- Ein Fertigungsauftragskopf wurde manuell zur Berechnung erstellt, und erstmalig wurden Zeilendaten erstellt.
- Es wurden Änderungen am Fertigungsauftragskopf zur Neuberechnung aller Zeilendaten vorgenommen.

Mit der Funktion Aktualisieren werden vorgenommene Änderungen an einem Fertigungsauftragkopf berechnet, wobei Fertigungsstücklistenebenen keine Rolle spielen. Mithilfe der Funktion Aktualisieren werden im Wesentlichen die Werte der Komponentenzeilen und Arbeitsgänge berechnet und initiiert, die auf den definierten Stammdaten in der zugehörigen Fertigungsstückliste und im zugehörigen Arbeitsplan basieren und der Auftragsmenge und dem Fälligkeitsdatum im Kopf des Fertigungsauftrags entsprechen.

Sie können die FA-Zeilen entweder manuell eintragen oder Sie verwenden die Funktion, die die FA-Zeilen aus dem Fertigungsauftragskopf berechnet.  

> [!NOTE]
> Wenn Sie die Funktion Aktualisieren zur Berechnung der FA-Zeilen aus dem Fertigungsauftragskopf verwenden, werden die bestehenden FA-Zeilen gelöscht und neue Zeilen berechnet.  

## <a name="to-replan-a-production-order"></a>Einen Fertigungsauftrag neu planen  
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Geplante Prod. Aufträge** ein und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie den Fertigungsauftrag, den Sie neu planen wollen.  
3.  Wählen Sie im Inforegister **Zeilen** die Aktionen **Zeilen**, und dann Zeilen, und dann **Komponenten**.  
4.  Fügen Sie eine Komponente hinzu, die einen Fertigungsartikel oder eine Unterkomponente darstellt.  
5.  Klicken Sie im Fertigungsauftrag auf die Aktion **Neu planen**.  

    Definieren Sie auf der Seite **FA neu planen**, wie und was neu geplant werden soll.  
6.  Wählen Sie im Feld **Planungsrichtung** eine der folgenden Optionen aus.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**"Rückwärts"**|Berechnet die Folge der Arbeitsgänge rückwärts, ab dem frühesten möglichen Enddatum, wie durch Fälligkeitsdatum und andere geplante Aufträge definiert, bis zum spätesten möglichen Startdatum. **Hinweis:** Diese Standardoption ist in den meisten Situationen angemessen.|  
    |**"Vorwärts"**|Berechnet den Vorgang vorwärts, ab dem frühesten spätesten möglichen Startdatum, definiert durch Fälligkeitsdatum und/oder andere geplante Aufträge, bis zum frühesten möglichen Enddatum zu berechnen. **Hinweis:** Diese Option ist nur bei Aufträgen mit schnellstmöglicher Fertigstellung relevant.|  

7.  Wählen Sie im Feld **Planen** aus, ob Produktionsanforderungen für Fertigungsartikel in der Fertigungsstückliste berechnet werden sollen wie folgt.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**"Keine Ebene"**|Berücksichtigt keine Herstellung der unteren Ebene. Dadurch wird lediglich der Plan des Artikels aktualisiert, wie bei der Funktion Aktualisieren.|  
    |**"Eine Ebene"**|Planen für Fertigungsbedarf auf der ersten Ebene. Es können Fertigungsaufträge der ersten Ebenen erstellt werden.|  
    |**"Alle Ebenen"**|Planen für Fertigungsbedarf auf allen Ebenen. (Es können Fertigungsaufträge für alle Ebenen erstellt werden.)|  

8.  Wählen Sie **Eine Ebene**, und wählen Sie die Schaltfläche **OK**, um den Fertigungsauftrag neu zu planen, sowie einen neuen zugrunde liegenden Fertigungsauftrag für die eingeführte Unterkomponente zu berechnen und zu erstellen, wenn diese nicht vollständig verfügbar ist.  

> [!NOTE]  
>  Mithilfe der Funktion **Neu planen** implementierte Änderungen wirken sich mit hoher Wahrscheinlichkeit auf den Kapazitätsbedarf des Fertigungsauftrags aus, sodass Sie die Arbeitsgänge anschließend ggf. neu planen müssen.  

## <a name="to-refresh-a-production-order"></a>Einen Fertigungsauftrag aktualisieren  
Wenn Sie FA-Zeilen geändert haben, dann müssen Sie die Komponenten des Fertigungsauftrags aktualisieren. Im weiteren Vorgang werden die Komponenten für einen fest geplanten Fertigungsauftrag berechnet. Die Schritte sind für eine Arbeitsplanzeile ähnlich.

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Firm Planned Prod. Auftrag** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Erstellen von Montageaufträgen](production-how-to-create-production-orders.md).  
3.  Wählen Sie die Aktion **Aktualisieren** aus.
4. Auf der Seite **Produktionsauftrag aktualisieren** können Sie unter folgenden Optionen wählen:

    |Option||Description|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Planungsrichtung**|**Vorwärts**|Die Planung beginnt mit dem Startdatum und rechnet vorwärts bis zum Enddatum. Damit Sie diese Option verwenden können, müssen Sie das Startdatum eingegeben haben.|  
    ||**Rückwärts**|Die Planung beginnt mit dem Enddatum und wird dann rückwärts in Richtung Startdatum fortgesetzt.|  
    |**Berechnen**|**Zeilen**|Wählen Sie dieses Feld aus, um die FA-Zeilen zu berechnen.|  
    ||**Arbeitspläne**|Dieses Feld hat keinen Einfluss auf die Berechnung der FA-Zeilen.|  
    ||**Komponentenbedarf**|Dieses Feld hat keinen Einfluss auf die Berechnung der FA-Zeilen.|  
    |**Logistik**|**Eingehende erwartete Lagerbewegung erstellen**|Dieses Feld hat keinen Einfluss auf die Berechnung der FA-Zeilen.|  

5. Klicken Sie zum Bestätigen auf die Schaltfläche **OK**. Nun werden die FA-Zeilen berechnet.

> [!NOTE]  
>  Die Berechnung der FA-Komponenten löscht die bisherigen Änderungen in den Komponenten.

## <a name="see-also"></a>Siehe auch  
[Planung](production-planning.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]