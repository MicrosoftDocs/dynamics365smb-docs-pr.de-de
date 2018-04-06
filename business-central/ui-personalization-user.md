---
title: Personalisieren von Seiten in Financials | Microsoft Docs
description: "Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen entspricht."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 64a41b5fbb3452c158c8f77b2f73b661b714522f
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="personalizing-your-workspace"></a>Personalisieren Ihres Arbeitsbereichs
<!--NAV in the Web client-->
Sie können Ihren Arbeitsbereich für Ihre Arbeit *personalisieren* oder anpassen und Präferenzen definieren, indem Sie die Seiten ändern, so dass Sie nur die Informationen angezeigt erhalten, die Sie benötigen. Die Personalisierungsänderungen, die Sie durchführen, beeinflussen nur, was Sie sehen, und nicht, was die Benutzer sehen.

Abhängig von der Art der Seite und was sie umfasst, können Sie:

-   Felder hinzufügen, bewegen und entfernen.
-   Spalten in einer Liste hinzufügen, verschieben und bewegen.
-   Ändern Sie die Fixierung von Spalten in der Liste. Dieser Bereich sperrt eine oder mehrere Spalten der linken Seite in einer Übersicht, sodass Sie immer vorhanden ist, auch Sie blättern.
-   Passen Sie die Breite der Spalten aus einer Liste.
-   Bewegen und entfernen Sie  Stapel (Kacheln).
-   Teile bewegen und entfernen. Die Teile sind Unterteilungen oder Regionen auf einer Seite, die Bedingungen wie mehrere Felder, eine andere Seite, Ein Diagramm oder Kacheln enthalten.  

## <a name="to-personalize-a-page"></a>So passen Sie eine Seite individuell an

1. In der rechten oberer Ecke wählen Sie ![Einstellungen](media/ui-experience/settings_icon_small.png "Symbol für Rollencenter einstellen") und dann **Personalisieren**.

    Das **Personalisieren** Banner erscheint oben und zeigt an, dass Sie mit den Änderungen beginnen können.

    ![Modus personalisieren](media/ui_personalize_mode_small.png "Modus personalisieren")

2.  Öffnen Sie die Seite, die Sie personalisieren möchten.

    Wenn Sie ein Schlosssymbol im Banner sehen, siehe [Warum die Seite gesperrt ist](ui-personalization-locked.md) für weitere Informationen.

3.  Zeigen Sie auf einen Bereich, den Sie anpassen möchten, beispielsweise ein Feld oder ein Spaltenüberschrift in einer Liste. Alles, was Sie anpassen können, wird gleichzeitig mit einem Pfeil oder einem Rahmen hervorgehoben.
<!--
    -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
    -   If the component is a part, the extent of the part is indicated by a border.
    -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
    -->

4.  Verwenden Sie diese Tabelle, die Ihnen hilft, Änderungen vorzunehmen:     <table>
        <tr><th>Was möchten Sie tun</td><th>So geht es</th></tr>
        <tr><td>Etwas verschieben, wie ein Feld, eine Spalte in der Liste, eine Kachel oder ein Teil</td><td> Zeigen Sie auf eine beliebige Stelle in, was Sie befördern möchten, und ziehen Sie sie im neuen Lagerort. Der Lagerort wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.</td></tr>
        <tr><td>Entfernen Sie etwas</td><td>Auswählen der Pfeilspitze und wählen Sie <b>auf Entfernen</b> aus. </td></tr>
        <tr><td>Hinzufügen eines Felds oder einer Spalte</td><td>Im Banner<b>Personalisieren</b> wählen Sie <b>mehr</b> und wählen Sie das <b>Feld</b> aus.<br /></br>Der Berecih <b>Feld oder Seite hinzufügen</b> wird geöffnet auf der rechten Seite. Es führt die Felder auf, die Sie auf der Seite hinzufügen können. Die Felder, die als <b>Platziert</b> gekennzeichnet werden, sind bereits auf der Seite. Die Felder, die als <b>Bereit</b> gekennzeichnet werden, sind nocht nicht auf der Seite.<br /></br>Um ein Feld hinzuzufügen, ziehen Sie es aus dem Bereich an den gewünschten Ort. Der Lagerort wird entweder mit einer horizontalen oder einer vertikalen Zeile angegeben.</td></tr>
        <tr><td>Ändern Sie die Fixierung von Spalten in der Liste.</td><td>Wählen Sie die Spalte der Pfeilspitze, die Sie als letzte Spalte der Fixierung möchten, und wählen Sie dann <b>Fixierung einstellen</b> aus.<br /><br/>Wenn Sie die Fixierung wieder am ursprünglichen Ort wünschen, wählen Sie die Pfeilspitze für die aktuelle Fixierung und wählen Sie <b>Fixierung löschebn</b> aus. Hinweis: Sie können die ursprüngliche Fixierung nicht entfernen.</td></tr>
        <tr><td>Ändern der Breite einer Spalte</td><td>In der Tabellenkopfzeile ziehen Sie den rechten Rand der Spalte. <br /><br />Um die Spaltenbreite zu maximieren, um die längste Textzeile in der Spalte anzupassen, doppelklicken Sie auf den rechten Rand.</td></tr>
      </table>

    > [!IMPORTANT]  
    >   Sie können Änderungen an einer Übersicht nicht ändern, wenn die Liste als Kacheln angezeigt wird. Sie müssen zuerst die Seite wechseln und zur Listenansicht gehen, indem Sie ![Als Liste anzeigen](media/ui_show_as_list_icon.png "Anzeigen als Listenpfeil") auswählen.

5.  Sie können fortfahren, um Änderungen auf derselben Seite vorzunehmen oder auf eine andere Seite zu verschieben. Ihre Änderungen werden automatisch gespeichert, während Sie diese erstellen. Wenn Sie im Fenster **Personalisieren** Banner fertig sind, wählen Sie **Erledigt** aus.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"></a>Löschen Sie die Personalisierung, um eine Seite oder im ursprünglichen Layout zu ändern
Deaktivieren Sie alle an dieser Seite im Lauf der Zeit vorgenommenen Personalisierungsänderungen, sodass die Seite wieder wie vorher aussieht Um dies zu tun, wählen Sie **Personalisieren** und **Mehr** und dann **Personalisierung löschen**.

## <a name="personalization-in-detail"></a>Personalisierung im Detail
Um die Personalisierung besser zu verstehen, finden Sie hier einige Hinweise.  
-   Wenn Sie Änderungen auf einer Kartenseite vornehmen, gelten die Änderungen für alle Datensätze, die Sie aus dieser Übersicht öffnen. Wenn Sie beispielsweise einen bestimmten Debitor aus der Debitorenlistenseite öffen und anschließend die Seite anpassen, indem Sie ein Feld hinzufügen. Wenn Sie andere Debitoren aus der Liste öffnen, wird das Feld, das Sie hinzugefügt haben, auch angezeigt.
-   Änderungen, die Sie machen, treten in allen Ihren Rollencenter in Kraft. Wenn Sie beispielsweise eine Änderung in der Liste der Debitoren ändern, wenn das Rollencenter auf Geschäftsführer festgelegt ist, finden Sie auch die Änderung in der Debitorenübersicht, wenn das Rollencenter auf Verkaufsauftragsprozess festgelegt wurde.
-   Änderungen an einer Seite in einem Bereich treten auf der Seite in Kraft, in der sie angezeigt werden.  
-   Sie können Felder und Spalten von einer vordefinierten nur Liste hinzufügen, die auf der Seite sind. Sie können keine neuen Referenzen erstellen.

## <a name="see-also"></a>Siehe auch
[Verwalten der Personalisierung](ui-personalization-manage.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Anpassen der [!INCLUDE[d365fin](includes/d365fin_md.md)] Erfahrung](ui-experiences.md)  

