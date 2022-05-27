---
title: Debitoren synchronisieren
description: Import von Debitoren von oder Export von Debitoren nach Shopify durchführen
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 92ac46e9f7e69204b4c7edee4aa430a8786b6c0b
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768160"
---
# <a name="synchronize-customers"></a>Debitoren synchronisieren

Wenn eine Bestellung aus Shopify importiert wird, sind die Informationen zum Debitor für die Weiterverarbeitung des Dokuments in [!INCLUDE[prod_short](../includes/prod_short.md)] unerlässlich. Es sind zwei Hauptoptionen und deren Kombinationen verfügbar:

* Speziellen Debitor für alle Bestellungen verwenden.
* Aktuelle Debitoreninformationen aus Shopify importieren. Diese Option ist auch verfügbar, wenn Sie den Debitor zunächst von [!INCLUDE[prod_short](../includes/prod_short.md)] nach Shopify exportieren.

## <a name="how-connector-chooses-which-customer-to-use"></a>So wählt der Konnektor aus, welcher Debitor verwendet werden soll

Die Funktion *Bestellung aus Shopify importieren* versucht, den Debitor in der folgenden Reihenfolge auszuwählen:

1. Wenn die **Standarddebitorennr.** in der **Shopify-Debitorenvorlage** für das entsprechende Land definiert ist, wird die **Standarddebitorennr.** unabhängig von den Einstellungen in **Debitorenimport von Shopify** und **Debitorenzuordnungstyp** verwendet.
2. Wenn **Debitorenimport von Shopify** und **Standarddebitorennr.** definiert sind, wird die **Standarddebitorennr.** verwendet.

Die nächsten Schritte hängen vom **Debitorenzuordnungstyp** ab.

* **Immer Standarddebitor verwenden** – Verwenden Sie dann den Debitor, der im Feld **Standarddebitorennr.** im Fenster **Shopify-Shop-Karte** definiert ist.
* **Per E-Mail/Telefon** – Der Konnektor versucht, vorhandene Debitoren zuerst anhand der ID, dann per E-Mail und dann per Telefon zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.
* **Informationen für Rechnungsadresse** – Der Konnektor versucht, bestehende Debitoren zuerst anhand der ID und dann anhand der Rechnungsadresse zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.

> [!NOTE]  
> Der Konnektor verwendet Informationen aus der Rechnungsadresse und erstellt die Rechnung an den Debitor in [!INCLUDE[prod_short](../includes/prod_short.md)]. Verkauf an Debitor entspricht Rechnung an Debitor.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Wichtige Einstellungen beim Import von Debitoren aus Shopify

Entweder importieren Sie Debitoren aus Shopify in großen Mengen oder zusammen mit dem Import von Bestellungen. Sie können den Prozess mit den folgenden Einstellungen verwalten:

|Feld|Description|
|------|-----------|
|**Debitorenimport aus Shopify**|Wählen Sie **Alle Debitoren** aus, wenn Sie planen, Debitoren in großen Mengen aus Shopify zu importieren, indem Sie entweder manuell die Aktion **Debitoren synchronisieren** oder die Auftragswarteschlange für wiederkehrende Aktualisierungen verwenden. Debitoreninformationen werden unabhängig von der Auswahl immer zusammen mit der Bestellung importiert. Die Verwendung dieser Informationen hängt jedoch von **Shopify-Debitorenvorlagen** und Einstellungen im Feld **Debitorenzuordnungstyp** ab.|
|**Kundenzuordnungstyp**|Definieren Sie, wie der Konnektor die Zuordnung durchführen soll.<br>- **Per E-Mail/Telefon**, wenn der Konnektor den importierten Shopify-Debitor dem vorhandenen Debitor in [!INCLUDE[prod_short](../includes/prod_short.md)] mit E-Mail-Adresse und Telefonnummer zuordnen soll.</br>- **Informationen für Rechnungsadresse** – Wenn der Konnektor Shopify-Debitoren vorhandenen Deboriten in [!INCLUDE[prod_short](../includes/prod_short.md)] anhand der Adressinformationen des Rechnungsempfängers zuordnen soll.</br>Wählen Sie **Immer Standarddebitor verwenden**, wenn das System einen Debitor aus dem Feld **Standarddebitorennr.** verwenden soll . |
|**Shopify Kann Debitoren aktualisieren**| Wählen Sie aus, ob der Konnektor gefundene Debitoren aktualisieren soll, wenn die Optionen **Per E-Mail/Telefon** oder **Informationen für Rechnungsadresse** im Feld **Debitorenzuordnungstyp** ausgewählt sind.|
|**Unbekannte Debitoren automatisch erstellen**| Legen Sie fest, ob der Konnektor fehlende Debitoren erstellen soll, wenn die Optionen **Per E-Mail/Telefon** oder **Informationen für Rechnungsadresse** im Feld **Debitorenzuordnungstyp** ausgewählt sind. Ein neuer Kunde wird mit importierten Daten und dem **Debitorenvorlagencode** erstellt, der auf den Seiten **Shopify-Shop-Karte** oder **Shopify-Debitorenvorlage** definiert ist. Beachten Sie, dass der Shopify-Debitor über mindestens eine Adresse verfügen muss. Wenn diese Option nicht aktiviert ist, müssen Sie den Debitor erstellen und ihn mit dem Shopify-Debitor verknüpfen. Sie können die Erstellung eines Debitors jederzeit manuell auf der Seite **Shopify-Bestellung** initiieren.|
|**Debitorenvorlagencode**|Wird zusammen mit **Unbekannte Debitoren automatisch erstellen** verwendet.<br> Wählen Sie die Standardvorlage aus, die für automatisch erstellte Debitoren verwendet werden soll. Sie können Vorlagen pro Land/Region im Fenster **Shopify-Debitorenvorlagen** definieren, was für die korrekte Steuerberechnung hilfreich ist. Weitere Informationen finden Sie unter [Anmerkungen zu Steuern](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Debitorenvorlage pro Land

Einige Einstellungen können auf Länder-/Regionsebene oder auf Bundesstaats-/Provinzebene definiert werden. Die Einstellungen können unter [Versand und Lieferung](https://www.shopify.com/admin/settings/shipping) in Shopify konfiguriert werden.

Mit der **Shopify-Debitorenvorlage** können Sie die folgenden Schritte für jedes Land ausführen:

1. Geben Sie die **Standarddebitorennr.** an, die Vorrang vor der Auswahl in den Feldern **Debitorenimport aus Shopify** und **Debitorenzuordnungstyp** hat. Sie wird im importierten Verkaufsauftrag verwendet.
2. Definieren Sie den **Debitorenvorlagencode**, der zum Erstellen fehlender Debitoren verwendet wird, wenn **Unbekannte Debitoren automatisch erstellen** aktiviert ist. Wenn **Debitorenvorlagencode** leer ist, verwendet die Funktion **Debitorenvorlagencode**, der auf der **Shopify-Shop-Karte** definiert ist.
3. In manchen Fällen ist der **Debitorenvorlagencode** pro Land nicht ausreichend, um eine korrekte Steuerberechnung zu gewährleisten. Zum Beispiel für Länder mit Umsatzsteuer.

> [!NOTE]  
> Die Ländercodes sind Ländercodes nach ISO 3166-1 Alpha 2. Weitere Informationen finden Sie unter [Ländercode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Debitoren nach Shopify exportieren

Vorhandene Debitoren können in großen Mengen nach Shopify exportiert werden. Infolgedessen werden ein Debitor und eine Standardadresse erstellt. Sie können den Prozess mithilfe der folgenden Einstellungen verwalten:

|Feld|Description|
|------|-----------|
|**Debitoren nach Shopify** exportieren|Legen Sie fest, ob alle Debitoren mit einer gültigen E-Mail-Adresse in großen Mengen von [!INCLUDE[prod_short](../includes/prod_short.md)] nach Shopify exportiert werden sollen, entweder manuell mit der Aktion **Debitoren synchronisieren** oder über die Auftragswarteschlange für wiederkehrende Aktualisierungen.|
|**Kann Shopify-Debitoren aktualisieren**|Wird zusammen mit **Debitor nach Shopify exportieren**. Aktivieren Sie die Option, wenn Sie später Updates über [!INCLUDE[prod_short](../includes/prod_short.md)] für bereits bestehende Debitoren in Shopify generieren möchten.|

> [!NOTE]  
> Nachdem Sie Debitoren in Shopify erstellt haben, können Sie direkte Einladungen an Debitoren senden. Dadurch werden Sie zur Aktivierung ihres Kontos ermutigt.

### <a name="populate-customer-information-in-shopify"></a>Debitoreninformationen in Shopify ausfüllen

Ein Debitor in Shopify hat einen Vornamen, einen Nachnamen, eine E-Mail-Adresse und/oder eine Telefonnummer. Sie können den Vor- und Nachnamen basierend auf den Daten aus der Debitorenkarte in [!INCLUDE[prod_short](../includes/prod_short.md)] ausfüllen.

|Priorität|Feld in Debitorenkarte|Description|
|------|------|-----------|
|0|**Kontaktname**|Höchste Priorität, wenn das Feld **Kontaktname** ausgefüllt und das Feld **Kontaktquelle** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|
|2|**Name 2**|Wenn das Feld **Name 2** ausgefüllt und das Feld **Quelle von Name 2** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|
|3|**Name**|Niedrigste Priorität, wenn das Feld **Name** ausgefüllt und das Feld **Namensquelle** auf der **Shopify-Shop-Karte** die Optionen *Vorname und Nachname* oder *Nachname und Vorname* enthält, die festlegen, wie die Werte getrennt werden sollen.|

Ein Debitor in Shopify verfügt auch über eine Standardadresse, die neben Vorname, Nachname, E-Mail und/oder Telefon auch Angaben wie Unternehmen und Adresse enthalten kann. Sie können das Feld **Unternehmen** basierend auf Daten aus der Debitorenkarte in [!INCLUDE[prod_short](../includes/prod_short.md)] ausfüllen.

|Priorität|Feld in Debitorenkarte|Description|
|------|------|-----------|
|0|**Name**|Höchste Priorität, wenn das Feld **Namensquelle** auf der **Shopify-Shop-Karte** die Option *Unternehmensname* enthält.|
|2|**Name 2**|Niedrigste Priorität, wenn das Feld **Quelle von Name 2** auf der **Shopify-Shop-Karte** die Option *Unternehmensname* enthält.|

Wählen Sie für Adressen, bei denen Land/Provinz verwendet wird, die Option *Code* oder *Name* im Feld **Länderquelle** auf der **Shopify-Shop-Karte** aus, um festzulegen, welcher Datentyp in [!INCLUDE[prod_short](../includes/prod_short.md)] im Feld **Land** gespeichert werden soll.

## <a name="sync-customers"></a>Debitoren synchronisieren

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie Debitoren synchronisieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Debitoren synchronisieren** aus.

Verwenden Sie alternativ die Aktion **Debitorensynchronisierung starten** im Fenster **Shopify-Debitoren** aus, oder suchen Sie nach dem Stapelverarbeitungsauftrag **Debitoren synchronisieren**.

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Konnektor für Shopify](get-started.md)  
