---
title: Anlagenwartung einrichten
description: 'Um Anlagenreparaturen und -Dienst zu verwalten, geben Sie allgemeine Wartungsinformationen, Codes für die Art der Arbeit und eine Buchung für Kosten an.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'repair, service'
ms.search.form: '5600, 5642'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-fixed-asset-maintenance"></a>Um Anlagenwartung einzurichten:
Um die Anlagenwartung zu verwalten, müssen Sie erst einige allgemeine Wartungsinformationen einrichten, ein Buchungskonto für Wartungskosten und Wartungscodes für die Arten von Arbeit, beispielsweise Instandhaltung oder Reparatur.

## <a name="to-set-up-general-maintenance-information"></a>So richten Sie allgemeine Wartungsinformationen ein:
Wenn Sie die Felder für Wartung eingerichtet haben, können Sie Wartungsausgaben aus einem Buch.-Blatt buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage, für die Sie den Versicherungsposten festlegen wollen, und wählen die Aktion **Bearbeiten** aus.
3. Füllen Sie auf dem Inforegister **Wartung** die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>So richten Sie Wartungscodes ein
Wenn Sie Wartungskosten aus einem Fibu Buch.-Blatt buchen, füllen Sie das Feld **Wartungscode** aus. So erfassen Sie, welche Art von Wartung durchgeführt wurde, beispielsweise Instandhaltung oder Reparatur.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Wartung** ein und wählen Sie dann den zugehörigen Link.
2. Legen Sie auf der Seite **Wartung** Codes für unterschiedliche Arten von Wartungsarbeiten fest.

## <a name="to-set-up-maintenance-expense-accounts"></a>So richten Sie Aufwandskonten für die Wartung ein
Um Wartungskosten zu buchen, müssen Sie erst eine Kontonummer auf der Seite **Anlagenbuchungsgruppen** eingeben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **FA-Buchungsgruppen** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie das Feld **Aufwandskto. Wartung** für jede einzelne Buchungsgruppe aus.

> [!NOTE]  
>   Um festzulegen, ob Wartungskosten auf Kostenstellen und/oder Kostenträger verteilt werden, müssen Sie einen Verteilungsschlüssel einrichten. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
