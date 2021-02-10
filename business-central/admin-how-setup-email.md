---
title: E-Mail in Business Central einrichten | Microsoft Docs
description: Beschreibt, wie E-Mail-Konten mit Business Central verbunden werden, damit Sie ausgehende Nachrichten senden können, ohne eine andere App öffnen zu müssen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.date: 06/15/2020
ms.author: bholtorf
ms.openlocfilehash: 44fb1f467b0b44c41456a64c8de3f5ae9dc85786
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752750"
---
# <a name="set-up-email"></a>E-Mail einrichten
Menschen in Unternehmen senden täglich Informationen und Dokumente wie Verkaufsdokumente und Bestellungen sowie Rechnungen per E-Mail. Administratoren können dies vereinfachen, indem sie ein oder mehrere E-Mail-Konten mit [!INCLUDE[prod_short](includes/prod_short.md)] verbinden. So können Sie Dokumente senden, ohne eine E-Mail-App öffnen zu müssen. Sie können jede Nachricht einzeln mit grundlegenden Formatierungswerkzeugen wie Schriftarten, Stilen, Farben usw. zusammenstellen und Anhänge mit bis zu 100 MB hinzufügen. Administratoren können auch Berichtslayouts einrichten, die nur die wichtigsten Informationen aus Dokumenten enthalten. Weitere Informationen finden Sie unter [Senden von Dkumenten über E-Mail](ui-how-send-documents-email.md).

Die E-Mail-Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)] sind nur für ausgehende Nachrichten. Sie können keine Antworten erhalten, d.h es ist keine Posteingangsseite vorhanden in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden, bevor Sie eine E-Mail einrichten können, müssen Sie vor Ort eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)] im Azure-Portal erstellen. Die App-Registrierung wird [!INCLUDE[prod_short](includes/prod_short.md)] aktiviert, um mit Ihrem E-Mail-Anbieter zu authentifizieren und zu autorisieren. Weitere Informationen finden Sie unter [E-Mail für Business Central lokal einrichten](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). In [!INCLUDE[prod_short](includes/prod_short.md)] online erledigen wir das für Sie.

## <a name="required-permissions"></a>Erforderliche Berechtigungen
Um E-Mails einzurichten, müssen Sie den **E-MAIL-EINRICHTEN** Berechtigungssatz haben. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md). 

## <a name="adding-email-accounts"></a>E-Mail-Konten hinzufügen
Sie fügen E-Mail-Konten über Erweiterungen hinzu, mit denen Konten verschiedener Anbieter eine Verbindung herstellen können in [!INCLUDE[prod_short](includes/prod_short.md)]. Mit den Standarderweiterungen können Sie Konten von Microsoft Exchange Online verwenden, aber möglicherweise sind andere Erweiterungen verfügbar, mit denen Sie Konten von anderen Anbietern wie Google Mail verbinden können.

Nachdem Sie ein E-Mail-Konto hinzugefügt haben, können Sie vordefinierte Geschäftsszenarien angeben, in denen das Konto zum Senden von E-Mails verwendet werden soll. Sie können beispielsweise festlegen, dass alle Benutzer Verkaufsbelege von einem Konto senden und Dokumente von einem anderen Konto kaufen. Weitere Informationen finden Sie unter [Weisen Sie E-Mail-Konten E-Mail-Szenarien zu](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

In der folgenden Tabelle werden die standardmäßig verfügbaren E-Mail-Erweiterungen beschrieben.

|Erweiterung  |Beschreibung  |Beispiele für die Verwendung  |
|---------|---------|---------|
|**Microsoft 365**|Jeder sendet E-Mails von einem freigegebenen Postfach in Exchange Online.|Wenn beispielsweise alle Nachrichten aus derselben Abteilung stammen, sendet Ihre Verkaufsorganisation Nachrichten von einem sales@cronus.com-Konto. Dies erfordert, dass Sie ein freigegebenes Postfach im Office 365 Admin Center einrichten. Weitere Informationen finden Sie unter [Freigegebene Postfächer](/Exchange/collaboration/shared-mailboxes/shared-mailboxes.md).|
|**Aktueller Benutzer**|Jeder sendet E-Mails von dem Konto, bei dem er sich angemeldet hat in [!INCLUDE[prod_short](includes/prod_short.md)].|Ermöglichen Sie die Kommunikation von einzelnen Konten.|
|**Andere (SMTP)**|Verwenden Sie SMTP-Protokoll zum Senden von E-Mails.|Ermöglichen Sie die Kommunikation über Ihren SMTP-Mailserver. |

> [!NOTE]
> Die Erweiteriungen **Microsoft 365** und **Aktueller Benutzer** verwenden die Konten, die Sie für Benutzer im Microsoft 365 Admin Center für Ihr Office 365 Abonnement eingerichtet haben. Um E-Mails mit den Erweiterungen senden zu können, müssen Benutzer über eine gültige Lizenz für Exchange Online verfügen. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Ältere SMTP-Einstellungen und die E-Mail-SMTP-Connector-Erweiterung
Wenn Sie bereits [!INCLUDE[prod_short](includes/prod_short.md)] verwenden und E-Mails über die ältere SMTP-Einrichtung konfiguriert haben, können Sie Ihre Einrichtung parallel zur Erweiterung E-Mail – SMTP Connector weiter verwenden. Wenn wir Ihre [!INCLUDE[prod_short](includes/prod_short.md)] in der nächsten Release-Version aktualisieren, kopieren wir Ihre alten SMTP-Einstellungen in die Erweiterung Email – SMTP Connector. Wenn Sie fertig sind, kann Ihr Administrator die erweiterten E-Mail-Funktionen aktivieren und Sie verwenden die Erweiterung E-Mail – SMTP Connector. Weitere Informationen hierzu finden Sie unter [Funktionsverwaltung](/dynamics365/business-central/dev-itpro/administration/feature-management.md#about-feature-management). Es gibt jedoch keine Synchronisation zwischen der SMTP Connector-Erweiterung und den Legacy-Einstellungen. Wenn Sie die SMTP-Einstellungen in der Erweiterung ändern, sollten Sie dieselben Änderungen in der alten SMTP-Einrichtung vornehmen oder umgekehrt.

> [!NOTE]
> Wenn Sie Anpassungen haben, die auf der alten SMTP-E-Mail-Einrichtung basieren, besteht die Möglichkeit, dass bei Ihren Anpassungen ein Fehler auftritt, wenn Sie E-Mail-Erweiterungen verwenden. Wir empfehlen, dass Sie die Erweiterungen einrichten und testen, bevor Sie den Funktionsschalter für erweiterte E-Mail-Funktionen aktivieren.

## <a name="add-email-accounts"></a>E-Mail-Konten hinzufügen
Die unterstützte Einrichtungsanleitung für das **Einrichten von E-Mails** kann Ihnen helfen, rasch mit dem Senden von E-Mails zu beginnen.

> [!NOTE]
> Sie müssen über ein Standard-E-Mail-Konto verfügen, auch wenn Sie nur ein Konto hinzufügen. Das Standardkonto wird für alle E-Mail-Szenarien verwendet, die keinem Konto zugewiesen sind. Weitere Informationen finden Sie unter [Weisen Sie E-Mail-Konten E-Mail-Szenarien zu](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Servicevertragskontengruppen** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Office 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>Weisen Sie E-Mail-Konten E-Mail-Szenarien zu
E-Mail-Szenarien sind Prozesse, bei denen ein Dokument wie ein Verkaufsdokument oder eine Bestellung oder eine Benachrichtigung wie eine Einladung an einen externen Buchhalter gesendet wird. Sie können bestimmte E-Mail-Konten für bestimmte Szenarien verwenden. Beispielsweise können Sie festlegen, dass alle Benutzer Verkaufsdokumente immer von einem Konto senden, Dokumente von einem anderen kaufen und Lager- oder Produktionsdokumente von einem dritten Konto aus senden. Sie können Szenarien jederzeit zuweisen, neu zuweisen und entfernen, aber Sie können jeweils nur einem E-Mail-Konto ein Szenario zuweisen. Das Standardkonto für E-Mail wird für alle E-Mail-Szenarien verwendet, die keinem Konto zugewiesen sind.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Richten Sie wiederverwendbare E-Mail-Texte und Layouts für Verkaufs- und Einkaufsbelege ein
Sie können Berichte verwenden, um wichtige Informationen aus Verkaufs- und Kaufdokumenten in Texte für E-Mails aufzunehmen. In diesem Verfahren wird beschrieben, wie Sie den Bericht **Verkaufsrechnung** für gebuchte Verkaufsrechnungen einrichten, aber der Prozess ist für andere Berichte ähnlich.

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Berichtsauswahl Verkäufe** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Berichts-Auswahl - Verkauf** unter **Verwendung** wählen Sie **Rechnung**.
3. In einer neuen Zeile im Feld **Berichts-ID** wählen Sie beispielsweise Standardbericht 1306.
4. Wählen Sie das Kontrollkästchen **Für E-Mail-Text verwenden**.
5. Wählen Sie das Feld **E-Mail-Text-Layout-Code** und wählen Sie ein Layout aus der Liste aus.

    Berichtslayouts definieren das Format und den Inhalt des E-Mail-Texts, einschließlich den Standardtext, wie Anrede oder Anweisungen, die den Dokumentinformationen vorangehen. Sie können alle verfügbaren Berichtslayouts sehen, wenn Sie die Schaltfläche **Aus vollständiger Liste auswählen** in der Liste auswählen.
6. Um das Layout anzusehen oder zu bearbeiten, auf dem der E-Mail-Text basiert, gehen Sie zur Seite **Benutzerdefinierte Berichtslayouts** und wählen die Aktion **Layout bearbeiten** aus.
7. Um Ihren Debitoren anzubieten, für Verkäufe unter Verwendung eines Zahlungsservice wie Paypal elektronisch zu bezahlen, können Sie die Paypal-Informationen und Links auch in den E-Mail-Text einfügen. Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch Paypal](sales-how-enable-payment-service-extensions.md)
8. Wählen Sie die Schaltfläche **OK** aus.

Wenn Sie jetzt beispielsweise die Aktion **Senden** auf der Seite **Gebuchte Verkaufsrechnung** auswählen, enthält der E-Mail-Text die Beleginformationen 1306 des Berichts, der vom formatierten Standardtext entsprechend dem Berichtslayout stammt, das Sie in Schritt 5 ausgewählt haben.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Verwenden eine Ersatz-Absenderadresse für ausgehende E-Mail-Nachrichten
Wenn Sie die früheren SMTP-Einstellungen verwenden, können Sie jedoch die **Senden Als** oder **Senden im Auftrag von** Funktionen von Microsoft Exchange zum Ändern der Absenderadresse für ausgehende Nachrichten verwenden. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet das SMTP- Konto zur Authentifizierung bei Exchange, ersetzt jedoch entweder die Absenderadresse durch die von Ihnen angegebene oder ändert sie durch im Namen von.

Im Folgenden finden Sie Beispiele für die Verwendung von Senden als und Senden im Namen von [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Wenn Sie Dokumente wie Kauf- oder Verkaufsaufträge an Lieferanten und Kunden senden, möchten Sie möglicherweise, dass sie von einer Adresse _noreply@yourcompanyname.com_ stammen.
 * Wenn Ihr Workflow eine Genehmigungsanfrage per E-Mail unter Verwendung der E-Mail-Adresse des Antragstellers sendet.

> [!Note]
> Sie können nur ein Konto verwenden, um Absenderadressen zu ersetzen. Das heißt, Sie können nicht eine Ersatzadresse für Einkaufsprozesse und eine andere für Verkaufsprozesse haben.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Um eine Ersatz-Senderadresse einzurichgen für alle ausgehenden E-Mail-Nachrichten
1. In dem **Exchange Admin Center** für Ihr Microsoft 365-Konto suchen Sie das Postfach, das als Ersatzadresse verwendet werden soll, und kopieren Sie die Adresse oder notieren Sie sie. Wenn Sie eine neue Adresse benötigen, rufen Sie Ihr Microsoft 365 Admin Center auf, um einen neuen Benutzer zu erstellen und dessen Postfach einzurichten.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun") aus, geben Sie **SMTP-E-Mail-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
3. In dem Feld **Senden als** geben Sie in das Feld die Ersatzadresse ein.
4. Kopieren oder notieren Sie die Adresse im Feld **Benutzeridentifikation**.
5. In dem **Exchange Admin Center** suchen Sie die Mailbox, die als Ersatzadresse verwendet werden soll, und geben Sie die Adresse in das Feld **Benutzeridentifikation** im Feld **Senden Als** ein. Weitere Informationen finden Sie unter [Verwenden Sie die Exchange-Verwaltungskonsole, um einzelnen Postfächern Berechtigungen zuzuweisen ](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Verwendung der Ersatzadresse in Genehmigungsworkflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **SMTP-E-Mail-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Kopieren oder notieren Sie die Adresse im Feld **Benutzeridentifikation**.
3. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Genehmigungsbenutzereinrichtung** ein und wählen Sie dann den entsprechenden Link.
4. In dem **Exchange Admin Center**, finden Sie die Postfächer für jeden Benutzer auf der Seite **Genehmigungsbenutzer einrichten** und im Feld **Senden Als** geben Sie die Adresse aus dem Bereich **Benutzeridentifikation** der Seite **SMTP-E-Mail einrichten** in [!INCLUDE[prod_short](includes/prod_short.md)] ein. Weitere Informationen finden Sie unter [Verwalten von Berechtigungen für Empfänger](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **SMTP-E-Mail-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
6. Um die Ersetzung zu aktivieren, aktivieren Sie das Kontrollkästchen **Erlaube Absenderersetzung**.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] legt fest, welche Adresse in der folgenden Reihenfolge angezeigt werden soll: <br><br> 1. Die Adrsse, die im Feld **E-Mail** auf der Seite **Genehmigungsbenutzer einrichten** für Nachrichten in einem Workflow angegeben ist. <br> 2. Die Adresse im Feld **Senden Als** auf der Seite **SMTP-E-Mail-Setup** einrichten. <br> 3. Die Adresse im Feld **Benutzeer-ID** auf der Seite **SMTP-E-Mail einrichten**.

## <a name="set-up-document-sending-profiles"></a>Belegsendeprofile einrichten
Sie können für jeden Ihrer Kunden eine bevorzugte Methode zum Senden von Verkaufsunterlagen einrichten, damit Sie nicht jedes Mal, wenn Sie ein Dokument senden, eine Versandoption auswählen müssen, z. B. ob Sie das Dokument per E-Mail oder als elektronisches Dokument senden möchten. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Öffentliche Ordner und Regeln für die E-Mail-Anmeldung in Exchange Online einrichten
Machen Sie mehr aus der Kommunikation zwischen Verkäufern und Ihren bestehenden oder potenziellen Kunden, indem Sie den E-Mail-Austausch nachverfolgen und diese dann in umsetzbare Gelegenheiten umwandeln. Weitere Informationen finden Sie unter [Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten nachverfolgen](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Als nächstes verbinden Sie [!INCLUDE[prod_short](includes/prod_short.md)] mit Exchange Online. Weitere Informationen finden Sie unter [Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten nachverfolgen](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>Einrichten von E-Mails für Business Central lokal 
[!INCLUDE[prod_short](includes/prod_short.md)] lokal kann mit Services integriert werden, die auf Microsoft Azure basieren. Zum Beispiel können Sie Cortana Intelligence für intelligentere Cashflow-Prognosen verwenden, Power BI, um Ihr Geschäft zu visualisieren und Exchange Online zum Versenden von E-Mails. Die Integration mit diesen Diensten basiert auf einer App-Registrierung in Azure Active Directory. Die App-Registrierung bietet Authentifizierungs- und Autorisierungsdienste für die Kommunikation. So verwenden Sie die E-Mail-Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)] lokal, Sie müssen Sie [!INCLUDE[prod_short](includes/prod_short.md)] als App im Azure-Portal registrieren und dann [!INCLUDE[prod_short](includes/prod_short.md)] mit der App-Registrierung verwenden. In den folgenden Abschnitten werden diese Schritte beschrieben.

### <a name="create-an-app-registration-for-prod_short-in-azure-portal"></a>Erstellen Sie eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)] in Azure Portal
Die Schritte zur Registrierung von [!INCLUDE[prod_short](includes/prod_short.md)] im Azure-Portal werden in [Registrieren Sie eine Bewerbung in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) beschrieben. Die Einstellungen, die für die E-Mail-Funktionen spezifisch sind, sind die delegierten Berechtigungen, die Sie Ihrer App-Registrierung erteilen. In der folgenden Tabelle sind die Mindestberechtigungen aufgeführt.

|API/Berechtigungsname  |Typ  |Beschreibung  |
|---------|---------|---------|
|Microsoft Graph/User.Read |Stellvertretend|Melden Sie sich an und lesen Sie das Benutzerprofil.         |
|Microsoft Graph/Mail.ReadWrite |Stellvertretend|Verfassen Sie eine E-Mail-Nachricht.         |
|Microsoft Graph/Mail.Send|Stellvertretend|E-Mail-Nachricht senden.         |
|Microsoft Graph/offline_access|Stellvertretend|Behalten Sie die Einwilligung zum Datenzugriff bei. <!--need to verify this-->|

> [!TIP]
> Wenn Sie Ihre App-Registrierung erstellen, müssen Sie folgende Informationen angeben. Sie benötigen sie, um eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] herzustellen, um Ihre App zu registrieren.
> 
> * Anwendungs-ID (Client-ID) 
> * URI umleiten (optional)
> * Geheimer Clientschlüssel

Für allgemeine Informationen zum Registrieren einer Anwendung gehen Sie zu [Schnellstart: Anwendung bei der Microsoft-Identitätsplattform registrieren](/azure/active-directory/develop/quickstart-register-app.md). 

### <a name="connect-prod_short-to-your-app-registration"></a>[!INCLUDE[prod_short](includes/prod_short.md)] mit Ihrer App-Anmeldung verbinden
Nachdem Sie Ihre Anwendung im Azure-Portal registriert haben, klicken Sie auf [!INCLUDE[prod_short](includes/prod_short.md)], benutzen Sie die **E-Mail-Anwendung AAD-Registrierung** unterstützte Einrichtung, um die Verbindung [!INCLUDE[prod_short](includes/prod_short.md)] herzustellen.

1. In [!INCLUDE[prod_short](includes/prod_short.md)] wählen Sie das Symbol ![Glühbirne, das die Funktion „wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **AAD-E-Mail-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Wenn Sie zum ersten Mal eine Verbindung herstellen, können Sie alternativ die unterstützte Einrichtung **E-Mail einrichten** verwenden. Der Leitfaden benötigt die Informationen, um eine Verbindung zu Ihrer App-Registrierung herzustellen. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-also"></a>Siehe auch
[Freigegebene Postfächer in Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Einrichten [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)  
[Nutzen von [!INCLUDE[prod_short](includes/prod_short.md)] als Ihr Unternehmenspostfach in Outlook](admin-outlook.md)  
[Abrufen von [!INCLUDE[prod_short](includes/prod_short.md)] auf meinem mobilen Gerät](install-mobile-app.md)
