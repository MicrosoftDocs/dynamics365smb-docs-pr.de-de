---
title: Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central
description: 'Erfahren Sie, wie Sie vorgehen müssen, wenn während der Synchronisierung von Daten zwischen Shopify und Business Central ein Fehler auftritt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
ms.service: dynamics-365-business-central
---

# Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central

Es kann vorkommen, dass Sie bei der Synchronisierung von Daten zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] Probleme lösen müssen. Auf dieser Seite werden Schritte zur Fehlerbehebung bei einigen häufig auftretenden Szenarien definiert.

## Aufgaben im Vordergrund ausführen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shop** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie Probleme lösen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** aus.

Wenn nun die Synchronisierungsaktion ausgelöst wird, wird die Aufgabe im Vordergrund ausgeführt. Wenn ein Fehler auftritt, erhalten Sie einen Fehlerdialog mit einem **Details kopieren**-Link. Verwenden Sie den Link, um Informationen zur weiteren Analyse in einen Texteditor zu kopieren.

## Protokolle

Die Protokollierungsfunktionen können es einfacher machen, herauszufinden, warum ein Fehler aufgetreten ist. Auf der Seite **Shopify Shop-Karte** im Feld **Protokollierungsmodus** können Sie den Detaillierungsgrad angeben, den Sie über Fehler erfassen möchten. Das Feld bietet die folgenden Optionen:

- **Deaktiviert** – Protokollieren Sie keine Informationen über Fehler.
- **Nur Fehler** – Protokollieren Sie nur die Fehlermeldung, ohne die Anforderungs-/Antwortpaare. Diese Einstellung ist die Standardeinstellung für neue Shops.
- **Alle** – Protokollieren Sie die Anforderungs-/Antwortpaare für alle Transaktionen, einschließlich derjenigen, die erfolgreich waren. Die kontinuierliche Protokollierung aller Fehler kann [!INCLUDE [prod_short](../includes/prod_short.md)] verlangsamen. Verwenden Sie diesen Modus, wenn der Datenaustausch nicht zu Fehlern führt, Sie aber mehr Erkenntnisse über die Daten erhalten möchten, die tatsächlich gesendet und empfangen wurden. Beachten Sie, dass einige Daten immer protokolliert werden, ungeachtet dessen, ob die Protokollierung aktiviert ist oder nicht. Weitere Informationen finden Sie unter [Datenerfassung](#data-capture).

### Um die Protokolle zu überprfen

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Protokolleinträge** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den zugehörigen Protokolleintrag aus und öffnen Sie dann die Seite **Shopify-Protokolleintrag**.
3. Überprüfen Sie die Anfrage, den Statuscode und die Beschreibung sowie die Antwortwerte.

> [!TIP]
> Wenn Sie Kontakt mit dem Shopify-Support aufnehmen müssen, da Sie bei der Fehlerbehebung Hilfe benötigen, beachten Sie die Informationen im Feld **Anfrage ID**. Mithilfe dieser Informationen kann der Support das Problem schneller lösen.

Sie können die Anfrage- und Antwortwerte als Dateien im Textformat herunterladen.

### Verwalten von Protokolleinträgen

Um die Größe Ihrer Datenbank unter Kontrolle zu halten, sind Protokolleinträge in einer Datenaufbewahrungsrichtlinie mit dem Namen **Shopify Protokolleintrag**. Mit Aufbewahrungsrichtlinien können Sie festlegen, wie lange Sie verschiedene Datentypen speichern möchten. Standardmäßig werden Shopify Protokolleinträge einen Monat lang aufbewahrt. Weitere Informationen zu Aufbewahrungsrichtlinien finden Sie unter [Aufbewahrungsrichtlinien definieren](../admin-data-retention-policies.md).

Über der Seite **Shopify Log-Einträge** können Sie außerdem alle Protokolleinträge oder die Einträge löschen, die älter als sieben Tage sind.

## Datenerfassung

Unabhängig davon, ob die Protokollierung eingeschaltet ist, werden einige Shopify-Antworten immer protokolliert. Sie können die Protokolle auf der Seite **Datenerfassungsliste** einsehen oder herunterladen.

Wählen Sie auf einer der folgenden Seiten die Aktion **Abgerufene Shopify Daten**:

- **Shopify-Auftrag**
- **Shopify-Auftragsposition**
- **Shopify-Auftragserfüllungen**
- **Shopify-Auftragslieferkosten**
- **Shopify-Auftragstransaktionen**
- **Shopify-Rückgabe**
- **Shopify-Rückgabeposition**
- **Shopify-Erstattung**
- **Shopify-Erstattungsposition**
- **Shopify-Auszahlungen**
- **Shopify-Zahlungstransaktionen**
- **Shopify-Transaktionen**

## Synchronisierung zurücksetzen

Für eine optimale Leistung importiert der Connector nur Debitoren, Produkte und Aufträge, die nach der letzten Synchronisierung erstellt oder geändert wurden. Auf der Seite **Shopify Shop-Karte** stehen Ihnen Funktionen zur Verfügung, mit denen Sie das Datum/die Uhrzeit der letzten Synchronisierung ändern oder komplett zurücksetzen können. Diese Funktion stellt sicher, dass alle Daten synchronisiert werden, nicht nur die Änderungen seit der letzten Synchronisierung.

Diese Funktion gilt nur für Synchronisierungen von Shopify auf [!INCLUDE[prod_short](../includes/prod_short.md)]. Sie kann nützlich sein, wenn Sie gelöschte Daten wie Produkte, Kunden oder gelöschte Bestellungen wiederherstellen müssen.

## Fordern Sie das Access-Token an

Wenn [!INCLUDE[prod_short](../includes/prod_short.md)] keine Verbindung zu Ihrem Shopify-Konto herstellen kann, versuchen Sie, den Zugriffs-Token von Shopify anzufordern. Möglicherweise müssen Sie ein neues Token beantragen, wenn Änderungen an den Sicherheitsschlüsseln oder erforderlichen Berechtigungen (Anwendungsbereichen) vorgenommen wurden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. , geben Sie **Shopify-Shops** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie den Zugriffstoken abrufen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern** aus.
4. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden.

Der Schalter **Hat AccessKey** ist eingeschaltet.

## Überprüfen und aktivieren Sie die Berechtigungen für HTTP-Anfragen in einer nicht produktiven Umgebung

Damit die Shopify Connector-Erweiterung korrekt funktioniert, benötigt sie die Berechtigung, HTTP-Anfragen zu stellen. HTTP-Anfragen sind für alle Erweiterungen verboten, wenn Sie Tests in Sandbox-Umgebungen ausführen.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Erweiterungsverwaltung** ein und wählen Sie dann den zugehörigen Link.
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

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie den Access-Token rotieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern**.
4. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem an Shopify-Konto an, überprüfen Sie den Datenschutz und die Berechtigungen, und wählen Sie dann die Schaltfläche **App installieren** aus.

## Bekannte Probleme

### Fehler: Der Verkaufskopf existiert nicht. Identifizierungsfelder und -werte: Dokumententyp='Quote',No.='YOUR SHOPIFY STORE'

Um die Preise zu berechnen, erstellt der Shopify-Connector ein temporäres Verkaufsdokument (Angebot) für einen temporären Debitor (Geschäftscode) und lässt die Standard-Preisberechnungslogik ihre Arbeit erledigen. Wenn eine Erweiterung eines Drittanbieters Ereignisse in einem temporären Verkaufsbeleg abonniert, ist die Kopfzeile möglicherweise nicht verfügbar. Wir empfehlen Ihnen, sich an den Erweiterungsanbieter zu wenden. Bitten Sie ihn, seinen Code zu ändern, um nach temporären Datensätzen zu suchen. In einigen Fällen muss er nur die `IsTemporary`-Methode an der richtigen Stelle hinzufügen. Um mehr über `IsTemporary` zu erfahren, gehen Sie zu [IsTemporary](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-istemporary-method). 

Um zu überprüfen, ob das Problem durch eine Erweiterung eines Drittanbieters verursacht wird, verwenden Sie die Verknüpfung **Informationen in die Zwischenablage kopieren** in der Fehlermeldung und kopieren Sie den Inhalt in den Texteditor. Die Informationen enthalten eine **AL-Aufrufliste**, wobei die oberste Zeile die Zeile ist, in der der Fehler aufgetreten ist. Das Folgende ist ein Beispiel einer AL-Aufrufliste.

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

### Fehler: Gen. Die Geschäftsbuchungsgruppe muss einen Wert in Debitor haben: „IHR SHOPIFY-GESCHÄFT“. Sie darf nicht leer sein

Wählen Sie im Feld **Debitorenvorlagencode** im Fenster **Shopify Shop-Karte** die Vorlage aus, in der **Geschäftsbuchungsgruppe** ausgefüllt ist. Die Debitorenvorlage wird zum Anlegen von Debitoren und zum Berechnen von Verkaufspreisen auf Verkaufsbelegen verwendet.

### Fehler: Importieren von Daten in Ihren Shopify Shop ist nicht aktiviert. Gehen Sie zur Shop-Karte, um sie zu aktivieren

Aktivieren Sie die Seite **Shopify Shop-Karte** **Datensynchronisierung mit Shopify zulassen**. Diese Einstellung hilft, den Onlineshop davor zu schützen, Demodaten aus [!INCLUDE[prod_short](../includes/prod_short.md)] abzurufen.

### Fehler: Oauth Fehler invalid_request: Konnte Shopify API-Anwendung mit api_key nicht finden

Es scheint, dass Sie die [Embed App](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) verwenden, bei der die Client URL das Format hat: `https://[application name].bc.dynamics.com`. Der Konnektor Shopify funktioniert nicht für Embed Apps. Um mehr zu erfahren, gehen Sie zu [Für welche Microsoft-Produkte ist der Shopify Connector verfügbar?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### Fehler: Interner Fehler. Anscheinend ist auf Ihrer Seite ein Fehler aufgetreten. Anforderungs-ID: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Wenden Sie sich innerhalb von sieben Tagen nach Auftreten dieses Fehlers an den Shopify-Support und geben Sie die Anforderungs-ID an. Weitere Informationen finden Sie unter [Supportmöglichkeiten für Shopify](shopify-faq.md#shopify).

### Fehler: Oauth error invalid_request: Ihr Konto verfügt nicht über die Berechtigung, den angeforderten Zugriff für diese App zu gewähren. 

Anscheinend hat der Benutzer, der Zugriff anfordert, keine Rechte zum Verwalten von Apps (die Möglichkeit, Apps und Kanäle zu verwalten und zu installieren und möglicherweise App-Gebühren zu genehmigen). Möglicherweise können Sie dieses Problem beheben, indem Sie die App als Kontoinhaber installieren. Alternativ können Sie die **App-Berechtigung** für den Benutzer in den Einstellungen [**Benutzer und Berechtigungen**](https://www.shopify.com/admin/settings/account) in Ihrer **Shopify-Verwaltung** überprüfen.  

### [{„message“:„Zugriff für FELD-Feld verweigert.“,„locations“:[{„line“:0,„column“:0}],„path“:[„path“],„extensions“:{„code“:„ACCESS_DENIED“,„documentation“:https://shopify.dev/api/usage/access-scopes}}]

Fordern Sie ein neues Token an, da die aktualisierte Version des Connectors mehr Berechtigungen (Anwendungsbereiche) erfordert. Weitere Informationen finden Sie unter [Anforderung des Zugriffstokens](#request-the-access-token).

## Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)
