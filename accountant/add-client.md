---
title: Kunden in die Dynamics 365-Buchhaltererfahrung holen | Microsoft Docs
description: Erfahren Sie, wie Sie vorhandenen Kunden dem Accountant Hub für Dynamics 365 hinzufügen.
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 95a4153c56693d8bdd28980f1acff14b917a9488
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300067"
---
# <a name="add-clients-to-your-dashboard-in-include-d365acc_longincludesd365acc_long_mdmd"></a>Fügen Sie Clients Ihren Dashboard in [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)] Kunden hinzu
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Sie können einen Client hinzufügen, indem Sie die Seite **Clients** verwenden, das Sie öffnen können, indem Sie die **Clients verwalten** Aktion im Menüband auswählen. Wählen Sie **Neu** aus, und füllen Sie die relevanten Felder aus.  

> [!div class="mx-imgBorder"]
> ![Einen Kunden hinzufügen](./media/accountant-add-client/manage-client.png)

Die Daten in der Karte für jeden Client werden von Ihnen angegeben, und Sie können diese bei Bedarf ändern. Jedoch ist das **Client URL** Feld wichtig - Damit können Sie auf jeden Client zugreifen [!INCLUDE [d365fin](includes/d365fin_md.md)]. Verwenden Sie die **Client prüfen URL** Aktion im Menüband, um zu prüfen, ob Sie den entsprechenden Link eingegeben haben. Die URL, die Sie eingeben müssen zeigt zur [!INCLUDE [d365fin](includes/d365fin_md.md)] des Clients und enthält deren Domänenadresse. Wenn Sie beispielsweise bestimmte Domänen wie MyBusiness.com haben, dann ist der Link zur [!INCLUDE [d365fin](includes/d365fin_md.md)] *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Vor der Aktualisierung im Mai 2018 hatte die URL, die Sie festgelegt haben, ein anderes Format mit dem Firmennamen des Clients zu Beginn. Mit der Aktualisierung von [!INCLUDE [d365fin](includes/d365fin_md.md)] ist das Format ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, wo ```clientdomain``` die Domäne Ihres Clients dargestellt wird.  

Die Client URL wird verwendet, wenn Sie das Menüelement **Zum Unternehmen gehen** im Dashboard [!INCLUDE [d365acc](includes/d365acc_md.md)] wählen.  

### <a name="get-invited-to-a-clients-include-d365fin_longincludesd365fin_long_mdmd"></a>Laden Sie sich bei einem Client [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] ein
Ein Unternehmen, mit [!INCLUDE [d365fin](includes/d365fin_md.md)] dem Sie in als ihre [!INCLUDE [d365fin](includes/d365fin_md.md)] externen Buchhalter einladen kann. Um eingeladen zu werden, müssen Sie diesen die E-Mail geben, die Sie verwenden mit [!INCLUDE [d365acc](includes/d365acc_md.md)] wie zum Beispiel <em>me@accountant.com</em>. Der Administrator Ihres Clients kann Sie dann dem System hinzufügen, indem Sie den Assistenten **Externen Buchhalter einladen** ausführen.  

Deshalb erhalten Sie von Ihrem Kunden E-Mails mit Links zu ihrem [!INCLUDE [d365fin](includes/d365fin_md.md)] Der erste Link ist eine Einladung, um Zugriff zu deren Unternehmen zu erhalten. Öffnen Sie den Link und nehmen Sie die Schritte an, die Sie dem [!INCLUDE [d365fin](includes/d365fin_md.md)] Ihres Kunden hinzufügen. Der zweite Link dient dazu, diesen Kunden Ihrem Dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] hinzufügen, wie oben beschrieben.  

Wenn Sie die Einladung akzeptiert haben, werden Sie angemeldet und können auf die Finanzdaten des Kunden aus dem Rollencenter **Buchhalter** heraus zugreifen. Weitere Informationen finden Sie unter [Buchhalter-Erfahrung in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Siehe auch
[Erste Schritte mit [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Problembehebung bei [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  
