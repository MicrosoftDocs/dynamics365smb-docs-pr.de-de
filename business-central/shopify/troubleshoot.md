---
title: Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central
description: Erfahren Sie, was zu tun ist, wenn bei der Synchronisierung von Daten zwischen Shopify und Business Central etwas schief gelaufen ist
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30118, 30119, 30120,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 47b0d72283b4d017bb522c3e71f6c61501b59d5b
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361941"
---
# <a name="troubleshooting-shopify-and-business-central-synchronization"></a>Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central

Es kann vorkommen, dass Sie bei der Synchronisierung von Daten zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] Probleme ausführen müssen. Auf dieser Seite werden Schritte zur Fehlerbehebung bei einigen häufig auftretenden Szenarien definiert.

## <a name="logs"></a>Protokolle

Wenn eine Synchronisierungsaufgabe fehlschlägt, können Sie die Protokollierung aktivieren, indem Sie den Schalter **Protokollierung aktivieren** auf der Seite **Shopify Shop-Karte** aktivieren. Dann lösen Sie die Synchronisierungsaufgabe manuell aus und überprüfen Sie die Protokolle.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. , geben Sie **Shopify-Protokolleinträge** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den zugehörigen Protokolleintrag aus, und öffnen Sie die Seite **Shopify-Protokolleintrag**.
3. Überprüfen Sie die Anfrage, den Statuscode und die Beschreibung sowie die Antwortwerte.

Denken Sie später daran, die Protokollierung später abzuschalten, um negative Auswirkungen auf die Leistung und eine Vergrößerung der Datenbank zu vermeiden.

Auf der Seite **Shopify-Protokolleinträge** können Sie die Löschung aller Protokolleinträge oder solcher, die älter als sieben Tage sind, auslösen.

## <a name="data-capture"></a>Datenerfassung

Unabhängig von den Einstellungen für **Protokoll aktiviert** werden einige Antworten von Shopify immer protokolliert. Diese können auf der Seite **Datenerfassungsliste** überprüft oder heruntergeladen werden.

Wählen Sie die Aktion **Abgerufene Shopify-Daten** auf einer der folgenden Seiten aus:

- **Shopify-Auftrag**
- **Shopify-Auftragserfüllungen**
- **Shopify-Auftragslieferkosten**
- **Shopify-Auftragstransaktionen**
- **Shopify-Auszahlungen**
- **Shopify-Zahlungstransaktionen**
- **Shopify-Transaktionen**

## <a name="reset-sync"></a>Synchronisierung zurücksetzen

Für eine optimale Leistung importiert der Konnektor nur Kunden, Produkte und Bestellungen, die seit der letzten Synchronisierung erstellt oder geändert wurden. auf der Seite **Shopify Shop-Karte** stehen Ihnen Funktionen zur Verfügung, mit denen Sie das Datum/die Uhrzeit der letzten Synchronisierung ändern oder komplett zurücksetzen können. Diese Funktion stellt sicher, dass beim Ausführen der Synchronisierung alle Daten und nicht nur die Änderungen seit der letzten Synchronisierung synchronisiert werden.

Diese Funktion gilt nur für Synchronisierungen von Shopify auf [!INCLUDE[prod_short](../includes/prod_short.md)]. Sie kann nützlich sein, wenn Sie gelöschte Daten wie Produkte, Kunden oder gelöschte Bestellungen wiederherstellen müssen.

## <a name="request-the-access-token"></a>Fordern Sie das Access-Token an

Wenn [!INCLUDE[prod_short](../includes/prod_short.md)] keine Verbindung zu Ihrem Shopify-Konto herstellen kann, versuchen Sie, den Zugriffs-Token von Shopify anzufordern. Diese Anfrage kann erforderlich sein, wenn die Sicherheitsschlüssel rotieren oder sich die erforderlichen Berechtigungen (Scopes) ändern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. , geben Sie **Shopify-Shops** ein, und wählen Sie den entsprechenden Link aus.
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

## <a name="rotate-the-shopify-access-token"></a>Shopify-Zugriffstoken rotieren

Die folgenden Prozeduren beschreiben, wie Sie den Access Token, der vom Shopify- Konnektor für den Zugriff auf Ihren Shopify Onlineshop verwendet wird, rotieren können.

### <a name="in-shopify"></a>In Shopify

1. Gehen Sie in Ihrem **Shopify Admin** zu [Apps](https://www.shopify.com/admin/apps).
2. Wählen Sie **Löschen** in der Zeile mit der **Dynamics 365 Business Central**-App aus.
3. In der angezeigten Nachricht wählen Sie **Löschen**.

### <a name="in-prod_short"></a>In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. , geben Sie **Shopify-Shops** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop, für den Sie den Access-Token rotieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern**.
4. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem an Shopify-Konto an, überprüfen Sie den Datenschutz und die Berechtigungen, und wählen Sie dann die Schaltfläche **App installieren** aus.

## <a name="known-issues"></a>Bekannte Probleme

*General Bus. Buchungsgruppe* darf nicht null oder leer sein; Das Debitorenfeld muss einen Wert enthalten. Korrigieren:

Füllen Sie das Feld **Kundenvorlagencode** im Fenster **Shopify Shop-Karte** mit der Vorlage aus, in der **Geschäftsbuchungsgruppe** ausgefüllt ist. Die Debitorenvorlage wird nicht nur für die Erstellung von Debitoren, sondern auch für die Berechnung des Verkaufspreises und bei der Erstellung von Verkaufsdokumenten verwendet.

### <a name="importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Importieren von Daten in Ihren Shopify Shop ist nicht aktiviert. Gehen Sie zur Shop-Karte, um sie zu aktivieren

Aktivieren Sie im Fenster **Shopify Shop-Karte** **Datensynchronisierung mit Shopify zulassen**.  Dieser Umschalter soll den Online-Shop davor schützen, Demo-Daten aus [!INCLUDE[prod_short](../includes/prod_short.md)] abzurufen.

## <a name="see-also"></a>Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)