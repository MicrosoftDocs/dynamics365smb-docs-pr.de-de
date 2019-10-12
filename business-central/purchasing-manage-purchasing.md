---
title: Überblick der Aufgaben zum Verwalten von Einkauf | Microsoft Docs
description: Zeigt die Aufgaben zum Verwalten der Einkaufs- oder Beschaffungsvorgänge, einschließlich das Vorgehen bei Einkaufsrechnungen und Bestellungen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 001a0ed999641529249ceb90913633f34c48b827
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312364"
---
# <a name="purchasing"></a>Einkauf
Sie erstellen eine Einkaufsrechnung oder Einkaufsbestellung, um die Kosten der Einkäufe zu erfassen und Kreditoren zu verfolgen. Wenn Sie einen Bestand steuern müssen, werden Einkaufsrechnungen auch verwendet, um Lagerbestände dynamisch zu aktualisieren, sodass Sie Ihre Lagerbestandskosten minimieren und besseren Kundenservice bereitstellen können. Die Einkaufskosten, einschließlich Servicekosten und Bestandswerte, die aus der Buchung von Einkaufsrechnungen resultieren, tragen zu den Gewinnzahlen und anderen finanziellen Kennziffern in Ihrem Rollencenter bei.

Sie müssen Einkaufsbestellungen verwenden, wenn es für den Einkaufsprozess erforderlich ist, Teillieferungen einer Bestellmenge zu erfassen, weil beispielsweise die vollständige Menge beim Kreditor nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Einkaufsbestellungen verwenden. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Einkaufsbestellungen genau wie bei Einkaufsrechnungen.

Sie können Verkaufsrechnungen automatisch erstellen lassen, indem Sie den OCR-Dienst (optische Zeichenerkennung) verwenden, um PDF-Rechnungen Ihrer Kreditoren zu elektronischen Dokumenten umwandeln, die dann zu Einkaufsrechnungen durch einen Workflow umgewandelt werden. Um diese Funktionalität nutzen zu können, müssen Sie den OCR-Service zuerst anmelden und dann verschiedene Einrichtungen ausführen. Weitere Informationen finden Sie unter [Eingehende Belege verarbeiten](across-process-income-documents.md).      

Produkte können Lagerartikel und Dienstleistungen sein. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

Für alle Einkaufsprozesse können Sie einen Genehmigungsworkflows einfügen, beispielsweise um große Einkäufe an bestimmten Kreditoren vom Buchhaltungs-Manager zu genehmigen. Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.

| An | Siehe |
| --- | --- |
| Erstellen Sie eine Einkaufsrechnung, um Ihre Vereinbarung mit dem Kreditor zu erfassen, bestimmte Produkte unter speziellen Lieferungs- und Zahlungsbedingungen zu kaufen. |[Erfassen eines Einkaufs](purchasing-how-record-purchases.md) |
|Erstellen Sie eine Einkaufsanfrage, um eine Anforderung für ein Angebot beim Lieferanten zu tragen, den Sie in eine Einkaufsbestellung umwandeln zu können.|[Angebotsanforderungen](purchasing-how-request-quotes.md)|
| Erstellen Sie eine Einkaufsrechnung für alle oder die ausgewählten Zeilen auf einer Verkaufsrechnung. |[Einkauf von Artikeln für einen Verkauf](purchasing-how-purchase-products-sale.md) |
|Verstehen, was passiert, wenn Sie Einkaufsbelege buchen.|[Einkäufe buchen](ui-post-purchases.md)|
| Aktionen ausführen in einer unbezahlten gebuchten Einkaufsrechnung, um einen Gutschriftsprozess automatisch zu erstellen, und entweder die Einkaufsrechnung zu stornieren oder neu zu erstellen um Korrekturen vorzunehmen. |[Ändern oder Löschen einer unbezahlten Verkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Erstellen Sie eine Einkaufsgutschrift, um eine bestimmte gebuchte Einkaufsrechnung wiederherzustellen, um anzugeben, welche Produkte Sie an den Kreditor zurückliefern und welchen Zahlungsbetrag Sie eintreiben. |[Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-register-new-vendors.md) |
|Bereiten Sie sich vor, um Lieferungen vom selben Kreditor einmal zu fakturieren, indem Sie die Wareneingänge in einer Rechnung zusammenfassen.|[Zusammenfassen von Lieferungen in einer einzelnen Rechnung](purchasing-how-to-combine-receipts.md)|
|Konvertieren Sie zum Beispiel elektronische Rechnungen von Ihren Kreditoren in Business Central in Einkaufsrechnungen.|[Vorgehensweise: Elektronische Belege empfangen und konvertieren](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Erfahren Sie, wie Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] wenn Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum geliefert wird.|[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)|
|Lösen Sie auf Verwirrung auf, wenn zwei oder mehr Datensätze für denselben Kreditor vorhanden sind.|[Doppelt Datensätze zusammenführen](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Siehe auch
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Projekte verwalten](projects-manage-projects.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
