---
title: Verwalten von Rollen und Benutzer | Microsoft Docs
description: Erfahren, wie Benutzer, Profile und Rollencenter in Finanzen and Operations, Business Central verwaltet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "925377"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Benutzer, Profile und Rollencenter verstehen

In [!INCLUDE[d365fin](includes/d365fin_md.md)], werden Benutzer von einem Administrator hinzugefügt, der auch Zugriff auf den Bereichen aus Feld [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt, den sie, in ihrer Arbeit benötigen.  

Zugriff auf die Funktionalität wird durch *Benutzergruppen* und *Profile* verwaltet. Als Administrator können Sie Profile zuordnen und ändern, und Sie können Benutzer als Teil des [!INCLUDE[d365fin](includes/d365fin_md.md)] Abonnements hinzufügen und  entfernen.  

## <a name="adding-users"></a>Hinzufügen von Benutzern

Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] online hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://aka.ms/CreateOffice365Users).

Dann kann der Administrator Berechtigungen jedem Benutzerund Benutzergruppen zuweisen. Weitere Informationen finden Sie unter [Verwalten von Benutzern und Berechtigungen](ui-how-users-permissions.md).  

Die leistungsstarksten Berechtigungen, die ein Benutzer haben kann, ist der SUPER-Berechtigungssatz. Jeder Mandant muss mindestens einen Benutzer mit diesem Berechtigungssatz haben, aber es ist ein Verfahren, jedem Benutzer Berechtigungen zu geben, die ihren Arbeitsanforderungen in [!INCLUDE[prodshort](includes/prodshort.md)] entsprechen und nicht mehr. Dies ist hilfreich, um sicherzustellen, dass Benutzer nur Zugriff auf Daten haben, die für ihre Arbeit wichtig sind.  

> [!TIP]
> Es ist eine Verfahren, sicherzustellen, dass auch der Office 365 Administrator den SUPER-Berechtigungssatz hat in [!INCLUDE[prodshort](includes/prodshort.md)], weil dies Verwaltungsaufgaben viele einfacher macht, einschließlich Aufstellungsintegration mit anderen Apps.

### <a name="users-of-on-premises-deployments"></a>Lokale Bereitstellungen von Benutzern

Für lokale Bereitstellungen von [!INCLUDE[d365fin](includes/d365fin_md.md)] kann der Administrator zwischen verschiedenen Autorisierungsmechanismen für Benutzer auswählen. Wenn Sie einen Benutzer erstellen, stellen Sie je nach Anmeldeinformationstyp in der aktuellen [!INCLUDE[server](includes/server.md)]-Instanz verschiedene Informationen bereit. Weitere Informationen finden Sie unter [Authentifizierungs- und Anmeldeinformationstypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) im Abschnitt Verwaltung des Entwicklers und des ITPro-Inhalts für. [!INCLUDE[d365fin](includes/d365fin_md.md)]  

## <a name="profiles"></a>Profile

Alle Mitarbeiter in Ihrem Mandanten, die Zugriff haben auf[!INCLUDE[d365fin](includes/d365fin_md.md)] sind einem *Profil* zugewiesen, das Zugriff  auf das *Rollencenter* gibt.

Profile sind Sammlungen von [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzern, die dasselbe Rollencenter nutzen. Ein Rollencenter ist der Einstiegspunkt und die Homepage für [!INCLUDE[d365fin](includes/d365fin_md.md)] und gibt Ihnen Zugriff zu den wichtigsten Aufgaben und zeigt verschiedene Einblicke und Schlüsselleistungsindikatoren (KPIs) über Ihre Arbeit an.  

> [!NOTE]  
>  In der aktuellen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] online können Sie keine Profile einfügen, ändern oder löschen.  

### <a name="CreateProfile"></a>Erstellen eines Profils

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus, geben Sie **Profil-Liste** ein, und wählen Sie dann den zugehörigen Link aus.  

2.  Auf der Seite **Profilliste** wählen Sie die **Neu** Aktion aus, um die Seite **Neue Profil-Karte** zu öffnen.  

3.  Geben Sie im Feld **Profil-ID** einen Namen ein, der die gewünschte Rolle des Benutzers beschreibt.  

4.  Geben Sie im Feld **Beschreibung** eine Beschreibung der Profil-ID, beispielsweise **Auftragsverarbeitung** ein.  

5.  Legen Sie das Feld **Rollencenter-ID** auf das Rollencenter fest, das Sie dem Profil zuweisen wollen.  

Das Verfahren zum Ändern eines vorhandenen Profils ist dasselbe, außer dass Sie ein vorhandenes Profil in der **Profilliste** auswählen, anstatt auf **Neu** zu klicken.  


### <a name="copy-a-profile"></a>So kopieren Sie ein Profil
Durch Kopieren eines Profils sparen Sie Zeit, wenn Sie ähnlichen Einstellungen in einem Profil verwenden möchten und nur einige wenige Einstellungen ändern möchten.

1.  Öffnen Sie das Profil, das Sie kopieren möchten, und wählen Sie dann die Aktion **Profil kopieren** aus.

2.  Geben Sie im Feld **Neue Profil-ID** einen Namen für das zu kopierende Profil ein.

3.  Legen Sie das Feld **Neuer Profilbereich** auf eines der Folgenden fest:

    - **System**, damit das neue Profil für alle Tenantdatenbanken verfügbar ist, die die Anwendung verwenden.
    - **Tenant**, damit das neue Profil nur der aktuellen Tenantdatenbank zur Verfügung steht.
4. Wenn Sie fertig sind, wählen Sie die Schaltfläche **OK** aus.

### <a name="ExportImportProfile"></a>Exportieren und Importieren von Profilen

Sie können Profile als XML-Dateien aus und nach einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank exportieren, bzw. importieren. Durch das Exportieren und das Importieren eines Profils können Sie Zeit speichern, wenn Sie die Benutzeroberfläche konfigurieren, da Sie eine vorhandene Profilkonfiguration wieder verwenden, statt ein Profil von Grund auf neu konfigurieren zu müssen. Wenn Sie ein Profil haben, das in einer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbank konfiguriert ist und Sie alle oder einige derselben Profilkonfigurationen in einer anderen Datenbank erneut verwenden möchten, können Sie das Profil in eine XML-Datei exportieren. Anschließend können Sie die XML-Profildatei in die andere Datenbank importieren.

-   Um ein Profil zu exportieren, können Sie die **Profile exportieren** Aktion aus **Profilübersicht** oder **Profilkarte** auswählen oder Sie können **Profile exportieren** suchen. Speichern Sie die XML-Datei an einem Speicherort auf Ihrem Computer oder Netzwerk.

-   Um ein Profil zu importieren, können Sie die **Profile importieren** Aktion aus Profilübersicht oder **Profilliste** auswählen oder Sie können **Profile importieren** suchen. 

    > [!NOTE]  
    >  Sie können kein Profil importieren, das bereits in der Datenbank vorhanden ist, auch wenn die XML-Datei einen anderen Namen oder unterschiedlichen Inhalt hat. Sie müssen das vorhandene Profil löschen, bevor Sie das neue Profil importieren können.


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
