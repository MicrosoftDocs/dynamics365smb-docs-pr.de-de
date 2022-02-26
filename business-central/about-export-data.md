---
title: Business Central-Daten nach Excel exportieren
description: Sie können Ihre Finanzberichte und Intelligence-Daten von Business Central in Excel exportieren, oder Ihre Financials Daten in Excel öffnen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.search.form: 9901
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 078b3988feb2d6e11d0601ca5aae48cdc5e6f893
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012006"
---
# <a name="exporting-your-business-data-to-excel"></a>Exportieren Ihrer Geschäftsdaten nach Excel
Wenn Sie mit Ihren Daten von [!INCLUDE[prod_short](includes/prod_short.md)] in Excel arbeiten, können Sie alle Listen in Excel öffnen und dort damit arbeiten. Möchten Sie das Abonnement für [!INCLUDE[prod_short](includes/prod_short.md)] stornieren, können Sie die Daten in Excel exportieren, sodass Sie diese nicht verlieren.

## <a name="opening-lists-in-excel"></a>Öffnen von Listen in Excel
Sie können Daten aus jeder Liste, jedem Arbeitsblatt oder jedem Eintrag in Excel öffnen. Sie öffnen einfach die Seite, die Sie anzeigen möchten, und wählen dann **In Excel öffnen**. Beispielsweise öffnen Sie die Liste der Debitoren (nach **Debitoren** suchen) und wählen Sie dann **In Excel öffnen** aus. Ihr Browser fordert Sie auf, das generierte Excel-Arbeitsblatt zu öffnen oder zu speichern.  

> [!NOTE]
> Verwenden Sie diese Option, wenn Sie keine Änderungen vornehmen und die Änderungen zurück auf [!INCLUDE[prod_short](includes/prod_short.md)] veröffentlichen möchten.  

Jede Liste enthält mehrere Spalten und der Export in Excel enthält sämtliche Spalten, die in Ihrer aktuellen Ansicht enthalten sind. Wenn Sie Spalten hinzufügen oder entfernen möchten, bevor Sie die Liste in Excel öffnen, öffnen Sie das Shortcutmenü für jede mögliche Spalte und geben dann die Spalten an, die angezeigt werden sollen. Diese Liste der Spalten ist für die meisten Listen anders und sie zeigt die Struktur der Datenbank, in der Ihre Daten gespeichert sind. Wenn Sie nicht sicher sind, welche Art der Daten eine bestimmte Spalte enthält, können Sie diese zur Ansicht hinzuzufügen und anschließend entscheiden, ob Sie diese wieder entfernen möchten.  

### <a name="edit-data-in-excel"></a>Daten in Excel bearbeiten
Ihre [!INCLUDE[prod_short](includes/prod_short.md)] Benutzeroberfläche wird das Add-In für Excel integrieren, sodass Sie Daten in Excel bearbeiten können. Weitere Informationen finden Sie unter [Finanzauswertungen analysieren Microsoft Excel](finance-analyze-excel.md).  

## <a name="exporting-data-to-other-finance-systems"></a>Daten in andere Finanzsysteme exportieren
Wenn Sie Ihre Abonnement für [!INCLUDE[prod_short](includes/prod_short.md)] stornieren möchten, können Sie die Daten in Excel exportieren, damit Sie in Ihrem nächsten Finanzsystem bereitstehen.  

Sie können alle Seiten exportieren, aber möglicherweise benötigen Sie nicht alles. Ziehen Sie in Betracht, nur die wesentlichen Seiten zu exportieren, und denken Sie daran, alle Spalten hinzuzufügen, wie zuvor beschrieben:  

* Kontenplan  
* Debitoren  
* Kreditoren  
* Banken  
* Artikel  

Wenn Sie alle Ihre finanzielle Transaktionen verfügbar haben möchten, sind dies sehr viele Daten. Der Export kann deshalb mehrere Minuten dauern. Die Finanztransaktionen werden auf der Seite **Sachposten** angezeigt.  

Es ist empfehlenswert, dass Sie auch erwägen, Daten von den nächsten Seiten zu exportieren:  

* Debitorenposten  
* Kreditorenposten  
* Bankposten  
* Artikelposten  
* Buchungsmatrix Einrichtung  
* Debitorenbuchungsgruppen  
* Kreditorenbuchungsgruppen  
* Artikelbuchungsgruppen  
* Bankbuchungsgruppe  
* Sachkontenbudgets  
* Finanzbudgetposten  
* Verkaufsangebote  
* Verkaufsrechnungen  
* Einkaufsrechnungen  
* Kontakte  
* Verkäufer  

> [!NOTE]  
> Wenn Sie mehr als einen Mandanten in [!INCLUDE[prod_short](includes/prod_short.md)] erfasst haben, müssen Sie die entsprechenden Daten der einzelnen Unternehmen exportieren.

> [!NOTE]
> Sie müssen über mindestens eine der folgenden Berechtigungen verfügen, um Daten in Excel zu öffnen oder zu bearbeiten:
>    - Berechtigungssatz *D365 Excel-Exportaktion*  
>    - Systemberechtigung 6110 *Aktionsexport nach Excel zulassen*.  

Weitere Informationen finden Sie unter [So erhalten Sie eine Übersicht der Benutzerberechtigungen](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Abbrechen des Abonnements für [!INCLUDE[prod_short](includes/prod_short.md)]](admin-cancel.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Finanzauswertungen analysieren in Microsoft Excel](finance-analyze-excel.md)  
[Finanzen](finance.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]