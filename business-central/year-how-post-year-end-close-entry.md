---
title: 'Vorgehensweise: Buchen und überprüfen des Jahresabschlusspostens | Microsoft Docs'
description: Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung "GuV-Konten Nullstellung" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191734"
---
# <a name="post-the-year-end-closing-entry"></a>So buchen Sie den Jahresabschlussposten
Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.

## <a name="to-post-the-year-end-closing-entry"></a>So buchen Sie den Jahresabschlussposten
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Fibu Buch.Blatt** im Feld **Buch.-Blattname** das Buch.-Blatt mit den Abschlussposten aus.
3. Überprüfen Sie die Posten.
4. Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.

> [!NOTE]  
>   Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt. Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt. Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.

## <a name="see-also"></a>Siehe auch
[Schließen von Buchhaltungsperioden](year-close-account-periods.md)  
[Schließen der Bücher](year-close-books.md)  
[GuV-Konten Nullstellung](year-close-income-statement.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
