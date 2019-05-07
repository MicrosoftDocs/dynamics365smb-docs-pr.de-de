---
title: 'Vorgehensweise: Einrichten von Basislagern mit Vorgangsbereichen | Microsoft Docs'
description: Wenn in den Basislagerkonfigurationen interne Vorgangsbereiche wie Produktion oder Montage vorhanden sind, in denen Lagerplätze das Einrichtungsfeld **Lagerplatz notwendig** und möglicherweise die Einrichtungsfelder **Kommissionierung erforderlich** und **Einlagerung erforderlich** verwenden, können Sie drei Basislagerbelege verwenden, um Ihre Lageraktivitäten für interne Vorgangsbereiche zu erfassen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 02c9152719a362254aa719a5ee803f3181aa463f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "912194"
---
# <a name="set-up-basic-warehouses-with-operations-areas"></a>Einrichten von Basislagern mit Vorgangsbereichen
Wenn in den Basislagerkonfigurationen interne Vorgangsbereiche wie Produktion oder Montage vorhanden sind, in denen Lagerplätze das Einrichtungsfeld **Lagerplatz notwendig** und möglicherweise die Einrichtungsfelder **Kommissionierung erforderlich** und **Einlagerung erforderlich** verwenden, können Sie die folgenden Basislagerbelege verwenden, um Ihre Lageraktivitäten für interne Vorgangsbereiche zu erfassen:  

- Seite **Lagerbestandsumlagerung**  
- Seite **Lagerkommissionierung**  
- Seite **Lagereinlagerung**

> [!NOTE]
> Obwohl die Einstellungen **Kommissionierung erforderlich** und **Einlagerung erforderlich** genannt werden, können Sie weiterhin Wareneingänge und Lieferungen direkt aus den Quellgeschäftsunterlagen an Lagerorten, in denen Sie diese Kontrollkästchen aktivieren.  

Um diese Seiten mit internen Vorgängen zu verwenden, wie Komponenten zu kommissionieren und in die Produktion zu verschieben, sind, abhängig davon, wie viel Kontrolle Sie benötigen, alle oder einige der folgenden Einrichtungsschritte erforderlich:  

- Aktivieren Sie die Kommissionierungs-, Umlagerungs- und Einlagerungsbelege.  
- Definieren Sie Standardlagerplatzstrukturen für Komponenten und die Endartikel, die zu Arbeitsgangressourcen laufen und von diesen abgehen.  
- Erstellen Sie Lagerorte für den Zugang und den Abgang, die für spezielle Arbeitsgangressourcen dediziert sind, um zu verhindern, das Artikel für ausgehende Belege kommissioniert werden.

Lagerfachcodes, die auf Lagerortkarten eingerichtet werden, definieren einen Standardlagerfluss für bestimmte Aktivitäten wie z. B. Komponenten in einer Montageabteilung. Mithilfe zusätzlicher Funktionen wird sichergestellt, dass Artikel, die in einem bestimmten Lagerfach platziert werden, nicht umgelagert oder für sonstige Aktivitäten entnommen werden können. Weitere Informationen finden Sie unter [So erstellen Sie festgelegte Komponentenlagerplätze](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Die folgenden Verfahren basieren auf dem Einrichten von grundlegenden Lageraktivitäten um eine Fertigungsstätte. Die Schritte sind für andere Arbeitsgangsbereiche, wie Montage, Servicemanagement und Projekte ähnlich.  

> [!NOTE]  
>  Im folgenden Verfahren wird das Einrichtungsfeld **Lagerplatz notwendig** auf Lagerortkarten als Voraussetzung aktiviert, da dies als Grundlage für alle Logistikstufen gilt.  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a>Um den Inventurprozess für Aktivitäten des internen Arbeitsgangs ausführen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Lagerortkarte, die Sie einrichten möchten.  
3.  Aktivieren Sie im Inforegister **Lager** das Kontrollkästchen **Einlagerung erforderlich**, um anzugeben, dass ein Lagereinlagerungs- oder ein Lagerbestandsumlagerungsbeleg erstellt werden kann, wenn ein eingehender oder ein interner Herkunftsbeleg mit einem Lagerplatzcode freigegeben wird.  
4.  Aktivieren Sie das Kontrollkästchen **Kommissionierung erforderlich**, um anzugeben, dass ein Lagerkommissionierbeleg oder ein Lagerbestandsumlagerungsbeleg erstellt werden muss, wenn ein ausgehender oder ein interner Herkunftsbeleg mit einem Lagerplatzcode erstellt wird.  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a>Um eine Standardlagerplatzstruktur im Fertigungsbereich zu definieren  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Lagerort, die Sie einrichten möchten.  
3.  Geben Sie im Inforegister **Lagerplätze** im Feld **Off. Fert.-Ber.-Lagerpl.-Code** den Code des Lagerorts im Fertigungsbereich mit einer Menge von Komponenten ein, die der Maschinist verbrauchen kann, ohne eine Lageraktivität anfordern zu müssen, um sie zum Lagerplatz zu bringen. Artikel, die an diesem Lagerplatz eingelagert werden, werden in der Regel eingerichtet zur automatischen Buchung. Das bedeutet, dass das Feld **Buchungsmethode** die Option **Vorwärts** oder **Rückwärts** enthält.  
4. Geben Sie im Feld **Fert.-Bereitst.-Lagerplatzcode** den Code des Lagerplatzes im Fertigungsbereich an, wo Komponenten, die für die Fertigung an diesem Lagerplatz kommissioniert werden, standardmäßig platziert werden, bevor sie verbraucht werden können. Artikel, die an diesem Lagerplatz eingelagert werden, werden in der Regel eingerichtet zur manuellen Verbrauchsbuchung. Das bedeutet, dass das Feld **Buchungsmethode** **Manuell** oder **Kommiss. + Vorwärts** oder **Kommiss. + Rückwärts** für Kommissionierungen und Lagerbestandsumlagerungen enthält.  

    > [!NOTE]  
    >  Wenn Sie Lagerkommissionierungen verwenden, definiert das Feld **Lagerplatzcode** in der Komponentenzeile eines Fertigungsauftrags den *Entnahme*-Lagerplatz, in dem die Anzahl der Komponenten bei Buchung des Verbrauchs verringert wird. Wenn Sie Lagerbestandsumlagerungen verwenden, definiert das Feld **Lagerplatzcode** in FA-Komponentenzeilen den *Einlagerungs*-Lagerplatz im Vorgangsbereich, in dem der Lagermitarbeiter die Komponenten platzieren muss.  

5. Geben Sie im Inforegister **Lagerplätze** im Feld **Fert.-Ausgangslagerplatzcode** den Code des Lagerorts im Fertigungsbereich ein, von dem fertige Endartikel standardmäßig entnommen werden, sofern der Vorgang eine Lageraktivität beinhaltet. In den Basis-Lagerkonfigurationen wird die Aktivität als Lagereinlagerung oder Lagerbestandsumlagerung erfasst.  

Komponentenzeilen in Fertigungsaufträgen mit dem Vorgabe-Lagerplatzcode erfordern jetzt, dass mit der Methode "Vorwärts" geleerte Komponenten dort platziert werden. Jedoch können, bis die Komponenten von diesem Lagerplatz verbraucht sind, Komponenten von diesem Lagerplatz durch andere Bedarfsanforderungen kommissioniert oder verbraucht werden, weil sie weiterhin als verfügbare Lagerplatzinhalte gelten. Um sicherzustellen, dass der Lagerplatzinhalt nur für den Komponentenbedarf verfügbar ist, der diesen Fert.-Bereitst.-Lagerplatzcode verwendet, müssen Sie das Feld **Dediziert** der Zeile für diesen Lagerplatzcode auf der Seite **Lagerplätze** auswählen, das Sie über die Lagerortkarte öffnen.

Dieses Flussdiagramm zeigt, wie das Feld **Lagerplatzcode** in FA-Komponentenzeilen entsprechend Ihrer Einrichtung ausgefüllt wird.  

![Lagerplatz-Flussdiagramm](media/binflow.png "Lagerfluss")    

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a>Um eine Standardlagerplatzstruktur im Montagebereich zu definieren
Komponenten für Montageaufträge können nicht mit Lagerkommissionierungen kommissioniert oder gebucht werden. Verwenden Sie stattdessen die Seite **Lagerbestandsumlagerung**. Weitere Informationen finden Sie in[Umlagern von Komponenten in einen Arbeitsgangbereich in den grundlegenden Lagerfunktionen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Bei der Kommissionierung und Lieferung von Verkaufszeilenmengen, die auftragsbezogen montiert werden, müssen Sie bestimmte Regeln einhalten, wenn sie die Lagerkommissionierzeilen erstellen. Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in [Artikel mit Lagerkommissionierungen auswählen](warehouse-how-to-pick-items-with-inventory-picks.md).

Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md).

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a>So richten Sie ein, dass eine Lagerbestandsumlagerung automatisch erstellt wird, wenn die Lagerkommissionierung für die Montageartikel erstellt wird.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Montageeinrichtung** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das Kontrollkästchen **Umlagerungen automatisch erstellen**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a>Um den Lagerplatz im Montagebereich einzurichten, wo Komponenten standardmäßig platziert werden, bevor sie bei der Montage verbraucht werden können.
Der Wert in diesem Feld wird automatisch in das Feld **Lagerplatzcode** in Montageauftragszeilen eingefügt, wenn dieser Lagerort in das Feld **Lagerortcode** in der Montageauftragszeile eingegeben wird.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Lagerort, die Sie einrichten möchten.
3. Füllen Sie das Feld **Mont.-Bereitst.-Lagerplatzcode** aus.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a>Um den Lagerplatz im Montagebereich einzurichten, auf den fertige Montageartikel gebucht werden, wenn sie im Lager montiert werden.
Der Wert in diesem Feld wird automatisch in das Feld **Lagerplatzcode** in Montageauftragszeilenköpfen eingefügt, wenn dieser Lagerortcode in das Feld **Lagerortcode** in den Montageauftragszeilenkopf befüllt wird.

Lagerplatzcodes, die auf Lagerortkarten eingerichtet werden, geben einen standardmäßigen Warenfluss für bestimmte Lageraktivitäten an, wie für den Verbrauch von Komponenten in einer Produktionsabteilung. Zusätzliche Funktionen sind vorhanden, um sicherzustellen, dass Artikel, die an einem Vorgabe-Lagerplatz platziert werden, durch andere Aktivitäten nicht umgelagert oder kommissioniert werden können.

> [!NOTE]
> Dieses Setup ist nur für Lagerorte möglich, für die das Feld Lagerplatz notwendig ausgewählt ist.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Lagerort, die Sie einrichten möchten.
3. Füllen Sie das Feld **Montage-Ausgangslagerplatzcode** aus.

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a>Um den Lagerplatz einzurichten, auf den fertige Montageartikel gebucht werden, wenn sie entsprechend einem verknüpftem Auftrag montiert werden.
Von diesem Lagerplatz werden die Montageartikel sofort über eine Lagerkommissionierung geliefert, um den Verkaufsauftrag zu erfüllen.

> [!NOTE]
> Dieses Feld kann nicht verwendet werden, wenn für den Lagerort die Verwendung der gesteuerten Kommissionierung und Einlagerung eingerichtet wurde.

Der Lagerplatzcode wird aus der Verkaufsauftragszeile in den Montageauftragskopf kopiert, um Fließbandarbeitern mitzuteilen, wo der Abgang platziert werden muss, um ihn zum Liefern vorzubereiten. Er wird ebenfalls in die Lagerkommissionierzeile kopiert, um den Lagermitarbeiter mitzuteilen, von die Lieferung entnommen werden soll.

> [!NOTE]
> Der Auftragsmontage-Ausgangslagerplatz ist immer leer. Wenn Sie eine Auftragsmontage-Verkaufszeile buchen, dann wird der Lagerplatzinhalt zuerst positiv mit dem Montageausstoß reguliert. Unmittelbar danach wird er mit der gelieferten Menge negativ reguliert.

Der Wert in diesem Feld wird automatisch in das Feld "Lagerplatzcode" in Verkaufsauftragszeilen eingefügt, die eine Menge im Feld **Menge für Auftragsmontage** enthalten, oder wenn das Feld **Beschaffungsmethode** des zu verkaufenden Artikels **Auftragsmontage** enthält.

Wenn **LP-Code f. Prog.fert.lief.** leer ist, wird stattdessen das **Montage-Ausgangslagerplatzcode** Feld verwendet. Wenn beide Einrichtungsfelder leer sind, dann wird der zuletzt benutzte Lagerplatz mit Inhalt im Feld **Lagerplatzcode** in Verkaufsauftragszeilen verwendet.

Der gleiche Lagerplatzcode wird wiederum in das Feld **Lagerplatzcode** der Lagerkommissionierzeile kopiert, die die Lieferung der Auftragsmontagemenge verwaltet. Weitere Informationen finden Sie im Abschnitt "Verwenden von Auftragsmontageartikeln in [Artikel mit Lagerkommissionierungen auswählen](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Lagerort, die Sie einrichten möchten.
3. Füllen Sie das Feld **LP-Code f. Prog.fert.lief.** aus.

## <a name="to-create-dedicated-component-bins"></a>So erstellen Sie dedizierte Komponentenlagerplätze
Sie können angeben, dass Mengen in einem Lagerplatz vor der Kommissionierung für andere Bedarfsposten als den Bedarf ihres aktuellen Zwecks geschützt werden.

Mengen in Fert.-Bereitst.-Lagerplätzen/Fert.-Ausgangslagerplätzen können weiterhin reserviert werden. Entsprechend sind die Mengen in dedizierten Lagerplätzen im Feld **Total verfügbare Menge** auf der Seite **Reservierung** enthalten.

Beispielsweise wird eine Arbeitsplatzgruppe mit einem Lagerplatzcode im Feld **Fert.-Bereitst.-Lagerplatzcode** eingerichtet. Komponentenzeilen in Fertigungsaufträgen mit diesem Lagerplatzcode erfordern, dass mit der Methode "Vorwärts" geleerte Komponenten dort platziert werden. Jedoch können, bis die Komponenten von diesem Lagerplatz verbraucht sind, Komponenten von diesem Lagerplatz durch andere Bedarfsanforderungen kommissioniert oder verbraucht werden, weil sie weiterhin als verfügbare Lagerplatzinhalte gelten. Um sicherzustellen, dass der Lagerplatzinhalt nur für den Komponentenbedarf verfügbar ist, der diesen Fert.-Bereitst.-Lagerplatzcode verwendet, müssen Sie das Feld **Dediziert** der Zeile für diesen Lagerplatzcode auf der Seite **Lagerplätze** auswählen, das Sie über die Lagerortkarte öffnen.

Das Einrichten eines Fert.-Bereitst.-Lagerplatzes/Fert.-Ausgangslagerplatzes stellt ähnliche Funktionen für die Verwendung von Lagerplatzarten zur Verfügung, die nur in erweiterten Lagerfunktionen verfügbar sind. Weitere Informationen finden Sie unter [Einrichten von Lagerplatzarten](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Artikel in den Fert.-Bereitst.-Lagerplätzen/Fert.-Ausgangslagerplätzen werden nicht geschützt, wenn sie als Produktionskomponenten mit der Lagerkommissionierungsseite kommissioniert und verbraucht werden.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus. Wählen Sie die Lagerortkarte, die Sie aktualisieren möchten.  
2.  Wählen Sie die Aktion **Lagerplätze** aus.  
3.  Wählen Sie das Feld **Dediziert** für alle Lagerplätze aus, die für bestimmte interne Arbeitsgänge exklusiv verwendet werden sollen und an denen Mengen für diese Arbeitsgänge reserviert werden sollen, nachdem sie dort platziert wurden.  

> [!NOTE]  
>  Der Lagerplatz muss leer sein, damit das Feld **Dediziert** ausgewählt oder gelöscht werden kann.

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
