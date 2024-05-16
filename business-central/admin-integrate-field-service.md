---
title: In Microsoft Dynamics 365 Field Service integrieren
description: Integrieren Sie Business Central mit Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>In Microsoft Dynamics 365 Field Service integrieren

Serviceorganisationen brauchen eine umfassende Anwendung, bei der Finanzen, Bestand und Beschaffung eng mit der Servicebereitstellung verknüpft sind. Sie generieren mit jeder Transaktion Finanzdaten. Jeder Arbeitsauftrag repräsentiert Kosten und Umsätze und jede Ressource generiert Gewinn und Verlust. Durch Interaktionen mit Debitoren werden Sachposten hinzugefügt. Die Integration von [!INCLUDE [prod_short](includes/prod_short.md)] mit [!INCLUDE [field-service-short](includes/field-service-short.md)] rationalisiert den Ende-zu-Ende-Prozess der Verwaltung von Serviceabläufen und sorgt für einen reibungslosen Informationsfluss zwischen den beiden Systemen.  

Sie können in [!INCLUDE [field-service-short](includes/field-service-short.md)] ganz einfach Arbeitsaufträge erstellen und verwalten, den Fortschritt von Serviceaufgaben nachverfolgen, Ressourcen zuweisen und Verbrauchsinformationen erfassen. Wenn Sie einen Arbeitsauftrag in [!INCLUDE [field-service-short](includes/field-service-short.md)] abschließen, ermöglicht die Integration die reibungslose Übertragung von Daten an [!INCLUDE [prod_short](includes/prod_short.md)] zur weiteren Verarbeitung.  

Die Integration erleichtert auch die Rechnungsstellung und Erfüllung von Arbeitsaufträgen in [!INCLUDE [prod_short](includes/prod_short.md)]. Sie können anhand der in [!INCLUDE [field-service-short](includes/field-service-short.md)] erfassten Serviceaktivitäten und Verbrauchsdaten genaue Rechnungen erstellen.  

Wenn Sie [!INCLUDE [prod_short](includes/prod_short.md)] mit [!INCLUDE [field-service-short](includes/field-service-short.md)] integrieren, müssen Sie Daten nicht manuell eingeben oder weniger Aufgaben doppelt erledigen. Die Integration bietet außerdem einen umfassenden Überblick über Serviceabläufe und Finanzen und führt so zu einer besseren Entscheidungsfindung und betrieblichen Effizienz.

## <a name="prerequisites"></a>Voraussetzungen

Da [!INCLUDE [field-service-short](includes/field-service-short.md)] auf Dynamics 365 Sales aufbaut, müssen Sie [eine Verbindung zu Dataverse einrichten](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) und [die Integration mit Dynamics 365 Sales aktivieren](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### <a name="permissions-and-security-roles-for-user-accounts"></a>Berechtigungen und Sicherheitsrollen für Benutzerkonten

Wenn Sie die Integrationslösung installieren, werden die Berechtigungen für das Integrationsbenutzerkonto konfiguriert. Wenn sich diese Berechtigungen ändern, müssen Sie sie möglicherweise zurücksetzen. Installieren Sie dazu die Integrationslösung von der Seite **Dynamics 365 Verbindungseinrichtung** aus durch Auswahl von **Integrationslösung neu bereitstellen** neu. In den folgenden Abschnitten sind die Berechtigungen und Sicherheitsrollen aufgeführt, welche die Lösung für jede App bereitstellt.

#### <a name="sales"></a>Vertrieb

* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] Integrationsadministrierende
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-Integrationsbenutzender
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-Produktverfügbarkeitsbenutzender

#### <a name="business-central"></a>Business Central

Benutzende, die Projekt-Buch.-Blätter buchen, müssen über die folgenden Berechtigungssätze verfügen:

* Dynamics 365 Sales-Integration

#### <a name="field-service"></a>Field Service

Um die integrierten Daten nutzen zu können, müssen Benutzende über die folgende Sicherheitsrolle verfügen:

* Business Central Field Service-Integration

Benutzende müssen beispielsweise über diese Rolle verfügen, um Arbeitsaufträge zur Verarbeitung mit [!INCLUDE [prod_short](includes/prod_short.md)] verknüpfen zu können.

> [!NOTE]
> Stellen Sie sicher, dass den Benutzenden in [!INCLUDE [field-service-short](includes/field-service-short.md)] die Standardsicherheitsrollen und -profile zugewiesen sind.  
>
> Weitere Informationen zu Spaltensicherheitsprofilen in [!INCLUDE [field-service-short](includes/field-service-short.md)] finden Sie unter [Field Service-Sicherheitsrollen](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Administrierende müssen den Benutzenden in Power Platform eines der entsprechenden Spaltensicherheitsprofile hinzufügen. Weitere Informationen finden Sie unter [Einem Spaltensicherheitsprofil Teams und Benutzende zur Steuerung des Zugriffs hinzufügen](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Um die Aktion **In Business Central öffnen** in Sales verwenden zu können, müssen Sie über die folgenden Berechtigungen für die folgenden Tabellen verfügen:
>
> * Sie müssen über **Leseberechtigungen** für die Tabelle **Dynamics 365 Business Central-Verbindung** (nav_connection) verfügen.
> * Sie müssen über **Lese**-, **Schreib**- und **Löschberechtigungen** für die Tabelle **Dynamics 365 Business Central-Standardverbindung** (nav_defaultconnection) verfügen.

### <a name="other-settings-in-field-service"></a>Weitere Einstellungen in Field Service

Nehmen Sie auf der Seite **Field Service-Einstellungen** die folgenden Änderungen vor:

* Löschen Sie auf der Registerkarte **Einkauf** das Feld **Nicht vorrätiger Produkte verwenden**. Andernfalls erhalten Sie möglicherweise eine „Nicht vorrätig“-Warnung, wenn Sie ein Produkt auswählen, das in [!INCLUDE [field-service-short](includes/field-service-short.md)] nicht vorrätig, in [!INCLUDE [prod_short](includes/prod_short.md)] aber vorrätig ist.
* Deaktivieren Sie auf der Registerkarte **Arbeitsauftrag/Buchung** die Umschalter **Preis berechnen** und **Kosten berechnen**. Wählen Sie im Feld **Rechnungserstellung Arbeitsauftrag** **Nie** aus.

> [!NOTE]
> Durch das Einrichten einer Verbindung zu [!INCLUDE [field-service-short](includes/field-service-short.md)] wird die Kopplung zwischen Ressourcen und Produkten aufgehoben. Um [!INCLUDE [prod_short](includes/prod_short.md)]-Artikel in [!INCLUDE [field-service-short](includes/field-service-short.md)] verfügbar zu machen, aktualisieren Sie das Feld **Field Service-Produkttyp** so, dass es mit dem Feld **Typ** der Artikel in [!INCLUDE [prod_short](includes/prod_short.md)] übereinstimmt. Weitere Informationen finden Sie unter [Produkt oder Service erstellen](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>Die Integration in Business Central einrichten

Nachdem Sie eine Verbindung zu Dataverse und Sales hergestellt haben, können Sie Ihre Integration zu [!INCLUDE [field-service-short](includes/field-service-short.md)] einrichten. Wählen Sie auf der Seite **Unterstützte Einrichtung** in [!INCLUDE [prod_short](includes/prod_short.md)] **Integration zu Dynamics 365 Field Service einrichten** aus, um die Anleitung zur unterstützten Einrichtung auszuführen. In diesem Abschnitt werden die wichtigsten Einstellungen in der Anleitung beschrieben.

Damit Benutzende den Verbrauch von Artikeln und Services in [!INCLUDE [field-service-short](includes/field-service-short.md)]-Arbeitsaufträgen buchen können, geben Sie die **Projekt-Buch.-Blattvorlage** und den **Projekt-Buch.-Blattstapel** an, die zum Buchen des Verbrauchs von Produkten und Services verwendet werden sollen.

Da Services in [!INCLUDE [field-service-short](includes/field-service-short.md)] als Dauer ausgedrückt werden, geben Sie die **Stunden-Maßeinheit** an, die in [!INCLUDE [prod_short](includes/prod_short.md)] zum Umrechnen der Dauer in Mengen verwendet werden soll.

Sie können auch festlegen, wann Arbeitsauftragsprodukt- und servicezeilen mit [!INCLUDE [prod_short](includes/prod_short.md)] synchronisiert werden sollen. Sie können beispielsweise synchronisiert werden, wenn Arbeitsauftragszeilen verwendet werden oder wenn jemand einen Arbeitsauftrag abschließt. Wählen Sie die entsprechende Option im Feld **Synchronisieren von Arbeitsauftragsprodukten/-services**.

Nachdem Arbeitsauftragsprodukte und -services mit Projekt-Buch.-Blättern in [!INCLUDE [prod_short](includes/prod_short.md)] synchronisiert wurden, können Sie auswählen, ob die Projekt.-Buch-Blätter manuell gebucht werden sollen. Wählen Sie im Feld **Projekt-Buch.-Blattpositionen automatisch buchen** die entsprechende Option aus:

* Bei Abschluss eines Arbeitsauftrags.
* Bei Verwendung eines Arbeitsauftragsprodukts oder -services.

Nachdem Sie die Einrichtung abgeschlossen haben, führen Sie eine vollständige Synchronisierung von der Seite **Einrichtung der Dynamics 365 Field Service Integration** aus durch. Diese Aktion synchronisiert Tabellenzuordnungen für Elemente wie:

* Projektaufgaben für Projekte, bei denen **Verbrauchslink standardmäßig anwenden** festgelegt ist. Durch die Synchronisation können [!INCLUDE [prod_short](includes/prod_short.md)]-Projekte in [!INCLUDE [field-service-short](includes/field-service-short.md)] ausgewählt werden.
* Bei Ressourcen, die nicht gesperrt sind, ist **Arbeitszeittabelle verwenden** nicht ausgewählt und auf der Seite **Einrichtung der Dynamics 365 Field Service Integration** ist **Stunden** als Maßeinheit festgelegt.
* Serviceartikel (erfordert die Nutzung der Premium-Umgebung in [!INCLUDE [prod_short](includes/prod_short.md)]).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Field Service-Standard-Entitätszuordnungen für die Synchronisierung

Die Basis für die Synchronisation von Tabellen und Feldern in [!INCLUDE [prod_short](includes/prod_short.md)] mit Tabellen und Spalten in Dataverse, damit Daten ausgetauscht werden können. Die Zuordnung erfolgt über Integrationstabellen. Weitere Informationen zu Tabellenzuordnungen finden Sie unter [Zu synchronisierende Tabellen und Felder zuordnen](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Die Integration mit [!INCLUDE [field-service-short](includes/field-service-short.md)] führt die folgenden Standardzuordnungen für Integrationstabellen ein:

* **PJLINE-WORDERPRODUCT**: Ordnet Arbeitsauftragsprodukte in [!INCLUDE [field-service-short](includes/field-service-short.md)] Projektbuchungsblattzeilen in [!INCLUDE [prod_short](includes/prod_short.md)] zu.
* **PJLINE-WORDERSERVICE**: Ordnet Arbeitsauftragsservices in [!INCLUDE [field-service-short](includes/field-service-short.md)] Projektbuchungsblattzeilen in [!INCLUDE [prod_short](includes/prod_short.md)] zu.
* **PROJECTTASK**: Ordnet Projekte und Projektaufgaben in [!INCLUDE [prod_short](includes/prod_short.md)] Produkten in externen Projekten in [!INCLUDE [field-service-short](includes/field-service-short.md)] zu.
* **RESOURCE-BOOKABLERSC**: Ordnet Ressourcen in [!INCLUDE [prod_short](includes/prod_short.md)] buchbaren Ressourcen in [!INCLUDE [field-service-short](includes/field-service-short.md)] zu.
* **SVCITEM-CUSTASSET** (nur Premium-Umgebung): Ordnet Serviceartikel in [!INCLUDE [prod_short](includes/prod_short.md)] Debitorenanlagen in [!INCLUDE [field-service-short](includes/field-service-short.md)] zu.

## <a name="use-data-in-both-applications"></a>Daten in beiden Anwendungen verwenden

In den folgenden Abschnitten werden die Features beschrieben, bei denen Sie die Daten aus [!INCLUDE [prod_short](includes/prod_short.md)] und [!INCLUDE [field-service-short](includes/field-service-short.md)] verwenden können.

### <a name="field-service-1"></a>Außendienst

Sie können [Arbeitsaufträge erstellen](/dynamics365/field-service/create-work-order), indem Sie das **Dienstkonto** und das **Abrechnungskonto** von [!INCLUDE [prod_short](includes/prod_short.md)] verwenden. Bei Arbeitsaufträgen müssen Sie die **Business Central-Projektaufgabe** im Feld **Externes Projekt** auswählen. Durch Auswahl eines Projekts können Sie Arbeitsauftragsprodukte und -services mit der entsprechenden Projektaufgabe in [!INCLUDE [prod_short](includes/prod_short.md)] synchronisieren.

Sie können Lager und Nichtlagerartikel auf Arbeitsaufträgen als **Arbeitsauftragsprodukte** hinzufügen und die vorhandene Menge sowie die Kosten und Preise aus [!INCLUDE [prod_short](includes/prod_short.md)] abrufen. Weitere Informationen finden Sie unter [Arbeitsauftrag aus dem Arbeitsauftragsformular und der Datensatzliste erstellen](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Sie können Artikel des Typs „Service“ als **Arbeitsauftragsservices** hinzufügen und die Kosten und Preise aus [!INCLUDE [prod_short](includes/prod_short.md)] abrufen. Weitere Informationen finden Sie auf der Registerkarte [Produkte und Services](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Wenn sich der Status eines Produkts oder eines Services in einem Arbeitsauftrag von **Geschätzt** auf **Gebraucht** in [!INCLUDE [field-service-short](includes/field-service-short.md)] ändert, wird dies mit den Projektbuchungsblattzeilen in [!INCLUDE [prod_short](includes/prod_short.md)] synchronisiert.

Sie können eine Ressource buchen und die **Buchungen** mit Arbeitsauftragsservices verknüpfen, indem Sie eine **Buchbare Ressource** aus [!INCLUDE [prod_short](includes/prod_short.md)] verwenden.

### <a name="business-central-1"></a>Business Central

Wenn Arbeitsaufträge Produkte und Services enthalten, werden, abhängig von Ihren Einstellungen auf der Seite **Einrichtung der Field Service-Integration**, Verbrauchsinformationen übertragen und mithilfe einer **Projekt-Buch.-Blatt** in [!INCLUDE [prod_short](includes/prod_short.md)] gebucht.

Die Werte **Zu fakturierende Menge** und **Zu fakturierende Dauer** werden in das Feld **In Rechnung zu übertragende Menge** kopiert. Basierend auf diesen Werten können Sie Verkaufsrechnungen in [!INCLUDE [prod_short](includes/prod_short.md)] erstellen und buchen, um sie dem Debitor in Rechnung zu stellen. Nachdem die Rechnung gebucht oder der Verbrauch in [!INCLUDE [prod_short](includes/prod_short.md)] verarbeitet wurde, werden die in Rechnung gestellte und die verbrauchte Menge auf der Registerkarte [!INCLUDE [prod_short](includes/prod_short.md)] auf den Seiten **Arbeitsauftragsprodukt** und **Arbeitsauftragsservice** angezeigt.  

Verwenden Sie die Seite **Projektplanzeilen**, um die Buchung und Rechnungsstellung des Verbrauchs von Arbeitsaufträgen nachzuverfolgen. Auf der Seite **Projektplanzeilen** können Sie Verkaufsrechnungen in [!INCLUDE [prod_short](includes/prod_short.md)] erstellen und buchen. Anschließend können Sie diese mit [!INCLUDE [field-service-short](includes/field-service-short.md)] synchronisieren und den Status der Rechnungen nachverfolgen.

> [!NOTE]
> Arbeitsauftragsservices mit einer Buchung, die eine buchbare Ressource verwendet, die mit einer [!INCLUDE [prod_short](includes/prod_short.md)]-Ressource verknüpft ist, werden mit zwei Projektbuchungsblattzeilen synchronisiert: eine Zeile vom Typ **Budget** für die verbundene Ressource und eine weitere Zeile vom Typ **Fakturierbar** für den zu wartenden Artikel.
>
> Das im Arbeitsauftragsservice ausgewählte Produkt muss an einen Artikel des Typs **Service** in [!INCLUDE [prod_short](includes/prod_short.md)] gekoppelt sein. Außerdem muss die Basiseinheit für den Artikel auf die **Stunden-Maßeinheit** eingestellt sein, die auf der Seite **Einrichtung der Dynamics 365 Field Service Integration** ausgewählt wurde.
>
> Sie können eine Rechnung für einen Artikel vom Typ **Service** aus der fakturierbaren Projektplanzeile erstellen und die Budgetprojektplanzeile verwenden, um Kosten für die Ressource zu erfassen.

## <a name="see-also"></a>Siehe auch

[Integration in Microsoft Dataverse über Datensynchronisierung](admin-common-data-service.md)  
[Zu synchronisierende Tabellen und Felder zuordnen](admin-how-to-modify-table-mappings-for-synchronization.md)
