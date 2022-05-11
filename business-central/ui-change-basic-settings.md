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
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: 683d70d7f01d35bd31c1a8e37f735e9a847cf863
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655644"
---
# <a name="change-basic-settings"></a>Ändern von grundlegenden Einstellungen

Au der Seite **Meine Einstellungen** können Sie grundlegende Einstellungen für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] ansehen und ändern. Änderungen, die Sie durchführen, betreffen nur den Arbeitsbereich, nicht die Arbeitsbereiche anderer Benutzer.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Rolle

Die Rolle bestimmt die Homepage, eine Startseite, die für die Anforderungen der Rolle entworfen wurde. Abhängig von der Rolle gibt die Homepage oder das Rollencenter Ihnen einen Überblick über das Unternehmen, Ihre Abteilung oder Ihre persönlichen Aufgaben. Es hilft Ihnen auch, zu Ihren Tagewerken zu navigieren und Arbeit zu finden, die Ihnen zugeordnet wird.

* Oben erlaubt es Ihnen die Navigation, zwischen Debitoren, Kreditoren, Artikeln sowie anderen wichtigen Listen von Informationen zu wechseln. Ebenso können Sie Aufgaben einleiten, wie eine neue Verkaufsrechnung direkt auf der Homepage zu erstellen.

* In der Mitte finden Sie die **Aktivitäten** Bereich, in dem aktuelle Daten angezeigt werden und auf den Sie klicken oder tippen können, um detailliertere Informationen anzuzeigen. Die zentralen Leistungs-Indikatoren können eingerichtet werden, um ein ausgewähltes Diagramm für eine visuelle Darstellung anzuzeigen, zum Beispiel, Cashflow oder Einnahmen und Ausgaben. Sie können eine Liste von Lieblingsdebitoren auf der Homepage auch für Geschäftskonten einrichten, mit denen Sie häufig Geschäfte tätigen oder besondere Aufmerksamkeit geben müssen.

### <a name="to-change-the-role"></a>So ändern Sie die Rolle

Das Standardrollencenter ist der **Geschäftsführer**, aber Sie können eine andere Rolle auswählen, um das Rollencenter zu nutzen, dass besser mit Ihren Anforderungen übereinstimmt.  

1. Wählen Sie in der oberen rechten Ecke das Symbol **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") und dann die Aktion **Meine Einstellungen**.
2. Wählen Sie auf der Seite **Meine Einstellungen** im Feld **Rollencenter** das Rollencenter aus, das Sie als den Standard festlegen möchten. Wählen Sie beispielsweise **Buchhalter/in** aus.
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="company"></a><a name="company"></a>Unternehmen

Ein Unternehmen dient als Container für Daten im Project [!INCLUDE[prod_short](includes/prod_short.md)] Es kann mehrere Unternehmen in einer Datenbank geben, aber nur eine kann gleichzeitig ausgewählt werden.

Der Standardmandant wird CRONUS bezeichnet und enthält nur Demodaten enthält. Sie können eine neue Firma mit benutzerdefinierten Daten erstellen. Weitere Informationen finden Sie unter [Neue Mandanten erstellen](about-new-company.md).

### <a name="to-change-the-company-name"></a>Um den Firmennamen zu ändern

Der Firmenname wird immer in der oberen linken Ecke angezeigt und fungiert als Aktion, die Sie auswählen können, um zum Rollencenter zurückzukehren. Diesen Namen können Sie auf der Seite **Firmeninformation** ändern.

1. Wählen Sie das Symbol ![, um das Menü „Einstellungen“ zu öffnen.](media/ui-experience/settings_icon_small.png) Symbol, und wählen Sie dann die Aktion **Unternehmensdaten**.
2. Geben Sie im Feld **Namen** den neuen Namen des Unternehmens ein.
3. Verlassen Sie die Seite. Das System startet neu und zeigt die neue Firma in der oberen linken Ecke an.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Anzeigen eines Firmenausweises für den schnellen Zugriff auf Unternehmensinformationen

In der oberen rechten Ecke können Sie ein benutzerdefiniertes Abzeichen hinzufügen, mit dem Sie schnell Informationen zu Firmennamen und Mandanten in einem Popup-Fenster anzeigen können. Das Firmenabzeichen ist auch nützlich, wenn [!INCLUDE[prod_short](includes/prod_short.md)] in eine andere Anwendung eingebettet ist, wie Microsoft Teams oder in einer anderen Webanwendung. In diesen Fällen dient, weil die [!INCLUDE[web_client](includes/web_client.md)] weniger umgebende Kontextinformationen anzeigt, das Firmenabzeichen als einzige Möglichkeit, um festzustellen, zu welchem Unternehmen oder welcher Umgebung ein Datensatz gehört.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Unternehmensdaten** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie im Inforegister **Unternehmenskennkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Wenn ein Firmenausweis definiert ist, können Sie den Firmennamen nicht wie beschrieben in [Um Firmennamen zu ändern](ui-change-basic-settings.md#to-change-the-company-name) ändern

## <a name="work-date"></a><a name="work-date"></a>Arbeitsdatum
Das am häufigsten verwendete Arbeitsdatum ist das heutige Datum. Um Aufgaben wie das Abschließen von Transaktionen für ein Datum auszuführen, das nicht das aktuelle Datum ist, müssen Sie vielleicht vorübergehend das Arbeitsdatum ändern.

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

Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden. Sie legt auch fest, welches Zeichen als Dezimaltrennzeichen verwendet wird, wenn Sie eine numerische Tastatur zur Eingabe von Daten verwenden. Weitere Informationen finden Sie unter [Eingabe von Daten](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a> Sprache

Ändert die Anzeigensprache. Dieses Feld erscheint nur, wenn es mehr als einer Sprache, gibt zum Auswählen.

Die ursprüngliche Sprache wird entweder vom Administrator oder durch die Browsereinstellungen bestimmt, wenn Sie sich anmelden bei [!INCLUDE[prod_short](includes/prod_short.md)]. Die Sprache, die Sie festlegen, wird in allen Geräten verwendet werden, bei denen Sie sich anmelden wie Telefon oder Tablet.

Zusätzliche Sprachen für [!INCLUDE[prod_short](includes/prod_short.md)] können von AppSource aus installiert werden. Während alle unterstützten Anzeigesprachen in der Liste angezeigt werden, muss der Administrator die entsprechende Sprachapplikation für den Mandanten installieren, bevor die Benutzer auf die neue Sprache in [!INCLUDE[prod_short](includes/prod_short.md)] wechseln können.  

## <a name="time-zone"></a>Zeitzone

Definiert die Zeitzone, in der Sie sich befinden. Wenn Sie sich zum ersten Mal bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden, wird die Zeitzone basierend auf der Adresse Ihres Unternehmens festgelegt. Ändern Sie es, wenn es nicht zu Ihrem physischen Standort passt.  

## <a name="notifications"></a>Benachrichtigungen

Wählen Sie den Link *Ändern, wann ich Benachrichtigungen erhalte*, um Benachrichtigungen zu ändern oder anzuzeigen, die Sie zu bestimmten Ereignissen oder Veränderungen im Status erhalten, wie wenn Sie einen Debitoren fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen. Weitere Informationen finden Sie unter [Benachrichtigungen verwalten](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Unterrichtstipps

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Weitere Informationen

[Neue Unternehmen anlegen](about-new-company.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
