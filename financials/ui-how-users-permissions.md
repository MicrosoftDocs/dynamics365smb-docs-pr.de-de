---
title: "Weisen Sie Berechtigungen zu und Erstellen oder ändern Sie Berechtigungssätze | Microsoft Docs"
description: "Beschreibt, wie Office 365-Benutzer bei Finance and Operations, Business edition hinzugefügt und dann Berechtigungen, Zugriffsrechte und Sicherheitseinstellungen vergeben werden."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7f02d9718f4697e5d7eb9113d52e8d6572555b52
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="manage-users-and-permissions"></a>Benutzer und ihre Berechtigungen verwalten.
Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Sobald der Benutzer im Office 365 erzeugt wurde, können sie in das Fensters **Benutzer** importiert werden, und zwar mithilfe der Aktion **Benutzer von Office 365 abrufen**. Benutzer werden Berechtigungssätze abhängig vom Plan, der dem Benutzer in Office 365 zugewiesen wird zugeordnet.

Sie können dann fortfahren, um den Benutzern Berechtigungssätze zuzuordnen, um festzulegen, in welchen Datenbankobjekten und auf welche Benutzeroberflächenelemente, sie Zugriff haben und auf welche Unternehmen.

Ein Zugriffsrechtsatz ist eine Sammlung von Berechtigungen für bestimmte Objekte in der Datenbank. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf [!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen können. Eine Anzahl vordefinierter Berechtigungssätze steht standardmäßig zur Verfügung. Sie können diese Zugriffsrechtsätze wie bereits definiert verwenden, die Standard-Zugriffsrechtsätze ändern oder zusätzliche eigene Zugriffsrechtsätze erstellen.

Sie können Benutzer Benutzergruppen hinzufügen. Damit ist es leichter, dieselben Berechtigungssätze mehreren Benutzern zuzuordnen.

Administratoren nutzen das Fenster **Benutzer einrichten**, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob  die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind.

## <a name="to-assign-permissions-to-a-user"></a>So ordnen Sie einem Benutzer ein Berechtigung zu
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie im Fenster **Eingehende Dokumente** das Fenster **Benutzerkarten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Um Benutzer in Benutzergruppen zu ordnen
Sie können Benutzergruppen einrichten, um Ihnen zu helfen, Berechtigungssätze für Benutzergruppen in Ihrem Unternehmen zu verwalten. Sie können eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe der neuen Benutzergruppe zu kopieren. Benutzergruppenelemente werden nicht kopiert.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer** die Aktion **Benutzergruppen** aus.
3. Im Fenster **Benutzergruppen** wählen Sie eine vorhandene Benutzergruppe aus, die Sie kopieren möchten, und wählen die Aktion **Benutzergruppe kopieren** aus.
4. In Feld **Neuer Benutzergruppencode** geben Sie den Namen der neuen Benutzergruppe an, und wählen Sie dann die Schaltfläche **OK** aus.

    Als Alternative zum Kopieren, können Sie die neue Aktion auswählen, eine neue Zeile für eine leere Benutzergruppe zu erstellen, die Sie dann manuell ausfüllen.
5. Um den neuen oder zusätzlichen Benutzern, im Fenster **Benutzergruppe** hinzuzufügen, wählen Sie die **Benutzergruppenmitglieder** Aktion aus.
6. Im Fenster **Benutzergruppenmitglieder** in einer neuen Zeile, füllen Sie die Felder wie notwendig aus, indem Sie aus bestehenden Benutzer auswählen.
7. Um neue oder zusätzliche Benutzer im Fenster **Benutzergruppe** hinzuzufügen, wählen Sie die **Benutzergruppenmitglieder** Aktion aus.
8. Im Fenster **Benutzergruppenmitglieder** in einer neuen Zeile, füllen Sie die Felder wie notwendig aus bestehenden Berechtigungssätzen auswählen.

## <a name="to-set-up-user-time-constraints"></a>So richten Sie Zeiteinschränkungen ein
Administratoren nutzen das Fenster Benutzer einrichten, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind. Administratoren können Benutzern Zuständigkeitseinheiten zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Zuständigkeitseinheiten](inventory-responsibility-centers.md).

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Benutzereinrichtung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer einrichten** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder je nach Bedarf aus.

## <a name="see-also"></a>Siehe auch
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Einrichtung und Verwaltung in [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-setup-and-administration.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

