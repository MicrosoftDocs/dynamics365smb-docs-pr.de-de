---
title: Abschreibungsrsicherung einrichten| Microsoft Docs
description: "Um die Abdeckung der Anlagenversicherung zu verwalten, müssen Sie pro Versicherung einige allgemeine Versicherungsinformationen und eine Versicherungskarte einrichten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 16098723fed40fbe26b9ba238e7fe5bf339003f5
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-fixed-asset-insurance"></a>Um Anlagenversicherung einzurichten:
Um die Abdeckung der Anlagenversicherung zu verwalten, müssen Sie pro Versicherung einige allgemeine Versicherungsinformationen und eine Versicherungskarte einrichten.

## <a name="to-set-up-general-insurance-information"></a>So richten Sie allgemeine Versicherungsinformationen ein
Um die Versicherungsfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]  verwenden zu können, müssen Sie einige allgemeine Versicherungsinformationen einrichten.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **FA Einrichtung** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>So richten Sie Versicherungsarten ein
Sie können die Versicherungspolicen in Kategorien gruppieren, beispielsweise für Diebstahl- und Feuerversicherungen. Die Versicherungsarten werden auf der Versicherungskarte verwendet.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versicherungsarten** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-insurance-cards"></a>So richten Sie Versicherungskarten ein
Sie können die gesammelten Informationen über die einzelnen Versicherungspolicen auf der Versicherungskarte eingeben.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versicherung** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Versicherung** die Aktion **Neu** aus, um eine neue Karte für eine Versicherungspolice zu erstellen.  
3. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-insurance-journal-templates"></a>So richten Sie Versicherungs Buch.-Blattvorlagen ein
[!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt automatisch eine Versicherungs-Buch.-Blattvorlage, wenn Sie zum ersten Mal das Fenster **Versicherungs Buch.-Blatt** öffnen; Sie können aber zusätzliche Vorlagen einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versicherungserfassungsvorlage** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-up-insurance-journal-batches"></a>So richten Sie Versicherungs Buch.-Blattnamen ein
Sie können zusätzliche Namen in einer Versicherungs Buch.-Blattvorlage einrichten. Die Werte in dem Buch.-Blattnamen werden als Vorgabewerte verwendet, wenn die Felder in den Buch.-Blattzeilen nicht ausgefüllt sind. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versicherungserfassungsvorlage** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie eine Vers. Buch.-Blattvorlage und dann die Aktion **Buch.-Blattnamen** aus.
3. Füllen Sie im Fenster **Vers. Buch.-Blattnamen** die notwendigen Felder aus.

> [!NOTE]  
>   Zahlen haben in Buch.-Blattnamen eine spezielle Funktion. Wenn die Buch.-Blattvorlage oder der Buch.-Blattname eine Nummer enthält, wird diese beim Buchen des Buch.-Blatts automatisch um eins hochgezählt. Wenn z. B. HH1 in dem Feld **Name** verwendet wurde, ändert sich der Name auf HH2, nachdem das Buch.-Blatt HH1 gebucht wurde.

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

