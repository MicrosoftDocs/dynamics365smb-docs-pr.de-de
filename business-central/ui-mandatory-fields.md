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
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: bc3cedf31aadb69e380b704f4019a86eb7864882
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935328"
---
# <a name="detecting-mandatory-fields"></a>Pflichtfelder erkennen
Wenn Sie Daten auf Seiten in  [!INCLUDE[d365fin](includes/d365fin_md.md)] eingeben, werden bestimmte Felder mit einem roten Sternchen markiert. Das rote Sternchen bedeutet, dass das Feld ausgefüllt werden muss, um einen bestimmten Prozess, der das Feld verwendet, abzuschließen (Beispiel: Buchung einer Transaktion, die den Wert in dem Feld verwendet).

Selbst wenn das Feld ein rotes Sternchen enthält, sind Sie nicht gezwungen, das Feld auszufüllen, bevor Sie mit anderen Feldern fortfahren oder die Seite schließen. Das rote Sternchen dient nur als Erinnerung, dass Sie am Beenden eines bestimmten Prozesses gehindert werden.

## <a name="examples"></a>Beispiele
Auf der Seite **Debitorenkarte** wird im Feld **Name** und in den drei **Buchungsgruppengebieten** das rote Sternchen angezeigt, um anzugeben, dass Sie eine Verkaufstransaktion für den Debitor nur dann buchen können, wenn diese ausgefüllt werden.

Auf der Seite **Artikelkarte** wird das rote Sternchen auf **Beschreibung** und den Basiseinheitencode Feldern angezeigt, um anzugeben, dass Sie den Artikel in einer Belegzeile (beispielsweise in einem Verkaufsauftrag) nur dann eingeben können, wenn auch diese Felder ausgefüllt werden.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
