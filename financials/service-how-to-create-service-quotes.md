---
title: So erstellen Sie Serviceangebote | Microsoft Docs
description: "Sie können das Fenster **Serviceangebot** verwenden, um Belege zu erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Kundenanfrage eingeben. Serviceangebote können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann vom Angebot in einen Auftrag umgewandelt werden."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d5348e7b15eb0337f2a5f829c871dadcf3133b86
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-service-quotes"></a>Vorgehensweise: Erstellen von Serviceangeboten
Sie können an Serviceangebote als Basis für Serviceaufträge denken. Tatsächlich sind sie fast identisch. Sie enthalten sowohl die Serviceartikelbeschreibung, wie der Debitor, die Art des Auftrags, den Artikel, für den Service, Gebührenzählung und benötigte Versandinformationen, und die Informationen über die tatsächliche Dienstarbeit.
 
Serviceangebote können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann vom Angebot in einen Auftrag umgewandelt werden.  
  
## <a name="to-create-a-service-quote"></a>So erstellen Sie ein Serviceangebot  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceangebote** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Erstellen Sie ein neues Serviceangebot.  
3. Geben Sie im Feld **Nr.** eine Nummer für das Serviceangebot ein. Wenn Sie Nummernserien für Serviceangebote im Fenster **Service Einrichtung** definiert haben, drücken Sie die Eingabetaste, um die nächste verfügbare Serviceangebotsnummer auszuwählen.  
4. Klicken Sie im Feld **Debitorennr.**  Feld wählen Sie den relevanten Debitoren aus der Liste.  

  > [!Note]  
  >  Die Debitorenfelder werden automatisch mit Informationen aus der Karte **Debitor** gefüllt. Wenn keine **Debitor**-Karte für den Debitor vorhanden ist und Sie eine Debitorenvorlage eingerichtet haben, können Sie aus dem Serviceangebot heraus einen Debitor erstellen. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **Kunde erstellen** aus.  
  
5. Abhängig von den Einstellungen auf dem Inforegister **Pflichtfelder** im Fenster  **Service Einrichtung** muss das Feld **Serviceauftragsart** auf dem Inforegister **Verkäufercode** ausgefüllt werden.  
6. Füllen Sie die Serviceartikelzeilen aus.  
7. Erfassen Sie die geschätzten Kosten in den Servicezeilen.  
  
## <a name="see-also"></a>Siehe auch  
[Vorgehensweise: Erstellen von Serviceaufträgen](service-how-to-create-service-orders.md)  
[Vorgehensweise: Bearbeiten von Serviceaufgaben](service-how-to-work-on-service-tasks.md)  

 
