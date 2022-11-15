---
title: Definieren Sie, wie die Daten elektronisch ausgetauscht werden
description: Definieren Sie, wie Business Central Daten mit externen Dateien wie elektronischen Belegen, Bankdaten, Artikelkatalogen und mehr austauscht.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.search.form: 1210, 1211, 1213, 1214, 1215, 1216, 1217
ms.date: 11/03/2022
ms.author: bholtorf
ms.openlocfilehash: 324fa2e1576deb3f9cb4b082f065218d1576fd78
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9744869"
---
# <a name="set-up-data-exchange-definitions"></a>Richten Sie Datenaustauschdefinitionen ein.

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] festlegen, um Daten in bestimmten Tabellen mit Daten in externen Dateien auszutauschen. Zum Beispiel, um elektronische Belege zu senden und zu empfangen, Bankdaten oder andere Daten wie Gehaltsabrechnungen und Artikelkataloge zu importieren und zu exportieren. Erfahren Sie mehr unter [Elektronischer Datenaustausch](across-data-exchange.md).  

Um eine Datenaustauschdefinition für eine Datendatei oder einen Datenstrom zu erstellen, können Sie das zugehörige XML-Schema verwenden, um zu definieren, welche Datenelemente auf der Registerkarte **Spaltendefinitionen** enthalten sein sollen. Weitere Informationen finden Sie unter Schritt 6 im Abschnitt [Die Formatierung der Zeilen und Spalten in der Datei beschreiben](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Mehr dazu erfahren Sie unter [Verwenden Sie XML-Schemata zur Vorbereitung von Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Normalerweise legen Sie die Datenaustauschdefinitionen auf der Seite **Datenaustauschdefinition** fest. Für die Aktualisierung von Wechselkursen ist es jedoch schneller, einen Währungsumtausch-Service zu verwenden. Erfahren Sie mehr unter [Update Currency Exchange Rates](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Wenn die Datei, die konvertiert wird, im XML-Format vorliegt, sollte der Begriff *„Spalte“* in diesem Artikel als *„XML-Element, das Daten enthält“* interpretiert werden.  

Dieser Artikel enthält die folgenden Verfahren:  

* Erstellen Sie eine Datenaustauschdefinition.
* Exportieren Sie eine Datenaustauschdefinition als XML-Datei zur Verwendung durch andere.
* Importieren Sie eine XML-Datei für eine bestehende Datenaustauschdefinition.

## <a name="create-a-data-exchange-definition"></a>Erstellen Sie eine Datenaustauschdefinition

Das Erstellen einer Datenaustauschdefinition beinhaltet zwei Aufgaben:  

1. Auf der Seite **Datenaustauschdefinition** beschreiben Sie die Formatierung aus Zeilen und Spalten in der Datei. Erfahren Sie mehr im Abschnitt [Sie beschreiben die Formatierung von Zeilen und Spalten in der Datei](#formatlinescolumns).  
2. Auf der Seite **Wechselkurszuordnungs** ordnen Sie Spalten in der Datendatei Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zu. Erfahren Sie mehr im Abschnitt [So ordnen Sie Spalten in der Datendatei den Feldern im Abschnitt [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields) zu.  

### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name=formatlinescolumns></a>Um die Formatierung von Zeilen und Spalten in der Datei zu beschreiben

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Datenaustauschdefinitionen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Im Inforegister **Allgemein** beschreiben Sie die Datenaustauschdefinition und den Datentyp, indem Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Definition|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geben Sie einen Code zur Identifizierung der Datenaustauschdefinition ein.|  
    |**Name**|Geben Sie einen Namen für die Datenaustauschdefinition ein.|  
    |**Dateityp**|Geben Sie an, für welche Art von Datei die Datenaustauschdefinition verwendet wird. Sie können zwischen vier Dateitypen auswählen:<br /><br /> -   **XML**: Geschichtete Zeichenfolgen des Inhalts und des Aufschlags, die von Tags, die die Funktion angeben, umgeben sind.<br />-   **Variabler Text**: Die Datensätze haben eine variable Länge und sind durch ein Zeichen, wie z.B. ein Komma oder semi\-colon oder einen Doppelpunkt, getrennt. Auch bekannt als *begrenzte Datei*.<br />-   **Fester Text**: Die Datensätze haben die gleiche Länge und stehen in einer separaten Zeile, auch bekannt als *Datei mit fester Breite*.<br />- **Json**: Geschichtete Zeichenfolgen des Inhalts in JavaScript.|  
    |**Typ**|Geben Sie an, für welche Art von Geschäftstätigkeit die Datenaustauschdefinition verwendet wird, zum Beispiel **Zahlungsexport**.|  
    |**Codeunit zur Datenverarbeitung**|Geben Sie die Codeunit an, die Daten in und aus Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] überträgt.|  
    |**Überprüfungs-Codeunit**|Geben Sie die Codeunit an, die verwendet wird, um Daten gegen vordefinierte Geschäftsregeln zu validieren.|  
    |**Lese-/Schreibe-Codeunit**|Geben Sie die Codeunit an, die importierte Daten vor der Zuordnung und exportierte Daten nach der Zuordnung verarbeitet.|  
    |**Lesen/Schreiben von XMLport**|Geben Sie die XMLport an, durch die eine importierte Datendatei oder ein Dienst vor der Zuordnung eintritt und durch die die exportierten Daten nach der Zuordnung wieder austreten, wenn sie in eine Datendatei oder einen Dienst geschrieben werden.|  
    |**Codeunit zur externen Datenverarbeitung**|Geben Sie die Codeunit an, die externe Daten in und aus dem Daten-Exchange-Framework überträgt.|  
    |**Benutzerfeedback-Codeunit**|Geben Sie die Codeunit an, die nach dem Zuordnen verschiedene Bereinigungen ausführt, wie das Markieren von exportierten Zeilen und das Löschen temporärer Datensätze.|  
    |**Dateiverschlüsselung**|Geben Sie die Codierung der Datei an. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Spaltentrennzeichen**|Geben Sie an, wie Spalten in der Datendatei getrennt werden, wenn die Datei den Typ **Variabler Text** hat.|  
    |**Kopfzeilen**|Geben Sie an, wie viele Kopfzeilen in der Datei vorhanden sind.<br /><br /> Diese Einstellung sorgt dafür, dass die Kopfdaten nicht importiert werden. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Kopfzeilentag**|Wenn eine Kopfzeile an verschiedenen Positionen in der Datei vorhanden ist, geben Sie den Text der ersten Spalte in der Kopfzeile ein.<br /><br /> Mit dieser Option stellen Sie sicher, dass die Kopfdaten nicht importiert werden. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Fußzeilentag**|Wenn eine Fußzeile an verschiedenen Positionen in der Datei vorhanden ist, geben Sie den Text der ersten Spalte in der Fußzeile ein.<br /><br /> Mit dieser Option stellen Sie sicher, dass die Fußzeilendaten nicht importiert werden. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  

   > [!TIP]
   > Um zu sehen, welche Codeunits Microsoft in vorhandenen Definitionen im Standardprodukt verwendet, sehen Sie sich die drei **Codeunit**-Felder auf der Seite **Feldzuordnung** unter dem **Allgemein** Inforegister für jede Definition an.  

4. Im Inforegister **Zeilendefinitionen** beschreiben Sie das Formatieren der Zeilen in der Datendatei, indem Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

    > [!NOTE]  
    > Für den Import von Bankauszügen erstellen Sie nur eine Zeile für das einzelne Format der Bankkontoauszugsdatei, die Sie importieren möchten.  
    >
    > Für den Export von Zahlungen können Sie eine Zeile für jede Zahlungsart erstellen, die Sie exportieren möchten. In diesem Fall zeigt das Inforegister **Spaltendefinitionen** verschiedene Spalten für jede Zahlungsart an.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Zeilentyp**|Gibt die Art der Zeile in der Datei an.|  
    |**Code**|Geben Sie einen Code zur Identifizierung der Zeile in der Datei ein.|  
    |**Name**|Geben Sie einen Namen ein, der die Zeile in der Datei beschreibt.|  
    |**Anzahl Spalten**|Geben Sie an, wie viele Spalten die Zeile in der Datendatei hat. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Datenzeilen-Tag**|Geben Sie die Position im entsprechenden XML-Schema des Elements an, die den Hauptposten der Datendatei darstellt. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Namespace**|Geben Sie den Namespace an, der in der Datei erwartet wird, um die Namespaceprüfung zu aktivieren. Sie können dieses Kontrollkästchen leer lassen, wenn Sie Namespaceprüfung nicht aktivieren möchten.|  
    |**Übergeordneter Code**|Geben Sie den übergeordneten Code der Zeile an, wie er im Feld **Code** angezeigt wird, wenn die Einrichtung des Datenaustauschs für Dateien mit übergeordneten und untergeordneten Elementen erfolgt, z.B. für einen Dokumentenkopf und Zeilen.

5. Wiederholen Sie Schritt 4, um eine Zeile für jede Dateidatenart zu erstellen, die Sie exportieren möchten.  

     Beschreiben Sie dann das Formatieren der Spalten in der Datendatei, indem Sie die Felder im Inforegister **Spaltendefinitionen** wie in der unten stehenden Tabelle beschrieben ausfüllen. Sie können die Strukturdatei, z.B. eine .xsd-Datei, für die Datendatei verwenden, um das Inforegister mit den entsprechenden Elementen vorauszufüllen. Mehr dazu erfahren Sie unter [Verwenden Sie XML-Schemata zur Vorbereitung von Datenaustauschdefinitionen](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Wählen Sie auf dem Inforegister **Spaltendefinitionen** die Aktion **Dateistruktur abrufen**.  
7. Wählen Sie auf der Seite **Dateistruktur abrufen** die entsprechende Strukturdatei und wählen Sie dann **OK**. Die Zeilen im Inforegister **Spaltendefinitionen** werden entsprechend der Struktur der Datendatei ausgefüllt.  
8. Füllen Sie im Inforegister **Spaltendefinitionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus oder bearbeiten Sie sie.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Spaltennr.**|Geben Sie die Nummer an, die die Position der Spalte in der Zeile der Datei angibt.<br /><br /> Für XML-Dateien geben Sie die Nummer an, die den Elementtyp in der Datei widergespiegelt, die die Daten enthält.|  
    |**Name**|Geben Sie den Namen der Spalte an.<br /><br /> Für XML-Dateien geben Sie die Markierung an, die die auszutauschenden Daten markiert.|  
    |**Datentyp**|Geben Sie an, ob die auszutauschenden Daten den Typ **Text**, **Datum** oder **Dezimal** haben.|  
    |**Datenformat**|Geben Sie das Format der Daten an, sofern vorhanden. Beispielsweise **MM-tt-jjjj**, wenn der Datentyp **Datum** ist. **Hinweis:** Für den Export geben Sie das Datenformat gemäß [!INCLUDE[prod_short](includes/prod_short.md)] an. Für den Import geben Sie das Datenformat entsprechend .Net Framework an. Weitere Informationen finden Sie unter [Standard Datums- und Zeitformatstrings](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Datenformatierungskultur**|Geben Sie das regionale Datenformat an, falls vorhanden. Beispielsweise **en-US**, wenn der Datentyp **Dezimal** ist, um sicherzustellen, dass ein Komma als Dezimaltrennzeichen verwendet wird, entsprechend dem US-Format. Weitere Informationen finden Sie unter [Standard Datums- und Zeitformatstrings](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Länge**|Geben Sie die Länge der Zeile mit fester Breite an, die diese Spalte enthält, wenn die Datendatei den Typ **Fester Text** hat.|  
    |**Beschreibung**|Gibt eine Beschreibung der Spalte zu Informationszwecken an.|  
    |**Pfad**|Geben Sie die Position des Elements im zugehörigen XML-Schema an.|  
    |**Kennzeichen mit negativem Zeichen**|Geben Sie den Wert ein, der in der Datendatei verwendet wird, um negative Beträge in Datendateien zu identifizieren, die keine negativen Vorzeichen enthalten können. Diese Identifikationsnummer wird verwendet, um die identifizierten Beträge während des Imports auf negative Vorzeichen zurückzusetzen. **Hinweis:** Dieses Feld ist nur für den Import relevant.|  
    |**Konstanten**|Geben Sie alle Daten an, die Sie in dieser Spalte exportieren möchten, wie etwa zusätzliche Informationen über die Zahlungsart. **Hinweis:** Dieses Feld ist nur für den Export relevant.|  
    |**Textauffüllung erforderlich**|Geben Sie an, dass die Daten Textauffüllungen enthalten müssen.|  
    |**Auffüllzeichen**|Geben Sie das Zeichen für die Textauffüllung an.|  
    |**Ausrichtung**|Geben Sie an, ob die Spaltenausrichtung links oder rechts ist.|  

9. Wiederholen Sie Schritt 8 für jede Spalte oder jedes XML-Element in der Datendatei, die/das Daten hat, die Sie mit [!INCLUDE[prod_short](includes/prod_short.md)] austauschen möchten.  

Der nächste Schritt bei der Erstellung einer Datenaustauschdefinition besteht darin, zu entscheiden, welche Spalten oder XML-Elemente welchen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden sollen.  

> [!NOTE]  
> Die spezielle Zuordnung hängt vom Geschäftszweck der Datendatei ab, die ausgetauscht werden soll, sowie von lokalen Variationen. Selbst der SEPA-Bankstandard verfügt über lokale Variationen. [!INCLUDE[prod_short](includes/prod_short.md)] Stützimport von SEPA Bankkontoauszug CAMT archiviert Out\-of\-the\-Box. Dies wird durch den **SEPA CAMT**-Datenaustausch-Definitionsdatensatzcode auf der Seite **Datenaustauschdefintion** angezeigt. Informationen über die bestimmte Feldzuordnung dieser SEPA CAMT Unterstützung, siehe. [Feld-Zuordnung, wenn sie SEPA CAMT Dateien importieren](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name="to-map-columns-in-the-data-file-to-fields-in-prod_short"></a><a name=mapfields></a>Zur Zuordnung von Spalten in der Datendatei zu Feldern in [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Manchmal sind die Werte in den Feldern, die Sie zuordnen möchten, unterschiedlich. In einer App für Unternehmen lautet der Sprachcode für die Vereinigten Staaten zum Beispiel „U.S.“, in einer anderen jedoch „US.“ Das heißt, Sie müssen den Wert beim Datenaustausch umwandeln. Dies geschieht durch Transformationsregeln, die Sie für die Felder definieren. Erfahren Sie mehr unter [Transformationsregeln](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Ab der Veröffentlichungswelle 2 2022 können Sie auch nach einem beliebigen Feld gruppieren, den Schlüsselindex zum Sortieren der Ergebnisse verwenden und die neuen Transformationstypen **Rundung** und **Feld Nachschlagefeld** verwenden.

1. Wählen Sie im Inforegister **Zeilendefinitionen** die Zeile aus, für die Sie Spalten zu Feldern zuordnen möchten, und wählen Sie dann **Feldzuordnung**. Die Seite **Datenaustauschzuordnung** wird geöffnet.  
2. Spezifizieren Sie im Inforegister **Allgemein** die Zuordnungen, indem Sie die Felder gemäß der Beschreibung in der folgenden Tabelle ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Tabellen-ID**|Geben Sie die Tabelle an, die die Felder enthält, zu oder aus denen Daten entsprechend der Zuordnung ausgetauscht werden.|  
    |**Als Zwischentabelle verwenden**|Gibt an, dass die im Feld **Tabellen-ID** ausgewählte Tabelle eine Zwischentabelle ist, in der die importierten Daten vor der Zuordnung zur Zieltabelle gespeichert werden.<br /><br /> In der Regel verwenden Sie eine vorläufige Tabelle, wenn die Datenaustauschdefinition verwendet wird, um elektronische Belege zu importieren und umwandeln, wie Kreditorenrechnungen in Einkaufsrechnungen in [!INCLUDE[prod_short](includes/prod_short.md)]. Erfahren Sie mehr unter [Elektronischer Datenaustausch](across-data-exchange.md).|  
    |**Name**|Geben Sie einen Namen für den Zuordnungssetup ein.|  
    |**Schlüsselindex**|Geben Sie den Schlüsselindex an, um die Quelldatensätze vor dem Exportieren zu sortieren.|
    |**Vorabzuordnungs-Codeunit**|Geben Sie die Codeunit an, die die Zuordnung zwischen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] und externen Daten vorbereitet.|  
    |**Zuordnungs-Codeunit**|Geben Sie die Codeunit an, die verwendet wird, um die angegebenen Spalten oder XML-Datenelemente den Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zuzuordnen.|  
    |**Codeunit für die Zuordnung im Nachhinein**|Geben Sie die Codeunit an, die die Zuordnung zwischen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] und externen Daten vervollständigt. **Hinweis**: Bei Verwendung der Funktion der AMC Banking 365 Fundamentals-Erweiterung wandelt codeunit exportierte Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] in ein für den Export bereitstehendes generisches Format um. Für den Import konvertiert die Codeunit externe Daten zu einem für den Import zu [!INCLUDE[prod_short](includes/prod_short.md)] geeigneten Format.|
3. Geben Sie auf der Registerkarte **Feldzuordnung** an, welche Spalten welchen Feldern in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden sollen, indem Sie die Felder wie in den folgenden Tabellen beschrieben ausfüllen, je nachdem, ob das Feld **Als Zwischentabelle verwenden** aktiviert wurde oder nicht.  
   * Wenn das Feld **Als Zwischentabelle verwenden** deaktiviert ist:

     |Feld|Description|  
     |--------------------------------- |---------------------------------------|  
     |**Spaltennr.**|Geben Sie an, für welche Spalte in der Datendatei Sie eine Zuordnung definieren möchten.<br /><br /> Sie können nur Spalten auswählen, die auf dem Inforegister **Spaltendefinitionen** auf der Seite **Datenaustauschdefinitionen** durch Zeilen dargestellt werden.|
     |**Spaltenbeschriftung**|Geben Sie die Beschriftung der Spalte in der externen Datei an, die dem Feld im Feld **Zieltabellen-ID** zugeordnet wird, wenn Sie eine Zwischentabelle für den Datenimport verwenden.|
     |**Feld-ID**|Geben Sie an, welchem Feld die Spalte im Feld **Spaltennr.** zugeordnet ist. Feldkarten zu.<br /><br /> Sie können nur aus Feldern auswählen, die in der Tabelle existieren, die Sie im Feld **Tabellen-ID** auf der Registerkarte **Allgemein** angegeben haben.|
     |**Feldbeschriftung**|Geben Sie die Beschriftung des Feldes in der externen Datei an, das dem Feld im Feld **Zieltabellen-ID** zugeordnet ist, wenn Sie eine Zwischentabelle für den Datenimport verwenden.|
     |**Optional**|Geben Sie an, ob die Zuordnung übersprungen werden soll, wenn das Feld leer ist. Wenn Sie diese Option nicht wählen, wird ein Exportfehler auftreten, wenn das Feld leer ist.|  
     |**Transformations-Regel**|Geben Sie die Regel an, die importierten Text in einen unterstützten Wert umwandelt, bevor er einem bestimmten Feld zugeordnet werden kann. Wenn Sie in diesem Feld einen Wert auswählen, wird derselbe Wert in das Feld **Transformationsregel** im Feld **Datenexch. Feld Zuordnung Buf.** Tabelle und umgekehrt. Im nächsten Abschnitt finden Sie weitere Informationen zu den verfügbaren Transformationsregeln, die angewendet werden können.|
     |**Wert überschreiben**|Geben Sie an, dass der aktuelle Wert durch einen neuen Wert überschrieben werden soll.|
     |**Priorität**|Geben Sie die Reihenfolge an, in der die Zuordnungen der Felder verarbeitet werden müssen. Die Zuordnung des Feldes mit der höchsten Prioritätsnummer wird zuerst verarbeitet.|
     |**Multiplikator**|Geben Sie einen Multiplikator an, der auf numerische Daten, einschließlich negativer Werte, angewendet wird.|

   * Wenn die Option **Als Zwischentabelle verwenden** aktiviert ist:

     |Feld|Description|  
     |---------------------------------|---------------------------------------|  
     |**Spaltennr.**|Geben Sie an, für welche Spalte in der Datendatei Sie eine Zuordnung definieren möchten.<br /><br /> Sie können nur Spalten auswählen, die auf dem Inforegister **Spaltendefinitionen** auf der Seite **Datenaustauschdefinitionen** durch Zeilen dargestellt werden.|
     |**Spaltenbeschriftung**|Geben Sie die Beschriftung der Spalte in der externen Datei an, die dem Feld im Feld **Zieltabellen-ID** zugeordnet wird, wenn Sie eine Zwischentabelle für den Datenimport verwenden.|
     |**Zieltabellen-ID**|Gibt die Tabelle an, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|
     |**Tabellenüberschrift**|Gibt den Namen der Tabelle im Feld **Zieltabellen-ID** an, die die Tabelle ist, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|
     |**Zielfeld-ID**|Gibt das Feld in der Zieltabelle an, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|
     |**Feldbeschriftung**|Gibt den Namen des Felds in der Zieltabelle an, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|
     |**Nur validieren**|Legen Sie fest, dass die Zuordnung von Elementen zu Feldern nicht zur Konvertierung von Daten, sondern nur zur Validierung von Daten verwendet wird.|
     |**Transformations-Regel**|Geben Sie die Regel an, die importierten Text in einen unterstützten Wert umwandelt, bevor er einem bestimmten Feld zugeordnet werden kann. Wenn Sie in diesem Feld einen Wert auswählen, wird derselbe Wert in das Feld **Transformationsregel** im Feld **Datenexch. Feld Zuordnung Buf.** Tabelle und umgekehrt. Im nächsten Abschnitt finden Sie weitere Informationen zu den verfügbaren Transformationsregeln, die angewendet werden können.|
     |**Priorität**|Geben Sie die Reihenfolge an, in der die Zuordnungen der Felder verarbeitet werden müssen. Die Zuordnung des Feldes mit der höchsten Prioritätsnummer wird zuerst verarbeitet.|

4. Geben Sie im Inforegister **Feldgruppierung** Regeln an, die Sie zum Gruppieren Ihrer Felder verwenden möchten, wenn Sie die Datei erstellen, indem Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

     |Feld|Description|  
     |--------------------------------- |---------------------------------------|  
     |**Feld-ID**|Geben Sie die Nummer des Felds in der externen Datei an, das für die Gruppierung verwendet wird und dieses Feld muss nach Benutzer festgelegt werden.|
     |**Feldbeschriftung**|Geben Sie die Beschriftung des Felds in der externen Datei an, das für die Gruppierung verwendet wird.|

## <a name="transformation-rules"></a>Transformationsregeln

Wenn die Werte in den Feldern, die Sie zuordnen, unterschiedlich sind, müssen Sie Transformationsregeln für Datenaustauschdefinitionen verwenden, um sie anzugleichen. Sie definieren Transformationsregeln für Datenaustauschdefinitionen, indem Sie eine vorhandene Definition öffnen oder eine neue Definition erstellen, dann auf dem Inforegister **Zeilendefinitionen** die Option **Verwalten**, und dann **Feldzuordnung** wählen. Vordefinierte Regeln werden bereitgestellt, aber Sie können auch eigene Regeln erstellen. In der folgenden Tabelle werden die Transformationstypen beschrieben, die Sie ausführen können.

|Option|Beschreibung|
|---------|---------|
|**Großbuchstaben**|Großschreibung aller Buchstaben.|
|**Kleinbuchstaben**|Kleinschreibung aller Buchstaben.|
|**Titelschreibung**|Großschreibung des ersten Buchstabens jedes Wortes.|
|**Kürzen**|Leerzeichen vor und nach dem Wert entfernen.|
|**Unterzeichenfolge**|Transformation eines bestimmten Teilwerts. Um anzugeben, wo die Umwandlung gestartet werden soll, wählen Sie entweder eine **Startposition** oder einen **Starttext**. Die Startposition ist eine Zahl, die das erste umzuwandelnde Zeichen darstellt. Der Anfangstext ist der Buchstabe unmittelbar vor dem zu ersetzenden Buchstaben. Wenn Sie mit dem ersten Buchstaben des Werts beginnen möchten, verwenden Sie stattdessen eine Startposition. Um festzulegen, wo die Umwandlung gestoppt werden soll, wählen Sie entweder **Länge**, d.h. die Anzahl der zu ersetzenden Zeichen, oder **Endtext**, d.h. das Zeichen, das unmittelbar nach dem letzten umzuwandelnden Zeichen steht.|
|**Ersetzen**|Suchen Sie einen Wert und ersetzen Sie ihn durch einen anderen. Diese Umwandlung ist nützlich, um einfache Werte zu ersetzen, z.B. ein bestimmtes Wort.|
|**Regulärer Ausdruck – Ersetzen**|Verwenden Sie einen regulären Ausdruck als Teil einer Such- und Ersetzungsoperation. Diese Umwandlung ist nützlich, um mehrere oder komplexere Werte zu ersetzen.|
|**Entfernen von nicht alphanumerischen Zeichen**|Löschen Sie Zeichen, die keine Buchstaben oder Zahlen sind, z. B. Symbole oder Sonderzeichen.|
|**Datumsformatierung**|Geben Sie an, wie Datumsangaben angezeigt werden sollen. Beispielsweise können Sie TT-MM-JJJJ in JJJJ-MM-TT umwandeln.|
|**Dezimalformatierung**|Definieren Sie Regeln für die Dezimalstelle und die Rundungsgenauigkeit.|
|**Regulärer Ausdruck - Übereinstimmen**|Verwenden Sie einen regulären Ausdruck, um einen oder mehrere Werte zu finden. Diese Regel ist vergleichbar mit den Optionen **Substring** und **Regelmäßiger Ausdruck - Ersetzen**.|
|**Benutzerdefiniert**|Diese Transformationsregel ist eine erweiterte Option, die die Unterstützung eines Entwicklers erfordert. Sie aktiviert ein Integrationsereignis, das Sie abonnieren können, wenn Sie Ihren eigenen Transformationscode verwenden möchten. Wenn Sie ein Entwickler sind und diese Option verwenden möchten, lesen Sie den folgenden Abschnitt.|
|**Datum/Uhrzeit-Formatierung**|Legen Sie fest, wie das aktuelle Datum und die Tageszeit angezeigt werden sollen.|
|**Feldsuche**|Verwenden Sie Felder aus verschiedenen Tabellen. Um sie verwenden zu können, müssen Sie einige Regeln befolgen. Verwenden Sie zunächst **Tabellen-ID**, um die ID der Tabelle anzugeben, die den Datensatz für die Feldsuche enthält. Geben Sie dann im Feld **Quellfeld-ID** die ID des Felds an, das den Datensatz für die Feldsuche enthält. Geben Sie schließlich im Feld **Zielfeld-ID** die ID des Felds an, um den Datensatz für die Feldsuche zu finden. Verwenden Sie optional das Feld **Feldsuchregel**, um den Typ der Feldsuche anzugeben. Für das **Ziel**-Feld wird der Wert aus der **Zielfeld-ID** verwendet, auch wenn sie leer ist. Für das Feld **Ursprung, wenn Ziel leer ist** wird der ursprüngliche Wert verwendet, wenn das Ziel leer ist.|
|**Runden**|Runden Sie den Wert in diesem Feld nach einigen zusätzlichen Regeln. Geben Sie zunächst im Feld **Präzision** eine Rundungsgenauigkeit an. Dann im Feld **Richtung** geben Sie die Rundungsrichtung an.|

> [!NOTE]  
> Erfahren Sie mehr über die Formatierung von Datum und Uhrzeit unter [Standard-Strings für die Formatierung von Datum und Uhrzeit](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### <a name="tip-for-developers-example-of-the-custom-option"></a>Tipp für Entwickler: Beispiel für die angepasste Option

Das folgende Beispiel zeigt, wie Sie Ihren eigenen Transformationscode implementieren.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Nachdem Sie Ihre Regeln definiert haben, können Sie sie testen. Geben Sie im Inforegister **Test** ein Beispiel für einen Wert ein, den Sie umwandeln möchten, und überprüfen Sie dann die Ergebnisse, indem Sie **Aktualisieren** wählen.

## <a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Exportieren einer Datenaustauschdefinition als XML-Datei zur Verwendung durch andere

Wenn Sie die Datenaustauschdefinition für eine bestimmte Datendatei erstellt haben, können Sie die Datenaustauschdefinition als XML-Datei exportieren, die Sie importieren können. Diese Aufgabe wird in der folgenden Prozedur beschrieben.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Datenaustauschdefinitionen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Datenaustauschdefinition aus, die Sie exportieren möchten.  
3. Wählen Sie die **Datenaustauschdefinition exportieren** Aktion aus.  
4. Speichern Sie die XML-Datei, die die Datenaustauschdefinition darstellt, an einem entsprechenden Ort.  

    Wenn eine Datenaustauschdefinition bereits erstellt wurde, müssen Sie nur die XML-Datei in das Daten-Exchange-Framework importieren. Diese Aufgabe wird in der folgenden Prozedur beschrieben.  

## <a name="import-an-existing-data-exchange-definition"></a>Importieren einer bestehenden Datenaustauschdefinition

1. Speichern Sie die XML-Datei, die die Datenaustauschdefinition darstellt, an einem entsprechenden Ort.  
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Datenaustauschdefinitionen** ein und wählen Sie dann den entsprechenden Link.  
3. Wählen Sie die **Datenaustauschdefinition importieren** Aktion aus.  
4. Wählen Sie die Datei aus, die Sie in Schritt 1 gespeichert haben.  

## <a name="see-also"></a>Siehe auch

[Datenaustausch einrichten](across-set-up-data-exchange.md)  
[Einrichten von Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder per SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
