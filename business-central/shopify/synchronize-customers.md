---
title: Debitoren synchronisieren
description: Import von Debitoren von oder Export von Debitoren nach Shopify durchführen
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 0c1402c4f41f108b504ad31829ede5a1095b6ce4
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317326"
---
# <a name="synchronize-customers"></a>Debitoren synchronisieren

Wenn ein Auftrag aus Shopify importiert wird, sind die Informationen über den Kunden für die weitere Verarbeitung des Dokuments in [!INCLUDE[prod_short](../includes/prod_short.md)] unerlässlich. Es sind zwei Hauptoptionen und deren Kombinationen verfügbar:

* Verwenden Sie einen speziellen Kunden für alle Bestellungen.
* Importieren Sie die tatsächlichen Kundeninformationen aus Shopify. Diese Option steht auch zur Verfügung, wenn Sie Kunden zuerst nach Shopify von [!INCLUDE[prod_short](../includes/prod_short.md)] exportieren.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Wie der Konnektor auswählt, welcher Kunde verwendet werden soll

Die Funktion *Bestellung importieren aus Shopify* versucht, den Kunden in der folgenden Reihenfolge auszuwählen:

1. Wenn das Feld **Standarddebitorennr.** Feld in der **Shopify Kundenvorlage** für das entsprechende Land definiert ist, dann wird die **Standardkunden-Nr.** wird verwendet, unabhängig von den Einstellungen in den Feldern **Kundenimport von Shopify** und **Kundenzuordnungstyp**. Weitere Informationen finden Sie unter [Debitorenvorlage pro Land](synchronize-customers.md#customer-template-per-country).
2. Wenn der **Kundenimport von Shopify** auf *Keine* festgelegt ist und die **Standardkunden-Nr.** in der **Shopify-Shop-Karte** definiert sind, wird die **Standarddebitorennr.** verwendet.

Die nächsten Schritte hängen von der **Kundenzuordnung Typ** ab.

* **Nehmen Sie immer den Standardkunden**, dann verwendet der Konnektor den in der **Standardkunden-Nr.** definierten Kunden. Feld auf der Seite **Shopify Shop-Karte**.
* **Nach E-Mail/Telefon**, der Konnektor versucht, den bestehenden Kunden zuerst nach der ID, dann nach der E-Mail und dann nach dem Telefon zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.
* **Nach Rechnungsinformationen** versucht der Konnektor, den bestehenden Kunden zunächst über die ID und dann über die Rechnungsadressinformationen zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.

> [!NOTE]  
> Der Konnektor verwendet die Informationen aus der Rechnungsadresse und erstellt den Rechnungsempfänger in [!INCLUDE[prod_short](../includes/prod_short.md)]. Verkauf an Debitor entspricht Rechnung an Debitor.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Wichtige Einstellungen beim Import von Debitoren aus Shopify

Entweder importieren Sie Debitoren aus Shopify in großen Mengen oder zusammen mit dem Import von Bestellungen. Sie können den Prozess mit den folgenden Einstellungen verwalten:

|Feld|Beschreibung|
|------|-----------|
|**Debitorenimport aus Shopify**|Wählen Sie **Alle Kunden**, wenn Sie Kunden aus Shopify in großen Mengen importieren möchten; entweder manuell mit der Aktion **Kunden synchronisieren** oder über die Auftragswarteschlange für wiederkehrende Aktualisierungen. Unabhängig von der Auswahl werden die Kundeninformationen immer zusammen mit der Bestellung importiert. Die Verwendung dieser Information hängt jedoch von den **Shopify Kundenvorlagen** und den Einstellungen im Feld **Kundenzuordnungstyp** ab.|
|**Kundenzuordnungstyp**|Legen Sie fest, wie der Konnektor die Zuordnung vornehmen soll.<br>- **Nach E-Mail/Telefon**, wenn Sie möchten, dass der Konnektor den importierten Shopify-Kunden anhand von E-Mail und Telefon einem bestehenden Kunden in [!INCLUDE[prod_short](../includes/prod_short.md)] zuordnet.</br>- **Nach Rechnungsinformationen**, wenn Sie möchten, dass der Konnektor den importierten Shopify-Kunden einem bestehenden Kunden in [!INCLUDE[prod_short](../includes/prod_short.md)] zuordnet und dabei die Adressinformationen der Partei verwendet, die die Rechnung erhält.</br>Wählen Sie **Immer den Standardkunden nehmen**, wenn Sie möchten, dass das System einen Kunden aus der **Standardkunden-Nr.** verwendet. . |
|**Shopify Kann Debitoren aktualisieren**| Wählen Sie, ob der Konnektor gefundene Kunden aktualisieren soll, wenn die Optionen **Nach E-Mail/Telefon** oder **Nach Rechnungsinformationen** im Feld **Kundenzuordnungstyp** ausgewählt sind.|
|**Unbekannte Debitoren automatisch erstellen**| Wählen Sie aus, ob der Konnektor fehlende Kunden erstellen soll, wenn die Optionen **Nach E-Mail/Telefon** oder **Nach Rechnungsinformationen** im Feld **Kundenzuordnungstyp** ausgewählt sind. Ein neuer Kunde wird anhand der importierten Daten und des **Kundenvorlagencodes** erstellt, der auf den Seiten **Shopify Shop-Karte** oder **Shopify Kundenvorlage** definiert ist. Beachten Sie, dass der Shopify-Debitor über mindestens eine Adresse verfügen muss. Wenn diese Option nicht aktiviert ist, müssen Sie einen Kunden manuell erstellen und mit dem Kunden Shopify verknüpfen. Sie können die Erstellung eines Debitors jederzeit manuell auf der Seite **Shopify-Bestellung** initiieren.|
|**Debitorenvorlagencode**|Wird zusammen mit **Unbekannte Debitoren automatisch erstellen** verwendet.<br> Wählen Sie die Standardvorlage aus, die für automatisch erstellte Debitoren verwendet werden soll. Stellen Sie sicher, dass die ausgewählte Vorlage die obligatorischen Felder enthält, wie z.B. **Gen. Geschäftsbuchungsgruppe**, **Kundenbuchungsgruppe**, MwSt.- oder steuerbezogene Felder.<br> Auf der Seite **Shopify Kundenvorlagen** können Sie Vorlagen pro Land/Region definieren, was für eine korrekte Steuerberechnung nützlich ist. <br>Weitere Informationen finden Sie unter [Steuern einrichen](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Debitorenvorlage pro Land

Einige Einstellungen können auf Länder-/Regionalebene oder auf der Ebene eines Staates/Provinz festgelegt werden. Die Einstellungen können unter [Versand und Lieferung](https://www.shopify.com/admin/settings/shipping) in Shopify konfiguriert werden.

Mit der **Shopify-Debitorenvorlage** können Sie die folgenden Schritte für jedes Land ausführen:

1. Geben Sie die **Standarddebitorennr.** an, die Vorrang vor der Auswahl in den Feldern **Debitorenimport aus Shopify** und **Debitorenzuordnungstyp** hat. Sie wird im importierten Verkaufsauftrag verwendet.
2. Definieren Sie den **Kundenvorlagencode**, mit dem fehlende Kunden erstellt werden, wenn **Unbekannte Kunden automatisch erstellen** aktiviert ist. Wenn der **Kundenvorlagencode** leer ist, dann verwendet die Funktion den **Kundenvorlagencode**, der auf der **Shopify Shop-Karte** definiert ist.
3. Legen Sie fest, ob die Preise für importierte Bestellungen Steuern/MwSt. enthalten.
4. In einigen Fällen reicht der für das Land definierte **Kundenvorlagencode** nicht aus, um eine korrekte Berechnung der Steuern zu gewährleisten. Zum Beispiel für Länder mit Umsatzsteuer. In diesem Fall könnte die **Steuerbereiche** eine nützliche Ergänzung sein.

> [!NOTE]  
> Die Ländercodes sind Ländercodes nach ISO 3166-1 Alpha 2. Weitere Informationen finden Sie unter [Ländercode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Debitoren nach Shopify exportieren

Vorhandene Debitoren können in großen Mengen nach Shopify exportiert werden. Infolgedessen werden ein Debitor und eine Standardadresse erstellt. Sie können den Prozess mithilfe der folgenden Einstellungen verwalten:

|Feld|Beschreibung|
|------|-----------|
|**Debitoren nach Shopify** exportieren|Wählen Sie, ob Sie alle Kunden mit einer gültigen E-Mail-Adresse von [!INCLUDE[prod_short](../includes/prod_short.md)] bis Shopify in großen Mengen exportieren möchten; entweder manuell, mit der Aktion **Kunden synchronisieren** oder über eine Job-Warteschlange für wiederkehrende Aktualisierungen.<br> Stellen Sie sicher, wenn Sie Debitoren mit Provinzen/Staaten exportieren, dass der **ISO-Code** für Länder/Regionen ausgefüllt ist.|
|**Kann Shopify-Debitoren aktualisieren**|Wird zusammen mit der Einstellung **Kunde exportieren nach Shopify** festgelegt. Aktivieren Sie es, wenn Sie später Aktualisierungen aus [!INCLUDE[prod_short](../includes/prod_short.md)] für Kunden erstellen möchten, die bereits in Shopify vorhanden sind.|

> [!NOTE]  
> Sobald Sie die Kunden in Shopify erstellt haben, möchten Sie vielleicht direkte Einladungen an die Kunden senden. Dadurch werden Sie zur Aktivierung ihres Kontos ermutigt.

### <a name="populate-customer-information-in-shopify"></a>Debitoreninformationen in Shopify ausfüllen

Ein Debitor in Shopify hat einen Vornamen, einen Nachnamen, eine E-Mail-Adresse und/oder eine Telefonnummer. Sie können den Vor- und Nachnamen über die Debitorenkarte in [!INCLUDE[prod_short](../includes/prod_short.md)] ausfüllen.

|Priorität|Feld in Debitorenkarte|Beschreibung|
|------|------|-----------|
|0|**Kontaktname**|Höchste Priorität, wenn das Feld **Kontaktname** ausgefüllt und das Feld **Kontaktquelle** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|
|2|**Name 2**|Wenn das Feld **Name 2** ausgefüllt und das Feld **Quelle von Name 2** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|
|3|**Name**|Niedrigste Priorität, wenn das Feld **Name** ausgefüllt und das Feld **Namensquelle** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|

Ein Debitor in Shopify verfügt auch über eine Standardadresse, die neben Vorname, Nachname, E-Mail und/oder Telefon auch Angaben wie Unternehmen und Adresse enthalten kann. Sie können das Feld **Unternehmen** basierend auf Daten aus der Debitorenkarte in [!INCLUDE[prod_short](../includes/prod_short.md)] ausfüllen.

|Priorität|Feld in Debitorenkarte|Beschreibung|
|------|------|-----------|
|0|**Name**|Höchste Priorität, wenn das Feld **Namensquelle** auf der **Shopify-Shop-Karte** die Option *Unternehmensname* enthält.|
|2|**Name 2**|Niedrigste Priorität, wenn das Feld **Quelle von Name 2** auf der **Shopify-Shop-Karte** die Option *Unternehmensname* enthält.|

Für Adressen, bei denen das Land/die Provinz verwendet wird, wählen Sie *Code* oder *Name* im Feld **Länderquelle** in der **Shopify Shop-Karte**, um anzugeben, welche Art von Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] im Feld **Land** gespeichert wird.

## <a name="sync-customers"></a>Debitoren synchronisieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify Shop** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Kunden synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Debitoren synchronisieren** aus.

Alternativ können Sie die Aktion **Kundensynchronisation starten** im Fenster **Shopify Kunden** verwenden oder nach dem Batchauftrag **Kunden synchronisieren** suchen.

Sie können die durchzuführende Aufgabe so planen, dass sie automatisiert ausgeführt werden. Weitere Informationen finden Sie unter [Wiederkehrende Aufgaben planen](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Konnektor für Shopify](get-started.md)  
