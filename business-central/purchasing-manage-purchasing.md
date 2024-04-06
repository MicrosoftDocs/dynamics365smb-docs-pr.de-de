---
title: Übersicht über die Aufgaben zum Verwalten von Einkäufen
description: 'Zeigt die Aufgaben zum Verwalten der Einkaufs- oder Beschaffungsvorgänge, einschließlich das Vorgehen bei Einkaufsrechnungen und Bestellungen.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="purchasing"></a>Einkauf

Sie erstellen eine Einkaufsrechnung oder Einkaufsbestellung, um die Kosten der Einkäufe zu erfassen und Kreditoren zu verfolgen. Wenn Sie einen Bestand steuern müssen, werden Einkaufsrechnungen auch verwendet, um Lagerbestände dynamisch zu aktualisieren, sodass Sie Ihre Lagerbestandskosten minimieren und besseren Kundenservice bereitstellen können. Die Einkaufskosten, einschließlich Servicekosten und Bestandswerte, die aus der Buchung von Einkaufsrechnungen resultieren, tragen zu den Gewinnzahlen und anderen finanziellen Kennziffern in Ihrem Rollencenter bei.

Sie müssen Einkaufsbestellungen verwenden, wenn es für den Einkaufsprozess erforderlich ist, Teillieferungen einer Bestellmenge zu erfassen, weil beispielsweise die vollständige Menge beim Kreditor nicht sofort verfügbar ist. Wenn Sie Artikel als Direktlieferung verkaufen, indem Sie direkt von Ihrem Kreditor an Ihren Debitor versenden, müssen Sie ebenfalls Einkaufsbestellungen verwenden. Weitere Informationen finden Sie unter [Direktlieferungen erstellen](sales-how-drop-shipment.md) In allen anderen Aspekten ist das Vorgehen bei Einkaufsbestellungen genau wie bei Einkaufsrechnungen.

Sie können Verkaufsrechnungen automatisch erstellen lassen, indem Sie den OCR-Dienst (optische Zeichenerkennung) verwenden, um PDF-Rechnungen Ihrer Kreditoren zu elektronischen Dokumenten umwandeln, die dann zu Einkaufsrechnungen durch einen Workflow umgewandelt werden. Um diese Funktionalität nutzen zu können, müssen Sie den OCR-Service zuerst anmelden und dann verschiedene Einrichtungen ausführen. Weitere Informationen finden Sie unter [Eingehende Belege](across-income-documents.md).

Produkte können Lagerartikel und Dienstleistungen sein. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

Für alle Einkaufsprozesse können Sie einen Genehmigungsworkflows einfügen, beispielsweise um große Einkäufe an bestimmten Kreditoren vom Buchhaltungs-Manager zu genehmigen. Weitere Informationen erhalten Sie unter [Genehmigungsworkflow verwenden](across-how-use-approval-workflows.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..

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
| Erfahren Sie, wie Sie [!INCLUDE[prod_short](includes/prod_short.md)] wenn Sie einen Artikel bestellen müssen, damit er zu einem bestimmten Datum geliefert wird.|[Terminberechnung für Einkäufe](purchasing-date-calculation-for-purchases.md)|
|Lösen Sie auf Verwirrung auf, wenn zwei oder mehr Datensätze für denselben Kreditor vorhanden sind.|[Doppelt Datensätze zusammenführen](sales-how-merge-duplicate-records.md)|
|Verwalten Sie Ihre Verpflichtung gegenüber einem Lieferanten, große Mengen zu kaufen, die im Laufe der Zeit in mehreren Sendungen geliefert werden.|[Arbeiten mit Rahmenbestellungen](sales-how-to-create-blanket-sales-orders.md)|

## <a name="external-document-numbers"></a>Externe Belegnummern

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-also"></a>Siehe auch

[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Neue Kreditoren einrichten](purchasing-how-register-new-vendors.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
