---
title: Erstellen von Kontaktunternehmen| Microsoft Docs
description: "Beschreibt, wie einer Kontaktkarte für jede neue Unternehmung oder potentielle neuen Unternehmung erstellt wird, mit dem Sie eine Geschäftsbeziehung haben."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 64bef8820ec10bb293ccda88e7384d5d9e868e1f
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-contact-companies"></a>Erstellen von Kontaktunternehmen
Sie können für jedes neue Unternehmen, mit dem Sie Geschäfte machen, eine Kontaktkarte anlegen. Das können z. B. Debitoren, Kreditoren, Interessenten, Banken, Rechtsanwälte, Berater usw. sein.

Es gibt zwei Möglichkeiten, um einen Kontakt zu erstellen: von Grund auf neu oder aus einem bestehenden Debitor, Kreditor oder Bankkonto.

Bevor Sie einen Kontakt anlegen, sollten Sie die Einstellungen im Fenster **Marketing & Vertrieb Einr.** überprüfen. Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)

## <a name="create-a-company-contact-from-scratch"></a>Neues eines Unternehmenskontakte von Grund auf
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.

    Wenn Sie im Fenster **Marketing & Vertrieb Einr.** eine Nummernserie für Kontakte eingegeben haben, können Sie alternativ auch die EINGABETASTE drücken, um die nächste verfügbare Kontaktnummer auszuwählen.  
4. Legen Sie **Art** auf **Unternehmen** fest.
5. Füllen Sie die weiteren Felder wie erforderlich aus.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto
Wenn Sie bereits eine Anzahl von Debitoren, Kreditoren und Bankkonten eingerichtet haben, können Sie Kontakte auf der Basis von bestehenden Daten erstellen. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen mit dem Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert.

> [!NOTE]  
>   Bevor Sie auf diese Weise ein Kontaktunternehmen erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten im Fenster **Marketingeinrichtung** angeben. Wenn Sie Kontakte aus Bankkonten erstellen, müssen Sie Nummernserie für Bankkonten im **Finanzbuchhaltungseinrichtung**-Fenster angeben.

1. Wählen Sie ![Glühlampe, die die Funktion "Teilen Sie mir mit, was Sie tun wollen"](media/ui-search/search_small.png "\"Teilen Sie mir mit, was Sie tun wollen\"") und Folgendes ein, je nachdem, von wo aus Sie Kontakte erstellen möchten, und wählen Sie dann den zugehörigen Link aus.
   * **Kontakte aus Debitoren erstellen**
   * **Kontakte aus Kreditoren erstellen**
   * **Kontakte aus Bankkonten erstellen**
2. Legen Sie im Abschnitt **Debitor**, **Kreditor** oder **Bankkonto** des Stapelverarbeitungsfenstert Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.
3. Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.

    Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen. Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung für Kreditoren zugewiesen, die im Fenster **Marketing & Vertrieb Einr.** festgelegt wurde.

> [!TIP]  
>   Sie können auch einen Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Siehe auch
[Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Kontakten Geschäftsbeziehungen zuordnen](marketing-business-relations.md#AssignBusRelContact)  
[Kontakt eine Branche zuordnen](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Zuordnen von Verteiler zu einem Kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Anlegen von Kontaktpersonen](marketing-create-contact-persons.md)  
[Arbeiten mit  Business Central](ui-work-product.md)

