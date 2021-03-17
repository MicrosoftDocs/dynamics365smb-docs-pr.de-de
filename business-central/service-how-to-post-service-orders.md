---
title: 'Vorgehensweise: Buchen von Serviceaufträgen | Microsoft Docs'
description: Nachdem Sie einen Serviceauftrag erstellt und eventuelle Änderungen vorgenommen haben, können Sie den Serviceauftrag buchen. Der Serviceauftrag muss mindestens eine Serviceartikelzeile und eine Servicezeile enthalten, bevor Sie den Auftrag buchen können. Sollte der Auftrag mehr als eine Serviceauftragszeile umfassen, bucht die Anwendung alle Zeilen in einem Durchgang.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8021015e9a1284aac815b93418a0b51e0064d8f5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389699"
---
# <a name="post-service-orders-and-credit-memos"></a>Buchen von Serviceaufträgen und Gutschriften
Nachdem Sie einen Serviceauftrag erstellt und eventuelle Änderungen vorgenommen haben, können Sie den Serviceauftrag buchen. Der Serviceauftrag muss mindestens eine Serviceartikelzeile und eine Servicezeile enthalten, bevor Sie den Auftrag buchen können. Sollte der Auftrag mehr als eine Serviceauftragszeile umfassen, bucht die Anwendung alle Zeilen in einem Durchgang.  

Wenn Sie eine große Anzahl an Serviceaufträgen haben, können Sie Zeit sparen, wenn Sie diese mit einer Stapelverarbeitung buchen. Sie können diese Stapelverarbeitung aus jedem Serviceauftrag ausführen.

> [!Tip]
> Bevor Sie einen Servicebeleg buchen, ist es vorteilhaft, die **Bericht testen** Aktion zu nutzen, um jeden Fehler oder fehlende Informationen zu prüfen. Wenn es Fehler gibt, müssen Sie das jeweilige Problem lösen. Sie können einen neuen Testbericht ausdrucken, um die Behebung zu bestätigen, und den Beleg dann buchen.

## <a name="to-post-a-service-order"></a>So buchen Sie einen Serviceauftrag    
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den relevanten Serviceauftrag.  
3. Auf der Seite **Serviceauftrag** wählen Sie eine der folgenden Aktionen aus.  

    |**Aktion**|**Ergebnis**|  
    |------------------|----------------|  
    |**Testbericht** | Überprüft alle Teile des Belegs und zeigt das Ergebnis in einem Bericht an. Wenn der Bericht Fehler oder fehlende Informationen angibt, müssen Sie das jeweilige Problem beheben. Sie können dann einen neuen Testbericht drucken.|  
    |**Buchen** | Bucht den Auftrag, ohne einen Lieferschein oder eine Rechnung zu drucken.|  
    |**Buchen und Drucken** | Bucht den Auftrag und druckt einen Lieferschein (wenn Sie den Auftrag liefern, ohne ihn zu fakturieren) oder eine Rechnung (wenn Sie den Auftrag fakturieren).|  
    |**Stapelbuchen** | Bucht mehrere Serviceaufträge einmal gleichzeitig.|  

4. Wenn Sie den Auftrag buchen, müssen Sie auswählen, wie Sie den Auftrag buchen möchten. Sie haben folgende Optionen:  

    |**Buchungsoption**|**Ergebnis**|  
    |------------------------|----------------|  
    |**Lieferung** | Bucht die Lieferung der Artikel.|  
    |**Fakturieren** | Fakturiert Artikel, die bereits geliefert wurden.|  
    |**Lieferung und Rechnung** | Fakturiert und liefert die Artikel.|  
    |**Liefern und verbrauchen** | Bucht die Lieferung und den Verbrauch für den Auftrag. Darüber hinaus werden die relevanten Mengen in den Servicezeilen des Auftrags und in den Servicelieferungsbelegen aktualisiert, die im Vorfeld für die Zeile gebucht wurden.|  

Sie können den Verbrauch nur buchen, wenn die Zeile eine Menge enthält, die geliefert, jedoch nicht fakturiert oder verbraucht wurde.  

Beim Buchen des Auftrags werden die entsprechenden Posten und gebuchten Belege erstellt. Die relevanten Felder werden im Serviceauftragsbeleg aktualisiert.  

## <a name="to-batch-post-service-orders"></a>So buchen Sie Serviceaufträge per Batchauftrag
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Stapelbuchen** aus.  
3.  Sie können einen Filter setzen, um bestimmte Serviceauftragsnummern oder ein Intervall von Auftragsnummern auszuwählen.  
4.  Klicken Sie zum Starten des Batchauftrags auf **OK**.  

## <a name="to-post-a-service-credit-memo"></a>So buchen Sie Servicegutschriften  
Wenn Sie eine Servicegutschrift erstellt und ausgefüllt haben, können Sie diese Gutschrift buchen. Wenn beim Buchen Fehler oder fehlende Informationen in der Gutschrift vorhanden sind, wird der Vorgang durch eine Fehlermeldung unterbrochen.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Servicegutschriften** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie eine neue Servicegutschrift. Wählen Sie die Aktion **Neu**.  
3. Füllen Sie die erforderlichen Felder aus.  
4. Wählen Sie die Aktion **Buchen** aus. Wenn Sie die Gutschrift gleichzeitig mit der Buchung drucken möchten, wählen Sie stattdessen die Aktion **Buchen und Drucken**.  
5. Um Gutschriften vor dem Buchen zu prüfen, aktivieren Sie **Testbericht**. Wenn Sie den Bericht ausführen, werden die Buchungsdaten, die im Beleg angegeben wurden, und weitere Daten überprüft.  
6. Bucht mehrere Servicegutschriften gleichzeitig. führen Sie die Stapelverarbeitung **Servicegutschriften stapelbuchen** aus. Das kann vorteilhaft sein, wenn Sie sehr viele Gutschriften buchen müssen.  

> [!NOTE]  
>  Es ist wichtig, dass alle erforderlichen Informationen für die Gutschriften vor dem Stapelbuchen eingegeben werden. Anderenfalls kann es geschehen, dass sie nicht gebucht werden. Sind die Buchungen durch den Batchauftrag abgeschlossen, zeigt eine Meldung an, wie viele der Servicegutschriften gebucht worden sind.  

## <a name="to-post-consumption-from-a-service-order"></a>So buchen Sie den Verbrauch von Serviceaufträgen aus  
Im folgenden Verfahren wird beschrieben, wie die Artikel, Ressourcenzeiten und/oder Kosten für eine bestimmte Servicearbeit gebucht werden, die Sie dem Debitor nicht in Rechnung stellen. Der Verbrauch von Artikeln, Stunden oder Kosten kann nur für eine gebuchte Lieferung gebucht werden, für die keine Rechnungen und kein Verbrauch gebucht wurde.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den Serviceauftrag, für den der Verbrauch gebucht werden soll.  
3. Wählen Sie den Serviceartikel aus. Wählen Sie die Aktion **Servicezeilen**.  
4. Suchen Sie nach den entsprechenden Posten, und geben Sie im Feld **Mge. zu verbrauchen** die Mengen an, für die Sie den Verbrauch buchen. Die Menge kann nicht größer als die bereits gelieferte Menge und die nicht fakturierte Restmenge nach einer teilweisen Fakturierung dieser Lieferung sein.  

    > [!NOTE]  
    >  Füllen Sie die Felder **Projektnr.**, **Projektaufgabennr.** und **Projektzeilenart** für die Servicezeile aus, um den Verbrauch in Bezug auf eine Aufgabe zu erfassen.  

5. Wählen Sie die zu buchenden Zeilen aus, und wählen Sie dann die Aktion **Buchen** aus. Wählen Sie auf der daraufhin angezeigten Seite die Option **Liefern und Verbrauchen**.  

Der Service wird als teilweise oder vollständig verbraucht gebucht (abhängig vom Wert im Feld **Mge. zu verbrauchen**) und die entsprechenden Posten werden erstellt. Darüber hinaus aktualisiert die Anwendung die zuvor gebuchten Servicelieferungsbelege chronologisch mit den verbrauchten Mengen. Die entsprechenden Mengen werden in den Servicezeilen des Auftrags aktualisiert.  

## <a name="to-post-shipments-from-service-orders"></a>So buchen Sie Lieferungen von Serviceaufträgen aus  
Nachdem Sie die Details eines Service angegeben haben, können Sie die Mengen für verwendete Artikel, Zeitaufwand und angefallene Kosten anpassen und buchen. Daraufhin werden die erforderlichen Änderungen durch [!INCLUDE[prod_short](includes/prod_short.md)] vorgenommen, sodass der neue Lagerbestand und der aktuelle Status der jeweiligen Auftragsabwicklung widergespiegelt werden.  

Der folgende Ablauf zeigt, wie man Lieferung der Servicezeilenartikel in Lagerplätzen bucht, die nicht so eingerichtet wurden, dass ein Lagerdurchlauf erforderlich ist.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceauftrag** ein und wählen Sie dann den entsprechenden Link. 2. Wählen Sie auf der Seite für den ausgewählten Serviceauftrag **Aktionen**, **Auftrag**, **Servicezeilen** aus.  
3. Suchen Sie auf der Seite **Servicezeilen** nach den entsprechenden Posten, und geben Sie die zu buchende Menge in das Feld **Zu liefern** ein.  

   > [!NOTE]  
   >  Der Wert für die zu liefernde Menge hängt davon ab, ob Sie die Lieferung teilweise oder insgesamt buchen möchten. Bei einer Gesamtlieferung muss der Wert im Feld **Zu liefern** dem Wert im Feld **Menge** entsprechen. Wenn Sie eine teilweise Lieferung buchen, müssen Sie die anfänglich zu liefernde Menge angeben. Wenn bereits ein Teil des Service auf dem Auftrag geliefert wurde, geben Sie diesen Wert im Feld **Menge geliefert** an. Die maximale Menge, die Sie in das Feld **Zu liefern** eingeben können, ist die Anzahl der Einheiten, die noch nicht geliefert wurden.  

4. Wählen Sie die Aktion **Buchen**. auf der angezeigten Seite wählen Sie die Schaltfläche **Versand**.

[!INCLUDE[prod_short](includes/prod_short.md)] Die Anwendung erstellt die Posten (Garantieposten, Artikelposten, Serviceposten oder Sachposten), erzeugt den gebuchten Servicelieferungsbeleg und aktualisiert die entsprechenden Felder in den Serviceauftragszeilen.  

Wenn der Lagerort so eingerichtet wurde, dass ein Lagerdurchlauf erforderlich ist, dann erfolgt die Lieferung und Umlagerung der Servicezeilenartikel auf die gleichen Weise wie für andere Herkunftsbelege. Der einzige Unterschied besteht darin, dass Servicezeilenartikel extern oder intern verbraucht werden können und daher zwei unterschiedliche Freigabefunktionen benötigen.  

Informationen über die Artikellieferung für Herkunftsbelege in den erweiterten Lagerkonfigurationen, finden Sie unter [Artikel für Lager-Lieferung auswählen](warehouse-pick-items.md).  

## <a name="to-undo-posted-consumption"></a>So machen Sie einen gebuchten Verbrauch rückgängig  
Sie können den Verbrauch der Serviceaufträge kündigen. Beispielsweise, da er versehentlich gebucht wurde.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Servicelieferungen** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie die gebuchte Servicelieferung, für die der fehlerhafte Verbrauch gebucht wurde.  
3. Wählen Sie die Aktion **Servicelinien**.  
4. Wählen Sie die Zeilen, die den falschen Verbrauch enthalten aus, und wählen die **Verbrauch stornieren** Aktion aus.  

 Für den Ausgleich wird eine Servicelieferungszeile mit negativen Werten in den Mengenfeldern für die ausgewählten Zeilen eingefügt.  
  
> [!NOTE]  
>  Sie können Dienstverbrauch nicht rückgängig machen, wenn:  

>    * Der Serviceauftrag geschlossen wurde.  
>    * Er für im Modul "Projekte" gebucht wurde und Projektposten zugeordnet sind.  

## <a name="to-post-service-lines"></a>So buchen Sie Servicezeilen  
Wenn Sie für längere Zeit mit einem Serviceauftrag arbeiten müssen, ohne diesen zu buchen, möchten Sie ggf. schon einige der Zeilen buchen, die damit verknüpft sind, z. B. um das Lager auf dem aktuellen Stand zu halten. Sie können buchen, indem Sie die relevanten Mengen in den zu buchenden Zeilen angeben. Sie können die Zeilen einzeln oder mehrere Zeilen gleichzeitig buchen.  

Die folgende Vorgehensweise beschreibt, wie die Lieferungsbuchung direkt aus einem Serviceauftrag heraus für Lagerorte ohne Lagerkosteneinrichtung erfolgt. Wenn der Lagerort so eingerichtet wurde, dass ein Lagerdurchlauf erforderlich ist, dann erfolgt die Lieferungsbuchung in einem anderen Logistikbeleg, abhängig von der Einrichtung des Lagerorts.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den relevanten Serviceauftrag, und wählen Sie die **Servicezeilen** Aktion aus.  
4. Füllen Sie in den Zeilen, die Sie buchen möchten, die Felder **Zu liefern**, **Zu fakturieren** und **Mge. zu verbrauchen** aus, je nachdem, wie Sie die Zeilen buchen möchten.  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="see-also"></a>Siehe auch  
[Buchen in der Serviceverwaltung](service-service-posting.md)  
[Erstellen eines Serviceauftrags](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]