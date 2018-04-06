---
title: 'Vorgehensweise: Einlagerung der fertiggestellten Produktion | Microsoft Docs'
description: "Wie Sie Ihre Fertigprodukte aus der Produktion einlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7918a962f3349c68cd7245e9b12f83975aee5ac
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="put-away-production-or-assembly-output"></a>Einlagerung der fertiggestellten Produktion oder Montage
Wie Sie Ihre Fertigprodukte aus der Produktion einlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

Bei Basis-Lagerkonfigurationen, bei denen für den Lagerort die Bearbeitung der Einlagerung erforderlich ist, jedoch nicht die des Wareneingangs, verwenden Sie den Beleg **Lagereinlagerung**, um die Einlagerung der Fertigprodukte zu organisieren und zu erfassen.  

Wenn für Ihren Lagerort in den Basis-Lagerkonfigurationen die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist, können Sie entweder eine interne Einlagerungsanforderung oder eine Lagerplatzumlagerung erstellen, um die Fertigprodukte einzulagern.  

Der erste Schritt zum Erstellen der Einlagerung ist das Erstellen der Lagereinlagerungsanforderung. Diese Anforderung informiert das Lager, dass die Fertigprodukte aus der Produktion oder der Montage des Fertigungsauftrags zur Einlagerung bereit sind.

## <a name="to-create-the-inbound-warehouse-request"></a>So erstellen Sie die Lagereinlagerungsanforderung:  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Freigegebener FA** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Fertigungsauftrag, der für die Einlagerungen bereitsteht, die Aktion **Eingehende Lageranf. erstellen** aus.  

> [!NOTE]  
>  Sie können die Einlagerungsanforderung auch erstellen, indem Sie das Kontrollkästchen **Lagereinlag.-Anford. erstellen** aktivieren, wenn Sie den Fertigungsauftrag aktualisieren. Weitere Informationen finden Sie unter [Aktualisieren oder ersetzen von Produktionsaufträgen.](production-how-to-replan-refresh-production-orders.md)  

## <a name="to-put-output-away-with-an-inventory-put-away"></a>So lagern Sie Ausstoß mit einer Lagereinlagerung ein:  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Einlagerung** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Erstellen Sie eine neue Lagereinlagerung. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Um zu den Fertigungsaufträgen zu gelangen, wählen Sie die Aktion **Herkunftsbeleg holen** aus, und wählen Sie den freigegebenen Fertigungsauftrag aus.  
4.  Füllen Sie die Einlagerungszeilen entsprechend aus.
5.  Wenn die Zeilen zum Buchen bereit sind, wählen Sie die Aktion **Buchen** aus. Das Buchen erzeugt die erforderlichen Lagerplatzposten und bucht die Istmeldung der Artikel.  

Sie können eine **Lagereinlagerung** auch direkt aus dem freigegebenen Fertigungsauftrag erstellen. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wenn Sie eine Lagereinlagerung buchen, wird davon ausgegangen, dass alle Arbeitsgänge entsprechend dem Standardarbeitsplan gebucht werden, dies bedeutet, dass die fertiggestellte Menge gemäß des letzten Arbeitsgangs gebucht wird. Sie können das FA-Istmeldungs Buch verwenden, um Abweichungen der fertiggestellten Menge zu buchen und Einstellungen der Bearbeitungszeiten vorzunehmen. Wenn es notwendig ist, Teilbuchungen vorzunehmen, nachdem Sie die Lagereinlagerung erstellt haben, ist dies für Rüstzeiten und Mengen für alle Arbeitsgänge mit Ausnahme des letzten Arbeitsgangs möglich. In diesem Fall wird der letzten Arbeitsgang durch die Lagereinlagerung gesteuert.  

Wenn Sie nur die Bereitstellungszeit oder die Prozesszeit für den letzten Arbeitsgang buchen, dann legen Sie die fertig gestellte Menge für den letzten Arbeitsgang auf 0. Alternativ können Sie auswählen, die letzte Zeile auch gar nicht zu buchen, indem Sie sie einfach löschen  

## <a name="to-put-output-away-with-a-warehouse-internal-put-away"></a>So lagern Sie Fertigerzeugnisse mithilfe der internen Einlagerungsanforderung ein:
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Interne Kommiss.-Anforderung** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie den Kopfbereich einer neuen internen Einlagerungsanforderung mindestens mit dem **Lagerortcode** aus.  
4. Tragen Sie für jeden Artikel, den Sie ins Lager einlagern möchten, eine Zeile ein. Sie müssen nur die Felder **Artikelnr.** und **Menge** ausfüllen.  

    > [!NOTE]  
    >  Wenn Sie das Feld **Artikelnr.** auswählen, wird die **Lagerplatzinhaltsübersicht** anstelle der **Artikelübersicht** angezeigt. Dies liegt daran, dass Sie einen Artikel einlagern möchten, der sich in einem bestimmten Lagerplatz befindet – einen Lagerplatzinhalt – und nicht nur einen Artikel. Außerdem wissen Sie bereits, aus welchem Lagerplatz der Artikel entnommen werden soll.  

4.  Um die Vorschlagszeilen mit dem gesamten oder dem gefilterten Lagerplatzinhalt der Lagerplätze des Lagerorts zu füllen, wählen Sie die Aktion **Lagerplatzinhalt abrufen** aus.  
5.  Wählen Sie die Aktion **Einlagerung erstellen** und die Artikel aus, die Sie aus der Produktion umlagern möchten, befinden sich jetzt in Einlagerungsanweisungen, deren Einlagerung Lager ansteht.  

> [!NOTE]  
>  Wenn Ihr Lagerort so eingerichtet wurde, dass er die gesteuerte Einlagerung und Kommissionierung verwendet, ist das Lager über die Vorgabelagerplätze der Produktion mit der Produktionsstätte verbunden: die Lagerplätze für die Fertigungsbereitstellung, den Fertigungsausgang sowie die offene Fertigungsbereitstellung, die Sie auf der Lagerortkarte im Inforegister **Lagerplätze** festlegen. Wenn Sie die Istmeldung eines Fertigungsauftrags buchen, werden die Fertigerzeugnisse automatisch in den **Fertigungsausgangslagerplatz** eingelagert. Sie gehen genauso vor, wie oben beschrieben, um die Fertigerzeugnisse einzulagern, außer dass Sie, anstatt den Vorgabelagerplatz des Artikels zu verwenden, die Artikel aus dem **Fertigungsausgangslagerplatz** in den Vorgabelagerplatz des Artikels umlagern oder einlagern.  

## <a name="to-manually-specify-a-bin-to-store-items-from-production-output"></a>Um manuell einen Lagerplatz festzulegen, in dem fertiggestellte Artikel aus der Produktion eingelagert werden sollen  
1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplatzumlagerungsvorschlag** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Füllen Sie den Kopf aus, und erstellen Sie eine Zeile für jeden Artikel, den Sie im Lager einlagern möchten.  
3.  Füllen Sie die beiden Felder **Von Lagerplatzcode** und **Nach Lagerplatzcode** aus und geben Sie die Menge in das Feld **Menge** ein.  
4.  Um die Vorschlagszeilen mit dem gesamten oder dem gefilterten Lagerplatzinhalt der Lagerplätze des Lagerorts zu füllen, wählen Sie die Aktion **Lagerplatzinhalt abrufen** aus.  
5. Wählen Sie die Aktion **Lagerplatzumlagerung erstellen** aus. Die Lagerplatzumlagerungsanweisung werden mit Zeilen der Art "Entnahme" und "Einlagerung" erstellt, die von Lagermitarbeitern ausgeführt werden können.  

> [!NOTE]  
>  Sie können die Herkunftsbelegnummer, wie die Fertigungsauftragsnummer für keine dieser Prozeduren in die interne Einlagerungsanforderung, Einlagerung oder Lagerplatzumlagerung eingeben.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

