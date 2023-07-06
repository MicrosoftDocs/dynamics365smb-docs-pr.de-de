---
title: Fertigung durch Fremdarbeitsvertrag
description: 'Dieses Thema gibt einen erweiterten Überblick über die erweiterte Funktionalität der Lohnbearbeitung in Business Central, einschließlich Arbeitsplatzfelder und Arbeitspläne.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 99000886
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="subcontract-manufacturing"></a><a name="subcontract-manufacturing"></a><a name="subcontract-manufacturing"></a>Fertigung durch Fremdarbeitsvertrag

Ausgewählte Arbeitsgänge an Kreditoren weiter zu vergeben, ist in vielen Fertigungsunternehmen üblich. Fremdarbeit kann ein seltener Vorgang oder integraler Bestandteil aller Fertigungsschritte sein.

[!INCLUDE[prod_short](includes/prod_short.md)] gibt mehrere Werkzeuge für das Verwalten von Fremdarbeit:  

- Arbeitsplatzgruppen mit zugewiesenen Kreditoren: Mit dieser Funktion können Sie eine Arbeitsgruppe einrichten, die einem Kreditor (Subunternehmer) zugewiesen ist. Eine solche Arbeitsplatzgruppe wird als Arbeitsplatzgruppe für Fremdarbeit bezeichnet. Sie können eine Arbeitsplatzgruppe für Fremdarbeit für einen Arbeitsplanvorgang angeben, wodurch Sie die als Fremdarbeit vergebene Aktivität problemlos verarbeiten können. Außerdem können Sie die Kosten des Vorgangs auf Arbeitsplan- oder Arbeitsplatzebene kennzeichnen.  
- Arbeitsplatzgruppenkosten auf Basis von Einheiten oder Zeit: Über diese Funktion können Sie angeben, ob Kosten, die der Arbeitsplatzgruppe zugewiesen sind, auf einer Fertigungszeit oder einem Pauschalbetrag pro Einheit basieren. Üblicherweise stellen Subunternehmer für ihre Leistungen einen Pauschalbetrag pro Einheit in Rechnung; die Anwendung kann aber mit den beiden Optionen (Fertigungszeit und Pauschalbetrag pro Einheit) umgehen.  
- Fremdarbeitenarbeitsblatt: Mit dieser Funktion können Sie nach den Fertigungsaufträgen mit Material suchen, die an einen Subunternehmer gesendet werden können, und können Sie automatisch aus Arbeitsplänen für Fertigungsaufträge Einkaufsbestellungen für Fremdarbeitsvorgänge erstellen. Die Anwendung bucht automatisch die Einkaufsbestellung zum Produktionsauftrag während die Einkaufsbestellung gebucht wird. Ein Fertigungsauftrag muss den Status "Freigegeben" haben, damit aus einem Fremdarbeitenarbeitsblatt auf ihn zugegriffen und er dort verwendet werden kann.  

## <a name="subcontract-work-centers"></a><a name="subcontract-work-centers"></a><a name="subcontract-work-centers"></a>Arbeitsplatzgruppen für Fremdarbeiten
Arbeitsplatzgruppen für Fremdarbeiten werden auf gleiche Weise eingerichtet wie normale Arbeitsplatzgruppen, allerdings mit weiteren Informationen. Arbeitsplänen werden sie in gleicher Weise zugewiesen wie andere Arbeitsplatzgruppen.  

### <a name="subcontract-work-center-fields"></a><a name="subcontract-work-center-fields"></a><a name="subcontract-work-center-fields"></a>Felder unter "Arbeitsplatzgruppen für Fremdarbeiten"
Das Feld **Kreditorennr.** kennzeichnet die Arbeitsplatzgruppe als Arbeitsplatzgruppe für Fremdarbeit. Sie können die Nummer eines Subunternehmers (Fremdarbeiters) eingeben, der die Arbeitsplatzgruppe bereitstellt. Dieses Feld kann zum Verwalten von Arbeitsplatzgruppen verwendet werden, die unternehmensextern sind, in denen aber eine vertragsgebundene Verarbeitung erfolgt.  

Wenn Sie für Fremdarbeiten mit dem Kreditor einen anderen Satz für jeden Prozess vereinbart haben, können Sie das Kontrollkästchen **Spezieller Einstandspreis** aktivieren. Dadurch erhalten Sie die Möglichkeit, für jeden Arbeitsgang einen Betrag einzurichten und somit die Zeit zu sparen, die für die erneute Eingabe der einzelnen Einkaufsbestellungen erforderlich ist. Für die Verarbeitung werden nicht die Kosten in den Kostenfeldern der Arbeitsplatzgruppe, sondern der Einstandspreis im Arbeitsgang verwendet. Durch Aktivieren des Kontrollkästchens **Spezieller Einstandspreis** werden die Einstandspreise für den Kreditor pro Arbeitsplanvorgang berechnet.  

Wenn Sie für Fremdarbeiten einen einzelnen Satz pro Kreditor vereinbart haben, belassen Sie das Feld **Spezieller Einstandspreis** deaktiviert. Die Einstandspreise werden eingerichtet, indem die Felder **EK-Preis**, **Kosten %** und **Gemeinkostensatz** ausgefüllt werden.  

### <a name="routings-that-use-subcontract-work-centers"></a><a name="routings-that-use-subcontract-work-centers"></a><a name="routings-that-use-subcontract-work-centers"></a>Arbeitspläne, in denen Arbeitsplatzgruppen für Fremdarbeit verwendet werden
Arbeitsplatzgruppen für Fremdarbeit können für Arbeitsgänge in Arbeitsplänen in gleicher Weise verwendet werden wie normale Arbeitsplatzgruppen.  

Sie können einen Arbeitsplan erstellen, für den eine externe Arbeitsplatzgruppe als standardmäßiger Fertigungsschritt verwendet wird. Alternativ können Sie den Arbeitsplan für einen bestimmten Fertigungsauftrag so ändern, dass er einen externen Arbeitsgang enthält. Dies kann in einer Notsituation, z. B. wenn ein Server nicht ordnungsgemäß funktioniert, oder in einer Zeitspanne mit höherem Bedarf erforderlich sein, in der Arbeiten, die in der Regel innerbetrieblich ausgeführt werden, an einen Subunternehmer vergeben werden müssen.  

Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  

## <a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a><a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a><a name="calculate-subcontracting-worksheets-and-create-subcontract-purchase-orders"></a>Fremdarbeitenarbeitsblätter berechnen und Fremdarbeitsbestellung erstellen
Sobald Sie den Fremdarbeitenarbeitsblatt berechnet haben, wird der entsprechende Beleg (in diesem Fall eine Einkaufsbestellung) erstellt.  

Die Seiten **Fremdarbeitenarbeitsblatt** funktioniert wie die **Planungsarbeitsblatt** indem es den erforderlichen Vorrat berechnet, in diesem Fall Aufträge, die Sie im Arbeitsblatt überprüfen und dann mit der Funktion **Ereignismeldung durchführen** erstellen.  

> [!NOTE]  
>  Ein Fertigungsauftrag muss den Status **Freigegeben** haben, damit aus einem Fremdarbeitenarbeitsblatt auf ihn zugegriffen und er dort verwendet werden kann.  

### <a name="to-calculate-the-subcontracting-worksheet"></a><a name="to-calculate-the-subcontracting-worksheet"></a><a name="to-calculate-the-subcontracting-worksheet"></a>Fremdarbeitenarbeitsblatt berechnen
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fremdarbeitenvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2.  Damit das Arbeitsblatt berechnet wird, klicken Sie auf Aktionen **Fremdarbeit berechnen**.  
3.  Definieren Sie auf der Seite **Fremdarbeit berechnen** den Filter für an Subunternehmer vergebene Arbeitsgänge oder die Arbeitsplatzgruppen, in der sie ausgeführt werden, um nur die relevanten Fertigungsaufträge zu berechnen.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

    Sehen Sie sich die Zeilen auf der Seite **Fremdarbeitenarbeitsblatt** an. Die Informationen in diesem Arbeitsblatt stammen aus dem Fertigungsauftrag und den FA-Arbeitsgängen und werden in die Einkaufsbestellung übernommen, wenn dieser Beleg erstellt wird. Wie bei den anderen Arbeitsblättern auch können Sie eine Zeile aus dem Arbeitsblatt löschen, ohne dass sich dies auf die ursprünglichen Informationen auswirkt. Die Informationen werden wieder angezeigt, wenn Sie die Funktion **Fremdarbeit berechnen** das nächste Mal ausführen.  

### <a name="to-create-the-subcontract-purchase-order"></a><a name="to-create-the-subcontract-purchase-order"></a><a name="to-create-the-subcontract-purchase-order"></a>Einkaufsbestellung für Fremdarbeit generieren
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fremdarbeitenvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die **Ereignismeldung durchführen** Aktion aus.  
3.  Wählen Sie das Feld **Bestellungen/Aufträge drucken**, um die Einkaufsbestellung zu drucken, wenn diese erstellt wird.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

Wenn alle als Fremdarbeit zu vergebende Arbeitsgänge an denselben Kreditor gesendet werden müssen, dann wird nur eine Einkaufsbestellung erstellt.  

Die Arbeitsblattzeile, die in eine Einkaufsbestellung umgewandelt wurde, wird aus dem Arbeitsblatt gelöscht. Sobald eine Einkaufsbestellung erstellt wurde, erscheint sie nicht mehr im Arbeitsblatt.  

## <a name="posting-subcontract-purchase-orders"></a><a name="posting-subcontract-purchase-orders"></a><a name="posting-subcontract-purchase-orders"></a>Einkaufsbestellungen für Fremdarbeiten buchen
Sobald die Einkaufsbestellungen für Subunternehmer erstellt wurden, können sie gebucht werden. Nach Empfang der Bestellung wird ein Kapazitätsposten im Fertigungsauftrag gebucht, und bei der Fakturierung der Bestellung wird der EK-Preis der Einkaufsbestellung im Fertigungsauftrag gebucht.  

## <a name="to-post-a-subcontract-purchase-order"></a><a name="to-post-a-subcontract-purchase-order"></a><a name="to-post-a-subcontract-purchase-order"></a>So buchen Sie eine Fremdarbeitsbestellung
1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie eine Einkaufsbestellung, die über den Fremdarbeitenarbeitsblatt erstellt wurde.  

    In den Einkaufsbestellungszeilen werden dieselben Informationen angezeigt, die im Arbeitsblatt enthalten waren. Die **Fertigungsauftrag Auftragsnr.**, **Fertigungsauftrag Auftragszeilennr.**, **Arbeitsgangnr.** und **Arbeitsplatzgruppennr.** Felder werden mit den Informationen aus dem ursprünglichen Fertigungsauftrag ausgefüllt.  

3.  Wählen Sie die Aktion **Buchen** aus.  

Wenn der Einkauf als eingegangen gebucht wird, wird automatisch ein Istmeldungs-Buch.-Blattzeilenposten für den Produktionsauftrag gebucht. Dieses wird nur angewendet, wenn der Nebenvertragsarbeitsgang der letzte Arbeitsgang im FA-Arbeitsplan ist.  

> [!CAUTION]  
>  Automatisches Buchen von Ausgaben für einen aktuellen Fertigungsauftrag, wenn Fremdartikel eingehen, wird nicht erforderlich sein. Gründe für dieses könnten sein, dass die voraussichtlich fertig gestellte Menge, die gebucht wurde, sich von der tatsächlichen Menge unterscheidet und dass das Buchungsdatum der automatischen Istmeldung möglicherweise irreführend ist.  
>   
>  Damit nicht die erwartete Menge eines Fertigungsauftrags gebucht wird, wenn Fremdarbeitsbestellungen eingehen, vergewissern Sie sich, dass der vergebene Arbeitsgang nicht der letzte Arbeitsgang ist. Alternativ können Sie einen neuen letzten Arbeitsgang für die endgültig fertig gestellte Menge eingeben.  

Wenn die Einkaufsbestellung als fakturiert gebucht wird, wird der EK-Preis der Einkaufsbestellung auf die Produktion gebucht.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch
[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
