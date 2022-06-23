---
title: Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central
description: Erfahren Sie, wie Sie vorgehen müssen, wenn während der Synchronisierung von Daten zwischen Shopify und Business Central ein Fehler auftritt
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ff2e4aca52f479e461dab0d9d0f0ce4958d19353
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808863"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central

Es ist möglich, dass Situationen auftreten, in denen Sie Probleme beheben müssen. Auf dieser Seite werden Schritte zur Fehlerbehebung bei einigen häufig auftretenden Szenarien definiert.

## <a name="logs"></a>Protokolle

Wenn eine Synchronisierungsaufgabe fehlschlägt, können Sie die Protokollierung aktivieren, indem Sie den Umschalter **Protokoll aktivieren** auf der **Shopify-Shop-Karte** aktivieren. Lösen Sie die Synchronisierungsaufgabe manuell aus, und überprüfen Sie die Protokolle.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Protokolleinträge** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den zugehörigen Protokolleintrag aus, und öffnen Sie das Fenster **Shopify-Protokolleintrag**.
3. Überprüfen Sie die Anforderung, den Statuscode und die Beschreibung sowie die Antwort.

Denken Sie daran, die Protokollierung zu deaktivieren, um negative Auswirkungen auf die Leistung und eine Erhöhung der Datenbankgröße zu vermeiden.

Im Fenster **Shopify-Protokolleinträge** können Sie die Löschung aller Protokolleinträge oder solcher, die älter als sieben Tage sind, auslösen.

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

Für eine optimale Leistung importiert der Konnektor nur Kunden, Produkte und Bestellungen, die seit der letzten Synchronisierung erstellt oder geändert wurden. Auf der **Shopify-Shop-Karte** sind Funktionen verfügbar, um das/die Datum/Uhrzeit der letzten Synchronisierung zu ändern oder vollständig zurückzusetzen. Diese Funktion stellt sicher, dass beim Ausführen der Synchronisierung alle Daten und nicht nur die Änderungen seit der letzten Synchronisierung synchronisiert werden.

Diese Funktion gilt nur für Synchronisierungen von Shopify mit [!INCLUDE[prod_short](../includes/prod_short.md)] und kann hilfreich sein, wenn Sie gelöschte Daten wie Produkte, Kunden oder gelöschte Bestellungen wiederherstellen müssen.

## <a name="update-the-access-token"></a>Zugriffstoken aktualisieren

Wenn [!INCLUDE[prod_short](../includes/prod_short.md)] keine Verbindung zu Ihrem Shopify-Konto herstellen kann, versuchen Sie, den Zugriffstoken zurückzusetzen.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie den Zugriffstoken abrufen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern** aus.
4. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden.

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Konnektor für Shopify](get-started.md)  
