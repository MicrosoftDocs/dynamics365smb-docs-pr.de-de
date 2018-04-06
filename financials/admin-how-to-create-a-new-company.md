---
title: 'So geht es: Ein neues Unternehmen erstellen | Microsoft Docs'
description: Um RapidStart Services zu verwenden , werden Tabellen und Seiten erstellt, aber sie enthalten keine Daten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c07b7c4e6b1c82004295a187184a6f3ccb4c7c7
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="create-a-new-company"></a>Erstellen eines neuen Mandanten.
Um RapidStart Servcies für [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verwenden, müssen Sie zunächst einen neuen Mandanten erstellen, für den Sie eine Kunden-Implementierung durchführen wollen. Bei der Erstellung eines neuen Mandanten werden die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Standardtabellen und -seiten erstellt, aber sie enthalten keine Daten.

Darüber hinaus können Sie bestimmte Einrichtungsdaten bei Ihrem Unternehmen anwenden, nachdem Sie es initialisiert haben. Die Informationen werden in einem Konfigurationspaket, eine .rapidstart-Datei bereitgestellt, die Inhalt in einem komprimierten Format bereitstellt.  

Beispielkonfigurationspakete, einschließlich landes-/regionspezifischer Dateien, sind im CRONUS Demounternehmen enthalten. Verwenden Sie die folgende Vorgehensweisen, um das Beispielkonfigurationspaket mit einem neuen Mandanten zu verwenden.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Beispielskonfigurationspaket BASICCONFIG verwenden  
1. Demounternehmen CRONUS International Ltd öffnen. Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).
2. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurationspaket** ein. Wählen Sie dann den zugehörigen Link aus.  
3. Wählen Sie das BASICCONFIG-Paket von der Liste aus, und wählen **Exportpaket**.  

Verwenden Sie das folgende Vorgehen, um einen neuen Mandanten zu erstellen, und verwenden Sie das BASICCONFIG-Paket als Teil des Prozesses.  

## <a name="to-create-a-new-company"></a>So erstellen Sie einen neuen Mandanten:  
1. Erstellen eines neuen Mandanten. Weitere Informationen finden Sie unter  [Neue Mandanten erstellen in[!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).
2. Vom RapidStart-Dienste-Implementierungs-Rollencenter können Sie das Konfigurationspaket jetzt importieren, das Sie aus CRONUS International Ltd.- exportierten.

Nachdem Sie ein neues Unternehmen erstellt haben, werden einige Tabellen automatisch ausgefüllt, auch wenn keine Unternehmensvorlage angewendet wird. Beispielsweise können Sie die Standardcodes für Buchungen und Stapeltransaktionen im Fenster **Quellencode** prüfen. Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] zur Verfügung stellen, sollten Sie diese Tabelle prüfen und auf sämtliche lokale sprachliche Aspekte achten.

## <a name="about-data-tables"></a>Info zu Datentabellen
[!INCLUDE[d365fin](includes/d365fin_md.md)]  Datentabellen liegen in zwei Haupttypen vor: Master und Einrichtung. Wenn Sie eine Mandantkonfiguration erstellen, können Sie diese Arten verwenden, um Ihre Konfigurationsstrategie zu konzentrieren.  

### <a name="master-data-tables"></a>Stammdatentabellen  
In der folgenden Tabelle sind einige Bespiele für -Stammdatentabellen aufgeführt. Wenn Sie einen neuen Mandanten initialisieren, sind diese Tabellen leer.  

|Tabellennr.|Tabellenname|  
|-------------------|--------------------|  
|15|Sachkonto|  
|18|Debitor|  
|23|Kreditor|  
|27|Option|  
|5050|Kontakt|  

### <a name="setup-data-tables"></a>Einrichtungsdatentabellen  
Die folgende Tabelle enthält Beispiele für Einrichtungsdatentabellen, in denen Sie Einrichtungsinformationen im Konfigurationsfragebogen erfassen. Diese Tabellen enthalten Basisinformationen, wenn der Mandant erstellt wird.  

|Tabellennr.|Tabellenname|  
|-------------------|--------------------|  
|98|Finanzbuchhaltungs-Einrichtung:|  
|311|Debitoren & Verkauf Einr.|  
|312|Kreditoren & Einkauf Einr.|  
|313|Lagereinrichtung|  

Zusätzlich zu den Einrichtungsdatentabellen hat [!INCLUDE[d365fin](includes/d365fin_md.md)] auch Datentabellen, die Kernangaben zu dem Unternehmen und seinen Geschäftsprozesse enthalten. In der folgenden Tabelle werden einige dieser Felder aufgeführt:  

|Tabellennr.|Tabellenname|  
|-------------------|--------------------|  
|3|Zahlungsbedingungen|  
|4|Währung|  
|6|Debitorenpreisgruppen|  
|5700|Lagerhaltungsdaten|

  

## <a name="see-also"></a>Siehe auch  
[Übernehmen von Konfiguration in neue Mandanten](admin-apply-configuration-to-new-companies.md)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)

