---
title: 'Gewusst wie: Ressourcen zuweisen einrichten | Microsoft Docs'
description: 'Erfahren Sie, wie das System helfen kann, sicherzustellen, die Sie einer Person zuweisen, welches die Qualifikationen benötigen können, um eine Service bereitstellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="set-up-resource-allocation"></a><a name="set-up-resource-allocation"></a><a name="set-up-resource-allocation"></a>Um Ressourcenzuweisung einzurichten:
Um sicherzustellen dass eine Serviceaufgabe gut ausgeführt wird, ist es wichtig, eine Ressource zu finden die qualifiziert ist, die Arbeit zu tun. Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, sodass es einfach is, Person zuzuordnen, die die rechten Qualifikationen für das Projekt haben. In [!INCLUDE[prod_short](includes/prod_short.md)] zeigen wir die _Ressourcenzuordnung_. Sie können Ressourcen anhand ihrer Qualifikation, Verfügbarkiet oder ob sie sich in demselben Servicegebiet befindet wie der Debitor zuordnen. 

Um die Ressourcenzuordnungen zu aktivieren, müssen Sie einrichten:  
  
* Die Qualifikationen, die erforderlich sind, um Serviceartikel zu reparieren und zu verwalten. Produktbuchungsgruppen werden Artikeln und Ressourcen zugewiesen.  
* Die geografischen Regionen, die Zonen, die Sie für Ihren Markt definieren. Zum Beispiel Ost, West, Mitte usw. Diese werden Debitoren und Ressourcen zugewiesen.  
* Ob Qualifikationen oder Zonen anzeigt werde und ob eine Warnung angezeigt wird, wenn jemand eine unqualifizierte Ressource ausgewählt hat oder eine Ressource, die sich nicht in der Nähe des Debitors befindet.  

## <a name="to-set-up-skills"></a><a name="to-set-up-skills"></a><a name="to-set-up-skills"></a>So richten Sie Qualifikationen ein:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Fertigkeiten** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><a name="to-assign-skills-to-service-items-and-resources"></a><a name="to-assign-skills-to-service-items-and-resources"></a>Produktbuchungsgruppen werden Artikeln und Ressourcen zugewiesen.
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Serviceartikel** oder **Ressourcen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte für den Serviceartikel oder die Ressource, und wählen Sie anschließend eine der folgenden Optionen aus:  
  
    * Für Serviceartikel wählen Sie **Ressourcenqualifikationen** aus.  
    * Für Ressourcen wählen Sie **Qualifikationen** aus.  

## <a name="to-set-up-zones"></a><a name="to-set-up-zones"></a><a name="to-set-up-zones"></a>Um Servicegebiete einzurichten:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Zonen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><a name="to-assign-zones-to-customers-and-resources"></a><a name="to-assign-zones-to-customers-and-resources"></a>Um Ressourcen und Debitoren Servicegebieten zuzuordnen:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitor** oder **Ressourcen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Karte für den Serviceartikel oder die Ressource, und wählen Sie anschließend eine der folgenden Optionen aus:  
  
    * Für Debitoren wählen Sie eine Zone in dem Feld **Servicegebietscode** aus.  
    * Für Ressourcen wählen Sie die **Servicegebiete** Aktion aus.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Um anzugeben, was dargestellt werden soll, wenn eine Ressource ausgewählt wird
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Service Einrichtung** ein, und wählen Sie dann den entsprechenden Link. 
2. Wählen Sie im Feld **Ressourcenqualifikationsoption** eine der Optionen aus, die in der folgenden Tabelle beschrieben werden.  
  
    |**Option**|**Beschreibung**|  
    |------------|-------------|  
    |Code anzeigen | Zeigt nur den Code an.|  
    |Warnung anzeigen | Zeigt die Daten an und zeigt eine Warnmeldung an, wenn Sie eine Ressource auswählen, die nicht qualifiziert ist.|  
    |Keine Verwendung | Zeigt nicht diese Information an.|  

## <a name="to-update-resource-capacity"></a><a name="to-update-resource-capacity"></a><a name="to-update-resource-capacity"></a>Um die Ressourcenkapazität zu erweitern
Sie können die Kapazität von Ressourcen ändern.  
  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcenkapazität** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Ressource und wählen Sie die Aktion **Ressourcen zuweisen** aus.  
3. Nehmen Sie die Änderungen vor, und wählen Sie dann **Kapazität aktualisieren** aus.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Um Qualifikationen für Artikel, Serviceartikel oder Serviceartikelgruppen zu aktualisieren
Wenn Sie die Qualifikationscodes ändern möchten, die Artikeln zugeordnet sind, beispielsweise **PC** auf **PCS**, können Sie dies entweder für den Artikel, für alle Artikel oder Serviceartikel in einer Serviceartikelgruppe tun.  
  
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Elemente** oder **Serviceartikel** oder **Serviceartikel-Gruppe** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die Entität, die Sie aktualisieren möchten und wählen Sie die **Ressourcenqualifikationen** Aktion aus.  
3. Wählen Sie in der Zeile mit dem zu ändernden Qualifikationscode im Feld **Qualifikationscode** den relevanten Qualifikationscode aus.  
4.  Wenn der Artikel über zugeordnete Serviceartikel verfügt, wird ein Dialogfeld mit den folgenden zwei Optionen geöffnet:  
  
    * Ändern Sie die Qualifikationen in den ausgewählten Wert: Wählen Sie diese Option aus, wenn Sie bei allen verknüpften Serviceartikeln den alten Qualifikationscode durch den neuen ersetzen möchten.  
    * Löschen Sie die Qualifikationen, oder aktualisieren Sie ihre Beziehung zueinander: Wählen Sie diese Option aus, wenn Sie den Qualifikationscode nur für diesen Artikel ändern möchten. Der Qualifikationscode für die verknüpften Serviceartikel wird neu zugeordnet, d. h., das Feld **Zugewiesen von** wird aktualisiert.  
  
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch
[Ressourcen zuordnen](service-how-to-allocate-resources.md)  
[Einrichten von Arbeits- und Servicezeiten](service-how-setup-work-service-hours.md)  
[Fehlerberichte einrichten](service-how-setup-fault-reporting.md)  
[Einrichten von Codes für Standardservices](service-how-setup-service-coding.md)  
 



[!INCLUDE[footer-include](includes/footer-banner.md)]
