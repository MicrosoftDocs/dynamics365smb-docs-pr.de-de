---
title: Arbeiten mit Finanzübersichten in Excel
description: 'Mehr erfahren, wie Sie die Finanzauswertungen in Microsoft Excel von Business Central für eine bessere Analyse öffnen können.'
author: edupont04
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="analyzing-financial-statements-in-microsoft-excel" />Analysieren von Finanzauswertungen in Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] liefert KPIs und erhält einen Überblick über die Finanzen Ihres Unternehmens. Im Folgenden finden Sie Beispiele für die Analyse von KPIs und Übersichten in Excel:

* Öffnen Sie Listen in Excel öffnen und analysieren die Daten dort. 
* Sie können jedoch umfangreiche Finanzauswertungen wie Ihre Bilanz oder der GuV in Excel exportieren, die Daten analysieren und Berichte drucken.  

> [!TIP]
> Standardmäßig sind die Berichte, die Sie in Excel anzeigen können, darauf ausgelegt, Ihnen bei der Analyse des laufenden Jahres zu helfen. Eine Ausnahme bildet jedoch der Gewinn- und Verlustbericht. Mit diesem Bericht können Sie Daten filtern, um frühere Jahre in Ihre Analysen einzubeziehen.

## <a name="getting-the-overview-and-the-details-in-excel" />Abrufen der Übersicht und Details in Excel

Sie wählen die Finanzberichte zum Anzeigen in Excel mit der Aktion **Berichte** im Business Manager und Buchhalter Rollen-Centers ab. Wenn Sie den anzuzeigenden Kontoauszug auswählen, wird er in Excel oder in Excel online geöffnet. Ein Add-In verbindet die Daten mit [!INCLUDE [prod_short](includes/prod_short.md)]. Sie müssen sich möglicherweise mit demselben Konto anmelden, das Sie mit [!INCLUDE [prod_short](includes/prod_short.md)] verwenden. In der folgenden Tabelle sind die Berichte aufgeführt, sowie wo sie verfügbar sind.  


|Bericht  |Rollencenter  |
|---------|---------|
|Kontenplan                 | Geschäftsführer, Buchhalter |
|Gewinn- und Verlustrechnung              | Geschäftsführer, Buchhalter |
|Cashflow-Auszug       | Geschäftsführer, Buchhalter |
|Auszug nicht ausgeschütteter Gewinne| Geschäftsführer, Buchhalter |
|Ermittelte Verkaufssteuern         | Geschäftsführer, Buchhalter |
|Debitorenaufstellungen           | Geschäftsführer, Buchhalter |
|Kreditor-Saldenrückblick         | Buchhalter |
|Debitor - Saldenrückblick      | Buchhalter |

Nehmen wir mal an, Sie möchten den Cashflow vertiefter ansehen. Vom Geschäftsleiter- oder dem Buchhalter-Rollencenter aus können Sie den Bericht **Cashflow-Auszug** in Excel öffnen, tatsächlich exportieren wir aber die relevanten Daten für Sie und erstellen ein Excel-Arbeitsblatt auf Grundlage einer vordefinierte Vorlage. Abhängig von Ihrem Browser werden Sie aufgefordert, möglicherweise das Arbeitsblatt zu öffnen oder zu speichern.  

Dort finden Sie eine Registerkarte, in der die Daten für Sie im ersten Arbeitsblatt ausgebreitet werden. Alle Daten, die exportiert wurden, sind ebenfalls in anderen Arbeitsblättern vorhanden, wenn Sie sie benötigen. Sie können den Bericht sofort drucken, oder Sie können das Feld ändern, solange Sie die Übersicht und die Details haben, die Sie anzeigen möchten. Verwenden Sie das [!INCLUDE [prod_short](includes/prod_short.md)] Excel-Add-In, um Daten zu filtern und zu analysieren.  

### <a name="understanding-the-excel-templates" />Grundlegendes zu den Excel-Vorlagen

Die vordefinierten Excel-Berichte basieren auf den Daten im aktuellen Unternehmen. Zum Beispiel hat das Demounternehmen den Kontenplan eingerichtet, um drei Barkonten unter *Umlaufvermögen* aufzulisten: 10100 **Girokonto**, 10200 **Sparkonto** und 10300 **Portokasse**. Bei den Konten ist das Feld **Konto-Unterkategorie** auf *Bargeld* festgelegt und ihr kombinierter Betrag, der als *Bargeld* im Excel-Bericht **Bilanz** angezeigt wird.  

Andere Blätter im Excel-Arbeitsblatt zeigen die Daten hinter dem Bericht an. Um herauszufinden, was sich hinter den Gruppierungen in den Excel-Berichten verbirgt, müssen Sie möglicherweise die Listen in [!INCLUDE [prod_short](includes/prod_short.md)] filtern.  

## <a name="the--excel-add-in" />Das [!INCLUDE [prod_short](includes/prod_short.md)]-Excel-Add-in

Ihre [!INCLUDE [prod_short](includes/prod_short.md)] Benutzeroberfläche umfasst das Add-In für Excel. Abhängig von Ihrem Abonnement werden Sie automatisch angemeldet, oder Sie müssen Ihre Anmeldedetails festlegen, die Sie für [!INCLUDE [prod_short](includes/prod_short.md)] verwenden. Weitere Informationen finden Sie unter [Anzeigen und Bearbeiten in Excel von Business Central](across-work-with-excel.md).  

Mit dem Add-In können Sie neue Daten aus [!INCLUDE [prod_short](includes/prod_short.md)] abrufen, und Sie können Änderungen zurück in [!INCLUDE [prod_short](includes/prod_short.md)] importieren. Die Möglichkeit, ein Rückverfolgen der Daten zurück zur Datenbank ist nicht für Finanzberichte, die in Excel angezeigt werden können, verfügbar.  

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Siehe auch

[Anzeigen und Arbeit in Excel aus Business Central](across-work-with-excel.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
