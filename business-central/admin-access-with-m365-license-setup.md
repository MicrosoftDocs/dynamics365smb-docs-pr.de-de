---
title: Zugriff mit Microsoft 365-Lizenzen einrichten
description: Eine Anleitung, wie Administratoren den Zugriff auf Business Central mit Microsoft 365-Lizenzen konfigurieren können.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: f509c0a8bf5e9320eb0f2712863984221b7138b9
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744995"
---
# <a name="set-up-access-with-microsoft-365-licenses"></a>Zugriff mit Microsoft 365-Lizenzen einrichten 

Administratoren müssen mehrere Aktivitäten abschließen, bevor Benutzer mit ihrer Microsoft 365-Lizenz auf Business Central zugreifen können. Die folgenden Schritte stellen die Mindesteinrichtung dar, die für den Einstieg erforderlich ist.  

## <a name="deploy-the-business-central-app-for-teams"></a>Business Central-App für Teams bereitstellen 

Für Business Central-Lizenzinhaber zum Teilen von Daten in Teams und für Microsoft 365-Lizenzinhaber, um auf diese Daten zugreifen zu können, muss die Business Central-App für Teams installiert sein. Obwohl Benutzer die App selbst installieren können, wird empfohlen, dass Administratoren die zentrale Bereitstellung verwenden. Durch die zentrale Bereitstellung können Sie die App einem breiteren Publikum in der gesamten Organisation zur Verfügung stellen und den Aufwand einzelner Benutzer minimieren. 

Informationen zum zentralen Bereitstellen der Business Central-App für Teams finden Sie unter [Installieren der Business Central-App mit Hilfe der zentralen Bereitstellung](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Wenn Sie zuvor die zentrale Bereitstellung ausgeführt und die App nur für die Sicherheitsgruppe der lizenzierten Business Central-Benutzer bereitgestellt haben, müssen Sie sie erneut ausführen, um sie für zusätzliche Gruppen oder die gesamte Organisation bereitzustellen, je nachdem, wie Sie den Zugriff konfigurieren.

> [!TIP]
> Suchen Sie nach einer schnelleren Möglichkeit, diese Funktion auszuprobieren? Testnutzer können die App installieren unter [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp).

## <a name="configure-permissions"></a>Berechtigungen konfigurieren

Business Central ist von Haus aus sicher und minimiert das Risiko, indem keine Berechtigungen für Microsoft 365-Benutzer standardmäßig gewährt werden. Administratoren müssen Objektberechtigungen konfigurieren, die festlegen, auf welche Tabellen, Seiten und Berichte in Teams nur mit einer Microsoft 365-Lizenz zugegriffen werden kann. Diese Berechtigungen sind die Startberechtigungen, die zugewiesen werden, wenn sich ein Benutzer zum ersten Mal mit seiner Microsoft 365-Lizenz anmeldet. 

So konfigurieren Sie Startberechtigungen:

1. Suchen Sie in Business Central nach **Lizenzkonfiguration**.
2. Wählen Sie die Microsoft 365-Lizenz aus.
3. Wählen Sie oben auf der **Microsoft 365**-Lizenzseite das Bearbeiten-Symbol ![Bearbeiten-Symbol](media/edit-pencil.png) aus, aktivieren Sie dann **Berechtigungen anpassen**. 
4. Fügen Sie im Abschnitt **Benutzerdefinierte Berechtigungssätze** die entsprechenden Berechtigungssätze hinzu und wählen Sie aus, ob sie für ein einzelnes Unternehmen oder alle Unternehmen in der Umgebung gelten.

> [!NOTE]
> Beim Synchronisieren der Benutzerliste in Business Central mit Benutzern in Microsoft 365, werden nur Benutzer, die über eine Business Central-Lizenz verfügen, zur Benutzerliste von Business Central hinzugefügt. Benutzer mit nur einer Microsoft 365-Lizenz werden der Benutzerliste hinzugefügt, wenn sie zum ersten Mal auf Business Central zugreifen. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).

> [!TIP]
> Suchen Sie nach einer schnelleren Möglichkeit, diese Funktionssandbox oder Auswertungsfirma auszuprobieren? Weisen Sie den Berechtigungssatz **D365 Lesen** zu, der den meisten Objekten Berechtigungen erteilt.  

Beim Arbeiten mit mehreren Umgebungen muss die Lizenzkonfiguration auf jede Umgebung angewendet werden und kann in jeder Umgebung unterschiedlich sein. 

Weitere Informationen finden Sie unter [Zuweisen von Berechtigungen zu Benutzern und Gruppen](ui-define-granular-permissions.md) und [Zusammenstellen von Berechtigungssätzen](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="turn-on-access-with-microsoft-365-licenses"></a>Zugriff mit Microsoft 365-Lizenzen aktivieren

Der Zugriff mit Microsoft 365-Lizenzen ist standardmäßig deaktiviert. Der Zugriff muss für jede Umgebung separat aktiviert werden, sodass Administratoren die Kontrolle erhalten und eine gestaffelte Einführung in der gesamten Organisation möglich ist. Sie aktivieren den Zugriff über das Business Central Admin Center: 

1. Wählen Sie in der oberen rechten Ecke **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") > **Admin Center**.  
2. Wählen Sie im Admin Center  **Umgebungen** aus, und wählen Sie dann die Umgebung aus, für die Sie den Lizenzzugriff ändern möchten. 
3. Wählen Sie auf der **Umgebungsdetails**-Seite **Ändern** für die Einstellung **Zugriff mit Microsoft 365-Lizenzen**.
4. In dem Bereich **Microsoft 365-Lizenzen** schalten Sie den Schalter ein. 
5. Wählen Sie **Speichern** aus, wenn Sie fertig sind, und akzeptieren Sie die Bestätigung. Die Änderung tritt sofort in Kraft.

## <a name="test-your-setup"></a>Ihre Einrichtung testen

Um zu überprüfen, ob Ihr Setup für die Produktion bereit ist, helfen Ihnen die folgenden Schritte, das Vertrauen aufzubauen, dass alles so funktioniert, wie es sollte. 

1. Erstellen oder identifizieren Sie zwei Testbenutzer (A und B).

   - Testbenutzer A muss über eine Business Central-Lizenz und Microsoft 365-Lizenz mit Zugriff auf Teams verfügen.
   - Testbenutzer B muss nur eine Microsoft 365-Lizenz mit Zugriff auf Teams haben.

2. Melden Sie sich als Testbenutzer A beim Business Central-Webclient an.

   1. Öffnen Sie einen Datensatz, auf den Testbenutzer B Zugriff haben soll, z. B. eine **Artikel**-Karte in der entsprechenden Firma und Umgebung.
   2. Wählen Sie **Teilen** ![!Aktion auf Seiten mit anderen Apps teilen.](media/share-icon.png) > **Für Teams freigeben**, um das Fenster „Für Teams freigeben“ aufzurufen.
   3. In dem Feld **Freigeben für** fügen Sie Testnutzer B als Empfänger hinzu. 
   4. Warten Sie, bis der Link zu einer Karte erweitert wird, und wählen Sie „Teilen“ aus. 

3. Melden Sie sich bei Microsoft Teams als Testbenutzer B an.

   1. Wählen Sie „Chat“ aus, und öffnen Sie die Unterhaltung mit Testbenutzer A. 
   2. Wählen Sie in der von Testbenutzer A gesendeten Nachricht die Schaltfläche „Details“ auf der Karte aus. Wenn der Business Central-Client angezeigt wird und schreibgeschützt ist, war Ihre Einrichtung erfolgreich. 

> [!TIP]
> Ist ein Fehler aufgetreten? Überprüfen Sie [Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Siehe auch

[Business Central-Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md#minimum-requirements)  
[Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license-troubleshooting.md)  
[Integration von Business Central und Microsoft Teams](across-teams-overview.md)  