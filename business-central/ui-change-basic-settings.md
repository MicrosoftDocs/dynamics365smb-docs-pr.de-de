---
title: Die Grundeinstellungen für den aktuellen Benutzer ändern
description: Hier erfahren Sie, wie Sie einige grundlegende Einstellungen in Business Central festlegen können, z. B. Ihre Rolle und Ihr Rollenzentrum, Ihre Firma, Ihr Arbeitsdatum und Ihre Zeitzonen.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date, decimal separator
ms.search.form: 9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 08/31/2022
ms.author: jswymer
ms.openlocfilehash: de393807ae00efb5bc01a5f6c1fb0be8e98fdf36
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606062"
---
# <a name="change-basic-settings"></a>Ändern von grundlegenden Einstellungen

Au der Seite **Meine Einstellungen** können Sie grundlegende Einstellungen für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] ansehen und ändern. Änderungen, die Sie durchführen, betreffen nur den Arbeitsbereich, nicht die Arbeitsbereiche anderer Benutzer.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Rolle

Die Rolle bestimmt die Homepage, eine Startseite, die für die Anforderungen der Rolle entworfen wurde. Abhängig von der Rolle gibt die Homepage oder das Rollencenter Ihnen einen Überblick über das Unternehmen, Ihre Abteilung oder Ihre persönlichen Aufgaben. Es hilft Ihnen auch, zu Ihren Tagewerken zu navigieren und Arbeit zu finden, die Ihnen zugeordnet wird.

* Oben erlaubt es Ihnen die Navigation, zwischen Debitoren, Kreditoren, Artikeln sowie anderen wichtigen Listen von Informationen zu wechseln. Ebenso können Sie Aufgaben einleiten, wie eine neue Verkaufsrechnung direkt auf der Homepage zu erstellen.

* In der Mitte finden Sie die **Aktivitäten** Bereich, in dem aktuelle Daten angezeigt und ausgewählt werden können, um detailliertere Informationen anzuzeigen. Die zentralen Leistungs-Indikatoren können eingerichtet werden, um ein ausgewähltes Diagramm für eine visuelle Darstellung anzuzeigen, zum Beispiel, Cashflow oder Einnahmen und Ausgaben. Sie können eine Liste von Lieblingsdebitoren auf der Homepage auch für Geschäftskonten einrichten, mit denen Sie häufig Geschäfte tätigen oder besondere Aufmerksamkeit geben müssen.

### <a name="change-the-role"></a>Die Rolle ändern

Das Standardrollencenter ist der **Geschäftsführer**, aber Sie können eine andere Rolle auswählen, um das Rollencenter zu nutzen, dass besser mit Ihren Anforderungen übereinstimmt.  

1. Wählen Sie in der oberen rechten Ecke das Symbol **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") und dann die Aktion **Meine Einstellungen**.
2. Wählen Sie auf der Seite **Meine Einstellungen** im Feld **Rollencenter** das Rollencenter aus, das Sie als den Standard festlegen möchten. Wählen Sie beispielsweise **Buchhalter/in** aus.
3. Wählen Sie **OK** aus.

## <a name="company"></a><a name="company"></a>Unternehmen

Ein Unternehmen dient als Container für Daten im Project [!INCLUDE[prod_short](includes/prod_short.md)] Es kann mehrere Unternehmen in einer Datenbank geben, aber nur eine kann gleichzeitig ausgewählt werden. Der Standardmandant wird CRONUS bezeichnet und enthält nur Demodaten enthält.

Das Feld **Unternehmen** zeigt das Unternehmen, in dem Sie derzeit arbeiten, und Sie können es verwenden, um zu einem anderen Unternehmen zu wechseln. Der Firmenname wird immer in der oberen linken Ecke angezeigt und fungiert als Aktion, die Sie auswählen können, um zum Rollencenter zurückzukehren.

> [!TIP]
> Sie können die Firma auch ändern, indem Sie den Firmenumschalter (Strg+O) verwenden. Weitere Informationen zu dieser Funktion und anderen Möglichkeiten zum Ändern des Unternehmens oder der Umgebung finden Sie unter [Wechsel zu einem anderen Unternehmen oder einer anderen Umgebung](ui-organization-switch.md).

Der Standardmandant wird CRONUS bezeichnet und enthält nur Demodaten enthält. Sie können eine neue Firma mit benutzerdefinierten Daten erstellen. Weitere Informationen finden Sie unter [Neue Mandanten erstellen](about-new-company.md).

<!--
### To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date"></a><a name="work-date"></a>Arbeitsdatum

Das am häufigsten verwendete Arbeitsdatum ist das heutige Datum. Um Aufgaben wie das Abschließen von Transaktionen für ein Datum auszuführen, das nicht das aktuelle Datum ist, müssen Sie vielleicht vorübergehend das Datum ändern.

> [!TIP]  
> Geben Sie in alle Datumsfelder Folgendes ein **t** ein, um das heutige Datum schnell einzugeben, geben Sie Folgendes ein **w** um schnell das Arbeitsdatum einzugeben, das der Wert im Feld **Arbeitsdatum** auf der Seite **Meine Einstellungen** ist.

> [!IMPORTANT]  
> Wenn Sie sich abmelden oder zu einem anderen Unternehmen wechseln, nachdem Sie das Arbeitsdatum geändert haben, werden die Arbeitsdaten auf das standardmäßige Arbeitsdatum zurückgesetzt. Wenn Sie sich daher das nächste Mal anmelden in zum ursprünglichen Unternehmen zurückkehren, muss Sie das Arbeitsdatum ggf. erneut einstellen.

### <a name="work-date-indication"></a>Arbeitsdatumsangabe

Das Arbeitsdatum ist auf Seiten, die bearbeitet werden können, kritisch. Wenn das Arbeitsdatum auf einer bearbeitbaren Seite nicht auf das heutige Datum festgelegt ist, werden auf der Seite zwei Arten von Indikatoren angezeigt:

* Oben auf der Seite wird eine Erinnerung angezeigt, die Sie darüber informiert, auf welches Datum das Arbeitsdatum eingestellt ist. Die Erinnerung bietet einen direkten Link zur Einstellung des Arbeitsdatums auf der **Meine Einstellungen** Seite, sodass Sie das Datum ändern, wenn Sie möchten. In der Erinnerung können Sie auch festlegen, dass die Erinnerung für den Rest Ihrer Sitzung nicht angezeigt wird. Sofern Sie das Arbeitsdatum nicht auf "Heute" ändern, wird die Erinnerung beim nächsten Anmelden angezeigt.

* Wenn Sie die Erinnerung verwerfen, wird das Arbeitsdatum im Titel der Seite angezeigt.  

Wenn das Arbeitsdatum nicht auf den aktuellen Tag (heute) festgelegt ist, wird das aktuelle Arbeitsdatum auf allen Seiten, auf denen Sie Daten bearbeiten können, in der oberen linken Ecke angezeigt.

## <a name="region"></a><a name="region"></a> Region

Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden. Sie legt auch fest, welches Zeichen als Dezimaltrennzeichen verwendet wird, wenn Sie eine numerische Tastatur zur Eingabe von Daten verwenden. Erfahren Sie mehr unter [Daten eingeben](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a> Sprache

Ändert die Anzeigensprache. Dieses Feld erscheint nur, wenn es mehr als einer Sprache, gibt zum Auswählen.

Die ursprüngliche Sprache wird entweder vom Administrator oder durch die Browsereinstellungen bestimmt, wenn Sie sich anmelden bei [!INCLUDE[prod_short](includes/prod_short.md)]. Die Sprache, die Sie festlegen, wird in allen Geräten verwendet werden, bei denen Sie sich anmelden wie Telefon oder Tablet.

Zusätzliche Sprachen für [!INCLUDE[prod_short](includes/prod_short.md)] können von AppSource aus installiert werden. Während alle unterstützten Anzeigesprachen in der Liste angezeigt werden, muss der Administrator die entsprechende Sprachapplikation für den Mandanten installieren, bevor die Benutzer auf die neue Sprache in [!INCLUDE[prod_short](includes/prod_short.md)] wechseln können.  

## <a name="time-zone"></a>Zeitzone

Definiert die Zeitzone, in der Sie sich befinden. Wenn Sie sich zum ersten Mal bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden, wird die Zeitzone basierend auf der Adresse Ihres Unternehmens festgelegt. Ändern Sie es, wenn es nicht zu Ihrem physischen Standort passt.  

## <a name="notifications"></a>Benachrichtigungen

Wählen Sie den Link *Ändern, wann ich Benachrichtigungen erhalte*, um Benachrichtigungen zu ändern oder anzuzeigen, die Sie zu bestimmten Ereignissen oder Veränderungen im Status erhalten, wie wenn Sie einen Debitoren fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen. Erfahren Sie mehr unter [Verwalten von Benachrichtigungen](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Unterrichtstipps

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Neue Unternehmen anlegen](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
