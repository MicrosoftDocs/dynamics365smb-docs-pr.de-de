---
title: 'Vorgehensweise: Einrichten von MwSt.-Berichten'
description: Informationen aus verschiedenen Rechnungstypen werden verwendet, um Daten in den Ausfuhr-Listenbericht EU zu speisen. Um einen MwSt-Bericht unter dem System ELMA5 von Business Central einzurichten, müssen Sie die Parameter melden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 91f572f1b7673ac8ea01e3057345ae9c95adaa4b
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779109"
---
# <a name="set-up-vat-reports"></a>Richten Sie die MwSt.-Berichte ein.
Informationen aus verschiedenen Rechnungstypen werden verwendet, um Daten in den Ausfuhr-Listenbericht EU zu speisen. Um einen MwSt-Bericht unter dem System ELMA5 von [!INCLUDE[d365fin](../../includes/d365fin_md.md)] einzurichten, müssen Sie die Parameter melden.  

## <a name="to-set-up-a-vat-report"></a>So richten Sie einen MwSt-Bericht ein  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **VAT-Bereichtsservice** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie im Inforegister **Allgemein** das Feld **Übermittelte Berichte bearbeiten** aus, damit Benutzer MwSt.-Erklärungen, die an die Steuerbehörden übermittelt wurden, ändern können.  

    Wenn Sie das Feld leer lassen, müssen Benutzer stattdessen eine Korrektur-MwSt.-Erklärung erstellen.  

3.  Wählen Sie das Kontrollkästchen **Stornozeilen exportieren**, wenn Sie Informationen über Stornierungszeilen berücksichtigen wollen, wenn Sie Daten für den MwSt von EU-Verkäufen exportieren. Weitere Informationen finden Sie unter [Gewusst wie: MwSt korrigieren](how-to-correct-vat-reports.md)  
4.  Geben Sie im Inforegister **Nummerierung** die Nummernserie an, die für Standard-MwSt.-Erklärungen verwendet werden soll. Dieses ist standardmäßig die Seriennummer, die in beliebigen MwSt Berichten verwendet wird, die Sie erstellen.  

    Abhängig von den Anforderungen können Sie die gleichen Nummernserien für alle MwSt.-Erklärungen oder separate Nummernserien für jede Art von MwSt.-Erklärung verwenden.

    Wenn beispielsweise Ihre Unternehmen separate Nummernserien für Standard- und für Korrektur-MwSt.-Erklärungen verwendet, ist diese Nummernserie die Standardnummernserie. Benutzer können eine andere Nummernserie in **Nr.** auswählen Feld, wenn sie Korrekturberichte erstellen.  

5.  Im Inforegister **ZIVIT** können Sie Informationen für die Felder anzeigen.  
6.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [MwSt.-Abrechnung](vat-reporting.md)   
 [Erstellen von MwsT-Berichten.](how-to-create-vat-reports.md)
