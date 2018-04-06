---
title: "Erstellen Sie Artikelkarten für Services oder Waren | Microsoft Docs"
description: "Sie stellen Artikelkarten für Serviceleistungen an, die Sie für physische als Stunden und Produkte, wie Montageartikel, Fertigprodukte aus der Produktion, Komponenten oder Menge verkaufen, die Sie von Ihrem Lagerbestand verkaufen."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9643e71c29adf4b4be1d9d474832e3e29f2c21d8
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="register-new-items"></a>Neue Artikel registrieren
Produkte sind die Basis Ihres Unternehmens, die Waren oder Dienstleistungen, mit denen Sie handeln. Jedes Produkt muss als Artikelkarte registriert werden.

Artikelkarten verwahren die Informationen, die benötigt werden, um Produkte einzukaufen, einzulagern, zu liefern und zu berechnen.

Die Artikelkarte kann den Typ **Bestand** oder **Service** haben, um anzuzeigen, ob das Produkt eine physische Einheit oder eine Arbeitszeiteinheit ist. Neben einiger Felder, die sich mit den physischen Aspekten eines Artikels verknüpfen, arbeiten alle Felder auf einer Artikelkarte auf die gleiche Weise für Lagerartikel und Dienstleistungen. Weitere Informationen über den Verkauf von Artikeln finden Sie unter [Produkte verkaufen](sales-how-sell-products.md) oder [Fakturieren](sales-how-invoice-sales.md).

Ein Artikel kann als übergeordneter Artikel mit zugrunde liegenden untergeordneten Elementen in Stücklisten (BOM) strukturiert werden. In [!INCLUDE[d365fin](includes/d365fin_md.md)] kann eine Stückliste entweder eine Montagestückliste oder eine Fertigungsstückliste sein, abhängig von dessen Verwendung. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Wenn für verschiedene Artikelarten Artikelvorlagen existieren, öffnet sich ein Fenster, aus dem Sie eine entsprechende Artikelvorlage auswählen können, sobald eine neue Artikelkarte erstellt wird . Wenn nur eine Artikelvorlage vorhanden ist, verwenden neue Artikelkarten immer diese Vorlage.

Wenn Sie den gleichen Artikel von mehr als einem Kreditoren einkaufen, können Sie die Kreditoren mit der Artikelkarte anschließen. Die Kreditoren erscheinen dann im Fenster **Artikel/Lieferanten Katalog**, damit Sie einen alternativen Kreditor einfach auswählen können.

## <a name="to-create-a-new-item-card"></a>So erstellen Sie eine neue Artikelkarte
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Fenster **Artikel** die Aktion **Neu** aus.

    Wenn nur eine Artikelvorlage vorhanden ist, öffnet sich eine neue Artikelkarte bei der einige Felder mit Informationen aus der Vorlage ausgefüllt sind.
3. Wählen Sie im Fenster **Vorlage für neuen Artikel auswählen** die Vorlage, die Sie für die neue Artikelkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Artikelkarte wird geöffnet, in der einige Felder mit Daten aus der Vorlage ausgefüllt sind.
5. Wenn nötig, fahren Sie mit dem Ausfüllen oder Ändern der Felder auf der Artikelkarte fort. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Die Wahl der **Kostenmethode** legt fest, wie der Einstandspreis berechnet wird, indem Annahmen über die physische Bewegung der Artikel durch Ihr Unternehmen gemacht werden. Fünf Lagerabgangsmethoden stehen, abhängig von der Art des Artikels zur Verfügung. Weitere Informationen finden Sie unter [Designdetails: Lagerabgangsmethoden".](design-details-costing-methods.md)
>
> Wenn Sie die **Durchschnitt** verwenden, dann werden die Einstandskosten als Durchschnittskosten nach dem Kauf berechnet. Bestand wird mit der Annahme bewertet, dass aller Bestand gleichzeitig verkauft wird. Für Artikel, die die Lagerabgangsmethode verwenden, können Sie das Feld **Einstandspreis** auf der Artikelkarte wählen, um die Historie von Transaktionen anzuzeigen, denen der d**urchschnittliche Einstandspreis** berechnet wird

Im Inforegister **Preise und Buchungen** können Sie spezielle Preise oder Rabatte anzeigen, die Sie für den Artikel gewähren, wenn bestimmte Kriterien, wie z.B. Debitor, Mindestbestellmenge oder Enddatum erfüllt sind. Jede Zeile stellt einen Sonderpreis oder einen Zeilenrabatt dar. Jede Spalte stellt ein Kriterium an, das gelten muss, um den Sonderpreis, den Sie im **Einheitenpreis**-Feld eingeben, oder den Zeilenrabatt, den Sie im **Zeilenrabatt**-Feld eingeben, zu rechtfertigen. Weitere Informationen finden Sie unter [Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md)

Der Artikel ist nun erfasst und die Debitorenkarte ist bereit, in Einkaufs- und Verkaufsbelegen verwendet zu werden.

Wenn Sie diese Artikelkarte als Vorlage zum Erstellen neuer Artikelkarten verwenden möchten, können Sie sie als Vorlage speichern. Weitere Informationen finden Sie im folgenden Abschnitt.

## <a name="to-save-the-item-card-as-a-template"></a>So speichern Sie die Artikelkarte als Vorlage
1. Wählen Sie im Fenster **Artikelkarte** die Aktion **Als Vorlage speichern** aus. Das Fenster **Arikelvorlage** wird geöffnet und zeigt die Artikelkarte als Vorlage.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um Dimensionen in den Vorlagen wiederzuverwenden, wählen Sie die Aktion **Dimensionen**. Das Fenster **Dimensionen Vorlagenübersicht** wird geöffnet und zeigt alle Dimensionscodes, die für den Artikel eingerichtet werden.
4. Bearbeiten Sie oder geben Sie Dimensionscodes ein, die für die neuen Artikelkarten gelten, die mit der Vorlage erstellt wurden.
5. Wenn Sie die neue Artikelvorlage abgeschlossen haben, klicken Sie auf die Schaltfläche **OK**.

Die Artikelvorlage wird der Liste von Artikelvorlagen hinzugefügt, damit Sie diese verwenden können, um neue Debitorenkarten zu erstellen.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>So richten Sie mehrere Kreditoren für einen Artikel ein  
Wenn Sie den gleichen Artikel von mehr als einem Kreditoren einkaufen, müssen Sie die benötigten Informationen für jeden Kreditor eingeben. Dies umfasst z. B. Preise, Lieferzeit, Rabatte usw.  

1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Bearbeiten** aus.  
3.  Wählen Sie die Aktion **Verkäufer** aus.  
4.  Wählen Sie das Feld **Kreditorennr.**, und wählen Sie den Kreditor aus, den Sie für den Artikel einrichten möchten.  
5.  Optional können Sie die restlichen Felder ausfüllen.  
6.  Wiederholen Sie die Schritte 2 bis 5 für jeden Verkäufer, von dem Sie den Artikel kaufen möchten.

Die Kreditoren erscheinen dann im Fenster **Artikel/Lieferanten Katalog**, damit Sie einen alternativen Kreditor einfach auswählen können.

## <a name="see-also"></a>Siehe auch
  [Lagerbest](inventory-manage-inventory.md)  
  [Einkauf](purchasing-manage-purchasing.md)  
  [Verkauf](sales-manage-sales.md)  
  [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

