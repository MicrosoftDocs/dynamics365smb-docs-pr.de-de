---
title: Mit Microsoft Dataverse verbinden (enthält Video)
description: 'Legen Sie eine Verbindung zwischen Business Central und Dataverse fest. Unternehmen erstellen die Verbindung normalerweise, um Daten mit einer anderen Dynamics 365 Business App zu integrieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 02/28/2024
ms.service: dynamics-365-business-central
---
# Mit Microsoft Dataverse verbinden

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

In diesem Artikel wird beschrieben, wie Sie eine Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einrichten. Typischerweise stellen Unternehmen die Verbindung her, um Daten mit einer anderen Dynamics 365-Geschäftsanwendung, z. B. [!INCLUDE[crm_md](includes/crm_md.md)], zu integrieren und zu synchronisieren.  

## Bevor Sie beginnen

Sie müssen einige Informationen bereithalten, bevor Sie die Verbindung herstellen:  

* Die URL für die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung, mit der Sie eine Verbindung herstellen möchten. Wenn Sie die unterstützte Anleitung zur **Dataverse-Verbindungseinrichtung** zum Herstellen der Verbindung verwenden, werden wir Ihre Umgebungen ermitteln. Sie können auch die URL einer anderen Umgebung in Ihrem Mandanten eingeben.  
* Der Benutzername und das Passwort eines Kontos, das über Administratorberechtigungen in [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verfügt.  
* Wenn Sie eine lokale [!INCLUDE[prod_short](includes/prod_short.md)] 2020 Veröffentlichungszyklus 1, Version 16.5 haben, lesen Sie den Artikel zu [Einige bekannte Probleme](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Sie müssen die beschriebene Problemumgehung ausführen, bevor Sie eine Verbindung zu [!INCLUDE[cds_long_md](includes/cds_long_md.md)] herstellen können.
* Die lokalen Währungen, die jedes Unternehmen verwendet. [!INCLUDE [prod_short](includes/prod_short.md)]-Unternehmen können sich mit einer [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Umgebung verbinden, die eine andere Basiswährung als ihre Landeswährung hat. Weitere Informationen zum Umgang mit der Einrichtung mehrerer Währungen finden Sie unter [Für verschiedene Währungen zulassen](#allow-for-different-currencies).

> [!IMPORTANT]
> Ihre [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung darf sich nicht im Administrationsmodus befinden. Der Administrationsmodus führt dazu, dass die Verbindung fehlschlägt, da das Integrationsbenutzerkonto für die Verbindung keine Administratorrechte besitzt. Weitere Informationen finden Sie unter [Verwaltungsmodus](/power-platform/admin/admin-mode).

> [!Note]
> Diese Schritte beschreiben das Verfahren in [!INCLUDE[prod_short](includes/prod_short.md)] online.
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal und nicht das Microsoft Entra Konto verwenden, um die Verbindung mit [!INCLUDE [cds_long_md](includes/cds_long_md.md)] herzustellen, müssen Sie außerdem einen Benutzernamen und ein Kennwort eines Benutzerkontos für die Integration angeben. Dieses Konto wird als „Integrationsbenutzer“-Konto bezeichnet. Wenn Sie ein Microsoft Entra-Konto verwenden, ist das Integrationsbenutzerkonto weder erforderlich noch wird es angezeigt. Der Integrationsbenutzer wird automatisch eingerichtet und benötigt keine Lizenz.

## Ihre Business Central- und Dataverse-Umgebungen verknüpfen

Unternehmen möchten ihre Daten innerhalb ihrer Datenschutzgrenzen sicher aufbewahren, insbesondere wenn ihre betriebswirtschaftliche Anwendung in andere Apps integriert ist. Durch die Verknüpfung von [!INCLUDE [prod_short](includes/prod_short.md)]- und [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebungen erfüllen Sie nicht nur diese Anforderungen, sondern bieten Ihren Administrierenden auch eine einfachere Möglichkeit, Ihre Integrationen mit anderen Dynamics 365-Apps zu erstellen und zu verwalten.

Im [!INCLUDE [prod_short](includes/prod_short.md)] Admin Center können Sie Ihre [!INCLUDE [prod_short](includes/prod_short.md)]-Umgebung mit Ihrer [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Umgebung verknüpfen. [!INCLUDE [prod_short](includes/prod_short.md)] kann die Informationen aus dem Link verwenden, um die Integration mit anderen Dynamics 365-Apps, wie etwa Sales und Field Service, einfacher und sicherer zu gestalten. Beispielsweise ist die verknüpfte [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Umgebungs-URL standardmäßig auf der Seite **Dataverse-Verbindungseinrichtung** verfügbar und wenn Sie die Anleitung für die unterstützte **Dataverse-Verbindungseinrichtung** ausführen.

## Für verschiedene Währungen zulassen

[!INCLUDE [prod_short](includes/prod_short.md)]-Unternehmen können sich mit einer [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Umgebung verbinden, die eine andere Basiswährung als ihre Landeswährung hat.

> [!NOTE]
> Für die Synchronisierung mehrerer Währungen ist eine unidirektionale Synchronisierung von [!INCLUDE [prod_short](includes/prod_short.md)] bis [!INCLUDE [cds_long_md](includes/cds_long_md.md)] erforderlich.

Um mehr über die Basiswährung in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] zu erfahren, gehen Sie zu [Entität der Transaktionswährung (Währung)](/powerapps/developer/data-platform/transaction-currency-currency-entity). 

Um mehr über die Währungen in [!INCLUDE [prod_short](includes/prod_short.md)] zu erfahren, gehen Sie zu [Währungen in Business Central](finance-currencies.md).

Um unterschiedliche Währungen zu ermöglichen, stellen Sie vor dem Herstellen einer Verbindung sicher, dass Sie die folgenden Einstellungen angegeben haben:

* Die Einstellung der Basistransaktionswährung in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] hat den Währungscode, der auf der Seite **Währungen** in [!INCLUDE [prod_short](includes/prod_short.md)] angegeben ist.
* Für die Währung [!INCLUDE [prod_short](includes/prod_short.md)] ist auf der Seite **Währungswechselkurse** mindestens ein Wechselkurs angegeben.

Wenn Sie die Verbindung zu [!INCLUDE [cds_long_md](includes/cds_long_md.md)] aktivieren, fügt [!INCLUDE [prod_short](includes/prod_short.md)] seine Hauswährung der **Währung**-Entität in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] hinzu. Die lokale Währung verwendet den Wechselkurs aus dem Feld **Währungsfaktor** auf der Seite **Währungswechselkurse**.

Da die Währungssynchronisierung unidirektional von [!INCLUDE [prod_short](includes/prod_short.md)] an [!INCLUDE [cds_long_md](includes/cds_long_md.md)] erfolgt, werden Geldbeträge wie folgt konvertiert und synchronisiert:

* Beträge in der [!INCLUDE [cds_long_md](includes/cds_long_md.md)] Basiswährung werden basierend auf dem letzten synchronisierten Wechselkurs von [!INCLUDE [prod_short](includes/prod_short.md)] in die [!INCLUDE [prod_short](includes/prod_short.md)] lokale Währung umgerechnet.
* Beträge in der [!INCLUDE [prod_short](includes/prod_short.md)] lokalen Währung werden mit der [!INCLUDE [prod_short](includes/prod_short.md)] lokalen Währung in einer der anderen (nicht Basis-)Währungen in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] synchronisiert.

## Verbindung zu [!INCLUDE[cds_long_md](includes/cds_long_md.md)] einrichten

Für alle anderen Authentifizierungsarten als die Microsoft 365-Authentifizierung legen Sie Ihre Verbindung auf der Seite **Dataverse Verbindungseinrichtung** auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)] fest. Für die Microsoft 365-Authentifizierung empfehlen wir Ihnen, die Anleitung **Dataverse Verbindungseinrichtung** zur unterstützten Einrichtung zu verwenden. Der Leitfaden erleichtert die Einrichtung der Verbindung und die Festlegung erweiterter Funktionen, wie z. B. Personenbesitz und Erstsynchronisierung.  

> [!IMPORTANT]
> Während der Einrichtung der Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] wird der Administrator aufgefordert, der registrierten Azure-Anwendung mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)] Integration für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu erteilen:
>
> * Die Berechtigung **Auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zugreifen** ist erforderlich, damit [!INCLUDE[prod_short](includes/prod_short.md)] im Namen des Administrators automatisch einen nicht lizenzierten, nicht interaktiven Benutzer der Anwendung [!INCLUDE[prod_short](includes/prod_short.md)] Integration erstellen, diesem Benutzer Sicherheitsrollen zuweisen und [!INCLUDE[prod_short](includes/prod_short.md)] Integration Solution für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] bereitstellen kann. Diese Berechtigung wird nur einmal beim Einrichten der Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verwendet.  
> * Die Berechtigung **Vollzugriff auf Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** ist erforderlich, damit automatisch erstellte Benutzer der Anwendung [!INCLUDE[prod_short](includes/prod_short.md)] Integration auf [!INCLUDE[prod_short](includes/prod_short.md)]-Daten zugreifen können, die synchronisiert werden.  
> * Die Berechtigung **Anmelden und Ihr Profil lesen** ist erforderlich, um zu überprüfen, ob dem Benutzer, der sich anmeldet, tatsächlich die Sicherheitsrolle „Systemadministrator“ in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zugewiesen ist.  
>
> Durch die Einwilligung im Namen der Organisation berechtigt der Administrator die registrierte Azure-Anwendung mit dem Namen [!INCLUDE[prod_short](includes/prod_short.md)] Integration für [!INCLUDE[cds_long_md](includes/cds_long_md.md)], Daten mit automatisch erstellten Anmeldeinformationen des Benutzers der Anwendung [!INCLUDE[prod_short](includes/prod_short.md)] zu synchronisieren.

### So verwenden Sie die Dataverse Anleitung zur unterstützten Einrichtung

Die Anleitung zur unterstützten Einrichtung für die Verbindung von Dataverse kann Ihnen helfen, die Verbindung einfacher herzustelle und Sie kann Ihnen sogar beim Ausführen einer ersten Synchronisierung helfen. Wenn Sie die anfängliche Synchronisierung ausführen möchten, überprüft [!INCLUDE[prod_short](includes/prod_short.md)] die Daten in beiden Anwendungen und gibt Empfehlungen für die anfängliche Synchronisierung. Die folgende Tabelle beschreibt die Empfehlungen.

|Empfehlung  |Beschreibung  |
|---------|---------|
|**Vollständige Synchronisierung**|Daten existieren nur in [!INCLUDE[prod_short](includes/prod_short.md)] oder nur in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Die Empfehlung lautet, alle Daten des Dienstes, der sie hat, mit dem anderen Dienst zu synchronisieren.|
|**Keine Synchronisation**|Daten sind in beiden Anwendungen vorhanden, und eine vollständige Synchronisierung würde die Daten duplizieren. Die Empfehlung ist, Datensätze zu koppeln.|
|**Abhängigkeit nicht erfüllt**|Daten sind in beiden Anwendungen vorhanden, aber die Zeile oder Tabelle kann nicht synchronisiert werden, da dies von einer Zeile oder Tabelle abhängt, für die die Empfehlung Keine Synchronisierung gilt. Wenn beispielsweise Kunden nicht synchronisiert werden können, können auch Daten für Kontakte, die von den Kundendaten abhängen, nicht synchronisiert werden.|

> [!IMPORTANT]
> In der Regel verwenden Sie die vollständige Synchronisierung nur, wenn Sie die Anwendungen zum ersten Mal integrieren, und nur eine Anwendung enthält Daten. Eine vollständige Synchronisierung kann in einer Demonstrationsumgebung hilfreich sein, da in jeder Anwendung automatisch Datensätze erstellt und gekoppelt werden, wodurch die Arbeit mit synchronisierten Daten beschleunigt wird. Sie sollten die vollständige Synchronisierung jedoch nur ausführen, wenn Sie eine Zeile in [!INCLUDE[prod_short](includes/prod_short.md)] für jede Zeile in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] für die Tabellenzuordnungen möchten. Andernfalls kann das Ergebnis doppelte Datensätze sein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Unterstützte Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Eine Verbindung zu Microsoft Dataverse** einrichten, um das Leitfaden für das unterstützte Setup zu starten.
3. Füllen Sie die Felder nach Bedarf aus.

> [!NOTE]
> Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass die Popups blockiert sind. Erlauben Sie Popups von `https://login.microsoftonline.com`, um sich anzumelden.

### So erstellen oder pflegen Sie den Link manuell

Die folgende Prozedur beschreibt, wie die Verbindung auf der Seite **Dataverse Verbindungs-Einrichtung** manuell eingerichtet wird. Auf der Seite **Dataverse-Verbindungseinrichtung** verwalten Sie die Integrationseinstellungen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Dataverse Einrichtung der Verbindung** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ein.

    |Feld|Beschreibung|
    |-----|-----|
    |**Umgebungs-URL**|Wenn Sie Umgebungen in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] besitzen, werden wir diese für Sie finden, wenn Sie den Einrichtungsleitfaden ausführen. Wenn Sie eine Verbindung zu einer anderen Umgebung in einem anderen Mandanten herstellen möchten, können Sie die Administrator-Zugangsdaten für die Umgebung eingeben, und wir werden diese ermitteln. |
    |**Aktiviert**|Beginnen Sie mit der Verwendung der Integration. Wenn Sie die Verbindung nicht sofort aktivieren, werden die Verbindungseinstellungen gespeichert, aber Benutzer können nicht von [!INCLUDE[prod_short](includes/prod_short.md)] aus auf [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Daten zugreifen. Sie können zu dieser Seite zurückkehren und die Verbindung später aktivieren.  |

3. Wählen Sie im Feld **Eigentümermodell** aus, ob Sie möchten, dass eine Team-Tabelle in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] neue Datensätze oder ein oder mehrere bestimmte Benutzer besitzen soll. Wenn Sie **Person** wählen, müssen Sie jeden Benutzer angeben. Wenn Sie **Team** wählen, wird die Standard-Geschäftseinheit im Feld **Gekoppelte Geschäftseinheit** angezeigt.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Um die Verbindungseinstellungen zu testen, wählen Sie **Verbindung**, und dann **Verbindung testen**.  

    > [!NOTE]  
    > Wenn keine Datenverschlüsselung in [!INCLUDE[prod_short](includes/prod_short.md)] aktiviert ist, werden Sie gefragt, ob sie diese aktivieren möchten. Um Datenverschlüsselung zu aktivieren, wählen Sie **Ja** aus, und stellen Sie die erforderlichen Informationen bereit. Anderenfalls wählen Sie **Nein** aus. Sie können die Datenverschlüsselung später aktivieren. Weitere Informationen finden Sie unter [Verschlüsseln von Daten in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in der Hilfe für Entwickler und die Verwaltung.  
5. Wenn die [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Synchronisierung nicht bereits eingerichtet ist, werden Sie gefragt, ob Sie die Standardsynchronisierungskonfiguration verwenden möchten. Abhängig davon, ob Sie Datensätze in [!INCLUDE[cds_long_md](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] angepasst bleiben sollen, wählen Sie **Ja** oder **Nein** aus.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## Kopplung basierend auf Übereinstimmung anpassen

Ab dem Veröffentlichungszyklus 2 im Jahr 2021 kann ein Administrtator Kriterien zum Koppeln von Datensätzen auf der Grundlage von Übereinstimmungen eingeben. Sie können den Algorithmus für den Abgleich von Datensätzen an den folgenden Stellen in [!INCLUDE [prod_short](includes/prod_short.md)] starten:

* Listenseiten, die Datensätze anzeigen, die mit [!INCLUDE [cds_long_md](includes/cds_long_md.md)] synchronisiert sind, wie z.B. die Seiten Kunden und Artikel.  

    Markieren Sie mehrere Datensätze und wählen Sie dann die Aktion **Bezogen**, wählen Sie **Dataverse**, wählen Sie **Koppeln** und dann **Abgleichsbasiertes Koppeln**.

    Wenn Sie den abgleichsbasierten Kopplungsprozess von einer Stammdatenliste aus starten, wird ein Kopplungsauftrag nach der Festlegung der Kopplungskriterien geplant.  
* Die **Dataverse Full Synch. Überprüfung** Seite.  

    Wenn der Vollsynchronisationsprozess nicht gekoppelte Datensätze in [!INCLUDE [prod_short](includes/prod_short.md)] und in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] erkennt, wird der Link **Kopplungskriterien auswählen** für die entsprechende Integrationstabelle angezeigt.  

    Sie können den Prozess **Vollständige Synchronisierung ausführen** auf den Seiten **Dataverse-Verbindungseinrichtung** und **Dynamics 365-Verbindungseinrichtung** starten. Sie können ihn auch in der unterstützten Einrichtungsanleitung **Verbindung zu Dataverse einrichten** starten, wenn Sie die Einrichtung abgeschlossen haben.  

    Wenn Sie den abgleichsbasierten Kopplungsprozess auf der Seite **Bewertung der vollständigen Dataverse-Synchronisierung** starten, wird nach Abschluss der Einrichtung ein Kopplungsauftrag geplant.  
* Die Liste **Integrationstabellenzuordnungen**.  

    Markieren Sie eine Zuordnung, wählen Sie die Aktion **Koppeln** und dann **Abgleichsbasierte Kopplung**.

    Wenn Sie den abgleichsbasierten Kopplungsprozess über eine Integrationstabellenzuordnung starten, wird ein Kopplungsauftrag für alle nicht gekoppelten Datensätze in der Zuordnung ausgeführt. Sie können auch nicht gekoppelte Datensätze aus der Liste auswählen, um das Projekt nur für diese Datensätze auszuführen.

In allen drei Fällen öffnet sich die Seite **Kopplungskriterien auswählen**, auf der Sie die entsprechenden Kopplungskriterien festlegen können. Auf dieser Seite können Sie die Kopplung mit den folgenden Aufgaben anpassen:

* Wählen Sie die Felder aus, die für den Abgleich der [!INCLUDE [prod_short](includes/prod_short.md)]-Datensätz mit [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Entitäten verwendet werden sollen. Sie können festlegen, ob beim Abgleich zwischen Groß- und Kleinschreibung unterschieden werden soll.  

* Geben Sie an, ob nach dem Koppeln von Datensätzen eine Synchronisierung erfolgen soll. Wenn Datensätze eine bidirektionale Zuordnung verwenden, können Sie auch festlegen, was geschieht, wenn Konflikte auf der Seite **Aktualisierungskonflikte auflösen** aufgelistet sind.  

* Legen Sie die Reihenfolge fest, in der die Datensätze durchsucht werden, indem Sie eine *Übereinstimmungspriorität* für die entsprechenden Zuordnungsfelder angeben. [!INCLUDE [prod_short](includes/prod_short.md)] sucht basierend auf dem Wert im Feld **Übereinstimmungspriorität** in aufsteigender Reihenfolge nach einer Übereinstimmung. Ein leerer Wert im Feld **Übereinstimmungspriorität** ist gleich der Priorität 0, bei der es sich um die höchste Priorität handelt. Felder mit der Priorität 0 werden zuerst berücksichtigt.  

* Legen Sie fest, ob eine neue Entitätsinstanz in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] erstellt werden soll, falls anhand der Abgleichskriterien keine eindeutige, ungekoppelte Übereinstimmung gefunden werden kann. Um diese Funktionalität zu aktivieren, wählen Sie die Aktion **Neu erstellen, wenn keine Übereinstimmung gefunden werden kann**.  

### Anzeigen der Ergebnisse des Kopplungsauftrags

Um die Ergebnisse des Kopplungsauftrags anzuzeigen, öffnen Sie die Seite **Integrationstabellenzuordnungen**, wählen Sie die entsprechende Zuordnung aus, wählen Sie die Aktion **Kopplung** und dann die Aktion **Protokoll des Kopplungsauftrags**.  

Wenn Datensätze nicht gekoppelt werden konnten, können Sie den Wert in der Spalte **Fehler** auswählen, um eine Liste mit Fehlern zu öffnen, die den Grund für deren Auftreten beschreiben.  

Die Kopplung schlägt in der Regel aus folgenden Gründen fehl:

* Es wurden keine passenden Kriterien definiert

    Führen Sie die abgleichsbasierte Kopplung erneut aus, aber denken Sie daran, Kopplungskriterien zu definieren.

* Für die in den Abgleichskriterien angegebenen Felder wurde keine Übereinstimmung gefunden.

    Wiederholen Sie die Kopplung mit verschiedenen Feldern.

* Für mehrere Datensätze wurden basierend auf den in den Abgleichskriterien angegebenen Feldern mehrere Übereinstimmungen gefunden.  

    Wiederholen Sie die Kopplung mit verschiedenen Feldern.

* Es wurde eine Übereinstimmung gefunden, aber der Datensatz ist bereits mit einem Datensatz in [!INCLUDE [prod_short](includes/prod_short.md)] gekoppelt.  

    Wiederholen Sie die Kopplung mit verschiedenen Feldern, oder untersuchen Sie, warum die [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Entität mit dem Datensatz in [!INCLUDE [prod_short](includes/prod_short.md)] gekoppelt ist.

> [!TIP]
> Damit Sie sich einen Überblick über den Fortschritt der Kopplung verschaffen können, zeigt das Feld **Gekoppelt mit Dataverse** an, ob ein Datensatz mit einer [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-Entität gekoppelt ist. Sie können die Liste der zu synchronisierenden Datensätze mit dem Feld **Gekoppelt mit Dataverse** filtern.

## Verbindungen von Business Central Online zur Verwendung der zertifikatsbasierten Authentifizierung upgraden

> [!NOTE]
> Dieser Abschnitt ist nur für [!INCLUDE[prod_short](includes/prod_short.md)] Online-Mandanten relevant, die von Microsoft gehostet werden. Online-Mandanten, die von ISVs gehostet werden, und lokale Installationen sind davon nicht betroffen.

Im April 2022 wird der Office365-Authentifizierungstyp (Benutzername/Kennwort) nicht mehr von [!INCLUDE[cds_long_md](includes/cds_long_md.md)] unterstützt. Weitere Informationen finden Sie unter [Abkündigung des Office365-Authentifizierungstyps](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). Außerdem wird im März 2022 die Verwendung der Client-Geheimnis-basierten Service-to-Service-Authentifizierung für Online-Mandanten von [!INCLUDE[prod_short](includes/prod_short.md)] nicht mehr unterstützt. Sie müssen die zertifikatsbasierten Service-to-Service-Authentifizierung für Verbindungen mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] verwenden. [!INCLUDE[prod_short](includes/prod_short.md)] Online-Mandanten, die von ISVs gehostet werden, und lokale Installationen können weiterhin den geheimen Clientschlüssel für die Authentifizierung verwenden.

Um eine Unterbrechung der Integrationen zu vermeiden, _müssen Sie die Verbindung auf die Verwendung der zertifikatsbasierten Authentifizierung umstellen_. Obwohl die Umstellung für März 2022 geplant ist, empfehlen wir Ihnen dringend, das Upgrade so bald wie möglich durchzuführen. Die folgenden Schritte beschreiben, wie Sie ein Upgrade auf zertifikatsbasierte Authentifizierung durchführen. 

### So aktualisieren Sie Ihre Business Central Online-Verbindung, um die zertifikatsbasierte Authentifizierung zu verwenden

1. Je nachdem, ob Sie mit Dynamics 365 Sales integriert sind, führen Sie einen der folgenden Schritte aus:
   * Wenn ja, öffnen Sie die Seite **Microsoft Dynamics 365 Verbindungseinrichtung**.
   * Wenn nicht, öffnen Sie die Seite **Dataverse Einrichtung der Verbindung**.
2. Wählen Sie **Verbindung** und dann **Zertifikatsauthentifizierung verwenden**, um die Verbindung auf die Verwendung einer zertifikatsbasierten Authentifizierung umzustellen.
3. Melden Sie sich mit den Anmeldeinformationen des Administrators für Dataverse an. Die Anmeldung sollte weniger als eine Minute dauern.

> [!NOTE]
> Sie müssen diese Schritte in jeder [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung wiederholen, einschließlich der Produktions- und Sandbox-Umgebungen, und in jeder Firma, in der Sie eine Verbindung zu [!INCLUDE[cds_long_md](includes/cds_long_md.md)] haben.

## Verbinden von lokalen Versionen

Sie müssen einige Informationen auf der Seite **Dataverse-Verbindungseinrichtung** eingeben, um [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu verbinden.

Um eine Verbindung mit einem Microsoft Entra-Konto herzustellen, müssen Sie eine Anwendung als Microsoft Entra-ID registrieren. Sie müssen die Anwendungs-ID, das Geheimnis des Schlüsseltresors und die Umleitungs-URL angeben. Die Umleitungs-URL ist bereits ausgefüllt und sollte für die meisten Installationen funktionieren. Sie müssen Ihre Installation für die Verwendung von HTTPS einrichten. Weitere Informationen finden Sie unter [Konfigurieren von SSL zum Sichern der Business Central Web Client-Verbindung](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Wenn Sie Ihren Server für eine andere Homepage einrichten, können Sie die URL jederzeit ändern. Der geheime Clientschlüssel wird als verschlüsselte Zeichenfolge in Ihrer Datenbank gespeichert. 

### So registrieren Sie eine Anwendung in Microsoft Entra-ID, um eine Verbindung mit Dataverse über Business Central herzustellen

Bei den folgenden Schritten wird davon ausgegangen, dass Sie Microsoft Entra-ID verwenden, um Identitäten und den Zugriff zu verwalten. Weitere Informationen zum Registrieren einer Anwendung in Microsoft Entra-ID finden Sie unter [Schnellstart: Anwendung bei der Microsoft-Identitätsplattform registrieren](/azure/active-directory/develop/quickstart-register-app). 

1. Wählen Sie im Navigationsbereich von Azure-Portal unter **Verwalten** die Option **Authentifizierung** aus.  
2. Fügen Sie unter **URLs umleiten** die Umleitungs-URL hinzu, die auf der Seite **Dataverse-Verbindungseinrichtung** in [!INCLUDE[prod_short](includes/prod_short.md)] vorgeschlagen wird.
3. Wählen Sie unter **Verwalten** die Option **API-Berechtigungen** aus.
4. Wählen Sie unter **Konfigurierte Berechtigungen** die Option **Berechtigung hinzufügen** aus, und fügen Sie anschließen der Registerkarte **Microsoft APIs** delegierte Berechtigungen hinzu:
    * Fügen Sie für Business Central die **Financials.ReadWrite.All**-Berechtigungen hinzu.
    * Fügen Sie für Dynamics CRM die **user_impersonation**-Berechtigungen hinzu.  

    > [!NOTE]
    > Der Name der Dynamics CRM-API kann sich ändern.

5. Wählen Sie unter **Verwalten** die Option **Zertifikate & Geheimnisse** aus, und erstellen Sie dann einen neuen geheimen Schlüssel für Ihre App. Sie verwenden den geheimen Schlüssel in [!INCLUDE[prod_short](includes/prod_short.md)], im Feld **Geheimer Clientschlüssel** auf der Seite **Dataverse-Verbindungseinrichtung**, oder Sie speichern ihn in einem sicheren Speicher und stellen ihn in einem Ereignisabonnenten bereit, wie weiter oben in diesem Thema beschrieben.
6. Wählen Sie **Übersicht** aus, und suchen Sie dann den Wert **Anwendungs-(Client-)ID**. Diese ID ist die Client-ID Ihrer Anwendung. Sie müssen sie auf der Seite **Dataverse-Verbindungseinrichtung** im Feld **Client-ID** eingeben oder in einem sicheren Speicher speichern und in einem Ereignisabonnenten bereitstellen.
7. Geben Sie in [!INCLUDE[prod_short](includes/prod_short.md)] auf der Seite **Dataverse-Verbindungseinrichtung** im Feld **Umgebungs-URL** die URL für Ihre [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung ein.
8. Aktivieren Sie das Kontrollkästchen **Aktiviert**, um die Verbindung mit [!INCLUDE[cds_long_md](includes/cds_long_md.md)] zu aktivieren.
9. Melden Sie sich mit Ihrem Administratorkonto für Microsoft Entra-ID an (dieses Konto muss eine gültige Lizenz für [!INCLUDE[cds_long_md](includes/cds_long_md.md)] haben und ein Administrator in Ihrer [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-Umgebung sein). Nachdem Sie sich angemeldet haben, werden Sie aufgefordert, Ihrer registrierten Anwendung zu erlauben, sich im Namen der Organisation bei [!INCLUDE[cds_long_md](includes/cds_long_md.md)] anzumelden. Sie müssen Ihre Zustimmung geben, um die Einrichtung abzuschließen.

   > [!NOTE]
   > Wenn Sie nicht aufgefordert werden, sich mit Ihrem Administratorkonto anzumelden, liegt dies wahrscheinlich daran, dass Popups blockiert sind. Erlauben Sie Popups von `https://login.microsoftonline.com`, um sich anzumelden.

### So trennen Sie [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Dataverse Einrichtung der Verbindung** ein und wählen Sie dann den zugehörigen Link.
2. Schalten Sie auf der Seite **Dataverse Verbindungseinrichtung** die Umschaltung auf **Aktiviert**.  

## Siehe auch

[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
