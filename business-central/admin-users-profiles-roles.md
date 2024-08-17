---
title: Verwalten von Benutzern und Rollen
description: 'Erfahren Sie, wie Sie Benutzerprofile in Business Central verwalten können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 07/26/2024
ms.custom: bap-template
ms.search.form: '9171,'
---
# <a name="manage-user-profiles"></a>Benutzerprofile verwalten

Weisen Sie allen Benutzern Profile zu, die Folgendes widerspiegeln:

* ihre geschäftliche Rolle
* die Abteilung, in der sie arbeiten
* einen weiteren Kategorisierungstyp

Mithilfe von Profilen können Administratoren zentral definieren und verwalten, welche unterschiedlichen Benutzertypen auf Business Central zugreifen können.

Die typische geschäftliche Verwendung eines Profils ist eine Rolle. Ein Profil wird daher *Profil (Rolle)* benannt in der Benutzeroberfläche.

Als Administrator erstellen und verwalten Sie Profile auf der **Profile (Rollen)** Seite. Jedes Profil verfügt über eine Karte, auf der die Einstellungen für die zugehörige Rolle verwaltet werden. Die Karte enthält folgende Informationen:

* Name der Rolle
* Benutzereinstellungen
* Das vom Profil genutzte Rollencenter

Weitere Informationen zu Benutzereinstellungen und Rollencentern finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md).

Bevor Sie Benutzerprofile verwalten können, müssen Sie die Benutzer erstellen und über das Microsoft 365 Admin Center hinzufügen. Anschließend können Sie jedem Benutzer oder jeder Benutzergruppe Berechtigungen zuweisen. Berechtigungen definieren die Funktionen, auf die Benutzer zugreifen können. Weitere Informationen zu Berechtigungseinstellungen finden Sie unter [Benutzenden und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Seitenanpassung

Sie können die Seitenlayouts für ein Profil so anpassen, dass alle Benutzenden, denen das Profil zugewiesen wurde, die angepassten Seiten sehen. Als Administrator passen Sie Seiten an, indem Sie dieselben Funktionen verwenden wie Benutzer, wenn sie Personalisierungen vornehmen. Weitere Informationen zum Anpassen von Seitenlayouts finden Sie unter [Seiten für Profile anpassen](ui-personalization-manage.md).

## <a name="create-a-profile"></a>Erstellen eines Profils

Wenn Sie ein vorhandenes Profil nicht kopieren können, können Sie manuell ein neues Profil erstellen.

1. Auswählen die ![Suche nach Seite oder Bericht.](media/ui-search/search_small.png "Suche nach Seiten- oder Berichtssymbolen") Symbol, geben Sie  **Profile (Rollen)** ein und Auswählen dann das zugehörige verknüpfen.  
2. Führen Sie auf der Seite  **Profile (Rollen)**  die Aktion  **Neu** Auswählen aus.  
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Wenn Sie möchten, dass ein bestimmtes Profil nur ganz bestimmten Benutzern zur Verfügung steht, können Sie das Feld **Beschreibung** auf `Navigation menu only.` festlegen. Auf diese Weise wird das Profil aus der Liste der verfügbaren Rollen in **Meine Einstellungen** ausgeschlossen.

## <a name="copy-a-profile"></a>So kopieren Sie ein Profil

Um Zeit zu sparen, können Sie ein neues Profil erstellen, indem Sie ein vorhandenes kopieren. Kopieren Sie eines mit ähnlichen Einstellungen wie das, das Sie erstellen möchten.

Wenn Sie ein Profil kopieren, werden auch alle beteiligten Seitenanpassungen kopiert, sowohl die vom Benutzer erstellten als auch die von Erweiterungen abgeleiteten.

1. Auswählen Sie auf der Seite  **Profile (Rollen)**  die Zeile für das Profil, das Sie kopieren möchten, und Auswählen Sie anschließend die Aktion  **Profil kopieren** .
2. Füllen Sie die Felder  **Profil-ID**  und  **Anzeigename**  aus und klicken Sie anschließend auf die Schaltfläche  **OK** .
3. Auf der **Profile (Rollen)** Seite, öffnen Sie die neu erstellte Profilkarte und bearbeiten Sie die anderen Felder nach Bedarf.

## <a name="edit-a-profile"></a>Bearbeiten eines Profils

Sie können ein Profil bearbeiten, indem Sie die Felder auf der Seite **Profile (Rollen)** ändern. Die Änderungen sind jedoch für Benutzende, denen das Profil zugewiesen wurde, erst nach dem Abmelden und Wiedereintritt sichtbar.

> [!Caution]
> Benennen Sie ein Profil nicht um, während die Benutzer, denen das Profil zugewiesen wurde, angemeldet sind, da es bei Benutzern zu einem Einfrieren des Produkts kommen kann und ein Neustart erforderlich ist.

## <a name="assign-a-profile-to-a-user"></a>Einem Benutzer ein Profil zuweisen

Benutzer können sich selbst eine Rolle zuweisen (die ein Profil darstellt), indem Sie das Feld **Rolle** auf der Seite **Meine Einstellungen** auswählen. Als Administrator können Sie dasselbe über die Seite **Profile (Rollen)** tun.

1. Wählen Sie auf der Seite  **Profile (Rollen)**  das Profil aus, das Sie zuweisen möchten, und wählen Sie anschließend die Aktion  **Benutzerpersonalisierungsliste**  aus.
2. Wählen Sie auf der Seite  **Benutzereinstellungen**  den Benutzer aus, dem Sie das Profil zuweisen möchten, und führen Sie anschließend die Aktion  **Bearbeiten**  aus.
3. In dem **Profil ID** Feld wählen Sie das entsprechende Profil aus.

Wenn Sie einem Benutzer ein anderes Profil zuweisen, bleiben alle vom Benutzer mit dem vorherigen Profil vorgenommenen Personalisierungen erhalten.

## <a name="define-user-settings-for-a-profile"></a>Definieren von Benutzereinstellungen für ein Profil

Auf der Seite **Meine Einstellungen** können Benutzer das grundlegende Verhalten ihres Kontos definieren, z. B. das Rollencenter, die Sprache und die Benachrichtigungen, die sie erhalten. Weitere Informationen zu Benutzereinstellungen finden Sie unter [Grundeinstellungen ändern](ui-change-basic-settings.md).

Als Administrator können Sie die Einstellungen für ein Profil definieren. Die Einstellungen gelten für alle Benutzenden, die der Rolle zugewiesen sind.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **Profile (Rollen)** ein und Auswählen dann das zugehörige verknüpfen.
2. Auswählen die Zeile für das Profil, für das Sie die Benutzereinstellungen ändern möchten, und Auswählen dann die Aktion  **Liste der Benutzerpersonalisierungen** .
3. Auf der Seite **Benutzeranpassungen** öffnen Sie die Karte für den Benutzer, dessen Einstellungen Sie ändern möchten.
4. Füllen Sie auf der Seite **Benutzerpersonalisierungskarte** die Felder nach Bedarf aus.

## <a name="activate-a-profile"></a>Aktivieren eines Profils

Wenn Sie ein Profil erstellen, können Sie definieren, ob, wo und wie das Profil und seine Informationen den Benutzern zur Verfügung gestellt werden.

Aktivieren Sie auf der Seite **Profile (Rollen)** die folgenden Kontrollkästchen:

* **aktiviert** um anzugeben, ob die zugehörige Rolle in der Liste angezeigt wird **Verfügbare Rollen** Seite für Benutzer zur Auswahl.  
* **Als Standardprofil verwenden** um das Profil anzugeben, das für Benutzende gilt, denen keine bestimmte Rolle zugewiesen wurde.
* **Deaktivieren Sie die Personalisierung** um anzugeben, ob Benutzer der entsprechenden Rolle ihren Arbeitsbereich personalisieren können.
* **Zeige im Rollen-Explorer**, um festzulegen, ob Aktionen für Geschäftsfunktionen, die im Profil enthalten sind, in der erweiterten Ansicht des Rollen-Explorers, einer Feature-Übersicht, angezeigt werden. Weitere Informationen über den Rollen-Explorer finden Sie unter [Suche nach Seiten mit dem Rollen-Explorer](ui-role-explorer.md).

## <a name="export-profiles"></a>Profile exportieren

Sie können Profile aus [!INCLUDE[prod_short](includes/prod_short.md)] exportieren und in einem anderen Mandanten wiederzuverwenden. Die Profile werden in eine ZIP-Datei exportiert, die Applikationssprachendateien (AL-Dateien) enthält. Sie können die .al-Dateien zum Entwickeln von Erweiterungen wiederverwenden. Weitere Informationen zum Exportieren von Profilen finden Sie unter [Client zum Erstellen von Profilen und Seitenanpassungen verwenden](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Führen Sie auf der Seite  **Profile (Rollen)**  die Aktion  **Profile exportieren**  aus.

    Diese Aktion exportiert eine .zip-Datei, die .al-Dateien für alle Profile enthält.

## <a name="import-profiles"></a>Profile importieren

Sie können Profile importieren, die aus Business Central exportiert wurden. Die Schritte sind mehr oder weniger das Gegenteil der Schritte zum Exportieren von Profilen.

1. Führen Sie auf der Seite  **Profile (Rollen)**  die Aktion  **Profile importieren** Auswählen aus.
1. Folgen Sie den Schritten des Assistenten **Importprofile**.

    Wenn Sie nur ausgewählte Profile importieren möchten, verwenden Sie das Kontrollkästchen **Ausgewählt**, um anzugeben, welche importiert werden sollen.
1. Auswählen die Schaltfläche  **Ausgewählte importieren** .

    Diese Aktion importiert eine .zip-Datei, die die .al-Dateien der ausgewählten Profile enthält.

## <a name="delete-a-profile"></a>Löschen eines Profils

Sie können ein Profil löschen, indem Sie auf die Schaltfläche **Löschen** klicken auf der **Profile (Rollen)** Seite. Es gelten jedoch folgende Einschränkungen:

* Sie können ein Profil, das Benutzenden oder einer Benutzergruppe zugeordnet ist, nicht löschen.
* Sie können keine Profile löschen, die aus Erweiterungen stammen. Die Erweiterung muss zuerst deinstalliert werden.
* Sie können nur je ein Profil gleichzeitig löschen.

## <a name="delete-personalizations"></a>Personalisierungen löschen

### <a name="delete-all-personalizations-made-by-a-specific-user"></a>Alle von einem bestimmten Benutzer vorgenommenen Personalisierungen löschen

Sie können alle Änderungen löschen, die ein Benutzer an Seiten vornimmt, wodurch die Seiten auf den ursprünglichen Zustand Layout zurückgesetzt werden. Personalisierungen sind keinem Profil (einer Rolle) zugeordnet. Wenn ein Benutzer eine Seite personalisiert, erlebt er die Personalisierungen auf der Seite, unabhängig davon, welche Rolle er verwendet.<!--Deleting changes can be useful, for example, if an employee changes role and no longer needs them. The profile defines the page layout and deletions restore it back to that definition.--> 

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **Benutzereinstellungen** ein und Auswählen dann das zugehörige verknüpfen.

    Auf der Seite  **Benutzereinstellungen**  sind alle Benutzer aufgelistet.<!--who make personalizations-->.

2. Auswählen der Benutzer, dessen Personalisierungen Sie löschen möchten.
3. Führen Sie auf der Seite  **Benutzereinstellungen** Karte Auswählen die Aktion  **Personalisierte Seiten löschen**  aus und akzeptieren Sie anschließend die angezeigte Meldung.

Der Benutzer sieht die Änderungen bei der nächsten Anmeldung.

Sie können auch alle Seitenanpassungen für ein Profil löschen. Weitere Informationen finden Sie unter [So löschen Sie alle Anpassungen für ein Profil](ui-personalization-manage.md#delete-all-customizations-for-a-profile).

### <a name="delete-personalizations-for-specific-pages"></a>Personalisierungen für bestimmte Seiten löschen

Sie können Personalisierungen löschen, die ein oder mehrere Benutzende an bestimmten Seiten vorgenommen haben. Das Löschen von Personalisierungen ist nützlich, wenn beispielsweise ein geänderter Geschäftsprozess dazu führt, dass eine Personalisierung nicht mehr verwendet werden kann. Durch das Wiederherstellen wird das Seitenlayout wieder auf das im Profil festgelegte Layout zurückgesetzt.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie  **Personalisierte Seiten** ein und Auswählen dann das zugehörige verknüpfen.

    Auf der Seite  **Personalisierte Seiten**  werden alle personalisierten Seiten und der Benutzer aufgelistet, zu dem sie gehören.

    <!--A checkmark in the **Legacy Personalization** field indicates that the personalization was done in an older version of [!INCLUDE[prod_short](includes/prod_short.md)], which handled personalization differently. Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.-->

2. Auswählen die Zeile für die Seitenpersonalisierung, die Sie löschen möchten, und Auswählen dann die Aktion  **Löschen** .

Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.  

Sie können auch alle individuellen Seitenanpassungen für ein Profil löschen. Weitere Informationen finden Sie unter [So löschen Sie alle Anpassungen für eine bestimmte Seite für ein Profil](ui-personalization-manage.md#delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Verwalten von Benutzersitzungen

Als Administrator von [!INCLUDE[prod_short](includes/prod_short.md)] Online können Sie Benutzersitzungen im Administration Center verwalten. Weitere Informationen finden Sie unter [Sitzungen verwalten][def] im Verwaltungsinhalt.  

Für [!INCLUDE[prod_short](includes/prod_short.md)] (lokal) können Sie Sitzungen beispielsweise mit SQL Server Management Studio verwalten. Weitere Informationen finden Sie unter [Technische Dokumentation zu SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Siehe auch

[Benutzer*innen und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md)  
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

[def]: /dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions
