---
title: "Überblick der Aufgaben zum Verwalten von Verkäufen | Microsoft Docs"
description: "Beschreibt, wie Verkaufsaktivitäten verwaltet werden"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 06/30/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ebdcfc8c2be94398c1ebd7d5268a94b568e3b23b
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="sales"></a>Verkauf
Sie erstellen eine Verkaufsrechnung oder eine Bestellung, um Ihre Vereinbarung mit dem Kunden zu erfassen, um bestimmte Produkte unter speziellen Liefer- und Zahlungsbedingungen zu verkaufen.

Sie müssen Verkaufsaufträge verwenden, wenn der Verkaufsprozess dies erfordert, so dass Sie Teile einer Bestellmenge liefern können, weil beispielsweise die vollständige Menge nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Verkaufsaufträge verwenden. In allen anderen Aspekten ist das Vorgehen bei Verkaufsaufträgen gleich wie bei Verkaufsrechnungen.

Bei Verkaufs- und Marketingmaßnahmen dreht sich alles um die richtige Entscheidung und das richtige Timing. Die Marketingfunktionalität in [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt hierzu eine exakte und zeitnahe Übersicht über die Kontaktinformationen, damit Sie Interessenten gegenüber effizienter auftreten und die Kundenzufriedenheit steigern können. Weitere Informationen hierzu finden Sie unter [Relationsship Management](marketing-relationship-management.md).

Sie können mit dem Debitor verhandeln, indem Sie zuerst ein Verkaufsangebot erstellen, das Sie in eine Verkaufsrechnung umwandeln können, wenn Sie dem Verkauf zustimmen. Nachdem der Debitor die Vereinbarung bestätigt hat, beispielsweise nach dem Angebotsprozess, können Sie eine Auftragsbestätigung senden, um Ihre Verpflichtung zu erfassen, die Produkte wie vereinbart zu liefern.

Wenn Sie die Produkte teilweise oder gesamthaft liefern, buchen Sie die Verkaufsrechnung oder den Verkaufsauftrag als geliefert oder als geliefert und fakturiert, um den zugehörigen Artikel und die Debitorenposten im System zu erfassen.

Im betrieblichen Umfeld, in dem der Debitor bezahlen muss, bevor Produkte, wie in der Einzelhandelsbranche, geliefert werden, müssen Sie den Zahlungseingang für die Produkte abwarten, bevor Sie die Produkte liefern. In den meisten Fällen verarbeiten Sie eingehende Zahlungen einige Wochen nach Lieferung, indem Sie die Zahlungen in ihre entsprechenden gebuchten, unbezahlten Verkaufsrechnungen übernehmen. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Sie können eine gebuchte Verkaufsrechnung einfach korrigieren oder stornieren, bevor sie bezahlt wird. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn der Debitor eine Änderung früh im Bestellvorgang anfordert. Wenn die gebuchte Verkaufsrechnung bezahlt ist, müssen Sie eine Verkaufsgutschrift erstellen, um den Verkauf zu stornieren.

Verkaufsbelege können als PDF-Dateien als E-Mail-Anhang gesendet werden. Der E-Mail-Text enthält einen Auszug des Verkaufsbelegs, wie Produkte, Einstandsbetrag und eine Verbindung zur Paypal-Seite. Weitere Informationen finden Sie unter [Vorgehensweise: Senden von Belegen per E-Mail](ui-how-send-documents-email.md).

Für alle Verkaufsprozesse können Sie einen Genehmigungsworkflows einfügen, beispielsweise um große Verkäufe an bestimmten Debitoren vom Buchhaltungs-Manager zu genehmigen. Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.

| Aufgabe | Siehe |
| --- | --- |
| Erstellen Sie ein Verkaufsangebot, in dem Sie Produkte auf verkäuflichen Bedingungen anbieten, bevor Sie das Angebot in eine Verkaufsrechnung umwandeln. |[Vorgehensweise: Machen Sie ein Angebot](sales-how-make-offers.md) |
| Erstellen Sie eine Verkaufsrechnung, um Ihre Vereinbarung mit dem Kunden zu erfassen, um Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu verkaufen. |[Vorgehensweise: Fakturieren](sales-how-invoice-sales.md) |
| Verarbeiten Sie einen Verkaufsauftrag, der Teillieferung oder Direktlieferungen beinhaltet. |[Gewusst wie: Produkte verkaufen](sales-how-sell-products.md) |
|Richten Sie Standardverkaufscodes oder Standardeinkaufscodes, die Sie in Belegen beispielsweise für Wiederk Ersatzaufträge schnell einfügen können.|[Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)|  
| Verknüpfen Sie einen Verkaufsauftrag mit einer Bestellung, um einen Direktlieferungsartikel zu verkaufen, der direkt von Ihrem Lieferanten an Ihren Kunden geliefert wird. |[So geht's: Direktlieferungen erstellen](sales-how-drop-shipment.md) |
| Verwendungsfunktionen in einer unbezahlten gebuchten Verkaufsrechnung, um einen Gutschriftsprozess automatisch auszuführen, und entweder die Verkaufsrechnung zu stornieren oder neu zu erstellen, um Korrekturen vorzunehmen. |[Vorgehensweise: Ändern oder Löschen einer unbezahlten Verkaufsrechnung](sales-how-correct-cancel-sales-invoice.md) |
| Erstellen Sie eine Verkaufsgutschrift, um eine bestimmte gebuchte Verkaufsrechnung wiederherzustellen, um anzugeben, welche Produkte der Debitor zurückliefert und welchen Zahlungsbetrag Sie erstatten. |[Vorgehensweise: Verarbeiten einer Verkaufsrücklieferung oder von Stornierungen](sales-how-process-sales-returns-cancellations.md) |
| Erstellen Sie eine Debitorenkarte für jeden Debitor, an den Sie verkaufen. |[Vorgehensweise: Einen neuen Debitor registrieren](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Siehe auch
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.MD)  
[Projektmanagement](projects-manage-projects.md)    
[Lieferkette](madeira-supply-chain.md)      
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

