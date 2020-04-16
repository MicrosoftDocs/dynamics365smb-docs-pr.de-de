---
title: Die Benutzerfreundlichkeit auswählen, um erweiterte Funktionen ein- oder auszublenden| Microsoft Docs
description: Erfahren Sie, was die Essential- und Premium-Stufen der Benutzerfreundlichkeit für die Benutzerschnittstelle, Anwendungsbereiche und Ihr Unternehmen bedeutet.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3329a694f4c27a2a314d82dd2f71eb31c9f36d98
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194619"
---
# <a name="change-which-features-are-displayed"></a>Funktionen, die angezeigt werden ändern
[!INCLUDE[d365fin](includes/d365fin_md.md)] wurde entwickelt, um Ihnen zu helfen, Ihr Unternehmen unabhängig von Größe und Komplexität zu führen. Im Mittelpunkt des Produkts stehen wesentliche Funktionen wie Finanzberichterstattung, Vertrieb, Einkauf und Lagerverwaltung. Mit zunehmender Komplexität des Unternehmens können Sie z.B. Funktionen für das Fertigungs- und Servicemanagement aktivieren.

Sie können die Produktkomplexität und damit die Funktionen definieren, auf die die Benutzer des Unternehmens Zugriff erhalten, indem Sie die Einstellung **Erfahrung** auf der Seite **Firmeninformationen** ändern. Beachten Sie, dass die Erfahrungseinstellung auch geändert werden kann, indem Sie bestimmte Erweiterungen von AppSource hinzufügen. Weitere Informationen finden Sie unter [Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)] mithilfe der Erweiterungen](ui-extensions.md).

Die verfügbaren Optionen werden in der folgenden Tabelle beschrieben.

| Erfahrung | Auswirkungen auf Benutzeroberfläche |
| --- | --- |
| **Essential** |Zeigt alle Aktionen und Felder für alle verfügbaren Geschäftsfunktionalitäten an.|
| **Premium** |Zeigt alle Aktionen und Felder für alle Geschäftsfunktionalität einschließlich, Produktion und Dienstleistungs-Verwaltung an.|

Die unter [!INCLUDE[d365fin](includes/d365fin_md.md)] wählbaren Erfahrungen spiegeln die für das Produkt definierten Lösungslizenzen, sogenannte Pläne, wider. Informationen zu den Plänen Essential und Premium finden Sie unter [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) auf der Microsoft Dynamics 365 Marketing-Seite. Siehe dazu auch [[!INCLUDE[d365fin](includes/d365fin_md.md)]-Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?linkid=2068931) (erfordert Zugriff auf CustomerSource oder PartnerSource).

> [!IMPORTANT]  
> Alle regulären Benutzer in einer Lösung müssen demselben Plan, Basis oder Premium zugewiesen sein, bevor die Erfahrung für das Unternehmen ausgewählt werden kann. Entsprechend kann ein Benutzer auf erstklassige Funktionen zugreifen, wenn eine oder mehrere andere Benutzer nur auf b wichtige Funktion nur zugreifen können. Dies ist nicht der Fall für reguläre Benutzer der Art Teammitglieder, interner Administrator, externer Buchhalter und delegierter Administrator, dem jeder ein unterschiedlicher Plan als bei anderen Benutzern in der Lösung zugeordnet werden können.<br /><br /> Nur Benutzer vom Typ Evaluation oder Premium können den Wert im Feld **Erfahrung** von Essential auf Premium ändern.

Bevor Sie die Benutzereinstellungen eines Unternehmens definieren, definieren Sie den Zugriff der Benutzer auf bestimmte Funktionen und Seiten, indem Sie Berechtigungen zuweisen. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).

Die Einstellung **Erfahrung** gilt für alle Benutzer in einem Unternehmen, aber jeder Benutzer kann seine eigene Erfahrung durch Ändern von Seitenlayouts und Inhalten weiter personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Erstklassige Funktionen ausführen, nachdem ein Plan aktualisiert wurde
Benutzer werden Plänen in Microsoft 365 Admin Center in Verbindung mit allgemeiner Arbeit zugewiesen, um die Business Central-Benutzer zu erstellen. Weitere Informationen finden Sie unter [Benutzer einzeln oder in großen Mengen zu Office 365](https://support.office.com/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc) hinzufügen.

### <a name="to-update-plan-changes-in-users-groups"></a>Um Planänderungen der Benutzergruppen zu aktualisieren
Wenn Sie eine Änderung in den Benutzerplänen in Microsoft 365 Admin Center vorgenommen haben, wie mehr Benutzer dem Premium-Plan hinzuzufügen, muss die Änderung in [!INCLUDE[d365fin](includes/d365fin_md.md)] vorgenommen werden.

1. Als Administrator anmelden.
2. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
3. Wählen Sie auf der Seite **Benutzer** die Aktion **Alle Benutzergruppen neu einrichten**.

Alle neuen Informationen über die Schemata der Benutzer zusammen mit den zugeordneten Benutzergruppen werden jetzt entsprechend den Planänderungen aktualisiert.

### <a name="to-select-the-premium-experience"></a>Die Premium-Umgebung auswählen
Sie können jetzt fortfahren, die neuen Benutzeroberfläche auszuwählen.
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Firmeninformationen** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Unternehmensinformation** können Sie die **Benutzerfreundlichkeit** für Ihren Mandanten im Feld **Inforegister** festlegen.

## <a name="help-assumes-premium-experience"></a>Die Hilfe geht von der Premium-Umgebung aus
Alle Funktionsbeschreibungen in der Dokumentation behandeln [!INCLUDE[d365fin](includes/d365fin_md.md)] die **Premium**-Umgebung, decken also den gesamten Umfang der Benutzeroberflächenelemente ab.

## <a name="see-also"></a>Siehe auch
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Business Central anpassen](ui-customizing-overview.md)  
[Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[Neue Unternehmen anlegen](about-new-company.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Lizenzierungshandbuches](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
