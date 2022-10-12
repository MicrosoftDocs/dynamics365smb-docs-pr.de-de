---
title: Kommissionierung für Produktion, Montage oder Projekte in Grund-Lagerkonfiguration
description: Wenn Ihr Lagerort eine Verarbeitung der Kommissionierung, aber keine Versandverarbeitung erfordert, verwenden Sie die Seite Lagerkommissionierungen, um die Kommissionierung der Komponenten zu erfassen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617876"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Kommissionierung für Produktion, Montage oder Projekte in Grund-Lagerkonfigurationen

Wie Sie Ihre Kommissionierungskomponenten für Produktions- oder Montageaufträge einlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Für die Produktion in einer Basis-Lagerkonfiguration kommissionieren

Wenn ein Lagerort Kommissionierungsverarbeitung, aber keine Versandverarbeitung erfordert, können Sie die Seite **Lagerkommissionierung** verwenden. Auf der Seite **Lagerkommissionierung** können Sie die Kommissionierung von Artikeln organisieren und aufzeichnen, deren Buchungsmethode auf **Manuell** eingestellt ist. Wenn Sie eine Lagerkommissionierung erfassen, wird der Verbrauch der kommissionierten Komponenten gebucht. Alternativ können Sie **Lagerbestandsumlagerung** mit Bezug auf ein Quelldokument verwenden, um Komponenten mit Buchungsmethode auf **Manuell**, **Kommiss. + Vorwärts**, **Kommiss. + Rückwärts** Fertigungsaufträgen zuzuweisen.

Wenn Produktionsschritte in Lagerprozesse integriert werden durch Lagerplätze oder durch gesteuerte Einlagerungen und Kommissionierungen, werden Komponenten von dem Lagerort verbraucht, der in jeder Fertigungsauftragskomponentenzeile definiert wird. Alle benötigten Komponenten müssen an diesem Lagerort verfügbar sein. Andernfalls wird die manuelle oder die geleerte Verbrauchsbuchung für diese Komponente angehalten.

> [!NOTE]  
> Bestandskommissionierungen, Lagerbestandsumlagerungen und Lagerkommissionierungen weisen folgende wichtige Unterschiede auf:  
>
> - Wenn Sie eine Lagerkommissionierung für einen internen Vorgang erfassen, wie etwa Produktion, wird der Verbrauch der kommissionierten Komponenten gleichzeitig gebucht. Wenn Sie eine Lagerbestandsumlagerung oder eine Kommissionierung für einen internen Vorgang registrieren, erfassen Sie nur die physische Umlagerung der benötigten Komponenten an einen Lagerplatz im Arbeitsgangbereich, ohne den Verbrauch zu buchen.  
> - Wenn Sie Lagerkommissionierungen verwenden, definiert das Feld **Lagerplatzcode** in der Komponentenzeile eines Fertigungsauftrags den *Entnahme*-Lagerplatz, in dem die Anzahl der Komponenten bei Buchung des Verbrauchs verringert wird. Wenn Sie Lagerbestandsumlagerungen oder eine Kommissionierung verwenden, definiert das Feld **Lagerplatzcode** in FA-Komponentenzeilen den *Einlagerungs*-Lagerplatz im Vorgangsbereich, in dem der Lagermitarbeiter die Komponenten platzieren muss.  

Zum Kommissionieren oder Umlagern von Komponenten für Herkunftsbelege muss eine ausgehende Lagerbewegung vden Lagerbereich über den Komponentenbedarf benachrichtigen. Die ausgehende Lageranforderung wird erstellt, wenn Sie Folgendes tun:

- Ändern des Status eines Fertigungsauftrags auf Freigegeben.
- Dient zum Erstellen eines freigegebenen Produktionsauftrags.  

Die Buchungsmethoden beeinflussen auch den Fluss der Komponenten in der Produktion. Weitere Informationen finden Sie unter [Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren](production-how-to-flush-components-according-to-operation-output.md). **Lagerbestandsumlagerung** mit Verweisen auf das Quelldokument und **Kommissionierung** können nicht zum Kommissionieren von Komponenten mit Buchungsmethoden *Vorwärts* und *Rückwärts* verwendet werden. **Lagerkommissionierung** kann aber nicht zum Kommissionieren von Komponenten mit einer Buchungsmethode außer *Manuell* verwendet werden. Verwenden Sie zum Behandeln der verbleibenden Komponenten **Lagerbestandsumlagerung** ohne Verweis auf ein Quelldokument. Weitere Informationen finden Sie in [Umlagern von Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

In erweiterten Lagerkonfigurationen, in denen Standorte sowohl Kommissionierungen als auch Sendungen erfordern, müssen Sie die Seite **Lagerauswahl** verwenden, um Komponenten mit der Buchungsmethode, die auf *Manuell*, *Kommiss. + Vorwärts*, *Kommiss. + Rückwärts* zu Fertigungsaufträgen zu bringen. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Kommissionieren von Komponenten zur Produktion oder für Projekte in Basis-Lagerkonfigurationen

In Basis--Lagerkonfigurationen, in der der Lagerort nur für Kommissionierung eingerichtet wurde, können Sie Komponenten für Produktions- und Projektplanungsaktivitäten auf der Seite **Lagerkommissionierung** kommissionieren. Weitere Informationen finden Sie unter [Entnahme von Artikeln mit Kommissionierungen](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Die Möglichkeit, Komponenten für Auftragsplanungslinien auszuwählen, wurde hinzugefügt[!INCLUDE[d365fin](includes/d365fin_md.md)] 2022 Veröffentlichungswelle 2. Um die Funktion zu verwenden, muss Ihr Administrator **Funktion Aktualisieren: Lagerbestand und Lagerkommissionierungen von Aufträgen aus aktivieren** auf der Seite **Funktionsverwaltung** aktivieren.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] verwendet den Wert im Feld **Verbleibende Menge** in der Auftragsplanungszeile, wenn es Bestandsentnahmen erstellt. Um Bestandsentnahmen für Aufträge zu verwenden, müssen Sie den Schalter **Nutzungslink anwenden** auf der Seite **Projektkarte** Seite für das Projekt umschalten. Auf diese Weise können Sie die Nutzung anhand Ihres Plans verfolgen. Wenn Sie den Schalter nicht einschalten, bleibt die Restmenge bei **0** und die Bestandsauswahl wird nicht erstellt. Weitere Informationen finden Sie unter [Projektverbrauch-Nachverfolgung einrichten](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking)

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Lagerkommissionierungen** ein und wählen Sie dann den zugehörigen Link.  
2. Um zu den Komponenten des Fertigungsauftrags zu gelangen, wählen Sie die Aktion **Herkunftsbeleg holen** aus, und wählen Sie den freigegebenen Fertigungsauftrag aus.  
3. Führen Sie die Kommissionierung der Komponente aus und erfassen Sie dann die tatsächlichen Kommissionierinformationen im Feld **Bewegungsmenge**.  
4. Wenn die Zeilen zum Buchen bereit sind, wählen Sie die Aktion **Buchen** aus. Das Buchen erzeugt die erforderlichen Lagerplatzposten und bucht den Verbrauch der Artikel.  

Sie können eine **Lagerkommissionierung** auch direkt aus dem freigegebenen Fertigungsauftrag erstellen. Wählen Sie die Aktion **Bestandseinlagerung/Kommissionierung/Umlagerung erstellen** aus, wählen Sie das Kontrollkästchen **Lagerkomm. erst.**, und wählen Sie dann die Schaltfläche **OK** aus.

Alternativ können Sie die **Lagerbestandsumlagerung** mit Bezug auf das Quelldokument verwenden, um Elemente zwischen Lagerplätzen zu verschieben. Sie müssen den Verbrauch separat registrieren. Weitere Informationen finden Sie unter [Produktionsverbrauch mit Stapelverarbeitung buchen](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Für die Montage in einer Basis-Lagerkonfiguration kommissionieren

Verwenden Sie die folgenden Seiten, um für Montageaufträge zu kommissionieren:

- Die Seite **Lagerbestandsumlagerung**.
- Wenn Ihr Lagerort Kommissionierungen, aber keine Lieferungen erfordert, verwenden Sie die Seite **Lagerkommissionierung**, um für Verkäufe zu kommissionieren, zu montieren und zu liefern, in denen Artikel montiert werden müssen, bevor sie geliefert werden können. Weitere Informationen finden Sie unter [Verwenden von Auftragsmontageartikeln mit Lagerkommissionierungen](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

In erweiterten Lagerkonfigurationen, bei denen für Lagerplätze sowohl Kommissionierungen als auch Lieferungen benötigt werden, müssen Sie die Seite **Kommissionierungen** verwenden, um Komponenten in Montageaufträge einzubringen. Weitere Informationen unter [Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Verarbeiten von Auftragsmontageartikel mit Lagerkommissionierungen

Die Seite **Lagerkommissionierung** wird auch verwendet, um für Verkäufe zu kommissionieren und zu liefern, in denen Artikel montiert werden müssen, bevor sie geliefert werden können. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).

Die zu liefernden Artikel in Programmfertigung sind an einem Lagerplatz erst dann tatsächlich vorhanden, wenn sie zusammengestellt und als Ausgabe für einen Lagerplatz im Montagebereich gebucht wurden. Daher folgt die Kommissionierung dieser Artikel für den Versand einem speziellen Ablauf. Von einem Lagerplatz bringen Lagermitarbeiter die Montageartikel zur Versandstelle und buchen dann die Lagerkommissionierung. Die gebuchte Lagerkommissionierung bucht dann den Montageausstoß, den Komponentenverbrauch und die Verkaufslieferung.

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um eine automatische Lagerbestandsumlagerung zu erstellen, wenn die Lagerkommissionierung für die Montageartikel erstellt wird. Um die Bewegungen automatisch zu erstellen, müssen Sie das Feld **Umlagerungen automatisch erstellen** auf der Seite **Montageeinrichtung** auswählen. Weitere Informationen finden Sie in [Umlagern von Komponenten in einen Arbeitsgangbereich in den grundlegenden Lagerfunktionen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

[!INCLUDE[prod_short](includes/prod_short.md)] erstellt Lagerkommissionierzeilen für Verkaufsartikel werden je nachdem, ob keine, einige oder alle Verkaufspositionsmengen auf Bestellung gefertigt werden, auf unterschiedliche Weise erstellt.

- Im Verkauf, wo Sie Bestandsentnahmen verwenden, um Bestandslieferungen zu buchen, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] eine Bestandskommissionierposition für jede Verkaufsauftragsposition. Wenn der Artikel in verschiedene Behälter gelegt wird, wird mehr als eine Zeile erstellt. Diese Kommissionierzeilen basieren auf der Menge im Feld **Zu liefern**.
- In Verkäufen, bei denen die gesamte Menge aus der Verkaufsauftragszeile montiert wird, wird eine Lagerkommissionierzeile für diese Menge erstellt. Der Wert im Feld "Menge für Montage" entspricht dem Wert im Feld **Zu liefern**. Das Feld **Auftragsmontage** wird in der Zeile ausgewählt.

Wenn ein Montageausgabefluss für den Lagerort eingerichtet wird, wird der Wert im Feld **LP-Code f. Prog.fert.lief.** oder im Feld **Montage-Ausgangslagerplatzcode** in dieser Reihenfolge in das Feld **Lagerplatzcode** in der Lagerkommissionierzeile eingefügt.

Wenn kein Lagerplatzcode in der Verkaufsauftragszeile angegeben wird und kein Montageausgabefluss für den Lagerort eingerichtet wird, bleibt das Feld **Lagerplatzcode** in der Lagerkommissionierzeile leer. Der Lagermitarbeiter muss die Seite **Lagerplatzinhalte** öffnen und den Lagerort auswählen, in dem die Montageartikel montiert werden.

Wenn ein Teil der Menge zunächst montiert werden muss und andere aus dem Lager kommissioniert werden müssen, werden von [!INCLUDE[prod_short](includes/prod_short.md)] mindestens zwei Lagerkommissionierzeilen erstellt. Eine Kommissionierzeile ist für die Programmfertigungsmenge. Die andere Kommissionierzeile hängt davon ab, welche Lagerplätze die Restmenge aus dem Lagerbestand erfüllen können. Lagerplatzcodes in den beiden Zeilen werden auf verschiedene Weise ausgefüllt, wie für die beiden verschiedenen Verkaufsarten beschrieben. Weitere Informationen finden Sie im Abschnitt "Kombinationsszenarien" in [Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Auffüllen des Verbrauchslagerplatzes

Dieses Flow-Diagramm zeigt, wie das Feld **Lagerplatzcode** auf den Zeilen der Produktionsauftragskomponenten entsprechend der Einrichtung Ihres Standorts gefüllt wird.

![Flowdiagramm Lagerplatz.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
