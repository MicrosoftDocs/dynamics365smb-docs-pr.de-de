---
title: Invoicing und Business Central verwenden | Microsoft Docs
description: Problemumgehung zum Aufrufen von Microsoft Invoicing, wenn Sie sich auf Dynamics 365 Business Central
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 917887deae163a76b233e1635344e537806f6215
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Mithilfe des gleichen Office 365 Kontos in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] und Microsoft Invoicing
Wenn Sie sich für eine Testversion anmelden [!INCLUDE[d365fin](includes/d365fin_md.md)], können das Programm 30-Tage lang testen, Sie können ein Abonnement abschließen oder Sie können die Verwendung von [!INCLUDE[d365fin](includes/d365fin_md.md)] beenden. In allen Fällen sehen Sie bei der Anmeldung in das Office-Portal eine Kachel **Geschäftszentrum** und klicken darauf. Dieses ist ein Teil des Office 365 Business Premium Abonnements, deshalb sieht nicht jeder die Kachel im Office-Portal.  

Wenn Sie auf das Geschäftszentrum zugreifen, sehen Sie ein Abschnitt, der **Fakturierung** genannt wird. Wenn Sie auf diesen Abschnitt zugreifen, sehen Sie eine Meldung, dass Sie nicht auf Microsoft Invoicing zugreifen können, da Ihr Konto verwendet wird in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Sie sehen eine ähnliche Meldung, wenn Sie die mobile App für die Fakturierung einrichten.  

## <a name="workaround"></a>Problemumgehung
Invoicing und [!INCLUDE[d365fin](includes/d365fin_md.md)] haben eine freigegebene Plattform. Das bedeutet, dass Sie als bestehender Benutzer von [!INCLUDE[d365fin](includes/d365fin_md.md)] erkannt werden, wenn Sie auf Rechnungsstellung im Geschäftszentrum klicken. Der Grund ist, dass das Invoicing nicht das gleiche Unternehmen als [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden kann.  

Daher müssen Sie sich bei [!INCLUDE[d365fin](includes/d365fin_md.md)] anmelden und Ihr bestehendes Unternehmen umbenennen und dann ein neues Unternehmen erstellen, dass Sie dann in Invoicing verwenden können. Keine Daten werden bei dieser Problemumgehung überschrieben oder verschoben.

### <a name="to-rename-your-company"></a>Ihr Unternehmen umbenennen
1.  Anmelden bei [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Unternehmen** ein, und wählen dann den zugehörigen Link aus.  
3.  Im Fenster **Unternehmen** wählen Sie die Schaltfläche **Liste bearbeiten** aus.  
4.  Ändern den Namen des Postens *Mein Unternehmen* in etwas anderes.  

    Warten Sie mehrere Minuten. Wir machen einige Änderungen in der zugrunde liegenden Datenbank und das kann eine Weile dauern.
5.  Wenn die Anwendung wieder bereit steht, wählen Sie die Schaltfläche **Neues Unternehmen erstellen** aus.  
6.  Im Dialogfeld, das erscheint, geben Sie den Namen als *Mein Unternehmen* an, und wählen Sie die Option **Suiten-Produktion – nur Einrichtungsdaten** aus.  

Dies kann wieder mehrere Minuten dauern. Wenn der Vorgang abgeschlossen ist, sind Sie in der Lage, auf Invoicing als Teil IhrerOffice 365 Business Premium Erfahrung zuzugreifen.  

### <a name="what-about-my-data"></a>Informationen zu Ihren Daten.
Wenn Sie die Vorlage Meine Mandanten umbenennen auswählen, werden die Datenbanktabellen, die Ihre bestehenden [!INCLUDE[d365fin](includes/d365fin_md.md)] Daten speichern, umbenennte, aber die Daten selber werden nicht berührt  

Wenn Sie "Invoicing" und [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, werden die Daten in zwei verschiedenen Containern gespeichert (die zwei Unternehmen). Nichts wird freigegebent, daher müssen Sie Debitoren und Artikel in beiden Unternehmen verwalten.  

## <a name="see-also"></a>Siehe auch
[Häufig gestellte Fragen](across-faq.md)  
[Verwaltung](admin-setup-and-administration.md)  

