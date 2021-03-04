---
title: Anzeigen und Arbeit in Excel aus Business Central
description: Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/06/2020
ms.author: jswymer
ms.openlocfilehash: cb172cd1d3285128e871fedb44ccd70fb84a669a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754167"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Anzeigen und Arbeit in Excel aus Business Central

Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen. Dazu haben Sie zwei Optionen. Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen. Der Unterschied zwischen den beiden Methoden ist wie folgt::  

## <a name="open-in-excel"></a>In Excel öffnen

- Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken. Das Excel-Arbeitsmappe enthält die gleichen Zeilen und Spalten, die auf der Seite in [!INCLUDE[prod_short](includes/prod_short.md)] erscheinen.

- Sie können Änderungen mit Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht auf  [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen. Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern.

- Diese Aktion geht auf Windows und Mac Os.

> [!NOTE]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] lokal ist die Aktion **In Excel öffnen** standardmäßig verfügbar. Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.

## <a name="edit-in-excel"></a>In Excel bearbeiten

- Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken, sodass die Excel-Arbeitsmappe fast dieselben Datensätze und Spalten enthält.

- Der Vorteil der **Bearbeiten Sie in Excel** Aktion ist, dass es Sie Änderungen mit Datensätzen in Excel vornimmt und die Änderungen zurück in [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen können,

- Das geht nur auf Windows; nicht Mac Os.

- Sie können das Unternehmen, mit dem Sie zusammenarbeiten, wechseln. Um das Unternehmen zu wechseln, wählen Sie dazu im Excel-Add-In-Fensterbereich das Symbol **Optionen** ![Excel-Add-In-Optionen](media/cogwheel.png "Excel-Add-In-Optionen") und wählen Sie dann das Unternehmen aus dem Feld **Unternehmen**.  

    > [!IMPORTANT]
    > Wenn Sie das Unternehmen ändern, stellen Sie sicher, dass das Feld **Umgebung** nicht leer ist. Wenn dies der Fall ist, dann stellen Sie sie auf eine der verfügbaren Optionen ein; andernfalls wird das Add-In nicht korrekt funktionieren.  

Wenn Sie Änderungen am Add-In vornehmen, müssen Sie es neu laden, um die Verbindung zu aktualisieren. Verwenden Sie zum Neuladen das ![Excel-Add-In-Menü](media/excel-addin-menu.png "Excel-Add-In-Menü") in der oberen rechten Ecke des Add-Ins. Wenn Sie das Add-In nicht laden können, wenden Sie sich an Ihren Administrator. Wenn Sie der Administrator sind, lesen Sie [Einrichten des Excel-Add-Ins zum Bearbeiten von Business Central-Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort ist die Aktion **In Excel bearbeiten** nur verfügbar, wenn das Excel-Add-In von Ihrem Administrator konfiguriert wurde, und nur für den Web-Client verfügbar. Wenn Sie als Administrator erfahren möchten, wie Sie das Excel-Add-In installieren, lesen Sie [Einrichtung des Excel-Add-Ins zur Bearbeitung von Business Central Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="see-the-differences-between-the-options"></a>Sehen Sie sich die Unterschiede zwischen den Optionen an
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Finanzauswertungen analysieren in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Business Central](ui-work-product.md)  
[Verbesserungen der Excel-Integration in der Veröffentlichungswelle 2 von 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]