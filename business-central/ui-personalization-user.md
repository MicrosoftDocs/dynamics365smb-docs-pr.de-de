---
title: Personalisieren von Seiten | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen in Business Central entspricht.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922088"
---
# <a name="personalizing-your-workspace"></a>Personalisieren Ihres Arbeitsbereichs

Sie können Ihren Arbeitsbereich für Ihre Arbeit *personalisieren* oder anpassen und Präferenzen definieren, indem Sie die Seiten ändern, so dass Sie nur die Informationen angezeigt erhalten, die Sie benötigen. Die Personalisierungsänderungen, die Sie durchführen, beeinflussen nur, was Sie sehen, und nicht, was die Benutzer sehen.

Je nach Art der Seite und was enthalten ist, können Sie verschiedene Dinge tun, z.B. Verschieben und Ausblenden von Feldern, Spalten und Aktionen Verschieben und Ausblendern ganzer Teile und mehr.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Zusätzlich zu dem, was Benutzer personalisieren können, können Administratoren und Superuser die Personalisierungen der Benutzer überschreiben und definieren, welche Funktionen in allen oder bestimmten Unternehmen zugänglich sind. Weitere Informationen finden Sie unter [Anpassen von Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>So passen Sie eine Seite individuell an

1. In der rechten oberer Ecke wählen Sie ![Einstellungen](media/ui-experience/settings_icon_small.png "Symbol für Rollencenter einstellen") und dann **Personalisieren**.

    Das **Personalisieren** Banner erscheint oben und zeigt an, dass Sie mit den Änderungen beginnen können.

    ![Modus personalisieren](media/ui_personalize_mode_small.png "Modus personalisieren")

2. Öffnen Sie die Seite, die Sie personalisieren möchten.

    Wenn Sie im Banner ein ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") oder ![Personalisieren blockiert](media/personalization-blocked-icon.png "Personalisieren blockiert") sehen, können Sie die Seite nicht personalisieren. Weitere Informationen finden Sie unter [Warum kann ich die Seite nicht personalisieren](ui-personalization-locked.md).

3. Zeigen Sie auf einen Bereich, den Sie anpassen möchten, beispielsweise ein Feld oder ein Spaltenüberschrift in einer Liste. Alles, was Sie anpassen können, wird gleichzeitig mit einer Pfeilspitze oder einem Rahmen hervorgehoben. Im [nächsten Abschnitt](#What) finden Sie Einzelheiten darüber, was Sie tun können.

4. Sie können fortfahren, um Änderungen auf derselben Seite vorzunehmen oder eine andere Seite zu öffnen. Ihre Änderungen werden automatisch gespeichert, während Sie diese erstellen. Wenn Sie im Fenster **Personalisieren** Banner fertig sind, wählen Sie **Erledigt** aus.

## <a name="What"></a>Was Sie personalisieren können

|Was möchten Sie tun|So geht es|Bemerkungen|
|----|------------|-------|
|Etwas verschieben, wie ein Feld, eine Spalte in der Liste, eine Kachel, Aktion oder ein Teil|Zeigen Sie auf eine beliebige Stelle in, was Sie befördern möchten, und ziehen Sie sie im neuen Lagerort. Der Lagerort wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.<br /><br />![Symbol "Kann nicht hierher verschoben werden"](media/personalization-cannot-move-here.png "Personalisierungsmodus - Symbol \"Kann nicht hierher verschoben werden\"") gibt an, dass Sie das Element nicht an den ausgewählte Standort verschieben können.|Die Teile sind Unterteilungen oder Regionen auf einer Seite, die Bedingungen wie mehrere Felder, eine andere Seite, Ein Diagramm oder Kacheln enthalten.<br /><br />Weitere Einzelheiten zur Aktionspersonalisierung finden Sie im [nächsten Abschnitt](ui-personalization-user.md#Actions). |
|Etwas ausblenden, wie ein Feld, eine Spalte in der Liste, eine Kachel oder ein Teil.|Auswählen der Pfeilspitze und wählen Sie <b>Ausblenden</b> aus.|Wenn das Feld, das Sie ausblenden, auch in der Inforegisterüberschrift angezeigt wird, wenn das Inforegister reduziert ist, erscheint das Feld dort nicht länger.|
|Hinzufügen eines Felds oder einer Spalte.|Im Banner<b>Personalisieren</b> wählen Sie <b>mehr</b> und wählen Sie das <b>Feld</b> aus.<br /></br>Der Berecih <b>Feld oder Seite hinzufügen</b> wird geöffnet auf der rechten Seite. Es führt die Felder auf, die Sie auf der Seite hinzufügen können.<br /><br />Um ein Feld hinzuzufügen, ziehen Sie es aus dem Bereich an den gewünschten Ort. Der Lagerort wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.|Jede Seite enthält einen vordefinierten Satz von Feldern, die Sie anzeigen können. Verwenden Sie dieses Verfahren, um Felder oder Spalten hinzuzufügen, die zuvor nicht angezeigt wurden oder um Felder anzuzeigen, die Sie ausgeblendet haben.|
|Zeigen Sie ein Feld in der Überschrift eines Inforegisters an, wenn das Inforegister reduziert ist.|Wählen Sie die Pfeilspitze aus und wählen Sie <b>Bei Reduzierung anzeigen</b> aus. <br /> <br />Wenn Sie diese Option nicht finden, ist sie bereits festgelegt. In diesem Fall wählen Sie <b>Immer anzeigen</b> aus, damit das Feld nicht mehr in der Inforegisterüberschrift angezeigt wird.|*Inforegister* ist der Begriff, der für eine Gruppe von Feldern verwendet wird, die unter einer gemeinsamen Überschrift angezeigt werden. Verwenden Sie <b>Bei Reduzierung anzeigen</b>-Option, um die wichtigsten Felder anzuzeigen. Wenn Sie ein Feld im der Überschrift auswählen, wird das Inforegister mit Fokus auf dem ausgewählten Feld geöffnet.<br /><br />Diese Option wird nur angewendet, wenn eine Seite mehr als ein Inforegister hat. Wenn nur ein Inforegister da ist, kann es nicht reduziert werden, sodass die <b>Bei Reduzierung anzeigen</b>-Option nicht verfügbar ist.|
|Lassen Sie ein Feld anzeigen, wenn Sie **Mehr anzeigen** auswählen.|Wählen Sie die Pfeilspitze aus und wählen Sie <b>Unter „Mehr anzeigen“ anzeigen</b> aus. <br /> <br />Wenn Sie die Option <b>Unter „Mehr anzeigen“ anzeigen</b> nicht sehen, ist sie bereits festgelegt. Wenn Sie in diesem Fall ein Feld immer anzeigen lassen möchten, und nicht nur, wenn Sie **Mehr anzeigen** auswählen, wählen Sie <b>Immer anzeigen</b> aus.||
|Ändern Sie die Fixierung von Spalten in der Liste. |Wählen Sie die Spalte der Pfeilspitze, die Sie als letzte Spalte der Fixierung möchten, und wählen Sie dann <b>Fixierung einstellen</b> aus.<br /><br/>Wenn Sie die Fixierung wieder am ursprünglichen Ort wünschen, wählen Sie die Pfeilspitze für die aktuelle Fixierung und wählen Sie <b>Fixierung löschebn</b> aus. Hinweis: Sie können die ursprüngliche Fixierung nicht entfernen.|Der Fixierungsbereich gibt die Spalten an, die immer links erscheinen, auch wenn Sie horizontal blättern.|  
|Ändern der Breite einer Spalte.|In der Tabellenkopfzeile ziehen Sie den rechten Rand der Spalte. <br /><br />Um die Spaltenbreite zu maximieren, um die längste Textzeile in der Spalte anzupassen, doppelklicken Sie auf den rechten Rand.||
|Überspringen Sie ein Feld, wenn die EINGABETASTE gedrückt wird.|Wählen Sie die Pfeilspitze neben dem Feld oder der Spaltenüberschrift in der Liste aus, und wählen Sie **Von der Schnelleingabe ausschließen** aus. <br /><br /> Wenn Sie diese Option nicht sehen, ist das Überspringen für das Feld bereits festgelegt. Wenn Sie in diesem Fall Überspringen des Felds beenden möchten, wählen Sie **In Schnelleingabe einbeziehen** aus. |Siehe [Beschleunigen der Dateneingabe mithilfe der Schnelleingabe](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Personalisieren von Aktionen

Sie können die Aktionsleiste personalisieren, die sich oben auf der Seite befindet. Dies wird in der folgenden Abbildung im hervorgehebenen Bereich dargestellt.

![Personalisieren der Aktionsleiste](media/personalize-action-bar.png "Personalisieren der Aktionsleiste")

Mit der Personalisierung können Sie entscheiden, welche Aktionen auf der Befehlsleiste angezeigt werden und wo diese angezeigt werden. Sie können einzelne Aktionen oder Aktionsgruppen ausblenden, anzeigen oder verschieben. Das Personalisieren der Aktionsleiste wird im Grunde wie bei anderen Elementen des Arbeitsbereichs durchgeführt. Allerdings hängen die Möglichkeiten einer Aktion oder Gruppe von der Position der Aktion oder Gruppe auf der Aktionsleiste ab. Die beste Methode dies herauszufinden ist, es einfach auszuprobieren und sich vom Bildschirm führen zu lassen. Die folgenden Abschnitte erklären einige der Nuancen der Personalisierung der Aktionsleiste.

### <a name="action-bar-overview"></a>Aktionsleisten-Übersicht

Es gibt einige Bedingungen, mit denen Sie vertraut sein sollten, um die Aktionsanpassung besser zu verstehen: *Aktionsgruppe* und *Heraufgestufte Kategorie*.  

*Aktionsgruppe* ist das Element, das sich erweitert, um weitere Aktionen oder Gruppen anzuzeigen. Zum Beispiel ist **Buchen** in der folgenden Abbildung eine Aktionsgruppe.

Eine *Heraufgestufte Kategorie* ist eine Aktionsgruppe, die zwischen den beiden senkrechten Strichen `|` auf der Befehlsleiste erscheint. Die Kategorien enthalten normalerweise die am häufigsten verwendeten Aktionen, sodass Sie sie schnell finden können. Zum Beispiel sind **Freigeben**, **Buchen**, **Rechnung** und **Navigieren** in der folgenden Abbildung heraufgestufte Kategorien.

![Personalisieren der Aktionsleistengruppe](media/personalize-action-bar-group-clip.png "Personalisieren der Aktionsleistengruppe")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>So werden Aktionen und Gruppen entfernt, ausgeblendet und angezeigt

Um eine Aktion oder Aktionsgruppe anzuzeigen oder auszublenden, wählen Sie sie aus und wählen dann eine der folgenden Optionen aus:

|Option|Was sie tut|
|------|------------
|**Löschen**|Diese Option wird angezeigt, wenn die ausgewählte Aktion auch anderswo auf der Aktionsleiste angezeigt wird. Wird diese Option ausgewählt, wird die Aktion aus dem ausgewählten Standort gelöscht, sodass sie nicht mehr angezeigt wird. Die Aktion oder Aktionsgruppe bleibt am anderen Standort. |
|**Ausblenden**|Diese Option wird angezeigt, wenn sich die Aktion oder Aktionsgruppe an keiner anderen Stelle auf der Befehlsleiste befindet. Zum Beispiel **Löschen**; wird diese Option ausgewählt, wird die Aktion oder die Aktionsgruppe von der Aktionsleiste verschwinden. Im Personalisierungsmodus wird die Aktion oder die Aktionsgruppe allerdings noch an der aktuellen Stelle angezeigt, wenn auch abgedunkelt.|
|**Anzeigen**|Diese Option wird angezeigt, wenn die Aktion oder Aktionsgruppe zuvor ausgeblendet wurde (abgedunkelt). Wird diese Option ausgewählt, wird die Aktion oder die Aktionsgruppe in der Aktionsleiste erscheinen.|

### <a name="to-move-actions-and-action-groups"></a>So werden Aktionen und Aktionsgruppen verschoben

Um eine Aktion oder eine Aktionsgruppe zu verschieben, ziehen Sie sie an die gewünschte Stelle, wie bei Feldern und Spalten.

Stellen, an denen Sie Aktionen oder Aktionsgruppen ablegen können, wird durch eine horizontale Linie zwischen zwei Aktionen oder einem Rand um eine Aktionsgruppe angegeben.

- Sie können einzelne Aktionen in die heraufgestuften Kategorien verschieben, aber Sie können die Reihenfolge der Aktionen in der Kategorie nicht neu anordnen.
- Sie können eine Aktionsgruppe nicht in eine heraufgestufte Kategorie verschieben.
- Um eine Aktion oder eine Aktionsgruppe in eine andere leere Aktionsgruppe zu verschieben, ziehen Sie Aktion oder Aktionsgruppe in die neue Gruppe und lassen Sie sie im Feld **Aktion hier ablegen** fallen.

## <a name="additional-points-of-interest"></a>Zusätzliche Punkte von Interesse

Um die Personalisierung besser zu verstehen, finden Sie hier einige Hinweise.

- Wenn Sie Änderungen auf einer Kartenseite vornehmen, gelten die Änderungen für alle Datensätze, die Sie aus dieser Übersicht öffnen. Wenn Sie beispielsweise einen bestimmten Debitor aus der Debitorenlistenseite öffen und anschließend die Seite anpassen, indem Sie ein Feld hinzufügen. Wenn Sie andere Debitoren aus der Liste öffnen, wird das Feld, das Sie hinzugefügt haben, auch angezeigt.
- Änderungen, die Sie machen, treten in allen Ihren Rollencenter in Kraft. Wenn Sie beispielsweise eine Änderung in der Liste der Debitoren ändern, wenn das Rollencenter auf Geschäftsführer festgelegt ist, finden Sie auch die Änderung in der Debitorenübersicht, wenn das Rollencenter auf Verkaufsauftragsprozess festgelegt wurde.
- Änderungen an einer Seite in einem Bereich treten auf der Seite in Kraft, in der sie angezeigt werden.  
- Sie können Felder und Spalten von einer vordefinierten nur Liste hinzufügen, die auf der Seite sind. Sie können keine neuen Referenzen erstellen.

## <a name="to-clear-personalization"></a>So wird eine Personalisierung gelöscht

Deaktivieren Sie einige oder alle an dieser Seite im Lauf der Zeit vorgenommenen Personalisierungsänderungen. Um dies zu tun, wählen Sie **Personalisieren** und **Mehr**, **Personalisierung löschen** und dann eine der folgenden Optionen. Beachten Sie, dass das Löschen der Personalisierung nicht rückgängig gemacht werden kann.

|Option|Was sie tut|
|------|------------
|Nur Aktionen|Löscht die Personalisierungsänderungen, die Sie an der Aktionsleiste dieser Seite gemacht haben.|
|Alles außer Aktionen|Löscht die Personalisierungsänderungen, die Sie an dieser Seite gemacht haben, außer denen in der Aktionsleiste. Dies umfasst Änderungen an Feldern, Spalten, Teilen und Kacheln. |
|Alle|Löscht alle an dieser Seite vorgenommenen Personalisierungsänderungen, sodass die Seite wieder wie vorher aussieht. Dies umfasst Änderungen an der Aktionsleiste, den Feldern, Spalten, Teilen und Kacheln.|

## <a name="see-also"></a>Siehe auch

[Verwalten der Personalisierung](ui-personalization-manage.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
