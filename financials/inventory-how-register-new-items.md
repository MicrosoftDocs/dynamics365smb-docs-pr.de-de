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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 719e11f2c8fee3d7e5dd3736754700b68f57379c
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-register-new-items"></a>Vorgehensweise: Einen neuen Artikel registrieren
Produkte sind die Basis Ihres Unternehmens, die Waren oder Dienstleistungen, mit denen Sie handeln. Jedes Produkt muss als Artikelkarte registriert werden.

Artikelkarten verwahren die Informationen, die benötigt werden, um Produkte einzukaufen, einzulagern, zu liefern und zu berechnen.

Die Artikelkarte kann den Typ **Bestand** oder **Service** haben, um anzuzeigen, ob das Produkt eine physische Einheit oder eine Arbeitszeiteinheit ist. Neben einiger Felder, die sich mit den physischen Aspekten eines Artikels verknüpfen, arbeiten alle Felder auf einer Artikelkarte auf die gleiche Weise für Lagerartikel und Dienstleistungen. Weitere Informationen über den Verkauf von Artikeln finden Sie unter [So gehts: Produkte verkaufen](sales-how-sell-products.md) oder [So gehts: Fakturieren](sales-how-invoice-sales.md).

Ein Artikel kann als übergeordneter Artikel mit zugrunde liegenden untergeordneten Elementen in Stücklisten (BOM) strukturiert werden. In [!INCLUDE[d365fin](includes/d365fin_md.md)], bezeichnet eine Stückliste als eine Montagestückliste. Sie verwenden Montagestücklisten, um übergeordnete Artikel zu strukturieren, die Sie als Sets verkaufen, die aus den Komponenten des übergeordneten Artikels bestehen oder für die Sie die Auftragsmontage oder das Lager haben. Weitere Informationen finden Sie unter [Arbeiten mit Stücklisten](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Wenn für verschiedene Artikelarten Artikelvorlagen existieren, öffnet sich ein Fenster, aus dem Sie eine entsprechende Artikelvorlage auswählen können, sobald eine neue Artikelkarte erstellt wird . Wenn nur eine Artikelvorlage vorhanden ist, verwenden neue Artikelkarten immer diese Vorlage.

## <a name="to-create-a-new-item-card"></a>So erstellen Sie eine neue Artikelkarte
1. Wählen Sie auf der Startseite die Aktion **Artikel**, um die Liste der vorhandenen Artikel zu öffnen.  
2. Wählen Sie im Fenster **Artikel** die Aktion **Neu** aus.

    Wenn nur eine Artikelvorlage vorhanden ist, öffnet sich eine neue Artikelkarte bei der einige Felder mit Informationen aus der Vorlage ausgefüllt sind.
3. Wählen Sie im Fenster **Vorlage für neuen Artikel auswählen** die Vorlage, die Sie für die neue Artikelkarte verwenden möchten.
4. Wählen Sie die Schaltfläche **OK** aus. Eine neue Artikelkarte wird geöffnet, in der einige Felder mit Daten aus der Vorlage ausgefüllt sind.
5. Wenn nötig, fahren Sie mit dem Ausfüllen oder Ändern der Felder auf der Artikelkarte fort. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

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

## <a name="see-also"></a>Siehe auch
  [Lagerbest](inventory-manage-inventory.md)  
  [Einkauf](purchasing-manage-purchasing.md)  
  [Verkauf](sales-manage-sales.md)  
  [Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
