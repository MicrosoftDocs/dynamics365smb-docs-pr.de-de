---
title: Erste Schritte mit Konnektor für Shopify
description: Erste Schritte beim Konfigurieren der Verbindung zwischen Business Central und Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 64fae9efdda832f14593564b9a19101d120c9712
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808933"
---
# <a name="get-started-with-the-shopify-connector"></a>Erste Schritte mit dem Shopify-Konnektor

Verbinden Sie Ihre(n) Shopify Store(s) mit [!INCLUDE [prod_short](../includes/prod_short.md)], um maximieren Sie die Produktivität Ihres Unternehmens. Sie können Erkenntnisse aus Ihrem Unternehmen und Ihrem Shopify Store als eine Einheit verwalten und anzeigen. 

Der Shopify-Konnektor umfasst die folgenden Funktionen:

- Unterstützung für mehrere Shopify-Shops  

  - Jeder Shop verfügt über eine eigene Einrichtung, einschließlich einer Sammlung von Produkten, Standorten zur Bestandsberechnung und Preislisten.  
- Bidirektionale Synchronisierung von Artikeln oder Produkten  

  - Der Konnektor synchronisiert Bilder, Artikelvarianten, Barcodes, Kreditorenartikelnummer, erweiterte Texte und Tags.  
  - Exportieren Sie Artikelattribute nach Shopify.  
  - Verwenden Sie ausgewählte Debitorenpreisgruppen und Rabatte, um die nach Shopify exportierten Preise zu definieren.  
  - Entscheiden Sie, ob Artikel automatisch erstellt werden können, oder lassen Sie nur Aktualisierungen bestehender Produkte zu.  
- Synchronisierung von Lagerbeständen  

  - Wählen Sie einige oder alle verfügbaren Standorte in [!INCLUDE [prod_short](../includes/prod_short.md)] aus.  
  - Aktualisieren Sie die Lagerbestände an mehreren Standorten in Shopify.  
- Bidirektionale Synchronisierung von Debitoren  

  - Ordnen Sie Debitoren intelligent per Telefon und E-Mail zu.  
  - Verwenden Sie beim Erstellen von Debitoren länderspezifische Vorlagen, um sicherzustellen, dass die Steuereinstellungen korrekt sind.  
- Aufträge aus Shopify importieren  

  - Während des Imports können Sie Debitoren automatisch in [!INCLUDE [prod_short](../includes/prod_short.md)] erstellen oder sich dazu entscheiden, diese in Shopify zu verwalten.  
  - Schließen Sie Bestellungen ein, die in anderen Kanälen wie Shopify POS oder Amazon erstellt wurde.  
  - Versandkosten, Geschenkgutscheine, Tipps, Versand- und Zahlungsmethoden, Transaktionen und Betrugsrisiko.  
  - Erhalten Sie Auszahlungsinformationen von Shopify Payments.  
- Einfache Verfolgung von Auftragserfüllungsinformationen  

  - Wählen Sie optional aus, Artikelverfolgungsinformationen aus [!INCLUDE [prod_short](../includes/prod_short.md)] in Shopify zu schreiben.  

Um Shopify mit [!INCLUDE [prod_short](../includes/prod_short.md)] zu verwenden, müssen Sie zuerst ein paar Schritte ausführen. Dieser Artikel dient als Leitfaden für die vollständige Integration Ihres Shopify-Shops in [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Voraussetzungen für Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Einen Shopify-Onlineshop

Um ein neues Shopify-Konto zu erstellen oder sich für eine kostenlose 14-tägige Testversion anzumelden, navigieren Sie zu [Shopify](https://www.shopify.com/). Weitere Informationen zum Erstellen und Personalisieren Ihres Onlineshops finden Sie unter [Shopify-Hilfezentrum](https://help.shopify.com/).
  
Andere Vertriebskanäle werden unterstützt, z. B. Shopify-POS.

### <a name="recommended-settings"></a>Empfohlene Einstellungen

- Deaktivieren Sie **Bestellung automatisch archivieren** im Abschnitt **Auftragsabwicklung** in den Einstellungen für die [**Kasse**](https://www.shopify.com/admin/settings/checkout) in Ihrer **Shopify-Verwaltung**.

Weitere Informationen zu Shopify-Einstellungen für Demo- und Testszenarien finden Sie unter [Test- und Trainingsszenarien](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Voraussetzungen für Business Central

- Stellen Sie sicher, dass die **[Shopify Connector](https://go.microsoft.com/fwlink/?linkid=2196238)**-App installiert ist.

Die App ist für alle Neuanmeldungen und Testversionen vorinstalliert. Weitere Informationen zum Installieren von Apps über den Marktplatz erhalten Sie unter [Installieren und Deinstallieren von Erweiterungen](../ui-extensions-install-uninstall.md#install). Führen Sie die unten aufgeführten Schritte aus, wenn Sie nicht über [!INCLUDE[prod_short](../includes/prod_short.md)] verfügen.

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>Installatieren der **Dynamics 365 Business Central**-App in Ihrem Shopify-Onlineshop

Für das bestehende [!INCLUDE[prod_short](../includes/prod_short.md)] ist dieser Schritt optional und kann übersprungen werden.

1. Suchen Sie die [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-App im [Shopify Appstore](https://apps.shopify.com/)
2. Wählen Sie die Schaltfläche **App hinzufügen** aus. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden. Wählen Sie den gewünschten Onlineshop aus, falls Sie über mehrere verfügen.
3. Nachdem Sie den Datenschutz und die Berechtigungen überprüft haben, wählen Sie die Schaltfläche **App installieren** aus.
  Sie können die installierte **Dynamics 365 Business Central**-App im Abschnitt **Apps** in der Seitenleiste von **Shopify-Verwaltung** finden und öffnen.
4. Wählen **Jetzt registrieren** aus, um die Testversion von [!INCLUDE[prod_short](../includes/prod_short.md)] zu starten, oder wählen Sie **Anmelden** aus, wenn Sie bereits über [!INCLUDE[prod_short](../includes/prod_short.md)] verfügen. Sie werden zu Ihrem [!INCLUDE[prod_short](../includes/prod_short.md)] unter [Business Central](https://businesscentral.dynamics.com) weitergeleitet.
5. Die nächsten Schritte sollten in [!INCLUDE[prod_short](../includes/prod_short.md)] ausgeführt werden.

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Verbinden von Business Central mit dem Shopify-Onlineshop

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu**.  
3. Geben Sie im Feld **Code** den gewünschten Code ein.  
4. Geben Sie im Feld **Shopify-URL** die URL Ihres zu verbindenden Onlineshops ein. Verwenden Sie das folgende Format: `https://{shop}.myshopify.com/`.
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

