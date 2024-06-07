---
title: 'Ändern, welche Funktionen angezeigt werden'
description: 'Erfahren Sie, was die Essential- und Premium-Stufen der Benutzerfreundlichkeit für die Benutzerschnittstelle, Anwendungsbereiche und Ihr Unternehmen bedeutet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: '1,'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="change-which-features-are-displayed"></a>Angezeigte Features ändern

[!INCLUDE[prod_short](includes/prod_short.md)] wurde entwickelt, um Ihnen zu helfen, Ihr Unternehmen unabhängig von Größe und Komplexität zu führen. Im Mittelpunkt des Produkts stehen wesentliche Funktionen wie Finanzberichterstattung, Vertrieb, Einkauf und Lagerverwaltung. Mit zunehmender Komplexität des Unternehmens können Sie z.B. Funktionen für das Fertigungs- und Servicemanagement aktivieren.

Sie können die Produktkomplexität und damit die Funktionen definieren, auf die die Benutzer des Unternehmens Zugriff erhalten, indem Sie die Einstellung **Erfahrung** auf der Seite **Firmeninformationen** ändern. Beachten Sie, dass die Erfahrungseinstellung auch geändert werden kann, indem Sie bestimmte Erweiterungen von AppSource hinzufügen. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)] mithilfe der Erweiterungen](ui-extensions.md).

Die verfügbaren Optionen werden in der folgenden Tabelle beschrieben.

| Erfahrung | Auswirkungen auf Benutzeroberfläche |
| --- | --- |
| **Essential** |Zeigt alle Aktionen und Felder für alle verfügbaren Geschäftsfunktionalitäten an.|
| **Premium** |Zeigt alle Aktionen und Felder für alle Geschäftsfunktionalität einschließlich, Produktion und Dienstleistungs-Verwaltung an.|

Die unter [!INCLUDE[prod_short](includes/prod_short.md)] wählbaren Erfahrungen spiegeln die für das Produkt definierten Lösungslizenzen, sogenannte Pläne, wider. Informationen zu den Plänen Essential und Premium finden Sie unter [Business Central](https://go.microsoft.com/fwlink/?linkid=2264940) auf der Microsoft Dynamics 365 Marketing-Seite. Siehe auch [[!INCLUDE[prod_short](includes/prod_short.md)] Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?linkid=2264939).

> [!IMPORTANT]  
> Benutzende des Typs Teammitglieder, interner Administrator, externer Buchhalter und delegierter Administrator, denen jeweils ein unterschiedlicher Plan als bei anderen Benutzern in der Lösung zugeordnet werden kann. Nur Benutzer vom Typ Evaluation oder Premium können den Wert im Feld **Erfahrung** von Essential auf Premium ändern.

> [!NOTE]
> Im ersten Veröffentlichungszyklus 2024 kann sich ein Benutzender mit dem Premium-Plan bei einem Unternehmen anmelden, das den Essentials-Plan verwendet. Der Premium-Benutzende kann jedoch keine der Funktionen nutzen, die die Premium-Lizenz bietet. Das Gleiche gilt nicht in die entgegengesetzte Richtung. Benutzende mit dem Essentials-Plan können sich mit dem Premium-Plan nicht bei einem Unternehmen anmelden.

Bevor Sie die Benutzereinstellungen eines Unternehmens definieren, definieren Sie den Zugriff der Benutzer auf bestimmte Funktionen und Seiten, indem Sie Berechtigungen zuweisen. Weitere Informationen finden Sie unter [Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

Die Einstellung **Erfahrung** gilt für alle Benutzer in einem Unternehmen, aber jeder Benutzer kann seine eigene Erfahrung durch Ändern von Seitenlayouts und Inhalten weiter personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Premium-Funktionen aktivieren, nachdem ein Plan aktualisiert wurde

Benutzer werden Plänen in Microsoft 365 Admin Center in Verbindung mit allgemeiner Arbeit zugewiesen, um Business Central Benutzer zu erstellen. Weitere Informationen finden Sie unter [Fügen Sie Benutzer hinzu und weisen Sie gleichzeitig Lizenzen zu](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a>Um Planänderungen der Benutzergruppen zu aktualisieren

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Wenn Sie eine Änderung in den Benutzerplänen im Microsoft 365 Admin Center gemacht haben, wie mehr Benutzer dem Premium Plan hinzuzufügen, muss die Änderung in [!INCLUDE[prod_short](includes/prod_short.md)] aktualisiert werden.

1. Als Administrator anmelden.
2. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
3. Wählen Sie auf der Seite **Benutzer** die Aktion **Benutzer aus Microsoft 365 aktualisieren** aus.

### <a name="to-select-the-premium-experience"></a>Die Premium-Umgebung auswählen

Sie können jetzt fortfahren, die neuen Benutzeroberfläche auszuwählen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Unternehmensdaten** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Unternehmensinformation** können Sie die **Benutzerfreundlichkeit** für Ihren Mandanten im Feld **Inforegister** festlegen.

## <a name="help-assumes-the-premium-experience"></a>Die Hilfe geht von der Premium-Umgebung aus

Alle Funktionsbeschreibungen in der Dokumentation behandeln [!INCLUDE[prod_short](includes/prod_short.md)] die **Premium**-Umgebung, decken also den gesamten Umfang der Benutzeroberflächenelemente ab.

## <a name="see-also"></a>Siehe auch

[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Business Central anpassen](ui-customizing-overview.md)  
[Benutzenden und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md)  
[Neue Unternehmen anlegen](about-new-company.md)  
[Grundlegende Einstellungen ändern](ui-change-basic-settings.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
