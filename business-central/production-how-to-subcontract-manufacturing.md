---
title: Fertigung in Fremdarbeit
description: 'Dieser Artikel bietet einen ausführlichen Überblick über die erweiterte Funktionalität der Lohnvergabe, einschließlich Arbeitsplatzfeldern und Arbeitsplänen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: '99000886,'
ms.date: 06/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Fertigung in Fremdarbeit

Ausgewählte Arbeitsgänge an Kreditoren weiter zu vergeben, ist in vielen Fertigungsunternehmen üblich. Fremdarbeit kann ein seltener Vorgang oder integraler Bestandteil aller Fertigungsschritte sein.

[!INCLUDE[prod_short](includes/prod_short.md)] gibt mehrere Werkzeuge für das Verwalten von Fremdarbeit:  

- Arbeitsplatzgruppen mit zugewiesenen Kreditoren: Mit dieser Funktion können Sie eine Arbeitsgruppe einrichten, die einem Kreditor (Subunternehmer) zugewiesen ist. Dieser Arbeitsplatz wird als Lohnarbeitsplatz bezeichnet. Sie können eine Arbeitsplatzgruppe für Fremdarbeit für einen Arbeitsplanvorgang angeben, wodurch Sie die als Fremdarbeit vergebene Aktivität problemlos verarbeiten können. Außerdem können Sie die Kosten des Vorgangs auf Arbeitsplan- oder Arbeitsplatzebene kennzeichnen.  
- Arbeitsplatzgruppenkosten auf Basis von Einheiten oder Zeit: Über diese Funktion können Sie angeben, ob Kosten, die der Arbeitsplatzgruppe zugewiesen sind, auf einer Fertigungszeit oder einem Pauschalbetrag pro Einheit basieren. Üblicherweise stellen Subunternehmer für ihre Leistungen einen Pauschalbetrag pro Einheit in Rechnung; die Anwendung kann aber mit den beiden Optionen (Fertigungszeit und Pauschalbetrag pro Einheit) umgehen.  
- Fremdarbeitenarbeitsblatt: Mit dieser Funktion können Sie nach den Fertigungsaufträgen mit Material suchen, die an einen Subunternehmer gesendet werden können, und können Sie automatisch aus Arbeitsplänen für Fertigungsaufträge Einkaufsbestellungen für Fremdarbeitsvorgänge erstellen. Die Anwendung bucht automatisch die Einkaufsbestellung zum Produktionsauftrag während die Einkaufsbestellung gebucht wird. Ein Fertigungsauftrag muss den Status "Freigegeben" haben, damit aus einem Fremdarbeitenvorschlag auf ihn zugegriffen und er in dem Vorschlag verwendet werden kann.  

## Lohnarbeitsplätze  

Arbeitsplatzgruppen für Fremdarbeiten werden auf gleiche Weise eingerichtet wie normale Arbeitsplatzgruppen, allerdings mit weiteren Informationen. Sie werden den Arbeitsplänen auf die gleiche Weise wie andere Arbeitsplätze zugewiesen.  

### Felder für das Lohnarbeitsplatzzentrum  

Das Feld **Kreditorennr.** kennzeichnet die Arbeitsplatzgruppe als Arbeitsplatzgruppe für Fremdarbeit. Sie können die Nummer eines Subunternehmers (Fremdarbeiters) eingeben, der die Arbeitsplatzgruppe bereitstellt. In diesem Feld können Arbeitsstellen verwaltet werden, die nicht im Unternehmen angesiedelt sind, sondern im Rahmen eines Vertrags Verarbeitungsvorgänge durchführen.  

Wenn Sie für Fremdarbeiten mit dem Kreditor einen anderen Satz für jeden Prozess vereinbart haben, können Sie das Kontrollkästchen **Spezieller Einstandspreis** aktivieren. Mit dieser Einstellung können Sie für jede Arbeitsgangzeile Kosten festlegen und müssen nicht jede Bestellung erneut eingeben. Für die Verarbeitung werden nicht die Kosten in den Kostenfeldern der Arbeitsplatzgruppe, sondern der Einstandspreis im Arbeitsgang verwendet. Durch Aktivieren des Kontrollkästchens **Spezieller Einstandspreis** werden die Einstandspreise für den Kreditor pro Arbeitsplanvorgang berechnet.  

Wenn Sie für Fremdarbeiten einen einzelnen Satz pro Kreditor vereinbart haben, belassen Sie das Feld **Spezieller Einstandspreis** deaktiviert. Die Kosten werden durch Ausfüllen der Felder  **Direkte Stückkosten**,  **Indirekte Kosten %** und  **Gemeinkostensatz**  eingerichtet.  

### Arbeitspläne, die Fremdarbeitsplätze nutzen

Arbeitsplatzgruppen für Fremdarbeit können für Arbeitsgänge in Arbeitsplänen in gleicher Weise verwendet werden wie normale Arbeitsplatzgruppen.  

Sie können einen Arbeitsplan erstellen, für den eine externe Arbeitsplatzgruppe als standardmäßiger Fertigungsschritt verwendet wird. Alternativ können Sie den Arbeitsplan für einen bestimmten Fertigungsauftrag so ändern, dass er einen externen Arbeitsgang enthält. Dies kann in einem Notfall erforderlich sein, beispielsweise wenn ein Server nicht ordnungsgemäß funktioniert, oder während einer vorübergehenden Phase höherer Nachfrage, in der Arbeiten, die Sie normalerweise intern erledigen, an einen Subunternehmer vergeben werden müssen.  

Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  

## Berechnen Sie Subunternehmerarbeitsblätter und erstellen Sie Subunternehmerbestellungen  

Nachdem Sie den Lohnarbeitsschein berechnet haben, wird das entsprechende Dokument erstellt. In diesem Fall eine Bestellung.  

Die Seiten **Fremdarbeitenarbeitsblatt** funktioniert wie die **Planungsarbeitsblatt** indem es den erforderlichen Vorrat berechnet, in diesem Fall Aufträge, die Sie im Arbeitsblatt überprüfen und dann mit der Funktion **Ereignismeldung durchführen** erstellen.  

> [!NOTE]  
> Ein Fertigungsauftrag muss den Status **Freigegeben** haben, damit aus einem Fremdarbeitenarbeitsblatt auf ihn zugegriffen und er dort verwendet werden kann.  

### Fremdarbeitenarbeitsblatt berechnen  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fremdarbeitenvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2. Damit das Arbeitsblatt berechnet wird, klicken Sie auf Aktionen **Fremdarbeit berechnen**.  
3. Legen Sie auf der Seite  **Subaufträge berechnen**  Filter für die an Subunternehmer vergebenen Vorgänge oder die Arbeitszentren fest, in denen sie ausgeführt werden, um nur die relevanten Produktionsaufträge zu berechnen.  
4. Wählen Sie die Schaltfläche **OK** aus.  

    Sehen Sie sich die Zeilen auf der Seite **Fremdarbeitenarbeitsblatt** an. Die Informationen in diesem Arbeitsblatt stammen aus dem Fertigungsauftrag und den FA-Arbeitsgängen und werden in die Einkaufsbestellung übernommen, wenn dieser Beleg erstellt wird. Wie bei den anderen Vorschlägen auch können Sie eine Zeile aus dem Vorschlag löschen, ohne dass sich dies auf die ursprünglichen Informationen auswirkt. Die Informationen werden wieder angezeigt, wenn Sie die Funktion **Fremdarbeit berechnen** das nächste Mal ausführen.  

### Einkaufsbestellung für Fremdarbeit generieren  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fremdarbeitenvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Ereignismeldung durchführen** Aktion aus.  
3. Wählen Sie das Feld **Bestellungen/Aufträge drucken**, um die Einkaufsbestellung zu drucken, wenn diese erstellt wird.  
4. Wählen Sie die Schaltfläche **OK** aus.  

Wenn alle als Fremdarbeit zu vergebende Arbeitsgänge an denselben Kreditor gesendet werden müssen, dann wird nur eine Einkaufsbestellung erstellt.  

Die Arbeitsblattzeile, die in eine Einkaufsbestellung umgewandelt wurde, wird aus dem Arbeitsblatt gelöscht. Nachdem eine Bestellung erstellt wurde, wird sie nicht mehr im Arbeitsblatt angezeigt.  

## Buchen von Subunternehmerbestellungen  

Nachdem die Subunternehmer-Bestellungen erstellt wurden, können sie gebucht werden. Nach Empfang der Bestellung wird ein Kapazitätsposten im Fertigungsauftrag gebucht, und bei der Fakturierung der Bestellung wird der EK-Preis der Einkaufsbestellung im Fertigungsauftrag gebucht.  

## So buchen Sie eine Fremdarbeitsbestellung
 
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie eine Einkaufsbestellung, die über den Fremdarbeitenarbeitsblatt erstellt wurde.  

    In den Einkaufsbestellungszeilen werden dieselben Informationen angezeigt, die im Arbeitsblatt enthalten waren. Die **Fertigungsauftrag Auftragsnr.**, **Fertigungsauftrag Auftragszeilennr.**, **Arbeitsgangnr.** und **Arbeitsplatzgruppennr.** Felder werden mit den Informationen aus dem ursprünglichen Fertigungsauftrag ausgefüllt.  

3. Wählen Sie die Aktion **Buchen**.  

Wenn der Einkauf als eingegangen gebucht wird, wird automatisch ein Ausgabejournaleintrag für den Produktionsauftrag gebucht, sofern es sich bei dem Fremdarbeitsvorgang um den letzten Vorgang im Arbeitsplan des Produktionsauftrags handelt.  

> [!CAUTION]  
> Automatisches Buchen von Ausgaben für einen aktuellen Fertigungsauftrag, wenn Fremdartikel eingehen, wird nicht erforderlich sein. Gründe für dieses könnten sein, dass die voraussichtlich fertig gestellte Menge, die gebucht wurde, sich von der tatsächlichen Menge unterscheidet und dass das Buchungsdatum der automatischen Istmeldung möglicherweise irreführend ist.  
>
> Damit nicht die erwartete Menge eines Fertigungsauftrags gebucht wird, wenn Fremdarbeitsbestellungen eingehen, vergewissern Sie sich, dass der vergebene Arbeitsgang nicht der letzte Arbeitsgang ist. Alternativ können Sie einen neuen letzten Arbeitsgang für die endgültig fertig gestellte Menge eingeben.  

Wenn die Einkaufsbestellung als fakturiert gebucht wird, wird der EK-Preis der Einkaufsbestellung auf die Produktion gebucht.  

> [!NOTE]  
> Soll-Kosten werden nur für Artikeltransaktionen verwaltet. Bei immateriellen Transaktionsarten, wie z. B. über Subunternehmer-Einkaufsaufträge gebuchte Kapazitäten, fallen keine erwarteten Kosten an. Lassen Sie sich nicht dadurch verwirren, dass das Veröffentlichen einer Quittung möglicherweise das Veröffentlichen einer Ausgabe Trigger bedeutet. Diese Transaktionen sind getrennt und die erwarteten Produktionskosten werden unabhängig voneinander berechnet.  

## Siehe auch  

[Fertigung](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
