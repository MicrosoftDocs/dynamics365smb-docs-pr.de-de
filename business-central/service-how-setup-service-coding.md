---
title: Codes für Standard-Services festlegen
description: 'Erfahren Sie, wie Sie Codes für regelmäßig ausgeführte Service-Aktivitäten mit einer vordefinierten Zeile festlegen können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'service, service item, service order, repairs, maintenance'
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="set-up-standard-service-codes"></a>Standardservicecodes einrichten

Bei der Durchführung eines normalen Service müssen häufig Servicebelege erstellt werden, die Servicezeilen mit ähnlichen Informationen enthalten. Um dies Zeilen einfach zu erstellen, können Sie Standardservicecodes einrichten, die einen vordefinierten Satz Servicezeilen haben. Wenn Sie den Code in einem Verkaufsbeleg auswählen, werden die Zeilen automatisch eingegeben. Sie können eine beliebige Anzahl von Standardservicecodes einrichten und jeder Code kann eine unbegrenzte Anzahl von Servicezeilen verschiedener Arten aufweisen, z. B. Artikel, Ressourcen, Kosten oder damit verknüpfte Standardtexte. Die Servicezeilen jedes Standardservicecodes werden auf der Karte **Standardservicecode** erstellt. Sie können dann die Standardservicecodes Servicecodeartikelgruppen zuweisen im Fenster **Standardservicecodes Serviceartikelgruppen**. Wenn Sie später einen Servicebeleg erstellen, können Sie die **Standardservicecodes abrufen** Aktion verwenden, um Servicezeilen hinzuzufügen.  
  
> [!Tip]
> Sie können das gleive Vorgehen verwenden, um Zeilen in Verkaufs- und Einkaufsbelegen zu erstellen. Weitere Informationen finden Sie unter [Erstellen Sie wiederkehrende Verkaufs- und Einkaufszeilen](sales-how-work-standard-lines.md).  
  
## <a name="to-set-up-a-standard-service-code"></a>So richten Sie einen Standardservicecode ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Standard Servicecodes** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>So weisen Sie einer Serviceartikelgruppe einen Standardservicecode zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Service-Elementgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie die Servicezeilen aus, die mit diesem Servicecode verknüpft sind.  

## <a name="see-also"></a>Siehe auch

[Service](service-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
