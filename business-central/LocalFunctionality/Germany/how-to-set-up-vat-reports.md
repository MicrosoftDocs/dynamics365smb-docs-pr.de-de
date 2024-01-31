---
title: 'So legen Sie MwSt.-Berichte fest [DE]'
description: 'Um einen MwSt-Bericht unter dem System ELMA5 von Business Central einzurichten, müssen Sie die Parameter melden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Festlegen von MwSt.-Berichten in der deutschen Version
Informationen aus verschiedenen Rechnungstypen werden verwendet, um Daten in den Ausfuhr-Listenbericht EU zu speisen. Um einen MwSt-Bericht unter dem System ELMA5 von [!INCLUDE[prod_short](../../includes/prod_short.md)] einzurichten, müssen Sie die Parameter melden.  

## So richten Sie einen MwSt-Bericht ein  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **MWSt.-Berichtseinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie im Inforegister **Allgemein** das Feld **Übermittelte Berichte bearbeiten** aus, damit Benutzer MwSt.-Erklärungen, die an die Steuerbehörden übermittelt wurden, ändern können.  

    Wenn Sie das Feld leer lassen, müssen Benutzer stattdessen eine Korrektur-MwSt.-Erklärung erstellen.  

3.  Wählen Sie das Kontrollkästchen **Stornozeilen exportieren**, wenn Sie Informationen über Stornierungszeilen berücksichtigen wollen, wenn Sie Daten für den MwSt von EU-Verkäufen exportieren. Weitere Informationen finden Sie unter [Gewusst wie: MwSt korrigieren](how-to-correct-vat-reports.md)  
4.  Geben Sie im Inforegister **Nummerierung** die Nummernserie an, die für Standard-MwSt.-Erklärungen verwendet werden soll. Dieses ist standardmäßig die Seriennummer, die in beliebigen MwSt Berichten verwendet wird, die Sie erstellen.  

    Abhängig von den Anforderungen können Sie die gleichen Nummernserien für alle MwSt.-Erklärungen oder separate Nummernserien für jede Art von MwSt.-Erklärung verwenden.

    Wenn beispielsweise Ihre Unternehmen separate Nummernserien für Standard- und für Korrektur-MwSt.-Erklärungen verwendet, ist diese Nummernserie die Standardnummernserie. Benutzer können eine andere Nummernserie in **Nr.** auswählen Feld, wenn sie Korrekturberichte erstellen.  

5.  Im Inforegister **ZIVIT** können Sie Informationen für die Felder anzeigen.  
6.  Wählen Sie die Schaltfläche **OK** aus.  

## Siehe auch  
 [MwSt.-Abrechnung](vat-reporting.md)   
 [Erstellen von MwsT-Berichten](how-to-create-vat-reports.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]