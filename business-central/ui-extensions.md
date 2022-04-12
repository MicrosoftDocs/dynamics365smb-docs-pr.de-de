---
title: Anpassen von Business Central Online mithilfe der Erweiterungen
description: Erfahren Sie alles über das Hinzufügen von Funktionen und das Anpassen von Business Central durch die Installation von Erweiterungen hier.
author: edupont04
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont
ms.openlocfilehash: 56c564274e396d9699286b18d882c2a21f8721ef
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510687"
---
# <a name="customizing-business-central-online-using-extensions"></a>Anpassen von Business Central Online mithilfe der Erweiterungen

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] online ändern, indem Sie beispielsweise Erweiterungen installieren, die Funktionalität hinzufügen, das Verhalten ändern oder Zugriff auf die neuen Onlinediensten geben.

> [!NOTE]
> Um Erweiterungen von AppSource zu installieren bzw. zu deinstallieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe **D365 Extension Mgt.** sein oder explizit über den Berechtigungssatz **EXTEN. MGT. - ADMIN** verfügen. Als Administrator können Sie anderen Benutzern in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).  
>
> Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

> [!IMPORTANT]  
> Das Hochladen von Tenant-Erweiterungen und die Installation von AppSource-Erweiterungen werden über die Seite **Erweiterungsverwaltung** für lokale Installationen nicht unterstützt. Sie können AppSource-Erweiterungen nicht vor Ort installieren, auch in Docker-basierten Bereitstellungen.

Wenn Sie das [!INCLUDE[prod_short](includes/prod_short.md)] zuerst starten, werden bestimmte Erweiterungen bereits eingerichtet. Im Zeitverlauf werden mehr Erweiterungen für Sie zugänglich und Sie können auswählen, ob Sie die Erweiterung verwenden möchten oder nicht.

Beispielsweise bietet Microsoft eine Erweiterung an, die die Integration mit PayPal Payments Standard ermöglicht. Diese Erweiterung wird standardmäßig eingerichtet.
Wenn aber keine andere Erweiterung bereitgestellt wird, die die Integration mit einem anderen Zahlungsservice anbietet, können Sie die neue Erweiterung einrichten und dann auswählen, welcher der beiden Services verwendet werden soll.  

Sie verwalten die Erweiterung auf der **Erweiterungs-Verwaltungs**-Seite. Sie können vom Startbildschirm auf diese Seite zugreifen. Wählen Sie alternativ das Symbol **Nach Seite oder Bericht suchen** aus ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechter Ecke, geben Sie **Erweiterung** ein, und wählen Sie dann den zugehörigen Link aus. Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Erweiterungen](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Wenn Sie der Meinung sind, Sie sollten Zugriff zu einer Erweiterung haben, können die Funktionalität aber nicht finden, überprüfen Sie die Seite **Erweiterungsverwaltung**, wenn die Erweiterung dort nicht aufgeführt wird, können Sie sie einrichten, wie im folgenden Abschnitt erläutert.  

> [!NOTE]  
> Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/) über Ihr E-Mail-Konto an, das Sie für [!INCLUDE[prod_short](includes/prod_short.md)] online verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können auch auf den Marketplace aus [!INCLUDE[prod_short](includes/prod_short.md)]zugreifen. Auf der Seite **Erweiterungsverwaltung** können Sie die Erweiterungen sehen, die zur Zeit installiert sind, und Sie können die Seite **Marketplace für Erweiterungen** öffnen, die die [!INCLUDE[prod_short](includes/prod_short.md)]-Erweiterungen anzeigt, die aktuell über die AppSource verfügbar sind. Wenn Sie den Link *Weitere Apps* auswählen, werden Sie auf [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) weitergeleitet.  

Wenn Sie eine Erweiterung auswählen, können Sie erfahren, was die Erweiterung ausführt, und auf die Hilfe für die Erweiterung zugreifen, um mehr darüber zu erfahren. Wenn Sie eine Erweiterung erhalten möchten, müssen Sie die Nutzungsbedingungen zustimmen. Wenn Sie Erweiterungen von der AppSource-Website abrufen, werden Sie in [!INCLUDE[prod_short](includes/prod_short.md)] angemeldet, um die Installation abzuschließen.  

Wenn Sie eine Erweiterung installieren, müssen Sie diese möglicherweise einrichten, wie ein Konto zur Verwendung mit Erweiterung für **PayPal Payments Standard für [!INCLUDE[prod_short](includes/prod_short.md)]** definieren.
Andere Erweiterungen fügen einfach Felder einer vorhandenen Seite hinzu, oder sie fügen beispielsweise eine neue Seite hinzu.   

Wenn Sie eine Erweiterung deinstallieren und Sie dann Ihre Absicht ändern, können Sie sie wieder einrichten. Wenn Sie eine Erweiterung deinstallieren, die Sie verwendet haben, werden die Daten beibehalten, sodass, wenn Sie die Erweiterung erneut einrichten, die Daten noch verfügbar sind. Es sind einige Erweiterungen erforderlich. Sie können diese nicht von der **Extension Management** Seite deinstallieren. Wenn Sie es versuchen, wird eine Fehlermeldung angezeigt.  

Einige Erweiterungen werden von Microsoft bereitgestellt, und andere Erweiterungen werden von anderen [anderen Unternehmen](ui-extensions-other.md) bereitgestellt. Alle Erweiterungen werden getestet, bevor sie zugänglich gemacht werden, aber wir empfehlen, dass Sie auf die Links zugreifen, die mit jeder Erweiterung zur Verfügung gestellt wurden, um mehr über die Erweiterung zu erfahren, bevor Sie entscheiden, sie zu installieren.  

> [!NOTE]  
> Sie können nach neuen Erweiterungen von Microsoft und anderen Anbietern unter [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) Ausschau halten.


## <a name="extensions-and-data-transfer"></a>Erweiterungen und Datenübertragung

Da die folgenden Erweiterungen mit anderen Diensten kommunizieren, übertragen sie möglicherweise Daten außerhalb der [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung:

* AMC Banking 365 Fundamentals-Erweiterung
* Bild-Analyse
* Vorhersage verspäteter Zahlungen
* PayPal Payments Standard
* Verkaufs‑ und Lagerbestandsplanung
* WorldPay Payments Standard

Dies gilt auch für einige Funktionen in der Basisanwendung, z. B. die folgenden Funktionen:

* Cashflowplanung
* Belegaustauschdienst
* Dataverse-Verbindungen
* OCR-Dienst
* Online Map
* EU VAT Reg.-Nr. Service

## <a name="recommended-apps"></a>Empfohlene Apps
Microsoft Partner und Wiederverkäufer können eine Erweiterung erstellen, mit der sie Listen von Apps zusammenstellen können, die sie ihren Kunden häufig empfehlen. Wenn sie dies tun und die Erweiterung für Ihren Mandanten bereitstellen, sind die Apps auf der Seite **Empfohlene Apps** verfügbar. Dort können Sie sich über jede App informieren und entscheiden, ob Sie sie installieren möchten.

> [!NOTE]
> Wenn Sie ein Microsoft-Partner oder -Wiederverkäufer sind und eine Liste empfohlener Apps bereitstellen möchten, lesen Sie [Empfohlene Apps von AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## <a name="see-also"></a>Weitere Informationen

[Erweiterungen installieren und deinstallieren](ui-extensions-install-uninstall.md)  
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
