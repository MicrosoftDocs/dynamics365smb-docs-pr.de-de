---
title: Nutzung von Business Central with Outlook| Microsoft Docs
description: Dieser Service hat eine starke Integration mit Office 365 und macht es möglich, dass Sie Ihre Geschäftsaktivitäten und E-Mails mit Debitoren und Kreditoren direkt in Outlook verwalten können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 08/14/2019
ms.author: edupont
ms.openlocfilehash: 70299f86a1ebc3251780eb05f8b68afeff23fa5e
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887691"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Nutzen Sie Business Central als Ihr Unternehmenspostfach in Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] stellt die Möglichkeit vor, Geschäftsaktivitäten mit Ihren Debitoren und Kreditoren direkt in Microsoft Outlook zu verwalten. Mit dem [!INCLUDE[d365fin](includes/d365fin_md.md)] Outlook-Add-In können Sie die Finanzdaten sehen, die mit den Debitoren und Kreditoren verknüpft sind, sowie Finanzbelege wie beispielsweise Angebote und Rechnungen erstellen und versenden.  

## <a name="getting-the-add-in"></a>Das Add-in abrufen
Die ersten Schritte sind einfach mit dem [!INCLUDE[d365fin](includes/d365fin_md.md)] Add-In für Outlook. Mit dem unterstützten Setup Richten Sie Ihren **Geschäfts-Eingang in Outlook** ein können Sie die Verbindung für sich oder für Ihre Organisation einrichten, wenn Ihre Organisation Office 365 verwendet. Geben Sie einfach Ihren Office 365 Benutzername und Passwort ein, wenn Sie dazu aufgefordert werden, und teilen Sie uns mit, ob Sie eine Beispiel-E-Mail-Nachricht erhalten möchten. Die [!INCLUDE[d365fin](includes/d365fin_md.md)] Add-Ins werden dann automatisch Outlook hinzugefügt. Weitere Informationen finden Sie unter [Mindestanforderungen für Outlook ](product-requirements.md#outlook).  

Wenn Sie Outlook öffnen, sehen Sie eine E-Mail-Nachricht vom *Dynamics 365 Business Central Admin*. Das neue Add-In wird dem Outlook-Menüband und Outlook Web Access hinzugefügt. Sie können die [!INCLUDE[prodshort](includes/prodshort.md)]-Add-Ins unmittelbar über oder unter dem Text der E-Mail sehen. Das Add-In selbst wird regelmäßig aktualisiert, und Sie werden benachrichtigt, wenn eine neue Version in Outlook bereit ist.  

> [!TIP]
> Wenn Sie das neue Outlook in einem Browser verwenden, können die [!INCLUDE [prodshort](includes/prodshort.md)] Add-Ins unter **Mehr Aktionen** ausgeblendet werden.

Einige Unternehmen, die Office 365 verwenden, grenzen die Berechtigungen der Benutzer ein, Add-Ins bereitzustellen. Daher müssen Sie sicherstellen, ob Sie ein Office 365-Abonnement haben, die E-Mail enthält und Ihnen ermöglicht, Add-Ins bereitzustellen. Wenn Sie das Add-In testen möchten, können Sie es in [Office 365 kostenlos testen](https://products.office.com/try).  

## <a name="using-the-contact-insights-add-in"></a>Nutzung des Contact Insights Add-In
Angenommen Sie erhalten eine E-Mail von einem Debitor, der für einige Artikel ein Angebot möchte. Sie können direkt in Outlook das [!INCLUDE[d365fin](includes/d365fin_md.md)]-Add-In öffnen, das den Sender als Debitoren identifiziert und die Debitorenkarte für das Unternehmen öffnet. Auf diesem Dashboard können Sie Übersichtsinformationen zum Debitor sehen, sowie weitere Details zu bestimmten Belegen anzeigen. Sie können sich auch die Verkaufshistorie für den Debitor anzeigen lassen. Wenn es ein neuer Kontakt ist, können Sie ihn als neuen Debitor in Outlook erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] ohne Outlook zu verlassen.  

Im Add-In können Sie ein Verkaufsangebot erstellen und es diesem Debitoren zusenden, ohne Outlook zu verlassen. Alle Informationen, die Sie zum Versenden des Verkaufsangebots benötigen, sind in Ihrem Geschäftseingang in Outlook verfügbar.  
Sobald Sie die Daten einmal eingeben haben, können Sie das Angebot buchen. Sie können es dann per E-Mail senden. [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt eine .PDF-Datei mit dem Verkaufsangebot und fügt sie der E-Mail-Nachricht hinzu, deren Entwurf Sie im Add-In erstellt haben.  

Möchten Sie eine E-Mail von einem Kreditor erhalten, können Sie das Add-In verwenden, um mit Kreditoren und Einkaufsrechnungen zu arbeiten.  

Manchmal möchten Sie mehr Felder sehen, als im Add-In angezeigt werden, z.B.wenn Sie Zeilen in einer Rechnung ausfüllen möchten. Um Ihnen mehr Platz zum Arbeiten zu geben, können Sie das Add-In in einer separaten Seite aufklappen. Es ist immer noch ein Teil von Outlook, aber Sie haben mehr Platz. Wenn Sie Daten für das Dokument in der Popup-Ansicht eingeben, werden die Änderungen automatisch gespeichert. Wenn Sie mit dem Eingeben der Daten für den Beleg fertig sind, können Sie die Schaltfläche **OK** wählen. Wenn Sie den Add-In-Frame in Outlook auswählen, wird das Dokument automatisch mit den Änderungen aktualisiert, die Sie in der Popup-Ansicht vorgenommen haben.  

## <a name="creating-invoices-from-your-meeting-appointments"></a>Erstellen Sie Rechnungen von Ihren Besprechungsterminen
Einige Unternehmen erfassen alle verrechenbaren Termine im Outlook-Kalender. Mit [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie die Rechnung für den Debitor direkt aus dem Kalenderelement heraus erstellen: Öffnen Sie den Termin und Sie können dann das Add-In [!INCLUDE[d365fin](includes/d365fin_md.md)] öffnen, bestehende Informationen prüfen oder eine Verkaufsrechnung oder einen anderen Verkaufsbeleg dort erstellen.  

## <a name="doing-quick-document-lookup"></a>Schnelle Belegsuche
Das verknüpfte [!INCLUDE[d365fin](includes/d365fin_md.md)] Dokument-Add-In gibt Ihnen schnell Zugriff auf Belege, die in E-Mails angegeben wurden. Das Add-In ist für eine E-Mail verfügbar, wenn im Text der Nachricht eine Belegnummer erkannt wird. Das Öffnen des Add-Ins bietet schnellen Zugriff auf den Beleg.  

Wenn Sie beispielsweise eine E-Mail erhalten, die den Text *S-QUO100* beinhaltet, identifiziert [!INCLUDE[d365fin](includes/d365fin_md.md)] diesen als Verkaufsangebot und Sie können diesen Beleg in Outlook öffnen. Wählen Sie in Outlook unmittelbar über dem Text der E-Mail die Schaltfläche **Dokumentenverknüpfung** aus. Wählen Sie in der Outlook-Webanwendung *S-QUO1001* im Text der E-Mail aus.  

Im Dokumentenverknüpfungs-Add-In können Sie genauso Vorgänge für den Beleg ausführen und den Beleg ändern, wie im [!INCLUDE[d365fin](includes/d365fin_md.md)] .

## <a name="adding-the-add-ins-manually"></a>Das Add-In manuell hinzufügen
In einigen Fällen werden die Add-Ins nicht automatisch hinzugefügt zu Outlook. Selbst wenn Sie oder ein Kollege die unterstützte Einrichtung im Auftrag des Unternehmens ausführen, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] möglicherweise nicht in Outlook angezeigt. Wenn Sie dieses Problem haben, können Sie die Add-Ins in [!INCLUDE[d365fin](includes/d365fin_md.md)] manuell hinzufügen.  

Zuerst müssen Sie sicherstellen, dass Sie Zugriff auf die Add-Ins in Ihrem Office 365 Konto haben. Öffnen Sie einfach Outlook in einem Browser, öffnen Sie eine Nachricht, wählen Sie **Mehr Aktionen** (...) oben in der Nachricht und dann unten in der Liste **Add-Ins abrufen** aus. Dies öffnet die **Add-Ins für Outlook**-Seite, auf der Sie [!INCLUDE[prodshort](includes/prodshort.md)] für Outlook aktivieren können. Wenn Sie dann wieder zurück zu Outlook navigieren, sollte [!INCLUDE[prodshort](includes/prodshort.md)] verfügbar sein.  

Analog können Sie im Outlook-Desktopclient überprüfen, ob [!INCLUDE[d365fin](includes/d365fin_md.md)] auf der Seite **Add-Ins abrufen** aufgeführt ist.  

In beiden Fällen müssen Sie, sollte [!INCLUDE[d365fin](includes/d365fin_md.md)] immer noch nicht verfügbar sein, die Add-in-Manifest-Datei abrufen. Für weitere Informationen wenden Sie bitte an Ihren Office 365 Administrator.

## <a name="using-other-email-accounts"></a>Verwenden anderer E-Mail-Konten

Die Add-Ins sind für die Verwendung mit Office 365 konzipiert. Wenn Sie [!INCLUDE [prodshort](includes/prodshort.md)] lokal nutzen, wird Ihr Administrator wissen, ob Sie die [!INCLUDE [prodshort](includes/prodshort.md)] Add-Ins in Outlook verwenden können. Weitere Informationen finden Sie unter [Welche E-Mail-Adresse kann verwenden mit [!INCLUDE[prodshort](includes/prodshort.md)]?](across-faq.md#what-email-address-can-i-use-with-) uUnd [Funktionen, die bestimmte Umstände erfordern](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).  

## <a name="see-also"></a>Siehe auch

[Erste Schritte](product-get-started.md)  
[Abrufen von Business Central auf meinem mobilen Gerät](install-mobile-app.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Mindestanforderungen für die Verwendung von Outlook](product-requirements.md#outlook)  
[Add-Ins in Outlook im Internet nutzen](https://support.office.com/en-us/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
