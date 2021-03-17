---
title: Warum ich eine Seite nicht personalisieren | Microsoft Docs
description: Erklärt, warum Sie eine Seite nicht personalisieren können und was Sie tun können, um sie zu entsperren, sodass Sie sie anpassen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 41b0989d388ee7ded2619136ded0a03d5830b78b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387549"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Warum eine Seite für Personalisierungen gesperrt ist

Es gibt zwei Bedingungen, die Sie am Personalisieren einer Seite hindern. Entweder ist die Seite gesperrt (wie durch das Symbol ![Personalisierungssperre](media/personalization-lock-icon.png "Personalisieren sperren") angezeigt) oder sie ist blockiert (wie durch das Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") angezeigt).

## <a name="locked-from-personalizing"></a>Für Personalisierung gesperrt

Wenn beim Öffnen einer Seite das Symbol ![Personalisierungssperre](media/personalization-lock-icon.png "Personalisieren sperren") im Banner **Personalisierung** zu sehen ist, bedeutet dies, dass Sie derzeit keine weiteren Personalisierungsänderungen an der Seite vornehmen können.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Hierfür gibt es zwei Gründe:

1. Sie haben die Seite zuvor personalisiert, aber dies erfolgte mithilfe einer früheren Version des Produkts. Wir haben die Art für die Personalisierung geändert seit Sie das letzte Mal die Seite personalisiert haben. Leider arbeiten die alte Art und die neue Art nicht zusammen.

2. Bis jetzt haben Sie nur [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] verwendet, um die Seite zu personalisieren.

### <a name="unlocking-the-page"></a>Entsperren der Seite

Wenn Sie eine Seite entsperren und weiter personalisieren möchten, wählen Sie das Symbol ![Personalisieren Sperre](media/personalization-lock-icon.png "Personalisieren sperren") und dann die Aktion **Entsperren**.  

Bevor Sie die Seite entsperren, beachten Sie Folgendes:

- Die aktuelle Personalisierung der Seite wird gelöscht. Die Seite kehrt zum ursprünglichen Layout zurück, und Sie müssen neu beginnen.

- In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] bleibt die Seite wie sie ist und wird von den Änderungen der neuen im Business Central-Central vorgenommenen Personalisierung nicht betroffen. Ab da sind die Personalisierungen in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] und im Business Central-Client völlig voneinander getrennt.

## <a name="blocked-from-personalizing"></a>Für Personalisierung blockiert

Wenn das Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") im Banner **Personalisierung** erscheint, bedeutet dies, dass Sie an der Personalisierung der Seite gehindert werden.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

Der Grund dafür ist, dass das Rollencenter oder die Rolle, die derzeit mit dem Benutzerkonto verknüpft ist, diese Seite speziell für Ihre Rolle ändert. Wenden Sie sich an Ihren Administrator, um Unterstützung zu erhalten. Versuchen Sie alternativ, zu einem Rollencenter zu wechseln, das die Rollenanpassung für diese Seite enthält. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).

## <a name="see-also"></a>Siehe auch
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]