---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: a62a1a628f22ff47fa86a64a72f5b1834960dc72
ms.sourcegitcommit: 428f180604e5afcf94fa0e92a0615f58c88e13cd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3931271"
---
Bevor Sie die E-Mail-Protokollierung einrichten können, müssen Sie Exchange Online mit [öffentlichen Ordnern](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ) vorbereiten. Dies kann im [Exchange Admin Center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) oder über die [Exchange-Verwaltungsshell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) erfolgen.  

> [!TIP]
> Wenn Sie die [Exchange-Verwaltungsshell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) verwenden, finden Sie in einem Beispielskript, das wir im [BCTech-Repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging) veröffentlicht haben, Anregungen zum Einrichten Ihres Skripts.

In der folgenden Liste werden die Hauptschritte mit Links zu weiteren Informationen beschrieben.  

- Erstellen Sie eine Administratorrolle für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle:

  |Eigenschaft        |Wert                     |
  |----------------|--------------------------|
  |Name            |Verwaltung öffentlicher Ordner |
  |Ausgewählte Rollen  |Öffentliche Ordner            |
  |Ausgewählte Mitglieder|Die E-Mail-Adresse des Benutzerkontos, mit dem Business Central das E-Mail-Protokollierungsprojekt ausführt|

  Weitere Informationen finden Sie unter [Rollengruppen verwalten](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Erstellen Sie ein neues Postfach für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle:

  |Eigenschaft        |Wert                     |
  |----------------|--------------------------|
  |Name            |Öffentliches Postfach            |

  Weitere Informationen finden Sie unter [Postfach für öffentliche Ordner in Exchange Server erstellen](/exchange/collaboration/public-folders/create-public-folder-mailboxes)  

- Neue öffentliche Ordner erstellen

  - Erstellen Sie einen neuen öffentlichen Ordner mit dem Namen *E-Mail-Protokollierung* im Stammverzeichnis, sodass der vollständige Pfad zum Ordner ```\Email Logging\``` wird.
  - Erstellen Sie zwei Unterordner, sodass das Ergebnis die folgenden vollständigen Pfade zu den Ordnern sind:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Weitere Informationen finden Sie unter [Öffentlichen Ordner erstellen](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Den öffentlichen Ordner *Warteschlange* für E-Mail aktivieren

  Weitere Informationen finden Sie unter [Öffentlichen Ordner für E-Mail aktivieren oder deaktivieren](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Das Senden von E-Mails an den öffentlichen Ordner *Warteschlange* mit Outlook oder der Exchange-Verwaltungsshell für E-Mail aktivieren

  Weitere Informationen finden Sie unter [Anonymen Benutzern erlauben, E-Mails an einen E-Mail-fähigen öffentlichen Ordner zu senden](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Legen Sie den Benutzer für die E-Mail-Protokollierung als Eigentümer der beiden öffentlichen Ordner *Warteschlange* und *Lager* fest, indem Sie Outlook oder die Exchange-Verwaltungsshell basierend auf den Informationen in der folgenden Tabelle verwenden:

  |Eigenschaft        |Wert                     |
  |----------------|--------------------------|
  |Benutzer            |Die E-Mail-Adresse des Benutzerkontos, mit dem Business Central das E-Mail-Protokollierungsprojekt ausführt|
  |Berechtigungsstufe|Besitzer                     |

  Weitere Informationen finden Sie unter [Dem öffentlichen Ordner Berechtigungen zuweisen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Erstellen Sie zwei neue E-Mail-Fluss-Regeln für öffentliche Ordner basierend auf den Informationen in der folgenden Tabelle.

  |Zweck  |Name |Bedingungen                        |Aktion                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Regel für eingehende E-Mails |An diese Organisation gesendete E-Mails protokollieren|*Der Absender* befindet sich *außerhalb der Organisation* und der *Empfänger* befindet sich *innerhalb der Organisation*|Das für den öffentlichen Ordner *Warteschlange* festgelegte E-Mail-Konto mit Bcc senden|
  |Regel für ausgehende E-Mails | Von dieser Organisation gesendete E-Mails protokollieren |*Der Absender* befindet sich *innerhalb der Organisation* und der *Empfänger* befindet sich *außerhalb der Organisation*|Das für den öffentlichen Ordner *Warteschlange* festgelegte E-Mail-Konto mit Bcc senden|
  
  Weitere Informationen finden Sie unter [E-Mail-Fluss-Regeln in Exchange Online verwalten](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) und [Aktionen für E-Mail-Fluss-Regeln in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Wenn Sie Änderungen in der Exchange-Verwaltungsshell vornehmen, werden die Änderungen nach einer Verzögerung im Exchange-Verwaltungscenter angezeigt. Die in Exchange vorgenommenen Änderungen sind nach einer Verzögerung auch in [!INCLUDE[prodshort](prodshort.md)] verfügbar.
