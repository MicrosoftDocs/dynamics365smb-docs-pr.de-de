---
title: Einnahmen und Ausgaben abgrenzen| Microsoft Docs
description: "Um Einnahmen und Ausgaben in Perioden außer der Periode zu erkennen, in der die Transaktion gebucht wird, können Sie Funktionen verwenden, um Einnahmen und Ausgaben über einen bestimmten Zeitplan automatisch zurückzustellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9a21f4e54dc5afd8144d0990a9f9bcc30401a82c
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="defer-revenues-and-expenses"></a>Einnahmen und Ausgaben abgrenzen
Um Einnahmen und Ausgaben in einer anderen Periode als in jener, in der die Transaktion gebucht wurde, zu erkennen, können Sie die Funktionen verwenden, um Einnahmen und Ausgaben über einen bestimmten Zeitplan automatisch zurückzustellen.

Um Einnahmen oder Ausgaben in den betroffenen Buchhaltungsperioden einzubeziehen, können Sie eine Abgrenzungsvorlage für die Ressource, den Artikel oder ein Sachkonto anlegen, für das die Einnahmen oder Ausgaben gebucht werden. Wenn Sie den zugehörigen Kauf- oder Verkaufsbeleg buchen, werden die Einnahmen oder Ausgaben zu den entsprechenden Buchhaltungsperioden zurückgestellt, entsprechend einem Abgrenzungsplan, der durch Einstellungen in der Abgrenzungsvorlage und das Buchungsdatum bestimmt wird.

## <a name="to-set-up-a-gl-account-for-deferral"></a>So richten Sie ein Sachkonto für Abgrenzungen ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder wie notwendig aus, um ein Sachkonto für abgegrenzte Einnahmen zu erstellen. Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md).
4. Wiederholen Sie die Schritte 2 und 3, um ein neues Sachkonto für abgegrenzte Ausgaben zu erstellen.

Für beide Arten von Abgrenzung wählen Sie im Feld **Art** **Bilanz** aus und benennen Sie die Konten entsprechend, wie "Nicht verdiente Erträge" für zurückgestellte Einnahmen und "nicht bezahlte Ausgaben" für abgegrenzte Ausgaben.

## <a name="to-set-up-a-deferral-template"></a>So richten Sie eine Abgrenzungsvorlage ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Abgrenzungsvorlagen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Geben Sie auf der Seite **Berechnungsmethode** an, wie das Feld **Betrag** für jede Periode auf der Seite **Abgrenzungsplan** berechnet wird. Sie haben die Wahl zwischen den folgenden Optionen:

   * **Linear**: Die regelmäßigen Abgrenzungsbeträge werden entsprechend der Anzahl der Perioden berechnet, verteilt entsprechend der Periodenlänge.
   * **Gleich pro Periode**: Die regelmäßigen Abgrenzungsbeträge werden entsprechend der Anzahl der Perioden berechnet, gleichmäßig nach Perioden verteilt.
   * **Tage pro Periode**: Die regelmäßigen Abgrenzungsbeträge werden entsprechend der Anzahl der Tage in der Periode berechnet.
   * **Benutzerdefiniert**: Die regelmäßig Abgrenzungsbeträge werden nicht berechnet. Sie müssen das Feld **Betrag** für jede Periode auf der Abgrenzungsplanseite manuell ausfüllen. Weitere Informationen finden Sie im Abschnitt „So ändern Sie einen Abgrenzungsplan aus einer Verkaufsrechnung”.
5. Im Feld **Periodenbeschr.** geben Sie eine Beschreibung an, die bei Einträgen für die Abgrenzungsbuchung angezeigt wird. Sie können die folgenden Platzhaltercodes für typische Werte eingeben, die automatisch eingefügt werden, wenn die Periodenbeschreibung angezeigt wird.

   * %1 = Die Tagesnummer des Periodenbuchungsdatums
   * %2 = Die Wochennummer des Periodenbuchungsdatums
   * %3 = Die Monatsnummer des Periodenbuchungsdatums
   * %4 = Der Monatsname des Periodenbuchungsdatums
   * %5 = Der Buchhaltungsperiodenname des Periodenbuchungsdatums
   * %6 = Das Geschäftsjahr des Periodenbuchungsdatums

Beispiel: Das Buchungsdatum ist 02.06.2016. Wenn Sie "Abgrenzungsausgabe für %4 %6" eingeben, ist die angezeigte Beschreibung "Abgrenzungsausgaben für Februar 2016".

## <a name="to-assign-a-deferral-template-to-an-item"></a>So weisen Sie einem Artikel eine Abgrenzungsvorlage zu
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Abgrenzungsvorlagen** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die Karte für den Artikel, für den Ausgaben oder Einnahmen zu den Buchungsperioden abgegrenzt werden müssen, wenn der Artikel gekauft oder verkauft wurde.
3. Im Feld **Standard-Abgrenzungsvorlage** wählen Sie die entsprechende Abgrenzungsvorlage aus.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice"></a>So ändern Sie einen Abgrenzungsplan von einer Verkaufsrechnung aus
> [!NOTE]  
>   Die Schritte in diesem Ablauf sind identisch, wie wenn Sie einen Abgrenzungsplan für Ausgaben aus einer Kaufrechnung ändern.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsrechnung** ein, und wählen dann den zugehörigen Link aus.
2. Erstellen Sie eine Verkaufsrechnung für einen Artikel, der einer Abgrenzungsvorlage zugewiesen ist. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).

    Beachten Sie Folgendes: Sobald Sie den Artikel (oder Ressource oder Sachkonto) in der Rechnungszeile eingeben, wird das Feld **Abgrenzungscode** mit dem Code der zugewiesenen Abgrenzungsvorlage ausgefüllt.
3. Wählen Sie die Aktion **Abgrenzungsplan** aus.
4. Ändern Sie auf der Seite **Abgrenzungsplan** die Einstellungen im Kopf oder die Werte in den Zeilen, zum Beispiel, um den Betrag bis zu einer zusätzlichen Buchhaltungsperiode zurückzustellen.
5. Wählen Sie die Aktion **Berechnungsplan** aus.
6. Wählen Sie die Schaltfläche **OK** aus. Der Abgrenzungsplan wird für die Verkaufsrechnung aktualisiert. Die zugehörige Abgrenzungsvorlage ist unverändert.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger"></a>Um anzuzeigen, wie die Abgrenzungsausgaben oder -einnahmen im Sachkonto gebucht werden
> [!NOTE]  
>   Die Schritte in diesem Ablauf sind die selben, wie Sie in der Vorschau sehen, wie Abgrenzungsausgaben gebucht werden.

1. Auf der Seite **Gebuchte Verkaufsrechnung** wählen Sie die Aktion **Buchung ansehen** aus.
2. Wählen Sie auf der Seite **Buchungsvorschau** die Option **Sachkonteneintrag** aus und wählen Sie dann **Zugehörige Einträge anzeigen** aus.

Zu einem bestimmten Abgrenzungskonto zu buchende Sachkonteneinträge, beispielsweise „Nicht verdiente Erträge”, werden von der Beschreibung bezeichnet, die Sie im Feld **Periodenbeschreibung** in der Abgrenzungsvorlage eingegeben haben, beispielsweise Einnahmeabgrenzungen für Februar 2016.

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report"></a>So überprüfen Sie gebuchte Abgrenzungen im Bericht „Verkaufsabgrenzungszusammenfassung” .
> [!NOTE]  
>   Die Schritte in diesem Ablauf sind die selben, wie Sie sie sehen, wenn Sie die Zusammenfassung des Einkaufsabgrenzungsberichts ansehen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Abgrenzungsverkaufsvorlagen** ein, und wählen dann den zugehörigen Link aus.
2. Geben Sie auf der Seite **Verkaufsabgrenzungszusammenfassung** im Feld **Saldo ab** das Datum ein, bis zu welchem Sie abgegrenzte Einnahmen anzeigen möchten.
3. Klicken Sie auf die Schaltfläche **Vorschau**.

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

