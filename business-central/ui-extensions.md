---
title: Erweiterungen installieren um Business Central anzupassen | Microsoft Docs
description: Informationen zum Hinzufügen von Funktionalität und Anpassungen für Business Central durch die Installation von Erweiterungen.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765921"
---
# <a name="customizing-business-central-using-extensions"></a>Anpassen von Business Central mithilfe der Erweiterungen

Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] ändern, indem Sie beispielsweise Erweiterungen installieren, die Funktionalität hinzufügen, das Verhalten ändern oder Zugriff auf die neuen Onlinediensten geben.

> [!NOTE]
> Um Erweiterungen von AppSource zu installieren oder Erweiterungen pro Mandanten hinzuzufügen, müssen Sie über die richtigen Berechtigungen verfügen. Sie müssen entweder Mitglied der Benutzergruppe D365 EXTENSION MGMT sein oder über den Berechtigungssatz D365 EXTENSION MGMT verfügen. Als Administrator können Sie anderen Benutzern in Ihrem Unternehmen Benutzergruppen und Berechtigungen zuweisen.<br /><br />
Um die Funktionen einer Erweiterung nutzen zu können, z. B. Seiten öffnen, Berichte ausführen, Aktionen auswählen usw., müssen Sie den Berechtigungssätzen zugewiesen sein, die als Teil der Erweiterung installiert werden.

> [!IMPORTANT]  
> Das Hochladen von Tenant-Erweiterungen und die Installation von AppSource-Erweiterungen werden über die Seite **Erweiterungsverwaltung** für lokale Installationen nicht unterstützt.

Wenn Sie das [!INCLUDE[d365fin](includes/d365fin_md.md)] zuerst starten, werden bestimmte Erweiterungen bereits eingerichtet. Im Zeitverlauf werden mehr Erweiterungen für Sie zugänglich und Sie können auswählen, ob Sie die Erweiterung verwenden möchten oder nicht.

Beispielsweise bietet Microsoft eine Erweiterung an, die die Integration mit PayPal Payments Standard ermöglicht. Diese Erweiterung wird standardmäßig eingerichtet.
Wenn aber keine andere Erweiterung bereitgestellt wird, die die Integration mit einem anderen Zahlungsservice anbietet, können Sie die neue Erweiterung einrichten und dann auswählen, welcher der beiden Services verwendet werden soll.  

Sie verwalten die Erweiterung auf der **Erweiterungs-Verwaltungs**-Seite. Sie können vom Startbildschirm auf diese Seite zugreifen. Wählen Sie alternativ das Symbol **Nach Seite oder Bericht suchen** aus ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") in der oberen rechter Ecke, geben Sie **Erweiterung** ein, und wählen Sie dann den zugehörigen Link aus. Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Erweiterungen](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Wenn Sie der Meinung sind, Sie sollten Zugriff zu einer Erweiterung haben, können die Funktionalität aber nicht finden, überprüfen Sie die Seite **Erweiterungsverwaltung**, wenn die Erweiterung dort nicht aufgeführt wird, können Sie sie einrichten, wie im folgenden Abschnitt erläutert.  

> [!NOTE]  
> Neue Erweiterungen sind nicht direkt in AppSource verfügbar, nachdem ein Update angekündigt wurde. Halten Sie unter [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) Ausschau nach den Erweiterungen.

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
