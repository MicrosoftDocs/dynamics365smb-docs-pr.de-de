---
title: "Dient zum Einrichten mehrerer Zinssätze."
description: "Sie können Zinsrechnungen mit mehreren Zinssätzen für eine bestimmte Periode berechnen. Die Zinsberechnung ist für alle finanziellen Belastungen, nur mit Veränderung des Zinssatzes für eine bestimmte Periode ähnlich."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0af01fe46f6b7df1149825c35a9fc0cc19482403
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-multiple-interest-rates"></a>Dient zum Einrichten mehrerer Zinssätze.
Mehrere Zinssätze werden für verschiedene Perioden für gestundete Zahlungen in den Geschäftstransaktionen verwendet. Beispielsweise zeigt eine Regierung den maximalen Zinsen, der für einen Verbraucher erhoben wird. Dieser Zinssatz kann zweimal jährlich geändert werden am 1. Januar und 1. Juli. Der Zinssatz zwischen Unternehmen (B2B) wird von beiden Parteien vereinbart und dort ist keine Begrenzung zu dieser Kundengruppe. Der angekündigte Kurs ist normalerweise vier Prozent mehr als die normalen Bankzinsen.

Wenn Sie Zinskonditionen und Mahnmethoden für verspätete Zahlungen einrichten, können Sie mehrere Zinssätzen angeben, damit die Strafgebühr aus verschiedenen Zinssätzen in verschiedenen Perioden berechnet wird. Weitere Informationen finden Sie unter [Offene Salden eintreiben](receivables-collect-outstanding-balances.md)

## <a name="to-set-up-multiple-interest-rates"></a>Einrichten mehrerer Zinssätze.  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnungsbestimmungen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Im Fenster **Zinskonditionen** wählen Sie den gewünschten Finanzausdruck, und wählen die Aktion **Zinssätze**.  
3.  Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Wählen Sie die Schaltfläche **OK** aus.  
5.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Mahnungsbestimmungen** ein. Wählen Sie dann den zugehörigen Link aus.  
6.  Im Fenster **Mahnsbestimmung** wählen Sie die gewünschte Mahnbestimmung und wählen die Aktion **Stufen** aus.  
7.  Im Fenster **Mahnstufen** wählen Sie das Feld **Zins berechnen** aus.  

Wenn Sie eine Zinsrechnung registrieren, wird deren Registrierung die Zinsrechnungen mit mehreren Zinssätzen während eines bestimmten Zeitraums anzeigen. Die Mahnung enthält außerdem die Kontaktdetails des Debitors, des Unternehmens, das die Mahnung ausgibt, den Zusatzbetrag und den Gesamtbetrag. Der Eröffnungsposten der Zinsrechnung wird fett angezeigt. Die Zinsrechnungen werden mit verschiedenen Zinssätzen für eine bestimmte Periode berechnet und werden nach dem Eröffnungsposten der Mahnung gedruckt.  

## <a name="see-also"></a>Siehe auch  
[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md)  
[Finance einrichten](finance-setup-finance.md)

