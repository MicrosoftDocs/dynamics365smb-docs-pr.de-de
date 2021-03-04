---
title: Benutzer nach Lizenzen erstellen | Microsoft Docs
description: Beschreibt, wie Benutzer basierend auf Lizenzen online oder vor Ort zu Business Central hinzugefügt werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 217b658e6a4c54996d3f0e9cfa7470f02908b380
ms.sourcegitcommit: 5d5451ee618f122c926e3189290f3765052f7077
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/11/2021
ms.locfileid: "4846340"
---
# <a name="create-users-according-to-licenses"></a>Benutzer nach Lizenzen anlegen

Dieser Artikel beschreibt, wie Administratoren Benutzer anlegen und festlegen, wer sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden kann und welche Berechtigungen den verschiedenen Benutzertypen entsprechend den Lizenzen erteilt werden.

Wenn Sie Benutzer in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen, können Sie ihnen über Berechtigungssätze spezifische Berechtigungen zuweisen und Benutzer in Benutzergruppen organisieren. Benutzergruppen machen es einfacher, Berechtigungen für mehrere Benutzer gleichzeitig zu verwalten. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md). 

Weitere Informationen zu den verschiedenen Lizenztypen und zur Funktionsweise der Lizenzierung finden Sie unter [!INCLUDE[prod_short](includes/prod_short.md)] Dynamics 365-Lizenzierungshandbuch, das Sie herunterladen können [https://go.microsoft.com/fwlink/?LinkId=866544](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Der Prozess der Benutzer- und Lizenzverwaltung variiert je nachdem, ob [!INCLUDE[prod_short](includes/prod_short.md)] online oder vor Ort eingesetzt wird. Für [!INCLUDE [prod_short](includes/prod_short.md)] online müssen Sie Benutzer von Microsoft 365 hinzufügen. In Vor-Ort-Bereitstellungen können Sie Benutzer direkt erstellen, bearbeiten und löschen.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Verwalten von Benutzern und Lizenzen in Online-Bereitstellungen

In der Online-Version von [!INCLUDE[prod_short](includes/prod_short.md)] wird die Anzahl der Benutzer durch das Abonnement definiert und Ihrem Mandanten im Microsoft Partner Center hinzugefügt, in der Regel durch Ihren Microsoft-Partner. Weitere Informationen finden Sie unter [Neukunden hinzufügen](/partner-center/add-a-new-customer) und [Kundenabonnements anlegen, aussetzen oder kündigen](/partner-center/create-a-new-subscription) in der Microsoft Partner Center Hilfe.

Um festzulegen, wer sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden kann, müssen Sie den Benutzern Produktlizenzen entsprechend den Rollen zuweisen, die sie in [!INCLUDE[prod_short](includes/prod_short.md)] ausführen werden. Dies kann auf folgende Weise geschehen:

- Der Microsoft 365-Administrator Ihres Unternehmens kann dies im [Microsoft 365 Admin Center](https://admin.microsoft.com) tun. Weitere Informationen finden Sie unter [Benutzer einzeln oder in großen Mengen zu Microsoft 365 hinzufügen](https://aka.ms/CreateOffice365Users).  
- Ein Microsoft-Partner kann Lizenzen im Microsoft 365 Administrationscenter oder im Microsoft Partner Center vergeben. Weitere Informationen finden Sie unter [Benutzerverwaltungsaufgaben für Kundenkonten](/partner-center/assign-licenses-to-users) in der Hilfe zum Microsoft Partner Center.

Weitere Informationen finden Sie unter [Administration von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in der Hilfe für Verwaltung.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Um Benutzer hinzuzufügen oder Benutzerinformationen und Lizenzzuweisungen in Business Central zu aktualisieren
Nachdem Sie Benutzer hinzugefügt oder Benutzerinformationen im Microsoft 365 Admin Center geändert haben, können Sie die Benutzerinformationen schnell importieren in [!INCLUDE[prod_short](includes/prod_short.md)]. Dies schließt Lizenzzuweisungen ein. 

1. Melden Sie sich als Administrator bei [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe dem Administratorkonto an.
2. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.  
3. Wählen Sie **Benuzter aktualisieren von Office 365**.

Wenn Sie neue Benutzer hinzufügen, müssen Sie im nächsten Schritt Benutzergruppen und Berechtigungen zuweisen. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md). Wenn Sie Benutzerinformationen aktualisieren und die Aktualisierung eine Lizenzänderung enthält, werden die Benutzer der entsprechenden Benutzergruppe zugewiesen und ihre Berechtigungssätze werden aktualisiert. Weitere Informationen finden Sie unter [Berechtigungen über Benutzergruppen verwalten](ui-define-granular-permissions.md).  

> [!NOTE]
> Alle Benutzer müssen der gleichen Lizenz zugeordnet werden, entweder Essential oder Premium. Weitere Informationen finden Sie im Microsoft Dynamics 365 Business Central-Lizenzierungshandbuch. Der Leitfaden steht auf der Website [Business Central](https://dynamics.microsoft.com/business-central/overview/) zum Herunterladen zur Verfügung.

Weitere Informationen über die Synchronisierung von Benutzerinformationen mit Microsoft 365 finden Sie im Abschnitt [Synchronisierung mit Microsoft 365](#m365).

> [!NOTE]
> Wenn Sie einen externen Buchhalter verwenden, um Ihre Bücher und Finanzberichterstattung zu verwalten, können Sie ihn/sie in Ihr Business Central einladen, damit er/sie mit Ihnen an Ihren Steuerdaten zu arbeiten. Weitere Informationen finden Sie unter [Ihren externen Buchhalter in Ihr Business Central einladen](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>So entfernen Sie den Zugriff eines Benutzers auf das System

In Online-Bereitstellungen können Sie einem Benutzer den Zugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] entziehen. Alle Verweise auf den Benutzer werden beibehalten, aber der Benutzer kann sich nicht anmelden und aktive Sitzungen für den Benutzer werden beendet.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Seite **Benutzerkarte** für den jeweiligen Benutzer, und wählen Sie dann im Feld **Status** **Deaktiviert**.
3. Um dem Benutzer erneut Zugriff zu gewähren, ändern Sie das Feld **Zustand** auf **aktiviert**.

Sie können die Lizenz auch von einem Benutzer im Microsoft 365 Admin Center entfernen. Der Benutzer kann sich dann nicht mehr anmelden. Weitere Informationen finden Sie unter [Lizenzen von Benutzern entfernen](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synchronisierung mit Microsoft 365

Wenn Sie einem Benutzer in Microsoft 365 eine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)] zuweisen, gibt es zwei Möglichkeiten, den Benutzer in [!INCLUDE[prod_short](includes/prod_short.md)] anzulegen.  

- Der Administrator kann den Benutzer durch Auswahl der Aktion **Benutzer aktualisieren von Office 365** auf der Seite **Benutzer** wie in der Sektion [So fügen Sie einen Benutzer hinzu oder aktualisieren Benutzerinformationen in Business Central](#adduser) beschrieben.
- Die Lizenzinformationen werden automatisch aktualisiert, wenn sich der Benutzer zum ersten Mal anmeldet.

In beiden Fällen werden eine Reihe von Einstellungen automatisch vorgenommen. Diese sind in der zweiten und dritten Spalte der Tabelle unten aufgeführt.

Wenn Sie die Benutzerinformationen in Microsoft 365 ändern, können Sie [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren, um die Änderung widerzuspiegeln. Je nachdem, was Sie aktualisieren möchten, verwenden Sie eine der Aktionen auf der Seite **Benutzer**. Die Aktionen werden in den letzten drei Spalten in der folgenden Tabelle beschrieben.

> [!NOTE]
> Die in der folgenden Tabelle beschriebenen Aktionen sind korrekt, Sie benötigen jedoch nur eine **Benutzer aktualisieren von Office 365**, die hinzugefügt wurde, um den Prozess zu vereinfachen. Die anderen Aktionen werden in einer zukünftigen Version von entfernt [!INCLUDE[prod_short](includes/prod_short.md)].

|Was passiert, wenn:|Erster Benutzer, erste Anmeldung|Benutzer von Microsoft 365 abrufen|Benutzer von Microsoft 365 aktualisieren|Standardbenutzergruppen des Benutzers wiederherstellen|Benutzergruppen aktualisieren|Benutzerinformationen aus Microsoft 365 aktualisieren|
|-|-|-|-|-|-|-|
|Umfang:|Aktueller Benutzer|Neue Benutzer in Microsoft 365|Mehrere ausgewählte Benutzer|Einzelner ausgewählter Benutzer (außer aktuellem)|Mehrere ausgewählte Benutzer|Mehrere ausgewählte Benutzer|
|Erstellen Sie den neuen Benutzer und weisen Sie ihm einen SUPER-Berechtigungssatz zu.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Aktualisieren Sie den Benutzerdatensatz basierend auf den tatsächlichen Informationen in Microsoft 365: Bundesland/Kanton, vollständiger Name, Kontakt-E-Mail, Authentifizierungs-E-Mail.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synchronisieren Sie Benutzerpläne (Lizenzen) mit Lizenzen und Rollen, die in Microsoft 365 zugewiesen sind.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Fügen Sie den Benutzer gemäß den aktuellen Benutzerplänen zu Benutzergruppen hinzu. Entfernen Sie die SUPER-Berechtigung für alle Benutzer außer dem ersten angemeldeten Benutzer und [Administratoren](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Mindestens ein SUPER ist erforderlich.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Entfernt manuell zugewiesene Benutzergruppen und Berechtigungen.|**X**<br /><br />Aktualisieren Sie die Benutzergruppenzuordnungen.| |

## <a name="the-device-license"></a>Die Gerätelizenz

Die Dynamics 365 Business Central-Gerätelizenz erlaubt es mehreren Benutzern, ein Gerät, das von der Lizenz abgedeckt ist, gleichzeitig zu benutzen. Dabei kann es sich z.B. um eine Verkaufsstelle, eine Werkstatt oder ein Lagergerät handeln. Wenn Sie eine Anzahl von Gerätelizenzen erworben haben, können sich bis zu dieser Anzahl von Benutzern, die der Gruppe Dynamics 365 Business Central Gerätebenutzer zugeordnet sind, gleichzeitig anmelden. Weitere Informationen finden Sie im Microsoft Dynamics 365 Business Central-Lizenzierungshandbuch. Der Leitfaden steht auf der Website [Business Central](https://dynamics.microsoft.com/business-central/overview/) zum Herunterladen zur Verfügung.

Der Microsoft 365-Administrator Ihres Unternehmens oder Ihr Microsoft-Partner kann die Dynamics 365 Business Central-Gerätebenutzergruppe erstellen und Gerätebenutzer als Mitglieder im [Microsoft 365 Admin Center](https://admin.microsoft.com/) oder im [Azure-Portal](https://portal.azure.com/) hinzufügen.

### <a name="device-user-limitations"></a>Einschränkungen für Gerätebenutzer

Benutzer mit der Gerätelizenz können die folgenden Aufgaben in [!INCLUDE[prod_short](includes/prod_short.md)] nicht ausführen:

- Richten Sie Aufträge so ein, dass sie als geplante Aufgaben in der Auftragswarteschlange ausgeführt werden. Gerätebenutzer sind gleichzeitige Benutzer. Daher können wir nicht sicherstellen, dass der beteiligte Benutzer im System vorhanden ist, wenn eine erforderliche Aufgabe ausgeführt wird.

- Ein Gerätebenutzer kann nicht der erste Benutzer sein, der sich anmeldet. Ein Benutzer vom Typ Administrator, Vollbenutzer oder externer Buchhalter muss sich als erster anmelden, damit er [!INCLUDE[prod_short](includes/prod_short.md)] einrichten kann. Weitere Informationen finden Sie unter [Administration von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in der Hilfe für Verwaltung.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>So erstellen Sie eine Dynamics 365 Business Central-Gerätebenutzergruppe

1. Wechseln Sie im Microsoft 365 Admin Center zur **Gruppen**-Seite.
2. Wählen Sie die Aktion **Gruppe hinzufügen**.
3. Wählen Sie auf der Seite **Gruppentyp auswählen** die Aktion **Sicherheit** und dann die Aktion **Hinzufügen**.
4. Geben Sie auf der Seite **Grundlagen** als Name der Gruppe **Dynamics 365 Business Central Gerätebenutzer** ein.
  
   >[!NOTE]
   >Der Name der Gruppe muss auf Englisch genau wie in Schritt 4 angegeben geschrieben werden, auch wenn Sie eine andere Sprache verwenden.
5. Wählen Sie die Schaltfläche **Schließen** aus.

> [!NOTE]
> Sie können auch eine Gruppe der Art Microsoft 365 erstellen. Weitere Informationen finden Sie unter [Gruppen vergleichen](https://docs.microsoft.com/office365/admin/create-groups/compare-groups)

### <a name="to-add-members-to-the-group"></a>So fügen Sie der Gruppe Mitglieder hinzu

1. Aktualisieren Sie im Microsoft 365 Admin Center die Seite **Gruppen**, damit Ihre neue Gruppe angezeigt wird.
2. Wählen Sie die **Dynamics 365 Business Central-Gerätebenutzer**-Gruppe und dann die **Alle anzeigen und Mitglieder verwalten**-Aktion.
3. Wählen Sie die Aktion **Mitglieder hinzufügen**.
4. Wählen Sie die Benutzer aus, die Sie hinzufügen möchten, und wählen Sie anschließend die Schaltfläche **Speichern** aus.
5. Wählen Sie die Schaltfläche **Schließen** dreimal aus.

Sie können der Dynamics 365 Business Central-Gerätebenutzergruppe nach Bedarf beliebig viele Benutzer hinzufügen. Die Anzahl der Geräte, an denen sich Benutzer gleichzeitig anmelden können, wird jedoch durch die Anzahl der erworbenen Gerätelizenzen definiert.

> [!NOTE]
> Sie müssen Benutzern, die Mitglieder der Dynamics 365 Business Central-Gerätebenutzergruppe sind, keine [!INCLUDE[prod_short](includes/prod_short.md)]-Lizenz zuweisen.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Verwalten von Benutzern und Lizenzen in lokalen Bereitstellungen

Bei lokalen Bereitstellungen wird die Anzahl der Benutzerlizenzen in der Lizenzdatei (.flf) angegeben. Wenn ein Administrator oder Microsoft-Partner die Lizenzdatei hochlädt, kann der Administrator angeben, welche Benutzer sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden können.

Bei lokalen Implementierungen erstellt, bearbeitet und löscht der Administrator Benutzer direkt von der Seite **Benutzer**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>So bearbeiten oder löschen Sie einen Benutzer in einer Vor-Ort-Bereitstellung

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Benutzer aus, und wählen Sie anschließend die Aktion **Bearbeiten** aus.
3. Füllen Sie auf der Seite **Benutzerkarte** die Informationen nach Bedarf aus.  
4. Um einen Benutzer zu löschen, markieren Sie den Benutzer, den Sie löschen möchten, und wählen Sie dann die Aktion **Löschen**.

> [!NOTE]
> Bei Vor-Ort-Bereitstellungen kann ein Administrator angeben, wie Benutzeranmeldeinformationen in der [!INCLUDE[server](includes/server.md)]-Instanz authentifiziert werden sollen. Wenn Sie einen Benutzer anlegen, geben Sie die Art des Berechtigungsnachweises an, den Sie verwenden.
>
> Weitere Informationen finden Sie in [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in der Administrationshilfe für [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Siehe auch

[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Ändern, welche Merkmale angezeigt werden](ui-experiences.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Hinzufügen von Benutzern zu Microsoft 365 für Unternehmen](https://aka.ms/CreateOffice365Users)  
[Sicherheit und Schutz in Business Central (Verwaltungsinhalte)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]