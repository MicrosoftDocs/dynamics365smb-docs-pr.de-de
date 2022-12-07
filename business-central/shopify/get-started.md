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
ms.openlocfilehash: bc3c5769a100909faedbfacce58bb1a2b146f5ad
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802983"
---
# <a name="get-started-with-the-shopify-connector"></a>Erste Schritte mit dem Shopify-Konnektor

Verbinden Sie Ihre(n) Shopify Store(s) mit [!INCLUDE [prod_short](../includes/prod_short.md)], um maximieren Sie die Produktivität Ihres Unternehmens. Sie können Erkenntnisse aus Ihrem Unternehmen und Ihrem Shopify Store als eine Einheit verwalten und anzeigen.

Um Shopify mit [!INCLUDE [prod_short](../includes/prod_short.md)] zu verwenden, müssen Sie zunächst einige Dinge erledigen. Dieser Artikel dient als Anleitung für die Integration Ihres Shopify-Shops mit [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Voraussetzungen für Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Einen Shopify-Onlineshop

Weitere Informationen zum Erstellen von Shopify-Tests und empfohlenen Einstellungen finden Sie unter [Erstellen und Einrichten eines Shopify-Kontos](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Voraussetzungen für Business Central

- Stellen Sie sicher, dass die **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-App installiert ist.

  Die App ist für alle Neuanmeldungen und Testversionen vorinstalliert. Erfahren Sie mehr über die Installation von Apps aus AppSource unter [Installieren und Deinstallieren von Erweiterungen](../ui-extensions-install-uninstall.md#install). Führen Sie die unten aufgeführten Schritte aus, wenn Sie nicht über [!INCLUDE[prod_short](../includes/prod_short.md)] verfügen.

- Stellen Sie sicher, dass der Benutzer über ausreichende Berechtigungen verfügt. Der Konnektor Shopify wird durch die auf *Shopify - Admin (SHPFY - ADMIN)* festgelegte Berechtigung abgedeckt. Weitere Informationen finden Sie unter [Benutzer entsprechend den Lizenzen erstellen](../ui-how-users-permissions.md) und [Benutzern und Gruppen Berechtigungen zuweisen](../ui-define-granular-permissions.md)


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

### <a name="known-issues"></a>Bekannte Probleme

- Der Browser blockiert das Popup-Fenster. Wenn Sie den Schalter **Aktiviert** aktivieren, öffnet das System die Seite **Warte auf Antwort - diese Seite nicht schließen**, die auf einen Zugriffstoken von Shopify wartet. Wenn diese Seite geschlossen oder blockiert ist, können Sie keine Verbindung zu Shopify herstellen. Erfahren Sie mehr unter [Anforderung des Zugriffstokens](troubleshoot.md#request-the-access-token)
- [Oauth Fehler invalid_request: Konnte Shopify API-Anwendung mit api_key nicht finden](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Kann keine Verbindung von der Sandbox aus herstellen](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## <a name="next-steps"></a>Nächste Schritte

Jetzt ist Ihr Onlineshop mit [!INCLUDE[prod_short](../includes/prod_short.md)] verbunden. In den nächsten Schritten definieren Sie, wie und was synchronisiert werden soll.

- [Artikel synchronisieren](synchronize-items.md)
- [Debitoren synchronisieren](synchronize-customers.md)
- [Bestellungen synchronisieren](synchronize-orders.md)

## <a name="see-also"></a>Siehe auch

[Beispielhafte Vorgehensweise: Einrichten und Verwenden des Shopify Konnektors](walkthrough-setting-up-and-using-shopify.md)  

