---
title: Weisen Sie einem Kreditor eine Prioritätsstufe zu| Microsoft Docs
description: Sie können sowohl Zahlen Ihren Kreditoren oder Lieferanten zuweisen, um sie zu priorisieren und Zahlungsvorschläge in  Business Central zu erleichtern.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 177fb324e39a59abbfc1b50e6ceaa34d4ae06f56
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926897"
---
# <a name="prioritize-vendors"></a>Kreditoren priorisieren
[!INCLUDE[d365fin](includes/d365fin_md.md)] kann verschiedene Zahlungen an Kreditoren vorschlagen. Dies können z. B. Zahlungen sein, die in Kürze fällig sind, oder Zahlungen, bei denen Sie einen Rabatt erhalten können. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).

Zuerst müssen Sie den Kreditoren priorisieren, indem Sie ihm Nummern zuweisen.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>So priorisieren Sie Kreditoren
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Anbieter** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die entsprechende Kreditor, und klicken Sie dann auf **Bearbeiten** .
3. Geben Sie im Feld **Priorität** eine Zahl ein.

[!INCLUDE[d365fin](includes/d365fin_md.md)] geht davon aus, dass die niedrigsten Nummern (außer 0) die höchste Priorität haben. Wenn Sie also z. B. 1, 2 und 3 verwenden, erhält 1 die höchste Priorität.

Falls Sie einem Kreditor keine Priorität zuweisen wollen, lassen Sie das Feld **Priorität** leer. Wenn Sie dann die Funktion "Zahlungsvorschlag" verwenden, wird dieser Kreditor nach den Kreditoren aufgeführt, die eine Priorität haben. Sie können so viele Prioritäten einrichten wie Sie benötigen.

## <a name="see-also"></a>Siehe auch
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
