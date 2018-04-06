---
title: Problembehandlung Integration mit Microsoft Flow| Microsoft Docs
description: "Problemlösung beim Bereitstellen von Financials als Datenquelle und beim Definieren einer OData-URL für Ihre Webdienste, um eine Geschäfts-App mithilfe einem automatisierten Workflow zu erstellen."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 60ce05760251da39280eb8a4884cb80586c2ab62
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Problembehandlung bei der Integration mit Microsoft Flow - angeforderte URL zu lang
Sie können die Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)] als Teil eines Workflows in Microsoft Flow verwenden.  

> [!NOTE]  
>   Sie müssen ein gültiges Konto mit [!INCLUDE[d365fin](includes/d365fin_md.md)] und Flow haben.  

Wenn Sie einen Microsoft Flow mithilfe des [!INCLUDE[d365fin](includes/d365fin_md.md)] Connectors erstellen, erhalten Sie möglicherweise eine Fehlermeldung, dass die angeforderte URL zu lang ist, nachdem der Flow erstellt wurde, wie beispielsweise **RequestUriTooLong**.

## <a name="cause"></a>Grund
Um einen Flow auszulösen, sucht er Änderungen in Ihren Daten. Bei der Festlegung, ob sich Ihre Daten verändert haben, vergleichen die Connectors die zwischengespeicherten Daten mit den neuen Daten, die von der Quelle angefordert werden.  

Wenn die Datenenanforderung eine URL erstellt, die zu lang, schlägt sie fehl. Gemeinsame Ursachen können sein:
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
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](upload-data.md)  
[Benutzer und ihre Berechtigungen verwalten.](ui-how-users-permissions.md)    
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzen](finance.md)  

