---
title: E-Mail in Business Central einrichten | Microsoft Docs
description: 'Beschreibung: Beschreibt, wie der SMTP-Server des Unternehmens verwendet wird, um in Business Central E-Mail zu senden und zu empfangen und wie die E-Mail-Servereinstellungen verwendet werden, die im Office 365 Abonnement erstellt wurden.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 90e119dc44a23bcd9dca7920d05538ac685a44f6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304612"
---
# <a name="set-up-email"></a>E-Mail einrichten
Um E-Mails aus [!INCLUDE[d365fin](includes/d365fin_md.md)] zu senden und zu erhalten, müssen Sie die Felder auf der Seite SMTP-Mail-Einrichtung ausfüllen.

Anstatt die SMTP-Server-Details manuell einzugeben, können Sie die Funktion **Office 365 Server-Einstellungen übernehmen** verwenden, um sie mit den Informationen aus Ihrem Office 365-Abonnement einzugeben.

Sie können E-Mails entweder manuell einrichten wie unten beschrieben oder Sie können den Leitfaden für das unterstützte Setup für die **E-Mail-Einrichtung** verwenden. Weitere Informationen finden Sie unter [Vorbereitungen für das Ausführen von Geschäften](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Zum Einrichten von E-Mails
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **SMTP E-Mail einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Wenn Sie ein Konto verwenden, für das eine Zwei-Faktor-Authentifizierung erforderlich ist, muss das Kennwort, das Sie in das Feld **Passwort** eingeben, das gleiche sein wie das, das Sie für Ihr Office 365-Abonnement verwenden, und es muss vom Typ **App-Passwort** sein.
3. Wählen Sie alternativ die Aktion **Server-Einstellungen Office 365 übernehmen** aus, um Informationen einzufügen, die bereits für Ihr Office 365 Abonnement definiert ist.
4. Wenn alle korrekt Felder ausgefüllt sind, wählen Sie die Aktion **Test-E-Mail-Einrichtung** aus.
5. Wenn der Test erfolgreich war, schließen Sie die Seite.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Verwenden eine Ersatz-Absenderadresse für ausgehende E-Mail-Nachrichten
Alle ausgehenden E-Mail-Nachrichten von [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden die Standardadresse für das Konto, das Sie wie oben beschrieben auf der Seite SMTP-E-Mail-Setup angegeben haben. Sie können jedoch die **Senden Als** oder **Senden im Auftrag von** Funktionen auf Ihrem Exchange-Server zum Ändern der Absenderadresse für ausgehende Nachrichten verwenden. [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet das Standardkonto zur Authentifizierung bei Exchange, ersetzt jedoch entweder die Absenderadresse durch die von Ihnen angegebene oder ändert sie durch im Namen von.

Im Folgenden finden Sie Beispiele für die Verwendung von Senden als und Senden im Namen von [!INCLUDE[d365fin](includes/d365fin_md.md)].:

 * Wenn Sie Dokumente wie Kauf- oder Verkaufsaufträge an Lieferanten und Kunden senden, möchten Sie möglicherweise, dass sie von einer Adresse _noreply@yourcompanyname.com_ stammen.
 * Wenn Ihr Workflow eine Genehmigungsanfrage per E-Mail unter Verwendung der E-Mail-Adresse des Antragstellers sendet.

> [!Note]
> Sie können nur ein Konto verwenden, um Absenderadressen zu ersetzen. Das heißt, Sie können nicht eine Ersatzadresse für Einkaufsprozesse und eine andere für Verkaufsprozesse haben.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Um eine Ersatz-Senderadresse einzurichgen für alle ausgehenden E-Mail-Nachrichten
1. In dem **Exchange Admin Center** für Ihr Office 365 Konto suchen Sie das Postfach, das als Ersatzadresse verwendet werden soll, und kopieren Sie die Adress oder notieren Sie sie. Wenn Sie eine neue Adresse benötigen, rufen Sie Ihr Microsoft 365 Admin Center auf, um einen neuen Benutzer zu erstellen und dessen Postfach einzurichten.
2. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wählen Sie die ![Glühlampe, die die Funktion öffnet „Wie möchten Sie weiter verfahren“](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren"). Geben Sie **SMTP E-Mail einrichten** ein, und wählen dann den zugehörigen Link aus.
3. In dem Feld **Senden als** geben Sie in das Feld die Ersatzadresse ein.
4. Kopieren oder notieren Sie die Adresse im Feld **Benutzeridentifikation**.
5. In dem **Exchange Admin Center** suchen Sie die Mailbox, die als Ersatzadresse verwendet werden soll, und geben Sie die Adresse in das Feld **Benutzeridentifikation** im Feld **Senden Als** ein. Weitere Informationen finden Sie unter [Verwalten von Berechtigungen für Empfänger](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Verwendung der Ersatzadresse in Genehmigungsworkflows
1. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wählen Sie die ![Glühlampe, die die Funktion öffnet „Wie möchten Sie weiter verfahren“](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren"). Geben Sie **SMTP E-Mail einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Kopieren oder notieren Sie die Adresse im Feld **Benutzeridentifikation**.
3. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Genehmigungsbenutzer Einrichtung** ein, und wählen dann den zugehörigen Link aus.
4. In dem **Exchange Admin Center**, finden Sie die Postfächer für jeden Benutzer auf der Seite **Genehmigungsbenutzer einrichten** und im Feld **Senden Als** geben Sie die Adresse aus dem Bereich **Benutzeridentifikation** der Seite **SMTP-E-Mail einrichten** in [!INCLUDE[d365fin](includes/d365fin_md.md)] ein. Weitere Informationen finden Sie unter [Verwalten von Berechtigungen für Empfänger](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wählen Sie die ![Glühlampe, die die Funktion öffnet „Wie möchten Sie weiter verfahren“](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren"). Geben Sie **SMTP E-Mail einrichten** ein, und wählen dann den zugehörigen Link aus.
6. Um die Ersetzung zu aktivieren, aktivieren Sie das Kontrollkästchen **Erlaube Absenderersetzung**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] legt fest, welche Adresse in der folgenden Reihenfolge angezeigt werden soll: <br><br> 1. Die Adrsse, die im Feld **E-Mail** auf der Seite **Genehmigungsbenutzer einrichten** für Nachrichten in einem Workflow angegeben ist. <br> 2. Die Adresse im Feld **Senden Als** auf der Seite **SMTP-E-Mail-Setup** einrichten. <br> 3. Die Adresse im Feld **Benutzeer-ID** auf der Seite **SMTP-E-Mail einrichten**.


## <a name="see-also"></a>Siehe auch  
[Freigegebene Postfächer in Exchange Online](https://docs.microsoft.com/en-us/exchange/collaboration-exo/shared-mailboxes)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Einrichten [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Nutzen von [!INCLUDE[d365fin](includes/d365fin_md.md)] als Ihr Unternehmenspostfach in Outlook](admin-outlook.md)  
[Abrufen von [!INCLUDE[d365fin](includes/d365fin_md.md)] auf meinem mobilen Gerät](install-mobile-app.md)
