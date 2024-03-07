---
title: Anzeigen und Bearbeiten in Excel von Business Central aus (enthält ein Video)
description: 'Mehr erfahren, wie Sie die Finanzaufstellungen in Microsoft Excel von  Business Central für eine Analyse der Daten öffnen können.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Anzeigen und Arbeit in Excel aus Business Central

Bei Seiten, die eine Liste von Datensätzen in Zeilen und Spalten anzeigen, wie z.B. eine Liste von Kunden, Verkaufsaufträgen oder Rechnungen, können Sie die Liste nach Microsoft Excel exportieren und dort anzeigen lassen. Je nach Seite haben Sie zwei Optionen für die Anzeige in Excel. Beide Optionen sind über das Symbol **Freigeben** verfügbar. ![Eine Seite in einer anderen App freigeben.](media/share-icon.png) am oberen Rand einer Seite. Sie können entweder die **In Excel öffnen** Aktion oder die **Bearbeiten Sie in Excel** Aktion dieser Seite auswählen. Dieser Artikel erklärt die beiden Aktionen.

## In Excel öffnen

Mit der Aktion **Öffnen in Excel** können Sie Änderungen an den Datensätzen in Excel vornehmen, aber Sie können die Änderungen nicht zurück auf [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen. Sie können die Änderungen nur in einer Excel-Datei speichern, ohne die Daten in [!INCLUDE[prod_short](includes/prod_short.md)] zu verändern.

- Mit dieser Aktion respektiert Excel alle Filter auf der Seite, die die angezeigten Datensätze einschränken. Das Excel-Arbeitsblatt enthält die gleichen Zeilen und Spalten, die auf der Seite in [!INCLUDE[prod_short](includes/prod_short.md)] erscheinen.

- Diese Aktion geht auf Windows und Mac Os.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

> [!IMPORTANT]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] lokal ist die Aktion **In Excel öffnen** standardmäßig verfügbar. Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] lokal für die Bearbeitung von Daten in Excel einrichten, wird die Aktion **In Excel öffnen** durch die Aktion **In Excel bearbeiten** ersetzt.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> In Excel haben ganze Zahlen in Spalten am Ende ein Dezimalzeichen (wie einen Punkt `.` oder ein Komma `,`), obwohl das Dezimalzeichen in Business Central nicht angezeigt wird. Das Dezimalzeichen hängt von den Regionseinstellungen Ihres Geräts ab. Beispielsweise könnte `10` in Business Central als `10.` oder `10,` in Excel erscheinen. Sie können das Format in Excel ändern, indem Sie die Werte auswählen und dann <kbd>Strg</kbd>+<kbd>1</kbd> auswählen. Weitere Informationen zum Ändern des Zahlenformats in Excel finden Sie unter [Zahlen formatieren](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).


## In Excel bearbeiten

Die Aktion **In Excel bearbeiten** ist für die meisten Listen verfügbar, aber nicht für alle. Mit der Aktion **Bearbeiten in Excel** nehmen Sie Änderungen an Datensätzen in Excel vor und veröffentlichen die Änderungen dann wieder in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn Excel geöffnet wird, sehen Sie den Bereich **Excel Add-in** auf der rechten Seite.

- Mit dieser Aktion berücksichtigt Excel die meisten Filter auf der Seite, die die angezeigten Datensätze einschränken, sodass das Excel-Arbeitsblatt fast dieselben Datensätze und Spalten enthält.

- Um die neuesten Daten von [!INCLUDE[prod_short](includes/prod_short.md)] abzurufen, wählen Sie **Aktualisieren** im Excel Add-in Fensterbereich.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### Erstmalige Anmeldung

Die Aktion **In Excel bearbeiten** setzt voraus, dass das Business Central-Add-in in Excel installiert ist. In manchen Fällen hat Ihr Administrator festgelegt, dass das Add-in automatisch für Sie installiert wird. In diesem Fall müssen Sie sich nur bei Business Central im Bereich **Excel Add-in** mit Ihrem Benutzernamen und Kennwort anmelden. Andernfalls öffnet sich der Bereich **Neues Office Add-in**. Um das Add-in zu installieren, wählen Sie **Diesem Add-in vertrauen**, wodurch das Add-in direkt aus dem Office Store installiert wird.

Wenn sich das Add-in nicht installieren lässt, wenden Sie sich entweder an Ihren Admin oder versuchen Sie, es manuell zu installieren. Weitere Informationen finden Sie unter [Das Add-In manuell für den eigenen Gebrauch installieren](admin-deploy-excel-addin.md#install).

### Arbeiten Sie über Umgebungen und Firmen hinweg

Sie können die Firma wechseln, mit der Sie gerade arbeiten. Um die Firma zu wechseln, wählen Sie das Symbol **Optionen** ![Excel-Add-In-Optionen](media/cogwheel.png "Excel-Add-In-Optionen") im Excel-Add-in-Fenster und wählen Sie dann die Firma aus dem Feld **Firma**.  

> [!IMPORTANT]
> Wenn Sie das Unternehmen ändern, stellen Sie sicher, dass das Feld **Umgebung** nicht leer ist. Wenn dies der Fall ist, dann stellen Sie sie auf eine der verfügbaren Optionen ein; andernfalls wird das Add-In nicht korrekt funktionieren.  

Wenn Sie Änderungen am Add-In vornehmen, müssen Sie es neu laden, um die Verbindung zu aktualisieren. Verwenden Sie zum Neuladen das ![Excel-Add-In-Menü](media/excel-addin-menu.png "Excel-Add-In-Menü") in der oberen rechten Ecke des Add-Ins. Wenn Sie das Add-in nicht laden können, wenden Sie sich an Ihren Administrator. Wenn Sie der Administrator sind, lesen Sie [Holen Sie das Business Central-Add-in für Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Das Add-in funktioniert mit Excel für das Web (online) von jedem Gerät aus, solange Sie einen unterstützten Browser verwenden. Es funktioniert auch mit der Excel App für Windows (PC), aber nicht für macOS.
>
> Für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort ist die Aktion **In Excel bearbeiten** nur verfügbar, wenn das Excel-Add-In von Ihrem Administrator konfiguriert wurde, und nur für den Web-Client verfügbar. Wenn Sie als Administrator erfahren möchten, wie Sie das Excel-Add-In installieren, lesen Sie [Einrichtung des Excel-Add-Ins zur Bearbeitung von Business Central Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### Beschränkungen bei der Verwendung von Excel für das Web 

Wenn **Bearbeiten in Excel** auf Listenseiten für Tabellen mit vielen Spalten verwendet wird, kann die resultierende Arbeitsmappe zu viele Spalten haben, als dass die Datei in Excel für das Web angezeigt werden könnte. [!INCLUDE[prod_short](includes/prod_short.md)] begrenzt die exportierte Arbeitsmappe automatisch auf 100 Spalten, wenn OneDrive für die Systemfunktionen konfiguriert ist. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## Siehe auch

[Analysieren von Finanzberichten in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Business Central](ui-work-product.md)  
[Verbesserungen der Excel-Integration in der Veröffentlichungswelle 2 von 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
