---
title: 'Gewusst wie: Einnahmen und Ausgaben abgrenzen| Microsoft Docs'
description: "Beschreibt, wie Einnahmen und Ausgaben in Perioden außerhalb der Periode, in der die Transaktion gebucht wird, abgegrenzt werden können, indem Einnahmen und Ausgaben über einen bestimmten Zeitplan automatisch zurückgestellt werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 03/24/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5d7dbdc6001f221df0659d5aca1e5939398e3a31
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-defer-revenues-and-expenses"></a>Gewusst wie: Einnahmen und Ausgaben zurückstellen
Um Einnahmen und Ausgaben in einer anderen Periode als in jener, in der die Transaktion gebucht wurde, zu erkennen, können Sie die Funktionen verwenden, um Einnahmen und Ausgaben über einen bestimmten Zeitplan automatisch zurückzustellen.

Um Einnahmen oder Ausgaben in den betroffenen Buchhaltungsperioden einzubeziehen, können Sie eine Abgrenzungsvorlage für die Ressource, den Artikel oder ein Sachkonto anlegen, für das die Einnahmen oder Ausgaben gebucht werden. Wenn Sie den zugehörigen Kauf- oder Verkaufsbeleg buchen, werden die Einnahmen oder Ausgaben zu den entsprechenden Buchhaltungsperioden zurückgestellt, entsprechend einem Aufschubzeitplan, der durch Einstellungen in der Aufschubvorlage und das Buchungsdatum bestimmt wird.

**Hinweis: ** Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter] [Benutzeroberfläche [!INCLUDE[d365fin](includes/d365fin_md.md)] (ui-experiences.md) anpassen.

## <a name="to-set-up-a-gl-account-for-deferral"></a>So richten Sie ein Sachkonto für Abgrenzungen ein
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen **aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder wie notwendig aus, um ein Sachkonto für abgegrenzte Einnahmen zu erstellen. Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md).
4. Wiederholen Sie die Schritte 2 und 3, um ein neues Sachkonto für abgegrenzte Ausgaben zu erstellen.

Für beide Arten Aufschub, wählen Sie im Feld **Art** **Bilanz** aus und benennen Sie die Konten entsprechend, wie "Nicht verdiente Erträge" für zurückgestellte Einnahmen und "nicht bezahlte Ausgaben" für abgegrenzte Ausgaben.

## <a name="to-set-up-a-deferral-template"></a>So richten Sie eine Aufschubvorlage ein
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen **aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Abgrenzungsvorlage** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Geben Sie Feld **Berechnungsmethode** an, wie das Feld **Betrag** für jede Periode im Fenster **Abrechnungsplan** berechnet wird. Sie haben die Wahl zwischen den folgenden Optionen:

   * **Linear**: Die regelmäßigen Abgrenzungsbeträge werden entsprechend der Anzahl der Perioden berechnet, verteilt entsprechend der Periodenlänge.
   * **Gleich pro Periode**: Die regelmäßigen Abgrenzungsbeträge werden entsprechend der Anzahl der Perioden berechnet, gleichmäßig nach Perioden verteilt.
   * **Tage pro Periode**: Die regelmäßigen Abgrenzungsbeträge werden entsprechend der Anzahl der Tage in der Periode berechnet.
   * **Benutzerdefiniert**: Die regelmäßig Abgrenzungsbeträge werden nicht berechnet. Sie müssen das Feld **Betrag** für jede Periode im Abgrenzungsplanfenster manuell ausfüllen. Weitere Informationen finden Sie im Abschnitt „So ändern Sie einen Aufschubzeitplan aus einer Verkaufsrechnung”.
5. In der **Periodenbeschr.** Feld geben Sie eine Beschreibung an, die bei Einträgen für die Abgrenzungsbuchung angezeigt wird. Sie können die folgenden Platzhaltercodes für typische Werte eingeben, die automatisch eingefügt werden, wenn die Periodenbeschreibung angezeigt wird.

   * %1 = Die Tagesnummer des Periodenbuchungsdatums
   * %2 = Die Wochennummer des Periodenbuchungsdatums
   * %3 = Die Monatsnummer des Periodenbuchungsdatums
   * %4 = Der Monatsname des Periodenbuchungsdatums
   * %5 = Der Buchhaltungsperiodenname des Periodenbuchungsdatums
   * %6 = Das Geschäftsjahr des Periodenbuchungsdatums

Beispiel: Das Buchungsdatum ist 02.06.2016. Wenn Sie "Abgrenzungsausgabe für %4 %6" eingeben, ist die angezeigte Beschreibung "Abgrenzungsausgaben für Februar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>So weisen Sie einem Artikel eine Aufschubvorlage zu
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen **aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Abgrenzungsvorlage** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie die Karte für den Artikel, für den Ausgaben oder Einnahmen zu den Buchungsperioden abgegrenzt werden müssen, wenn der Artikel gekauft oder verkauft wurde.
3. Im Feld **Standard-Abgrenzungsvorlage** wählen Sie die entsprechende Abgrenzungsvorlage aus.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>So ändern Sie einen Aufschubzeitplan von einer Verkaufsrechnung aus
**Notiz**: Die Schritte in diesem Ablauf sind identisch, wie wenn Sie einen Abgrenzungsplan für Ausgaben aus einer Kaufrechnung ändern.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus **![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "")Symbol nach Seite oder Bericht suchen. Geben Sie **Verkaufsechnung** ein und wählen Sie dann den entsprechenden Link aus.
2. Erstellen Sie eine Verkaufsrechnung für einen Artikel, der einer Abgrenzungsvorlage zugewiesen ist. Weitere Informationen finden Sie unter [Gewusst wie: Rechnungsverkäufe](sales-how-invoice-sales.md).

    Beachten Sie Folgendes: Sobald Sie den Artikel (oder Ressource oder Sachkonto) in der Rechnungszeile eingeben, wird das Feld **Abgrenzungscode** mit dem Code der zugewiesenen Abgrenzungsvorlage ausgefüllt.
3. Wählen Sie die Aktion **Abgrenzungsplan** aus.
4. Ändern Sie im Fenster **Aufschubzeitplan** die Einstellungen im Kopf oder die Werte in den Zeilen, zum Beispiel, um den Betrag bis zu einer zusätzlichen Buchhaltungsperiode zurückzustellen.
5. Wählen Sie die Aktion **Berechnungsplan** aus.
6. Wählen Sie die Schaltfläche **OK** aus. Der Aufschubzeitplan wird für die Verkaufsrechnung aktualisiert. Die zugehörige Aufschubvorlage ist unverändert.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Um anzuzeigen, wie die Abgrenzungsausgaben oder -einnahmen im Sachkonto gebucht werden
**Notiz**: Die Schritte in diesem Ablauf sind die selben, wie Sie in der Vorschau sehen, wie Abgrenzungsausgaben gebucht werden.

1. Im Fenster **Gebuchte Verkaufsrechnung** wählen Sie die Aktion **Buchung ansehen** aus.
2. Wählen Sie im Fenster **Buchungsvorschau** die Option **Sachkonteneintrag** aus und wählen Sie dann **Zugehörige Einträge anzeigen** aus.

Sachkonteneinträge, die im entsprechenden Abgrenzungskonto gebucht werden müssen, wie beispielsweise "Nicht verdiente Erträge" werden durch die Beschreibung bezeichnet, die Sie unter **Perioden Beschr.** eingegeben haben. Feld in der Abgrenzungsvorlage beispielsweise "Ausgaben abgegrenzt für Februar 2016".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>So überprüfen Sie gebuchte Aufschübe im Bericht „Verkaufsaufschubzusammenfassung” .
**Notiz**: Die Schritte in diesem Ablauf sind die selben, wie Sie sie sehen, wenn Sie die Zusammenfassung des Einkaufsabgrenzungsberichts ansehen.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus! ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Gebuchte Verkaufsabgrenzungszusammenfassung** eingeben und den entsprechenden Link auswählen.„”
2. Geben Sie im Fenster **Verkaufsaufschubzusammenfassung** im Feld **Saldo ab** das Datum ein, bis zu welchem Sie zurückgestellte Einnahmen anzeigen möchten.
3. Klicken Sie auf die Schaltfläche **Vorschau**.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Vorgehensweise: Arbeit mit Fibu-Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

