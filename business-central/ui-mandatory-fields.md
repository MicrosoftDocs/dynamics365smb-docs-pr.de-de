---
title: Pflichtfeld, um Arbeitsgänge abzuschließen | Microsoft Docs
description: Erhalten von Informationen zu den Feldern, die mit einem roten Sternchen gekennzeichnet werden, das angibt, dass sie benötigt werden und ausgefüllt werden müssen, um Arbeitsgänge benötigt.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: f525077069107e1365728aaaaf1e4791a250c6ee
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760367"
---
# <a name="detecting-mandatory-fields"></a>Pflichtfelder erkennen
Wenn Sie Daten auf Seiten in  [!INCLUDE[prod_short](includes/prod_short.md)] eingeben, werden bestimmte Felder mit einem roten Sternchen markiert. Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Prozess, der das Feld verwendet, abzuschließen (Beispiel: Buchung einer Transaktion, die den Wert in dem Feld verwendet).

Selbst wenn das Feld ein rotes Sternchen enthält, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schließen. Das rote Sternchen dient nur als Erinnerung, dass Sie am Beenden eines bestimmten Prozesses gehindert werden.

## <a name="examples"></a>Beispiele
Auf der Seite **Debitorenkarte** wird im Feld **Name** und in den drei **Buchungsgruppengebieten** das rote Sternchen angezeigt, um anzugeben, dass Sie eine Verkaufstransaktion für den Debitor nur dann buchen können, wenn diese ausgefüllt werden.

Auf der Seite **Artikelkarte** wird das rote Sternchen auf **Beschreibung** und den Basiseinheitencode Feldern angezeigt, um anzugeben, dass Sie den Artikel in einer Belegzeile (beispielsweise in einem Verkaufsauftrag) nur dann eingeben können, wenn auch diese Felder ausgefüllt werden.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
