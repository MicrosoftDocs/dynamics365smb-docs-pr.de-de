---
title: Mit Intrastat-Berichten arbeiten
description: 'Erfahren Sie, wie Sie den Handel mit Firmen in anderen EU-Ländern/-Regionen mit Hilfe des Intrastat-Systems melden können.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 01/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---
# <a name="work-with-intrastat-reporting"></a>Mit Intrastat-Berichten arbeiten

Alle Firmen in der Europäischen Union (EU) müssen ihren Handel mit anderen EU-Ländern/Regionen melden. Warenbewegungen müssen jeden Monat dem Statistischen Amt Ihres Landes/Ihrer Region mitgeteilt und die Berichte müssen an die Steuerbehörden übermittelt werden. Intrastat ist das System zur Erfassung von Handelsstatistiken für Waren innerhalb dieser Länder/Regionen. Sie verwenden **Intrastat-Bericht**, um periodische Intrastat-Berichte (in der Regel monatlich) zu erstellen, in denen der Handel mit Waren gemäß der lokalen Gesetzgebung erfasst, aufgezeichnet und gemeldet wird.

Die Intrastat-Meldungen basieren auf den grundlegenden EU-Vorschriften, die für alle Länder/Regionen gelten; in der Praxis gibt es jedoch einige Unterschiede zwischen den einzelnen Ländern/Regionen. Jedes Land/jede Region hat seine/ihre eigenen Regeln, was genau und wie zu melden ist.

> [!IMPORTANT]  
> Dieser Artikel beschreibt das neue Intrastat-Erlebnis, das ab der [!INCLUDE[prod_short](includes/prod_short.md)] Veröffentlichungswelle 2 im Jahr 2022 zur Verfügung steht, erweiterte Funktionen enthält und [für bestehende Firmen eingeschaltet werden muss](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Wenden Sie sich an Ihren Administrator, um die neue Funktionalität einzuschalten und festzulegen.
>
> Lesen Sie den Artikel zur Einrichtung und Verwendung von Intrastat in der Vorgängerversion unter [Intrastat einrichten und melden](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]  
> Intrastat-Informationen gelten nicht für die Bewegung von Dienstleistungen zwischen Ländern/Regionen, sondern nur für Waren (Artikel und Anlagen). Wenn die lokale Regierung die Registrierung des Dienstleistungsverkehrs zwischen Ländern/Regionen verlangt, kann dies über die Funktion **Dienstleistungserklärung** erfolgen.
>
> Wir gehen derzeit davon aus, dass diese Funktion ab November 2022 als App unter [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) verfügbar sein wird. Um sie zu nutzen, müssen Sie sie zu diesem Zeitpunkt zunächst auf der Seite **Erweiterungsverwaltung** installieren.

## <a name="fill-in-the-intrastat-report"></a>Füllen Sie im Intrastat-Bericht

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol aus, geben Sie **Intrastat Liste** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**, um einen neuen **Intrastat-Bericht** zu erstellen.
3. Wenn Sie einige interne Informationen über den **Intrastat Bericht** eingeben müssen, tragen Sie diese Informationen in das Feld **Beschreibung** ein.
4. Geben Sie im Feld **Statistischer Zeitraum** den Monat an, für den die Daten gemeldet werden sollen. Geben Sie den Zeitraum als vierstellige Zahl ohne Leerzeichen oder Symbole ein. Je nach Land/Region geben Sie entweder zuerst den Monat und dann das Jahr ein oder umgekehrt. Geben Sie zum Beispiel entweder *2206* oder *0622* für Juni 2022 ein.
5. Wählen Sie die Aktion **Mahnungszeile vorschlagen**. Die Felder **Beginndatum** und **Enddatum** enthalten bereits die für den Statistikzeitraum im Kopf des Intrastat-Berichts angegebenen Daten.
6. Im Feld **Kosten Zu-/Abschlag %** können Sie einen Prozentsatz (zur Deckung der Transport- und Versicherungskosten) eingeben. Wenn Sie einen Prozentsatz eingeben, ist der Inhalt des Feldes **Statistischer Wert** dementsprechend höher. Wenn Sie diese Funktion jedoch nutzen möchten, müssen Sie das Feld **Betrag inkl. Artikel Zu-/Abschläge** auf **Ja** setzen.
7. Schließlich können Sie auf dem Inforegister **Zusätzlich** zusätzliche Konfigurationen festlegen:
   1. **Neuberechnung für Nullbeträge übergehen**, um festzulegen, dass Zeilen ohne Beträge während des Batchauftrags nicht neu berechnet werden.
   2. **Nullbeträge überspringen**, um festzulegen, dass Artikelposten ohne Beträge nicht in den Batchauftrag aufgenommen werden.
   3. **Nicht fakturierte Einträge überspringen**, um festzulegen, ob Sachkontoeinträge, die versandt oder empfangen, aber noch nicht fakturiert wurden, von dem Prozess ausgeschlossen werden sollen.
8. Klicken Sie zum Starten des Batchauftrags auf **OK**.

Der Batchauftrag ruft alle Elemente im Statistikzeitraum ab und fügt sie als Zeilen in den **Intrastat-Bericht** ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Ändern des Intrastat-Berichts

Bei Bedarf können Sie die Zeilen ändern, aber immer wenn Sie einen Wert in der Zeile des Intrastat-Berichts ändern, wird das Feld **Korrektur** automatisch als **Ja** markiert. Schließlich können Sie auch manuell eine neue Zeile hinzufügen, wenn es dafür einen Grund gibt. Um eine neue Zeile manuell hinzuzufügen:

1. Wählen Sie auf der Seite **Intrastat-Bericht** die Aktion **Neue Zeile** in der Registerkarte **Zeilen**.
2. Wählen Sie die Option **Empfang** oder **Versand** im Feld **Typ**.
3. Wählen Sie im Feld **Quellentyp** eine der Quellen: **Element erfassen**, **FA erfassen** oder **Auftrag erfassen**.
4. Basierend auf dem **Quellentyp** im Feld **Positionsnummer** können Sie ein **Element** (in beiden Fällen **Positionserfassung** oder **Job-Erfassung**) oder **Anlagen** wählen.
5. Füllen Sie weitere Felder aus, die Sie für die Intrastat-Berichterstattung benötigen.

> [!NOTE]  
> Wenn Sie dem Intrastat-Bericht manuell eine neue Zeile hinzufügen, muss das Feld **Datum** in der Zeile innerhalb des Bereichs **Statistischer Zeitraum** liegen, den Sie in der Kopfzeile hinzugefügt haben.

## <a name="validate-intrastat-lines"></a>Intrastat-Zeilen validieren

Nachdem Sie den **Intrastat-Bericht** ausgefüllt haben, können Sie die Aktion **Checkliste Bericht** ausführen, um sicherzustellen, dass alle Informationen im **Intrastat-Bericht** korrekt sind. Pflichtfelder, die Sie auf der Seite **Intrastat Bericht Checkliste** festgelegt haben und deren Werte fehlen, werden in der **Fehler und Warnung** FactBox auf der Seite **Intrastat Bericht** angezeigt.

Führen Sie den Bericht **Prüfliste Intrastat-Bericht** aus, um die Intrastat-Zeilen zu prüfen, bevor sie in das gewünschte Format exportiert werden. Die Prüfung wird innerhalb des **Intrastat-Berichts** ausgeführt.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Neuberechnung von Gewicht oder zusätzlicher Maßeinheit

Wenn Sie die Fehlermeldung *„Gesamtgewicht“ in der Intrastat-Berichtszeile darf nicht leer sein* erhalten, liegt das wahrscheinlich daran, dass Sie das Feld **Nettogewicht** nicht auf der verwendeten Quelle, dem Artikel oder der Anlage festgelegt haben. Suchen Sie in diesem Fall nach der Karteikarte für das Element oder die Anlage und fügen Sie den erforderlichen Wert hinzu. Danach müssen Sie nur den **Intrastat Bericht** erneut öffnen und die folgenden Schritte ausführen:

1. Wählen Sie die Option **Recalc. Gewicht/Suppl. UOM**, um das **Gesamtgewicht** und/oder die **Zusatzmenge** neu zu berechnen.
2. Wählen Sie eine der Optionen:

    1. **Gewicht** - um nur das **Gesamtgewicht** neu zu berechnen, basierend auf den aktuellen Informationen zum **Nettogewicht** auf den Karten der Elemente und Anlagen.
    2. **Zusatzmenge** - um nur die **Zusatzmenge** in der Zeile **Intrastat-Bericht** neu zu berechnen, falls vorhanden, basierend auf den aktuellen Informationen über **Zusatzeinheit** auf den Karten der Elemente und Anlagen.
    3. **Beides** - um sowohl **Gesamtgewicht** als auch **Zusatzmenge** neu zu berechnen, basierend auf den aktuellen Informationen auf den Karten der Elemente und Anlagen.
3. Wählen Sie **OK**, um den Batchauftrag zu starten.

## <a name="report-intrastat-in-a-file"></a>Intrastat Berichte in einer Datei

Sie können den Intrastat-Bericht als Datei senden, je nach den Anforderungen der verschiedenen lokalen Behörden. Bevor Sie die Datei erstellen, sollten Sie den **Checklistenbericht** ausführen, um zu prüfen, ob alle Zeilen alle notwendigen und gültigen Informationen enthalten. So erstellen Sie eine Datei:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Intrastat Liste** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie **Intrastat-Bericht**, den Sie als Datei melden möchten.
3. Falls Sie dies noch nicht getan haben, füllen Sie den **Intrastat-Bericht** manuell aus oder wählen Sie die Aktion **Zeilen vorschlagen**.
4. Wählen Sie die Aktion **Aus Datei erstellen** aus.
5. Die Intrastat-Datei wird in dem gewünschten Format gespeichert.

Sobald Sie die Datei erstellt haben, füllt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die folgenden Details zum Bericht aus:

* Das **Exportdatum**, um das Datum anzugeben, an dem der Bericht exportiert wurde.
* Die **Exportzeit**, um die Uhrzeit anzugeben, zu der der Bericht exportiert wurde.

> [!NOTE]  
> Wenn Sie das nächste Mal eine Datei erstellen, werden in den Feldern **Exportdatum** und **Exportzeit** nur Informationen über die zuletzt erstellte Datei gespeichert.

## <a name="intrastat-rules"></a>Intrastat-Regeln

### <a name="grouping-lines"></a>Zeilen gruppieren

In **Intrastat-Bericht**-Zeilen gibt es keine Gruppierung nach Feldern. Alle Einträge werden aus der Originalquelle kopiert, so dass Sie sie anhand der Kombination von **Quellentyp** und **Quellennummer** schnell auffinden können.

Die von den Behörden benötigte Gruppierung wird in der exportierten Datei bereitgestellt. Sie müssen dies in der **Data Exchange Definition** konfigurieren, die vollständig konfigurierbar ist. Weitere Informationen finden Sie unter [Definitionen für den Datenaustausch festlegen](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Berichterstattung über Anlagen

Anlagen werden in den Intrastat Zeilen nur angezeigt, wenn:

* Die **FA-Buchungsart** im Feld **Sachkonto-Eintrag** ist **Anschaffungskosten** und wenn die **Belegart** im Falle von Einkäufen **Rechnung** ist und
* Die **FA-Buchungsart** im Feld **Mehrwertsteuer-Sachkonto** ist **Verkaufserlös** und wenn die **Belegart** **Rechnung** ist, im Falle von Verkäufen.

### <a name="intrastat-report-statuses"></a>Status der Intrastat-Berichte

Wenn Sie mit dem **Intrastat-Bericht** arbeiten, sehen Sie ein **Status**-Feld im Dokumentenkopf. Hier finden Sie die folgenden Status zusammen mit den dazugehörigen Regeln:

* **Offen**: Dieser Status wird automatisch erstellt, wenn Sie einen neuen Intrastat-Bericht erstellen und Sie können alle Vorgänge in diesem Status durchführen.
* **Freigegeben**: [!INCLUDE[prod_short](includes/prod_short.md)] ändert den Status automatisch auf *Freigegeben*, wenn Sie eine Datei erstellen. Von diesem Moment an können Sie Ihren **Intrastat-Bericht** nicht mehr ändern. Wenn Sie etwas ändern und erneut berichten müssen, können Sie die Aktion **Wieder öffnen** verwenden, um den Intrastat-Bericht erneut zu öffnen. Sobald das Dokument wieder geöffnet ist, können Sie die Aktion **Freigeben** verwenden, um das Dokument wieder freizugeben.
* **Gemeldet**: Gibt an, ob der Eintrag bereits an die Steuerbehörden gemeldet wurde. Dies ist kein regulärer Status, sondern ein unabhängiges Feld. Selbst wenn Sie den Intrastat-Bericht erneut öffnen würden, würde er anzeigen, dass die Datei für diesen Bericht bereits erstellt wurde.

### <a name="locations-in-intrastat-reporting"></a>Standorte in der Intrastat-Berichterstattung

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet immer die Informationen im Feld **Länder-/Regionscode** auf der Seite **Standortkarte** als Land für den **Absender** oder **Empfänger** von Waren. Wenn diese Informationen nicht vorhanden sind oder der Standort nicht verwendet wurde, verwendet das System die Informationen von der Seite **Unternehmensinformationen**.   

> [!NOTE]  
> Wenn das Unternehmen in mehr als einem Land tätig ist, funktionieren die Intrastat-Berichte nicht für alle Länder, in denen Standorte konfiguriert sind. Die Berichterstattung basiert nur auf dem Hauptland, da es derzeit nicht möglich ist, länderübergreifende Berichte zu verwenden.  

### <a name="triangular-trade-in-intrastat"></a>Dreiecksgeschäft in Intrastat

Beim Dreiecksgeschäft handelt es sich um den Handel zwischen drei Ländern oder Regionen, bei dem die Waren das Land des berichtenden Unternehmens umgehen. In Business Central kann dies auch durch die Funktion [Direktlieferung](sales-how-drop-shipment.md) durchgeführt werden. Um diese Option zu aktivieren, aktivieren Sie das Feld **Direktlieferung einschließen** in der **Intrastat-Berichtseinrichtung**.  

Wenn Sie diese Option aktivieren, verwendet das System die folgenden Regeln, jedoch nur, wenn Sie **Direktlieferung** im **Verkaufsauftrag** gekennzeichnet haben: 

| Wareneingangsformular | Lieferung an | Erwartetes Intrastat-Ergebnis |
|----------|------------|----------------------|
| Land gemäß den **Unternehmensdaten** | Land gemäß den **Unternehmensdaten** | Keine Intrastat-Positionen |  
| Land gemäß den **Unternehmensdaten** | EU-Land weicht vom Land in den **Unternehmensdaten** ab | Intrastat-Versandposition | 
| Land gemäß den **Unternehmensdaten** | Nicht-EU-Land | Keine Intrastat-Positionen |   
| EU-Land weicht vom Land in den **Unternehmensdaten** ab | Land gemäß den **Unternehmensdaten** | Intrastat-Eingangspositionen | 
| EU-Land weicht vom Land in den **Unternehmensdaten** ab | EU-Land weicht vom Land in den **Unternehmensdaten** ab | Keine Intrastat-Positionen |
| EU-Land weicht vom Land in den **Unternehmensdaten** ab | Nicht-EU-Land | Keine Intrastat-Positionen | 
| Nicht-EU-Land | Land gemäß den **Unternehmensdaten** | Keine Intrastat-Positionen |  
| Nicht-EU-Land | EU-Land weicht vom Land in den **Unternehmensdaten** ab | Keine Intrastat-Positionen |
| Nicht-EU-Land | Nicht-EU-Land | Keine Intrastat-Positionen |   

## <a name="see-also"></a>Siehe auch

[Intrastat-Berichte einrichten](finance-how-setup-report-intrastat.md)  
[Finanzmanagement](finance.md)  
[Direktlieferung](sales-how-drop-shipment.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
