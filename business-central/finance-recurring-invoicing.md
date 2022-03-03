---
title: Mit wiederkehrenden Umsätzen arbeiten
description: Erfahren Sie mehr über die verfügbaren Optionen zum automatischen Senden von Abonnementrechnungen an Ihre Kunden und zum Registrieren wiederkehrender Einnahmen.
author: AndreiPanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: recurring, invoicing, subscription, billing
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
ms.openlocfilehash: cf990ec5de639054a79e98275be76cb0aed989d1
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8128791"
---
# <a name="work-with-recurring-revenue-in-prod_short"></a>Arbeiten mit wiederkehrenden Umsätzen in [!INCLUDE[prod_short](includes/prod_short.md)]

Viele Unternehmen wechseln von einem Geschäftsumsatzmodell, bei dem der Umsatz aus dem einmaligen Kauf eines Debitors erzielt wird, zu einem Abonnementmodell, bei dem der Umsatz durch die Bereitstellung eines dauerhaften Zugangs zu einer Ware oder Dienstleistung regelmäßig erzielt wird.
[!INCLUDE[prod_short](includes/prod_short.md)] bietet folgende Optionen zur Automatisierung des Sendes von Abonnementrechnungen an Ihre Debitoren und zur Registrierung wiederkehrender Umsätze. 

## <a name="register-revenue-with-a-recurring-general-journal"></a>Registrieren von Umsatz mit einem wiederkehrenden Fibu Buch.-Blatt

Bei einem wiederkehrenden Buch.-Blatt handelt es sich um ein Fibu Buch.-Blatt mit speziellen Feldern zur Verwaltung von Transaktionen, die häufig und nur mit geringfügigen oder keinen Änderungen gebucht werden (z. B. Mieten, Abonnements, Strom- oder Heizungsrechnungen). Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Mit einem wiederkehrenden Buchungsblatt müssen Posten, die regelmäßig gebucht werden, nur einmal eingetippt werden. Das bedeutet, dass Einträge wie Konten, Dimensionen oder Dimensionswerte nach der Buchung im Buchungsblatt verbleiben. Werden Anpassungen notwendig, können Sie diese mit jeder Buchung durchführen.

### <a name="why-use-this-option"></a>Warum sollten Sie diese Option verwenden?

Mit dieser Option definieren Sie flexible Fakturierungsintervalle mit [Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).

Mit dieser Option können Sie in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] jedoch keine Rechnungen drucken und senden.  

Weitere Informationen finden Sie unter [Arbeiten mit wiederkehrenden Buch.-Blättern](ui-work-general-journals.md#working-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Erstellen mehrerer Rechnungen basierend auf einem wiederkehrenden Projekt-Buch.-Blatt

Das wiederkehrende Projekt-Buch.-Blatt ist eine erweiterte Alternative zum Fibu Buch.-Blatt. Sie definieren Artikel, Ressourcen und Sachkonten, die für jedes Projekt wiederholt werden müssen, und Sie geben die Häufigkeit der Wiederholung an.  

Nach dem Buchen eines wiederkehrenden Projekt-Buch.-Blatts können Sie mit der Aufgabe **Projektverkaufsrechnung erstellen** mehrere Rechnungen erstellen. Sie können erstellte Rechnungen auf der Seite **Verkaufsrechnungen** überprüfen und buchen.

### <a name="why-use-this-option"></a>Warum sollten Sie diese Option verwenden?

Mit dieser Option gehen Sie gemäß dem Standard-Fakturierungsverfahren mit allen seinen Vorteilen vor, Standard- und Debitorenlayouts für Kommunikationspräferenzen eingeschlossen. Sie können die Preise für jedes Projekt auch einzeln definieren.

Für jeden neuen Debitor müssen Sie jedoch ein neues Projekt erstellen und dem wiederkehrenden Buch.-Blatt Zeilen hinzufügen. 

Weitere Informationen finden Sie unter [Erstellen von Projekt-Buch.-Blattzeilen](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) und [Erstellen mehrerer Projektverkaufsrechnungen](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Erstellen mehrerer Rechnungen basierend auf wiederkehrenden Verkaufszeilen

Wenn Sie häufiger Verkaufs- und Einkaufszeilen mit ähnlichen Daten erstellen müssen, können Sie wiederkehrende Verkaufszeilen einrichten, die Sie anschließend in wiederkehrende Verkaufs- und Einkaufsbelege, z. B. in wiederkehrende Ersatzaufträge, einfügen können. Verwenden Sie den Batchauftrag **Wiederkehrende Verkaufsrechnungen erstellen**, um Verkaufsrechnungen gemäß wiederkehrenden Verkaufszeilen zu erstellen, die den Debitoren zugeordnet sind und Buchungsdaten enthalten, die innerhalb der Gültigkeitszeiträume liegen, die Sie in den wiederkehrenden Verkaufszeilen festgelegt haben.  

### <a name="why-use-this-option"></a>Warum sollten Sie diese Option verwenden?

Mit dieser Option können Sie mehreren Debitoren dieselben wiederkehrenden Zeilen zuweisen. Sie können die Gültigkeitsdauer für die wiederkehrenden Verkaufszeilen für einen bestimmten Debitor definieren. Sie können demselben Debitor mehrere wiederkehrende Zeilen zuweisen, die alle in der Rechnung enthalten sein werden.

Es gibt jedoch keine Möglichkeit, Festpreise für Artikel festzulegen, da [!INCLUDE[prod_short](includes/prod_short.md)] die am Dokumentdatum gültigen tatsächlichen Preise und Rabatte verwenden und versuchen wird, die beste Kombination für den niedrigsten Preis zu finden.  

Weitere Informationen finden Sie unter [Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a>Wiederkehrende Rechnungen mit Servicevertrag

Ein Servicevertrag enthält die Servicevertragsvereinbarungen zwischen den Debitoren und dem Unternehmen. Ein Servicevertrag beinhaltet servicebezogene Vereinbarungen sowie die Serviceartikel, für die Sie als Vertragsbestandteil Serviceleistungen erbringen.  

Sie können das Startdatum des Vertrags festlegen, das Fakturierungsintervall, ob der Vertrag im Voraus bezahlt wird oder nicht, sowie Details zur Preisaktualisierung, falls Sie die Preise ändern möchten, während der Vertrag aktiv ist. Sie können sowohl Serviceartikel als auch Artikel in Servicevertragszeilen verwenden.
Sie können Vertragsvorlagen erstellen, um die Erstellungsweise für verschiedene Vertragsarten zu definieren.  

### <a name="why-use-this-option"></a>Warum sollten Sie diese Option verwenden?

Mit dieser Option verwenden Sie einen Teil der erweiterten Serviceverwaltungsfunktionen, die nicht nur auf die Ausstellung wiederkehrender Rechnungen beschränkt sind, sondern auch die Abläufe in Werkstatt und Außendienst unterstützen.

Für diese Option wird jedoch die Premium-Lizenz benötigt. Einrichtung und Verwaltung der Serviceverwaltung bieten bei einfacheren Abonnementszenarien möglicherweise keine großen Vorteile.  

Weitere Informationen finden Sie unter [Arbeiten mit Serviceverträgen und Servicevertragsangeboten](service-how-to-create-service-contracts-and-service-contract-quotes.md) und [Mehrere Serviceverträge in Rechnung stellen](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a>Zugehörige Funktionen
Es gibt mehrere zugehörige Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a>Verkauf Rahmenauftrag

Ein Verkauf Rahmenauftrag stellt ein Gerüst für eine langfristige Vereinbarung zwischen Ihrem Unternehmen und einem Debitor dar.
Ein Rahmenauftrag wird in der Regel erstellt, wenn sich ein Debitor verpflichtet hat, größere Mengen abzunehmen, die über einen längeren Zeitraum in mehreren kleineren bereitgestellt werden. Häufig decken Rahmenaufträge nur einen bestimmten Artikel ab, für den bestimmte Liefertermine vorgegeben sind. Der Hauptgrund für die Verwendung eines Rahmenauftrags anstelle eines Verkaufsauftrags besteht darin, dass die bei einem Rahmenauftrag eingegebenen Mengen keinen Einfluss auf die Artikelverfügbarkeit haben, aber zu Planungszwecken verwendet werden können.

#### <a name="why-use-this-option"></a>Warum sollten Sie diese Option verwenden?

Mit dieser Option verwenden Sie den voraussichtlichen Bedarf, sodass die Informationen während den normalen Planungsroutinen berücksichtigt werden. Weitere Informationen finden Sie unter [Absatzplanungen und Rahmenaufträge](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Die Standardversion bietet jedoch keine sofort einsatzbereite Möglichkeit, mehrere Rahmenaufträge in großen Mengen zu verarbeiten.

Weitere Informationen finden Sie unter [Arbeiten mit Verkauf Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a>Wiederkehrende Aufträge (Norwegen)

Sie können wiederkehrende Aufträge verwenden, um Vorlagen für Rahmenaufträge zu erstellen, sodass Verkaufsaufträge basierend auf von Ihnen festgelegten Datumsintervallen erstellt werden können. Wenn Sie beispielsweise alle zwei Wochen denselben Verkaufsauftrag liefern, können Sie einen Verkauf Rahmenauftrag verwenden und wiederkehrende Bestellungen erstellen.
Sie können wiederkehrende Gruppen verwenden, um eine Reihe von Parametern zu definieren, die zeigen, wie Sie Bestellungen aufgeben. Diese Gruppen sind Rahmenaufträgen zugeordnet, die regelmäßig angelegt werden müssen. Um die wiederkehrenden Bestellungen zu erstellen, müssen Sie den Prozess zum Erstellen wiederkehrender Bestellungen regelmäßig ausführen. 

#### <a name="why-use-this-option"></a>Warum sollten Sie diese Option verwenden?

Mit dieser Option können Sie zwischen festen und „besten“ Preisen wählen.

Diese Option ist jedoch nur in Norwegen verfügbar. Die Gültigkeitsdauer kann auf der Ebene der wiederkehrenden Gruppen definiert werden.

Weitere Informationen finden Sie unter [Wiederkehrende Aufträge](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Wiederkehrende Umsätze und Abonnementabrechnungen durch andere Anbieter

Unter [AppSource.microsoft.com](https://appsource.microsoft.com/) können Sie Erweiterungen für Business Central abrufen. Einige Erweiterungen werden von Microsoft bereitgestellt, und andere Erweiterungen werden von anderen anderen Unternehmen bereitgestellt. Die Liste der Erweiterungen durch andere Unternehmen wächst jeden Monat. Rufen Sie regelmäßig [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) auf und holen Sie sich die Apps, die Ihnen das Arbeiten in Business Central erleichtern.  

## <a name="see-also"></a>Siehe auch

[Datumsformeln](ui-enter-date-ranges.md#using-date-formulas)  
[Arbeiten mit wiederkehrenden Buchblättern](ui-work-general-journals.md#working-with-recurring-journals)  
[Erstellen von Projekt-Buch.-Blattzeilen](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Erstellen mehrerer Projektverkaufsrechnungen](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md)  
[Arbeiten mit Serviceverträgen und Servicevertragsangeboten](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Mehrere Serviceverträge in Rechnung stellen](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Absatzplanungen und Rahmenaufträge Nachfrage](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Arbeiten mit Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)  
[Wiederkehrende Aufträge (Norwegen)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]