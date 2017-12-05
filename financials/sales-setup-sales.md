---
title: "Überblick der Aufgaben zum konfigurieren von Verkaufsprozessen | Microsoft Docs"
description: "Gliedert die Aufgaben, um Regeln und Werte einzurichten, um Ihre Vertriebsrichtlinien und Arbeitsgänge zu definieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d94177e37fec6abf278dc8edac71b03c569c9581
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-sales"></a>Einrichten von Verkäufen
Bevor Sie Verkaufsprozesse verwalten können, müssen die Regeln und Werte konfiguriert werden, die die Vertriebsrichtlinien des Mandanten definieren.

Zuerst muss die allgemeine Einrichtung definiert werden, z. B. welche Verkaufsbelege erforderlich sind und wie deren Werte gebucht werden. Diese allgemeine Einrichtung erfolgt in der Regel einmal bei der anfänglichen Implementierung.

Eine separate Reihe von Aufgaben, die mit der Erfassung neuer Kreditoren im Zusammenhang stehen, dient dazu, alle Sonderpreis oder Rabattvereinbarungen zu speichern, die Sie mit einzelnen Kreditoren haben.

Einrichten von finanzbezogenen Verkäufen wie Zahlungsformen und Währungen werden im Finanzsetupabschnitt behandelt. Weitere Informationen finden Sie unter [Einrichten von Finanzen](finance-setup-finance.md).

| Aufgabe | Siehe |
| --- | --- |
| Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen. |[Vorgehensweise: Einen neuen Debitor registrieren](sales-how-register-new-customers.md) |
| Aktivieren Sie Debitoren, um über Paypal zu bezahlen, indem Sie das Paypal-Logo in Verkaufsbelegen auswählen. |[Gewusst wie: Aktivieren von Debitoren-Zahlungen durch Paypal](sales-how-enable-payment-service-extensions.md) |
| Geben Sie die verschiedenen Rabatte und alternativen Preise ein, die Sie den Debitoren abhängig von Artikel, Mengen und/oder Datum gewähren. |[Erfassen von Verkaufspreisen, Skonti und Zahlungsvereinbarungen](sales-how-record-sales-price-discount-payment-agreements.md) |
| Einrichten von Verkäufer, sodass Sie diese den Debitorenkontakten zuweisen können oder die Leistung des Verkaufspersonals messen können und als Basis für die Berechnung von Verkaufsprovisionen oder der Prämie zuweisen können. |[Gewusst wie: Verkäufer einrichten](sales-how-setup-salespeople.md) |
| Geben Sie für einzelne Debitoren oder für alle Debitoren an, wie Verkaufsbelege standardmäßig gesendet werden, wenn Sie die Aktion **Buchen und senden** auswählen. |[Vorgehensweise: Einrichten von Belegsendeprofilen](sales-how-setup-document-send-profiles.md) |
| Legen Sie die E-Mail a, um eine Zusammenfassung der Informationen des Verkaufsbelegs zu erhalten, der gesendet wird. |[Gewusst wie: Senden von Belegen über E-Mail](ui-how-send-documents-email.md). |
|Verwenden Sie einen EU-Webdienst, um die MwSt-IdNr. eines Debitors zu überprüfen.|[Vorgehensweise: Überprüfen der MwSt-IdNr.](finance-setup-vat.md)|
|Geben Sie Informationen über die verschiedenen eingesetzten Transportkreditoren ein, einschließlich einer Verknüpfung zu ihrem Paketverfolgungsservice.|[Vorgehensweise: Zusteller einrichten](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

