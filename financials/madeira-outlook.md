---
title: Dynamics 365 Business edition mit Outlook nutzen| Microsoft Docs
description: "Dynamics 365 Business edition hat eine starke Integration mit Office 365 und macht es möglich, dass Sie Ihre Geschäftsaktivitäten und E-Mails mit Debitoren und Kreditoren direkt in Outlook zu verwalten können."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: cfe0eed4090ef458e774da8d0bc03910247570d7
ms.openlocfilehash: 473c21085c54c7f97f34404eeb18683cf4479e41
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="using-dynamics-365-for-finance-and-operations-business-edition-as-your-business-inbox-in-outlook"></a>Dynamics 365 for Finance and Operations, Business edition als Ihr Unternehmensposteingang mit Outlook verwenden
[!INCLUDE[d365fin](includes/d365fin_md.md)] stellt die Möglichkeit vor, Geschäftsaktivitäten mit Ihren Debitoren und Kreditoren direkt in Microsoft Outlook zu verwalten. Mit dem [!INCLUDE[d365fin](includes/d365fin_md.md)] Outlook-Add-In können Sie die Finanzdaten sehen, die mit den Debitoren und Kreditoren verknüpft sind, sowie Finanzbelege wie beispielsweise Angebote und Rechnungen erstellen und versenden.  

## <a name="getting-the-add-in"></a>Das Add-in abrufen
Einer der Schritte der unterstützten Konfiguration für "Erste Schritte" in [!INCLUDE[d365fin](includes/d365fin_md.md)] ist das Fenster **Führen Sie Ihr Unternehmen in Office 365**. Wenn Sie in diesem Fenster die Schaltfläche **In Outlook einrichten** anklicken, müssen Sie Ihren Office 365 Benutzernamen und -Kennwort angeben. Die [!INCLUDE[d365fin](includes/d365fin_md.md)] Add-Ins werden dann automatisch Outlook hinzugefügt.  

Wenn Sie Outlook öffnen, sehen Sie eine E-Mail-Nachricht von Dynamics 365 Admin. Das neue Add-In wird dem Outlook-Menüband und Outlook Web Access hinzugefügt. Sie können es im Add-In-Menüband, unmittelbar über dem Text der E-Mail sehen. Das Add-In selbst wird regelmäßig aktualisiert, und Sie werden benachrichtigt, wenn eine neue Version in Outlook bereit ist.  

Einige Unternehmen, die Office 365 verwenden, grenzen die Berechtigungen der Benutzer ein, Add-Ins bereitzustellen. Daher müssen Sie sicherstellen, ob Sie ein Office 365-Abonnement haben, die E-Mail enthält und Ihnen ermöglicht, Add-Ins bereitzustellen. Wenn Sie das Add-In testen möchten, können Sie es in Ve [Office 365 kostenlos testen](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Nutzung des Contact Insights Add-In
Angenommen Sie erhalten eine E-Mail von einem Debitor, der für einige Artikel ein Angebot möchte. Sie können direkt in Outlook das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Add-In öffnen, das den Sender als Debitoren identifiziert und die Debitorenkarte für das Unternehmen öffnet. Auf diesem Dashboard können Sie Übersichtsinformationen zum Debitor sehen, sowie weitere Details zu bestimmten Belegen anzeigen. Sie können sich auch die Verkaufshistorie für den Debitor anzeigen lassen. Wenn es ein neuer Debitor ist, können Sie ihn als neuen Debitor in Outlook erstellen, [!INCLUDE[d365fin](includes/d365fin_md.md)] ohne Outlook zu verlassen.  

Im Add-In können Sie ein Verkaufsangebot erstellen und es diesem Kunden zusenden, ohne Outlook zu verlassen. Alle Informationen, die Sie zum Versenden des Verkaufsangebots benötigen, sind in Ihrem Geschäftseingang in Outlook verfügbar.  
Sobald Sie die Daten einmal eingeben haben, können Sie das Angebot buchen. Sie können es dann per E-Mail senden. [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt eine .PDF-Datei mit dem Verkaufsangebot und fügt sie der E-Mail-Nachricht hinzu, deren Entwurf Sie im Add-In erstellt haben.  

Möchten Sie eine E-Mail von einem Kreditor erhalten, können Sie das Add-In verwenden, um mit Kreditoren und Einkaufsrechnungen zu arbeiten.  

Manchmal möchten Sie mehr Felder sehen, als im Add-In angezeigt werden, z.B.wenn Sie Zeilen in einer Rechnung ausfüllen möchten. Um Ihnen mehr Platz zum Arbeiten zu geben, können Sie das Add-In in einem separaten Fenster aufklappen. Es ist immer noch ein Teil von Outlook, aber Sie haben mehr Platz. Wenn Sie Daten für das Dokument in der Popup-Ansicht eingeben, werden die Änderungen automatisch gespeichert. Wenn Sie mit dem Eingeben der Daten für den Beleg fertig sind, können Sie die Schaltfläche **OK** wählen. Wenn Sie den Add-In-Frame in Outlook auswählen, wird das Dokument automatisch mit den Änderungen aktualisiert, die Sie in der Popup-Ansicht vorgenommen haben.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Erstellen Sie Rechnungen von Ihren Besprechungsterminen
Einige Unternehmen erfassen alle verrechenbaren Termine im Outlook-Kalender. Mit [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die Rechnung für den Debitor direkt aus dem Kalenderelement heraus erstellen: Öffnen Sie den Termin und Sie können dann das Add-In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen, bestehende Informationen prüfen oder eine Verkaufsrechnung oder einen anderen Verkaufsbeleg dort erstellen.  

## <a name="doing-quick-document-lookup"></a>Schnelle Belegsuche
Das verknüpfte [!INCLUDE[d365fin](includes/d365fin_md.md)] Dokument-Add-In gibt Ihnen schnell Zugriff auf Belege, die in E-Mails angegeben wurden. Das Add-In ist für eine E-Mail verfügbar, wenn im Text der Nachricht eine Belegnummer erkannt wird. Das Öffnen des Add-Ins bietet schnellen Zugriff auf den Beleg.  

Wenn Sie beispielsweise eine E-Mail erhalten, die den Text *S-QUO100* beinhaltet, identifiziert [!INCLUDE[d365fin](includes/d365fin_md.md)] diesen als Verkaufsangebot und Sie können diesen Beleg in Outlook öffnen. Wählen Sie in Outlook unmittelbar über dem Text der E-Mail die Schaltfläche **Dokumentenverknüpfung** aus. Wählen Sie in der Outlook-Webanwendung *S-QUO1001* im Text der E-Mail aus.  

Im Dokumentenverknüpfungs-Add-In können Sie genauso Vorgänge für den Beleg ausführen und den Beleg ändern, wie im [!INCLUDE[d365fin](includes/d365fin_md.md)] .

## <a name="adding-the-add-ins-manually"></a>Das Add-In manuell hinzufügen
In einigen Fällen werden die Add-Ins nicht automatisch hinzugefügt zu Outlook. Selbst wenn Sie oder ein Kollege die unterstützte Einrichtung im Auftrag des Unternehmens ausführen, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] möglicherweise nicht in Outlook angezeigt. Wenn Sie dieses Problem haben, können Sie die Add-Ins in [!INCLUDE[d365fin](includes/d365fin_md.md)] manuell hinzufügen.  

Zuerst müssen Sie sicherstellen, dass Sie Zugriff auf die Add-Ins in Ihrem Office 365 Konto haben. Öffnen Sie einfach Ihren Outlook Web Access in einem Browser und fügen Sie dann `/owa/#path=/options/manageapps` der URL in der Adressleiste hinzu. Dadurch öffnet sich die Seite **Add-Ins verwalten**. Dort können Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] für Ihr Outlook aktivieren. Wenn Sie dann wieder zurück zu Outlook navigieren, sollte [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbar sein.  

Analog ist es im Outlook-Desktopclient. Sie können überprüfen, dass [!INCLUDE[d365fin](includes/d365fin_md.md)] im Fenster **Add-Ins verwalten** aufgeführt ist.  

In beiden Fällen müssen Sie, sollte [!INCLUDE[d365fin](includes/d365fin_md.md)] immer noch nicht verfügbar sein, die Add-in-Manifest-Datei abrufen. Für weitere Informationen wenden Sie bitte an Ihren Office 365 Administrator.

## <a name="see-also"></a>Siehe auch
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  

