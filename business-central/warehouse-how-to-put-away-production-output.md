---
title: Einlagern der fertig gestellten Produktion
description: Wie Sie Ihre Fertigprodukte aus der Produktion einlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2b04e07a6660ebeb32cc93594c77b8ff8e782766
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784217"
---
# <a name="put-away-production-or-assembly-output"></a>Einlagerung der fertiggestellten Produktion oder Montage

Wie Sie Ihre Fertigprodukte aus der Produktion einlagern, hängt davon ab, wie Ihr Lagerort eingerichtet wurde. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

Bei Basis-Lagerkonfigurationen, bei denen für den Lagerort die Bearbeitung der Einlagerung erforderlich ist, verwenden Sie den Beleg **Lagereinlagerung**, um die fertig gestellte Menge zu buchen oder um die Einlagerung der Fertigprodukte zu organisieren und zu erfassen.  

> [!NOTE]  
> Lagereinlagerung wird für Montageprozesse nicht unterstützt. Sie buchen einen Montageauftrag, um die Ausgabe zu registrieren. Wenn Sie Behälter verwenden, können Sie Elemente später zwischen Behältern verschieben. Weitere Informationen finden Sie unter [Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Wenn für Ihren Lagerort in den Basis-Lagerkonfigurationen die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist, können Sie entweder eine interne Einlagerungsanforderung oder eine Lagerplatzumlagerung erstellen, um die Fertigprodukte einzulagern.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>So lagern Sie fertiggestellte Artikel aus der Produktion mit einer Lagereinlagerung ein:

Der erste Schritt zum Erstellen der Einlagerung ist das Erstellen der Lagereinlagerungsanforderung. Diese Anforderung informiert das Lager, dass die Fertigprodukte aus der Produktion oder der Montage des Fertigungsauftrags zur Einlagerung bereit sind.

### <a name="to-create-the-inbound-warehouse-request"></a>So erstellen Sie die Lagereinlagerungsanforderung:  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Freigegebener FA** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie im Fertigungsauftrag, der für die Einlagerungen bereitsteht, die Aktion **Eingehende Lageranf. erstellen** aus.  

> [!NOTE]  
> Sie können die Einlagerungsanforderung auch erstellen, indem Sie das Feld **Lagereinlag.-Anford. erstellen** aktivieren, wenn Sie den Fertigungsauftrag aktualisieren. Weitere Informationen finden Sie unter [Aktualisieren oder Ersetzen von Fertigungsaufträgen](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-output-away-with-an-inventory-put-away"></a>So lagern Sie Ausstoß mit einer Lagereinlagerung ein:  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Lagereinlagerung** ein, und wählen Sie dann den zugehörigen Link.  
2.  Erstellen Sie eine neue Lagereinlagerung. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3.  Um zu den Fertigungsaufträgen zu gelangen, wählen Sie die Aktion **Herkunftsbeleg holen** aus, und wählen Sie den freigegebenen Fertigungsauftrag aus.  
4.  Füllen Sie die Einlagerungszeilen entsprechend aus.
5.  Wenn die Zeilen zum Buchen bereit sind, wählen Sie die Aktion **Buchen** aus. Das Buchen erzeugt die erforderlichen Lagerplatzposten und bucht die Istmeldung der Artikel.  

Sie können eine **Lagereinlagerung** auch direkt aus dem freigegebenen Fertigungsauftrag erstellen. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wenn Sie eine Lagereinlagerung buchen, wird davon ausgegangen, dass alle Arbeitsgänge entsprechend dem Standardarbeitsplan gebucht werden, dies bedeutet, dass die fertiggestellte Menge gemäß des letzten Arbeitsgangs gebucht wird. Sie können das FA-Istmeldungs Buch verwenden, um Abweichungen der fertiggestellten Menge zu buchen und Einstellungen der Bearbeitungszeiten vorzunehmen. Wenn es notwendig ist, Teilbuchungen vorzunehmen, nachdem Sie die Lagereinlagerung erstellt haben, ist dies für Rüstzeiten und Mengen für alle Arbeitsgänge mit Ausnahme des letzten Arbeitsgangs möglich. In diesem Fall wird der letzten Arbeitsgang durch die Lagereinlagerung gesteuert.  

Wenn Sie nur die Bereitstellungszeit oder die Prozesszeit für den letzten Arbeitsgang buchen, dann legen Sie die fertig gestellte Menge für den letzten Arbeitsgang auf 0. Alternativ können Sie auswählen, die letzte Zeile auch gar nicht zu buchen, indem Sie sie einfach löschen  

## <a name="to-put-assembly-and-production-output-away-in-advanced-warehouse-configurations"></a>Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration
Wenn Sie die Ausgabe des Produktions- oder Montageauftrags in dem Lager buchen, das für die gezielte Einlagerung und Kommissionierung eingerichtet ist, wird die Ausgabe in den im Produktions- oder Montageauftrag definierten Behälter gelegt. 

In der folgenden Tabelle werden verschiedene Möglichkeiten zum Verschieben von Artikeln innerhalb des Lagers mit erweiterten Konfigurationen beschrieben, bei denen alle Lageraktivitäten in einem gerichteten Workflow ausgeführt werden müssen. 

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Artikel mit dem Lagerplatzumlagerungsarbeitsblatt umlagern.|[Umlagerung von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet)|  
|Erstellen einer internen interne Einlag.-Anforderung zur Lagerung produzierter oder montierter Artikel in einer grundlegenden oder erweiterten Lagerkonfiguration.|[Erstellen einer interne Einlag.-Anforderung](warehouse-how-to-create-put-aways-from-internal-put-aways.md#to-create-an-internal-put-away)|

> [!NOTE]  
> Sie können die Herkunftsbelegnummer, wie die Fertigungsauftragsnummer für keine dieser Prozeduren in die interne Einlagerungsanforderung, Einlagerung oder Lagerplatzumlagerung eingeben.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
