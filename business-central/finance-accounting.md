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
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896133"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Buchhalter-Erfahrung in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Jedes Unternehmens muss seine Bücher führen und die Buchhaltung genehmigen. Einige Unternehmen verwenden einen externen Buchhalter, und andere haben einen Buchhalter als Mitarbeiter. Unabhängig von der Art des Buchhalters, den Sie sind, können sie das **Buchhalter**-Rollencenter als Startbildschirm in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden. Von hier können Sie auf alle Seiten zugreifen, die Sie in Ihrer Arbeit benötigen.  

## <a name="accountant-role-center"></a>Buchhalter-Rollencenter
Das Rollencenter bildet ein Dashboard mit Aktivitätskacheln, die Ihnen Echtzeitkennzahlen anzeigen und Ihnen Zugriff auf die Daten geben. Im oberen Seitenbereich im Menüband haben Sie Zugriff auf weitere Aktionen wie das Öffnen der häufig verwendeten Finanzberichte und Kontoauszüge in Excel. Im Navigationsbereich links können Sie schnell zwischen den Listen wechseln, die Sie häufig verwenden. Hier finden Sie weitere Bereiche, wie **Gebuchte Belege** mit den verschiedenen Belegarten, die der Mandant gebucht hat.  

Wenn Sie neu sind bei [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie eine Liste der Videos starten direkt von Ihrem Rollencenter aus. Sie können auch **Erste Schritte** starten, die die Schlüsselbereiche unterstreichen.  

## <a name="inviteaccountant"></a>Ihren externen Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten.

Sobald Ihr Buchhalter zu den verwendeten [!INCLUDE[d365fin](includes/d365fin_md.md)] Zugriff hat, können sie das Rollencenter **Buchhalter** verwenden, das Zugriff auf den relevantesten Seiten für ihre Arbeit gibt.  

In der neuesten Version von machen wir es Ihnen ganz einfach, Ihren externen Buchhalter einzuladen. Öffnen Sie einfach die Seite **Benutzer** und wählen Sie im Band die Aktion **Externen Buchhalter einladen**. Es wird eine E-Mail für Sie vorbereitet. Sie tragen einfach nur die E-Mail-Adresse Ihres Buchhalters ein und senden die Einladung ab.  
> [!Note]  
> Dies setzt voraus, dass Sie SMPT-E-Mail eingerichtet haben. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).   

![Ihren Buchhalter einladen](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> Die E-Mail-Adresse des Buchhalters muss eine Arbeitsadresse sein, die auf Azure Active Directory basiert. Wenn der Buchhalter eine andere Art von E-Mail verwendet, kann die Einladung nicht gesendet werden.  

### <a name="behind-the-scenes"></a>Hinter den Kulissen
[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält drei Lizenzen des Typs „Externer Buchhalter“. Wenn Ihr Unternehmen einen externen Buchhalter verwendet, können Sie Zugriff auf Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] gewähren, indem Sie ihm/ihr eine solche Lizenz zuweisen. Weitere Informationen zur Lizenzierung finden Sie unter [Microsoft Dynamics 365 Busincess Central-Lizenzierungsleitfaden](https://go.microsoft.com/fwlink/?LinkId=871590). 

Wenn für Ihr Abonnement noch eine Lizenz verfügbar ist, kann Ihr Administrator oder Weiterverkaufspartner externe Benutzer über Azure-Portal hinzufügen und diesem Benutzer die „Externer Buchhalter“-Lizenz zuweisen. Weitere Informationen finden Sie unter [Hinzufügen von Azure Active Directory B2B-Zusammenarbeitsbenutzer im Azure-Portal](/azure/active-directory/b2b/add-users-administrator).

Anschließend können Sie den Buchhalter von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus einladen, indem Sie die Anleitung für unterstützte Einrichtung **Externen Buchhalter einladen** verwenden. Da für diese Aufgabe jedoch der Zugriff auf die Verwaltung von Benutzern und Lizenzen in Azure Active Directory erforderlich ist, muss dem Benutzer, der diese Einladung versendet, die Rolle **Globaler Administrator** oder **Benutzeradministrator** im Office 365 Admin Center zugewiesen sein. Weitere Informationen finden Sie unter [Informationen zu Administratorrollen](/office365/admin/add-users/about-admin-roles) im Office 365-Administratorinhalt. 

## <a name="accountant-hub"></a>Accountant Hub
Wenn Sie ein Buchhalter mit mehreren Kunden sind, können Sie das [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] für einen besseren Überblick über Ihre Kundens verwenden. Von hier können Sie auf den Tenant jedes Clients zugreifen [!INCLUDE[d365fin](includes/d365fin_md.md)] und das Buchhalter-Rollencenter verwenden, wie oben beschrieben. Weitere Informationen finden Sie unter [Willkommen bei [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] ist derzeit in einer begrenzten Anzahl von Märkten in der öffentlichen Vorschau verfügbar.

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
[Dynamics 365 – Accountant Hub auf Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
