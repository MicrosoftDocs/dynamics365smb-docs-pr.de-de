---
title: Verwalten von Kunden mit Dynamics 365 Sales (enthält Video) | Microsoft Dokumente
description: Sie können Dynamics 365 Sales von Business Central aus mit nahtloser Integration und Synchronisation im Lead-to-Cash-Prozess verwenden.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'integration, synchronize, map, Sales'
ms.search.forms: '9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250'
ms.date: 09/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="use-dynamics-365-sales-from-business-central"></a>Verwenden von Dynamics 365 Sales von Business Central
Wenn Sie Dynamics 365 Sales for Customer Engagement verwenden, können Sie nahtlose Integration in den Interessent-zu-Geld-Prozess nutzen, indem Sie [!INCLUDE[prod_short](includes/prod_short.md)] für Backend-Aktivitäten wie Auftragsverarbeitung, Lagerbestandsverwaltung und Finanzbearbeitung verwenden.

Bevor Sie die Integrationsfunktionen verwenden können, muss Ihr Systemadministrator die Verbindung einrichten und Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] definieren. Weitere Informationen finden Sie unter [Integrieren in Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> In diesen Schritten wird die Integration von Onlineversionen von [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] beschrieben. Informationen zur lokalen Konfiguration finden Sie unter [Dynamics 365 Sales für die lokale Integration vorbereiten](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Die Integration der Anwendungen ermöglicht den Zugriff auf Daten in Sales von [!INCLUDE[prod_short](includes/prod_short.md)] aus und in einigen Fällen auch umgekehrt. Sie können mit Datentypen, die bei beiden Diensten gleich sind, arbeiten und diese synchronisieren. Dazu zählen etwa Debitoren, Kontakte und Verkaufsinformationen. Außerdem können Sie die Daten an beiden Anwendungen auf dem aktuellen Stand halten.  

Beispielsweise kann ein Verkäufer in [!INCLUDE[crm_md](includes/crm_md.md)] die Preislisten aus [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, wenn er einen Kundenauftrag erstellt. Wenn sie den Artikel der Debitorenauftragszeile unter [!INCLUDE[crm_md](includes/crm_md.md)] hinzufügen, können sie den Lagerbestand (Verfügbarkeit) des Artikels unter [!INCLUDE[prod_short](includes/prod_short.md)] sehen.

Umgekehrt können Auftragsbearbeiter in [!INCLUDE[prod_short](includes/prod_short.md)] Kundenaufträge bearbeiten, die automatisch oder manuell von [!INCLUDE[crm_md](includes/crm_md.md)] übertragen werden. Sie können z.B. Debitorauftragszeilen für Artikel oder Ressourcen erstellen und buchen, die in [!INCLUDE[crm_md](includes/crm_md.md)] als Einschreibprodukte eingegeben wurden. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] kann nur in [!INCLUDE[crm_md](includes/crm_md.md)] integriert werden. Andere Dynamics 365-Anwendungen, die den Standard-Workflow oder das Datenmodell in [!INCLUDE[crm_md](includes/crm_md.md)] ändern, z.B. Project Service Automation, können die Integration zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] unterbrechen.

## <a name="coupling-records"></a>Kopplungsdatensätze
Mit dem Leitfaden für das unterstütze Setup können Sie die zu synchronisierenden Daten auswählen. Später können Sie die Synchronisierung für bestimmte Datensätze einrichten. Dies wird als *Kopplung* bezeichnet. Sie können z.B. ein bestimmtes Konto in [!INCLUDE[crm_md](includes/crm_md.md)] mit einem bestimmten Debitor in [!INCLUDE[prod_short](includes/prod_short.md)] koppeln. In diesem Abschnitt wird beschrieben, was berücksichtigt werden sollte, wenn Sie Datensätze koppeln.

Wenn Sie z.B. Konten in [!INCLUDE[crm_md](includes/crm_md.md)] als Debitoren in [!INCLUDE[prod_short](includes/prod_short.md)] sehen wollen, müssen Sie die beiden Arten von Datensätzen koppeln. Dazu verwenden Sie auf der Listenseite **Debitoren** in [!INCLUDE[prod_short](includes/prod_short.md)] die **Kopplung einrichten**-Aktion. Dann geben Sie unter [!INCLUDE[crm_md](includes/crm_md.md)] an, welche [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren mit welchen Konten übereinstimmen sollen.

Sie können auch ein Konto in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen (und koppeln), z.B. basierend auf einem Debitorendatensatz in [!INCLUDE[prod_short](includes/prod_short.md)], indem Sie **Konto in Dynamics 365 Sales** erstellen, oder umgekehrt, indem Sie **Debitor in [!INCLUDE[prod_short](includes/prod_short.md)]** erstellen.

Wenn Sie eine Kopplung zwischen zwei Datensätzen einrichten, können Sie manuell anfordern, dass der aktuelle Datensatz, beispielsweise einen Debitor, sofort durch Kontodaten aus Sales (oder aus [!INCLUDE[prod_short](includes/prod_short.md)]) mithilfe der **Jetzt synchronisieren**-Aktion überschrieben werden. Die **Jetzt synchronisieren**-Aktion, die fragt, ob Sales oder [!INCLUDE[prod_short](includes/prod_short.md)]-Datensatzdaten überschrieben werden sollen.

In einigen Fällen müssen Sie projektspezifische Datenbestände vor anderen Datensätzen koppeln, wie in der folgenden Tabelle dargestellt.

|Daten|Was zuerst koppeln|
|-----|----|
|Debitoren und Konten|Paare von Verkäufern mit [!INCLUDE[crm_md](includes/crm_md.md)] Benutzer|
|Artikel und Ressourcen|Koppeln von Einheiten mit [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitengruppen|
|Artikel und Ressourcenpreise|Koppeln Sie Kundenpreisgruppen mit [!INCLUDE[crm_md](includes/crm_md.md)]-Preisen|

> [!NOTE]  
> Wenn Ihre Preise oder Debitoren Fremdwährungen verwenden, stellen Sie sicher, dass Sie Währungen mit Sales-Transaktionswährungen koppeln.

In [!INCLUDE[crm_md](includes/crm_md.md)] hängen Debitorenaufträge von Informationen wie Debitoren, Mengeneinheiten, Währungen, Debitorenpreisgruppen und Artikeln und/oder Ressourcen ab. Damit Verkaufsaufträge arbeiten, müssen Sie Debitoren, Einheiten, Währungen, Debitorenpreisgruppen, Artikel und/oder Ressourcen koppeln.

## <a name="fully-synchronizing-records"></a>Datensätze vollständig synchronisieren
Am Ende der Anleitung zur unterstützten Einrichtung können Sie die Aktion **Vollständige Synchronisierung ausführen** wählen, um die Synchronisierung aller [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze mit allen zugehörigen Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] zu starten. Auf der Seite **Dynamics 365 Sales vollständige Synchronisierung prüfen** wählen Sie die Aktion **Starten** aus. Die vollständige Synchronisierung kann einige Zeit in Anspruch nehmen, aber Sie können die Arbeit in [!INCLUDE[prod_short](includes/prod_short.md)] fortsetzen, während sie im Hintergrund läuft.

Um den Status aus einzelnen Projekte in einer vollständigen Synchronisierung zu prüfen, wählen Sie auf der Seite **Dynamics 365 Sales vollständigen Synchronisierung prüfen** einen Datensatz, um Details anzeigen. Um den Status der Synchronisierung zu aktualisieren, aktualisieren Sie die Seite.

Auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** können Sie Details über sämtliche Synchronisierungen sehen. Von hier können Sie die Seite **Integrationstabellenzuordnungen** auch öffnen, um Details über die Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] und Sales zu finden, die synchronisiert werden müssen.

## <a name="handling-sales-order-data"></a>Bearbeiten von Verkaufsauftragsdaten
Verkaufsaufträge, die Verkäufer in [!INCLUDE[crm_md](includes/crm_md.md)] einreichen, werden automatisch zu [!INCLUDE[prod_short](includes/prod_short.md)] übertragen, wenn Sie das Kontrollkästchen **Verkaufsaufträge automatisch erstellen** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** auswählen.
Alternativ können Sie eingereichte Verkaufsaufträge aus [!INCLUDE[crm_md](includes/crm_md.md)] mithilfe der Aktion **Erstellen in [!INCLUDE[prod_short](includes/prod_short.md)]**, die auf der Seite **Verkaufsaufträge - Dynamics 365 for Sales** verfügbar ist, manuell konvertieren.
In solchen Verkaufsaufträgen wird das **Name** Feld im ursprünglichen Auftrag dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[prod_short](includes/prod_short.md)] übertragen und zugeordnet.

Dies kann auch gehen, wenn der ursprüngliche Verkaufsauftrag geschriebene Produkte enthält, d.h. Artikel oder Ressourcen sind nicht in beiden Apps erfasst worden. In diesem Fall müssen Sie die Felder **Geschriebenen Produkttyp** und die **Geschriebene Produktnummer** ausfüllen auf der Seite **Debitoren & Verkauf Einr.**, damit Verkäufe nicht registrierter Produkte einem angegebenen Artikel oder Ressourcennummer zugeordnet werden.

> [!NOTE]
> Sie können keinen manuellen Posten einem Artikel oder einer Ressource in [!INCLUDE[prod_short](includes/prod_short.md)] zuordnen, der/die an ein Produkt in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt ist. Um manuelle Posten zu ermöglichen, empfehlen wir, dass Sie einen Artikel oder eine Ressource speziell für diesen Zweck erstellen und diese(n) nicht an ein Produkt in [!INCLUDE[crm_md](includes/crm_md.md)] koppeln. 

Wenn die Artikelbeschreibung des ursprünglichen Verkaufsauftrags lang ist, wird eine zusätzliche Verkaufsauftragszeile der Art **Bemerkung** erstellt, um den Text in dem Verkaufsauftrag in [!INCLUDE[prod_short](includes/prod_short.md)]festzuhalten.

Aktualisierungen von Feldern auf Verkaufsauftragsköpfen, wie z. B. die Felder „Letztes Lieferdatum“ oder „Gewünschtes Lieferdatum“, die in der Integrationstabellenzuordnung **VERKAUFSAUFTRAG-AUFTRAG** zugeordnet sind, werden periodisch mit [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Prozesse wie das Freigeben, Lieferung oder Fakturierung eines Verkaufsauftrags werden auf der Verkaufsauftragszeitachse in [!INCLUDE[crm_md](includes/crm_md.md)] gebucht. Weitere Informationen finden Sie unter [Einführung in die Aktivitätsfeeds](/dynamics365/sales-enterprise/manage-activities). Informationen zum Aktivieren von Buchungen und Aktivitäten für Bestellungen in [!INCLUDE[crm_md](includes/crm_md.md)] finden Sie unter [Richten Sie das Notizsteuerelement ein, um auf Informationen über Beiträge für eine benutzerdefinierte Entität zuzugreifen](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) in der Customer Engagement-Dokumentation. Der Artikel bezieht sich auf Customer Engagement On-Premises, aber die Schritte sind für die Online-Version identisch. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Periodische Synchronisierung basierend auf der Integrationstabellenzuordnung **VERKAUFSAUFTRAG-AUFTRAG** funktioniert nur, wenn die Verkaufsauftragsintegration aktiviert ist. Weitere Informationen finden Sie unter [Verbindungseinstellungen auf der Einrichtungsseite für die Sales Verbindung](admin-prepare-dynamics-365-for-sales-for-integration.md). Nur Verkaufsaufträge, die aus übermittelten Verkaufsaufträgen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt wurden, werden synchronisiert. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Bearbeiten von Verkaufsangebotsdaten
Verkaufsangebote, die in [!INCLUDE[crm_md](includes/crm_md.md)] aktiviert werden, werden automatisch zu [!INCLUDE[prod_short](includes/prod_short.md)] übertragen, wenn Sie das Kontrollkästchen **Automatisches Verarbeiten von Angeboten** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** auswählen.
Alternativ können Sie aktivierte Verkaufsangebote aus [!INCLUDE[crm_md](includes/crm_md.md)] mithilfe der Aktion **Prozess in [!INCLUDE[prod_short](includes/prod_short.md)]** auf der Seite **Verkaufsangebot - Dynamics 365 Sales** verwenden.
In solchen Verkaufsangeboten wird das **Name**-Feld im ursprünglichen Angebot dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[prod_short](includes/prod_short.md)] übertragen und zugeordnet. Auch wird das Feld **Gültig bis** beim Angebot übertragen und dem Feld **Angebot gültig bis** auf dem Verkaufsangebot in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet.  

Verkaufsangebote unterliegen vielen Überarbeitungen, bis sie abgeschlossen werden. Manuelle und automatische Verarbeitung von Verkaufsangeboten in [!INCLUDE[prod_short](includes/prod_short.md)] stellt sicher, dass vorherige Versionen von Verkaufsanfragen archiviert werden, bevor neue Überarbeitungen von Verkaufsanfragen von [!INCLUDE[crm_md](includes/crm_md.md)] verarbeitet werden.

Wenn Sie **Verarbeiten** in [!INCLUDE[prod_short](includes/prod_short.md)] für ein Angebot wählen, das den Status **Gewonnen** hat, wird ein Verkaufsauftrag in [!INCLUDE[prod_short](includes/prod_short.md)] nur dann erstellt, wenn ein entsprechender Verkaufsauftrag in [!INCLUDE[crm_md](includes/crm_md.md)] eingereicht wird. Andernfalls wird das Angebot nur in [!INCLUDE[prod_short](includes/prod_short.md)] freigegeben. Wenn ein entsprechender Verkaufsauftrag später in [!INCLUDE[crm_md](includes/crm_md.md)] eingereicht wird und ein Verkaufsauftrag auf dessen Grundlage erstellt wird, wird die **Angebotsnummer** im Verkaufsauftrag aktualisiert und das Angebot wird archiviert.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Behandlung der gebuchten Verkaufsrechnungen, Debitoren-Zahlungen und Statistiken
Nach der Erfüllung eines Verkaufsauftrags, werden dafür Rechnungen erstellt. Wenn Sie Aufträge fakturieren, können Sie gebuchte Verkaufsrechnung übertragen an [!INCLUDE[crm_md](includes/crm_md.md)], wenn Sie das Kontrollkästchen **Rechnung erstellen in [!INCLUDE[crm_md](includes/crm_md.md)]** auf der Seite **Gebuchte Verkaufsrechnungen** auswählen. Gebuchte Rechnungen werden an [!INCLUDE[crm_md](includes/crm_md.md)] mit dem Status **Fakturiert** übertragen.

Sobald Sie die Zahlung des Debitors für die Verkaufsrechnung in [!INCLUDE[prod_short](includes/prod_short.md)] erhalten, wird der Verkaufsrechnungsstatus auf **Bezahlt** mit dem **Statusgrund** auf **Teilweise** festgelegt, wenn teilweise bezahlt oder auf **Komplett** festgelegt, wenn vollständig bezahlt, wenn Sie die Aktion **Kontostatistik aktualisieren** auf der Debitorenseite in [!INCLUDE[prod_short](includes/prod_short.md)] auswählen. Die Funktion **Kontostatistik aktualisieren** aktualisiert auch Werte wie **Saldo** und **Gesamtverkäufe** in der **Infobox [!INCLUDE[prod_short](includes/prod_short.md)] Kontostatistik** in [!INCLUDE[crm_md](includes/crm_md.md)]. Alternativ können Sie geplante Aufträge (Debitoren-Statistik und POSTEDSALESINV-INV) automatisch für beide Vorgänge im Hintergrund ausführen. 

## <a name="handling-sales-prices"></a>Handhabung von Verkaufspreisen
> [!NOTE]
> In Veröffentlichungszyklus 2 von 2020 haben wir optimierte Prozesse zum Einrichten und Verwalten von Preisen und Rabatten veröffentlicht. Wenn Sie ein neuer Kunde mit dieser Version sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Die Schritte zum Abschluss dieses Prozesses unterscheiden sich, je nachdem, ob Ihr Administrator die neue Preiserfahrung aktiviert hat. 

> [!NOTE]
> Wenn die Standard-Preissynchronisation bei Ihnen nicht funktioniert, empfehlen wir die angepassten Funktionalitäten der Integration zu verwenden. Weitere Informationen finden Sie unter [Anpassen einer Integration mit Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Aktuelle Erfahrung](#tab/current-experience/)
In der aktuellen Preiserfahrung synchronisiert [!INCLUDE[prod_short](includes/prod_short.md)] Verkaufspreise, die: 

* Für alle Debitoren gelten. Standard-Verkaufspreislisten werden auf der Basis des Preises im Feld **Einheitspreis** auf der Seite **Elementkarte** für die Artikel erstellt.
* Anwenden auf eine bestimmte Debitor-Preisgruppe. Zum Beispiel Verkaufspreise für Ihre Einzel- oder Großhandelskunden. Um Preise auf Basis einer Kundenpreisgruppe zu synchronisieren, gehen Sie wie folgt vor:

    1. Koppeln Sie die Elemente, für die Preise durch die Kundenpreisgruppe festgelegt sind.
    2. Auf der Seite **Kundenpreisgruppen** koppeln Sie die Kundenpreisgruppe, indem Sie **Bezogen**, dann **Dynamics 365 Sales**, **Kopplung** und dann **Kopplung einrichten** wählen. Die Kopplung erstellt eine aktive Preisliste in [!INCLUDE[prod_short](includes/prod_short.md)] mit dem gleichen Namen wie die Debitor-Preisgruppe in [!INCLUDE[crm_md](includes/crm_md.md)] und synchronisiert automatisch alle Artikel, für die die Debitor-Preisgruppe den Preis definiert.

:::image type="content" source="media/customer-price-group.png" alt-text="Kundenpreisgruppen-Seite.":::

#### [Neue Erfahrung](#tab/new-experience/)  

Die neue Preiserfahrung synchronisiert Preislisten, die die folgenden Kriterien erfüllen:

* **Aktualisierung von Standardwerten zulassen** ist ausgeschaltet.
* Der Preistyp ist Verkauf.
* Der Betragstyp ist Preis.
* Der Produkttyp in den Zeilen muss Element oder Ressource sein. 
* Eine Mindestmenge ist nicht angegeben.

[!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert Verkaufspreise, die für alle Debitoren gelten. Standard-Verkaufspreislisten werden auf der Basis des Preises im Feld **Einheitspreis** auf der Seite **Elementkarte** für die Artikel erstellt.

Um Preislisten zu synchronisieren, wählen Sie auf der Seite **Verkaufspreisliste** **Bezogen**, **Dynamics 365 Sales**, **Kopplung** und dann **Kopplung einrichten**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Seite Verkaufspreislisten.":::

---


## <a name="see-also"></a>Weitere Informationen
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Marketing & Vertrieb](marketing-relationship-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)    
[Überblick über Sales und Verkaufs-Hub](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
