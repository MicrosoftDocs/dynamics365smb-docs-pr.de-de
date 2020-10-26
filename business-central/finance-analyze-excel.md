---
title: Arbeiten mit Finanzübersichten in Excel
description: Mehr erfahren, wie Sie die Finanzauswertungen in Microsoft Excel von Business Central für eine bessere Analyse öffnen können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 53221cbacb35e7e82077295a6f7098f07c2b02e6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913471"
---
# <a name="analyzing-financial-statements-in-microsoft-excel"></a>Analysieren von Finanzauswertungen in Microsoft Excel

In [!INCLUDE [prodshort](includes/prodshort.md)], können Sie KPIs sehen und Übersichten über die Finanzlage des Unternehmens anzeigen. Sie können ebenfalls Listen in Excel öffnen und die Daten dort analysieren. Sie können jedoch umfangreiche Finanzauswertungen wie die Bilanz oder der GuV in Excel exportieren, die Daten analysieren und Änderungen wieder importieren .  

Im Geschäftsführer und im Buchhalter Rollencenter können Sie aus einem Dropdownmenü im Kapitel "Listen" im Menüband auswählen, welche Finanzberichte Sie in Excel anzeigen möchten. Wenn Sie den anzuzeigenden Kontoauszug auswählen, wird er in Excel oder in Excel online geöffnet. Ein Add-In verbindet die Daten mit [!INCLUDE [prodshort](includes/prodshort.md)]. Sie müssen sich möglicherweise mit demselben Konto anmelden, das Sie mit [!INCLUDE [prodshort](includes/prodshort.md)] verwenden.  

## <a name="getting-the-overview-and-the-details-in-excel"></a>Abrufen der Übersicht und Details in Excel

Im Menüband wählen Sie den entsprechenden Excel-Bericht aus und lassen ihn öffnen, damit Sie die gesuchte Information sehen. In dieser Version von [!INCLUDE [prodshort](includes/prodshort.md)], bieten wir die folgenden Excel-Berichte an:

- Kontenplan  
- GuV  
- Cashflowauszug  
- Auszug nicht ausgeschüttete Gewinne  
- Kreditor-Saldenrückblick  
- Debitor-Saldenrückblick  

Nehmen wir mal an, Sie möchten den Cashflow vertiefter ansehen. Vom Geschäftsleiter- oder dem Buchhalter-Rollencenter aus können Sie den Bericht **Cashflowauszug** in Excel öffnen, tatsächlich exportieren wir aber die relevanten Daten für Sie und erstellen eine Excel-Arbeitsmappe auf Grundlage einer vordefinierte Vorlage. Abhängig von Ihrem Browser werden Sie aufgefordert, möglicherweise die Arbeitsmappe zu öffnen oder zu speichern.  

Dort finden Sie eine Registerkarte, in der die Daten für Sie im ersten Fenster ausgebreitet werden. Alle Daten, die exportiert wurden, sind ebenfalls in anderen Arbeitsblättern vorhanden, wenn Sie sie benötigen. Sie können den Bericht sofort drucken, oder Sie können das Feld ändern, solange Sie die Übersicht und die Details haben, die Sie anzeigen möchten. Verwenden Sie das [!INCLUDE [prodshort](includes/prodshort.md)] Excel-Add-In, um Daten zu filtern und zu analysieren.  

### <a name="understanding-the-excel-templates"></a>Grundlegendes zu den Excel-Vorlagen

Die vordefinierten Excel-Berichte basieren auf den Daten im aktuellen Unternehmen. Zum Beispiel hat das Demounternehmen den Kontenplan eingerichtet, um drei Barkonten unter *Umlaufvermögen* aufzulisten: 10100 **Girokonto** , 10200 **Sparkonto** und 10300 **Portokasse** . Bei den Konten ist das Feld **Konto-Unterkategorie** auf *Bargeld* festgelegt und ihr kombinierter Betrag, der als *Bargeld* im Excel-Bericht **Bilanz** angezeigt wird.  

Zusätzliche Blätter in der Excel-Arbeitsmappe zeigen die Daten hinter dem Bericht an. Um jedoch herauszufinden, was sich hinter den Gruppierungen in den Excel-Berichten verbirgt, müssen Sie möglicherweise zu [!INCLUDE [prodshort](includes/prodshort.md)] zurückkehren und beispielsweise auf die Listen Filter anwenden.  

## <a name="the-prodshort-excel-add-in"></a>Das [!INCLUDE [prodshort](includes/prodshort.md)]-Excel-Add-in

Ihre [!INCLUDE [prodshort](includes/prodshort.md)] Benutzeroberfläche umfasst das Add-In für Excel. Abhängig von Ihrem Abonnement werden Sie automatisch angemeldet, oder Sie müssen die selben Anmeldedetails festlegen, die Sie verwenden für [!INCLUDE [prodshort](includes/prodshort.md)]. Weitere Informationen finden Sie unter [Anzeigen und Bearbeiten in Excel von Business Central](across-work-with-excel.md).  

Mit dem Add-In können Sie neue Daten abrufen von [!INCLUDE [prodshort](includes/prodshort.md)], und Sie können Änderungen zurück importieren [!INCLUDE [prodshort](includes/prodshort.md)]. Die Möglichkeit, ein Rückverfolg«»en der Daten zurück zur Datenbank für Excel-Finanzberichte in der Liste oben wird deaktiviert.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Anzeigen und Arbeit in Excel aus Business Central](across-work-with-excel.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit  Business Central](ui-work-product.md)  
