---
title: Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central
description: Erfahren Sie, was zu tun ist, wenn bei der Synchronisierung von Daten zwischen Shopify und Business Central etwas schief gelaufen ist
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 83678c6c81b29a524405699425be877459b6568d
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075317"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central

Es kann vorkommen, dass Sie bei der Synchronisierung von Daten zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] Probleme ausführen müssen. Auf dieser Seite werden Schritte zur Fehlerbehebung bei einigen häufig auftretenden Szenarien definiert.

## <a name="logs"></a>Protokolle

Wenn eine Synchronisierungsaufgabe fehlschlägt, können Sie die Protokollierung aktivieren, indem Sie den Schalter **Protokollierung aktivieren** in der **Shopify Shop-Karte** aktivieren. Lösen Sie die Synchronisierungsaufgabe manuell aus und überprüfen Sie die Protokolle.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Protokolleinträge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den zugehörigen Protokolleintrag aus, und öffnen Sie das Fenster **Shopify-Protokolleintrag**.
3. Überprüfen Sie die Anfrage, den Statuscode und die Beschreibung sowie die Antwort.

Denken Sie daran, die Protokollierung später abzuschalten, um negative Auswirkungen auf die Leistung und eine Vergrößerung der Datenbank zu vermeiden.

Über das Fenster **Shopify Log-Einträge** können Sie das Löschen aller Log-Einträge oder derjenigen, die älter als sieben Tage sind, auslösen.

## <a name="data-capture"></a>Datenerfassung

Unabhängig von den Einstellungen für **Protokoll aktiviert** werden einige Antworten von Shopify immer protokolliert. Diese können im Fenster **Datenerfassungsliste** überprüft oder heruntergeladen werden.

Wählen Sie die Aktion **Abgerufene Shopify-Daten** auf einer der folgenden Seiten aus:

- **Shopify-Auftrag**
- **Shopify-Auftragserfüllungen**
- **Shopify-Auftragslieferkosten**
- **Shopify-Auftragstransaktionen**
- **Shopify-Auszahlungen**
- **Shopify-Zahlungstransaktionen**
- **Shopify-Transaktionen**

## <a name="reset-sync"></a>Synchronisierung zurücksetzen

Für eine optimale Leistung importiert der Konnektor nur Kunden, Produkte und Bestellungen, die seit der letzten Synchronisierung erstellt oder geändert wurden. Auf der Karte **Shopify Shop** stehen Ihnen Funktionen zur Verfügung, mit denen Sie das Datum/die Uhrzeit der letzten Synchronisierung ändern oder komplett zurücksetzen können. Diese Funktion stellt sicher, dass beim Ausführen der Synchronisierung alle Daten und nicht nur die Änderungen seit der letzten Synchronisierung synchronisiert werden.

Diese Funktion gilt nur für Synchronisierungen von Shopify mit [!INCLUDE[prod_short](../includes/prod_short.md)] und kann hilfreich sein, wenn Sie gelöschte Daten wie Produkte, Kunden oder gelöschte Bestellungen wiederherstellen müssen.

## <a name="request-the-access-token"></a>Fordern Sie das Access-Token an

Wenn [!INCLUDE[prod_short](../includes/prod_short.md)] keine Verbindung zu Ihrem Shopify-Konto herstellen kann, versuchen Sie, den Zugriffs-Token von Shopify anzufordern. Diese Anfrage kann erforderlich sein, wenn die Sicherheitsschlüssel rotieren oder sich die erforderlichen Berechtigungen (Scopes) ändern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop aus, für den Sie den Zugriffstoken abrufen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern** aus.
4. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden.

Der Schalter **Hat AccessKey** wird aktiviert.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Überprüfen und aktivieren Sie die Berechtigungen für Http-Anfragen, wenn Sie in einer nicht produktiven Umgebung ausgeführt werden

Damit die Shopify Konnektor-Erweiterung korrekt funktioniert, benötigt sie die Berechtigung, Http-Anfragen zu stellen. Beim Testen in Sandboxen sind die Http-Anforderungen für alle Erweiterungen verboten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Erweiterungsverwaltung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Erweiterung *Shopify Konnektor*.
3. Wählen Sie die Aktion **Konfigurieren**, um die Seite **Erweiterungseinstellungen** zu öffnen.
4. Stellen Sie sicher, dass der Schalter **HTTPClient-Anfragen zulassen** aktiviert ist.

## <a name="rotate-the-shopify-access-key"></a>Rotieren des Shopify Access-Schlüssels

Die folgenden Prozeduren beschreiben, wie Sie den Access Token, der vom Shopify Konnektor für den Zugriff auf Ihren Shopify Onlineshop verwendet wird, rotieren können.

### <a name="in-shopify"></a>In Shopify

1. Gehen Sie in Ihrem **Shopify Admin** zu [Apps](https://www.shopify.com/admin/apps).
2. In der Zeile mit der App **Dynamics 365 Business Central** wählen Sie **Löschen**.
3. In der angezeigten Nachricht wählen Sie **Löschen**.

### <a name="in-prod_short"></a>In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie den Access-Token rotieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern**.
4. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem an Shopify-Konto an, überprüfen Sie den Datenschutz und die Berechtigungen, und wählen Sie dann die Schaltfläche **App installieren** aus.

## <a name="see-also"></a>Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)  