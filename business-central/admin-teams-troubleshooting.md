---
title: Problembehandlung bei der Microsoft Teams Integration
description: 'Erfahren Sie, was Sie als Administrator tun können, um die Microsoft Teams Integration zu steuern.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 09/19/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# <a name="troubleshoot-microsoft-teams-integration-with-"></a>Problembehandlung bei der Microsoft Teams Integration mit [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel enthält Informationen zum Erkennen und Beheben von Problemen, die bei der Verwendung von Microsoft Teams mit [!INCLUDE [prod_short](includes/prod_short.md)] als typischer Benutzer oder Administrator auftreten können.

## <a name="the-sign-in-link-doesnt-work"></a>Der Anmeldelink funktioniert nicht

Wenn Sie versuchen, sich bei der App [!INCLUDE [prod_short.md](includes/prod_short.md)] für Teams unmittelbar nach der Installation der App anzumelden, und der Anmeldelink reagiert nicht, kann dies daran liegen, dass die Installation der App noch nicht vollständig abgeschlossen ist. Um das Problem zu beheben, melden Sie sich von Ihrem Teams-Client ab und melden Sie sich erneut an.

## <a name="the-settings-page-is-empty"></a>Die Einstellungsseite ist leer

Sie müssen sich zuerst anmelden, um Ihre Einstellungen zu erreichen. Um sich bei der App anzumelden, fügen Sie entweder einen Link zu einem [!INCLUDE [prod_short.md](includes/prod_short.md)]-Datensatz hinzu, oder suchen Sie nach Kontakten. Beide Aktionen führen Sie durch eine Anmeldeerfahrung, nach der Sie die Seite **Einstellungen** verwenden können.

## <a name="i-changed-company-but-it-didnt-seem-to-work"></a>Ich habe das Unternehmen gewechselt, aber es schien nicht zu funktionieren

Nachdem Sie das Unternehmen auf der Seite **Einstellungen** geändert haben, stellen Sie möglicherweise fest, dass das Dropdownmenü des Befehlsfelds anzeigt, dass Sie immer noch nach dem vorherigen Unternehmen suchen. Dieses Problem tritt auf, wenn Sie die Seite **Einstellungen** direkt aus dem Befehlsfeld öffnen. In diesem Fall wurde das Unternehmen erfolgreich geändert, und Sie suchen tatsächlich das Unternehmen, zu dem Sie gewechselt sind. Das Problem ist, dass das Dropdownmenü für das Befehlsfeld noch nicht aktualisiert wurde. Schließen Sie das Befehlsfeld oder entfernen Sie [!INCLUDE [prod_short.md](includes/prod_short.md)] aus dem Befehlsfeld, und öffnen Sie die App erneut, um sicherzustellen, dass die Dropdownliste das gesuchte Unternehmen korrekt wiedergibt. 


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts"></a>„Ein Fehler ist aufgetreten“ bei der Suche nach Kontakten

Dieser Fehler kann auftreten, wenn Sie in einem Unternehmen suchen, das nicht initialisiert wurde oder nicht mehr reagiert. Sie können beispielsweise nicht in einem neuen Unternehmen suchen, das die Nutzungsbedingungen noch nicht akzeptiert hat. Versuchen Sie, sich beim Webclient [!INCLUDE [prod_short.md](includes/prod_short.md)] anzumelden, um dieses Problem zu beheben, und bearbeiten oder schließen Sie alle angezeigten ersten Dialoge.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a>„Kann die Kontakt/Kontaktzusammenfassung API nicht finden“ Fehler bei der Suche nach Kontakten

Dieses Problem kann durch Anpassungen oder Branchenlösungen verursacht werden, die [!INCLUDE [prod_short.md](includes/prod_short.md)] beeinflussen oder verändern, oder sie stellen keine Kontakt- oder Kontaktzusammenfassungs-API zur Verfügung. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihren Administrator oder Support-Partner.

## <a name="none-of-my-links-expand-into-a-card"></a>Keiner meiner Links wird zu einer Karte erweitert

Wenn dieses Problem auftritt, sollten Sie Folgendes ausprobieren:

1. Stellen Sie zunächst sicher, dass die [!INCLUDE [prod_short](includes/prod_short.md)] App für Teams installiert ist.

    Melden Sie sich zur Überprüfung bei der Team-Desktop-App oder bei Teams im Browser an. Wählen Sie dann auf der linken Seite **Apps** und suchen Sie nach **[!INCLUDE [prod_short](includes/prod_short.md)]**. Wenn Sie die **[!INCLUDE [prod_short](includes/prod_short.md)]** App finden, wählen Sie sie aus, um die App-Detailseite zu öffnen. Wenn die Schaltlfläche **Hinzufügen** angezeigt wird, dann ist die [!INCLUDE [prod_short](includes/prod_short.md)] App nicht installiert. Weitere Informationen zum Installieren der App finden Sie unter [Installieren Sie die [!INCLUDE [prod_short](includes/prod_short.md)] App für Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gastbenutzer können Apps nicht sofort installieren. Weitere Informationen zu Gastbenutzern finden Sie in unseren [FAQ zur Zusammenarbeit mit Gästen](teams-faq.md?tabs=collaborating#language). 

2. Überprüfen Sie als Nächstes, ob Sie mit der richtigen Identität angemeldet sind.

    Gehen Sie in Teams zu einem beliebigen Chat, und klicken Sie im Feld zum Verfassen von Nachrichten mit rechts auf das Symbol [!INCLUDE [prod_short](includes/prod_short.md)], und wählen Sie dann **Einstellungen** aus. Das angezeigte Fenster gibt das Benutzerkonto an, mit dem Sie angemeldet sind. Stellen Sie sicher, dass es sich um das richtige Benutzerkonto handelt.

3. Stellen Sie sicher, dass Codeunit 2718 **Seitenzusammenfassungsanbieter** als Webdienst veröffentlicht wird.

    Teams verbindet sich mit [!INCLUDE [prod_short](includes/prod_short.md)] mithilfe eines Endpunkts für diese codeunit im [!INCLUDE [prod_short](includes/prod_short.md)] Service. Weitere Informationen zum Veröffentlichen von Webdiensten finden Sie unter [Webdienst veröffentlichen](across-how-publish-web-service.md).

4. Ihre Organisation kann Sie auch daran hindern, Links einzufügen, die sich zu Karten erweitern. Wenden Sie sich an Ihren Administrator, um die für Sie möglicherweise geltenden Organisationsrichtlinien des Teams zu verstehen.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mein Link wird manchmal nicht zu einer Karte

Ein Link wird in den folgenden Situationen nicht zu einer Karte erweitert:

- Der Link zielt auf eine Seite ab, die (auf technischer Ebene) nicht mit einer Quelltabelle in [!INCLUDE [prod_short](includes/prod_short.md)] verbunden ist. Sie können prüfen, ob die Seite eine Quelltabelle hat, indem Sie den Seitenprüfbereich im Webclient in [!INCLUDE [prod_short](includes/prod_short.md)] überprüfen verwenden. Weitere Informationen zur Seiteninspektion finden Sie unter [Seiten überprüfen](across-inspect-page.md).
- Teams unterstützen in einigen Funktionen keine Linkvorschau. Wenn Sie beispielsweise einen Chat beenden, sind Sie Gast einer anderen Organisation.
- Netzwerkprobleme führen dazu, dass Teams den Versuch, die Karte anzuzeigen, beispielsweise nach 15 Sekunden abbricht.
- Teams können den Link möglicherweise nicht erweitern, wenn Sie bereits einen Link in dasselbe Feld zum Erstellen von Nachrichten eingefügt und die Karte gelöscht haben.

Der Link muss auch alle erforderlichen Informationen enthalten, um den Datensatz zu lokalisieren und die entsprechende Karte anzuzeigen. Diese Informationen umfassen:

- Der Umgebungsname, indem er in den URL-Pfad aufgenommen wird. Wenn Sie den Umgebungsnamen nicht angeben, geht Teams davon aus, dass Sie versuchen, die Umgebung mit dem Namen Produktion zu erreichen.
- Der Firmenname unter Verwendung von *Firma =* Parameter
- Die Seitenkennung unter Verwendung des *Seite =* Parameter
- Das Lesezeichen für den Datensatz mithilfe vom *Lesezeichen =* Parameter

Beispiel:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Für technische Details zur [!INCLUDE [prod_short](includes/prod_short.md)] URL gehen Sie zur [Web Client URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) in der [!INCLUDE [prod_short](includes/prod_short.md)] Entwickler- und IT Pro-Hilfe.

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

- Stellen Sie für iOS oder Android sicher, dass Ihre Browsereinstellungen den Zugriff auf die Kamera und den Standort für die mobile Teams-App zulassen. 

Hilfe zum Ändern dieser Einstellungen finden Sie unter [Meine Kamera funktioniert nicht in Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) auf Microsoft Support.

Die [!INCLUDE [prod_short](includes/prod_short.md)] App unterstützt den Speicherort in der Team-Desktop-App nicht. Weitere Informationen über Standorte finden sie unter [FAQ zu Teams](teams-faq.md#location).

In einige Browsern, wie im neuen Microsoft Edge können Sie auswählen, welche Gerätekamera verwendet werden soll, wenn Ihr Gerät mehrere Kameras unterstützt. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams zeigt gemischte Sprachen für meine Karten und Kartendetails an

Damit Karten und Kartendetails in Teams konsistent in derselben Sprache angezeigt werden, wie in der Sprache Ihres Team-Clients und in der Sprache, in der Sie sie verwenden [!INCLUDE [prod_short](includes/prod_short.md)] muss der Webclient übereinstimmen.

- Informationen zum Ändern der Sprache in Teams finden Sie unter [Ändern Sie die Einstellungen in Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) auf Microsoft Support. 

- Erfahren Sie, wie Sie die Sprache in [!INCLUDE [prod_short](includes/prod_short.md)] ändern können unter [Grundeinstellungen ändern – Sprache](ui-change-basic-settings.md#language).

Weitere Informationen zur Funktionsweise von Sprachen zwischen Teams und [!INCLUDE [prod_short](includes/prod_short.md)] finden Sie unter [Teams FAQ](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ich habe ein Feld im Detailfenster bearbeitet, aber meine Änderung wurde nicht gespeichert

Änderungen, die Sie an einem Feld in den Detailfenstern vornehmen, werden automatisch gespeichert, wenn Sie das Feld verlassen. Bevor Sie das Fenster nach dem Ändern eines Felds schließen, wählen Sie die <kbd>Tabulatortaste</kbd> aus oder klicken bzw. tippen Sie außerhalb des Felds.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Im App-Startfeld wurde eine neue Kachel angezeigt. Wie entferne ich es?

Wenn Sie Ihre Apps auf der Office 365-Startseite (https://home.office.com) oder im App-Startfeld anzeigen, wird nach der Installation von [!INCLUDE [prod_short](includes/prod_short.md)] App für Teams eine neue Kachel mit dem Namen „Business Central Teams Integration Service Connector“ angezeigt. Diese Kachel bietet an sich keinen Wert und kann sicher ausgeblendet werden.

Als Administrator, der Microsoft Entra-Administratorrechte hat, können Sie die Kachel ausblenden, indem Sie die folgenden Schritte ausführen:

1. Melden Sie sich beim [Microsoft Entra Admin Center](https://entra.microsoft.com/) an.
2. Wählen Sie **Unternehmens-Apps** und dann **Business Central Teams Integration Service Connector** aus.
3. Wählen Sie **Eigenschaften** aus, und stellen Sie den Schalter **Sichtbar für Benutzer** auf **Nein**.
4. Wählen Sie **Speichern** aus.

> [!NOTE]
> Es wird eine Weile dauern, bis diese Änderung wirksam wird.

## <a name="duplicate-text-in-the-share-to-teams-window"></a>Text im Fenster An Teams weitergeben duplizieren

Wenn Sie Text in das Nachrichtenfeld im Fenster **Freigeben für Teams** einfügen, wird der Text dupliziert. Dieses Problem ist Microsoft bekannt und wird in einem späteren Update behoben. 

## <a name="unable-to-sign-in-to-the-share-to-teams-window"></a>Keine Anmeldung im Fenster Für Teams freigeben möglich

Dieses Problem kann verschiedene Ursachen haben. Zum Beispiel muss die Identität, mit der Sie sich anmelden, Zugriff auf Microsoft Teams haben, z. B. über ein Microsoft 365-Abonnement.

## <a name="my-cards-no-longer-have-a-popout-button"></a>Meine Karten enthalten keine Popout-Schaltfläche mehr

Ab April 2022 enthalten Links, die in Teams als kompakte Karte angezeigt werden, keine **Popout**-Schaltfläche mehr. Um diese Karte in einem eigenen Fenster zu öffnen, wählen Sie die Schaltfläche **Details** aus, und wählen Sie dann aus dem Ellipsenmenü (**...**) in der oberen rechten Ecke des Fensters die Option **Im Browser öffnen** aus.

## <a name="cant-pin-a-card-to-tab"></a>Eine Karte kann nicht an den Tab angeheftet werden

Für dieses Problem gibt es zwei Gründe.

- Wenn die Karte von Search ME geteilt wurde, kann sie nicht an eine Registerkarte angeheftet werden. 

- Kann erst angeheftet werden, wenn Sie Ihre erste Business Central-Registerkarte hinzugefügt haben. Dieses Problem ist in Teams bekannt. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a>Jemand hat einen Tab hinzugefügt, aber die Registerkarte wird mir nicht angezeigt

Dieses Problem besteht, weil Sie die BC-App für Teams nicht installiert haben. Nur diejenigen, die die App installiert haben, sehen Business Central-Registerkarten.

## <a name="others-see-a-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a>Andere sehen eine andere Sortierung oder ein anderes Spaltenlayout als das, was der Registerkartenautor sieht

Dieses Problem liegt wahrscheinlich daran, dass Sie eine Listenansicht freigegeben haben, die eine persönliche Ansicht ist. Arbeiten Sie in diesem Fall mit Ihrem Administrator zusammen, um entweder rollenspezifische Listenansichten zu erstellen, die die verschiedenen Rollen im Kanal/Chat abdecken, oder erstellen Sie diese Ansicht für die gesamte Organisation, damit alle eine einheitliche Ansicht erhalten.


## <a name="see-also"></a>Siehe auch

[[!INCLUDE [prod_short](includes/prod_short.md)] und Microsoft Teams Integration Übersicht](across-teams-overview.md)  
[Die App [!INCLUDE [prod_short](includes/prod_short.md)] für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Suche nach Debitoren, Kreditoren und anderen Kontakten von Microsoft Teams](across-search-contacts-teams.md)  
[Datensätze in Microsoft Teams freigeben](across-working-with-teams.md)  
[Teams FAQ](teams-faq.md)  
[Ändern von Firmen- und anderen Einstellungen in Teams](across-teams-settings.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
