---
title: 'So geht''s: Einrichten der Anlagenversicherung| Microsoft Docs'
description: "Beschreibt, wie Versicherungen für Anlagen eingerichtet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6473b74823f787e6b1eac599bb95b6d100a02c1e
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Einrichten der Anlagenversicherung
<a id="how-to-set-up-fixed-asset-insurance" class="xliff"></a>
Um die Abdeckung der Anlagenversicherung zu verwalten, müssen Sie pro Versicherung einige allgemeine Versicherungsinformationen und eine Versicherungskarte einrichten.

## So richten Sie allgemeine Versicherungsinformationen ein
<a id="to-set-up-general-insurance-information" class="xliff"></a>
Um die Versicherungsfunktionen in [!INCLUDE[d365fin](includes/d365fin_md.md)]  verwenden zu können, müssen Sie einige allgemeine Versicherungsinformationen einrichten.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Anlagen einrichten** eingeben und den entsprechenden Link auswählen.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## So richten Sie Versicherungsarten ein
<a id="to-set-up-insurance-types" class="xliff"></a>
Sie können die Versicherungspolicen in Kategorien gruppieren, beispielsweise für Diebstahl- und Feuerversicherungen. Die Versicherungsarten werden auf der Versicherungskarte verwendet.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Versicherungsart** ein und wählen Sie dann den entsprechenden Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## So richten Sie Versicherungskarten ein
<a id="to-set-up-insurance-cards" class="xliff"></a>
Sie können die gesammelten Informationen über die einzelnen Versicherungspolicen auf der Versicherungskarte eingeben.  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus** ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Versicherung** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie im Fenster **Versicherung** die Aktion **Neu** aus, um eine neue Karte für eine Versicherungspolice zu erstellen.  
3. Füllen Sie die Felder je nach Bedarf aus.

## So richten Sie Versicherungs Buch.-Blattvorlagen ein
<a id="to-set-up-insurance-journal-templates" class="xliff"></a>
[!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt automatisch eine Versicherungs-Buch.-Blattvorlage, wenn Sie zum ersten Mal das Fenster **Versicherungs Buch.-Blatt** öffnen; Sie können aber zusätzliche Vorlagen einrichten. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Versicherungs-Journalvorlage** ein und wählen Sie dann den entsprechenden Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.

## So richten Sie Versicherungs Buch.-Blattnamen ein
<a id="to-set-up-insurance-journal-batches" class="xliff"></a>
Sie können zusätzliche Namen in einer Versicherungs Buch.-Blattvorlage einrichten. Die Werte in dem Buch.-Blattnamen werden als Vorgabewerte verwendet, wenn die Felder in den Buch.-Blattzeilen nicht ausgefüllt sind. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Versicherungs-Journalvorlage** ein und wählen Sie dann den entsprechenden Link aus.  
2. Wählen Sie eine Vers. Buch.-Blattvorlage und dann die Aktion **Buch.-Blattnamen** aus.
3. Füllen Sie im Fenster **Vers. Buch.-Blattnamen** die notwendigen Felder aus.

**Hinweis**Zahlen haben in Buch.-Blattnamen eine spezielle Funktion. Wenn die Buch.-Blattvorlage oder der Buch.-Blattname eine Nummer enthält, wird diese beim Buchen des Buch.-Blatts automatisch um eins hochgezählt. Wenn z. B. HH1 in dem Feld **Name** verwendet wurde, ändert sich der Name auf HH2, nachdem das Buch.-Blatt HH1 gebucht wurde.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

