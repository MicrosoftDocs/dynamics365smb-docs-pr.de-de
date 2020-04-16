---
title: Einrichten aus vorgeschlagenen Feldwerten| Microsoft Docs
description: Um manuell Berechnungen und vollständige Aufgaben schnell und genau zu erledigen, können Sie automatische Dateneingabe einrichten, sodass Business Central gerade ausgewählte Felder ausfüllt
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4e40f53543b094233c896e627ecfe6eb056e3d20
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195468"
---
# <a name="letting-d365fin-suggest-values"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] Werte vorschlagen lassen
[!INCLUDE[d365fin](includes/d365fin_md.md)] kann Ihnen dabei helfen, Aufgaben schneller und korrekter zu erledigen, indem es Felder oder Zeilen mit Daten ergänzt, die Sie sonst berechnen und manuell eingeben müssten. Obwohl solche automatische Dateneingaben immer korrekt sind, können Sie diese später ändern, wenn Sie dies wünschen.

Funktionen, die Feldwerte für Sie eingeben, werden in der Regel für Aufgaben angeboten, in denen Sie große Volumen von Transaktionsdaten eingeben müssen und Fehler vermeiden und Zeit sparen möchten. Dieses Thema enthält eine Auswahl solcher Funktionen. Weitere Abschnitte werden in zukünftigen Aktualisierungen des [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt.

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Das Kontrollkästchen **Ausgleichsbetrag vorschlagen** auf der Seite **Fibu Buch.-Blattnamen**
Wenn Sie beispielsweise von Fibu Buch.-Blattzeilen mehrere Ausgaben eingeben, die alle in demselben Bankkonto gebucht werden müssen, dann wird jedes Mal, wenn Sie eine neue Buch.-Blattzeile für Ausgaben eingeben, das Feld **Betrag** auf der Bankkontoenzeile automatisch mit dem Betrag aktualisiert, mit dem die Ausgabe ausgeglichen ist. Weitere Informationen zum Arbeiten mit Fibu Buch.-Blättern, finden Sie unter [Arbeiten mit Fibu Buch.-Blätter](ui-work-general-journals.md)

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Um das Feld **Betrag** auf Fibu Buch.-Blattzeilen automatisch zu aktualisieren.
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie in der Zeile für Ihren bevorzugten Fibu Buch.-Blattnamen das Kontrollkästchen **Ausgleichbetrag vorschlagen**.
3. Öffnen Sie das Fibu Buch.-Blatt, um Transaktionen unter Verwendung der beschriebenen Funktionen zum automatischen Buchen eines Feldwerts zu erfassen und zu buchen.       

Weitere Informationen darüber, wie ein persönliches Buch.-Blatt zum Beispiel für die Ausgabenbehandlung eingerichtet wird, finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Das Feld **Automatisch empfangene Daten einsetzen** auf der Seite **Zahlungs-Registrierung**
Die Seite **Zahlungs-Registrierung** zeigt ausstehende eingehende Zahlungen als Zeilen an, welche gebuchte Verkaufsbelege darstellen, in denen ein Betrag zur Zahlung fällig ist. Weitere Informationen zum Ausgleichen von Debitorenzahlungen finden Sie unter [Manuelles Abstimmen von Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Ihre Hauptaktionen auf der Seite ist es das Kontrollkästchen **Getätigte Zahlungen** und das Feld **Eingangsdatum** auszufüllen. Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] so aufsetzen, dass das Arbeitsdatum automatisch im Feld **Eingangsdatum** ausgefüllt wird, wenn Sie das Kontrollkästchen **Zahlung** getätigt anklicken.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Um das Feld **Eingangsdatum** auf der Seite **Zahlungs-Registrierung** automatisch auszufüllen
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Zahlungsregistrierung einrichten** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Kontrollkästchen **Eingangsdatum automatisch ausfüllen** aus.
3. Öffnen Sie die Seite **Zahlungs-Registrierung** und fahren Sie fort, um eingehende Debitorenzahlungen anhand der beschriebenen Funktionen zum automatischen Posten eines Feldwerts zu verarbeiten.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finanzen](finance.md)
