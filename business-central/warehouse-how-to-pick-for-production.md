---
title: Kommissionieren Produktion oder Montage im Basislager
description: Wenn Ihr Lagerort eine Verarbeitung der Kommissionierung, aber keine Versandverarbeitung erfordert, verwenden Sie die Seite Lagerkommissionierungen, um die Kommissionierung der Komponenten zu organisieren und zu erfassen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: c3827bb8ab272b38972c17d79933ce0aa187e32d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445797"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Kommissionierung für Montage oder Produktion in Grund-Lagerkonfiguration
Wie Sie Ihre Kommissionierungskomponenten für Produktions- oder Montageaufträge einlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).


## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Für die Produktion in einer Basis-Lagerkonfiguration kommissionieren
Die Buchungsmethode beeinflusst auch den Fluss der Komponenten in der Produktion. Weitere Informationen finden Sie unter [Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md).

In erweiterten Lagerkonfigurationen, in denen Standorte sowohl Kommissionierungen als auch Sendungen erfordern, müssen Sie die Seite **Lagerauswahl** verwenden, um Komponenten mit der Buchungsmethode, die auf *Manuell*, *Kommiss. + Vorwärts*, *Kommiss. + Rückwärts* zu Fertigungsaufträgen zu bringen. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

Bei Basis-Lagerkonfigurationen, bei denen für den Lagerort die Bearbeitung der Kommissionierung erforderlich ist, jedoch nicht die Bearbeitung des Warenausgangs, können Sie die Seite **Lagerkommissionierung** verwenden, um die Kommissionierung von Komponente mit der Buchungsmethode auf *Manuell* zu organisieren und zu erfassen. Wenn Sie eine Lagerkommissionierung für einen internen Vorgang erfassen, wie etwa Produktion, wird der Verbrauch der kommissionierten Komponenten gleichzeitig gebucht. Alternativ können Sie **Lagerbestandsumlagerung** mit Bezug auf ein Quelldokument verwenden, um Komponenten mit Buchungsmethode auf *Manuell*, *Kommiss. + Vorwärts*, *Kommiss. + Rückwärts* zu Fertigungsaufträgen zu bringen.

Wenn Produktionsschritte in Lagerprozesse integriert werden, entweder durch Lagerplätze oder durch gesteuerte Einlagerungen und Kommissionierungen, ist der Lagerort, von dem die Komponenten verbraucht werden, der Lagerort, der in jeder Fertigungsauftragskomponentenzeile definiert wird. Alle benötigten Komponenten müssen an diesem Lagerort verfügbar sein. Andernfalls wird die manuelle oder die geleerte Verbrauchsbuchung für diese Komponente angehalten.

**Lagerbestandsumlagerung** mit Verweisen auf das Quelldokument und **Kommissionierung** können nicht zum Kommissionieren von Komponenten mit Buchungsmethode *Vorwärts* und *Rückwärts* verwendet werden. **Lagerkommissionierung** kann aber nicht zum Kommissionieren von Komponenten mit einer Buchungsmethode außer *Manuell* verwendet werden. Verwenden Sie zum Behandeln der verbleibenden Komponenten **Lagerbestandsumlagerung** ohne Verweis auf ein Quelldokument. Weitere Informationen finden Sie in [Umlagern von Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

> [!NOTE]  
>  Bestandskommissionierungen, Lagerbestandsumlagerungen und Lagerkommissionierungen weisen folgende wichtige Unterschiede auf:  
>   
>  -   Wenn Sie eine Lagerkommissionierung für einen internen Vorgang erfassen, wie etwa Produktion, wird der Verbrauch der kommissionierten Komponenten gleichzeitig gebucht. Wenn Sie eine Lagerbestandsumlagerung oder eine Kommissionierung für einen internen Vorgang registrieren, erfassen Sie nur die physische Umlagerung der benötigten Komponenten an einen Lagerplatz im Arbeitsgangbereich, ohne den Verbrauch zu buchen.  
> -   Wenn Sie Lagerkommissionierungen verwenden, definiert das Feld **Lagerplatzcode** in der Komponentenzeile eines Fertigungsauftrags den *Entnahme*-Lagerplatz, in dem die Anzahl der Komponenten bei Buchung des Verbrauchs verringert wird. Wenn Sie Lagerbestandsumlagerungen oder eine Kommissionierung verwenden, definiert das Feld **Lagerplatzcode** in FA-Komponentenzeilen den *Einlagerungs*-Lagerplatz im Vorgangsbereich, in dem der Lagermitarbeiter die Komponenten platzieren muss.  

Eine Systemvoraussetzung für das Kommissionieren oder Umlagern von Komponenten für Herkunftsbelege ist, dass eine ausgehende erwartete Lagerbewegung vorhanden ist, um den Lagerbereich über den Komponentenbedarf zu benachrichtigen. Die ausgehende erwartete Lagerbewegung wird erzeugt, wenn der Status des Fertigungsauftrags zu Freigegeben geändert wird oder wenn der freigegebene Fertigungsauftrag angelegt wird.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Kommissionieren von Produktionskomponenten in grundlegenden Lagerkonfigurationen mithilfe der Bestandsauswahl
In Basis--Lagerkonfigurationen, in der der Lagerort nur für Kommissionierung eingerichtet wurde, können Sie Komponenten für Produktions- und Montageaktivitäten auf der Seite **Lagerkommissionierung** kommissionieren. Weitere Informationen finden Sie unter [Entnahme von Artikeln mit Kommissionierungen](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den zugehörigen Link.  
2.  Um zu den Komponenten des Fertigungsauftrags zu gelangen, wählen Sie die Aktion **Herkunftsbeleg holen** aus, und wählen Sie den freigegebenen Fertigungsauftrag aus.  
3.  Führen Sie die Kommissionierung aus und erfassen Sie dann die tatsächlichen Kommissionierinformationen im Feld **Bewegungsmenge**.  
4.  Wenn die Zeilen zum Buchen bereit sind, wählen Sie die Aktion **Buchen** aus. Das Buchen erzeugt die erforderlichen Lagerplatzposten und bucht den Verbrauch der Artikel.  

Sie können eine **Lagerkommissionierung** auch direkt aus dem freigegebenen Fertigungsauftrag erstellen. Wählen Sie die Aktion **Bestandseinlagerung/Kommissionierung/Umlagerung erstellen** aus, wählen Sie das Kontrollkästchen **Lagerkomm. erst.**, und wählen Sie dann die Schaltfläche **OK** aus.

Alternativ können Sie die **Lagerbestandsumlagerung** mit Bezug auf das Quelldokument verwenden, um Elemente zwischen Lagerplätzen zu verschieben. Sie müssen den Verbrauch separat registrieren. Weitere Informationen finden Sie unter [Produktionsverbrauch mit Stapelverarbeitung buchen](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Für die Montage in einer Basis-Lagerkonfiguration kommissionieren
In erweiterten Lagerkonfigurationen, bei denen für Lagerplätze sowohl Kommissionierungen als auch Lieferungen benötigt werden, müssen Sie die Seite **Kommissionierungen** verwenden, um Komponenten in Montageaufträge einzubringen. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

In Basislagerkonfigurationen können Sie für Montageaufträge auch mit der Seite **Lagerbestandsumlagerung** kommissionieren. 

In grundlegenden Lagerkonfigurationen, in denen der Standort eine Kommissionierabwicklung erfordert, jedoch keine Versandabwicklung, wird die Seite **Lagerkommissionierung** auch zum Kommissionieren, Montieren und Versenden für Kundenaufträge verwendet, bei denen Artikel montiert werden müssen, bevor sie versendet werden können. Weitere Informationen finden Sie unter [Verwenden von Auftragsmontageartikeln mit Lagerkommissionierungen](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Verarbeiten von Auftragsmontageartikel mit Lagerkommissionierungen
Die Seite **Lagerkommissionierung** wird auch verwendet, um für Verkäufe zu kommissionieren und zu liefern, in denen Artikel montiert werden müssen, bevor sie geliefert werden können. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).

Die zu liefernden Artikel sind an einem Lagerplatz erst dann tatsächlich vorhanden, wenn sie zusammengestellt und als Ausstoß für einen Lagerplatz im Montagebereich gebucht wurden. Das bedeutet, dass das Kommissionieren von Auftragsmontageartikeln zur Lieferung einem speziellen Ablauf folgt. Von einem Lagerplatz bringen Lagermitarbeiter die Montageartikel zur Versandstelle und buchen dann die Lagerkommissionierung. Die gebuchte Lagerkommissionierung bucht dann den Montageausstoß, den Komponentenverbrauch und die Verkaufslieferung.

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um eine automatische Lagerbestandsumlagerung zu erstellen, wenn die Lagerkommissionierung für die Montageartikel erstellt wird. Um dies zu aktivieren, müssen Sie das Feld **Umlagerungen automatisch erstellen** auf der Seite **Montageeinrichtung** auswählen. Weitere Informationen finden Sie in [Umlagern von Komponenten in einen Arbeitsgangbereich in den grundlegenden Lagerfunktionen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerkommissionierzeilen für Verkaufsartikel werden je nachdem, ob keine, einige oder alle Verkaufspositionsmengen auf Bestellung gefertigt werden, auf unterschiedliche Weise erstellt.

Bei regulären Verkäufen, wo Sie Lagerkommissionierungen verwenden, um Liefer- und Lagermengen zu buchen, wird eine Verkaufsauftragszeile, oder mehre, wenn der Artikel in verschiedenen Lagerplätzen platziert ist, erstellt für jede Verkaufszeile. Diese Kommissionierzeile basiert auf der Menge im Feld **Zu liefern**.

In Auftragsmontageverkäufen, bei denen die gesamte Menge aus der Verkaufsauftragszeile montiert wird, wird eine Lagerkommissionierzeile für diese Menge erstellt. Das bedeutet, dass der Wert im Feld "Menge für Montage" dem Wert im Feld **Zu liefern** entspricht. Das Feld **Auftragsmontage** wird in der Zeile ausgewählt.

Wenn ein Montageausgabefluss für den Lagerort eingerichtet wird, wird der Wert im Feld **LP-Code f. Prog.fert.lief.** oder der Wert im Feld **Montage-Ausgangslagerplatzcode** in dieser Reihenfolge in das Feld **Lagerplatzcode** in der Lagerkommissionierzeile eingefügt.

Wenn kein Lagerplatzcode in der Verkaufsauftragszeile angegeben wird und kein Montageausgabefluss für den Lagerort eingerichtet wird, bleibt das Feld **Lagerplatzcode** in der Lagerkommissionierzeile leer. Der Lagermitarbeiter muss die Seite **Lagerplatzinhalte** öffnen und den Lagerort auswählen, in dem die Montageartikel montiert werden.

In Kombinationsszenarien in denen ein Teil der Menge zunächst montiert werden muss und andere aus dem Lager kommissioniert werden müssen, werden mindestens zwei Lagerkommissionierzeilen erstellt. Eine Kommissionierzeile ist für die Programmfertigungsmenge. Die andere Kommissionierzeile hängt davon ab, welche Lagerplätze die Restmenge aus dem Lagerbestand erfüllen können. Lagerplatzcodes in den beiden Zeilen werden auf verschiedene Weise ausgefüllt, wie für die beiden verschiedenen Verkaufsarten beschrieben. Weitere Informationen finden Sie im Abschnitt "Kombinationsszenarien" in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Auffüllen des Verbrauchslagerplatzes
Dieses Flussdiagramm zeigt, wie das Feld **Lagerplatzcode** in Fertigungsauftrags-Komponentenzeilen entsprechend Ihrer Lagerplatzeinrichtung ausgefüllt wird.

![Flowdiagramm Lagerplatz.](media/binflow.png "BinFlow")

## <a name="see-also"></a>Weitere Informationen
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
