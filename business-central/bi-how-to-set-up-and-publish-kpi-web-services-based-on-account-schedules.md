---
title: "Vorgehensweise: Einrichten und Veröffentlichen von KPI-Webdienste auf der Basis von Kontenschemata  | Microsoft Docs"
description: Dieses Thema beschreibt, wie die KPI-Daten Kontenschema basierend auf bestimmte Kontenschemata angezeigt werden.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9e7adbe575df0b9253ead53ca2a5c782fa27e064
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>Einrichten und Veröffentlichen von KPI-Webdienste auf der Basis von Kontenschemata
Im Fenster **Kontopaln KPI Web-Service einrichten** richten Sie ein, wie die Kontenschema-KPI-Daten angezeigt werden, und auf welchen spezifischen Kontenschemata die KPIs basieren. Wenn Sie die Schaltfläche **Webdienst veröffentlichen** wählen, werden die angegebenen Kontenschema-KPI-Daten der Liste der veröffentlichten Webdienste im Fenster **Web-Dienste** hinzugefügt.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>So richten Sie einen KPI-Webdienst ein und veröffentlichen ihn, der auf Kontenschemata basiert  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan KPI Web Serivde einrichten** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie im Inforegister **Allgemein** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Anfang Geplante Werte**|Geben Sie an, zu welchem Zeitpunkt prognostizierte Werte in der Grafik des Kontenschema-KPIs angezeigt werden.<br /><br /> Die prognostizierten Werte werden aus dem Sachpostenbudget abgerufen, das Sie im Feld **Sachkostenbudgetname** auswählen. **Hinweis:**  Um KPIs zu erhalten, die die prognostizierten Zahlen nach einem bestimmten Datum und die tatsächlichen Zahlen vor dem Datum anzeigen, können Sie das Feld **Buchungen zulassen ab** im Fenster **Sachkonto einrichten** ändern. Weitere Informationen finden Sie unter Einrichten von Gruppenbuchungen|  
    |**Finanzbudgetname**|Geben Sie den Namen des Finanzbudgetpostens an, das prognostizierte Werte für den Webdienst des Kontenschema-KPIs bereitstellt.|  
    |**Periode**|Geben Sie die Periode an, auf dem der Kontenschema-KPI-Webservice basiert.|  
    |**Anzeigen nach**|Geben Sie an, in welchem Zeitintervall der Kontenschema KPI gezeigt wird.|  
    |**Webdienstname**|Geben Sie den Namen des Kontenschema-KPIs an.<br /><br /> Dieser Name wird im Feld **Servicename** im Fenster **Webservice** angezeigt.|  

    Fahren Sie fort, ein oder mehrere Kontenschemata anzugeben, die Sie als KPI-Webdienst gemäß der Einrichtung veröffentlichen möchten, die Sie in der vorhergegangenen Tabelle vorgenommen haben.  

3.  Füllen Sie im Inforegister **Kontenschemata** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Kontenschemaname**|Geben Sie das Kontenschema, auf dem der Kontenschema-KPI-Webservice basiert.|  
    |**Kontenschemabeschreibung**|Geben Sie die Beschreibung des Kontenschemas an, auf dem der KPI-Webservice basiert.|  

4.  Wiederholen Sie Schritt 3 für alle Kontenschemata, auf denen der Webdienst des Kontenschema-KPI basieren soll.  
5.  Um das ausgewählte Kontenschema einzusehen oder zu bearbeiten, wählen Sie auf dem Inforegister **Kontenschema** **Kontenschema bearbeiten**.  
6.  Um die Daten der Kontenschemas-KPIs anzuzeigen, die Sie eingerichtet haben, wählen Sie auf der Registerkarte Navigieren, in der Gruppe **Allgemein Kontoschema KPI Webservice**.  
7.  Veröffentlichen Sie den Kontenplan KPI Webdienst. Wählen Sie die Aktion **Webdient veröffentlichen**. Der Webdienst wird der Liste der veröffentlichten Webdienste im Fenster **Webservices** hinzugefügt.  

> [!NOTE]  
>  Sie können auch den KPI-Webdienst veröffentlichen, indem Sie im Feld **Webdienst-Setup für KPI-Kontenschema** aus dem Seitenobjekt **Webdienste** verweisen. Weitere Informationen finden Sie unter [Veröffentlichen eines Webservice](across-how-publish-web-service.md).  

## <a name="see-also"></a>Siehe auch  
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

