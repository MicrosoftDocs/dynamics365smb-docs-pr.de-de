---
title: Synchronisierung und Datenintegration | Microsoft Docs
description: 'Die Synchronisierung kopiert Daten zwischen Microsoft Dataverse Tabellen und Business Central-Datensätze, um die Daten in beiden Systeme auf dem neuesten Stand zu halten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
ms.date: 06/14/2021
ms.author: bholtorf
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a><a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Synchronisieren von Daten in Business Central mit Microsoft Dataverse


Wenn Sie [!INCLUDE[prod_short](includes/cds_long_md.md)] in [!INCLUDE[prod_short](includes/prod_short.md)] integrieren, können Sie entscheiden, ob die Daten der ausgewählten Felder von [!INCLUDE[prod_short](includes/prod_short.md)] (wie Debitoren, Kontakte und Vertriebsmitarbeiter) mit entsprechenden Zeilen in [!INCLUDE[prod_short](includes/cds_long_md.md)] synchronisieren (beispielsweise Konten, Kontakte und Benutzer). Je nach Art des Datensatzes können Sie Zeilen von [!INCLUDE[prod_short](includes/cds_long_md.md)] nach [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren oder umgekehrt. Weitere Informationen finden Sie unter [Integrieren in Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Bei der Synchronisierung werden die folgenden Elemente einbezogen:

* Integrationstabellenzuordnungen
* Integrationsfeldzuordnungen
* Synchronisierungsregeln
* Gekoppelte Datensätze

Wenn die Synchronisierung eingerichtet ist, können Sie die [!INCLUDE[prod_short](includes/prod_short.md)] Datensätze mit [!INCLUDE[prod_short](includes/cds_long_md.md)] Zeilen koppeln, um ihre Daten zu synchronisieren. Sie können eine Synchronisierung manuell oder nach Plan starten. Die folgende Tabelle zeigt eine Übersicht über die Methoden der Synchronisierung von Datensätzen.  

|  Typ  |  Art  |  Siehe  |  
|--------|----------|-------|  
|Manuelle Synchronisierung|Synchronisieren Sie auf Basis von Zeilen.<br /><br /> Sie können, beispielsweise als Debitor, einzelne Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] mit einer entsprechenden [!INCLUDE[prod_short](includes/cds_long_md.md)] Zeile synchronisieren, beispielsweise einem Konto. So arbeiten Benutzer normalerweise mit [!INCLUDE[prod_short](includes/cds_long_md.md)]-Daten in [!INCLUDE[prod_short](includes/prod_short.md)].|[Datensätze manuell koppeln und synchronisieren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synchronisieren Sie auf Basis einer Tabellenzuordnung.<br /><br /> Sie können alle Datensätze in einer [!INCLUDE[prod_short](includes/prod_short.md)]-Tabelle mit einer [!INCLUDE[prod_short](includes/cds_long_md.md)] Tabelle synchronisieren.|[Synchronisieren einzelner Tabellenzuordnungen](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synchronisieren Sie alle geänderten Datensätze für alle Tabellenzuordnungen.<br /><br /> Sie können alle Datensätze synchronisieren, die in den [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen seit der letzten Synchronisierung geändert wurden.|[Synchronisierung aller geänderten Datensätze](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Vollständige Synchronisierung aller Daten für alle Tabellenzuordnungen.<br /><br /> Sie können alle Daten in den [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen und die [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabellen, die zugeordnet werden, synchronisieren, und neue Datensätze oder Tabellen in der Ziellösung für ungekoppelte Datensätze in der Quelllösung erstellen.<br /><br /> Bei der vollständigen Synchronisierung werden alle Daten synchronisiert und die Kopplung ignoriert. Normalerweise führen Sie eine vollständige Synchronisierung durch, wenn Sie die Integration einrichten und nur eine der Lösungen enthält Daten. Eine vollständige Synchronisierung kann auch in einer Demonstrationsumgebung hilfreich sein.|[Ausführen einer vollständigen Synchronisierung](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Geplante Synchronisierung|Synchronisieren Sie alle Änderungen an Daten für alle Tabellenzuordnungen.<br /><br /> Sie können [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[prod_short](includes/cds_long_md.md)] in geplanten Intervallen synchronisieren, indem Sie Projekte in der Projektwarteschlange einrichten.|[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> Die Synchronisierung zwischen [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] basiert auf der geplanten Ausführung von Jobwarteschlangeneinträgen und garantiert keine Echtzeitdatenkonsistenz zwischen zwei Diensten. Um weitere Informationen zur Datenkonsistenz in Echtzeit zu erhalten, sollten Sie [Virtuelle Business Central-Tabellen](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) oder Business Central-APIs erkunden.   


## <a name="standard-table-mapping-for-synchronization"></a><a name="standard-table-mapping-for-synchronization"></a>Standard-Tabellenzuordnung für die Synchronisierung
Tabellen in [!INCLUDE[prod_short](includes/cds_long_md.md)] wie beispielsweise Konten, werden mit äquivalenten Arten von Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] wie beispielsweise Debitoren integriert. Um mit [!INCLUDE[prod_short](includes/cds_long_md.md)]-Daten zu arbeiten, richten Sie Verknüpfungen, auch Kopplungen genannt, zwischen Tabellen in [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] ein.

Die folgende Tabelle zeigt die standardmäßige Zuordnung zwischen Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Sie können Konfigurationsänderungen an Integrationstabellen- und Feldzuordnungen auf ihre Standardeinstellungen zurücksetzen, indem Sie die Zuordnungen auswählen und dann **Standardsynchronisationseinrichtung verwenden** wählen.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synchronisierungsrichtung | Standardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Verkäufer/Einkäufer | Benutzer | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] Kontaktfilter: **Status** ist **Nein**, **Benutzer lizenziert** ist **Ja**, Integrationsbenutzermodus ist **Nein** |
| Debitor | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] Kontofilter: **Beziehungstyp** ist **Debitor** und **Status** ist **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)] Filter: **Blockiert** ist leer (Debitor ist nicht blockiert). |
| Kreditor | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] Kontofilter: **Beziehungstyp** ist **Kreditor** und **Status** ist **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)] Filter: **Blockiert** ist leer (Kreditor ist nicht blockiert). |
| Kontakt | Kontakt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Kontaktfilter: **Type** ist **Person** und der Kontakt wird einem Unternehmen zugewiesen. [!INCLUDE[prod_short](includes/cds_long_md.md)] Kontaktfilter: Der Kontakt wird einem Unternehmen zugeordnet und der übergeordnete Debitorentyp ist **Debitor**. |
| Währung | Transaktionswährung | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> Die **Dataverse**-Aktionen stehen auf Seiten nicht zur Verfügung, z. B. auf der Seite „Kundenkarte“ für Datensätze, die den Tabellenfilter auf der Zuordnung der Integrationstabelle nicht beachten.

### <a name="tip-for-admins-viewing-table-mappings"></a><a name="tip-for-admins-viewing-table-mappings"></a>Tipp für Administratoren: Aufrufen von Tabellenzuordnungen
Sie können die Zuordnung zwischen den Tabellen in [!INCLUDE[prod_short](includes/cds_long_md.md)] und den Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] auf der Seite **Integrationstabellenzuordnungen** aufrufen, auf der Sie auch Filter anwenden können. Sie legen die Zuordnung zwischen den Feldern in [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen und den Spalten in [!INCLUDE[prod_short](includes/cds_long_md.md)]-Tabellen auf der Seite **Integrationsfeldzuordnung** fest, auf der Sie zusätzliche Zuordnungslogiken hinzufügen können. Dies kann beispielsweise hilfreich sein, wenn Sie Fehler bei der Synchronisierung beheben müssen.

## <a name="see-also"></a><a name="see-also"></a>Siehe auch
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)   
[Planen einer Synchronisierung](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
