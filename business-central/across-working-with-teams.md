---
title: Business Central-Datensätze in Microsoft Teams teilen
description: 'Erfahren Sie, wie Sie die Business Central-App für Microsoft Teams verwenden.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 09/22/2022
ms.author: jswymer
---

# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams" />Gemeinsame Nutzung von Business Central Datensätzen und Seitenlinks in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] bietet einige Möglichkeiten, Daten aus Business Central direkt in einer Microsoft Teams-Unterhaltung zu teilen:

<!-- 
## <a name="overview" />Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Wenn Sie die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert haben, können Sie eine interaktive Karte des Business Central-Datensatzes in eine Teams-Unterhaltung einbinden.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Mit oder ohne die installierte [!INCLUDE [prod_short](includes/prod_short.md)]-App können Sie einen Link von Seiten in Business Central in einer Teams-Unterhaltung teilen.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

In den folgenden Abschnitten werden die verschiedenen Möglichkeiten im Detail beschrieben.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation" />Einbinden und Anzeigen einer Business Central Karte in einer Teams Unterhaltung

Mit der Business Central-App für Teams können Sie einen Link aus einem beliebigen Business Central-Datensatz, z.B. einem Debitor oder Verkaufsauftrag, kopieren und in eine Teams-Unterhaltung einfügen. Die App verbindet Microsoft Teams mit Ihren Geschäftsdaten in [!INCLUDE [prod_short](includes/prod_short.md)]\. Anschließend erweitert sie den Link zu einer kompakten, interaktiven Karte, die Informationen über den Datensatz anzeigt. Wenn Sie sich in der Unterhaltung befinden, können Sie und Ihre Mitarbeiter weitere Details zum Datensatz anzeigen, Daten bearbeiten und Maßnahmen ergreifen&mdash;ohne Teams zu verlassen.

[![Teams-Integration in Business Central](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites" />Voraussetzungen

- Sie haben Zugriff auf Microsoft Teams.
- Sie haben die [!INCLUDE [prod_short](includes/prod_short.md)]-App in Teams installiert. Weitere Informationen finden Sie unter [Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md).

> [!NOTE]
> Alle Teilnehmer einer Teams-Unterhaltung können Karten für Business Central-Datensätze anzeigen, die Sie an die Unterhaltung senden. Um weitere Details zu Datensätzen anzuzeigen (durch Verwenden der Schaltflächen **Details** oder **Pop-out** auf einer Karte), benötigen diese jedoch Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)]. Weitere Informationen finden Sie unter [Verwalten der Microsoft Teams-Integration](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation" />Eine Business Central-Karte in eine Teams-Unterhaltung einfügen

1. Verwenden Sie Ihren Browser, um sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anzumelden.
2. Öffnen Sie den Datensatz, den Sie teilen möchten.

    Die App dient zum Anzeigen einer Karte für fast alle Typen von [!INCLUDE [prod_short](includes/prod_short.md)]-Seiten. Sie bietet jedoch die beste Umgebung, wenn es für Seiten verwendet wird, die einen einzelnen Datensatz anzeigen, wie z. B. einen Artikel, einen Kunden oder einen Verkaufsauftrag.
3. Kopieren Sie den Link auf die Seite.

    Es gibt zwei Möglichkeiten, den Link zu kopieren. Die einfachste und bevorzugte Weise ist die Auswahl von **Freigeben** ![Symbol in Business Central freigeben](media/share-icon.png) > **Link kopieren**. Die andere Möglichkeit besteht darin, die gesamte URL direkt aus der Adressleiste des Browsers zu kopieren.

    [![Kopieren Sie die Business Central-URL aus dem Browser.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Wechseln Sie zu Teams und beginnen Sie eine Unterhaltung, die mit einer Person, einer Personengruppe oder einem Teamkanal geführt werden kann.
5. Fügen Sie den Link (die URL) in das Nachrichtenfeld ein, in dem Sie die Nachricht erstellen.

    ![Fügen Sie die Business Central URL in Teams ein.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Wenn Sie beispielsweise die Meldung *Business Central möchte eine Vorschau dieses Links anzeigen.* erhalten, bedeutet dies, dass Sie die Business Central-App für Teams nicht installiert haben. Um die App zu installieren, wählen Sie **Vorschauversion zeigen** aus, und folgen Sie den Anweisungen.
6. Wenn Sie zum ersten Mal einen Link in eine Unterhaltung einfügen, werden Sie aufgefordert, sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anzumelden und der App die Zustimmung zum Datenabruf zu geben. Folgen Sie einfach den Anweisungen auf dem Bildschirm.

    > [!NOTE]
    > Sie müssen diesen Schritt nur einmal ausführen.
7. Warten Sie einen Moment, während eine Karte im Nachrichtenfeld generiert wird.
8. Wenn die Karte angezeigt wird, überprüfen Sie den Inhalt der Karte sorgfältig auf sensible Informationen, bevor Sie die Nachricht senden. Dieser Schritt ist wichtig, da nach dem Senden der Nachricht jeder Unterhaltungsteilnehmer die Karte sehen kann.
9. Wenn Sie mit der Karte zufrieden sind, wählen Sie **Senden** aus, um sie der Unterhaltung hinzuzufügen.

    > [!TIP]
    > Nachdem die Karte angezeigt wird und bevor Sie **Senden** auswählen, können Sie die eingefügte URL bei Bedarf löschen.
10. Um weitere Details anzuzeigen oder Änderungen an der Karte vorzunehmen, wählen Sie **Details** aus. Weitere Informationen finden Sie im nächsten Abschnitt.

### <a name="view-card-details" />Kartendetails anzeigen

Sobald eine Karte an ein Gespräch gesendet wurde, können alle Teilnehmer mit den [ordnungsgemäßen Berechtigungen](admin-teams-integration.md#permissions) **Einzelheiten** auswählen, um ein Fenster zu öffnen, in dem weitere Informationen zum Datensatz angezeigt werden&mdash; und möglicherweise Änderungen am Datensatz vornehmen. Es spielt keine Rolle, ob Sie die Karte senden oder die Karte empfangen. Die Funktion **Details** ist besonders für Empfänger nützlich, da sie ihnen schnell präzise und zielgerichtete Informationen über den Datensatz liefert.

Das Detailfenster ähnelt der Anzeige in [!INCLUDE [prod_short](includes/prod_short.md)], konzentriert sich jedoch auf die Seite oder den Datensatz, um den es auf der Karte geht. Wenn Sie mit dem Anzeigen und Vornehmen von Änderungen fertig sind, schließen Sie das Fenster, um zur Unterhaltung in Teams zurückzukehren.

Hier sind einige Dinge zu beachten, wenn Sie mit den Kartendetails arbeiten:

- Um die Kartendetails zu öffnen, müssen Benutzer die Berechtigung für die Seite und ihre Daten in [!INCLUDE [prod_short](includes/prod_short.md)]\. haben.
- Karten in Team-Chats werden nicht automatisch auf Änderungen aktualisiert. Alle Änderungen, die Sie an einem Datensatz im Detailfenster speichern, werden in [!INCLUDE [prod_short](includes/prod_short.md)]\. gespeichert. Auf der Karte in Teams werden die Änderungen in der Konvertierung jedoch erst angezeigt, wenn Sie den Link erneut einfügen.

Weitere Informationen zum Arbeiten mit Karten und Kartendetails finden Sie unter [Teams FAQ](teams-faq.md).

## <a name="a-nameshare-linkashare-a-link-to-page-from-business-central-to-teams" /><a name="share-link"></a>Einen Link zu einer Seite von Business Central an Teams weitergeben

Direkt von den meisten Sammlungsseiten, wie der Seite **Elemente**, und Detailseiten, wie der Karte **Elemente**, können Sie einen Link zu der Seite an bestimmte Empfänger in einer Unterhaltung in Teams senden. So können Sie beispielsweise einen Link zu einer gefilterten Ansicht Ihrer Datensätze freigeben. Die Empfänger können dann den Link auswählen, um die Seite in [!INCLUDE [prod_short](includes/prod_short.md)]\. zu öffnen.

[![!Das Menü Teilen, das auf einer Karte angezeigt wird.](media/teams-share-link-v2.png "Das Menü Teilen, das auf einer Karte angezeigt wird.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites" />Voraussetzungen

- Sie haben Zugriff auf Microsoft Teams.
- (Optional) Sie haben die App [!INCLUDE [prod_short](includes/prod_short.md)] in Teams installiert. 

  Wenn die App installiert ist, enthalten Nachrichten, die Sie mit dem Link versenden, auch eine kompakte Karte für die Seite. Weitere Informationen zum Installieren der App finden Sie unter [Installieren Sie die [!INCLUDE [prod_short](includes/prod_short.md)] App für Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link" />Einen Link freigeben

1. Öffnen Sie in [!INCLUDE [prod_short](includes/prod_short.md)]\, die Seite, die Sie teilen möchten.
2. Wählen Sie oben auf der Seite die Aktion ![!Für andere Apps freigeben auf Seiten.](media/share-icon.png) Symbol und dann **Für Teams freigeben**.
3. Falls Sie dazu aufgefordert werden, melden Sie sich bei Teams mit Ihrem Benutzernamen und Kennwort an.
4. Geben Sie auf der Seite **Für Teams freigeben** den Namen einer Person, einer Gruppe oder eines Kanals ein, an den Sie die Nachricht senden möchten.
5. Das Nachrichtenfeld enthält einen Link zu dieser Seite. Wenn die App [!INCLUDE [prod_short](includes/prod_short.md)] für Teams installiert ist, wird im Nachrichtenfeld auch eine Karte für den verlinkten Datensatz oder die verlinkte Seite angezeigt.

   Fügen Sie weitere Informationen hinzu, wenn Sie möchten, und wählen Sie dann **Freigeben**.
6. Der Link wurde nun geteilt. Wenn Sie zu der Unterhaltung gehen möchten, wählen Sie **Zu Teams gehen**.

## <a name="see-also" />Siehe auch

[Übersicht über die Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
[Installieren Sie die [!INCLUDE [prod_short](includes/prod_short.md)] App für Microsoft Teams](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Suchen Sie nach Debitoren, Kreditoren und anderen Kontakten aus Microsoft Teams](across-search-contacts-teams.md)  
[Ändern der Firma und anderer Einstellungen in Teams](across-teams-settings.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Entwickeln für Teams Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
