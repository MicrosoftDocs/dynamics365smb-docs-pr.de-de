---
title: Einrichten aus vorgeschlagenen Feldwerten| Microsoft Docs
description: "Um manuell Berechnungen und vollständige Aufgaben schnell und genau zu erledigen, können Sie automatische Dateneingabe einrichten, sodass Financials gerade ausgewählte Felder ausfüllen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3ca73c8298101eb02aac397894f87f7a5f58a5c2
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="letting-included365finincludesd365finmdmd-suggest-values"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] Werte vorschlagen lassen
[!INCLUDE[d365fin](includes/d365fin_md.md)] kann Ihnen dabei helfen, Aufgaben schneller und korrekter zu erledigen, indem es Felder oder Zeilen mit Daten ergänzt, die Sie sonst berechnen und manuell eingeben müssten. Obwohl solche automatische Dateneingaben immer korrekt sind, können Sie diese später ändern, wenn Sie dies wünschen.

Funktionen, die Feldwerte für Sie eingeben, werden in der Regel für Aufgaben angeboten, in denen Sie große Volumen von Transaktionsdaten eingeben müssen und Fehler vermeiden und Zeit sparen möchten. Dieses Thema enthält eine Auswahl solcher Funktionen. Weitere Abschnitte werden in zukünftigen Aktualisierungen des [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzugefügt.

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Das Kontrollkästchen **Ausgleichsbetrag vorschlagen** im **Fibu Buch.-Blattnamen** Fenster
Wenn Sie beispielsweise von Fibu Buch.-Blattzeilen mehrere Ausgaben eingeben, die alle in demselben Bankkonto gebucht werden müssen, dann wird jedes Mal, wenn Sie eine neue Buch.-Blattzeile für Ausgaben eingeben, das Feld **Betrag** auf der Bankkontoenzeile automatisch mit dem Betrag aktualisiert, mit dem die Ausgabe ausgeglichen ist. Weitere Informationen zum Arbeiten mit Fibu Buch.-Blättern, finden Sie unter [Arbeiten mit Fibu Buch.-Blätter](ui-work-general-journals.md)

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Um das Feld **Betrag** auf Fibu Buch.-Blattzeilen automatisch zu aktualisieren.
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie in der Zeile für Ihren bevorzugten Fibu Buch.-Blattnamen das Kontrollkästchen **Ausgleichbetrag vorschlagen**.
3. Öffnen Sie das Fibu Buch.-Blatt, um Transaktionen unter Verwendung der beschriebenen Funktionen zum automatischen Buchen eines Feldwerts zu erfassen und zu buchen.       

Weitere Informationen darüber, wie ein persönliches Buch.-Blatt zum Beispiel für die Ausgabenbehandlung eingerichtet wird, finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Das Feld **Automatisch empfangene Daten einsetzen** im Fenster **Zahlungs-Registrierung**
Das Fenster **Zahlungs-Registrierung** zeigt ausstehende eingehende Zahlungen als Zeilen an, welche gebuchte Verkaufsbelege darstellen, in denen ein Betrag zur Zahlung fällig ist. Weitere Informationen finden Sie unter [Vorgehensweise: Manuelles Abstimmen von Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

Ihre Hauptaktionen im Fenster ist es das Kontrollkästchen **Getätigte Zahlungen** und das Feld **Eingangsdatum** auszufüllen. Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] so aufsetzen, dass das Arbeitsdatum automatisch im Feld **Eingangsdatum** ausgefüllt wird, wenn Sie das Kontrollkästchen **Zahlung** getätigt anklicken.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Um das Feld **Eingangsdatum** im Fenster **Zahlungs-Registrierung** automatisch auszufüllen
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Einrichtung der Zahlungserfassung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie das Kontrollkästchen **Eingangsdatum automatisch ausfüllen** aus.
3. Öffnen Sie das Fenster **Zahlungs-Registrierung** und fahren Sie fort, um eingehende Debitorenzahlungen anhand der beschriebenen Funktionen zum automatischen Posten eines Feldwerts zu verarbeiten.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finanzen](finance.md)

