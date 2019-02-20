---
title: "Gewusst wie: Buchen von Inventuraufträgen"
description: "Nach Fertigstellen eines Inventurauftrags und Ändern des Status in Beendet kann er gebucht werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 1acac32a417f794801da50c866db2643ea0a4c2d
ms.openlocfilehash: 9aa3d69d41a4f8667499908d5a8b3a48f7e1cb44
ms.contentlocale: de-de
ms.lasthandoff: 01/22/2019

---
# <a name="post-physical-inventory-orders"></a>So buchen Sie Inventuraufträge
Nach Fertigstellen eines Inventurauftrags und Ändern des Status in **Beendet** kann er gebucht werden.  

Der Status eines Inventurauftrags kann unter folgenden Voraussetzungen auf **Beendet** festgelegt werden:  

- Alle zugehörigen Inventurerfassungen weisen den Status **Beendet** auf.  
- Jede Inventurauftragszeile wurde in mindestens einer Inventurerfassungszeile erfasst.  
- Die Kontrollkästchen **In Erfassungszeilen enthalten** und **Berechnete erw. Menge** wurden für alle Inventurauftragszeilen aktiviert.  

Nach dem Buchen des Auftrags können die gebuchten Inventuraufträge angezeigt werden. Gebuchte Lagerbelege bieten einen vollständigen Überblick über den Inventurprozess.  

## <a name="to-post-a-physical-inventory-order"></a>So buchen Sie einen Inventurauftrag  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie den Inventurauftrag aus, den Sie fertig stellen möchten, klicken Sie auf **Bearbeiten**.  

    Auf der Seite **Inventurauftrag** kann die Menge angezeigt werden, die nach Ausführung der Inventur im Feld **Erfasste Menge (Basis)** erfasst wurde.  

3.  Wählen Sie die Schaltfläche **Fertigstellung** aus.  
4.  Wählen Sie die Schaltfläche **Ja** aus. Der Wert im Feld **Status** wird in **Beendet** geändert.  

    > [!NOTE]  
    >  Eine Änderung des Inventurauftragskopfs oder der Inventurauftragszeilen ist nicht möglich.  

5.  Wählen Sie die zu buchenden Zeilen aus, und wählen Sie dann die Aktion **Buchen** und dann **OK** aus.  

## <a name="to-view-posted-physical-inventory-orders"></a>So zeigen Sie gebuchte Inventuraufträge an  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventur durchführen** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie auf der Seite **Gebuchter Inventurauftrag** den gebuchten Inventurauftrag aus, den Sie anzeigen möchten, klicken Sie auf Aktionen und anschließend auf **Ansicht**.  
3.  Um einer Liste zugehörige Inventurerfassungen anzuzeigen, wählen Sie die Aktion **Erfassungen** aus.  

    Sie können auch einen Bericht ausführen, in dem die Differenz zwischen der erwarteten Menge und der erfassten Menge zurückgegeben wird.  

4.  Schließen Sie die Seite.  

## <a name="see-also"></a>Siehe auch  
 [Inventurbelege](physical-inventory-documents.md)   
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)

