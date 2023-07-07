---
title: Feld "Status" in Belegen
description: 'Informieren Sie sich über den Status „Offen“ und „Freigegeben“ in Angebots-, Auftrags- oder Gutschriftdokumenten.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents"></a>Feld "Status" in Belegen

Wenn Sie ein Angebot/eine Anfrage, einen Verkaufsauftrag/eine Bestellung oder eine Gutschrift erstellen, enthält das Feld **Status** im Belegkopf als Vorgabewert den Status **Offen**.

Nachdem Sie den Beleg ausgefüllt haben, können Sie ihn freigeben. Mit [!INCLUDE[prod_short](includes/prod_short.md)] ändert sich der Wert im Feld **Status** auf **Freigegeben**. Dieser Status zeigt an, dass der Auftrag für die nächste Verarbeitungsstufe bereit ist, bevor er gebucht wird.

| Status | Description |
| ------ | ----------- |
| Öffnen   | Sie können Änderungen an dem Beleg vornehmen. |
| Freigegeben | Der Beleg wurde für die nächste Verarbeitungsstufe freigegeben, und Sie können keine Änderungen an Zeilen des Typs *Artikel* und *Anlage* vornehmen.<br /><br />Sie können einen freigegebenen Beleg wieder öffnen, wenn Sie Änderungen an seinem Inhalt vornehmen möchten. Um den überarbeiteten Beleg zum nächsten Verarbeitungsschritt weiterzuleiten, muss dieser erneut freigegeben werden. |
| Genehmigung ausstehend   | Der Beleg muss noch genehmigt werden. |
| Ausstehende Vorauszahlung | Eine Vorauszahlungsrechnung wurde für den Beleg gebucht. |

## <a name="release-process"></a>Freigabe-Prozess

Sie können das Freigabeverfahren auf verschiedene Weise nutzen, um Ihren normalen Arbeitsablauf zu erleichtern, z.B. um die Verfahren der Firma für Genehmigungen zu befolgen oder um Lagerort-Aktivitäten zu starten.

### <a name="approval-procedures"></a>Genehmigungsverfahren

Ihre Firma kann das Freigabeverfahren verwenden, um anzuzeigen, dass ein anderer Benutzer den Beleg genehmigt hat oder dass ein externer Kontakt die Spezifikationen des Belegs erfüllen kann, wie in diesen Beispielen gezeigt:

* Sie können eine Bestellung erst freigeben, wenn Ihr Kreditor angegeben hat, dass er bereit ist, die Bestellung auszuführen.
* Sie erstellen eine Bestellung und ein zweiter Benutzer muss sie genehmigen, vielleicht aus Sicherheitsgründen, bevor Sie sie freigeben dürfen.
* Der Manager, der für die Genehmigung aller Rückerstattungen zuständig ist, muss eine Gutschrift freigeben, die Sie erstellt haben.

Erfahren Sie mehr über Genehmigungsworkflows unter [Verwenden Sie Arbeitsabläufe](across-use-workflows.md).

### <a name="warehouse-activities"></a>Lageraktivitäten

Wenn der Bestellstatus **Offen** ist, beginnt der Lagerort nicht mit der Vorbereitung der Lieferung und erwartet nicht, dass die Artikel einer Bestellung eingehen. Wenn Sie die Bestellung freigeben, geben Sie an, dass die Bestellung abgeschlossen ist und dass der Lagerort sie in seine Aktivitäten aufnehmen kann.

## <a name="reopen-a-released-order"></a>Eine freigegebene Bestellung wieder öffnen

Sie können Änderungen an einem freigegebenen Auftrag/einer freigegebenen Bestellung vornehmen, indem Sie ihn/sie wieder öffnen. Sie können jedoch die Mengen in Zeilen, die bereits vom Lagerhaus verarbeitet wurden, nur noch erhöhen.

Wenn Sie die Änderungen vornehmen und die Bestellung erneut freigeben, berechnet [!INCLUDE [prod_short](includes/prod_short.md)] die Mehrwertsteuer (VAT) und den Rechnungsrabatt neu.

Wenn Sie Änderungen an einem freigegebenen Auftrag/einer freigegebenen Bestellung vornehmen, müssen Sie das Lagerhaus darüber in Kenntnis setzen.

> [!NOTE]
> Wenn Sie eine einzelne offene Bestellung oder Gutschrift buchen möchten, ohne sie vorher freizugeben, gibt [!INCLUDE [prod_short](includes/prod_short.md)] den Beleg automatisch frei, wenn Sie ihn buchen. Wenn Sie Ihre Bestellungen oder Gutschriften mit der Funktion **Batch buchen** buchen, können Sie wählen, ob Sie nur die freigegebenen Bestellungen oder Gutschriften buchen möchten.

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
