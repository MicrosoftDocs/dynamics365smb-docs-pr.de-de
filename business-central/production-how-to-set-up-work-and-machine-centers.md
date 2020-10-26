---
title: 'Vorgehensweise: Einrichten von Arbeits- und Servicezeiten | Microsoft Docs'
description: Auf einer **Arbeitsplatzgruppenkarte** sind die konstanten Werte und Anforderungen der jeweiligen Fertigungsressource organisiert, und dadurch werden die Istmengen der Fertigung in dieser Arbeitsplatzgruppe gesteuert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1e162dadd88fd7db781e884d0cde395bcff6250c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910705"
---
# <a name="set-up-work-centers-and-machine-centers"></a>Arbeitsplätze und Arbeitsplatzgruppen einrichten

Die Anwendung unterscheidet zwischen drei verschiedenen Arten von Kapazitätseinheiten. Diese sind hierarchisch angeordnet. Jede Ebene enthält die untergeordneten Ebenen.  

Die oberste Ebene ist die Abteilung. Arbeitsplatzgruppen werden den Abteilungen zugeordnet. Jede Arbeitsplatzgruppe gehört zu einer Abteilung.

Sie können unterschiedliche Arbeitsplätze zu einer Arbeitsplatzgruppe zusammenfassen. Ein Arbeitsplatz kann nur zu einer Arbeitsplatzgruppe gehören.  

Die geplante Kapazität einer Arbeitsplatzgruppe besteht aus der Verfügbarkeit der entsprechenden Arbeitsplätze und der zusätzlichen geplanten Verfügbarkeit der Arbeitsplatzgruppe. Die geplante Verfügbarkeit der Abteilung ist die Summe aller Verfügbarkeiten der entsprechenden Arbeitsplätze und Arbeitsplatzgruppen.  

Die Verfügbarkeit wird in Kalenderposten gespeichert.  

> [!IMPORTANT]
> Bevor Sie anfangen oder Arbeitsplätze einrichten, müssen Sie Betriebskalender einrichten. Weitere Informationen finden Sie unter [Erstellen von Betriebskalendern](production-how-to-create-work-center-calendars.md).

## <a name="to-set-up-a-work-center"></a>Um Arbeitsplatzgruppen einzurichten:

Nachfolgend ist beschrieben, wie ein alternativer Arbeitsplatzkalender eingerichtet wird. Die Schritte, um ein Arbeitsplatzkalenders einzurichten außer für das **Arbeitsplatz-Einrichtung** Inforegister.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Arbeitsplatzgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie im Feld **Abteilung** die übergeordnete Ebene, unter der sich die Arbeitsplatzgruppe befindet, sofern relevant. Wählen Sie aus der Dropdown-Liste die Aktion **Neu** aus.  
5. Wählen Sie das Feld **Gesperrt** aus, wenn Sie verhindern möchten, dass die Arbeitsplatzgruppe bei einer Verarbeitung verwendet wird. Das bedeutet, dass die Ausgabe für einen Artikel nicht gebucht werden kann, der für die Arbeitsplatzgruppe gefertigt wird. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-post-output-quantity.md).
6. Geben Sie im Feld **EK-Preis** die Kosten der Fertigung einer Einheit in dieser Arbeitsplatzgruppe ein, ausschließlich aller anderen Kostenelemente. Diese Kosten werden häufig als *direkte Arbeitskosten* bezeichnet.  
7. Geben Sie im Feld **Kosten %** die Gesamtkosten des Einsatzes der Arbeitsplatzgruppe als Prozentsatz des EK-Preises ein. Dieser prozentuale Betrag wird in der Berechnung des Einstandspreises zum EK-Preis addiert.  
8. Geben Sie im Feld **Gemeinkostensatz** die nicht mit dem eigentlichen Betrieb verbundenen Kosten für die Arbeitsplatzgruppe (z. B. Wartungsausgaben) als absoluten Betrag ein.  

    Das Feld **Einstandspreis** enthält den berechneten Einstandspreis für die Fertigung einer Einheit in der Arbeitsplatzgruppe, wobei alle Kostenelemente berücksichtigt sind.  

    Einstandspreis = EK-Preis + (EK-Preis x Kosten %) + Gemeinkostensatz.  

9. Legen Sie im Feld **Einstandspreisberechnung** fest, ob der obigen Berechnung die benötigte Zeitspanne ( **Zeit** ) oder die Anzahl der gefertigten Einheiten ( **Einheiten** ) zugrunde gelegt werden soll.  
10. Markieren Sie das Feld **Spezifische Stückkosten** , wenn Sie die Stückkosten des Arbeitsplatzes in der Arbeitsplanzeile, in der er verwendet wird, definieren wollen. Dies kann sich als unerlässlich bei Arbeitsgängen mit wesentlich abweichenden Kapazitätskosten erweisen, die normalerweise in dieser Arbeitsplatzgruppe verarbeitet werden.  
11. Wählen Sie im Feld **Buchungsmethode** aus, ob der Ausgabebuchung in dieser Arbeitsplatzgruppe manuell oder automatisch mit einer der folgenden Methoden berechnet und gebucht werden soll, indem eine der folgenden Methoden verwendet wird.

    |Option|Beschreibung|
    |------|-----------|
    |**Manuell**|Der Verbrauch wird manuell im Ausgabe- oder Produktionsjournal gebucht.|
    |**Vorwärts**|Verbrauch wird automatisch berechenet und gebucht, wenn der Fertigungsftrag freigegeben ist.|
    |**Rückwärts**|Verbrauch wird automatisch berechenet und gebucht, wenn der Fertigungsftrag beendet ist.|

    > [!NOTE]
    > Gegebenenfalls kann die hier und auf der **Artikelkarte** ausgewählte Buchungsmethode für einzelne Arbeitsgänge überschrieben werden, indem die Einstellungen für Arbeitsgänge geändert wird.

12. Geben Sie im Feld **Einheitencode** die Zeiteinheit ein, die bei der Kostenberechnung und der Kapazitätsplanung der Arbeitsplatzgruppe zugrunde gelegt werden soll.
    Um regelmäßig den Verbrauch erfassen zu können, müssen Sie zunächst die Buchungsmethode einrichten. Die Einheiten, die Sie eingeben, sind Basiseinheiten. Die Bearbeitungszeit wird z. B. in Stunden und Minuten gemessen.

    > [!NOTE]  
    > Beachten Sie bei der Verwendung von Tagen, dass 1 Tag 24 Stunden und nicht 8 (Arbeitsstunden) hat.

13. Geben Sie im Feld **Kapazität** an, ob in der Arbeitsplatzgruppe mehrere Personen bzw. Maschinen gleichzeitig eingesetzt werden. Wenn in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Installation das Element "Arbeitsplatz" nicht enthalten ist, muss in diesem Feld der Wert **1** festgelegt sein.  
14. Geben Sie im Feld **Effektivität** an, wie hoch die tatsächliche Effektivität der Arbeitsplatzgruppe prozentual hinsichtlich der erwarteten Standardeffektivität ist. Wenn Sie **100** eingeben, bedeutet dies, dass die Isteffektivität der Arbeitsplatzgruppe mit der Standardeffektivität übereinstimmt.  
15. Wählen Sie das Kontrollkästchen **Konsolidierter Kalender** , wenn Sie auch Arbeitsplätze verwenden. Dadurch ist sichergestellt, dass Kalenderposten oben aus den Arbeitsplatzkalendern ermittelt werden.  
16. Wählen Sie im Feld **Betriebskalender** einen Einkaufskalender. Weitere Informationen finden Sie unter [Erstellen von Betriebskalendern](production-how-to-create-work-center-calendars.md).  
17. Geben Sie im Feld **Warteschlangenzeit** eine feste Zeitspanne an, die ablaufen muss, bevor die zugewiesenen Arbeiten in dieser Arbeitsplatzgruppe begonnen werden können. Beachten Sie, dass die Warteschlangenzeit auf die anderen nicht fertigungsbezogenen Zeitelemente wie Wartezeit und Transportzeit aufgeschlagen wird, die sie für Arbeitsgänge in dieser Arbeitsplatzgruppe definieren können.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Beispiel - unterschiedliche Arbeitsplätze, die einer Arbeitsplatzgruppe zugewiesen sind

Es ist wichtig zu planen, welche Kapazitätsarten die Gesamtkapazität ergeben, wenn Sie Arbeitsplatzgruppen und Arbeitsplätze einrichten.

Wenn unterschiedliche Arbeitsplätze (zum Beispiel 210 Packtisch 1, 310 Lackierkabine) einer Arbeitsplatzgruppe zugeordnet sind, ist die Betrachtung der einzelnen Kapazitäten entscheidend, da der Ausfall eines einzelnen Arbeitsplatzes den gesamten Fertigungsprozess unterbrechen kann. Die Arbeitsplatzgruppen können entsprechend ihrer Kapazität eingegeben werden, sie werden jedoch nicht in die Planung mit aufgenommen. Durch Deaktivieren des Feldes **Konsolidierter Kalender** wird nur die Kapazität der Arbeitsplatzgruppe, jedoch nicht die Kapazität der Arbeitsplätze, bei der Planung zugewiesen.

Wenn jedoch identische Arbeitsplätze (wie zum Beispiel 210 Packtisch 1 und 220 Packtisch 2) in einer Arbeitsplatzgruppe zusammengefasst werden, ist die Betrachtung der Arbeitsplatzgruppe als Summe der ihr zugeordneten Arbeitsplätze von Interesse. Daher wird die Arbeitsplatzgruppe selbst mit der Kapazität Null geführt. Durch Aktivierung des Feldes **Konsolidierter Kalender** wird die gemeinsame Kapazität der Arbeitsplatzgruppe zugewiesen.

Wenn die Kapazität von Arbeitsplätzen keinen Beitrag zur Gesamtkapazität leisten soll, können Sie dies mit der Effektivität = 0 erreichen.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>So wird ein in der Kapazität eingeschränkter Arbeitsplatz oder Arbeitsplatzgruppe eingerichtet

Sie müssen die Produktionsressourcen einrichten, die Sie als kritisch betrachten, damit diese nur eine Auslastung bis zu einer Kapazitätsgrenze annimmt, anstelle der Standardeinstellung ohne Kapazitätsgrenze, die andere Produktionsressourcen annehmen. Eine Ressource mit eingeschränkter Kapazität kann eine Arbeitsplatzgruppe oder ein Arbeitsplatz sein, den Sie als Flaschenhals erkannt haben und dessen Auslastung Sie deshalb begrenzen möchten.

[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt keine ausführliche Fertigungsbereichssteuerung. Planung einer durchführbaren Nutzung von Ressourcen durch Bereitstellung eines Rohschnittzeitplans, jedoch keine automatische Erstellung und Verwaltung von detaillierten Plänen, die auf Prioritäten oder Optimierungsregeln basieren.

Auf der Seite **Ressourcen mit eingeschränkter Kapazität** können Sie ein Setup vornehmen, das eine Überladung bestimmter Ressourcen verhindert und sicherstellt, dass keine Kapazität unzugewiesen bleibt, wenn dies die Durchlaufzeit eines Fertigungsauftrags erhöhen könnte. Im Feld **Toleranz (% der gesamten Kapazität)** können Sie eine Toleranzperiode zu Ressourcen hinzufügen, um die Aufspaltung von Arbeitsgängen zu minimieren. Dies ermöglicht dem System, Auslastung am letzten möglichen Tag zu planen, indem es den kritischen Auslastungsprozentsatz etwas überschreitet, wenn dies die Anzahl der Arbeitsgänge verringern kann, die aufgeteilt werden.

Beim Planen mit eingeschränkter Kapazität stellt sicher das System sicher, dass keine Ressourcen oberhalb der definierten Kapazität (Grenzbelastung) geladen werden. Dies geschieht, indem jeder Arbeitsgang dem nächsten verfügbaren Zeitfenster zugewiesen wird. Wenn das Zeitfenster nicht ausreicht, um den gesamten Arbeitsgang abzuschließen, wird der Arbeitsgang in zwei Teile aufgeteilt, die in die nächsten verfügbaren Zeitfenster gesetzt werden.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Kapazitätsengpässe bei den Ressourcen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** .
3. Füllen Sie die Felder je nach Bedarf aus.

> [!NOTE]
> Vorgänge auf Arbeitsplätzen oder Arbeitsplätzen, die als eingeschränkte Ressourcen eingerichtet wurden, werden immer seriell geplant. Das bedeutet, dass immer wenn eine eingeschränkte Ressource mehrere Kapazitäten hat, dann können diese Kapazitäten nur nacheinander und nicht nebeneinander geplant werden, wie es der Fall wäre, wenn der Maschinen- oder der Arbeitsplatz nicht als eingeschränkte Ressource eingerichtet wurde. In einer eingeschränkten Ressource ist das Feld Kapazität der Arbeitsplatzgruppe oder der Arbeitsplatz größer als 1.

> Im Falle der Teilung des Arbeitsgangs wird die Rüstzeit nur einmal zugeordnet, da davon ausgegangen wird, dass einige manuelle Ausgleiche vorgenommen werden, um den Plan zu optimieren.

## <a name="see-also"></a>Siehe auch

[Einkaufskalender einrichten](production-how-to-create-work-center-calendars.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)  
[Planung](production-planning.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
