---
title: Problembehandlungsintegration in Microsoft Flow| Microsoft Docs
description: Problemlösung beim Bereitstellen von Business Central als Datenquelle und eine OData-URL Ihrer Webdienste festlegen, um eine Geschäfts-App mithilfe einem automatisierten Workflow zu erstellen.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 8a43df89261867f80ba16782cde92b040ce180c8
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240234"
---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Problembehandlungsintegration in Microsoft Flow – angeforderte URL zu lang
Sie können Ihre [!INCLUDE[d365fin](includes/d365fin_md.md)]-Daten als Teil eines Workflows in Microsoft Flow verwenden.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.  

Wenn Sie einen Microsoft Flow mithilfe des [!INCLUDE[d365fin](includes/d365fin_md.md)]-Connectors erstellen, erhalten Sie möglicherweise eine Fehlermeldung, dass die angeforderte URL zu lang ist, nachdem der Flow erstellt wurde, wie beispielsweise **RequestUriTooLong**.

## <a name="cause"></a>Grund
Um einen Flow auszulösen, sucht er Änderungen in Ihren Daten. Bei der Festlegung, ob sich Ihre Daten verändert haben, vergleichen die Connectors die zwischengespeicherten Daten mit den neuen Daten, die von der Quelle angefordert werden.  

Wenn die Datenanforderung eine URL erstellt, die zu lang, schlägt sie fehl. Gemeinsame Ursachen können sein:
- Grundsätzlich jede Quelltabelle mit über 250 Zeilen
- Quelltabellen, die mehrere Tausend Datensätze enthalten

## <a name="workaround"></a>Problemumgehung
Folgen Sie diesen Schritten als Problemumgehung.
1. Bearbeiten Sie den Flow, der fehlschlägt.
2. Erweitern Sie **Zeigen Sie erweiterte Optionen an** im Flowauslöser.
3. Geben Sie im Feld **Zählung überspringen** die Anzahl Datensätze ein, die übersprungen werden sollen.  
Wenn die Tabelle beispielsweise, die Sie als Datenquelle verwenden, 4.000 Datensätze hat, geben Sie 4.000 als die Anzahl der Datensätze ein, die übersprungen werden sollen.
4. Aktualisieren Sie den Flow.

> [!NOTE]  
> Der Connector ist derzeit in Beta-Vesion. Aktualisierungen, wie Datenänderungen behandelt werden, sind für eine spätere Freigabe geplant.


## <a name="see-also"></a>Siehe auch
[Nutzung von [!INCLUDE[d365fin](includes/d365fin_md.md)] in einem automatisierten Workflow](across-how-use-financials-data-source-flow.md)  
[Erste Schritte](product-get-started.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)    
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  
