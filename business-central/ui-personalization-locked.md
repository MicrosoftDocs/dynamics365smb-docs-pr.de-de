---
title: Warum eine Seite für Personalisierungen gesperrt ist
description: Für Sie ist möglicherweise die Personalisierung einer Seite blockiert. Lesen Sie hier, wie Sie sie entsperren können, um sie zu personalisieren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.search.form: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 503ff89fd1e1c5c40b55929f80ce390d1a5fc307
ms.sourcegitcommit: f9143302b8271f5924a027cacdf29dc37c95f4c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8655436"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Warum eine Seite für Personalisierungen gesperrt ist

Es gibt zwei Bedingungen, die Sie am Personalisieren einer Seite hindern. Entweder ist die Seite gesperrt (angezeigt durch das Symbol ![Personalisierungssperre.](media/personalization-lock-icon.png "Personalisieren sperren")) oder sie ist gesperrt (angezeigt durch das Symbol ![Personalisierung gesperrt.](media/personalization-blocked-icon.png "Personalisierung blockiert") Symbol).

## <a name="locked-from-personalizing"></a>Für Personalisierung gesperrt

Wenn es ein ![Personalisierungssperre.](media/personalization-lock-icon.png "Personalisieren sperren") Symbol im **Personalisierung**-Banner angezeigt wird, wenn Sie eine Seite öffnen, können Sie derzeit keine weiteren Personalisierungsänderungen an der Seite vornehmen.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Hierfür gibt es zwei Gründe:

1. Sie haben die Seite zuvor personalisiert, aber dies erfolgte mithilfe einer früheren Version des Produkts. Wir haben die Art für die Personalisierung geändert seit Sie das letzte Mal die Seite personalisiert haben. Leider arbeiten die alte Art und die neue Art nicht zusammen.

2. Bis jetzt haben Sie nur den veralteten Bogen [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] verwendet, um die Seite zu personalisieren.

### <a name="unlocking-the-page"></a>Entsperren der Seite

Wenn Sie eine Seite entsperren und weiter personalisieren möchten, wählen Sie das Symbol ![Personalisieren Sperre](media/personalization-lock-icon.png "Personalisieren sperren") und dann die Aktion **Entsperren**.  

> [!CAUTION]
> Die aktuelle Personalisierung der Seite wird gelöscht. Die Seite kehrt zum ursprünglichen Layout zurück, und Sie müssen neu beginnen.  

## <a name="blocked-from-personalizing"></a>Für Personalisierung blockiert

Wenn das Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") im Banner **Personalisierung** angezeigt wird, können Sie keine Personalisierung der Seite vornehmen.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Der Grund dafür ist, dass das Rollencenter oder die Rolle, die derzeit mit dem Benutzerkonto verknüpft ist, diese Seite speziell für Ihre Rolle ändert. Wenden Sie sich an Ihren Administrator, um Unterstützung zu erhalten. Versuchen Sie alternativ, zu einem Rollencenter zu wechseln, das die Rollenanpassung für diese Seite enthält. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).

## <a name="see-also"></a>Siehe auch

[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
