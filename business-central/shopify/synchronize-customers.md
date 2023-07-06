---
title: Debitoren synchronisieren
description: Import von Debitoren von oder Export von Debitoren nach Shopify durchführen
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# <a name="synchronize-customers"></a><a name="synchronize-customers"></a><a name="synchronize-customers"></a>Debitoren synchronisieren

Wenn ein Auftrag aus Shopify importiert wird, sind die Informationen über den Kunden für die weitere Verarbeitung des Dokuments in [!INCLUDE[prod_short](../includes/prod_short.md)] unerlässlich. Dafür stehen zwei Hauptoptionen und ihre Kombinationen zur Verfügung:

* Verwenden Sie einen speziellen Kunden für alle Bestellungen.
* Importieren Sie die tatsächlichen Kundeninformationen aus Shopify. Diese Option steht auch zur Verfügung, wenn Sie Kunden zuerst nach Shopify von [!INCLUDE[prod_short](../includes/prod_short.md)] exportieren.

## <a name="important-settings-when-importing-customers-from-shopify"></a><a name="important-settings-when-importing-customers-from-shopify"></a><a name="important-settings-when-importing-customers-from-shopify"></a>Wichtige Einstellungen beim Import von Debitoren aus Shopify

Ob Sie nun Debitoren aus Shopify in großen Mengen oder Bestellungen importieren: Verwenden Sie folgende Einstellungen, um den Vorgang zu verwalten:

|Feld|Beschreibung|
|------|-----------|
|**Debitorenimport aus Shopify**|Wählen Sie **Alle Kunden**, wenn Sie Kunden aus Shopify in großen Mengen importieren möchten; entweder manuell mit der Aktion **Kunden synchronisieren** oder über die Auftragswarteschlange für wiederkehrende Aktualisierungen. Unabhängig von der Auswahl werden die Kundeninformationen immer zusammen mit der Bestellung importiert. Die Verwendung dieser Information hängt jedoch von den **Shopify Kundenvorlagen** und den Einstellungen im Feld **Kundenzuordnungstyp** ab.|
|**Kundenzuordnungstyp**|Legen Sie fest, wie der Konnektor die Zuordnung vornehmen soll.<br>- **Nach E-Mail/Telefon**, wenn Sie möchten, dass der Konnektor den importierten Shopify-Kunden anhand von E-Mail und Telefon einem bestehenden Kunden in [!INCLUDE[prod_short](../includes/prod_short.md)] zuordnet.</br>- **Nach Rechnungsinformationen**, wenn Sie möchten, dass der Konnektor die Adresse des Rechnungsempfängers verwenden, um den importierten Shopify-Debitor einem bestehenden Debitor in [!INCLUDE[prod_short](../includes/prod_short.md)] zuzuordnen und dabei die Adressinformationen der Partei verwendet, die die Rechnung erhält.</br>- Wählen Sie **Immer den Standarddebitoren nehmen**, wenn Sie möchten, dass das System einen Debitoren aus der **Standarddebitorennr.** verwendet Feld |
|**Shopify Kann Debitoren aktualisieren**| Wählen Sie dieses Feld, ob der Konnektor gefundene Debitoren aktualisieren soll, wenn die Optionen **Nach E-Mail/Telefon** oder **Nach Rechnungsinformationen** im Feld **Debitorzuordnungstyp** ausgewählt sind.|
|**Unbekannte Debitoren automatisch erstellen**| Wählen Sie dieses Feld, ob der Konnektor fehlende Debitoren erstellen soll, wenn die Optionen **Nach E-Mail/Telefon** oder **Nach Rechnungsinformationen** im Feld **Debitorzuordnungstyp** ausgewählt sind. Ein neuer Kunde wird anhand der importierten Daten und des **Kundenvorlagencodes** erstellt, der auf den Seiten **Shopify Shop-Karte** oder **Shopify Kundenvorlage** definiert ist. Beachten Sie, dass der Shopify-Debitor über mindestens eine Adresse verfügen muss. Bei Bestellungen, die über den Shopify-Vertriebskanal POS erstellt wurden, fehlen häufig Adressangaben. Wenn diese Option nicht aktiviert ist, müssen Sie einen Debitoren manuell erstellen und mit dem Debitor Shopify verknüpfen.|
|**Debitorenvorlagencode**|Dieses Feld wird zusammen mit **Unbekannte Debitoren automatisch erstellen** verwendet.<br>- Wählen Sie die Standardvorlage aus, die für automatisch erstellte Debitoren verwendet werden soll. Stellen Sie sicher, dass die ausgewählte Vorlage die obligatorischen Felder enthält, wie z.B. **Gen. Geschäftsbuchungsgruppe**, **Debitorbuchungsgruppe**, MwSt.- oder steuerbezogene Felder.<br>- Auf der Seite **Shopify Debitorenvorlagen** können Sie Vorlagen pro Land/Region definieren, was für eine korrekte Steuerberechnung nützlich ist. <br>- Erfahren Sie mehr unter [Steuern festlegen](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a><a name="customer-template-per-country"></a><a name="customer-template-per-country"></a>Debitorenvorlage pro Land

Einige Einstellungen können auf der Ebene eines Landes/Region oder eines Staates/Provinz festgelegt werden. Die Einstellungen können unter [Versand und Lieferung](https://www.shopify.com/admin/settings/shipping) in Shopify festgelegt werden.

Mit der **Shopify-Debitorenvorlage** können Sie die folgenden Schritte für jeden Debitor ausführen:

1. Geben Sie die **Standarddebitorennr.** an, die Vorrang vor der Auswahl in den Feldern **Debitorenimport aus Shopify** und **Debitorenzuordnungstyp** hat. Sie wird im importierten Verkaufsauftrag verwendet.
2. Definieren Sie den **Kundenvorlagencode**, mit dem fehlende Kunden erstellt werden, wenn **Unbekannte Kunden automatisch erstellen** aktiviert ist. Wenn der **Kundenvorlagencode** leer ist, dann verwendet die Funktion den **Kundenvorlagencode**, der auf der **Shopify Shop-Karte** definiert ist.
3. Legen Sie fest, ob die Preise für importierte Bestellungen Steuern/MwSt. enthalten.
4. In manchen Fällen ist der für ein Land definierte **Debitorvorlagencode** nicht ausreichend, um die korrekte Berechnung der Steuern zu gewährleisten (z. B. für Länder mit Umsatzsteuer). In diesem Fall könnte **Steuerbereiche** eine nützliche Ergänzung sein.
5. Das Feld **Steuergebiet** enthält auch einen **Ländercode** und einen **Bezirksnamen** Paar. Dieses Paar ist nützlich, wenn der Connector einen Code in einen Namen umwandeln muss oder umgekehrt.

> [!NOTE]  
> Die Ländercodes sind Ländercodes nach ISO 3166-1 Alpha 2. Erfahren Sie mehr unter [Ländercode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a><a name="export-customers-to-shopify"></a><a name="export-customers-to-shopify"></a>Debitoren nach Shopify exportieren

Sie können bestehende Debitoren in Shopify in großen Mengen exportieren. In jedem Fall werden ein Debitor und eine Standardadresse erstellt. Der Prozess kann mit den folgenden Einstellungen verwaltet werden:

|Feld|Beschreibung|
|------|-----------|
|**Debitoren nach Shopify** exportieren|Wählen Sie diese Option, wenn Sie alle Debitor von [!INCLUDE[prod_short](../includes/prod_short.md)] nach Shopify in großen Mengen exportieren möchten. Sie können dies entweder manuell tun, indem Sie die Aktion **Debitoren synchronisieren** oder automatisch mithilfe einer Auftragswarteschlange für wiederkehrende Aktualisierungen verwenden.<br> Stellen Sie sicher, wenn Sie Debitoren mit Adressen, die Provinzen/Staaten beinhalten exportieren, dass der **ISO-Code** für Länder/Regionen ausgefüllt ist.|
|**Kann Shopify-Debitoren aktualisieren**|Diese Option funktioniert mit der Einstellung **Debitor nach Shopify exportieren**. Aktivieren Sie die Option, wenn Sie später Aktualisierungen aus [!INCLUDE[prod_short](../includes/prod_short.md)] für Kunden erstellen möchten, die bereits in Shopify vorhanden sind.|

Für den Export eines Debitors gelten die folgenden Voraussetzungen:

* Der Debitor muss eine gültige E-Mail-Adresse haben.
* Auf der Karte des Debitors ist ein Land/Region ausgewählt, bei lokalen Kunden mit leerem Land/Region muss für das auf der Seite **Unternehmensdaten** angegebene Land/Region ein ISO-Code definiert sein.
* Wenn der Debitor eine Telefonnummer hat, muss die Nummer eindeutig sein, denn Shopify akzeptiert keinen zweiten Debitor mit derselben Telefonnummer.
* Wenn der Debitor eine Telefonnummer hat, muss diese im E.164-Format vorliegen. Andere Formate werden unterstützt, wenn sie eine Nummer darstellen, die von überall auf der Welt gewählt werden kann. Die folgenden Formate sind gültig:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Nachdem Sie die Debitor in Shopify erstellt haben, können Sie ihnen direkte Einladungen schicken, um sie zur Aktivierung ihrer Konten zu bewegen.

### <a name="populate-customer-information-in-shopify"></a><a name="populate-customer-information-in-shopify"></a><a name="populate-customer-information-in-shopify"></a>Debitoreninformationen in Shopify ausfüllen

In Shopify verfügt ein Debitor über einen Vornamen, einen Nachnamen, eine E-Mail-Adresse und/oder eine Telefonnummer. Sie können die Vor- und Familiennamen aus der Kundenkarte in [!INCLUDE[prod_short](../includes/prod_short.md)] eingeben.

|Priorität|Feld in der Kundenkarte|Description|
|------|------|-----------|
|0|**Kontaktname**|Höchste Priorität, wenn das Feld **Kontaktname** ausgefüllt und das Feld **Kontaktquelle** auf der **Shopify-Shop-Karte** entweder die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|
|2|**Name 2**|Wenn das Feld **Name 2** ausgefüllt und das Feld **Quelle von Name 2** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|
|3|**Name**|Niedrigste Priorität, wenn das Feld **Name** ausgefüllt und das Feld **Namensquelle** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|

In Shopify verfügt ein Debitor auch über eine Standardadresse. Zusätzlich zu Vorname, Nachname, E-Mail-Adresse und/oder Telefon kann die Adresse ein Unternehmen und eine Adresse enthalten. Sie können das Feld **Firma** auf der Grundlage der Daten aus der Kundenkarte in [!INCLUDE[prod_short](../includes/prod_short.md)] ausfüllen.

|Priorität|Feld in der Kundenkarte|Description|
|------|------|-----------|
|0|**Name**|Höchste Priorität, wenn das Feld **Namensquelle** auf der **Shopify-Shop-Karte** die Option *Unternehmensname* enthält.|
|2|**Name 2**|Niedrigste Priorität, wenn das Feld **Quelle von Name 2** auf der **Shopify-Shop-Karte** die Option *Unternehmensname* enthält.|

Wählen Sie für Adressen, bei denen Bezirk/Provinz verwendet wird, die Option **Code** oder **Name** im Feld **Länderquelle** auf der **Shopify-Shop-Karte** aus, Der Code bzw. der Name gibt den Typ der gespeicherten Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] im Feld **Bezirk** an. Denken Sie daran, Kundenvorlagen pro Land zu initialisieren, damit die Ländercode-/Namenszuordnung fertig ist. 


## <a name="sync-customers"></a><a name="sync-customers"></a><a name="sync-customers"></a>Debitoren synchronisieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Shop** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den bestimmten Shop aus, für den Sie Debitoren synchronisieren möchten.
3. Wählen Sie die Aktion **Debitoren synchronisieren** aus.

Alternativ können Sie die Aktion **Kundensynchronisation starten** im Fenster **Shopify Kunden** verwenden oder nach dem Batchauftrag **Kunden synchronisieren** suchen.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)  
