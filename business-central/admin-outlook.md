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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b088cf18c10dd451c7c5974e98f0c0cbba5bad0b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186898"
---
# <a name="using-business-central-as-your-business-inbox-in-outlook"></a>Nutzen Sie Business Central als Ihr Unternehmenspostfach in Outlook

[!INCLUDE[d365fin](includes/d365fin_md.md)] stellt die Möglichkeit vor, Geschäftsaktivitäten mit Ihren Debitoren und Kreditoren direkt in Microsoft Outlook zu verwalten. Mit dem [!INCLUDE[d365fin](includes/d365fin_md.md)] Outlook-Add-In können Sie die Finanzdaten sehen, die mit den Debitoren und Kreditoren verknüpft sind, sowie Finanzbelege wie beispielsweise Angebote und Rechnungen erstellen und versenden.  

## <a name="getting-the-add-in"></a>Das Add-in abrufen
Die ersten Schritte sind einfach mit dem [!INCLUDE[d365fin](includes/d365fin_md.md)] Add-In für Outlook. Mit dem unterstützten Setup Richten Sie Ihren **Geschäfts-Eingang in Outlook** ein können Sie die Verbindung für sich oder für Ihre Organisation einrichten, wenn Ihre Organisation Office 365 verwendet. Geben Sie einfach Ihren Office 365 Benutzername und Passwort ein, wenn Sie dazu aufgefordert werden, und teilen Sie uns mit, ob Sie eine Beispiel-E-Mail-Nachricht erhalten möchten. Die [!INCLUDE[d365fin](includes/d365fin_md.md)] Add-Ins werden dann automatisch Outlook hinzugefügt. Weitere Informationen finden Sie unter [Mindestanforderungen für Outlook](product-requirements.md#outlook).  

Wenn Sie Outlook öffnen, sehen Sie eine E-Mail-Nachricht vom *Dynamics 365 Business Central Admin*. Das neue Add-In wird dem Outlook-Menüband und Outlook Web Access hinzugefügt. Sie können die [!INCLUDE[prodshort](includes/prodshort.md)]-Add-Ins unmittelbar über oder unter dem Text der E-Mail sehen. Das Add-In selbst wird regelmäßig aktualisiert, und Sie werden benachrichtigt, wenn eine neue Version in Outlook bereit ist.  

> [!TIP]
> Wenn Sie das neue Outlook im Web verwenden, können die [!INCLUDE [prodshort](includes/prodshort.md)]-Add-Ins unter **Weitere Aktionen** ausgeblendet werden. Wenn Sie das Add-In häufig verwenden, können Sie es so anheften, dass es immer sofort sichtbar ist. Weitere Informationen finden Sie unter [Verwenden von Add-Ins in Outlook im Web](https://support.office.com/article/using-add-ins-in-outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?ns=OLWAO365B&version=16).  

Wenn Sie mit mehr als einer [!INCLUDE [prodshort](includes/prodshort.md)] Firma arbeiten, können Sie in Outlook ganz einfach zwischen den Unternehmen wechseln. Wählen Sie in der Aktionsleiste **Weitere Aktionen** aus, und dann sehen Sie die Option zum Wechseln zwischen Unternehmen.  

<!--TEMP-->
> [!NOTE]
> Der Wechsel zwischen Unternehmen erfordert [!INCLUDE [prodshort](includes/prodshort.md)] 2019 Release Wave 2 oder höher wie angekündigt im [Release-Plan](/dynamics365-release-plan/2019wave2/dynamics365-business-central/switch-between-companies-business-inbox-outlook).

Einige Unternehmen, die Office 365 verwenden, schränken die Berechtigungen der Benutzer zur Bereitstellung von Add-Ins ein. Sie müssen also sicherstellen, dass Sie ein Office 365-Abonnement haben, das E-Mail enthält und Ihnen die Bereitstellung von Add-Ins erlaubt. Wenn Sie das Add-In trotzdem ausprobieren möchten, können Sie [Office 365 kostenlos ausprobieren](https://products.office.com/try).  

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

Die Add-Ins sind für die Verwendung mit Office 365 konzipiert. Wenn Sie [!INCLUDE [prodshort](includes/prodshort.md)] lokal nutzen, wird Ihr Administrator wissen, ob Sie die [!INCLUDE [prodshort](includes/prodshort.md)] Add-Ins in Outlook verwenden können. Weitere Informationen finden Sie unter [Welche E-Mail-Adresse kann verwenden mit [!INCLUDE[prodshort](includes/prodshort.md)]?](across-faq.md#email) uUnd [Funktionen, die bestimmte Umstände erfordern](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Erste Schritte](product-get-started.md)  
[Abrufen von Business Central auf meinem mobilen Gerät](install-mobile-app.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Finanzen](finance.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Mindestanforderungen für die Verwendung von Outlook](product-requirements.md#outlook)  
[Add-Ins in Outlook im Internet nutzen](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  
