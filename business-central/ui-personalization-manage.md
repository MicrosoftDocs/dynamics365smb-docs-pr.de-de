---
title: Verwaltung von Personalisierung als Administrator in Business Central | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen entspricht.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250595"
---
# <a name="managing-personalization-as-an-administrator"></a>Personalisierung als Administrator verwalten

 Benutzer können ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen. Als Administrator steuern und verwalten Sie Personalisierungen nach:

-   Aktivieren oder Deaktivieren der Personalisierungsfunktion für die gesamte Anwendung (nur lokale Installation).
-   Aktivieren oder Deaktivieren der Personalisierungsfunktion für Benutzer eines bestimmten Profils.
-   Löschen aller Seitenanpassungen, die Benutzer vorgenommen haben.

## <a name="EnablePersonalization"></a> So aktivieren oder deaktivieren Sie Personalisierung (nur lokal)

Standardmäßig ist die Personalisierung im Client nicht aktiviert. Sie aktivieren oder deaktivieren die Personalisierung, indem Sie die Konfigurationsdatei (navsettings.json) der Business Central-Web Server-Instanz ändern, die dem Clients dient.

1. Um die Personalisierung zu aktivieren, müssen Sie die folgende Zeile in der navsettings.json-Datei hinzufügen:

    ```
    "PersonalizationEnabled": "true"
    ```

    Um die Personalisierung zu deaktivieren, entfernen Sie diese Zeile oder bearbeiten sie folgendermaßen:

    ```
    "PersonalizationEnabled": "false"
    ```

    Weitere Informationen darüber, wie Sie die navsettings.json-Datei ändern, finden Sie unter [Direktes Ändern der navsettings.json-Datei](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings)

2. Generieren Sie die Anwendungssymbole und laden Sie diese herunter.

    Dieser Schritt ist optional und nicht erforderlich, um die Personalisierung zu aktivieren. Er stellt jedoch sicher, dass neue Seiten, die von den Entwicklern erstellt werden, angepasst werden können.

    1. Zuerst generieren Sie die Symbole, indem Sie die finsql.exe mit dem Befehl `generatesymbolreference` ausführen. Die finsql.exe-Datei befindet sich im Installationsordner für die [!INCLUDE[server](includes/server.md)]- und Dynamics NAV-Entwicklungsumgebung (CSIDE). Um die Symbole zu erstellen, öffnen Sie eine Eingabeaufforderung, navigieren zum Verzeichnis, in dem die Datei gespeichert ist, und führen folgenden Befehl aus:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Beispiel:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Weitere Informationen finden Sie unter [Gleichzeitiges Ausführen von C/SIDE und AL](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Konfigurieren Sie die [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-Instanz zu: **Laden der Anwendungssymbolverweise bei Serverstart aktivieren** (EnableSymbolLoadingAtServerStartup). Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>So deaktivieren Sie die Personalisierung für ein Profil

Sie können verhindern, dass alle Benutzer, die zu einem bestimmten Profil gehören, ihre Seiten personalisieren können.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Profile** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie das Profil aus, das Sie ändern möchten.
3. Aktivieren Sie das Kontrollkästchen **Anpassung deaktivieren**, und klicken Sie dann auf die Schaltfläche **OK**.

## <a name="to-clear-user-personalizations"></a>So löschen Sie Benutzeranpassungen

Die Löschung der Seitenanpassung ändert die Seite oder erstellt das ursprüngliche Layout wieder. Es gibt zwei Möglichkeiten, die Anpassungen zu löschen, die Benutzer auf Seiten vorgenommen haben: mit der Seite **Benutzeranpassung löschen** und mithilfe der Anwendung der Seite **Benutzeranpassungskarte**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>So löschen Sie Benutzeranpassungen mithilfe der Seite "Benutzeranpassungen löschen"

Die Seite **Benutzeranpassung löschen** gibt Ihnen die Möglichkeit, die Personalisierung für eine Seite oder pro Benutzer zu löschen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung löschen** ein, und wählen dann den zugehörigen Link aus.

    Die Seite führt alle Seiten auf, die angepasst wurden und den Benutzer, denen sie gehören.

    >[!NOTE]
    > Ein Häkchen in den Spalten **Vorgänger-Anpassung** bedeutet, dass die Personalisierung in einem vorherigen Version von, die erforderlich war [!INCLUDE[d365fin](includes/d365fin_md.md)]die Anpassung, Bearb die unterscheidet, als sie jetzt zu konfigurieren. Benutzer, die versuchen, diese Seiten zu personalisieren, können dies nicht tun, es sei denn, sie entsperren die Seite. Weitere Informationen finden Sie unter [Warum eine Seite zum Personalisieren gesperrt ist](ui-personalization-locked.md).

2. Wählen Sie den Posten, den Sie löschen möchten, und wählen die Aktion **Löschen** aus.

    Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>So löschen Sie Benutzeranpassungen mithilfe der Seite "Benutzeranpassungskarte".

Die Seite **Benutzeranpassungskarte** gibt Ihnen die Möglichkeit, die Personalisierung für alle Seiten für eijnen bestimmten Benutzer zu löschen. Dazu müssen Sie die Schreibberechtigung für Tabelle 2000000072 **Profil** haben.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzeranpassung** ein, und wählen dann den zugehörigen Link aus.

    Die Seite **Benutzeranpassung** führt alle Benutzer auf, die möglicherweise eine personalisierte Seite haben. Wenn Sie einen Benutzer in der Übersicht nicht finden können, bedeutet dies, dass sie keine personalisierten Seiten haben.

2. Wählen den Benutzer aus der Liste aus und wählen Sie dann die Aktion **Bearbeiten** aus.

3. Wählen Sie auf der Registerkarte **Aktionen** **Personalisierte Seiten löschen** aus.

    Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.

## <a name="see-also"></a>Siehe auch
[Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
