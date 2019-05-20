---
title: 'Gewusst wie: Ressourcen zuweisen einrichten | Microsoft Docs'
description: Erfahren Sie, wie das System helfen kann, sicherzustellen, die Sie einer Person zuweisen, welches die Qualifikationen benötigen können, um eine Service bereitstellen.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 7b7a01bc61d55379cd12563d1f31f331c3b4fd74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251952"
---
# <a name="set-up-resource-allocation"></a>Um Ressourcenzuweisung einzurichten:
Um sicherzustellen dass eine Serviceaufgabe gut ausgeführt wird, ist es wichtig, eine Ressource zu finden die qualifiziert ist, die Arbeit zu tun. Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] einrichten, sodass es einfach is, Person zuzuordnen, die die rechten Qualifikationen für das Projekt haben. In [!INCLUDE[d365fin](includes/d365fin_md.md)] zeigen wir die _Ressourcenzuordnung_. Sie können Ressourcen anhand ihrer Qualifikation, Verfügbarkiet oder ob sie sich in demselben Servicegebiet befindet wie der Debitor zuordnen. 

Um die Ressourcenzuordnungen zu aktivieren, müssen Sie einrichten:  
  
* Die Qualifikationen, die erforderlich sind, um Serviceartikel zu reparieren und zu verwalten. Produktbuchungsgruppen werden Artikeln und Ressourcen zugewiesen.  
* Die geografischen Regionen, die Zonen, die Sie für Ihren Markt definieren. Zum Beispiel Ost, West, Mitte usw. Diese werden Debitoren und Ressourcen zugewiesen.  
* Ob Qualifikationen oder Zonen anzeigt werde und ob eine Warnung angezeigt wird, wenn jemand eine unqualifizierte Ressource ausgewählt hat oder eine Ressource, die sich nicht in der Nähe des Debitors befindet.  

## <a name="to-set-up-skills"></a>So richten Sie Qualifikationen ein:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fähigkeiten** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Produktbuchungsgruppen werden Artikeln und Ressourcen zugewiesen.
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird. Geben Sie **Serivce-Artikel** oder **Ressource** ein und wählen Sie den zugehörigen Link aus.  
2. Öffnen Sie die Karte für den Serviceartikel oder die Ressource, und wählen Sie anschließend eine der folgenden Optionen aus:  
  
    * Für Serviceartikel wählen Sie **Ressourcenqualifikationen** aus.  
    * Für Ressourcen wählen Sie **Qualifikationen** aus.  

## <a name="to-set-up-zones"></a>Um Servicegebiete einzurichten:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zonen** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Um Ressourcen und Debitoren Servicegebieten zuzuordnen: 
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") geöffnet wird. Geben Sie **Debitor** oder **Ressource** ein und wählen Sie den zugehörigen Link aus.  
2. Öffnen Sie die Karte für den Serviceartikel oder die Ressource, und wählen Sie anschließend eine der folgenden Optionen aus:  
  
    * Für Debitoren wählen Sie eine Zone in dem Feld **Servicegebietscode** aus.  
    * Für Ressourcen wählen Sie die **Servicegebiete** Aktion aus.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Um anzugeben, was dargestellt werden soll, wenn eine Ressource ausgewählt wird
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Service einrichten** ein, und wählen dann den zugehörigen Link aus. 
2. Wählen Sie im Feld **Ressourcenqualifikationsoption** eine der Optionen aus, die in der folgenden Tabelle beschrieben werden.  
  
    |**Option**|**Beschreibung**|  
    |------------|-------------|  
    |Code anzeigen | Zeigt nur den Code an.|  
    |Warnung anzeigen | Zeigt die Daten an und zeigt eine Warnmeldung an, wenn Sie eine Ressource auswählen, die nicht qualifiziert ist.|  
    |Keine Verwendung | Zeigt nicht diese Information an.|  

## <a name="to-update-resource-capacity"></a>Um die Ressourcenkapazität zu erweitern  
Sie können die Kapazität von Ressourcen ändern.  
  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Ressourcen-Kapazität** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Ressource und wählen Sie die Aktion **Ressourcen zuweisen** aus.  
3. Nehmen Sie die Änderungen vor, und wählen Sie dann **Kapazität aktualisieren** aus.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Um Qualifikationen für Artikel, Serviceartikel oder Serviceartikelgruppen zu aktualisieren
Wenn Sie die Qualifikationscodes ändern möchten, die Artikeln zugeordnet sind, beispielsweise **PC** auf **PCS**, können Sie dies entweder für den Artikel, für alle Artikel oder Serviceartikel in einer Serviceartikelgruppe tun.  
  
1. Wählen Sie das Symbol![ Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben **Artikel** oder **Service-Artikel** ein oder **Service-Artikel-Gruppe** und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie die Entität, die Sie aktualisieren möchten und wählen Sie die **Ressourcenqualifikationen** Aktion aus.  
3. Wählen Sie in der Zeile mit dem zu ändernden Qualifikationscode im Feld **Qualifikationscode** den relevanten Qualifikationscode aus.  
4.  Wenn der Artikel über zugeordnete Serviceartikel verfügt, wird ein Dialogfeld mit den folgenden zwei Optionen geöffnet:  
  
    * Ändern Sie die Qualifikationen in den ausgewählten Wert: Wählen Sie diese Option aus, wenn Sie bei allen verknüpften Serviceartikeln den alten Qualifikationscode durch den neuen ersetzen möchten.  
    * Löschen Sie die Qualifikationen, oder aktualisieren Sie ihre Beziehung zueinander: Wählen Sie diese Option aus, wenn Sie den Qualifikationscode nur für diesen Artikel ändern möchten. Der Qualifikationscode für die verknüpften Serviceartikel wird neu zugeordnet, d. h., das Feld **Zugewiesen von** wird aktualisiert.  
  
## <a name="see-also"></a>Siehe auch
[Ressourcen zuordnen](service-how-to-allocate-resources.md)  
[Einrichten von Arbeits- und Servicezeiten](service-how-setup-work-service-hours.md)  
[Fehlerberichte einrichten](service-how-setup-fault-reporting.md)  
[Einrichten von Codes für Standardservices](service-how-setup-service-coding.md)  
 

