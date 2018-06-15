---
title: Benutzerberechtigungen zuweisen oder bearbeiten | Microsoft Docs
description: "Beschreibt, wie Office 365 Benutzern Business Centrals hinzugefügt wird und vergibt dann Berechtigungen, Zugriffsrechte und Sicherheitseinstellungen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 05/24/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: 443c04799e9aa2b9aa4ede15006ecb5e9773ce6b
ms.contentlocale: de-de
ms.lasthandoff: 05/28/2018

---
# <a name="manage-users-and-permissions"></a>Benutzer und ihre Berechtigungen verwalten.
Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Sobald der Benutzer im Office 365 erzeugt wurde, können sie in das Fensters **Benutzer** importiert werden, und zwar mithilfe der Aktion **Benutzer von Office 365 abrufen**. Benutzer werden Berechtigungssätze abhängig vom Plan, der dem Benutzer in Office 365 zugewiesen.

Sie können dann fortfahren, um den Benutzern Berechtigungssätze zuzuordnen, um festzulegen, in welchen Datenbankobjekten und auf welche Benutzeroberflächenelemente, sie Zugriff haben und auf welche Unternehmen. Sie können Benutzer Benutzergruppen hinzufügen. Damit ist es leichter, dieselben Berechtigungssätze mehreren Benutzern zuzuordnen.

Ein Zugriffsrechtsatz ist eine Sammlung von Berechtigungen für bestimmte Objekte in der Datenbank. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf [!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen können. Eine Anzahl vordefinierter Berechtigungssätze steht standardmäßig zur Verfügung.  

Administratoren nutzen das Fenster **Benutzer einrichten**, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind.

Ein anderes System, das definiert, welche Benutzer zugreifen können, ist das Festlegen von Erfahrungen. Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>So ordnen Sie einem Benutzer ein Berechtigung zu
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie im Fenster **Eingehende Dokumente** das Fenster **Benutzerkarten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Um Benutzer in Benutzergruppen zu ordnen
Sie können Benutzergruppen einrichten, um Ihnen zu helfen, Berechtigungssätze für Benutzergruppen in Ihrem Unternehmen zu verwalten.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer** die Aktion **Benutzergruppen** aus.
3. Wählen Sie im Fenster **Benutzergruppen** die Aktion **Benutzergruppenmitglieder** aus.
6. Wählen Sie im Fenster **Benutzergruppenmitglieder** die Aktion **Benutzer hinzufügen** aus.
7. Um neue oder zusätzliche Benutzer im Fenster **Benutzergruppe** hinzuzufügen, wählen Sie die **Benutzergruppenmitglieder** Aktion aus.
8. Im Fenster **Benutzergruppenmitglieder** in einer neuen Zeile, füllen Sie die Felder wie notwendig aus bestehenden Berechtigungssätzen auswählen.

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>So kopieren Sie eine Benutzergruppe und all seine Zugriffsrechtsätze
Zur schnellen Definition einer neuen Benutzergruppe können Sie eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe zur neuen Benutzergruppe zu kopieren.

Die Mitglieder der Benutzergruppe werden nicht in die neue Benutzergruppe kopiert. Sie müssen sie hinterher manuell hinzufügen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Wählen Sie die Benutzergruppe aus, die Sie kopieren möchten, und wählen Sie **Benutzergruppe kopieren** aus.
3. Im Feld **Neuer Benutzergruppencode** geben Sie einen Namen für die Gruppe an. Wählen Sie dann die Schaltfläche **OK** aus.

Die neue Benutzergruppe wird dem Fenster **Benutzergruppen** hinzugefügt. Fahren Sie fort, um Benutzer hinzuzufügen. Weitere Informationen finden Sie im Abschnitt „So ordnen Sie Benutzer in Benutzergruppen“.

## <a name="to-set-up-user-time-constraints"></a>So richten Sie Zeiteinschränkungen ein
Administratoren nutzen das Fenster Benutzer einrichten, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind. Administratoren können Benutzern Zuständigkeitseinheiten zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Zuständigkeitseinheiten](inventory-responsibility-centers.md).

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Benutzereinrichtung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer einrichten** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder je nach Bedarf aus.

## <a name="see-also"></a>Siehe auch
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

