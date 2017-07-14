---
title: Erstellen von Kontaktunternehmen| Microsoft Docs
description: Beschreibt, wie Sie Kontaktunternehmen in Financials erstellen
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bd8dfb8abc9387ad6b9c500f25feb181878b6cfe
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Erstellen von Kontaktunternehmen
<a id="create-contact-companies" class="xliff"></a>
Sie können für jedes neue Unternehmen, mit dem Sie Geschäfte machen, eine Kontaktkarte anlegen. Das können z. B. Debitoren, Kreditoren, Interessenten, Banken, Rechtsanwälte, Berater usw. sein.

Es gibt zwei Möglichkeiten, um einen Kontakt zu erstellen: von Grund auf neu oder aus einem bestehenden Debitor, Kreditor oder Bankkonto.

Bevor Sie einen Kontakt anlegen, sollten Sie die Einstellungen im Fenster **Marketing & Vertrieb Einr.** überprüfen. Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)

## Neues eines Unternehmenskontakte von Grund auf
<a id="create-a-company-contact-from-scratch" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Kontakte** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.

    Wenn Sie im Fenster **Marketing & Vertrieb Einr.** eine Nummernserie für Kontakte eingegeben haben, können Sie alternativ auch die EINGABETASTE drücken, um die nächste verfügbare Kontaktnummer auszuwählen.  
4. Legen Sie **Art** auf **Unternehmen** fest.
5. Füllen Sie die weiteren Felder wie erforderlich aus.

## Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto
<a id="create-a-company-contact-from-a-customer-vendor-or-bank-account" class="xliff"></a>
Wenn Sie bereits eine Anzahl von Debitoren, Kreditoren und Bankkonten eingerichtet haben, können Sie Kontakte auf der Basis von bestehenden Daten erstellen. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen mit dem Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert.

**Hinweis**: Bevor Sie auf diese Weise ein Kontaktunternehmen erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten im Fenster **Marketingeinrichtung** angeben. Wenn Sie Kontakte aus Bankkonten erstellen, müssen Sie Nummernserie für Bankkonten im **Finanzbuchhaltungseinrichtung**-Fenster angeben.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben abhängig vom Ort, an dem Sie die Kontakte erstellen möchten und wählen den zugehörigen Link aus.
   * **Kontakte aus Debitoren erstellen**
   * **Kontakte aus Kreditoren erstellen**
   * **Kontakte aus Bankkonten erstellen**
2. Legen Sie im Abschnitt **Debitor**, **Kreditor** oder **Bankkonto** des Stapelverarbeitungsfenstert Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.
3. Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.

    Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen. Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung für Kreditoren zugewiesen, die im Fenster **Marketing & Vertrieb Einr.** festgelegt wurde.

**Tipp**: Sie können auch einen Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## Siehe auch
<a id="see-also" class="xliff"></a>
[Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Kontakten Geschäftsbeziehungen zuordnen](marketing-business-relations.md#AssignBusRelContact)  
[Kontakt eine Branche zuordnen](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Zuordnen von Verteiler zu einem Kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Gewusst wie: Anlegen von Kontaktpersonen](marketing-create-contact-persons.md)  
[Arbeiten mit Financials](ui-work-product.md)

