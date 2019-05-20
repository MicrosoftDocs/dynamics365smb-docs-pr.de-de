---
title: Abschreibungsverwaltung einrichten| Microsoft Docs
description: Um Anlagenreparaturen und -Dienst zu verwalten, geben Sie allgemeine Wartungsinformationen, Codes für die Art der Arbeit und eine Buchung für Kosten an.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ba01ccb88349a1f1943655949a36e2a21f3ae2de
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244493"
---
# <a name="set-up-fixed-asset-maintenance"></a>Um Anlagenwartung einzurichten:
Um die Anlagenwartung zu verwalten, müssen Sie erst einige allgemeine Wartungsinformationen einrichten, ein Buchungskonto für Wartungskosten und Wartungscodes für die Arten von Arbeit, beispielsweise Instandhaltung oder Reparatur.

## <a name="to-set-up-general-maintenance-information"></a>So richten Sie allgemeine Wartungsinformationen ein:
Wenn Sie die Felder für Wartung eingerichtet haben, können Sie Wartungsausgaben aus einem Buch.-Blatt buchen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Anlagen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Anlage, für die Sie den Versicherungsposten festlegen wollen, und wählen die Aktion **Bearbeiten** aus.
3. Füllen Sie auf dem Inforegister **Wartung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>So richten Sie Wartungscodes ein
Wenn Sie Wartungskosten aus einem Fibu Buch.-Blatt buchen, füllen Sie das Feld **Wartungscode** aus. So erfassen Sie, welche Art von Wartung durchgeführt wurde, beispielsweise Instandhaltung oder Reparatur.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verwaltung** ein, und wählen dann den zugehörigen Link aus.
2. Legen Sie auf der Seite **Wartung** Codes für unterschiedliche Arten von Wartungsarbeiten fest.

## <a name="to-set-up-maintenance-expense-accounts"></a>So richten Sie Aufwandskonten für die Wartung ein
Um Wartungskosten zu buchen, müssen Sie erst eine Kontonummer auf der Seite **Anlagenbuchungsgruppen** eingeben.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Auftragsbuchungsruppen** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie das Feld **Aufwandskto. Wartung** für jede einzelne Buchungsgruppe aus.

> [!NOTE]  
>   Um festzulegen, ob Wartungskosten auf Kostenstellen und/oder Kostenträger verteilt werden, müssen Sie einen Verteilungsschlüssel einrichten. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
