---
title: "Vorgehensweise: Einrichten von Kostenträgern| Microsoft Docs"
description: "Erfahren Sie, wie Sie Kostenträger eingerichtet werden, die gleich sind wie Dimensionen in der Finanzbuchhaltung."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3f371a772f710576a70bac4808b15be091a61d66
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-cost-objects"></a>Einrichten von Kostenträgern
Kostenträger sind Projekte, Produkte oder Services eines Unternehmens. Der Kostenträgerplan ähnelt den Dimensionsinformationen für das Sachkonto. Sie können den Kostenträgerplan auf die folgenden Weisen einrichten:  

* Transferieren Sie Dimensionswerte im Sachkonto zum Kostenträgerplan. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
* Erstellen Sie einen neuen Kostenträgerplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenträgerplan einen neuen Kostenträger hinzu. Sie müssen jeden Kostenträger einzeln erstellen.  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a>So transferieren Sie Dimensionswerte aus dem Sachkonto zum Kostenträgerplan  
1.  Legen Sie eine Dimension als Kostenträgerdimension im Fenster **Kostenträger-Dimensionen aktualisieren** fest. Nur die Werte aus dieser Dimension werden übertragen.  
2.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kostentr'gerplan** ein und wählen dann den zugehörigen Link aus.  
3.  Wählen Sie die Aktion **Kostenträger aus Dimension abrufen**, um Dimensionswerte zum Kostenträgerplan zu übertragen. Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.  

    > [!NOTE]  
    >  Sie können das Feld **Kostenträgerdimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Sachkonto zum Kostenträgerplan definiert wird. Sie können keine Synchronisierung des Kostenträgerplans mit Dimensionswerten aus dem Sachkonto definieren.  

Der Kostenträgerplan enthält jetzt alle angegebenen Dimensionswerte aus dem Sachkonto und umfasst Titel und Zwischensummen.  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a>So richten Sie im Fenster Kostenstellenträger neue Kostenträger ein  
Sie können Kostenkarten im Fenster **Kostenträger** oder im Fenster **Kostenträgerkarte** einrichten und verwalten. So richten Sie im Fenster **Kostenträger** neue Kostenstellenträger ein.  

1.  Öffnen Sie das Fenster **Kostenstellenträger** im Bearbeitungsmodus.  
2.  Geben Sie im Feld **Code** den Kostenträgercode ein. Alle Kostenträger müssen einen Code aufweisen.  
3.  Geben Sie im Feld **Namen** den Kostenträgernamen ein.  
4.  Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck des Kostenträgers anzugeben.  

    * Für Kostenträger der **Summe**-Zeilenart müssen Sie das Feld **Summe Von/Bis** ausfüllen. Verwenden Sie den **Oder**-Operator, der eine vertikale Zeile (**&#124;**) ist, um Bereiche von Kostenträgern festzulegen.  
    * Für Kostenträger der **Bis-Summe**-Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.  
5.  Füllen Sie das Feld **Sortierungsauftrag** aus.  
6.  Wählen Sie die nächste leere Zeile aus, um einen neuen Kostenträger zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.  
7.  Nachdem Sie alle Kostenträger eingerichtet haben, wählen Sie die Aktion **Kostenträger einrücken** aus. Wählen Sie die Schaltfläche **Ja** aus.  

> [!IMPORTANT]  
>  Wenn Sie Definitionen in den **Summe Von/Bis**-Feldern für **Bis-Summe**-Kostenträger eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben. Die Funktion überschreibt die Werte in allen **Bis-Summe**-Feldern.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
[Definieren von Kostenstellen und Kostenträgern für Kontenpläne](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Salden zwischen Kostenart, Kostenstelle und Kostenträger](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)   
[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)   
[Informationen zur Kostenrechnung](finance-about-cost-accounting.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

