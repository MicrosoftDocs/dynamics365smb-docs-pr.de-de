---
title: Feld "Status" in Belegen
description: Informieren Sie sich über den Status „Offen“ und „Freigegeben“ in Angebots-, Auftrags- oder Gutschriftdokumenten.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,
ms.search.form: ''
ms.date: 09/19/2022
ms.author: a-reishima
ms.openlocfilehash: c96909b4ee37673ee7b0c752224478a144ad853e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608164"
---
# <a name="status-field-on-documents"></a>Feld "Status" in Belegen

Wenn Sie ein Angebot/eine Anfrage, einen Verkaufsauftrag/eine Bestellung oder eine Gutschrift erstellen, enthält das Feld **Status** im Belegkopf als Vorgabewert den Status **Offen**.

Nachdem Sie den Beleg ausgefüllt haben, können Sie ihn freigeben und [!INCLUDE[prod_short](includes/prod_short.md)] ändert den Wert im Feld **Status** in **Freigegeben**. Dieser Status zeigt an, dass der Auftrag für den nächsten Bearbeitungsschritt bereit ist, bevor er dann gebucht wird.

| Status | Description |
| ------ | ----------- |
| Öffnen   | Sie können Änderungen an dem Beleg vornehmen. |
| Freigegeben | Der Beleg wurde für den nächsten Verarbeitungsschritt freigegeben, und Sie können keine Änderungen an Zeilen der Art *Artikel* und *Anlage* mehr vornehmen.<br /><br />Sie können einen freigegebenen Beleg wieder öffnen, wenn Sie Änderungen an seinem Inhalt vornehmen möchten. Um den überarbeiteten Beleg zum nächsten Verarbeitungsschritt weiterzuleiten, muss dieser erneut freigegeben werden. |
| Genehmigung ausstehend   | Der Beleg muss noch genehmigt werden. |
| Ausstehende Vorauszahlung | Eine Vorauszahlungsrechnung wurde für den Beleg gebucht. |

## <a name="releasing"></a>Freigeben

Sie können den Vorgang des Freigebens auf verschiedene Arten nutzen, so dass er gut in Ihren normalen Arbeitsablauf passt, z. B. um unternehmensüblichen Abläufen bezüglich Genehmigungen oder Logistikaktivitäten zu folgen.

### <a name="approval-procedures"></a>Genehmigungsverfahren

Ihr Unternehmen kann das Genehmigungsverfahren nutzen, um anzuzeigen, dass ein anderer Anwender das Dokument genehmigt hat oder dass eine externe Kontaktperson die Anforderungen im Beleg erfüllen kann, wie in folgenden Beispielen dargestellt:

* Sie können nur dann eine Bestellung freigeben, wenn Ihr Lieferant Ihnen mitgeteilt hat, dass er bereit ist, die bestellten Mengen auszuliefern.
* Sie legen eine Bestellung an und ein zweiter Anwender muss diese genehmigen, z. B. aus Sicherheitsgründen, bevor Sie sie freigeben dürfen.
* Eine Gutschrift, die Sie angelegt haben, muss von dem für alle Erstattungen verantwortlichen Manager freigegeben werden.

Erfahren Sie mehr über Genehmigungsworkflows unter [Verwenden Sie Arbeitsabläufe](across-use-workflows.md).

### <a name="warehouse-activities"></a>Lageraktivitäten

Wenn der Auftragsstatus **Offen** ist, beginnt das Lagerhaus nicht mit der Auslieferung und erwartet keinen Wareneingang von Artikeln in Bestellungen. Wenn Sie den Auftrag/die Bestellung freigeben, geben Sie zu verstehen, dass der Auftrag/die Bestellung vollständig ist und dass er/sie in den Aktivitäten des Lagerhauses berücksichtigt werden kann.

## <a name="reopening-a-released-order"></a>Eine freigegebene Bestellung wieder öffnen

Sie können Änderungen an einem freigegebenen Auftrag/einer freigegebenen Bestellung vornehmen, indem Sie ihn/sie wieder öffnen. Sie können jedoch die Mengen in Zeilen, die bereits vom Lagerhaus verarbeitet wurden, nur noch erhöhen.

Wenn Sie Ihre Änderungen vorgenommen haben und den Auftrag/die Bestellung wieder freigeben, werden die Mehrwertsteuer und den Rechnungsrabatt neu berechnet.

Wenn Sie Änderungen an einem freigegebenen Auftrag/einer freigegebenen Bestellung vornehmen, müssen Sie das Lagerhaus darüber in Kenntnis setzen.

> [!NOTE]
> Wenn Sie einen einzelnen offenen Auftrag oder eine einzelne offene Bestellung oder Gutschrift buchen möchten, ohne ihn/sie vorher freizugeben, gibt die Anwendung den Beleg automatisch beim Buchen frei. Wenn Sie Ihre Aufträge/Bestellungen oder Gutschriften buchen, indem Sie die **Stapelverarbeitung** verwenden, können Sie wählen, dass Sie nur die Aufträge/Bestellungen oder Gutschriften buchen möchten, die Sie freigegeben haben.

## <a name="see-also"></a>Siehe auch

[Produkte mit einem Verkaufsauftrag des Debitors verkaufen](sales-how-sell-products.md)  
[Einkäufe mit Einkaufsrechnungen erfassen](purchasing-how-record-purchases.md)  
[Versenden von Artikeln](warehouse-how-ship-items.md)  
[Empfangen von Artikeln](warehouse-how-receive-items.md)  
[Artikelgenehmigungsworkflow verwenden](across-how-use-approval-workflows.md)  
[Sortieren, Durchsuchen und Filtern von Listen](ui-enter-criteria-filters.md)  
[Beleg archivieren](across-how-to-archive-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
