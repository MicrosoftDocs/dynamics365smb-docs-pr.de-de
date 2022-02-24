---
title: 'So geht es: Ein neues Unternehmen erstellen | Microsoft Docs'
description: Um RapidStart Services zu verwenden, werden Tabellen und Seiten erstellt, aber sie enthalten keine Daten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: c7042e783ec004cb2de637e6544c590bc8b9b81c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187196"
---
# <a name="create-a-new-company"></a>Erstellen eines neuen Mandanten.
Um RapidStart Services für [!INCLUDE[d365fin](includes/d365fin_md.md)] zu verwenden, müssen Sie zunächst einen neuen Mandanten erstellen, für den Sie eine Debitoren-Implementierung durchführen wollen. Bei der Erstellung eines neuen Mandanten werden die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Standardtabellen und -seiten erstellt, aber sie enthalten keine Daten.

Darüber hinaus können Sie bestimmte Einrichtungsdaten bei Ihrem Unternehmen anwenden, nachdem Sie es initialisiert haben. Die Informationen werden in einem Konfigurationspaket, eine .rapidstart-Datei bereitgestellt, die Inhalt in einem komprimierten Format bereitstellt.  

Beispielkonfigurationspakete, einschließlich landes-/regionspezifischer Dateien, sind im CRONUS-Demounternehmen enthalten. Verwenden Sie die folgende Vorgehensweisen, um das Beispielkonfigurationspaket mit einem neuen Mandanten zu verwenden.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Beispielskonfigurationspaket BASICCONFIG verwenden  
1. Öffnen Sie das Unternehmen „CRONUS International Ltd.“. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).
2. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Konfigurationspakete** ein, und wählen Sie dann den zugehörigen Link.  
3. Wählen Sie das BASICCONFIG-Paket von der Liste aus, und wählen **Exportpaket**.  

Verwenden Sie das folgende Vorgehen, um einen neuen Mandanten zu erstellen, und verwenden Sie das BASICCONFIG-Paket als Teil des Prozesses.  

## <a name="to-create-a-new-company"></a>So erstellen Sie einen neuen Mandanten:  
1. Erstellen eines neuen Mandanten. Weitere Informationen finden Sie unter [Neue Mandanten erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).
2. Vom RapidStart Services-Implementierungs-Rollencenter können Sie das Konfigurationspaket jetzt importieren, das Sie aus CRONUS International Ltd. exportierten.

Nachdem Sie ein neues Unternehmen erstellt haben, werden einige Tabellen automatisch ausgefüllt, auch wenn keine Unternehmensvorlage angewendet wird. Beispielsweise können Sie die Standardcodes für Buchungen und Stapeltransaktionen auf der Seite **Quellencode** prüfen. Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] zur Verfügung stellen, sollten Sie diese Tabelle prüfen und auf sämtliche lokale sprachliche Aspekte achten.

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
[Konfigurationen für neue Unternehmen übernehmen](admin-apply-configuration-to-new-companies.md)  
[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
