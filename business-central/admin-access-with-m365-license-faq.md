---
title: Zugriff mit Microsoft 365-Lizenzen FAQ
description: Hier erhalten Sie Antworten auf allgemeine Fragen zum Zugriff auf Business Central mit Microsoft 365-Lizenzen.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# <a name="access-with-microsoft--licenses-faq" />Zugriff mit Microsoft 365-Lizenzen FAQ

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Benutzer können mit ihrer Microsoft 365-Lizenz auf Business Central-Daten in Microsoft Teams zugreifen. Dieser Artikel beantwortet häufig gestellte Fragen von Administratoren, Beratern und anderen. Entwickler sollten sich die FAQ für Entwickler ansehen. Fragen zur Integration von Business Central mit Microsoft Teams finden Sie unter [Teams FAQ](teams-faq.md).

## [Berechtigungen](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users" />Kann ich proaktiv unterschiedliche Startberechtigungen für verschiedene Gruppen von Benutzern konfigurieren?

Zur Zeit nicht. Business Central lässt nur die Konfiguration einer Gruppe von Berechtigungen zu, die allen Microsoft 365-Benutzern zugewiesen werden, wenn sie sich zum ersten Mal bei Business Central anmelden.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in" />Kann ich proaktiv Berechtigungen, Profile und Einstellungen für einzelne Benutzer konfigurieren, bevor sie sich anmelden?

Ja. Das ist über Sicherheitsgruppen möglich. Indem Sie eine Sicherheitsgruppe auf eine Umgebung anwenden, legen Sie die Gesamtheit der Benutzer fest, die Zugriff auf diese Umgebung haben. Diese Sicherheitsgruppe kann Benutzer mit einer Business Central-Lizenz und Benutzer mit einer Microsoft 365-Lizenz umfassen. Wenn Sie das nächste Mal die Benutzer von Microsoft 365 in der Liste **Benutzer** aktualisieren, werden die Datensätze der Microsoft 365 Benutzer erstellt. Sie können dann Benutzergruppen, Berechtigungen, Profile und andere Einstellungen zuweisen, bevor sich der Benutzer angemeldet hat.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to" />Kann ich, nachdem sich ein Benutzer angemeldet hat, ändern, auf welche Objekte er Zugriff hat?

Ja. Nachdem sich ein Benutzer zum ersten Mal angemeldet hat und sein Datensatz bereitgestellt wurde, verwalten Administratoren diese Benutzer wie alle anderen Benutzer von Business Central. Sie können zum Beispiel Berechtigungen für verschiedene Objekte hinzufügen oder entfernen. Wenn Sie die Berechtigungssätze, die der Microsoft 365-Lizenz auf der Seite Lizenzkonfiguration zugewiesen sind, ändern, wirkt sich die Änderung nur auf die nächsten Benutzer aus, die sich zum ersten Mal anmelden.

### <a name="how-do-i-prevent-access-to-sensitive-tables" />Wie kann ich den Zugriff auf sensible Tabellen verhindern?

Business Central bietet ein leistungsstarkes und flexibles Berechtigungsmodell, in dem Administratoren Berechtigungssätze festlegen können, die den Zugriff auf bestimmte Objekte, Geschäftsprozesse oder ganze Rollen ermöglichen. Um den Zugriff auf sensible Tabellen zu verhindern, können Sie angepasste Berechtigungssätze erstellen, die die Berechtigung für sensible Objekte ausschließen. Weitere Informationen zum Ausschluss von Berechtigungen finden Sie unter [Erstellen eines Berechtigungssatzes](ui-define-granular-permissions.md).  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group" />Kann ich, anstatt die Lizenzkonfiguration anzupassen, eine Benutzergruppe anpassen?

Ja. Das Hinzufügen von Berechtigungssätzen zur Benutzergruppe Microsoft Teams Interne Benutzer in Business Central hat unter dem Strich denselben Effekt wie das Hinzufügen von Berechtigungssätzen zur Lizenz Microsoft 365, solange die Zuordnung der Lizenz Microsoft 365 zu dieser Benutzergruppe bestehen bleibt. Dieser Ansatz hat den zusätzlichen Vorteil, dass die Berechtigungen immer mit den Mitgliedern der Gruppe synchronisiert werden, wenn Sie die Benutzergruppe ändern.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions" />Erteilt ein Benutzer von Business Central neue Berechtigungen, wenn er einen Datensatz in Teams freigibt?

Anz. Diese Aktion ist nicht dasselbe wie das Teilen eines Links zu einem SharePoint-Dokument, bei dem die Person, die das Dokument teilt, die Berechtigung für andere erteilen kann. In Business Central können nur Administratoren Berechtigungen konfigurieren und zuweisen. Im Vergleich zur Freigabe von SharePoint-Dokumenten entspricht dies der Auswahl der Option „Für Personen mit bestehendem Zugriff freigeben“.

### <a name="does-this-feature-support-row-level-security" />Unterstützt diese Funktion die Sicherheit auf Zeilenebene?

Ja. Auch wenn eine Person, die mit ihrer Microsoft 365-Lizenz auf einen Datensatz in Teams zugreift, über die richtigen Berechtigungen für Tabellen- und Seitenobjekte verfügt, werden die Berechtigungen auf Zeilenebene durchgesetzt, wenn sie für diese Tabelle implementiert wurden.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams" />Wenn ich Berechtigungen konfiguriere, die Schreibzugriff beinhalten, können Benutzer dann in Teams schreiben?

Wenn Sie Business Central so konfigurieren, dass eine Berechtigung festgelegt wird, die den Zugriff auf ein oder mehrere Objekte zum Einfügen, Ändern oder Löschen umfasst, können Benutzer mit dieser Berechtigung auch dann nicht in Teams schreiben, wenn sie nur eine Microsoft 365-Lizenz haben. Der Business Central Service erzwingt schreibgeschützten Zugriff, unabhängig davon, welche Berechtigung Sie zum Einfügen, Ändern oder Löschen zuweisen.  

Auch wenn Business Central diesen Schutz bietet, empfehlen wir Ihnen dennoch, Berechtigungssätze mit Schreibzugriff zu vermeiden. Auf diese Weise vermeiden Sie Probleme, wenn Benutzer die Rolle wechseln oder neue Lizenzen erwerben.  

## [Einrichtung und Konfiguration](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment" />Warum ist die Einstellung zur Aktivierung des Zugriffs für meine Umgebung nicht verfügbar?

Die Aktivierung der Barrierefreiheit mit Microsoft 365-Lizenzen ist nur für Business Central Umgebungen der Plattformversion 21.1 oder höher verfügbar. Wenn Ihre Umgebung auf diese Mindestversion aktualisiert wird, wird die Einstellung automatisch verfügbar. Um die Version Ihrer Umgebung zu überprüfen, gehen Sie im Admin-Center von Business Central auf die Seite mit den Umgebungsdetails für die Umgebung. Oder melden Sie sich bei der Umgebung an und rufen Sie die Seite **Hilfe & Support** im Menü **Hilfe** auf.

### <a name="can-i-access-business-central-on-premises-with-microsoft--licenses" />Kann ich mit Microsoft 365-Lizenzen auf Business Central vor Ort zugreifen?

Nein, das wird nicht unterstützt. Business Central zeigt eine Fehlermeldung an, wenn Benutzer versuchen, in Teams auf die Datensätze von Business Central on premises zuzugreifen.

### <a name="what-is-the-employee-profile" />Was ist das Mitarbeiterprofil?

Das Profil **Mitarbeiter**, das auf der Listenseite **Profile (Rollen)** angezeigt wird, wurde mit Update 21.1 eingeführt. Es ist das Standardprofil, das Benutzern zugewiesen wird, die mit ihrer Microsoft 365-Lizenz auf Business Central zugreifen. Dieses Profil ist für Personen in einem Unternehmen gedacht, die keine bestimmte Rolle in Business Central haben und nur die Daten einsehen müssen, die für sie freigegeben wurden.

### <a name="what-is-the-teams-users-user-group" />Was ist die Benutzergruppe Teams Benutzer?

Die Gruppe **Microsoft Teams Interne Benutzer**, die auf der Seite **Benutzergruppen** angezeigt wird, wurde mit Update 21.1 eingeführt. Diese Gruppe ist die Standardbenutzergruppe für Benutzer, die mit ihrer Microsoft 365-Lizenz auf Business Central zugreifen. Die Benutzergruppe ist für Personen gedacht, die innerhalb der gleichen Organisation, in der Business Central gehostet wird, mit Microsoft Teams zusammenarbeiten.  

### <a name="do-users-that-only-have-a-microsoft--license-show-up-in-the-users-list-in-business-central" />Werden Benutzer, die nur eine Microsoft 365-Lizenz haben, in der Liste Benutzer in Business Central angezeigt?

Ja. Wenn Sie Sicherheitsgruppen auf Umgebungen anwenden, werden diese Benutzer in der Liste Benutzer angezeigt, nachdem Sie die Aktion Benutzer von Microsoft 365 aktualisieren aus der Liste **Benutzer** verwendet haben. Wenn Sie keine Sicherheitsgruppen anwenden, erscheinen die Datensätze der Benutzer in der Liste Benutzer, nachdem sie das erste Mal auf einen Business Central-Datensatz zugegriffen haben.

### <a name="does-this-feature-work-for-embed-isv-solutions" />Funktioniert diese Funktion auch für eingebettete ISV-Lösungen?

Ja. Benutzer mit nur einer Microsoft 365-Lizenz können auch auf Datensätze in Umgebungen zugreifen, die unter der Domäne *.bc.dynamics.com ausgeführt werden.

## [Lizenzierung](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central" />Kann ein Kunde diese Funktion nutzen, wenn er nicht über Business Central verfügt?

Der Zugriff auf Business Central mit einer Microsoft 365-Lizenz ist für Organisationen gedacht, die Business Central bereits abonniert haben und eine oder mehrere Business Central Umgebungen mit lizenzierten Business Central Benutzern betreiben. Sie bietet Microsoft 365-Kunden, die keinen Business Central-Plan haben, keine neuen Funktionen oder Nutzungsrechte.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization" />Wie hilft mir das bei der Verwaltung der Abonnement-Kalkulationen in meinem Unternehmen?

Um die Produktivität zu maximieren und ihre Vorgänge zu rationalisieren, kaufen KMUs häufig Dynamics 365 Business Central zusammen mit Microsoft 365. In diesem Fall erhalten die meisten Personen eine Microsoft 365-Lizenz, aber nur bestimmte Rollen oder Personen erhalten eine Business Central-Lizenz. Business Central bietet Flexibilität bei der Lizenzierung, so dass die Kunden nur für das bezahlen, was sie benötigen:

- Benutzer, die vollen Zugriff auf Business Central benötigen, erhalten in der Regel eine Business Central Essentials oder Business Central Premium Lizenz. 
- Benutzer, die einen eingeschränkten Schreibzugriff benötigen, erhalten in der Regel eine Business Central Team Member-Lizenz.
- Alle anderen Mitarbeiter im Unternehmen, die nur gelegentlich Geschäftsdaten lesen müssen, die mit ihnen geteilt werden, können dies tun, wenn sie eine Microsoft 365-Lizenz haben. Ihnen muss keine Team Member-Lizenz zugewiesen werden. Andere Lizenzierungsoptionen sind verfügbar. Weitere Informationen finden Sie in der Anleitung [Dynamics 365 Lizenzierung](https://go.microsoft.com/fwlink/?LinkId=866544).

### <a name="is-this--free-of-charge" />Ist dies zu 100% kostenlos?
 
Anz. Der Zugriff auf die Daten von Business Central in Microsoft Teams setzt voraus, dass jeder Benutzer entweder eine Business Central-Lizenz oder eine Microsoft 365-Lizenz aus der Liste der unterstützten Pläne besitzt.

### <a name="does-this-work-with-microsoft--trials-and-business-central-trials" />Funktioniert dies mit Microsoft 365-Tests und Business Central-Tests?

Ja. Wenn einem Benutzer eine Microsoft 365-Lizenz aus einem Test eines unterstützten Plans zugewiesen wird, kann er auch in Teams auf Business Central Datensätze zugreifen. Kunden können dann ausprobieren, wie Microsoft-Produktivitäts- und Business-Apps zusammenarbeiten, und Verkäufer und Berater von Partnern können diese Funktion einfach demonstrieren. Zum Beispiel können Partner ihre eigenen Azure AD-Mandanten aus [https://aka.ms/CDX](https://aka.ms/CDX) bereitstellen, die Microsoft 365-Tests und Business Central-Tests zur Demonstration von Business Central enthalten.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft--license-whats-that" />In der Liste der Lizenzen in Business Central wird eine Microsoft 365-Lizenz angezeigt. Was ist das?

Die Seite **Lizenzkonfiguration** in Business Central zeigt die verschiedenen Arten von Lizenzen an, die den Zugriff auf den Business Central-Dienst ermöglichen. In Version 21 hat Microsoft diese Liste um Microsoft 365 erweitert, um den Zugriff auf Business Central zu ermöglichen. Diese Liste von Lizenzen bedeutet nicht, dass Ihr Unternehmen Abonnements für eine dieser Lizenzen gekauft hat oder dass Ihr Unternehmen den Zugriff über diese Lizenzen aktiviert hat.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft--license-for-this-feature-to-work" />Muss ich eine neue Art von Microsoft 365-Lizenz erwerben, damit diese Funktion funktioniert?

Microsoft hat keine neuen Lizenzen oder Pläne erstellt, um diese Funktion zu ermöglichen. Diese Funktion basiert vollständig auf den bestehenden Microsoft 365-Tarifen und -Lizenzen. Wenn Sie bereits einen der unterstützten Microsoft 365-Tarife abonniert haben, verfügen Sie bereits über dieses neue Nutzungsrecht. Andernfalls, wenn Sie heute kein Microsoft 365-Abonnement haben, können Sie sich hier für Microsoft 365 Business Premium oder ähnliche Pläne anmelden. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft--license" />Wie kann ich herausfinden, welche Benutzer nur eine Microsoft 365-Lizenz haben?

Es gibt mehrere Möglichkeiten. Gehen Sie im Admin-Center Microsoft 365 zur Liste **Aktive Benutzer** und sehen Sie in der Spalte **Lizenzen** nach. Gehen Sie in Business Central zur Liste **Benutzer**, wählen Sie einen der Benutzer aus und sehen Sie sich die FactBox **Lizenzen** an.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft--license" />Wie kann ich die Liste Benutzer in Business Central filtern, um Benutzer zu sehen, die nur eine Microsoft 365 Lizenz haben?

Diese Aufgabe ist derzeit nicht über einen Filter oder eine Listenansicht möglich. Sie können jedoch einen Benutzer in der Liste auswählen und die FactBox Lizenzen anzeigen, die nur Microsoft 365 enthält, wenn der Benutzer nur eine Microsoft 365-Lizenz besitzt.

### <a name="what-about-users-that-have-both-a-microsoft--license-and-a-business-central-license" />Was ist mit Benutzern, die sowohl eine Microsoft 365-Lizenz als auch eine Business Central-Lizenz haben?

Wenn einem Benutzer mehrere Lizenzen zugewiesen sind, haben die höheren Lizenznutzungsrechte beim Zugriff auf Business Central Vorrang vor den niedrigeren Lizenznutzungsrechten. In diesem Fall berechtigt die Business Central-Lizenz den Benutzer zu mehr Benutzerrechten. So können Benutzer Datensätze von Business Central in Teams lesen und schreiben und auf den Business Central Web Client im Browser zugreifen, genau wie jeder andere Business Central-Lizenzinhaber. Wenn für die Microsoft 365-Lizenz bestimmte Berechtigungssätze festgelegt wurden, erhält der Benutzer die konfigurierten Berechtigungssätze in Kombination mit den Berechtigungssätzen aus der Business Central-Lizenz oder denjenigen, die dem Benutzer bereits zugewiesen wurden.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license" />Steht diese Lizenzierung in Zusammenhang mit der Business Central Team Member-Lizenz?

Es gibt keinen Zusammenhang zwischen Business Central Team Member-Lizenzen und dem Zugriff auf Business Central in Microsoft Teams mit Microsoft 365-Lizenzen. Obwohl Microsoft Teams und die dazugehörige Dokumentation sich auf Personen in einem Team als *Teammitglieder* beziehen, ist dies ein Sammelbegriff für eine Gruppe von Microsoft Teams Benutzern. Er bezieht sich nicht auf Business Central Lizenzen.

### <a name="does-business-central-enforce-any-of-the-constraints" />Setzt Business Central eine der Einschränkungen durch?

Ja, alle Plattformeinschränkungen und Mindestanforderungen, einschließlich der Lizenzierungsanforderungen, werden von der Business Central Plattform durchgesetzt. Diese leitet Benutzer mit spezifischen Fehlermeldungen an, um ihnen bei der Fehlersuche in ihrer Einrichtung zu helfen und Missbrauch zu verhindern. Wenn beispielsweise ein Benutzer, der nur über eine Microsoft 365-Lizenz verfügt, versucht, im Browser auf den Business Central Web Client zuzugreifen, wird der Zugriff verweigert und eine entsprechende Fehlermeldung angezeigt. 

## [Benutzung](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android" />Kann ich auf Datensätze in Teams für iOS und Teams für Android zugreifen?

Derzeit ist es nicht möglich, mit einer Microsoft 365-Lizenz auf Business Central-Daten auf Teams Mobile zuzugreifen. Microsoft arbeitet daran, diese Funktionalität in Kürze zu ermöglichen. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings" />Wie können Benutzer ihre persönlichen Einstellungen in Meine Einstellungen ändern?

Wenn ein Benutzer zum ersten Mal nur mit seiner Microsoft 365-Lizenz auf Business Central zugreift, werden seine Benutzereinstellungen wie Sprache, Zeitzone und regionale Einstellungen automatisch auf der Grundlage seines Betriebssystems oder seiner Browsereinstellungen festgelegt. Administratoren können diese Einstellungen von Business Central aus für jeden Benutzer ändern. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time" />Wovon hängt die Wahl der Sprache ab, wenn Sie sich zum ersten Mal anmelden?

Die Sprache, in der Sie Business Central erleben, wird auf der Grundlage verschiedener Faktoren festgelegt, darunter der Teams Client, über den Sie das erste Mal auf Business Central zugegriffen haben. Für die Desktop-App von Teams, Teams für iOS und Teams für Android wird die Sprache des Betriebssystems verwendet. Für Teams für das Web wird die Sprache des Browsers verwendet. In allen anderen Fällen wird die Sprache von Teams nicht berücksichtigt. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details" />Warum kann ich einige der farbigen Links in Registerkarten und Kartendetails nicht aktivieren?

Aktionsfähige Links auf den Seiten von Business Central werden oft als fettgedruckte Hyperlinks angezeigt, die aktiviert werden können, um zu anderen Seiten zu gelangen oder einen Vorgang auszuführen. Auf technischer Ebene sind diese Links in der Regel als Feldwerte ohne Beschriftung implementiert, die einen Code auslösen und bei denen die Wahl des Stils oft den Status widerspiegelt. Wenn Benutzer mit ihrer Microsoft 365-Lizenz auf Seiten von Business Central zugreifen, sind die Links so gestaltet, als ob sie aktiviert werden könnten. Sie können jedoch nicht aktiviert werden, da diese Lizenz keine Nutzungsrechte zum Ausführen von Aktionen bietet.  

### <a name="why-cant-i-activate-page-notification-actions" />Warum kann ich die Aktionen für Seitenbenachrichtigungen nicht aktivieren?

Kontextbezogene Benachrichtigungen, die auf Seiten angezeigt werden, werden oft von aktivierbaren Links begleitet. Wenn Benutzer mit ihrer Microsoft 365-Lizenz auf Seiten von Business Central zugreifen, werden diese Links angezeigt, können aber nicht aktiviert werden, da diese Lizenz keine Nutzungsrechte zum Ausführen von Aktionen bietet. Auf technischer Ebene sind diese Links als Aktionen implementiert.

### <a name="can-microsoft--users-remove-tabs" />Können Microsoft 365-Benutzer Registerkarten entfernen?

Ja. Jeder im Chat oder Kanal kann von anderen erstellte Registerkarten entfernen. Das Entfernen einer Registerkarte hat keine Auswirkungen auf die Daten in Business Central, aber die Registerkarte wird für alle Benutzer im Chat oder Channel entfernt.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others" />Wenn ich nicht filtern kann, kann ich dann trotzdem eine gefilterte Liste sehen, die von anderen erstellt wurde?

Benutzer, die mit ihrer Microsoft 365-Lizenz auf Business Central zugreifen, haben nicht die Nutzungsrechte, um über den Filterbereich zu filtern oder Listenansichten anzuwenden. Wenn jedoch ein anderer Benutzer eine Registerkarte erstellt hat, die eine gefilterte Listenseite enthält, sehen auch Microsoft 365-Benutzer die auf die Registerkarte angewandten Filter.

---

## <a name="see-also" />Siehe auch

[Übersicht über den Business Central Access mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md#minimum-requirements)  
[Zugriff mit Microsoft 365-Lizenzen festlegen](admin-access-with-m365-license-setup.md)  
