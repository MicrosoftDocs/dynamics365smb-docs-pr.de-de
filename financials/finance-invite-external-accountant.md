---
title: "Fügen Sie Ihren externen Buchhalter Ihrem Financials hinzu | Microsoft Docs"
description: "Erfahren Sie, wie Sie den externen Buchhalter zu Ihrem Dynamics 365 for Financials einladen können."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Externen Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten.

Sobald Ihr Buchhalter zu den verwendeten [!INCLUDE[d365fin](includes/d365fin_md.md)] Zugriff hat, können sie das Rollencenter **Buchhalter** verwenden, das Zugriff auf den relevantsten Fenstern für ihre Arbeit gibt.  

> [!NOTE]  
>  Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer Financials Experience](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Ihren Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] benötigt die Einladung des externen Buchhalters einem Administrator, der ihn Ihrem Active Directory-Tenant hinzuzufügen. Die Schritte dazu hängen von der Art des Kontos ab, das Sie verwendet haben, als Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmeldeten. Dieses Thema basiert auf Grundlage von Dimensionswertcodes von einem Office 365-Konto, welches Microsoft Azure Active Directory verwendet.  

> [!TIP]  
>  Es wird empfohlen, dass Sie Ihrem Partner [!INCLUDE[d365fin](includes/d365fin_md.md)] für Hilfe kontaktieren.  

Wenn Sie Ihr Abonnement von [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht mehr aktiviert haben die Evaluationsunternehmung nicht mehr verwenden, haben Sie einen Azure Active Directory Tenant. Der Administrator oder [!INCLUDE[d365fin](includes/d365fin_md.md)] Partner verwaltet diesen Tenant in [Azure Portal](https://portal.azure.com). Dieses ist, woher neue Benutzer hinzugefügt werden und Lizenzen angewendet und entfernt werden. Weitere Informationen finden Sie unter [Microsoft Azure-Portalübersicht](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

### <a name="separate-license"></a>Lizenzen trennen
Einer der Lizenztypen für [!INCLUDE[d365fin](includes/d365fin_md.md)] ist *Externer Buchhalter*. Dieser Lizenztyp ist für Benutzer wie externe Buchhalter gedacht. Das bedeutet, dass Sie einen zusätzlichen Arbeitsplatz in den aktuellen Active Directory nicht kaufen oder eine der vorhandenen Benutzerkonten auf [!INCLUDE[d365fin](includes/d365fin_md.md)] Ihrem externen Buchhalter verwenden müssen. Wenn beispielsweise Ihr aktuelles Office 365-Abonnement 10 Benutzer umfasst für [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sie 10 *Volle Benutzer*-Lizenzen verwenden, kann der Administrator den externen Buchhalter als Gastbenutzer in Azure hinzufügen und diesem Benutzer die *Externer Buchhalter*-Lizenz ohen zusätzliche Kosten zuweisen. Sie können jedoch einen Benutzer mit der *Externer Buchhalter*-Lizenz haben. Wenn Sie mehrere Benutzer hinzufügen möchten, müssen Sie das 365-Abonnement Office entsprechend aktualisieren.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Buchhalter Experiences in Dynamics 365 for Financials](finance-accounting.md)  
[Financials for Accounts in Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

