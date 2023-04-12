---
title: Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central
description: 'Erfahren Sie, was zu tun ist, wenn bei der Synchronisierung von Daten zwischen Shopify und Business Central etwas schief gelaufen ist'
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central

Es kann vorkommen, dass Sie bei der Synchronisierung von Daten zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] Probleme lösen müssen. Auf dieser Seite werden Schritte zur Fehlerbehebung bei einigen häufig auftretenden Szenarien definiert.

## Aufgaben im Vordergrund ausführen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shop** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie Probleme lösen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** aus.

Wenn nun die Synchronisierungsaktion ausgelöst wird, wird die Aufgabe im Vordergrund ausgeführt, und wenn ein Fehler auftritt, erhalten Sie einen Fehlerdialog mit dem Link **Details kopieren** . Verwenden Sie diesen Link, um zusätzliche Informationen zur weiteren Analyse in einen Texteditor zu kopieren.

## Protokolle

Wenn eine Synchronisierungsaufgabe fehlschlägt, können Sie die Protokollierung aktivieren, indem Sie den Schalter **Protokollierung aktivieren** auf der Seite **Shopify Shop-Karte** aktivieren. Dann lösen Sie die Synchronisierungsaufgabe manuell aus und überprüfen Sie die Protokolle.

### Um die Protokollierung zu aktivieren

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Shopify Shop** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie Probleme lösen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Schalten Sie den Schalter **Log Enabled** ein.

### Um die Protokolle zu überprfen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. , geben Sie **Shopify-Protokolleinträge** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den zugehörigen Protokolleintrag aus, und öffnen Sie die Seite **Shopify-Protokolleintrag**.
3. Überprüfen Sie die Anfrage, den Statuscode und die Beschreibung sowie die Antwortwerte. Sie können die Anfrage- und Antwortwerte als Dateien im Textformat herunterladen.

Denken Sie später daran, die Protokollierung auszuschalten, um negative Auswirkungen auf die Leistung und eine Vergrößerung der Datenbank zu vermeiden.

Auf der Seite **Shopify-Protokolleinträge** können Sie die Löschung aller Protokolleinträge oder solcher, die älter als sieben Tage sind, auslösen.

## Datenerfassung

Unabhängig von den Einstellungen für **Protokoll aktiviert** werden einige Antworten von Shopify immer protokolliert. Diese können auf der Seite **Datenerfassungsliste** überprüft oder heruntergeladen werden.

Wählen Sie auf einer der folgenden Seiten die Aktion **Abgerufene Shopify Daten**:

- **Shopify-Auftrag**
- **Shopify-Auftragserfüllungen**
- **Shopify-Auftragslieferkosten**
- **Shopify-Auftragstransaktionen**
- **Shopify-Auszahlungen**
- **Shopify-Zahlungstransaktionen**
- **Shopify-Transaktionen**

## Synchronisierung zurücksetzen

Für eine optimale Leistung importiert der Konnektor nur Kunden, Produkte und Bestellungen, die seit der letzten Synchronisierung erstellt oder geändert wurden. auf der Seite **Shopify Shop-Karte** stehen Ihnen Funktionen zur Verfügung, mit denen Sie das Datum/die Uhrzeit der letzten Synchronisierung ändern oder komplett zurücksetzen können. Diese Funktion stellt sicher, dass beim Ausführen der Synchronisierung alle Daten und nicht nur die Änderungen seit der letzten Synchronisierung synchronisiert werden.

Diese Funktion gilt nur für Synchronisierungen von Shopify auf [!INCLUDE[prod_short](../includes/prod_short.md)]. Sie kann nützlich sein, wenn Sie gelöschte Daten wie Produkte, Kunden oder gelöschte Bestellungen wiederherstellen müssen.

## Fordern Sie das Access-Token an

Wenn [!INCLUDE[prod_short](../includes/prod_short.md)] keine Verbindung zu Ihrem Shopify-Konto herstellen kann, versuchen Sie, den Zugriffs-Token von Shopify anzufordern. Diese Anfrage kann erforderlich sein, wenn die Sicherheitsschlüssel rotieren oder sich die erforderlichen Berechtigungen (Scopes) ändern.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. , geben Sie **Shopify-Shops** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie den Zugriffstoken abrufen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern** aus.
4. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden.

Der Schalter **Hat AccessKey** wird aktiviert.

### Überprüfen und aktivieren Sie die Berechtigungen für Http-Anfragen, wenn Sie in einer nicht produktiven Umgebung ausgeführt werden

Damit die Shopify Konnektor-Erweiterung korrekt funktioniert, benötigt sie die Berechtigung, Http-Anfragen zu stellen. Beim Testen in Sandboxen sind die Http-Anforderungen für alle Erweiterungen verboten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Erweiterungsverwaltung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Erweiterung **Shopify Konnektor**.
3. Wählen Sie die Aktion **Konfigurieren**, um die Seite **Erweiterungseinstellungen** zu öffnen.
4. Stellen Sie sicher, dass der Schalter **HTTPClient-Anfragen zulassen** aktiviert ist.

## Shopify-Zugriffstoken rotieren

Die folgenden Prozeduren beschreiben, wie Sie den Access Token, der vom Shopify- Konnektor für den Zugriff auf Ihren Shopify Onlineshop verwendet wird, rotieren können.

### In Shopify

1. Gehen Sie in Ihrem **Shopify Admin** zu [Apps](https://www.shopify.com/admin/apps).
2. Wählen Sie **Löschen** in der Zeile mit der **Dynamics 365 Business Central**-App aus.
3. In der angezeigten Nachricht wählen Sie **Löschen**.

### In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. , geben Sie **Shopify-Shops** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop, für den Sie den Access-Token rotieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern**.
4. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem an Shopify-Konto an, überprüfen Sie den Datenschutz und die Berechtigungen, und wählen Sie dann die Schaltfläche **App installieren** aus.

## Bekannte Probleme

### Fehler: Der Verkaufskopf existiert nicht. Identifizierungsfelder und -werte: Dokumententyp='Quote',No.='YOU SHOPIFY STORE'

Um die Preise zu berechnen, erstellt der Shopify-Connector ein temporäres Verkaufsdokument (Angebot) für einen temporären Kunden (Geschäftscode) und lässt die Standard-Preisberechnungslogik ihre Arbeit erledigen. Es ist ein typisches Szenario, wenn eine Erweiterung eines Drittanbieters Ereignisse in der Verkaufszeile abonniert, aber nicht überprüft, ob der Datensatz temporär ist, sodass auf die Kopfzeile möglicherweise nicht zugegriffen werden kann. Wir empfehlen, den Anbieter der Erweiterung zu kontaktieren und ihn zu bitten, seinen Code zu ändern, um zu prüfen, ob die Aufzeichnungen vorübergehend sind. In einigen Fällen ist das Hinzufügen der `IsTemporary` Methode an der richtigen Stelle genug. Um mehr über IsTemporary zu erfahren, gehen Sie zu [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Um zu überprüfen, ob das Problem durch eine Erweiterung eines Drittanbieters verursacht wird, verwenden Sie die Verknüpfung **Informationen in die Zwischenablage kopieren** in der Fehlermeldung und kopieren Sie den Inhalt in den Texteditor. Die Informationen enthalten eine **AL-Aufrufliste**, wobei die oberste Zeile die Zeile ist, in der der Fehler aufgetreten ist. Das Folgende ist ein Beispiel für eine AL-Aufrufliste.

Al-Aufrufliste: 
```AL
[Object Name]([Object type] [Object Id]).[Function Name] line [XX] - [Extension Name] by [Publisher] 
...
"Sales Line"(Table 37)."No. - OnValidate"(Trigger) line 98 - Base Application by Microsoft
"Shpfy Product Price Calc."(CodeUnit 30182).CalcPrice line 20 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateTempProduct line 137 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).CreateProduct line 5 - Shopify Connector by Microsoft
"Shpfy Create Product"(CodeUnit 30174).OnRun(Trigger) line 12 - Shopify Connector by Microsoft
"Shpfy Add Item to Shopify"(Report 30106)."Item - OnAfterGetRecord"(Trigger) line 2 - Shopify Connector by Microsoft
"Shpfy Products"(Page 30126)."AddItems - OnAction"(Trigger) line 5 - Shopify Connector by Microsoft
```

Denken Sie daran, die AL-Aufruflisten-Informationen mit dem Anbieter der Nebenstelle zu teilen.

### Fehler: Gen. Geschäftsbuchungsgruppe muss einen Wert in Debitor haben: IHR SHOPIFY-STORE. Sie darf nicht leer sein

Füllen Sie das Feld **Kundenvorlagencode** im Fenster **Shopify Shop-Karte** mit der Vorlage aus, in der **Geschäftsbuchungsgruppe** ausgefüllt ist. Die Kundenvorlage wird nicht nur für die Erstellung von Debitoren verwendet, sondern auch für die Berechnung des Verkaufspreises und bei der Erstellung von Belegen.

### Fehler: Importieren von Daten in Ihren Shopify Shop ist nicht aktiviert. Gehen Sie zur Shop-Karte, um sie zu aktivieren

Aktivieren Sie im Fenster **Shopify Shop-Karte** **Datensynchronisierung mit Shopify zulassen**. Dieser Umschalter soll den Online-Shop davor schützen, Demo-Daten aus [!INCLUDE[prod_short](../includes/prod_short.md)] abzurufen.

### Fehler: Oauth Fehler invalid_request: Konnte Shopify API-Anwendung mit api_key nicht finden

Es scheint, dass Sie die [Embed App](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) verwenden, bei der die Client URL das Format hat: `https://[application name].bc.dynamics.com`. Der Konnektor Shopify funktioniert nicht für Embed Apps. Weitere Informationen finden Sie unter [Für welche Microsoft Produkte ist der Konnektor Shopify verfügbar?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

## Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)
