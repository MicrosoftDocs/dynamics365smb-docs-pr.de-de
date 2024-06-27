---
title: Artikelkarten für Waren oder Dienstleistungen erstellen
description: 'Sie erstellen Artikelkarten für Dienstleistungen, die Sie als Stunden verkaufen, und für physische Produkte. Beispiele hierfür sind Montageartikel und fertige Waren, die Sie aus Ihrem Bestand verkaufen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="register-new-items"></a>Neue Artikel registrieren

Artikel sind Waren oder Dienstleistungen, die Sie kaufen, lagern, verkaufen, liefern und abrechnen. Verwenden Sie die **Artikelkarte**, um Informationen zu den folgenden Artikeltypen zu registrieren:

* **Bestand** gibt an, dass der Artikel eine physische Einheit ist, die Sie im Lager verwalten und verfolgen.
* **Nicht Bestand** sind physische Einheiten, die Sie im Bestand weder verwalten noch verfolgen.
* **Service**artikel sind eine Arbeitszeiteinheit, die in der Regel in der Serviceverwaltung verwendet wird.

Weitere Informationen zu diesen Artikeltypen finden Sie unter [Info zu Artikeltypen](inventory-about-item-types.md).

> [!TIP]
> Es gibt auch Katalogartikel, die ähnlich wie die nicht auf Lager befindlichen Artikel sind, da es sich um Artikel handelt, die Sie den Kunden anbieten, diese aber erst verwalten, wenn Sie sie verkaufen. Weitere Informationen finden Sie unter [Mit Katalogartikeln arbeiten](inventory-how-work-nonstock-items.md).  

## <a name="primary-and-alternate-vendors"></a>Primäre und alternative Anbieter

Wenn Sie denselben Artikel bei mehreren Kreditoren nkaufen, können Sie die Kreditoren mit dem Artikel verbinden. Verwenden Sie die Aktion **Kreditoren** auf der Seite **Artikelkarte**, um die Seite **Artikel/Lieferanten Katalog** zu öffnen. Auf der Seite werden die Kreditoren angezeigt, bei denen Sie den Artikel kaufen, sodass Sie beim Erstellen einer Bestellung problemlos einen alternativen Kreditor erstellen oder auswählen können.

## <a name="use-item-templates"></a>Artikelvorlagen verwenden

Um beim Erstellen neuer Artikel Einstellungen für verschiedene Artikeltypen wiederzuverwenden, können Sie Artikel als Artikelvorlagen speichern. Mithilfe von Artikelvorlagen können Sie neue Artikel schneller hinzufügen und die Konsistenz Ihrer Artikeldaten erhöhen. Wenn Sie einen neuen Artikel registrieren, wird eine Seite angezeigt, auf der Sie eine Vorlage auswählen können. Nachdem Sie eine Vorlage ausgewählt haben, werden deren Einstellungen für das von Ihnen erstellte Element automatisch eingetragen. Wenn Sie nur über eine Artikelvorlage verfügen, verwenden neue Artikel immer diese Vorlage. Weitere Informationen zum Einrichten einer Artikelvorlage finden Sie unter [Eine Artikelkarte als Artikelvorlage speichern](#save-an-item-card-as-an-item-template).

## <a name="include-items-in-bills-of-materials"></a>Artikel in Stücklisten aufnehmen

Sie können Hierarchien mit einem Hauptartikel und zugrunde liegenden Komponentenartikeln in Montage- und Produktionsstücklisten strukturieren. Weitere Informationen Stücklisten finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

## <a name="to-create-a-new-item-card"></a>So erstellen Sie eine neue Artikelkarte

Das folgende Video zeigt, wie ein Artikel auf der Seite „Artikelkarte“ eingerichtet wird. Sie können jedoch auch neue Artikel einrichten, indem Sie vorhandene kopieren. Weitere Informationen finden Sie unter [Vorhandene Artikel kopieren, um neue Artikel zu erstellen](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> Die Wahl der **Kostenmethode** legt fest, wie der Einstandspreis berechnet wird, indem Annahmen über die physische Bewegung der Artikel durch Ihr Unternehmen gemacht werden. Fünf Lagerabgangsmethoden stehen, abhängig von der Art des Artikels zur Verfügung. Weitere Informationen zur Kostenkalkulation finden Sie unter [Designdetails: Nachkalkulationsmethoden](design-details-costing-methods.md).
>
> Wenn Sie **Durchschnitt** wählen, werden die Stückkosten des Artikels als durchschnittliche Stückkosten zu jedem Zeitpunkt nach dem Kauf berechnet. Bestand wird mit der Annahme bewertet, dass aller Bestand gleichzeitig verkauft wird. Mit dieser Einstellung können Sie das Feld **Einstandspreis** auf der Seite **Einst.-Pr. (durchschn.)-Ber., Übersicht** auswählen, um die Transaktionen anzuzeigen, die zum Berechnen der durchschnittlichen Kosten herangezogen wurden.

Sie können Sonderpreise oder Rabatte verwenden, die Sie oder Ihr Kreditor nach bestimmten Kriterien für den Artikel gewähren. Kriterien sind beispielsweise Kunde, Mindestbestellmenge oder Enddatum. Sonderpreise werden durch Auswahl der Aktionen **Sonderpreise festlegen** oder **Sonderrabatte festlegen** eingerichtet. Jede Zeile zum Beispiel auf der Seite **Verkaufspreise** repräsentiert einen Sonderpreis. Jede Spalte stellt ein Kriterium dar, das angewendet werden muss, um einem Debitor den Sonderpreis zu gewähren, den Sie in das Feld **VK-Preis** auf der Seite **Verkaufspreise** eingeben. Weitere Informationen zur Preisgestaltung finden Sie unter [Verkaufspreise, Rabatt und Zahlungsvereinbarungen aufzeichnen](sales-how-record-sales-price-discount-payment-agreements.md) oder [Spezielle Verkaufspreise und Rabatte aufzeichnen](purchasing-how-record-purchase-price-discount-payment-agreements.md).

### <a name="save-an-item-card-as-an-item-template"></a>Artikelkarte als Artikelvorlage speichern

1. Wählen Sie auf der Seite **Artikelkarte** die Aktion **Als Vorlage speichern** aus. Die Seite **Arikelvorlage** zeigt die Artikelkarte als Vorlage.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Sie können Dimensionen für Artikel auch wiederverwenden. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Die Seite **Dimensionsvorlagen** zeigt die Dimensionen an, die für den Artikel eingerichtet werden. Bearbeiten oder fügen Sie Dimensionen hinzu, die für neue Artikel gelten, die Sie über die Vorlage erstellen.

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

## <a name="delete-item-cards"></a>Artikelkarten löschen

Wenn Sie eine Transaktion für einen Artikel gebucht haben, können Sie die Karte nicht löschen, da die Posten möglicherweise für die Bestandsbewertung oder die Prüfung erforderlich sind. Um Artikelkarten mit Posten zu löschen, wenden Sie sich an einen Microsoft-Partner, um dies über einen Code durchzuführen.  

## <a name="manage-inventory-in-warehouses"></a>Lagerbestand in Lagern verwalten

Wenn Sie einen neuen Artikel erfassen, werden Felder angezeigt, die sich auf die Lagerverwaltung beziehen, insbesondere im Inforegister **Lager**. Wenn Ihre Organisation die Lagerverwaltungsfunktionen in [!INCLUDE [prod_short](includes/prod_short.md)] nicht verwendet, können Sie diese Felder ignorieren.  

Wenn Ihre Organisation später eine Lagerverwaltung einrichtet, empfehlen wir Ihnen sicherzustellen, dass jeder vorhandene Artikel die richtigen Informationen in den verschiedenen Feldern enthält. Auf diese Weise können die Lagerprozesse wie erwartet ablaufen. Die Informationen können Felder wie **Lagerklassencode** oder **Einlagerungsvorlagencode** umfassen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).  

## <a name="planning"></a>Planung

Wenn Ihre Firma die Prozesse der Lieferplanung in [!INCLUDE [prod_short](includes/prod_short.md)] verwendet, müssen Sie die entsprechenden Felder auf dem Inforegister **Planung** ausfüllen. Eine Einführung in den Planungsbereich finden Sie unter [Details zur Planung: Zentrale Konzepte des Planungssystems](design-details-central-concepts-of-the-planning-system.md).  

Beispiele für die Verwendung der Felder auf der Inforegisterkarte **Planung** finden Sie unter [Bewährte Verfahren für die Einrichtung: Planungsparameter](setup-best-practices-planning-parameters.md).  

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
