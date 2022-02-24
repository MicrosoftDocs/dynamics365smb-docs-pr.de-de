---
title: 'Vorgehensweise: Verwenden der Fertigungsloseinheit | Microsoft Docs'
description: Wenn ein Artikel in einer Einheit am Lager geführt, aber in einer anderen Einheit gefertigt wird, kann ein Fertigungsauftrag erstellt werden, für den eine Fertigungsloseinheit verwendet wird, um in der Stapelverarbeitung FA berechnen die richtige Menge der Komponenten zu berechnen. Ein Beispiel für eine Berechnung über eine Fertigungsloseinheit ergibt sich, wenn ein Produktionsartikel am Lager in Einheiten geführt, aber in Tonnen gefertigt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 550a7ff11dc63f35326f5daabfe0d25d928c86d7
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877735"
---
# <a name="work-with-manufacturing-batch-units-of-measure"></a>Verwenden der Fertigungsloseinheit
Wenn ein Artikel in einer Einheit am Lager geführt, aber in einer anderen Einheit gefertigt wird, wird ein Fertigungsauftrag erstellt, für den eine Fertigungsloseinheit verwendet wird, um in der Stapelverarbeitung **Herstellungsantrag erneuern** die richtige Menge der Komponenten zu berechnen. Ein Beispiel für eine Berechnung über eine Fertigungsloseinheit ergibt sich, wenn ein Produktionsartikel am Lager in Einheiten geführt, aber in Tonnen gefertigt wird.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Eine Fertigungsstückliste mit eine Fertigungsloseinheit erstellen  
1.  Die Fertigungsloseinheit wird für den zu fertigenden Artikel auf der Seite **Artikeleinheiten als alternative Einheit** eingerichtet. Die Fertigungsloseinheit ersetzt nicht die Basiseinheit für den Artikel.  
2.  Erstellen Sie eine Fertigungsstückliste für den Artikel, die mit der Fertigungsloseinheit eingerichtet wird. Weitere Informationen finden Sie unter [Erstellen von Montagestücklisten](production-how-to-create-production-boms.md).  
3.  Wählen Sie im Feld **Basiseinheitencode** die Fertigungsloseinheit aus.  
4.  Geben Sie für jede Zeile der Fertigungsstückliste in das Feld **Komponentenmenge** die Menge dieses Komponentenartikels ein, die zum Erstellen dieser Fertigungsloseinheit erforderlich ist.  
5.  Öffnen Sie die **Artikelkarte** des zugehörigen Artikels.  

    Wählen Sie im Inforegister **Beschaffung** im Feld **Fert.-Stücklistennr.** die oben erstellte Fertigungsstückliste aus.  
6.  Erstellen Sie einen Fertigungsauftragskopf mit dem Artikel, der mit der Fertigungsloseinheit eingerichtet wurde. Weitere Informationen finden Sie unter [Erstellen von Montageaufträgen](production-how-to-create-production-orders.md).  
7.  Wählen Sie die Schaltfläche **Aktualisieren**, und wählen Sie dann die Schaltfläche **OK**.  

Wählen Sie im Inforegister **Zeilen** **Aktionen**, und wählen Sie Zeile, und dann **Komponenten**, um das Ergebnis anzuzeigen. Die Anwendungberechnet die richtige Menge der Komponenten, die für die Fertigungsstückliste gemäß der Fertigungsloseinheit erforderlich ist.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Fertigungsloseinheit in einem Fertigungsauftrag berechnen  
1.  Erstellen Sie einen Fertigungsauftragskopf mit dem Artikel, der mit der Fertigungsloseinheit eingerichtet wurde.  
2.  Geben Sie in der Zeile des Fertigungsauftrags in das Feld **Artikelnr.** die Artikelnummer eine, die im Kopf steht.  
3.  Geben Sie in das Feld **Menge** die Menge ein, die im Kopf steht.  
4.  Wählen Sie im Feld **Basiseinheitencode** den Fertigungsloseinheitencode aus.  
5.  Wählen Sie die Aktion **Aktualisieren** aus.
6.  Deaktivieren Sie auf dem Inforegister **Berechnen** das Feld Kontrollkästchen **Zeilen**.  
7.  Wählen Sie die Schaltfläche **OK** aus.  
8.  Wählen Sie im Inforegister **Zeilen** **Aktionen**, und wählen Sie Zeile, und dann **Komponenten**, um das Ergebnis anzuzeigen. Die richtige Menge der Komponenten, die für die Fertigungsstückliste gemäß der Fertigungsloseinheit erforderlich ist, wird berechnet.  

## <a name="see-also"></a>Siehe auch  
[Routings erstellen](production-how-to-create-routings.md)  
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)     
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planung](production-planning.md)   
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
