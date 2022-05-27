---
title: Erste Schritte mit Konnektor für Shopify
description: Erste Schritte beim Konfigurieren der Verbindung zwischen Business Central und Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768153"
---
# <a name="get-started-with-the-shopify-connector"></a>Erste Schritte mit dem Shopify-Konnektor

[!INCLUDE [prod_short](../includes/prod_short.md)] gibt Ihnen die Flexibilität, Ihre(n) Shopify-Store(s) damit zu verbinden, um die Produktivität Ihres Unternehmens zu maximieren. Mithilfe des Shopify-Konnektors können Sie Erkenntnisse aus Ihrem Unternehmen und Ihrem Shopify-Onlineshop als eine Einheit verwalten und anzeigen. Um Shopify mit [!INCLUDE [prod_short](../includes/prod_short.md)] verwenden zu können, müssen Sie einige Schritte ausführen. Diese Seite dient als Leitfaden für die vollständige Integration Ihres Shopify-Shops in [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Voraussetzungen für Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Einen Shopify-Onlineshop

Um ein neues Shopify-Konto zu erstellen oder sich für eine kostenlose 14-tägige Testversion anzumelden, navigieren Sie zu [Shopify](https://www.shopify.com/). Weitere Informationen zum Erstellen und Personalisieren Ihres Onlineshops finden Sie unter [Shopify-Hilfezentrum](https://help.shopify.com/).
  
- Andere Vertriebskanäle werden unterstützt, z. B. Shopify-POS.

### <a name="recommended-settings"></a>Empfohlene Einstellungen

- Deaktivieren Sie **Bestellung automatisch archivieren** im Abschnitt **Auftragsabwicklung** in den Einstellungen für die [**Kasse**](https://www.shopify.com/admin/settings/checkout) in Ihrer **Shopify-Verwaltung**.

Weitere Informationen zu Shopify-Einstellungen für Demo- und Testszenarien finden Sie unter [Test- und Trainingsszenarien](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Voraussetzungen für Business Central

- Stellen Sie sicher, dass die Erweiterung **Mit Shopify für [!INCLUDE[prod_short](../includes/prod_short.md)] verbinden** installiert ist.

Die Erweiterung ist für alle Neuanmeldungen und Testversionen vorinstalliert. Wenn Sie Erweiterungen vom Marktplatz installieren müssen, besuchen Sie [Installieren und Deinstallieren von Erweiterungen](../ui-extensions-install-uninstall.md#install). Führen Sie die unten aufgeführten Schritte aus, wenn Sie nicht über [!INCLUDE[prod_short](../includes/prod_short.md)] verfügen.
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Verbinden von Business Central mit dem Shopify-Onlineshop

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie im Feld **Code** den gewünschten Code ein.  
4. Geben Sie im Feld **Shopify-URL** die URL Ihres zu verbindenden Onlineshops ein.
5. Aktivieren Sie den Umschalter **Aktiviert**, und überprüfen und akzeptieren Sie die allgemeinen Geschäftsbedingungen.
6. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem an Shopify-Konto an, überprüfen Sie den Datenschutz und die Berechtigungen, und wählen Sie dann die Schaltfläche **App installieren** aus.

Wiederholen Sie die Schritte 2–6 für alle Onlineshops, die Sie verbinden möchten.

### <a name="next-steps"></a>Nächste Schritte

Jetzt ist Ihr Onlineshop mit [!INCLUDE[prod_short](../includes/prod_short.md)] verbunden. In den nächsten Schritten definieren Sie, wie und was synchronisiert werden soll.

- [Artikel synchronisieren](synchronize-items.md)
- [Debitoren synchronisieren](synchronize-customers.md)
- [Bestellungen synchronisieren](synchronize-orders.md)

## <a name="see-also"></a>Siehe auch

[Test- und Trainingsszenarien](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

