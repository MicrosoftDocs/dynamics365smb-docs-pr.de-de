---
title: Erweiterungen installieren und deinstallieren
description: Hier erfahren Sie etwas über das Installieren und Deinstallieren von Erweiterungen in Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 03/25/2022
ms.author: solsen
ms.openlocfilehash: fcdfe843071bc416973b7411e5702a690e7e377d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514751"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Erweiterungen in Business Central installieren und deinstallieren

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] ändern, indem Sie Erweiterungen installieren. Diese Erweiterungen können beispielsweise Funktionen hinzufügen, das Verhalten ändern oder Ihnen den Zugriff auf die neuen Onlinedienste ermöglichen. Weitere Informationen finden Sie unter [Anpassen von Business Central über Erweiterungen](ui-extensions.md).

> [!NOTE]
> Um Erweiterungen von AppSource zu installieren bzw. zu deinstallieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe „EXTEND. MGT. - ADMIN“ sein oder über den Berechtigungssatz „EXTEND. MGT. - ADMIN“ verfügen. Als Administrator können Sie anderen Benutzern in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen.
>
> Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.

> [!NOTE]  
> Der Berechtigungssatz **EXTEND. MGT. - ADMIN** wurde in Business Central 2021, Veröffentlichungszyklus 1, als Ersatz für den Berechtigungssatz **D365 EXTENSION MGT** in früheren Versionen eingeführt.

## <a name="install-an-extension"></a><a name="install"></a>Eine Erweiterung installieren

Sie verwalten die Erweiterungen auf der Seite **Erweiterungsverwaltung**. Sie können vom Startbildschirm auf diese Seite zugreifen. Alternativ wählen Sie das Symbol **Seite oder Bericht suchen** ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechten Ecke, geben Sie **Erweiterung** ein und wählen Sie dann den entsprechenden Link.  

Sie können neue Erweiterungen vom Marketplace auf [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) abrufen. Hier können Sie alle verfügbaren Erweiterungen für [!INCLUDE[prod_short](includes/prod_short.md)] anzeigen und Apps, Erweiterungen und Inhaltspakete für andere Microsoft-Produkte abrufen. Legen Sie die gewünschten Filter fest, werfen Sie einen Blick auf die Informationen für jede Erweiterung, und rufen Sie eine Erweiterung für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] ab.  

> [!NOTE]  
> Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/) über Ihr E-Mail-Konto an, das Sie für [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können auch auf den Marketplace aus [!INCLUDE[prod_short](includes/prod_short.md)]zugreifen. Auf der Seite **Erweiterungsverwaltung** können Sie die Erweiterungen sehen, die zur Zeit installiert sind, und Sie können die Seite **Marketplace für Erweiterungen** öffnen, die die [!INCLUDE[prod_short](includes/prod_short.md)]-Erweiterungen anzeigt, die aktuell über die AppSource verfügbar sind. Wenn Sie den Link *Weitere Apps* auswählen, werden Sie auf [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) weitergeleitet.  

Wenn Sie eine Erweiterung auswählen, können Sie erfahren, was die Erweiterung ausführt, und auf die Hilfe für die Erweiterung zugreifen, um mehr darüber zu erfahren. Wenn Sie eine Erweiterung erhalten möchten, müssen Sie die Nutzungsbedingungen zustimmen. Wenn Sie Erweiterungen von der AppSource-Website abrufen, werden Sie in [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet, um die Installation abzuschließen.  

Wenn Sie eine Erweiterung installieren, müssen Sie diese möglicherweise einrichten, wie ein Konto zur Verwendung mit Erweiterung für **PayPal Payments Standard für [!INCLUDE[prod_short](includes/prod_short.md)]** definieren.
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

## <a name="upload-a-per-tenant-extension-pte"></a>Eine Pro-Tenant-Erweiterung (PTE) hochladen

Sie laden eine PTE hoch, indem Sie die Seite **Erweiterungsverwaltung** verwenden. Gehen Sie auf der Seite **Erweiterungsverwaltung** zu **Verwalten** und wählen Sie dann **Erweiterung hochladen**. Geben Sie auf der Seite **Erweiterung hochladen und bereitstellen** die hochzuladende .app-Datei an. Um fortzufahren, wählen Sie die Schaltfläche **Akzeptieren** und dann die Schaltfläche **Bereitstellen**. Damit wird der Prozess des Bereitstellens des PTE gestartet.

Wenn der PTE Änderungen am Schema enthält, können Sie *einen Upload des PTE erzwingen*. Wählen Sie dazu im **Schema-Synchronisationsmodus** die Option **Erzwingen**. Sie erhalten einen Bestätigungsdialog, den Sie akzeptieren müssen, bevor Sie fortfahren.  

## <a name="uninstall-an-extension"></a>Eine Erweiterung deinstallieren

Sie deinstallieren eine Erweiterung, indem Sie die Seite **Erweiterungsverwaltung** verwenden. Wenn Sie eine Erweiterung deinstallieren und Sie Ihre Meinung anschließend ändern, können Sie die Erweiterung erneut installieren. Wenn Sie eine Erweiterung deinstallieren, die Sie verwendet haben, werden die Daten standardmäßig beibehalten, falls Sie die Erweiterung erneut installieren sollten. Sie können die Daten jedoch auch zusammen mit der Erweiterung löschen. Verwenden Sie hierfür das Kontrollkästchen **Erweiterungsdaten löschen**. Standardmäßig ist dieses Kontrollkästchen *nicht aktiviert*.

> [!IMPORTANT]  
> Wenn Sie das Kontrollkästchen **Erweiterungsdaten löschen** aktivieren, wird ein Bestätigungsdialogfeld angezeigt, in dem Sie **OK** auswählen müssen. Wenn das Kontrollkästchen **Erweiterungsdaten löschen** aktiviert ist und Sie die Erweiterung jetzt deinstallieren, werden Sie aufgefordert, die Deinstallation der Erweiterung und das Löschen der Daten zu bestätigen. Die Aktion kann nicht rückgängig gemacht werden.
Einige Erweiterungen sind erforderlich. Sie können diese nicht von der **Extension Management** Seite deinstallieren. Wenn Sie es versuchen, wird eine Fehlermeldung angezeigt.  

## <a name="see-also"></a>Siehe auch

[Anpassen von Business Central](ui-customizing-overview.md)  
[Business Central-Erweiterungen von anderen Anbietern](ui-extensions-other.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[Aktivieren von Debitoren-Zahlungen durch PayPal](sales-how-enable-payment-service-extensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen migrieren](across-import-data-configuration-packages.md)  
[Einrichten der britischen Postleitzahlerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen für andere Anbieter](ui-extensions-other.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]