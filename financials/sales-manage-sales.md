---
title: "Überblick der Aufgaben zum Verwalten von Verkäufen | Microsoft Docs"
description: "Beschreibt, wie Verkaufsaktivitäten verwaltet werden"
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 95f235e743ed97b1ac90a6e0583b9bd19dcb7ead
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="sales"></a>Verkauf
Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Kunden zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.

Sie müssen Verkaufsaufträge verwenden, wenn der Verkaufsprozess dies erfordert, so dass Sie Teile einer Bestellmenge liefern können, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Verkaufsaufträge verwenden. In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen. Im Verkaufsauftrag können Sie die Funktionalität der Lieferterminzusage auch verwenden, um ein bestimmtes Lieferdatum Ihren Debitoren mitzuteilen.  

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung oder einen Verkaufsauftrag umwandeln können, wenn Sie dem Verkauf zustimmen. Nachdem der Debitor die Vereinbarung bestätigt hat, beispielsweise nach dem Angebotsprozess, können Sie eine Auftragsbestätigung senden, um Ihre Verpflichtung zu erfassen, die Produkte wie vereinbart zu liefern.

Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift oder eine Verkaufsreklamation erstellen, um den Verkauf zu stornieren.

Bei Verkaufs- und Marketingmaßnahmen dreht sich alles um die richtige Entscheidung und das richtige Timing. Die Marketingfunktionalität in [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt hierzu eine exakte und zeitnahe Übersicht über die Kontaktinformationen, damit Sie Interessenten gegenüber effizienter auftreten und die Kundenzufriedenheit steigern können. Weitere Informationen hierzu finden Sie unter [Relationsship Management](marketing-relationship-management.md).

Im betrieblichen Umfeld, in dem der Debitor bezahlen muss, bevor Produkte, wie in der Einzelhandelsbranche, geliefert werden, müssen Sie den Zahlungseingang für die Produkte abwarten, bevor Sie die Produkte liefern. In den meisten Fällen verarbeiten Sie eingehende Zahlungen einige Wochen nach Lieferung, indem Sie die Zahlungen in ihre entsprechenden gebuchten, unbezahlten Verkaufsrechnungen übernehmen. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Verkaufsbelege können als PDF-Dateien als E-Mail-Anhang gesendet werden. Der E-Mail-Text enthält einen Auszug des Verkaufsbelegs, wie Produkte, Einstandsbetrag und eine Verbindung zur Paypal-Seite. Weitere Informationen finden Sie unter [Vorgehensweise: Senden von Belegen per E-Mail](ui-how-send-documents-email.md).

Für alle Verkaufsprozesse können Sie einen Genehmigungsworkflows einfügen, beispielsweise um große Verkäufe an bestimmten Debitoren vom Buchhaltungs-Manager zu genehmigen. Weitere Informationen erhalten Sie unter [Workflows verwenden](across-use-workflows.md).

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.

| Aufgabe | Siehe |
| --- | --- |
| Erstellen Sie ein Verkaufsangebot, in dem Sie Produkte auf verkäuflichen Bedingungen anbieten, bevor Sie das Angebot in eine Verkaufsrechnung umwandeln. |[Vorgehensweise: Machen Sie ein Angebot](sales-how-make-offers.md) |
| Erstellen Sie eine Verkaufsrechnung, um Ihre Vereinbarung mit dem Kunden zu erfassen, um Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu verkaufen. |[Vorgehensweise: Fakturieren](sales-how-invoice-sales.md) |
| Verarbeiten Sie einen Verkaufsauftrag, der Teillieferung oder Direktlieferungen beinhaltet. |[Gewusst wie: Produkte verkaufen](sales-how-sell-products.md) |
|Richten Sie Standardverkaufscodes oder Standardeinkaufscodes, die Sie in Belegen beispielsweise für Wiederk Ersatzaufträge schnell einfügen können.|[Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)|  
| Verknüpfen Sie einen Verkaufsauftrag mit einer Bestellung, um einen Direktlieferungsartikel zu verkaufen, der direkt von Ihrem Lieferanten an Ihren Kunden geliefert wird. |[So geht's: Direktlieferungen erstellen](sales-how-drop-shipment.md) |
|Lassen Sie einen Katalogartikel von einem Kreditor an Ihr Lager liefern, so dass Sie den Artikel an Ihren Debitor liefern können.|[Vorgehensweise: Spezialaufträge erstellen](sales-how-to-create-special-orders.md)|
| Verwendungsfunktionen in einer unbezahlten gebuchten Verkaufsrechnung, um einen Gutschriftsprozess automatisch auszuführen, und entweder die Verkaufsrechnung zu stornieren oder neu zu erstellen, um Korrekturen vorzunehmen. |[Vorgehensweise: Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md) |
| Erstellen Sie eine Verkaufsgutschrift, um eine bestimmte gebuchte Verkaufsrechnung wiederherzustellen, um anzugeben, welche Produkte der Debitor zurückliefert und welchen Zahlungsbetrag Sie erstatten. |[Vorgehensweise: Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md) |
|Verwalten der Abnahmegarantiemengen des Debitors, die im Zeitverlauf in mehreren Lieferungen geliefert werden.|[Vorgehensweise: Arbeiten mit Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)|
|Verkaufen Sie Montageartikel, die zu dem Zeitpunkt nicht verfügbar sind, indem Sie einen verknüpften Montageauftrag erstellen, um die gesamte oder einen Teil der Verkaufauftragsmenge zu beziehen.|[Vorgehensweise: Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md)|
|Einen Debitor einmal für mehrere Warenausgänge eine Rechnung stellen, indem Sie Lieferungen in einer Rechnung zusammenfassen.|[Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informieren Sie Ihre Debitoren über das Auftragslieferdatum, indem Sie entweder das Möglichkeitsdatum für Beschaffungszusage oder das Lieferzusageversprechen berechnen.|[So wird's gemacht: Lieferterminzusagen berechnen](sales-how-to-calculate-order-promising-dates.md)|

## <a name="see-also"></a>Siehe auch
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Vorgehensweise: Einen neuen Debitor registrieren](sales-how-register-new-customers.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Projektmanagement](projects-manage-projects.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

