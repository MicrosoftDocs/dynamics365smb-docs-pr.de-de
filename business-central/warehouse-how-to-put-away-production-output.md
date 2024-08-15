---
title: Einlagern der fertig gestellten Produktion
description: 'Dieser Artikel beschreibt, wie Sie Ihre Produktionsausgabe einlagern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.forms: '9326, 99000831, 9315, 7375'
---
# <a name="put-away-production-or-assembly-output"></a>Einlagerung der fertiggestellten Produktion oder Montage

Wie Sie Ihren Output aus der Produktion einlagern, hängt davon ab, wie Ihr Lagerort festgelegt ist. Weitere Informationen finden Sie unter [Einrichten von Warehouse Management](warehouse-setup-warehouse.md).  

Bei Basis-Lagerkonfigurationen, bei denen für den Lagerort die Bearbeitung der Einlagerung erforderlich ist, verwenden Sie den Beleg **Lagereinlagerung**, um die fertig gestellte Menge zu buchen oder um die Einlagerung der Fertigprodukte zu organisieren und zu erfassen.  

> [!NOTE]  
> Montageprozesse unterstützen keine Lagereinlagerungen. Sie buchen einen Montageauftrag, um die Ausgabe zu registrieren. Wenn Sie Lagerplätze verwenden, können Sie Elemente später zwischen Lagerplätzen verschieben. Weitere Informationen finden Sie unter [Ad-hoc-Umlagerung von Artikeln in Basis-Lagerkonfigurationen](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).  

Wenn für einen Lagerort in den erweiterten Lagerkonfigurationen die Bearbeitung der Einlagerung und des Wareneingangs erforderlich ist, können Sie entweder eine interne Einlagerungsanforderung oder eine Lagerplatzumlagerung erstellen, um die Fertigprodukte einzulagern.  

## <a name="to-put-away-production-output-with-an-inventory-put-away"></a>So lagern Sie fertiggestellte Artikel aus der Produktion mit einer Lagereinlagerung ein:

Der erste Schritt zur Einlagerung von Ausgabe ist das Erstellen der Lagereinlagerungsanforderung. Diese Anforderung informiert das Lager, dass die Fertigprodukte aus der Produktion oder der Montage des Fertigungsauftrags zur Einlagerung bereit sind.

### <a name="to-create-the-inbound-warehouse-request"></a>So erstellen Sie die Lagereinlagerungsanforderung:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Freigegebener Fertigungsauftrag** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Fertigungsauftrag, der für die Einlagerungen bereitsteht, und dann die Aktion **Eingehende Lageranf. erstellen** aus.  

> [!NOTE]  
> Sie können die Einlagerungsanforderung auch erstellen, indem Sie das Feld **Lagereinlag.-Anford. erstellen** aktivieren, wenn Sie den Fertigungsauftrag aktualisieren. Weitere Infromationen finden Sie unter [Aktualisieren oder Neugestalten von Fertigungsaufträgen](production-how-to-replan-refresh-production-orders.md).  

### <a name="to-put-away-output-with-an-inventory-put-away"></a>So lagern Sie Ausstoß mit einer Lagereinlagerung ein:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagereinlagerungen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Lagereinlagerung. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Um zu den Fertigungsaufträgen zu gelangen, wählen Sie die Aktion **Herkunftsbeleg holen** aus, und wählen Sie den freigegebenen Fertigungsauftrag aus.  
4. Füllen Sie die Einlagerungszeilen nach Bedarf aus.
5. Wenn die Zeilen zum Buchen bereit sind, wählen Sie die Aktion **Buchen** aus. Buchen erzeugt die Lagerplatzposten und bucht die Ausgabe der Artikel.  

    [!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

Sie können eine **Lagereinlagerung** auch direkt aus dem freigegebenen Fertigungsauftrag erstellen. Weitere Informationen finden Sie unter [Artikel mit Lagereinlagerungen einlagern](warehouse-how-to-put-items-away-with-inventory-put-aways.md).  

Wenn Sie eine Lagereinlagerung buchen, wird davon ausgegangen, dass alle Arbeitsgänge entsprechend dem Standardarbeitsplan gebucht werden. Das heißt, die Ausbringungsmenge wird entsprechend dem letzten Vorgang gebucht. Sie können das FA-Istmeldungs Buch verwenden, um Abweichungen der fertiggestellten Menge zu buchen und Einstellungen der Bearbeitungszeiten vorzunehmen. Wenn Sie Teilbuchungen vorzunehmen müssen, nachdem Sie die Lagereinlagerung erstellt haben, ist dies für Rüstzeiten und Mengen für alle Arbeitsgänge mit Ausnahme des letzten Arbeitsgangs möglich. Der letzten Arbeitsgang wird durch die Lagereinlagerung gesteuert.  

Wenn Sie nur die Bereitstellungszeit oder die Prozesszeit für den letzten Arbeitsgang buchen, legen Sie die fertig gestellte Menge für den letzten Arbeitsgang auf 0. Sie können auswählen, die letzte Zeile auch gar nicht zu buchen, indem Sie sie einfach löschen.

## <a name="to-put-away-assembly-and-production-output-in-advanced-warehouse-configurations"></a>Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration

Wenn Sie die Ausgabe des Produktions- oder Montageauftrags in einem Lager buchen, das gezielte Einlagerung und Kommissionierung verwendet, wird die Ausgabe in den im Produktions- oder Montageauftrag definierten Lagerplätze gelegt. Weitere Informationen über verschiedene Möglichkeiten, Artikel im Lager mit erweiterten Konfigurationen zu verschieben, finden Sie unter [Artikel in erweiterten Lagerkonfigurationen verschieben](warehouse-how-to-move-items-in-advanced-warehousing.md#to-move-items-with-the-warehouse-movement-worksheet).

> [!NOTE]  
> Sie können die Herkunftsbelegnummer, wie die Fertigungsauftragsnummer nicht in den Belegen für die interne Einlagerungsanforderung, Einlagerung oder Umlagerung für Montage- oder Fertigungsausgabeprozesse eingeben.  

## <a name="see-also"></a>Weitere Informationen

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
