---
title: Synchronisierung und Datenintegration | Microsoft Docs
description: Die Synchronisierung kopiert Daten zwischen Dynamics 365 for Sales-Posten und Business Central-Datensätze, um die Daten in beiden Systeme auf dem neuesten Stand zu halten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: e52010384de83d95011cb29a88cad17a5eba817c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940172"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Synchronisieren von Daten in Business Central und Dynamics 365 for Sales
Wenn Sie [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)] integrieren, können Sie entscheiden, ob die Daten der ausgewählten Felder von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätzen (wie Debitoren, Kontakten und Vertriebsmitarbeitern) mit entsprechenden Datensätzen in [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren (beispielsweise Konten, Kontakte und Benutzer). Je nach Art des Datensatzes können Sie Daten von [!INCLUDE[crm_md](includes/crm_md.md)] nach [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisieren oder umgekehrt. Weitere Informationen finden Sie unter [Integrieren in Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Bei der Synchronisierung werden die folgenden Elemente einbezogen:

* Integrationstabellenzuordnungen
* Integrationsfeldzuordnungen
* Synchronisierungsregeln
* Gekoppelte Datensätze

Wenn die Synchronisierung eingerichtet ist, können Sie die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze mit [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätzen koppeln, um ihre Daten zu synchronisieren. Sie können eine Synchronisierung manuell oder nach Plan starten. Die folgende Tabelle zeigt eine Übersicht über die Methoden der Synchronisierung von Datensätzen.  

|  Typ  |  Art  |  Siehe  |  
|--------|----------|-------|  
|Manuelle Synchronisierung|Synchronisieren Sie auf Basis von Datensätzen.<br /><br /> Sie können, beispielsweise als Debitor, einzelne Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] mit einem entsprechenden [!INCLUDE[crm_md](includes/crm_md.md)]-Datensatz synchronisieren, beispielsweise einem Konto. So arbeiten Benutzer normalerweise mit [!INCLUDE[crm_md](includes/crm_md.md)]-Daten in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Datensätze manuell koppeln und synchronisieren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchronisieren Sie auf Basis einer Tabellenzuordnung.<br /><br /> Sie können alle Datensätze in einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabelle mit einer [!INCLUDE[crm_md](includes/crm_md.md)]-Einheit synchronisieren.|[Synchronisieren einzelner Tabellenzuordnungen](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synchronisieren Sie alle geänderten Datensätze für alle Tabellenzuordnungen.<br /><br /> Sie können alle Datensätze synchronisieren, die in den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen seit der letzten Synchronisierung geändert wurden.|[Synchronisierung aller geänderten Datensätze](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Vollständige Synchronisierung aller Daten für alle Tabellenzuordnungen.<br /><br /> Sie können alle Daten in den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen und die [!INCLUDE[crm_md](includes/crm_md.md)]-Einheiten, die zugeordnet werden, synchronisieren, und neue Datensätze in der Ziellösung für ungekoppelte Datensätze in der Quelllösung erstellen.<br /><br /> Bei der vollständigen Synchronisierung werden alle Daten synchronisiert und die Kopplung ignoriert. Normalerweise führen Sie eine vollständige Synchronisierung durch, wenn Sie die Integration einrichten und nur eine der Lösungen enthält Daten. Eine vollständige Synchronisierung kann auch in einer Demonstrationsumgebung hilfreich sein.|[Ausführen einer vollständigen Synchronisierung](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Geplante Synchronisierung|Synchronisieren Sie alle Änderungen an Daten für alle Tabellenzuordnungen.<br /><br /> Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] in geplanten Intervallen synchronisieren, indem Sie Projekte in der Projektwarteschlange einrichten.|[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard-Sales-Entitätszuordnungen für die Synchronisierung
Entitäten in [!INCLUDE[crm_md](includes/crm_md.md)], wie beispielsweise Konten, werden mit äquivalenten Arten von Entitäten, wie beispielsweise Debitoren, in [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert. Um mit [!INCLUDE[crm_md](includes/crm_md.md)]-Daten zu arbeiten, richten Sie Verknüpfungen, auch Kopplungen genannt, zwischen Einheiten in [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] ein.

Die folgende Tabelle zeigt die standardmäßige Zuordnung zwischen Einheiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)], die [!INCLUDE[crm_md](includes/crm_md.md)] bietet.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synchronisierungsrichtung|Standardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Verkäufer/Einkäufer|Benutzer|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Vertriebskontaktfilter: **Status** ist **Nein**, **Benutzer lizenziert** **Ja** ist, Integrationsbenutzer Modus ist **Nein**|
|Debitor|Konto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-Kontenfilter: **Verhältnisart** ist **Debitor** und **Status** ist **Aktiv**.|
|Kontakt|Kontakt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Kontaktfilter: **Typ** ist **Person** und der Kontakt wird einem Unternehmen zugeordnet. Sales Kontaktfilter: Kontakt wird einem Unternehmen zugeordnet und die übergeordnete Debitorenart ist **Konto**.|
|Währung|Transaktionswährung|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Maßeinheit|Einheiten-Gruppe|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Artikel|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Vertriebskontaktfilter: **Produkt-Typ** ist **Verkaufs-Lager**|
|Ressource|Produkt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Vertriebskontaktfilter: **Produkt-Typ** ist **Service**|
|Debitorenpreisgruppe|VK-Preisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkaufspreis|Produkt-Preisliste|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Kontaktfilter: **Verkaufscode** ist nicht leer, **Verkaufsart** ist **Debitorenpreisgruppe**|
|Verkaufschance|Verkaufschance|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Verkaufsrechnungskopf|Fakturieren|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkaufsrechnungszeile|Rechnungsprodukt|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkaufsauftrags-Kopf|Verkaufsauftrag|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)] Verkaufskopffilter: **Belegart** ist „Auftrag”, **Status** ist „Freigegeben”|
|Hinweise zu Verkaufsaufträgen|Hinweise zu Verkaufsaufträgen|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Tipp für Administratoren: Aufrufen von Einheitenzuordnungen
Sie können die Zuordnung zwischen den Einheiten in [!INCLUDE[crm_md](includes/crm_md.md)] und den Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] auf der Seite **Integrationstabellenzuordnungen** aufrufen, auf der Sie auch Filter anwenden können. Sie legen die Zuordnung zwischen den Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen und den Feldern in [!INCLUDE[crm_md](includes/crm_md.md)]-Einheiten auf der Seite **Integrationsfeldzuordnung** fest, auf der Sie zusätzliche Zuordnungslogiken hinzufügen können. Dies kann beispielsweise hilfreich sein, wenn Sie Fehler bei der Synchronisierung beheben müssen.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Tipp für Entwickler: Zuordnen von Feldern in Business Central zu den Optionssätzen im Verkauf
Wenn Sie Entwickler sind und Optionen zu den Optionssätzen in [!INCLUDE[crm_md](includes/crm_md.md)] hinzufügen möchten, müssen Sie dies wissen. Es gibt drei Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)], die den Optionsfeldern der Einheit **Konto** in [!INCLUDE[crm_md](includes/crm_md.md)] zugeordnet sind. Datensätze in den Tabellen, die nicht mit den Optionen in [!INCLUDE[crm_md](includes/crm_md.md)] verknüpft sind, werden nicht synchronisiert. Das bedeutet, dass das Feld **Option** in [!INCLUDE[crm_md](includes/crm_md.md)] leer ist.

Die folgende Tabelle zeigt Zuordnungen der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen für das Feld **Option** in der Einheit **Konto** in [!INCLUDE[crm_md](includes/crm_md.md)].

|Tisch|Optionsfeld in der Kontoeinheit|
|----------------------|-------------------------------------------|
|Zahlungsbedingungen|Zahlungsbedingungen|
|Lieferbedingung|Adresse 1: Frachtbedingungen|
|Zusteller|Adresse 1: Versandmethode|

### <a name="synchronization-rules"></a>Synchronisierungsregeln
Die folgende Tabelle beschreibt Regeln, die die Synchronisierung zwischen den Anwendungen steuern.

> [!NOTE]  
> Ändert an Daten in [!INCLUDE[crm_md](includes/crm_md.md)], die durch das [!INCLUDE[crm_md](includes/crm_md.md)]-Verbindungsbenutzerkonto vorgenommen wurden, werden nicht synchronisiert. Daher empfiehlt es sich, bei der Nutzung dieses Kontos keine Daten zu ändern. Weitere Informationen finden Sie unter [Einrichten der Integration mit Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tisch|Regel|
|-----|----|
|Debitoren|Bevor ein Debitor mit einem Konto synchronisiert werden kann, muss der Verkäufer, der dem Debitor zugewiesen ist, mit einem Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt werden. Wenn Sie den „DEBITOREN – Dynamics 365 for Sales-Synchronisierungsauftrag“ ausführen und wenn Sie es so einrichten, dass neue Datensätze erstellt werden, achten Sie darauf, dass Sie Verkäufer mit [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzern synchronisieren, bevor Sie Debitoren mit [!INCLUDE[crm_md](includes/crm_md.md)]-Konten synchronisieren. <br /> <br />Der „DEBITOREN – Dynamics 365 for Sales-Synchronisierungsauftrag“ synchronisiert nur Sales-Konten, die den Beziehungstyp „Debitor“ haben.|
|Kontakte|Nur Kontakte in [!INCLUDE[crm_md](includes/crm_md.md)], die mit einem Konto verknüpft sind, werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellt. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Einheit in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Währungen|Währungen werden an Transaktionswährungen in [!INCLUDE[crm_md](includes/crm_md.md)] basierend auf ISO-Codes gekoppelt. Nur Währungen, die einen Standard-ISO-Code haben, werden mit Transaktionswährungen gekoppelt und synchronisiert.|
|Einheiten|Maßeinheiten werden mit Einheitengruppen in [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Es kann nur eine Einheit in der Einheitengruppe definiert sein.|
|Artikel|Wenn Elemente mit [!INCLUDE[crm_md](includes/crm_md.md)]-Produkten synchronisiert werden, erstellt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch eine Preisliste in [!INCLUDE[crm_md](includes/crm_md.md)]. Um Synchronisationsfehler zu vermeiden, sollten Sie diese Preisliste nicht manuell ändern.|
|Verkäufer|Verkäufer werden mit den Systembenutzern in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt. Der Benutzer muss aktiviert werden und lizenziert werden und darf nicht der integrierte Benutzer sein. Die Notiz, dass dies die erste Tabelle ist, die synchronisiert werden muss, weil sie Debitoren, Kontakten, Verkaufschancen und in den Verkaufsrechnungen verwendet wird.|
|Ressourcen|Ressourcen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Produkten synchronisiert, die den Produkttyp-Service haben.|
|Debitorenpreisgruppen|Debitorenpreisgruppen werden mit Verkaufspreislisten synchronisiert.|
|Verkaufspreise|Verkaufspreise, die Verkaufsart Debitorenpreisgruppe haben und einen definierten Verkaufscode haben werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Preislistenzeilen synchronisiert|
|Verkaufschancen|Chancen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Chancen synchronisiert. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Einheit in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Gebuchte Verkaufsrechnungen|Gebuchte Verkaufsrechnungen werden mit Verkaufsrechnungen synchronisiert. Bevor eine Rechnung synchronisiert werden kann, ist es besser, alle anderen Einheiten, die in der Rechnung teilnehmen können, von Verkäufer zu Preislisten zu synchronisieren. Der Verkäufer-Codewert im Rechnungskopf definiert den Besitzer der gekoppelten Einheit im Verkauf.|
|Verkaufsaufträge|Freigegebene Verkaufsaufträge (Kopf) werden mit Verkaufsaufträgen synchronisiert. Bevor ein Auftrag synchronisiert werden kann, ist es besser, alle anderen Einheiten, die an dem Auftrag teilnehmen können, von Verkäufern zu Preislisten zu synchronisieren. Der Verkäufer-Codewert im Auftragskopf definiert den Besitzer der gekoppelten Einheiten im Verkauf.|  

## <a name="see-also"></a>Siehe auch  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrieren in Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
