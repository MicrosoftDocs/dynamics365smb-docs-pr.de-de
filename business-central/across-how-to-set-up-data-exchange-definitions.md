---
title: Definieren, wie Daten elektronisch übermittelt | Microsoft Docs
description: Nutzen Sie den OCR-Dienst zur Umwandlung von PDF- oder Bilddateien in elektronische Belege konvertiert werden können.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 02/11/2020
ms.author: sgroespe
ms.openlocfilehash: dfd06fce9aab0de6afb725ab4625138b62305a1a
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076782"
---
# <a name="set-up-data-exchange-definitions"></a>Richten Sie Datenaustauschdefinitionen ein.
Sie können [!INCLUDE[d365fin](includes/d365fin_md.md)] so einrichten, dass Daten in bestimmten Tabelle mit Daten in externen Dateien ausgetauscht werden, zum Beispiel zum Senden und Empfangen elektronischer Belege oder zum Importieren und Exportieren von Bankdaten und anderen Daten, wie Lohnabrechnung, Währungswechselkursen und Artikelkatalogen. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).  

Zur Vorbereitung für das Erstellen einer Datenaustauschdefinition für eine Datendatei oder einen Datenstrom können Sie das zugehörige XML-Schema verwenden, um zu definieren, welche Datenelemente im Inforegister **Spaltendefinitionen** berücksichtigt werden sollen. Weitere Informationen finden Sie unter Schritt 6 im Abschnitt [Die Formatierung der Zeilen und Spalten in der Datei beschreiben](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Weitere Informationen finden Sie im Thema [Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinition](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md) in der Anwendungshilfe.  

Normalerweise richten Sie Datenaustauschdefinitionen auf der Seite **Datenaustauschdefiniton** ein. Wenn Sie jedoch eine Datenaustauschdefinition für den Service zum Aktualisieren von Wechselkursen einrichten, beginnen Sie den Vorgang auf der vereinfachten Seite **Wechselkursaktualisierung Karte einrichten** .  

> [!NOTE]  
>  Wenn die konvertierte Datei eine XML-Datei ist, sollte der Begriff *„Spalte“* in diesem Thema als *„XML-Element, das Daten enthält“* interpretiert werden.  

In diesem Thema werden die folgenden Prozeduren beschrieben:  

* Eine Datenaustauschdefinition generieren  
* Eine Datenaustauschdefinition als XML-Datei zur Verwendung durch andere exportieren  
* So importieren Sie eine XML-Datei für eine bestehende Datenaustauschdefinition  

## <a name="to-create-a-data-exchange-definition"></a>Eine Datenaustauschdefinition generieren  
Das Erstellen einer Datenaustauschdefinition beinhaltet zwei Aufgaben:  

1. Auf der Seite **Datenaustauschdefinition** beschreiben Sie die Formatierung aus Zeilen und Spalten in der Datei.  
2. Auf der Seite **Wechselkurszuordnungs** ordnen Sie Spalten in der Datendatei Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu.  

Dies wird in den folgenden Verfahren beschrieben.  

> [!TIP]
> Um zu sehen welche Codeunits Microsoft in bestehenden Definitionen im Standardprodukt verwendet, überprüfen Sie die drei **Codeunit**-Felder in der Kopfzeile der Seite **Feldzuordnung** für jede Definition.

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Die Formatierung der Zeilen und Spalten in der Datei beschreiben  
1. Geben Sie im Feld **Suchen** einen Wert für **Datenaustauschdefinitionen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Im Inforegister **Allgemein** beschreiben Sie die Datenaustauschdefinition und den Datentyp, indem Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Definition|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geben Sie einen Code zur Identifizierung der Datenaustauschdefinition ein.|  
    |**Name**|Geben Sie einen Namen für die Datenaustauschdefinition ein.|  
    |**Dateityp**|Geben Sie an, für welche Art von Datei die Datenaustauschdefinition verwendet wird. Sie können zwischen vier Dateitypen auswählen:<br /><br /> -   **XML**: Geschichtete Zeichenfolgen des Inhalts und des Aufschlags, die von Tags, die die Funktion angeben, umgeben sind.<br />-   **Variabler Text**: Datensätze haben eine variable Länge und sind durch ein Zeichen, z. B. ein Komma oder \-Semikolon geteilt. Auch bekannt als *Datei mit Trennzeichen*.<br />-   **Fester Text**: Datensätze haben dieselbe Länge, unter Verwendung von Auffüllzeichen, und mit jedem Datensatz auf einer separaten Zeile. Auch bekannt als *Datei mit fester Breite*.<br />- **Json**: Geschichtete Zeichenfolgen des Inhalts in JavaScript.|  
    |**Typ**|Geben Sie an, für welche Art von Geschäftstätigkeit die Datenaustauschdefinition verwendet wird, zum Beispiel **Zahlungsexport**.|  
    |**Codeunit zur Datenverarbeitung**|Geben Sie die Codeunit an, die Daten in und aus Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] überträgt.|  
    |**Überprüfungs-Codeunit**|Geben Sie die Codeunit an, die verwendet wird, um Daten gegen vordefinierte Geschäftsregeln zu validieren.|  
    |**Lese-/Schreibe-Codeunit**|Geben Sie die Codeunit an, die importierte Daten vor der Zuordnung und exportierte Daten nach der Zuordnung verarbeitet.|  
    |**Lesen/Schreiben von XMLport**|Geben Sie den XMLport an, über den eine importierte Datendatei oder ein Datendienst vor der Zuordnung eingefügt wird und über den exportierte Daten ausgehen, wenn sie nach der Zuordnung in eine Datendatei oder einen Datendienst geschrieben werden.|  
    |**Codeunit zur externen Datenverarbeitung**|Geben Sie die Codeunit an, die externe Daten in und aus dem Daten-Exchange-Framework überträgt.|  
    |**Benutzerfeedback-Codeunit**|Geben Sie die Codeunit an, die nach dem Zuordnen verschiedene Bereinigungen ausführt, wie das Markieren von exportierten Zeilen und das Löschen temporärer Datensätze.|  
    |**Dateiverschlüsselung**|Geben Sie die Codierung der Datei an. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Spaltentrennzeichen**|Geben Sie an, wie Spalten in der Datendatei getrennt werden, wenn die Datei den Typ **Variabler Text** hat.|  
    |**Kopfzeilen**|Geben Sie an, wie viele Kopfzeilen in der Datei vorhanden sind.<br /><br /> Dadurch wird sichergestellt, dass die Kopfzeilendaten nicht importiert werden. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Kopfzeilentag**|Wenn eine Kopfzeile an verschiedenen Positionen in der Datei vorhanden ist, geben Sie den Text der ersten Spalte in der Kopfzeile ein.<br /><br /> Dadurch wird sichergestellt, dass die Kopfzeilendaten nicht importiert werden. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Fußzeilentag**|Wenn eine Fußzeile an verschiedenen Positionen in der Datei vorhanden ist, geben Sie den Text der ersten Spalte in der Fußzeile ein.<br /><br /> Dadurch wird sichergestellt, dass die Fußzeilendaten nicht importiert werden. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  

4. Im Inforegister **Zeilendefinitionen** beschreiben Sie das Formatieren der Zeilen in der Datendatei, indem Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

    > [!NOTE]  
    >  Für den Import von Bankauszügen erstellen Sie nur eine Zeile für das einzelne Format der Bankkontoauszugsdatei, die Sie importieren möchten.  
    >   
    >  Für den Export von Zahlungen können Sie eine Zeile für jede Zahlungsart erstellen, die Sie exportieren möchten. In diesem Fall zeigt das Inforegister **Spaltendefinitionen** verschiedene Spalten für jede Zahlungsart an.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Geben Sie einen Code zur Identifizierung der Zeile in der Datei ein.|  
    |**Name**|Geben Sie einen Namen ein, der die Zeile in der Datei beschreibt.|  
    |**Anzahl Spalten**|Geben Sie an, wie viele Spalten die Zeile in der Datendatei hat. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Datenzeilen-Tag**|Geben Sie die Position im entsprechenden XML-Schema des Elements an, die den Hauptposten der Datendatei darstellt. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Namespace**|Geben Sie den Namespace an, der in der Datei erwartet wird, um die Namespaceprüfung zu aktivieren. Sie können dieses Kontrollkästchen leer lassen, wenn Sie Namespaceprüfung nicht aktivieren möchten.|  

5. Wiederholen Sie Schritt 4, um eine Zeile für jede Dateidatenart zu erstellen, die Sie exportieren möchten.  

     Beschreiben Sie dann das Formatieren der Spalten in der Datendatei, indem Sie die Felder im Inforegister **Spaltendefinitionen** wie in der unten stehenden Tabelle beschrieben ausfüllen. Sie können die Strukturdatei verwenden, zum Beispiel eine XSD-Datei, damit das Inforegister mithilfe der Datendatei mit den relevanten Elementen vorab ausgefüllt wird. Weitere Informationen finden Sie im Thema [Verwenden von XML-Schemata zur Vorbereitung der Datenaustauschdefinition](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md) in der Anwendungshilfe.  

6. Wählen Sie im Inforegister **Spaltendefinitionen** die Option **Dateistruktur abrufen**.  
7. Wählen Sie auf der Seite **Datenstruktur abrufen** die zugehörige Strukturdatei aus, und wählen Sie dann die Schaltfläche **OK** aus. Die Zeilen im Inforegister **Spaltendefinitionen** werden entsprechend der Struktur der Datendatei ausgefüllt.  
8. Füllen Sie im Inforegister **Spaltendefinitionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus oder bearbeiten Sie sie.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Spaltennr.**|Geben Sie die Nummer an, die die Spaltenposition auf der Zeile in der Datei wiedergibt.<br /><br /> Für XML-Dateien geben Sie die Nummer an, die den Elementtyp in der Datei widergespiegelt, die die Daten enthält.|  
    |**Name**|Geben Sie den Namen der Spalte an.<br /><br /> Für XML-Dateien geben Sie die Markierung an, die die auszutauschenden Daten markiert.|  
    |**Datentyp**|Geben Sie an, ob die auszutauschenden Daten den Typ **Text**, **Datum** oder **Dezimal** haben.|  
    |**Datenformat**|Geben Sie das Format der Daten an, sofern vorhanden. Beispielsweise **MM-tt-jjjj**, wenn der Datentyp **Datum** ist. **Hinweis**: Für den Export geben Sie das Datenformat entsprechend [!INCLUDE[d365fin](includes/d365fin_md.md)] an. Für den Import geben Sie das Datenformat entsprechend .Net Framework an. Weitere Informationen finden Sie unter [Standardformatzeichenfolgen für Datum und Uhrzeiten](https://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Datenformatierungskultur**|Geben Sie die Kultur des Datenformats an, sofern vorhanden. Beispielsweise **en-US**, wenn der Datentyp **Dezimal** ist, um sicherzustellen, dass ein Komma als Dezimaltrennzeichen verwendet wird, entsprechend dem US-Format. Weitere Informationen finden Sie unter [Standardformatzeichenfolgen für Datum und Uhrzeiten](https://go.microsoft.com/fwlink/?LinkID=323466). **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Länge**|Geben Sie die Länge der Zeile mit fester Breite an, die diese Spalte enthält, wenn die Datendatei den Typ **Fester Text** hat.|  
    |**Beschreibung**|Geben Sie eine Beschreibung der Spalte zur Information ein.|  
    |**Pfad**|Geben Sie die Position des Elements im zugehörigen XML-Schema an.|  
    |**Kennzeichen mit negativem Zeichen**|Geben Sie den Wert ein, der in der Datendatei verwendet wird, um negative Beträge in Datendateien zu identifizieren, die keine negativen Vorzeichen enthalten können. Diese Identifikationsnummer wird verwendet, um die identifizierten Beträge während des Imports auf negative Vorzeichen zurückzusetzen. **Hinweis**: Dieses Feld ist nur für den Import relevant.|  
    |**Konstanten**|Geben Sie alle Daten an, die Sie in dieser Spalte exportieren möchten, wie etwa zusätzliche Informationen über die Zahlungsart. **Hinweis:** Dieses Feld ist nur für den Export relevant.|  

9. Wiederholen Sie Schritt 8 für jede Spalte oder jedes XML-Element in der Datendatei, die/das Daten hat, die Sie mit [!INCLUDE[d365fin](includes/d365fin_md.md)] austauschen möchten.  

 Der nächste Schritt bei der Erstellung einer Datenaustauschdefinition besteht darin, zu entscheiden, welche Spalten oder XML-Elemente welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet werden sollen.  

> [!NOTE]  
>  Die spezielle Zuordnung hängt vom Geschäftszweck der Datendatei ab, die ausgetauscht werden soll, sowie von lokalen Variationen. Selbst der SEPA-Bankstandard verfügt über lokale Variationen. [!INCLUDE[d365fin](includes/d365fin_md.md)] Stützimport von SEPA Bankkontoauszug CAMT archiviert Out\-of\-the\-Box. Dies wird durch den **SEPA CAMT**-Datenaustausch-Definitionsdatensatzcode auf der Seite **Datenaustauschdefintion** angezeigt. Informationen über die bestimmte Feldzuordnung dieser SEPA CAMT Unterstützung, siehe. [Feld-Zuordnung, wenn sie SEPA CAMT Dateien importieren](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-d365fin"></a>Spalten in der Datendatei Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zuordnen  
> [!TIP]
> Manchmal sind die Werte in den Feldern, die Sie zuordnen möchten, unterschiedlich. In einer Geschäftsanwendung lautet der Sprachcode für die USA beispielsweise „U.S.“, in der anderen „US“. Das heißt, Sie müssen den Wert beim Datenaustausch umwandeln. Dies geschieht durch Transformationsregeln, die Sie für die Felder definieren. Weitere Informationen finden Sie unter [Transformationsregeln](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

1. Wählen Sie im Inforegister **Zeilendefinitionen** die Zeile aus, für die Sie Spalten Feldern zuordnen möchten, und wählen Sie dann **Feldzuordnung** aus. Die Seite **Datenaustauschzuordnung** wird geöffnet.  
2. Spezifizieren Sie im Inforegister **Allgemein** die Zuordnungen, indem Sie die Felder gemäß der Beschreibung in der folgenden Tabelle ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Tabellen-ID**|Geben Sie die Tabelle an, die die Felder enthält, zu oder aus denen Daten entsprechend der Zuordnung ausgetauscht werden.|  
    |**Als Zwischentabelle verwenden**|Gibt an, dass die im Feld **Tabellen-ID** ausgewählte Tabelle eine Zwischentabelle ist, in der die importierten Daten vor der Zuordnung zur Zieltabelle gespeichert werden.<br /><br /> In der Regel verwenden Sie eine vorläufige Tabelle, wenn die Datenaustauschdefinition verwendet wird, um elektronische Belege zu importieren und umwandeln, wie Kreditorenrechnungen in Einkaufsrechnungen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Weitere Informationen finden Sie unter [Daten elektronisch austauschen](across-data-exchange.md).|  
    |**Name**|Geben Sie einen Namen für den Zuordnungssetup ein.|  
    |**Vorabzuordnungs-Codeunit**|Geben Sie die Codeunit an, die die Zuordnung zwischen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] und externen Daten vorbereitet.|  
    |**Zuordnungs-Codeunit**|Geben Sie die Codeunit an, die verwendet wird, um die angegebenen Spalten oder XML-Datenelemente den Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zuzuordnen.|  
    |**Codeunit für die Zuordnung im Nachhinein**|Geben Sie die Codeunit an, die die Zuordnung zwischen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] und externen Daten vervollständigt. **Hinweis**: Bei Verwendung der Funktion „AMC Banking 365 Fundamentals-Erweiterung“ wandelt Codeunit exportierte Daten aus [!INCLUDE[d365fin](includes/d365fin_md.md)] in ein für den Export bereitstehendes generisches Format um. Für den Import konvertiert die Codeunit externe Daten zu einem für den Import zu [!INCLUDE[d365fin](includes/d365fin_md.md)] geeigneten Format.|  

3.  Geben Sie im Inforegister **Feldzuordnung** an, welche Spalten welchen Feldern in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet sind, indem Sie die Felder wie in der folgenden Tabelle beschrieben ausfüllen.  

    |Feld|Beschreibung|  
    |---------------------------------|---------------------------------------|  
    |**Spaltennr.**|Geben Sie an, für welche Spalte in der Datendatei Sie eine Zuordnung definieren möchten.<br /><br /> Sie können nur Spalten auswählen, die im Inforegister **Spaltendefinitionen** auf der Seite **Datenaustauschdefintion** durch Zeilen angezeigt werden.|  
    |**Feld-ID**|Geben Sie an, welchem Feld die Spalte im Feld **Spaltennr.** zugeordnet ist. Feldkarten zu.<br /><br /> Sie können aus den Feldern nur auswählen, die in der Tabelle vorhanden sind, die Sie im Feld **Tabelle** im Inforegister **Allgemein** angegeben haben.|  
    |**Optional**|Geben Sie an, dass die Zuordnung übersprungen wird, wenn das Feld leer ist. **Hinweis**: Wenn Sie dieses Kontrollkästchen nicht aktivieren, tritt ein Exportfehler auf, wenn das Feld leer ist. **Hinweis:** Dieses Feld ist nur für den Export relevant.|  
    |**Zieltabellen-ID**|Nur sichtbar, wenn das Kontrollkästchen **Als Zwischentabelle verwenden** aktiviert ist.<br /><br /> Gibt die Tabelle an, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|  
    |**Zieltabellenbeschriftung**|Nur sichtbar, wenn das Kontrollkästchen **Als Zwischentabelle verwenden** aktiviert ist.<br /><br /> Gibt den Namen der Tabelle im Feld **Zieltabellen-ID** an, die die Tabelle ist, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|  
    |**Zielfeld-ID**|Nur sichtbar, wenn das Kontrollkästchen **Als Zwischentabelle verwenden** aktiviert ist.<br /><br /> Gibt das Feld in der Zieltabelle an, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|  
    |**Zielfeldbeschriftung**|Nur sichtbar, wenn das Kontrollkästchen **Als Zwischentabelle verwenden** aktiviert ist.<br /><br /> Gibt den Namen des Felds in der Zieltabelle an, der der Wert im Feld **Spaltenbezeichnung** zugeordnet wird, wenn eine Zwischentabelle für den Datenimport verwendet wird.|  
    |**Optional**|Nur sichtbar, wenn das Kontrollkästchen **Als Zwischentabelle verwenden** aktiviert ist.<br /><br /> Geben Sie an, ob die Zuordnung übersprungen werden soll, wenn das Feld leer ist. Wenn Sie dieses Kontrollkästchen nicht aktivieren, tritt ein Exportfehler auf, wenn das Feld leer ist.|  

Die Datenaustauschdefinition kann jetzt für Benutzer aktiviert werden. Weitere Informationen finden Sie unter [Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md), [SEPA-Überweisung einrichten](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer), [Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md) und unter [Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

### <a name="transformation-rules"></a>Transformationsregeln
Wenn die Werte in den Feldern, die Sie zuordnen, unterschiedlich sind, müssen Sie Transformationsregeln für Datenaustauschdefinitionen verwenden, um sie anzugleichen. Sie definieren Transformationsregeln für Datenaustauschdefinitionen, indem Sie eine vorhandene Definition öffnen oder eine neue Definition erstellen, dann auf dem Inforegister **Zeilendefinitionen** die Option **Verwalten**, und dann **Feldzuordnung** wählen. Vordefinierte Regeln werden bereitgestellt, aber Sie können auch eigene Regeln erstellen. In der folgenden Tabelle werden die Transformationstypen beschrieben, die Sie ausführen können.

|Option|Beschreibung|
|---------|---------|
|**Großbuchstaben**|Großschreibung aller Buchstaben.|
|**Kleinbuchstaben**|Kleinschreibung aller Buchstaben.|
|**Titelschreibung**|Großschreibung des ersten Buchstabens jedes Wortes.|
|**Kürzen**|Leerzeichen vor und nach dem Wert entfernen.|
|**Unterzeichenfolge**|Transformation eines bestimmten Teilwerts. Um anzugeben, wo die Umwandlung gestartet werden soll, wählen Sie entweder eine **Startposition** oder einen **Starttext**. Die Startposition ist eine Zahl, die das erste umzuwandelnde Zeichen darstellt. Der Anfangstext ist der Buchstabe unmittelbar vor dem zu ersetzenden Buchstaben. Wenn Sie mit dem ersten Buchstaben des Werts beginnen möchten, verwenden Sie stattdessen eine Startposition. Um anzugeben, wo die Umwandlung gestoppt werden soll, wählen Sie entweder **Länge**, was die Anzahl der zu ersetzenden Zeichen ist, oder **Nachtext** aus, was das Zeichen unmittelbar nach dem letzten zu transformierenden Zeichen ist.|
|**Ersetzen**|Suchen Sie einen Wert und ersetzen Sie ihn durch einen anderen. Dies ist nützlich, um einfache Werte wie ein bestimmtes Wort zu ersetzen.|
|**Regulärer Ausdruck – Ersetzen**|Verwenden Sie einen regulären Ausdruck als Teil einer Such- und Ersetzungsoperation. Dies ist nützlich, um mehrere oder komplexere Werte zu ersetzen.|
|**Entfernen von nicht alphanumerischen Zeichen**|Löschen Sie Zeichen, die keine Buchstaben oder Zahlen sind, z. B. Symbole oder Sonderzeichen.|
|**Datumsformatierung**|Geben Sie an, wie Datumsangaben angezeigt werden sollen. Beispielsweise können Sie TT-MM-JJJJ in JJJJ-MM-TT umwandeln.|
|**Dezimalformatierung**|Definieren Sie Regeln für die Dezimalstelle und die Rundungsgenauigkeit.|
|**Regulärer Ausdruck - Übereinstimmen**|Verwenden Sie einen regulären Ausdruck, um einen oder mehrere Werte zu finden. Dies ist den Optionen **Unterzeichenfolge** und **Regulärer Ausdruck – Ersetzen** ähnlich.|
|**Benutzerdefiniert**|Dies ist eine erweiterte Option, die die Unterstützung eines Entwicklers erfordert. Sie aktiviert ein Integrationsereignis, das Sie abonnieren können, wenn Sie Ihren eigenen Transformationscode verwenden möchten. Wenn Sie Entwickler sind und diese Option verwenden möchten, finden Sie weitere Informationen unten im Abschnitt „Tipp für Entwickler: Beispiel für die benutzerdefinierte Option“.|
|**Datum/Uhrzeit-Formatierung**|Legen Sie fest, wie das aktuelle Datum sowie die Uhrzeit angezeigt werden sollen.|

#### <a name="tip-for-developers-example-of-the-custom-option"></a>Tipp für Entwickler: Beispiel für die benutzerdefinierte Option
Das folgende Beispiel zeigt, wie Sie Ihren eigenen Transformationscode implementieren.

```
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
Nachdem Sie Ihre Regeln definiert haben, können Sie sie testen. Geben Sie im Abschnitt **Prüfung** ein Beispiel für einen Wert ein, den Sie transformieren möchten, und überprüfen Sie die Ergebnisse.

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Eine Datenaustauschdefinition als XML-Datei zur Verwendung durch andere exportieren
Wenn Sie die Datenaustauschdefinition für eine bestimmte Datendatei erstellt haben, können Sie die Datenaustauschdefinition als XML-Datei exportieren, die Sie importieren können. Dies wird im folgender Verfahren beschrieben.  

1. Geben Sie im Feld **Suchen** einen Wert für **Datenaustauschdefinitionen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Datenaustauschdefinition aus, die Sie exportieren möchten.  
3. Wählen Sie die **Datenaustauschdefinition exportieren** Aktion aus.  
4. Speichern Sie die XML-Datei, die die Datenaustauschdefinition darstellt, an einem entsprechenden Ort.  

    Wenn eine Datenaustauschdefinition bereits erstellt wurde, müssen Sie nur die XML-Datei in das Daten-Exchange-Framework importieren. Dies wird im folgender Verfahren beschrieben.  

### <a name="to-import-an-existing-data-exchange-definition"></a>So importieren Sie eine vorhandene Datenaustauschdefinition  
1. Speichern Sie die XML-Datei, die die Datenaustauschdefinition darstellt, an einem entsprechenden Ort.  
2. Geben Sie im Feld **Suchen** einen Wert für **Datenaustauschdefinitionen** ein, und wählen Sie dann den zugehörigen Link aus.  
3. Wählen Sie die Aktion **Neu** aus. Die Seite **Datenaustauschdefinition** wird geöffnet.  
4. Wählen Sie die **Datenaustauschdefinition importieren** Aktion aus.  
5. Wählen Sie die Datei aus, die Sie in Schritt 1 gespeichert haben.  

## <a name="see-also"></a>Siehe auch  
[Datenaustausch einrichten](across-set-up-data-exchange.md)  
[Einrichten des Senden und Empfangen von elektronischen Belegen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Eingehende Belege](across-income-documents.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
