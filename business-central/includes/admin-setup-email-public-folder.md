---
author: edupont04
ms.topic: include
ms.date: 02/15/2022
ms.author: edupont
---

> [!NOTE]
> In den folgenden Abschnitten wird davon ausgegangen, dass Sie über Administratorzugriff für Exchange Online verfügen.

Bevor Sie die E-Mail-Protokollierung einrichten können, müssen Sie Office 365 mit [öffentlichen Ordnern](/exchange/collaboration-exo/public-folders/public-folders) vorbereiten. Dies kann im [Exchange Admin Center](/exchange/exchange-admin-center?preserve-view=true) oder über [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true) erfolgen.

> [!TIP]
> Wenn Sie [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) verwenden, finden Sie in einem Beispielskript, das wir im [BCTech-Repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging) veröffentlicht haben, Anregungen zum Einrichten Ihres Skripts.

Führen Sie die folgenden Schritte zum Einrichten von Exchange Online mit Links zu weiteren Informationen aus.

### Eine Administratorrollengruppe erstellen

Erstellen Sie eine Administratorrollengruppe für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle:

|Eigenschaft        |Wert                     |
|----------------|--------------------------|
|Name            |Verwaltung öffentlicher Ordner |
|Ausgewählte Rollen  |Öffentliche Ordner            |
|Ausgewählte Benutzer  |Die E-Mail-Adresse des Benutzerkontos, mit dem Business Central das E-Mail-Protokollierungsprojekt ausführt|

Weitere Informationen finden Sie unter [Rollengruppen in Exchange Online verwalten](/exchange/permissions-exo/role-groups).

### Ein neues Postfach für öffentliche Ordner erstellen

Erstellen Sie ein neues Postfach für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle:

|Eigenschaft        |Wert                     |
|----------------|--------------------------|
|Name            |Öffentliches Postfach            |

Weitere Informationen finden Sie unter [Ein Postfach für öffentliche Ordner erstellen](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### Neue öffentliche Ordner erstellen

1. Erstellen Sie einen neuen öffentlichen Ordner mit dem Namen **E-Mail-Protokollierung** im Stammverzeichnis, sodass der vollständige Pfad zum Ordner `\Email Logging\` wird.
2. Erstellen Sie zwei Unterordner, sodass das Ergebnis die folgenden vollständigen Pfade zu den Ordnern sind:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Weitere Informationen finden Sie unter [Öffentlichen Ordner erstellen](/exchange/collaboration-exo/public-folders/create-public-folder).

### Besitz für öffentliche Ordner festlegen

Legen Sie den E-Mail-Protokollierungsbenutzer als Besitzer der beiden öffentlichen Ordner *Warteschlange* und *Speicher* fest.

Weitere Informationen finden Sie unter [Dem öffentlichen Ordner Berechtigungen zuweisen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### Den öffentlichen Ordner *Warteschlange* für E-Mail aktivieren

  Weitere Informationen finden Sie unter [Öffentlichen Ordner für E-Mail aktivieren oder deaktivieren](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### Das Senden von E-Mails an den öffentlichen Ordner *Warteschlange* aktivieren

Aktivieren Sie das Senden von E-Mails an den öffentlichen Ordner *Warteschlange* mit Outlook oder der Exchange-Verwaltungsshell für E-Mail.

Weitere Informationen finden Sie unter [Anonymen Benutzern erlauben, E-Mails an einen E-Mail-fähigen öffentlichen Ordner zu senden](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### E-Mail-Fluss-Regeln erstellen

Erstellen Sie zwei neue E-Mail-Fluss-Regeln für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle:

|Zweck  |Name |Diese Regel anwenden, wenn...             |Führen Sie die folgenden Schritte aus...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Regel für eingehende E-Mails |An diese Organisation gesendete E-Mails protokollieren|*Der Absender* befindet sich *außerhalb der Organisation* und der *Empfänger* befindet sich *innerhalb der Organisation*|Das für den öffentlichen Ordner *Warteschlange* festgelegte E-Mail-Konto mit Bcc senden|
|Regel für ausgehende E-Mails | Von dieser Organisation gesendete E-Mails protokollieren |*Der Absender* befindet sich *innerhalb der Organisation* und der *Empfänger* befindet sich *außerhalb der Organisation*|Das für den öffentlichen Ordner *Warteschlange* festgelegte E-Mail-Konto mit Bcc senden|

Weitere Informationen finden Sie unter [E-Mail-Fluss-Regeln in Exchange Online verwalten](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) und [Aktionen für E-Mail-Fluss-Regeln in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Wenn Sie Änderungen in der Exchange-Verwaltungsshell vornehmen, werden die Änderungen nach einer Verzögerung im Exchange-Verwaltungscenter angezeigt. Die in Exchange vorgenommenen Änderungen sind nach einer Verzögerung auch in [!INCLUDE[prod_short](prod_short.md)] verfügbar. Die Verzögerung kann mehrere Stunden betragen.
