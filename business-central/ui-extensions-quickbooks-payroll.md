---
title: Nutzung der Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung| Microsoft Docs
description: Beschreibt, wie die Erweiterung verwendet wird, um Gehalts- und Lohntransaktionen aus dem Quickbooks-Gehaltsabrechnungsdienst zu importieren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 01/09/2019
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 79729b42b660399893aebe1116c80ef3b3209042
ms.openlocfilehash: ac68f8a4d67224ad55b1c34ff9b2e4ffa2c372aa
ms.contentlocale: de-de
ms.lasthandoff: 01/15/2019

---
# <a name="the-quickbooks-payroll-file-import-extension"></a>Die Quickbooks-Gehaltsabrechnungsdatei-Importerweiterung
Verwenden Sie die QuickBooks-Gehaltsabrechnungsdatei-Importerweiterung, um Gehaltsabrechnungstransaktionen von QuickBooks mit den Sachkonten in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu importieren. Dies ist beispielsweise dann nützlich, wenn Sie von QuickBooks zu [!INCLUDE[d365fin](includes/d365fin_md.md)] wechseln oder, dass Sie Löhne auslagern aber diese in [!INCLUDE[d365fin](includes/d365fin_md.md)] nachverfolgen möchten.

## <a name="steps-to-import-payroll-data"></a>So importieren Sie Lohndaten
Der erste Schritt für Sie oder IHren Buchhalter ist es, die Exportfunktionen in QuickBook zu verwenden, um die Lohndaten in eine .IIF Datei zu exportieren. Der zweite Schritt ist es, die **Fibu Buch.-Blätter** in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu öffnen und die **Lohntransaktionen importieren** Aktion zu verwenden, um die Datei zu importieren. Während des Importvorgangs ordnen Sie Sachkonten aus QuickBooks auf den entsprechenden Konten in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zuletzt buchen Sie die Gehaltsabrechnungstransaktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]mentsprechend der Kontozuordnung. 

Weitere Informationen finden Sie unter [Gehaltsabrechnungstransaktionen importieren](finance-how-import-payroll-transactions.md).

## <a name="see-also"></a>Siehe auch
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)    
[Finanzen](finance.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

