---
title: "Weisen Sie Berechtigungen zu und Erstellen oder ändern Sie Berechtigungssätze | Microsoft Docs"
description: "Beschreibt, wie Office 365 Benutzern Financials hinzugefügt wird und vergibt dann Berechtigungen, Zugriffsrechte und Sicherheitseinstellungen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 564ef68a1571611efee32db1cf3759cda6a04c80
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-users-and-permissions"></a>Vorgehensweise: Verwalten Sie Benutzer und Berechtigungen| Microsoft Docs
Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Sobald der Benutzer im Office 365 erzeugt wurde, können sie in das Fensters **Benutzer** importiert werden, und zwar mithilfe der Aktion **Benutzer von Office 365 abrufen**. Benutzer werden Berechtigungssätze abhängig vom Plan, der dem Benutzer in Office 365 zugewiesen wird zugeordnet.

Sie können dann fortfahren, um den Benutzern Berechtigungssätze zuzuordnen, um festzulegen, in welchen Datenbankobjekten und auf welche Benutzeroberflächenelemente, sie Zugriff haben und auf welche Unternehmen.

Ein Zugriffsrechtsatz ist eine Sammlung von Berechtigungen für bestimmte Objekte in der Datenbank. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf |[!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen können. Eine Anzahl vordefinierter Berechtigungssätze steht standardmäßig zur Verfügung. Sie können diese Zugriffsrechtsätze wie bereits definiert verwenden, die Standard-Zugriffsrechtsätze ändern oder zusätzliche eigene Zugriffsrechtsätze erstellen.

Sie können Benutzer Benutzergruppen hinzufügen. Damit ist es leichter, dieselben Berechtigungssätze mehreren Benutzern zuzuordnen.

Administratoren nutzen das Fenster **Benutzer einrichten**, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob  die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind.

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in Suite festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="to-assign-permissions-to-a-user"></a>So ordnen Sie einem Benutzer ein Berechtigung zu
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie im Fenster **Eingehende Dokumente** das Fenster **Benutzerkarten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Um Benutzer in Benutzergruppen zu ordnen
Sie können Benutzergruppen einrichten, um Ihnen zu helfen, Berechtigungssätze für Benutzergruppen in Ihrem Unternehmen zu verwalten. Sie können eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe der neuen Benutzergruppe zu kopieren. Benutzergruppenelemente werden nicht kopiert.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Alternativ wählen Sie im Fenster **Benutzer** die Aktion **Benutzergruppen** aus.
3. Im Fenster **Benutzergruppen** wählen Sie eine vorhandene Benutzergruppe aus, die Sie kopieren möchten, und wählen die Aktion **Benutzergruppe kopieren** aus.
4. In Feld **Neuer Benutzergruppencode** geben Sie den Namen der neuen Benutzergruppe an, und wählen Sie dann die Schaltfläche **OK** aus.

    Als Alternative zum Kopieren, können Sie die neue Aktion auswählen, eine neue Zeile für eine leere Benutzergruppe zu erstellen, die Sie dann manuell ausfüllen.
5. Um den neuen oder zusätzlichen Benutzern, im Fenster **Benutzergruppe** hinzuzufügen, wählen Sie die **Benutzergruppenmitglieder** Aktion aus.
6. Im Fenster **Benutzergruppenmitglieder** in einer neuen Zeile, füllen Sie die Felder wie notwendig aus, indem Sie aus bestehenden Benutzer auswählen.
7. Um neue oder zusätzliche Benutzer im Fenster **Benutzergruppe** hinzuzufügen, wählen Sie die **Benutzergruppenmitglieder** Aktion aus.
8. Im Fenster **Benutzergruppenmitglieder** in einer neuen Zeile, füllen Sie die Felder wie notwendig aus bestehenden Berechtigungssätzen auswählen.

## <a name="to-create-or-modify-permission-sets"></a>Um Berechtigungssätze zu erstellen oder zu ändern
Wenn die Standardberechtigungssätze, die in [!INCLUDE[d365fin](includes/d365fin_md.md)] zur Verfügung gestellt wurden, nicht ausreichen oder für Ihre Organisation nicht geeignet sind, können Sie neue Berechtigungssätze erstellen. Wenn die einzelne Objektberechtigungen, die einen Berechtigungssatz definieren, nicht angemessen sind, dann können Sie einen Berechtigungssatz bearbeiten. Sie können einen Berechtigungssatz manuell erstellen, oder Sie können eine Aufzeichnungsfunktion verwenden, die Ihre Aktionen erfasst, während Sie durch ein Szenario navigieren und dann den benötigten Berechtigungssatz generieren.

### <a name="to-create-or-modify-permission-sets-manually"></a>Um Berechtigungssätze manuell zu erstellen oder zu ändern
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Alternativ wählen Sie im Fenster **Benutzer** die Aktion **Berechtigungssatz** aus.
3. Alternativ wählen Sie im Fenster **Benutzer** die Aktion **Neu** aus.
4. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.
5. Wählen Sie die Aktion **Berechtigungen** aus.
6. Füllen Sie im Fenster **Berechtigungen** die Felder im Kopf nach Bedarf aus.
7. In einer neuen Zeile füllen Sie die fünf Felder für die verschiedenen Berechtigungstypen aus, wie in der folgenden Tabelle beschrieben.

    |Option|Beschreibung|
    |------|-----------|
    |Leer|Gibt an, dass der Berechtigungstyp nicht für das Objekt gewährt wird.|
    |**Ja**|Gibt an, dass der Berechtigungstyp nicht für den direkten Zugriff auf das Objekt gewährt wird.|
    |**Indirekt**|Gibt an, dass der Berechtigungstyp nicht für den indirekten Zugriff auf das Objekt gewährt wird.|

    Indirekte Berechtigungen für eine Tabelle bedeutet, dass Sie die Tabelle und das Lesen von diesem nicht öffnen können, aber Sie können die Daten in dieser Tabelle über ein anderes Objekt, wie eine Seite anzeigen, auf die Sie die Berechtigung haben zuzugreifen. Weitere Informationen finden Sie im Abschnitt "Beispiel - Indirekte Berechtigung" in diesem Thema.

8. Geben Sie im Feld **Sicherheitsfilter** einen Filter ein, den Sie für Berechtigungen anwenden möchten, indem Sie das Feld auswählen, auf das Sie den Zugriff einschränken möchten.

    Wenn Sie beispielsweise einen Sicherheitsfilter erstellen möchten, damit ein Benutzer nur Verkäufe mit einem bestimmten Verkäufercode anzeigen kann, wählen Sie die Feldnummer für das Feld **Verkäufercode** aus. Im Feld **Feldfilter** geben Sie dann den Wert ein, den Sie verwenden möchten, um den Zugriff zu begrenzen. Beispielsweise um Benutzern den Zugriff nur auf Annette Hills Verkäufe zu gewähren, geben Sie AH ein.
9. Wiederholen Sie die Schritte 7 und 8 und fügen Sie Berechtigungen für zusätzliche Objekte dem Berechtigungssatz hinzu.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Um Berechtigungssätze durch die Erfassung Ihrer Aktionen zu erstellen oder zu ändern
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
2. Alternativ wählen Sie im Fenster **Benutzer** die Aktion **Berechtigungssatz** aus.
3. Alternativ wählen Sie im Fenster **Benutzer** die Aktion **Neu** aus.
4. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.
5. Wählen Sie die Aktion **Berechtigungen** aus.
6. Alternativ wählen Sie im Fenster **Berechtigung** die Aktion **Start** aus.

    Ein Aufnahmeprozesses beginnt, alle Ihre Aktionen in der Benutzeroberfläche zu erfassen.
7. Wechseln Sie zu den verschiedenen Möglichkeiten und Aktivitäten in [!INCLUDE[d365fin](includes/d365fin_md.md)] für die Benutzer mit diesem Berechtigungssatz, die darauf zugreifen sollen. Sie müssen die Aufgaben ausführen, für die Sie Berechtigungen erfassen möchten.
8. Wenn Sie die Erfassung abschließen möchten, kehren Sie zum Fenster **Berechtigungen** zurück, und wählen Sie die **Beenden** Aktion aus.
9. Wählen Sie die Schaltfläche **Ja**, um die erfassten Berechtigungen dem neuen Berechtigungssatz zuzuordnen.
10. Für jedes Objekt in der erfassten Liste geben Sie an, ob Benutzer in der Lage sind, Datensätze in den erfassen Tabellen einzufügen, zu ändern oder zu löschen. Siehe Schritt 7 im Abschnitt "Berechtigungssätze manuell zu erstellen oder zu verändern".

### <a name="example---indirect-permission"></a>Beispiel - Indirekte Berechtigungen
Sie können indirekte Berechtigungen zuweisen, um ein Objekt nur über ein anderes Objekt zu verwenden.
Beispielsweise kann ein Benutzer die Berechtigung haben, Codeunit 80 **Verkaufsbuchung** auszuführen. Die **Verkaufsbuchung** Codeunit führt viele Aufgaben aus, einschließlich der Bearbeitung von Tabelle 37 **Verkaufsposition** aus. Wenn der Benutzer ein Verkaufsdokument in der Codeunit **Verkaufsbuchung** buch, überprüft [!INCLUDE[d365fin](includes/d365fin_md.md)], ob der Benutzer über die Berechtigung zum Bearbeiten der Tabelle **Einkaufszeile** verfügt. Wenn nicht, kann die Codeunit ihre Aufgaben nicht ausführen und der Benutzer erhält eine Fehlermeldung. In diesem Fall wird die Codeunit erfolgreich ausgeführt.

Jedoch muss der Anwender keinen vollen Zugriff auf die Tabelle **Verkaufszeile** haben, um Codeunit auszuführen. Wenn der Benutzer über indirekte Berechtigungen für die Tabelle **Verkaufszeile** verfügt, wird die Codeunit **Verkaufseinheit** erfolgreich ausgeführt. Wenn ein Benutzer über indirekte Berechtigungen verfügt, kann dieser Benutzer die Tabelle **Verkaufszeile** nur ändern, indem die **Verkaufsbuchung** Codeunit oder ein anderes Objekt ausgeführt wird, das die Berechtigung zum ändern der Tabelle **Verkaufsposition** hat. Der Benutzer kann die Tabelle **Verkaufsposition** nur von unterstützten Anwendungsbereichen aus ändern. Der Benutzer kann die Funktion mit anderen Methoden nicht unbeabsichtigt oder böswillig ausführen.

## <a name="to-set-up-user-time-constraints"></a>So richten Sie Zeiteinschränkungen ein
Administratoren nutzen das Fenster Benutzer einrichten, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob  die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind. Administratoren können Benutzern Zuständigkeitseinheiten zuordnen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")aus und geben Sie **Benutzereinrichtung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer einrichten** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder je nach Bedarf aus.

## <a name="see-also"></a>Siehe auch
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Willkommen bei [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

