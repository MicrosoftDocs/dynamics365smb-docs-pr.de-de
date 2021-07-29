---
title: Anzeigen und Arbeit in Excel aus Business Central
description: Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 6bf12f55f6bce843c4ed12f2a40db542367fffde
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443476"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Anzeigen und Arbeit in Excel aus Business Central

Mit Seiten, die eine Liste der Datensätze in den Zeilen und Spalten anzeigen, wie eine Liste von Debitoren von Verkaufsaufträgen oder Rechnungen können Sie die Daten mithilfe von Microsoft Excel anzeigen. Je nach Seite haben Sie zwei Optionen für die Anzeige in Excel. Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen. Dieser Artikel erklärt die Unterschiede zwischen den beiden Aktionen.

## <a name="open-in-excel"></a>In Excel öffnen

Mit der Aktion **Öffnen in Excel** können Sie Änderungen an den Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht zurück auf [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen. Sie können die Änderungen in die Excel-Datei nur auf dem Computer speichern.

- Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken. Das Excel-Arbeitsblatt enthält die gleichen Zeilen und Spalten, die auf der Seite in [!INCLUDE[prod_short](includes/prod_short.md)] erscheinen.

- Diese Aktion geht auf Windows und Mac Os.

- Ab Update 18.3 können Sie auch Listen anzeigen, die in Seitenteilen dargestellt werden, wie die Zeilen in einem Verkaufsauftrag. Im Moment ist diese Funktion eine optionale Funktionalität, die erfordert, dass Sie **Beliebigen Listenteil nach Excel exportieren** in **Funktionsverwaltung** aktivieren. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management). 

> [!NOTE]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] lokal ist die Aktion **In Excel öffnen** standardmäßig verfügbar. Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>In Excel bearbeiten

Mit der Aktion **Bearbeiten in Excel** nehmen Sie Änderungen an Datensätzen in Excel vor und veröffentlichen die Änderungen dann wieder in [!INCLUDE[prod_short](includes/prod_short.md)].

- Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken, sodass das Excel-Arbeitsblatt fast dieselben Datensätze und Spalten enthält.

- Das geht nur auf Windows; nicht Mac Os.

- Sie können das Unternehmen, mit dem Sie zusammenarbeiten, wechseln. Um die Firma zu wechseln, wählen Sie das Symbol **Optionen** ![Excel-Add-In-Optionen](media/cogwheel.png "Excel-Add-In-Optionen") im Excel-Add-in-Fenster und wählen Sie dann die Firma aus dem Feld **Firma**.  

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