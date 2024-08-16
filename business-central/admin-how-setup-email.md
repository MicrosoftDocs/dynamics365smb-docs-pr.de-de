---
title: E-Mail in Business Central einrichten
description: 'Beschreibt, wie E-Mail-Konten mit Business Central verbunden werden, damit Sie ausgehende Nachrichten senden können, ohne eine andere App öffnen zu müssen.'
author: brentholtorf
ms.author: bholtorf
ms.topic: get-started
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263, 8898_Primary, 8897_Primary'
ms.date: 06/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-email"></a>E-Mail einrichten

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Menschen in Unternehmen senden täglich Informationen und Dokumente wie Verkaufsdokumente und Bestellungen sowie Rechnungen per E-Mail. Administratoren können ein oder mehrere E-Mail-Konten mit [!INCLUDE[prod_short](includes/prod_short.md)] verbinden. So können Sie Dokumente senden, ohne eine E-Mail-App öffnen zu müssen. Sie können jede Nachricht einzeln mit grundlegenden Formatierungswerkzeugen wie Schriftarten, Stilen, Farben usw. zusammenstellen und Anhänge mit bis zu 100 MB hinzufügen. Mit Berichtslayouts können Administratoren außerdem die wichtigsten Informationen aus Belegen einbeziehen. Erfahren Sie mehr unter [Artikel versenden und Dokumente per E-Mail versenden](ui-how-send-documents-email.md).

E-Mail-Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)] sind nur für ausgehende Nachrichten vorgesehen. Sie können keine Antworten erhalten, d. h. die Seite „Posteingang“ ist nicht vorhanden.

> [!NOTE]
> Sie können die E-Mail-Funktionalitäten von [!INCLUDE[prod_short](includes/prod_short.md)] online nur mit Exchange Online verwenden. Wir unterstützen keine hybriden Szenarien, wie z.B. die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] online mit einer lokalen Version von Exchange.
>
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal verwenden, bevor Sie eine E-Mail einrichten können, müssen Sie vor Ort eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)] im Azure-Portal erstellen. Die App-Registrierung wird [!INCLUDE[prod_short](includes/prod_short.md)] aktiviert, um mit Ihrem E-Mail-Anbieter zu authentifizieren und zu autorisieren. Weitere Informationen unter [E-Mail für Business Central On-Premises einrichten](admin-how-setup-email.md#set-up-email-for-business-central-on-premises). In [!INCLUDE[prod_short](includes/prod_short.md)] online erledigen wir das für Sie.

## <a name="requirements"></a>Anforderungen

Für die Einrichtung und Verwendung der E-Mail-Funktionen gibt es einige Anforderungen.

* Um E-Mails einzurichten, müssen Sie den **E-MAIL-EINRICHTEN** Berechtigungssatz haben. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).
* Jeder, der die E-Mail-Funktionen verwenden möchte, muss über eine umfassende Lizenz verfügen [!INCLUDE [prod_short](includes/prod_short.md)]. Delegierte Administratoren und Gastbenutzer können zum Beispiel das E-Mail-Konto des Mandanten nicht verwenden.

## <a name="add-email-accounts"></a>E-Mail-Konten hinzufügen

Sie fügen E-Mail-Konten über Erweiterungen hinzu, mit denen Konten verschiedener Anbieter eine Verbindung herstellen können in [!INCLUDE[prod_short](includes/prod_short.md)]. Mit den Standarderweiterungen können Sie Konten von Microsoft Exchange Online verwenden. Möglicherweise sind jedoch andere Erweiterungen verfügbar, mit denen Sie Konten von anderen Anbietern verbinden können, z. B. Gmail.

Sie können vordefinierte Geschäftsszenarien angeben, in denen ein E-Mail-Konto zum Senden von E-Mails verwendet werden soll. Sie können beispielsweise festlegen, dass alle Benutzer Verkaufsbelege von einem Konto senden und Dokumente von einem anderen Konto kaufen. Erfahren Sie mehr unter [E-Mail-Szenarien zu E-Mail-Konten zuweisen](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

In der folgenden Tabelle werden die standardmäßig verfügbaren E-Mail-Erweiterungen beschrieben.

|Erweiterung  |Beschreibung  |Beispiele für die Verwendung  |
|---------|---------|---------|
|**Microsoft 365-Konnektor**|Jeder sendet E-Mails von einem freigegebenen Postfach in Exchange Online.|Wenn beispielsweise alle Nachrichten aus derselben Abteilung stammen, sendet Ihre Verkaufsorganisation Nachrichten von einem sales@cronus.com-Konto. Diese Option erfordert, dass Sie ein freigegebenes Postfach im Microsoft 365 Admin Center einrichten. Weitere Informationen finden Sie unter [Freigegebene Postfächer](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Konnektor für aktuellen Benutzer**|Jeder sendet E-Mails von dem Konto, bei dem er sich angemeldet hat in [!INCLUDE[prod_short](includes/prod_short.md)].|Ermöglichen Sie die Kommunikation von einzelnen Konten.|
|**SMTP Connector**|Verwenden Sie SMTP-Protokoll zum Senden von E-Mails.|Ermöglichen Sie die Kommunikation über Ihren SMTP-Mailserver. |

Die Erweiterungen **Microsoft 365-Konnektor** und **Aktueller Benutzer-Konnektor** verwenden die Konten, die Sie für Benutzer im Microsoft 365 Admin Center für Ihr Microsoft 365-Abonnement eingerichtet haben. Um E-Mails mit den Erweiterungen senden zu können, müssen Benutzer über eine gültige Lizenz für Exchange Online verfügen. In Sandbox-Umgebungen erfordern diese Erweiterungen einschließlich der Erweiterung **Outlook-REST-API** außerdem, dass die Einstellung **HttpClient-Anfragen zulassen** aktiviert ist. Um zu überprüfen, ob es für diese Erweiterungen aktiviert ist, gehen Sie zur Seite **Erweiterungsverwaltung**, wählen Sie die Erweiterung und dann die Option **Konfigurieren** aus.

Externe Benutzer wie delegierte Administratoren und externe Buchhalter können diese Erweiterungen nicht zum Senden von E-Mail-Nachrichten über [!INCLUDE[prod_short](includes/prod_short.md)] verwenden.

> [!NOTE]
> Wenn Sie die Service-to-Service-Authentifizierung (S2S) verwenden, können die Konnektoren „Microsoft 365“ und „Aktueller Benutzer“ den Benutzer nicht authentifizieren, wenn dieser ein Verkaufs- oder Einkaufsdokument per E-Mail sendet. Wenn jemand ein Dokument sendet, wird die folgende Fehlermeldung angezeigt:
>
> „Sie sind nicht berechtigt, auf diese Ressource zuzugreifen: https:\//graph.microsoft.com/.default. Wenden Sie sich an Ihren Systemadministrator.“
>
> Das Problem wird durch die gebundenen Aktionen der Dokument-APIs verursacht, die E-Mails senden. Weitere Informationen zu gebundenen Aktionen finden Sie unter [Gebundene Aktionen](/dynamics365/business-central/dev-itpro/api-reference/v2.0/resources/dynamics_salesinvoice#bound-actions). 
>
> Wenn Sie die S2S-Authentifizierung und die E-Mail-Funktionen verwenden möchten, verwenden Sie die Option „SMTP Connector“.
<br><br>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="use-smtp"></a>SMTP verwenden

Wenn Sie das SMTP-Protokoll zum Senden von E-Mails über [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchten, können Sie die SMTP Connector-Erweiterung verwenden. Wenn Sie ein Konto einrichten, das SMTP verwendet, ist das Feld **Absendertyp** wichtig. Wenn Sie **Bestimmter Benutzer** auswählen, werden E-Mails mit dem Namen und anderen Informationen des Kontos gesendet, das Sie einrichten. Wenn Sie jedoch **Aktueller Benutzer** auswählen, werden E-Mails von dem E-Mail-Konto gesendet, das für das Konto jedes Benutzers angegeben ist. „Aktueller Benutzer“ ähnelt der Funktion „Senden als“. Weitere Informationen finden Sie unter [Eine Ersatz-Absenderadresse für ausgehende E-Mail-Nachrichten verwenden](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Um OAuth für SMTP verwenden zu können, müssen sich alle Benutzer im selben Microsoft Entra-Mandanten befinden. 
> 
> Sie müssen eine Anwendungsregistrierung im Azure-Portal erstellen und dann die Anleitung **Microsoft Entra-ID einrichten** zur unterstützten Einrichtung in [!INCLUDE[prod_short](includes/prod_short.md)] ausführen, um eine Verbindung mit Microsoft Entra-ID herzustellen. Weitere Informationen finden Sie unter [Eine App-Registrierung für Business Central im Azure-Portal erstellen](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online unterstützt nicht länger die Verwendung der Standardauthentifizierung für SMTP. Mandanten, die derzeit SMTP AUTH verwenden, sind von dieser Änderung nicht betroffen. Wir empfehlen jedoch dringend, die neueste Version von [!INCLUDE [prod_short](includes/prod_short.md)] zu verwenden und die OAuth 2.0-Authentifizierung für SMTP einzurichten. Wir werden keine zertifikatbasierte Authentifizierung für frühere Versionen von [!INCLUDE [prod_short](includes/prod_short.md)]wie z. B. Version 14, hinzufügen. Wenn Sie die OAuth 2.0-Authentifizierung nicht einrichten können, empfehlen wir Ihnen, Alternativen von Drittanbietern zu prüfen, wenn Sie SMTP-E-Mail in früheren Versionen verwenden möchten.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="use-the-set-up-email-assisted-setup-guide"></a>Leitfaden zur unterstützten Einrichtung „E-Mail einrichten“ verwenden

Die unterstützte Einrichtungsanleitung für das **Einrichten von E-Mails** kann Ihnen helfen, rasch mit dem Senden von E-Mails zu beginnen.

> [!NOTE]
> Sie müssen über ein Standard-E-Mail-Konto verfügen, auch wenn Sie nur ein Konto hinzufügen. Das Standardkonto wird für alle E-Mail-Szenarien verwendet, die keinem Konto zugewiesen sind. Erfahren Sie mehr unter [E-Mail-Szenarien zu E-Mail-Konten zuweisen](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **E-Mail-Konten einrichten** ein, und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>E-Mail-Szenarien zu E-Mail-Konten zuweisen

E-Mail-Szenarien sind Prozesse, bei denen ein Dokument gesendet wird. Beispielsweise eine Einkaufsbestellung oder ein Verkaufsauftrag oder eine Benachrichtigung wie eine Einladung an einen externen Buchhalter. Bestimmte E-Mail-Konten können für bestimmte Szenarien verwendet werden. Beispielsweise können Sie festlegen, dass alle Benutzer Verkaufsdokumente immer von einem Konto senden, Dokumente von einem anderen kaufen und Lager- oder Produktionsdokumente von einem dritten Konto aus senden. Sie können Szenarien jederzeit zuweisen, neu zuweisen und entfernen. Ein Szenario kann jeweils nur einem E-Mail-Konto zugewiesen werden. Das Standard-E-Mail-Konto wird für alle Szenarien verwendet, die keinem Konto zugewiesen sind.

Auf der Seite **Zuordnung von E-Mail-Szenarien** können Sie die Aktion **Standardanhänge festlegen** wählen, um Anhänge zu E-Mail-Szenarien hinzuzufügen. Die Anhänge sind dann immer verfügbar, wenn Sie eine E-Mail für ein Dokument verfassen, das mit dem Szenario in Verbindung steht. Jedes E-Mail-Szenario kann einen oder mehrere Standardanhänge haben. Die Standardanhänge werden automatisch zu den E-Mails für das E-Mail-Szenario hinzugefügt. Wenn Sie zum Beispiel einen Verkaufsauftrag per E-Mail versenden, wird der für das Szenario Verkaufsauftrag angegebene Standardanhang hinzugefügt. Standardanhänge werden im Abschnitt **Anhänge** unten auf der Seite **E-Mail verfassen** angezeigt. Sie können der E-Mail manuell Anhänge hinzufügen, die nicht zum Standard gehören.

<!--
## <a name="to-set-up-email"></a>To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a>Anzeigerichtlinien einrichten

Sie können die E-Mail-Nachrichten steuern, auf die ein Benutzer auf den Seiten „E-Mail-Ausgang“ und „Gesendete E-Mails“ zugreifen kann.

Wählen Sie unter **Benutzer-E-Mail-Ansichtsrichtlinien** einen Benutzer und dann eine der folgenden Optionen im Feld **E-Mail-Ansichtsrichtlinie** aus:

* **Eigene E-Mails anzeigen** – Der Benutzer kann nur seine eigenen E-Mail-Nachrichten anzeigen.
* **Alle E-Mails anzeigen** – Der Benutzer kann alle E-Mail-Nachrichten anzeigen, einschließlich E-Mails, die von anderen Benutzern gesendet wurden.
* **Ansicht, wenn Zugriff auf alle verknüpften Datensätze** – Diese Anzeigerichtlinie wird verwendet, wenn keine andere Richtlinie angegeben ist. Ein Benutzer kann E-Mail-Nachrichten anzeigen, die andere Benutzer gesendet haben, wenn der Benutzer Zugriff auf den gesendeten Datensatz und alle zugehörigen Datensätze hat. Beispiel: Benutzer A hat eine gebuchte Verkaufsrechnung an einen Kunden gesendet. Benutzer B kann die E-Mail-Nachricht anzeigen, wenn er sowohl Zugriff auf die Rechnung als auch auf den Kunden hat.
* **Ansicht, wenn Zugriff auf zugehörige Datensätze** – Der Benutzer kann E-Mail-Nachrichten anzeigen, die von anderen Personen gesendet wurden, wenn der Benutzer Zugriff auf mindestens einen Datensatz hat, der sich auf den gesendeten Datensatz bezieht. Beispiel: Benutzer A hat eine gebuchte Verkaufsrechnung an einen Kunden gesendet. Benutzer B kann die E-Mail-Nachricht anzeigen, wenn er entweder Zugriff auf die Rechnung oder auf den Kunden hat.

> [!NOTE]
> Wenn Sie das Feld **Benutzer-ID** leer lassen und dann die Aktion **E-Mail-Anzeigerichtlinie** auswählen, gilt die Anzeigerichtlinie für alle Benutzer.

## <a name="specify-how-many-messages-an-account-can-send-per-minute"></a>Geben Sie an, wie viele Nachrichten ein Konto pro Minute senden kann

Einige E-Mail-Anbieter (ISP) begrenzen die Anzahl der E-Mail-Nachrichten, die ein E-Mail-Konto auf einmal oder innerhalb eines bestimmten Zeitraums (oder beides) senden kann. Diese als *E-Mail-Drosselung* bekannte Praxis hilft ISP dabei, den Datenverkehr auf ihren Servern zu kontrollieren und Spam zu verhindern. Wenn ein E-Mail-Konto die Obergrenze überschreitet, kann der ISP die Nachrichten blockieren. Um sicherzustellen, dass die Anzahl der Nachrichten, die Sie von [!INCLUDE [prod_short](includes/prod_short.md)] versenden, die Obergrenze Ihres ISP einhält, geben Sie für jedes Ihrer E-Mail-Konten die Obergrenze an.

Das Standardobergrenze für die Kontotypen Microsoft 365 und „Aktueller Benutzer“ ist 30, was der von Exchange Online festgelegten Obergrenze entspricht.

Es gibt zwei Möglichkeiten, die Obergrenze anzugeben:

* Wenn Sie bei der Erstellung eines neuen Kontos den Leitfaden für die unterstützte Einrichtung von E-Mails verwenden, geben Sie die Obergrenze im Feld **Ratenbegrenzung pro Minute** an.
* Für bereits bestehende E-Mail-Konten geben Sie die Obergrenze im Feld **E-Mail-Ratenbegrenzung** an.

## <a name="set-up-reusable-email-texts-and-layouts"></a>Wiederverwendbare E-Mail-Texte und -Layouts einrichten

Sie können Berichte verwenden, um wichtige Informationen aus Verkaufs-, Kauf- und Service-Dokumenten in Texte für E-Mails einzubinden. Berichtslayouts definieren den Stil und den Inhalt des Textes in der E-Mail. Der Inhalt kann Texte wie eine Begrüßung oder Anweisungen enthalten, die den Dokumenteninformationen vorangestellt sind. In diesem Verfahren wird beschrieben, wie Sie den Bericht **Verkaufsrechnung** für gebuchte Verkaufsrechnungen einrichten, aber der Prozess ist für andere Berichte ähnlich.

> [!NOTE]
> Um das Layout zum Erstellen von Inhalten für E-Mail-Nachrichten zu verwenden, müssen Sie den Word-Dateityp für Ihr Layout verwenden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Berichtsauswahlen - Verkäufe** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Berichts-Auswahl - Verkauf** unter **Verwendung** wählen Sie **Rechnung**.
3. In einer neuen Zeile im Feld **Berichts-ID** wählen Sie beispielsweise Standardbericht 1306.
4. Wählen Sie das Kontrollkästchen **Für E-Mail-Text verwenden** aus.
5. Wählen Sie das Feld **E-Mail-Text-Layout-Beschreibung** und ein Layout aus der Liste aus.
6. Wählen Sie das Layout auf der Seite **Benutzerdefinierte Berichtslayouts** und anschließend die Aktion **Layout exportieren** aus, um das Layout, auf dem der E-Mail-Text basiert, anzuzeigen oder zu bearbeiten. Wenn Sie das Layout anpassen, verwenden Sie die Aktion **Layout importieren**, um das neue Layout hochzuladen.
    > [!NOTE]
    > Erstellen Sie zum Anpassen eines Standardberichtslayouts – wie 1306 – eine Kopie des Berichts. [!INCLUDE [prod_short](includes/prod_short.md)] hilft Ihnen beim Erstellen einer Kopie, wenn Sie ein benutzerdefiniertes Layout für einen Standardbericht importieren. Dem Namen Ihres neuen benutzerdefinierten Berichtslayouts wird das Präfix „Kopie von“ vorangestellt.
7. Wenn Sie Kunden die Verwendung eines Zahlungsdienstes wie PayPal ermöglichen möchten, müssen Sie den Dienst einrichten. Anschließend werden die PayPal-Informationen und der Link in den E-Mail-Text eingefügt. Weitere Informationen finden Sie unter [Aktivieren Sie Debitoren-Zahlung durch PayPal](sales-how-enable-payment-service-extensions.md)
8. Wählen Sie die Schaltfläche **OK** aus.

Wenn Sie jetzt beispielsweise die Aktion **Senden** auf der Seite **Gebuchte Verkaufsrechnung** auswählen, enthält der E-Mail-Text die Beleginformationen 1306 des Berichts, der vom formatierten Standardtext entsprechend dem Berichtslayout stammt, das Sie in Schritt 5 ausgewählt haben.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Eine Ersatz-Absenderadresse für ausgehende E-Mail-Nachrichten verwenden

Wenn Sie die SMTP Connector-Erweiterung verwenden, können Sie jedoch die **Senden Als** oder **Senden im Auftrag von** Funktionen von Microsoft Exchange zum Ändern der Absenderadresse für ausgehende Nachrichten verwenden. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet das SMTP- Konto zur Authentifizierung bei Exchange, ersetzt jedoch entweder die Absenderadresse durch die von Ihnen angegebene oder ändert sie durch „Im Namen von“.

Wenn Sie ein Konto einrichten und die Funktionen „Senden als“ oder „Senden im Auftrag“ von Exchange verwenden möchten, können Sie im Feld **Absendertyp** die Option **Bestimmter Benutzer** auswählen.

Alternativ können Sie **Aktueller Benutzer** auswählen, um Benutzern das Senden von Nachrichten über den SMTP-Connector zu ermöglichen. Die Nachricht scheint von dem E-Mail-Konto gesendet zu werden, das im Feld „Kontakt-E-Mail“ auf der Benutzerkarte für den Benutzer angegeben ist, als der sie angemeldet sind. Es funktioniert jedoch ähnlich wie die Funktion „Senden als“ und wird von dem Konto gesendet, das in der Einrichtung von SMTP Connector angegeben ist.

Im Folgenden finden Sie Beispiele für die Verwendung von Senden als und Senden im Namen von [!INCLUDE[prod_short](includes/prod_short.md)]:

* Vielleicht möchten Sie, dass die Bestellungen oder Verkaufsaufträge, die Sie an Kreditoren oder Debitoren senden, so aussehen, als kämen sie von einer _noreply@yourcompanyname.com_-Adresse.
* Wenn Ihr Workflow eine Genehmigungsanfrage per E-Mail unter Verwendung der E-Mail-Adresse des Antragstellenden sendet.

> [!Note]
> Sie können nur ein Konto verwenden, um Absenderadressen zu ersetzen. Das heißt, Sie können nicht eine Ersatzadresse für Einkaufsprozesse und eine andere für Verkaufsprozesse haben.

<!--
### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a>Belegsendeprofile einrichten

Sie können Zeit sparen, indem Sie für jeden Ihrer Kunden eine bevorzugte Methode zum Senden von Verkaufsbelegen einrichten. Sie müssen nicht jedes Mal, wenn Sie ein Dokument senden, eine Sendeoption auswählen, z. B. ob das Dokument per E-Mail oder als elektronisches Dokument gesendet werden soll. Weitere Informationen finden Sie unter [Einrichten von Belegsendeprofilen](sales-how-setup-document-send-profiles.md).

## <a name="optional-set-up-email-logging-in-exchange-online"></a>Optional: E-Mail-Protokollierung in Exchange Online einrichten

Nutzen Sie die Kommunikation zwischen Vertriebsmitarbeitern und Ihren bestehenden oder potenziellen Kunden optimal. Sie können den E-Mail-Austausch verfolgen und ihn dann in umsetzbare Verkaufsmöglichkeiten verwandeln. Erfahren Sie mehr unter [Austausch von E-Mail-Nachrichten zwischen Verkäufern und Kontakten nachverfolgen](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="optional-monitor-email-usage-and-troubleshoot-email-failures-with-telemetry"></a>Optional: Überwachen Sie die E-Mail-Nutzung und beheben Sie E-Mail-Fehler mithilfe von Telemetrie

Administratoren können die Telemetriefunktion in [!INCLUDE[prod_short](includes/prod_short.md)] einschalten, um Daten über Nutzung und Ausfälle verschiedener Funktionen im System abzurufen. Für E-Mails protokollieren wir die folgenden Vorgänge:

- Eine E-Mail wurde erfolgreich gesendet  
- Der Versuch, eine E-Mail zu senden, ist fehlgeschlagen   
- Die Authentifizierung bei einem SMTP-Server war erfolgreich/ist fehlgeschlagen  
- Die Verbindung mit einem SMTP-Server war erfolgreich/ist fehlgeschlagen  

Mithilfe dieser Daten können Sie die E-Mail-Nutzung überwachen und E-Mail-Fehler beheben. Weitere Informationen unter [Analysieren von E-Mail-Telemetrie (Verwaltungsinhalte)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace).  

## <a name="set-up-email-for-business-central-on-premises"></a>E-Mails für Business Central On-Premises einrichten

[!INCLUDE[prod_short](includes/prod_short.md)] lokal kann mit Services integriert werden, die auf Microsoft Azure basieren. Zum Beispiel können Sie Cortana Intelligence für intelligentere Cashflow-Prognosen verwenden, Power BI, um Ihr Geschäft zu visualisieren und Exchange Online zum Versenden von E-Mails. Die Integration mit diesen Diensten basiert auf einer App-Registrierung in Microsoft Entra-ID. Die App-Registrierung bietet Authentifizierungs- und Autorisierungsdienste für die Kommunikation. So verwenden Sie die E-Mail-Funktionen in [!INCLUDE[prod_short](includes/prod_short.md)] lokal, Sie müssen Sie [!INCLUDE[prod_short](includes/prod_short.md)] als App im Azure-Portal registrieren und dann [!INCLUDE[prod_short](includes/prod_short.md)] mit der App-Registrierung verwenden. In den folgenden Abschnitten werden diese Schritte beschrieben.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Eine App-Registrierung für Business Central im Azure-Portal erstellen

Die Schritte zur Registrierung von [!INCLUDE[prod_short](includes/prod_short.md)] im Azure-Portal werden in [Registrieren Sie eine Bewerbung in Microsoft Entra-ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) beschrieben.

> [!NOTE]
> Damit die E-Mail-Funktionen verwendet werden können, muss Ihre App-Registrierung eine mehrinstanzenfähige Konfiguration verwenden.

Die Einstellungen, die für die E-Mail-Funktionen spezifisch sind, sind die delegierten Berechtigungen, die Sie Ihrer App-Registrierung erteilen. In der folgenden Tabelle sind die Mindestberechtigungen aufgeführt.

|API/Berechtigungsname  |Typ  |Beschreibung  |
|---------|---------|---------|
|Microsoft Graph/User.Read |Stellvertretend|Melden Sie sich an und lesen Sie das Benutzerprofil.         |
|Microsoft Graph/Mail.ReadWrite |Stellvertretend|Verfassen Sie eine E-Mail-Nachricht.         |
|Microsoft Graph/Mail.Send|Stellvertretend|E-Mail-Nachricht senden.         |
|Microsoft Graph/offline_access|Stellvertretend|Behalten Sie die Einwilligung zum Datenzugriff bei.|
|Microsoft Graph / Mail.Send.Shared|Stellvertretend|Freigegebenes Postfach|

Wenn Sie SMTP Connector verwenden oder OAuth 2.0 zur Authentifizierung verwenden möchten, unterscheiden sich die Berechtigungen geringfügig. In der folgenden Tabelle sind die Berechtigungen aufgeführt.

|API/Berechtigungsname  |Typ  |Beschreibung  |
|---------|---------|---------|
|Microsoft Graph/offline_access|Stellvertretend|Behalten Sie die Einwilligung zum Datenzugriff bei.|
|Microsoft Graph / openid|Stellvertretend|Melden Sie Benutzer an.|
|Microsoft Graph/User.Read |Stellvertretend|Melden Sie sich an und lesen Sie das Benutzerprofil.         |
|Microsoft Graph / SMTP.Send|Stellvertretend|Senden Sie E-Mails aus Postfächern mit SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Stellvertretend|Melden Sie sich an und lesen Sie das Benutzerprofil.         |

Wenn Sie Ihre App-Registrierung erstellen, müssen Sie folgende Informationen angeben. Sie benötigen sie, um eine Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] herzustellen, um Ihre App zu registrieren.
 
* Anwendungs-ID (Client-ID)
* URI umleiten (optional)
* Geheimer Clientschlüssel

Allgemeine Informationen zum Registrieren einer Anwendung erhalten Sie unter [Schnellstart: Anwendung bei der Microsoft-Identitätsplattform registrieren](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Wenn Sie Probleme haben, das SMTP-Protokoll zum Senden von E-Mails zu verwenden, nachdem Sie eine Verbindung zu [!INCLUDE[prod_short](includes/prod_short.md)] hergestellt haben, kann daran liegen, dass SMTP AUTH für Ihren Mandanten nicht aktiviert ist. Wir empfehlen, stattdessen die E-Mail-Konnektoren Microsoft 365 und aktuelle Benutzer zu verwenden, da diese Microsoft Graph Mail-APIs verwenden. Wenn Sie jedoch das SMTP-Protokoll verwenden müssen, können Sie SMTP AUTH aktivieren. Weitere Informationen finden Sie unter [Aktivieren oder deaktivieren Sie die SMTP-Übermittlung für authentifizierte Clients (SMTP AUTH) in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect--to-your-app-registration"></a>[!INCLUDE[prod_short](includes/prod_short.md)] mit Ihrer App-Anmeldung verbinden

Nachdem Sie Ihre Anwendung im Azure-Portal registriert haben, verwenden Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Seite **E-Mail-Anwendung Microsoft Entra-ID-Registrierung**, um die Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] herzustellen.

1. Wählen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun") aus, geben Sie **Microsoft Entra-ID-Registrierung der E-Mail-Anwendung** ein, und wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Wenn Sie zum ersten Mal eine Verbindung herstellen, können Sie alternativ die unterstützte Einrichtung **E-Mail einrichten** verwenden. In diesem Fall enthält die Anleitung auch die Seite „Microsoft Entra-ID-Registrierung per E-Mail-Anwendung“, auf der Sie die Informationen für die Verbindung mit Ihrer App-Registrierung hinzufügen können. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Microsoft Entra ID, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant)** or **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Microsoft Entra ID, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
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
[Belege per E-Mail senden](ui-how-send-documents-email.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] über Erweiterungen](ui-extensions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] als Ihr Unternehmenspostfach in Outlook verwenden](admin-outlook.md)  
[Abrufen von [!INCLUDE[prod_short](includes/prod_short.md)] auf meinem mobilen Gerät](install-mobile-app.md)   
[Abrufen von [!INCLUDE[prod_short](includes/prod_short.md)] auf meinem mobilen Gerät](install-mobile-app.md)   
[Analysieren von E-Mail-Telemetrie (Verwaltungsinhalte)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
