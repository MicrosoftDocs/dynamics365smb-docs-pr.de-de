---
title: Übersicht der Aufgaben zum Konfigurieren von Verkaufsprozessen
description: 'Übersicht der Aufgaben, die erforderlich sind, um Regeln und Werte festzulegen, die Ihre Richtlinien und Prozesse für den Vertrieb definieren, einschließlich der allgemeinen Einrichtung und der finanzbezogenen Einrichtung des Vertriebs.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'trade, sell, configure'
ms.search.form: '170, 172, 300, 301, 428, 456, 459, 1401'
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Einrichten von Verkäufen

Bevor Sie Verkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Vertriebsrichtlinien des Mandanten definieren.

Auf der Seite **Verkauf & Forderungen** müssen Sie die allgemeine Einrichtung festlegen, z.B. welche Verkaufsbelege erforderlich sind, wie deren Werte gebucht werden und welche Art von Zeilen standardmäßig erstellt werden sollen. Diese allgemeine Einrichtung erfolgt in der Regel einmal bei der anfänglichen Implementierung.

Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben. Weitere Informationen finden Sie unter [Sonderverkaufspreise und Rabatte erfassen](sales-how-record-sales-price-discount-payment-agreements.md).

Einrichten von finanzbezogenen Verkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt. Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).

| Aufgabe | Siehe |
| --- | --- |
| Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen. |[Registriert einen neuen Debitor](sales-how-register-new-customers.md) |
| Aktivieren Sie Debitoren, um über PayPal zu bezahlen, indem Sie das PayPal-Logo in Verkaufsbelegen auswählen. |[Aktivieren von Debitoren-Zahlungen durch PayPal](sales-how-enable-payment-service-extensions.md) |
| Geben Sie die verschiedenen Rabatte und alternativen Preise ein, die Sie den Debitoren abhängig von Artikel, Mengen und/oder Datum gewähren. |[Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md) |
| Einrichten von Verkäufer, sodass Sie diese den Debitorenkontakten zuweisen können oder die Leistung des Verkaufspersonals messen können und als Basis für die Berechnung von Verkaufsprovisionen oder der Prämie zuweisen können. |[Verkäufer einrichten](sales-how-setup-salespeople.md) |
| Geben Sie für einzelne Debitoren oder für alle Debitoren an, wie Verkaufsbelege standardmäßig gesendet werden, wenn Sie die Aktion **Buchen und senden** auswählen. |[Belegsendeprofile einrichten](sales-how-setup-document-send-profiles.md) |
| Legen Sie die E-Mail a, um eine Zusammenfassung der Informationen des Verkaufsbelegs zu erhalten, der gesendet wird. |[Dokumente per E-Mail versenden](ui-how-send-documents-email.md) |
|Verwenden Sie einen EU-Webdienst, um die MwSt-IdNr. eines Debitors zu überprüfen.|[MwSt-IdNr. prüfen](finance-setup-vat.md)|
|Definieren Sie die verschiedenen Incoterms, die Sie Debitoren oder Ihren Kreditoren anbieten.|[Lieferbedingungen einrichten](sales-how-set-up-shipment-methods.md)|
|Geben Sie Informationen über die verschiedenen eingesetzten Transportkreditoren ein, einschließlich einer Verknüpfung zu ihrem Paketverfolgungsservice.|[Zusteller einrichten](sales-how-to-set-up-shipping-agents.md)|
|Geben Sie Standardberichte an, die für verschiedene Dokumenttypen verwendet werden sollen.|[Berichtsauswahl in Business Central](across-report-selections.md)|
|Geben Sie an, ob Benutzer Verkaufsrechnungen buchen dürfen und ob sie diese zusammen mit einer Lieferung buchen müssen. |[Rechnungsbuchungsrichtlinie für Benutzer definieren](admin-setup-invoice-posting-policy.md)|

## Siehe auch
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
