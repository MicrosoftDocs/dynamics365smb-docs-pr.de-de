---
title: Erweiterungen installieren, um Business Central anzupassen
description: Informationen zum Hinzufügen von Funktionalität und Anpassungen für Business Central durch die Installation von Erweiterungen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: app, add-in, manifest, customize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fa72fad5899fab4830bf6c0956eaf99b6c773a53
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757017"
---
# <a name="customizing-business-central-using-extensions"></a>Anpassen von Business Central mithilfe der Erweiterungen

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] ändern, indem Sie beispielsweise Erweiterungen installieren, die Funktionalität hinzufügen, das Verhalten ändern oder Zugriff auf die neuen Onlinediensten geben.

> [!NOTE]
> Um Erweiterungen von AppSource zu installieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe D365 EXTENSION MGMT sein oder über den Berechtigungssatz D365 EXTENSION MGMT verfügen. Als Administrator können Sie anderen Benutzern in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen.

Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.

> [!IMPORTANT]  
> Das Hochladen von Tenant-Erweiterungen und die Installation von AppSource-Erweiterungen werden über die Seite **Erweiterungsverwaltung** für lokale Installationen nicht unterstützt.

Wenn Sie das [!INCLUDE[prod_short](includes/prod_short.md)] zuerst starten, werden bestimmte Erweiterungen bereits eingerichtet. Im Zeitverlauf werden mehr Erweiterungen für Sie zugänglich und Sie können auswählen, ob Sie die Erweiterung verwenden möchten oder nicht.

Beispielsweise bietet Microsoft eine Erweiterung an, die die Integration mit PayPal Payments Standard ermöglicht. Diese Erweiterung wird standardmäßig eingerichtet.
Wenn aber keine andere Erweiterung bereitgestellt wird, die die Integration mit einem anderen Zahlungsservice anbietet, können Sie die neue Erweiterung einrichten und dann auswählen, welcher der beiden Services verwendet werden soll.  

Sie verwalten die Erweiterung auf der **Erweiterungs-Verwaltungs**-Seite. Sie können vom Startbildschirm auf diese Seite zugreifen. Wählen Sie alternativ das Symbol **Nach Seite oder Bericht suchen** aus ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechter Ecke, geben Sie **Erweiterung** ein, und wählen Sie dann den zugehörigen Link aus. Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Erweiterungen](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Wenn Sie der Meinung sind, Sie sollten Zugriff zu einer Erweiterung haben, können die Funktionalität aber nicht finden, überprüfen Sie die Seite **Erweiterungsverwaltung**, wenn die Erweiterung dort nicht aufgeführt wird, können Sie sie einrichten, wie im folgenden Abschnitt erläutert.  

> [!NOTE]  
> Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/) über Ihr E-Mail-Konto an, das Sie für [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können auch auf den Marketplace aus [!INCLUDE[prod_short](includes/prod_short.md)]zugreifen. Auf der Seite **Erweiterungsverwaltung** können Sie die Erweiterungen sehen, die zur Zeit installiert sind, und Sie können die Seite **Marketplace für Erweiterungen** öffnen, die die [!INCLUDE[prod_short](includes/prod_short.md)]-Erweiterungen anzeigt, die aktuell über die AppSource verfügbar sind. Wenn Sie den Link *Weitere Apps* auswählen, werden Sie auf [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) weitergeleitet.  

Wenn Sie eine Erweiterung auswählen, können Sie erfahren, was die Erweiterung ausführt, und auf die Hilfe für die Erweiterung zugreifen, um mehr darüber zu erfahren. Wenn Sie eine Erweiterung erhalten möchten, müssen Sie die Nutzungsbedingungen zustimmen. Wenn Sie Erweiterungen von der AppSource-Website abrufen, werden Sie in [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet, um die Installation abzuschließen.  

Wenn Sie eine Erweiterung installieren, müssen Sie diese möglicherweise einrichten, wie ein Konto zur Verwendung mit Erweiterung für **Paypal Payments Standard für [!INCLUDE[prod_short](includes/prod_short.md)]** definieren.
Andere Erweiterungen fügen einfach Felder einer vorhandenen Seite hinzu, oder sie fügen beispielsweise eine neue Seite hinzu.   

Wenn Sie eine Erweiterung deinstallieren und Sie dann Ihre Absicht ändern, können Sie sie wieder einrichten. Wenn Sie eine Erweiterung deinstallieren, die Sie verwendet haben, werden die Daten beibehalten, sodass, wenn Sie die Erweiterung erneut einrichten, die Daten noch verfügbar sind. Es sind einige Erweiterungen erforderlich. Sie können diese nicht von der **Extension Management** Seite deinstallieren. Wenn Sie es versuchen, wird eine Fehlermeldung angezeigt.  

Einige Erweiterungen werden von Microsoft bereitgestellt, und andere Erweiterungen werden von anderen [anderen Unternehmen](ui-extensions-other.md) bereitgestellt. Alle Erweiterungen werden getestet, bevor sie zugänglich gemacht werden, aber wir empfehlen, dass Sie auf die Links zugreifen, die mit jeder Erweiterung zur Verfügung gestellt wurden, um mehr über die Erweiterung zu erfahren, bevor Sie entscheiden, sie zu installieren.  

Microsoft stellt die folgenden Erweiterungen bereit:  

* [AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md)
* [Ceridian-Gehaltsliste](ui-extensions-ceridian-payroll.md)
* [Unternehmens-Hub](ui-extensions-company-hub.md)  
* [Dynamics GP Datenmigration](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Wesentliche Geschäfts-Einblicke](ui-extensions-essential-business-insights.md)
* [Schliffbildanalysator](ui-extensions-image-analyzer.md)
* [Intelligente Cloud](ui-extensions-data-replication.md)
* [Intelligente Cloud-Basis](ui-extensions-intelligent-cloud.md)  
* [Vorhersagen verspäteter Zahlungen](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [QuickBooks Datenmigration](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online-Datenmigration](ui-extensions-quickbooks-online-data-migration.md)
* [QuickBooks-Lohndatei-Import](ui-extensions-quickbooks-payroll.md)
* [Verkaufs- und Lagerbestandsplanung](ui-extensions-sales-forecast.md)
* [MwSt.-Gruppe](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK – C5 Datenmigration](ui-extensions-c5-data-migration.md)
* [DK – Zahlungen und Abstimmungen](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK – Steuerdateiformate](ui-extensions-tax-file-formats-dk.md)
* [Die britische Postleitzahlenerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [USA/CA/GB/AU/NZ/ZA – Überweisungsbescheid senden](ui-extensions-send-remittance-advice.md)

> [!NOTE]  
> Neue Erweiterungen sind nicht direkt in AppSource verfügbar, nachdem ein Update angekündigt wurde. Halten Sie unter [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) Ausschau nach der Erweiterung.

## <a name="see-also"></a>Siehe auch

[Anpassen von Business Central](ui-customizing-overview.md)  
[Business Central-Erweiterungen von anderen Anbietern](ui-extensions-other.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[Aktivieren von Debitoren-Zahlungen durch Paypal](sales-how-enable-payment-service-extensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](across-import-data-configuration-packages.md)  
[Einrichten der britischen Postleitzahlerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen für andere Anbieter](ui-extensions-other.md)  
[Erste Schritte](product-get-started.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]