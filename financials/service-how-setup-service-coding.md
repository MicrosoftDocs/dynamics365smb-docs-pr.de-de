---
title: "Vorgehensweise: Einrichten von Codes für Standardservices | Microsoft Docs"
description: "Erfahren Sie, wie Codes für Dienstaktivitäten eingerichtet werden, die Sie häufig ausführen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8a31e312fc12d75d4eb75a191b2b82bf9a6ff3c5
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-standard-service-codes"></a>Vorgehensweise: Einrichten von Standardservicecodes
Bei der Durchführung eines normalen Service müssen häufig Servicebelege erstellt werden, die Servicezeilen mit ähnlichen Informationen enthalten. Um dies Zeilen einfach zu erstellen, können Sie Standardservicecodes einrichten, die einen vordefinierten Satz Servicezeilen haben. Wenn Sie den Code in einem Verkaufsbeleg auswählen, werden die Zeilen automatisch eingegeben. Mit jedem Servicecode kann eine unbegrenzte Anzahl Servicezeilen verschiedener Arten, Artikel, Ressourcen, Kosten oder Standardtexten verknüpft sein. Für jeden Standardservicecode können Servicezeilen im Fenster **Standard-Servicecodkarte** erstellt werden. Sie können dann die Standardservicecodes Servicecodeartikelgruppen zuweisen im Fenster **Standardservicecodes Serviceartikelgruppen**. Wenn Sie später einen Servicebeleg erstellen, können Sie die **Standardservicecodes abrufen** Aktion verwenden, um Servicezeilen hinzuzufügen.  
  
> [!Tip]
>  Sie können das gleive Vorgehen verwenden, um Zeilen in Verkaufs- und Einkaufsbelegen zu erstellen. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).    
  
## <a name="to-set-up-a-standard-service-code"></a>So richten Sie einen Standardservicecode ein    
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Standardservicecode** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>So weisen Sie einer Serviceartikelgruppe einen Standardservicecode zu
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Serviceartikelgruppen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.  

## <a name="see-also"></a>Siehe auch
[Service](service-service.md)
