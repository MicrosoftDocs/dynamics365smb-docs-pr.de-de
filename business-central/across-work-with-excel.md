---
title: Anzeigen und Bearbeiten in Excel von Business Central aus (enthält ein Video)
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
ms.openlocfilehash: 7800eb9d9852e8cc13eed26ce3e42fa318f7e185
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940251"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Anzeigen und Arbeit in Excel aus Business Central

Bei Seiten, die eine Liste von Datensätzen in Zeilen und Spalten anzeigen, wie z.B. eine Liste von Kunden, Verkaufsaufträgen oder Rechnungen, können Sie die Liste nach Microsoft Excel exportieren und dort anzeigen lassen. Je nach Seite haben Sie zwei Optionen für die Anzeige in Excel. Beide Optionen sind über das Symbol **Freigeben** verfügbar. ![Eine Seite in einer anderen App freigeben.](media/share-icon.png) am oberen Rand einer Seite. Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen. Dieser Artikel erklärt die Unterschiede zwischen den beiden Aktionen.

## <a name="open-in-excel"></a>In Excel öffnen

Mit der Aktion **Öffnen in Excel** können Sie Änderungen an den Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht zurück auf [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen. Sie können die Änderungen nur in einer Excel-Datei speichern, ohne die Daten in [!INCLUDE[prod_short](includes/prod_short.md)] zu verändern.

- Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken. Das Excel-Arbeitsblatt enthält die gleichen Zeilen und Spalten, die auf der Seite in [!INCLUDE[prod_short](includes/prod_short.md)] erscheinen.

- Diese Aktion geht auf Windows und Mac Os.

- Ab Update 18.3 können Sie auch Listen anzeigen, die in Seitenteilen dargestellt werden, wie die Zeilen in einem Verkaufsauftrag. 

> [!NOTE]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] lokal ist die Aktion **In Excel öffnen** standardmäßig verfügbar. Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]  

## <a name="edit-in-excel"></a>In Excel bearbeiten

Die Aktion **In Excel bearbeiten** ist für die meisten Listen verfügbar, aber nicht für alle. Mit der Aktion **Bearbeiten in Excel** nehmen Sie Änderungen an Datensätzen in Excel vor und veröffentlichen die Änderungen dann wieder in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Excel geöffnet wird, sehen Sie den Bereich **Excel Add-in** auf der rechten Seite.

- Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken, sodass das Excel-Arbeitsblatt fast dieselben Datensätze und Spalten enthält.

- Um die neuesten Daten von [!INCLUDE[prod_short](includes/prod_short.md)] zu erhalten, wählen Sie **Aktualisieren** im Excel-Add-in-Fenster.

- Sie können die Firma wechseln, mit der Sie gerade arbeiten. Um die Firma zu wechseln, wählen Sie das Symbol **Optionen** ![Excel-Add-In-Optionen](media/cogwheel.png "Excel-Add-In-Optionen") im Excel-Add-in-Fenster und wählen Sie dann die Firma aus dem Feld **Firma**.  

    > [!IMPORTANT]
    > Wenn Sie das Unternehmen ändern, stellen Sie sicher, dass das Feld **Umgebung** nicht leer ist. Wenn dies der Fall ist, dann stellen Sie sie auf eine der verfügbaren Optionen ein; andernfalls wird das Add-In nicht korrekt funktionieren.  

Wenn Sie Änderungen am Add-In vornehmen, müssen Sie es neu laden, um die Verbindung zu aktualisieren. Verwenden Sie zum Neuladen das ![Excel-Add-In-Menü](media/excel-addin-menu.png "Excel-Add-In-Menü") in der oberen rechten Ecke des Add-Ins. Wenn Sie das Add-in nicht laden können, wenden Sie sich an Ihren Administrator. Wenn Sie der Administrator sind, lesen Sie [Holen Sie das Business Central-Add-in für Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Das Add-in funktioniert mit Excel für das Web (online) von jedem Gerät aus, solange Sie einen unterstützten Browser verwenden. Es funktioniert auch mit der Excel App für Windows (PC), aber nicht für macOS.
>
> Für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort ist die Aktion **In Excel bearbeiten** nur verfügbar, wenn das Excel-Add-In von Ihrem Administrator konfiguriert wurde, und nur für den Web-Client verfügbar. Wenn Sie als Administrator erfahren möchten, wie Sie das Excel-Add-In installieren, lesen Sie [Einrichtung des Excel-Add-Ins zur Bearbeitung von Business Central Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### <a name="first-time-sign-in"></a>Erstmalige Anmeldung

Die Aktion **In Excel bearbeiten** setzt voraus, dass das Business Central-Add-in in Excel installiert ist. In manchen Fällen hat Ihr Administrator festgelegt, dass das Add-in automatisch für Sie installiert wird. In diesem Fall müssen Sie sich nur bei Business Central im Bereich **Excel Add-in** mit Ihrem Benutzernamen und Kennwort anmelden. Andernfalls öffnet sich der Bereich **Neues Office Add-in**. Um das Add-in zu installieren, wählen Sie **Diesem Add-in vertrauen**, wodurch das Add-in direkt aus dem Office Store installiert wird.

Wenn sich das Add-In aus irgendeinem Grund nicht installieren lässt, wenden Sie sich an Ihren Admin oder versuchen Sie, es manuell zu installieren. Weitere Informationen finden Sie unter [Das Add-In manuell für den eigenen Gebrauch installieren](admin-deploy-excel-addin.md#install).

## <a name="see-the-differences-between-the-options"></a>Sehen Sie sich die Unterschiede zwischen den Optionen an
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Finanzauswertungen analysieren in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Business Central](ui-work-product.md)  
[Verbesserungen der Excel-Integration in der Veröffentlichungswelle 2 von 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]