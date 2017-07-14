---
title: "Vorgehensweise: Ändern oder Löschen einer unbezahlten Einkaufsrechnung| Microsoft Docs"
description: "Vorgehensweise: Ändern oder Löschen einer unbezahlten Einkaufsrechnung"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fba080da79d3a9d3f816c8ddc0a02c877211bcb4
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Vorgehensweise: Ändern oder Löschen einer unbezahlten Einkaufsrechnung
<a id="how-to-correct-or-cancel-unpaid-purchase-invoices" class="xliff"></a>
Sie können eine bezahlte Einkaufsrechnung korrigieren oder abbrechen. Dies ist nützlich, wenn Sie einen Tippfehler korrigieren möchten, oder wenn Sie den Kauf früh im Bestellvorgang ändern möchten.

Wenn Sie bereits für Produkte auf der gebuchten Einkaufsrechnung bezahlt haben, können Sie diese aus der gebuchten Einkaufsrechnung selbst nicht korrigieren oder stornieren. Stattdessen müssen Sie eine Einkaufsgutschrift manuell erstellen, um den Einkauf zu stornieren. Weitere Informationen finden Sie unter [Vorgehensweise: Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

Im Fenster **Geb. Einkaufsrechnung** können Sie die Schaltfläche **Korrigieren** oder **Stornieren** wählen. Wenn Sie eine gebuchte Einkaufsrechnung korrigieren oder stornieren, wird sie in allen Sach- und Inventurposten angewendet, die erstellt wurden, als die erste Einkaufsrechnung gebucht wurde. Dadurch wird die gebuchte Einkaufsrechnung in Ihren Finanzdatensätzen storniert und verlässt die gebuchte Korrektureinkaufsgutschrift für Ihr Protokoll. Nachfolgend wird die Verwendung von **Korrigieren** und **Stornieren** beschrieben.

## Gebuchte Einkaufsrechnung korrigieren
<a id="to-correct-a-posted-purchase-invoice" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Rechnungen** eingeben und den entsprechenden Link auswählen.  
2. Wählen Sie die gebuchte Einkaufsrechnung, die Sie korrigieren möchten.  

    **Hinweis**: Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Im Fenster **Gebuchte Einkaufsrechnung** wählen Sie **Korrekt** aus.

    Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt, auf dem Sie die Korrektur machen können. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md). Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.

    Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung storniert.

## Gebuchte Einkaufsrechnung stornieren
<a id="to-cancel-a-posted-purchase-invoice" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Rechnungen** eingeben und den entsprechenden Link auswählen.  
2. Wählen Sie die gebuchte Einkaufsrechnung, die Sie stornieren möchten.

    **Hinweis**: Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Einkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Im Fenster **Gebuchte Einkaufsrechnung** wählen Sie **Stornieren** aus.

    Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. Das Feld **Storniert** am Anfang gebuchten Einkaufsrechnung wird auf **Ja** geändert.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Einkaufsgutschrift anzuzeigen, die die gebuchte Einkaufsrechnung storniert.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Einkauf](purchasing-manage-purchasing.md)  
[Vorgehensweise: Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

