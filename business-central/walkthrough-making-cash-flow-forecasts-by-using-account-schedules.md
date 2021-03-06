---
title: Exemplarische Vorgehensweise – Erstellen von Cashflowplanungen mithilfe von Kontenschemata
description: Erfahren Sie, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 48a176c4c363c4a33ae336d754be71c9f7dd0aeb
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772104"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Exemplarische Vorgehensweise: Erstellen von Cashflowplanungen mithilfe von Kontenschemata

In dieser exemplarischen Vorgehensweise wird beschrieben, wie Sie mit Kontenschemata arbeiten können, um Cashflowplanungen zu erstellen. Kontenschemata führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können. In Kontenschemata können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten. Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Einrichten eines neuen Cashflowkonto-Zeitplannamens.  
- Einrichten von Kontenschemazeilen.  
- Einrichten eines neuen Spaltenlayouts.  
- Zuweisen eines Spaltenlayouts zu einem Kontenschema.  
- Anzeigen und Drucken der Cashflowplanung.  

### <a name="prerequisites"></a>Voraussetzungen

Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Die Cashflowarbeitsblattszeilen werden erfasst  

## <a name="roles"></a>Rollen

Die Aufgaben in dieser exemplarischen Vorgehensweise werden von den folgenden Benutzern ausgeführt:  

- CONTROLLER  

## <a name="story"></a>Hintergrund

Ken ist ein Controller bei CRONUS , der Monatscashflowplanungen erstellt. Es schließt Finanzen, Verkauf, Einkauf und Anlagen in die Planung ein und zeigt sie dann CFO Sara für den Geschäfteseinblick.  

## <a name="setting-up-a-new-account-schedule-name"></a>Einrichten eines neuen Kontenschemanamens

Ein Kontenschema besteht aus einem Cashflow-Kontenschemanamen mit einer Reihe von Zeilen und einem Spaltenlayout.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Einen neuen Kontenschemanamen einrichten:  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kontenschemata** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Cashflow zu erstellen.  
3. Geben Sie im Feld **Namen** **Planung** ein.  
4. Geben Sie im Feld **Beschreibung** eine Beschreibung für die **Cashflowplanung** ein.  
5. Lassen Sie die Felder **Standard Spaltenlayout** und **Analyseansichtsname** leer.  

## <a name="setting-up-account-schedule-lines"></a>Einrichten von Kontenschemazeilen

Nachdem ein Kontenschemaname eingerichtet wurde, definiert Ken jede Zeile, die im Cashflow-Kontenschema angezeigt wird. Ken definiert Zeilen, die in Berichten zusätzlich zu den Zeilen angezeigt werden können, die nur Berechnungszwecken dienen.  

### <a name="to-set-up-account-schedule-lines"></a>So richten Sie Kontenschemazeilen ein  

1. Wählen Sie auf der Seite **Kontenplannamen** den neuen **Prognose** Kontenplannamen, den Sie erstellt haben, und wählen Sie dann die Aktion **Kontenplan bearbeiten**.  
2. Auf der Seite **Kontoplan** geben Sie jede Zeile wie in der folgenden Tabelle ein.  

    > [!TIP]  
    >  Mithilfe der Funktion **CF-Konten einfügen** können Sie die Cashflowkonten aus dem Kontenplan für Cashflowkontos schnell markieren und sie in Kontenschemazeilen kopieren.  

    | Rubrikennr. | Beschreibung              | Zusammenzählungsart            | Zusammenzählung | Zeilenart   | Betragsart | Anzeigen |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Offene Einkaufsaufträge        | Cashflowposten - Konten | 20       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Miete                  | Cashflowposten - Konten | 30       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Finanzanlagen         | Cashflowposten - Konten | 40       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Anlagenabgang    | Cashflowposten - Konten | 50       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Privatinvestitionen      | Cashflowposten - Konten | 60       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Sonstige Lieferungen   | Cashflowposten - Konten | 70       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Offene Serviceaufträge      | Cashflowposten - Konten | 80       |Bewegung | Nettobetrag  | Ja  |
    | R20     | Zahlungseingänge gesamt      | Formel                  | R10      |Bewegung | Nettobetrag  | Ja  |
    | R20     | Zahlungseingänge gesamt      | Formel                  | R10      |Bewegung | Nettobetrag  | Ja  |
    | R30     | Verbindlichkeiten                 | Cashflowposten - Konten | 1010     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Offene Bestellungen     | Cashflowposten - Konten | 1020     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Personalkosten          | Cashflowposten - Konten | 1030     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Lfd. Kosten            | Cashflowposten - Konten | 1040     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Finanzkosten            | Cashflowposten - Konten | 1050     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Investitionen              | Cashflowposten - Konten | 1070     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Privatverbrauch     | Cashflowposten - Konten | 1090     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Fällige MwSt.                  | Cashflowposten - Konten | 1100     |Bewegung | Nettobetrag  | Ja  |
    | R30     | Sonstige Ausgaben           | Cashflowposten - Konten | 1110     |Bewegung | Nettobetrag  | Ja  |
    | R40     | Barausgaben gesamt | Formel                  | R30      |Bewegung | Nettobetrag  | Ja  |
    | R50     | Überschuss                  | Formel                  | R20+R40  |Bewegung | Nettobetrag  | Ja  |
    | R60     | Cashflowmittel          | Cashflowposten - Konten | 2100     |Bewegung | Nettobetrag  | Ja  |
    | R70     | Cashflow gesamt          | Formel                  | R50+R60  |Bewegung | Nettobetrag  | Ja  |

    > [!NOTE]
    > Die Zeilennummer R10 wird verwendet, um die Gesamtsummen für Forderungen zu erfassen. Die Zeilennummer R20 wird verwendet, um die Summe aller Zahlungseingänge zu berechnen. Die Zeilennummer R30 wird verwendet, um die Gesamtsummen für Verbindlichkeiten zu erfassen. Die Zeilennummer R40 wird verwendet, um die Summe aller Barausgaben zu berechnen. Die Zeilennummer R50 wird verwendet, um die Summe des Kassenüberschusses zu erfassen. Die Zeilennummer R60 wird verwendet, um die liquiden Mittel zu erfassen. Die Zeilennummer R70 wird verwendet, um den geplanten Cashflow zu berechnen.

## <a name="setting-up-a-new-column-layout"></a>Einrichten eines neuen Spaltenlayouts.

Bevor Ken die Cashflowplanungen drucken kann, muss er das Spaltenlayout für die numerischen Informationen erstellen. In den Spalten definiert er genau die Informationen, die er aus den Zeilen verwenden möchte.

- Die erste Spalte hat die Nummer *C10* mit dem Titel **Betrag** und enthält die Bewegung.  
- Die zweite Spalte die die Nummer *C20* mit dem Titel **Saldo bis Datum** und enthält die Transaktionen für die Periode.  
- Die dritte Spalte die die Nummer *C30* mit dem Titel **Gesamtes Jahr** und enthält die Bewegung in den Salden während des gesamten Geschäftsjahres.  
- Schließlich weisen Sie das Spaltenlayout als Standard-Spaltenlayout für das Kontenschema **Planung** zu.  

## <a name="to-set-up-a-new-column-layout"></a>So richten Sie ein neues Spaltenlayout ein

1. Wählen Sie im Fenster **Kontoschemaname** den neuen **Planung**-Kontenschemanamen aus, den Sie erstellt haben. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Spaltenlayouteinrichtung bearbeiten** aus.

    > [!TIP]
    > Sie finden die gleiche Aktion auf der Seite **Kontenschema**, wenn Sie das Kontenschema **Prognose** dort noch bearbeiten.

2. Erstellen Sie ein neues Spaltenlayout mit dem Namen **Cashflow**.

3. Wählen Sie die Schaltfläche OK.

4. Geben Sie jede Zeile genau wie in der folgenden Tabelle ein.

    |Spaltennr.|Spaltenüberschrift|Spaltenart|Postenart|Betragsart|Anzeigen|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Betrag|Bewegung|Posten|Nettobetrag|Immer|  
    |C20|Betrag bis Datum|Saldo bis Datum|Posten|Nettobetrag|Immer|  
    |C30|Gesamtes Geschäftsjahr|Gesamtes Geschäftsjahr|Posten|Nettobetrag|Immer|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Das Spaltenlayout dem Kontenschemanamen zuweisen

Ken kann das Spaltenlayout jetzt dem Kontenschemanamen zuweisen.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Das Spaltenlayout dem Kontenschemanamen zuweisen:  

1. Auf der Seite **Kontenschema**, auf der Sie mit dem Kontenschema **Prognose** arbeiten, wählen Sie die Aktion **Spaltenlayout-Setup bearbeiten**.  
2. Wählen Sie im Feld **Spaltenlayoutname** das Spaltenlayout **Cashflow** aus, um es als Standard-Spaltenlayout zuzuordnen.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>So können Sie die Cashflowplanung anzeigen und drucken

1. Wählen Sie auf der Seite **Kontoschemanamen** auf der Registerkarte **Übersicht** in der Gruppe Prozess die Option Übersicht aus, um die Cashflowplanung anzuzeigen.  
2. Auf der Seite **Kontoschemaübersicht** können Sie einen Betrag auswählen und die Cashflowplanungs Posten dann anzeigen, aus denen sich der Betrag zusammensetzt. Darüber hinaus können Sie die Formel anzeigen, die verwendet wird, um den Betrag zu berechnen. Sie können die Beträge auch nach Datum und Dimension filtern.  
3. Wählen Sie die Aktion **Drucken** aus, um die Cashflowplanung zu drucken.  

## <a name="see-also"></a>Siehe auch

[Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]