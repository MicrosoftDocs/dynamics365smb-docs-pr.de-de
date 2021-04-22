---
title: Auftrag nach Auftrag planen | Microsoft Docs
description: Diese Planungsaufgabe kann auf der Seite **Auftragsplanung** ausgeführt werden, in dem der gesamte neue Bedarf sowie Informationen über die Verfügbarkeit und Beschaffungsvorschläge angezeigt werden. Das Fenster bietet eine Übersicht und die erforderlichen Tools für eine effektive Bedarfsplanung anhand der Verkaufs- und Komponentenzeilen, auf deren Grundlage dann verschiedene Arten von Beschaffungsaufträgen direkt erstellt werden können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ab3929a410a280494d806e7aeea5c54ce966769e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787977"
---
# <a name="plan-for-new-demand-order-by-order"></a>Planung der Bestellung eines neuen Bedarfs von Auftrag
Diese Planungsaufgabe kann auf der Seite **Auftragsplanung** ausgeführt werden, in dem der gesamte neue Bedarf sowie Informationen über die Verfügbarkeit und Beschaffungsvorschläge angezeigt werden. Das Fenster bietet eine Übersicht und die erforderlichen Tools für eine effektive Bedarfsplanung anhand der Verkaufs- und Komponentenzeilen, auf deren Grundlage dann verschiedene Arten von Beschaffungsaufträgen direkt erstellt werden können.  

Sie können die Seite **Auftragsplanung** in zwei Arten eingeben, je nach Herangehensweise: Von einem Auftrag, die Sie speziell für oder im Stapelbetrieb planen möchten, da Sie für alle planen möchten und aus einem neuen Bedarf.  


## <a name="to-plan-for-new-production-order-demand"></a>So planen Sie neue Fertigungsaufträge  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Geplante Fertigungsaufträge** ein, und wählen Sie dann den zugehörigen Link. (Sie können diese Schritte für einen geplanten, fest geplanten oder freigegebenen Fertigungsauftrag ausführen).
2.  Öffnen Sie den Fertigungsauftrag, für den Sie planen möchten, und wählen Sie die **Planung** Aktion aus.  
3.  Klicken Sie auf der Seite **Auftragsplanung** auf Funktionen und dann auf **Planung berechnen**.  

Auf der Seite Fenster werden Planungszeilen entsprechend dem Ansichtsfilter **Fertigungsbedarf** angezeigt, d. h. die unausgeführten Komponentenzeilen aller vorhandenen Fertigungsaufträge. Bedarf nur für den einen Fertigungsauftrag wird nicht angezeigt, da es notwendig ist, für einen Fertigungsauftrag mit einer Übersicht des Bedarfs für möglicherweise ältere Komponentenzeilen zu planen. Planungszeilen für den Fertigungsauftrag im Kontext werden erweitert.  

## <a name="to-plan-for-any-new-demand"></a>Für beliebigen neuen Bedarf planen  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Auftragsplanung** ein, und wählen Sie dann den zugehörigen Link.  
2.  Klicken Sie auf der Seite **Auftragsplanung** auf Funktionen und dann auf **Planung berechnen**.
3.  Wählen Sie die Schaltfläche **Ausklappen (+)** vor dem Datum im Feld **Bedarfsdatum**, um die zugrunde liegenden Planungszeilen anzuzeigen, die Bedarfszeilen mit unzureichender Verfügbarkeit darstellen.  
4.  Für die einzelnen aufgeklappten Planungszeilen, bzw. Bedarfszeilen werden unten auf der Seite Werte in Informationsfeldern angezeigt.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Menge an anderen Lagerorten**|Gibt an, ob der Artikel an einem anderen Lagerort vorhanden ist. Sie können ihn dann suchen und auswählen.|  
    |**Ersatzartikel vorhanden**|Zeigt, ob ein Ersatzartikel für den Artikel erstellt wird. Sie können ihn dann suchen und auswählen. Beachten Sie, dass diese Funktion nur für Komponenten gilt, d. h. für Bedarfszeilen der Art **Produktion**.|  
    |**Verfügbare Menge**|Zeigt die Gesamtverfügbarkeit des Artikels, bzw. den Verfügbarkeitssaldo.|  
    |**Frühestes verfügbares Datum**|Zeigt das Eingangsdatum eines eingehenden Beschaffungsauftrags an, der die benötigte Menge nach dem Bedarfsdatum abdecken kann.|  

5.  Wählen Sie im Feld **Beschaffungsmethode** aus, welche Art von Beschaffungsauftrag erstellt werden soll.  

    Der Standardwert ist der auf der Artikelkarte oder Lagerhaltungsdatenkarte, ist vorgegeben, Sie können ihn jedoch mit einer der drei Optionen ändern:  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Einkauf**|Erstellt eine Bestellung.|  
    |**Umlagerung**|Erstellt einen Umlagerungsauftrag.|  
    |**Fertigungsauftrag**|Erstellt einen Fertigungsauftrag.|  

    Im Feld **Liefern von** müssen Sie entsprechend der ausgewählten Beschaffungsmethode einen Wert auswählen.  

    > [!NOTE]  
    >  Wenn dieses Feld leer bleibt, wird bei Verwendung der Funktion **Beschaffungsaufträge erstellen** eine Fehlermeldung angezeigt und es wird keine Ersatzbestellung für die entsprechende Planungszeile erstellt. Dies trifft jedoch nicht zu, wenn als Beschaffungsmethode **Fertigungsauftrag** gewählt wurde.  

6.  Im Feld **Liefern von** können Sie in der entsprechenden Liste die gewünschte Lieferquelle suchen und auswählen:  

    - Bei der Beschaffungsmethode **Einkauf** wird über die Suchschaltfläche in diesem Feld die Seite **Artikel/Lieferanten Katalog** durchsucht.  
    - Bei der Beschaffungsmethode **Umlagerung** wird über die Suchschaltfläche in diesem Feld die Seite **Lagerorteübersicht** durchsucht.  

    Wenn der Bedarfsartikel an einem anderen Lagerort vorhanden ist, wird dies unten im Feld mit der Angabe der **der an anderen Lagerorten vorhandenen Menge** angezeigt, und Sie können dann den Lagerort suchen und auswählen, von dem der Artikel nach Erstellung des Umlagerungsauftrags geliefert werden soll.  

    Wenn für den Bedarfsartikel ein Ersatzartikel vorhanden ist, wird unten im Feld **Ersatzartikel vorhanden** der Text **Ja** angezeigt und Sie können dann auf der Seite **Ersatzartikelposten** den Ersatzartikel auswählen.  

7.  Aktivieren Sie in das Feld **Reservieren**, wenn Sie eine Reservierung vom gerade erstellten Beschaffungsauftrag für die Bedarfszeile vornehmen möchten. In der Standardeinstellung ist das Feld leer.  

    > [!NOTE]  
    >  Sie könne das Feld nur aktivieren, wenn der Artikel auf seiner Artikelkarte den Wert **Optional** oder **Immer** im Feld **Reservieren** angegeben hat.  

8.  Im Feld **Bestellmenge** können Sie die Menge angeben, die in den gerade erstellten Beschaffungsauftrag übernommen werden soll.   
    Der Standardwert ist die im Feld **Bedarfsmenge** angegebene Menge. Sie können jedoch bei Kenntnis der Nachfragesituation auch mehr oder weniger bestellen. Wenn Sie beispielsweise auf der Seite **Auftragsplanung** sehen, dass sich mehrere nicht zusammengehörige Bedarfszeilen auf denselben gekauften Artikel beziehen und ungefähr zum gleichen Datum fällig werden, können Sie diese Bedarfszeilen konsolidieren, indem Sie die insgesamt benötigte Menge in das Feld **Bestellmenge** der Zeile eingeben und dann die anderen obsoleten Planungszeilen für diesen Artikel löschen.  

9.  In den Feldern **Fälligkeitsdatum** und **Auftragsdatum** können Sie das jeweilige Datum eingeben, das für die erstellten Beschaffungsaufträge gelten soll.  

    Diese beiden Felder sind über das Feld **Vorg. Sich.-Zuschl. Besch.-Zt.** miteinander verknüpft, das auf der Seite **Produktionseinrichtung** gefunden werden kann. Standardmäßig ist das Fälligkeitsdatum gleich dem Bedarfsdatum, Sie können dies jedoch beliebig ändern.  

> [!NOTE]  
>  Wenn Sie ein Datum eingeben, das nach dem Bedarfsdatum liegt, erhalten Sie eine Warnmeldung.  

## <a name="to-make-supply-orders"></a>Beschaffungsaufträge erstellen  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Geplante Fertigungsaufträge** ein, und wählen Sie dann den zugehörigen Link. Sie können diese Schritte für einen geplanten, fest geplanten oder freigegebenen Fertigungsauftrag ausführen.  
2.  Öffnen Sie den Fertigungsauftrag, für den Sie planen möchten, und wählen Sie die **Planung** Aktion aus.  
3.  Platzieren Sie den Cursor in einer Planungszeile, und klicken Sie auf **Bestellungen erstellen**.  
4.  Wählen Sie auf der Seite **Beschaffungsaufträge erstellen** im Inforegister **Auftragsplanung** im Feld **Aufträge erstellen für** eine der folgenden Optionen aus.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**die aktive Zeile**|Erstellen Sie einen Beschaffungsauftrag nur für die Zeile, in der der Cursor platziert wurde.|  
    |**den aktiven Auftrag**|Erstellen Sie Beschaffungsaufträge für alle Zeilen in der Bestellung, in die der Cursor platziert wurde.|  
    |**Alle Zeilen**|Erstellen Sie Beschaffungsaufträge für alle Zeilen auf der Seite **Auftragsplanung**.|  

5.  Definieren Sie auf dem Inforegister **Optionen**, welche Beschaffungsaufträge bzw. Bestellarbeitsblattszeilen erstellt werden sollen.  

    > [!NOTE]  
    >  Die zuletzt vorgenommenen Einstellungen auf der Seite **Beschaffungsaufträge erstellen** werden unter Ihrer Benutzer-ID gespeichert und für die nächste Verwendung der Seite beibehalten.  

6.  Wählen Sie die Schaltfläche **OK**, um die vorgeschlagenen Beschaffungsaufträge bzw. Bestellarbeitsblattszeilen zu erstellen.  

Sie haben nun die Planung für den nicht erfüllten Bedarf durchgeführt, indem Sie die entsprechenden Beschaffungsaufträge erstellt haben. Ausführliche Informationen über spezielle Abläufe bei der Verwendung der Seite **Auftragsplanung** sind je nach den entsprechenden internen Richtlinien des Unternehmens vorhanden.  

Nachdem Sie die Planung auf der Seite **Auftragsplanung** abgeschlossen haben, also beispielsweise eine Alternativmöglichkeit für die Mengenbeschaffung definiert haben, können Sie mit dem Erstellen von Beschaffungsaufträgen für weitere Planungszeilen fortfahren.  

> [!NOTE]  
>  Aus den erstellten Beschaffungsaufträgen kann sich neuer, von diesen Beschaffungsaufträgen abhängiger Bedarf ergeben, und für diesen Fall wählen Sie noch einmal **Planung berechnen**, um diese zu ermitteln und zu bearbeiten, bevor Sie in der Liste fortfahren.  

## <a name="see-also"></a>Siehe auch  
[Exemplarische Vorgehensweise: Manuelle Beschaffungsplanung](walkthrough-planning-supplies-manually.md)  
[Planung](production-planning.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]