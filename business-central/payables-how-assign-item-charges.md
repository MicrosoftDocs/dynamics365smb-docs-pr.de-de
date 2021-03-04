---
title: Zuordnen von Artikelzu-/-abschlägen zu Einkäufen oder Verkäufen| Microsoft Docs
description: Wenn Sie Ihren Lagerartikel Kosten wie Fracht, Versicherung, Umlagerung und Transport hinzufügen möchten, die beim Kauf oder Verkauf entstehen, können Sie die Artikelgebührenfunktion verwenden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost, landed cost
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bd6392753b41ac080fd0933f9f3a55ddc17a2a54
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759617"
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Verwenden von Artikelzuschlägen für zusätzliche Kosten
Um eine korrekte Bewertung sicherzustellen, müssen Ihre Lagerartikel Kosten wie Fracht, Versicherung, Umlagerung und Transport enthalten, die beim Kauf oder Verkauf entstehen. Die Kosten eines eingekauften Artikels bestehen aus dem Einkaufspreis des Kreditors und allen zusätzlichen Artikelzuschlägen, die einzelnen Wareneingängen oder Rücklieferungen zugewiesen werden können. Die Frachtkosten der verkauften Artikel zu kennen, kann für Ihr Unternehmen genauso wichtig sein wie die Einkaufspreise der eingekauften Artikel zu kennen.

Zusätzlich zum Aufzeichnen der hinzugefügten Kosten zum Lagerwert, können Sie die Funktion Artikelzuschlag wie folgt verwenden:

- Die Identifizierung der Gesamtkosten eines Artikels, um bessere Entscheidungen bezüglich der Optimierung des Vertriebsnetzes zu treffen.
- Die Analyse der Zusammensetzung eines Verkaufspreises/Einstandspreises eines Artikels.
- Die Einberechnung von Einkaufsrabatten in den Einstandspreis und von Verkaufsrabatten in den Verkaufspreis.

Bevor Sie Artikeln Gebühren zuweisen können, müssen Sie Artikelchargennummern für unterschiedliche Artikelarten zuweisen, inklusive Sachkontokosten, die mit Verkäufen, Einkäufen und Lagerregulierungen verknüpft sind. Eine Artikelzuschlagsnummer enthält eine Kombination von Produktbuchungsgruppe, Steuergruppencode, MwSt.-Produktbuchungsgruppe und Artikelzuschlag. Wenn Sie die Nummer des Artikel Zu-/Abschlags in einen Einkaufs- oder Verkaufsbeleg eingeben, ermittelt die Anwendung ein Sachkonto auf der Basis der Einrichtung des Artikel Zu-/Abschlags und der Informationen im jeweiligen Beleg.

Für Bestellungen und Verkaufsbelege können Artikelzuschläge auf zwei Arten zugeordnet werden:
- Auf dem Beleg, auf dem der Artikel aufgeführt ist, auf den sich der Artikelzuschlag bezieht. Dies ist in der Regel für Belege der Fall, die noch nicht vollständig gebucht sind.
- Auf einer getrennten Rechnung, indem Sie den Artikelzuschhlag mit einem gebuchten Beleg oder einer Lieferung verknüpfen, in denen der Artikel vorkommt, zu dem der Artikelzuschlag gehört.

> [!NOTE]  
>   Sie können Artikelzuschläge in Bestellungen, Rechnungen und Gutschriften für Verkaufs- und Einkaufsberichte zuweisen. Die folgenden Verfahren beschreiben, wie man mit Artikelzuschlägen für eine Einkaufsrechnung arbeitet. Die Schritte sind für alle anderen Einkaufs- und Verkaufsbelege ähnlich.

## <a name="example"></a>Beispiel
In diesem Video wird gezeigt, wie Sie im Rahmen der Lagerkostenberechnung mit zusätzlichen Lieferkosten umgehen.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Vorgehensweise: Eine Artikelzu-/-abschlagsnummer einrichten
Sie können die Artikel Zu-/Abschlagsnummern verwenden, um die verschiedenen Arten von Artikel Zu-/Abschlägen, die in Ihrem Unternehmen verwendet werden, zu verwalten.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel Zu-/Abschläge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Artikel-Gebühren** die Aktion **Neu** aus, um eine neue Zeile für eine zu erstellen.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Um einen Artikel Zu-/Abschlag in die Einkaufsrechnung für den Artikel zuordnen
Wenn Sie den Artikel-Zu-/Abschlag kennen, und den Zeitpunkt Sie eine Einkaufsrechnung für den Artikel betreffen, gehen Sie folgendermaßen vor.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kaufrechnungen** ein und wählen Sie dann den entsprechenden Link.
2. Eine neue Einkaufsrechnung erstellen. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
3. Stellen Sie sicher, dass die Einkaufsrechnung eine oder mehrere Zeilen vom Artikeltyp hat.
4. Geben Sie eine neue Zeile ein, und wählen Sie **Zu-/Abschlag (Artikel)** im Feld **Art**.
5. Geben Sie in dem Feld **Menge** die Anzahl der Einheiten dieses Artikel Zu-/Abschlages ein, für die Sie eine Rechnung erhalten haben.
6. Geben Sie in dem Feld **EK-Preis** den Betrag der Artikelgebühr an.
7. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    In den folgenden Schritten führen Sie die aktuelle Zuordnung aus. Bis die Artikelgebühr vollständig zugewiesen wird, wird der Wert im Feld **Menge zuordnen** in roter Schrift angezeigt..
8. Klicken Sie auf dem Inforegister **Zeilen** auf Aktionen **Artikelgebühr-Zuweisung**.

    Die Seite **Artikel Zu-/Abschlagszuweisung** öffnet sich und zeigt eine Zeile für jede Zeile der Art in der Einkaufsrechnung. Um den Artikel Zu-/Abschlag in einen oder mehreren Verkaufsrechnungszeilen zuzuweisen, können Sie eine Funktion verwenden die es für Sie zugewiesen und verteilt oder Sie das **Menge. zuordnen** Feld manuell ausfüllen können. Die folgenden Schritte beschreiben, wie Vorschlagungs-ArtikelZu-/Abschlags-Zuweisungsfunktion verwendet.

9. Auf der Seite **Artikel Zu-/Abschlagszuweisung** wählen Sie die **Artikel Zu-/Abschlagszuweisung vorschlagen** Aktion aus.
10. Wenn es mehr Rechnungszeilen als eine Art des Artikels gibt, wählen Sie eine der vier Verteilungsoptionen aus.  

Bis die Artikelgebühr vollständig zugewiesen wird, wird der Wert im Feld **Menge zuordnen** in roter Schrift angezeigt..

Der Artikelzuschlag wird nun der Einkaufsrechnung zugeordnet. Wenn Sie den Wareneingang der Einkaufsrechnung buchen, werden die Lagerwerte der Artikel mit den Kosten für Artikelzu-/-abschläge aktualisiert.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Um einen Artikel Zu-/Abschlag in die Einkaufsrechnung für den Artikel zuordnen
Wenn Sie eine Rechnung für die Zu-/Abschläge erhalten, nachdem Sie den Wareneingang der ursprünglichen Einkaufsrechnung wurde, gehen Sie folgendermaßen vor.
1. Wiederholen Sie die Schritte 1 bis 8 unter [Um einen Artikel Zu-/Abschlag in die Einkaufsrechnung für den Artikel zuordnen](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Klicken Sie auf der Seite **Artikel Zu-/Abschlagszuweisung** auf die Aktion **Rücksendungszeilen holen**.
3. Auf der Seite **Einkauf Lieferzeilen** wählen Sie die Zeile Geb. Einkaufslieferung für den Artikel, dem Sie den Artikel Zu-/Abschlag zuordnen möchten, und wählen Sie dann die Schaltfläche **OK** aus.
4. Wählen Sie die **Artikel Zu-/Abschlagszuweisung vorschlagen** Aktion aus.

Artikelzu-/Abschläge der separaten Einkaufsrechnung wird jetzt dem Artikel in der gebuchten Einkaufslieferung zugeordnet, d aktualisiert der Lagerwert des Artikels mit den Kosten für Artikelzu-/-abschläge.

## <a name="see-also"></a>Siehe auch
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]