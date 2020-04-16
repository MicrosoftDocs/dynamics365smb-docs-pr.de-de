---
title: Betrachtungs- und Bearbeitung grundlegender Einstellungen | Microsoft Docs
description: Erfahren Sie, wie Sie mehrere grundlegenden Einstellungen einrichten, zum Beispiel im Rollencenter, im Unternehmen oder im Arbeitsdatum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: cd3d7a821c088b6e9f457e3bf3dc05d0c53525c4
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194595"
---
# <a name="change-basic-settings"></a>Ändern von grundlegenden Einstellungen

Au der Seite **Meine Einstellungen** können Sie grundlegende Einstellungen für [!INCLUDE[d365fin](includes/d365fin_md.md)] ansehen und ändern. Änderungen, die Sie durchführen, betreffen nur den Arbeitsbereich, nicht die Arbeitsbereiche anderer Benutzer.  

## <a name="role-center"></a><a name="role-center"></a> Rollencenter
Das Rollencenter erstellt die Homepage, eine Startseite, die für die Anforderungen der Rolle entworfen wurde. Abhängig von der Rolle gibt das Rollencenter Ihnen einen Überblick über das Unternehmen, Ihre Abteilung oder Ihre persönlichen Aufgaben. Es hilft Ihnen auch, zu Ihren Tagewerken zu navigieren und Arbeit zu finden, die Ihnen zugeordnet wird.

-   Oben erlaubt es Ihnen die Navigation, zwischen Debitoren, Kreditoren, Artikeln sowie anderen wichtigen Listen von Informationen zu wechseln. Ebenso können Sie Aufgaben einleiten, wie eine neue Verkaufsrechnung direkt im Rollencenter zu erstellen.

-   In der Mitte finden Sie die **Aktivitäten** Bereich, in dem aktuelle Daten angezeigt werden und auf den Sie klicken oder tippen können, um detailliertere Informationen anzuzeigen. Die zentralen Leistungs-Indikatoren können eingerichtet werden, um ein ausgewähltes Diagramm für eine visuelle Darstellung anzuzeigen, zum Beispiel, Cashflow oder Einnahmen und Ausgaben. Sie können eine Liste von Lieblingsdebitoren im Rollencenter auch für Konten einrichten, mit denen Sie häufig Geschäfte tätigen oder denen sie besondere Aufmerksamkeit geben müssen.

### <a name="to-change-the-role"></a>So ändern Sie die Rolle
Das Standardrollencenter ist der **Geschäftsführer**, aber Sie können eine andere Rolle auswählen, um das Rollencenter zu nutzen, dass besser mit Ihren Anforderungen übereinstimmt.
1. In der oberen rechter Ecke wählen Sie das Symbol **Einstellungen** aus ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") und wählen dann die Aktion **Meine Einstellungen**.
2. Wählen Sie auf der Seite **Meine Einstellungen** im Feld **Rollencenter** das Rollencenter aus, das Sie als den Standard festlegen möchten. Wählen Sie beispielsweise **Buchhalter/in** aus.
3. Wählen Sie die Schaltfläche **OK** aus.

## <a name="company"></a><a name="company"></a>Unternehmen
Ein Unternehmen dient als Container für Daten im Project [!INCLUDE[d365fin](includes/d365fin_md.md)] Es kann mehrere Unternehmen in einer Datenbank geben, aber nur eine kann gleichzeitig ausgewählt werden.

Der Standardmandant wird CRONUS bezeichnet und enthält nur Demodaten enthält. Sie können eine neue Firma mit benutzerdefinierten Daten erstellen. Weitere Informationen finden Sie unter [Neue Mandanten erstellen](about-new-company.md).

## <a name="to-change-the-company-name"></a>Um den Firmennamen zu ändern
Der Firmenname wird immer in der oberen linken Ecke angezeigt und fungiert als Aktion, die Sie auswählen können, um zum Rollencenter zurückzukehren. Diesen Namen können Sie auf der Seite **Firmeninformation** ändern.

1. Wählen Sie das Symbol ![Zahnrad, um das Einstellungsmenü zu öffnen](media/ui-experience/settings_icon_small.png), und wählen Sie dann die Aktion **Firmeninformationen**.
2. Geben Sie im Feld **Namen** den neuen Namen des Unternehmens ein.
3. Verlassen Sie die Seite. Das System startet neu und zeigt die neue Firma in der oberen linken Ecke an.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a>Anzeigen eines Firmenausweises für den schnellen Zugriff auf Unternehmensinformationen  
In der oberen rechten Ecke können Sie ein benutzerdefiniertes Abzeichen hinzufügen, mit dem Sie schnell Informationen zu Firmennamen und Mandanten in einem Popup-Fenster anzeigen können.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Unternehmensinformationen** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie im Inforegister **Unternehmenskennkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Wenn ein Firmenausweis definiert ist, können Sie den Firmennamen nicht wie beschrieben in [Um Firmennamen zu ändern](ui-change-basic-settings.md#to-change-the-company-name) ändern

## <a name="work-date"></a><a name="work-date"></a>Arbeitsdatum
Das am häufigsten verwendete Arbeitsdatum ist das heutige Datum. Um Aufgaben wie das Abschließen von Transaktionen für ein Datum auszuführen, das nicht das aktuelle Datum ist, müssen Sie vielleicht vorübergehend das Arbeitsdatum ändern.

> [!TIP]  
> Geben Sie in alle Datumsfelder Folgendes ein **t** ein, um das heutige Datum schnell einzugeben, geben Sie Folgendes ein **w** um schnell das Arbeitsdatum einzugeben, das der Wert im Feld **Arbeitsdatum** auf der Seite **Meine Einstellungen** ist.

> [!IMPORTANT]  
>  Wenn Sie sich abmelden oder zu einem anderen Unternehmen wechseln, nachdem Sie das Arbeitsdatum geändert haben, werden die Arbeitsdaten auf das standardmäßige Arbeitsdatum zurückgesetzt. Wenn Sie sich daher das nächste Mal anmelden in zum ursprünglichen Unternehmen zurückkehren, muss Sie das Arbeitsdatum ggf. erneut einstellen.

### <a name="work-date-indication"></a>Arbeitsdatumsangabe
Wann immer das Arbeitsdatum nicht auf das heutige Datum gesetzt ist, erscheinen zwei Arten von Indikatoren auf Seiten, die bearbeitet werden können und bei denen das Arbeitsdatum daher von entscheidender Bedeutung ist:

- Oben auf der Seite wird eine Erinnerung angezeigt, die Sie darüber informiert, auf welches Datum das Arbeitsdatum eingestellt ist. Die Erinnerung bietet einen direkten Link zur Einstellung des Arbeitsdatums auf der **Meine Einstellungen** Seite, sodass Sie das Datum ändern, wenn Sie möchten. In der Erinnerung können Sie auch festlegen, dass die Erinnerung für den Rest Ihrer Sitzung nicht angezeigt wird. Sofern Sie das Arbeitsdatum nicht auf "Heute" ändern, wird die Erinnerung beim nächsten Anmelden angezeigt.

- Wenn Sie die Erinnerung verwerfen, wird das Arbeitsdatum im Titel der Seite angezeigt.  
--> Wenn das Arbeitsdatum nicht auf den aktuellen Tag (heute) festgelegt ist, wird das aktuelle Arbeitsdatum auf allen Seiten, auf denen Sie Daten bearbeiten können, in der oberen linken Ecke der Seite angezeigt.

## <a name="region"></a><a name="region"></a> Region

Die Einstellung **Region** bestimmt, wie Daten, Uhrzeiten, Ziffern und Währungen angezeigt oder formatiert werden.

## <a name="language"></a><a name="language"></a> Sprache
Ändert die Anzeigensprache. Dieses Feld erscheint nur, wenn es mehr als einer Sprache, gibt zum Auswählen.

Die ursprüngliche Sprache wird entweder vom Administrator oder durch die Browsereinstellungen bestimmt, wenn Sie sich anmelden bei [!INCLUDE[d365fin](includes/d365fin_md.md)]. Die Sprache, die Sie festlegen, wird in allen Geräten verwendet werden, bei denen Sie sich anmelden wie Telefon oder Tablet.

Zusätzliche Sprachen für [!INCLUDE[prodshort](includes/prodshort.md)] können von AppSource aus installiert werden. Während alle unterstützten Anzeigesprachen in der Liste angezeigt werden, muss der Administrator die entsprechende Sprachapplikation für den Mandanten installieren, bevor die Benutzer auf die neue Sprache in [!INCLUDE[prodshort](includes/prodshort.md)] wechseln können.  

## <a name="changing-when-i-receive-notifications"></a>Ändern, wann I Benachrichtigungen erhalten.
Wählen Sie diesen Link, um Benachrichtigungen zu ändern oder anzuzeigen, die Sie zu bestimmten Ereignissen oder Veränderungen im Status erhalten, wie wenn Sie einen Debitoren fakturieren wollen, der einen überfälligen Saldo hat oder der verfügbare Lagerbestand geringer ist als die Menge, die Sie verkaufen wollen. Weitere Informationen finden Sie unter [Benachrichtigungen verwalten](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Neue Unternehmen anlegen](about-new-company.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
