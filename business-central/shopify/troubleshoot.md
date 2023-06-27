---
title: Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central
description: 'Erfahren Sie, wie Sie vorgehen müssen, wenn während der Synchronisierung von Daten zwischen Shopify und Business Central ein Fehler auftritt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.search.form: '30118, 30119, 30120, 30101, 30102'
---

# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Fehlerbehebung bei der Synchronisierung zwischen Shopify und Business Central

Es kann vorkommen, dass Sie bei der Synchronisierung von Daten zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] Probleme lösen müssen. Auf dieser Seite werden Schritte zur Fehlerbehebung bei einigen häufig auftretenden Szenarien definiert.

## <a name="run-tasks-in-the-foreground"></a>Aufgaben im Vordergrund ausführen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shop** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie Probleme lösen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** aus.

Wenn nun die Synchronisierungsaktion ausgelöst wird, wird die Aufgabe im Vordergrund ausgeführt. Wenn ein Fehler auftritt, erhalten Sie einen Fehlerdialog mit einem **Details kopieren**-Link. Verwenden Sie den Link, um Informationen zur weiteren Analyse in einen Texteditor zu kopieren.

## <a name="logs"></a>Protokolle

Wenn eine Synchronisierungsaufgabe fehlschlägt, können Sie die Protokollierung aktivieren, indem Sie den Schalter **Protokollierung aktivieren** auf der Seite **Shopify Shop-Karte** aktivieren. Dann lösen Sie die Synchronisierungsaufgabe manuell aus und überprüfen Sie die Protokolle.

### <a name="to-enable-logging"></a>Um die Protokollierung zu aktivieren

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Shopify Shop** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie Probleme lösen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Schalten Sie den Schalter **Log Enabled** ein.

### <a name="to-review-logs"></a>Um die Protokolle zu überprfen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. , geben Sie **Shopify-Protokolleinträge** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den zugehörigen Protokolleintrag aus und öffnen Sie dann die Seite **Shopify-Protokolleintrag**.
3. Überprüfen Sie die Anfrage, den Statuscode und die Beschreibung sowie die Antwortwerte. Sie können die Anfrage- und Antwortwerte als Dateien im Textformat herunterladen.

Denken Sie daran, die Protokollierung später auszuschalten, um negative Auswirkungen auf die Leistung und eine Vergrößerung der Datenbank zu vermeiden.

Über der Seite **Shopify Log-Einträge** können Sie das Löschen aller Protokolleinträge oder der Einträge, die älter als sieben Tage sind, auslösen.

## <a name="data-capture"></a>Datenerfassung

Unabhängig davon, ob **Protokoll aktiviert** aktiviert ist, werden einige Shopify Antworten immer protokolliert. Sie können die Protokolle auf der Seite **Datenerfassungsliste** einsehen oder herunterladen.

Wählen Sie auf einer der folgenden Seiten die Aktion **Abgerufene Shopify Daten**:

- **Shopify-Auftrag**
- **Shopify-Auftragserfüllungen**
- **Shopify-Auftragslieferkosten**
- **Shopify-Auftragstransaktionen**
- **Shopify-Auszahlungen**
- **Shopify-Zahlungstransaktionen**
- **Shopify-Transaktionen**

## <a name="reset-sync"></a>Synchronisierung zurücksetzen

Für eine optimale Leistung importiert der Connector nur Debitoren, Produkte und Aufträge, die nach der letzten Synchronisierung erstellt oder geändert wurden. Auf der Seite **Shopify Shop-Karte** stehen Ihnen Funktionen zur Verfügung, mit denen Sie das Datum/die Uhrzeit der letzten Synchronisierung ändern oder komplett zurücksetzen können. Diese Funktion stellt sicher, dass alle Daten synchronisiert werden, nicht nur die Änderungen seit der letzten Synchronisierung.

Diese Funktion gilt nur für Synchronisierungen von Shopify auf [!INCLUDE[prod_short](../includes/prod_short.md)]. Sie kann nützlich sein, wenn Sie gelöschte Daten wie Produkte, Kunden oder gelöschte Bestellungen wiederherstellen müssen.

## <a name="request-the-access-token"></a>Fordern Sie das Access-Token an

Wenn [!INCLUDE[prod_short](../includes/prod_short.md)] keine Verbindung zu Ihrem Shopify-Konto herstellen kann, versuchen Sie, den Zugriffs-Token von Shopify anzufordern. Möglicherweise müssen Sie ein neues Token beantragen, wenn Änderungen an den Sicherheitsschlüsseln oder erforderlichen Berechtigungen (Anwendungsbereichen) vorgenommen wurden.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. , geben Sie **Shopify-Shops** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie den Zugriffstoken abrufen möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern** aus.
4. Melden Sie sich bei Ihrem Shopify-Konto an, falls Sie dazu aufgefordert werden.

Der Schalter **Hat AccessKey** wird aktiviert.

## <a name="verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment"></a>Überprüfen und aktivieren Sie die Berechtigungen für HTTP-Anfragen in einer nicht produktiven Umgebung

Damit die Shopify Connector-Erweiterung korrekt funktioniert, benötigt sie die Berechtigung, HTTP-Anfragen zu stellen. Beim Testen in Sandboxen sind die HTTP-Anforderungen für alle Erweiterungen verboten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Erweiterungsverwaltung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Erweiterung **Shopify Konnektor**.
3. Wählen Sie die Aktion **Konfigurieren**, um die Seite **Erweiterungseinstellungen** zu öffnen.
4. Stellen Sie sicher, dass der Schalter **HTTPClient-Anfragen zulassen** aktiviert ist.

## <a name="rotate-the-shopify-access-token"></a>Shopify-Zugriffstoken rotieren

Die folgenden Prozeduren beschreiben, wie Sie den Access Token, der vom Shopify- Konnektor für den Zugriff auf Ihren Shopify Onlineshop verwendet wird, rotieren können.

### <a name="in-shopify"></a>In Shopify

1. Gehen Sie in Ihrem **Shopify Admin** zu [Apps](https://www.shopify.com/admin/apps).
2. Wählen Sie **Löschen** in der Zeile mit der **Dynamics 365 Business Central**-App aus.
3. In der angezeigten Nachricht wählen Sie **Löschen**.

### <a name="in-"></a>In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie den Access-Token rotieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zugriff anfordern**.
4. Wenn Sie dazu aufgefordert werden, melden Sie sich bei Ihrem an Shopify-Konto an, überprüfen Sie den Datenschutz und die Berechtigungen, und wählen Sie dann die Schaltfläche **App installieren** aus.

## <a name="known-issues"></a>Bekannte Probleme

### <a name="error-the-sales-header-does-not-exist-identification-fields-and-values-document-typequotenoyour-shopify-store"></a>Fehler: Der Verkaufskopf existiert nicht. Identifizierungsfelder und -werte: Dokumententyp='Quote',No.='YOUR SHOPIFY STORE'

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

### <a name="error-gen-bus-posting-group-must-have-a-value-in-customer-your-shopify-store-it-cannot-be-zero-or-empty"></a>Fehler: Gen. Die Geschäftsbuchungsgruppe muss einen Wert in Debitor haben: „IHR SHOPIFY-GESCHÄFT“. Sie darf nicht leer sein

Wählen Sie im Feld **Debitorenvorlagencode** im Fenster **Shopify Shop-Karte** die Vorlage aus, in der **Geschäftsbuchungsgruppe** ausgefüllt ist. Die Debitorenvorlage wird zum Anlegen von Debitoren und zum Berechnen von Verkaufspreisen auf Verkaufsbelegen verwendet.

### <a name="error-importing-data-to-your-shopify-shop-isnt-enabled-go-to-the-shop-card-to-enable-it"></a>Fehler: Importieren von Daten in Ihren Shopify Shop ist nicht aktiviert. Gehen Sie zur Shop-Karte, um sie zu aktivieren

Aktivieren Sie die Seite **Shopify Shop-Karte** **Datensynchronisierung mit Shopify zulassen**. Diese Einstellung hilft, den Onlineshop davor zu schützen, Demodaten aus [!INCLUDE[prod_short](../includes/prod_short.md)] abzurufen.

### <a name="error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key"></a>Fehler: Oauth Fehler invalid_request: Konnte Shopify API-Anwendung mit api_key nicht finden

Es scheint, dass Sie die [Embed App](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) verwenden, bei der die Client URL das Format hat: `https://[application name].bc.dynamics.com`. Der Konnektor Shopify funktioniert nicht für Embed Apps. Um mehr zu erfahren, gehen Sie zu [Für welche Microsoft-Produkte ist der Shopify Connector verfügbar?](shopify-faq.md#which-microsoft-products-are-the-shopify-connector-available-for).

### <a name="error-internal-error-looks-like-something-went-wrong-on-our-end-request-id-xxxxxxxx-xxxx-xxxx-xxxx-xxxx"></a>Fehler: Interner Fehler. Anscheinend ist auf Ihrer Seite ein Fehler aufgetreten. Anforderungs-ID: XXXXXXXX-XXXX-XXXX-XXXX-XXXX

Bitte wenden Sie sich innerhalb von 7 Tagen nach Auftreten dieses Fehlers an den Shopify-Support und geben Sie die Anforderungs-ID an. Weitere Informationen finden Sie unter [Supportmöglichkeiten für Shopify](shopify-faq.md#shopify).

## <a name="see-also"></a>Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)
