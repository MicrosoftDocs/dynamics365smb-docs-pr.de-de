---
title: 1099-Transaktionen in den USA melden| Microsoft Docs
description: "In Ihren Einkaufsbelegen können Sie angeben, dass 1099 für den Beleg vorgeschrieben ist und Sie können den Code 1099 für den Kreditor angeben."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a0a31c28b6c96dc80593ac3862b97b36c3ec81c7
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="reporting-1099-transactions-in-the-us"></a>1099-Transaktionen in den USA melden
Die Bundessteuerbehörde der USA (IRS) benötigt eine oder mehrere Versionen des Steuerformulars 1099 für Zahlungen an Kreditoren. Kopien dieser Formulare müssen jedes Jahr an Kreditoren am oder vor dem letzten Tag im Januar gesendet werden. In Ihren Einkaufsbelegen können Sie angeben, dass 1099 für den Beleg vorgeschrieben ist und Sie können den Code 1099 für den Kreditor angeben.  

## <a name="1099-codes"></a>1099-Codes
In [!INCLUDE[d365fin](includes/d365fin_md.md)] sind die häufigsten 1099-Codes für Sie bereits eingerichtet, sodass Sie darauf vorbereitet sind, die erforderlichen Erklärungen zu generieren. Die Codes werden im Fenster **IRS 1099-Formularfeld** definiert, wo Sie auch neue 1099-Codes hinzufügen können. Für jeden steuerpflichtigen Kreditor können Sie auch den relevanten 1099-Code im Inforegister **Zahlungen** auf der Kreditorenkarte angeben.  

Mit dem Bericht **Kreditor 1099 – Informationen** können Sie die 1099-Transaktionen überprüfen, die während einer angegebenen Zeitspanne bezahlt werden. Am Ende des Geschäftsjahres können Sie 1099-Transaktionen auf Formularvordrucken ausdrucken.  

## <a name="printing-1099-tax-forms"></a>Drucken von Steuerformularen 1099
Vom Fenster **IRS 1099-Formularfeld** aus können Sie auf die folgenden Steuerformulare zugreifen:  

* Kreditor 1099 Div  

  Druckt das Formular 1099-DIV der Bundessteuerbehörde für Dividenden und Verteilung aus. Sie können alle oder bestimmte 1099-DIV-Formulare drucken. Der Bericht verwendet die Codes, die für die Betragsfelder im DIV-Formular aus dem Fenster **IRS 1099-Formularfeld** gelten.  
* Kreditor 1099 Int  

  Druckt das Formular 1099-INT der Bundessteuerbehörde für Zinserträge. Sie können alle oder bestimmte 1099-INT-Formulare drucken. Der Bericht verwendet die Codes, die für die Betragsfelder im INT-Formular aus dem Fenster **IRS 1099-Formularfeld** gelten.  
* Kreditor 1099 Misc - Sonstige Einnahmen  

  Druckt das Formular 1099-MISC der Bundessteuerbehörde für sonstige Einnahmen. Sie können alle oder bestimmte 1099-MISC-Formulare drucken. Der Bericht verwendet die Codes, die für die Betragsfelder im MISC-Formular aus dem Fenster **IRS 1099-Formularfeld** gelten.  

Die gesetzlichen Änderungen, die diesen Bericht und die Tabellendaten beeinflussen, werden im Allgemeinen in den Jahresendupdates behandelt.
Es kann hilfreich sein, den Bericht **Kreditor 1099 – Informationen** auszuführen, um die Daten zu überprüfen, bevor die Formulare gedruckt werden.

## <a name="submitting-1099-tax-forms-electronically"></a>1099-Steuerformulare elektronisch versenden
Um die 1099-Steuerformulare elektronisch zu versenden, verwenden Sie den Bericht **Kreditor 1099 – magnetische Medien**. Gibt die Formulare 1099 an, die exportiert werden können. Die Formularinformationen, die durch diesen Bericht exportiert werden, sind die gleichen wie die Berichte, die 1099-Formulare drucken, die im vorherigen Abschnitt beschrieben werden.  

Der Bericht verwendet die Codes, die für die Betragsfelder im Formular aus dem Fenster **IRS 1099-Formularfeld** gelten. Die Codes werden den Formularfeldern in den Dateilayouts dieses Berichts zugeordnet, deshalb müssen die Tabellendaten und die Berichtsversion für ein bestimmtes Steuerjahr übereinstimmen. Wenn irgendwelche benutzerdefinierten Codes der Tabelle hinzugefügt werden, müssen diese den Formularfeldern innerhalb dieses Objekts zugeordnet werden.  

Die gesetzlichen Änderungen, die diesen Bericht und die Tabellendaten beeinflussen, werden im Allgemeinen in den Jahresendupdates behandelt.
Es kann hilfreich sein, den Bericht **Kreditor 1099 – Informationen** auszuführen, um die Daten zu überprüfen, bevor die elektronische Datei generiert wird.  

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Einen neuen Kreditor registrieren](purchasing-how-register-new-vendors.md)  
[Vorgehensweise: Einkauf erfassen](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]  

