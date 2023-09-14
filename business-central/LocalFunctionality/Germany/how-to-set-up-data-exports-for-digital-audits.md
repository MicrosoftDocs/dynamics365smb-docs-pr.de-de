---
title: 'Festlegen von Datenexporten für eine digitale Prüfung [DE]'
description: 'Sie müssen die Exportdatensatzquellen einrichten, um die Daten für eine digitale Prüfungen basierend auf GDPdU zu exportieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/27/2022
ms.author: bholtorf
---
# Datenexporte für eine digitale Betriebsprüfung (GoBD/GDPdU) in der deutschen Version festlegen

Sie müssen die Exportdatensatzquellen einrichten, um Daten für eine digitale Prüfung entsprechend den Grundsätzen zum Datenzugriff und zur Prüfbarkeit digitaler Unterlagen (GDPdU) zu exportieren. Für jeden Datenexporttyp müssen Sie eine oder mehrere Datensatzquellen definieren, wobei jede Quelle eine Tabelle darstellt, aus der Daten exportiert werden sollen. 

> [!NOTE]  
> Beim erstmaligen Öffnen der Seite **Datenexporte** werden drei Datenexportdatensätze mit vordefinierten Einstellungen mit den Codes **GLAcc 2022**, **FAAcc 2022** und **Item 2022** erstellt. Betrachten Sie diese Datenexport-Datensätze als vorgefertigte Vorlagen zum Exportieren von Daten aus [!INCLUDE[prod_short](../../includes/prod_short.md)] nach Anforderungen der Behörde.
>
> - **GLAcc 2022** kann zum Exportieren von Sachkonto-/Personendaten verwendet werden.
> - **FAAcc 2022** kann zum Exportieren von Daten verwendet werden, die sich auf Anlagendaten beziehen.
> - **Item 2022** kann zum Exportieren von Artikel- und Rechnungsdaten verwendet werden.


## So richten Sie einen GDPdU-Datenexport ein  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") Symbol. Geben Sie **Datenexporte** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie auf der Seite **Datenexporte** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |-----|-----------|  
    |**Code**|Geben Sie den eindeutigen Code für den Datenexport, wie **Export-1** an.|  
    |**Beschreibung**|Definieren Sie die Beschreibung für den Datenexport.|  

Dem Datenexport müssen Datensatzdefinitionen hinzugefügt werden. Jede Datensatzdefinition stellt eine Tabelle dar, aus der Daten exportiert werden.  

## Wählen Sie eine Datensatzdefinition aus, die Sie einer GDPdU-Definitionsgruppe hinzufügen möchten.  

1. Wählen Sie auf der Seite **Datenexport** in der Gruppe Start die Option **Definitionen aufzeigen** aus.  
2. Füllen Sie auf der Seite **Datenexport - Berichtsdefinitonen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |-----|-----------|  
    |**Datenexportcode**|Wählen Sie den Datenexportcode aus.<br /><br /> Wenn kein Datenexportcode vorhanden ist, können Sie einen neuen erstellen.|  
    |**Beschreibung**|Die Beschreibung der Datensatzdefinition.|  
    |**Exportpfad**|Definieren Sie den Pfad, in dem die exportierten Dateien gespeichert werden.|  

    Als Nächstes müssen Sie die entsprechende .dtd-Datei, die gemäß GDPdU erforderlich ist, z. B. **gdpdu-01-08-2002.dtd** hinzufügen. Wenn Sie eine neue DTD-Datei importieren müssen, um eine vorhandene Datei zu ersetzen, müssen Sie die vorhandene DTD-Datei zuerst exportieren.  

3. Wählen Sie die Aktion **Importieren** aus.  
4. Wählen Sie auf der Seite **Importieren** die DTD-Datei aus, die den Workflow enthält, und wählen Sie dann die Schaltfläche **Öffnen**.  

Danach müssen Sie die Quelle für die zu exportierenden Daten definieren.  

## So fügen Sie einem Datenexport Quelltabellen hinzu  

1. Wählen Sie auf der Seite **Datenexport-Definitionen aufzeichnen** in der Gruppe Start die Option **Quelle aufzeigen** aus.  
2. Füllen Sie auf der Seite **Datenexport - Berichtsquelle** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tabellennr.**|Wählen Sie die Nummer der Haupttabelle aus, aus der Daten exportiert werden sollen.<br /><br /> Wenn Sie einen Wert in Feld **Tabellennr.** eingeben das Feld **Tabellenname** wird aktualisiert.|  
    |**Tabellenname exportieren**|Optional. Es wird eine Archivdatei mit den notwendigen Daten erstellt, die eine Datei INDEX.XML enthält. Sie können den vorgeschlagenen Namen, der in der INDEX.XML-Datei verwendet wird, während des Exports ändern. Der Standardname ist der Name der Tabelle ohne Sonderzeichen aufgrund der Anforderungen des Prüftools.<br /><br /> **Tipp:** In den meisten Fällen basieren die Felder **Tabellenname exportieren** und **Exportdateiname** auf dem gleichen Wert.<br /><br /> Es kann Fälle geben, in denen Sie definieren, die selbe Tabelle mehrfach zu exportieren. Sie können verschiedene Export-Tabellennamen für jeden Tabelleneintrag auswählen, und die Export-Dateiname wird automatisch angepasst. Sie können den Export-Dateinamen ändern, solange er eindeutig ist.<br /><br /> [!INCLUDE[prod_short](../../includes/prod_short.md)] benennt automatisch die Dateien wie folgt.<br /><br /> **Tabellenname** Sachkonto<br /><br /> **Tabellenname exportieren**: Sachkonto<br /><br /> **Dateiname exportieren** Sachkonto.txt<br /><br /> **Tabellenname** Sachkonto<br /><br /> **Tabellenname exportieren:**: Sachkonto1<br /><br /> **Dateiname exportieren:** Sachkonto1.txt|  
    |**Periodenfeldnr.**|Geben Sie einen Filter an, für den das Feld zum Erstellen des XML-Dokuments verwendet wird und legen Sie das Startdatum und das Enddatum des Berichts fest.<br /><br /> Wenn Sie zum Beispiel die Tabelle **Sachposten** als Quelldatei für den Datenexport auswählen, können Sie eines der Datumsfelder auswählen, die in dieser Tabelle stehen.|  
    |**Tabellenfilter**|Geben Sie ein Feld an, für das Sie einen Filter festlegen möchten.<br /><br /> Auf der Seite **Tabellenfilter** geben Sie Filtereinstellungen in der Spalte **Feldfilter** ein.<br /><br /> Beispielsweise können Sie ein Feld angeben, das Informationen über den Betrag überträgt. Sie können ein Datumsfeld festlegen und dafür einen Filter setzen, wenn Sie in einem Zeitraum unterschiedliche Startdaten setzen möchten. Enddatum. Sie können ein Datumsfeld nicht angeben und dafür einen Filter festlegen, wenn dasselbe Feld bereits im Feld Perioden-Gebiet " verwendet wird.|  
    |**Feldnr. Datumsfilter**|Definieren Sie ein Filterfeld, wenn die Tabelle eines hat.<br /><br /> Wenn die Tabelle mehr als einen Datumsfilter hat, definieren Sie keinen in diesem Feld.|  
    |**Behandlung von Datumsfiltern**|Geben Sie an, wie z. B. Datumsfilter bearbeitet werden sollen:<br /><br /> - \<blank\>: Es ist kein Filter festgelegt.<br /><br /> - Periode: Verwenden Sie das angegebene Startdatum und das Enddatum.<br /><br /> - Nur Enddatum: Verwenden Sie das Enddatum der Stapelverarbeitung.<br /><br /> - Nur Startdatum: Verwenden Sie das Startdatum - 1 der Stapelverarbeitung.|  
    |**Exportdateiname**|Geben Sie den Namen des Arbeitsblattes an, in die die Daten exportiert werden sollen.<br /><br /> Wenn die Tabelle beispielsweise **Sachkonto** ist, kann der Wert des **Tabellennamen exportieren** **Sachkonto** sein, und der Wert des Felds **Exportdateiname** kann **Sachkonto.txt** sein.|  
    |**Schlüsselnr.**|Optional. Definieren Sie das Schlüsselfeld.|

    > [!NOTE]  
    > Die Datei „INDEX.XML“ enthält Tabellen- und Feldnamen in englischer Sprache, die auf den Namen von Tabellen und Feldern basieren. Die Namen von Tabellen und Feldern werden in `<Name>` -Tags und Bildunterschriften in `<Description>` -Tags in der Datei INDEX.xml definiert.   
    
    > [!NOTE]  
    > Tabellen- und Feldnamen werden unverändert geschrieben, einschließlich Leerzeichen, Punkten, Klammern usw. Die einzigen Zeichen, die aus den Namen entfernt werden, sind *&*, *'* (einfaches Anführungszeichen), *"* (doppeltes Anführungszeichen), *<* (Kleiner-als-Zeichen) und *>* (Größer-als-Zeichen).   

    Weitere Informationen finden Sie unter [GDPdU-Filterbeispiele](gdpdu-filter-examples.md).  

    Danach müssen Sie die Felder definieren, von denen Daten exportiert werden.  

3. Im Bereich **Felder** in der Symbolleiste, wählen Sie **Hinzufügen** aus.  
4. Auf der Seite **Datenexport-Felderübersicht** wählen Sie ein oder mehrere Felder aus, die Sie exportieren möchten, und wählen Sie dann die Schaltfläche **OK** aus.  

    1. Wählen Sie auf der Registerkarte die Aktionen **Nach oben** oder **Nach unten**, um die Reihenfolge der Felder zu ändern.  
    2. Um ein Feld aus der Liste der ausgewählten Felder zu entfernen, wählen Sie **Löschen**.  

Sie haben die Haupttabelle hinzugefügt, aus der Daten exportiert werden sollen. Optional können Sie mindestens eine zugehörige Tabelle hinzufügen.  

## So fügen Sie eine verwandte Tabelle einer Datenexportquelle hinzu  

1. Auf der Seite **Datenexport - Datensatzherkunft** in der Zeile unter der Zeile für die Haupttabelle fügen Sie die verknüpfte Tabelle hinzu.  
2. Wählen Sie die Aktion **Einrücken** aus.  
3. Wählen Sie die eingerückte Tabelle aus und wählen Sie dann die Aktion **Beziehung** aus.  
4. Füllen Sie auf der Seite **Datenexport - Berichtsbeziehungstabelle** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Von Feldnr.**|Enthält die Nummer des Feld in der übergeordneten Tabelle. Sie können angeben, dass das Feld einen Bezug zu einem Feld in der untergeordneten Tabelle besitzt.|  
    |**Zu Feldnr.**|Enthält die Nummer des Felds in der untergeordneten Tabelle. Sie können angeben, dass ein Feld in der übergeordneten Tabelle einen Bezug zu diesem Feld besitzt.|  

    > [!NOTE]  
    >  Die Felder **Von Feldname** und **Zu Feldname** werden automatisch ausgefüllt.  

5. Wählen Sie die Schaltfläche **OK** aus.  

Nachdem Sie Tabellen und Felder hinzugefügt haben, müssen Sie überprüfen, dass die Struktur der Datenexportquelle korrekt ist.  

## Um die Datenexportquelle zu überprüfen  

Wählen Sie auf der Seite **Datenexport-Quelle aufzeichnen** in der Gruppe Start die Option **Überprüfen** aus.  

Dies überprüft die Liste der Felder anhand der Schlüssel für die Tabellen. Wenn Sie einen Primärschlüssel auswählen, nachdem Sie einen sekundären Schlüssel ausgewählt haben, wird eine Fehlermeldung angezeigt und Sie müssen die Reihenfolge der Felder im Bereich **Felder** ändern.

## Siehe auch

[Prozess für Digital-Überwachung (GoBD/GDPdU)](process-for-digital-audits.md)  
[Daten für eine digitale Prüfung exportieren](how-to-export-data-for-a-digital-audit.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
