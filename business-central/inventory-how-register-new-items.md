---
title: Erstellen Sie Artikelkarten für Services oder Waren | Microsoft Docs
description: Sie stellen Artikelkarten für Serviceleistungen an, die Sie für physische als Stunden und Produkte, wie Montageartikel, Fertigprodukte aus der Produktion, Komponenten oder Menge verkaufen, die Sie von Ihrem Lagerbestand verkaufen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 74eb66c4303acb452972f9ac3c7dda008e3c6502
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923820"
---
# <a name="register-new-items"></a>Neue Artikel registrieren

Artikel sind die Basis Ihres Unternehmens, die Waren oder Dienstleistungen, mit denen Sie handeln. Jeder Artikel muss als Artikelkarte registriert werden.

Artikelkarten verwahren die Informationen, die benötigt werden, um Artikel einzukaufen, einzulagern, zu liefern und zu berechnen.

Gibt an, ob die Artikelkarte einen **Bestand**, **Service** oder **Nicht-Bestand** ist, wenn die Einheit eine physische Einheit ist, die nicht im Lagerbestand verfolgt wird. Weitere Informationen zu diesen Arten finden Sie unter [über Einheitstypen](inventory-about-item-types.md)

Ein Artikel kann als übergeordneter Artikel mit zugrunde liegenden untergeordneten Elementen in Stücklisten (BOM) strukturiert werden. In [!INCLUDE[d365fin](includes/d365fin_md.md)] kann eine Stückliste entweder eine Montagestückliste oder eine Fertigungsstückliste sein, abhängig von dessen Verwendung. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

Wenn Sie den gleichen Artikel von mehr als einem Kreditoren einkaufen, können Sie die Kreditoren mit der Artikelkarte anschließen. Die Kreditoren erscheinen dann auf der Seite **Artikel/Kreditoren Katalog**, damit Sie einen alternativen Kreditor einfach auswählen können.

Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Katalogelemente sollen nicht mit regulären Artikel der Art **Nicht-Lager** verwechselt werden. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Wenn für verschiedene Artikelarten Artikelvorlagen existieren, öffnet sich eine Seite, aus dem Sie eine entsprechende Artikelvorlage auswählen können, sobald eine neue Artikelkarte erstellt wird . Wenn nur eine Artikelvorlage vorhanden ist, verwenden neue Artikelkarten immer diese Vorlage.

Im folgenden Verfahren wird erläutert, wie Sie eine Objektkarte von Grund auf neu erstellen. Sie können auch neue Objektkarten erstellen, indem Sie vorhandene kopieren. Weitere Informationen finden Sie unter [Kopieren Sie vorhandene Elemente, um neue Elemente zu erstellen](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>So erstellen Sie eine neue Artikelkarte

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Artikel** die Aktion **Neu** aus.

    Wenn nur eine Artikelvorlage vorhanden ist, öffnet sich eine neue Artikelkarte bei der einige Felder mit Informationen aus der Vorlage ausgefüllt sind.
3. Wählen Sie auf der Seite **Vorlage für neuen Artikel auswählen** die Vorlage, die Sie für die neue Artikelkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Artikelkarte wird geöffnet, in der einige Felder mit Daten aus der Vorlage ausgefüllt sind.
5. Wenn nötig, fahren Sie mit dem Ausfüllen oder Ändern der Felder auf der Artikelkarte fort. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Die Wahl der **Kostenmethode** legt fest, wie der Einstandspreis berechnet wird, indem Annahmen über die physische Bewegung der Artikel durch Ihr Unternehmen gemacht werden. Fünf Lagerabgangsmethoden stehen, abhängig von der Art des Artikels zur Verfügung. Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden".](design-details-costing-methods.md)
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

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Artikel** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.  
3. Wählen Sie die Aktion **Kreditoren** aus.  
4. Wählen Sie das Feld **Kreditorennr.**, und wählen Sie den Kreditor aus, den Sie für den Artikel einrichten möchten.  
5. Optional können Sie die restlichen Felder ausfüllen.  
6. Wiederholen Sie die Schritte 2 bis 5 für jeden Verkäufer, von dem Sie den Artikel kaufen möchten.

Die Kreditoren erscheinen dann auf der Seite **Artikel/Kreditoren Katalog**, damit Sie einen alternativen Kreditor einfach auswählen können.

## <a name="categories-attributes-and-variants"></a>Kategorien, Attribute und Varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="deleting-item-cards"></a>Löschen von Artikelkarten

Wenn Sie eine Transaktion für einen Artikel gebucht haben, können Sie die Karte nicht löschen, da die Posten möglicherweise für die Bestandsbewertung oder die Prüfung erforderlich sind. Um Artikelkarten mit Posten zu löschen, wenden Sie sich an einen Microsoft-Partner, um dies über einen Code durchzuführen.  

## <a name="manage-inventory-in-warehouses"></a>Lagerbestand in Lagern verwalten

Wenn Sie einen neuen Artikel erfassen, werden Felder angezeigt, die sich auf die Lagerverwaltung beziehen, insbesondere im Inforegister **Lager**. Wenn Ihre Organisation die Lagerverwaltungsfunktionen in [!INCLUDE [prodshort](includes/prodshort.md)] nicht verwendet, können Sie diese Felder ignorieren.  

Wenn Ihre Organisation später die Lagerverwaltung einrichtet, müssen Sie in den meisten Fällen zu jedem vorhandenen Artikel zurückkehren, um sicherzustellen, dass zu diesem die richtigen Informationen in den verschiedenen Feldern vorhanden sind, damit die Lagerprozesse wie erwartet ausgeführt werden können. Diese Informationen können Felder wie **Lagerklassencode** oder **Einlagerungsvorlagencode** umfassen. Weitere Informationen finden Sie unter [Designdetails: Lagerhaus einrichten](design-details-warehouse-setup.md).  

## <a name="see-also"></a>Siehe auch

[Lagerbestand](inventory-manage-inventory.md)  
[Einheiten einrichten](inventory-how-setup-units-of-measure.md)  
[Zollpositionen](finance-how-setup-report-intrastat.md#tariff-numbers)  
[Abstimmen der Lagerkosten mit der Finanzbuchhaltung](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Erstellen von Nummernkreisen](ui-create-number-series.md)  
[Buchungsgruppen einrichten](finance-posting-groups.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
