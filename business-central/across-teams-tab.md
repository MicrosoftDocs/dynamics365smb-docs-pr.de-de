---
title: Business Central-Registerkarte in Microsoft Teams hinzufügen
description: 'Erfahren Sie, wie Sie Registerkarten in Teams hinzufügen, die Business Central-Seiten anzeigen.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# <a name="add-business-central-tab-in-microsoft-teams"></a>Business Central-Registerkarte in Microsoft Teams hinzufügen

[!INCLUDE [online_only](includes/online_only.md)]

In Teams werden Registerkarten oben in Kanälen und Chats angezeigt, mit denen die Teilnehmer schnell auf relevante Informationen zugreifen können. In diesem Artikel werden verschiedene Möglichkeiten zum Hinzufügen einer Registerkarte erläutert, die [!INCLUDE [prod_short](includes/prod_short.md)]-Daten anzeigt.

![Registerkarten in Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a>Über Business Central-Registerkarten

Eine [!INCLUDE [prod_short](includes/prod_short.md)]-Registerkarte bietet eine fokussierte Ansicht von Listen- und -Kartenseiten von [!INCLUDE [prod_short](includes/prod_short.md)]. Die Registerkarte zeigt nicht den vollständigen [!INCLUDE [prod_short](includes/prod_short.md)]-Webclient. Es gibt weder Browserrand, [!INCLUDE [prod_short](includes/prod_short.md)]-Banner (z. B. mit „Wie möchten Sie weiter verfahren“, Suche, Hilfe) oder oberes Navigationsmenü, nur Seiteninhalt und seine Aktionen. Der Inhalt ist interaktiv, Sie können also Aktionen und Links auswählen, Daten ändern und vieles mehr. Sie sind auf das beschränkt, was Sie sehen und tun können, indem Sie dieselben Berechtigungen verwenden, die Ihrem Konto in [!INCLUDE [prod_short](includes/prod_short.md)] zugewiesen wurden.

Um zu erfahren, wer die Inhalte in einer [!INCLUDE [prod_short](includes/prod_short.md)]-Registerkarte anzeigen kann, siehe [Wer kann den Inhalt einer Registerkarte sehen?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Sind Sie ein Entwickler? Sie können Registerkarten auch programmgesteuert mithilfe der Microsoft Graph-API hinzufügen. Weitere Informationen finden Sie unter [Business Central-Registerkarten zu Teams hinzufügen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a>Voraussetzungen

Zum Hinzufügen einer [!INCLUDE [prod_short](includes/prod_short.md)]-Registerkarte müssen folgende Voraussetzungen erfüllt sein:

- Sie haben Zugriff auf Microsoft Teams.
- Sie haben eine [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenz.
- Sie haben die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert. Weitere Informationen finden Sie unter [Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).

Zum Anzeigen einer [!INCLUDE [prod_short](includes/prod_short.md)]-Registerkarte, die von einem anderen Teilnehmer im Channel oder Chat hinzugefügt wurde, müssen folgende Voraussetzungen erfüllt sein:

- Sie haben Zugriff auf Microsoft Teams.
- Sie haben eine [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenz oder eingeschränkten Zugriff auf Business Central nur mit einer Microsoft 365-Lizenz. Weitere Informationen finden Sie unter [Business Central-Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md).
- Sie haben die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert.

## <a name="add-tab-using-recommended-content"></a>Registerkarte mit empfohlenem Inhalt hinzufügen

Verwenden Sie diese Schritte, um eine Registerkarte hinzuzufügen, indem Sie auswählen, was aus einer leicht verfügbaren Liste empfohlener Inhalte angezeigt werden soll, die auf Ihrem Rollencenter basieren, ohne Teams zu verlassen. Weitere Informationen zu den Inhalten, aus denen Sie auswählen können, finden Sie unter [Woher kommen die empfohlenen Inhalte?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Wählen Sie oben in einem Kanal oder Chat in Teams **+ Registerkarte hinzufügen** aus.
2. Geben Sie im **Suchen**-Feld *Business Central* ein, wählen Sie dann das **[!INCLUDE [prod_short](includes/prod_short.md)]**-Symbol aus, und warten Sie, bis das Konfigurationsfenster für die [!INCLUDE [prod_short](includes/prod_short.md)]-Registerkarte angezeigt wird.

   ![Zeigt das Konfigurationsfenster der Business Central-Registerkarte in Teams an](media/teams-bc-tab-config-window.png)

3. Die Option **Aus empfohlenen Inhalten auswählen** zeigt das Unternehmen in [!INCLUDE [prod_short](includes/prod_short.md)], mit dem Sie arbeiten. Wenn Sie Inhalte von einem anderen Unternehmen anzeigen möchten, wählen Sie das aktuelle Unternehmen aus und verwenden Sie dann die Optionen **Umgebung** und **Unternehmen** zur Angabe des Unternehmens, mit dem Sie zusammenarbeiten möchten.
4. Wählen Sie den Abwärtspfeil in der Option **Registerkarteninhalte** aus und wählen Sie den Inhalt aus, den Sie anzeigen möchten.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Einige Seiten können unterschiedliche Ansichten enthalten, bei denen es sich um Variationen der Seite handelt, die gefiltert wird, um bestimmte Daten anzuzeigen. Um die Ansicht für den Inhalt zu ändern, wählen Sie den Abwärtspfeil für die Option **Bevorzugte Ansicht** aus, und wählen Sie die Ansicht aus der Liste aus.

   Weitere Informationen zu Ansichten finden Sie unter [Listenansichten speichern und personalisieren](ui-views.md).
6. Wählen Sie **Über diese Registerkarte auf dem Kanal posten** aus, um automatisch eine Ankündigung im Teams-Kanal oder -Chat zu posten, um die Teilnehmer wissen zu lassen, dass Sie diese Registerkarte hinzugefügt haben.
7. Wählen Sie **Speichern** aus.

## <a name="add-tab-using-a-page-link"></a>Registerkarte über einen Seitenlink hinzufügen

Eine weitere Möglichkeit, einen Tab hinzuzufügen, indem Sie einen Link (URL) zu der Seite verwenden, die Sie anzeigen möchten. Diese Methode ist nützlich, wenn Sie einen bestimmten [!INCLUDE [prod_short](includes/prod_short.md)]-Datensatz oder eine Listenseite anzeigen möchten, die in Ihrem Rollencenter nicht mit einem Lesezeichen versehen ist.

1. Wählen Sie oben in einem Kanal oder Chat in Teams **+ Registerkarte hinzufügen** aus.
2. Geben Sie in das **Suchen**-Feld *Business Central* ein und wählen Sie dann das **[!INCLUDE [prod_short](includes/prod_short.md)]**-Symbol aus.
3. Warten Sie, bis das [!INCLUDE [prod_short](includes/prod_short.md)]-Registerkartenkonfigurationsfenster angezeigt wird, und wählen Sie dann die Option **Stattdessen einen [!INCLUDE [prod_short](includes/prod_short.md)]-Link einfügen** aus.

   ![Zeigt das Konfigurationsfenster der Business Central-Registerkarte in Teams an und hebt die Verknüpfungsoption hervor](media/teams-bc-tab-config-window-page-link.png)
4. Gehen Sie zu [!INCLUDE [prod_short](includes/prod_short.md)], und öffnen Sie die Seite, die Sie auf der Registerkarte anzeigen möchten.
5. Kopieren Sie den Link auf die Seite.

   Es gibt zwei Möglichkeiten, den Link zu kopieren. Die einfachste und bevorzugte Weise ist die Auswahl von **Freigeben** ![Symbol in Business Central freigeben](media/share-icon.png) > **Link kopieren**. Die andere Möglichkeit besteht darin, die gesamte URL aus der Adressleiste des Browsers zu kopieren. Weitere Informationen zu diesem Schritt finden Sie unter [Gemeinsame Nutzung von Business Central-Datensätzen und Seitenlinks](across-working-with-teams.md).

6. Gehen Sie zurück zu Teams und fügen Sie den Link in das **URL**-Feld ein.
7. Geben Sie im Feld **Registerkartenname** einen Namen ein, der auf der Registerkarte angezeigt wird.
8. Wählen Sie **Über diese Registerkarte auf dem Kanal posten** aus, um automatisch eine Ankündigung im Teams-Kanal oder -Chat zu posten, um die Teilnehmer wissen zu lassen, dass Sie diese Registerkarte hinzugefügt haben.
9. Wählen Sie **Speichern** aus.

## <a name="add-tab-by-pinning-card-details"></a>Registerkarte durch Anheften von Kartendetails hinzufügen

Verwenden Sie diese Schritte, um eine Registerkarte für einen Datensatz hinzuzufügen, der in einem Teams-Kanal oder -Chat geteilt oder eingefügt wurde. Informationen zum Freigeben von Datensätzen und Seitenlinks in Teams finden Sie unter [Datensätze und Seitenlinks in Teams freigeben](across-working-with-teams.md).

1. Wählen Sie in Teams die Schaltfläche **Details** auf der Karte aus.
2. Wählen Sie in der oberen rechten Ecke der Kartendetails das Symbol **An den Anfang des Chats anheften** ![Stecknadelsymbol zum Hinzufügen der Teams-Registerkarte in Business Central](media/pin-teams.png) aus.

## <a name="change-a-tab-and-its-content"></a>Eine Registerkarte und ihren Inhalt ändern

Nachdem eine Registerkarte hinzugefügt wurde, können Sie bestimmte Änderungen an der Registerkarte vornehmen. Beispielsweise können Sie die Registerkarte umbenennen, verschieben und entfernen. Sie finden diese Aktionen in den Registerkartenoptionen, die verfügbar sind, indem Sie auf der Registerkarte den Abwärtspfeil auswählen.

![Zeigt das Konfigurationsfenster der Business Central-Registerkarte in Teams und das Registerkartenoptionsmenü an](media/teams-bc-tab-config-window-options.png)

Was den Inhalt einer Registerkarte betrifft, können Sie die Daten ändern, wenn Sie die Berechtigung dafür haben. Wenn Sie die Daten ändern, werden andere die Änderungen nicht sehen, bis sie die Registerkarte verlassen und zurückkehren. Gleiches gilt für Sie, wenn jemand anders Änderungen an Daten vornimmt. Sie können die Seite, die auf der Registerkarte angezeigt wird, nicht ändern, also entfernen Sie einfach die Registerkarte und fügen Sie eine andere hinzu.

Sie können auch Ihre Ansicht der Seite und ihrer Daten ändern, z. B. sortieren und das Layout zwischen Listen- und Kachelansicht wechseln. Wenn Sie diese Art von Änderungen vornehmen, haben sie keinen Einfluss darauf, was andere sehen. Sie sehen, was Sie ursprünglich gepostet haben, bis sie selbst ähnliche Änderungen vornehmen.

## <a name="see-also"></a>Siehe auch

[Übersicht über die Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
[Die App [!INCLUDE [prod_short](includes/prod_short.md)] für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Gemeinsame Nutzung von Business Central-Datensätzen und Seitenlinks in Microsoft Teams](across-working-with-teams.md)
[Teams FAQ](teams-faq.md)  
[Suche nach Debitoren, Kreditoren und anderen Kontakten von Microsoft Teams](across-search-contacts-teams.md)  
[Ändern von Firmen- und anderen Einstellungen in Teams](across-teams-settings.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Entwickeln für Teams Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
