---
title: 'So geht es: Nachfrageplanung erstellen | Microsoft Docs'
description: Verkaufs- und Absatzplanungen können auf der Seite **Nachfrageplanung** vorgenommen werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: b62d947a72de677466aadee4a657c970a6133919
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3190587"
---
# <a name="create-a-demand-forecast"></a>Bedarfsplanung erstellen
Verkaufs- und Absatzplanungen können auf der Seite **Nachfrageplanung** vorgenommen werden.  

Die Absatzplanungsfunktionen werden verwendet, um voraussichtlichen Bedarf zu erstellen; der tatsächliche Bedarf wird aus Verkaufs- und Fertigungsaufträgen erstellt. Beim Erstellen des Produktionsplans (Master Production Schedule, MPS) wird die Planung gegen die Verkaufs- und Fertigungsaufträge aufgerechnet. Mit der Absatzplanungsoption *Komponente* wird festgelegt, welche Anforderungen bei einem Saldierungsvorgang berücksichtigt werden sollen. Gilt die Absatzplanung für einen Verkaufsartikel, werden nur Verkaufsaufträge gegen die Absatzplanung saldiert. Wenn sie für Komponenten gilt, wird nur der abhängige Bedarf aus Fertigungsauftragskomponenten gegen die Absatzplanung saldiert.  

Absatzplanung ermöglicht es Ihnen, "Was-wenn"-Szenarien zu erstellen sowie effizient und Kosten sparend für den Bedarf zu planen und diesen zu befriedigen. Eine genaue Absatzplanung kann den entscheidenden Unterschied bei der Kundenzufriedenheit hinsichtlich Lieferterminzusagen und termingerechter Lieferung ausmachen.  

## <a name="sales-forecasts-and-production-forecasts"></a>Absatzplanungen und Fertigungsplanungen  
Die von der Anwendung bereitgestellten Absatzplanungsfunktionen können dazu verwendet werden, Absatz- oder Fertigungsplanungen zusammen oder voneinander unabhängig zu erstellen. Beispielsweise haben die meisten Auftragsfertigungsunternehmen keine fertigen Waren auf Lager, weil jeder Artikel erst nach der Bestellung gefertigt wird. Das Vorhersagen von Aufträgen (Absatzplanung) ist entscheidend für eine angemessene Verweilzeit der Halbwaren (Fertigungsplanung). So können z. B. Komponententeile mit langen Lieferzeiten, wenn sie nicht bestellt oder auf Lager sind, zu einer Fertigungsverzögerung führen.  

-   Die Absatzplanung ist die beste Schätzung der Verkaufsabteilung, welche Mengen zukünftig verkauft werden, und wird nach Artikel und Periode angegeben. Die Absatzplanung ist aber nicht immer der Fertigung angemessen.  
-   Bei der Absatzplanung handelt es sich um die Prognose des Produktionsplaners hinsichtlich der Anzahl von Endartikeln und entsprechenden Halbfabrikaten, die in bestimmten Perioden produziert werden müssen, um den geplanten Verkauf zu decken.  

In den meisten Fällen ändert der Fertigungsplaner die Absatzplanung dann entsprechend den Gegebenheiten der Fertigung, wobei die Absatzplanung dennoch weiterhin erfüllt wird.  

Das Erstellen von Absatzplanungen erfolgt manuell auf der Seite **Nachfrageplanung**. Es können mehrere Absatzplanungen vorhanden sein, die nach Name und Art unterschieden werden. Eine Absatzplanung kann je nach Bedarf kopiert und bearbeitet werden. Für Planungszwecke ist aber immer nur jeweils eine Absatzplanung zulässig.  

Eine Absatzplanung besteht aus einer Reihe von Datensätzen, wobei in jedem Datensatz die Artikelnummer, das Planungsdatum und die Planungsmenge angegeben sind. Die Absatzplanung eines Artikels erstreckt sich über eine Periode, die durch das Planungsdatum des aktuellen sowie das Planungsdatum des nächsten (späteren) Planungsdatensatzes definiert ist. Aus Planungssicht sollte die Planungsmenge zu Beginn der Bedarfsperiode verfügbar sein.  

Sie müssen eine Absatzplanung als *Verkaufsartikel*, *Komponente* oder *Beides* kennzeichnen. Die Planungsart *Verkaufsartikel* wird für Absatzplanungen verwendet. Die Fertigungsplanung wird mit der Art *Komponente* erstellt. Die Planungsart *Beides* wird nur verwendet, um dem Planer einen Überblick über die Absatz- und die Fertigungsplanung zu geben. Bei dieser Option können die Planungsposten nicht bearbeitet werden. Durch Kennzeichnen mit diesen Planungsarten können Sie zum Eingeben einer Absatzplanung dasselbe Vorschlagsblatt wie für eine Fertigungsplanung verwenden und können Sie beide Planungen auf demselben Blatt anzeigen. Beachten Sie, dass die unterschiedlichen Eingaben (Absatz und Fertigung) beim Berechnen der Planung entsprechend der Artikel- und Produktionseinrichtung unterschiedlich behandelt werden.  

## <a name="component-forecast"></a>Komponentenabsatzplanung  
Die Komponentenabsatzplanung kann als eine Optionsplanung in Bezug auf einen übergeordneten Artikel angesehen werden. Dies kann beispielsweise hilfreich sein, wenn der Planer den Bedarf für die Komponente schätzen kann.  

Da die Komponentenabsatzplanung dazu verwendet wird, Optionen für einen übergeordneten Artikel zu definieren, muss die Menge für die Komponentenabsatzplanung kleiner gleich der Planungsmenge des Verkaufsartikels sein. Ist die Menge für die Komponentenabsatzplanung größer als die Planungsmenge des Verkaufsartikels, wird die Differenz zwischen diesen beiden Planungsarten als unabhängiger Bedarf angesehen.  

## <a name="forecasting-periods"></a>Planungsperioden  
 Die Planungsperiode erstreckt sich von ihrem Startdatum bis zu dem Datum, an dem die nächste Absatzplanung beginnt. Auf der Seite für Zeitintervalle haben Sie mehrere Auswahlmöglichkeiten, um den Bedarf für ein bestimmtes Datum einer Periode einzufügen. Es empfiehlt sich daher, den Bereich einer Planungsperiode nicht zu ändern, es sei denn, sie möchten alle Planungsposten auf das Startdatum dieser Periode verschieben.  

## <a name="forecast-by-locations"></a>Absatzplanung nach Lagerorten  
In der Produktionseinrichtung kann festgelegt werden, wenn Sie Filter nach Lagerorten zu prognostizieren soll, wenn Sie einen Plan berechnen. Beachten Sie aber , dass die Gesamtabsatzplanung möglicherweise nicht repräsentativ ist, wenn auf dem Lagerort basierende Absatzplanungen isoliert angezeigt werden.

## <a name="to-create-a-demand-forecast"></a>So erstellen Sie eine Absatzplanung

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Bedarfsplanung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Inforegister **Allgemein** im Feld **Nachfragelanungsname** eine Planung aus. Es können mehrere Absatzplanungen vorhanden sein, die nach Name und Absatzplanungsart unterschieden werden.  
3. Im Feld **Lagerortfilter** müssen Sie den Lagerort auswählen, für den die Planung gelten soll.
4. Im Feld **Anzeigen nach**, um den Zeitraum zu ändern, der in jeder Spalte angezeigt wird. Folgende Intervalle stehen zur Auswahl: **Tag**, **Woche**, **Monat**, **Quartal**, **Jahr** oder **Buchhaltungsperiode**, gemäß Einrichtung in Ihrem Finanzbereich.    

> [!NOTE]  
>  Sie sollten sich sehr gut überlegen, welches Zeitintervall für zukünftige Absatzplanungen verwendet werden soll, sodass das Zeitintervall durchgängig einheitlich ist. Wenn Sie eine Planungsmenge eingeben, gilt diese am ersten Tag des ausgewählten Zeitintervalls. Wenn Sie also beispielsweise "Monat" ausgewählt haben, geben Sie die Planungsmenge für den ersten Tag des Monats ein. Wenn Sie "Quartal" ausgewählt haben, geben Sie die Planungsmenge für den ersten Tag des ersten Monats des Quartals ein.

5. Wählen Sie im Feld **Anzeigen als** aus, wie die Planungsmengen für das Zeitintervall dargestellt werden sollen. Bei Auswahl von **Bewegung** wird die Bewegung im Saldo für das Zeitintervall angezeigt. Bei Auswahl von **Saldo bis Datum** wird auf der Seite der Saldo zum letzten Tag des Zeitintervalls angezeigt.  
6. Wählen Sie im Feld **Planungsart** eine Option aus: **Verkaufsartikel**, **Komponente** oder **Beides**. Wenn Sie **Verkaufsartikel** oder **Komponente** ausgewählt haben, können Sie die Menge pro Periode bearbeiten. Wenn Sie **Beides** ausgewählt haben, können Sie die Menge zwar nicht bearbeiten, Sie haben jedoch die Möglichkeit, sie im Dropdown-Menü auszuwählen und die Absatzplanungsposten anzuzeigen.  
7. Geben Sie einen **Datumsfilter** an, wenn Sie den Umfang der angezeigten Daten beschränken möchten.  
8. Im Inforegister **Bedarfsprognosematrix** geben Sie die prognostizierten Megnen an, indem Sie eine Menge in die Zelle eingeben, die ein Artikel darstellt zu einem bestimmten Datum oder in einem bestimmten Zeitraum. Beachten Sie, dass in leeren Zellen die Suchschaltfläche eine leere Seite öffnet, die angibt, dass Sie einen Wert manuell eingeben müssen.   

> [!NOTE]  
>  Sie haben auch die Möglichkeit zum Bearbeiten einer bestehenden Absatzplanung. Klicken Sie auf der Seite **Nachfrageplanungsmatrix** auf **Aktionen, Absatzplanung kopieren**, und füllen Sie die Seite **Absatzplanung** mit einer vorhandenen Planung aus. Die Mengen können anschließend gemäß den Anforderungen bearbeitet werden.  

## <a name="see-also"></a>Siehe auch  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)   
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
