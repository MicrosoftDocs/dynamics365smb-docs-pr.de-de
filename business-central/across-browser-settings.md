---
title: Ihren Browser einrichten
description: Beschreibt das Einrichten von Browsern für die Arbeit mit Business Central und den darin integrierten Produkten.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 12/04/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Ihren Browser für die Arbeit mit Business Central-Webclient einrichten und Probleme damit beheben

In diesem Artikel wird erläutert, wie Sie Ihren Browser so einrichten, dass [!INCLUDE[web_client](includes/web_client.md)] und alle seine Funktionen ordnungsgemäß funktionieren. Lesen Sie diesen Artikel, wenn Sie Probleme beim Öffnen von [!INCLUDE[web_client](includes/web_client.md)] haben, da die Einstellungen Ihres Browsers manche Probleme verursachen können.

Der Artikel enthält Details zum Einrichten von Microsoft Edge, aber die Anforderungen für JavaScript, Cookies und Popups sind jedoch für alle unterstützten Browser gleich. Informationen zu anderen Browsern finden Sie in den Anweisungen des Herstellers.  

## <a name="use-a-supported-browser"></a>Einen unterstützten Browser verwenden

Stellen Sie sicher, dass Sie einen der unterstützten Browser verwenden. Siehe [Mindestanforderungen für die Nutzung von Business Central](product-requirements.md#browsers).

Wir empfehlen Ihnen, eine stabile Kanalversion eines Webbrowsers zu verwenden, da es sich um die zuverlässigste und stabilste Version handelt, die umfangreichen Tests und Fehlerbehebungen unterzogen wurde. Dies stellt sicher, dass Sie das beste Erlebnis haben und bei der Verwendung des Webclients weniger wahrscheinlich auf Probleme stoßen.  

## <a name="allow-javascript-from-business-central"></a>JavaScript von Business Central aus zulassen

*Problem:*

Wenn der Browser kein JavaScript zulässt, sehen Sie **NotSupported/DisabledJavaScript** in der Adressleiste und die Nachricht **HTTP-Fehler 404.0 – nicht gefunden**, wenn Sie versuchen [!INCLUDE[prod_short](includes/prod_short.md)] zu öffnen, und den 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Fix:*

1. Im Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **JavaScript**.
2. Führen Sie einen der folgenden Schritte aus. Wählen Sie den von Ihrer Organisation empfohlenen Schritt aus:

    - Bewegen Sie die Umschaltung **Zulassen** nach links (Aus). Wählen Sie dann **Hinzufügen** und geben Sie die Adresse (URL) ein für [!INCLUDE[prod_short](includes/prod_short.md)] im Kästchen **Seite**. Wählen Sie **Hinzufügen**, wenn fertig.
    - Bewegen Sie die Umschaltung **Zulassen** nach rechts (Ein).

## <a name="allow-cookies-from-business-central"></a>Cookies für Business Central zulassen

*Problem:*

Wenn der Browser keine Cookies zulässt, wird folgende Fehlermeldung angezeigt:

**Die Seite wurde leider nicht gefunden. Bitte überprüfen Sie die Adresse und versuchen Sie es erneut.** 

*Fix:*

1. In Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **Cookies und Site-Daten**.
2. Bewegen Sie die Umschaltung **Ermöglichen Sie Websites das Speichern und Lesen von Cookie-Daten** nach rechts (Ein).  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Pup-Ups von Business Central zulassen

[!INCLUDE[prod_short](includes/prod_short.md)] lässt sich in mehrere Produkte integrieren. In einigen Fällen, wie bei Microsoft Teams, öffnet sich [!INCLUDE[prod_short](includes/prod_short.md)] innerhalb des Produkts. Diese Funktion erfordert, dass Ihr Browser Popups zulässt von [!INCLUDE[prod_short](includes/prod_short.md)].

*Problem:*

Wenn Popups für [!INCLUDE[prod_short](includes/prod_short.md)] blockiert werden, erhalten Sie eine Nachricht ähnlich der folgenden:

**Etwas ist schief gelaufen. Ihr Browser blockiert möglicherweise Popups, die von Business Central benötigt werden.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Fix:*

1. In Microsoft Edge gehen Sie zu **Einstellungen** > **Cookies und Site-Berechtigungen** > **Popups und Umleitung**.
2. Bewegen Sie die Umschaltung **Blockiert** nach rechts (Ein).
3. Wählen Sie **Hinzufügen**. In dem Kästchen **Seite** geben Sie `https://businesscentral.dynamics.com` ein und wählen Sie **Hinzufügen** aus.

## <a name="see-also"></a>Siehe auch

[Teams Problembehebung](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
