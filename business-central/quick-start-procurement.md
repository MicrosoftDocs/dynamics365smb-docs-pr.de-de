---
title: Beschaffung Schnellstart (enthält Video)
description: Erfahren Sie, wie Sie die ersten wichtigen Felder über Kreditor in Business Central ausfüllen, damit Sie mit dem Kauf von Produkten und Dienstleistungen beginnen können.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 7d0b33b668bede3ac1a1a7b8bd981693c54cd4b7
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940001"
---
# <a name="procurement-quick-start"></a>Schnellstart Beschaffung

Um Produkte und Dienstleistungen kaufen zu können, müssen Sie zunächst Lieferanten festlegen. Sobald dies geschehen ist, können Sie mit der Registrierung von Bestellungen und dem Erhalt von Rechnungen beginnen.  

## <a name="set-up-vendors"></a>Kreditor festlegen

Das folgende Video zeigt Ihnen, wie Sie unter [!INCLUDE[prod_short](includes/prod_short.md)] einen Kreditor festlegen.

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### <a name="set-up-a-new-vendor"></a>Einrichten eines neuen Kreditors

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Weitere Informationen und zusätzliche Dinge, die Sie bei der Registrierung von Kreditoren tun können, finden Sie unter [Neue Kreditoren registrieren](purchasing-how-register-new-vendors.md).  

## <a name="create-new-purchase-orders"></a>Neue Bestellungen erstellen

Wenn Sie etwas von einem Kreditor kaufen, haben Sie zwei Möglichkeiten. Die erste und einfachste ist, einfach eine Einkaufsrechnung zu erstellen. Sie müssen jedoch Bestellungen verwenden, wenn Ihr Einkaufsprozess erfordert, dass Sie einen teilweisen Eingang einer Bestellmenge erfassen, z.B. weil die volle Menge beim Einkäufer nicht verfügbar war.

Das folgende Video zeigt Ihnen, wie Sie eine Bestellung in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-order"></a>So erstellen Sie eine Bestellung  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten"). Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  

2. Wählen Sie auf der Seite **Einkaufsbestellungen** die Aktion **Neu**, um eine neue Bestellung zu erstellen.

3. Geben Sie in das Feld **Kreditorenname** den Namen eines vorhandenen Kreditors ein.

    Die anderen Felder auf der Seite **Einkaufskopf** sind nun mit den Standardinformationen über den ausgewählten Kreditor gefüllt.  

4. Füllen Sie die übrigen Felder auf der Seite **Bestellung** nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Sie können nun die Zeilen der Bestellung mit den Artikeln oder Ressourcen ausfüllen, die Sie vom Kreditor gekauft haben.

5. Geben Sie auf der Seite **Zeilen** Inforegister in das Feld **Positionsnummer** die Nummer eines Bestandsartikels oder einer Dienstleistung ein.

6. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der eingekauft wird.

    Das Feld **Zeilenmenge** wird aktualisiert, um den Wert im Feld **EK-Preis** multipliziert ist mit dem Wert im Feld **Menge** anzuzeigen.

7. Geben Sie in das Feld **Bestellrabattbetrag** einen Betrag ein, der von dem Wert abgezogen werden soll, der im Feld **Gesamtbetrag inkl. MwSt.** am Ende der Bestellung angezeigt wird.

8. Falls Sie die eingekauften Artikel oder Dienstleistungen erhalten, wählen Sie aus **Buchen**.

Weitere Informationen und zusätzliche Möglichkeiten, die Sie beim Erstellen einer Bestellung haben, finden Sie unter [Einkauf](purchasing-manage-purchasing.md).  

## <a name="create-a-purchase-invoice"></a>Erstellen Sie eine Einkaufsrechnung  

Sie erstellen eine Einkaufsrechnung, um die Kosten der Käufe zu erfassen und die Verbindlichkeiten a. LL zu verfolgen. Das Erstellen einer Einkaufsrechnung ist ähnlich wie das Erstellen einer Bestellung.

### <a name="how-to-create-and-post-a-purchase-invoice"></a>So erstellen und buchen Sie eine Einkaufsrechnung  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Einkaufsrechnung** die Aktion **Neu**, um eine neue Einkaufsrechnung zu erstellen.
3. Geben Sie im Feld **Kreditor** den Namen eines vorhandenen Kreditors ein.

    Andere Felder auf der Seite **Einkaufsrechnung** werden nun mit den Standardinformationen vom ausgewählten Kreditor ausgefüllt.

4. Füllen Sie auf der Seite **Einkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Sie sind nun bereit, die Einkaufsrechnungszeilen mit Artikeln oder Ressourcen auszufüllen, die Sie vom Lieferanten gekauft haben.

5. Geben Sie auf der Seite **Zeilen** Inforegister in das Feld **Positionsnummer** die Nummer eines Bestandsartikels oder einer Dienstleistung ein.
6. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der eingekauft wird.

    Das Feld **Zeilenbetrag** wird aktualisiert und zeigt den Wert im Feld **Direkte Kosten pro Einheit** multipliziert mit dem Wert im Feld **Menge**.

7. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

8. Wenn Sie die gekauften Artikel oder Dienstleistungen erhalten, wählen Sie **Buchen**.

Der Kauf wird nun im Bestand, in den Ressourcen-Sachkonten und in den Finanzdokument widergespiegelt, und die Kreditorenzahlung wird aktiviert. Die Einkaufsrechnung wird in der Liste der gebuchten Einkaufsrechnungen entfernt und durch einen neuen Beleg in der Liste der gebuchten Einkaufsrechnungen ersetzt.  

Weitere Informationen und zusätzliche Möglichkeiten beim Erstellen einer Einkaufsrechnung finden Sie unter [Einkäufe mit Einkaufsrechnungen erstellen](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Weitere Informationen

[Business Central Schnellstarts](quick-start-business-central.md)  
[Einkaufsübersicht](Purchasing-manage-purchasing.md)  
[Einkäufe mit Einkaufsrechnungen erfassen](purchasing-how-record-purchases.md)  
