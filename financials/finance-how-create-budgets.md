---
title: Erstellen von Budgets| Microsoft Docs
description: "Erstellen Sie Budgets, um verschiedene Finanzaktivitäten zu prognostizieren und Dimensionen zu den einzelnen Intelligence-Zwecken zuzuordnen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7dfd3cc7efe00b48a39982bb220ccc21b7409da4
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create--budgets"></a>So wird's gemacht: neue Budgets erzeugen
Sie können für dieselbe Periode mehrere Budgets verwalten, indem Sie Budgets mit verschiedenen Namen einrichten. Zuerst richten Sie den Budgetnamen ein und geben die Budgetzahlen ein. Der Budgetname wird dann allen Budgetposten zugewiesen, die Sie erstellen.  

 Wenn Sie ein Budget erstellen, können Sie für jedes Budget vier Dimensionen festlegen. Diese bugetspezifischen Dimensionen werden Budgetdimensionen genannt. Sie wählen die Budgetdimensionen für jedes Budget aus den Dimensionen, die Sie bereits eingerichtet haben. Budgetdimensionen können Budgetposten hinzugefügt werden und als Filter für ein Budget verwendet werden. Weitere Informationen finden Sie unter [Arbeiten mit Dimensionen](finance-dimensions.md)

 Budgets spielen eine wichtige Rolle in der Business Intelligence wie Finanzauswertung auf Basis von Kontenschemata, die erneut den Budgetposten enthalten, oder beim geplant Analysieren von tatsächlichen Beträgen im Kontenplan. Weitere Informationen finden Sie unter [Business Intelligence](bi.md).   

 > [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.  

### <a name="to-create-a-new-budget"></a>Einrichten eines neuen Budgets  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen] Symbol (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **G/L-Blatt Budgets** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Liste bearbeiten** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Buch.-Blatt bearbeiten** aus.
4. Im Fenster oben von **Budget** füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.  

    Nur Posten, die diesen Budgetnamen enthalten, der im Feld **Artikelbudgetname** angezeigt wird, werden nun angezeigt. Da der Budgetname gerade erstellt wurde, gibt es keine Posten, die dem Filter entsprechen. Daher ist das Fenster leer.  
5. Wählen Sie zum Eingeben eines Betrags die entsprechende Zelle in der Matrix. Das Fenster **Finanzbudgetposten** wird geöffnet.  
6. Erstellen Sie eine neue Zeile, und füllen Sie das Feld **Betrag** aus. Schließen Sie das Fenster **Finanzbudgetposten**.  
7. Wiederholen Sie die Schritte 5 bis 6, bis alle Budgetbeträge eingegeben sind.  

> [!NOTE]  
>  Im Inforegister  **Filter** stehen zwischen vier und acht Filter zur Verfügung, abhängig davon, wie viele  Budgetdimensionen für den Budgetnamen eingerichtet wurden.   

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Business Intelligence](bi.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

