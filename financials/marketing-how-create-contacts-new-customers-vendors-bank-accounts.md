---
title: "Erstellen eines Kreditors, Debitors oder Bankkontos über einen Kontakt | Microsoft Docs"
description: "Sie können einen bestehenden Kontakt als Debitor, Kreditor oder Bankkonto mithilfe der vorhandenen Daten und angeben Geschäftsbeziehung erfassen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 289213b9c44b07387fd0dcf315b9d08750bdd9f7
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Vorgehensweise: So erstellen Sie einen Kontakt aus einem Debitor, Kreditor oder Bankkonto
Sie können vorhandene Kontakte als Debitoren, Kreditoren oder als Bankkonten erfassen. Beim Erstellen eines Kreditors, Debitors oder Bankkontos aus einem Kontakt können Sie vorhandene Daten verwenden. Wenn Sie einen Debitor, Kreditor oder ein Bankkonto auf diese Weise erstellen, wird es mit dem Kontakt synchronisiert Die Synchronisierung macht Informationen, die zwischen Kontakten und Debitoren, Kreditoren oder Bankkonto gleich sind, identisch.

**Hinweis**: Bevor Sie auf diese Weise ein erfassen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten im Fenster Marketingeinrichtung angeben. Wenn Sie Kontakte als Bankkonten erfassen, müssen Sie Nummernserie für Bankkonten im **Finanzbuchhaltungseinrichtung**-Fenster angeben.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Kontakte** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Kontakt aus, den Sie als Debitor, Kreditor oder Bankkonto erstellen möchten.
3. Wählen Sie die Aktionen **Erstellen als**, und wählen Sie denn entweder **Debitor**, **Kreditor** oder **Bank**.
4. Bestätigen Sie die nachfolgende Meldung.

Die Kontaktinformationen werden von der Karte **Kontakt** auf die Karte **Bankkonto**, die Karte **Debitor** oder die Karte **Kreditor** übertragen. Sie können den einzelnen Karten spezifische Informationen, wie Fakturierungs- und Zahlungsdetails hinzufügen.

## <a name="see-also"></a>Siehe auch
[Gewusst wie: Erstellen von neuen Kontaktunternehmen](marketing-create-contact-companies.md)  
[Gewusst wie: Anlegen von Kontaktpersonen](marketing-create-contact-persons.md)  
[Marketing & Vertrieb einrichten](marketing-setup-marketing.md)  
[Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[So gehts: Kontakte mit vorhandenen Debitoren, Kreditoren und Bankkonten verknüpfen](marketing-how-link-contact.md)  
[Kontakten Geschäftsbeziehungen zuordnen](marketing-business-relations.md#AssignBusRelContact)  
[Arbeiten mit Dynamics 365](ui-work-product.md)

