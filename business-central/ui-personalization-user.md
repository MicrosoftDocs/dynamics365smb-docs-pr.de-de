---
title: Personalisierte Seiten (enthält ein Video)
description: 'Hier erfahren Sie, wie Sie die Benutzeroberfläche anpassen und Ihren Arbeitsbereich in Business Central an Ihre Arbeitsweise und persönlichen Vorlieben anpassen können.'
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 12/05/2023
ms.author: jswymer
---
# Arbeitsbereich personalisieren

Sie können ihren Arbeitsbereich an Ihre Arbeit und Ihre Bedürfnisse anpassen. Ändern Sie die Seiten so, dass sie nur die Informationen anzeigen, die Sie benötigen, wo Sie sie benötigen. Personalisierung wirkt sich nur auf den Arbeitsbereich aus. Es ändert nichts daran, wie andere arbeiten. Sie können alle Typen von Seiten personalisieren, einschließlich der Seite [Rollencenter](ui-change-basic-settings.md#role-center).

> [!NOTE]
> Aufgrund von Einschränkungen der Designfunktionen im Webclient ist es derzeit nicht möglich, die Steuerelemente innerhalb der Rastersyntax anzupassen oder zu personalisieren.
Dies gilt für alle Designmodi, nicht nur für die Personalisierung.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Sie können verschiedene Änderungen vornehmen, z. B. Verschieben und Ausblenden von Feldern, Spalten,Aktionen oder Verschieben und Ausblendern ganzer Teile und mehr. Die meisten Personalisierungen müssen vorgenommen werden, indem zuerst das Banner **Personalisierung** aktiviert wird. Einfache Anpassungen, wie z. B. die Spaltenbreite, können Sie sofort an jeder Liste vornehmen.

> [!NOTE]
> Administratoren können dieselben Layoutänderungen wie Benutzer durchführen, indem sie Profil (Rolle) anpassen, dem mehrere Benutzer zugewiesen sind. Um mehr über Seiten für Rollen zu erfahren, gehen Sie zu [Seiten für Rollen anpassen](ui-personalization-manage.md)<br /><br />
Administratoren können auch Personalisierungen der Benutzer überschreiben und definieren, welche Funktionen in allen oder bestimmten Unternehmen zugänglich sind. Weitere Informationen finden Sie unter [Anpassen von Business Central](ui-customizing-overview.md).

## Video

Das folgende Video zeigt einige Möglichkeiten, wie Sie Ihr Rollencenter personalisieren können.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## Ändern der Breite einer Spalte

Sie können die Größe der Spalten in jeder Liste einfach ändern. Ziehen Sie einfach die Grenze zwischen zwei Spalten nach links oder rechts.  

1. Ziehen Sie im Kopf einer Liste die Grenze zwischen zwei Spalten.
2. Alternativ können Sie auch auf die Grenze zwischen zwei Spalten doppelklicken, um die Breite der Spalte automatisch anzupassen. Anhand der Breite wird die für die Lesbarkeit optimale Größe eingestellt.

Wie bei anderen Personalisierungen werden die Änderungen, die Sie an der Spaltenbreite vornehmen, in Ihrem Konto gespeichert und folgen Ihnen, unabhängig davon, auf welchem Gerät Sie sich anmelden.

## Beginnen Sie mit der Personalisierung, indem Sie den Personalisierungsmodus verwenden

1. Öffnen Sie eine beliebige Seite, die Sie personalisieren möchten.
1. Wählen Sie in der oberen rechten Ecke das Symbol ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollencenter") Symbol, und wählen Sie dann die Aktion **Personalisieren**.

    Das **Personalisieren** Banner erscheint oben und zeigt an, dass Sie mit den Änderungen beginnen können.

    > [!NOTE]
    > Um während der Personalisierung zu navigieren, verwenden Sie <kbd>Strg</kbd>+<kbd>Klicken<kbd> auf eine Aktion, wenn diese durch die Pfeilspitze hervorgehoben ist.

    Wenn Sie im Banner ein ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") oder ![Personalisieren blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") auf dem Banner sehen, können Sie die Seite nicht personalisieren. Weitere Informationen finden Sie unter [Warum eine Seite für die Personalisierung gesperrt ist](ui-personalization-locked.md).

1. Zeigen Sie zum Ändern eines Oberflächenelements auf das Element, z. B. eine Aktion, ein Feld oder einen Teil. Das Element wird sofort mit einer Pfeilspitze oder einem Rand hervorgehoben. Wählen Sie das Element aus und wählen Sie dann eine der beiden Optionen **Bewegung**, **Entfernen**, **Verbergen, verstecken**, **Anzeigen**, **Anzeigen unter mehr anzeigen**, **Anzeigen, wenn alle verborgen**, **Immer anzeigen**, **Einfrierfenster einstellen/löschen**, oder **Schnelleingabe einschließen/ausschließen**, abhängig vom T und Status des Oberflächenelements.
1. Um ein Feld hinzuzufügen, wählen Sie die **+ Feld** Aktion. Von dem Bereich **Feld zu Seite hinzufügen** ziehen Sie ein Feld per Drag und Drop an die gewünschte Position auf der Seite.
1. Wenn Sie das Layout einer oder mehrerer Seiten geändert haben, wählen Sie die Schaltfläche **Fertig** im Banner **Personalisierung**.

Weitere Informationen finden Sie unter [Was Sie personalisieren können](#What).

## <a name="What"></a>Was Sie personalisieren können

|Was möchten Sie tun|So geht es|Bemerkungen|
|----|------------|-------|
|Etwas verschieben, wie ein Feld, eine Spalte in der Liste, eine Kachel, Aktion oder ein Teil an eine andere Stelle auf der Seite|Zeigen Sie auf eine beliebige Stelle, was Sie verschieben möchten, und ziehen Sie sie an die neue Position. Eine dicke horizontale oder vertikale Linie gibt die Position an.<br /><br />![Symbol „Kann nicht hierher verschoben werden“](media/personalization-cannot-move-here.png "Personalisierungsmodus – Symbol „Kann nicht verschoben werden“") gibt an, dass Sie das Element nicht an den ausgewählten Standort verschieben können.|Die Teile sind Unterteilungen oder Regionen auf einer Seite, die Bedingungen wie mehrere Felder, eine andere Seite, Ein Diagramm oder Kacheln enthalten.<br /><br />[Erfahren Sie mehr über die Personalisierung von Aktionen](#Actions)<br>[Erfahren Sie mehr über die Personalisierung von Teilen](#Parts)|
|Blenden Sie ein aktuell angezeigtes Element aus, z. B. ein Feld, eine Spalte in einer Liste, eine Kachel, eine Aktion oder einen Teil.|Wählen Sie das Element, die Pfeilspitze und dann <b>Ausblenden</b> aus.|Im Personalisierungsmodus werden ausgeblendete Aktionen durch kursiven Text ausgegraut und ausgeblendete Teile durch diagonale Linien schattiert. Ausgeblendete Felder und Spalten werden auf der Seite nicht angezeigt. <!--The element is grayed when you are in personalizing mode.--> Wenn Sie den Personalisierungsmodus verlassen, verschwinden alle Elemente aus der Ansicht. Wenn das Feld, das Sie ausblenden, auch in der Inforegisterüberschrift angezeigt wird, wenn das Inforegister reduziert ist, wird das Feld dort nicht länger angezeigt.|
|Zeigen Sie eine Aktion oder einen Teil an, der derzeit ausgeblendet ist|Wählen Sie für ein graues (ausgeblendetes) Element die Pfeilspitze und dann <b>Anzeigen</b>.|Das versteckte Element ist wieder sichtbar.|
|Ein Feld anzeigen, das derzeit ausgeblendet ist|In dem <b>Personalisierung</b> Banner, wählen Sie die <b>+ Feld</b> Aktion.<br /></br>Der Bereich <b>Feld zur Seite hinzufügen</b> wird rechts auf der Seite geöffnet. Wenn Sie ein Feld im Bereich auswählen, wird seine verborgene Position auf der Seite angezeigt.<br /><br />Um ein Feld anzuzeigen, ziehen Sie es aus dem Bereich oder der ausgeblendeten Position an den gewünschten Ort. Die Position wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.<br><br> Eine andere Möglichkeit besteht darin, die Pfeilspitze an der verborgenen Position des Felds auszuwählen und **Anzeigen** auszuwählen. |Jede Seite enthält einen vordefinierten Satz von Feldern, die Sie zur Anzeige auswählen können.<br /><br />[Weitere Informationen zu Arbeitsfeldern](#fields) |
|Zeigen Sie ein Feld in der Überschrift eines Inforegisters an, wenn es reduziert ist.|Wählen Sie die Pfeilspitze aus und dann wählen Sie <b>Bei Reduzierung anzeigen</b> aus. <br /> <br />Wenn Sie diese Option nicht finden, ist sie bereits festgelegt. In diesem Fall wählen Sie <b>Immer anzeigen</b> auf dem Inforegister aus, damit das Feld nicht mehr in der Inforegisterüberschrift angezeigt wird.|*Inforegister* ist der Begriff, der für eine Gruppe von Feldern verwendet wird, die unter einer gemeinsamen Überschrift angezeigt werden. Verwenden Sie <b>Bei Reduzierung anzeigen</b>-Option, um die wichtigsten Felder anzuzeigen. Wenn Sie ein Feld in der Überschrift auswählen, wird das Inforegister mit Fokus auf dem ausgewählten Feld geöffnet.<br /><br />Diese Option wird nur angewendet, wenn eine Seite mehr als ein Inforegister hat. Wenn nur ein Inforegister da ist, kann es nicht reduziert werden, sodass die Option <b>Bei Reduzierung anzeigen</b> nicht verfügbar ist.|
|Lassen Sie ein Feld anzeigen, wenn Sie **Mehr anzeigen** auswählen.|Wählen Sie die Pfeilspitze aus und wählen Sie dann <b>Unter „Mehr anzeigen“ anzeigen</b> aus.|Wenn Sie die Option <b>Unter „Mehr anzeigen“ anzeigen</b> nicht sehen, ist das Feld bereits festgelegt. Wenn Sie in diesem Fall ein Feld immer anzeigen lassen möchten, und nicht nur, wenn Sie **Mehr anzeigen** auswählen, wählen Sie <b>Immer anzeigen</b> aus.|
|Ändern Sie, ob ein Feld bearbeitet werden kann oder nicht.|Wählen Sie das Feld aus, wählen Sie die Pfeilspitze auf dem Feld aus und wählen Sie dann <b>Bearbeitung sperren</b> aus, um zu verhindern, dass der Feldwert geändert wird, oder <b>Bearbeitung entsperren</b>, um das Ändern des Feldwerts zu ermöglichen.|Sie können nur Felder entsperren, die Sie zuvor selbst gesperrt haben. Einige Felder sind standardmäßig gesperrt, entweder absichtlich oder durch einen Profiladministrator, der [die Seite angepasst hat](ui-personalization-manage.md). Diese Felder können nicht entsperrt werden.|
|Ändern Sie die Fixierung von Spalten in der Liste. |Wählen Sie nun die Spalte der Pfeilspitze, die Sie als letzte Spalte der Fixierung möchten, und wählen Sie dann <b>Fixierung einstellen</b> aus.<br /><br/>Wenn Sie die Fixierung wieder am ursprünglichen Ort wünschen, wählen Sie die Pfeilspitze für die aktuelle Fixierung und wählen Sie dann <b>Fixierung löschen</b> aus. Hinweis: Sie können die ursprüngliche Fixierung nicht entfernen.|Der Fixierungsbereich gibt die Spalten an, die immer links in der Liste erscheinen, auch wenn Sie horizontal blättern.|  
|Überspringen Sie ein Feld, wenn die EINGABETASTE gedrückt wird.|Wählen Sie die Pfeilspitze neben dem Feld oder der Spaltenüberschrift in der Liste aus, und wählen Sie dann **Von der Schnelleingabe ausschließen** aus.  | Wenn Sie **Von der Schnelleingabe ausschließen** nicht sehen, wird das Feld bereits übersprungen. Wenn Sie in diesem Fall Überspringen des Felds beenden möchten, wählen Sie **In Schnelleingabe einbeziehen** aus.<br><br>[Weitere Informationen zur Schnelleingabe](ui-enter-data.md#QuickEntry)|
|Ordnen und entfernen Sie Ansichten, die gefilterte Listen darstellen.|Klicken Sie auf die Pfeilspitze neben einer Ansicht und wählen Sie dann **Verschieben**, **Entfernen**, oder **Verbergen**.|[Weitere Informationen zum Personalisieren von Listenansichten](ui-views.md)|  
|Fügen Sie einer Seite oder einem Bericht in Ihrem Role Center eine neue Aktion hinzu.|Wählen Sie das Lesezeichensymbol auf der Zielseite, auf der Berichtsanforderungsseite oder im Fenster „Wie möchten Sie weiter verfahren“ aus.|[Weitere Informationen zum Setzen von Lesezeichen für Seiten und Berichte](ui-bookmarks.md)|
|Listen immer erweitert oder reduziert anzeigen|Wählen Sie in der oberen linken Ecke der Liste die Schaltfläche **Alle erweitern** oder **Alle reduzieren** aus. Sie können auch die Aktion **Alle erweitern** oder **Alle reduzieren** im Menü der ersten Spalte auswählen. |Gilt für reduzierbare Hierarchielisten|

## <a name="Actions"></a>Aktionsleiste und Menüs personalisieren

Mit der Personalisierung können Sie entscheiden, welche Aktionen auf den Navigations- und Aktionsleisten und in den Rollenzentren angezeigt werden sollen und wo sie angezeigt werden sollen. Sie können einzelne Aktionen oder Aktionsgruppen ausblenden, anzeigen oder verschieben.

Das folgende Video zeigt, wie Sie Aktionen auf Seiten und Rollencentern personalisieren können.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

Die Personalisierung der Navigations- und Aktionsleisten erfolgt im Wesentlichen auf die gleiche Weise wie bei anderen UI-Elementen. Allerdings hängen die Möglichkeiten einer Aktion oder Gruppe von der Position der Aktion oder der Gruppe auf der Aktionsleiste ab. Die beste Methode dies herauszufinden ist, es einfach auszuprobieren und sich von den Pfeilen führen zu lassen.

Es gibt einige Bedingungen, mit denen Sie vertraut sein sollten, um die Aktionsanpassung besser zu verstehen: *Aktionsgruppe* und *Heraufgestufte Kategorie*.  

Eine *Aktionsgruppe* ist ein Element, das sich erweitert, um weitere Aktionen oder Gruppen anzuzeigen. Auf der Seite **Verkaufsaufträge** ist beispielsweise eine Aktionsgruppe die Aktion **Funktionen**, die bei Auswahl der Aktion **Aktionen** angezeigt wird.

Eine *Heraufgestufte Kategorie* ist eine Aktionsgruppe, die vor der senkrechten Linie `|` auf der Befehlsleiste erscheint. Die Kategorien enthalten normalerweise die am häufigsten verwendeten Aktionen, sodass Sie sie schnell finden können. Zum Beispiel auf der **Kundenaufträge** Seite sind die Aktionen **Bestellung**, **Freisetzung** und **Buchungen** heraufgestufte Kategorien.

> [!NOTE]  
> Um die Personalisierung zu löschen, wählen Sie den Pfeil, der das Designermenü des Teils umgibt, und dann **Personalisierung löschen** aus.

### Aktionen und Aktionsgruppen entfernen, ausblenden und anzeigen

Wenn Sie eine Aktion ein- oder ausblenden möchten, definieren die Optionen unter der Pfeilspitze, was je nach Status der Aktion geschehen kann. 

1. Wählen Sie die Pfeilspitze für eine Aktion oder Aktionsgruppe aus.
2. Wählen Sie eine der folgenden Optionen aus:

|Option|Was sie tut|
|------|------------
|**Löschen**|Diese Option wird angezeigt, wenn die ausgewählte Aktion auch an anderer Stelle in der Navigations- oder Aktionsleiste angezeigt wird. Wird diese Option ausgewählt, wird die Aktion aus dem ausgewählten Standort gelöscht, sodass sie nicht mehr angezeigt wird. Die Aktion oder Aktionsgruppe bleibt am anderen Standort. |
|**Ausblenden**|Diese Option wird angezeigt, wenn sich die Aktion oder Aktionsgruppe nicht an anderer Stelle in der Navigationsleiste oder Aktionsleiste befindet. Wie **Entfernen** führt die Auswahl dieser Option dazu, dass die Aktion oder Aktionsgruppe aus der Navigations- oder Aktionsleiste verschwindet. Im Personalisierungsmodus wird die Aktion oder die Aktionsgruppe allerdings noch an der aktuellen Stelle angezeigt, aber abgedunkelt.|
|**Anzeigen**|Diese Option wird angezeigt, wenn die Aktion oder Aktionsgruppe zuvor ausgeblendet wurde (abgedunkelt). Wenn Sie diese Option wählen, erscheint die Aktion oder Aktionsgruppe in der Navigationsleiste oder der Aktionsleiste.|

### Aktionen und Aktionsgruppen verschieben

Stellen, an denen Sie Aktionen oder Aktionsgruppen ablegen können, wird durch eine horizontale Linie zwischen zwei Aktionen oder einem Rand um eine Aktionsgruppe angegeben. Folgende Beschränkungen gelten:

- Sie können einzelne Aktionen in die heraufgestuften Kategorien verschieben, aber Sie können die Reihenfolge der Aktionen in der Kategorie nicht neu anordnen.
- Sie können eine Aktionsgruppe nicht in eine heraufgestufte Kategorie verschieben.

1. Um eine Aktion oder eine Aktionsgruppe zu verschieben, ziehen Sie sie an die gewünschte Position, wie bei Feldern und Spalten.
2. Um eine Aktion oder eine Aktionsgruppe in eine andere leere Aktionsgruppe zu verschieben, ziehen Sie Aktion oder Aktionsgruppe in die neue Gruppe und lassen Sie sie im Feld **Aktion hier ablegen** fallen.

### Über das Automatisieren-Menü

- Sie können das Menü **Automatisieren** oder das Untermenü **Power Automate** und seine Aktionen nicht ausblenden oder verschieben.
- Sie können Flows, die unter dem Element **Automatisieren** enthalten sind, verschieben, aber Sie können sie nicht über die Personalisierung ausblenden. Durch das Verschieben des Flows wird der Flow an den Zielort kopiert, er wird jedoch nicht aus dem Element **Automatisieren** entfernt.

> [!TIP]
> Als Administrator können Sie das Element **Automatisierung** vor den Benutzern verbergen. Mehr dazu erfahren Sie unter [Einrichten der Power Automate Integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="Parts"></a>Personalisierung von Teilen

Zeigen Sie auf <kbd>ALT</kbd>+<kbd>NACH-OBEN-TASTE</kbd> oder wählen Sie es aus. Teile sind Bereiche auf einer Seite, die in der Regel aus mehreren Feldern, Diagrammen oder anderen Inhalten bestehen. Ein Teil zeigt einen farbigen Rahmen, wenn Sie den Fokus auf den Teil legen. Beispielsweise besteht ein Startbildschirm des Rollenzentrums aus mehreren Teilen. Aufgrund ihrer klar definierten Grenzen können Sie den gesamten Teil und dessen Inhalt personalisieren.

- Um ein Teil zu verschieben, ziehen Sie es mit Drag und Drop an die gewünschte Position. Eine farbige Linie zeigt gültige Positionen auf dem Bildschirm an. Beispielsweise können Infofelder nur neben andere Infofelder im Infofelder-Fensterbereich verschoben werden.
- Sie können einen Teil ausblenden, indem Sie die Option **Ausblenden** unter dem Pfeil wählen.
- Wenn Sie mit der Personalisierung beginnen oder zu einer neuen Seite navigieren, werden alle Teile, die derzeit verborgen sind, auf der Seite mit einem unverwechselbaren Bildmaterial angezeigt, um darauf hinzuweisen, dass sie verborgen sind. Sie können diesen Teil einblenden, indem Sie die Option **Anzeigen** unter der Pfeilspitze wählen.

Sie können alle Personalisierungsänderungen, die Sie innerhalb eines einzelnen Teils vorgenommen haben, löschen, indem Sie die Aktion **Personalisierung löschen** unter der Pfeilspitze des Teils wählen. Die Freigabe der Personalisierung eines Teils wirkt sich nur auf Änderungen des Inhalts des Teils aus, nicht auf die Platzierung oder Sichtbarkeit des Teils auf der Seite.  

## <a name="fields"></a> Mit Feldern und Spalten arbeiten

Wenn Sie eine Seite personalisieren, verwenden Sie den Bereich **Feld zur Seite hinzufügen**, um Felder anzuzeigen, die derzeit auf der Seite ausgeblendet sind. Sie öffnen diesen Bereich, indem Sie oben auf der Seite die Aktion **+ Feld** auswählen. Im Gegensatz zu anderen Elementen werden ausgeblendete Felder im Personalisierungsmodus nicht auf der Seite selbst angezeigt. Sie können jedoch ausgeblendete Felder identifizieren, indem Sie den Bereich **Feld zur Seite hinzufügen** verwenden.

Um die Arbeit mit Feldern zu vereinfachen, finden Sie hier einige allgemeine Richtlinien, die Sie bei der Verwendung des Bereichs **Feld zur Seite hinzufügen** befolgen sollten:

- Standardmäßig werden im Bereich alle ausgeblendeten Felder aufgelistet, die durch das Symbol [Zeigt das Symbol für ausgeblendete Felder](media/hidden-icon.png "Zeigt das Symbol für ausgeblendete Felder an") gekennzeichnet sind.
- Sie können die Liste filtern und andere Felder anzeigen, beispielsweise die aktuell auf der Seite angezeigten, indem Sie über der Liste die Schaltfläche **Empfohlene Felder** auswählen und eine Filteroption auswählen. Der Name der Schaltfläche ändert sich je nach der von Ihnen gewählten Filteroption.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Zeigt die Filterschaltfläche im Bereich „Ein Feld hinzufügen“ im Personalisierungsmodus an.":::
- Wenn Sie ein Feld in der Liste auswählen, wird seine Position auf der Seite hervorgehoben. Wenn das Feld derzeit ausgeblendet ist, wird seine geplante Position schattiert angezeigt. 
- Um weitere Details zu einem Feld in der Liste zu erhalten, zeigen Sie darauf oder wählen Sie <kbd>ALT</kbd>+<kbd>NACH-OBEN-TASTE</kbd> aus, um einen Tooltip anzuzeigen.
- Die im Bereich „Feld zur Seite hinzufügen“ verfügbaren Felder werden vom Entwickler der Seite und ihrer Quelltabelle oder von einem Profiladministrator bestimmt, der [die Seite angepasst hat](ui-personalization-manage.md). Sie können keine neuen Referenzen erstellen.
- Einige Seiten verfügen über mehrere Seitenfelder, die derselben Quelltabelle zugeordnet sind. Im Bereich werden beide bzw. alle dieser Seitenfelder unabhängig voneinander angezeigt. Das Ein-/Ausblenden/Verschieben dieser Felder erfolgt ebenfalls unabhängig voneinander, ohne dass sich das eine auf das andere auswirkt.


### Machen Sie ein ausgeblendetes Feld sichtbar

Es gibt zwei Möglichkeiten, ein Feld anzuzeigen, das derzeit auf der Seite ausgeblendet ist:

- Ziehen Sie das Feld an die gewünschte Position. Der Zielort wird mit einer dicken horizontalen oder vertikalen Linie angegeben.
- Wählen Sie das Feld in der Liste aus, gehen Sie dann zum schattierten Feld auf der Seite und wählen Sie die Option **Anzeigen** aus.

## Personalisierung löschen

Deaktivieren Sie einige oder alle an dieser Seite im Lauf der Zeit vorgenommenen Personalisierungsänderungen.

1. Auf dem Banner **Personalisierung** wählen Sie die **Klare Personalisierung** Aktion.
2. Wählen Sie eine der folgenden Optionen aus.  

> [!CAUTION]
> Das Löschen der Personalisierung kann nicht rückgängig gemacht werden.

|Option|Was sie tut|
|------|------------
|**Nur Navigationsmenü**|Löscht alle Personalisierungsänderungen, die Sie am Navigationsmenü vorgenommen haben, das im Rollencenter und auf anderen Seiten freigegeben ist. Zu diesen Änderungen zählen alle neuen Aktionen, die als Lesezeichen hinzugefügt wurden, sowie alle Änderungen an Links und Gruppen im Menü.|  
|**Nur Aktionen**|Löscht alle Personalisierungsänderungen, die Sie jemals an der Navigation oder den Aktionsleisten auf der Seite vorgenommen haben.|
|**Nur Felder und Spalten**|Löscht alle Personalisierungsänderungen, die Sie jemals an der Seite vorgenommen haben, mit Ausnahme der Änderungen an der Navigations- oder Aktionsleiste. Hierzu zählen beispielsweise Änderungen an Feldern, Spalten, Teilen und Kacheln. |
|**Alle**|Löscht alle an dieser Seite vorgenommenen Personalisierungsänderungen, sodass die Seite wieder wie zuvor aussieht. Hierzu zählen beispielsweise Änderungen an Navigations- und Aktionsleisten, Feldern, Spalten, Teilen und Kacheln.|

## Tipps und andere Punkte von Interesse

Um die Personalisierung besser zu verstehen, finden Sie hier einige Hinweise.

- Wenn Sie Änderungen an einer Kartenseite vornehmen, die Sie aus einer Liste öffnen, gelten die Änderungen für alle Datensätze, die Sie aus dieser Liste öffnen. Wenn Sie beispielsweise einen bestimmten Debitor aus der Debitorenlistenseite öffen und anschließend die Seite anpassen, indem Sie ein Feld hinzufügen. Wenn Sie andere Debitoren aus der Liste öffnen, wird das Feld, das Sie hinzugefügt haben, auch angezeigt.
- Änderungen, die Sie machen, betreffen alle Ihre Rollencenter. Wenn Sie beispielsweise eine Änderung an der „Debitoren“-Liste vornehmen, wenn das Rollencenter auf „Geschäftsführer“ festgelegt ist, sehen Sie die Änderung auch auf der **Debitoren**-Seite, wenn das Rollencenter auf „Verkaufsauftragverarbeitung“ festgelegt ist.
- Änderungen an einer Seite in einem Bereich treten auf der Seite in Kraft, in der sie angezeigt werden.  
- Sie können eine Seite nicht personalisieren, die im [Analysemodus](analysis-mode.md) ist. Der Schalter **Analysieren** ist deaktiviert. Sollten Sie versuchen, in den Personalisierungsmodus zu wechseln, während sich die Seite im Analysemodus befindet, wird der Analysemodus automatisch ausgeschaltet. 
- Einige Seiten verfügen über mehrere Seitenfelder, die derselben Quelltabelle zugeordnet sind. Im Bereich werden beide bzw. alle dieser Seitenfelder unabhängig voneinander angezeigt. Das Ein-/Ausblenden/Verschieben dieser Felder erfolgt ebenfalls unabhängig voneinander, ohne dass sich das eine auf das andere auswirkt.
- Wenn ein Teil oder eine Gruppe ausgeblendet ist, werden weiterhin Geisterfelder darin angezeigt, aber Sie können dieses Feld nicht per Drag und Drop verschieben oder hinzufügen/anzeigen, bis Sie die Gruppe/den Teil sichtbar gemacht haben.


## Siehe auch
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Grundlegende Einstellungen ändern](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
