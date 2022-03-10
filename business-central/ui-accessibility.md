---
title: Assistive Funktionen
description: Dieser Artikel enthält Informationen über Tastaturkürzel und andere unterstützende Funktionen in Business Central für Menschen mit Behinderungen.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, charts, tooltips, screen reader
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.date: 06/23/2021
ms.author: jswymer
ms.openlocfilehash: 6389387e2b2e9dcaa2d709e7e376f38a3dd8e1a9
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334564"
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Eingabehilfe und Tastenkombinationen

In diesem Artikel finden Sie Informationen zu den Funktionen, die [!INCLUDE[prod_short](includes/prod_short.md)] für Menschen mit Behinderungen leicht zugänglich machen. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die folgenden Funktionen:  

- Tastaturkurzbefehle. Siehe [Tastaturkurzbefehle](keyboard-shortcuts.md).
- Touch- und Stiftgesten auf Tablets und Telefonen. Siehe [Touch- und Stiftgesten](touch-gestures.md).
- Navigation  
- Überschrift  
- Alternativer Text für Bilder und Links  
- Unterstützung für allgemeine assistive Technologien 
- Vergrößern oder Verkleinern auf einer beliebigen Seite
- Tooltips auf Elementen in der Benutzeroberfläche

## <a name="navigation"></a><a name="Navigation"></a> Navigation
  
Sie können verschiedene Kombinationen der Tabulator-, Umschalt- und Pfeiltasten Ihrer Tastatur verwenden, um zwischen Elementen auf einer Seite zu wechseln. Zu den Elementen gehören Aktionen, Felder und Spalten, Teile und andere Steuerelemente. Allgemein gilt: Drücken Sie die Tabulatortaste oder Umschalt+Tab, um zum nächsten oder vorherigen Element zu wechseln.

Wenn Sie den Fokus auf einen Bereich legen, der Aktionen enthält, wie die Navigationsleiste oben im Rollencenter oder die Aktionsleiste auf anderen Seiten, verwenden Sie die Pfeiltasten, um sich durch die verschiedenen Aktionen und Gruppen zu bewegen. Drücken Sie die Eingabetaste bei einer Gruppe, um die darunter liegenden Aktionen zu öffnen, und fahren Sie dann mit den Pfeiltasten fort. Drücken Sie die Tabulatortaste oder Umschalt+Tab, um sich aus dem Aktionsbereich herauszubewegen.

Mit Hilfe der Tabulatorreihenfolge können Sie auch zwischen der Hauptseite des Browsers und Dialogfeldern, die z. B. eine Bestätigung anfordern, oder der Anmeldeseite wechseln.  

## <a name="headings-in-content"></a><a name="Headings"></a> Überschriften in Content

Die HTML-Quelle für den [!INCLUDE[prod_short](includes/prod_short.md)] Inhalt verwendet Tags, um Benutzern der assistive Technologie zu helfen, die Struktur und den Inhalt der Seite zu erkennen. So werden beispielsweise für Listenseiten die Spalten in den Spaltenüberschriften und die Kategorien festgelegt und werden mit TITEL-Aattribut innerhalb des Tags festgelegt. Caption für Elementen wie Felder, Infoboxen und Inforegister sind in den Überschriftstags enthalten (H1, H2, H3 und H4).  

## <a name="image-and-links"></a><a name="Images"></a> Bild und Links

Ein Text für Bilder wird mit dem ALT-Attribut innerhalb des IMG-Tags festgelegt. Ein beschreibender Text für Hyperlinks wird mit dem Titelattribut innerhalb des A-Tags festgelegt.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> Assistive Technologien

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene assistive Technologien, wie kontrastreiches, Sprachausgaben und Spracherkennungs-Software. Einige assistive Technologien funktionieren möglicherweise nicht mit bestimmten Elementen«» [!INCLUDE[prod_short](includes/prod_short.md)] in Seiten.  

## <a name="zoom"></a><a name="zoom"></a> Zoom

Die meisten Browser verwenden Standardtastenkürzel, um die aktuelle Seite zu vergrößern und zu verkleinern. Diese Tastenkombinationen sind nicht spezifisch für [!INCLUDE [prod_short](includes/prod_short.md)], aber sie funktionieren, wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] in einem Browser verwenden. Eine Liste der unterstützten Tastaturkürzel finden Sie unter [Tastaturkürzel zum Vergrößern und Verkleinern](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>QuickInfos

QuickInfos sind für die meisten Elemente der Benutzeroberfläche verfügbar, z. B. für Seitenfelder und Spalten, Aktionen, Kacheln und Diagramme. Eine QuickInfo bietet zusätzlichen Text, der ein Element erklärt, damit Sie seinen Zweck besser verstehen. 

Auf QuickInfos wird auf unterschiedliche Weise zugegriffen, je nach Client (Web oder Mobile) und dem Gerät, mit dem Sie arbeiten. Verwenden Sie die folgende Tabelle als Anleitung. Einige QuickInfos können von Bildschirmlesegeräten gelesen werden. In diesem Fall greifen Sie auf die QuickInfos wie in der Tabelle beschrieben zu und verwenden dann das Bildschirmlesegerät, um zu den QuickInfos zu navigieren, wie Sie es mit jedem anderen Element tun würden.

#### <a name="accessing-tooltips"></a>Zugriff auf Tooltips

|Element|Mausaktion für Web-Client|Tastaturkürzel für Web-Client|Touch-Geste auf Tablet/Telefon für Mobile-App|Unterstützung für Bildschirmleser|
|-------|-----------------|------------|--------------------------|---------------------|
|Seitenfelder und Spaltenüberschriften|Bewegen Sie den Mauszeiger über die Feldbeschriftung oder die Spaltenüberschrift oder klicken Sie darauf|Bewegen Sie den Fokus auf das Feld oder die Spaltenüberschrift und drücken Sie Alt+Pfeiltasten nach oben|Tippen Sie auf die Feldbeschriftung |ja|
|Diagrammelemente, wie ein Balken, eine Zeile, ein Kreissegment usw.|Bewegen Sie den Mauszeiger über das Element|Bewegen Sie den Fokus auf das Element, z. B. mit den Pfeiltasten|Tippen und halten Sie das Element|ja|
|Aktionen|Mit dem Mauszeiger über die Aktion fahren|keine|keine |keine|
|Cue-Kacheln|Bewegen Sie den Mauszeiger über die Kachel |keine|keine|keine|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>Weitere Zugriffsinformationen

Sie können zusätzliche Informationen über Eingabehilfen mit Microsoft-Produkten und assistiven Technologien der Site [Microsoft-Eingabehilfe](https://go.microsoft.com/fwlink/?LinkId=262160) finden.

## <a name="see-also"></a>Siehe auch

[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Häufig gestellte Fragen](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
