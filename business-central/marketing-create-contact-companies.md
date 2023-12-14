---
title: Erstellen Sie Geschäftskontakte
description: 'Umreißt die Aufgaben, die zum Erstellen von Kontakten und der Definition Ihrer Geschäftsbeziehungen auf der Kontaktkarte erforderlich sind.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.date: 08/30/2022
ms.author: bholtorf
---
# <a name="create-contacts"></a>Kontakt erstellen

Wenn Sie eine Geschäftsbeziehung mit jemandem in einem anderen Unternehmen aufbauen, fügen Sie ihn als Kontakt hinzu [!INCLUDE[prod_short](includes/prod_short.md)]. Fügen Sie dann alle Informationen über sie oder das Unternehmen hinzu, die für die zukünftige Kommunikation nützlich sein könnten. Auf der Seite **Kontaktkarte** können Sie die folgenden Arten von Kontakten erstellen:

* **Person** – Verwenden, wenn Sie in diesem Fall direkten Kontakt zu jemandem haben und Sie haben dessen Kontaktdaten.
* **Unternehmen** – Verwenden Sie dies, wenn beispielsweise der Kontakt keine Einzelperson ist, sondern eine juristische Person, wie ein Auftragnehmer oder eine Bank.

Die Informationen, die für jeden Kontakttyp relevant sind, sind unterschiedlich, somit sind die verfügbaren Felder und Aktionen unterschiedlich. Beispielsweise können Sie Projektverantwortlichkeiten nur einer Person und eine Branche nur einem Unternehmen zuweisen.

Sie können manuellen Änderungen im Feld **Art** später vornehmen. Alternativ können Sie die Felder im Inforegister **Übernahme** auf der Seite **Marketing-Einrichtung** verwenden, um die Daten anzugeben, die zwischen einer Person und ihrem Unternehmen geteilt werden sollen. Erfahren Sie mehr unter [Kontakte einrichten](marketing-setup-contacts.md).

Wenn beispielsweise ein Kontakt in einen Debitor umgewandelt wird, wird die Kontaktperson oder das Kontaktunternehmen zum Namen des Debitors. Der Datensatz für den Kontakt wird beibehalten, und Sie können den Kontakt und den Debitor so verknüpfen, dass deren Daten künftig synchronisiert werden.

> [!NOTE]
> Wenn Sie die [Funktion Update für Konvertierungsvorlagen](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees) einschalten, dann können Sie auch Kreditoren oder Mitarbeiter aus Geschäftskontakten erstellen.
>
> Wenn Sie jedoch bereits die integrierte Funktion zum automatischen Erstellen von Debitoren oder Artikeln verwenden, dann unterstützt dieses Funktions-Update keine angepassten Felder, und neu erstellte Debitoren oder Artikel enthalten diese Daten nicht.

## <a name="to-create-a-contact-manually"></a>So werden Kontakte manuell erstellt:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kontakte** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.
3. Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.

   Wenn Sie andererseits auf der Seite **Marketingsetup** eine Nummernserie für Kontakte eingerichtet haben, können Sie die <kbd>EINGABETASTE</kbd> auswählen, um die nächste verfügbare Kontaktnummer einzufügen.
4. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>So erstellen Sie einen Kontakt aus einem Debitor, Kreditor oder Bankkonto

Wenn Sie vorhandene Debitoren, Kreditoren und Bankkonten haben, für die Sie Kontaktkarten erstellen möchten, können Sie die Stapelverarbeitungen **Kontakte erstellen von** verwenden. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen später mit den verbundenen Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert. Erfahren Sie mehr unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren, Mitarbeitern und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Bevor Sie Kontakte basierend auf vorhandenen Daten erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auf dem Inforegister **Interkationen** auf der Seite **Marketingeinrichtung** angeben. Erfahren Sie mehr unter [Kontakte einrichten](marketing-setup-contacts.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie eine der folgenden Angaben ein, die mit der Entität übereinstimmt, woraus Sie Kontakte erstellen möchten, und wählen Sie dann den entsprechenden Link.
   * **Kontakte aus Debitoren erstellen**
   * **Kontakte aus Kreditoren erstellen**
   * **Kontakte aus Bankkonten erstellen**
2. Legen Sie auf der geöffneten Anforderungsseite in den Abschnitten **Debitor**, **Kreditor** oder **Bankkonto** die Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.
3. Klicken Sie auf **OK**, um mit der Erstellung der Kontakte zu beginnen.

Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen. Den neu erstellten Kontakten wird automatisch der Geschäftsbeziehungscode zugewiesen, der auf der Seite **Marketing & Vertrieb Einr.** festgelegt wurde.

> [!TIP]  
> Sie können dies auch andersherum tun, z. B. indem Sie einen Debitor, einen Kreditor, einen Mitarbeiter oder ein Bankkonto aus einem Kontakt erstellen. Weitere Informationen finden Sie unter [Erstellen eines Kunden, Kreditors, Mitarbeiters oder Bankkontos über einen Kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>So erstellen Sie einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto aus einem Kontakt

Wenn Sie einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto für das Unternehmen haben, für das Sie einen Kontakt erstellen möchten, können Sie die Aktion **Erstellen als** verwenden. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen später mit den verbundenen Debitoren-, Kreditoren-, Mitarbeiter- oder den Bankkontoinformationen synchronisiert. Erfahren Sie mehr unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).<!--Should this link include "Employees" as per the section title below?-->

> [!NOTE]  
> Bevor Sie Debitoren, Kreditoren, Mitarbeiter oder Bankkonten aus Kontakten erstellen können, müssen Sie einen Geschäftsbeziehungscode auf der Seite **Marketingeinrichtung** im Inforegister **Interaktionen** angeben. Erfahren Sie mehr unter [Kontakte einrichten](marketing-setup-contacts.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontakte** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Kontakt aus, den Sie als Debitor, Kreditor, Mitarbeiter oder Bankkonto erstellen möchten.
3. Wählen Sie die Aktion **Erstellen als**, und wählen Sie denn entweder **Debitor**, **Kreditor**, **Bank** oder **Mitarbeiter**.
4. Wählen Sie **OK** aus.

Die Kontaktinformationen werden von der Kontaktkarte auf eine neue Debitoren-, Kreditoren-, Mitarbeiter- oder Bankkontenkarte übertragen. Sie können den einzelnen Karten spezifische Informationen, wie Fakturierungs- und Zahlungsdetails hinzufügen. Beispiel: Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>So verknüpfen Sie einen Kontakt mit einem vorhanden Debitor, Kreditor, Mitarbeiter oder einem Bankkonto

Wenn Sie einen Kontakt und entweder einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto für das gleiche Unternehmen haben, können Sie die beiden Entitäten verknüpfen, sodass Daten synchronisiert werden.

1. Öffnen Sie den Kontakt, den Sie verknüpfen möchten.
2. Wählen Sie die Aktion **Mit vorhandenem verknüpfen** aus, und wählen Sie dann die Aktion **Debitor**, **Kreditor**, **Bank**, oder **Mitarbeiter** aus.
3. Wählen Sie auf der Seite, die sich öffnet, den Debitor, Kreditor, Mitarbeiter oder das Bankkonto für die Verknüpfung aus.
4. Geben Sie im Feld **Felder übernehmen von** an, welche Felder im Fall von widersprüchlichen Informationen in den Feldern, die Kontakt und Debitor, Kreditor, Mitarbeiter und Bankkonto gemein haben, Priorität haben sollen. Wenn sich z. B. der Verkäufercode für den Kontakt und den Debitor unterscheidet, können Sie entscheiden, dass der eine auf der Kontaktkarte bleiben soll, indem Sie **Kontakt** auswählen.
5. Wählen Sie **OK** aus.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>So entfernen Sie eine Verknüpfung zwischen einem Kontakt mit einem vorhanden Debitor, Kreditor, Mitarbeiter oder einem Bankkonto

Wenn Sie einen Kontakt mit einem Kunden, Lieferanten, Mitarbeiter oder Bankkonto falsch verknüpft haben, entfernen Sie die Verknüpfung zwischen den Entitäten, damit die Daten nicht mehr synchronisiert werden.

1. Öffnen Sie den Kontakt mit dem falschen Link.  
2. Wählen Sie die Aktion **Geschäftsbeziehung** aus.  
3. Wählen Sie auf der Seite, die sich öffnet, den Debitor, Kreditor, Mitarbeiter oder das Bankkonto aus, für die Sie die Verknüpfung entfernen möchten.  
4. Wählen Sie die Aktion **Löschen** aus.  

> [!NOTE]  
> Verwenden Sie nicht das Fenster **Geschäftsbeziehungen** zum Ändern bestehender Beziehungen. Entfernen Sie stattdessen die Beziehung und verwenden Sie die Aktion **Verknüpfung mit bestehenden**. Weitere Informationen finden Sie unter [So verknüpfen Sie einen Kontakt mit einem vorhandenen Kreditor, Debitor, Mitarbeiter oder Bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Synchronisieren von Kontakten mit Debitoren, Kreditoren, Mitarbeitern und Bankkonten

Wenn einige Ihrer Kontakte auch Debitoren, Kreditoren, Mitarbeiter oder Bankkonten sind, können Sie diese dann mit Daten aus dem Kontakt synchronisieren und die folgenden Vorteile gewinnen:

* Sie müssen die Informationen nur an einer Stelle aktualisieren. Wenn Sie z. B. die Telefonnummer des Kontakts ändern, wird die Telefonnummer automatisch für den Debitor, Kreditor, Mitarbeiter oder das Bankkonto aktualisiert.
* Wenn Sie beim Erstellen einer Debitoren-, Kreditoren-, Mitarbeiter- oder Bankkontokarte eine Nummernserie für Kontakte angegeben haben, wird automatisch ein Kontakt erstellt.
* Über den Kontakt können Sie Verkaufsangebote und -aufträge sowie Einkaufsanfragen und –aufträge erstellen.
* Sie können Ihre Interaktionen erfassen, wie z. B. das Drucken von Aufträgen, Rahmenaufträgen, das Erstellen von Verkaufsserviceaufträgen, das Senden von E-Mails, usw.
* Wenn Sie einen Kontakt löschen, der mit einem Debitor, Kreditor, Mitarbeiter oder Bankkonto verknüpft ist, wird nur der Kontakt entfernt. Der Debitor, Kreditor, Mitarbeiter oder das Bankkonto bleibt erhalten.
* Ähnlich, wenn Sie einen Debitor, Kreditor, Mitarbeiter oder ein Bankkonto löschen, der bzw. das mit einem Kontakt verknüpft ist, bleibt der Kontakt erhalten.

> [!NOTE]  
> Bestimmte Informationen, wie Fakturierungs- und Buchungsdetails, sind für Kontakte nicht verfügbar. Wenn Sie Kontakte als Debitoren, Kreditoren, Mitarbeiter oder Bankkonten erstellen, möchten Sie diese Informationen möglicherweise manuell hinzufügen.

Es gibt drei Möglichkeiten, die Datensynchronisierung zwischen Kontakten und Debitoren, Kreditoren, Mitarbeitern und Bankkonten zu aktivieren:

* Wenn Sie Kontakte aus Debitoren, Kreditoren oder Bankkonten erstellen. Weitere Informationen finden Sie unter [Erstellen eines Kontakts aus Debitoren, Kreditoren, Mitarbeiter oder Bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Wenn Sie Debitoren, Kreditoren, Mitarbeiter oder Bankkonten aus Kontakten erstellen. Weitere Informationen finden Sie unter [Erstellen eines Kunden, Kreditors, Mitarbeiters oder Bankkontos über einen Kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Wenn Sie Kontakte mit bestehenden Debitoren, Kreditoren, Mitarbeitern oder Bankkonten von der Kontaktkarte verknüpfen. Weitere Informationen finden Sie unter [So verknüpfen Sie einen Kontakt mit einem vorhandenen Kreditor, Debitor, Mitarbeiter oder Bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>So sehen Sie, mit welchem Debitor, Kreditor, Mitarbeiter oder Bankkonto ein Kontakt verknüpft ist

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kontakte** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Zeile für einen Kontakt aus, wählen Sie die Aktion **Verknüpfte Informationen** und dann die Aktion **Debitor/Kreditor/Bankkonto/Mitarbeiter** aus.

## <a name="see-also"></a>Siehe auch

[Kontakte verwalten](marketing-contacts.md)  
[Kontakte einrichten](marketing-setup-contacts.md)  
[Verwenden Sie Online-Karten, um Standorte und Wegbeschreibungen zu finden](across-online-maps.md)  
[Arbeiten mit Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
