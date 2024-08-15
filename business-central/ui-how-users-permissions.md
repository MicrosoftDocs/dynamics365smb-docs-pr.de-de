---
title: Benutzer gemäß Lizenzen erstellen
description: 'Beschreibt, wie Benutzer basierend auf Lizenzen online oder vor Ort zu Business Central hinzugefügt werden.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '119, 6300, 6301, 6302, 8930, 9800_Primary, 9807_Primary, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173, 774_Primary'
ms.date: 05/03/2024
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Benutzer gemäß Lizenzen erstellen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Dieser Artikel beschreibt, wie Administratoren Benutzer erstellen und festlegen, wer sich anmelden kann bei [!INCLUDE[prod_short](includes/prod_short.md)]. Dieser Artikel beschreibt auch, wie Sie Berechtigungen gemäß Ihren Produktlizenzen verschiedenen Benutzenden zuweisen.

Wenn Sie Benutzer in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen, erteilen Sie ihnen über Berechtigungssätze Berechtigungen. Sie können Benutzer auch in Benutzergruppen organisieren. Benutzergruppen erleichtern die gleichzeitige Verwaltung von Berechtigungen und anderen Einstellungen für mehrere Benutzer. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

Für weitere Informationen zu den verschiedenen Lizenztypen und zur Funktionsweise der Lizenzierung in [!INCLUDE[prod_short](includes/prod_short.md)], [laden Sie das Dynamics 365-Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?LinkId=866544) herunter.

> [!NOTE]
> Der Prozess der Benutzer- und Lizenzverwaltung variiert je nachdem, ob [!INCLUDE[prod_short](includes/prod_short.md)] online oder vor Ort eingesetzt wird. Für [!INCLUDE [prod_short](includes/prod_short.md)] online müssen Sie Benutzer von Microsoft 365 hinzufügen. In Vor-Ort-Bereitstellungen können Sie Benutzer direkt erstellen, bearbeiten und löschen.  

## Benutzer und Lizenzen in Online-Mandanten verwalten

Benutzerkonten in [!INCLUDE[prod_short](includes/prod_short.md)] müssen zunächst im Admin-Center Microsoft 365 erstellt werden. Diese Benutzerkonten sind nicht exklusiv für [!INCLUDE [prod_short](includes/prod_short.md)]. Wenn Sie andere Tarife abonniert haben, können Sie sich damit auch bei anderen Anwendungen anmelden, beispielsweise bei Power BI. Informationen zum Erstellen von Benutzern im Admin-Center Microsoft 365 finden Sie unter [Benutzer im Admin-Center von Microsoft erstellen](/microsoft-365/admin/add-users/add-users).

Ihr Abonnement für [!INCLUDE[prod_short](includes/prod_short.md)] online bestimmt, wie viele [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzerlizenzen Sie zulassen können. Benutzer werden Ihrem Mandanten im Microsoft Partner Center hinzugefügt, in der Regel von Ihrem Microsoft-Partner. Weitere Informationen finden Sie unter [Verwaltung von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Sie weisen den Benutzenden Lizenzen entsprechend der Arbeit zu, die jeder Benutzende in [!INCLUDE[prod_short](includes/prod_short.md)] erledigt. Sie können Lizenzen auf verschiedene Arten zuweisen:

- Der Microsoft 365-Administrator Ihres Unternehmens kann dies im [Microsoft 365 Admin Center](https://admin.microsoft.com) vornehmen. Weitere Informationen finden Sie unter [Benutzer einzeln oder in großen Mengen zu Microsoft 365](/microsoft-365/admin/add-users/add-users) hinzufügen.  
- Ein Microsoft-Partner kann Lizenzen im Microsoft 365 Admin Center oder im Microsoft Partner Center vergeben. Weitere Informationen finden Sie unter [Benutzerverwaltungsaufgaben für Kundenkonten](/partner-center/assign-licenses-to-users) in der Hilfe zum Microsoft Partner Center.

Weitere Informationen finden Sie unter [Administration von Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in der Hilfe für Verwaltung.

Nachdem die Benutzerkonten im Microsoft 365 Admin-Center erstellt wurden, gibt es zwei Möglichkeiten, sie in [!INCLUDE [prod_short](includes/prod_short.md)] zu importieren:

- Ein Benutzerkonto wird automatisch importiert, wenn sich der Benutzende das erste Mal bei [!INCLUDE [prod_short](includes/prod_short.md)] anmeldet.

   > [!NOTE]
   > Nachdem Benutzende sich online in [!INCLUDE [prod_short](includes/prod_short.md)] angemeldet haben, können Sie diese Benutzenden nicht löschen.

- Der Administrator kann Benutzer importieren, indem er auf der Seite **Benutzer* die Aktion **Benutzer aktualisieren aus Microsoft 365** wählt.

Beide Ansätze haben ihre eigenen Vorteile, und Sie können sie gleichzeitig verwenden. Jeder Ansatz lässt zu, dass Administratoren [!INCLUDE [prod_short](includes/prod_short.md)] proaktiv konfigurieren, um die Startberechtigungen, Benutzergruppen und Benutzerprofile zuzuweisen. Mit der Aktion **Benutzer aktualisieren ab Microsoft 365** erhalten Administratoren mehr Steuerelemente zur Anpassung von Berechtigungen, Benutzergruppen und Profilen. Diese Vorgehensweise ist ideal, wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] zum ersten Mal einrichten, bevor sich Benutzende anmelden, oder wenn Sie ein neues Team von Benutzenden hinzufügen.

> [!NOTE]
> Nachdem Sie Benutzer im Microsoft 365 Admin Center der hinzugefügt haben, empfehlen wir, dass Sie die Benutzerinformationen in [!INCLUDE[prod_short](includes/prod_short.md)] so bald wie möglich aktualisieren. Es ist einfach, die Benutzerinformationen auf dem neuesten Stand zu halten und sicherzustellen, dass sich die Benutzer immer anmelden können. Weitere Informationen finden Sie unter [Um Benutzer hinzuzufügen oder Benutzerinformationen und Lizenzzuweisungen in Business Central zu aktualisieren](#adduser).<br>
>
> Das Aktualisieren von Benutzerinformationen ist besonders wichtig, wenn Sie Berechtigungssätze für die Lizenz angepasst haben. Wenn ein neuer Benutzer versucht, sich in [!INCLUDE[prod_short](includes/prod_short.md)] anzumelden, bevor Sie ihn hinzugefügt haben, kann er dies möglicherweise nicht. Weitere Informationen finden Sie unter [Berechtigungen basierend auf Lizenzen konfigurieren](#licensespermissions).
>
> Benutzer, bei denen dieses Problem auftritt, werden jedoch nicht wirklich blockiert. Sie können entweder die **Zruck zur Startseite** Aktion verwenden oder sich einfach erneut anmelden, um das Problem zu lösen.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Weitere Informationen finden Sie unter [Delegierter Administratorzugriff auf Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

### <a name="licensespermissions"></a>Berechtigungen auf Grundlage von Lizenzen konfigurieren

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Admins können Berechtigungssätze und Benutzergruppen für jede Lizenz festlegen.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->  

Die allgemein verwendete Lizenz *Dynamics 365 Business Central Teammitglied* verfügt beispielsweise standardmäßig über die folgenden Berechtigungssätze:

- D365 LESEN
- D365-TEAMMITGLIED
- IN EXCEL BEARBEITEN – ANZEIGEN
- BERICHT EXPORTIEREN – EXCEL
- LOKAL

Andere Berechtigungen werden auf der Grundlage der Benutzergruppen, die der Lizenz zugewiesen sind, automatisch hinzugefügt. Wenn Sie einen neuen Benutzenden auf der Grundlage dieser Lizenz erstellen, weist [!INCLUDE[prod_short](includes/prod_short.md)] die Berechtigungssätze zu, die von den Benutzergruppen und den Berechtigungssätzen der Lizenz stammen. Die gleichen Startberechtigungen werden dem Benutzer zugewiesen, wenn sein Benutzerkonto automatisch in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt wurde oder wenn der Administrator die Aktion **Benutzer aus Microsoft 365** auf der Seite **Benutzer** verwendet hat.

Wenn diese Standardkonfiguration nicht die richtige Einrichtung für eine bestimmte Umgebung ist, kann der Admin diese Konfiguration ändern. Benutzerdefinierte Berechtigungen wirken sich jedoch nur auf neue Benutzende aus, denen diese Lizenz zugewiesen wurde. Berechtigungen für vorhandene Benutzende, denen die Lizenz zugewiesen wurde, sind davon nicht betroffen.  

1. Melden Sie sich als Administrator bei [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe dem Administratorkonto an.  
2. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Lizenzkonfiguration** ein, und wählen Sie dann den zugehörigen Link.  

    <!--Alternatively, if you're already in the **Users** page, you can run the **Update Users from Microsoft 365** guide, and then, on the first page of the guide, choose the **Configure permissions per license** link.-->  
3. Auf der **Lizenzkonfiguration**-Seite wählen Sie die Lizenz aus, die Sie anpassen möchten, und Sie wählen dann die **Konfigurieren**-Aktion aus.  
4. Wählen Sie das Feld **Berechtigungen anpassen**, um die Anpassung zu aktivieren, und nehmen Sie dann die Änderungen vor.  

    In unserem Beispiel möchte der Administrator die Berechtigung zum Bearbeiten in Excel entfernen, also entfernt er die *Excel-Exportaktion*-Benutzergruppe aus der Team Member-Lizenz. Danach können neue Benutzende, denen die Teammitglied-Lizenz zugewiesen wurde, keine Daten nach Excel exportieren. Wenn die Organisation ihre Meinung zu diesem Thema ändert, können sie einfach zur **Lizenzkonfiguration**-Seite zurückkehren und die Anpassung für diesen Lizenztyp deaktivieren.  

> [!IMPORTANT]
> Diese Anpassung der Berechtigungen wird nur für neue Benutzer wirksam, denen Sie die entsprechende Lizenz zuweisen. Vorhandene Benutzer werden nicht aktualisiert. Wir empfehlen, dass Sie Berechtigungen anpassen, bevor Sie mit der Zuweisung von Benutzerlizenzen im Microsoft 365 Admin Center beginnen.

### <a name="adduser"></a>Um Benutzer hinzuzufügen oder Benutzerinformationen und Lizenzzuweisungen in Business Central zu aktualisieren

Nachdem Sie Benutzer hinzugefügt oder Benutzerinformationen im Microsoft 365 Admin Center geändert haben, können Sie die Benutzerinformationen schnell in [!INCLUDE[prod_short](includes/prod_short.md)] importieren. Der Import enthält Lizenzzuweisungen.  

> [!TIP]
> Wenn Sie Benutzerinformationen aktualisieren müssen und viele Benutzende haben, können Sie den Filterbereich verwenden, um die Liste einzugrenzen. Sie können nach grundlegenden Informationen wie dem Benutzernamen filtern oder mehr technische Filter festlegen, beispielsweise nach der Sicherheits-ID des Benutzenden.

1. Melden Sie sich als Administrator bei [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe dem Administratorkonto an.
2. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.  
3. Wählen Sie **Benuzter von Microsoft 365** aktualisieren.

> [!IMPORTANT]  
> Das Ausführen der Synchronisierung von Benutzern von Microsoft 365 unter Verwendung der Anleitung **Benutzer aktualisieren von Microsoft 365** erfordert den SUPER-Berechtigungssatz.

> [!NOTE]
> Die Funktion  **Benutzer aktualisieren von Microsoft 365** Anleitung aktualisiert keine Benutzer, denen keine Lizenz zugewiesen ist, z. B. jemand, der ein  [Dynamics 365-Administrator ist](/entra/identity/role-based-access-control/permissions-reference#dynamics-365-administrator). Diese Benutzer werden bei der nächsten Anmeldung bei Umgebung aktualisiert.

Der nächste Schritt für neu erstellte Benutzer ist die Zuweisung von Benutzergruppen und Berechtigungen. Informationen hierzu finden Sie unter [Benutzern und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md). Wenn Sie Benutzende mit einer Lizenzänderung aktualisieren, weist [!INCLUDE [prod_short](includes/prod_short.md)] die Benutzenden der entsprechenden Benutzergruppe zu und aktualisiert ihre Berechtigungssätze. Weitere Informationen finden Sie unter [Berechtigungen über Benutzergruppen verwalten](ui-define-granular-permissions.md).  

> [!NOTE]
> Mit der Veröffentlichungswelle 1 von 2024 kann sich ein Benutzer einer Premium-Lizenz bei einem Unternehmen anmelden, bei dem das Feld **Benutzererfahrung** auf der Seite **Unternehmensdaten** auf **Essentials** festgelegt ist. Der Premium-Benutzende kann jedoch keine der Funktionen nutzen, die die Premium-Lizenz bietet. In der umgekehrten Richtung funktioniert das nicht. Benutzer mit einer Essentials-Lizenz können sich nicht bei einem Unternehmen anmelden, bei dem **Benutzererfahrung** auf der Seite **Unternehmensdaten** auf **Premium** festgelegt ist. Weitere Informationen zur Lizenzierung finden Sie auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/) Website.

Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten. Weitere Informationen finden Sie unter [Ihren externen Buchhalter in Ihr Business Central einladen](finance-accounting.md#inviteaccountant).

Weitere Informationen zur Synchronisierung von Benutzerinformationen mit Microsoft 365 finden Sie im Abschnitt [Synchronisierung mit Microsoft 365](#m365).

> [!NOTE]
> Wenn Sie eines externen Buchhalter verwenden, um Ihre Buch und Berichte zu verwalten, können Sie sie für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten. Weitere Informationen finden Sie unter [Ihren externen Buchhalter in Ihr Business Central einladen](finance-accounting.md#inviteaccountant).

### So entfernen Sie den Zugriff eines Benutzers auf das System

Sie können den Zugriff eines Benutzers auf [!INCLUDE[prod_short](includes/prod_short.md)] Online entfernen. Alle Verweise auf den Benutzer bleiben erhalten. Der Benutzer kann sich jedoch nicht anmelden, und aktive Sitzungen für den Benutzer werden beendet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Seite **Benutzerkarte** für den jeweiligen Benutzer, und wählen Sie dann im Feld **Status** **Deaktiviert**.
3. Um dem Benutzer erneut Zugriff zu gewähren, ändern Sie das Feld **Status** auf **aktiviert**.

Sie können die Lizenz auch von einem Benutzer im Microsoft 365 Admin Center entfernen. Der Benutzer kann sich dann nicht mehr anmelden. Weitere Informationen finden Sie unter [Lizenzen von Benutzern entfernen](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="m365"></a>Synchronisierung mit Microsoft 365

Wenn Sie einem Benutzer in Microsoft 365 eine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)] zuweisen, gibt es zwei Möglichkeiten, den Benutzer in [!INCLUDE[prod_short](includes/prod_short.md)] anzulegen.  

- Der Administrator kann den Benutzer durch Auswahl der Aktion **Benutzer aktualisieren von Microsoft 365** auf der Seite **Benutzer** wie in der Sektion [So fügen Sie einen Benutzer hinzu oder aktualisieren Benutzerinformationen in Business Central](#adduser) beschrieben.
- Die Lizenzinformationen werden automatisch aktualisiert, wenn sich Benutzende zum ersten Mal anmelden.

In beiden Fällen werden mehrere Einstellungen automatisch angewendet. Diese Einstellungen sind in der zweiten und dritten Spalte der folgenden Tabelle aufgeführt.

Wenn Sie die Benutzerinformationen in Microsoft 365 ändern, können Sie [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren, um die Änderung widerzuspiegeln. Je nachdem, was Sie aktualisieren möchten, verwenden Sie eine der Aktionen auf der Seite **Benutzer**. Die Aktionen sind in den letzten beiden Spalten der folgenden Tabelle beschrieben.

|Was passiert, wenn:|Erster Benutzer, erste Anmeldung|Benutzer von Microsoft 365 aktualisieren|Standardbenutzergruppen des Benutzers wiederherstellen|
|-|-|-|-|
|Umfang:|Aktueller Benutzer|Mehrere ausgewählte Benutzer|Einzelner ausgewählter Benutzer (außer aktuellem)|
|Erstellen Sie den neuen Benutzer und weisen Sie ihm einen SUPER-Berechtigungssatz zu.<br /><br /><!--Platform-->|**X**|**X** | | 
|Aktualisieren Sie den Benutzerdatensatz basierend auf den tatsächlichen Informationen in Microsoft 365: Bundesland/Kanton, vollständiger Name, Kontakt-E-Mail, Authentifizierungs-E-Mail.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|
|Synchronisieren Sie Benutzerpläne (Lizenzen) mit Lizenzen und Rollen, die in Microsoft 365 zugewiesen sind.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|
|Fügen Sie den Benutzer gemäß den aktuellen Benutzerplänen zu Benutzergruppen hinzu. Entfernen Sie die SUPER-Berechtigung für alle Benutzer außer dem ersten angemeldeten Benutzer und [Administratoren](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Mindestens ein SUPER ist erforderlich.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**<br /><br />Entfernt manuell zugewiesene Benutzergruppen und Berechtigungen.|

Benutzer können auf [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze in Teams nur mit ihrer Microsoft 365-Lizenz zugreifen. Wenn der Zugriff für eine Umgebung aktiviert ist, werden bei der Synchronisierung mit der Aktion **Benutzende von Microsoft 365 aktualisieren** Benutzende, die nur eine Microsoft 365-Lizenz haben, übersprungen. Um diese Benutzer in die Synchronisierung einzubeziehen, müssen Sie zunächst die Umgebungseinstellungen aktualisieren, indem Sie eine Sicherheitsgruppe zuweisen, die Benutzer mit einer [!INCLUDE[prod_short](includes/prod_short.md)]-Lizenz und Benutzer mit nur einer Microsoft 365-Lizenz enthält.

Erfahren Sie mehr über die Sicherung des Zugriffs auf Umgebungen mithilfe von Sicherheitsgruppen unter [Verwalten des Zugriffs mithilfe von Microsoft Entra-Gruppen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups).

Einen Überblick über den Zugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] in Teams mit Microsoft 365-Lizenzen finden Sie unter [admin-access-with-m365-license](admin-access-with-m365-license.md).

## Benutzer und Lizenzen in lokalen Bereitstellungen verwalten

Bei lokalen Bereitstellungen wird die Anzahl der Benutzerlizenzen in der Lizenzdatei (.bclicense oder .flf) angegeben. Wenn ein Administrator oder Microsoft-Partner die Lizenzdatei hochlädt, kann er angeben, welche Benutzer sich bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden können.

Bei lokalen Implementierungen erstellt, bearbeitet und löscht der Administrator Benutzer direkt von der Seite **Benutzer**.

### So bearbeiten oder löschen Sie einen Benutzer in einer Vor-Ort-Bereitstellung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Benutzer aus, und wählen Sie anschließend die Aktion **Bearbeiten** aus.
3. Füllen Sie auf der Seite **Benutzerkarte** die Informationen nach Bedarf aus.  
4. Um einen Benutzer zu löschen, markieren Sie den Benutzer, den Sie löschen möchten, und wählen Sie dann die Aktion **Löschen**.

> [!NOTE]
> Bei Vor-Ort-Bereitstellungen kann ein Administrator angeben, wie Benutzeranmeldeinformationen in der [!INCLUDE[server](includes/server.md)]-Instanz authentifiziert werden sollen. Wenn Sie einen Benutzer anlegen, geben Sie die Art des Berechtigungsnachweises an, den Sie verwenden.
>
> Weitere Informationen finden Sie in [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in der Administrationshilfe für [!INCLUDE[prod_short](includes/prod_short.md)].

## Den Benutzerstatus nach Lizenztyp analysieren

Sie können das Feature **Datenanalyse** zur Analyse von Daten auf der Seite [Benutzende](https://businesscentral.dynamics.com/?page=9800) verwenden. Sie müssen keinen Bericht ausführen und keine andere Anwendung wie beispielsweise Excel öffnen. Das Feature bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Benutzende nach Status“ oder „Benutzende nach Lizenztyp“ oder jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

### Szenarios für die Benutzeranalyse

Die folgenden Abschnitte enthalten Beispiele für Szenarios, in denen Ihnen die Analyse der Benutzerliste helfen kann, den Status Ihrer Benutzenden zu überwachen.

| Region | An... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
| [Benutzende nach Status](#example-users-by-status) | Lassen Sie sich eine Liste der Benutzenden basierend auf ihrem Status (aktiviert/deaktiviert) anzeigen. | [Benutzer](https://businesscentral.dynamics.com/?page=9800) | **Status**, **Benutzername**, **Vollständiger Name**, **Autorisierungs-E-Mail** und **Lizenztyp**. |
| [Benutzende nach Lizenztyp](#example-users-by-license-type) | Lassen Sie sich eine Liste der Benutzenden basierend auf ihrem Lizenztyp anzeigen. | [Benutzer](https://businesscentral.dynamics.com/?page=9800) | **Lizenztyp**, **Status**, **Benutzername**, **Vollständiger Name** und **Autorisierungs-E-Mail**. |

### Beispiel: Benutzende nach Status

Um Benutzende nach Status zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Liste [Benutzende](https://businesscentral.dynamics.com/?page=9800) und wählen Sie das Symbol :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben"::: aus, um den Analysemodus zu aktivieren.
1. Entfernen Sie auf dem Menü **Spalten** alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** auf der rechten Seite aus).
1. Ziehen Sie die Felder **Status** (Benutzender aktiviert/deaktiviert) und **Lizenztyp** in den Bereich **Zeilengruppen**.
1. Wählen Sie die Felder **Benutzername**, **Vollständiger Name** und **Autorisierungs-E-Mail** aus.
1. Benennen Sie Ihre Analyseregisterkarte in **Benutzende nach Status** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source=" media/data-analysis-users.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Änderungsprotokollposten“ (Wer hat wann welche Daten geändert?)." lightbox="media/data-analysis-users.png":::

### Beispiel: Benutzende nach Lizenztyp

Um Benutzende nach Lizenztyp zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Liste [Benutzende](https://businesscentral.dynamics.com/?page=9800) und wählen Sie das Symbol :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben"::: aus, um den Analysemodus zu aktivieren.
1. Entfernen Sie auf dem Menü **Spalten** alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** auf der rechten Seite aus).
1. Ziehen Sie die Felder **Lizenztyp** und **Status** in den Bereich **Zeilengruppen**.
1. Wählen Sie die Felder **Benutzername**, **Vollständiger Name** und **Autorisierungs-E-Mail** aus.
1. Benennen Sie Ihre Analyseregisterkarte in **Benutzende nach Lizenztyp** oder in etwas anderes um, das diese Analyse beschreibt.

## Siehe auch

[Benutzenden und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Ändern, welche Merkmale angezeigt werden](ui-experiences.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Lizenzierung in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Benutzer zu Microsoft 365 für Unternehmen hinzufügen](/microsoft-365/admin/add-users/add-users)  
[Sicherheit und Schutz in Business Central (Verwaltungsinhalte)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Benutzern eine Telemetriekennung zuweisen](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
