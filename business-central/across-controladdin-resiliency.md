---
title: Ausfallsicherheit von Add-Ins in Business Central steuern
description: 'Was zu tun ist, wenn Steuerelement-Add-Ins oder benutzerdefinierte Steuerelemente zu eingeschränkter Funktionalität in Business Central führen.'
ms.topic: conceptual
author: brentholtorf
ms.author: bholtorf
ms.date: 12/12/2023
ms.service: dynamics-365-business-central
---

# <a name="control-add-in-resiliency-in-business-central"></a>Ausfallsicherheit von Add-Ins in Business Central steuern

Ab Update 20.0 von [!INCLUDE[prod_short](includes/prod_short.md)], werden langsam ausgeführte Steuerelement-Add-Ins automatisch erkannt und ein Dialogfeld ähnlich dem folgenden wird angezeigt.

![Beschäftigt – Steuerungs-Add-In](media/controladdin-resiliency.png "Beschäftigt – Steuerungs-Add-In")

Ein fehlerhaftes Steuerelement-Add-In kann Ihre Erfahrung mit Business Central beeinträchtigen und dazu führen, dass die Seite, an der Sie arbeiten, langsam startet. Es hat keine Auswirkungen auf die Daten und Ihre Änderungen werden immer gespeichert. Wenn die Warnung wie oben dargestellt angezeigt wird, können Sie sie ausblenden. Sie kann jedoch erneut auftreten, und wenn das Problem weiterhin besteht, sollten Sie sich an Ihren Administrator wenden.

## <a name="see-also"></a>Siehe auch
[Best Practices zur Steuerung der Add-In-Leistung](/dynamics365/business-central/dev-itpro/developer/devenv-control-addin-bestpractices)  
