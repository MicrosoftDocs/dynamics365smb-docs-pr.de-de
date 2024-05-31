---
title: Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer
description: 'Verwenden Sie Rechnungsbuchungsrichtlinien, um zu steuern, ob ein Benutzer Verkaufs- und Einkaufsrechnungen buchen kann.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer

Unternehmen haben oft einzigartige Prozesse zum Buchen von Verkaufs- und Einkaufsrechnungen und Lieferungen. Beispielsweise können die Prozesse von einer Person, die alles auf einer Bestellung bucht, bis zu mehreren Mitarbeitern variieren. Sie können Benutzer daran hindern, Rechnungen zu buchen oder verlangen, dass Rechnungen zusammen mit Lieferungen oder Belegen gebucht werden.

## <a name="to-specify-a-posting-policy"></a>Um eine Buchhaltungsperioden festlegen

Auf der Seite **Benutzereinrichtung** in den **Richtlinien zum Buchen von Verkaufsrechnungen** und **Purch. Wählen Sie in den Feldern Rechnungsbuchungsrichtlinie** eine der folgenden Optionen aus:

* **Zugelassen** (Standard) – Behalten Sie das aktuelle Verhalten bei, bei dem ein Benutzer die zu verwendende Veröffentlichungsoption auswählen kann, z. B. **Versenden**, **Rechnung** und **Lieferung und Rechnung**. 
* **Verboten** - Verhindert, dass der Benutzer Rechnungen verbucht. Business Central zeigt einen Bestätigungsdialog an, der nur die Optionen **Versenden** oder **Empfangen** bereitstellt.
* **Obligatorisch** – Ermöglichen Sie dem Benutzer, Rechnungen zusammen mit Belegen oder Sendungen zu buchen. Business Central zeigt einen Bestätigungsdialog an, der die Optionen **Versenden und Rechnung** oder **Empfangen und Rechnung** bereitstellt.

## <a name="effect-on-documents"></a>Auswirkung auf die Dokumente

Die folgende Tabelle beschreibt, wie sich Rechnungsbuchungsrichtlinien auf Dokumente auswirken.

> [!NOTE]
> Wenn Sie Verkaufs- und Einkaufsrechnungen sowie Gutschriften buchen, stehen Ihnen keine Buchungsoptionen zur Verfügung. In den Belegen werden die physischen und finanziellen Transaktionen immer gemeinsam gebucht. Sie können Rechnungen und Gutschriften nicht teilweise buchen.

|Beleg | Option 1: Zulassen <br>Zeigt eine Reihe von Optionen an| Option 2: Verboten <br>Bestätigungsdialog | Optio 3: Zwingend <br>Bestätigungsdialog|
|--|--|--|--|
|Verkaufsauftrag |- Versand <br>- Fakturieren <br>- Versand und fakturieren |Möchten Sie die Lieferung buchen? |Möchten Sie die Lieferung und Rechnung buchen?|
|Verkaufsrechnungen|Keine Optionen|Möchten Sie die Rechnung buchen?|Möchten Sie die Rechnung buchen?|
|Verkaufsgutschrift|Keine Optionen|Möchten Sie die Gutschrift buchen?|Möchten Sie die Gutschrift buchen?|
|Verkaufsreklamation |- Empfang <br>- Fakturieren <br>- Empfang und Rechnung |Möchten Sie den Wareneingang buchen? |Möchten Sie den Wareneingang und die Rechnung buchen?|
|Lagerkommissionierung |- Versand <br>- Versand und fakturieren |Möchten Sie die Lieferung buchen? |Möchten Sie die Lieferung und Rechnung buchen?|
|Einkaufsbestellung |- Empfang <br>- Fakturieren <br>- Empfang und Rechnung |Möchten Sie den Wareneingang buchen? |Möchten Sie den Wareneingang und die Rechnung buchen?|
|Einkaufsrechnung|Keine Optionen|Möchten Sie die Rechnung buchen?|Möchten Sie die Rechnung buchen?|
|Einkaufsgutschrift|Keine Optionen|Möchten Sie die Gutschrift buchen?|Möchten Sie die Gutschrift buchen?|
|Einkaufsreklamation |- Versand <br>- Fakturieren <br>- Versand und fakturieren |Möchten Sie die Lieferung buchen? |Möchten Sie die Lieferung und Rechnung buchen?|
|Lagereinlagerung |- Empfang <br>- Empfang und Rechnung |Möchten Sie den Wareneingang buchen? |Möchten Sie den Wareneingang und die Rechnung buchen?|
|Warenausgang |- Versand <br>- Versand und fakturieren | Möchten Sie die Lieferung buchen? |Möchten Sie die Lieferung und Rechnung buchen?|

   > [!Note]
   > Die Einstellung wirkt sich nicht auf die Buchung allgemeiner Buchungszeilen aus, in denen Sie **Rechnung** im Feld **Art des Dokuments** auswählen können.

## <a name="see-also"></a>Weitere Informationen

[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Käufe mit Einkaufsrechnungen und Aufträgen erfassen](purchasing-how-record-purchases.md)  
[Artikel für einen Verkauf kaufen, indem Sie Einkaufsrechnungen erstellen](purchasing-how-purchase-products-sale.md)
[Machen Sie sich bereit für das Geschäft](ui-get-ready-business.md)  
