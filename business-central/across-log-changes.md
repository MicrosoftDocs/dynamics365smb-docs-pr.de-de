---
title: "Benutzer-Aktivität in einem Änderungsprotokoll nachverfolgen | Microsoft Docs"
description: "Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 59afb06e9d43bdadc5ceacf563a9e6faf7439b7b
ms.openlocfilehash: bc56e07a540c24f53b88651ad2b2ff5e1e56a571
ms.contentlocale: de-de
ms.lasthandoff: 12/05/2018

---
# <a name="auditing-changes-in-business-central"></a>Protokollieren von Änderungen in Business Central

Sie können die Änderungsanmeldung aktivieren, sodass [!INCLUDE[d365fin](includes/d365fin_md.md)] Sie den Verlauf der Aktivitäten sehen. Das Protokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Im **Änderungsprotokoll** sind Posten chronologisch bestellt und zeigt Änderungen an, die in den Feldern der angegebenen Tabellen vorgenommen wurden. Das Änderungsprotokoll erfasst alle Änderungen, die auf der Tabelle vorgenommen wurden.

> [!Important]
> Die Konfiguration eines Benutzers in **Änderungsprotokollposten** ist nicht sichtbar, bis die Sitzung des Benutzers neu gestartet wird, was in folgenden Fällen geschieht:
<br />
> * Die Sitzung war abgelaufen und wurde aktualisiert.
> * Der Benutzer hat ein anderes Unternehmen oder Rollencenter ausgewählt.
> * Der Benutzer hat sich an- und wieder angemeldet.

## <a name="working-with-the-change-log"></a>Arbeiten mit dem Änderungsprotokoll

Ein verbreitetes Problem in einem Finanzsystem ist die Lokalisierung von Fehlern und Änderungen von Daten. Es könnte alles sein – von einer falschen Debitorentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung. Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden. Sie müssen jede Tabelle und jedes Feld festlegen, die/das die Anwendung protokollieren soll, und dann das Änderungsprotokoll aktivieren.  

Sie verwenden die Seite **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls. Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.

Wenn Sie auf der Seite **Änderungsprotokoll Einrichtung** die Aktion **Tabellen** wählen, können Sie angeben, welche Tabellen auf Änderungen verfolgt werden sollen, und welche Änderungen verfolgt werden sollen. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfolgt auch mehrere Systemtabellen.

Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**. Wenn Sie Posten löschen möchten, können Sie dies auf der Seite **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.  

## <a name="see-also"></a>Siehe auch
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sortieren](ui-sorting.md)  
[Seite oder Bericht suchen verwenden](ui-search.md)  
[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

