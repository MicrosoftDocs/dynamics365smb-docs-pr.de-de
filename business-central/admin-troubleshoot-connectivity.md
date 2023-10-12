---
title: Problembehandlung der Konnektivität
description: 'Beschreibt, wie Sie die Seite Problembehandlung der Konnektivität verwenden, um Probleme bei der Online-Verbindung zu Business Central zu identifizieren und zu beheben.'
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
---
# Problembehandlung der Konnektivität für Business Central

> **Geltet für:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Diese Funktion befindet sich derzeit in der Vorschau. Die Funktionalität und die Belege können sich in späteren Versionen ändern. Wenn Sie auf der Grundlage Ihrer eigenen Erkenntnisse zur Dokumentation beitragen möchten, wählen Sie bitte ![Artikel in GitHub bearbeiten.](media/github-edit-pencil.png) **Bearbeiten**, und schlagen Sie Änderungen vor. Dann werden wir uns das ansehen!

[!INCLUDE[prod_short](includes/prod_short.md)] Online enthält die Seite **Problembehandlung Konnektivität**, die Sie verwenden können, um Probleme mit Ihrer Verbindung zum Online-Dienst zu identifizieren. Es gibt mehrere Dinge, die die Konnektivität zu Business Central beeinflussen, wie die Firewall-Einstellungen Ihres Netzwerks oder die Konfiguration des Domänen-Namensdienstes. Auf der Seite können Sie eine Liste von Prüfungen ausführen, die allgemeine Probleme mit der Konnektivität von Business Central diagnostizieren. Sie können die Informationen verwenden, um zu versuchen, die Probleme selbst zu beheben, oder sie an Ihren Support-Mitarbeiter weitergeben.

> [!NOTE]
> Die Seite **Problembehandlung der Konnektivität** testet nicht die Leistung oder Zuverlässigkeit des Netzwerks, wie z. B. die Geschwindigkeit Ihrer Verbindung. Sie prüft nur die Konnektivität zu verschiedenen Ressourcen.

## Starten Sie die Konnektivitätsprüfung 

1. Öffnen Sie einen Internetbrowser.
2. Geben Sie in der Adresse die URL ein, die Sie verwenden, um Business Central zu öffnen und fügen Sie am Ende `/connectivity` hinzu. 

    Wenn Sie zum Beispiel `https://businesscentral.dynamics.com` verwenden, dann geben Sie ein:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Oder, wenn die URL die Mandanten-ID enthält, z. B. `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, dann Folgendes:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. Auf der Seite **Problembehandlung Konnektivität** wählen Sie **Prüfung starten**.

    Eine Reihe von Prüfungen wird ausgeführt, und das Ergebnis jeder Prüfung wird angezeigt:

    - ![Konnektivitätsprüfung erfolgreich.](media/connectivity-check.png) zeigt an, dass die Prüfung erfolgreich war.
    - ![Konnektivitätsprüfung fehlgeschlagen.](media/connectivity-failed.png) zeigt an, dass der Check fehlgeschlagen ist. Lesen Sie die Nachricht unterhalb des Checks für weitere Details.
    - ![Konnektivitätsprüfung wurde nicht ausgeführt.](media/connectivity-blocked.png) zeigt an, dass die Prüfung nicht ausgeführt wurde, typischerweise wegen eines Fehlers bei einer früheren Prüfung. Lesen Sie die Nachricht unterhalb des Checks für weitere Details.

4. Um die Prüfung erneut auszuführen, wählen Sie **Prüfung neu starten**.

In den folgenden Abschnitten werden die ausgeführten Prüfungen erläutert und es werden einige Tipps zur Behebung von Problemen gegeben.

## Grundlegende Internet-Konnektivität

Überprüft, ob Sie eine Verbindung zum Internet haben, indem es prüft, ob Sie auf eine bekannte öffentliche Domäne zugreifen können, wie www.bing.com.

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Ihr Browser unterstützt diese Prüfung nicht|Öffnen Sie die Seite in einem unterstützten Browser, und versuchen Sie es erneut. Eine Liste der unterstützten Browser finden Sie unter [Mindestanforderungen für die Verwendung von Business Central – Browser](product-requirements.md#browsers)|
|Der Server mit der folgenden URL konnte nicht angefunkt werden: {url}|Überprüfen Sie die Firewall-Einstellungen.|

## CDN (Content Delivery Network)-Ressourcen werden geladen

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet Azure Content Delivery Network (CDN), um Ressourcen bereitzustellen, die zum Ausführen des Business Central Web-Clients erforderlich sind. Dieser Check prüft, ob die erforderlichen Ressourcen verfügbar und zugänglich sind, indem er die Business Central-Instanz im CDN anpingt.

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Ihr Browser unterstützt diese Prüfung nicht|Siehe **Prüfung der grundlegenden Internet-Konnektivität**.|
|Der Server mit der folgenden URL konnte nicht angefunkt werden: {url}|Überprüfen Sie die Firewall-Einstellungen.|

## Benutzer-Authentifizierung

Überprüft, ob sich der aktuelle Benutzer mit einem gültigen Business Central-Konto angemeldet hat.

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Kein Benutzer ist derzeit authentifiziert|Melden Sie sich bei Business Central mit einem gültigen Benutzernamen und Kennwort an.|

## Erkennung von Business Central-Umgebungen

Prüft, ob Business Central-Umgebungen für einen authentifizierten Benutzer verfügbar sind, und überprüft dann, ob der Benutzer in der Umgebung authentifiziert werden kann.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Kein authentifizierter Benutzer, für den diese Prüfung durchgeführt werden soll|Siehe die Prüfung **Benutzerauthentifizierung**.|
|Es konnten keine verfügbaren Umgebungen für Ihr Konto abgerufen werden.|Überprüfen Sie die Liste der verfügbaren Umgebungen im Business Central Admin Center.|
|Ihr Benutzername oder Kennwort ist falsch, oder Sie haben kein gültiges Konto.| Überprüfen Sie, ob Sie sich mit dem richtigen Benutzernamen und Kennwort angemeldet haben.|

## Konnektivität der Anwendungsdienste

Überprüft, ob der authentifizierte Benutzer eine Verbindung zu einer ermittelten Umgebung herstellen kann, normalerweise beginnend mit der Produktionsumgebung.

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Kein authentifizierter Benutzer, für den diese Prüfung durchgeführt werden soll|Siehe **Benutzerauthentifizierung prüfen**.|
|Es konnten keine verfügbaren Umgebungen für Ihr Konto abgerufen werden.|Siehe **Ermittlung von Business Central Umgebungen**.|
|Keine Cluster-Adresse, für die diese Prüfung durchgeführt werden soll|Überprüfen Sie die Liste der verfügbaren Umgebungen im Business Central Admin Center.|
|Versionsendpunkt existiert nicht|Überprüfen Sie die Liste der verfügbaren Umgebungen im Business Central Admin Center.|

## Webserver-Konnektivität

Überprüft, ob der authentifizierte Benutzer erfolgreich Verbindungen mit dem Webserver herstellen kann.

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Kein authentifizierter Benutzer, für den diese Überprüfung durchgeführt werden soll|Siehe **Benutzerauthentifizierung prüfen**.|
|Es konnten keine verfügbaren Umgebungen für Ihr Konto abgerufen werden.|Siehe **Ermittlung von Business Central Umgebungen**.|
|Keine Cluster-Adresse, für die diese Prüfung durchgeführt werden soll|Überprüfen Sie die Liste der verfügbaren Umgebungen im Business Central Admin Center.|
|Fehler beim Herstellen einer Verbindung mit dem Webserver|Leeren Sie den Cache und laden Sie die Seite neu.|

## Dienststatus

Meldet den Dienstzustand von Business Central, indem nach gemeldeten Ausfällen gesucht wird.

|Problem|Was Sie versuchen sollten|
|-------|-------------|
|Kein authentifizierter Benutzer, für den diese Überprüfung durchgeführt werden soll|Siehe **Benutzerauthentifizierung prüfen**.|
|Leider ist Business Central vorübergehend nicht verfügbar. Bitte versuchen Sie es später erneut.|Versuchen Sie es später noch einmal.|

## Siehe auch

[Ressourcen für Hilfe und Support](product-help-and-support.md)  
[Übersicht der Aufgaben zum Festlegen von Business Central](setup.md)  
[Häufig gestellte Fragen zur Verwendung von Business Central](across-faq.yml)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Das Business Central Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
