---
title: Anpassen von Business Central Online mithilfe von Apps
description: Erfahren Sie alles über das Hinzufügen von Funktionen und das Anpassen von Business Central durch die Installation von Apps in diesem Artikel.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: solsen
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 06/27/2024
ms.service: dynamics-365-business-central
---
# <a name="customizing-business-central-online-using-apps"></a>Anpassen von Business Central Online mithilfe von Apps

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] online ändern, indem Sie beispielsweise Apps installieren, die Funktionalität hinzufügen, das Verhalten ändern oder Zugriff auf die neuen Onlinediensten geben. Diese Apps werden auch *Erweiterungen*, weil sie *erweitern* [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="manage-apps"></a>Apps verwalten

Wenn Sie das [!INCLUDE[prod_short](includes/prod_short.md)] zuerst starten, werden bestimmte Apps bereits eingerichtet. Im Zeitverlauf werden mehr Apps für Sie zugänglich und Sie können auswählen, ob Sie die App verwenden möchten oder nicht.

Beispielsweise bietet Microsoft eine App an, die die Integration mit PayPal Payments Standard ermöglicht. Diese Erweiterung wird standardmäßig eingerichtet. Es könnte jedoch eine Erweiterung geben, die die Integration mit einem anderen Zahlungsdienst ermöglicht. In diesem Fall können Sie die neue Erweiterung installieren und dann auswählen, welche Sie verwenden möchten.  

Um eine Anwendung verwenden zu können, müssen Sie über die Berechtigungen verfügen, die mit der Anwendung installiert wurden.

Um Apps von AppSource zu installieren bzw. zu deinstallieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe **D365 Extension Mgt.** sein oder explizit über den Berechtigungssatz **EXTEN. MGT. - ADMIN** verfügen. Als Administrator können Sie anderen Benutzenden in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).  

> [!IMPORTANT]  
> Zum [!INCLUDE [prod_short](includes/prod_short.md)] lokal können Sie keine Erweiterungen pro Mandant hochladen oder AppSource Apps installieren über die Seite **Erweiterungsverwaltung**. Sie können AppSource-Apps nicht vor Ort installieren, auch in Docker-basierten Bereitstellungen.

Sie verwalten die Apps auf der **Erweiterungsverwaltungs**-Seite. Sie können vom Startbildschirm auf diese Seite zugreifen. Wählen Sie alternativ das Symbol **Nach Seite oder Bericht suchen** aus ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") in der oberen rechter Ecke, geben Sie **Erweiterung** ein, und wählen Sie dann den zugehörigen Link aus. Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Apps](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Wenn Sie der Meinung sind, Sie sollten Zugriff zu einer App haben, können die Funktionalität aber nicht finden, überprüfen Sie die Seite **Erweiterungsverwaltung**, wenn die App dort nicht aufgeführt wird, können Sie sie einrichten, wie im folgenden Abschnitt erläutert.  

> [!NOTE]  
> Melden Sie sich auf [AppSource.microsoft.com](https://appsource.microsoft.com/) über Ihr E-Mail-Konto an, das Sie für [!INCLUDE[prod_short](includes/prod_short.md)] online verwenden. Verwenden Sie dasselbe E-Mail-Konto für andere Produkte und Dienste für eine reibungslose Nutzung.  

Sie können AppSource möglicherweise auch von [!INCLUDE[prod_short](includes/prod_short.md)] aus starten. Auf der Seite **Erweiterungsverwaltung** können Sie die Apps sehen, die zur Zeit installiert sind, und Sie können die Seite **Microsoft AppSource-Apps** öffnen, welche die [!INCLUDE[prod_short](includes/prod_short.md)]-Apps anzeigt, die aktuell über AppSource verfügbar sind. Wenn Sie die Aktion **AppSource anzeigen** auswählen, werden Sie an [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) weitergeleitet. Weitere Informationen finden Sie unter [AppSource-Apps verwalten](admin-manage-appsource-apps.md).

Wenn Sie eine App auswählen, können Sie erfahren, was die App ausführt, und auf die Hilfe für die App zugreifen, um mehr darüber zu erfahren. Wenn Sie eine App erhalten möchten, müssen Sie die Nutzungsbedingungen zustimmen. Wenn Sie Apps von der AppSource-Website abrufen, melden Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] an, um die Installation abzuschließen.  

Wenn Sie eine Apps installieren, müssen Sie diese möglicherweise einrichten, wie ein Konto zur Verwendung mit Erweiterung für **PayPal Payments Standard für [!INCLUDE[prod_short](includes/prod_short.md)]** definieren. Andere Apps fügen einer vorhandenen Seite Felder oder sie fügen beispielsweise eine neue Seite hinzu.

Wenn Sie eine App deinstallieren und Sie dann Ihre Absicht ändern, können Sie sie wieder einrichten. Wenn Sie eine App deinstallieren, bleiben Ihre Daten erhalten. Wenn Sie die App erneut installieren, sind sie weiterhin verfügbar. Einige Apps sind erforderlich und können nicht über die Seite **Erweiterungsverwaltung** deinstalliert werden.

Einige Apps werden von Microsoft bereitgestellt, und andere Apps werden von anderen [anderen Unternehmen](ui-extensions-other.md) bereitgestellt. Alle Apps werden getestet, bevor sie zugänglich gemacht werden, aber wir empfehlen, dass Sie auf die Links zugreifen, die mit jeder Erweiterung zur Verfügung gestellt wurden, um mehr über die App zu erfahren, bevor Sie entscheiden, sie zu installieren.  

> [!NOTE]  
> Sie können nach neuen Apps von Microsoft und anderen Anbietern unter [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) Ausschau halten.

## <a name="apps-and-data-transfer"></a>Apps und Datenübertragung

Da die folgenden Apps mit anderen Diensten kommunizieren, übertragen sie möglicherweise Daten außerhalb der [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung:

* AMC Banking 365 Fundamentals-Erweiterung
* Bild-Analyse
* Vorhersage verspäteter Zahlungen
* PayPal Payments Standard
* Umsatz- und Lagerbestandsplanung
* WorldPay Payments Standard

Dasselbe gilt für die Basisanwendung, beispielsweise für die folgenden Funktionen:

* Cashflowplanung
* Belegaustauschdienst
* Dataverse-Verbindungen
* OCR-Dienst
* Online-Karte
* EU VAT Reg.-Nr. Dienst

## <a name="connect-your-business"></a>Verbinden Sie Ihr Unternehmen

Ab 2022 Veröffentlichungszyklus 2, [!INCLUDE [prod_short](includes/prod_short.md)] Online-Umgebungen können eine oder mehrere Apps auf der Seite **Konnektivitäts-Apps** und **Banking-Apps** auflisten. Diese Apps können Ihr Unternehmen mit externen Diensten verbinden, um die Produktivität durch die Automatisierung von Prozessen zu steigern. Beispielsweise können Sie sich mit Ihren Banken verbinden und Banktransaktionen automatisch importieren. Die Apps lassen sich einfach installieren und direkt von dieser Seite aus einrichten. Wählen Sie eine App aus, um mehr über Funktionen und Preise zu erfahren.  

Zeigen Sie die Liste der vorgeschlagenen Apps an, indem Sie die Aktion **Konnektivitäts-Apps** auf der Seite **Erweiterungsverwaltung**.  

> [!NOTE]
> Die erste Person, die die Seite **Konnektivitäts-Apps** öffnet, muss der Erweiterung erlauben, sich mit einem externen Dienst zu verbinden. Lassen Sie die Verbindung einmal oder immer zu. Wenn Sie die Verbindung blockieren möchten, müssen Sie die entsprechenden Apps auf AppSource finden.

Dieser externe Dienst generiert basierend auf Ihrem Land oder Ihrer Region eine Liste relevanter Apps

## <a name="recommended-apps"></a>Empfohlene Apps

Microsoft Partner und Wiederverkäufer können eine App erstellen, mit der sie Listen von Apps zusammenstellen können, die sie ihren Kunden häufig empfehlen. Wenn sie dies tun und die App für Ihren Mandanten bereitstellen, sind die Apps auf der Seite **Empfohlene Apps** verfügbar. Dort können Sie sich über jede App informieren und entscheiden, ob Sie sie installieren möchten.

> [!NOTE]
> Wenn Sie ein Microsoft-Partner oder -Wiederverkäufer sind und eine Liste empfohlener Apps bereitstellen möchten, lesen Sie [Empfohlene Apps von AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) im Verwaltungsinhalt.

## <a name="see-also"></a>Siehe auch

[Apps installieren und deinstallieren](ui-extensions-install-uninstall.md)  
[Business Central anpassen](ui-customizing-overview.md)  
[Business Central-Apps von anderen Anbietern](ui-extensions-other.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[Aktivieren von Debitoren-Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Einrichten der britischen Postleitzahlerweiterung GetAddress.io](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Apps für andere Anbieter](ui-extensions-other.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
