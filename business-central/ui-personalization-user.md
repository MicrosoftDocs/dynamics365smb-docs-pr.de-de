---
title: Personalisieren von Seiten | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen in Business Central entspricht.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c0fe93df0022f66aa5cc3964c2717e2e6ca76147
ms.sourcegitcommit: 8a4e66f7fc8f9ef8bdf34595e0d3983df4749376
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262190"
---
# <a name="personalize-your-workspace"></a>Ihren Arbeitsbereich personalisieren
Sie können Ihren Arbeitsbereich für Ihre Arbeit personalisieren oder anpassen und Präferenzen definieren, indem Sie die Seiten ändern, so dass Sie nur die Informationen angezeigt erhalten, die Sie auch benötigen. Die Personalisierungsänderungen, die Sie durchführen, beeinflussen nur, was Sie sehen, und nicht, was die Benutzer sehen.

Sie können alle Arten von Seiten personalisieren, einschließlich der Seite Rollencenter. Weitere Informationen zu Rollencentern finden Sie unter [Rollencenter](ui-change-basic-settings.md#role-center).

Je nach Art der Seite und was enthalten ist, können Sie verschiedene Änderungen vornehmen, z.B. Verschieben und Ausblenden von Feldern, Spalten,Aktionen oder Verschieben und Ausblendern ganzer Teile und mehr. Die meisten Personalisierungen müssen durch erstmaliges Aktivieren der Banner **Personalisierung** vorgenommen werden, aber sehr einfache Anpassungen wie Spaltenbreite, können sofort auf jeder Liste durchgeführt werden.

> [!NOTE]
> Administratoren können dieselben Layoutänderungen wie Benutzer durchführen, indem sie den Arbeitsbereich für ein Profil anpassen, dem mehrere Benutzer zugewiesen sind. Weitere Informationen finden Sie unter [Seiten für Profile anpassen](ui-personalization-manage.md)<br /><br />
Administratoren können auch Personalisierungen der Benutzer überschreiben und definieren, welche Funktionen in allen oder bestimmten Unternehmen zugänglich sind. Weitere Informationen finden Sie unter [Anpassen von Business Central](ui-customizing-overview.md).

## <a name="to-change-the-width-of-a-column"></a>Ändern der Breite einer Spalte
Sie können die Größe von Spalten in jeder Liste leicht ändern, indem Sie die Grenze zwischen zwei Spalten nach links oder rechts ziehen.
1. Ziehen Sie im Kopf einer Liste die Grenze zwischen zwei Spalten.
2. Alternativ können Sie auch auf die Grenze zwischen zwei Spalten doppelklicken, um die Breite der Spalte automatisch anzupassen. Dadurch wird die Breite auf die für die Lesbarkeit optimale Größe eingestellt.

Wie bei anderen Personalisierungen werden die Änderungen, die Sie an der Spaltenbreite vornehmen, in Ihrem Konto gespeichert und folgen Ihnen, unabhängig davon, auf welchem Gerät Sie sich anmelden.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>So beginnen Sie mit der Personalisierung einer Seite über das Banner **Personalisieren**
1. Öffnen Sie eine beliebige Seite, die Sie personalisieren möchten.
2. In der rechten oberer Ecke wählen Sie das Symbol ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollencenter") aus und wählen dann die Aktion **Personalisieren**.

    Das **Personalisieren** Banner erscheint oben und zeigt an, dass Sie mit den Änderungen beginnen können.

    > [!NOTE]
    > Um während der Personalisierung zu navigieren, drücken Sie Strg + Klicken auf eine Aktion, wenn diese durch die Pfeilspitze hervorgehoben ist.

    Wenn Sie im Banner ein ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") oder ![Personalisieren blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") auf dem Banner sehen, können Sie die Seite nicht personalisieren. Weitere Details finden Sie unter [Warum eine Seite zum Personalisieren gesperrt ist](ui-personalization-locked.md).

3. Um ein Feld hinzuzufügen, wählen Sie die **+ Feld** Aktion.
4. Von dem Bereich **Feld zu Seite hinzufügen** ziehen Sie ein Feld per Drag & Drop an die gewünschte Position auf der Seite.
5. Zeigen Sie zum Ändern eines Oberflächenelements auf das Element, z. B. eine Aktion, ein Feld oder einen Teil. Das Element wird sofort mit einer Pfeilspitze oder einem Rand hervorgehoben.
6. Wählen Sie das Element aus und wählen Sie dann eine der beiden Optionen **Bewegung**, **Entfernen**, **Verbergen, verstecken**, **Anzeigen**, **Anzeigen unter mehr anzeigen**, **Anzeigen, wenn alle verborgen**, **Immer anzeigen**, **Einfrierfenster einstellen/löschen**, oder **Schnelleingabe einschließen/ausschließen**, abhängig vom T und Status des Oberflächenelements. Weitere Informationen finden Sie unter [Was Sie personalisieren können](#What).
7. Wenn Sie das Layout einer oder mehrerer Seiten geändert haben, wählen Sie die Schaltfläche **Fertig** im Banner **Personalisierung**.

## <a name="what-you-can-personalize"></a><a name="What"></a>Was Sie personalisieren können

|Was möchten Sie tun|So geht es|Bemerkungen|
|----|------------|-------|
|Etwas verschieben, wie ein Feld, eine Spalte in der Liste, eine Kachel, Aktion oder ein Teil|Zeigen Sie auf eine beliebige Stelle, was Sie verschieben möchten, und ziehen Sie sie an die neue Position. Die Position wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.<br /><br />![Symbol „Kann nicht hierher verschoben werden“](media/personalization-cannot-move-here.png "Personalisierungsmodus – Symbol „Kann nicht verschoben werden“") gibt an, dass Sie das Element nicht an den ausgewählten Standort verschieben können.|Die Teile sind Unterteilungen oder Regionen auf einer Seite, die Bedingungen wie mehrere Felder, eine andere Seite, Ein Diagramm oder Kacheln enthalten.<br /><br />Weitere Einzelheiten zur Aktionspersonalisierung finden Sie unter [Personalisierungs-Aktionen](ui-personalization-user.md#Actions). |
|Etwas verbergen, wie ein Feld, eine Spalte in der Liste, eine Kachel, Aktion oder ein Teil.|Pfeil wählen und <b>Ausblenden</b> auswählen.|Das Element ist im Personalisierungsmodus grau hinterlegt. Wenn das Feld, das Sie ausblenden, auch in der Inforegisterüberschrift angezeigt wird, wenn das Inforegister reduziert ist, wird das Feld dort nicht länger angezeigt.|
|Versteckte Aktionen und Teile anzeigen.|Wählen Sie für ein graues (ausgeblendetes) Element die Pfeilspitze und dann <b>Anzeigen</b>.|Das versteckte Element ist wieder sichtbar.|
|Hinzufügen eines Felds oder einer Spalte.|In dem <b>Personalisierung</b> Banner, wählen Sie die <b>+ Feld</b> Aktion.<br /></br>Der Berecih <b>Feld oder Seite hinzufügen</b> wird geöffnet auf der rechten Seite. Es führt die Felder auf, die Sie auf der Seite hinzufügen können.<br /><br />Um ein Feld hinzuzufügen, ziehen Sie es von der Position an den gewünschten Ort. Die Position wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.|Jede Seite enthält einen vordefinierten Satz von Feldern, die Sie anzeigen können. Verwenden Sie dieses Verfahren, um Felder oder Spalten hinzuzufügen, die zuvor nicht angezeigt wurden oder um Felder anzuzeigen, die Sie ausgeblendet haben.|
|Zeigen Sie ein Feld in der Überschrift eines Inforegisters an, wenn das Inforegister reduziert ist.|Wählen Sie die Pfeilspitze aus und dann wählen Sie <b>Bei Reduzierung anzeigen</b> aus. <br /> <br />Wenn Sie diese Option nicht finden, ist sie bereits festgelegt. In diesem Fall wählen Sie <b>Immer anzeigen</b> auf dem Inforegister aus, damit das Feld nicht mehr in der Inforegisterüberschrift angezeigt wird.|*Inforegister* ist der Begriff, der für eine Gruppe von Feldern verwendet wird, die unter einer gemeinsamen Überschrift angezeigt werden. Verwenden Sie <b>Bei Reduzierung anzeigen</b>-Option, um die wichtigsten Felder anzuzeigen. Wenn Sie ein Feld im der Überschrift auswählen, wird das Inforegister mit Fokus auf dem ausgewählten Feld geöffnet.<br /><br />Diese Option wird nur angewendet, wenn eine Seite mehr als ein Inforegister hat. Wenn nur ein Inforegister da ist, kann es nicht reduziert werden, sodass die <b>Bei Reduzierung anzeigen</b>-Option nicht verfügbar ist.|
|Lassen Sie ein Feld anzeigen, wenn Sie **Mehr anzeigen** auswählen.|Wählen Sie die Pfeilspitze aus und wählen Sie dann <b>Unter „Mehr anzeigen“ anzeigen</b> aus. <br /> <br />Wenn Sie die Option <b>Unter „Mehr anzeigen“ anzeigen</b> nicht sehen, ist sie bereits festgelegt. Wenn Sie in diesem Fall ein Feld immer anzeigen lassen möchten, und nicht nur, wenn Sie **Mehr anzeigen** auswählen, wählen Sie <b>Immer anzeigen</b> aus.||
|Ändern Sie die Fixierung von Spalten in der Liste. |Wählen Sie nun die Spalte der Pfeilspitze, die Sie als letzte Spalte der Fixierung möchten, und wählen Sie dann <b>Fixierung einstellen</b> aus.<br /><br/>Wenn Sie die Fixierung wieder am ursprünglichen Ort wünschen, wählen Sie die Pfeilspitze für die aktuelle Fixierung und wählen Sie dann <b>Fixierung löschen</b> aus. Hinweis: Sie können die ursprüngliche Fixierung nicht entfernen.|Der Fixierungsbereich gibt die Spalten an, die immer links erscheinen, auch wenn Sie horizontal blättern.|  
|Überspringen Sie ein Feld, wenn die EINGABETASTE gedrückt wird.|Wählen Sie die Pfeilspitze neben dem Feld oder der Spaltenüberschrift in der Liste aus, und wählen Sie dann **Von der Schnelleingabe ausschließen** aus. <br /><br /> Wenn Sie diese Option nicht sehen, ist das Überspringen für das Feld bereits festgelegt. Wenn Sie in diesem Fall Überspringen des Felds beenden möchten, wählen Sie **In Schnelleingabe einbeziehen** aus. |Siehe [Beschleunigen der Dateneingabe mithilfe der Schnelleingabe](ui-enter-data.md#QuickEntry)|
|Ordnen und entfernen Sie Ansichten, die gefilterte Listen darstellen.|Klicken Sie auf die Pfeilspitze neben einer Ansicht und wählen Sie dann **Verschieben**, **Entfernen**, oder **Verbergen**.|Weitere Informationen unter [Speichern und personalisieren Sie Listenansichten](ui-views.md)|  
|Fügen Sie einer Seite oder einem Bericht in Ihrem Role Center eine neue Aktion hinzu.|Wählen Sie das Lesezeichensymbol auf der Zielseite, auf der Berichtsanforderungsseite oder im Fenster „Wie möchten Sie weiter verfahren“ aus.|Weitere Informationen finden Sie unter [Erstellen eines Lesezeichens für eine Seite oder einen Bericht im Rollencenter](ui-bookmarks.md)|
|Listen immer erweitert oder reduziert anzeigen|Wählen Sie die Schaltfläche „Alle erweitern“ oder „Alle reduzieren“ oben rechts in der Liste, oder wählen Sie die Aktion „Alle erweitern“ oder „Alle reduzieren“ im Menü der ersten Spalte aus. |Gilt für reduzierbare Hierarchielisten|

## <a name="personalizing-actions"></a><a name="Actions"></a>Personalisieren von Aktionen

Mit der Personalisierung können Sie entscheiden, welche Aktionen auf den Navigations- und Aktionsleisten und in den Rollenzentren angezeigt werden sollen und wo sie angezeigt werden sollen. Sie können einzelne Aktionen oder Aktionsgruppen ausblenden, anzeigen oder verschieben. Die Personalisierung der Navigations- und Aktionsleisten erfolgt im Wesentlichen auf die gleiche Weise wie bei anderen UI-Elementen. Allerdings hängen die Möglichkeiten einer Aktion oder Gruppe von der Position der Aktion oder der Gruppe auf der Aktionsleiste ab. Die beste Methode dies herauszufinden ist, es einfach auszuprobieren und sich von den Pfeilen führen zu lassen.

Es gibt einige Bedingungen, mit denen Sie vertraut sein sollten, um die Aktionsanpassung besser zu verstehen: *Aktionsgruppe* und *Heraufgestufte Kategorie*.  

Eine *Aktionsgruppe* ist ein Element, das sich erweitert, um weitere Aktionen oder Gruppen anzuzeigen. Zum Beispiel auf der **Kundenaufträge** Seite, die **Funktionen** Aktion, die bei Auswahl der Aktionen **Aktionen** angezeigt wird, ist eine Aktionsgruppe.

Eine *Heraufgestufte Kategorie* ist eine Aktionsgruppe, die vor der senkrechten Linie `|` auf der Befehlsleiste erscheint. Die Kategorien enthalten normalerweise die am häufigsten verwendeten Aktionen, sodass Sie sie schnell finden können. Zum Beispiel auf der **Kundenaufträge** Seite sind die Aktionen **Bestellung**, **Freisetzung** und **Buchungen** heraufgestufte Kategorien.

> [!NOTE]
> Sie können die Aktionsleiste, die in Teilen auf der Seite angezeigt wird, nicht personalisieren (z. B. den Teil der Verkaufszeilen auf der Seite **Verkaufsauftrag**).

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>So werden Aktionen und Aktionsgruppen entfernt, ausgeblendet und angezeigt
Wenn Sie eine Aktion ein- oder ausblenden möchten, definieren die Optionen unter der Pfeilspitze, was je nach Status der Aktion geschehen kann.
1. Wählen Sie die Pfeilspitze für eine Aktion oder Aktionsgruppe aus.
2. Wählen Sie eine der folgenden Optionen aus:

|Option|Was sie tut|
|------|------------
|**Löschen**|Diese Option wird angezeigt, wenn die ausgewählte Aktion auch an anderer Stelle in der Navigations- oder Aktionsleiste angezeigt wird. Wird diese Option ausgewählt, wird die Aktion aus dem ausgewählten Standort gelöscht, sodass sie nicht mehr angezeigt wird. Die Aktion oder Aktionsgruppe bleibt am anderen Standort. |
|**Ausblenden**|Diese Option wird angezeigt, wenn sich die Aktion oder Aktionsgruppe nicht an anderer Stelle in der Navigationsleiste oder Aktionsleiste befindet. Wie **Entfernen** führt die Auswahl dieser Option dazu, dass die Aktion oder Aktionsgruppe aus der Navigations- oder Aktionsleiste verschwindet. Im Personalisierungsmodus wird die Aktion oder die Aktionsgruppe allerdings noch an der aktuellen Stelle angezeigt, aber abgedunkelt.|
|**Anzeigen**|Diese Option wird angezeigt, wenn die Aktion oder Aktionsgruppe zuvor ausgeblendet wurde (abgedunkelt). Wenn Sie diese Option wählen, erscheint die Aktion oder Aktionsgruppe in der Navigationsleiste oder der Aktionsleiste.|

### <a name="to-move-actions-and-action-groups"></a>So werden Aktionen und Aktionsgruppen verschoben
Stellen, an denen Sie Aktionen oder Aktionsgruppen ablegen können, wird durch eine horizontale Linie zwischen zwei Aktionen oder einem Rand um eine Aktionsgruppe angegeben. Folgende Beschränkungen gelten:

- Sie können einzelne Aktionen in die heraufgestuften Kategorien verschieben, aber Sie können die Reihenfolge der Aktionen in der Kategorie nicht neu anordnen.
- Sie können eine Aktionsgruppe nicht in eine heraufgestufte Kategorie verschieben.

1. Um eine Aktion oder eine Aktionsgruppe zu verschieben, ziehen Sie sie an die gewünschte Position, wie bei Feldern und Spalten.
2. Um eine Aktion oder eine Aktionsgruppe in eine andere leere Aktionsgruppe zu verschieben, ziehen Sie Aktion oder Aktionsgruppe in die neue Gruppe und lassen Sie sie im Feld **Aktion hier ablegen** fallen.


## <a name="personalizing-parts"></a><a name="Parts"></a>Personalisierung von Teilen

Teile sind Bereiche auf einer Seite, die in der Regel aus mehreren Feldern, Diagrammen oder anderen Inhalten bestehen und durch einen farbigen Rahmen gekennzeichnet sind, wenn der Fokus auf den Teil gesetzt wird. Beispielsweise besteht ein Startbildschirm des Rollenzentrums aus mehreren Teilen. Aufgrund ihrer klar definierten Grenzen können Sie sowohl den gesamten Teil als auch seinen Inhalt personalisieren.

- Um ein Teil zu verschieben, ziehen Sie es mit Drag & Drop an die gewünschte Position. Eine farbige Linie zeigt gültige Positionen auf dem Bildschirm an. Beispielsweise können Infofelder nur neben andere Infofelder im Infofelder-Fensterbereich verschoben werden.
- Sie können einen Teil ausblenden, indem Sie die Option **Ausblenden** unter dem Pfeil wählen.
- Wenn Sie mit der Personalisierung beginnen oder zu einer neuen Seite navigieren, werden alle Teile, die derzeit verborgen sind, auf der Seite mit einem unverwechselbaren Bildmaterial angezeigt, um darauf hinzuweisen, dass sie verborgen sind. Sie können diesen Teil einblenden, indem Sie die Option **Anzeigen** unter der Pfeilspitze wählen.

Sie können alle Personalisierungsänderungen, die Sie innerhalb eines einzelnen Teils vorgenommen haben, löschen, indem Sie die Aktion **Personalisierung löschen** unter der Pfeilspitze des Teils wählen. Die Freigabe der Personalisierung eines Teils wirkt sich nur auf Änderungen des Inhalts des Teils aus, nicht auf die Platzierung oder Sichtbarkeit des Teils auf der Seite.  


## <a name="to-clear-personalization"></a>So wird eine Personalisierung gelöscht
Deaktivieren Sie einige oder alle an dieser Seite im Lauf der Zeit vorgenommenen Personalisierungsänderungen.

1. Auf dem Banner **Personalisierung** wählen Sie die **Klare Personalisierung** Aktion.
2. Wählen Sie eine der folgenden Optionen aus. Beachten Sie, dass das Löschen der Personalisierung nicht rückgängig gemacht werden kann.

|Option|Was sie tut|
|------|------------
|**Nur Navigationsmenü**|Löscht alle Personalisierungsänderungen, die Sie am Navigationsmenü vorgenommen haben, das im Rollencenter und auf anderen Seiten freigegeben ist. Dies umfasst alle neuen Aktionen, die als Lesezeichen hinzugefügt wurden, sowie alle Änderungen an Links und Gruppen im Menü.|  
|**Nur Aktionen**|Löscht alle Personalisierungsänderungen, die Sie jemals an der Navigation oder den Aktionsleisten auf der Seite vorgenommen haben.|
|**Nur Felder, Spalten und Teile**|Löscht alle Personalisierungsänderungen, die Sie jemals an der Seite vorgenommen haben, mit Ausnahme der Änderungen an der Navigations- oder Aktionsleiste. Dies umfasst Änderungen an Feldern, Spalten, Teilen und Kacheln. |
|**Alle**|Löscht alle an dieser Seite vorgenommenen Personalisierungsänderungen, sodass die Seite wieder wie zuvor aussieht. Dazu gehören Änderungen an Navigations- und Aktionsleisten, Feldern, Spalten, Teilen und Kacheln.|

## <a name="additional-points-of-interest"></a>Zusätzliche Punkte von Interesse
Um die Personalisierung besser zu verstehen, finden Sie hier einige Hinweise.

- Wenn Sie Änderungen auf einer Kartenseite vornehmen, gelten die Änderungen für alle Datensätze, die Sie aus dieser Übersicht öffnen. Wenn Sie beispielsweise einen bestimmten Debitor aus der Debitorenlistenseite öffen und anschließend die Seite anpassen, indem Sie ein Feld hinzufügen. Wenn Sie andere Debitoren aus der Liste öffnen, wird das Feld, das Sie hinzugefügt haben, auch angezeigt.
- Änderungen, die Sie machen, treten in allen Ihren Rollencenter in Kraft. Wenn Sie beispielsweise eine Änderung auf der Seite **Debitoren** ändern, wenn das Rollencenter auf Geschäftsführer festgelegt ist, finden Sie auch die Änderung in der Debitorenübersicht, wenn das Rollencenter auf Verkaufsauftragsprozess festgelegt wurde.
- Änderungen an einer Seite in einem Bereich treten auf der Seite in Kraft, in der sie angezeigt werden.  
- Sie können Felder und Spalten von einer vordefinierten nur Liste hinzufügen, die auf der Seite sind. Sie können keine neuen Referenzen erstellen.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Merkmale angezeigt werden](ui-experiences.md)  
