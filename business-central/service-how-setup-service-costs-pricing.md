---
title: Preisgestaltung und Kalkulationen für Dienste festlegen
description: 'Erfahren Sie, wie Sie Funktionen zur Preisgestaltung verwenden, um Ihre Anwendung so festzulegen und anzupassen, dass Sie Preise für Serviceartikel, Reparaturen und Aufträge anwenden und anpassen können.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/25/2021
ms.author: edupont
---

# Einrichten von Preisen und zusätzlichen Kosten für Services
Mithilfe der [!INCLUDE[prod_short](includes/prod_short.md)]-Preisfunktionen kann die Anwendung so eingerichtet und konfiguriert werden, dass Preise für Serviceartikel, Reparaturen und Aufträge übernommen und angepasst werden. Diese Preisentscheidungen werden anschließend problemlos an den Abrechnungsprozess übertragen.  
  
Entsprechend den Implementierungsanforderungen können Sie Preisgruppen festlegen und sie bestimmten Zeiträumen, Debitoren oder Währungen zuordnen. Sie können feste, minimale oder maximale Preise abhängig von den Serviceverträgen einrichten, die mit Debitoren abgeschlossen wurden. Zuletzt können Sie beim Anpassen der Preise die Änderungen anzeigen und genehmigen, bevor Sie sie an das Hauptbuch übertragen.  

## So richten Sie eine Servicepreisgruppe ein
Sie können Servicepreisgruppen einrichten, um Gruppen von Serviceartikeln zu bilden, die derselben Servicepreisgestaltung unterliegen. Sie verbinden die Servicepreisgruppen mit den Serviceartikeln in den Serviceartikelzeilen. Servicepreisgruppen können auch mit Serviceartikelgruppen verbunden werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicepreisgruppen** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Servicepreisgruppe.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Wählen Sie die Aktion **Einrichten** aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Die Felder **Anpassungstyp** und **Betrag** arbeiten zusammen, um zu definieren, ob diese Anpassung einen festen Betrag betrifft, oder ob sie nur gilt, wenn der gesamte Servicepreis den Betrag im Feld **Betrag** über- oder unterschreitet.  

## So richten Sie eine Servicepreiskorrekturgruppe ein  
Sie wählen für jede Art von Servicepreisgestaltung eine Servicepreiskorrekturgruppe. Beispielsweise können Sie Preiskorrekturgruppen einrichten, um die Preise für Fracht oder Ersatzteile anzupassen.  
  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Service-Preiskorrekturgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine neue Servicepreiskorrekturgruppe.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Geben Sie im Feld **Art** geben Sie die Art des Postens ein, den Sie anpassen möchten.  
  
    * Um nur einen bestimmten Posten zu korrigieren, geben Sie die Nummer des Postens in **Nr.** ein Feld Wenn Sie das Feld leer lassen, werden ALLE Posten der Art, die Sie im Feld **Art** festgelegt haben, korrigiert.  
    * Um die Servicepreise anzupassen, die nur für einen bestimmten Arbeitstyp passen, füllen Sie das Feld **Arbeitstyp** aus. Wenn Sie das Feld leer lassen, wird es ignoriert.  
  
5. Im Feld **Beschreibung** können Sie eine kurze Beschreibung der Servicepreiskorrektur hinterlegen.  
6. Um Servicepreise anzupassen, die sich nur auf eine bestimmte Produktbuchungsgruppe beziehen, füllen Sie das Feld **Gen. Prod. Buchungsgruppe** aus.

> [!Tip]
> Sie können **Details** auswählen, um zusätzliche Informationen für die Anpassungsgruppe hinzufügen. Beispielsweise können Sie festlegen, welcher Artikel zur Servicepreiskorrekturgruppe gehört, und ob es sich um einen Artikel, eine Ressource, eine Ressourcengruppe oder eine Servicegebühr handelt.  

## Einrichten zusätzlicher Kosten für Services
Wenn Sie mit Serviceartikeln und Serviceaufträgen arbeiten, können Sie zusätzliche Kosten, wie Reisekosten in bestimmten Servicegebieten oder die Grundgebühren erfassen. Wenn Sie einen Serviceauftrag erstellen, können Sie diese Kosten einfügen und eine Zeile mit dem Typ **Kosten** wird dem Auftrag hinzugefügt. Wenn Sie die Kosten in alle Serviceaufträge übernehmen möchten, können Sie Standardkosten einrichten. Wenn Sie beispielsweise immer eine Grundgebühr anwenden möchten.
  
### Um Servicekosten einzurichten
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Servicekosten** ein und wählen Sie dann den zugehörigen Link. 
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### Um Standardkosten für Serviceaufträge anzugeben
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Service Einrichtung** ein und wählen Sie dann den zugehörigen Link. 
2. Geben Sie im Feld **Serviceauftragsgrundgebühr** die entsprechenden Servicekosten aus.

## Siehe auch
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]