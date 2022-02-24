---
title: Wie Sie Daten für eine Digital-Überwachung exportieren
description: Sie können Unternehmensdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. In der folgenden exemplarischen Vorgehensweise wird der durchgängige Prozess beschrieben, dies ist jedoch nur ein Beispiel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6e179f21988d5bdd4d15f1961b1cb2c6af5c578e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181150"
---
# <a name="walkthrough-exporting-data-for-a-digital-audit"></a>Wie Sie Daten für eine Digital-Überwachung exportieren
Sie können Geschäftsdaten für Überwachungszwecke exportieren. Die Einrichtung des Datenexportes unterscheidet sich von anderen Unternehmen und Sie sollten Ihren Steuerberater und den Steuerprüfer um Rat fragen. In der folgenden exemplarischen Vorgehensweise wird der durchgängige Prozess beschrieben, dies ist jedoch nur ein Beispiel.  

Die Beispielimplementierung illustriert ein Szenario, in dem der Prüfer Sie auffordert, Daten aus der Finanzbuchhaltung zu exportieren, und Informationen über Ihre Debitoren und Kreditoren bereitzustellen. Dies ist kein Beispiel, das auf tatsächlichen Anforderungen von Steuerprüfern basiert, aber es dient zur Veranschaulichung, wie Sie Daten entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU) in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] exportieren.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

- Einrichten von Anforderungen für den Datenexport.  
- Einrichten von Quellen für den Datenexport.  
- Exportieren von Daten für die Steuerprüfer.  

## <a name="prerequisites"></a>Voraussetzungen  
Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

- Die deutsche Version von [!INCLUDE[d365fin](../../includes/d365fin_md.md)] mit dem CRONUS AG-Demounternehmen.
- Die .DTD-Datei, die gemäß GDPdU erforderlich ist. In diesem Szenario **gdpdu-01-08-2002.dtd**.  

## <a name="story"></a>Hintergrund  
Cassie ist Buchhalterin bei der CRONUS AG. Sie wurde vom Steuerprüfer des Unternehmens benachrichtigt, dass diese eine Liste der Bestellungs- und Verkaufstransaktionen im ersten Quartal des Kalenderjahres 2013 einsehen wollen. Cassie kennt die Art der Finanzdaten, die der Prüfer möchte, aber sie benötigt die Hilfe von Sean, um den Export einzurichten.  

Sean ist ein Hauptbenutzer der CRONUS AG. Er versteht, wie die Daten technisch mit Tabellen und Feldern eingerichtet werden. Daher unterstützt er normalerweise Cassie, die Datenexporte für die Prüfer einzurichten. Von anderen Datenexporten weiß er, dass das Werkzeug, das die Prüfer verwenden, einige Anforderungen hat, was die exportierten Dateien enthalten müssen, aber er braucht die Hilfe von Cassie, um genau festzulegen, welche Daten benötigt werden.  

## <a name="defining-the-requirements"></a>Festlegen der Anforderungen  
Cassis richtet die anforderungen für den Datenexport ein. Die Prüfer haben sie um Einsicht in Transaktionen mit Debitoren und Kreditoren gebeten. Daher weiß sie, dass sie Daten aus der Debitoren-, Kreditoren- und der Finanzbuchhaltung benötigt.  

### <a name="to-set-up-the-requirements-for-a-data-export"></a>Einrichten von Anforderungen für den Datenexport  

1.  Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“"), geben Sie **Datenexport** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu**.  
3.  Füllen Sie auf der Seite **Datenexporte** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Der eindeutige Identifikationscode für den Datenexport **AUDIT-Q113**.|  
    |**Beschreibung**|Die Beschreibung für den Datenexport, **Datenexport für Q1 von CY 2013**.|  

    Der eindeutige Identifikationscode **AUDIT-Q113** ist ein Container für den Datenexport  

    Als Nächstes fügt Cassie Beschreibungen der Art der Daten hinzu, die sie im Export benötigt.  

4.  Wählen Sie auf der Seite **Datenexport** in der Gruppe Start die Option **Definitionen aufzeigen** aus.  
5.  Auf der Seite **Datenexport - Datensatzdefinitionen** wählen Sie das Feld **Datensatzcode**, und wählen Sie dann in dem Fenster, das erscheint **Neu** aus.  
6.  Füllen Sie auf der Seite **Datenexport - Berichtsarten** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Enthält den Code für die Art des Geschäfts **GLCUSTVEND**.|  
    |**Beschreibung**|Die Beschreibung für den Datensatztyp, **Sach-, Debitor-. verkaufen**.|  

7.  Wählen Sie die Schaltfläche **OK** aus.  
8.  Füllen Sie auf der Seite **Datenexport - Berichtsdefinitonen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Datensatzcode**|Hier wird der Datensatzcode ausgewählt **GLCUSTVEND**.|  
    |**Beschreibung**|Die Beschreibung für den Datensatztyp wird automatisch hinzugefügt, aber Sie können dieses auf **Finanzbuchhaltung, Debitoren und Kreditoren** ändern.|  
    |**Exportpfad**|Definieren Sie den Pfad, in dem die exportierten Dateien gespeichert werden.<br /><br /> In diesem Szenario **C:Exporte**.|  

    Wenn der angegebene Ordner vorhanden ist, wählen Sie die Schaltfläche **Ja**, um sie zu erstellen.  

Danach definiert Cassie die Quelle für die zu exportierenden Daten. Sie weiß von früheren Exporten, dass sie Daten aus den folgenden Tabellen benötigt:  

- **Sachkonto**  
- **Debitor**  
- **Kreditor**  

### <a name="to-specify-requirements-for-the-source-for-the-data-export"></a>Um Anforderungen für die Quelle für den Datenexport festzulegen  

1.  Wählen Sie auf der Seite **Datenexport-Definitionen aufzeichnen** in der Gruppe Start die Option **Quelle aufzeigen** aus.  
2.  Im **Datenexport - Datensatzherkunft** auf der Seite **Tabellennr.** Feld geben Sie **15** ein.  

    Der Name der untergeordneten Tabelle wird automatisch im Feld **Tabellenname** mit dem **Finanzbuchhaltungskonto** aktualisiert.  

3.  Im Bereich **Notizen** wählen Sie den Link aus, und geben Sie dann den folgenden Text ein:  

    **Ich benötige Posten, die die betroffenen Konten, das Buchungsdatum, den Saldo und die Bewegung anzeigen.**  

4.  Wiederholen Sie die beiden vorherigen Schritte, um die Tabellen 18, **Debitor** und 23 **Kreditor** der Datenexport Datensatzquelle hinzuzufügen.  

    Für diese Tabellen bittet Cassie um Daten für alle Debitoren und Kreditoren sowie um ausführliche Informationen zu jeder Transaktion basierend auf den Debitorenposten und den Kreditorenposten. Sie bittet auch um die Bewegungen am Anfang des Zeitraums, während des Zeitraums und nach dem Zeitraum, für den der Datenexport bestimmt ist.  

5.  Wählen Sie die Schaltfläche **OK** aus.  

Cassie hat die Art der Daten beschrieben, die sie benötigt, und informiert Sean, dass sie dessen Hilfe beim Einrichten des Datenexport benötigt.  

## <a name="setting-up-the-source-for-the-data-export"></a>Einrichten von Quellen für den Datenexport  
Cassie und Sean haben über die Anforderungen gesprochen. Cassie hat erklärt, was die Bemerkungen bedeuten, die sie für die ersten drei Tabellen in den Datensatzquellen erstellt hat. Am nächsten Tag kann Sean die Einrichtung der Quelle für den Datenexport abschließen.  

Zuerst fügt Stephan die erforderliche .dtd-Datei der Datensatzdefinition des Datenexports hinzu.  

### <a name="to-add-a-dtd-file-to-a-record-definition"></a>So fügen Sie eine .dtd-Datei einer zugehörigen Berichtsdefinirion hinzu  

1.  Auf der Seite **Datenexporte** wählen Sie den Datenexport **AUDIT-Q113** und wählen die Aktion **Datensatzdefinitionen**.  
2.  Auf der Seite **Datenexport - Datensatzdefinitionen** wählen Sie die Zeile, in der das Feld **Datenexport - Datensatz-Typcode** auf **GLCUSTVEND** gesetzt ist und wählen dann **Importieren** aus.  
3.  Wählen Sie auf der Seite **Importieren** die DTD-Datei aus, die den Workflow enthält, und wählen Sie dann die Schaltfläche **Öffnen**.  

Als Nächstes fügt Sean der Quelle die Tabelle **Sachposten** hinzu. Dann fügt er Felder aus dieser Tabelle und aus der Tabelle **Sachkonto** hinzu.  

### <a name="to-add-the-gl-entry-table-to-the-data-export-record-source"></a>Um die Sachkontotabelle der Datenexportherkunft hinzuzufügen  

1.  auf der Seite **Datenexport - Datensatzdefinitionen** wählen Sie die Zeile, in der das Feld **Datenexport - Datensatz-Typcode** auf **GLCUSTVEND** gesetzt ist und wählen dann **Datenquelle aufzeichnen** aus.  
2.  auf der Seite **Datenexport - Datensatzherkunft** wählen Sie die Zeile unter der Zeile für die Tabelle **Sachkonto** und wählen dann die Aktion **Neu** aus.  
3.  In der **Tabellennummer** Feld geben Sie **17** ein.  

    Der Name der untergeordneten Tabelle wird automatisch im Feld **Tabellenname** mit dem **Finanzbuchhaltungskonto** aktualisiert.  

4.  Wählen Sie die Aktion **Einrücken** aus.  

    Dieses rückt die Tabelle **Sachposten** unter der Tabelle **Sachkonto** ein. Als Nächstes fügt Stephan eine Tabellenbeziehung zwischen den beiden Tabellen hinzu.  

5.  Wählen Sie die Aktion **Beziehung** aus.  
6.  Füllen Sie auf der Seite **Datenexport - Berichtsarten** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Von Feldnr.**|Enthält die Nummer des Feld in der übergeordneten Tabelle. In diesem Szenario wird das Feld **Nummer** auf der Tabelle **Sachkonto** erstellt.|  
    |**Zu Feldnr.**|Enthält die Nummer des Feld in der übergeordneten Tabelle. In diesem Szenario das Feld **Sachkontonr.** der Tabelle **Sachposten**.|  

7.  Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-add-fields-from-the-gl-account-and-gl-entry-tables-to-the-data-export-record-source"></a>So fügen Sie Felder aus den Sachkonten und Sachpostentabellen der Datenexport-Datensatzquelle hinzu.  

1.  Auf der Seite **Datenexport - Datensatzherkunft** wählen Sie die Zeile unter der Zeile für die Tabelle **Sachkonto** und wählen dann die Aktion **Hinzufügen** aus.  
2.  Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.  

    |Feldnummer|Name des Felds|  
    |------------------|----------------|  
    |1|**Nr.**|  
    |2|**Name**|  
    |4|**Kontoart.**|  
    |31|**Saldo bis Datum**|  
    |32|**Bewegung**|  

3.  Auf der Seite **Datenexport - Datensatzherkunft** wählen Sie die Zeile unter der Zeile für die Tabelle **Sachkonto** und dann auf der Registerkarte **Felder** wählen Sie **Hinzufügen** aus.  
4.  Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.  

    |Feldnummer|Name des Felds|  
    |------------------|----------------|  
    |4|**Buchungsdatum**|  
    |5|**Belegart**|  
    |17|**Betrag**|  

Sean hat das Feld **Buchungsdatum** aus der Tabelle **Sachposten** hinzugefügt, da Cassie die Daten anhand dem Buchungsdatum gefiltert benötigt. Jetzt verwendet Stephan das Feld, um das Feld in der Tabelle **Sachposten** anzugeben, das verwendet wird, um den Zeitraum für den Datenexport zu berechnen.  

### <a name="to-add-a-period-filter-to-a-table-in-a-data-export-source"></a>Um einen Periodenfilter einer Tabelle in einer Datenexportquelle hinzuzufügen  

1.  Auf der Seite **Datenexport - Datensatzherkunft** wählen Sie die Zeile unter der Zeile für die Tabelle **Sachkonto** und dann auf der Registerkarte Felder wählen Sie **Periodenfeld-Nr.** aus.  
2.  Auf der Seite **Datenexport Felderübersicht** wählen Sie das Feld **Buchungsdatum**, und wählen Sie dann die Schaltfläche **OK** aus.  

    Die Seite **Datenexport-Felderübersicht** wird gefiltert, um nur die Datumsfelder anzuzeigen.  

Das bedeutet, dass, wenn Cassie die Daten exportiert und dem Startdatum und dem Enddatum der Periode anzeigt, welche die Auditoren möchten, dass der Export Posten enthält, in denen das Feld **Buchungsdatum** auf dem festgelegten Startdatum und Enddatum ist.  

Als Nächstes fügt Stephan die Tabellen **Debitor** und **Kreditor** hinzu.  

### <a name="to-add-the-customer-table"></a>Um die Kundentabelle hinzuzufügen  

1.  Füllen Sie auf der Seite **Datenexport - Berichtsquelle** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tabellennr.**|**18**|  
    |**Tabellenname exportieren**|**Debitor**|  
    |**Exportdateiname**|**Customer.txt**|  

2.  Im Bereich **Felder** in der Symbolleiste, wählen Sie **Hinzufügen** aus.  
3.  Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.  

    |Feldnummer|Name des Felds|  
    |------------------|----------------|  
    |1|**Nr.**|  
    |2|**Name**|  
    |21|**Debitorenbuchungsgruppe**|  
    |59|**Saldo (MW)**|  
    |61|**Bewegung (MW)**|  

4.  Wiederholen Sie die vorherigen zwei Schritte, um das Feld **Saldo (MW)** erneut hinzuzufügen.  
5.  Wählen Sie die Zeile für die erste Instanz des Felds **Saldo (MW)**, und dann im Feld **Behandlung von Datumsfiltern** wählen Sie **Startdatum** aus.  
6.  Wählen Sie die Zeile für die erste Instanz des Felds **Saldo (MW)**, und dann im Feld **Behandlung von Datumsfiltern** wählen Sie **Startdatum** aus.  
7.  Wählen Sie die Zeile für die erste Instanz des Felds **Nettoveränderung (LCY)**, und dann im Feld **Behandlung von Datumsfiltern** wählen Sie **Startdatum...Enddatum** aus.  

    In der folgenden Tabelle werden die Feldwerte für die Felder in der Tabelle **Debitor**.  

    |**Feldnr.**|**Feldname**|**Feldeigenschaft**|**Behandlung von Datumsfiltern**|**Feldnamen exportieren**|  
    |---------------------------------------|----------------------------------------|-----------------------------------------|-------------------------------------------------|------------------------------------------------|  
    |1|**Nr.**|**Normal**||**Nein**|  
    |2|**Name**|**Normal**||**Name**|  
    |21|**Debitorenbuchungsgruppe**|**Normal**||**Debitorenbuchungsgruppe**|  
    |59|**Saldo (MW)**|**FlowFields**|**..Startdatum**|**StartBalanceLCY**|  
    |59|**Saldo (MW)**|**FlowFields**|**..Enddatum**|**EndBalanceLCY**|  
    |61|**Bewegung (MW)**|**FlowFields**|**Anfangsdatum..Enddatum**|**NetChangeLCYPeriod**|  

    > [!TIP]  
    >  Um die Reihenfolge der Felder zu ändern, wählen Sie ein Feld, und dann in der Symbolleiste wählen Sie **Nach oben** oder **Nach unten** aus.  

Stephan hat die Tabelle **Debitor** der Datenexportquelle hinzugefügt. Nun fügt er die Tabelle **Kreditor** hinzu.  

### <a name="to-add-the-vendor-table"></a>Um die Kundentabelle hinzuzufügen  

1.  Füllen Sie auf der Seite **Datenexport - Berichtsquelle** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tabellennr.**|**23**|  
    |**Tabellenname exportieren**|**Kreditor**|  
    |**Exportdateiname**|**Vendor.txt**|  

2.  Befolgen Sie die Schritte der vorangehenden Vorgehensweise, um Felder aus der Tabelle **Kreditor** der Datenexportquelle hinzuzufügen.  

     In der folgenden Tabelle werden die Feldwerte für die Felder in der Tabelle **Debitor** beschrieben.  

    |**Feldnr.**|**Feldname**|**Feldeigenschaft**|**Behandlung von Datumsfiltern**|**Feldnamen exportieren**|  
    |---------------------------------------|----------------------------------------|-----------------------------------------|-------------------------------------------------|------------------------------------------------|  
    |1|**Nr.**|**Normal**||**Nein**|  
    |2|**Name**|**Normal**||**Name**|  
    |21|**Kreditorenbuchungsgruppe**|**Normal**||**Kreditorenbuchungsgruppe**|  
    |59|**Saldo (MW)**|**FlowFields**|**..Startdatum**|**StartBalanceLCY**|  
    |59|**Saldo (MW)**|**FlowFields**|**..Enddatum**|**EndBalanceLCY**|  
    |61|**Bewegung (MW)**|**FlowFields**|**Anfangsdatum..Enddatum**|**NetChangeLCYPeriod**|  

Sean hat die Einrichtung fast abgeschlossen, jedoch möchte er überprüfen, ob die Datenexportquelle die technischen Anforderungen des Prüftools erfüllt.  

### <a name="to-validate-the-data-export-source"></a>Um die Datenexportquelle zu überprüfen  

Wählen Sie die Aktion **Überprüfen** aus.  

Sean hat nun die Einrichtung des Datenexports basierend auf den Anforderungen von Cassie abgeschlossen. Er benachrichtigt sie, sodass sie mit dem Exportieren von Daten für die Steuerprüfer beginnen kann.  

## <a name="exporting-data-for-the-tax-auditors"></a>Exportieren von Daten für die Steuerprüfer.  
Cassie möchte Daten exportieren, die sie anschließend den Steuerprüfern senden kann.  

### <a name="to-export-data"></a>Daten exportieren  

1.  Wählen Sie das Symbol ![Suche nach Seite oder Bericht](../../media/ui-search/search_small.png "Symbol „Suche nach Seite oder Bericht“") aus, geben Sie **Geschäftsdaten exportieren** ein und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie auf der Seite **Geschäftsdaten exportieren** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Startdatum**|Das Startdatum. Schritte in diesem Szenario **01-01-2018**.|  
    |**Enddatum**|Das Enddatum. Schritte in diesem Szenario **03-31-2018**.|  

3.  Füllen Sie im Fenster **Datenexportberichtsdefinitionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Datenexportcode**|In diesem Szenario **AUDIT-Q113**.|  
    |**Datenexport - Datens.-Typcode**|In diesem Szenario **GLCUSTVEND**.|  

4.  Um Daten zu exportieren, wählen Sie die Schaltfläche **OK**, um den Export zu starten.  

Wenn der Export abgeschlossen ist, wird Cassie benachrichtigt. Nun kann sie die exportierten Dateien den Steuerprüfern senden. Zuerst überprüft sie die Dateien im Ordner C: Exports auf ihrem Computer. Es gibt eine Datei für jede Tabelle, und die Dateien haben die Namen, die Sean in der Datenexportquelle angegeben hat. Es gibt auch eine INDEX.XML-Datei, die die Struktur des Datenexports mit den Namen der Tabellen und Felder beschreibt, die Sean angegeben hat.  

## <a name="next-steps"></a>Nächste Schritte  
Wenn die Steuerprüfer Cassies Dateien in ihre Software importieren, können sie die Daten lesen, die sie exportiert hat. Wenn die Auditoren eine neue Version des gleichen Datenexports benötigen, kann Cassie den Export erneut ausführen.  

Wenn die Steuerprüfer das nächste Mal neue Daten anfordern, können Cassie und Sean zusammenarbeiten, um einen neuen Datenexport zu erstellen.  

## <a name="see-also"></a>Siehe auch  
 [Prozess für Digital-Überwachung](process-for-digital-audits.md)   
 [Wie Sie Daten für eine Digital-Überwachung einrichten](how-to-set-up-data-exports-for-gdpdu.md)   
 [Wie Sie Daten für eine Digital-Überwachung exportieren](how-to-export-data-for-a-digital-audit.md)
