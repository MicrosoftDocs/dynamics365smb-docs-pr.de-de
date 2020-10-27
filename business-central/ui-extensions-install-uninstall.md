---
title: Installieren und Deinstallieren von Erweiterungen in Business Central | Microsoft Docs
description: Hier erfahren Sie etwas über das Installieren und Deinstallieren von Erweiterungen in Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: a0e62b60f9624cad44efa7fd42c5840a2ecd07b5
ms.sourcegitcommit: aea079b66e35c447bf31a11ffc2069cfdaf2ef38
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "3970360"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Installieren und Deinstallieren von Erweiterungen in Business Central

Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] ändern, indem Sie Erweiterungen installieren. Diese Erweiterungen können beispielsweise Funktionen hinzufügen, das Verhalten ändern oder Ihnen den Zugriff auf die neuen Onlinedienste ermöglichen. Weitere Informationen finden Sie unter [Anpassen von Business Central über Erweiterungen](ui-extensions.md).

> [!NOTE]
> Um Erweiterungen von AppSource zu installieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe D365 EXTENSION MGMT sein oder über den Berechtigungssatz D365 EXTENSION MGMT verfügen. Als Administrator können Sie anderen Benutzern in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen.<br /><br />
Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.

## <a name="installing-an-extension"></a>Eine Erweiterung wird installiert

Sie verwalten die Erweiterungen auf der Seite **Erweiterungsverwaltung** . Sie können vom Startbildschirm auf diese Seite zugreifen. Wählen Sie alternativ das Symbol **Nach Seite oder Bericht suchen** aus ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechter Ecke, geben Sie **Erweiterung** ein, und wählen Sie dann den zugehörigen Link aus.  

Sie können neue Erweiterungen vom Marketplace auf [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) abrufen. Hier können Sie alle verfügbaren Erweiterungen für [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen und Apps, Erweiterungen und Inhaltspakete für andere Microsoft-Produkte abrufen. Legen Sie die gewünschten Filter fest, werfen Sie einen Blick auf die Informationen für jede Erweiterung, und rufen Sie eine Erweiterung für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] ab.  

> [!NOTE]  
> Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/) über Ihr E-Mail-Konto an, das Sie für [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können auch auf den Marketplace aus [!INCLUDE[d365fin](includes/d365fin_md.md)]zugreifen. Auf der Seite **Erweiterungsverwaltung** können Sie die Erweiterungen sehen, die zur Zeit installiert sind, und Sie können die Seite **Marketplace für Erweiterungen** öffnen, die die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Erweiterungen anzeigt, die aktuell über die AppSource verfügbar sind. Wenn Sie den Link *Weitere Apps* auswählen, werden Sie auf [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) weitergeleitet.  

Wenn Sie eine Erweiterung auswählen, können Sie erfahren, was die Erweiterung ausführt, und auf die Hilfe für die Erweiterung zugreifen, um mehr darüber zu erfahren. Wenn Sie eine Erweiterung erhalten möchten, müssen Sie die Nutzungsbedingungen zustimmen. Wenn Sie Erweiterungen von der AppSource-Website abrufen, werden Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] angemeldet, um die Installation abzuschließen.  

Wenn Sie eine Erweiterung installieren, müssen Sie diese möglicherweise einrichten, wie ein Konto zur Verwendung mit Erweiterung für **Paypal Payments Standard für [!INCLUDE[d365fin](includes/d365fin_md.md)]** definieren.
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
* [UK - GetAddress.io britische Postleitzahlen](ui-extensions-getaddressio.md)
* [USA/CA/GB/AU/NZ/ZA – Überweisungsbescheid senden](ui-extensions-send-remittance-advice.md)

## <a name="uninstalling-an-extension"></a>Deinstallieren einer Erweiterung

Sie deinstallieren eine Erweiterung über die Seite **Erweiterungsverwaltung** . Wenn Sie eine Erweiterung deinstallieren und Sie Ihre Meinung anschließend ändern, können Sie die Erweiterung erneut installieren. Wenn Sie eine Erweiterung deinstallieren, die Sie verwendet haben, werden die Daten standardmäßig beibehalten, falls Sie die Erweiterung erneut installieren sollten. Sie können die Daten jedoch auch zusammen mit der Erweiterung löschen. Verwenden Sie hierfür das Kontrollkästchen **Erweiterungsdaten löschen** . Standardmäßig ist dieses Kontrollkästchen *nicht aktiviert* .

> [!IMPORTANT]  
> Wenn Sie das Kontrollkästchen **Erweiterungsdaten löschen** aktivieren, wird ein Bestätigungsdialogfeld angezeigt, in dem Sie **OK** auswählen müssen. Wenn das Kontrollkästchen **Erweiterungsdaten löschen** aktiviert ist und Sie die Erweiterung jetzt deinstallieren, werden Sie aufgefordert, die Deinstallation der Erweiterung und das Löschen der Daten zu bestätigen. Die Aktion kann nicht rückgängig gemacht werden.
Einige Erweiterungen sind erforderlich. Sie können diese nicht von der **Extension Management** Seite deinstallieren. Wenn Sie es versuchen, wird eine Fehlermeldung angezeigt.  

## <a name="see-also"></a>Siehe auch

[Erweitern von Dynamics 365 Business Central](about-develop-extensions.md)  
[Business Central-Erweiterungen von anderen Anbietern](ui-extensions-other.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[Aktivieren von Debitoren-Zahlungen durch Paypal](sales-how-enable-payment-service-extensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](across-import-data-configuration-packages.md)  
[Einrichten der britischen Postleitzahlerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen für andere Anbieter](ui-extensions-other.md)  
[Erste Schritte](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
