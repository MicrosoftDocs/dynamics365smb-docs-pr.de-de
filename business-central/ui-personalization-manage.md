---
title: Anpassen von Seiten für Rollen | Microsoft Docs
description: Erfahren Sie, wie Sie die Benutzeroberfläche für ein Profil (eine Rolle) anpassen, sodass allen Benutzern, die diese Rolle zugewiesen haben, ein benutzerdefinierter Arbeitsbereich angezeigt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cf7f261f945828b78db55cde0dda70d12b158127
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760342"
---
# <a name="customize-pages-for-profiles"></a>Seiten für Profile anpassen
Benutzer können Seiten für ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

Administratoren können Seiten für ein Profil anpassen, z. B. entsprechend der jeweiligen Geschäftsrolle oder Abteilung, sodass allen Benutzern, denen das Profil zugewiesen ist, das angepasste Seitenlayout angezeigt wird. Als Administrator passen Sie die Seiten an, indem Sie dieselben Funktionen verwenden wie Benutzer, wenn sie Personalisierungen vornehmen.

> [!NOTE]
> Die typische geschäftliche Verwendung eines Profils ist eine Rolle. Ein Profil wird daher *Profil (Rolle)* benannt in der Benutzeroberfläche.

Die Seitenanpassung beginnt mit **Profile (Rollen)** Seite, Ausgangspunkt des Administrators für die Verwaltung der Benutzerprofile auf einzelnen Profilkarten. Zusätzlich zum Anpassen des Seitenlayouts steuern Sie verschiedene andere Einstellungen für Profile in der **Profil (Rolle)** Seite für jedes Profil. Weitere Informationen finden Sie unter [Profile verwalten](admin-users-profiles-roles.md).

## <a name="to-customize-pages-for-a-profile"></a>Um Seiten für ein Profil anzupassen
1. Wählen Sie die ![Glühbirne , die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Profile (Rollen)** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie dir Zeile für die Personalisierungsseite, die Sie löschen möchten, und wählen die Aktion **Bearbeiten** aus.
3. Wählen Sie die Aktion **Seiten anpassen**.

    [!INCLUDE[prod_short](includes/prod_short.md)] öffnet eine neue Browser-Registerkarte für das ausgewählte Profil mit dem Banner **Anpassen** Banner aktiviert. Das **Anpassen** Banner bietet die gleiche Funktionalität wie das **Personalisierung** Banner, das den Benutzern zur Verfügung steht.

4. Passen Sie die Seiten an die Anforderungen der jeweiligen Rolle oder Abteilung an, so wie es ein Benutzer bei der Personalisierung tun würde. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

    > [!NOTE]
    > Um während der Personalisierung zu navigieren, drücken Sie Strg + Klicken auf eine Aktion, wenn diese durch die Pfeilspitze hervorgehoben ist.

5. Wenn Sie das Layout einer oder mehrerer Seiten geändert haben, wählen Sie die Schaltfläche **Fertig** im Banner **Anpassen**.
6. Schließen Sie die Browser-Registerkarte.

Die Anpassung von Seiten wird jetzt für das Profil aufgezeichnet.

## <a name="to-view-all-customized-pages-for-a-profile"></a>Um angepasste Seiten für ein Profil anzuzeigen

Sie können sich einen Überblick darüber verschaffen, welche Seiten für ein Profil angepasst wurden, um beispielsweise zu planen, welche Seiten weiter angepasst oder gelöscht werden sollen.

- Auf der Seite **Profil (Rolle)** wählen Sie die Aktion **Angepasste Seiten verwalten**.

Auf der Seite **Benutzerdefinierte Seiten** können Sie Anpassungen löschen und Fehler beheben, indem Sie nach potenziellen Problemen suchen.  

## <a name="to-delete-all-customizations-for-a-profile"></a>Löschen aller Anpassungen für ein Profil
Sie können alle Anpassunge, die Sie für ein Profil vorgenommen haben, stornieren. Mit einer Erweiterung eingeführte Anpassungen und von einem Benutzer vorgenommene Personalisierungen werden nicht gelöscht. Sie können alle Personalisierungen mit einer anderen Aktion löschen. Weitere Informationen finden Sie unter [Löscht alle von einem Benutzer vorgenommenen Personalisierungen](admin-users-profiles-roles.md#to-delete-all-personalizations-made-by-a-user).

- Auf der **Profil (Rolle)** Seite wählen Sie auf der Seite für ein benutzerdefiniertes Profil die Option **Löschen Sie benutzerdefinierte Seiten** Aktion.

Das Seitenlayout für das Profil wird auf das Standardlayout zurückgesetzt.  

## <a name="to-delete-customization-for-specific-pages-for-a-profile"></a>So löschen Sie die Anpassung für bestimmte Seiten eines Profils
Sie können auch alle individuellen Seitenanpassungen löschen, die Sie für ein gemacht haben. Mit einer Erweiterung eingeführte Anpassungen und von einem Benutzer vorgenommene Personalisierungen werden nicht gelöscht. Sie können eine bestimmte Seitenpersonalisierung mit einer anderen Aktion löschen. Weitere Informationen finden Sie unter [So löschen Sie alle Personalisierungen für bestimmte Seiten](admin-users-profiles-roles.md#to-delete-personalizations-for-specific-pages).

1. Auf der Seite **Profil (Rolle)** wählen Sie die Aktion **Angepasste Seiten verwalten**.
2. Auf der Seite **Angepasste Seiten** wählen Sie mindestens eine Zeile für Seitenanpassungen aus, die Sie löschen möchten, und wählen Sie dann die Aktion **Löschen** aus.

Das Layout der ausgewählten Seiten wird an die von Ihnen vorgenommenen Änderungen angepasst.

## <a name="see-also"></a>Siehe auch

[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
