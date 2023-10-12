---
title: Apps installieren und deinstallieren
description: Hier erfahren Sie etwas über das Installieren und Deinstallieren von Apps und Erweiterungen in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 09/07/2023
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 2514, 20350'
---

# Erweiterungen (Apps) in Business Central installieren und deinstallieren

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] ändern, indem Sie Apps installieren. Sie können beispielsweise Funktionen hinzufügen, das Verhalten ändern oder Ihnen den Zugriff auf die neuen Onlinedienste ermöglichen. Weitere Informationen finden Sie unter [Anpassen von Business Central über Erweiterungen](ui-extensions.md).

> [!NOTE]
> Um Apps von AppSource zu installieren bzw. zu deinstallieren oder Apps pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe „D365 Extension MGT“ sein oder über „EXTEND. MGT. - ADMIN“ verfügen. Als Administrator können Sie anderen Benutzenden in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen. Um mehr über Benutzergruppen und Berechtigungen zu erfahren, gehen Sie zu [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).
>
> Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.

Um eine Erweiterung zu verwenden, müssen Ihnen die zugehörigen Berechtigungssätze zugewiesen werden.

## <a name="install"></a>Erweiterung installieren

Sie verwalten Apps und Erweiterungen auf der **Erweiterungsverwaltung**-Seite. Sie können vom Startbildschirm auf diese Seite zugreifen. Alternativ wählen Sie das Symbol **Seite oder Bericht suchen** ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechten Ecke, geben Sie **Erweiterung** ein und wählen Sie dann den entsprechenden Link.  

Sie können neue Apps und Erweiterungen vom Marketplace auf [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) abrufen. Der Marktplatz bietet alle verfügbaren Apps für [!INCLUDE[prod_short](includes/prod_short.md)], sowie Apps und Inhaltspakete für andere Microsoft-Produkte. Legen Sie die gewünschten Filter fest, werfen Sie einen Blick auf die Informationen für jede Erweiterung, und rufen Sie eine Erweiterung für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] ab.  

> [!NOTE]  
> Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/) über Ihr E-Mail-Konto an, das Sie für [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können AppSource möglicherweise auch von [!INCLUDE[prod_short](includes/prod_short.md)] aus starten. Auf der Seite **Erweiterungsverwaltung** können Sie die Apps sehen, die zur Zeit installiert sind, und Sie können die Seite **Marketplace für Erweiterungen** öffnen, die die [!INCLUDE[prod_short](includes/prod_short.md)]-Apps anzeigt, die aktuell über die AppSource verfügbar sind. Wenn Sie den Link *Weitere Apps* auswählen, werden Sie auf [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) weitergeleitet.  

Wählen Sie eine App aus, um mehr darüber zu erfahren, was sie ausführt, und auf die Hilfe für die App zugreifen, um mehr darüber zu erfahren. Wenn Sie eine App erhalten möchten, müssen Sie ihre Nutzungsbedingungen zustimmen. Wenn Sie Apps von der AppSource-Website abrufen, werden Sie in [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet, um die Installation abzuschließen.  

Nachdem Sie eine App installiert haben, müssen Sie sie möglicherweise einrichten. Bei einigen Apps müssen Sie einige Informationen angeben, bevor Sie sie verwenden können. Beispielsweise nach der Installation der App **PayPal Payments Standard** müssen Sie die E-Mail-Adresse oder die Händlerkonto-ID für Ihr PayPal-Konto angeben. Um eine App einzurichten oder herauszufinden, welche Informationen Sie benötigen, wählen Sie auf der Seite **Installierte Erweiterungen** die Aktion **Einrichten** aus.  

Andere Apps fügen einfach Felder einer vorhandenen Seite hinzu, oder sie fügen beispielsweise eine neue Seite hinzu.

Wenn Sie eine App deinstallieren und Sie dann Ihre Absicht ändern, können Sie sie wieder einrichten. Wenn Sie eine App deinstallieren, die Sie verwendet haben, werden Ihre Daten nicht gelöscht. Die Daten sind wieder verfügbar, wenn Sie die App erneut installieren.

Einige Apps werden von Microsoft bereitgestellt, und andere Apps werden von anderen [anderen Unternehmen](ui-extensions-other.md) bereitgestellt. Wir empfehlen Ihnen, mehr über die App zu erfahren, bevor Sie sie installieren.

Microsoft stellt die folgenden Apps bereit:

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

## Eine App einrichten

Nachdem Sie eine App installiert haben, müssen Sie sie möglicherweise einrichten. Zum Beispiel für die App **PayPal Payments Standard for [!INCLUDE[prod_short](includes/prod_short.md)]** müssen Sie das zu verwendende PayPal-Konto angeben. Wenn dies der Fall ist, werden Sie nach Abschluss der Installation von [!INCLUDE[prod_short](includes/prod_short.md)] gefragt, ob Sie die App sofort einrichten möchten. Setups können erforderlich sein, damit die App funktioniert, oder optional.

Wenn Sie Ihre App sofort einrichten möchten und sie eine erforderliche Einrichtung hat, öffnet [!INCLUDE[prod_short](includes/prod_short.md)] die erforderliche Einrichtung. Die Einrichtung kann entweder eine Seite sein, auf der Sie Informationen eingeben, oder eine unterstützte Einrichtungsanleitung, die Sie durch die einzelnen Schritte führt. Wenn Sie die Einrichtung nicht auf einmal abschließen, können Sie die Seite **Einrichtungen für _Name der App_** verwenden, die alle Einrichtungen für die App auflistet. Erforderliche Einrichtungen, gekennzeichnet durch **Fettschrift**.

## Eine Pro-Tenant-Erweiterung (PTE) hochladen

Sie laden eine PTE hoch, indem Sie die Seite **Erweiterungsverwaltung** verwenden. Gehen Sie auf der Seite **Erweiterungsverwaltung** zu **Verwalten** und wählen Sie dann **Erweiterung hochladen**. Geben Sie auf der Seite **Erweiterung hochladen und bereitstellen** die hochzuladende .app-Datei an. Um fortzufahren, wählen Sie die Schaltfläche **Akzeptieren** und dann die Schaltfläche **Bereitstellen** aus. Dadurch wird der Bereitstellungsprozess des PTE gestartet.

Wenn der PTE Änderungen am Schema enthält, können Sie *einen Upload des PTE erzwingen*. Wählen Sie dazu im **Schema-Synchronisationsmodus** die Option **Erzwingen**. Sie erhalten einen Bestätigungsdialog, den Sie akzeptieren müssen, bevor Sie fortfahren.  

## Eine App deinstallieren

Sie deinstallieren eine App, indem Sie die Seite **Erweiterungsverwaltung** verwenden. Um eine App zu deinstallieren, wählen Sie sie auf der Seite und wählen Sie dann die Aktion **Deinstallieren** aus. Wenn Sie eine App deinstallieren und Sie Ihre Meinung anschließend ändern, können Sie die App erneut installieren.

Wenn Sie eine App deinstallieren, die Sie verwendet haben, werden Ihre Daten nicht standardmäßig gelöscht. Wenn Sie sicher sind, dass Sie die App nicht erneut installieren, können Sie die Daten löschen, wenn Sie sie deinstallieren. Um Daten zu löschen, wenn Sie eine App deinstallieren, aktivieren Sie den Umschalter **Erweiterungsdaten löschen** . Sie erhalten einen Bestätigungsdialog und müssen zur Aktivierung **Ja** wählen. Nachdem der Schalter **Erweiterungsdaten löschen** aktiviert wurde, können Sie die App deinstallieren, und Sie werden aufgefordert, die Deinstallation der App und das Löschen der Daten zu bestätigen.

> [!IMPORTANT]  
> * Möglicherweise gibt es andere Apps, die die zu deinstallierende App erfordern oder von ihr abhängen. Diese Apps werden als *abhängige Elemente* bezeichnet. Sie können eine App erst deinstallieren, wenn Sie auch ihre abhängigen Erweiterungen deinstallieren. Wenn Sie eine App mit abhängigen Apps deinstallieren, werden die abhängigen Erweiterungen in einem Dialogfeld aufgelistet. Um fortzufahren, müssen Sie **Ja** auswählen, um die App und ihre abhängigen Erweiterungen zu deinstallieren.
> * Wenn Sie den Umschalter **Erweiterungsdaten löschen** aktivieren, werden durch die Deinstallation der App alle Daten für die Erweiterung *plus* die Daten für alle abhängigen Apps gelöscht. Die Aktion kann nicht rückgängig gemacht werden.
> * Einige Apps sind erforderlich und können auf der Seite **Erweiterungsverwaltung** nicht gelöscht werden.  

Wenn Sie die Daten einer deinstallierten App behalten möchten, können Sie die Daten später löschen. Auf der Seite **Verwaiste Erweiterungsdaten löschen** werden die Apps aufgelistet, für die Sie noch Daten haben. Um die Daten zu löschen, wählen Sie die Anwendung aus und wählen Sie dann **Daten löschen**. 

## Siehe auch

[Business Central anpassen](ui-customizing-overview.md)  
[Business Central-Erweiterungen von anderen Anbietern](ui-extensions-other.md)  
[Den Envestnet Yodlee Bank Feeds-Service einrichten](bank-how-setup-bank-statement-service.md)  
[Aktivieren von Debitoren-Zahlungen durch PayPal](sales-how-enable-payment-service-extensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten der britischen Postleitzahlerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen für andere Anbieter](ui-extensions-other.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
