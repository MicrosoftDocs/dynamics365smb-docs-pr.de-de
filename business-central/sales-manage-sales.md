---
title: Übersicht der Aufgaben zum Verwalten von Verkäufen
description: 'Lesen Sie alles darüber, wie Sie die Dienste von Business Central für die Verwaltung von Verkaufsaktivitäten mit Ihren Debitoren mit Verkaufsrechnungen, Aufträgen, Angeboten und mehr nutzen können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="sales"></a>Verkauf

Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.

Sie müssen Verkaufsaufträge verwenden, wenn der Verkaufsprozess dies erfordert, so dass Sie Teile einer Bestellmenge liefern können, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Verkaufsaufträge verwenden. In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Im Verkaufsauftrag können Sie die Funktionalität der Lieferterminzusage auch verwenden, um ein bestimmtes Lieferdatum Ihren Debitoren mitzuteilen.  

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung oder einen Verkaufsauftrag umwandeln können, wenn Sie dem Verkauf zustimmen. Nachdem der Debitor die Vereinbarung bestätigt hat, beispielsweise nach dem Angebotsprozess, können Sie eine Auftragsbestätigung senden, um Ihre Verpflichtung zu erfassen, die Produkte wie vereinbart zu liefern.

Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor der Debitor sie bezahlt. Zum Beispiel, um einen Tippfehler zu korrigieren oder wenn der Debitor frühzeitig im Bestellvorgang um eine Änderung bittet. Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift oder eine Verkaufsreklamation erstellen, um den Verkauf zu stornieren.

Bei Verkaufs- und Marketingmaßnahmen dreht sich alles um die richtige Entscheidung und das richtige Timing. Die Marketingfunktionalität in [!INCLUDE[prod_short](includes/prod_short.md)] gibt hierzu eine exakte und zeitnahe Übersicht über die Kontaktinformationen, damit Sie Interessenten gegenüber effizienter auftreten und die Debitorenzufriedenheit steigern können. Erfahren Sie mehr unter [Marketing und Vertrieb](marketing-relationship-management.md).

Wenn Sie Microsoft Dynamics 365 Sales für den Kontakt zu Ihren Kunde verwenden, können Sie [!INCLUDE [prod_short](includes/prod_short.md)] für die Backendaktivitäten verwenden und erreichen so eine nahtlose Integration mit dem Lead-to-Cash-Prozess. Zum Beispiel, um Aufträge abzuwickeln, den Lagerbestand zu verwalten und sich um Ihre Finanzen zu kümmern. Erfahren Sie mehr über [Dynamics 365 Sales von Business Central aus verwenden](marketing-integrate-dynamicscrm.md)

Im betrieblichen Umfeld, in dem der Debitor bezahlen muss, bevor Produkte, wie in der Einzelhandelsbranche, geliefert werden, müssen Sie den Zahlungseingang für die Produkte abwarten, bevor Sie die Produkte liefern. In den meisten Fällen verarbeiten Sie eingehende Zahlungen einige Wochen nach Lieferung, indem Sie die Zahlungen in ihre entsprechenden gebuchten, unbezahlten Verkaufsrechnungen übernehmen. Erfahren Sie mehr unter [Vorgehensweise zum Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Verkaufsbelege können als PDF-Dateien als E-Mail-Anhang gesendet werden. Der E-Mail-Text enthält einen Auszug des Verkaufsbelegs, wie Produkte, Gesamtbetrag und eine Verbindung zur PayPal-Seite. Erfahren Sie mehr unter [Artikel versenden und Dokumente per E-Mail versenden](ui-how-send-documents-email.md).

Sie können für alle Vertriebsprozesse einen Genehmigungsworkflow integrieren. Bei einem Genehmigungsworkflow kann es zum Beispiel notwendig sein, dass eine Führungskraft große Verkäufe an bestimmte Debitoren genehmigt. Erfahren Sie mehr unter [Workflows verwenden](across-use-workflows.md).

Die folgenden Abschnitte beschreiben eine Reihe von Aufgaben mit Links zu den Artikeln, die sich mit ihnen befassen.

## <a name="get-started-with-sales-capabilities"></a>Erste Schritte mit Finanzfunktionen

Legen Sie vor dem Verkauf fest, wie Sie die Vertriebsprozesse Ihres Unternehmens handhaben möchten.

|Zweck ...| Siehe |
|---|---|
| Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen.|[Neue Debitoren registrieren](sales-how-register-new-customers.md) |
| Festlegen, wie Sie den Verkauf abwickeln, beispielsweise Preise und Rabatte, Kundenpreis- und Rabattgruppen, Verkaufende, Versandmethoden und Agenten. | [Verkäufe einrichten](sales-setup-sales.md) |

## <a name="sales-analytics"></a>Vertriebsanalyse

In diesem Abschnitt werden die Analysetools beschrieben, mit denen Sie sich Einblick in Ihre Verkaufsdaten verschaffen können.

| Zweck ... | Siehe |
| --- | --- |
| Mehr über die Möglichkeiten zur Analyse von Verkaufsdaten erfahren. | [Vertriebsanalysen – Übersicht](sales-analytics-overview.md) |
| Ad-hoc-Analysen von Verkaufsdaten direkt auf Listenseiten und in Abfragen durchführen. | [Vertriebsanalyseberichte erstellen](bi-how-create-analysis-views-reports.md) |
| Integrierte Verkaufsberichte kennenlernen. | [Integrierte Vertriebsberichte](sales-reports.md) |

## <a name="quote-to-order-to-sales-invoice"></a>Vom Angebot zum Auftrag bis zur Verkaufsrechnung

In der folgenden Tabelle wird die Verwendung einfacher Verkaufsprozesse beschrieben.

|Zweck ...| Siehe |
|---|---|
| Erstellen Sie ein Verkaufsangebot, in dem Sie Produkte auf verkäuflichen Bedingungen anbieten, bevor Sie das Angebot in eine Verkaufsrechnung umwandeln. |[Verkaufsangebote erstellen](sales-how-make-offers.md) |
| Einen Verkaufsauftrag verarbeiten (vielleicht mit Teillieferungen oder einer Direktlieferung). |[Produkte verkaufen](sales-how-sell-products.md) |
| Erstellen Sie eine Verkaufsrechnung, um Ihre Vereinbarung mit dem Debitoren zu erfassen, um Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu verkaufen. |[Verkäufe fakturieren](sales-how-invoice-sales.md) |
|Verstehen, was passiert, wenn Sie Verkaufsbelege buchen.|[Verkäufe buchen](ui-post-sales.md)|

Wenn Sie komplexere Vertriebsprozesse benötigen, finden Sie in der folgenden Tabelle Artikel, die erklären, was Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] tun können.

|Zweck ...| Siehe |
|---|---|
| Erfüllen Sie einen Kundenauftrag mit mehreren Teillieferungen. | [Teillieferungen verarbeiten](sales-how-send-partial-shipments.md) |
| Richten Sie Standardverkaufscodes oder Standardeinkaufscodes, die Sie in Belegen beispielsweise für Wiederk Ersatzaufträge schnell einfügen können.|[Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)|  
|Verwalten der Abnahmegarantiemengen des Debitors, die im Zeitverlauf in mehreren Lieferungen geliefert werden.|[Arbeiten mit Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)|
|Einen Debitor einmal für mehrere Warenausgänge eine Rechnung stellen, indem Sie Lieferungen in einer Rechnung zusammenfassen.|[Lieferungen in einer einzelnen Rechnung zusammenfassen](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Montageartikel, die zu dem Zeitpunkt nicht verfügbar sind, durch einen Verknüpften Montageauftrag verkaufen. Über den Montageauftrag kann die volle oder eine Teilmenge des Verkaufsauftrags geliefert werden.|[Programmfertigungsartikel verkaufen](assembly-how-to-sell-items-assembled-to-order.md)|

## <a name="pick-and-ship"></a>Kommissionieren und ausliefern

In der folgenden Tabelle wird beschrieben, wie Sie Artikel für einen Verkaufsauftrag entnehmen und an den Debitor versenden.

| Zweck | Siehe |
| --- | --- |
|Bereiten Sie die Kommissionierung von Artikeln für den Warenausgang vor.|[Kommissionierliste drucken](sales-how-print-picking-list.md)|
| Verknüpfen Sie einen Verkaufsauftrag mit einer Bestellung, um einen Direktlieferungsartikel zu verkaufen, der direkt von Ihrem Kreditoren an Ihren Debitoren geliefert wird. |[Direktlieferungen machen](sales-how-drop-shipment.md) |
|Lassen Sie einen Katalogartikel von einem Kreditor an Ihr Lager liefern, so dass Sie den Artikel an Ihren Debitor liefern können.|[Spezialaufträge erstellen](sales-how-to-create-special-orders.md)|
|Informieren Sie Ihre Debitoren über das Auftragslieferdatum, indem Sie entweder das Möglichkeitsdatum für Beschaffungszusage oder das Lieferzusageversprechen berechnen.|[Datumsangaben für Lieferterminzusagen berechnen](sales-how-to-calculate-order-promising-dates.md)|
| Lernen, wie ein Paket aus einer gebuchten Verkaufslieferung verfolgt wird. | [Paketverfolgung](sales-how-track-packages.md) |

## <a name="canceled-orders-refunds-and-returns"></a>Stornierte Aufträge, Rückerstattungen und Retouren

In der nachfolgenden Tabelle wird der Umgang mit Stornierungen von Bestellungen, Rückerstattungen und Warenretouren beschrieben.

| Zweck | Siehe |
| --- | --- |
| Verwendungsfunktionen in einer unbezahlten gebuchten Verkaufsrechnung, um einen Gutschriftsprozess automatisch auszuführen, und entweder die Verkaufsrechnung zu stornieren oder neu zu erstellen, um Korrekturen vorzunehmen. |[Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md) |
| Erstellen Sie eine Verkaufsgutschrift, um eine bestimmte gebuchte Verkaufsrechnung wiederherzustellen, um anzugeben, welche Produkte der Debitor zurückschickt und welcher Betrag erstattet wird. |[Retouren oder Stornierungen verarbeiten](sales-how-process-sales-returns-cancellations.md) |

## <a name="other-processes-in-sales"></a>Andere Prozesse im Verkauf

In der folgenden Tabelle wird der Umgang mit anderen Verkaufsprozessen beschrieben.

| Zweck | Siehe |
| --- | --- |
|Lösen Sie auf Verwirrung auf, wenn zwei oder mehr Datensätze für denselben Debitor vorhanden sind.|[Doppelte Datensätze zusammenführen](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Siehe auch

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Neue Debitoren registrieren](sales-how-register-new-customers.md)  
[Überblick über Verkaufsanalysen](sales-analytics-overview.md)   
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allgemeine Unternehmensfunktionen](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
