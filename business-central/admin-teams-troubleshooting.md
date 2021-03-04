---
title: Problembehandlung bei der Microsoft Teams Integration
description: Erfahren Sie, was Sie als Administrator tun können, um die Microsoft Teams Integration zu steuern.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 10612a3e5e257969b2daf0839ea0826316a956ee
ms.sourcegitcommit: 36a32c997b201ff32ed8c1cff8179b36e2468c47
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2021
ms.locfileid: "5046532"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Problembehandlung bei der Microsoft Teams Integration mit [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel enthält Informationen zum Erkennen und Beheben von Problemen, die bei der Verwendung von Microsoft Teams mit [!INCLUDE [prod_short](includes/prod_short.md)] als typischer Benutzer oder Administrator auftreten können.

## <a name="none-of-my-links-expand-into-a-card"></a>Keiner meiner Links wird zu einer Karte erweitert 

Wenn dieses Problem auftritt, sollten Sie Folgendes ausprobieren:

1. Stellen Sie zunächst sicher, dass die [!INCLUDE [prod_short](includes/prod_short.md)] App für Teams installiert ist.

    Melden Sie sich zur Überprüfung bei der Team-Desktop-App oder bei Teams im Browser an. Wählen Sie dann auf der linken Seite **Apps** und suchen Sie nach **[!INCLUDE [prod_short](includes/prod_short.md)]**. Wenn Sie die **[!INCLUDE [prod_short](includes/prod_short.md)]** App finden, wählen Sie sie aus, um die App-Detailseite zu öffnen. Wenn die Schaltlfläche **Für mich hinzufügen** angezeigt wird, dann ist DIE [!INCLUDE [prod_short](includes/prod_short.md)] App nicht installiert. Weitere Informationen zum Installieren der App finden Sie unter [Installieren Sie die [!INCLUDE [prod_short](includes/prod_short.md)] App für Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gastbenutzer können Apps nicht sofort installieren. Weitere Informationen zu Gastbenutzern finden Sie in unseren FAQ zur Zusammenarbeit mit Gästen. 

2. Überprüfen Sie als Nächstes, ob Sie mit der richtigen Identität angemeldet sind.

    Gehen Sie in Teams zu einem beliebigen Chat und wählen Sie im Feld zum Verfassen von Nachrichten das Symbol [!INCLUDE [prod_short](includes/prod_short.md)] aus. Wenn das Fenster angezeigt wird, überprüfen Sie, ob der Benutzer, der angibt, dass Sie verbunden sind, mit dem übereinstimmt, mit dem Sie eine Verbindung herstellen mit [!INCLUDE [prod_short](includes/prod_short.md)].

3. Stellen Sie sicher, dass Codeunit 2718 **Seitenzusammenfassungsanbieter** als Webdienst veröffentlicht wird.

    Teams verbindet sich mit [!INCLUDE [prod_short](includes/prod_short.md)] mithilfe eines Endpunkts für diese codeunit im [!INCLUDE [prod_short](includes/prod_short.md)] Service. Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

4. Ihre Organisation kann Sie auch daran hindern, Links einzufügen, die sich zu Karten erweitern. Wenden Sie sich an Ihren Administrator, um die für Sie möglicherweise geltenden Organisationsrichtlinien des Teams zu verstehen.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mein Link wird manchmal nicht zu einer Karte 

Ein Link wird in den folgenden Situationen nicht zu einer Karte erweitert:

- Der Link zielt auf eine Seite eines Typs ab, der keinen Datensatz darstellt. Zum Beispiel könnte es ein Link sein zum [!INCLUDE [prod_short](includes/prod_short.md)] Rollencenter. Sie können den Seitentyp über den Seitenprüfbereich im Webclient in [!INCLUDE [prod_short](includes/prod_short.md)] überprüfen. Weitere Informationen zur Seiteninspektion finden Sie unter [Seiten überprüfen](across-inspect-page.md).
- Der Link zielt auf eine Seite ab, die (auf technischer Ebene) nicht mit einer Quelltabelle in [!INCLUDE [prod_short](includes/prod_short.md)] verbunden ist. Sie können prüfen, ob die Seite eine Quelltabelle hat, indem Sie den Seitenprüfbereich im Webclient in [!INCLUDE [prod_short](includes/prod_short.md)] überprüfen verwenden. Weitere Informationen zur Seiteninspektion finden Sie unter [Seiten überprüfen](across-inspect-page.md). 
- Teams unterstützen in einigen Funktionen keine Linkvorschau. Wenn Sie beispielsweise einen Chat beenden, befinden Sie sich in einer Besprechung oder Sie sind Gast einer anderen Organisation.
- Teams geben den Versuch, die Karte anzuzeigen, stillschweigend nach 15 Sekunden auf, beispielsweise aufgrund von Netzwerkproblemen.
- Teams können den Link möglicherweise nicht erweitern, wenn Sie bereits einen Link in dasselbe Feld zum Erstellen von Nachrichten eingefügt und die Karte gelöscht haben.

Der Link muss auch alle erforderlichen Informationen enthalten, um den Datensatz zu lokalisieren und die entsprechende Karte anzuzeigen. Diese Informationen umfassen:

- Der Umgebungsname, indem er in den URL-Pfad aufgenommen wird. Wenn Sie den Umgebungsnamen nicht angeben, geht Teams davon aus, dass Sie versuchen, die Umgebung mit dem Namen Produktion zu erreichen.
- Der Firmenname unter Verwendung von *Firma =* Parameter
- Die Seitenkennung unter Verwendung des *Seite =* Parameter
- Das Lesezeichen für den Datensatz mithilfe vom *Lesezeichen =* Parameter

Beispiel:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Für technische Details zur [!INCLUDE [prod_short](includes/prod_short.md)] URL gehen Sie zur [Web Client URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) in der [!INCLUDE [prod_short](includes/prod_short.md)] Entwickler- und IT Pro-Hilfe.

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>Die Karte wird im Feld zum Erstellen von Nachrichten angezeigt, die Auswahl der Schaltfläche Details bewirkt jedoch nichts 

Nachdem ein Link zu einer Karte im Feld zum Erstellen von Nachrichten erweitert wurde, müssen Sie die Nachricht an den Chat senden, bevor Sie die Schaltfläche **Einzelheiten** verwenden können.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Das Detailfenster wird geöffnet, es wird jedoch ein Fehler angezeigt, bevor Details angezeigt werden

Dieses Problem kann durch ein paar Dinge verursacht werden: fehlende Berechtigungen in [!INCLUDE [prod_short](includes/prod_short.md)] oder Browsereinstellungen (bei Verwendung von Teams im Browser).

1. Überprüfen Sie Ihre Berechtigungen in [!INCLUDE [prod_short](includes/prod_short.md)].

    Um Details für eine Karte anzuzeigen, überprüft [!INCLUDE [prod_short](includes/prod_short.md)] Ihre Lizenz und Berechtigungen, um diesen bestimmten Datensatz und diese Seite in dem bestimmten Unternehmen und der jeweiligen Umgebung anzuzeigen. Wenn Sie für keines dieser Dinge autorisiert sind, wird die [!INCLUDE [prod_short](includes/prod_short.md)] Standard-Fehlermeldung zu Berechtigungen im Detailfenster angezeigt. 

    Weitere Informationen zu Berechtigungen finden Sie unter [Zuweisen von Berechtigungen für Benutzer und Gruppen](ui-define-granular-permissions.md)

2. Überprüfen Sie Ihre Browsereinstellungen, wenn Sie Teams im Browser verwenden.

    - Der Popup-Blocker Ihres Browsers muss entweder deaktiviert oder eingestellt sein, damit Popups aus dem den Domänen *businesscentral.dynamics.com* oder *bc.dynamics.com* zugelassen werden. Informationen zum Zulassen von Popups für [!INCLUDE [prod_short](includes/prod_short.md)] sehen Sie unter [Browser einrichten](across-browser-settings.md#popup).
    - Ihr Browser muss während der Arbeit Zugriff auf den lokalen Browserspeicher für Cookies und Einstellungen haben.
    - Vermeiden Sie das Verwenden von Gast- oder privatem Surfen, sofern dies nicht erforderlich ist, da bestimmte Inhalte in einigen Browsern verworfen oder blockiert werden.

    Weitere Informationen zu den Mindestanforderungen an den Browser finden Sie unter [Mindestanforderungen für die Verwendung [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Ich habe Probleme mit der Kamera oder dem Standort in Teams 

Beim Benutzen von [!INCLUDE [prod_short](includes/prod_short.md)] Funktionen im Detailfenster, die Zugriff auf Ihren Standort oder Ihre Gerätekamera erfordern, müssen Sie zunächst Ihre Zustimmung erteilen, damit Teams auf diese Gerätefunktionen zugreifen können.  

- Stellen Sie für Teams im Browser sicher, dass Ihre Browsereinstellungen den Zugriff auf Kamera und Standort für https://teams.microsoft.com ermöglichen. 

- Stellen Sie im Browser sicher, dass Ihre Browsereinstellungen den Zugriff auf Kamera und Standort für iOS oder Android ermöglichen. 

Hilfe zum Ändern dieser Einstellungen finden Sie unter [Meine Kamera funktioniert nicht in Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) auf Microsoft Support.

Die [!INCLUDE [prod_short](includes/prod_short.md)] App unterstützt den Speicherort in der Team-Desktop-App nicht. Weitere Informationen über Standorte finden sie unter [FAQ zu Teams](teams-faq.md#location).

In einige Browsern, wie im neuen Microsoft Edge können Sie auswählen, welche Gerätekamera verwendet werden soll, wenn Ihr Gerät mehrere Kameras unterstützt. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams zeigt gemischte Sprachen für meine Karten und Kartendetails an 

Damit Karten und Kartendetails in Teams konsistent in derselben Sprache angezeigt werden, wie in der Sprache Ihres Team-Clients und in der Sprache, in der Sie sie verwenden [!INCLUDE [prod_short](includes/prod_short.md)] muss der Webclient übereinstimmen.

- Informationen zum Ändern der Sprache in Teams finden Sie unter [Ändern Sie die Einstellungen in Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) auf Microsoft Support. 

- Erfahren Sie, wie Sie die Sprache in [!INCLUDE [prod_short](includes/prod_short.md)] ändern können unter [Grundeinstellungen ändern – Sprache](ui-change-basic-settings.md#language).

Weitere Informationen zur Funktionsweise von Sprachen zwischen Teams und [!INCLUDE [prod_short](includes/prod_short.md)] finden Sie unter [Teams FAQ](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ich habe ein Feld im Detailfenster bearbeitet, aber meine Änderung wurde nicht gespeichert

Änderungen, die Sie an einem Feld in den Detailfenstern vornehmen, werden automatisch gespeichert, wenn Sie das Feld verlassen. Bevor Sie das Fenster nach dem Ändern eines Felds schließen, müssen Sie die Tabulatortaste drücken oder außerhalb des Felds klicken/tippen.

## <a name="see-also"></a>Siehe auch

[[!INCLUDE [prod_short](includes/prod_short.md)] und Microsoft Teams Integration Übersicht](across-teams-overview.md)  
[Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]