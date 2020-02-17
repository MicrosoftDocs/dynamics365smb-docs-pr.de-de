---
title: Fehlerbehebung bei Synchronisationsfehlern | Microsoft Docs
description: Bietet eine Anleitung zum Erkennen und Beheben von Synchronisationsfehlern.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 489e66165c5441ea63043a30dee8af314ef5d815
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991808"
---
# <a name="troubleshooting-synchronization-errors"></a>Fehlerbehebung bei Synchronisationsfehlern
Bei der Integration von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief. In diesem Thema werden einige der typischen Fehler aufgeführt, die auftreten, und es werden einige Hinweise zu deren Behebung gegeben.

Fehler treten häufig auf, wenn ein Benutzer gekoppelte Datensätze bearbeitet hat oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist. Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzer diese selbst beheben. Diese Fehler werden durch Aktionen verursacht, z. B. Löschen eines Datensatzes in einer, jedoch nicht in beiden Geschäftsanwendungen und anschließendes Synchronisieren. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators. Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen. Beispiele für typische Probleme sind:  
  
* Die den Benutzern zugewiesenen Berechtigungen und Rollen sind nicht korrekt.  
* Das Administratorkonto wurde als Integrationsbenutzer angegeben.  
* Das Kennwort des Integrationsbenutzers erfordert eine Änderung, wenn sich der Benutzer anmeldet.  
* Die Wechselkurse für Währungen sind in der einen oder anderen App nicht angegeben.  
  
Sie müssen die Fehler manuell beheben. Es gibt jedoch einige Möglichkeiten, wie die Seite Ihnen helfen kann. Beispiel:  

* Die Felder **Quelle** und **Ziel** können Links zu dem Datensatz enthalten, in dem der Fehler gefunden wurde. Klicken Sie auf den Link, um den Datensatz zu öffnen und den Fehler zu untersuchen.  
* Die Aktion **Einträge löschen, die älter als 7 Tage sind** und die Aktion **Alle Einträge löschen** wird die Liste bereinigen. In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft. Vorsicht walten lassen. Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.

Manchmal können die Zeitstempel in Datensätzen zu Konflikten führen. In der Tabelle „CRM-Integrationsdatensatz“ werden die Zeitstempel „Letzte Synchronisierung geändert am“ und „Letzte CRM-Synchronisierung geändert am“ für die letzte in beide Richtungen durchgeführte Integration für einen Datensatz beibehalten. Diese Zeitstempel werden mit Zeitstempeln in Business Central- und Sales-Datensätzen verglichen. In Business Central befindet sich der Zeitstempel in der Integrationsdatensatztabelle.

Sie können nach Datensätzen filtern, die synchronisiert werden sollen, indem Sie die Zeitstempel der Datensätze in den „Integrationstabellenzuordnung“-Tabellenfeldern „Synchronisierung geändert in Filter“ und „Synchronisierung der Integrationstabelle“ vergleichen. Geänd. In Fltr.“.

Die Konfliktfehlermeldung „Der Debitorendatensatz kann nicht aktualisiert werden, weil er ein späteres Änderungsdatum als der Kontodatensatz hat“ oder „Der Kontodatensatz kann nicht aktualisiert werden, weil er ein späteres Änderungsdatum als der Kundendatensatz hat“ kann auftreten, wenn ein Datensatz einen Zeitstempel hat, der größer ist als IntegrationTableMapping. „Synchronisierung geändert in Filter“, aber er ist nicht aktueller als der Zeitstempel im Vertriebsintegrationsdatensatz. Dies bedeutet, dass der Quelldatensatz manuell und nicht über den Auftragswarteschlangenposten synchronisiert wurde. 

Der Konflikt tritt auf, weil der Zieldatensatz ebenfalls geändert wurde – der Zeitstempel des Datensatzes ist aktueller als der Zeitstempel des Vertriebsintegrationsdatensatzes. Die Zielprüfung erfolgt nur für bidirektionale Tabellen. 

Diese Datensätze werden jetzt auf die Seite „Übersprungene Synchronisierungsdatensätze“ verschoben, die Sie über die Seite Microsoft Dynamics-Verbindungssetup in Business Central öffnen können. Dort können Sie die beizubehaltenden Änderungen angeben und die Datensätze dann erneut synchronisieren.

## <a name="see-also"></a>Siehe auch
[Integrieren in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Einrichten des Benutzerkontos für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md) ein  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  
