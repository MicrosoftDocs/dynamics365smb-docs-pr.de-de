---
title: Erste Schritte mit Konnektor für Shopify
description: Erste Schritte beim Konfigurieren der Verbindung zwischen Business Central und Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b79691660ca84309057c3abab3d3a3df47271f58
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728410"
---
# <a name="get-started-with-the-shopify-connector"></a>Erste Schritte mit dem Shopify-Konnektor

Verbinden Sie Ihre(n) Shopify Store(s) mit [!INCLUDE [prod_short](../includes/prod_short.md)], um maximieren Sie die Produktivität Ihres Unternehmens. Sie können Erkenntnisse aus Ihrem Unternehmen und Ihrem Shopify Store als eine Einheit verwalten und anzeigen.

Der Shopify-Konnektor umfasst die folgenden Funktionen:

- Unterstützung für mehr als einen Shopify Shop.
  - Jeder Shop verfügt über eine eigene Einrichtung, einschließlich einer Sammlung von Produkten, Standorten zur Bestandsberechnung und Preislisten.  
- Bidirektionale Synchronisierung von Artikeln oder Produkten.
  - Der Konnektor synchronisiert Bilder, Artikelvarianten, Barcodes, Kreditorenartikelnummer, erweiterte Texte und Tags.  
  - Exportieren Sie Artikelattribute nach Shopify.  
  - Verwenden Sie ausgewählte Debitorenpreisgruppen und Rabatte, um die nach Shopify exportierten Preise zu definieren.  
  - Entscheiden Sie, ob Artikel automatisch erstellt werden können, oder lassen Sie nur Aktualisierungen bestehender Produkte zu.  
- Synchronisierung von Beständen.
  - Wählen Sie einige oder alle verfügbaren Standorte in [!INCLUDE [prod_short](../includes/prod_short.md)] aus.  
  - Aktualisieren Sie die Lagerbestände an mehreren Standorten in Shopify.  
- Bi-direktionale Synchronisierung von Debitor.
  - Ordnen Sie Debitoren intelligent per Telefon und E-Mail zu.  
  - Verwenden Sie beim Erstellen von Debitoren länderspezifische Vorlagen, um sicherzustellen, dass die Steuereinstellungen korrekt sind.  
- Import von Bestellungen aus Shopify.
  - Während des Imports können Sie Debitoren automatisch in [!INCLUDE [prod_short](../includes/prod_short.md)] erstellen oder sich dazu entscheiden, diese in Shopify zu verwalten.  
  - Schließen Sie Bestellungen ein, die in anderen Kanälen wie Shopify POS oder Amazon erstellt wurde.  
  - Versandkosten, Geschenkgutscheine, Tipps, Versand- und Zahlungsmethoden, Transaktionen und Betrugsrisiko.  
  - Erhalten Sie Auszahlungsinformationen von Shopify Payments.  
- Verfolgen Sie Erfüllungsinformationen.
  - Wählen Sie optional, ob Sie Informationen zur Artikelverfolgung von [!INCLUDE [prod_short](../includes/prod_short.md)] nach Shopify übertragen möchten.  

Um Shopify mit [!INCLUDE [prod_short](../includes/prod_short.md)] zu verwenden, müssen Sie zunächst einige Dinge erledigen. Dieser Artikel dient als Anleitung für die Integration Ihres Shopify-Shops mit [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Voraussetzungen für Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto.
- Ein Shopify-Online-Store.

Um ein neues Shopify-Konto zu erstellen oder sich für einen kostenlosen 14-tägigen Test anzumelden, gehen Sie zu [Shopify.com](https://www.shopify.com/). Erfahren Sie mehr darüber, wie Sie Ihren Online Store erstellen und personalisieren können im [Shopify Help Center](https://help.shopify.com/).
  
Andere Vertriebskanäle werden unterstützt, z. B. Shopify-POS.

### <a name="recommended-settings"></a>Empfohlene Einstellungen

- Deaktivieren Sie **Bestellung automatisch archivieren** im Abschnitt **Auftragsabwicklung** in den Einstellungen für die [**Kasse**](https://www.shopify.com/admin/settings/checkout) in Ihrer **Shopify-Verwaltung**.

Erfahren Sie mehr über Shopify Einstellungen für Demo- und Testszenarien unter [Test- und Trainingsszenarien](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Voraussetzungen für Business Central

- Stellen Sie sicher, dass die **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-App installiert ist.

Die App ist für alle Neuanmeldungen und Testversionen vorinstalliert. Erfahren Sie mehr über die Installation von Apps aus AppSource unter [Installieren und Deinstallieren von Erweiterungen](../ui-extensions-install-uninstall.md#install). Führen Sie die unten aufgeführten Schritte aus, wenn Sie nicht über [!INCLUDE[prod_short](../includes/prod_short.md)] verfügen.

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installieren Sie die Dynamics 365 Business Central App in Ihrem Shopify Online Store

Für das bestehende [!INCLUDE[prod_short](../includes/prod_short.md)] ist dieser Schritt optional und kann übersprungen werden.

1. Suchen Sie die [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-App im [Shopify Appstore](https://apps.shopify.com/)
2. Wählen Sie die Schaltfläche **App hinzufügen** aus. Melden Sie sich bei Ihrem Shopify-Konto an, wenn Sie dazu aufgefordert werden. Wählen Sie den gewünschten Onlineshop aus, falls Sie über mehrere verfügen.
3. Nachdem Sie den Datenschutz und die Berechtigungen überprüft haben, wählen Sie die Schaltfläche **App installieren** aus.

   Sie können die installierte **Dynamics 365 Business Central** App im Bereich **Apps** in der Seitenleiste der **Shopify Admin** Seite finden und öffnen.
4. Wählen Sie **Jetzt anmelden**, um den Test von [!INCLUDE[prod_short](../includes/prod_short.md)] zu starten oder **Anmelden**, wenn Sie bereits [!INCLUDE[prod_short](../includes/prod_short.md)] haben. Sie werden zu Ihrer [Business Central](https://businesscentral.dynamics.com) Seite weitergeleitet.
5. Die nächsten Schritte sollten in [!INCLUDE[prod_short](../includes/prod_short.md)] ausgeführt werden.

## <a name="connect-business-central-to-the-shopify-online-store"></a>Verbinden Sie Business Central mit dem Shopify-Online-Store

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie in das Feld **Code** den Code ein, der das Auffinden in [!INCLUDE[prod_short](../includes/prod_short.md)] erleichtert. Der Name könnte zum Beispiel widerspiegeln, was ein Geschäft verkauft, wie “Möbel„ oder “Kaffee“, oder das Land oder die Region, in der es tätig ist.
4. Geben Sie in das Feld **Shopify URL** die URL Ihres Online-Shops ein, die verbunden sein muss. Verwenden Sie das folgende Format: `https://{shop}.myshopify.com/`.
5. Aktivieren Sie den Schalter **Aktiviert**, lesen und akzeptieren Sie die Bestimmungen.
6. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem Shopify Konto an, prüfen Sie die Datenschutzbestimmungen und Berechtigungen und wählen Sie dann die Schaltfläche **App installieren**.

Wiederholen Sie die Schritte 2–6 für alle Onlineshops, die Sie verbinden möchten.

> [!NOTE]
> Stellen Sie sicher, dass Ihr Browser keine Pop-up-Fenster blockiert. Wenn Sie den Schalter **Aktiviert** aktivieren, öffnet das System die Seite **Warte auf Antwort - schließe diese Seite nicht**, die auf einen Zugriffs-Token von Shopify wartet. Wenn diese Seite geschlossen oder blockiert ist, können Sie keine Verbindung zu Shopify herstellen. Erfahren Sie mehr unter [Anforderung des Zugriffstokens](troubleshoot.md#request-the-access-token)

### <a name="next-steps"></a>Nächste Schritte

Jetzt ist Ihr Onlineshop mit [!INCLUDE[prod_short](../includes/prod_short.md)] verbunden. In den nächsten Schritten definieren Sie, wie und was synchronisiert werden soll.

- [Artikel synchronisieren](synchronize-items.md)
- [Debitoren synchronisieren](synchronize-customers.md)
- [Bestellungen synchronisieren](synchronize-orders.md)

## <a name="see-also"></a>Siehe auch

[Test- und Trainingsszenarien](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).
