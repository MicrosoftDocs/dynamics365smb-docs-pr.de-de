---
title: "Vorgehensweise: Ändern oder Löschen einer unbezahlten Verkaufsrechnung| Microsoft Docs"
description: "Vorgehensweise: Ändern oder Löschen einer unbezahlten Verkaufsrechnung"
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
ms.openlocfilehash: 9289aeb9b44ec300646fbe6e6fdbf77e72cd7b08
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a>Vorgehensweise: Ändern oder Löschen einer unbezahlten Verkaufsrechnung
Sie können eine bezahlte Verkaufsrechnung korrigieren oder abbrechen. Dies ist nützlich, wenn Ihnen ein Fehler unterläuft, oder wenn der Debitor eine Änderung anfordert.

**Hinweis**: Nachdem eine gebuchte Verkaufsrechnung teilweise oder vollständig gezahlt wurde, können Sie die Nummer aus der gebuchten Verkaufsrechnung selbst nicht korrigieren oder stornieren. Stattdessen müssen Sie eine Verkaufsgutschrift manuell erstellen, um den Verkauf zu stornieren und den Debitor zurückzuerstatten. Weitere Informationen finden Sie unter [Vorgehensweise: Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).

Im Fenster **Geb. Verkaufsrechnung** können Sie auf die Schaltfläche **Korrigieren** oder auf die Schaltfläche **Abbrechen** klicken, um die Aktionen auszuführen, die in der folgenden Tabelle beschrieben werden.

| Aktion | Beschreibung |
| --- | --- |
| **Korrigiereh** |Die gebuchte Verkaufsrechnung ist storniert. Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt. Sie können die Korrektur machen, bevor Sie den Verkaufsprozess fortsetzen. Die neue Verkaufsrechnung hat eine andere Nummer als die erste Verkaufsrechnung. Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. In der ursprünglich gebuchten Verkaufsrechnung werden die Kontrollkästchen "Storniert" und "Bezahlt" aktiviert. |
| **Abbrechen** |Die gebuchte Verkaufsrechnung ist storniert. Eine Korrekturverkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. In der ursprünglich gebuchten Verkaufsrechnung werden die Kontrollkästchen "Storniert" und "Bezahlt" aktiviert. |

Wenn Sie eine gebuchte Verkaufsrechnung korrigieren oder stornieren, wird sie in allen Sach- und Inventurposten angewendet, die erstellt wurden, als die erste Verkaufsrechnung gebucht wurde. Dadurch wird die gebuchte Verkaufsrechnung in Ihren Finanzdatensätzen storniert und verlässt die gebuchte Korrekturverkaufsgutschrift für Ihr Protokoll.

## <a name="to-correct-a-posted-sales-invoice"></a>Gebuchte Verkaufsrechnung korrigieren
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus! ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Verkaufsrechnungen** eingeben und den entsprechenden Link auswählen.„”  
2. Wählen Sie die gebuchte Verkaufsrechnung, die Sie korrigieren möchten.

    **Hinweis**: Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Verkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Im Fenster **Gebuchte Verkaufsrechnung** wählen Sie **Korrekt** aus.  
4. Eine neue Verkaufsrechnung mit den gleichen Informationen wird erstellt, auf dem Sie die Korrektur machen können. Das Feld **Storniert** am Anfang gebuchten Verkaufsrechnung wird auf **Ja** geändert.

    Eine Verkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren.
5. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Verkaufsgutschrift anzuzeigen, die die gebuchte Verkaufsrechnung storniert.

## <a name="to-cancel-a-posted-sales-invoice"></a>Gebuchte Verkaufsrechnung stornieren
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus! ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Verkaufsrechnungen** eingeben und den entsprechenden Link auswählen.„”  
2. Wählen Sie die gebuchte Verkaufsrechnung, die Sie stornieren möchten.

    **Hinweis**: Wenn Sie das Kontrollkästchen **Storniert** auswählen, dann können Sie die gebuchte Verkaufsrechnung nicht korrigieren, da sie bereits korrigiert wurde oder storniert wurde.
3. Im Fenster **Gebuchte Verkaufsrechnung** wählen Sie **Stornieren** aus.

    Eine Verkaufsgutschrift wird automatisch erstellt und gebucht, um die ursprüngliche gebuchte Verkaufsrechnung zu stornieren. Das Feld **Storniert** am Anfang gebuchten Verkaufsrechnung wird auf **Ja** geändert.
4. Wählen Sie die Registerkarte **Korrekturgutschrift anzeigen** aus, um die gebuchte Verkaufsgutschrift anzuzeigen, die die gebuchte Verkaufsrechnung storniert.

## <a name="see-also"></a>Siehe auch
[Verkauf](sales-manage-sales.md)  
[Einrichten von Verkäufen](sales-setup-sales.md)  
[Gewusst wie: Senden von Belegen über E-Mail](ui-how-send-documents-email.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

