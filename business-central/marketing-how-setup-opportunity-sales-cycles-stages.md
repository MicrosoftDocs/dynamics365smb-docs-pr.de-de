---
title: Einrichten von Verkaufschancen für Verkaufsprozesse und Prozess-Stufen| Microsoft Docs
description: Beschreibt, wie Verkaufsstufen, vom ersten Kontakt bis zum Schließen definiert, einen Verkaufsprozess erstellt und diesen zu Verkaufschancen in Business Central zuweist.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.search.forms: 5122, 5121, 5120, 5175, 5119
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 16c72d0c0b2b14e73b390b585b505f00956ac4d4
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059752"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Einrichten von Verkaufsprozessen für Verkaufschancen und Prozess-Stufen
Damit die Verkaufschancen verwendet werden kann, müssen zunächst Verkaufsprozesse sowie Verkaufsprozess-Stufen eingerichtet werden. Ein Verkaufsprozess setzt sich aus einer Reihe von Schritten zusammen, die vom ersten Kontakt bis zu einem Verkaufsabschluss reichen. Jeder Stufe kann bestimmten Bedingungen haben, die erfüllen sein müssen (z. B. ein Verkaufsangebot), bevor eine Verkaufschance in die nächste Stufe gehen kann. Sie können auch festlegen, ob eine Stufe übersprungen werden kann. Verkaufsprozesse können in beliebiger Anzahl eingerichtet werden. Gleiches gilt auch für die Anzahl der Verkaufsprozess-Stufen, die innerhalb eines Verkaufsprozesses eingerichtet werden.

Das Implementieren des Verkaufsprozesses für Verkaufschancen umfasst das Einrichten des Verkaufsprozesscodes, das Definiert der verschiedenen Stufen des Zyklus, und das Zuweisen des Zyklus zu den Verkaufschancen. Durch Zuweisen der relevanten Aktivität der Verkaufschance oder Aufgaben kann auch ein Teil des Einrichtens eines Verkaufsprozesses sein.

Dieses Thema beschreibt auch Entscheidungsträgern als Einrichtungsaufgaben und die Aktivitäten und wie Aufgaben zu den Aktionen zugewiesen werden. Weitere Informationen finden Sie unter [Um Aktionen mit Aufgaben einzurichten](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Um Verkaufschancen-Zykluscodes einzurichten:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsprozesse** ein und wählen Sie dann den zugehörigen Link. Die Seite **Verkaufsprozesse** wird geöffnet und führt alle vorhandenen Verkaufsprozesse auf.
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Wiederholen Sie diese Schritte, um weitere Verkaufsprozesse einzurichten. Nachdem Sie Verkaufsprozesse für Verkaufschancen eingerichtet haben, können Sie die verschiedenen Stufen innerhalb jedes Prozesses einrichten.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Verkaufsprozessstufe der Verkaufschance definieren
1. Wählen Sie auf der Seite **Verkaufsprozesse** den Verkaufsprozess für Verkaufschancen aus, für den Sie Stufen einrichten möchten, und wählen Sie dann die Aktion **Stufen**. Die Seite **Verkaufsprozess-Stufen** wird geöffnet.
2. Klicken Sie auf **Neu**, um eine neue Stufe für den Verkaufsprozess einzugeben.

Wiederholen Sie diese Schritte, um beliebig viele Stufen innerhalb des Verkaufsprozesses einzurichten.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Eine Verkaufsprozessstufe zu einer Verkaufschance zuordnen
Nachdem Sie die Stufe des Verkaufprozesses hinzugefügt haben, können Sie Verkaufschancen hinzufügen und dann die Stufe des Verkaufprozesses zu Verkaufschancen hinzufügen, indem Sie das Feld **Verkaufsprozesscode** verwenden. Weitere Informationen finden Sie unter [Erstellen von Verkaufschancen](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Um Aktionen mit Aufgaben einzurichten
Sie können mehrere Aufgabe, zum Beispiel Tätigkeiten kombinieren, die jede einen Schritt darstellen in den Aktivitäten. Alle Schritte innerhalb einer Aktion sind durch ein Datenformular miteinander verbunden. Sie können Aktionen Verkaufschancen, Verkäufern bzw. den Kontakten zuweisen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Aktivitäten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus.
3. Im Inforegister **Zeilen** geben Sie die notwendigen Felder ein, um eine oder mehrere Aufgaben in der Aktivität zu definieren.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Um Aufgaben oder Aktionen von Aufgaben zu Verkaufschancen zuzuweisen
Wenn Sie eine Aufgabe eingerichtet haben, können Sie sie in einer Verkaufschance zuordnen und die Aktivität zuweisen, zu der die Aufgabe gehört.

> [!NOTE]  
>   Diese Vorgehensweise beschreibt, wie Sie Aktivitätsaufgaben zu Verkaufschancen zuweisen. die Schritte sind ähnlich, wenn Sie Verkäufer und den Kontakten Aufgaben zuordnen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufschancen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie eine Chance und wählen Sie dann die Aktion **Aufgaben** aus.
3. Wählen Sie auf der Seite **Aufgabenliste** die Aktion **Aufgabe erstellen**.
4.  Füllen Sie auf der Seite **Aufgabe erstellen** die Felder wie benötigt aus.

    Beachten Sie im Feld **Verkaufschance**, dass es automatisch der Verkaufschance zugewiesen wird.
5. Wählen Sie die Schaltfläche **OK** aus.
6. Auf der Seite **Aufgabenlisten** wählen Sie die Verkaufschance und dann die **Aktivität zuweisen**-Aktion aus.
7. Auf der Seite **Aktivität zuweisen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**.

## <a name="see-also"></a>Siehe auch
[Verarbeiten von Verkaufschancen](marketing-processing-sales-opportunities.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]