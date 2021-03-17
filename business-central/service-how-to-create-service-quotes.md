---
title: So erstellen Sie Serviceangebote | Microsoft Docs
description: Sie können die Seite **Serviceangebot** verwenden, um Belege zu erstellen, in die Sie Informationen über den Service (Reparatur und Wartung) von Serviceartikeln auf Debitorenanfrage eingeben. Serviceangebote können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann vom Angebot in einen Auftrag umgewandelt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 92c93b2e0b876920f1c259d31b4d839a5b2ecbc0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388799"
---
# <a name="create-service-quotes"></a>Serviceangebote erstellen
Sie können an Serviceangebote als Basis für Serviceaufträge denken. Tatsächlich sind sie fast identisch. Sie enthalten sowohl die Serviceartikelbeschreibung, wie der Debitor, die Art des Auftrags, den Artikel, für den Service, Gebührenzählung und benötigte Versandinformationen, und die Informationen über die tatsächliche Dienstarbeit.
 
Serviceangebote können als Vorentwürfe von Serviceaufträgen betrachtet werden, die dann vom Angebot in einen Auftrag umgewandelt werden.  
  
## <a name="to-create-a-service-quote"></a>So erstellen Sie ein Serviceangebot  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceangebote** ein und wählen Sie dann den entsprechenden Link.  
2. Erstellen Sie ein neues Serviceangebot.  
3. Geben Sie im Feld **Nr.** eine Nummer für das Serviceangebot ein. Wenn Sie Nummernserien für Serviceangebote auf der Seite **Service Einrichtung** definiert haben, drücken Sie die Eingabetaste, um die nächste verfügbare Serviceangebotsnummer auszuwählen.  
4. Klicken Sie im Feld **Debitorennr.**  Feld wählen Sie den relevanten Debitoren aus der Liste.  

  > [!Note]  
  >  Die Debitorenfelder werden automatisch mit Informationen aus der Karte **Debitor** gefüllt. Wenn keine **Debitor**-Karte für den Debitor vorhanden ist und Sie eine Debitorenvorlage eingerichtet haben, können Sie aus dem Serviceangebot heraus einen Debitor erstellen. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **Debitor erstellen** aus.  
  
5. Abhängig von den Einstellungen auf dem Inforegister **Pflichtfelder** auf der Seite **Service Einrichtung** muss das Feld **Serviceauftragsart** auf dem Inforegister **Verkäufercode** ausgefüllt werden.  
6. Füllen Sie die Serviceartikelzeilen aus.  
7. Erfassen Sie die geschätzten Kosten in den Servicezeilen.  
  
## <a name="see-also"></a>Siehe auch  
[Erstellen von Serviceaufträgen](service-how-to-create-service-orders.md)  
[Mit Serviceaufgaben arbeiten](service-how-to-work-on-service-tasks.md)  

 

[!INCLUDE[footer-include](includes/footer-banner.md)]