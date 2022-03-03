---
title: Teams FAQ
description: Hier erhalten Sie Antworten auf einige typische Fragen zur Arbeit mit Teams und Business Central.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: 34c669f955bebf84149959182bb1ce8bdeb139a0
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147492"
---
# <a name="teams-faq"></a>Teams FAQ

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel beantwortet einige der Fragen, die Sie möglicherweise zur Arbeit mit Teams und [!INCLUDE [prod_short](includes/prod_short.md)] haben.

## <a name="general"></a>[Allgemein](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Wie melde ich mich bei der [!INCLUDE [prod_short.md](includes/prod_short.md)] App in Teams an?

Nach der Installation der App werden Sie aufgefordert, sich beim ersten Benutzen der App beim Einfügen von einem [!INCLUDE [prod_short.md](includes/prod_short.md)] Link in den Team-Chat oder wenn Sie die Aktion **Einzelheiten** auf einer Karte in Teams auswählen, anzumelden. Abhängig von Ihrem Team-Client müssen Sie möglicherweise Ihre Anmeldeinformationen eingeben, um auf [!INCLUDE [prod_short.md](includes/prod_short.md)] zuzugreifen.

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Wie melde ich mich bei der [!INCLUDE [prod_short.md](includes/prod_short.md)] App in Teams ab?

So melden Sie sich von Ihrer aktuellen Benutzeridentität mit der Sie eine Verbindung zu [!INCLUDE [prod_short.md](includes/prod_short.md)], hergestellt haben, ab. Gehen Sie zu einem beliebigen Chat-Erstellungsfeld und wählen Sie das [!INCLUDE [prod_short.md](includes/prod_short.md)] Symbol mit einem Rechtsklick und dann **Einstellungen** aus. Wenn das Fenster angezeigt wird, überprüfen Sie Ihre aktuell angemeldete Identität, und wählen Sie dann **Abmelden** aus.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>Stellt die App für Teams eine Verbindung zu [!INCLUDE [prod_short.md](includes/prod_short.md)] lokal her? 

Anzahl Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams funktioniert nur mit [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Es gibt keine Pläne, um die [!INCLUDE [prod_short.md](includes/prod_short.md)] Bereitstellungstypen&mdash;wie lokal, Hybrid Cloud oder Private Cloud&mdash;die Microsoft nicht direkt hostet oder verwaltet, bereitzustellen.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Funktioniert die App mit mehreren Unternehmen und Umgebungen? 

Ja. Um nach Kontakten in einem anderen Unternehmen zu suchen, wechseln Sie zu [Einstellungen](across-teams-settings.md). Wenn die App [!INCLUDE [prod_short.md](includes/prod_short.md)] einen Link in eine Karte erweitert, muss der Link die Umgebung und den Firmennamen enthalten, damit die App mit dem Datensatz in der richtigen Firma übereinstimmt. Sie können Links zu allen Unternehmen und Umgebungen einfügen, auf die Sie innerhalb Ihres Unternehmens und über das Konto [!INCLUDE [prod_short.md](includes/prod_short.md)], mit dem Sie sich angemeldet haben, Zugriff haben. Teilnehmer des Chats sehen die Karte. Sie können die Kartendetails jedoch nur anzeigen, wenn sie über Berechtigungen für das Unternehmen oder die Umgebung verfügen, in der dieser Datensatz gespeichert ist.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>In welchen Ländern oder Regionen ist die [!INCLUDE [prod_short.md](includes/prod_short.md)] App verfügbar? 

Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams ist nicht auf ein Land oder Region beschränkt. Die App ist in allen Märkten verfügbar, die derzeit vom Teams Marktplatz unterstützt werden. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Funktioniert die [!INCLUDE [prod_short.md](includes/prod_short.md)] App mit jeder Lokalisierung von [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. Die App soll mit jeder Lokalisierung von [!INCLUDE [prod_short.md](includes/prod_short.md)] funktionieren, unabhängig davon, ob diese Lokalisierung direkt von Microsoft oder über einen Partner angeboten wird. Weitere Informationen finden Sie unter [Verfügbarkeit nach Ländern/Regionen und unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Welche Sprachen [!INCLUDE [prod_short.md](includes/prod_short.md)] unterstützt die App?

Zwei Dinge bestimmen die Sprache für Karten und Kartendetails in Teams:

1. Ihre Sprache in Teams, die Sie in Ihren Kontoeinstellungen in Teams sehen können. 
2. Ihre Sprache in [!INCLUDE [prod_short.md](includes/prod_short.md)], die Sie im [!INCLUDE [prod_short.md](includes/prod_short.md)] Webclient sehen können (siehe [Grundeinstellung ändern – Sprache](ui-change-basic-settings.md#language)).

In der folgenden Tabelle wird erläutert, wie sich die Erfahrung für Nachrichtenautoren und -empfänger in Abhängigkeit von den Spracheinstellungen und der Verfügbarkeit von Sprachen unterscheidet.

|Wer|Karte|Kartendetails |
|-|----|--------------| 
|Autor der Nachricht |Wird in der Sprache angezeigt, die in Teams für Sie angegeben wurde. Wenn [!INCLUDE [prod_short.md](includes/prod_short.md)] nicht die gleiche Sprache anbietet, wird die Karte in Englisch angezeigt. |Wird in der Sprache angezeigt, die für Sie in [!INCLUDE [prod_short.md](includes/prod_short.md)] angezeigt wurde.  dies kann Sprachen aus Sprach-Apps enthalten, die von Partnern bereitgestellt werden. |
|Nachrichten-Empfänger |Wird in der Sprache des Nachrichtenautors angezeigt. |Wird in der Sprache angezeigt, die für Sie in [!INCLUDE [prod_short.md](includes/prod_short.md)] angezeigt wurde. |

Für die Liste der unterstützten Sprachen für [!INCLUDE [prod_short.md](includes/prod_short.md)] gehen Sie zu [Unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the-prod_shortmd-app-work-with-industry-solutions"></a>Funktioniert die [!INCLUDE [prod_short.md](includes/prod_short.md)]-App mit Branchenlösungen?

Ja. Es funktionieren jedoch nur einige Funktionen der App mit [Apps einbetten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- Die App arbeitet mit Links, die auf dem Muster **\*. bc.dynamics.com** basieren, das normalerweise mit „Apps einbetten“ verwendet wird.
- Die Kontaktsuche ist für eingebettete Apps, die die Basisanwendung von Microsoft ersetzen, nicht verfügbar.

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Wo finde ich die Teamintegration innerhalb des [!INCLUDE [prod_short.md](includes/prod_short.md)] Webclients? 

Derzeit gibt es keine Einbettung von Teams-Steuerelementen oder das Vorhandensein von Teams-Funktionen im [!INCLUDE [prod_short.md](includes/prod_short.md)] Web-Client oder anderen Clients.

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>Funktioniert [!INCLUDE [prod_short.md](includes/prod_short.md)] mit der mobilen App von Teams?

Ja. Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App kann über die Team-Desktop-App oder den Browser oder von einem Administrator für alle Benutzer installiert werden. Nach der Installation wird die [!INCLUDE [prod_short.md](includes/prod_short.md)] App automatisch in Teams für iOS und Android verfügbar. Auf Mobilgeräten können Sie nur von anderen gesendete Karten anzeigen, auf Details zugreifen oder die Karte hervorheben, um die volle Erfahrung in der [!INCLUDE [prod_short.md](includes/prod_short.md)] App zur Verfügung zu haben. Sie können keine Links einfügen, die beim Verfassen von Nachrichten zu Karten erweitert werden oder nach Kontakten suchen. Mindestanforderungen für Mobiltelefone finden Sie unter [Mindestanforderungen für die Verwendung von Business Central](product-requirements.md).

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>Ist die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams gleich wie die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für iOS und Android?

Anzahl Die App für Teams ist ein Add-In zu Microsoft Teams und exklusiv für kollaborative Erfahrungen konzipiert, die innerhalb von Teams aufleuchten. Auf der anderen Seite bietet die [!INCLUDE [prod_short.md](includes/prod_short.md)] mobile App Ihnen eine umfassende Erfahrung, mit der Sie arbeiten können mit [!INCLUDE [prod_short.md](includes/prod_short.md)] Daten auf Ihren Mobilgeräten.

Mobile Benutzer werden aufgefordert, sowohl die mobile App als auch die App zu installieren, damit Teams das Beste daraus [!INCLUDE [prod_short.md](includes/prod_short.md)] herausholen kann. Wenn beide installiert sind, können Sie die **Hervorhben** Aktion auf einer Karte in Teams auswählen, um die Kartendetails in der [!INCLUDE [prod_short.md](includes/prod_short.md)] App zu öffnen. Informationen zur Installation von [!INCLUDE [prod_short.md](includes/prod_short.md)] und der Teams App für Mobile, finden Sie unter:

- [Abrufen von Business Central auf meinem mobilen Gerät](install-mobile-app.md)
- [Holen Sie sich die mobile App von Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) unter Microsoft Support

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>Funktioniert die [!INCLUDE [prod_short.md](includes/prod_short.md)] App in allen Teams Clients?

Anzahl Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams wird bei der Installation als Paket für MacOS oder Linux nicht unterstützt. Auf diesen Plattformen können Sie stattdessen über einen unterstützten Browser auf Teams zugreifen.

Mindestanforderungen für [!INCLUDE [prod_short.md](includes/prod_short.md)] finden Sie unter [Mindestanforderungen für die Verwendung von Business Central](product-requirements.md#teams).

Informationen zur Auswahl der Team-Clients und zu deren Installation finden Sie unter [Clients für Microsoft Teams abrufen](/microsoftteams/get-clients) in der Teamdokumentation.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>Welches ist der beste Team-Client für [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Es gibt nur geringfügige Unterschiede und Einschränkungen zwischen Team-Clients, die sich auf Ihre Erfahrung mit der [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams auswirken können. Berücksichtigen Sie bei der Auswahl eines Team-Clients Folgendes:

- Auf die Kamera und den Standort kann nicht über das Detailfenster in der Team-Desktop-App zugegriffen werden.
- Telefonnummern können nicht über das Detailfenster in Teams für iOS, Teams für Android oder Teams im Browser aktiviert werden.
- Beim Verwenden von Microsoft Edge mit Teams im Browser können Sie problemlos über mehrere Identitäten und Konten hinweg arbeiten, indem Sie sich bei Teams aus verschiedenen Profilen anmelden. Erfahren Sie mehr über die Verwendung von Profilen in Microsoft Edge unter [Melden Sie sich an und erstellen Sie mehrere Profile in Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) auf Microsoft Support.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Was ist der beste Weg für mich, um [!INCLUDE [prod_short.md](includes/prod_short.md)] und Microsoft Teams potenziellen Kunden zu zeigen?

Wenn Sie ein Wiederverkaufspartner sind, möchten Sie möglicherweise eine Umgebung, in der Sie potenzielle Kunden im Rahmen von Vorverkaufsdemonstrationen anzeigen können. Um Auswirkungen auf Microsoft Teams in Ihrer Organisation zu vermeiden, erhalten Sie ein Microsoft 365-Demokonto unter [https://aka.ms/CDX](https://aka.ms/CDX). Mit diesem Konto haben Sie die volle Kontrolle über eine unabhängige Azure-Organisation, die Microsoft Teams und [!INCLUDE [prod_short.md](includes/prod_short.md)] umfasst. Weitere Informationen finden Sie unter [Vorbereiten von Demonstrationsumgebungen von Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>Nimmt die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams meine Anpassung und Personalisierung vor?

Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams kann Karten für Links zu Kundenseiten und Tabellen in [!INCLUDE [prod_short.md](includes/prod_short.md)] anzeigen, wie Seiten und Tabellen, die von Ihren eigenen benutzerdefinierten Erweiterungen oder von AppSource stammen.

Die Felder, die in Teams auf einer Karte angezeigt werden, können ebenfalls von [!INCLUDE [prod_short.md](includes/prod_short.md)] Anpassungen betroffen sein, die für Ihre Organisation installiert sind. Karten berücksichtigen keine rollenspezifischen Anpassungen oder Benutzerpersonalisierung. Das Fenster mit den Kartendetails zeigt jedoch die Datensatzdetails so an, wie Sie sie sehen würden in [!INCLUDE [prod_short.md](includes/prod_short.md)], einschließlich aller Erweiterungen, Rollenanpassungen und Benutzerpersonalisierung.

Wenn Sie nach Kontakten suchen, werden die Felder, die in der Tabelle **Kontakte** und in den Suchergebnissen der angezeigten Tabellen und Felder übereinstimmen, von keiner Anpassung oder Personalisierung betroffen.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>Wie wirken sich die für die App erforderlichen Berechtigungen auf meine Privatsphäre aus?

Vor der Installation der [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams können Sie die Mindestberechtigungen überprüfen, die für die Funktion der App erforderlich sind. Durch die Installation der App erklären Sie sich damit einverstanden, dass die App über die Berechtigung zum Empfangen von Nachrichten und Daten verfügt, die Sie bereitstellen, und dass Teams über die Berechtigung zum Speichern und Verarbeiten dieser Nachrichten verfügt.

Auch einige [!INCLUDE [prod_short.md](includes/prod_short.md)]-Funktionen erfordern das Öffnen externer Links geöffnet oder Zugriff auf Ihre Kamera oder Ihren geografischen Standort. Angenommen, Sie möchten ein Foto einer Kaufrechnung zur Verarbeitung aufnehmen. Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App verwendet diese Funktionen nicht ohne Ihre Zustimmung und sie werden nur von bestimmten Funktionen im Fenster **Einzelheiten** verwendet. Wenn Sie eine dieser Funktionen zum ersten Mal verwenden, wird in Teams ein Dialogfeld angezeigt, in dem Sie aufgefordert werden, Zugriff auf die erforderlichen Gerätefunktionen zu gewähren.

- Auf dem Team-Desktop überprüfen und passen Sie die App-Berechtigungen aus dem Fenster **Einstellungen** an. Wählen Sie Ihr Profilbild oben in der App aus und wählen Sie **Einstellungen** > **Berechtigungen**, dann wählen Sie die [!INCLUDE [prod_short.md](includes/prod_short.md)] App aus.

- Für Teams im Browser und Teams für iOS oder Android können Sie die Berechtigungen in Ihrem Browser oder in den Geräteeinstellungen überprüfen oder anpassen.

> [!NOTE]
> Die genauen [!INCLUDE [prod_short.md](includes/prod_short.md)]-Funktionen, die Sie zur Eingabe von Berechtigungen auffordern, hängen von den Add-On-Apps und Anpassungen ab, die auf die [!INCLUDE [prod_short.md](includes/prod_short.md)]-Umgebung angewendet werden, mit der Sie eine Verbindung herstellen.

### <a name="where-can-i-learn-about-my-privacy"></a>Wo kann ich etwas über meine Privatsphäre erfahren? 

Informationen dazu, wie Microsoft mit Ihren Daten umgeht, finden Sie in der [Microsoft-Datenschutzerklärung](https://go.microsoft.com/fwlink/?linkid=2030602). 

Wenden Sie sich an Ihren Administrator, um zu erfahren, wie Ihre Organisation mit dem Datenschutz Ihrer Daten umgeht.

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Wie deinstalliere ich die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams?

Um die App zu entfernen, die Sie für sich selbst installiert haben, gehen Sie zu einem beliebigen Chat-Erstellungskästchen und suchen Sie das Symbol [!INCLUDE [prod_short.md](includes/prod_short.md)]. Klicken Sie mit der rechten Maustaste auf das Symbol und wählen Sie **Deinstallieren** aus.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Wird Microsoft die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams weiter verbessern?

Bei Microsoft achten wir stets auf das Feedback aus unsere breitgefächerte Benutzer-Community und reagieren auf die häufigsten Vorschläge. Um zu erfahren, was als Nächstes für die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams geplant ist, gehen Sie zu [Dynamics 365-Release-Plan](/dynamics365-release-plan/2021wave1/).

Wenn Sie an der Verbesserung der App für Teams teilnehmen möchten oder eine Idee haben, die Ihre Arbeit oder Ihre Erfahrungen in der Zusammenarbeit in Teams vereinfacht, fügen Sie eine Idee hinzu oder stimmen Sie für vorhandene Ideen ab unter [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### <a name="where-can-i-find-teams-integration-inside-the-business-central-web-client"></a>Wo finde ich die Teams Integration innerhalb des Business Central Web Clients? 

Funktionen im Web Client, die mit Teams verknüpft sind, finden Sie unter [Datensätze und Seitenverknüpfungen teilen](across-working-with-teams.md#share-link) in Microsoft Teams.

## <a name="search-for-contacts"></a>[Suchen Sie nach Kontakten](#tab/contacts)

### <a name="which-tables-does-the-app-search-in"></a>In welchen Tabellen sucht die App?

Bei der Suche nach Kontakten aus der [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams, werden Ihre Suchbegriffe mit Datensätzen in der Tabelle **Kontakte** in [!INCLUDE [prod_short.md](includes/prod_short.md)] verglichen. 

### <a name="which-fields-in-the-contacts-table-can-i-search"></a>Welche Felder in der Kontakttabelle kann ich durchsuchen?

Während Sie Ihre Suchbegriffe in das Suchfeld eingeben, werden die Begriffe mit den meisten Feldern in der Tabelle **Kontakte** abgeglichen. Zu den Feldern gehören beispielsweise die Felder **Nr.**, **Name**, **Adresse**, **Telefonnr.** oder **Handynummer** und **E-Mail**. 

Suchbegriffe werden nicht mit benutzerdefinierten Feldern abgeglichen, die der Tabelle **Kontakte** durch Apps und Erweiterungen hinzugefügt werden.

### <a name="do-search-results-include-companies-and-persons"></a>Enthalten die Suchergebnisse Unternehmen und Personen?

Ja. Unter [!INCLUDE [prod_short.md](includes/prod_short.md)] können Kontakte vom Typ **Unternehmen** oder **Person** sein, wenn eine oder mehrere Personen mit einem Unternehmen verbunden sein können. In den Suchergebnissen haben Unternehmen und Personen unterschiedliche Symbole.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results"></a>Werden in den Ergebnissen Kontakte einer Geschäftsbeziehung angezeigt?

Ja. Einige Kontakte können Debitoren oder Kreditoren oder beides repräsentieren. Andere Kontakte ohne definierte Geschäftsbeziehung repräsentieren normalerweise potenzielle Debitoren. Kontakte zu anderen Geschäftsbeziehungen, einschließlich aller benutzerdefinierten Beziehungen, in denen Sie [!INCLUDE [prod_short.md](includes/prod_short.md)] konfiguriert haben, wird auch in den Suchergebnissen angezeigt.

### <a name="can-i-look-up-contact-details-during-meetings"></a>Kann ich während Besprechungen nach Kontaktdaten suchen?

Ja. Sie können Kontaktinformationen, den Verlauf der Interaktion und zugehörige Dokumente für Ihren Debitoren oder Kreditoren während einer Teambesprechung oder eines Anrufs während der Besprechung abrufen, ohne die Teams zu verlassen.

Über das Befehlsfeld können Sie von überall in Teams aus nach Kontaktdaten suchen. Sie können beispielsweise die Kontaktdaten im Teamkalender nachschlagen, um Besprechungen einzurichten.

### <a name="how-do-i-view-my-last-interactions-with-a-contact"></a>Wie sehe ich meine letzten Interaktionen mit einem Kontakt?

Das Detailfenster für einen Kontakt zeigt Interaktionsprotokolleinträge an. Die Interaktionsprotokolleinträge enthalten den Verlauf der Interaktionen, die Ihre Organisation mit dem jeweiligen Kontakt hatte. Die Interaktionen können E-Mails, die Sie ausgetauscht haben, Anrufe, die Sie erhalten haben, oder Dokumente, die Sie gesendet haben, umfassen.

Damit Interaktionen angezeigt werden, muss [!INCLUDE [prod_short.md](includes/prod_short.md)] konfiguriert sein, um Interaktionen zu verfolgen. Weitere Informationen zum Protokollieren von Interaktionen finden Sie unter [Aktivitäten mit Kontakten aufzeichnen](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction"></a>Wie registriere ich einen Teamanruf oder ein Meeting als Interaktion?

Suchen Sie im Detailfenster für einen Kontakt die Aktion **Interaktion erstellen**, und wählen Sie aus den eingehenden oder ausgehenden Anrufen als Interaktionsvorlagen. Sie können auch Ihre eigenen benutzerdefinierten Interaktionsvorlagen erstellen, die speziell für Teamkonversationen verwendet werden.

### <a name="can-i-call-a-contact-from-the-prod_shortmd-app-for-teams"></a>Kann ich einen Kontakt von der [!INCLUDE [prod_short.md](includes/prod_short.md)]-App für Teams anrufen?

[!INCLUDE [prod_short.md](includes/prod_short.md)] hat eine eingeschränkte Integration in Team-Anruffunktionen. Es ist nicht möglich, einen VOIP-Anruf sofort über die Kontaktkarte oder das Fenster mit den Kontaktdetails zu starten. Wenn Sie jedoch die Kontaktdetails in der Team-Desktop-App anzeigen, können Sie das Feld Telefonnummer auswählen, um diese Nummer zu wählen, wenn Teams als Standard-Wahl-App auf Ihrem Gerät eingerichtet ist. Um Festnetz- oder Mobiltelefonnummern mit PSTN, dem herkömmlichen Telefonsystem, zu wählen, benötigen Teams die Microsoft 365 Business Voice-App. Weitere Informationen finden Sie unter [Was ist Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor"></a>Wie kann ich aktuelle Dokumente für einen Debitor oder Kreditor anzeigen?

[!INCLUDE [prod_short.md](includes/prod_short.md)] bezieht sich in der Regel auf einen Kontakt mit einem Debitor- oder Kreditordatensatz, der wiederum mit Geschäftsvorfallsdatensätzen wie Angeboten oder Kaufrechnungen verknüpft ist. Um verwandte Dokumente für einen Kontakt anzuzeigen, gehen Sie zum Detailfenster für den Kontakt und wählen Sie den Feldwert **Geschäftsbeziehung** aus, oder verwenden Sie die Aktionen, um zum zugeordneten Debitor oder Kreditor zu navigieren. Erweitern Sie auf der Debitor- oder Kreditorseite den Infoboxbereich, um Statistiken für verschiedene Dokumente anzuzeigen, in die Sie einen Drilldown durchführen können. Ihre Erfahrung kann aufgrund Ihrer Anpassungen und Personalisierung abweichen.

### <a name="how-do-i-search-for-contacts-using-special-characters"></a>Wie suche ich mit Sonderzeichen nach Kontakten?

Sie können Suchkriterien mit fast allen Unicode-Zeichen eingeben. Jedoch behält sich [!INCLUDE [prod_short.md](includes/prod_short.md)] folgende Symbole für andere Zwecke vor: **=**, **.**, **\**_, and _*@**. Wenn Sie diese Symbole in Ihren Suchbegriffen verwenden, werden möglicherweise nicht die erwarteten Ergebnisse zurückgegeben. Wenn Sie nicht die erwarteten Ergebnisse sehen, schließen Sie die Symbole in Ihren Suchbegriffen in einfache Anführungszeichen ein, zum Beispiel **Contoso'='2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company"></a>Wie kann ich nach Kontakten suchen, die in einem anderen Unternehmen gespeichert sind?

Die [!INCLUDE [prod_short.md](includes/prod_short.md)]-App für Teams kann jeweils in einem Unternehmen nach Debitoren, Kreditoren und anderen Kontakten suchen.  
Um nach Kontakten zu suchen, die in einem anderen [!INCLUDE [prod_short.md](includes/prod_short.md)]-Unternehmen gespeichert sind, öffnen Sie [Einstellungen](across-teams-settings.md), dann ändern Sie die Umgebung und das Unternehmen von dort.

### <a name="are-prod_shortmd-contacts-different-than-the-ones-in-the-teams-contacts-screen"></a>Sind [!INCLUDE [prod_short.md](includes/prod_short.md)]-Kontakte anders als die auf dem Bildschirm „Teamkontakte“?

Ja. Kontakte, die in [!INCLUDE [prod_short.md](includes/prod_short.md)] gespeichert sind, stellen Geschäftskontakte dar, die Ihrer Organisation zur Verfügung stehen. Dies sind Kontakte, mit denen Sie eine etablierte und klar definierte Geschäftsbeziehung haben, oder Kontakte, die potenzielle Debitoren repräsentieren. Diese Kontakte sind normalerweise externe Kontakte. Im Vergleich dazu sind die in der Kontaktliste Team-Anrufkontakte Ihre eigenen Kontakte. Diese Kontakte werden nicht unbedingt mit anderen in Ihrer Organisation geteilt und repräsentieren normalerweise Kontakte innerhalb Ihrer Organisation.

### <a name="does-prod_shortmd-synchronize-contacts-with-teams"></a>Synchronisiert [!INCLUDE [prod_short.md](includes/prod_short.md)] Kontakte mit Teams?

Anzahl Kontakte gespeichert in [!INCLUDE [prod_short.md](includes/prod_short.md)] bleiben getrennt von Ihren in Teams gespeicherten Kontakten.
Derzeit ist nicht geplant, die beiden Listen miteinander zu synchronisieren.

### <a name="what-is-the-minimum-version-of-prod_shortmd-for-contact-search"></a>Was ist die Mindestversion von [!INCLUDE [prod_short.md](includes/prod_short.md)] für die Kontaktsuche?

Für die Kontaktsuche müssen Sie [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams Version 1.0.4 oder höher installiert haben, mit der Sie eine Verbindung zu [!INCLUDE [prod_short.md](includes/prod_short.md)]-Umgebungen ab Version 18 herstellen.

### <a name="can-i-search-from-my-mobile-device"></a>Kann ich von meinem mobilen Gerät aus suchen?

Die Kontaktsuche ist bei Teams für iOS und Teams für Android in diesem Moment nicht verfügbar.

### <a name="which-permissions-do-i-need-for-contact-search"></a>Welche Berechtigungen benötige ich für die Kontaktsuche?

Um nach Kontakten zu suchen, benötigen Sie die Berechtigung auf Objektebene für die Tabelle **Kontakte** innerhalb des Unternehmens [!INCLUDE [prod_short.md](includes/prod_short.md)], das durchsucht wird. Um das Detailfenster für einen Kontakt anzuzeigen, benötigen Sie mindestens die Leseberechtigung für die Seite **Kontakt** innerhalb des Unternehmens [!INCLUDE [prod_short.md](includes/prod_short.md)] und allen anderen verwandten Objekte.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin"></a>Kann ich die Kontaktsuche verwenden, wenn ich ein delegierter Administrator bin?

Ja. Sie können auch Kontakte und Kontaktdaten nachschlagen, wenn Sie eine delegierte Administratorrolle in einer Organisation haben.

### <a name="is-contact-search-affected-by-api-limits"></a>Ist die Kontaktsuche von API-Grenzwerten betroffen?

Ja. Die Suche nach Kontakten aus Teams basiert auf [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0-APIs und vorbehaltlich etwaiger API-Beschränkungen, die die Verwendung verwalten. Weitere Informationen zu den Grenzen finden Sie unter [Aktuelle API-Limits](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app"></a>Warum werde ich manchmal gebeten, die App einzurichten?

Nachdem Sie sich bei der [!INCLUDE [prod_short.md](includes/prod_short.md)]-App für Teams zum ersten Mal angemeldet haben, versucht die App, Ihr bevorzugtes Unternehmen in [!INCLUDE [prod_short.md](includes/prod_short.md)] zu bestimmen. Wenn die App das Unternehmen nicht bestimmen kann, müssen Sie möglicherweise zu **Einstellungen** wechseln und das Unternehmen auswählen, in dem Sie suchen möchten. Diese Situation tritt beispielsweise auf, wenn Sie in verschiedenen Umgebungen Ihres Unternehmens Zugriff auf mehrere Unternehmen haben. In diesem Fall müssen Sie ein Unternehmen auswählen, bevor Sie mit der Suche beginnen können.  

Die App kann Sie auch auffordern, die **Einstellungen** zu besuchen, wenn Sie kein [!INCLUDE [prod_short.md](includes/prod_short.md)]-Abonnement haben, es keine [!INCLUDE [prod_short.md](includes/prod_short.md)]-Umgebungen gibt oder Ihr Konto keine [!INCLUDE [prod_short.md](includes/prod_short.md)]-Lizenz hat.

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams"></a>Ich möchte nach Elementen oder Datensätzen aus anderen Tabellen suchen. Kann ich das von Teams aus machen?

Das Suchen in anderen Tabellen ist derzeit nicht möglich. Die [!INCLUDE [prod_short.md](includes/prod_short.md)]-App für Teams sucht nur in der [!INCLUDE [prod_short.md](includes/prod_short.md)]-Kontaktliste, die Kreditoren, Debitoren und andere Kontakte enthalten kann.

Wenn Sie möchten, dass die Suchfunktionen auch andere Tabellen enthalten, empfehlen wir unserer Community, eine Idee hinzuzufügen oder für vorhandene Ideen bei https://aka.ms/BusinessCentralIdeas zu stimmen.

## <a name="work-with-cards"></a>[Arbeiten mit Karten](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>Welche Arten von Links unterstützt die App?

Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams reagiert auf die meisten [!INCLUDE [prod_short.md](includes/prod_short.md)] Webclient-Links. Wenn sich der Link auf einen einzelnen Datensatz auf einer Seite bezieht, werden auf der Karte Felder für diesen Datensatz angezeigt. Die unterstützten Seitentypen umfassen: 

- Kartenseiten, z. B. die Artikelkarte
- Dokumentenseiten, z. B. das Kundenauftragsdokument
- ListPlus-Seiten, die einen einzelnen Datensatz darstellen, der aus anderen Datensätzen besteht, z. B. einen Kontoauszug
- Einfache Listenseiten, auf denen ein Datensatz nicht die Möglichkeit bietet, einen Drilldown in eine separate Detailseite auszuführen, z. B. die Liste der Postleitzahlen

Beim Einfügen eines Links in die Root-Webclient-URL wie https://businesscentral.dynamics.com zeigt die Karte stattdessen Informationen an, um neuen Benutzern den Einstieg in [!INCLUDE [prod_short.md](includes/prod_short.md)] zu erleichtern.

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>Wie lösche ich eine Karte, die ich an einen Chat gesendet habe?

Sie können eine Karte, die Sie bereits zum Chat gesendet haben, nicht löschen. Sie können jedoch die gesamte Nachricht löschen, zu der die Karte gehört.

Als Nachrichtenautor können Sie alle Nachrichten löschen, die Sie an Chats mit einer Person, einer Gruppe oder einem Kanal gesendet haben&mdash;es sei denn, Ihr Administrator hat Richtlinien eingerichtet, die das Löschen von Nachrichten verhindern. Wenn Sie einen Kanal als Kanalbesitzer moderieren, hat Ihnen Ihr Administrator möglicherweise auch die Berechtigung erteilt, alle Nachrichten im Kanal zu löschen, einschließlich der von anderen Benutzern gesendeten Nachrichten.

Durch das Löschen einer Nachricht, die eine Karte enthält, werden keine Daten in [!INCLUDE [prod_short.md](includes/prod_short.md)] gelöscht oder beeinflusst.

### <a name="do-cards-always-show-up-to-date-information"></a>Zeigen Karten immer aktuelle Informationen?

Anzahl Die Feldwerte auf einer Karte in Teams, einschließlich aller Bilder, basieren auf den Daten, die verfügbar waren, als diese Karte an den Chat gesendet wurde. [!INCLUDE [prod_short.md](includes/prod_short.md)] Karten werden in Teams nicht automatisch aktualisiert. 

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>Werden andere meine Karte sehen, wenn sie [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams nicht installiert haben? 

Wenn Sie eine Nachricht verfassen und an den Chat senden, die eine Karte enthält, sehen alle Benutzer die Karte,&mdash;auch wenn sie die [!INCLUDE [prod_short.md](includes/prod_short.md)]-App für Teams nicht installiert haben.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>Wie finde ich heraus, zu welcher Firma eine Karte in Teams gehört?

Wenn Sie über [!INCLUDE [prod_short.md](includes/prod_short.md)]-Unternehmen hinweg arbeiten, sprechen Sie mit Ihrem Administrator über die Aktivierung eines Unternehmensausweises für jedes Unternehmen. Wenn diese Option aktiviert ist, wird dieser auffällige Hinweis in jedem Detailfenster in Teams angezeigt und zeigt das Unternehmen und die Umgebung an, zu denen der Datensatz gehört. Informationen zum Einrichten eines Firmenausweises finden Sie unter [Anzeigen eines Firmenausweises für den schnellen Zugriff auf Firmeninformationen](ui-change-basic-settings.md#badge).

## <a name="work-with-card-details"></a>[Mit Kartendetails arbeiten](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Wo befindet sich die Schaltfläche Speichern im Detailfenster in Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] speichert automatisch Änderungen, die Sie an einem Feld vornehmen, sobald Sie das Feld verlassen. Um ein Feld zu verlassen, klicken/tippen Sie auf eine beliebige Stelle außerhalb des Felds oder verwenden Sie die Tabulatortaste, um zum nächsten Feld zu gelangen. Wenn Daten in einem Dialogfeld im Detailfenster angezeigt werden, müssen Sie möglicherweise die Schaltfläche **OK** auswählen, um [!INCLUDE [prod_short.md](includes/prod_short.md)] Änderungen zu speichern.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Wenn ich Details für eine Karte anzeigen möchte, sehen andere Benutzer mein Detailfenster?

Anzahl Während jeder im Chat oder Meeting die Karte selbst anzeigen kann, wird das Detailfenster nur dann auf Ihrem Gerät angezeigt, wenn Sie **Einzelheiten** auswählen. Andere Benutzer müssen wählen **Einzelheiten** auswählen, wenn sie das Detailfenster auf ihrem Gerät anzeigen möchten.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kann ich einen Teamanruf über das Detailfenster in Teams starten?

Ja. Wenn Sie die Teams-Desktop-App verwenden, können einen Anruf starten, indem Sie die verknüpfte Wählnummer in einem Telefonnummernfeld auswählen, wie zum Beispiel die **Mobiltelefonnr.** im Feld auf der Karte **Kontakt**. Teams muss Ihre festgelegte Wähl-App sein.

Um lokale oder internationale Festnetz‑ und Mobiltelefone von Teams aus anrufen zu können, benötigen Sie eine Business Voice-Lizenz für Unternehmensanrufe. Außerdem müssen Sie Teams als Anruflösung einrichten. Weitere Informationen finden Sie unter [Planen Sie die Sprachlösung Ihres Teams](/microsoftteams/cloud-voice-landing-page) in der Teamdokumentation.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kann ich Dokumente aus dem Detailfenster in Teams drucken?

Ja. Sie drucken Berichte und andere Dokumente mit den normalen [!INCLUDE [prod_short.md](includes/prod_short.md)] Druckfunktionen und allen Cloud-fähigen Drucker, die im Internet konfiguriert sind auf der Seite **Druckerverwaltung** unter [!INCLUDE [prod_short.md](includes/prod_short.md)]. Sie können nicht von Teams auf lokale Drucker drucken, die Ihrem Clientgerät bekannt sind, z. B. Drucker, auf denen Sie normalerweise über Ihren Browser drucken würden. Aus diesem Grund können Sie nicht über das Berichtsvorschau-Fenster drucken, sondern nur von der Hauptseite für Berichtsanforderungen direkt auf Ihren Cloud-Druckern.

Weitere Informationen zum Einrichten von Cloud-Druckern finden Sie unter [Drucker einrichten](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Kann ich über das Detailfenster in Teams auf die Kamera zugreifen?

Ja. [!INCLUDE [prod_short.md](includes/prod_short.md)] Funktionen im Detailfenster, die die Kamera verwenden, sind auf allen Team-Clients verfügbar.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Kann ich über das Detailfenster in Teams auf meinen Standort zugreifen?

Wenn Sie Funktionalität in [!INCLUDE [prod_short.md](includes/prod_short.md)] verwenden, die auf Ihre aktuellen Standortkoordinaten zugreifen können, z. B. mit Karten, müssen Sie Teams im Browser oder in der mobilen Team-App verwenden. Der Standort ist bei Verwendung der Team-Desktop-App nicht verfügbar. 

## <a name="collaborate-with-guests"></a>[Mit Gästen zusammenarbeiten](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kann ich Karten mit Benutzern außerhalb meiner Organisation teilen?

Ja. Wenn Sie eine Nachricht verfassen und senden, die eine Karte enthält, sehen alle Empfänger im Chat die Karte&mdash;selbst wenn sie Gäste oder außerhalb Ihrer Organisation sind. Gäste können das Detailfenster auch öffnen, wenn ihnen die Berechtigung zum Zugriff auf diese Daten erteilt wurde in [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Ist die Erfahrung für Benutzer, die Gäste sind, anders?

Ja. Wenn Sie Gastbenutzer von außerhalb Ihrer Organisation zur Teilnahme am Chat oder einem Kanal einladen, erhalten sie eine ähnliche, aber nicht identische Erfahrung im Vergleich zu Benutzern in Ihrer Organisation. Wenn ein Gast eine Nachricht mit einer Karte erhält, kann er diese anzeigen. Gastbennutzer können das Detailfenster auch öffnen, wenn ihnen die Berechtigung zum Zugriff auf diese Daten erteilt wurde in [!INCLUDE [prod_short.md](includes/prod_short.md)] und eine [!INCLUDE [prod_short.md](includes/prod_short.md)] Lizenz innerhalb Ihrer Organisation zugeweisen wurde. Wenn ein Gast eine Nachricht verfasst, werden Links zu Ihrer [!INCLUDE [prod_short.md](includes/prod_short.md)] oder ihrer nicht in Karten erweitert.

Weitere Informationen zu Ähnlichkeiten und Unterschieden zwischen Gästen und Teammitgliedern finden Sie unter [Gästeerfahrung in Teams](/MicrosoftTeams/guest-experience) in der Teamdokumentation.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Wie installiert ein Gastbenutzer die [!INCLUDE [prod_short.md](includes/prod_short.md)] App? 

Gäste haben keinen Zugriff auf den App-Marktplatz, um Apps selbst zu installieren. Die App kann jedoch basierend auf den Richtlinien Ihres Unternehmens automatisch für sie installiert werden. Eine andere Möglichkeit für einen Gastbenutzer, die [!INCLUDE [prod_short.md](includes/prod_short.md)] App zu installieren ist, wenn sie eine Chat-Nachricht erhalten, die eine [!INCLUDE [prod_short.md](includes/prod_short.md)] Karte enthält. In diesem Fall wählt der Benutzer die Schaltfläche **Einzelheiten** oder das Menü auf der Karte und installiert dann die [!INCLUDE [prod_short.md](includes/prod_short.md)] App zur Verwendung mit Ihrer Organisation. Nach der Installation der App erhält ein Benutzer nicht automatisch die Berechtigung, auf Daten von Ihnen zuzugreifen [!INCLUDE [prod_short.md](includes/prod_short.md)].

## <a name="share-to-teams"></a>[Freigeben an Teams](#tab/share)

### <a name="does-share-to-teams-send-a-compact-card"></a>Versendet Teilen über Teams eine kompakte Karte? 

Derzeit wird nur ein Deep Link zu der Seite freigegeben. Die Empfänger sehen in Ihrer Nachricht einen Hyperlink, den sie auswählen können, um in einem separaten Browserfenster zu [!INCLUDE [prod_short.md](includes/prod_short.md)] zu gelangen. 

### <a name="will-recipients-receive-the-message-from-me-or-from-a-business-central-service-account"></a>Erhalten die Empfänger die Nachricht von mir oder von einem Business Central Servicekonto? 

Wenn Sie die Funktion Für Teams freigeben verwenden, wird die Nachricht an eine Person, eine Gruppe oder einen Kanal gesendet, ähnlich wie wenn Sie die Nachricht selbst von Microsoft Teams aus gesendet hätten. Die Empfänger sehen die Nachricht von Ihnen in ihrem bevorzugten Teams Client und können wie gewohnt auf eine Nachricht von Ihnen reagieren und antworten. 

### <a name="is-share-to-teams-available-in-business-central-on-premises"></a>Ist „Share über Teams“ in Business Central On-Premises verfügbar? 

Anzahl Ähnlich wie bei der App [!INCLUDE [prod_short.md](includes/prod_short.md)] für Teams ist diese Funktion nur für den Web Client in [!INCLUDE [prod_short.md](includes/prod_short.md)] online verfügbar. Es ist nicht geplant, [!INCLUDE [prod_short.md](includes/prod_short.md)] Bereitstellungsarten &mdash;wie on-premises, Hybrid Cloud oder Private Cloud &mdash;zu unterstützen, die Microsoft nicht direkt hostet oder verwaltet.

### <a name="does-share-to-teams-grant-permissions-to-recipients"></a>Gewährt Teilen über Teams den Empfängern Berechtigungen? 

Anzahl Wenn Sie mit einer Person, einer Gruppe oder einem Kanal teilen, bleiben die Berechtigungen davon unberührt. Benutzer, die bereits die Berechtigung haben, die Seite und die Daten zu sehen, auf die der Link verweist, können dies tun. Benutzer, die keine Berechtigung zum Anzeigen der Seite und der Daten haben oder nicht über eine [!INCLUDE [prod_short.md](includes/prod_short.md)]-Lizenz verfügen, erhalten eine Fehlermeldung. 
 
### <a name="must-i-have-the-teams-desktop-app-installed-to-use-share-to-teams"></a>Muss ich die Teams Desktop App installiert haben, um Share über Teams nutzen zu können? 

Anzahl Alles, was Sie brauchen, ist ein gültiges Konto, das Zugriff auf Microsoft Teams hat. 

### <a name="is-share-to-teams-available-in-all-business-central-clients"></a>Ist Teilen über Teams in allen Business Central Clients verfügbar? 

Zurzeit ist „Teilen über Teams“ ausschließlich im Desktop Web Client und im Detailfenster von Teams verfügbar.  

### <a name="where-do-i-find-share-to-teams-in-business-central"></a>Wo finde ich die Funktion Für Teams freigeben in Business Central? 

Die Aktion **Für Teams freigeben** finden Sie im Menü **Freigeben** auf allen Seiten, wie Karten- und Belegseiten, Listen- oder Arbeitsblattseiten, einschließlich angepasster Seiten. Die Aktion ist nicht verfügbar auf Dialogfeldern oder Seiten, die als Dialogfelder angezeigt werden, wie Nachschlagefelder oder Assistenten.

---
## <a name="see-also"></a>Weitere Informationen

[[!INCLUDE [prod_short](includes/prod_short.md)] und Microsoft Teams Integration Übersicht](across-teams-overview.md)  
[Installieren Sie die [!INCLUDE [prod_short](includes/prod_short.md)] App für Microsoft Teams](across-install-app-for-teams.md)  
[Suchen Sie nach Debitoren, Kreditoren und anderen Kontakten aus Microsoft Teams](across-search-contacts-teams.md)  
[Datensätze in Microsoft Teams freigeben](across-working-with-teams.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Ändern von Firmen- und anderen Einstellungen in Teams](across-teams-settings.md)  
[Entwickeln für Teams Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]