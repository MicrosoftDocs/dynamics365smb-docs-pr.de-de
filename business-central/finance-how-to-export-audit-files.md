---
title: Export der Protokolldatei
description: 'In diesem Artikel wird erläutert, wie Sie verschiedene Exportformate einrichten und diese dann verwenden, basierend auf Wirtschaftsprüfer- oder Behördenanforderungen.'
author: altotovi
ms.service: dynamics365-business-central
ms.topic: how-to
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# <a name="audit-file-export" />Export der Protokolldatei

Der Export von Buchhaltungsinformationen aus dem System ist eine häufige Anforderung einiger lokaler Behörden oder Wirtschaftsprüfer. Exporte von Formaten und erforderlichen Informationen können davon abweichen. Einträge für den Export sind in der Regel Hauptbucheinträge (Sachbuch) oder Mehrwertsteuereinträge (MwSt.). Manchmal sind jedoch weitere Informationen erforderlich.

**Prüfdateiexport** ist eine vorinstallierte Erweiterung, mit der Sie verschiedene Einträge basierend auf Wirtschaftsprüfer- oder Behördenanforderungen exportieren können. Sie können die Funktionalität der Erweiterung unabhängig vom Formattyp oder den Einträgen verwenden, um den Datenexportprozess zu steuern. Die Funktionalität hat für den Export kein vorinstalliertes Dateiformat. Daher müssen Sie entweder eine App mit einem bestimmten Format installieren (z. B. SIE, SAF-T oder FAC) oder Ihr eigenes entwickeln.

> [!NOTE]
> Derzeit können Sie als zusätzliche App das SIE- oder SAF-T-Format auswählen. Partner können auch ein benutzerdefiniertes Format entwickeln. Die Anzahl der verfügbaren Formate wird im Laufe der Zeit zunehmen.

## <a name="set-up-audit-file-export" />Prüfdateiexport einrichten

1. Wählen Sie die Suchschaltfläche ![Lupenschaltfläche aus, welche das „Sie wünschen ...“-Feature öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"), geben Sie **Prüfdateiexport einrichten** ein und wählen Sie dann den entsprechenden Link aus.
2. Führen Sie auf der Seite **Prüfdateiexport einrichten** die folgenden Schritte aus:

    1. Geben Sie auf dem Inforegister **Allgemein** im Feld **Code des Exportformats für Protokolldatei** den Code des Standardexportformats der Prüfdatei ein. Nur die Formate sind verfügbar, die aktiviert wurden, als ein bestimmtes Dateiformat aus der Funktionsverwaltung installiert wurde, sowie die als benutzerdefiniertes Format hinzugefügt wurden.
    2. Aktivieren Sie auf dem Inforegister **Datenqualität** das Kontrollkästchen **Unternehmensinformationen prüfen**, um über darüber benachrichtigt zu werden, wenn Unternehmensinformationsfelder nicht richtig eingerichtet sind.
    3. Wählen Sie das Kontrollkästchen **Debitor prüfen** aus, um benachrichtigt zu werden, die für bestimmte Debitoren nicht ordnungsgemäß eingerichtet wurden.
    4. Wählen Sie das Kontrollkästchen **Kreditor prüfen** aus, um benachrichtigt zu werden, die für bestimmte Kreditoren nicht ordnungsgemäß eingerichtet wurden.
    5. Wählen Sie das Kontrollkästchen **Bankkonto prüfen** aus, um benachrichtigt zu werden, die für bestimmte Bankkonten nicht ordnungsgemäß eingerichtet wurden.
    6. Aktivieren Sie das Kontrollkästchen **Postleitzahl prüfen** aus, um darüber benachrichtigt zu werden, wenn eine Postleitzahl nicht korrekt eingerichtet wurde.
    7. Aktivieren Sie das Kontrollkästchen **Adresse prüfen**, um benachrichtigt zu werden, wenn eine Adresse nicht korrekt eingerichtet wurde.
    8. Geben Sie im Feld **Standardpostleitzahl** die Postleitzahl ein, die verwendet werden soll, wenn auf der Debitoren- oder Kreditorenkarte keine Postleitzahl angegeben ist.

3. Wählen Sie die Suchschaltfläche ![Lupenschaltfläche aus, welche das „Sie wünschen ...“-Feature öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"), geben Sie **Exportformat für Prüfdatei einrichten** ein und wählen Sie dann den entsprechenden Link aus.
4. Führen Sie auf der Seite **Exportformat für Prüfdatei einrichten** die folgenden Schritte aus:

    1. Wählen Sie das Exportformat für die Prüfdatei aus, das Sie konfigurieren wollen. Nur die Formate sind verfügbar, die aktiviert wurden, als ein bestimmtes Dateiformat aus der Funktionsverwaltung installiert wurde, sowie die als benutzerdefiniertes Format hinzugefügt wurden.
    2. Geben Sie im Feld **Prüfdateiname** den Standarddateinamen oder die Dateinamenvorlage für die Prüfdatei an, die Sie exportieren möchten.
    3. Aktivieren Sie das Kontrollkästchen **In Zip archivieren**, um exportierte Dateien automatisch zu komprimieren.

## <a name="provide-the-gl-account-mapping-for-audit-file-export" />Die Sachkontenzuordnung für den Prüfdateiexport angeben

Für die meisten von Behörden angeforderten Formate für Sachkonten ist ein bestimmter Standardkontenplan erforderlich. Nachdem Sie Ihre Sachkonten konfiguriert haben, basiert Ihre exportierte Datei daher auf diesen Zuordnungen. Sie können mehr Zuordnungen in Ihrem System verwenden.

Gehen Sie wie folgt vor, um die Sachkontenzuordnung für den Prüfdateiexport anzugeben.

1. Wählen Sie die Suchschaltfläche ![Lupenschaltfläche aus, welche das „Sie wünschen ...“-Feature öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Sachkontozuordnung** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie auf der Seite **Sachkontozuordnung** **Neu**, um eine Zuordnung zu erstellen.
3. Geben Sie im Feld **Code** den Zuordnungscode an, der für den Berichtszeitraum steht.
4. Wählen Sie im Feld **Standardkontotyp** den Typ des Standardsachkontos aus.
5. Geben Sie im Feld **Exportformat für Prüfdatei** das Exportformat der Prüfdatei an, mit dem die Standardsachkonten verknüpft sind.
6. Im Feld **Periodentyp** gibt das System eine Buchhaltungsperiode oder einen benutzerdefinierten Periodentyp an, der basierend auf Ihrer Auswahl ein flexibles Startdatum und eine flexible Startzeit hat. Wenn Sie eine bestimmte Buchhaltungsperiode auswählen, wird das Feld auf **Buchhaltungsperiode** gesetzt. Andernfalls wird er auf **Datenbereich** gesetzt.
7. Geben Sie im Feld **Buchhaltungsperiode** das Startdatum der Buchhaltungsperiode an, die als Berichtszeitraum verwendet werden soll, wenn sie identisch sein sollen.
8. Wenn Sie das Feld **Buchhaltungsperiode** festlegen, werden die Felder **Anfangsdatum** und **Enddatum** basierend auf dem von Ihnen angegebenen Zeitraum automatisch festgelegt. Andernfalls können Sie das Start- und Enddatum für Ihre Berichterstellung manuell festlegen.
9. Wenn Sie bereits einen Standardkontenplan hinzugefügt haben, gehen Sie folgendermaßen vor:

    1. Geben Sie im Feld **Standard-Kontokategorienr.** die Kategorie des Standardkontos oder den Gruppierungscode an, der für die Zuordnung verwendet wird
    2. Geben Sie im Feld **Standard-Kontokategorienr.** den Standardkontocode oder den Gruppierungscode an, der für die Zuordnung verwendet wird

10. Wählen Sie das Kontrollkästchen **Eingangssaldo einbeziehen** aus, um anstelle der Nettoveränderung des Berichtszeitraums den Eingangssaldo des Sachkontos vom Typ **Bilanzkonto** für die Zuordnung zu berücksichtigen.
11. Gehen folgendermaßen vor, um mit der Zuordnung zu beginnen:

    1. Um Zeilen auf der Seite **Sachkontozuordnung** auf Grundlage eines vorhandenen Kontenplans zu generieren, wählen Sie **Quelle für Zuordnung initialisieren** aus. Um die Sachkontenzuordnung aus einem anderen Zuordnungscode zu kopieren, wählen Sie **Aus einer anderen Zuordnung kopieren** aus. Wenn Sie mit dem Anlegen von Zeilen fertig sind, werden alle Sachkonten mit gebuchten Einträgen grün markiert.
    2. Um nur Sachkonten mit Buchungen zu markieren, wählen Sie **Verfügbarkeit von Sachkontoeintrag aktualisieren** aus. Wenn die Option **Eingangssaldo einbeziehen** aktiviert ist, werden alle gebuchten Sachkontoeinträge für die Berechnung berücksichtigt. Ansonsten werden nur Sachkontoeinträge des Berichtszeitraums berücksichtigt.

## <a name="export-the-audit-file" />Die Prüfdatei exportieren

1. Wählen Sie die Suchschaltfläche ![Lupenschaltfläche aus, welche das „Sie wünschen ...“-Feature öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Exportbelege für Prüfdatei** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie auf der Seite **Exportbelege für Prüfdatei** **Neu** aus.
3. Gehen Sie auf dem Inforegister **Allgemein** folgendermaßen vor:

    1. Wählen Sie im Feld **Exportformat für Prüfdatei** das Format aus, das zum Exportieren der Prüfdatei verwendet wird.
    2. Wählen Sie im Feld **Sachkontozuordnungscode** den Sachkontozuordnungscode für den Berichtszeitraum aus.
    3. Wählen Sie das Kontrollkästchen **Nach Monat aufteilen** aus, wenn mehrere Prüfdateien pro Monat generiert werden sollen.
    4. Wählen Sie das Kontrollkästchen **Nach Datum aufteilen** aus, wenn mehrere Prüfdateien pro Tag generiert werden sollen.
    5. Geben Sie im **Kopfzeilenkommentar** den Kommentar ein, den Sie in die Kopfzeile der Prüfdatei einfügen wollen.
    6. Geben Sie im Feld **Kontakt** den Kontakt ein, der in die Kopfzeile der Prüfdatei exportiert werden soll.
    7. Wählen Sie das Kontrollkästchen **Mehrere ZIP-Dateien erstellen** aus, um mehrere ZIP-Dateien zu generieren.

        > [!IMPORTANT]
        > Aktivieren Sie dieses Kontrollkästchen nur, wenn Sie zuvor einige der Format-Apps installiert oder eine benutzerdefinierte App erstellt haben. Durch die Installation eines oder mehrerer der spezifischen Formate werden wahrscheinlich, je nach den Formatanforderungen, Felder und Funktionen zu der Funktionalität **Prüfdateien exportieren** hinzugefügt.

4. Gehen Sie auf dem Inforegister **Verarbeiten** folgendermaßen vor:

    1. Wählen Sie das Kontrollkästchen **Parallelverarbeitung** aus, wenn Sie möchten, dass die Generierung der Prüfdatei von parallelen Hintergrundaufträgen verarbeitet wird. Deaktivieren Sie das Kontrollkästchen, um Daten in Ihrer aktuellen Sitzung zu exportieren.
    2. Wenn Sie das Kontrollkästchen **Parallelverarbeitung** aktiviert haben, geben Sie im Feld **Max. Anzahl von Aufträgen** die maximale Anzahl der Hintergrundaufträgen ein, die gleichzeitig ausgeführt werden können.
    3. Geben Sie im Feld **Frühestes Startdatum/früheste Startzeit** das früheste Datum und die früheste Uhrzeit an, zu welcher der Hintergrundauftrag ausgeführt werden muss. Wenn Sie den Prozess durch die Auswahl von **Start** ausführen, können Sie den Status in den Inforegistern **Verarbeiten** und **Zeilen** nachverfolgen.

5. Wenn Sie fertig sind, wählen Sie **Als Datei herunterladen** aus, um die Prüfdatei für die ausgewählte Zeile herunterzuladen.

> [!IMPORTANT]
> Wenn Sie mehrere Einträge exportieren möchten, empfehlen wir, diese aufgrund möglicher Leistungsprobleme nicht in der aktuellen Sitzung zu exportieren. Sie sollten die Parallelverarbeitung stattdessen an arbeitsfreien Tagen oder Stunden verwenden.

## <a name="see-also" />Siehe auch
[Finanzmanagement](finance.md)  
[Das Hauptbuch und den Kontenplan verstehen](finance-general-ledger.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Arbeiten mit Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
