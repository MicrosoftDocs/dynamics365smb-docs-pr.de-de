---
title: "Die Benutzerfreundlichkeit auswählen, um erweiterte Funktionen ein- oder auszublenden| Microsoft Docs"
description: "Erfahren Sie, was die normale und essentielle Suitebenutzerfreundlichkeit für die Benutzerschnittstelle,  Anwendungsbereiche und Ihr Unternehmen bedeutet."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 05/27/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 6ff186cadae5771f131a128b3d3e977800925670
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---
# <a name="changing-which-features-are-displayed"></a>Sie können auswählen, welche Funktionen angezeigt werden
[!INCLUDE[d365fin](includes/d365fin_md.md)] ist dafür ausgelegt, Ihnen zu helfen, Ihr Geschäft zu führen, unabhängig vom Geschäftsbereich. Im Kernstück von [!INCLUDE[d365fin](includes/d365fin_md.md)] finden Sie die Finanzberichtserstattung und die Verkaufs- und Einkaufsprozesse. Sie fügen es der entsprechend den Unternehmensanforderungen hinzu, indem Sie aus AppSource Erweiterungen hinzufügen oder die Benutzeroberfläche ändern, die für Ihren Mandanten setzen. Weitere Informationen finden Sie unter[ Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Mittels der Erweiterungen](ui-extensions.md) im Abschnitt oder Benutzererfahrung auswählen.

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Eine Benutzerfreundlichkeit auswählen, um eine Funktion ein-  oder auszublenden
Die Benutzerfreundlichkeit bestimmt, wie viel der Kernfunktionalität in Fenstern angezeigt wird, mit dem Sie und Ihre Kollegen [!INCLUDE[d365fin](includes/d365fin_md.md)] nutzen. Im Fenster **Unternehmensinformation** können Sie die Benutzerfreundlichkeit für Ihren Mandanten im Feld **Erfahrung** festlegen.

> [!NOTE]  
> Diese Einstellung gilt für alle Anwender in Ihrem Unternehmen. Benutzer können ihre eigene Benutzeroberfläche noch weiter anpassen, indem sie Seitenlayouts und Inhalt ändern. Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs und der Seiten](ui-personalization-user.md).  

Die verfügbaren Optionen werden in der folgenden Tabelle beschrieben.

| Erfahrung | Auswirkungen auf Benutzeroberfläche |
| --- | --- |
| **Standard** |Zeigt nur Kernaktionen und Felder innerhalb der häufigsten Geschäftsfunktionalität, wie Verkauf, Einkauf, Lagerbestand und Finanzen, an. |
| **Wesentlich** |Zeigt alle Aktionen und Felder für alle verfügbaren Geschäftsfunktionalitäten an.|
| **Premium** |Zeigt alle Aktionen und Felder für alle Geschäftsfunktionalität einschließlich, Produktion und Dienstleistungs-Verwaltung an.|

> [!NOTE]  
> Die Erfahrung, aus der Sie auswählen können in [!INCLUDE[d365fin](includes/d365fin_md.md)] hängt von Ihrem Lösungslizenz ab, auch als Plan bezeichnet. Informationen zur **Wesentlich** und **Premium** finden Sie unter [Geschäfts-Zentrale](https://go.microsoft.com/fwlink/?linkid=870242) in der Microsoft Dynamics 365 Marketings-Site. Siehe auch das [!INCLUDE[d365fin](includes/d365fin_md.md)] Lizenzierungs-Handbuch](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409).

> [!IMPORTANT]  
> Alle regulären Benutzer in einer Lösung müssen demselben Plan, Basis oder Premium zugewiesen sein, bevor die Erfahrung für das Unternehmen ausgewählt werden kann. Entsprechend kann ein Benutzer auf erstklassige Funktionen zugreifen, wenn eine oder mehrere andere Benutzer nur auf  b wichtige Funktion nur zugreifen können. Dies ist nicht der Fall für reguläre Benutzer der Art Teammitglieder, interner Administrator, externer Buchhalter und delegierter Administrator, dem jeder ein unterschiedlicher Plan als bei anderen Benutzern in der Lösung zugeordnet werden können.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Erstklassige Funktionen ausführen, nachdem ein Plan aktualisiert wurde
Benutzer werden Plänen in Office 365 Admin Center in Verbindung mit allgemeiner Arbeit zugewiesen, um Business Central Benutzer zu erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Sie können dann, definieren das spezielle Funktionen und Fenster in der Benutzeroberfläche diese Benutzer zum Zugriff erlaubt sind, indem Zugriffsrechtsätze zuweist. Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Um Planänderungen der Benutzergruppen zu aktualisieren
Wenn Sie eine Änderung in den Benutzerplänen in Office 365 Admin Center gemacht haben, wie mehr Benutzer dem Premium Plan hinzuzufügen, muss die Änderung in [!INCLUDE[d365fin](includes/d365fin_md.md)] vorgenommen werden.

1. Als Administrator anmelden.
2. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Bericht suche") aus und geben Sie Benutzer. Wählen Sie dann **Benutzer**und den zugehörigen Link aus.
3. Wählen Sie im Fenster **Benutzer** die Aktion **Alle Benutzergruppen aktualisieren** aus.

Alle neuen Informationen über die Schemata der Benutzer zusammen mit den zugeordneten Benutzergruppen werden jetzt entsprechend den Planänderungen aktualisiert.

### <a name="to-select-the-premium-experience"></a>Die Premium-Umgebung auswählen
Sie können jetzt fortfahren, die neuen Benutzeroberfläche auszuwählen.
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol \"Nach Seite oder Bericht suchen\"") aus, geben Sie **Unternehmensdaten** ein, und wählen Sie dann den verknüpften Link aus.
2. Im Fenster **Unternehmensinformation** können Sie die **Benutzerfreundlichkeit** für Ihren Mandanten im Feld **Inforegister** festlegen.

## <a name="see-also"></a>Siehe auch
[Neue Unternehmen anlegen](about-new-company.md)  
[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)    
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Anpassen [!INCLUDE[d365fin](includes/d365fin_md.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Lizenzierungshandbuches](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

