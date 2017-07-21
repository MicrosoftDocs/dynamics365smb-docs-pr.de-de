---
title: "Aktualisieren von Währungswechselkursen | Microsoft Docs"
description: "Um mehrere Währungen in Ihrem Unternehmen zu verwenden, können Sie einen Code für jede Währung einrichten und einen externen Wechselkursdienst, wie Yahoo verwenden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Vorgehensweise: Aktualisieren von Währungswechselkursen
Sie müssen für jede Währung, die Sie verwenden, einen Währungscode einrichten, wenn Sie in anderen Währungen als Ihrer Mandantenwährung verkaufen oder einkaufen, Forderungen oder Verbindlichkeiten haben oder in unterschiedlichen Währungen buchen.  

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

Sie können einen externen Service verwenden, um Ihre Währungswechselkurses auf dem neuesten Stand zu halten. Der Service wird vorinstalliert und Yahoo Currency Exchange Rates ist vorbereitet und muss lediglich noch aktiviert werden.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>So richten Sie einen Währungswechselkurs-Service ein
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Fenster **Währungswechselkurs-Service** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie das Kontrollkästchen **Aktiviert**, um den Service zu aktivieren.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Um Währungswechselkurse über einen Service zu aktualisieren
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") ein und wählen **Währungswechselkurs-Dienste** und wählen dann den zugehörigen Link aus.
2. Wählen Sie die **Aktualisieren von Wechselkursen** Aktion aus.

Der Wert im Feld **Wechselkurs** wird im Fenster **Währung** mit dem aktuellen Währungswechselkurs aktualisiert.

## <a name="see-also"></a>Siehe auch
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

