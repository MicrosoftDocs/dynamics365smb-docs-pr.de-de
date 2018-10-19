---
title: Verwalten von Rollen und Benutzer | Microsoft Docs
description: Erfahren, wie Benutzer, Profile und Rollencenter in Finance and Operations, Business Central verwaltet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Benutzer, Profile und Rollencenter verstehen

In [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Benutzer von einem Administrator hinzugefügt, der auch Zugriff auf den Bereichen aus Feld [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt, den sie, in ihrer Arbeit benötigen.  

Zugriff auf die Funktionalität wird durch *Benutzergruppen* und *Profile* verwaltet. Als Administrator können Sie Profile zuordnen und ändern, und Sie können Benutzer als Teil des [!INCLUDE[d365fin](includes/d365fin_md.md)] Abonnements hinzufügen und  entfernen.  

## <a name="adding-users"></a>Hinzufügen von Benutzern

Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] online hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://aka.ms/CreateOffice365Users).

Dann kann der Administrator Berechtigungen jedem Benutzerund Benutzergruppen zuweisen. Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Lokale Bereitstellungen von Benutzern

Für lokale Bereitstellungen von [!INCLUDE[d365fin](includes/d365fin_md.md)] kann der Administrator zwischen verschiedenen Autorisierungsmechanismen für Benutzer auswählen. Wenn Sie einen Benutzer erstellen, stellen Sie je nach Anmeldeinformationstyp in der aktuellen [!INCLUDE[server](includes/server.md)]-Instanz verschiedene Informationen bereit. Weitere Informationen finden Sie unter [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) im Abschnitt Verwaltung des Entwicklers und des ITPro-Inhalts für. [!INCLUDE[d365fin](includes/d365fin_md.md)]  

## <a name="profiles"></a>Profile

Alle Mitarbeiter in Ihrem Mandanten, die Zugriff haben auf[!INCLUDE[d365fin](includes/d365fin_md.md)] sind einem *Profil* zugewiesen, das Zugriff  auf das *Rollencenter* gibt.

Profile sind Sammlungen von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzern, die dasselbe Rollencenter nutzen. Ein Rollencenter ist der Einstiegspunkt und die Homepage für [!INCLUDE[d365fin](includes/d365fin_md.md)] und gibt Ihnen Zugriff zu den wichtigsten Aufgaben und zeigt verschiedene Einblicke und Schlüsselleistungsindikatoren (KPIs) über Ihre Arbeit an.  

> [!NOTE]  
>  In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] online können Sie keine Profile einfügen, ändern oder löschen.  

## <a name="configuration-and-personalization"></a>Konfiguration und Anpassung
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
Benutzer personalisieren die Benutzeroberfläche ihrer persönlichen Version, indem sie die Benutzeroberfläche unter ihrer eigenen Benutzeranmeldung anpassen. Diese Anpassung kann vom Administrator gelöscht werden. Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).  

## <a name="see-also"></a>Siehe auch  
[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)  
[Personalisierung als Administrator verwalten](ui-personalization-manage.md)  
[Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md)  

