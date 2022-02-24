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
ms.date: 06/01/2020
ms.author: edupont
ms.openlocfilehash: 1aaf04237261481f21d10d5e7966666132ff1a8e
ms.sourcegitcommit: c5fcc204a1ba8aaf153ce3ad5d150295b144c0e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413643"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Buchhalter-Erfahrung in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Jedes Unternehmens muss seine Bücher führen und die Buchhaltung genehmigen. Einige Unternehmen verwenden einen externen Buchhalter, und andere haben einen Buchhalter als Mitarbeiter. Unabhängig von der Art des Buchhalters, den Sie sind, können sie das **Buchhalter**-Rollencenter als Startbildschirm in [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden. Von hier können Sie auf alle Seiten zugreifen, die Sie in Ihrer Arbeit benötigen.  

## <a name="accountant-role-center"></a>Buchhalter-Rollencenter
Das Rollencenter bildet ein Dashboard mit Aktivitätskacheln, die Ihnen Echtzeitkennzahlen anzeigen und Ihnen Zugriff auf die Daten geben. Im oberen Seitenbereich im Menüband haben Sie Zugriff auf weitere Aktionen wie das Öffnen der häufig verwendeten Finanzberichte und Kontoauszüge in Excel. Im Navigationsbereich links können Sie schnell zwischen den Listen wechseln, die Sie häufig verwenden. Hier finden Sie weitere Bereiche, wie **Gebuchte Belege** mit den verschiedenen Belegarten, die der Mandant gebucht hat.  

Wenn Sie neu sind bei [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie eine Liste der Videos starten direkt von Ihrem Rollencenter aus. Sie können auch **Erste Schritte** starten, die die Schlüsselbereiche unterstreichen.  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Ihren externen Buchhalter einladen zu Ihrem [!INCLUDE[d365fin](includes/d365fin_md.md)]
Wenn Sie einen externen Buchhalter verwenden, um Ihre Bücher und Finanzberichterstattung zu verwalten, kann Ihr Administrator sie für Ihr [!INCLUDE[d365fin](includes/d365fin_md.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten. [!INCLUDE[d365fin](includes/d365fin_md.md)] enthält drei Lizenzen des Typs „Externer Buchhalter“. Weitere Informationen über Lizenzierung finden Sie unter [Microsoft Dynamics 365 Business Central Lizenzleitfaden](https://go.microsoft.com/fwlink/?LinkId=871590).

Sobald Ihr Buchhalter zu den verwendeten [!INCLUDE[d365fin](includes/d365fin_md.md)] Zugriff hat, können sie das Rollencenter **Buchhalter** verwenden, das Zugriff auf den relevantesten Seiten für ihre Arbeit gibt.  

In der neuesten Version von machen wir es Ihnen ganz einfach, Ihren externen Buchhalter einzuladen. Öffnen Sie einfach die Seite **Benutzer** und wählen Sie im Band die Aktion **Externen Buchhalter einladen**. Es wird eine E-Mail für Sie vorbereitet. Sie tragen einfach nur die E-Mail-Adresse Ihres Buchhalters ein und senden die Einladung ab.  

> [!Note]  
> Dies setzt voraus, dass Sie SMPT-E-Mail eingerichtet haben. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).   

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Die E-Mail-Adresse des Buchhalters muss eine Arbeitsadresse sein, die auf Azure Active Directory basiert. Wenn der Buchhalter eine andere Art von E-Mail verwendet, kann die Einladung nicht gesendet werden. 
> 
> Für diese Aufgabe ist der Zugriff auf die Verwaltung von Benutzern und Lizenzen in Azure Active Directory erforderlich. Dem Benutzer, der diese Einladung versendet, muss die Rolle **Globaler Administrator** oder **Benutzeradministrator** im Microsoft 365 Admin Center zugewiesen sein. Weitere Informationen finden Sie unter [Informationen zu Administratorrollen](/microsoft-365/admin/add-users/about-admin-roles) im Microsoft 365-Administratorinhalt.  

### <a name="adding-your-accountant-to-your-office-365-via-azure-portal"></a>Hinzufügen Ihres Buchhalters zu Ihrem Office 365 über das Azure-Portal

Wenn Ihr Administrator oder Wiederverkäufer die Anleitung **Externen Buchhalter einladen** nicht verwenden möchte, können sie im Azure-Portal einen externen Benutzer hinzufügen und diesem Benutzer die Lizenz für externe Buchhalter zuweisen. Weitere Informationen finden Sie unter [Schnellstart: Ihrem Verzeichnis im Azure-Portal Gastbenutzer hinzufügen](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>So fügen Sie Ihren Buchhalter als Gastbenutzer hinzu

1. Öffne Sie das [Azure-Portal](https://portal.azure.com/).
2. Wählen Sie im linken Bereich **Azure Active Directory**.
3. Unter **Verwalten** wählen Sie **Benutzer**.
4. Wählen Sie **Neuer Gastbenutzer**.
5. Wählen Sie auf der Seite **Neuer Benutzer** die Option **Benutzer einladen** aus und fügen Sie Ihrem externen Buchhalter dann Informationen hinzu.  

   Schließen Sie optional eine persönliche Begrüßungsnachricht an den Buchhalter ein, um ihn darüber zu informieren, dass Sie ihn Ihrem [!INCLUDE [prodshort](includes/prodshort.md)] hinzufügen.

6. Wählen Sie **Einladen**, um die Einladung automatisch zu versenden. Oben rechts wird eine Benachrichtigung mit der Meldung **Erfolgreich eingeladener Benutzer** angezeigt. 
7. Nachdem Sie die Einladung gesendet haben, wird das Benutzerkonto automatisch als Gast zum Verzeichnis hinzugefügt.

Als Nächstes müssen Sie dem neuen Gastbenutzer eine Lizenz für [!INCLUDE [prodshort](includes/prodshort.md)] zuweisen.

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>So geben Sie Ihrem Buchhalter Zugriff auf Ihre [!INCLUDE [prodshort](includes/prodshort.md)]

1. Wählen Sie im Azure-Portal für den neu hinzugefügten Benutzer **Profil** und dann Sie **Bearbeiten** aus
2. Aktualisieren Sie die Feld **Verbrauchsort** auf das entsprechende Land, und wählen Sie dann **Speichern** aus.
3. Wählen Sie **Lizenzen** und öffnen Sie dann **Zuordnungen**.
4. Wählen Sie die Lizenz **Externer Dynamics 365 Business Central-Buchhalter**.  

    Wenn diese Lizenz nicht verfügbar ist, müssen Sie stattdessen eine verfügbare **Dynamics 365 Business Central für IWs**-Lizenz verwenden.
5. Speichern Sie die Zuordnung.

Bei Erfolg wird dem Gastbenutzer die Lizenz zugewiesen und das Gastkonto wird erstellt.

### <a name="importing-the-new-user-into-prodshort"></a>Importieren des neuen Benutzers in [!INCLUDE [prodshort](includes/prodshort.md)]

Der Buchhalter erhält eine E-Mail, in der er darüber informiert wird, dass er Zugriff auf Ihr Active Directory erhalten hat. Als Nächstes müssen Sie ihnen Zugriff auf das richtige Unternehmen in [!INCLUDE [prodshort](includes/prodshort.md)] gewähren.

#### <a name="to-add-the-accountant-to-the-right-company"></a>Hinzufügen des Buchhalters zum richtigen Unternehmen

1. Öffnen Sie das [!INCLUDE [prodshort](includes/prodshort.md)]-Unternehmen, auf die Sie dem Buchhalter Zugriff gewähren möchten unter [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.  
3. Wählen Sie die Aktion **Neue Benutzer von Office 365 abrufen** aus.

Dadurch wird das Benutzerkonto, das Sie im Azure-Portal erstellt haben, in das Unternehmen importiert. Weitere Informationen finden Sie unter [Hinzufügen eines Benutzers in Business Central](ui-how-users-permissions.md#adduser).  

Wenn Sie mehreren Unternehmen Zugriff gewähren möchten, müssen Sie sich bei jedem Unternehmen anmelden und diesen Vorgang wiederholen. Alternativ können Sie die Berechtigungsgruppen für das Benutzerprofil des Buchhalters in [!INCLUDE [prodshort](includes/prodshort.md)] aktualisieren, wie das Zuweisen der *D365 Bus Premium*-Benutzergruppe. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

<!--## Accountant Hub

If you are an accountant with several clients, you can use [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] for a better overview of your clients. From there, you can access each client's tenant in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the Accountant Role Center as described above. For more information see [Welcome to [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] is currently in public preview in a limited number of markets.-->

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Finanzauswertungen in Excel analysieren](finance-analyze-excel.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Einrichten der Cashflowanalyse](finance-setup-cash-flow-analyses.md)  
