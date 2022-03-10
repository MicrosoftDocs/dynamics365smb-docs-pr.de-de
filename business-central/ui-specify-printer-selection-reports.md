---
title: Einrichten von Druckern
description: Informieren Sie sich über die Einrichtung von Druckern, die Sie für Berichte und Belege verwenden können, und über die verschiedenen Druckfunktionen, die Ihnen in Business Central zur Verfügung stehen.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 8900, 9018, 9022
ms.date: 06/24/2021
ms.author: jswymer
ms.openlocfilehash: 317e90976aed760f55fc7122483377e8df11c906
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335144"
---
# <a name="set-up-printers"></a>Einrichten von Druckern

Das Drucken von Dokumenten und Berichten aus [!INCLUDE[prod_short](includes/prod_short.md)] ist eine wichtige Aufgabe für Geschäftsanwender. Benutzer möchten normalerweise Druckaufträge direkt an einen der Drucker Ihres Unternehmens senden, egal welchen [!INCLUDE[prod_short](includes/prod_short.md)] Client oder welche App sie verwenden. Da [!INCLUDE[prod_short](includes/prod_short.md)] Online ein Cloud-Dienst ist, kann er der lokale Drucker, die mit den Geräten der Benutzer verbunden sind, nicht direkt erreichen, aber eine Verbindung zu Cloud-fähigen Druckern herstellen.

Um Ihre Druckanforderungen zu erfüllen, bietet [!INCLUDE[prod_short](includes/prod_short.md)] folgende Funktionen:

|Funktion|Beschreibung|Webclient| Mobile App|App für Teams|
|-------|-----------|----------|-----------|--------------|
|Universal Print|Universal Print ist eine Druckerverwaltungslösung, die als Cloud-Service von Microsoft erhältlich ist. Mit dieser Funktion können Sie Ihre Drucker in Universal Print einrichten und dann für die Verwendung in [!INCLUDE[prod_short](includes/prod_short.md)] registrieren. Diese Funktion erfordert ein Universal Print-Abonnement und die Erweiterung **Universal Print-Integration**|![Funktioniert online.](media/check.png)|![Funktioniert online.](media/check.png)|![Funktioniert online](media/check.png)|
|E-Mail-Druck|Mit dieser Funktion können Sie E-Mail-fähige Drucker einrichten. [!INCLUDE[prod_short](includes/prod_short.md)] sendet anschließend Druckaufträge unter Verwendung der E-Mail-Adresse des Druckers an einen Drucker. Für diese Funktion sind E-Mail-fähige Drucker und die Erweiterung **E-Mail an Drucker senden** erforderlich.|![Funktioniert online.](media/check.png)|![Funktioniert online](media/check.png)|![Funktioniert online](media/check.png)|
|Browserdruck|Druckaufträge werden von der Druckfunktion des Browsers des Benutzers verarbeitet. Wenn ein Cloud-Drucker nicht installiert und eingerichtet ist oder wenn ein installierter Drucker ausfällt, werden beim Drucken standardmäßig die Druckoptionen des Browsers verwendet. Das Feld **Drucker** auf der Berichtsanforderungsseite zeigt *(Vom Browser gehandhabt)* an.|![Funktioniert online](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt auch benutzerdefinierte Druckererweiterungen, die noch mehr Druckfunktionen hinzufügen. Wenn also benutzerdefinierte Druckererweiterungen installiert sind, enthält Ihre Anwendung möglicherweise Druckfunktionen, die in diesem Artikel nicht beschrieben werden. 

## <a name="set-up-universal-print"></a>Universal Print einrichten

Universal Print ist ein auf Microsoft 365 basierender Abonnement-Service, der vollständig über Microsoft Azure ausgeführt wird. Sie erhalten eine zentralisierte Druckerverwaltung über das Universal Print-Portal. [!INCLUDE[prod_short](includes/prod_short.md)] stellt in Universal Print eingerichtete Drucker Clientbenutzern über die Erweiterung **Universal Print-Integration** zur Verfügung.

![Universal Print Einrichtung.](media/Universal-Print-arch.png)

Für die vollständige Einrichtung müssen Sie in Microsoft Azure über das [Azure-Portal](https://portal.azure.com) und in [!INCLUDE[prod_short](includes/prod_short.md)] arbeiten.

### <a name="supported-printers"></a>Unterstützte Drucker

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt dieselben Drucker wie Universal Print, die entweder Universal Print-kompatible oder nicht kompatible Drucker sein können. Nicht kompatible Drucker können nicht direkt mit Universal Print kommunizieren. Daher benötigen sie eine zusätzliche Anschlusssoftware, die von Universal Print bereitgestellt wird. Einige ältere Drucker werden möglicherweise nicht unterstützt. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Voraussetzungen

**Für [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] 2021 Veröffentlichungszyklus 1 oder höher
- Die Erweiterung **Universal Print-Integration** ist installiert

    Diese Erweiterung wird standardmäßig als Teil von [!INCLUDE[prod_short](includes/prod_short.md)] online und vor Ort veröffentlicht und installiert.  Sie können überprüfen, ob es auf der Seite **Erweiterungsverwaltung** installiert ist. Weitere Informationen finden Sie unter [Installieren und Deinstallieren von Erweiterungen in Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)]-On-premises
  - Azure Active Directory (AD) oder NavUserPassword-Authentifizierung ist konfiguriert
  - Eine Anwendung für Business Central ist in Ihrem Azure AD-Mandanten und [!INCLUDE[prod_short](includes/prod_short.md)] registriert

      Wie andere Azure-Dienste, mit denen [!INCLUDE[prod_short](includes/prod_short.md)] arbeitet, benötigt Universal Print eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)] in Azure Active Directory (Azure AD). Die App-Registrierung bietet Authentifizierungs- und Autorisierungsdienste zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und Universal Print.

      Ihre Bereitstellung verwendet möglicherweise bereits eine App-Registrierung für andere Azure-Dienste, z. B. Power BI. Wenn ja, verwenden Sie auch die vorhandene App-Registrierung für Universal Print, anstatt eine neue hinzuzufügen. In diesem Fall müssen Sie lediglich die App-Registrierung so ändern, dass sie die relevanten Druckberechtigungen für die Microsoft Graph-API enthält.

      Befolgen Sie die unter [Registrieren Sie eine Anwendung in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) beschriebenen Schritte, um eine App zu registrieren und die richtigen Berechtigungen festzulegen.

**Für Universal Print**

- Ein Universal Print-Abonnement/eine Lizenz für Ihre Organisation

    Weitere Informationen finden Sie unter [Universal Print lizenzieren](/universal-print/fundamentals/universal-print-license).

- Sie verfügen über die Rollen **Druckerverwaltung** und **Globaler Administrator** in Azure.

    Um Universal Print verwalten zu können, muss Ihr Konto über die Rollen **Druckerverwaltung** und **Globaler Administrator** in Azure AD verfügen. Diese Rollen werden nur für die Verwaltung von Universal Print benötigt. Benutzer müssen die Drucker von [!INCLUDE[prod_short](includes/prod_short.md)] nicht verwenden.

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Universal Print einrichten und Drucker in Microsoft Azure hinzufügen

Bevor Sie mit der Verwaltung von Universal Print-Druckern in Business Central beginnen können, müssen Sie einige Aufgaben ausführen, um Universal Print in Azure mit den gewünschten Druckern zum Laufen zu bringen.

Ausführliche Anweisungen zum Einrichten finden Sie unter [Erste Schritte: Universal Print einrichten](/universal-print/fundamentals/universal-print-getting-started) in der Universal Print-Dokumentation. Hier ist eine Übersicht über die Schritte, die Sie ausführen müssen. Die meisten dieser Schritte werden im Azure-Portal ausgeführt.

1. Weisen Sie sich und anderen Benutzern Universal Print-Lizenzen zu.

    Wie Sie die Lizenz zuweisen, hängt davon ab, ob Sie sich online oder lokal in Business Central integrieren.

    - Mit [!INCLUDE[prod_short](includes/prod_short.md)] online weisen Sie Lizenzen über das Microsoft 365 Admin-Center zu.

      Weitere Informationen finden Sie unter [Microsoft Admin Center-Hilfe – Benutzern Lizenzen zuweisen](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Mit [!INCLUDE[prod_short](includes/prod_short.md)]-On-premises weisen Sie Lizenzen in Ihrem Azure-Mandanten über das Azure-Portal zu.

      Weitere Informationen finden Sie unter [Azure Directory – Lizenzen im Azure Active Directory-Portal zuweisen oder entfernen](/azure/active-directory/fundamentals/license-users-groups).

2. Installieren Sie den Universal Print-Konnektor zum Registrieren von Druckern, die nicht direkt mit Universal Print kommunizieren können.

    Die meisten marktüblichen Drucker können nicht direkt mit Universal Print kommunizieren. Sie müssen den Universal Print-Konnektor für diese Drucker installieren. Weitere Informationen finden Sie unter [Installieren des Universal Print-Konnektors](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrieren Sie Ihre Drucker in Universal Print.

    Durch die Registrierung eines Druckers wird Universal Printer auf den Drucker aufmerksam.

    - Befolgen Sie bei Druckern, die direkt mit Universal Print kommunizieren können, die vom Druckerhersteller angegebenen Schritte.

    - Registrieren Sie bei anderen Druckern die Drucker über den Universal Print-Konnektor. 

      Weitere Informationen finden Sie unter [Druckerregistrierung](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Druckereigenschaften ändern (optional)

    Nachdem ein Drucker registriert wurde, können Sie Druckereigenschaften wie Standardeinstellungen anzeigen und ändern.

    Weitere Informationen finden Sie unter [Verwalten der Druckereinstellungen über das Universal Print-Portal](/universal-print/portal/configure-printer-settings).

5. Teilen Sie die Drucker.

    Jeder Drucker, in dem Sie [!INCLUDE[prod_short](includes/prod_short.md)] verwenden möchten, muss in Universal Print geteilt werden.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Weitere Informationen finden Sie unter [Drucker freigeben](/universal-print/portal/share-printers).

6. Geben Sie den Benutzern die Berechtigung für freigegebene Drucker.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Weitere Informationen finden Sie unter [Druckerberechtigungen](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Aktivieren Sie die Dokumentkonvertierung.

    Universal Print rendert Inhalte für den Druck im XPS-Format. Einige ältere marktübliche Drucker unterstützen das Rendern von XPS-Inhalten in vielen Fällen nicht &mdash;, sondern nur das PDF-Format. Das Drucken auf diesen Druckern schlägt fehl, es sei denn, Universal Print ist so eingerichtet, dass Dokumente in das vom Drucker unterstützte Format konvertiert werden.

    Weitere Informationen finden Sie unter [Dokumentkonvertierung – Übersicht](/universal-print/portal/document-conversion).

Jetzt können Sie die Drucker [!INCLUDE[prod_short](includes/prod_short.md)] hinzufügen, Standarddrucker für Berichte einrichten und drucken.  

### <a name="add-universal-printer-printers-to-business-central"></a>Universal Print-Drucker zu Business Central hinzufügen

Nachdem die Drucker in Universal Print eingerichtet und freigegeben wurden, können Sie sie in Business Central verwenden. Es gibt zwei Möglichkeiten, Universal Print-Drucker hinzuzufügen. Sie können die Drucker auf einmal oder einzeln hinzufügen.

Wenn Sie Drucker einzeln hinzufügen, können Sie denselben Universal Print-Drucker in Business Central mehrmals einrichten. Anschließend können Sie für jeden hinzugefügten Drucker die Druckeinstellungen wie Papierfach, Größe und Ausrichtung ändern. Auf diese Weise können Sie Drucker für verschiedene Berichte und Dokumente einrichten, für die besondere Ausgabeanforderungen gelten.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Klicken Sie auf **Universal Print**, und wählen Sie dann eine der folgenden Optionen aus:

    - **Alle Universal Print-Drucker hinzufügen**, um alle Drucker hinzuzufügen, die noch nicht hinzugefügt wurden. Sie können diese Option auch dann verwenden, wenn bereits Drucker hinzugefügt wurden. 

    - **Universal Print-Drucker hinzufügen**, um einen bestimmten Drucker hinzuzufügen.  
3. Folgen Sie den Anweisungen auf dem Bildschirm.

    - Wenn Sie **Alle Universal Print-Drucker hinzufügen** auswählen, beginnt die Einrichtung **Universal Print-Drucker hinzufügen**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Wenn Sie **Universal Print-Drucker hinzufügen** auswählen, erscheint die Seite **Universal Print-Drucker – Einstellungen**. Füllen Sie das Feld **Name** aus, und wählen Sie dann die Auslassungspunkte **...** neben dem Feld **Druckfreigabe in Universal Print** aus, um den Universal Print-Drucker auszuwählen. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Diese Aktionen überprüfen Ihre Azure AD-Einrichtung (für lokale Anwendungen), ob Sie über eine Universal Print-Lizenz verfügen, und fügen Sie schließlich die Drucker hinzu.

    > [!NOTE]
    > Wenn Sie vor Ort zum ersten Mal eine Verbindung zu Universal Print herstellen, wird die Seite „AZURE ACTIVE DIRECTORY-DIENSTBERECHTIGUNGEN“ angezeigt, und Sie werden aufgefordert, die Zustimmung zu Azure Services zu erteilen. Sie müssen nur einmal Ihre Zustimmung geben.

Nachdem ein Drucker hinzugefügt wurde, können Sie seine Einstellungen über **Druckerverwaltung** anzeigen und ändern. Wählen Sie einfach den Drucker und dann **Druckereinstellungen bearbeiten** aus. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>E-Mail-Druck einrichten

### <a name="prerequisites"></a>Voraussetzungen

- [!INCLUDE[prod_short](includes/prod_short.md)] 2020 Veröffentlichungszyklus 1 oder höher
- Erweiterung **E-Mail an Drucker senden** ist installiert

    Diese Erweiterung wird standardmäßig eingerichtet. Informationen zum Installieren von Erweiterungen finden Sie unter 
- Die E-Mail-Funktionalität ist eingerichtet.

   Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Einen E-Mail-Drucker hinzufügen

Die Seite **Druckerverwaltung** zeigt Drucker an, die eingerichtet sind. Die Seite gibt Ihnen auch Zugriff auf die Seite **Einstellungen** für jeden Drucker, um eine vorhandene Einrichtung zu bearbeiten oder einen neuen Drucker einzurichten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **E-Mail-Druck** und dann **Einen E-Mail-Drucker hinzufügen** aus.
3. Füllen Sie auf der Seite **E-Mail-Drucker-Einstellungen** die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Sie müssen das geeignete Papierformat für einen Drucker manuell auswählen, da keine lokalen Drucker- oder Benutzereinstellungen gespeichert werden können.
    >
    > Beachten Sie, dass die E-Mail-Drucker-Erweiterung standardmäßig auf **A4** Papierformat eingestellt ist, was z. B. in Nordamerika nicht geeignet ist.

### <a name="privacy-notice"></a>Datenschutzhinweis

Wenn Sie die E-Mail-Drucker-Erweiterung verwenden, dann werden alle oder einige Druckaufträge an die E-Mail-Adresse gesendet wie bei der Konfiguration des Druckers angegeben. Wir empfehlen dringend, dass eine eindeutige E-Mail-ID an ein Druckergerät gebunden wird, das nur die offiziellen Dienste des Hardware-Herstellers nutzt, wie z.B. HP ePrint, KonicaMinolta EveryonePrint oder Epson E-Mail-Druck.

Treffen Sie alle erforderlichen Datenschutzvorkehrungen, einschließlich der Sicherstellung, dass die E-Mail-Drucklösung über ordnungsgemäß konfigurierte Berechtigungen, Datenschutzeinstellungen und Aufbewahrungsrichtlinien verfügt. Es liegt in Ihrer Verantwortung, eine korrekte, verifizierte und funktionsfähige E-Mail-Adresse anzugeben. Weitere Informationen finden Sie unter [Microsoft-Datenschutzbestimmungen](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Standarddrucker einrichten

Es gibt verschiedene Möglichkeiten, Drucker einzurichten, die standardmäßig für Druckaufträge verwendet werden. Ein Standarddrucker ist nützlich, wenn Sie mit verschiedenen Berichten arbeiten, die aufgrund ihrer Platzierung in der Firma oder ihrer Ausgabemöglichkeiten unterschiedliche Drucker erfordern.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Einen Drucker als Standarddrucker für alle Druckaufträge festlegen

Auf der Seite **Druckerverwaltung** können Sie einen Drucker als Standarddrucker für alle Druckaufträge einrichten. Sie können den Drucker nur für Sie oder für alle Benutzer als Standard festlegen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Druckerverwaltung** ein, und wählen Sie dann den entsprechenden Link.

    > [!TIP]
    > Sie können auch die Seite **Druckerverwaltung** von der Seite **Druckerauswahl** durch Auswahl von **Druckerverwaltung** öffnen.  
2. Wählen Sie auf der Seite **Druckerverwaltung** einen Drucker aus der Liste, dann **Verwalten** und dann **Als Standarddrucker festlegen** oder **Als Standarddrucker für alle Benutzer festlegen** aus.

> [!NOTE]
> Das Festlegen eines Standarddruckers über die **Druckerverwaltung** fügt einen Eintrag in die **Druckerauswahl** hinzu.

### <a name="set-a-default-printer-for-specific-reports"></a>Den Standarddrucker für bestimmte Berichte festlegen

Auf der Seite **Druckerauswahl** können Sie den Drucker angeben, den ein Bericht standardmäßig verwendet. Standarddrucker werden auf Benutzerkontenbasis festgelegt. Sie können einen Standarddrucker nur für sich selbst, einen anderen Benutzer oder alle Benutzer festlegen.

> [!IMPORTANT]
> Für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort, kann die Seite **Druckerauswahl** nur für Cloud-Drucker verwendet werden, die durch Druckererweiterungen definiert sind, z. B. E-Mail-Druck und Universal Print-Drucker. Sie kann nicht für lokale Drucker verwendet werden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Druckerauswahlen** ein und wählen Sie dann den zugehörigen Link. Alternativ können Sie auf der Seite **Druckerverwaltung** einen Drucker auswählen und dann die Aktion **Druckerauswahl** wählen.
2. Wählen Sie die Aktion **Neu**, um eine Druckerauswahl für einen bestimmten Bericht hinzuzufügen.
3. Füllen Sie die Felder nach Bedarf aus.

Der angegebene Bericht ist jetzt so eingerichtet, dass er standardmäßig auf dem ausgewählten Drucker gedruckt wird.

> [!NOTE]
> Wenn Sie den betreffenden Bericht drucken, können Sie mit dem Feld **Drucken** auf der Anforderungsseite einen anderen auswählen.

> [!NOTE]
> Wenn Sie auf der Seite **Druckerauswahl** keinen Bericht für einen bestimmten Drucker einrichten, wird er auf dem Standarddrucker der Firma gedruckt, wie er auf der Seite **Druckerverwaltung** definiert ist.

Sie oder der Administrator können auch die Seite **Druckerauswahl** verwenden, um andere Varianten des Druckens für Benutzer und Berichte zu definieren. Die folgende Tabelle beschreibt die Kombination von Werten zur Angabe verschiedener Druckeinstellungen für einen Bericht.

|Aktion                                                 |Stellen Sie die folgenden Werte ein                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Einen Bericht für alle Benutzer auf einem bestimmten Drucker ausdrucken |Geben Sie Werte in den Feldern **Berichts-ID** und **Druckername** an und lassen Sie das Feld **Benutzer-ID** leer.|
|Drucken aller Berichte auf einem bestimmten Drucker für einen bestimmten Benutzer|Geben Sie Werte in die Felder **Benutzer-ID** und **Druckername** ein und lassen Sie das Feld **Berichts-ID** leer. Dieser Eintrag macht dasselbe wie die Aktion **Als mein Standarddrucker festlegen** auf der Seite **Druckverwaltung**.|
|Den Standarddrucker für alle Benutzer festlegen|Geben Sie einen Wert in das Feld **Druckername** ein und lassen Sie die Felder **Benutzer-ID** und **Berichts-ID** leer. Dieser Eintrag macht dasselbe wie die Aktion **Als Standarddrucker für alle Benutzer festlegen** auf der Seite **Druckverwaltung**.|
|Drucken eines bestimmten Berichts auf dem Standarddrucker des Benutzers|Geben Sie einen Wert in das Feld **Berichts-ID** ein und lassen Sie die Felder **Druckername** und **Benutzer-ID** leer.|
|Drucken eines bestimmten Berichts auf einem bestimmten Drucker für einen bestimmten Benutzer|Geben Sie Werte in allen drei Feldern an.|

> [!NOTE]
> Spezifischere Druckerauswahlen haben Vorrang vor einer allgemeineren Druckerauswahl. Zum Beispiel hat eine Druckerauswahl, die Werte in den Feldern **Benutzer-ID**, **Berichts-ID** und **Druckername** hat, Vorrang vor einer Druckerauswahl, die leere Einträge in den Feldern **Benutzer-ID** oder **Berichts-ID** hat.

### <a name="choosing-the-printer-when-running-a-report"></a>Auswählen des Druckers beim Ausführen eines Berichts
Anstatt den Standarddrucker zu verwenden, wenn Sie einen Bericht ausführen, können Sie diese Einstellung auf der Anforderungsseite außer Kraft setzen. Wählen Sie einfach im Dropdown-Menü **Drucker** den Drucker aus, den Sie für diesen Berichtsaufruf verwenden möchten.

### <a name="sizing-print-jobs"></a>Größe von Druckaufträgen anpassen

Das Drucken in der Cloud ist für Dokumente mit einer angemessenen Größe vorgesehen. Die meisten Clouddienste, einschließlich PrintNode und HP ePrint, sind auf 10 MB pro Auftrag begrenzt. Wenn Sie größere Berichte drucken müssen, müssen Sie diese möglicherweise in mehrere Ausdrucke aufteilen.

## <a name="see-also"></a>Siehe auch

[Berichte drucken](ui-work-report.md#PrintReport)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ausführen von Stapelverarbeitungen](ui-how-run-batch-jobs.md)  
[Dokumente per E-Mail versenden](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
