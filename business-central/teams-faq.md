---
title: Teams FAQ
description: Hier erhalten Sie Antworten auf einige typische Fragen zur Arbeit mit Teams und Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 01/26/2021
ms.author: jswymer
ms.openlocfilehash: 79b6069ffb4c73d783b2c05d3a44a55763805a52
ms.sourcegitcommit: 1c9eec7554305603d688bf85ce3986d0b1f72ede
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "5068434"
---
# <a name="teams-faq"></a>Teams FAQ

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel beantwortet einige der Fragen, die Sie möglicherweise zur Arbeit mit Teams und [!INCLUDE [prod_short](includes/prod_short.md)] haben.

## <a name="general"></a>[Allgemein](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Wie melde ich mich bei der [!INCLUDE [prod_short.md](includes/prod_short.md)] App in Teams an? 

Nach der Installation der App werden Sie aufgefordert, sich beim ersten Einfügen von einem [!INCLUDE [prod_short.md](includes/prod_short.md)] Link in den Team-Chat oder wenn Sie die Aktion **Einzelheiten** auf einer Karte in Teams auswählen, anzumelden. Abhängig von Ihrem Team-Client müssen Sie möglicherweise Ihre Anmeldeinformationen eingeben, um auf [!INCLUDE [prod_short.md](includes/prod_short.md)] zuzugreifen. 

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Wie melde ich mich bei der [!INCLUDE [prod_short.md](includes/prod_short.md)] App in Teams ab? 

So melden Sie sich von Ihrer aktuellen Benutzeridentität mit der Sie eine Verbindung zu [!INCLUDE [prod_short.md](includes/prod_short.md)] hergestellt haben, ab. Gehen Sie zu einem beliebigen Chat-Erstellungsfeld und wählen Sie das [!INCLUDE [prod_short.md](includes/prod_short.md)] Symbol darunter. Wenn das Fenster angezeigt wird, überprüfen Sie Ihre aktuell angemeldete Identität und wählen Sie dann **Abmelden** . Wenn Sie Teams im Browser verwenden, werden Sie auch von allen [!INCLUDE [prod_short.md](includes/prod_short.md)] Webclients im selben Browserfenster abgemeldet.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>Stellt die App für Teams eine Verbindung zu [!INCLUDE [prod_short.md](includes/prod_short.md)] lokal her? 

Anzahl Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams funktioniert nur mit [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Es gibt keine Pläne, um die [!INCLUDE [prod_short.md](includes/prod_short.md)] Bereitstellungstypen&mdash;wie lokal, Hybrid Cloud oder Private Cloud&mdash;die Microsoft nicht direkt hostet oder verwaltet, bereitzustellen.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Funktioniert die App mit mehreren Unternehmen und Umgebungen? 

Ja. Wenn die App [!INCLUDE [prod_short.md](includes/prod_short.md)] einen Link in eine Karte erweitert, muss der Link die Umgebung und den Firmennamen enthalten, damit die App mit dem Datensatz in der richtigen Firma übereinstimmt. Sie können Links zu allen Unternehmen und Umgebungen einfügen, auf die Sie innerhalb Ihres Unternehmens und über das Konto [!INCLUDE [prod_short.md](includes/prod_short.md)], mit dem Sie sich angemeldet haben, Zugriff haben. Teilnehmer des Chats sehen die Karte. Sie können die Kartendetails jedoch nur anzeigen, wenn sie über Berechtigungen für das Unternehmen oder die Umgebung verfügen, in der dieser Datensatz gespeichert ist.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>In welchen Ländern oder Regionen ist die [!INCLUDE [prod_short.md](includes/prod_short.md)] App verfügbar? 

Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams ist nicht auf ein Land oder Region beschränkt. Die App ist in allen Märkten verfügbar, die derzeit vom Teams Marktplatz unterstützt werden. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Funktioniert die [!INCLUDE [prod_short.md](includes/prod_short.md)] App mit jeder Lokalisierung von [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. Die App soll mit jeder Lokalisierung von [!INCLUDE [prod_short.md](includes/prod_short.md)] funktionieren, unabhängig davon, ob diese Lokalisierung direkt von Microsoft oder über einen Partner angeboten wird. Weitere Informationen finden Sie unter [Verfügbarkeit nach Ländern/Regionen und unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Welche Sprachen [!INCLUDE [prod_short.md](includes/prod_short.md)] unterstützt die App?
<!--TODO Run by Mike -->

Zwei Dinge bestimmen die Sprache für Karten und Kartendetails in Teams:

1. Ihre Sprache in Teams, die Sie in Ihren Kontoeinstellungen in Teams sehen können. 
2. Ihre Sprache in [!INCLUDE [prod_short.md](includes/prod_short.md)], die Sie im [!INCLUDE [prod_short.md](includes/prod_short.md)] Webclient sehen können (siehe [Grundeinstellung ändern – Sprache](ui-change-basic-settings.md#language)).

In der folgenden Tabelle wird erläutert, wie sich die Erfahrung für Nachrichtenautoren und -empfänger in Abhängigkeit von den Spracheinstellungen und der Verfügbarkeit von Sprachen unterscheidet.

|Wer|Karte|Kartendetails |
|-|----|--------------| 
|Autor der Nachricht |Wird in der Sprache angezeigt, die in Teams für Sie angegeben wurde. Wenn [!INCLUDE [prod_short.md](includes/prod_short.md)] nicht die gleiche Sprache anbietet, wird die Karte in Englisch angezeigt. |Wird in der Sprache angezeigt, die für Sie in [!INCLUDE [prod_short.md](includes/prod_short.md)] angezeigt wurde.  dies kann Sprachen aus Sprach-Apps enthalten, die von Partnern bereitgestellt werden. |
|Nachrichten-Empfänger |Wird in der Sprache des Nachrichtenautors angezeigt. |Wird in der Sprache angezeigt, die für Sie in [!INCLUDE [prod_short.md](includes/prod_short.md)] angezeigt wurde. |

Für die Liste der unterstützten Sprachen für [!INCLUDE [prod_short.md](includes/prod_short.md)] gehen Sie zu [Unterstützte Sprachen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Wo finde ich die Teamintegration innerhalb des [!INCLUDE [prod_short.md](includes/prod_short.md)] Webclients? 

Derzeit gibt es keine Einbettung von Teams-Steuerelementen oder das Vorhandensein von Teams-Funktionen im [!INCLUDE [prod_short.md](includes/prod_short.md)] Web-Client oder anderen Clients.  

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>Funktioniert [!INCLUDE [prod_short.md](includes/prod_short.md)] mit der mobilen App von Teams?

Ja. Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App kann über die Team-Desktop-App oder den Browser oder von einem Administrator für alle Benutzer installiert werden. Nach der Installation wird die [!INCLUDE [prod_short.md](includes/prod_short.md)] App automatisch in Teams für iOS und Android verfügbar. Auf Mobilgeräten können Sie von anderen gesendete Karten anzeigen, auf Details zugreifen oder die Karte hervorheben, um die volle Erfahrung in der [!INCLUDE [prod_short.md](includes/prod_short.md)] App zur Verfügung zu haben. Sie können jedoch keine Links einfügen, die beim Verfassen von Nachrichten zu Karten erweitert werden. Mindestanforderungen für Mobiltelefone finden Sie unter [Mindestanforderungen für die Verwendung von Business Central](product-requirements.md).

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

- Auf die Kamera und den Standort kann nicht über das Detailfenster in der Team-Desktop-App zugegriffen werden 
- Beim Verwenden von Microsoft Edge mit Teams im Browser können Sie problemlos über mehrere Identitäten und Konten hinweg arbeiten, indem Sie sich bei Teams aus verschiedenen Profilen anmelden. Erfahren Sie mehr über die Verwendung von Profilen in Microsoft Edge unter [Melden Sie sich an und erstellen Sie mehrere Profile in Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) auf Microsoft Support.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Was ist der beste Weg für mich, um [!INCLUDE [prod_short.md](includes/prod_short.md)] und Microsoft Teams potenziellen Kunden zu zeigen?

Wenn Sie ein Wiederverkaufspartner sind, möchten Sie möglicherweise eine Umgebung, in der Sie potenzielle Kunden im Rahmen von Vorverkaufsdemonstrationen anzeigen können. Um Auswirkungen auf Microsoft Teams in Ihrer Organisation zu vermeiden, erhalten Sie ein Microsoft 365-Demokonto unter [https://aka.ms/CDX](https://aka.ms/CDX). Mit diesem Konto haben Sie die volle Kontrolle über eine unabhängige Azure-Organisation, die Microsoft Teams und [!INCLUDE [prod_short.md](includes/prod_short.md)] umfasst. Weitere Informationen finden Sie unter [Vorbereiten von Demonstrationsumgebungen von Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>Nimmt die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams meine Anpassung und Personalisierung vor?

Die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams kann Karten für Links zu Kundenseiten und Tabellen in [!INCLUDE [prod_short.md](includes/prod_short.md)] anzeigen, wie Seiten und Tabellen, die von Ihren eigenen benutzerdefinierten Erweiterungen oder von AppSource stammen.

Die Felder, die in Teams auf einer Karte angezeigt werden, können ebenfalls von [!INCLUDE [prod_short.md](includes/prod_short.md)] Anpassungen betroffen sein, die für Ihre Organisation installiert sind. Karten berücksichtigen keine rollenspezifischen Anpassungen oder Benutzerpersonalisierung. Das Fenster mit den Kartendetails zeigt jedoch die Datensatzdetails so an, wie Sie sie sehen würden in [!INCLUDE [prod_short.md](includes/prod_short.md)], einschließlich aller Erweiterungen, Rollenanpassungen und Benutzerpersonalisierung.

### <a name="where-can-i-learn-about-my-privacy"></a>Wo kann ich etwas über meine Privatsphäre erfahren? 

Informationen dazu, wie Microsoft mit Ihren Daten umgeht, finden Sie in der [Microsoft-Datenschutzerklärung](https://go.microsoft.com/fwlink/?linkid=2030602). 

Wenden Sie sich an Ihren Administrator, um zu erfahren, wie Ihre Organisation mit dem Datenschutz Ihrer Daten umgeht. 

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Wie deinstalliere ich die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams? 

Um die App zu entfernen, die Sie für sich selbst installiert haben, gehen Sie zu einem beliebigen Chat-Erstellungskästchen und suchen Sie das [!INCLUDE [prod_short.md](includes/prod_short.md)] Symbol. Klicken Sie mit der rechten Maustaste auf das Symbol und wählen Sie Deinstallieren.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Wird Microsoft die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams weiter verbessern?

Bei Microsoft achten wir stets auf das Feedback aus unsere breitgefächerte Benutzer-Community und reagieren auf die häufigsten Vorschläge. Um zu erfahren, was als nächstes für die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams geplant ist, gehen Sie zu [Dynamics 365-Release-Plan](https://aka.ms/dynamics365releaseplan).

Wenn Sie an der Verbesserung der App für Teams teilnehmen möchten oder eine großartige Idee haben, die Ihre Arbeit oder Ihre Erfahrungen in der Zusammenarbeit in Teams vereinfacht, fügen Sie eine Idee hinzu oder stimmen Sie für vorhandene Ideen ab unter [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="working-with-cards"></a>[Arbeiten mit Karten](#tab/cards)

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

Wenn Sie eine Nachricht verfassen und an den Chat senden, die eine Karte enthält, sehen alle Benutzer die Karte, auch wenn sie die [!INCLUDE [prod_short.md](includes/prod_short.md)] App für Teams nicht installiert haben.

## <a name="working-with-card-details"></a>[Arbeiten mit Kartendetails](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Wo befindet sich die Schaltfläche Speichern im Detailfenster in Teams? 

[!INCLUDE [prod_short.md](includes/prod_short.md)] speichert automatisch Änderungen, die Sie an einem Feld vornehmen, sobald Sie das Feld verlassen. Um ein Feld zu verlassen, klicken/tippen Sie auf eine beliebige Stelle außerhalb des Felds oder verwenden Sie die Tabulatortaste, um zum nächsten Feld zu gelangen. Wenn Daten in einem Dialogfeld im Detailfenster angezeigt werden, müssen Sie möglicherweise die Schaltfläche **OK** auswählen, um [!INCLUDE [prod_short.md](includes/prod_short.md)] Änderungen zu speichern.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Wenn ich Details für eine Karte anzeigen möchte, sehen andere Benutzer mein Detailfenster? 

Anzahl Während jeder im Chat die Karte selbst anzeigen kann, wird das Detailfenster nur dann auf Ihrem Gerät angezeigt, wenn Sie **Einzelheiten** auswählen. Andere Benutzer müssen wählen **Einzelheiten** auswählen, wenn sie das Detailfenster auf ihrem Gerät anzeigen möchten.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kann ich einen Teamanruf über das Detailfenster in Teams starten? 

Ja. Sie können einen Anruf starten, indem Sie die verknüpfte Wählnummer in einem Telefonnummernfeld auswählen, wie zum Beispiel die **Mobiltelefonnummer** im Feld auf der Karte **Kontakt**. Teams muss Ihre festgelegte Wähl-App sein.

Um lokale oder internationale Festnetz- und Mobiltelefone von Teams aus anrufen zu können, benötigen Sie eine Teamlizenz für Unternehmensanrufe. Außerdem müssen Sie Teams als Anruflösung einrichten. Weitere Informationen finden Sie unter [Planen Sie die Sprachlösung Ihres Teams](/microsoftteams/cloud-voice-landing-page) in der Teamdokumentation.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kann ich Dokumente aus dem Detailfenster in Teams drucken? 

Ja. Sie drucken Berichte und andere Dokumente mit den normalen [!INCLUDE [prod_short.md](includes/prod_short.md)] Druckfunktionen und allen Cloud-fähigen Drucker, die im Internet konfiguriert sind auf der Seite **Druckerverwaltung** unter [!INCLUDE [prod_short.md](includes/prod_short.md)]. Sie können nicht von Teams auf lokale Drucker drucken, die Ihrem Clientgerät bekannt sind, z. B. Drucker, auf denen Sie normalerweise über Ihren Browser drucken würden. Aus diesem Grund können Sie nicht über das Berichtsvorschau-Fenster drucken, sondern nur von der Hauptseite für Berichtsanforderungen direkt auf Ihren Cloud-Druckern.

Weitere Informationen zum Einrichten von Cloud-Druckern finden Sie unter [Drucker einrichten](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Kann ich über das Detailfenster in Teams auf die Kamera zugreifen? 

Ja. [!INCLUDE [prod_short.md](includes/prod_short.md)] Funktionen im Detailfenster, die die Kamera verwenden, sind auf allen Team-Clients verfügbar.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Kann ich über das Detailfenster in Teams auf meinen Standort zugreifen?

Wenn Sie Funktionalität in [!INCLUDE [prod_short.md](includes/prod_short.md)] verwenden, die auf Ihre aktuellen Standortkoordinaten zugreifen können, z. B. mit Karten, müssen Sie Teams im Browser oder in der mobilen Team-App verwenden. Der Standort ist bei Verwendung der Team-Desktop-App nicht verfügbar. 

## <a name="collaborating-with-guests"></a>[Mit Gästen zusammenarbeiten ](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kann ich Karten mit Benutzern außerhalb meiner Organisation teilen? 

Ja. Wenn Sie eine Nachricht verfassen und senden, die eine Karte enthält, sehen alle Empfänger im Chat die Karte&mdash;selbst wenn sie Gäste oder außerhalb Ihrer Organisation sind. Gäste können das Detailfenster auch öffnen, wenn ihnen die Berechtigung zum Zugriff auf diese Daten erteilt wurde in [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Ist die Erfahrung für Benutzer, die Gäste sind, anders?

Ja. Wenn Sie Gastbenutzer von außerhalb Ihrer Organisation zur Teilnahme am Chat oder einem Kanal einladen, erhalten sie eine ähnliche, aber nicht identische Erfahrung im Vergleich zu Benutzern in Ihrer Organisation. Wenn ein Gast eine Nachricht mit einer Karte erhält, kann er diese anzeigen. Gastbennutzer können das Detailfenster auch öffnen, wenn ihnen die Berechtigung zum Zugriff auf diese Daten erteilt wurde in [!INCLUDE [prod_short.md](includes/prod_short.md)] und eine [!INCLUDE [prod_short.md](includes/prod_short.md)] Lizenz innerhalb Ihrer Organisation zugeweisen wurde. Wenn ein Gast eine Nachricht verfasst, werden Links zu Ihrer [!INCLUDE [prod_short.md](includes/prod_short.md)] nicht in Karten erweitert.

Weitere Informationen zu Ähnlichkeiten und Unterschieden zwischen Gästen und Teammitgliedern finden Sie unter [Gästeerfahrung in Teams](/MicrosoftTeams/guest-experience) in der Teamdokumentation.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Wie installiert ein Gastbenutzer die [!INCLUDE [prod_short.md](includes/prod_short.md)] App? 

Gäste haben keinen Zugriff auf den App-Marktplatz, um Apps selbst zu installieren. Die App kann jedoch basierend auf den Richtlinien Ihres Unternehmens automatisch für sie installiert werden. Eine andere Möglichkeit für einen Gastbenutzer, die [!INCLUDE [prod_short.md](includes/prod_short.md)] App zu installieren ist, wenn sie eine Chat-Nachricht erhalten, die eine [!INCLUDE [prod_short.md](includes/prod_short.md)] Karte enthält. In diesem Fall wählt der Benutzer die Schaltfläche **Einzelheiten** oder das Menü auf der Karte und installiert dann die [!INCLUDE [prod_short.md](includes/prod_short.md)] App zur Verwendung mit Ihrer Organisation. Nach der Installation der App erhält ein Benutzer nicht automatisch die Berechtigung, auf Daten von Ihnen zuzugreifen [!INCLUDE [prod_short.md](includes/prod_short.md)].

<!--TODO - check with Mike on this -->
---

## <a name="see-also"></a>Siehe auch

[[!INCLUDE [prod_short](includes/prod_short.md)] und Microsoft Teams Integration Übersicht](across-teams-overview.md)  
[Die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Microsoft Teams installieren](across-install-app-for-teams.md)  
[Teams Problembehebung](admin-teams-troubleshooting.md)  
[Entwicklung für die Teams-Integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
