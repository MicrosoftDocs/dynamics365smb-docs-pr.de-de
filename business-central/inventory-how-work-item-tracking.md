---
title: Zuweisen von Serien- und Chargennummern zu Artikeln für die Nachverfolgung | Microsoft Docs
description: Sie können Serien-/Chargennummern zu beliebigen ausgehenden oder eingehenden Belegen hinzufügen, und die gebuchte Artikelverfolgung wird in den entsprechenden Buchungsposten angezeigt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1ffb80f4571e96dcaa8acfbcb106f7fb582b4783
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377573"
---
# <a name="work-with-serial-and-lot-numbers"></a>Arbeiten mit Chargennummern und Seriennummern
Sie können Serien-/Chargennummern zu beliebigen ausgehenden oder eingehenden Belegen zuweisen, und die gebuchte Artikelverfolgung wird in den entsprechenden Buchungsposten angezeigt. Sie führen die Arbeit auf der Seite **Artikelverfolgungszeilen** aus, die Sie über einen eingehenden und ausgehenden Beleg öffnen können.

Die Matrix der Mengenfelder im Kopf der Seite **Artikelnachverfolgungszeile** zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf den Zeilen des Fensters eingegeben werden. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine 0 in den Feldern **Undefiniert** angezeigt wird.

Aus Leistungsgründen sammelt die Anwendung die Verfügbarkeitsinformationen, die auf der Seite **Artikelverfolgungszeilen** angezeigt werden, nur ein Mal, wenn Sie die Seite öffnen. Das heißt, dass die Anwendung die Verfügbarkeitsinformationen während der Zeit, in der die Seite geöffnet ist, nicht aktualisiert, und zwar auch dann nicht, wenn in dieser Zeit Änderungen am Lagerbestand oder an anderen Belegen vorgenommen werden.

Gibt gebuchte Serien-/Chargennummern an, die in einer Lieferkette vorwärts oder rückwärts verfolgt werden können. Dies ist für allgemeine Maßnahmen für die Qualitätssicherung und für Rückrufe eines fehlerhaften Produktes nützlich. Weitere Informationen finden Sie unter [Nachverfolgte Artikel reservieren](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Um in der Kommissionierung spezielle Serien-/Chargennummern zu kommissionieren:
Die Verarbeitung von ausgehenden Serien- oder Chargennummern ist eine häufige Aktivität, die in vielen verschiedenen Lagerprozessen verwendet wird.  

In anderen Prozessen haben die Lagerartikel keine Serien- oder Chargennummern und der Lagermitarbeiter muss bei Ausgangsaktivitäten neue zuordnen, die in der Regel aus einer vordefinierten Nummernserien stammen.

In den einfachen Prozessen haben die Lagerartikel bereits Serien- oder Chargennummern, die beispielsweise während der Einlagerung zugewiesen wurden. Diese Nummern werden ohne Aktivität der Lagermitarbeiter automatisch auf alle ausgehenden Lageraktivitäten übertragen.

In den bestimmten Fällen werden für Serien- oder Charge-numeriertes Lager, bestimmte Serien- oder Chargennummern im Herkunftsbeleg, wie einem Verkaufsauftrag definiert, den der Lagermitarbeiter während der Ausgangsaktivitäten berücksichtigen muss. Dies kann beispielsweise den Grund haben, dass der Debitor während des Bestellvorgangs eine bestimmte Charge fordert. Wenn der Lagerkommissionierungs- oder Kommissionierungsbeleg aus einem ausgehenden Herkunftsbeleg erstellt wird, in dem bereits Artikelverfolgungsnummern definiert sind, sind auf der Seite **Artikelnachverfolgungszeilen** alle Felder unter der Lagerkommissionierung schreibgeschützt, ausgenommen das **Feld Bewegungsmenge**. Die Lagerkommissionierzeilen legen die Artikelverfolgungsnummern der individuellen Zeilen für Lagerentnahme/Einlagerung fest. Die Menge wurde bereits in einzelne Serien- oder Chargennummer-Kombinationen aufgeteilt, da der Verkaufsauftrag die zu liefernden Artikelverfolgungsnummern enthalten hat.  

## <a name="item-tracking-availability"></a>Verfügbarkeit der Artikelverfolgung
Wenn Sie mit Chargen- oder Seriennummern arbeiten, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] die Verfügbarkeitsinformationen für Chargen- und Seriennummern und zeigt sie in den verschiedenen Artikelverfolgungsseiten an. Dadurch können Sie erkennen, welche Chargen- oder Seriennummer derzeit auf anderen Belegen verwendet wird. Dadurch werden Fehler und Unsicherheiten aufgrund von Doppelzuordnungen verringert.

Auf der Seite **Artikelverfolgungszeilen** wird in den Feldern **Verfügbarkeit, Chargennr.** oder **Verfügbarkeit, Seriennr.** ein Warnsymbol angezeigt, wenn die gesamte Menge oder Teile der Menge, die Sie ausgewählt haben, bereits auf anderen Belegen verwendet wurden oder wenn die Chargen- oder Seriennummer nicht verfügbar ist.

Auf der Seite **Chargennr./Seriennr.-Informationsliste**, auf der Seite **Chargennr./Seriennr. Verfügbarkeit** und auf der Seite **Artikelverfolgung – Posten auswählen** werden Informationen darüber angezeigt, welche Menge eines Artikels verwendet wird. Dies enthält die folgenden Informationen.

|Feld|Description|
|-----|-----------|  
|**Gesamtmenge**|Die Gesamtmenge des Artikels, die momentan im Lagerbestand vorhanden ist|
|**Total angeforderte Menge**|Die Gesamtanzahl der angeforderten Artikel, die auf diesem Beleg sowie auf anderen Belegen verwendet wird.|
|**Aktuell ausstehende Menge**|Die Anzahl der angeforderten Artikel, die auf dem aktuellen Beleg verwendet wird, aber noch nicht in die Datenbank übertragen wurde.|
|**Aktuell angeforderte Menge**|Die Anzahl der angeforderten Artikel, die auf dem aktuellen Beleg verwendet wird|
|**Total verfügbare Menge**|Die Gesamtanzahl des Artikels im Lagerbestand minus der Menge des Artikels, die zur Verwendung auf diesem sowie auf anderen Belegen angefordert ist (Total angeforderte Menge) und minus der Menge, die für diesen Beleg angefordert ist, aber noch nicht in die Datenbank übertragen wurde (Aktuell angeforderte Menge)|

Wenn Sie längere Zeit auf der Seite **Artikelverfolgungszeilen** arbeiten und wenn es viele Aktivitäten für den Artikel gibt, mit dem Sie arbeiten, können Sie die Verfügbarkeitsinformationen durch Klicken auf  Funktion,  **Verfügbarkeit aktualisieren** aktualisieren. Wenn Sie die Seite schließen, wird die Verfügbarkeit des Artikels automatisch neu überprüft, um zu bestätigen, dass es keine Verfügbarkeitsprobleme gibt.

## <a name="to-set-up-item-tracking-codes"></a>Um Artikelverfolgungscodes einzurichten
Ein Artikelverfolgungscode spiegelt die unterschiedlichen Betrachtungen wider, die ein Unternehmen bezüglich der Verwendung von Serien- und Chargennummern von Artikeln anstellt, die sich durch das Lager bewegen.  

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Nachverfolgungscodes** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Legen Sie auf dem Inforegister **Seriennr.** und **Chargennr.** die Vorgehensweisen zur Artikelverfolgung nach Serien- und Chargennummern fest.  

> [!NOTE]  
>  Wenn Sie bestimmte Artikel oder bestimmte Chargen während der Lebensdauer verfolgen möchten, müssen Sie die Felder **Seriennr.-spezifische Verf.** und **Chargennr.-spezifische Verf.** auswählen, fest. Wenn Sie eine ausgehende Einheit eines Artikels mit dem Artikelverfolgungscode verarbeiten, müssen Sie immer angeben, welche vorhandene Seriennummer oder welche vorhandene Chargennummer betroffen sein soll. Das bedeutet, dass der Artikel, von dem eine gewissen Menge verkauft wird, aus einem bestimmten Bereich von Seriennummern im Lagerbestand entnommen werden muss. Mit anderen Worten: die Seriennummer, die einem Artikel beim Wareneingang zugewiesen wurde, muss genau derjenigen beim Warenausgang entsprechen.

Da dieses Einrichtungsfeld alle möglichen Transaktionen für den Artikel abdeckt, werden die einzelnen Felder für Eingang und Ausgang ebenfalls mit Häkchen versehen. Die einzelnen Eingangs- und Ausgangsfelder haben aber nichts mit dem Ausgleich innerhalb des Lagers zu tun – sondern sie haben lediglich die Aufgabe, den Arbeitsablauf eines Unternehmens bezüglich der Zuweisung von Artikelverfolgungsnummern abzubilden.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Regeln für den Ablauf von Serien- oder Chargennummern einrichten:  
Für einige Artikel möchten Sie möglicherweise spezielle Ablaufdaten und Regeln in dem Artikelverfolgungscode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann bestimmte Serien- und Chargennummern ablaufen.

1. Wählen Sie einen bestehenden Artikelverfolgungscode aus bestehenden Artikelkarten aus, und wählen die Aktion **Bearbeiten**.  
2.  Aktivieren Sie im Inforegister **Sonst.** die folgenden Kontrollkästchen.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Fixes Ablaufdatum**|Gibt an, dass ein Ablaufdatum, das der Artikelverfolgungsnummer beim Wareneingang zugewiesen wurde, beim Warenausgang berücksichtigt werden muss.|  
    |**Ablaufdatum - Manuelle Eingabe**|Gibt an, dass Sie in der Artikelverfolgungszeile manuell ein Ablaufdatum eingeben müssen.|  
    |**Ablaufdaten ignorieren**|Gibt an, dass Sie keine Ablaufdaten berechnen möchten. |  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Garantien für Serien- oder Chargennummern einrichten:  
Für einige Artikel möchten Sie möglicherweise spezielle Garantievereinbarungen in dem Artikelverfolgungscode festlegen. Diese Funktionalität ermöglicht Ihnen nachzuvollziehen, wann die Garantien auf spezielle Serien- oder Chargennummern in Ihrem Lager auslaufen.        
1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Nachverfolgungscodes** ein und wählen Sie dann den entsprechenden Link.  

1. Wählen Sie einen bestehenden Artikelverfolgungscode aus bestehenden Artikelkarten aus, und wählen die Aktion **Bearbeiten**.  
2.  Füllen Sie im Inforegister **Sonstiges** das Feld **Garantiedatumsformel** aus, und markieren Sie das Kontrollkästchen wie folgt.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Garantiedatumsformel**|Gibt das letzte Garantiedatum für den Artikel an.|  
    |**Gar.-Datum - Manuelle Eingabe**|Zeigt an, dass Sie in der Artikelverfolgungszeile manuell ein Garantiedatum eingeben müssen.|  

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Serien- oder Chargennummern während einer eingehenden Transaktion zuzuordnen:  
Unternehmen möchten eventuell ihre Artikel von dem Moment an verfolgen, an dem diese das Unternehmen erreichen. In dieser Situation ist die Einkaufsbestellung oft der zentrale Beleg, obwohl die Artikelverfolgung von jedem beliebigen eingehenden Beleg aus gesteuert werden kann und die gebuchten Posten in den entsprechenden Artikelposten angezeigt werden können.  

Die genauen Regeln zur unternehmensweiten Verarbeitung von Artikelverfolgungsnummern werden durch die Einstellungen in der Tabelle **Artikelverfolgung** gesteuert.  

> [!NOTE]  
>  Um Artikelverfolgungsnummern in Lageraktivitäten zu verwenden, müssen die **Chargennr.-Verf. Lager**  und **Seriennr.-Verf. Lager** ausgewählt werden, da sie die speziellen Regeln der Handhabung von Serien- und Chargennummern in Lageraktivitäten definieren.  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Einkaufsbestellungen** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die gewünschte Belegzeile aus, und wählen Sie im Inforegister **Zeilen** die Option Aktionen , wählen Sie **Zeile** und dann **Artikelverfolgungszeilen**.  

    Zum Zuweisen von Serien- oder Chargennummern gibt es folgende Möglichkeiten:  

    -   Automatisch, indem Sie **Seriennr. zuweisen** oder **Chargennr. zuweisen** wählen, damit Serien-/Chargennummern aus vordefinierten Nummernserien zugeordnet werden.  
    -   Automatisch, indem Sie **Benutzerdef. Seriennr. erstellen** wählen, damit Serien-/Chargennummern auf der Basis von Nummernserien zugeordnet werden, die Sie speziell für die angekommenen Artikel festlegen.  
    -   Manuell, indem Sie Serien- oder Chargennummern direkt eingeben, z. B. die Nummern des Kreditors.  
    -   Manuell, indem Sie jeder Artikeleinheit eine bestimmte Nummer zuweisen.  

3. Um automatisch zuzuweisen, wählen Sie die **Benutzerdef. Seriennr. erstellen** Aktion.  
4. Im Feld **Benutzerdef. Seriennr.** geben Sie die Startnummer einer beschreibenden Seriennummernserie ein, z. B. **S/N-Kred0001**.  
5. Im Feld **Erhöhung** geben Sie "1" ein, um festzulegen, dass jede folgende Nummer um 1 höher sein soll als die vorige.  

    Das Feld **Menge zu erstellen** enthält standardmäßig die Menge aus der Zeile, Sie können diese Menge jedoch ändern.  

6. Wählen Sie das Feld **Neue Chargennr. erstellen**, um der neuen Seriennummern eine eigene Chargennummer zuzuteilen.  
7. Wählen Sie die Schaltfläche **OK** aus.  

Es wird eine Chargennummer mit einzelnen Seriennummern erstellt gemäß der Artikelmenge der Belegzeile, beginnend mit **S/N-Kred0001**.  

Die Matrix der Mengenfelder im Kopf des Fensters zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf der Seite einrichten. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine 0 in den Feldern **Undefiniert** angezeigt wird.  

Wenn der Beleg gebucht wird, werden die Artikelverfolgungsposten mit den entsprechenden Artikelposten verknüpft.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Serien- oder Chargennummern bei ausgehenden Vorgängen zuordnen  
Es gibt zwei Möglichkeiten, um ausgehenden Transaktionen Serien- und Chargennummern hinzuzufügen:  

-   Aus bestehenden Serien- oder Chargennummern auswählen. Dies trifft zu, wenn Artikelverfolgungsnummern bereits bei einem eingehenden Vorgang zugeordnet wurden. Weitere Informationen finden Sie unter [So wird's gemacht: Aus bestehenden Serien- und Chargennummern auswählen](inventory-how-work-item-tracking.md#to-select-from-existing-serial-or-lot-numbers)
-   Neue Serien- oder Chargennummern bei ausgehenden Vorgängen zuordnen. Dies trifft zu, wenn Artikelverfolgungsnummern Artikeln erst zugewiesen werden, wenn diese verkauft und lieferbereit sind.  

Die unterschiedlichen Regeln für Artikelverfolgungsnummern werden auf der Seiter **Artikelnachverfolgungscodekarte** eingerichtet.  

> [!NOTE]  
>  Um Artikelverfolgungsnummern bei Lageraktivitäten zuzuordnen, müssen die Kontrollkästchen **Seriennr.-Verf. Lager** und **Chargennr.-Verf. Lager** auf der Karte des Artikels ausgewählt werden.    

1. Wählen Sie die gewünschte Belegzeile aus, und wählen Sie im Inforegister **Zeilen** die Option Aktionen , wählen Sie **Auftrag** und dann **Artikelverfolgungszeilen**.  

    Sie können auf folgende Arten Artikelverfolgungsnummern zuordnen:  
    -   Automatisch aus vordefinierten Nummernserien: Klicken Sie auf der Registerkarte Aktionen in der Gruppe Funktionen auf **Seriennr. zuweisen** oder **Chargennr. zuweisen**.  
    -   Automatisch auf Basis von Parametern, die Sie speziell für den ausgehenden Artikel definieren: Klicken Sie auf der Registerkarte Aktionen in der Gruppe Funktionen auf Benutzerdef. **Seriennr. erstellen**.  
    -   Manuell, indem Sie Serien- oder Chargennummern ohne Verwendung von Nummernserien eingeben.  

2.  Für diesen Vorgang weisen Sie eine Seriennummer automatisch zu, indem Sie **Seriennr. zuweisen** auswählen.  

    Das Feld **Menge zu erstellen** enthält standardmäßig die Menge aus der Zeile, Sie können diese Menge jedoch ändern.  
3.  Wählen Sie das Feld **Neue Chargennr. erstellen**, um der neuen Seriennummern eine eigene Chargennummer zuzuteilen.  
4.  Wählen Sie die Schaltfläche **OK**, um eine Chargennummer und neue individuelle Seriennummern entsprechend der Menge in der Belegzeile zu erzeugen.  

Die Matrix der Mengenfelder im Kopf des Fensters zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf der Seite einrichten. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine **0** in den Feldern **Undefiniert** angezeigt wird.  

Wenn der Beleg gebucht wird, werden die Artikelverfolgungsposten mit den entsprechenden Artikelposten verknüpft.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Aus bestehenden Serien- oder Chargennummern auswählen  
Wenn Sie mit Artikeln arbeiten, für die Artikelverfolgung erforderlich ist, und ausgehende Transaktionen, bei denen die Artikel aus dem Lagerbestand abgehen, erstellen, müssen Sie üblicherweise die Chargen- oder Seriennummern von Artikeln verwenden, die es bereits im Lagerbestand gibt.  

 Die genauen Regeln zur unternehmensweiten Verarbeitung von Artikelverfolgungsnummern werden durch die Einstellungen in der Tabelle **Artikelverfolgung** gesteuert.  

> [!NOTE]  
>  Um Artikelverfolgungsnummern in Lageraktivitäten zu verwenden, muss der Artikel mit Seriennr./Chargenlagerverfolgung eingerichtet sein, da hiermit die speziellen Prinzipien der Behandlung von Serien- und Chargennummern im Lager gesteuert werden.

1.  Wählen Sie in einem beliebigen ausgehenden Beleg die Zeile aus, für die Sie Serien- oder Chargennummern auswählen möchten.  
2.  Wählen Sie im Inforegister **Zeilen** in **Aktionen** entweder **Zeilen** oder **Artikel** und dann wählen Sie **Artikelverfolgungszeilen**.  
3.  Auf der Seite **Artikelverfolgungszeilen** gibt es drei Möglichkeiten zum Angeben der Chargen- oder Seriennummer:  

    -   Wählen Sie in den Feldern **Chargennr.** oder **Seriennr.** auf und eine Nummer im Fenster **Artikelverf.-Zusammenfassung** aus.  
    -   Wählen Sie die Aktion **Posten** aus. Auf der Seite **Einträge auswählen** werden alle Chargen- oder Seriennummern sowie die Verfügbarkeitsinformationen angezeigt.

4. Geben Sie in das Feld **Ausgewählte Menge** für jede Chargen- oder Seriennummer die gewünschte Menge ein.   
5. Wählen Sie die Schaltfläche **OK** und die ausgewählten Artikelverfolgungsinformationen werden auf der Seite **Artikelverfolgungszeilen** übertragen.  
6. Geben oder lesen Sie die Artikelverfolgungsnummer ein.

Die Matrix der Mengenfelder im Kopf auf der Seite zeigt dynamisch die Mengen und die Summen der Artikelverfolgungsnummern an, die Sie auf der Seite einrichten. Die Mengen müssen denen in der Belegzeile entsprechen, was durch eine **0** in den Feldern **Undefiniert** angezeigt wird.  

 Wenn die Belegzeile gebucht wird, werden die Artikelverfolgungsinformationen auf die zugehörigen Artikelposten übertragen.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Um Serien-/Chargennummern in Umlagerungsaufträgen zu verarbeiten:  
Die Vorgehensweise zur Verarbeitung von Serien- und Chargennummern, die zwischen Lagerorten umgelagert werden, ist ähnlich der beim Einkauf und Verkauf von Artikeln.  

Der Umlagerungsauftrag ist allerdings insofern etwas Besonderes, als der Warenausgang und der Eingang von derselben Umlagerungszeile aus erfolgen und sie daher die gleiche Instanz der Seite **Artikelverfolgungszeilen** verwenden. Das bedeutetet, dass die Artikelverfolgungsnummern, die von dem einen Lagerort ausgeliefert werden, unverändert an dem anderen Ort ankommen müssen.  

 Die genauen Regeln zur unternehmensweiten Verarbeitung von Artikelverfolgungsnummern werden durch die Einstellungen in der Tabelle  **Artikelverfolgung** gesteuert.    
1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Transferaufträge** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie den Umlagerungsauftrag, die Sie bearbeiten möchten. Wählen Sie im Inforegister **Zeilen** in Aktionen entweder **Zeilen** oder **Artikel** und dann wählen Sie **Artikelverfolgungszeilen**.  
3.  Auf der Seite **Artikelverfolgungszeilen** weisen Sie eine Serien-/Chargennummer zu oder wählen eine aus, wie für jede andere ausgehende Artikeltransaktion.  

    Wenn Sie Serien-/Chargennummern für Umlagerungsartikel verarbeiten, sind diesen Artikeln normalerweise bereits Nummern zugeordnet. Daher besteht der Vorgang normalerweise darin, aus bestehenden Serien-/Chargennummern auszuwählen.  

4.  Buchen Sie den Umlagerungsauftrag (zuerst Warenausgang und dann Wareneingang), um festzuhalten, dass die Artikel mit ihren jeweiligen Artikelverfolgungsposten umgelagert werden.  

Während der Umlagerung bleibt die Seite **Artikelverfolgungszeilen** für Schreibvorgänge gesperrt.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>So verwenden Sie Serien- und Chargennummern beim Abrufen von Einkaufslieferzielen aus einer Einkaufsrechnung  
Wenn Sie Funktionen verwenden, um gebuchte Einkaufslieferzeilen oder Lieferzeilen aus den zugehörigen Rechnungen oder Gutschriften abzurufen, werden alle Artikelverfolgungszeilen in den Logistikbelegen automatisch übertragen, jedoch auf spezielle Art verarbeitet.

Die Funktionen unterstützen die folgenden eingehenden Prozesse:  
-   **Wareneingangszeilen holen** – von einer Einkaufsrechnung aus.  
-   **Rücklieferzeilen holen** – von einer Einkaufsgutschrift aus.  

Die Funktionen unterstützen die folgenden ausgehenden Prozesse:  
-   **Lieferzeilen holen** – von einer Verkaufsrechnung oder einem kombinierten Versand aus.  
-   **Rücksendungszeilen holen** – von einer Verkaufsgutschrift aus.  

In diesen Situationen werden die existierenden Artikelverfolgungszeilen automatisch in die Rechnung oder Gutschrift kopiert, die Seite **Artikelverfolgungszeilen** lässt allerdings keine Änderung der Serien- oder Chargennummer zu. Nur die Mengen können geändert werden.  

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie eine Einkaufsrechnung für Artikel, die mit Serien- oder Chargennummern eingekauft werden.  
3.  Wählen Sie in der Einkaufsrechnungszeile im Inforegister **Zeilen** die Option Funktion aus, und wählen Sie dann **Wareneingangszeilen holen** aus.  
4.  Wählen Sie auf der Seite **Wareneingangszeilen holen** eine Wareneingangszeile aus, die Artikelverfolgungszeilen hat, und klicken Sie anschließend auf **OK**.  

    Der Herkunftsbeleg wird in die Bestellrechnung als neue Zeile kopiert und dessen Artikelverfolgungszeilen werden in das darunter liegende Fenster **Artikelverfolgungszeilen** kopiert.  

5.  Wählen Sie in der Einkaufsrechnung die übertragene Wareneingangszeile aus.  
6.  Wählen Sie im Inforegister **Zeilen** **Zeile**, und dann **Artikelverfolgungszeile**, um die übertragenen Artikelverfolgungszeilen zu sehen.  

Die Inhalte der Felder **Seriennr.** und **Chargennr.** können nicht geändert werden. Sie können allerdings ganze Zeilen löschen oder die Mengen verändern, um Veränderungen in der Herkunftszeile auszugleichen.  

## <a name="to-record-serial-or-lot-number-information"></a>Serien- oder Chargennummerinformationen aufzeichnen  
Falls Sie spezielle Informationen mit einer bestimmten Artikelverfolgungsnummer verknüpfen müssen, z. B. für die Qualitätssicherung, können Sie dies in einer Serien- oder Chargennummer-Informationskarte vornehmen.

1. Öffnen eines Belegs, der die Serien- oder Chargennummern ist, die zugeordnet werden.
2. Öffnen Sie die Seite **Artikelverfolgungszeilen** für den Beleg.
3. Wählen Sie z. B. die **Seriennr.-Informationskarte** Aktion aus.  

    Die Felder **Seriennr.** und **Chargennr.** werden aus der Artikelverfolgungszeile vorab ausgefüllt.  
4. Geben Sie im Feld **Beschreibung** eine kurze Beschreibung ein, zum Beispiel über den Zustand des Artikels.  
5. Wählen Sie  **Bemerkung**, um einen separaten Bemerkungsdatensatz zu erstellen.  
6. Aktivieren Sie das Kontrollkästchen **Gesperrt**, um die Serien- oder Chargennummer von sämtlichen Transaktionen auszuschließen.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Sie können Serien- oder Losinformationskarten später ändern.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Bestehende Serien- oder Chargennummerinformationen ändern  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie einen Artikel, der einen Artikelverfolgungscode hat und Serien- oder Chargennummerinformationen hat.
3. Auf der Seite **Artikelkarte** wählen Sie die **Posten** Aktion aus, und wählen Sie dann **Posten** aus.
4. Wählen Sie das Feld **Chargennr.** oder **Seriennr.** aus. Wenn es für die Artikelverfolgungsnummer Informationen gibt, dann wird die Seite **Chargennr.-Informationsliste** oder **Seriennr.-Informationsliste** geöffnet.  
5. Wählen Sie eine Karte aus, und wählen Sie die **Chargennr./Seriennummer Informationskarte** Aktion aus.  
6. Ändern Sie den Kurzbeschreibungstext, den Bemerkungsdatensatz oder das Feld **Gesperrt**.  

Sie können die Serien- oder Chargennummern und auch die Mengen nicht ändern. Um dies zu tun, müssen Sie den betreffenden Artikelposten umbuchen. Weitere Informationen hierzu finden Sie unter [Chargen- oder Seriennummern umbuchen](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Um Chargen- oder Seriennummern zu ändern  
Ein Umbuchen der Artikelverfolgung für einen Artikel bedeutet, dass eine Chargen- oder Seriennummer in eine neue Chargen- oder Seriennummer oder das Ablaufdatum in ein neues Ablaufdatum geändert wird. Wenn Sie mit Chargen arbeiten, können Sie außerdem mehrere Chargen zu einer Charge vereinigen. Das Ausführen dieser Aufgaben erfolgt mit dem Artikel-Umlagerungs-Buch.-Blatt.

1.  Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), und geben Sie **Umlagerung Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie die Zeile mit den relevanten Informationen aus. Weitere Informationen finden Sie unter [Lagerbestand anhand der Belege erfassen](inventory-how-count-inventory-with-documents.md) oder [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md).
3.  Wählen Sie die **Artikelverfolgungszeilen** Aktion aus.  
4.  Wählen Sie im Feld **Seriennr.** oder **Chargennr.** die aktuelle Serien- oder Chargennummer aus.  
5.  Wenn Sie eine Einen neuen Artikelverfolgungsnummer eingeben möchten, geben Sie diese in das Feld **Neue Seriennr.** oder **Neue Chargennr.** ein. Bei Bedarf können Sie ein oder mehrere Chargen in einer oder mehreren neuen Chargen zusammenführen.  

    > [!NOTE]  
    >  Beachten Sie beim Umbuchen von Ablaufdatumsangaben, dass die Artikel mit den frühesten Ablaufdatumsangaben für ausgehende Transaktionen zuerst vorgeschlagen werden. Weitere Informationen finden Sie unter[ Korrigieren der FEFO..](warehouse-picking-by-fefo.md)  

5.  Wenn Sie ein neues Ablaufdatum für eine Serien- oder Chargennummer eingeben möchten, geben Sie dieses in das Feld **Neues Ablaufdatum** ein.  

    > [!IMPORTANT]  
    >  Wenn Sie eine Charge auf die gleiche Chargennummer, aber mit einem anderen Ablaufdatum umbuchen möchten, müssen Sie die gesamte Charge in einer Zeile des Artikel Umlagerungs Buch.-Blatts umbuchen. Wenn Sie mehrere Chargennummern zu einer neuen Chargennummer zusammenführen möchten (also mehrere Chargen zu einer neuen Charge zusammengeführt werden), müssen Sie für alle Chargen das gleiche Ablaufdatum eingeben. Wenn Sie eine vorhandene Charge in eine andere vorhandene Charge umbuchen, die ein anderes Ablaufdatum besitzt, müssen Sie das Ablaufdatum der zweiten Charge verwenden. Wenn Sie das Feld **Neues Ablaufdatum** leer lassen, wird die Chargen- oder Seriennummer ohne Ablaufdatum umgebucht.  

6.  Wenn Sie Informationen zu der alten Serien- oder Chargennummer haben, können Sie diese Informationen für die neue Serien- oder Chargennummer kopieren.  

    1.  Klicken Sie auf der Seite  **Artikelverfolgungszeilen** auf **Neue Seriennummerinformation** oder **Neuze Chargennummerninformation**  
    2.  Wenn Sie Informationen aus der alten Chargen- oder Seriennummer kopieren möchten, klicken Sie auf **Info kopieren**.  
    3.  Wählen Sie auf der Seite "Informationsliste" die Chargen- oder Seriennummer aus, von der Sie kopieren möchten, und wählen Sie **OK**.  

7.  Wenn Sie die vorhandenen Informationen für eine Chargen- oder Seriennummer ändern möchten, können Sie die Chargen- oder Serieninformationen aufzeichnen.  
8.  Buchen Sie das Buch.-Blatt, um die neuen Artikelverfolgungsnummern oder Ablaufdatumsangaben mit den entsprechenden Artikelposten zu verknüpfen.

## <a name="see-also"></a>Siehe auch
[Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)   
[Lagerbestand](inventory-manage-inventory.md)  
[Unter Designdetails: Artikelverfolgung](design-details-item-tracking.md)
[Unter Designdetails - Artikelverfolgung und Reservierungen](design-details-item-tracking-and-reservations.md)  
[Artikel reservieren](inventory-how-to-reserve-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]