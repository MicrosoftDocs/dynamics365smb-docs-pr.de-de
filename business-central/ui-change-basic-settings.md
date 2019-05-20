---
title: Betrachtungs- und Bearbeitung grundlegender Einstellungen | Microsoft Docs
description: Erfahren Sie, wie Sie mehrere grundlegenden Einstellungen einrichten, zum Beispiel im Rollencenter, im Unternehmen oder im Arbeitsdatum.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: d95d2f609129e4bdba35deda726323dbed2ba67a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250968"
---
# <a name="changing-basic-settings"></a>Ändern von grundlegenden Einstellungen
Auf der Seite [**Meine Einstellungen**](https://businesscentral.dynamics.com?page=9176 "Rufen Sie direkt die Benutzereinstellungsseite in Business Central auf") können Sie grundlegende Einstellungen anzeigen und ändern.[!INCLUDE[d365fin](includes/d365fin_md.md)] Änderungen, die Sie durchführen, betreffen nur den Arbeitsbereich; nicht die Arbeitsbereiche anderer Benutzer.  

## <a name="role-center"></a> Rollencenter
Das Rollencenter erstellt die Homepage, eine Startseite, die für die Anforderungen der Rolle entworfen wurde. Abhängig von der Rolle gibt das Rollencenter Ihnen einen Überblick über das Unternehmen, Ihre Abteilung oder Ihre persönlichen Aufgaben. Es hilft Ihnen auch, zu Ihren Tagewerken zu navigieren und Arbeit zu finden, die Ihnen zugeordnet wird.

-   Oben erlaubt es Ihnen die Navigation, zwischen Debitoren, Kreditoren, Artikeln sowie anderen wichtigen Listen von Informationen zu wechseln. Ebenso können Sie Aufgaben einleiten, wie eine neue Verkaufsrechnung direkt im Rollencenter zu erstellen.

-   Im Mittelpunkt finden Sie die Kacheln **Aktivitäten**. Aktivitäten zeigen aktuelle Daten an und können geklickt werden oder getippt werden, um detailliertere Informationen anzuzeigen. Die zentralen Leistungs-Indikatoren können eingerichtet werden, um ein ausgewähltes Diagramm für eine visuelle Darstellung anzuzeigen, zum Beispiel, Cashflow oder Einnahmen und Ausgaben. Sie können eine Liste von Lieblingsdebitoren auf der Homepage auch für Konten einrichten, mit denen Sie häufig Geschäfte tätigen oder besondere Aufmerksamkeit geben müssen.

### <a name="to-change-role-center"></a>So ändern Sie ein Rollencenter
Das Standardrollencenter ist der **Geschäftsführer**, aber Sie können ein anderes Rollencenter auswählen, das mit den Anforderungen besser übereinstimmt.
1. In der oberen rechter Ecke wählen Sie das Symbol **Einstellungen** aus ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol Rollencenter") und dann **Meine Einstellungen**.
2. Wählen Sie auf der Seite **Meine Einstellungen** im Feld **Rollencenter** das Rollencenter aus, das Sie als Standard festlegen möchten. Wählen Sie beispielsweise **Buchhalter/in** aus.
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="company"></a>Unternehmen
Ein Unternehmen dient als Container für Daten im Project [!INCLUDE[d365fin](includes/d365fin_md.md)] Es kann mehrere Unternehmen in einer Datenbank geben, aber nur eine kann gleichzeitig ausgewählt werden.

Der Standardmandant wird CRONUS bezeichnet und enthält nur Demodaten enthält.

> [!TIP]  
>   Wenn Sie einen anderen Namen des Mandanten in der Anwendung anzeigen möchten (z. B. im Rollencenter), legen Sie das Feld **Name** auf der Seite **Firmendaten** oder das Feld **Anzeigename** auf der Seite **Unternehmen** fest.  

## <a name="work-date"></a>Arbeitsdatum
Standardmäßig wird das aktuelle Datum (Systemdatum) verwendet. Um Aufgaben wie das Abschließen von Transaktionen für ein Datum auszuführen, das nicht das aktuelle Datum ist, müssen Sie möglicherweise vorübergehend das Arbeitsdatum ändern.

> [!TIP]  
>   Tippen Sie **a**, um rasch das Arbeitsdatum in ein Datumsfeld einzugeben. Schreiben Sie **h**, um rasch das aktuelle Datum in das Datumsfeld einzugeben.

> [!IMPORTANT]  
>   Wenn Sie sich abmelden oder zu einem anderen Unternehmen wechseln, nachdem Sie das Arbeitsdatum geändert haben, werden die Arbeitsdaten auf das standardmäßige Arbeitsdatum zurückgesetzt. Wenn Sie sich daher das nächste Mal anmelden in zum ursprünglichen Unternehmen zurückkehren, muss Sie das Arbeitsdatum ggf. erneut einstellen. 

### <a name="work-date-indication"></a>Arbeitsdatumsangabe
<!--
Whenever the work date is not set to the current day (today), there are two indicators on pages that you open for editing:

- A reminder appears at the top of the page that tells you what the work date is set to. The reminder provides a direct link to the work date setting on the **My Settings** page so you change the date if you want. From the reminder, you can also choose to dismiss the reminder for the rest of your session. Unless you change the work date to "today", the reminder will appear the next time you sign in. 

- If you dismiss the reminder, the work date will appear in the title of the page.  
-->
Wenn das Arbeitsdatum nicht auf den aktuellen Tag (heute) festgelegt ist, wird das aktuelle Arbeitsdatum auf allen Seiten, auf denen Sie Daten bearbeiten können, in der oberen linken Ecke der Seite angezeigt.
  
## <a name="region"></a> Region

Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden.


## <a name="language"></a> Sprache
Ändert die Anzeigensprache. Dieses Feld erscheint nur, wenn es mehr als einer Sprache, gibt zum Auswählen. 

Die ursprüngliche Sprache wird entweder vom Administrator oder durch die Browsereinstellungen bestimmt, wenn Sie sich anmelden bei [!INCLUDE[d365fin](includes/d365fin_md.md)]. Die Sprache, die Sie festlegen, wird in allen Geräten verwendet werden, bei denen Sie sich anmelden wie Telefon oder Tablet.

## <a name="changing-when-i-receive-notifications"></a>Ändern, wann I Benachrichtigungen erhalten.
Wählen Sie diesen Link, um Benachrichtigungen zu ändern oder anzuzeigen, die Sie zu bestimmten Ereignissen oder Veränderungen im Status erhalten, wie wenn Sie einen Debitoren fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen. Weitere Informationen finden Sie unter [Intelligente Benachrichtigungen](ui-smart-notifications.md).

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
