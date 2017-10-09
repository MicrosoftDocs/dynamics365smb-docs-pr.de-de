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
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b7efbb724f322d371e9e1b725612cb4eb0b3ceb2
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Externen Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten.

Sobald Ihr Buchhalter zu den verwendeten [!INCLUDE[d365fin](includes/d365fin_md.md)] Zugriff hat, können sie das Rollencenter **Buchhalter** verwenden, das Zugriff auf den relevantsten Fenstern für ihre Arbeit gibt.  

> [!NOTE]  
>  Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer Financials Experience](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Ihren Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
In der neuesten Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] machen wir es Ihnen ganz einfach, Ihren externen Buchhalter einzuladen. Öffnen Sie einfach das Fenster **Benutzer** und wählen Sie im Band die Aktion **Externen Buchhalter einladen**. Es wird eine E-Mail für Sie vorbereitet. Sie tragen einfach nur die E-Mail-Adresse Ihres Buchhalters ein und senden die Einladung ab.  

![Ihren Buchhalter einladen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Dies setzt voraus, dass Sie SMPT-E-Mail eingerichtet haben. Dies können Sie selbst machen, oder Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)]-Partner darum bitten. Zudem müssen als [!INCLUDE[d365fin](includes/d365fin_md.md)] Benutzeradministrator, nicht als der Geschäftsinhaber oder andere Benutzer angemeldet sind.  

### <a name="separate-license"></a>Lizenzen trennen
Hinter den Kulissen wird der Buchhalter Ihrem Active Directory-Mandanten hinzugefügt. Ihr Administrator kann überprüfen, ob der Buchhalter die Einladung akzeptiert und der richtigen Lizenz hinzugefügt wird. Die Schritte dazu hängen von der Art des Kontos ab, das Sie verwendet haben, als Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmeldeten. Dieses Thema basiert auf Grundlage von Dimensionswertcodes von einem Office 365-Konto, welches Microsoft Azure Active Directory verwendet.  

Wenn Sie Ihr Abonnement von [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht mehr aktiviert haben die Evaluationsunternehmung nicht mehr verwenden, haben Sie einen Azure Active Directory Tenant. Der Administrator oder [!INCLUDE[d365fin](includes/d365fin_md.md)] Partner verwaltet diesen Tenant in [Azure Portal](https://portal.azure.com). Dieses ist, woher neue Benutzer hinzugefügt werden und Lizenzen angewendet und entfernt werden. Weitere Informationen finden Sie unter [Microsoft Azure-Portalübersicht](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Einer der Lizenztypen für [!INCLUDE[d365fin](includes/d365fin_md.md)] ist *Externer Buchhalter*. Dieser Lizenztyp ist für Benutzer wie externe Buchhalter gedacht. Das bedeutet, dass Sie einen zusätzlichen Arbeitsplatz in den aktuellen Active Directory nicht kaufen oder eine der vorhandenen Benutzerkonten auf [!INCLUDE[d365fin](includes/d365fin_md.md)] Ihrem externen Buchhalter verwenden müssen. Wenn beispielsweise Ihr aktuelles Office 365 Abonnement 10 Benutzer umfasst für [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sie 10 *Volle Benutzer*-Lizenzen verwenden, kann der Administrator den externen Buchhalter als Gastbenutzer in Azure hinzufügen und diesem Benutzer die *Externer Buchhalter*-Lizenz ohen zusätzliche Kosten zuweisen. Sie können jedoch einen Benutzer mit der *Externer Buchhalter*-Lizenz haben. Wenn Sie mehrere Benutzer hinzufügen möchten, müssen Sie das Office 365 Abonnement entsprechend aktualisieren.  

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Vorgehensweise: Richten Sie E-Mail Nachricht manuell oder mit der unterstützten Einrichtung ein](madeira-how-setup-email.md)  
[Buchhalter Experiences in Dynamics 365 for Financials](finance-accounting.md)  
[Financials for Accounts in Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

