---
title: Betrachtungs- und Bearbeitung grundlegender Einstellungen in Financials| Microsoft Docs
description: Erfahren Sie, wie Sie mehrere grundlegenden Einstellungen in Financials einrichten, zum Beispiel im Rollencenter, im Unternehmen oder im Arbeitsdatum.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f71b0e7d53138be0f89abe4e7935ab7c21437d8e
ms.contentlocale: de-de
ms.lasthandoff: 05/28/2018

---
# <a name="changing-basic-settings"></a>Ändern von grundlegenden Einstellungen
Im Fenster **Meine Einstellungen** können Sie grundlegende Einstellungen für [!INCLUDE[d365fin](includes/d365fin_md.md)] ansehen und ändern. Änderungen, die Sie durchführen, betreffen nur den Arbeitsbereich; nicht die Arbeitsbereiche anderer Benutzer.  

## <a name="role-center"></a>Rollencenter
Das Rollencenter erstellt die Homepage, eine Startseite, die für die Anforderungen der Rolle entworfen wurde. Abhängig von der Rolle gibt das Rollencenter Ihnen einen Überblick über das Unternehmen, Ihre Abteilung oder Ihre persönlichen Aufgaben. Es hilft Ihnen auch, zu Ihren Tagewerken zu navigieren und Arbeit zu finden, die Ihnen zugeordnet wird.

-   Oben erlaubt es Ihnen die Navigation, zwischen Debitoren, Kreditoren, Artikeln sowie anderen wichtigen Listen von Informationen zu wechseln. Ebenso können Sie Aufgaben einleiten, wie eine neue Verkaufsrechnung direkt im Rollencenter zu erstellen.

-   Im Mittelpunkt finden Sie die Kacheln **Aktivitäten**. Aktivitäten zeigen aktuelle Daten an und können geklickt werden oder getippt werden, um detailliertere Informationen anzuzeigen. Die zentralen Leistungs-Indikatoren können eingerichtet werden, um ein ausgewähltes Diagramm für eine visuelle Darstellung anzuzeigen, zum Beispiel, Cashflow oder Einnahmen und Ausgaben. Sie können eine Liste von Lieblingsdebitoren auf der Homepage auch für Konten einrichten, mit denen Sie häufig Geschäfte tätigen oder besondere Aufmerksamkeit geben müssen.

### <a name="to-change-role-center"></a>So ändern Sie ein Rollencenter
Das Standardrollencenter ist der **Geschäftsführer**, aber Sie können ein anderes Rollencenter auswählen, das mit den Anforderungen besser übereinstimmt.
1. In der oberen rechter Ecke wählen Sie das Symbol **Einstellungen** aus ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol Rollencenter") und dann **Meine Einstellungen**.
2. Wählen Sie im Fenster **Meine Einstellungen** im Feld **Rollencenter** das Rollencenter aus, das Sie als Standard festlegen möchten. Wählen Sie beispielsweise **Buchhalter/in** aus.
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="company"></a>Unternehmen
Ein Unternehmen dient als Container für Daten im Project [!INCLUDE[d365fin](includes/d365fin_md.md)] Es kann mehrere Unternehmen in einer Datenbank geben, aber nur eine kann gleichzeitig ausgewählt werden.

Der Standardmandant wird CRONUS bezeichnet und enthält nur Demodaten enthält.

> [!TIP]  
>   Wenn Sie einen anderen Namen des Mandanten in der Anwendung anzeigen möchten (z. B. im Rollencenter), legen Sie das Feld **Name** auf der Seite **Firmendaten** oder das Feld **Anzeigename** auf der Seite **Unternehmen** fest.  

## <a name="work-date"></a>Arbeitsdatum
Standardmäßig wird das aktuelle Datum (Systemdatum) verwendet. Um Aufgaben wie das Abschließen von Transaktionen für ein Datum auszuführen, das nicht das aktuelle Datum ist, müssen Sie möglicherweise vorübergehend das Arbeitsdatum ändern.

> [!TIP]  
>   Tippen Sie **W** um rasch das Arbeitsdatum in ein Datumsfeld einzugeben. Schreiben Sie **T**, um rasch das aktuelle Datum in ein Datumsfeld einzugeben.

> [!IMPORTANT]  
>   Das Arbeitsdatum wird nur geändert, bis Sie den Mandanten schließen, oder bis das Datum sich ändert. Wenn Sie am nächsten Tag einen anderen oder denselben Mandanten öffnen und ein anderes Arbeitsdatum verwenden müssen, dann müssen Sie das Arbeitsdatum erneut einstellen.

## <a name="region"></a>Region
Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden.   


## <a name="language"></a>Sprache
Ändert die Anzeigensprache. Dieses Feld erscheint nur, wenn es mehr als einer Sprache, gibt zum Auswählen. 

Die ursprüngliche Sprache wird entweder vom Administrator oder durch die Browsereinstellungen bestimmt, wenn Sie sich anmelden bei [!INCLUDE[d365fin](includes/d365fin_md.md)]. Die Sprache, die Sie festlegen, wird in allen Geräten verwendet werden, bei denen Sie sich anmelden wie Telefon oder Tablet. 

## <a name="changing-when-i-receive-notifications"></a>Ändern, wann I Benachrichtigungen erhalten.
Wählen Sie diesen Link, um Benachrichtigungen zu ändern oder anzuzeigen, die Sie zu bestimmten Ereignissen oder Veränderungen im Status erhalten, wie wenn Sie einen Kunden fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen. Weitere Informationen finden Sie unter [Intelligente Benachrichtigungen](ui-smart-notifications.md).

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  

