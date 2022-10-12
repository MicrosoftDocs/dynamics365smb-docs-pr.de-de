---
title: Erstellen von Elementkarten für Waren oder Dienstleistungen (enthält Video)
description: Sie erstellen Artikelkarten für Dienstleistungen, die Sie als Stunden verkaufen, und für physische Produkte. Beispiele hierfür sind Montageartikel und fertige Waren, die Sie aus Ihrem Bestand verkaufen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item, item substitution
ms.search.form: 30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719
ms.date: 09/26/2022
ms.author: edupont
ms.openlocfilehash: 945197681e32f6d77ede2f1b0e727892a64d8277
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9604948"
---
# <a name="register-new-items"></a>Neue Artikel registrieren

Artikel sind die Basis Ihres Unternehmens, die Waren oder Dienstleistungen, mit denen Sie handeln. Jeder Artikel muss als Artikelkarte registriert werden.

Artikelkarten verwahren die Informationen, die benötigt werden, um Artikel einzukaufen, einzulagern, zu liefern und zu berechnen.

Gibt an, ob die Artikelkarte einen **Bestand**, **Service** oder **Nicht-Bestand** ist, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird. Weitere Informationen zu diesen Arten finden Sie unter [über Einheitstypen](inventory-about-item-types.md)

Ein Artikel kann als übergeordneter Artikel mit zugrunde liegenden untergeordneten Elementen in Stücklisten (BOM) strukturiert werden. Erfahren Sie mehr über Montagestücklisten und Produktionsstücklisten unter [Arbeiten mit Stücklisten ](inventory-how-work-BOMs.md).

Wenn Sie den gleichen Artikel von mehr als einem Kreditoren einkaufen, können Sie die Kreditoren mit der Artikelkarte anschließen. Die Kreditoren erscheinen dann auf der Seite **Artikel/Kreditoren Katalog**, damit Sie einen alternativen Kreditor einfach auswählen können.

*Katalogartikel* sind Artikel, die Sie Ihren Debitoren anbieten, die Sie nicht in Ihrem System verwalten möchten, bis Sie den Verkauf starten. Katalogelemente sind keine regulären Artikel der Art **Nicht-Lager**. Erfahren Sie mehr unter [Mit Katalogelementen arbeiten ](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Wenn für verschiedene Artikelarten Artikelvorlagen existieren, öffnet sich eine Seite, aus dem Sie eine entsprechende Artikelvorlage auswählen können, sobald eine neue Artikelkarte erstellt wird . Wenn nur eine Artikelvorlage vorhanden ist, verwenden neue Artikelkarten immer diese Vorlage.

Im folgenden Verfahren wird erläutert, wie Sie eine Objektkarte von Grund auf neu erstellen. Sie können auch neue Objektkarten erstellen, indem Sie vorhandene kopieren. Weitere Informationen finden Sie unter [Kopieren Sie vorhandene Elemente, um neue Elemente zu erstellen](inventory-how-copy-items.md).  

<br />
> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>So erstellen Sie eine neue Artikelkarte

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Die Wahl der **Kostenmethode** legt fest, wie der Einstandspreis berechnet wird, indem Annahmen über die physische Bewegung der Artikel durch Ihr Unternehmen gemacht werden. Fünf Lagerabgangsmethoden stehen, abhängig von der Art des Artikels zur Verfügung. Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden](design-details-costing-methods.md).
>
> Wenn Sie **Durchschnitt** wählen, dann werden die Stückkosten des Artikels als durchschnittliche Stückkosten zu jedem Zeitpunkt nach dem Kauf berechnet. Bestand wird mit der Annahme bewertet, dass aller Bestand gleichzeitig verkauft wird. Für Artikel, die die Lagerabgangsmethode verwenden, können Sie das Feld **Einstandspreis** auf der Artikelkarte wählen, um die Historie von Transaktionen anzuzeigen, denen der **durchschnittliche Einstandspreis** berechnet wird

Sie können Sonderpreise oder Rabatte für den Artikel anzeigen oder bearbeiten, die Sie gewähren oder die Ihr Kreditor Ihnen gewährt, wenn bestimmte Kriterien, wie z. B. Debitor, Mindestbestellmenge oder Enddatum erfüllt sind. Dazu wählen Sie die Aktionen **Sonderpreise festlegen** oder **Sonderrabatte festlegen** aus. Jede Zeile zum Beispiel auf der Seite **Verkaufspreise** repräsentiert einen Sonderpreis. Jede Spalte stellt ein Kriterium dar, das angewendet werden muss, um einem Debitor den Sonderpreis zu gewähren, den Sie in das Feld **VK-Preis** auf der Seite **Verkaufspreise** eingeben. Weitere Informationen finden Sie unter [Verkaufspreise, Rabatt und Zahlungsvereinbarungen aufzeichnen](sales-how-record-sales-price-discount-payment-agreements.md) oder [Spezielle Verkaufspreise und Rabatte aufzeichnen](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Der Artikel ist nun erfasst und die Debitorenkarte ist bereit, in Einkaufs- und Verkaufsbelegen verwendet zu werden.

Wenn Sie diese Artikelkarte als Vorlage zum Erstellen neuer Artikelkarten verwenden möchten, können Sie sie als Vorlage speichern. Weitere Informationen finden Sie im folgenden Abschnitt.  

### <a name="to-save-the-item-card-as-a-template"></a>So speichern Sie die Artikelkarte als Vorlage

1. Wählen Sie auf der Seite **Artikelkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Arikelvorlage** wird geöffnet und zeigt die Artikelkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionen Vorlagen** wird geöffnet und zeigt alle Dimensionscodes, die für den Artikel eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Artikelkarten gelten, die mit der Vorlage erstellt wurden.
5. Wenn Sie die neue Artikelvorlage abgeschlossen haben, klicken Sie auf die Schaltfläche **OK**.

Die Artikelvorlage wird der Liste von Artikelvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.

### <a name="items-used-in-production-orders"></a>Artikel, die in Fertigungsaufträgen verwendet werden

Wenn Sie Artikel registrieren möchten, die dann in Fertigungsaufträgen verwendet werden, geben Sie die Beschaffungsmethode im Inforegister **Beschaffung** als *Fertigungsauftrag* an. Weitere Informationen finden Sie unter [Info zu Montageaufträgen](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>So richten Sie mehrere Kreditoren für einen Artikel ein

Wenn Sie den gleichen Artikel von mehr als einem Kreditoren einkaufen, müssen Sie die benötigten Informationen für jeden Kreditor eingeben. Dies umfasst z. B. Preise, Lieferzeit, Rabatte usw.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.  
3. Wählen Sie die Aktion **Kreditoren** aus.  
4. Wählen Sie das Feld **Kreditorennr.**, und wählen Sie den Kreditor aus, den Sie für den Artikel einrichten möchten.  
5. Optional können Sie die restlichen Felder ausfüllen.  
6. Wiederholen Sie die Schritte 2 bis 5 für jeden Verkäufer, von dem Sie den Artikel kaufen möchten.

Die Kreditoren erscheinen dann auf der Seite **Artikel/Kreditoren Katalog**, damit Sie einen alternativen Kreditor einfach auswählen können.

## <a name="set-up-item-substitutions"></a>Ersatzartikel einrichten

Sie können Artikel so einrichten, dass sie über Ersatzartikel verfügen, z. B. andere Artikel, die anstelle des ursprünglichen Artikels verwendet werden können.

### <a name="to-make-an-item-substitution"></a>So legen Sie einen Ersatzartikel für einen Artikel fest

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.  
2. Suchen Sie den entsprechenden Artikel, und klicken Sie dann auf die **Artikelnr.**, um die Artikelkarte zu öffnen.  
3. Wählen Sie die Aktion **Zugehörig**, dann den **Artikel** und anschließend die Option **Ersatzartikel** aus, um die Seite **Ersatzartikel** zu öffnen.  
4. Wählen Sie das Feld **Ersatzartikelnr.** und dann den Ersatzartikel aus der Liste aus.
5. Füllen Sie die Felder auf der Seite bei Bedarf aus oder ändern Sie sie.

Wenn die angeforderte Menge, beispielsweise in einer Verkaufszeile, die Menge überschreitet, die am Lager verfügbar ist, dann wird eine Meldung darüber angezeigt, dass Ersatzartikel vorhanden sind.

> [!NOTE]  
> Beachten Sie, dass Artikelersetzungen nicht automatisch dazu führen, dass ein Artikel durch einen anderen Artikel ersetzt wird, beispielsweise beim Erstellen eines Verkaufsauftrags oder in einer Stückliste. Stattdessen werden Sie darüber benachrichtigt, dass Ihnen ein Ersatzartikel zur Verfügung steht.

## <a name="categories-attributes-and-variants"></a>Kategorien, Attribute und Varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Erfahren Sie mehr über Varianten unter [Produktvarianten verwalten](inventory-item-variants.md).  

## <a name="deleting-item-cards"></a>Löschen von Artikelkarten

Wenn Sie eine Transaktion für einen Artikel gebucht haben, können Sie die Karte nicht löschen, da die Posten möglicherweise für die Bestandsbewertung oder die Prüfung erforderlich sind. Um Artikelkarten mit Posten zu löschen, wenden Sie sich an einen Microsoft-Partner, um dies über einen Code durchzuführen.  

## <a name="manage-inventory-in-warehouses"></a>Lagerbestand in Lagern verwalten

Wenn Sie einen neuen Artikel erfassen, werden Felder angezeigt, die sich auf die Lagerverwaltung beziehen, insbesondere im Inforegister **Lager**. Wenn Ihre Organisation die Lagerverwaltungsfunktionen in [!INCLUDE [prod_short](includes/prod_short.md)] nicht verwendet, können Sie diese Felder ignorieren.  

Wenn Ihre Organisation später eine Lagerverwaltung einrichtet, empfehlen wir Ihnen sicherzustellen, dass jeder vorhandene Artikel die richtigen Informationen in den verschiedenen Feldern enthält. Auf diese Weise können die Lagerprozesse wie erwartet ablaufen. Die Informationen können Felder wie **Lagerklassencode** oder **Einlagerungsvorlagencode** umfassen. Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).  

## <a name="planning"></a>Planung

Wenn Ihre Firma die Prozesse der Lieferplanung in [!INCLUDE [prod_short](includes/prod_short.md)] verwendet, müssen Sie die entsprechenden Felder auf dem Inforegister **Planung** ausfüllen. Eine Einführung in den Planungsbereich finden Sie unter [Details zur Planung: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md).  

Beispiele für die Verwendung der Felder auf der Inforegisterkarte **Planung** finden Sie unter [Bewährte Verfahren für die Einrichtung: Planungsparameter](setup-best-practices-planning-parameters.md).  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/create-items/)

## <a name="see-also"></a>Siehe auch

[Bestand](inventory-manage-inventory.md)  
[Einheiten einrichten](inventory-how-setup-units-of-measure.md)  
[Produktvarianten verwalten](inventory-item-variants.md)  
[Intrastat-Berichte einrichten](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Abstimmen der Lagerkosten mit der Finanzbuchhaltung](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Buchungsgruppen einrichten](finance-posting-groups.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Info zu Planungsfunktionen](production-about-planning-functionality.md)  
[Bewährte Einrichtungsmethoden: Planungsparameter](setup-best-practices-planning-parameters.md)  
[Bewährte Einrichtungsmethoden: Beschaffungsplanung](setup-best-practices-supply-planning.md)  
[Designdetails: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md)  
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)  
[Designdetails: Planungsparameter](design-details-planning-parameters.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
