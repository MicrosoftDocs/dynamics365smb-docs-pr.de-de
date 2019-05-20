---
title: Business Central-Buchhaltungsumgebung | Microsoft Docs
description: Erhalten Sie Informationen über das Buchhalterportal für Business Central. und das Buchhalterrollencenter, das interne und externe Buchhalter im Kundenunternehmen unterstützt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/02/2019
ms.author: edupont
ms.openlocfilehash: f088e1319684b9a18a2b0c8ab5305f73747f6889
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446922"
---
# <a name="accountant-experiences-in-included365finlongincludesd365finlongmdmd"></a>Buchhalter-Erfahrung in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Jedes Unternehmens muss seine Bücher führen und die Buchhaltung genehmigen. Einige Unternehmen verwenden einen externen Buchhalter, und andere haben einen Buchhalter als Mitarbeiter. Unabhängig von der Art des Buchhalters, den Sie sind, können sie das **Buchhalter**-Rollencenter als Startbildschirm in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden. Von hier können Sie auf alle Seiten zugreifen, die Sie in Ihrer Arbeit benötigen.  

## <a name="accountant-role-center"></a>Buchhalter-Rollencenter
Das Rollencenter bildet ein Dashboard mit Aktivitätskacheln, die Ihnen Echtzeitkennzahlen anzeigen und Ihnen Zugriff auf die Daten geben. Im oberen Seitenbereich im Menüband haben Sie Zugriff auf weitere Aktionen wie das Öffnen der häufig verwendeten Finanzberichte und Kontoauszüge in Excel. Im Navigationsbereich links können Sie schnell zwischen den Listen wechseln, die Sie häufig verwenden. Hier finden Sie weitere Bereiche, wie **Gebuchte Belege** mit den verschiedenen Belegarten, die der Mandant gebucht hat.  

Wenn Sie neu sind bei [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie eine Liste der Videos starten direkt von Ihrem Rollencenter aus. Sie können auch **Erste Schritte** starten, die die Schlüsselbereiche unterstreichen.  

## <a name="accountant-hub"></a>Accountant Hub
Wenn Sie ein Buchhalter mit mehreren Kunden sind, können Sie das [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] für einen besseren Überblick über Ihre Kundens verwenden. Von hier können Sie auf den Tenant jedes Clients zugreifen [!INCLUDE[d365fin](includes/d365fin_md.md)] und das Buchhalter-Rollencenter verwenden, wie oben beschrieben. Weitere Informationen finden Sie unter [Willkommen bei [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Externen Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten.

Sobald Ihr Buchhalter zu den verwendeten [!INCLUDE[d365fin](includes/d365fin_md.md)] Zugriff hat, können sie das Rollencenter **Buchhalter** verwenden, das Zugriff auf den relevantesten Seiten für ihre Arbeit gibt.  

In der neuesten Version von machen wir es Ihnen ganz einfach, Ihren externen Buchhalter einzuladen. Öffnen Sie einfach die Seite **Benutzer** und wählen Sie im Band die Aktion **Externen Buchhalter einladen**. Es wird eine E-Mail für Sie vorbereitet. Sie tragen einfach nur die E-Mail-Adresse Ihres Buchhalters ein und senden die Einladung ab.  

![Ihren Buchhalter einladen](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Dies setzt voraus, dass Sie SMPT-E-Mail eingerichtet haben. Dies können Sie selbst machen, oder Ihren [!INCLUDE[d365fin](includes/d365fin_md.md)]-Partner darum bitten. Zudem müssen als [!INCLUDE[d365fin](includes/d365fin_md.md)] Benutzeradministrator, nicht als der Geschäftsinhaber oder andere Benutzer angemeldet sind. Schließlich müssen Sie das Testunternehmen verlassen haben, sodass Sie einen Azure Active Directory-Administrator haben.  

> [!IMPORTANT]  
> Die E-Mail-Adresse des Buchhalters muss eine Arbeitsadresse sein, die auf Azure Active Directory basiert. Wenn der Buchhalter eine andere Art von E-Mail verwendet, kann die Einladung nicht gesendet werden.  

### <a name="separate-license"></a>Lizenzen trennen
Hinter den Kulissen wird der Buchhalter Ihrem Active Directory-Mandanten hinzugefügt. Ihr Administrator kann überprüfen, ob der Buchhalter die Einladung akzeptiert und der richtigen Lizenz hinzugefügt wird. Die Schritte dazu hängen von der Art des Kontos ab, das Sie verwendet haben, als Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmeldeten. Dieses Thema basiert auf Grundlage von Dimensionswertcodes von einem Office 365-Konto, welches Microsoft Azure Active Directory verwendet.  

Wenn Sie Ihr Abonnement von [!INCLUDE[d365fin](includes/d365fin_md.md)] nicht mehr aktiviert haben die Evaluationsunternehmung nicht mehr verwenden, haben Sie einen Azure Active Directory Tenant. Der Administrator oder [!INCLUDE[d365fin](includes/d365fin_md.md)] Partner verwaltet diesen Tenant in [Azure Portal](https://portal.azure.com). Dieses ist, woher neue Benutzer hinzugefügt werden und Lizenzen angewendet und entfernt werden. Weitere Informationen finden Sie unter [Microsoft Azure-Portalübersicht](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

Einer der Lizenztypen für [!INCLUDE[d365fin](includes/d365fin_md.md)] ist *Externer Buchhalter*. Dieser Lizenztyp ist für Benutzer wie externe Buchhalter gedacht. Das bedeutet, dass Sie einen zusätzlichen Arbeitsplatz in den aktuellen Active Directory nicht kaufen oder eine der vorhandenen Benutzerkonten auf [!INCLUDE[d365fin](includes/d365fin_md.md)] Ihrem externen Buchhalter verwenden müssen. Wenn beispielsweise Ihr aktuelles Office 365 Abonnement 10 Benutzer umfasst für [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sie 10 *Volle Benutzer*-Lizenzen verwenden, kann der Administrator den externen Buchhalter als Gastbenutzer in Azure hinzufügen und diesem Benutzer die *Externer Buchhalter*-Lizenz ohen zusätzliche Kosten zuweisen. Sie können jedoch einen Benutzer mit der *Externer Buchhalter*-Lizenz haben. Wenn Sie mehrere Benutzer hinzufügen möchten, müssen Sie das Office 365 Abonnement entsprechend aktualisieren.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Analysieren von Finanzauswertungen in Excel](finance-analyze-excel.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Einrichten der Cashflowanalyse](finance-setup-cash-flow-analyses.md)  
[Willkommen bei [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 – Accountant Hub auf Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
