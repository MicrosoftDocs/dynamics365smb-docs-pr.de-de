---
title: 'So gehts: Arbeiten mit GIFI-Codes in Kanada| Microsoft Docs'
description: Weitere Informationen zu GIFI-Codes
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/23/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 03316fe6ad7a63c79a88f540a9c49f61450922f4
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So gehts: Arbeiten mit GIFI-Codes in Kanada
<a id="how-to-work-with-gifi-codes-in-canada" class="xliff"></a>
Steuerinformationen können Sachkonten, Berichte, GuV, Bilanzen und Auszüge nicht ausgeschütteter Gewinne beinhalten. Steuerinformationen werden mithilfe von Codes klassifiziert. Die Verwendung von Codes hilft den Behörden, Daten zu bearbeiten, sie für die elektronische Speicherung vorzubereiten und Steuerdaten elektronisch zu überprüfen . Außerdem hilft die Verwendung von Codes statistischen Organisationen, effizienter zu arbeiten, da Finanzdaten zeitnah zur Verfügung stehen. Weitere Informationen finden Sie auf der [Webseite der Canada Revenue Agency](http://www.cra-arc.gc.ca/).

Die Canada Revenue Agency verwendet den General Index of Financial Information (GIFI), um Finanz- und Steuerdaten zu erfassen, zu überprüfen und elektronisch zu verarbeiten. Üblicher Weise werden GIFI-Codes nur für die Buchungskonten zugewiesen, sodass jede Zusammenzählung durch die Steuervorbereitungs-Software ausgeführt wird.

Wenn ein Konto einem GIFI-Code zugeordnet ist, wird es der Einnahmenenagentur unter diesem Code gemeldet. Mehrere Konten können alle denselben GIFI-Code haben, aber jedes Konto kann nur einen GIFI-Code haben.

Sie können Saldoinformationen mit dem GIFI-Code exportieren und die exportierte Datei in Excel speichern. Dies ist nützlich, wenn Sie Informationen an Ihre Steuervorbereitungs-Software übertragen wollen.

## So richten Sie GIFI-Codes ein:
<a id="to-set-up-gifi-codes" class="xliff"></a>
In Dynamics NAV müssen Sie GIFI-Codes für Sachkonten, Berichte, Bilanzen, Einkommensblätter und Auszüge nicht ausgeschütteter Gewinne einrichten.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **GIFI-Codes** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Fenster **GIFI Codes** die Aktion **Neu** aus.
3. Richten Sie GIFI-Codes ein, indem Sie die Felder ausfüllen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## So ordnen Sie GIFI-Codes Sachkonten zu
<a id="to-associate-gifi-codes-with-gl-accounts" class="xliff"></a>
Um Finanzdaten mit GIFI-Code zu übermitteln, muss jeder GIFI-Code den entsprechenden Konten im Kontenplan zugeordnet werden.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie ein entsprechendes Sachkonto, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Inforegister **Kostenrechnung** im Feld **GIFI Code** den entsprechenden GIFI-Code aus.

## So verwenden Sie den GIFI-Code-Bericht, um Kontosalden anzuzeigen
<a id="to-view-account-balances-using-the-gifi-code-report" class="xliff"></a>
Sie können Ihre Kontosalden mit dem GIFI-Code überprüfen, indem Sie den **Kontosalden durch GIFI-Code**-Bericht verwenden.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Kontosaldo nach GIFI-Code** ein und wählen Sie dann den entsprechenden Link aus.
2. Legen Sie fest, was in den Bericht einbezogen werden soll, indem Sie die Felder ausfüllen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die **Druck** oder **Vorschau** Schaltfläche.

## So exportieren Sie Saldoinformationen mithilfe von GIFI-Codes
<a id="to-export-balance-information-using-gifi-codes" class="xliff"></a>
Sie können Saldoinformationen mithilfe von GIFI-Codes exportieren und die exportierte Datei in Excel speichern. Sie können die Datei ändern, speichern oder löschen. Sie können die Datei verwenden, um Informationen an Ihre Steuervorbereitungs-Software zu übertragen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **GIFI-Info in Excel exportieren** eingeben und den entsprechenden Link auswählen.
2. Geben Sie an, was Sie in Excel exportieren wollen, indem Sie die Felder ausfüllen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie die Schaltfläche **OK** aus.

**Hinweis:** Die Excel-Datei hat folgende Eigenschaften:

* Der Saldo wird auf den nächsten Prozentsatz gerundet, aber der Zellenwert behält den gleichen Prozentsatz bei, den er auch in der Finanzbuchhaltung hat.
* Negative Zahlen werden als positive Zahl in Klammern dargestellt. Dementsprechend wird -123 als (123) dargestellt.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Finanzen](finance.md)   
[Finance einrichten](finance-setup-finance.md)

