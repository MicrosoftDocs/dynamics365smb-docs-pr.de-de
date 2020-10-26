---
title: Einrichtung der Kostenrechnung | Microsoft Docs
description: Bevor Sie die Arbeit mit der Kostenrechnung beginnen können, müssen Sie Einrichtungsaufgaben ausführen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d39d30891d822c25b0ce4aaec84bbbbc714ae311
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910755"
---
# <a name="setting-up-cost-accounting"></a>Einrichten der Kostenrechnung
Bevor Sie die Arbeit mit der Kostenrechnung beginnen können, müssen Sie Einrichtungsaufgaben ausführen.

## <a name="balances-between-cost-type-cost-center-and-cost-object"></a>Salden zwischen Kostenart, Kostenstelle und Kostenträger
Wenn Sie die Kostenrechnung einrichten, müssen Sie sicherstellen, dass alle Daten einer Kostenart sowie einer Kostenstelle oder einem Kostenträger zugeordnet sind. Das bedeutet, dass jedem Kostenposten eine Kostenart und eine Kostenstelle oder ein Kostenträger zugewiesen sein muss. Diese Regel stellt sicher, dass jeder Kostenposten entweder in Kostenstellen oder in den Kostenträgern erscheint, jedoch nicht an beiden Stellen.  

Auf diese Weise erstellen Sie die folgende Buchhaltungsgleichung:  

*Kostenart-Saldo* = *Kostenstellen-Saldo* + *Kostenträger-Saldo*  

Wenn Sie den Kostenartenplan, den Kostenstellenplan und den Kostenträgerplan drucken, können Sie diese Beziehung analysieren.

## <a name="setting-up-cost-types"></a>Einrichten von Kostenarten
Kostenartenpläne ähneln Kontenpläne im Sachkonto. Sie können den Kostenartenplan auf die folgenden Weisen einrichten:  

-   Strukturieren Sie den Kostenartenplan ähnlich wie GuV-Konten im Sachkontenplan. Dann können Sie den Sachkontenplan in den Kostenartenplan übertragen. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
-   Erstellen Sie einen neuen Kostenartenplan, oder fügen Sie einem vorhandenen Kostenartenplan neue Kostenarten hinzu. Sie müssen jede neue Kostenart einzeln erstellen.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>So übertragen Sie den Sachkontenplan in den Kostenartenplan.  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Diagramm der Kostenarten** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Kostenarten aus K&ontenplan abrufen** . Klicken Sie im Dialogfeld auf die Schaltfläche **Ja** , um die Übertragung zu bestätigen. Die Funktion verwendet den Kontenplan, um einen Kostenartenplan zu erstellen.  

    Der Kostenartenplan enthält jetzt alle GuV-Konten im Sachkonto und umfasst Überschriften und Zwischensummen. Sie können den Kostenartenplan ändern, falls erforderlich. Beispielsweise können Sie doppelt vorhandene Kostenarten löschen.  

    > [!IMPORTANT]  
    >  Die **Kostenarten in Kontenplan registrieren** -Funktion aktualisiert das Verhältnis zwischen dem Kontenplan und dem Kostenartenplan. Das Feld **Nr.** wird ausgefüllt und geprüft, um sicherzustellen, dass jedes Sachkonto mit nur einer Kostenart verknüpft ist. Die Funktion wird automatisch ausgeführt, bevor Sie Sachposten in die Kostenrechnung übertragen.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a>So richten Sie auf der Seite "Liquiditätskontenplan" neue Liquiditätskonten ein  
1.  Öffnen Sie die Seite **Kontenplan-Arten** im Bearbeitungsmodus.  
2.  Füllen Sie je nach Bedarf die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Sie können Kostenarten auf der Seite **Kostenartkarte** oder auf der Seite **Kostenartenplan** einrichten und verwalten. So richten Sie auf der Seite **Liquiditätskontenplan** neue Liquiditätskonten ein.

3.  Nachdem Sie alle Kostenarten erstellt haben, wählen Sie die Aktion **Kostenarten einrücken** aus. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja** .  
4.  Verknüpfen Sie die neue Kostenart mit dem entsprechenden Sachkonto.  

    > [!IMPORTANT]  
    >  Wenn Sie in den Feldern **Zusammenzählung** Definitionen für die Zeilenart **Bis-Summe** eingetragen haben, bevor Sie die Funktion **Kostenarten einrücken** ausgeführt haben, müssen Sie diese Eintragungen wiederholen, da die Funktion die Werte in allen **Bis-Summe** -Feldern überschreibt.  

### <a name="to-update-cost-types"></a>So aktualisieren Sie Kostenarten  
1.  Auf der Seite **Kostenrechnung einrichten** wählen Sie aus, ob der Kostenartenplan automatisch aktualisiert werden soll, wenn der Kontenplan geändert wird.  
2.  Die folgenden Optionen stehen im Feld **Sachkonto ausrichten** zur Auswahl.  

- **Keine Ausrichtung** - Es gibt keine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.  
- **Automatisch** - Es gibt eine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.  
- **Eingabeaufforderung** - Eine Meldung wird mit der Frage angezeigt, ob Sie die entsprechende Änderung auch im Kostenartenplan vornehmen möchten, wenn Sie den Kontenplan ändern.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a>Definieren der Beziehung zwischen Kostenarten und Sachkonten
Das Verbindung zwischen der Kostenart und dem Sachkonto wird in der Kostenart und im Sachkonto erstellt.  

* Das Feld **Fibu-Kontenbereich** in der Tabelle **Kostenart** bestimmt, welche Sachkonten zu einer Kostenart gehören.  
* Das **Kostenartennummer** Feld im Kontenplan bestimmt, zu welcher Kostenart ein Sachkonto gehört.  

Diese beiden Felder werden automatisch ausgefüllt, wenn Sie die **Kostenarten aus Kontenplan abrufen** -Funktion verwenden.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types"></a>Beziehung zwischen Sachkonten und Kostenarten  
Zwischen Sachkonten und Kostenarten besteht eine n:1-Beziehung. Mehrere Sachkonten können zu einer Kostenart gehören, aber jedes Sachkonto gehört nur zu einer Kostenart. Die folgende Tabelle beschreibt die Einzelheiten der Beziehung.  

|Verbindungen|**Sachkontobereich**|**Kostenartnr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Ein Sachkonto für jede Kostenart|Ein Sachkonto|Eine Kostenart|  
|Mehrere Sachkonten für eine Kostenart|Sachkontobereich, z. B. 7110 ... 7193 für jedes Sachkonto|Für jedes Sachkonto im Bereich gibt es nur eine Kostenart|  
|Kostenarten ohne entsprechende Sachkonten|<Empty>||  
|Sachkonten, deren Posten nicht übertragen werden||<Empty>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger"></a>Kostenarten ohne Beziehung zum Sachkonto  
Eine Kostenart hat möglicherweise keine Beziehung zu Sachkonten, wenn eine der folgenden Bedingungen zutrifft:  

* Konten für die betriebliche Buchhaltung, wie Berech. Zinsen und Abschreibungen, entnehmen nur Kosten aus der betrieblichen Buchhaltung.  
* Helfende Kostenarten, wie Kostenarten 9901, 9902 und 9903 in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, werden als Haben- und Sollbeträge für Zuordnungen verwendet.  
* Das helfende Konto, 9920 in der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank, enthält tatsächliche Zugänge, die die Differenz zwischen Kosten und Ausgaben des Sachkontos anzeigen.

## <a name="setting-up-cost-centers"></a>Einrichten von Kostenstellen
Kostenstellen sind Abteilungen, die für die Kosten und die Einnahmen zuständig sind. Der Kostenstellenplan ähnelt den Dimensionsinformationen für das Sachkonto. Sie können den Kostenstellenplan auf die folgenden Weisen einrichten:  

-   Transferieren Sie Dimensionswerte im Sachkonto zum Kostenstellenplan. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
-   Erstellen Sie einen neuen Kostenstellenplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenstellenplan eine neue Kostenstelle hinzu. Sie müssen jede Kostenstelle einzeln erstellen.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a>So transferieren Sie Dimensionswerte im Sachkonto zum Kostenstellenplan  
1.  Richten Sie eine Dimension als Kostenstellendimension auf der Seite **Kostenstellendimension aktualisieren** ein. Nur die Werte aus dieser Dimension werden übertragen.  
2.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Diagramm der Kostenstellen** ein und wählen Sie dann den entsprechenden Link.  
3.  Klicken Sie auf der Registerkarte **Aktionen** in der Gruppe **Funktion** auf **Kostenstellen aus Dimension abrufen** , um Dimensionswerte zum Kostenstellenplan zu übertragen. Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.  

    > [!NOTE]  
    >  Sie können das Feld **Kostenstellendimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Sachkonto zum Kostenstellenplan definiert wird. Sie können keine Synchronisierung des Kostenstellenplans mit Dimensionswerten aus dem Sachkonto definieren.  

Der Kostenstellenplan enthält jetzt alle angegebenen Dimensionswerte aus dem Sachkonto und umfasst Titel und Zwischensummen.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page"></a>So richten Sie auf der Seite Kostenstellenplan neue Kostenstellen ein  
Sie können Kostenkarten auf der Seite **Kostenstellen** oder auf der Seite **Kostenstellenkarte** einrichten und verwalten. So richten Sie auf der Seite **Kostenstellenplan** neue Kostenstellen ein.  

1. Öffnen Sie die Seite **Kontenplan-Kostenstellen** im Bearbeitungsmodus.  
2. Geben Sie im Feld **Code** den Kostenstellencode ein. Alle Kostenstellen müssen einen Code aufweisen.  
3. Geben Sie im Feld **Namen** den Kostenstellennamen ein.  
4. Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck der Kostenstelle anzugeben.  

    - Für Kostenstellen der Art **Summe** müssen Sie das Feld **Zusammenzählung** ausfüllen. Verwenden Sie den **Oder** -Operator, der eine vertikale Zeile ( **&#124;** ) ist, um Bereiche von Kostenstellen festzulegen.  
    - Für Kostenstellen der **Bis-Summe** -Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.  
5.  Füllen Sie die Felder **Sortierreihenfolge** und **Kostenunterart** aus.  
6.  Wählen Sie die nächste leere Zeile aus, um eine neue Kostenstelle zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.  
7.  Nachdem Sie alle Kostenstellen eingerichtet haben, wählen Sie die Aktion **Kostenstellen einrücken** aus. Wählen Sie die Schaltfläche **Ja** aus.  

> [!IMPORTANT]  
>  Wenn Sie Definitionen in den **Zusammenzählung** -Feldern für **Bis-Summe** -Kostenstellen eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben. Die Funktion überschreibt die Werte in allen **Bis-Summe** -Feldern.

## <a name="setting-up-cost-objects"></a>Einrichten von Kostenträgern
Kostenträger sind Projekte, Produkte oder Services eines Unternehmens. Der Kostenträgerplan ähnelt den Dimensionsinformationen für das Sachkonto. Sie können den Kostenträgerplan auf die folgenden Weisen einrichten:  

* Transferieren Sie Dimensionswerte im Sachkonto zum Kostenträgerplan. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
* Erstellen Sie einen neuen Kostenträgerplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenträgerplan einen neuen Kostenträger hinzu. Sie müssen jeden Kostenträger einzeln erstellen.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>So transferieren Sie Dimensionswerte aus dem Sachkonto zum Kostenträgerplan  
1.  Legen Sie eine Dimension als Kostenträgerdimension auf der Seite **Kostenträger-Dimensionen aktualisieren** fest. Nur die Werte aus dieser Dimension werden übertragen.  
2.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Diagramm der Kostenträger** ein und wählen Sie dann den entsprechenden Link.  
3.  Wählen Sie die Aktion **Kostenträger aus Dimension abrufen** , um Dimensionswerte zum Kostenträgerplan zu übertragen. Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.  

    > [!NOTE]  
    >  Sie können das Feld **Kostenträgerdimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Sachkonto zum Kostenträgerplan definiert wird. Sie können keine Synchronisierung des Kostenträgerplans mit Dimensionswerten aus dem Sachkonto definieren.  

Der Kostenträgerplan enthält jetzt alle angegebenen Dimensionswerte aus dem Sachkonto und umfasst Titel und Zwischensummen.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page"></a>So richten Sie auf der Seite Kostenstellenträger neue Kostenträger ein  
Sie können Kostenkarten auf der Seite **Kostenträger** oder im Fenster **Kostenträgerkarte** einrichten und verwalten. So richten Sie auf der Seite **Kostenträger** neue Kostenstellenträger ein.  

1.  Öffnen Sie die Seite **Kontenplan-Objekte** im Bearbeitungsmodus.  
2.  Geben Sie im Feld **Code** den Kostenträgercode ein. Alle Kostenträger müssen einen Code aufweisen.  
3.  Geben Sie im Feld **Namen** den Kostenträgernamen ein.  
4.  Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck des Kostenträgers anzugeben.  

    * Für Kostenträger der **Summe** -Zeilenart müssen Sie das Feld **Summe Von/Bis** ausfüllen. Verwenden Sie den **Oder** -Operator, der eine vertikale Zeile ( **&#124;** ) ist, um Bereiche von Kostenträgern festzulegen.  
    * Für Kostenträger der **Bis-Summe** -Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.  
5.  Füllen Sie das Feld **Sortierungsauftrag** aus.  
6.  Wählen Sie die nächste leere Zeile aus, um einen neuen Kostenträger zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.  
7.  Nachdem Sie alle Kostenträger eingerichtet haben, wählen Sie die Aktion **Kostenträger einrücken** aus. Wählen Sie die Schaltfläche **Ja** aus.  

> [!IMPORTANT]  
>  Wenn Sie Definitionen in den **Summe Von/Bis** -Feldern für **Bis-Summe** -Kostenträger eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben. Die Funktion überschreibt die Werte in allen **Bis-Summe** -Feldern.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definieren von Kostenstellen und Kostenträgern für Kontenpläne
Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen. Wenn Sie die Übertragung ausführen, überträgt [!INCLUDE[d365fin](includes/d365fin_md.md)] nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind. Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definieren von Standarddimensionswerten für Sachkonten  
Für jedes Sachkonto können Sie Standarddimensionswerte in der Tabelle **Standard-Dimensionen** definieren. Das folgende Beispiel zeigt, wie Sie definieren, dass es immer eine Kostenstelle ABTEILUNG, aber nie einen Kostenträger PROJEKT geben soll, wenn Sie auf ein Sachkonto buchen.  

|**Dimensionscode**|**Dimensionswertbuchung**|  
|------------------------------------------|-----------------------------------------|  
|Abteilung|Code notwendig|  
|Kostenträger|Kein Code|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definieren von Dimensionswerten für Gemeinkosten und direkte Kosten  
 Sie können Gemeinkosten an eine Kostenstelle und direkte Kosten an einen Kostenträger übertragen. In der folgenden Tabelle wird die optimale Kombination aus Dimensionseinrichtungswerten angezeigt.  

|Übertragen in|Kostenstellenbuchung|Kostenträgerbuchung|  
|-----------------|-------------------------|-------------------------|  
|Kostenstelle|Code notwendig|Kein Code|  
|Kostenträger|Kein Code|Code notwendig|  

> [!NOTE]  
>  Um sicherzustellen, dass die vordefinierte Kostenstelle und der vordefinierte Kostenträger, die bzw. den Sie im Sachkonto eingerichtet haben, automatisch in die Kostenrechnung übertragen werden, aktivieren Sie das Kontrollkästchen **Fibu-Buchung prüfen** auf der Seite Kosenbuchungseinrichtung.

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)   
[Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
