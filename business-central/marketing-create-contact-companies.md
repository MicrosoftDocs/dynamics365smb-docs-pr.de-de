---
title: Erstellen Sie Geschäftskontakte
description: Beschreibt die Aufgaben zum Erstellen von Kontakten und Definieren Ihrer Geschäftsbeziehungen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 01/05/2021
ms.author: edupont
ms.openlocfilehash: 42645a038c3937644fe90ce895ee454e1d1b5d5c
ms.sourcegitcommit: fe6943d410f5dca4e8b2986f95501009ae982d98
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "4827043"
---
# <a name="create-contacts"></a>Kontakt erstellen
Wenn Sie eine Geschäftsbeziehung zu jemandem in einem anderen Unternehmen aufbauen, fügen Sie ihn als Kontakt hinzu [!INCLUDE[prod_short](includes/prod_short.md)]. Fügen Sie dann alle Informationen über sie oder das Unternehmen hinzu, die für die zukünftige Kommunikation nützlich sein können. Auf der Seite **Kontaktkarte** können Sie die folgenden Arten von Kontakten erstellen:

* **Person** – In der Regel haben Sie in diesem Fall direkten Kontakt zu jemandem und Sie haben dessen Kontaktdaten.
* **Unternehmen** – Wenn beispielsweise der Kontakt keine Einzelperson ist, sondern eine juristische Person, wie ein Auftragnehmer oder eine Bank. 

Die Informationen, die für jeden Kontakttyp relevant sind, sind unterschiedlich, somit sind die verfügbaren Felder und Aktionen unterschiedlich. Beispielsweise können Sie Projektverantwortlichkeiten nur einer Person und eine Branche nur einem Unternehmen zuweisen. 

Sie können manuellen Änderungen im Feld **Art** später vornehmen. Alternativ können Sie die Felder im Inforegister **Übernahme** auf der Seite **Marketing-Einrichtung** verwenden, um die Daten anzugeben, die zwischen einer Person und ihrem Unternehmen geteilt werden sollen. Weitere Informationen finden Sie unter [Einrichten von Kontakten](marketing-setup-contacts.md).

Wenn beispielsweise ein Kontakt in einen Debitor umgewandelt wird, wird die Kontaktperson oder das Kontaktunternehmen zum Namen des Debitors. Der Datensatz für den Kontakt wird beibehalten, und Sie können den Kontakt und den Debitor so verknüpfen, dass deren Daten künftig synchronisiert werden.

## <a name="to-create-a-contact-manually"></a>So werden Kontakte manuell erstellt:
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kontakte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.

    Wenn Sie andererseits auf der Seite **Marketingsetup** eine Nummernserie für Kontakte eingerichtet haben, können Sie die **EINGABETASTE** drücken, um die nächste verfügbare Kontaktnummer einzufügen.  
5. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>So erstellen Sie einen Kontakt aus einem Debitor, Kreditor oder Bankkonto
Wenn Sie Debitoren, Kreditoren und Bankkonten haben, für die Sie Kontaktkarten erstellen möchten, können Sie die Stapelverarbeitungen **Kontakte erstellen von** verwenden, um Kontakte auf der Basis von den bestehenden Daten zu erstellen. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen anschließend mit den verbundenen Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert. Weitere Informationen finden Sie unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Bevor Sie Kontakte basierend auf vorhandenen Daten erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auf dem Inforegister **Interkationen** auf der Seite **Marketingeinrichtung** angeben. Weitere Informationen finden Sie unter [Kontakte einrichten](marketing-setup-contacts.md).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie eine der folgenden Optionen ein, je nachdem, woraus Sie Kontakte erstellen möchten, und wählen Sie dann den entsprechenden Link.
   * **Kontakte aus Debitoren erstellen**
   * **Kontakte aus Kreditoren erstellen**
   * **Kontakte aus Bankkonten erstellen**
2. Legen Sie auf der geöffneten Anforderungsseite in den Abschnitten **Debitor**, **Kreditor** oder **Bankkonto** die Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.
3. Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.

Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen. Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung zugewiesen, die auf der Seite **Marketing & Vertrieb Einr.** festgelegt wurde.

> [!TIP]  
> Sie können dies auch andersherum tun, z. B. indem Sie einen Debitor, einen Kreditor oder ein Bankkonto aus einem Kontakt erstellen. Weitere Informationen finden Sie unter [So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>So erstellen Sie einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto aus einem Kontakt
Wenn Sie einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto für das Unternehmen haben, für das Sie einen Kontakt erstellen möchten, können Sie die Aktion **Erstellen als** verwenden. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen anschließend mit den verbundenen Debitoren-, Kreditoren-, Mitarbeiter- oder den Bankkontoinformationen synchronisiert. Weitere Informationen finden Sie unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Bevor Sie Debitoren, Kreditoren, Mitarbeiter oder Bankkonten aus Kontakten erstellen können, müssen Sie einen Geschäftsbeziehungscode auf der Seite **Marketingeinrichtung** im Inforegister **Interaktionen** angeben. Weitere Informationen finden Sie unter [Einrichten von Kontakten](marketing-setup-contacts.md).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kontakte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Kontakt aus, den Sie als Debitor, Kreditor, Mitarbeiter oder Bankkonto erstellen möchten.
3. Wählen Sie die Aktion **Erstellen als**, und wählen Sie denn entweder **Debitor**, **Kreditor**, **Bank** oder **Mitarbeiter**.
4. Wählen Sie die Schaltfläche **OK** aus.

Die Kontaktinformationen werden von der Kontaktkarte auf eine neue Debitoren-, Kreditoren-, Mitarbeiter- oder Bankkontenkarte übertragen. Sie können den einzelnen Karten spezifische Informationen, wie Fakturierungs- und Zahlungsdetails hinzufügen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>So verknüpfen Sie einen Kontakt mit einem vorhanden Debitor, Kreditor, Mitarbeiter oder einem Bankkonto
Wenn Sie einen Kontakt und entweder einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto für das gleiche Unternehmen haben, können Sie die beiden Entitäten verknüpfen, sodass Daten synchronisiert werden.

1. Öffnen Sie den Kontakt, den Sie verknüpfen möchten.
2. Wählen Sie die Aktion **Mit vorhandenem verknüpfen** aus, und wählen Sie dann die Aktion **Debitor**, **Kreditor**, **Bank**, oder **Mitarbeiter** aus.
3. Wählen Sie auf der Seite, die sich öffnet, den Debitor, Kreditor, Mitarbeiter oder das Bankkonto für die Verknüpfung aus.
4. Geben Sie im Feld **Felder übernehmen von** an, welche Felder im Fall von widersprüchlichen Informationen in den Feldern, die Kontakt und Debitor, Kreditor, Mitarbeiter und Bankkonto gemein haben, Priorität haben sollen. Wenn sich z. B. der Verkäufercode für den Kontakt und den Debitor unterscheidet, können Sie entscheiden, dass der eine auf der Kontaktkarte bleiben soll, indem Sie **Kontakt** auswählen.
5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>So entfernen Sie eine Verknüpfung zwischen einem Kontakt mit einem vorhanden Debitor, Kreditor, Mitarbeiter oder einem Bankkonto

Wenn Sie einen Kontakt und einen Kunden, Lieferanten, Mitarbeiter oder ein Bankkonto falsch verknüpft haben, entfernen Sie die Verknüpfung zwischen den Entitäten, damit die Daten nicht mehr synchronisiert werden.

1. Öffnen Sie den Kontakt mit dem falschen Link.  
2. Wählen Sie die Aktion **Geschäftsbeziehung** aus.  
3. Wählen Sie auf der Seite, die sich öffnet, den Debitor, Kreditor, Mitarbeiter oder das Bankkonto aus, für die Sie die Verknüpfung entfernen möchten.  
4. Wählen Sie die Aktion **Löschen** aus.  

> [!NOTE]  
> Verwenden Sie nicht das Fenster **Geschäftsbeziehungen** zum Ändern bestehender Beziehungen. Entfernen Sie stattdessen die Beziehung und verwenden Sie die Aktion **Verknüpfung mit bestehenden**. Weitere Informationen finden Sie im Abschnitt [So verknüpfen Sie einen Kontakt mit einem vorhandenen Kunden, Lieferanten oder Bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Synchronisieren von Kontakten mit Debitoren, Kreditoren, Mitarbeitern und Bankkonten
Wenn einige Ihrer Kontakte auch Debitoren, Kreditoren, Mitarbeiter oder Bankkonten sind, können Sie diese dann mit Daten aus dem Kontakt synchronisieren und die folgenden Vorteile gewinnen:

* Sie müssen die Informationen nur an einer Stelle aktualisieren. Wenn Sie z. B. die Telefonnummer des Kontakts ändern, wird die Telefonnummer automatisch für den Debitor, Kreditor, Mitarbeiter oder das Bankkonto geändert.
* Wenn Sie beim Erstellen einer Debitoren-, Kreditoren-, Mitarbeiter- oder Bankkontokarte eine Nummernserie für Kontakte angegeben haben, wird automatisch ein Kontakt erstellt.
* Über den Kontakt können Sie Verkaufsangebote und -aufträge sowie Einkaufsanfragen und –aufträge erstellen.
* Sie können Ihre Interaktionen erfassen, wie z. B. das Drucken von Aufträgen, Rahmenaufträgen, das Erstellen von Verkaufsserviceaufträgen, das Senden von E-Mails, usw.
* Wenn Sie einen Kontakt löschen, der mit einem Debitor, Kreditor, Mitarbeiter oder Bankkonto verknüpft ist, wird nur der Kontakt entfernt. Der Debitor, Kreditor, Mitarbeiter oder das Bankkonto bleibt erhalten.
* Wenn Sie einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto löschen, der bzw. das mit einem Kontakt verknüpft ist, bleibt der Kontakt erhalten.

> [!NOTE]  
> Bestimmte Informationen, wie Fakturierungs- und Buchungsdetails, sind für Kontakte nicht verfügbar. Wenn Sie Kontakte als Debitoren, Kreditoren, Mitarbeiter oder Bankkonten erstellen, möchten Sie diese möglicherweise manuell hinzufügen.

Es gibt drei Möglichkeiten, die Datensynchronisierung zwischen Kontakten und Debitoren, Kreditoren, Mitarbeitern und Bankkonten zu aktivieren:

* Wenn Sie Kontakte aus Debitoren, Kreditoren, Mitarbeitern oder Bankkonten erstellen. Siehe auch [So erstellen Sie einen Kontakt aus einem Debitor, Kreditor oder Bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Wenn Sie Debitoren, Kreditoren, Mitarbeiter oder Bankkonten aus Kontakten erstellen. Siehe auch [So erstellen Sie einen Debitor, Kreditor oder ein Bankkonto aus einem Kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Wenn Sie Kontakte mit bestehenden Debitoren, Kreditoren, Mitarbeitern oder Bankkonten von der Kontaktkarte verknüpfen. Siehe auch [Verknüpfen eines Kontakts mit einem vorhanden Debitor, Kreditor oder Konto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>So sehen Sie, mit welchem Debitor, Kreditor, Mitarbeiter oder Bankkonto ein Kontakt verknüpft ist
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Kontakte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Zeile für einen Kontakt aus, wählen Sie die Aktion **Verknüpfte Informationen** und dann die Aktion **Debitor/Kreditor/Bankkonto/Mitarbeiter** aus.

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Kontakte einrichten](marketing-setup-contacts.md)  
[Arbeiten mit Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]