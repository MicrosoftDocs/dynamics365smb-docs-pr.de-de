---
title: Übersicht der Aufgaben zum Verwalten von Verkäufen
description: 'Lesen Sie alles darüber, wie Sie die Dienste von Business Central für die Verwaltung von Verkaufsaktivitäten mit Ihren Debitoren mit Verkaufsrechnungen, Aufträgen, Angeboten und mehr nutzen können.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'trade, sell'
ms.search.form: 253
ms.date: 09/02/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="sales"></a>Verkauf

Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.

Sie müssen Verkaufsaufträge verwenden, wenn der Verkaufsprozess dies erfordert, so dass Sie Teile einer Bestellmenge liefern können, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Verkaufsaufträge verwenden. In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Im Verkaufsauftrag können Sie die Funktionalität der Lieferterminzusage auch verwenden, um ein bestimmtes Lieferdatum Ihren Debitoren mitzuteilen.  

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung oder einen Verkaufsauftrag umwandeln können, wenn Sie dem Verkauf zustimmen. Nachdem der Debitor die Vereinbarung bestätigt hat, beispielsweise nach dem Angebotsprozess, können Sie eine Auftragsbestätigung senden, um Ihre Verpflichtung zu erfassen, die Produkte wie vereinbart zu liefern.

Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift oder eine Verkaufsreklamation erstellen, um den Verkauf zu stornieren.

Bei Verkaufs- und Marketingmaßnahmen dreht sich alles um die richtige Entscheidung und das richtige Timing. Die Marketingfunktionalität in [!INCLUDE[prod_short](includes/prod_short.md)] gibt hierzu eine exakte und zeitnahe Übersicht über die Kontaktinformationen, damit Sie Interessenten gegenüber effizienter auftreten und die Debitorenzufriedenheit steigern können. Erfahren Sie mehr unter [Marketing und Vertrieb](marketing-relationship-management.md).

Wenn Sie Microsoft Dynamics 365 Sales for Customer Engagement verwenden, können Sie eine nahtlose Integration in den Interessent-zu-Bargeld-Prozess nutzen, indem Sie Business Central für Backend-Aktivitäten wie Auftragsverarbeitung, Lagerbestandsverwaltung und Finanzbearbeitung verwenden. Erfahren Sie mehr über [Dynamics 365 Sales von Business Central aus verwenden](marketing-integrate-dynamicscrm.md)

Im betrieblichen Umfeld, in dem der Debitor bezahlen muss, bevor Produkte, wie in der Einzelhandelsbranche, geliefert werden, müssen Sie den Zahlungseingang für die Produkte abwarten, bevor Sie die Produkte liefern. In den meisten Fällen verarbeiten Sie eingehende Zahlungen einige Wochen nach Lieferung, indem Sie die Zahlungen in ihre entsprechenden gebuchten, unbezahlten Verkaufsrechnungen übernehmen. Erfahren Sie mehr unter [Vorgehensweise zum Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Verkaufsbelege können als PDF-Dateien als E-Mail-Anhang gesendet werden. Der E-Mail-Text enthält einen Auszug des Verkaufsbelegs, wie Produkte, Einstandsbetrag und eine Verbindung zur PayPal-Seite. Erfahren Sie mehr unter [Artikel versenden und Dokumente per E-Mail versenden](ui-how-send-documents-email.md).

Für alle Verkaufsprozesse können Sie einen Genehmigungsworkflows einfügen, beispielsweise um große Verkäufe an bestimmten Debitoren vom Buchhaltungs-Manager zu genehmigen. Erfahren Sie mehr unter [Workflows verwenden](across-use-workflows.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

| Bis | Siehe |
| --- | --- |
|Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen.|[Registriert einen neuen Debitor](sales-how-register-new-customers.md)|
| Erstellen Sie ein Verkaufsangebot, in dem Sie Produkte auf verkäuflichen Bedingungen anbieten, bevor Sie das Angebot in eine Verkaufsrechnung umwandeln. |[Verkaufsangebote machen](sales-how-make-offers.md) |
| Erstellen Sie eine Verkaufsrechnung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu verkaufen. |[Fakturieren eines Verkaufs](sales-how-invoice-sales.md) |
| Verarbeiten Sie einen Verkaufsauftrag, der Teillieferung oder Direktlieferungen beinhaltet. |[Produkte verkaufen](sales-how-sell-products.md) |
|Verstehen, was passiert, wenn Sie Verkaufsbelege buchen.|[Verkäufe buchen](ui-post-sales.md)|
|Bereiten Sie die Kommissionierung von Artikeln für den Warenausgang vor.|[Kommissionierliste drucken](sales-how-print-picking-list.md)|
| Erfüllen Sie einen Kundenauftrag mit mehreren Teillieferungen. | [Teillieferungen verarbeiten](sales-how-send-partial-shipments.md) |
|Richten Sie Standardverkaufscodes oder Standardeinkaufscodes, die Sie in Belegen beispielsweise für Wiederk Ersatzaufträge schnell einfügen können.|[Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)|  
| Verknüpfen Sie einen Verkaufsauftrag mit einer Bestellung, um einen Direktlieferungsartikel zu verkaufen, der direkt von Ihrem Kreditoren an Ihren Debitoren geliefert wird. |[Direktlieferungen machen](sales-how-drop-shipment.md) |
|Lassen Sie einen Katalogartikel von einem Kreditor an Ihr Lager liefern, so dass Sie den Artikel an Ihren Debitor liefern können.|[Spezialaufträge erstellen:](sales-how-to-create-special-orders.md)|
| Verwendungsfunktionen in einer unbezahlten gebuchten Verkaufsrechnung, um einen Gutschriftsprozess automatisch auszuführen, und entweder die Verkaufsrechnung zu stornieren oder neu zu erstellen, um Korrekturen vorzunehmen. |[Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md) |
| Erstellen Sie eine Verkaufsgutschrift, um eine bestimmte gebuchte Verkaufsrechnung wiederherzustellen, um anzugeben, welche Produkte der Debitor zurückliefert und welchen Zahlungsbetrag Sie erstatten. |[Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md) |
|Verwalten der Abnahmegarantiemengen des Debitors, die im Zeitverlauf in mehreren Lieferungen geliefert werden.|[Arbeiten mit Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)|
|Verkaufen Sie Montageartikel, die zu dem Zeitpunkt nicht verfügbar sind, indem Sie einen verknüpften Montageauftrag erstellen, um die gesamte oder einen Teil der Verkaufauftragsmenge zu beziehen.|[Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md)|
|Einen Debitor einmal für mehrere Warenausgänge eine Rechnung stellen, indem Sie Lieferungen in einer Rechnung zusammenfassen.|[Zusammenfassen von Lieferungen in einer einzelnen Rechnung](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informieren Sie Ihre Debitoren über das Auftragslieferdatum, indem Sie entweder das Möglichkeitsdatum für Beschaffungszusage oder das Lieferzusageversprechen berechnen.|[Lieferterminzusagen-Daten berechnen](sales-how-to-calculate-order-promising-dates.md)|
|Lösen Sie auf Verwirrung auf, wenn zwei oder mehr Datensätze für denselben Debitor vorhanden sind.|[Doppelte Datensätze zusammenführen](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Siehe auch

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Neue Debitoren registrieren](sales-how-register-new-customers.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Projektmanagement](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
