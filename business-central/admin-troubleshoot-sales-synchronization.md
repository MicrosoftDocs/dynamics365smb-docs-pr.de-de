---
title: Fehlerbehebung bei Synchronisationsfehlern | Microsoft Docs
description: Dieses Thema enthält einige Anleitungen zur Identifizierung, Problembehandlung und Behebung von Synchronisationsfehlern.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 3ed35bc7d0d9db1cd609078372d98535703f6583
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6326513"
---
# <a name="troubleshooting-synchronization-errors"></a>Fehlerbehebung bei Synchronisationsfehlern
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Bei der Integration von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[prod_short](includes/cds_long_md.md)] sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief. In diesem Thema werden einige der typischen Fehler aufgeführt, die auftreten, und es werden einige Hinweise zu deren Behebung gegeben.

Fehler treten häufig auf, wenn ein Benutzer gekoppelte Datensätze bearbeitet hat oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist. Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzer diese selbst beheben. Diese Fehler werden durch Aktionen verursacht, z. B. Löschen von Daten, jedoch nicht in beiden Geschäftsanwendungen und anschließendes Synchronisieren. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Beispiel
Dieses Video zeigt ein Beispiel für die Behebung von Fehlern, die bei der Synchronisierung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] aufgetreten sind. Der Prozess ist für alle Integrationen derselbe. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators. Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen. Beispiele für typische Probleme sind:  
  
* Die den Benutzern zugewiesenen Berechtigungen und Rollen sind nicht korrekt.  
* Das Administratorkonto wurde als Integrationsbenutzer angegeben.  
* Das Passwort des Integrationsbenutzers ist so eingestellt, dass eine Änderung erforderlich ist, wenn der Benutzer sich anmeldet.  
* Die Wechselkurse für Währungen sind in der einen oder anderen App nicht angegeben.  
  
Sie müssen die Fehler manuell beheben. Es gibt jedoch einige Möglichkeiten, wie die Seite Ihnen helfen kann. Beispiel:  

* Die Felder **Quelle** und **Ziel** können Links zu dem Zeilen enthalten, in dem der Fehler gefunden wurde. Klicken Sie auf den Link, um den Fehler zu untersuchen.  
* Die Aktion **Einträge löschen, die älter als 7 Tage sind** und die Aktion **Alle Einträge löschen** wird die Liste bereinigen. In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft. Vorsicht walten lassen. Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.

Manchmal können die Zeitstempel in Datensätzen zu Konflikten führen. In der Tabelle CDS-Integrationsdatensatz werden die Zeitstempel Letzte Synchronisierung geändert am und Letzte CDS-Synchronisierung geändert am für die letzte in beide Richtungen durchgeführte Integration für eine Zeile beibehalten. Diese Zeitstempel werden mit Zeitstempeln in Business Central- und Sales-Datensätzen verglichen. In Business Central befindet sich der Zeitstempel in der Integrationsdatensatztabelle.

Sie können auf Datensätze filtern, die synchronisiert werden sollen, indem Sie die Zeilen-Zeitstempel in den Feldern „Synch. Bearbeitet an Filter“ und „Synch. Int. Tbl. Geänd. Auf Fltr.“.

Die Konfliktfehlermeldung „Der Debitorendatensatz kann nicht aktualisiert werden, weil er ein späteres Änderungsdatum als der Kontodatensatz hat“ oder „Der Kontodatensatz kann nicht aktualisiert werden, weil er ein späteres Änderungsdatum als der Kundendatensatz hat“ kann auftreten, wenn eine Zeile einen Zeitstempel hat, der größer ist als IntegrationTableMapping. „Synchronisierung geändert in Filter“, aber er ist nicht aktueller als der Zeitstempel im Vertriebsintegrationsdatensatz. Es bedeutet, dass die Quellzeile manuell synchronisiert wurde und nicht durch den Eintrag in der Jobwarteschlange. 

Der Konflikt entsteht, weil auch die Zielzeile geändert wurde - der Zeitstempel der Zeile ist aktueller als der Zeitstempel des Sales Integration Record. Die Zielprüfung erfolgt nur bei bidirektionalen Tabellen. 

Diese Datensätze werden jetzt auf die Seite „Übersprungene Synchronisierungsdatensätze“ verschoben, die Sie über die Seite Microsoft Dynamics-Verbindungssetup in Business Central öffnen können. Dort können Sie die beizubehaltenden Änderungen angeben und die Datensätze dann erneut synchronisieren.

## <a name="remove-couplings-between-records"></a>Kopplungen zwischen Datensätzen entfernen
Wenn bei Ihrer Integration ein Fehler auftritt und Sie Datensätze entkoppeln müssen, um die Synchronisierung zu beenden, können Sie dies für einen oder mehrere Datensätze gleichzeitig tun. Sie können einen oder mehrere Datensätze von Listenseiten oder der Seite **Fehler bei der Synchronisierung gekoppelter Daten** durch Auswahl einer oder mehrerer Zeilen und Auswahl von **Kopplung löschen** entkoppeln. Sie können auch alle Kupplungen für eine oder mehrere Tabellenzuordnungen auf der Seite **Zuordnungen der Integrationstabelle** entfernen. 

Wenn eine Entität mit einer unidirektionalen Kopplung in [!INCLUDE[prod_short](includes/prod_short.md)] gelöscht wird, müssen Sie die unterbrochene Kopplung manuell löschen. Wählen Sie dazu auf der Seite **Gekoppelte Daten-Synchronisationsfehler** die Aktion **Für Gelöschte suchen** und löschen Sie dann die Kopplungen.

## <a name="see-also"></a>Siehe auch
[Integration in Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Einrichten des Benutzerkontos für die Integration in Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit Microsoft Dataverse ein](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]