---
title: Debitoren und Unternehmen synchronisieren
description: Importieren und Exportieren Sie Debitoren aus bzw. nach Shopify.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Debitoren und Unternehmen synchronisieren

Wenn Sie einen Auftrag aus Shopify importieren, sind die Informationen über den Debitor für die weitere Verarbeitung des Dokuments in [!INCLUDE[prod_short](../includes/prod_short.md)] unerlässlich. Dafür stehen zwei Hauptoptionen und verschiedene Kombinationen zur Verfügung:

* Verwenden Sie einen speziellen Kunden für alle Bestellungen.
* Importieren Sie die Debitoreninformationen aus Shopify. Diese Option steht auch zur Verfügung, wenn Sie Debitoren nach Shopify von [!INCLUDE[prod_short](../includes/prod_short.md)] exportieren.

Mit Shopify können Sie Ihr Business-to-Business-(B2B-) und Direct-to-Customer-(DTC-)Geschäft mit der Leistung und Benutzerfreundlichkeit der All-in-one-Plattform von Shopify von nur einem Ort aus erledigen. Der Shopify-Konnektor funktioniert auch mit verschiedenen E-Commerce-Varianten.

Während Shopify zwei Entitäten – Debitor und Unternehmen – hat, verfügt [!INCLUDE[prod_short](../includes/prod_short.md)] nur über die Debitorenentität, die sich darauf auswirkt, wie die Synchronisierung funktioniert.

Wenn Sie DTC ausführen, wird der Kaufende in Shopify als Debitor erstellt. Anschließend wird der Debitor in [!INCLUDE[prod_short](../includes/prod_short.md)] als Shopify-Debitor zugeordnet und mit einem Debitor verknüpft bzw. konvertiert.

Wenn Sie B2B betreiben, wird der Kaufende in Shopify als Debitor mit einem Unternehmen verbunden. Der Debitor wird in [!INCLUDE[prod_short](../includes/prod_short.md)] als Shopify-Debitor importiert, und das Unternehmen wird in [!INCLUDE[prod_short](../includes/prod_short.md)] als Shopify-Unternehmen importiert und mit einem Debitoren verknüpft bzw. konvertiert.

Um einen Debitoren aus [!INCLUDE[prod_short](../includes/prod_short.md)] in Shopify zu exportieren, unterscheiden sich die Schritte, je nachdem, was Sie tun möchten:

* Exportieren Sie einen Debitoren als Shopify-Debitoren für DTC.
* Exportieren Sie einen Debitoren als Unternehmens- und Debitorenpaar für den B2B-Flow.

## Wichtige Einstellungen beim Import von DTC-Debitoren aus Shopify

Ob Sie nun Debitoren aus Shopify in großen Mengen oder Bestellungen importieren: Verwenden Sie folgende Einstellungen, um den Vorgang zu verwalten:

|Feld|Beschreibung|
|------|-----------|
|**Debitorenimport aus Shopify**|Wählen Sie **Alle Kunden**, wenn Sie Kunden aus Shopify in großen Mengen importieren möchten; entweder manuell mit der Aktion **Kunden synchronisieren** oder über die Auftragswarteschlange für wiederkehrende Aktualisierungen. Unabhängig von der Auswahl werden die Kundeninformationen immer zusammen mit der Bestellung importiert. Die Verwendung dieser Information hängt jedoch von den **Shopify Kundenvorlagen** und den Einstellungen im Feld **Kundenzuordnungstyp** ab.|
|**Kundenzuordnungstyp**|Legen Sie fest, wie der Konnektor die Zuordnung vornehmen soll.</br></br>- **Nach E-Mail/Telefon**, wenn Sie möchten, dass der Konnektor E-Mail-Konto- und Telefoninformationen verwendet, um den importierten Shopify-Debitoren anhand eines Debitoren in Business Central zuzuordnen.</br></br>- **Nach Rechnungsinformationen**, wenn Sie möchten, dass der Konnektor die Adresse des Rechnungsempfängers verwenden, um den importierten Shopify-Debitor einem bestehenden Debitor in Business Central zuzuordnen.</br></br>- **Nehmen Sie Immer den Standarddebitor**, wenn Sie möchten, dass das System einen Debitor aus dem Feld **Standarddebitornr.** verwendet. |
|**Shopify Kann Debitoren aktualisieren**| Wählen Sie dieses Feld, ob der Konnektor gefundene Debitoren aktualisieren soll, wenn die Optionen **Nach E-Mail/Telefon** oder **Nach Rechnungsinformationen** im Feld **Debitorzuordnungstyp** ausgewählt sind.|
|**Unbekannte Debitoren automatisch erstellen**| Wählen Sie dieses Feld, ob der Konnektor fehlende Debitoren erstellen soll, wenn die Optionen **Nach E-Mail/Telefon** oder **Nach Rechnungsinformationen** im Feld **Debitorzuordnungstyp** ausgewählt sind. Ein neuer Debitor wird anhand der importierten Daten und des **Debitorenvorlagencodes** erstellt, der auf den Seiten **Shopify Shop-Karte** oder **Shopify-Debitorenvorlage** definiert ist. Beachten Sie, dass der Shopify-Debitor über mindestens eine Adresse verfügen muss. Bei Bestellungen, die über den Shopify-Vertriebskanal POS erstellt wurden, fehlen häufig Adressangaben. Wenn diese Option nicht aktiviert ist, müssen Sie einen Debitoren manuell erstellen und mit dem Shopify-Debitor verknüpfen.|
|**Debitor.Unternehmensvorlagencode**|Verwenden Sie dieses Feld zusammen mit **Unbekannte Debitoren automatisch erstellen**.</br></br>Wählen Sie die Standardvorlage aus, die für automatisch erstellte Debitoren verwendet werden soll. Stellen Sie sicher, dass die ausgewählte Vorlage die obligatorischen Felder enthält, wie z. B. **Gen. Geschäftsbuchungsgruppe**, **Debitorbuchungsgruppe**, MwSt.- oder steuerbezogene Felder.</br></br>Auf der Seite **Shopify-Debitorenvorlagen** können Sie Vorlagen pro Land/Region definieren, was Ihnen dabei hilft, Steuern korrekt zu berechnen.</br></br>Weitere Informationen finden Sie unter [Steuern einrichten](setup-taxes.md).|

### Debitorenvorlage pro Land/Region

Einige Einstellungen können auf der Ebene eines Landes/Region oder eines Staates/Provinz festgelegt werden. Die Einstellungen können unter [Versand und Lieferung](https://www.shopify.com/admin/settings/shipping) in Shopify festgelegt werden.

Mit der **Shopify-Debitorenvorlage** können Sie die folgenden Schritte für jeden Debitor ausführen:

1. Geben Sie die **Standarddebitorennr.** an, die Vorrang vor der Auswahl in den Feldern **Debitorenimport aus Shopify** und **Debitorenzuordnungstyp** hat. Sie wird im importierten Verkaufsauftrag verwendet.
2. Definieren Sie den **Kundenvorlagencode**, mit dem fehlende Kunden erstellt werden, wenn **Unbekannte Kunden automatisch erstellen** aktiviert ist. Wenn der **Kundenvorlagencode** leer ist, dann verwendet die Funktion den **Kundenvorlagencode**, der auf der **Shopify Shop-Karte** definiert ist. Das System versucht zunächst, eine Vorlage für den **Länder-/Regionscode** für die Standardadresse zu finden. Wenn keine Vorlage gefunden wird, wird die erste Adresse verwendet.
3. In manchen Fällen ist der für ein Land/eine Region definierte **Debitorvorlagencode** nicht ausreichend, um die eine korrekte Berechnung der Steuern zu gewährleisten (z. B. für Länder/Regionen mit Umsatzsteuer). In diesem Fall könnte der **Steuerbereich** eine nützliche Ergänzung sein.
4. Das Feld **Steuergebiet** enthält auch einen **Ländercode** und einen **Bezirksnamen** Paar. Dieses Paar ist nützlich, wenn der Connector einen Code in einen Namen umwandeln muss oder umgekehrt.

> [!NOTE]  
> Die Ländercodes sind Ländercodes nach ISO 3166-1 Alpha 2. Erfahren Sie mehr unter [Ländercode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## Wichtige Einstellungen beim Export von DTC-Debitoren aus Shopify

Sie können bestehende Debitoren in Shopify in großen Mengen exportieren. In jedem Fall werden ein Debitor und eine Standardadresse erstellt. Der Prozess kann mit den folgenden Einstellungen verwaltet werden:

|Feld|Description|
|------|-----------|
|**Kann Shopify-Debitoren aktualisieren**| Aktivieren Sie diese Option, wenn Sie später Aktualisierungen aus Business Central für Debitoren erstellen möchten, die bereits in Shopify vorhanden sind.|

Für den Export eines Debitors gelten die folgenden Voraussetzungen:

* Der Debitor muss eine gültige E-Mail-Adresse haben.
* Stellen Sie sicher, wenn Sie Debitoren mit Adressen, die Provinzen/Staaten beinhalten exportieren, dass der **ISO-Code** für Länder/Regionen ausgefüllt ist.|
* Wenn auf der Kundenkarte ein Land bzw. eine Region ausgewählt ist, stellen Sie sicher, dass der **ISO-Code** angegeben ist. Für lokale Debitoren mit einem leeren Feld für Land/Region, verwendet der Shopify-Konnektor das auf der Seite **Unternehmensinformationen** angegebene Land bzw. die angegebene Region.
* Wenn der Debitor eine Telefonnummer hat, muss die Nummer eindeutig sein, denn Shopify akzeptiert keinen zweiten Debitor mit derselben Telefonnummer.
* Wenn der Debitor eine Telefonnummer hat, muss diese im E.164-Format vorliegen. Andere Formate werden unterstützt, wenn sie eine Nummer darstellen, die von überall auf der Welt gewählt werden kann. Die folgenden Formate sind gültig:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Nachdem Sie die Debitoren in Shopify erstellt haben, können Sie ihnen direkte Einladungen schicken, um sie zur Aktivierung ihrer Konten zu bewegen.

### Debitoreninformationen in Shopify ausfüllen

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

Wählen Sie für Adressen, bei denen Bezirk/Provinz verwendet wird, die Option **Code** oder **Name** im Feld **Länderquelle** auf der **Shopify-Shop-Karte** aus, Der Code bzw. der Name gibt den Typ der gespeicherten Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] im Feld **Bezirk** an. Denken Sie daran, Kundenvorlagen pro Land/Region zu initialisieren, damit die Ländercode-/Namenszuordnung fertig ist. 

## DTC-Debitoren nach Shopify exportieren

### Anfängliche Synchronisierung von Debitoren aus Business Central mit Shopify

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie **Shopify Kunden** ein und wählen Sie den zugehörigen Link.
2. Wählen Sie die Aktion **Debitor hinzufügen** aus.
3. Geben Sie im Feld **Shop-Code** den ersten Code ein. Wenn Sie das Fenster **Shopify-Debitoren** über die Seite **Shop-Karte** aufrufen, wird der Shop-Code automatisch ausgefüllt.
4. Legen Sie nach Bedarf Filter für Debitoren fest. Sie können beispielsweise nach Länder-/Regionscode filtern.
5. Wählen Sie **OK** aus.

Die daraus resultierenden Debitoren werden automatisch mit ihren Adressen in Shopify erstellt.

> [!NOTE]  
> Die erste Synchronisierung von Debitoren von [!INCLUDE[prod_short](../includes/prod_short.md)] nach Shopify berücksichtigt die Einstellungen **Kann Shopify-Debitoren aktualisieren** nicht.

### Debitoren synchronisieren

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify Shop** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den bestimmten Shop aus, für den Sie Debitoren synchronisieren möchten.
3. Wählen Sie die Aktion **Debitoren synchronisieren** aus.

Alternativ können Sie die Aktion **Kundensynchronisation starten** im Fenster **Shopify Kunden** verwenden oder nach dem Batchauftrag **Kunden synchronisieren** suchen.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

## B2B-Unternehmen

Wenn Sie B2B in Shopify verwenden, können Sie nicht nur Debitoren, sondern auch Unternehmen erstellen. Sie können einem Unternehmen einen oder mehrere Einzeldebitoren zuordnen. Darüber hinaus können Sie Zahlungsbedingungen, Standorte und Kataloge definieren.

## Wichtige Einstellungen beim Import von B2B-Unternehmen aus Shopify

Ob Sie nun Unternehmen aus Shopify in großen Mengen oder Bestellungen importieren: Verwenden Sie die Einstellungen in der folgenden Tabelle, um den Vorgang zu verwalten.

|Feld|Description|
|------|-----------|
|**Unternehmensimport aus Shopify**|Wählen Sie **Alle Unternehmen**, wenn Sie Debitoren aus Shopify in großen Mengen importieren möchten; entweder manuell mit der Aktion **Unternehmen synchronisieren** oder über die Auftragswarteschlange für wiederkehrende Aktualisierungen. Unabhängig von der Auswahl werden die Debitoreninformationen immer zusammen mit der Bestellung importiert. Die Verwendung dieser Information hängt jedoch von den **Shopify-Unternehmensvorlagen** und den Einstellungen im Feld **Mandantenzuordnungstyp** ab.|
|**Mandantenzuordnungstyp**|Legen Sie fest, wie der Konnektor die Zuordnung vornehmen soll.</br></br>- **Nach E-Mail/Telefon**, wenn Sie möchten, dass der Konnektor die importierten Shopify-Unternehmen anhand von E-Mail und Telefon des Hauptkontakts einem bestehenden Debitoren in Business Central zuordnet.</br></br>- Wählen Sie **Immer den Standardmandanten verwenden**, wenn Sie möchten, dass das System das Unternehmen aus dem Feld **Standardmandantennr.** verwendet. |
|**Shopify kann Mandanten aktualisieren**| Wählen Sie dieses Feld aus, wenn der Konnektor gefundene Debitoren aktualisieren soll, wenn die Option **Nach E-Mail/Telefon** im Feld **Mandantenzuordnungstyp** ausgewählt ist.|
|**Unbekannte Mandanten automatisch erstellen**| Wählen Sie dieses Feld aus, wenn der Konnektor neue Debitoren erstellen soll, wenn die Option **Nach E-Mail/Telefon** im Feld **Mandantenzuordnungstyp** ausgewählt ist. Ein neuer Debitor wird anhand der importierten Daten und des **Debitoren-/Unternehmensvorlagencodes** erstellt, der auf den Seiten **Shopify Shop-Karte** oder **Shopify Kundenvorlage** definiert ist.|
|**Debitoren-/Firmenvorlagencode**|Verwenden Sie dieses Feld zusammen mit **Unbekanntes Unternehmen automatisch erstellen** aus.</br></br>- Wählen Sie die Standardvorlage aus, die für automatisch erstellte Debitoren verwendet werden soll. Stellen Sie sicher, dass die obligatorischen Felder in der Vorlage ausgefüllt sind, wie z. B. **Gen. Geschäftsbuchungsgruppe**, **Debitorbuchungsgruppe**, **Mehrwertsteuer (MwSt.)** oder andere steuerbezogene Felder.</br></br>- Auf der Seite **Shopify Debitorenvorlagen** können Sie Vorlagen pro Land/Region definieren, was für eine korrekte Steuerberechnung nützlich ist.</br></br>Erfahren Sie mehr unter [Steuern festlegen](setup-taxes.md).|

> [!NOTE]  
> Das Unternehmen muss einen Hauptkontakt haben. Andernfalls springt der Konnektor zum Unternehmen.
> Es wird nur ein ältester Standort importiert.
> Es wird nur der Hauptkontakt importiert.

## Wichtige Einstellungen beim Export von B2B-Unternehmen nach Shopify

Sie können bestehende Debitoren in Shopify in großen Mengen als Unternehmen exportieren. Es werden jeweils ein Unternehmen und ein Standardstandort sowie ein Hauptkontakt angelegt. Es ist auch möglich, einen Katalog zu erstellen.

|Feld|Description|
|------|-----------|
|**Kann Shopify-Mandanten aktualisieren**| Aktivieren Sie diese Option, wenn Sie später Aktualisierungen aus Business Central für Unternehmen erstellen möchten, die bereits in Shopify vorhanden sind.|
|**Standardkontaktberechtigungen**| Geben Sie an, welche Berechtigungen dem Hauptkontakt zugewiesen werden müssen. Sie können zwischen **Keine**, **Nur Bestellung** und **Standortadministrator** wählen.|
|**Katalog automatisch erstellen**| Aktivieren Sie diese Option, wenn Sie einen Katalog erstellen möchten, der alle Produkte enthält. Für jedes exportierte Unternehmen wird ein Katalog erstellt.|

## Ein B2B-Unternehmen nach Shopify exportieren

### Anfängliche Synchronisierung von B2B-Unternehmen aus Business Central mit Shopify

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify-Mandanten** ein und wählen Sie den zugehörigen Link aus.
2. Wählen Sie die Aktion **Mandant hinzufügen** aus.
3. Geben Sie im Feld **Shop-Code** den ersten Code ein. Wenn Sie das Fenster **Shopify-Mandant** über die Seite **Shop-Karte** aufrufen, wird der Shop-Code automatisch ausgefüllt.
4. Legen Sie nach Bedarf Filter für den Debitor fest. Sie können beispielsweise nach Länder-/Regionscode filtern.
5. Wählen Sie **OK** aus.

Das resultierende Unternehmen und die resultierenden Debitoren werden automatisch in Shopify erstellt.

> [!NOTE]  
> Die erste Synchronisierung von Unternehmen von [!INCLUDE[prod_short](../includes/prod_short.md)] nach Shopify berücksichtigt die Einstellungen **Kann Shopify-Unternehmen aktualisieren** nicht.

### B2B-Unternehmen synchronisieren

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shop** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den bestimmten Shop aus, für den Sie Debitoren synchronisieren möchten.
3. Wählen Sie die Aktion **Mandanten synchronisieren** aus.

Verwenden Sie alternativ die Aktion **Mandantensynchronisierung starten** auf der Seite **Shopify-Mandant** oder suchen Sie nach dem Batchauftrag **Mandanten synchronisieren**.

Sie können für die Aufgabe eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

## Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)  
