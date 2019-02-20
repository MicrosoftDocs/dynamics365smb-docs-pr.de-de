---
title: Erstellen von Kontaktunternehmen| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: de-de
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Kontaktunternehmenerstellen
Ihr Unternehmen trifft regelmäßig mit anderen interessierten Unternehmen zusammen. Aus diesen Zusammentreffen ergeben sich in der Regel neue Geschäftsbeziehungen. Wird ein neuer Kontakt geknüpft, muss diese Information erfasst werden, um eine weitere Kommunikation zu ermöglichen.

Für eine effiziente Kommunikation empfiehlt es sich, einem bestimmten Unternehmen möglichst viele Daten zuzuordnen. So wird beispielsweise durch Zuordnen der jeweiligen Branche sichergestellt, dass bestimmte Unternehmen in für sie relevante Kommunikation einbezogen werden.

Darüber hinaus können Sie definieren, welche Geschäftsbeziehung mit einem Kontakt besteht. So kann es sich bei einem Kontakt beispielsweise um einen Interessenten, um eine Bank oder um einen Vertragsnehmer handeln.

## <a name="creatinge-contact-companies"></a>Kontaktunternehmen erstellen
Sie können für jedes neue Unternehmen, mit dem Sie Geschäfte machen, eine Kontaktkarte anlegen. Das können z. B. Debitoren, Kreditoren, Interessenten, Banken, Rechtsanwälte, Berater usw. sein.

Es gibt zwei Möglichkeiten, um einen Kontakt zu erstellen: von Grund auf neu oder aus einem bestehenden Debitor, Kreditor oder Bankkonto.

Bevor Sie einen Kontakt anlegen, können Sie die Einstellungen auf der Seite  **Marketing einrichten** überprüfen. Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)

### <a name="to-create-a-company-contact-from-scratch"></a>Einen Unternehmenskontakte von Grund auf erstellen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.

    Wenn Sie auf der Seiter **Marketing und Vertrieb einrichten** eine Nummernserie für Kontakte eingegeben haben, können Sie alternativ auch die EINGABETASTE drücken, um die nächste verfügbare Kontaktnummer auszuwählen.  
4. Legen Sie **Art** auf **Unternehmen** fest.
5. Füllen Sie die weiteren Felder wie erforderlich aus.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto
Wenn Sie bereits eine Anzahl von Debitoren, Kreditoren und Bankkonten eingerichtet haben, können Sie Kontakte auf der Basis von bestehenden Daten erstellen. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen mit dem Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert.

> [!NOTE]  
>   Bevor Sie auf diese Weise ein Kontaktunternehmen erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auf der Seite **Marketingeinrichtung** angeben. Wenn Sie Kontakte aus Bankkonten erstellen, müssen Sie Nummernserie für Bankkonten auf der Seite **Finanzbuchhaltungseinrichtung** angeben.

1. Wählen Sie ![Glühlampe, die die Funktion "Teilen Sie mir mit, was Sie tun wollen"](media/ui-search/search_small.png "\"Teilen Sie mir mit, was Sie tun wollen\"") und Folgendes ein, je nachdem, von wo aus Sie Kontakte erstellen möchten, und wählen Sie dann den zugehörigen Link aus.
   * **Kontakte aus Debitoren erstellen**
   * **Kontakte aus Kreditoren erstellen**
   * **Kontakte aus Bankkonten erstellen**
2. Legen Sie im Abschnitt **Debitor**, **Kreditor** oder **Bankkonto** der Stapelverarbeitungsseite den Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.
3. Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.

    Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen. Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung für Kreditoren zugewiesen, die auf der Seite **Marketing & Vertrieb Einr.** festgelegt wurde.

> [!TIP]  
>   Sie können auch einen Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten
Wenn einige Ihrer Kontakte auch Debitoren, Kreditoren oder Bankkonten sind, können Sie deren Kontaktinformationen mit dem entsprechenden Debitor, Kreditor oder Bankkonto synchronisieren. Die Synchronisierung macht Informationen, die zwischen Kontakten und Debitoren, Kreditoren oder Bankkonto gleich sind, identisch.  

Bevor Sie Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten synchronisieren, müssen Sie auf der Seite **Marketing & Vertrieb Einr.** einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten festlegen. Weitere Informationen finden Sie unter [Einrichten von Relationship Management](marketing-setup-marketing.md)

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Unterschiedliche Wege, um Kontakte mit Debitoren, Kreditoren und Bankkonten zu synchronisieren
Sie können Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten synchronisieren, indem Sie eine der folgenden drei Methoden verwenden:

* Verknüpfen Sie Kontakte auf der Kontaktkarte mit bestehenden Debitoren, Kreditoren oder Bankkonten. Weitere Informationen finden Sie unter [Kontakte mit Debitoren, Kreditoren und Bankkonten synchronisieren](marketing-how-link-contact.md).
* Erstellen Sie Debitoren, Kreditoren oder Bankkonten über den Kontakt. Weitere Informationen finden Sie unter [Debitor, Kreditor oder Bankkonto über einen Kontakt erstellen](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Erstellen Sie Kontakte aus Debitoren, Kreditoren oder Bankkonten. Weitere Informationen finden Sie unter [Erstellen eines Unternehmenskontakts aus einem Debitor, Kreditor oder Bankkonto](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Ergebnisse der Synchronisierung
Wenn der Kontakt mit dem Debitor, Kreditor oder Bankkonto synchronisiert ist:

* Sie müssen die Informationen nur an einer Stelle aktualisieren. Wenn Sie z. B. die Telefonnummer auf des Kontakts ändern, wird die Telefonnummer auf des Debitors-, Kreditors oder Bankkontos automatisch mit der gleichen Änderung aktualisiert.
* Wenn Sie beim Erstellen einer Debitoren-, Kreditoren- oder Bankkontokarte eine Nummernserie für Kontakte angegeben haben, wird automatisch eine Kontaktkarte für den Debitor, den Kreditor bzw. das Bankkonto erstellt.
* Über den Kontakt können Sie Verkaufsangebote und -Aufträge, Einkaufsanfragen und –Aufträge erstellen.
* Sie können Ihre Aktivitäten beim Durchführen von Aktionen erfassen lassen, z. B. das Drucken von Aufträgen oder Rahmenbestellungen, Erstellen von Verkaufsserviceaufträgen, Senden von E-Mails usw.
* Wenn Sie einen Kontakt löschen, der mit einem Debitor, Kreditor oder Bankkonto verknüpft ist, wird nur der Kontakt entfernt. Der Debitor, Kreditor oder das Bankkonto bleibt erhalten.
* Wenn Sie einen Debitor, einen Kreditor oder ein Bankkonto löschen, der bzw. das mit einem Kontakt verknüpft ist, bleibt der Kontakt erhalten.

> [!NOTE]  
>   Einige Informationen, wie Fakturierungs- und Buchungsdetails, erscheinen nicht auf der Kontaktkarte. Sie können sie manuell auf der Debitoren-, Kreditoren- und/oder Bankkontenkarte hinzufügen, wenn Sie Kontakte als Debitoren, Kreditoren oder Bankkonten erstellen.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisation von Kontakten mit Debitoren, Kreditoren und Bankkonten.
Wenn Sie Kontakt und entweder einen Debitor, Kreditor oder ein Bankkonto für das gleiche Unternehmen haben, können Sie die beiden Einheiten verknüpfen. Das Verknüpfen der beiden Einheiten ermöglicht Ihnen gemeinsame Daten zu synchronisieren, sodass diese an beiden Stellen identisch sind.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Verknüpfen eines Kontakts mit einem vorhanden Debitor, Kreditor oder Konto
1. Öffnen Sie den Kontakt, den Sie verknüpfen möchten.
2. Wählen Sie die Aktion **Mit vorhandenem verknüpfen** aus, und wählen Sie dann **Debirot**, **Kreditor** oder **Bank**.
3. Wählen Sie den Debitor, Kreditor oder das Bankkonto für die Verknüpfung aus.

   Legen Sie im Feld **Felder übernehmen von** fest, welche Felder im Konfliktfall Priorität haben sollen. Wenn sich z. B. der Verkäufercode im Kontakt von dem des Kredtors unterscheidet, können Sie entscheiden, dass die gültige Information aus dem Kontakt übernommen werden soll, indem Sie **Kontakt** auswählen.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Erstellen eines Kreditors, Debitors oder Bankkontos über einen Kontakt
   Sie können vorhandene Kontakte als Debitoren, Kreditoren oder als Bankkonten erfassen. Beim Erstellen eines Kreditors, Debitors oder Bankkontos aus einem Kontakt können Sie vorhandene Daten verwenden. Wenn Sie einen Debitor, Kreditor oder ein Bankkonto auf diese Weise erstellen, wird es mit dem Kontakt synchronisiert Die Synchronisierung macht Informationen, die zwischen Kontakten und Debitoren, Kreditoren oder Bankkonto gleich sind, identisch.

   **Hinweis**: Bevor Sie auf diese Weise ein erfassen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auf der Seite Marketingeinrichtung angeben. Wenn Sie Kontakte als Bankkonten erfassen, müssen Sie Nummernserie für Bankkonten auf der Seite **Finanzbuchhaltungseinrichtung** angeben.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto
   1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.
   2. Wählen Sie den Kontakt aus, den Sie als Debitor, Kreditor oder Bankkonto erstellen möchten.
   3. Wählen Sie die Aktionen **Erstellen als**, und wählen Sie denn entweder **Debitor**, **Kreditor** oder **Bank**.
   4. Bestätigen Sie die nachfolgende Meldung.

   Die Kontaktinformationen werden von der Karte **Kontakt** auf die Karte **Bankkonto**, die Karte **Debitor** oder die Karte **Kreditor** übertragen. Sie können den einzelnen Karten spezifische Informationen, wie Fakturierungs- und Zahlungsdetails hinzufügen.

## <a name="setting-up-business-relations-on-contact-companies"></a>Einrichten von Geschäftsbeziehungen für Kontaktunternehmen
Sie können Geschäftsbeziehungen verwenden, um die Geschäftsbeziehung anzuzeigen, die Sie mit Ihren Kontakten haben wie z. B. Interessent, Bank, Berater und Dienstleister usw. pflegen.

Die Nutzung von Geschäftsbeziehungen zu Kontakten ist ein zwei Schritte umfassender Prozess. Zuerst definieren Sie den Geschäftsbeziehungscode. Sie müssen diesen Schritt nur einmal für jede Geschäftsbeziehung ausführen. Sobald Sie einen Geschäftsbeziehungscode haben, können Sie den Code zu den Kontaktunternehmen zuweisen.

> [!NOTE]  
>   Wenn Sie planen, Ihre Kontakte mit Debitoren, Kreditoren oder Bankkonten in anderen Teilen der Anwendung zu synchronisieren, können Sie für sie eine Geschäftsbeziehung erstellen.

### <a name="to-define-a-business-relation-code"></a>Definieren eines Geschäftsbeziehungscodes
Der Geschäftsbeziehungscode definiert eine Kategorie oder einen Typ von Geschäftsbeziehung wie BANK oder Gesetz. Sie können mehrere Geschäftsbeziehungscodes haben. Um die Geschäftsbeziehung zu definieren, verwenden Sie die Seite **Geschäftsbeziehungen**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Geschäftsbeziehung** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus, und geben Sie einen Code und eine Beschreibung ein. Der Code kann maximal 11 Zeichen, sowohl Ziffern als auch Buchstaben, umfassen.

### <a name="AssignBusRelContact">Um Kontakten Geschäftsbeziehungen zuzuordnen:</a>
Sie können Geschäftsbeziehungen nicht zu Personen zuordnen – nur zu Unternehmen.

1. Öffnen Sie den Kontakt.
2. Wählen Sie die Aktion **Unternehmen** und dann die **Geschäftsbeziehungen**-Aktion aus.

    Die Seite **Kontakt Geschäftsbeziehungen** wird angezeigt.
3. Wählen Sie im Feld **Geschäftsbeziehungscode** die Geschäftsbeziehung aus, die Sie zuordnen möchten.

Wiederholen Sie diese Schritte, um beliebig viele Geschäftsbeziehungen zuzuordnen. Außerdem können Sie Geschäftsbeziehungen auf die gleiche Art in dem Fenster Kontaktübersicht zuordnen.

Die Anzahl der Geschäftsbeziehungen, die Sie dem Kontakt auf der Kontaktkarte zugeordnet haben, wird im Feld **Anzahl Geschäftsbeziehungen** im Abschnitt **Segmentierung** auf der Seite **Kontakt** angezeigt.

Nachdem Sie Ihren Kontakten Geschäftsbeziehungen zugeordnet haben, können Sie diese Informationen verwenden, um Kontakte für Ihre Segmente auszuwählen. Weitere Informationen finden Sie unter [Hinzufügen von Kontakten zu Segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Siehe auch
[Kontaktpersonenerstellen](marketing-create-contact-persons.md)   
[Arbeiten mit Business Central](ui-work-product.md)

