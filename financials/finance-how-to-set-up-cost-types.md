---
title: 'Vorgehensweise: Einrichten eines Kostenartenplans | Microsoft Docs'
description: "Kostenartenpläne ähneln Kontenpläne im Sachkonto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 945a60af52eec7fb4f00842acdac42472d735a12
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cost-types"></a>Einrichten von Kostenträgern
Kostenartenpläne ähneln Kontenpläne im Sachkonto. Sie können den Kostenartenplan auf die folgenden Weisen einrichten:  

-   Strukturieren Sie den Kostenartenplan ähnlich wie GuV-Konten im Sachkontenplan. Dann können Sie den Sachkontenplan in den Kostenartenplan übertragen. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
-   Erstellen Sie einen neuen Kostenartenplan, oder fügen Sie einem vorhandenen Kostenartenplan neue Kostenarten hinzu. Sie müssen jede neue Kostenart einzeln erstellen.  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a>So übertragen Sie den Sachkontenplan in den Kostenartenplan.  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Kostenartenplan** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Kostenarten aus K&ontenplan abrufen**. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen. Die Funktion verwendet den Kontenplan, um einen Kostenartenplan zu erstellen.  

    Der Kostenartenplan enthält jetzt alle GuV-Konten im Sachkonto und umfasst Überschriften und Zwischensummen. Sie können den Kostenartenplan ändern, falls erforderlich. Beispielsweise können Sie doppelt vorhandene Kostenarten löschen.  

    > [!IMPORTANT]  
    >  Die **Kostenarten in Kontenplan registrieren**-Funktion aktualisiert das Verhältnis zwischen dem Kontenplan und dem Kostenartenplan. Das **Nr.** Das Feld  wird ausgefüllt und geprüft, um sicherzustellen, dass jedes Sachkonto mit nur einer Kostenart verknüpft ist. Die Funktion wird automatisch ausgeführt, bevor Sie Sachposten in die Kostenrechnung übertragen.  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-window"></a>So richten Sie im Fenster "Liquiditätskontenplan" neue Liquiditätskonten ein  
1.  Öffnen Sie das Fenster **Kontenplan-Arten** im Bearbeitungsmodus.  
2.  Füllen Sie je nach Bedarf die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Sie können Kostenarten im Fenster **Kostenartkarte** oder im Fenster **Kostenartenplan** einrichten und verwalten. So richten Sie im Fenster **Liquiditätskontenplan** neue Liquiditätskonten ein.

3.  Nachdem Sie alle Kostenarten erstellt haben, wählen Sie die Aktion **Kostenarten einrücken** aus. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**.  
4.  Verknüpfen Sie die neue Kostenart mit dem entsprechenden Sachkonto.  

    > [!IMPORTANT]  
    >  Wenn Sie in den Feldern **Zusammenzählung** Definitionen für die Zeilenart **Bis-Summe** eingetragen haben, bevor Sie die Funktion **Kostenarten einrücken** ausgeführt haben, müssen Sie diese Eintragungen wiederholen, da die Funktion die Werte in allen **Bis-Summe**-Feldern überschreibt.  

## <a name="to-update-cost-types"></a>So aktualisieren Sie Kostenarten  
1.  Im Fenster **Kostenrechnung einrichten**  wählen Sie aus, ob der Kostenartenplan automatisch aktualisiert werden soll, wenn der Kontenplan geändert wird.  
2.  Die folgenden Optionen stehen im Feld **Sachkonto ausrichten** zur Auswahl.  

- **Keine Ausrichtung** - Es gibt keine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.  
- **Automatisch** - Es gibt eine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.  
- **Eingabeaufforderung** - Eine Meldung wird mit der Frage angezeigt, ob Sie die entsprechende Änderung auch im Kostenartenplan vornehmen möchten, wenn Sie den Kontenplan ändern.  

## <a name="see-also"></a>Siehe auch  
[Kostenrechnung](finance-manage-cost-accounting.md)  
[Definieren der Beziehung zwischen Kostenarten und Sachkonten](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   
[Definieren von Kostenstellen und Kostenträgern für Kontenpläne](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md)   
[Salden zwischen Kostenart, Kostenstelle und Kostenträger](finance-balances-between-cost-type-cost-center-and-cost-object.md)   
[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)   
[Terminologie der Kostenrechnung](finance-terminology-in-cost-accounting.md)   
[Informationen zur Kostenrechnung](finance-about-cost-accounting.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

