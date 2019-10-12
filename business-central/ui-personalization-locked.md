---
title: Warum ich eine Seite nicht personalisieren | Microsoft Docs
description: Erklärt, warum Sie eine Seite nicht personalisieren können und was Sie tun können, um sie zu entsperren, sodass Sie sie anpassen können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c77664a1013804de13303c8e1d162c437cf5d6e7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315132"
---
# <a name="why-a-page-is-locked-from-personalization"></a>Warum eine Seite für Personalisierungen gesperrt ist

Es gibt zwei Bedingungen, die Sie am Personalisieren einer Seite hindern. Entweder ist die Seite gesperrt (wie von ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") angegeben), oder sie ist blockiert (wie von ![Personalisieren blockiert](media/personalization-blocked-icon.png "Personalisieren blockiert")) angegeben.

## <a name="locked-from-personalizing"></a>Für Personalisierung gesperrt

Wenn ein Symbol ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") im Banner **Personalisieren** angezeigt wird, wenn Sie eine Seite öffnen (wie angezeigt) bedeutet dies, dass Sie zurzeit keine Personalisierungsänderungen an der Seite vornehmen können.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Hierfür gibt es zwei Gründe:

1. Sie haben die Seite zuvor personalisiert, aber dies erfolgte mithilfe einer früheren Version des Produkts. Wir haben die Art für die Personalisierung geändert seit Sie das letzte Mal die Seite personalisiert haben. Leider arbeiten die alte Art und die neue Art nicht zusammen.

2. Bis jetzt haben Sie nur [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] verwendet, um die Seite zu personalisieren.

### <a name="unlocking-the-page"></a>Entsperren der Seite

Wenn Sie eine Seite entsperren und dann weiter Personalisieren möchten, wählen Sie ![Personalisieren sperren](media/personalization-lock-icon.png "Personalisieren sperren") und dann **Sperre aufheben** aus.  

Bevor Sie die Seite entsperren, beachten Sie Folgendes:

- Die aktuelle Personalisierung der Seite wird gelöscht. Die Seite kehrt zum ursprünglichen Layout zurück, und Sie müssen neu beginnen.

- In [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] bleibt die Seite wie sie ist und wird von den Änderungen der neuen im Business Central-Central vorgenommenen Personalisierung nicht betroffen. Ab da sind die Personalisierungen in [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] und im Business Central-Client völlig voneinander getrennt.

## <a name="blocked-from-personalizing"></a>Für Personalisierung blockiert

Ein Symbol ![Personalisierung blockiert](media/personalization-blocked-icon.png "Personalisierung blockiert") im Personalisierungsbanner bedeutet, dass jegliche **Personalisierung** der Seite blockiert ist.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

Der Grund dafür ist, dass das Rollencenter oder die Rolle, die derzeit mit dem Benutzerkonto verknüpft ist, diese Seite speziell für Ihre Rolle ändert. Wenden Sie sich an Ihren Administrator, um Unterstützung zu erhalten. Versuchen Sie alternativ, zu einem Rollencenter zu wechseln, das die Rollenanpassung für diese Seite enthält. Weitere Informationen finden Sie unter [Ändern der Grundeinstellungen](ui-change-basic-settings.md).

## <a name="see-also"></a>Siehe auch
[Ihren Arbeitsbereich personalisieren](ui-personalization-user.md)  
[Seiten für Profile anpassen](ui-personalization-manage.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Funktionen, die angezeigt werden ändern](ui-experiences.md)  
