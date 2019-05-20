---
title: Invoicing und Business Central verwenden | Microsoft Docs
description: Problemumgehung für den Zugriff auf Microsoft Invoicing, wenn Sie sich für Dynamics 365 Business Central registriert haben.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0173d64e140cfea91bf7f08d821c2d30cf0eb7b3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241484"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Mithilfe des gleichen Office 365 Kontos in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] und Microsoft Invoicing
Wenn Sie sich für eine Testversion anmelden [!INCLUDE[d365fin](includes/d365fin_md.md)], können das Programm 30-Tage lang testen, Sie können ein Abonnement abschließen oder Sie können die Verwendung von [!INCLUDE[d365fin](includes/d365fin_md.md)] beenden. In allen Fällen sehen Sie bei der Anmeldung in das Office-Portal eine Kachel **Microsoft Invoicing** und klicken darauf. Dieses ist ein Teil des Office 365 Business Premium Abonnements, deshalb sieht nicht jeder die Kachel im Office-Portal.  

Wenn Sie auf Microsoft Invoicing zugreifen, sehen Sie eine Meldung, dass Sie nicht auf Microsoft Invoicing zugreifen können, da Ihr Konto verwendet wird in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Sie sehen eine ähnliche Meldung, wenn Sie die mobile App für die Fakturierung einrichten.  

## <a name="workaround"></a>Problemumgehung
Invoicing und [!INCLUDE[d365fin](includes/d365fin_md.md)] haben eine freigegebene Plattform. Das bedeutet, dass Sie als bestehender Benutzer von [!INCLUDE[d365fin](includes/d365fin_md.md)] erkannt werden, wenn Sie auf Rechnungsstellung im Office-Portal klicken. Der Grund ist, dass das Invoicing nicht das gleiche Unternehmen als [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden kann.  

Daher müssen Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden und Ihr bestehendes Unternehmen umbenennen und dann ein neues Unternehmen erstellen, dass Sie dann in Invoicing verwenden können. Keine Daten werden bei dieser Problemumgehung überschrieben oder verschoben.

### <a name="to-rename-your-company"></a>Ihr Unternehmen umbenennen
1. Melden Sie sich an bei [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. In der oberen rechter Ecke wählen Sie das Symbol **Einstellungen** aus ![Einstellungen](media/ui-experience/settings_icon_small.png "Einstellungssymbol Rollencenter") und dann **Meine Einstellungen**.
3. Wählen Sie im Feld **Unternehmen** ein anderes Unternehmen aus.
4. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unternehmen** ein, und wählen dann den zugehörigen Link aus.  
5. Auf der Seite **Unternehmen** wählen Sie **Liste bearbeiten** aus.  
6. Ändern den Namen des Postens *Mein Unternehmen* in etwas anderes.  

    Warten Sie mehrere Minuten. Wir machen einige Änderungen in der zugrunde liegenden Datenbank und das kann eine Weile dauern.
7.  Wenn die Anwendung wieder bereit steht, wählen Sie die Schaltfläche **Neues Unternehmen erstellen** aus.  
8.  Im Dialogfeld, das erscheint, geben Sie den Namen als *Mein Unternehmen* an, und wählen Sie die Option **Suiten-Produktion – nur Einrichtungsdaten** aus.  

Dies kann wieder mehrere Minuten dauern. Wenn der Vorgang abgeschlossen ist, sind Sie in der Lage, auf Invoicing als Teil Ihrer Office 365 Business Premium Erfahrung zuzugreifen.  

### <a name="what-about-my-data"></a>Informationen zu Ihren Daten.
Wenn Sie die Vorlage Meine Mandanten umbenennen auswählen, werden die Datenbanktabellen, die Ihre bestehenden [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten speichern, umbenennte, aber die Daten selber werden nicht berührt  

Wenn Sie "Invoicing" und [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden die Daten in zwei verschiedenen Containern gespeichert (die zwei Unternehmen). Nichts wird freigegebent, daher müssen Sie Debitoren und Artikel in beiden Unternehmen verwalten.  

## <a name="see-also"></a>Siehe auch
[Häufig gestellte Fragen](across-faq.md)  
[Verwaltung](admin-setup-and-administration.md)  
