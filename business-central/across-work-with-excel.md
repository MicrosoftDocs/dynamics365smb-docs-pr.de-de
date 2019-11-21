---
title: Anzeigen und Arbeit in Excel aus Business Central | Microsoft Docs
description: Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/24/2019
ms.author: jswymer
ms.openlocfilehash: 71b4e5b7124f929255f1374b38cfbe28c9f12d2b
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692800"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Anzeigen und Arbeit in Excel aus Business Central

Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen. Dazu haben Sie zwei Optionen. Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen. Der Unterschied zwischen den beiden Methoden ist der folgende:  

## <a name="open-in-excel"></a>In Excel öffnen

- Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken. Das bedeutet, dass die Excel-Arbeitsmappe die gleichen Zeilen und Spalten enthält, die auf der Seite in [!INCLUDE[prodshort](includes/prodshort.md)] erscheinen.

- Sie können Änderungen mit Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht auf  [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen. Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern. 

- Diese Aktion geht auf Windows und Mac Os. 

> [!NOTE]
> Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die Aktion **In Excel öffnen** standardmäßig verfügbar. Wenn Sie jedoch [!INCLUDE [prodshort](includes/prodshort.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.

## <a name="edit-in-excel"></a>In Excel bearbeiten

- Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken. Das bedeutet, dass die Excel-Arbeitsmappe fast die gleichen Datensätze und Spalten enthält.

- Der Vorteil der **Bearbeiten Sie in Excel** Aktion ist, dass es Sie Änderungen mit Datensätzen in Excel vornimmt und die Änderungen zurück in [!INCLUDE[prodshort](includes/prodshort.md)] veröffentlichen können,

- Das geht nur auf Windows; nicht Mac Os.

Diese wurde 2019 in der Release-Welle 2 erweitert. Weitere Informationen finden Sie unter [Erweiterungen der Excel-Integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> Für [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist die Aktion **In Excel bearbeiten** nur verfügbar, wenn das Excel-Add-In von Ihrem Administrator konfiguriert wurde. Wenn Sie als Administrator erfahren möchten, wie Sie das Excel-Add-In installieren, lesen Sie [Einrichtung des Excel-Add-Ins zur Bearbeitung von Business Central Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Bei [!INCLUDE[prodshort](includes/prodshort.md)] lokal ist diese Funktion nur für den Web-Client verfügbar.

### <a name="see-the-differences-between-the-options"></a>Sehen Sie sich die Unterschiede zwischen den Optionen an 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a>Siehe auch
[Arbeiten mit  Business Central](ui-work-product.md)  
