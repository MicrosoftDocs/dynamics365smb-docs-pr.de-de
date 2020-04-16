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
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 82b5f3ec52be27c4fbe60a6a63a0cfc5f6f1bd7c
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196543"
---
# <a name="troubleshooting-synchronization-errors"></a>Fehlerbehebung bei Synchronisationsfehlern
Bei der Integration von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit Common Data Service sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief. In diesem Thema werden einige der typischen Fehler aufgeführt, die auftreten, und es werden einige Hinweise zu deren Behebung gegeben.

Fehler treten häufig auf, wenn ein Benutzer gekoppelte Datensätze bearbeitet hat oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist. Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzer diese selbst beheben. Diese Fehler werden durch Aktionen verursacht, z. B. Löschen eines Datensatzes in einer, jedoch nicht in beiden Geschäftsanwendungen und anschließendes Synchronisieren. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).

## <a name="example"></a>Beispiel
Dieses Video zeigt ein Beispiel für die Fehlerbehebung bei Fehlern, die bei der Synchronisierung mit dem Vertrieb aufgetreten sind. Der Prozess ist für alle Integrationen derselbe. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators. Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen. Beispiele für typische Probleme sind:  
  
* Die den Benutzern zugewiesenen Berechtigungen und Rollen sind nicht korrekt.  
* Das Administratorkonto wurde als Integrationsbenutzer angegeben.  
* Das Passwort des Integrationsbenutzers ist so eingestellt, dass eine Änderung erforderlich ist, wenn der Benutzer sich anmeldet.  
* Die Wechselkurse für Währungen sind in der einen oder anderen App nicht angegeben.  
  
Sie müssen die Fehler manuell beheben. Es gibt jedoch einige Möglichkeiten, wie die Seite Ihnen helfen kann. Beispiel:  

* Die Felder **Quelle** und **Ziel** können Links zu dem Datensatz enthalten, in dem der Fehler gefunden wurde. Klicken Sie auf den Link, um den Datensatz zu öffnen und den Fehler zu untersuchen.  
* Die Aktion **Einträge löschen, die älter als 7 Tage sind** und die Aktion **Alle Einträge löschen** wird die Liste bereinigen. In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft. Vorsicht walten lassen. Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.

Manchmal können die Zeitstempel in Datensätzen zu Konflikten führen. In der Tabelle „CDS-Integrationsdatensatz“ werden die Zeitstempel „Letzte Synchronisierung geändert am“ und „Letzte CDS-Synchronisierung geändert am“ für die letzte in beide Richtungen durchgeführte Integration für einen Datensatz beibehalten. Diese Zeitstempel werden mit Zeitstempeln in Business Central- und Sales-Datensätzen verglichen. In Business Central befindet sich der Zeitstempel in der Integrationsdatensatztabelle.

Sie können nach Datensätzen filtern, die synchronisiert werden sollen, indem Sie die Datensatz-Zeitstempel in den Tabellenfeldern „Integration Table Mapping“ und „Synch. Modifiziert bei Filter“ und „Synch. Int. Tbl. Geänd. Auf Fltr.“.

Die Konfliktfehlermeldung „Der Debitorendatensatz kann nicht aktualisiert werden, weil er ein späteres Änderungsdatum als der Kontodatensatz hat“ oder „Der Kontodatensatz kann nicht aktualisiert werden, weil er ein späteres Änderungsdatum als der Kundendatensatz hat“ kann auftreten, wenn ein Datensatz einen Zeitstempel hat, der größer ist als IntegrationTableMapping. „Synchronisierung geändert in Filter“, aber er ist nicht aktueller als der Zeitstempel im Vertriebsintegrationsdatensatz. Dies bedeutet, dass der Quelldatensatz manuell und nicht über den Auftragswarteschlangenposten synchronisiert wurde. 

Der Konflikt entsteht, weil auch der Zielsatz geändert wurde - der Zeitstempel des Datensatzes ist aktueller als der Zeitstempel des Sales Integration Record. Die Zielprüfung erfolgt nur für bidirektionale Tabellen. 

Diese Datensätze werden jetzt auf die Seite „Übersprungene Synchronisierungsdatensätze“ verschoben, die Sie über die Seite Microsoft Dynamics-Verbindungssetup in Business Central öffnen können. Dort können Sie die beizubehaltenden Änderungen angeben und die Datensätze dann erneut synchronisieren.

## <a name="see-also"></a>Siehe auch
[Integrieren in Common Data Service](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Einrichten des Benutzerkontos für die Integration in Common Data Service](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit Common Data Service ein](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  
