---
title: Einrichten von Verkaufsprozessen für Verkaufschancen und Prozess-Stufen
description: Beschreibt, wie Verkaufsstufen, vom ersten Kontakt bis zum Schließen definiert, einen Verkaufsprozess erstellt und diesen zu Verkaufschancen in Business Central zuweist.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.search.forms: 5122, 5121, 5120, 5175, 5119, 5098, 5096
ms.date: 05/27/2022
ms.author: jswymer
ms.openlocfilehash: 4d87bc092ceffafecd460380a8a7d93849e988e6
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808985"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Einrichten von Verkaufsprozessen für Verkaufschancen und Prozess-Stufen

Bevor Sie mit der Verwendung von Verkaufschancen beginnen, müssen zunächst Verkaufsprozesse und Verkaufsprozess-Stufen einrichten. Ein Verkaufsprozess setzt sich aus einer Reihe von Schritten zusammen, die vom ersten Kontakt bis zu einem Verkaufsabschluss reichen. Für jede Stufe legen Sie die Anforderungen fest, die erfüllt werden müssen, wie z. B. ein Verkaufsangebot, bevor eine Verkaufschance in die nächste Stufe übergehen kann. Sie können auch festlegen, ob eine Stufe übersprungen werden kann. Sie können so viele Verkaufszyklen einrichten, wie Sie benötigen. Sie können innerhalb eines Verkaufszyklus so viele Phasen wie nötig einrichten.

Um Verkaufsprozesse für Verkaufschancen zu verwenden, müssen Sie den Verkaufsprozess einrichten, die verschiedenen Stufen des Prozesses definieren und den Prozess anschließend Verkaufschancen zuweisen. Durch Zuweisen der relevanten Aktivität der Verkaufschance oder Aufgaben kann auch ein Teil des Einrichtens eines Verkaufsprozesses sein.

In diesem Artikel wird auch beschrieben, wie Aufgaben und Aktivitäten eingerichtet und Aufgaben Aktivitäten zugewiesen werden. Weitere Informationen finden Sie unter [Um Aktionen mit Aufgaben einzurichten](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Um Verkaufschancen-Zykluscodes einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsprozesse** ein und wählen Sie dann den zugehörigen Link. Die Seite **Verkaufsprozesse** wird geöffnet und führt alle vorhandenen Verkaufsprozesse auf.
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Wiederholen Sie diese Schritte, um weitere Verkaufsprozesse einzurichten. Nachdem Sie Verkaufsprozesse für Verkaufschancen eingerichtet haben, können Sie die verschiedenen Stufen innerhalb jedes Prozesses einrichten.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Verkaufsprozessstufe der Verkaufschance definieren

1. Wählen Sie auf der Seite **Verkaufsprozesse** den Verkaufsprozess für Verkaufschancen aus, für den Sie Stufen einrichten möchten, und wählen Sie dann die Aktion **Stufen**. Die Seite **Verkaufsprozess-Stufen** wird geöffnet.
2. Klicken Sie auf **Neu**, um eine neue Stufe für den Verkaufsprozess einzugeben.

Wiederholen Sie diese Schritte, um beliebig viele Stufen innerhalb des Verkaufsprozesses einzurichten.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Eine Verkaufsprozessstufe zu einer Verkaufschance zuordnen

Nachdem Sie die Stufe des Verkaufprozesses hinzugefügt haben, können Sie Verkaufschancen hinzufügen und dann die Stufe des Verkaufprozesses zu Verkaufschancen hinzufügen, indem Sie das Feld **Verkaufsprozesscode** verwenden. Weitere Informationen finden Sie unter [Erstellen von Verkaufschancen](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Um Aktionen mit Aufgaben einzurichten

Sie können mehrere Aufgaben, z. B. Aufgaben, die jeweils einen Schritt darstellen, in Aktivitäten kombinieren. Alle Schritte innerhalb einer Aktion sind durch ein Datenformular miteinander verbunden. Sie können Aktionen Verkaufschancen, Verkäufern bzw. den Kontakten zuweisen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aktivitäten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Im Inforegister **Zeilen** geben Sie die notwendigen Felder ein, um eine oder mehrere Aufgaben in der Aktivität zu definieren.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Um Aufgaben oder Aktionen von Aufgaben zu Verkaufschancen zuzuweisen

Wenn Sie eine Aufgabe eingerichtet haben, können Sie sie in einer Verkaufschance zuordnen und die Aktivität zuweisen, zu der die Aufgabe gehört.

> [!NOTE]
> Sie können keine Aufgaben vom Typ *Besprechung* in [!INCLUDE [prod_short](includes/prod_short.md)] Online erstellen. Die Funktion erfordert Zugriff auf eine lokale Bereitstellung.

Die folgende Vorgehensweise beschreibt, wie Sie Verkaufschancen Aktivitätsaufgaben zuweisen. Die Schritte sind ähnlich, wenn Sie Verkäufern und Kontakten Aufgaben zuweisen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufschancen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie eine Chance und wählen Sie dann die Aktion **Aufgaben** aus.
3. Wählen Sie auf der Seite **Aufgabenliste** die Aktion **Aufgabe erstellen**.
4. Füllen Sie auf der Seite **Aufgabe erstellen** die Felder wie benötigt aus. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Wie aus dem Feld **Verkaufschance** zu ersehen ist, wird die Aufgabe automatisch der entsprechenden Verkaufschance zugewiesen.
5. Wählen Sie die Schaltfläche **OK**.
6. Auf der Seite **Aufgabenlisten** wählen Sie die Verkaufschance und dann die **Aktivität zuweisen**-Aktion aus.
7. Auf der Seite **Aktivität zuweisen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

## <a name="see-also"></a>Weitere Informationen

[Verarbeiten von Verkaufschancen](marketing-processing-sales-opportunities.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]