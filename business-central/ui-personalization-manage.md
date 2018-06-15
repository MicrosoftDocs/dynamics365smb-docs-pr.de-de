---
title: Verwaltung von Administrator als Personalisierung in Financials | Microsoft Docs
description: "Erfahren Sie, wie Sie die Benutzeroberfläche anpassen, damit diese Ihren Bedürfnissen entspricht."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 2d9b45bf21d325e60beadedfc94827d7f3fda075
ms.contentlocale: de-de
ms.lasthandoff: 04/18/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Personalisierung als Administrator verwalten
<!--NAV in the Web client-->
Benutzer können ihren Arbeitsbereich personalisieren, um ihren Bedürfnissen zu entsprechen. Als Administrator können Sie Anpassungen steuern und verwalten, indem Sie die Möglichkeit deaktivieren, dass Benutzer Seiten anpassen und sämtliche Seitenanpassungen löschen, die Benutzer vorgenommen haben.

## <a name="disable-personalization-for-a-profile"></a>Personalisierung für ein Profil deaktivieren
Sie können verhindern, dass alle Benutzer, die zu einem bestimmten Profil gehören, ihre Seiten personalisieren können.
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”") aus, geben Sie **Profile** ein, und wählen Sie dann den zugehörigen Link aus.
2.  Wählen Sie das Profil aus, das Sie ändern möchten.
3. Aktivieren Sie das Kontrollkästchen **Anpassung deaktivieren**, und klicken Sie dann auf die Schaltfläche **OK**.

## <a name="clear-user-personalizations"></a>Benutzerpersonalisierung deaktivieren

Die Löschung der Seitenanpassung ändert die Seite oder erstellt das ursprüngliche Layout wieder. Es gibt zwei Möglichkeiten, die Anpassungen zu löschen, die Benutzer auf Seiten vorgenommen haben: mit der Seite **Benutzeranpassung löschen** und mithilfe der Anwendung der Seite **Benutzeranpassungskarte**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Benutzeranpassungen löschen mithilfe der Seite Benutzeranpassungen löschen

Die Seite **Benutzeranpassung löschen** gibt Ihnen die Möglichkeit, die Personalisierung für eine Seite oder pro Benutzer zu löschen.

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen") und geben **Benutzerpersonalisierung löschen** ein und wählen dann den zugehörigen Link aus.

    Die Seite führt alle Seiten auf, die angepasst wurden und den Benutzer, denen sie gehören.

    >[!NOTE]
    > Ein Häkchen in den Spalten **Vorgänger-Anpassung** bedeutet, dass die Personalisierung in einem vorherigen Version von, die erforderlich war [!INCLUDE[d365fin](includes/d365fin_md.md)]die Anpassung, Bearb die unterscheidet, als sie jetzt zu konfigurieren. Benutzer, die versuchen, diese Seiten zu personalisieren, können dies nicht tun, es sei denn, sie entsperren die Seite. Weitere Informationen finden Sie unter [Warum eine Seite zum Personalisieren gesperrt ist](ui-personalization-locked.md).

2. Wählen Sie den Posten, den Sie löschen möchten, und wählen die Aktion **Löschen** aus.

    Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Benutzeranpassungen löschen mithilfe der Seite Benutzeranpassungskarte.

Die Seite **Benutzeranpassungskarte** gibt Ihnen die Möglichkeit, die Personalisierung für alle Seiten für eijnen bestimmten Benutzer zu löschen. Dazu müssen Sie die Schreibberechtigung für Tabelle 2000000072 **Profil** haben.

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png " Symbol Nach Bericht suche") aus und geben Sie **Benutzerpersonalisierung** ein und wäheln dann den zugehörigen Link aus.

    Die Seite **Benutzeranpassung** führt alle Benutzer auf, die möglicherweise eine personalisierte Seite haben. Wenn Sie einen Benutzer in der Übersicht nicht finden können, bedeutet dies, dass sie keine personalisierten Seiten haben.

2. Wählen den Benutzer aus der Liste aus und wählen Sie dann die Aktion **Bearbeiten** aus.

3.  Wählen Sie auf der Registerkarte **Aktionen** **Personalisierte Seiten löschen** aus.

    Der Benutzer sieht die Änderungen das nächste Mal bei der Anmeldung.

## <a name="see-also"></a>Siehe auch
[Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  

