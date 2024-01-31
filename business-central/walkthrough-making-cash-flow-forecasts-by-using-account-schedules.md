---
title: Erstellen Sie Cashflow-Prognosen mithilfe von Finanzberichten
description: 'Diese exemplarische Vorgehensweise beschreibt, wie Sie Finanzberichte verwenden können, um Cashflow-Prognosen in Business Central zu erstellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Walkthrough: Erstellen Sie Cashflow-Prognosen mithilfe von Finanzberichten

Diese exemplarische Vorgehensweise beschreibt, wie Sie Finanzberichte verwenden können, um Cashflow-Prognosen zu erstellen. Finanzberichte führen Berechnungen aus, die nicht direkt im Kontenplan für Cashflowkonten vorgenommen werden können. In Finanzberichten können Sie Zwischensummen für Cashflow-Auftragseingänge und -Auszahlungen einrichten. Diese Zwischensummen können in neue Summen einbezogen werden, die dann für Cashflowplanungen verwendet werden können.  

## Informationen zu dieser exemplarischen Vorgehensweise

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Einrichten eines neuen Cashflowkonto-Finanzberichtnamens.  
- Einrichten von Finanzberichtszeilen.  
- Einrichten einer neuen Spaltendefinition.  
- Zuordnen einer Spaltendefinition zu einem Finanzbericht.  
- Anzeigen und Drucken der Cashflowplanung.  

### Voraussetzungen

Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Ein Cashflowarbeitsblatt mit erfassten Zeilen  

## Rollen

Die Aufgaben in dieser exemplarischen Vorgehensweise werden von den folgenden Benutzern ausgeführt:  

- CONTROLLER  

## Hintergrund

Ken ist ein Controller bei CRONUS , der Monatscashflowplanungen erstellt. Ken schließt Finanzen, Verkauf, Einkauf und Anlagen in die Planungen ein und zeigt sie dann CFO Sara für den Geschäfteseinblick.  

## Einrichten eines neuen Finanzberichtnamens

Der Name des Finanzberichts ist der Name, den Sie der Cashflow-Prognose geben, der eine Reihe definierter Zeilen und eine Spaltendefinition enthält.  

### Einrichten eines neuen Finanzberichtnamens  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Finanzberichte** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Finanzberichte** wählen Sie **Neu**, um einen neuen Cashflow-Finanzberichtsnamen zu erstellen.  
3. Geben Sie im Feld **Namen** **Planung** ein.  
4. Geben Sie im Feld **Beschreibung** eine Beschreibung für die **Cashflowplanung** ein.  
5. Lassen Sie die Felder **Zeilendefinition** und **Spaltendefinition** leer.

## Einrichten von Zeilendefinitionslinien

Nachdem ein Finanzberichtsname eingerichtet wurde, definiert Ken jede Zeile im Cashflow-Finanzbericht. Ken definiert Zeilen, die in Berichten zusätzlich zu den Zeilen angezeigt werden können, die nur Berechnungszwecken dienen.  

### Einrichten von Zeilendefinitionslinien  

1. Auf der Seite **Finanzberichte** wählen Sie den neuen Finanzbericht **Planung** aus, den Sie erstellt haben, und wählen Sie dann **Zeilendefinition bearbeiten**.  
2. Auf der Seite **Zeilendefinition** geben Sie jede Zeile wie in der folgenden Tabelle ein.  

    > [!TIP]  
    > Mithilfe der Funktion **CF-Konten einfügen** können Sie die gewünschten Cashflowkonten aus dem Kontenplan für Cashflowkontos schnell markieren und sie in Zeilendefinitionszeilen kopieren.  

    | Zeilennr. | Description              | Zusammenzählungsart            | Zusammenzählung | Zeilenart   | Betragsart | Anzeigen |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Forderungen              | Cashflowposten - Konten | 10       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Offene Einkaufsaufträge        | Cashflowposten - Konten | 20       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Miete                  | Cashflowposten - Konten | 30       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Finanzanlagen         | Cashflowposten - Konten | 40       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Anlagenabgang    | Cashflowposten - Konten | 50       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Privatinvestitionen      | Cashflowposten - Konten | 60       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Sonstige Lieferungen   | Cashflowposten - Konten | 70       |Bewegung | Nettobetrag  | Ja  |
    | R10     | Offene Serviceaufträge      | Cashflowposten - Konten | 80       |Bewegung | Nettobetrag  | Ja  |
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

## Einrichten einer neuen Spaltendefinition

Vor dem Druzcken der Cashflowplanungen muss Ken die Spaltendefinition für die numerischen Informationen erstellen. In den Spalten definiert Ken die benötigten Informationen, die er in den Zeilen nutzen möchte.

- Die erste Spalte hat die Nummer *C10* mit dem Titel **Betrag** und enthält die Bewegung.  
- Die zweite Spalte die die Nummer *C20* mit dem Titel **Saldo bis Datum** und enthält die Transaktionen für die Periode.  
- Die dritte Spalte die die Nummer *C30* mit dem Titel **Gesamtes Jahr** und enthält die Bewegung in den Salden während des gesamten Geschäftsjahres.  
- Dann weist Ken die Spaltendefinition als Standardoption im **Planungs**-Finanzbericht zu.  

### Eine neue Spaltendefinition einrichten

1. Auf der Seite **Finanzberichte** wählen Sie den Namen des erstellen Finanzbericht **Planung** aus. Wählen Sie auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Spaltendefinition bearbeiten** aus.

2. Erstellen Sie eine neue Spaltendefinition mit dem Namen **Cashflow**.

3. Wählen Sie die Schaltfläche **OK**.

4. Geben Sie jede Zeile genau wie in der folgenden Tabelle ein.

    |Spaltennr.|Spaltenüberschrift|Spaltenart|Postenart|Betragsart|Anzeigen|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |D10|Betrag|Bewegung|Posten|Nettobetrag|Immer|  
    |C20|Betrag bis Datum|Saldo bis Datum|Posten|Nettobetrag|Immer|  
    |C30|Gesamtes Geschäftsjahr|Gesamtes Geschäftsjahr|Posten|Nettobetrag|Immer|

## Zuordnen einer Spaltendefinition zu einem Finanzberichtsnamen

Ken kann die Spaltendefinition jetzt dem Finanzberichtsnamen zuweisen.  

### Zuordnen einer Spaltendefinition zu einem Finanzberichtsnamen

1. Auf der Seite **Finanzberichte** wählen Sie den neuen Finanzbericht **Planung** aus, den Sie erstellt haben, und wählen Sie dann **Spaltendefinition bearbeiten**.  
2. Wählen Sie im Feld **Name** die Spaltendefinition **Cashflow** aus, um es als Standard-Spaltendefinition zuzuordnen.  

## Cashflowplanung anzeigen und drucken

1. Auf der Seite **Finanzberichte** wählen Sie den Finanzbericht **Planung**, um einen neuen Cashflow-Planung anzuzeigen.  
2. Auf der Seite **Finanzbericht** können Sie einen Betrag auswählen und die Cashflowplanungs Posten dann anzeigen, aus denen sich der Betrag zusammensetzt. Darüber hinaus können Sie die Formel anzeigen, die verwendet wird, um den Betrag zu berechnen. Sie können die Beträge auch nach Datum und Dimension filtern.  
3. Wählen Sie die Aktion **Drucken** aus, um die Cashflowplanung zu drucken.  

## Siehe auch

[Mit Finanzberichten arbeiten](bi-how-work-account-schedule.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
