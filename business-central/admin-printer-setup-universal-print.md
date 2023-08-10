---
title: Drucker für Universal Print einrichten
description: 'Erfahren Sie, wie Sie Universal Print verwenden können, um Cloud-Druck in Business Central bereitzustellen.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---

# <a name="set-up-universal-print-printers"></a>Drucker für Universal Print einrichten

Universal Print ist ein auf Microsoft 365 basierender Abonnement-Service, der vollständig über Microsoft Azure ausgeführt wird. Sie erhalten eine zentralisierte Druckerverwaltung über das Universal Print-Portal. [!INCLUDE[prod_short](includes/prod_short.md)] stellt in Universal Print eingerichtete Drucker Clientbenutzern über die Erweiterung **Universal Print-Integration** zur Verfügung.

![Universal Print Einrichtung.](media/Universal-Print-arch.png)

Für die vollständige Einrichtung müssen Sie in Microsoft Azure über das [Azure-Portal](https://portal.azure.com) und in [!INCLUDE[prod_short](includes/prod_short.md)] arbeiten. Die Einrichtung ist wie in diesem Artikel beschrieben in zwei Hauptaufgaben unterteilt:

1. Richten Sie Universal Print in Microsoft Azure ein und fügen Sie die Drucker, die Sie in Business Central verwenden möchte, in einer Druckfreigabe hinzu. Navigieren Sie zu [diesem Abschnitt](#set-up-universal-print-and-printers-in-microsoft-azure).
2. Fügen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Drucker aus den Druckfreigaben in Universal Print hinzu. Wechseln Sie zu [diesem Abschnitt](#add-printers-in-business-central-online) für online oder [hierher](#add-printers-in-business-central-on-premises) für lokal.

## <a name="prerequisites"></a>Voraussetzungen

- Unterstützte Drucker

  [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt dieselben Drucker wie Universal Print, die entweder Universal Print-kompatible oder nicht kompatible Drucker sein können. Nicht kompatible Drucker können nicht direkt mit Universal Print kommunizieren. Daher benötigen sie eine zusätzliche Anschlusssoftware, die von Universal Print bereitgestellt wird. Einige ältere Drucker werden möglicherweise nicht unterstützt. 

- Universal Print:

  - Ein Universal Print-Abonnement/eine Lizenz für Ihre Organisation

    Erfahren Sie mehr unter [Universal Print lizenzieren](/universal-print/fundamentals/universal-print-license).

  - Sie verfügen über die Rollen **Druckeradministrator** (oder Druckermanager) und **Globaler Administrator** in Azure.

    Um Universal Print verwalten zu können, muss Ihr Konto über die Rollen **Druckeradministrator** (oder Druckermanager) und **Globaler Administrator** in Azure AD verfügen. Diese Rollen werden nur für die Verwaltung von Universal Print benötigt. Es ist nicht erforderlich, dass Personen sie Einrichten und die Drucker von [!INCLUDE[prod_short](includes/prod_short.md)].

- [!INCLUDE[prod_short](includes/prod_short.md)] online and lokal:

  - [!INCLUDE[prod_short](includes/prod_short.md)] 2021 Veröffentlichungszyklus 1 oder später.
  - Die Erweiterung **Universal Print-Integration** ist installiert.

    Diese Erweiterung wird standardmäßig als Teil von [!INCLUDE[prod_short](includes/prod_short.md)] online und vor Ort veröffentlicht und installiert. Sie können überprüfen, ob es auf der Seite **Erweiterungsverwaltung** installiert ist. Weitere Informationen erhalten Sie unter [Installieren und Deinstallieren von Erweiterungen in Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] nur vor Ort:
  - Azure Active Directory (AD) oder NavUserPassword-Authentifizierung ist konfiguriert.
    > [!NOTE]
    >  Die Universal Print-Erweiterung unterstützt keine Service-to-Service (S2S)-Authentifizierung. Sie erfordert einen angemeldeten Benutzer, um Druckaufträge über die Graph-API an den universellen Druckdienst zu senden.
  - Eine Anwendung für Business Central ist in Ihrem Azure AD-Mandanten und [!INCLUDE[prod_short](includes/prod_short.md)] registriert.

    Wie andere Azure-Dienste, mit denen [!INCLUDE[prod_short](includes/prod_short.md)] arbeitet, benötigt Universal Print eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)] in Azure AD. Die App-Registrierung bietet Authentifizierungs- und Autorisierungsdienste zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Universal Print.

    Ihre Bereitstellung verwendet möglicherweise bereits eine App-Registrierung für andere Azure-Dienste, z. B. Power BI. Wenn ja, verwenden Sie auch die vorhandene App-Registrierung für Universal Print, anstatt eine neue hinzuzufügen. In diesem Fall müssen Sie lediglich die App-Registrierung so ändern, dass sie die relevanten Druckberechtigungen für die Microsoft Graph-API enthält: **PrinterShare.ReadBasic.All**, **PrintJob.Create** und **PrintJob.ReadBasic**. 

    Befolgen Sie die unter [Registrieren Sie eine Anwendung in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) beschriebenen Schritte, um eine App zu registrieren und die richtigen Berechtigungen festzulegen.

## <a name="set-up-universal-print-and-printers-in-microsoft-azure"></a>Universal Print und Drucker in Microsoft Azure einrichten

Bevor Sie mit der Verwaltung von Universal Print-Druckern in Business Central beginnen können, müssen Sie Aufgaben ausführen, um Universal Print in Azure mit den gewünschten Druckern zu verwenden.

Ausführliche Anweisungen zum Einrichten finden Sie unter [Erste Schritte: Universal Print einrichten](/universal-print/fundamentals/universal-print-getting-started) in der Universal Print-Dokumentation. Hier ist eine Übersicht über die Schritte, die Sie ausführen müssen. Die meisten dieser Schritte werden im Azure-Portal ausgeführt.

1. Weisen Sie sich und anderen Benutzern Universal Print-Lizenzen zu.

    Wie Sie die Lizenz zuweisen, hängt davon ab, ob Sie sich online oder lokal in Business Central integrieren.

    - Mit [!INCLUDE[prod_short](includes/prod_short.md)] online weisen Sie Lizenzen über das Microsoft 365 Admin-Center zu.

      Weitere Informationen finden Sie unter [Microsoft Admin Center-Hilfe – Benutzern Lizenzen zuweisen](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Mit [!INCLUDE[prod_short](includes/prod_short.md)]-On-premises weisen Sie Lizenzen in Ihrem Azure-Mandanten über das Azure-Portal zu.

      Weitere Informationen finden Sie unter [Azure Directory – Lizenzen im Azure Active Directory-Portal zuweisen oder entfernen](/azure/active-directory/fundamentals/license-users-groups).

2. Installieren Sie den Universal Print-Konnektor zum Registrieren von Druckern, die nicht direkt mit Universal Print kommunizieren können.

    Die meisten Drucker auf dem Markt können nicht nicht direkt mit Universal Print kommunizieren, deshalb müssen Sie den Universal Print-Konnektor installieren. Weitere Informationen finden Sie unter [Installieren des Universal Print-Konnektors](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrieren Sie Ihre Drucker in Universal Print.

    Durch die Registrierung eines Druckers wird Universal Printer auf den Drucker aufmerksam.

    - Befolgen Sie bei Druckern, die direkt mit Universal Print kommunizieren können, die vom Druckerhersteller angegebenen Schritte.

    - Registrieren Sie bei anderen Druckern die Drucker über den Universal Print-Konnektor. 

      Weitere Informationen finden Sie unter [Druckerregistrierung](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Druckereigenschaften ändern (optional)

    Nachdem ein Drucker registriert wurde, können Sie Druckereigenschaften wie Standardeinstellungen anzeigen und ändern.

    Weitere Informationen finden Sie unter [Verwalten der Druckereinstellungen über das Universal Print-Portal](/universal-print/portal/configure-printer-settings).

5. Teilen Sie die Drucker mit Benutzern.

    Jeder Drucker, den Sie in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchten, muss in Universal Print einer *Druckerfreigabe* hinzugefügt werden. Jeder Benutzer, der Zugriff auf den Drucker benötigt, muss als Mitglied der Druckerfreigabe hinzugefügt werden. Weitere Informationen finden Sie unter [Drucker freigeben](/universal-print/portal/share-printers).

    > [!TIP]
    > Sie können Benutzer später jederzeit hinzufügen oder entfernen. Weitere Informationen finden Sie unter [Druckerberechtigungen](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).

6. Aktivieren Sie die Dokumentkonvertierung.

    Universal Print rendert Inhalte für den Druck im XPS-Format. Einige ältere marktübliche Drucker unterstützen das Rendern von XPS-Inhalten in vielen Fällen nicht &mdash;, sondern nur das PDF-Format. Das Drucken auf diesen Druckern schlägt fehl, es sei denn, Universal Print ist so eingerichtet, dass Dokumente in das vom Drucker unterstützte Format konvertiert werden.

    Erfahren Sie mehr unter[ Übersicht über die Dokumentkonvertierung ](/universal-print/portal/document-conversion).

Jetzt können Sie die Drucker [!INCLUDE[prod_short](includes/prod_short.md)] hinzufügen, Standarddrucker für Berichte einrichten und drucken.  

## <a name="add-printers-in-business-central-online"></a>Drucker in Business Central Online hinzufügen

Nachdem die Drucker in Universal Print eingerichtet und freigegeben wurden, können Sie sie zur Verwendung in [!INCLUDE[prod_short](includes/prod_short.md)] hinzufügen. Es gibt zwei Möglichkeiten, Universal Print-Drucker hinzuzufügen. Sie können die Drucker auf einmal oder einzeln hinzufügen.

Wenn Sie Drucker einzeln hinzufügen, können Sie denselben Universal Print-Drucker in [!INCLUDE[prod_short](includes/prod_short.md)] mehrmals einrichten. Anschließend können Sie für jeden hinzugefügten Drucker die Druckeinstellungen wie Papierfach, Größe und Ausrichtung ändern. Auf diese Weise können Sie Drucker für verschiedene Berichte und Dokumente einrichten, für die besondere Ausgabeanforderungen gelten.

> [!NOTE]
> Verwenden Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal? Wenn ja, gehen Sie zum [nächsten Abschnitt](#add-printers-in-business-central-on-premises), die erstmalige Einrichtung ist etwas anders.  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Klicken Sie auf **Universal Print**, und wählen Sie dann eine der folgenden Optionen aus:

   - **Alle Universal Print-Drucker hinzufügen**, um alle Drucker hinzuzufügen, die noch nicht hinzugefügt wurden. Sie können diese Option auch dann verwenden, wenn bereits Drucker hinzugefügt wurden.
   - **Universal Print-Drucker hinzufügen**, um einen bestimmten Drucker hinzuzufügen.  
3. Folgen Sie den Anweisungen auf dem Bildschirm.

    - Wenn Sie **Alle Universal Print-Drucker hinzufügen** auswählen, beginnt die Einrichtung **Universal Print-Drucker hinzufügen**. 

    - Wenn Sie **Universal Print-Drucker hinzufügen** auswählen, erscheint die Seite **Universal Print-Drucker – Einstellungen**. Füllen Sie das Feld **Name** aus, und wählen Sie dann die Auslassungspunkte **...** neben dem Feld **Druckfreigabe in Universal Print** aus, um die Druckerfreigabe mit dem Universal Print-Drucker auszuwählen. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Nachdem ein Drucker hinzugefügt wurde, können Sie seine Einstellungen über **Druckerverwaltung** anzeigen und ändern. Wählen Sie einfach den Drucker und dann **Druckereinstellungen bearbeiten** aus.

## <a name="add-printers-in-business-central-on-premises"></a>Drucker in Business Central lokal hinzufügen

<!--With [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, unlike online, users aren't automatically authenticated with the registered app in Azure used for the Universal Print service. So, before any Business Central user (including admins) can add or even use Universal Print printers, they'll have to authenticate with the Azure app and grant access to the Universal Print service. The following procedure describes how to initiate this authentication flow. Each user typically only has to do this task once.-->

Bevor ein Benutzer Universal Print-Drucker zu Business Central hinzufügen oder verwenden kann, muss er den Zugriff auf die von Universal Print verwendeten Azure-Dienste autorisieren und ihm die Berechtigung für Daten und Vorgänge erteilen, z. B.:

- Anmelden und lesen des Benutzerprofils
- Lesen grundlegender Druckauftragsinformationen
- Erstellen von Druckaufträgen

Dies geschieht in der Regel beim ersten Herstellen einer Verbindung mit der für Universal Print verwendeten in Azure registrierten App. In Business Central Online erfolgt dieser Autorisierungsfluss nahtlos, ohne Benutzerinteraktion. Aber Business Central lokal funktioniert anders. Es erfordert, dass Sie oder jeder andere Benutzer, der Universal Print-Drucker verwenden möchte, den Authentifizierungsablauf initiiert&mdash;normalerweise nur einmal. Die direkteste Methode wird in den folgenden Schritten beschrieben. Ein weniger direkter Weg ist die Verbindung mit einem anderen integrierten Dienst, der dieselbe registrierte Azure-App verwendet, wie Power BI oder OneDrive. Jeder Benutzer muss diese Aufgabe normalerweise nur einmal ausführen.

> [!NOTE]
> Wenn Sie ein Administrator sind, empfehlen wir Ihnen, diese Aufgabe vor anderen Benutzern abzuschließen. Informieren Sie anschließend die Benutzer, die Universal Print-Drucker verwenden müssen, wie dies zu tun ist. Wenn die von Azure registrierte App für Universal Print die Zustimmung des Administrators für API-Berechtigungen erfordert, ist es einfacher, wenn Sie die Zustimmung im Namen der Organisation erteilen. Sie können die Administratoreinwilligung über das Azure-Portal erteilen, oder wenn Sie die folgenden Schritte ausführen. 

<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->
### <a name="connect-to-universal-print-for-the-first-time"></a>Erstmaliges Herstellen einer Verbindung mit Universal Print

Führen Sie diese Schritte aus, um zum ersten Mal eine Verbindung mit dem Universal Print-Dienst herzustellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Universal Print** > **Alle Universal Print-Drucker hinzufügen**, um den **Universal Print-Drucker hinzufügen**-Assisted Setup Guide (Assistenten).
3. Befolgen Sie die Anweisungen auf dem Bildschirm, bis Sie zur Seite AZURE ACTIVE DIRECTORY-SERVICEBERECHTIGUNGEN gelangen.

    <!--The AZURE ACTIVE DIRECTORY SERVICE PERMISSIONS page appears. You'll be prompted to give consent to Azure Services. You'll be lead through the process of verifying your Azure AD setup, checking your Universal Print license, and then adding the printers.-->

   ![Zeigt die Seite AZURE ACTIVE DIRECTORY-SERVICEBERECHTIGUNGEN](media/azure-ad-services-permissions.png "Zeigt die Seite AZURE ACTIVE DIRECTORY-SERVICEBERECHTIGUNGEN")

4. Wählen Sie den Link **Azure-Dienste autorisieren** aus.

   1. Wenn die Seite **Berechtigung angefordert** angezeigt wird, lesen Sie sie sorgfältig durch und wählen Sie **Akzeptieren**, um zuzustimmen und fortzufahren. Wenn Sie als Administrator arbeiten, können Sie **Zustimmung im Namen der Organisation** auswählen, wenn Sie für alle Benutzer zustimmen möchten.

      ![Zeigt die Seite Azure-Anforderungsberechtigungen](media/azure-ad-permissions-requested.png "Seite Azure-Anforderungsberechtigungen") an.

   2. Falls Sie dazu aufgefordert werden, melden Sie sich mit Ihrem Namen und Kennwort an.

5. Wenn die Autorisierung erfolgreich abgeschlossen wurde, kehren Sie zur Seite **Universal Print-Drucker hinzufügen** zurück. Wählen Sie **Weiter** > **Beenden**, um die Einrichtung abzuschließen.

Nachdem ein Drucker hinzugefügt wurde, können Sie seine Einstellungen über **Druckerverwaltung** anzeigen und ändern. Wählen Sie einfach den Drucker und dann **Druckereinstellungen bearbeiten** aus.

Sobald Sie die Erstanmeldung abgeschlossen haben, können Sie die Universal Print-Drucker zum Drucken von Berichten und anderen Druckaufträgen verwenden. Weitere Informationen finden Sie unter [Drucken eines Berichts](ui-work-report.md#PrintReport). Wenn Sie Drucker hinzufügen, entfernen oder ändern möchten, kehren Sie einfach zurück zur Seite **Druckverwaltung** zurück und wählen Sie **Universal Print**.

## <a name="common-problems-and-resolutions"></a>Häufige Probleme und Lösungen

In diesem Abschnitt erfahren Sie mehr über die häufigsten Probleme, auf die Benutzer möglicherweise stoßen, wenn sie versuchen, Universal Print-Drucker einzurichten oder zu verwenden.

### <a name="you-dont-have-access-to-the-printer-your-printer"></a>Sie haben keinen Zugriff auf den Drucker \<your-printer\>.

Wenn ein Benutzer diese Meldung erhält, wenn er versucht, einen Beleg auf einem Universal Print-Drucker zu drucken, kann dies durch eine der folgenden Bedingungen verursacht werden:

- Dem Benutzer ist keine Universal Print-Lizenz für sein Microsoft 365 - oder Azure Active AD-Konto zugewiesen. 
- Der Benutzer wird der Druckerfreigabe in Universal Print nicht zugewiesen.
- (Lokal) Die für Universal Print verwendete Azure-App-Registrierung funktioniert nicht oder wurde kürzlich geändert, seit sich der Benutzer das letzte Mal angemeldet hat.
- (Lokal) Der Benutzer hat sich noch nicht bei der von Azure registrierten App für die Universal Print-App angemeldet und zum ersten Mal zugestimmt.

## <a name="there-was-an-error-fetching-printers-shared-to-you"></a>Fehler beim Abrufen von freigegebenen Druckern.

Wenn ein Benutzer diese Meldung erhält, wenn er versucht, einen Universal Print-Drucker über die Seite **Druckerverwaltung** hinzuzufügen, liegt dies normalerweise daran, dass er sich noch nicht bei der von Azure registrierten App für Universal Printer-App angemeldet und zum ersten Mal zugestimmt hat. 
<!--
### <a name="troubleshooting"></a>Troubleshooting

#### <a name="you-dont-see-the-a-printer-in-the"></a>You don't see the a printer in the

The printer is not shared in Universal Print.

### <a name="you-get-an-error-when-tryong-to-add-all-or-a-single-printer"></a>You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## <a name="could-not-upload-the-document-to-print-job-50"></a>Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps




-->

## <a name="next-steps"></a>Nächste Schritte
[Standarddrucker einrichten](ui-specify-printer-selection-reports.md)

## <a name="see-also"></a>Siehe auch

[Übersicht der Drucker](admin-printer-setup-overview.md)  
[E-Mail-Drucker einrichten](admin-printer-setup-email.md)
[Einen Bericht drucken](ui-work-report.md#PrintReport)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ausführen von Stapelverarbeitungen](ui-how-run-batch-jobs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
