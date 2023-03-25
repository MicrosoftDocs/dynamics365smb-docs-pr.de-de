---
title: Intrastat-Berichterstattung festlegen
description: 'Erfahren Sie, wie Sie die Funktionen zur Intrastat-Meldung festlegen, um den Handel mit Firmen in anderen EU-Ländern zu melden.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Intrastat-Berichterstattung festlegen

Alle Firmen in der Europäischen Union (EU) müssen ihren Handel mit anderen EU-Ländern/Regionen melden. Unternehmen müssen die Bewegung von Waren jeden Monat an die Statistikbehörden in ihrem Land/ihrer Region melden, und der Bericht muss an die Steuerbehörden geliefert werden. Intrastat ist das System zur Erfassung von Handelsstatistiken für Waren innerhalb dieser Länder/Regionen. Sie verwenden **Intrastat-Bericht**, um die periodische Intrastat-Meldung (in der Regel monatlich) zu vervollständigen und den Handel mit Waren gemäß der lokalen Gesetzgebung zu erfassen, aufzuzeichnen und zu melden.

Die Intrastat-Meldungen basieren auf den grundlegenden EU-Vorschriften, die für alle Länder gelten; in der Praxis gibt es jedoch einige Unterschiede zwischen den einzelnen Ländern. Jedes Land hat seine eigenen Regeln, was genau und wie zu melden ist.

> [!NOTE]
> Intrastat-Informationen gelten nicht für die Bewegung von Dienstleistungen zwischen Ländern, sondern nur für Waren (Elemente und Anlagen). Wenn die lokale Regierung die Registrierung des Dienstleistungsverkehrs zwischen Ländern verlangt, kann dies über die Funktion **Dienstleistungserklärung** erfolgen.
>
> Diese Funktion wird voraussichtlich ab November 2022 als App unter [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) zur Verfügung stehen. Wenn Sie sie also nutzen möchten, müssen Sie sie zunächst auf der Seite **Erweiterungsverwaltung** installieren.

> [!IMPORTANT]
> Dieser Artikel behandelt das neue Intrastat-Erlebnis, das ab [!INCLUDE[prod_short](includes/prod_short.md)] Version 21 verfügbar ist. Wenden Sie sich an Ihren Administrator, um zu erfahren, welche Version Ihre Firma verwendet und um die neuen Funktionen zu aktivieren.
>
> Lesen Sie den Artikel zur Einrichtung und Verwendung von Intrastat in der Vorgängerversion unter [Intrastat einrichten und melden](finance-how-setup-report-intrastat-v20.md).

## Aktivieren Sie das neue Intrastat-Erlebnis

In der Veröffentlichungswelle 2 von 2022 enthält [!INCLUDE[prod_short](includes/prod_short.md)] ein neu gestaltetes Intrastat-Erlebnis mit erweiterten Funktionen. Wenn die neue Intrastat-Funktion in Ihrer Umgebung nicht aktiviert ist, kann sie von einem Administrator auf der Seite **Funktionsverwaltung** manuell aktiviert werden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Funktionsverwaltung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Funktionsverwaltung** die **Funktion Update: Ersetzen Sie die vorhandene Intrastat-Funktionalität durch die neue Intrastat-Erweiterung**. Mehr über die Funktionsverwaltung erfahren Sie unter [Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management) im Inhalt der Administration.
3. Wählen Sie in der Spalte **Aktivieren für** die Option **Alle Benutzer**.
4. Lesen Sie die Erklärung, wie das System aktualisiert werden soll und wählen Sie **Ja**, wenn Sie damit einverstanden sind.
5. Wählen Sie **Weiter** und Sie erhalten eine grundlegende Einrichtung für Intrastat. Lesen Sie mehr über die Intrastat-Einrichtung im Abschnitt [Intrastat-Konfiguration](#intrastat-configuration).
6. Nachdem Sie die Einrichtung abgeschlossen haben, wählen Sie **Abschließen**, um das neue Intrastat-Erlebnis zu nutzen.

> [!IMPORTANT]
> Beachten Sie, dass Sie die alten und neuen Erfahrungen nicht parallel verwenden können. Bevor Sie die Erweiterung in einer Produktionsumgebung aktivieren, empfiehlt es sich, diese Funktion zunächst in einer Sandbox-Umgebung mit einer Kopie der Produktionsdaten zu aktivieren und zu testen, bevor Sie dies in einer Produktionsumgebung tun. Sobald Sie eine neue Benutzererfahrung in Ihrer Produktionsumgebung aktiviert haben, können Sie nicht mehr zu der alten Intrastat-Funktionalität zurückkehren.

> [!NOTE]
> Je nach Standort Ihrer Firma genügt es, die oben beschriebene Funktion zu aktivieren. Für Länder mit speziellen Funktionen für das Intrastat-Reporting sollten Sie zusätzlich zur Haupterweiterung die länderspezifische Intrastat App aktivieren.

## Intrastat-Konfiguration

Bevor Sie Intrastat-Berichte verwenden können, müssen Sie mehrere Konfigurationen festlegen.

### Einrichtung der Intrastat-Berichte

Auf der Seite **Einrichtung der Intrastat-Berichterstattung** können Sie die Intrastat-Berichterstattung aktivieren und die Standardeinstellungen dafür festlegen. Sie können angeben, ob Sie Intrastat aus Sendungen (Versendungen), Eingängen (Ankünften) oder beidem melden müssen, je nach den Schwellenwerten, die in Ihren lokalen Vorschriften festgelegt sind. Sie können auch Standardtransaktionsarten für reguläre und Retourenbelege festlegen, die für die Art der Meldung von Transaktionen verwendet werden.

Um das Intrastat-Reporting festzulegen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Intrastat-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die Registerkarte **Allgemein** Inforegister und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt einige der Schlüsselfelder:

   | Feld | Description |
   | --- | --- |
   | **Eingänge melden** | Gibt an, dass Sie Zugänge der eingegangenen Waren in Intrastat-Berichte aufnehmen müssen. |
   | **Sendungen melden** | Gibt an, dass Sie Lieferungen versendeter Waren in Intrastat-Berichte aufnehmen müssen. |
   | **Sendungen basierend auf**  | Gibt an, aus welchen Intrastat-Berichtszeilen der Ländercode entnommen wird Sie können eine der Optionen wählen: **Verkauf an Land**, **Rechnung an Land** oder **Versand an Land**. |
   | **Umsatzsteuer-Nr. Basierend auf** | Legt fest, auf welcher Basis des Kunden-/Lieferantencodes die Umsatzsteuernummer (VAT) für den Intrastat-Bericht genommen wird. Sie können eine der folgenden Optionen wählen: **Verkauf mit MwSt** oder **Rechnung mit MwSt**. |
   | **Umsatzsteuer-Nr. der Firma in der Datei** | Legt fest, wie die Umsatzsteuer-Identifikationsnummer der Firma in die Intrastat-Datei exportiert wird. Sie können eine der folgenden Optionen wählen: MwSt.-Reg. Nr., Hinzufügen des EU-Ländercodes als Präfix und Entfernen des EU-Ländercodes aus der USt.-Reg. Nr. |
   | **Umsatzsteuer-Nr. des Lieferanten in der Datei** | Legt fest, wie die Umsatzsteuer-Identifikationsnummer eines Lieferanten in die Intrastat-Datei exportiert werden soll. Sie können eine der folgenden Optionen wählen: MwSt.-Reg. Nr., Hinzufügen des EU-Ländercodes als Präfix und Entfernen des EU-Ländercodes aus der USt.-Reg. Nr. |
   | **Kunden-Umsatzsteuer-Nr. in Datei** | Legt fest, wie die Umsatzsteuer-Identifikationsnummer eines Kunden in die Intrastat-Datei exportiert wird. Sie können eine der folgenden Optionen wählen: MwSt.-Reg. Nr., Hinzufügen des EU-Ländercodes als Präfix und Entfernen des EU-Ländercodes aus der USt.-Reg. Nr. |
   | **Partner-Umsatzsteuer abrufen** | Legt fest, aus welcher Zeile des **Intrastat-Berichts** die Umsatzsteuer-Identifikationsnummer des Partners aktualisiert wird. Je nach Ihren lokalen Anforderungen können Sie nur für den Eingang, nur für den Versand oder für beide Arten von Zeilen wählen. |
3. Öffnen Sie die Registerkarte **Standardtransaktionen** Inforegister und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt einige der Schlüsselfelder:

   | Feld | Description |
   | --- | --- |
   | **Vorgabe Trans. Typ** | Gibt den Standardtransaktionstyp für reguläre Verkaufslieferungen, Servicelieferungen und Einkaufslieferungen an. |
   | **Vorgabe Trans. Typ - Retouren** | Legt die Standard-Transaktionsart für Retouren, Service-Retouren und Kauf-Retouren fest. |
   | **Standard-Umsatzsteuer-Nr. für Privatpersonen** | Gibt die Standard-Umsatzsteueridentifikationsnummer für Privatpersonen an, falls die Privatperson eine eigene Umsatzsteuernummer im Intrastat-Bericht haben muss. |
   | **Standard 3-Parteien Inzahlungnahme USt.-Nr.** | Gibt die Standard-Mehrwertsteuernummer für 3-Parteien-Handel an, falls Sie keine eigene Mehrwertsteuernummer haben. |
   | **Standard-Umsatzsteuer für unbekannten Status** | Gibt die Standard-Mehrwertsteuernummer für einen unbekannten Status an. |
   | **Standard-Länder/Regionen-Code** | Legt den Standardcode für das Empfängerland fest. |
4. Öffnen Sie das Inforegister **Berichterstattung** und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt einige der Schlüsselfelder:

   | Feld | Description |
   | --- | --- |
   | **Daten Aust. Def. Code** | Gibt den Datenaustausch-Definitionscode an, um die Intrastat-Datei zu erzeugen. Funktioniert nur, wenn das Feld **Eingangs-/Sendungsdateien aufteilen** als **Nein** festgelegt ist. |
   | **Eingangs-/Sendungsdateien aufteilen** | Gibt an, ob Eingänge und Sendungen in zwei separaten Dateien gemeldet werden sollen. |
   | **Zip-Datei(-s)** | Legt fest, ob die Berichtsdatei(-en) der .zip-Datei hinzugefügt werden soll. |
   | **Daten Aust. Def. Code - Eingang** | Gibt den Data Exchange Definitionscode an, um die Intrastat-Datei für Wareneingänge zu erzeugen. Funktioniert nur, wenn das Feld **Eingangs-/Sendungsdateien aufteilen** als **Ja** festgelegt ist. |
   | **Daten Aust. Def. Code - Sendung** | Gibt den Datenaustausch-Definitionscode an, um die Intrastat-Datei für versandte Waren zu erzeugen. Funktioniert nur, wenn das Feld **Eingangs-/Sendungsdateien aufteilen** als **Ja** festgelegt ist. |
5. Öffnen Sie das Inforegister **Nummerierung**, um die **Intrastat-Nummern** festzulegen.

### Legen Sie eine Berichtsdatei fest

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Data Exchange Definitions** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Auf der Registerkarte **Allgemein** beschreiben Sie die Data Exchange Definition, den Dateityp, das Spaltentrennzeichen, die zugehörigen Codeunits, XMLport und andere Felder, indem Sie die Felder ausfüllen.
4. Auf der Registerkarte **Zeilendefinitionen** beschreiben Sie die Formatierung der Zeilen in der Datendatei, indem Sie die Felder basierend auf dem Feld **Zeilentyp** ausfüllen und die Anzahl der Spalten für diese Zeile festlegen.
5. Auf der Inforegisterkarte **Spaltendefinitionen** füllen Sie die Zeile für jede geplante Spalte aus. Sie können Spaltennamen, Datentypen (*Text*, *Datum* oder *Dezimal*), die Länge der Zeile mit fester Breite, die die Spalte enthält, wenn die Datei vom Typ Fester Text ist, und einige andere Parameter definieren.
6. Wählen Sie die Aktion **Feldzuordnung** auf dem Inforegister **Zeilendefinitionen**, um die Seite **Feldzuordnung** zu öffnen.
7. Erstellen Sie den neuen Eintrag, und wählen Sie auf der Registerkarte **Allgemein** Inforegister die richtige **Tabellen-ID** (für **Intrastat Report Zeile** wählen Sie 4812), und füllen Sie dann weitere Felder aus:
   1. Geben Sie in dem Feld **Schlüsselindex** den Schlüsselindex an, nach dem die Datensätze vor dem Export sortiert werden sollen.
   2. Wählen Sie die richtige **Zuordnung Codeunit**.
8. Fügen Sie auf der Inforegister-Registerkarte **Feldzuordnung** die Spalten hinzu, die Sie zuvor auf der Inforegister-Registerkarte **Spaltendefinitionen** konfiguriert haben, und fügen Sie dann Folgendes hinzu:
   1. Geben Sie für jede der Spalten die **Feld-ID** an.
   2. Geben Sie die **Transformationsregel** für jede Spalte an, die Sie benötigen. Sie gibt die Regel an, die importierten Text in einen unterstützten Wert umwandelt, bevor er einem bestimmten Feld in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden kann. Wenn Sie einen Wert in diesem Feld auswählen, wird der genaue Wert in das Feld **Transformationsregel** in der **Daten Aust. Feld Zuordnung Puf.** Tabelle und umgekehrt.
9. Wenn Sie Einträge auf der Basis einiger Spalten gruppieren müssen, wählen Sie auf der Inforegisterkarte **Feldgruppierung** die Felder aus, die Sie für die Gruppierung verwenden möchten.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] wird mit der vorkonfigurierten Data Exchange Definition für Intrastat für alle lokalisierten Länder geliefert. Erfahren Sie mehr über das Erstellen einer neuen Datenaustausch-Definition in dem Artikel [Datenaustausch-Definitionen einrichten](across-how-to-set-up-data-exchange-definitions.md).

### Pflichtfelder mit der Checkliste für den Intrastat-Bericht festlegen

In einigen Ländern verlangen die Behörden, dass Intrastat-Berichte z.B. die Versandmethode für Einkäufe oder andere Werte enthalten, wenn die Verkäufe einen bestimmten Schwellenwert überschreiten.

So legen Sie Pflichtfelder und/oder Werte auf der Seite **Intrastat-Bericht** fest:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Prüfliste Intrastat-Bericht**.
3. Fügen Sie die erforderlichen Zeilen für die Überprüfung anhand der folgenden Anweisungen hinzu:
   1. Legen Sie das Feld **Feld Nr.** auf ein Feld fest, das auf einen nicht leeren Wert geprüft werden muss.
   2. Füllen Sie das Feld **Filterausdruck** bei Bedarf auf der Grundlage der folgenden Regeln aus:
      1. Wenn Sie die **Filterseite** öffnen, wählen Sie den **Filter**, den Sie für die Überprüfung verwenden müssen.
      2. Im nächsten Schritt wählen Sie einen Wert, der sich auf den **Filter** bezieht, den Sie verwendet haben.
      3. Wenn Sie weitere Filter für dieses Feld benötigen, können Sie einen weiteren Filter hinzufügen, indem Sie die gleichen Schritte ausführen.
      4. Wenn Sie die Eingabe der Filter für das gewählte Feld abgeschlossen haben, wählen Sie **OK**.
   3. Markieren Sie das Feld **Umgekehrter Filterausdruck**, um festzulegen, dass die Prüfung der Felder nur in den Zeilen ausgeführt wird, die nicht dem Filterausdruck entsprechen. Wenn die Zeile nicht gefiltert wird, wird dieses Feld ignoriert.

> [!NOTE]
> Wenn Sie die **Filterseite** über die Zeile **Filterausdruck** öffnen, können Sie alle Standardfilterausdrücke verwenden, die sich auf das spezifische Feld beziehen, das Sie filtern möchten.
>
> Gehen Sie beim Einrichten von Validierungsregeln sorgfältig vor. Sie können von Land zu Land unterschiedlich sein.

## Angepasste Codeunits in Intrastat-Berichten verwenden

Wenn Sie die Funktionsweise von Intrastat ändern möchten und die Standardkonfiguration nicht ausreicht, können Sie das System anpassen, indem Sie die Standardfunktionen erweitern. Wenn Sie das Verhalten von Intrastat weiter verändern möchten, können Sie Ihre eigenen Codeunits entwickeln. Wenn Sie Codeunits erstellen, müssen Sie jedoch zusätzliche Änderungen vornehmen, um sie verwenden zu können. Um das System für die Verwendung Ihrer eigenen Objekte zu konfigurieren:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Konfiguration MwSt.-Berichte** ein und wählen Sie dann den entsprechenden Link.
2. Fügen Sie auf der Seite **Konfiguration MwSt.-Berichte** eine neue Zeile hinzu.
3. Wählen Sie im Feld **Typ des MwSt.-Berichts** die Option **Intrastat-Bericht**.
4. Geben Sie im Feld **VAT Report Version** die Version des Berichts an.
5. Danach können Sie Ihre Codeunits für die folgenden Optionen hinzufügen: a. Geben Sie im Feld **Zeilen vorschlagen codeunit-ID** die neue codeunit für das Vorschlagen von Zeilen in den Zeilen des Intrastat-Berichts an.
   b. Geben Sie im Feld **Inhalt codeunit-ID** die neue codeunit für den Export von Daten als Datei über eine Datenaustauschdefinition an.
   c. Geben Sie im Feld **codeunit-ID validieren** die neuen codeunits für die Validierung von Ergebnissen in Intrastat-Berichtszeilen an.

> [!IMPORTANT]
>
> Diese Zeile muss leer sein, wenn Sie die Standard Codeunits verwenden. Sie sollten nur dann eine Zeile erstellen und konfigurieren, wenn Sie angepasste Codeunits entwickelt haben.

## Andere Intrastat-Konfigurationen

> [!IMPORTANT]
> Kunden- und Lieferantenkarten enthalten ein Feld, **Intrastat-Partnertyp**, das die gleichen Optionswerte wie das Feld **Partnertyp** hat: „“ (leer), *Firma*, und *Person*. Das Feld **Intrastat-Partnertyp** hat das Feld **Partnertyp** im Intrastat-Reporting ersetzt. Das Feld **Partnertyp** wird im einheitlichen Euro-Zahlungsverkehrsraum (SEPA) zur Definition des SEPA-Lastschriftverfahrens (Core oder B2B) verwendet. Das Feld **Intrastat-Partnertyp** wird nur für Intrastat-Meldungen verwendet. Auf diese Weise können Sie bei Bedarf unterschiedliche Werte für die beiden Felder angeben.
>
> Wenn das Feld **Intrastat-Partnertyp** leer gelassen wird, wird der Wert aus dem Feld **Partnertyp** für die Intrastat-Meldung verwendet.

Außer **Intrastat-Bericht-Einrichtung**, **Data Exchange Definitionen** und **Intrastat-Bericht-Checkliste** müssen Sie noch weitere Einstellungen vornehmen:

| Seite | Description |
| ---- | ----------- |
| **Länder/Regionen** | Bevor Sie mit der Verwendung von Intrastat-Berichten beginnen, müssen Sie auch die Seite **Länder/Regionen** festlegen. Auf dieser Seite müssen Sie den **EU Länder/Regionen Code** und **Intrastat Code** hinzufügen, um einen Code für das Land/die Region anzugeben, mit dem/der Sie Handel treiben, da dieser in den Intrastat-Berichten verwendet wird. |
| **Zollsatz-Nummern** | In vielen Ländern legen die Zoll- und Steuerbehörden 8-stellige Codes für verschiedene Artikel fest. Damit die Elemente bei der Erfassung in der Intrastat-Journalzeile die erforderlichen Informationen enthalten, müssen Sie den Artikelcode auf der Seite **Zollsätze** eingeben. Suchen Sie die Codes für die Elemente, mit denen Ihre Firma handelt, und geben Sie sie auf der Seite **Zollsätze** ein. |
| **Verkehrszweige** | Es gibt sieben einstellige Codes für Intrastat-Verkehrszweige. **1** für den Seetransport, **2** für den Schienentransport, **3** für den Straßentransport, **4** für den Lufttransport, **5** für den Posttransport, **7** für feste Anlagen und **9** für den Transport mit eigenem Antrieb (z.B. der Transport eines Autos durch Fahren). [!INCLUDE[prod_short](includes/prod_short.md)] erfordert diese spezifischen Codes nicht; wir empfehlen jedoch, dass die Beschreibungen eine ähnliche Bedeutung haben. |
| **Transaktionsarten** | Länder und Regionen haben unterschiedliche Codes für Arten von Intrastat-Transaktionen, wie z.B. gewöhnlicher Kauf und Verkauf, Umtausch von zurückgegebenen Waren und Umtausch von nicht zurückgegebenen Waren. Legen Sie alle Codes fest, die für Ihr Land/Ihre Region gelten. Diese Codes werden dann auf dem Inforegister **Auslandshandel** auf Einkaufs- und Verkaufsbelegen und bei der Bearbeitung von Retouren verwendet. |
| **Transaktionsspezifikationen** | Legen Sie Codes fest, um die Beschreibungen der Transaktionsarten zu ergänzen. |
  > [!NOTE]
  > Ab Januar 2022 verlangt Intrastat unterschiedliche Transaktionsnatur-Codes für Versendungen an Privatpersonen oder nicht mehrwertsteuerlich registrierte Unternehmen und an mehrwertsteuerlich registrierte Unternehmen. Um diese Anforderung zu erfüllen, empfehlen wir Ihnen, die Transaktionsnatur-Codes auf der Seite **Transaktionsarten** entsprechend den Anforderungen in Ihrem Land zu überprüfen und/oder neue hinzuzufügen. Sie sollten auch das Feld **Intrastat-Partnertyp** auf *Person* für eine Privatperson oder einen nicht mehrwertsteuerlich registrierten Geschäftskunden auf der entsprechenden **Kunden**-Seite überprüfen und aktualisieren. Wenn Sie sich nicht sicher sind, welche Intrastat-Partnerart oder Transaktionsart Sie verwenden sollen, empfehlen wir Ihnen, einen Experten in Ihrem Land oder Ihrer Region zu fragen.

| **Feld** | **Beschreibung** |
| --------- | --------------- |
| **Nettogewicht** | Das Gewicht ist eine der grundlegenden Konfigurationen im Zusammenhang mit der Intrastat-Meldung, da das **Gesamtgewicht** für die Meldung obligatorisch ist. Um für diese Anforderung bereit zu sein, müssen Sie auch das Feld **Nettogewicht** auf der Karte des Elements oder der Anlage ausfüllen. |
| **Herkunftsland-Code** | Verwenden Sie die zweistelligen ISO-Alpha-Codes auf der Karte des Elements oder der Anlage für das Land, in dem die Ware erworben oder hergestellt wurde. Wenn die Ware in mehr als einem Land hergestellt wurde, ist das Ursprungsland das letzte Land, in dem sie in nennenswertem Umfang verarbeitet wurde. |
| **Mehrwertsteuer-Identifikationsnummer des Partnerunternehmens im Status des Einfuhrlandes** | Dies ist die Umsatzsteuer-Identifikationsnummer des Partnerunternehmens im Status des Einfuhrlandes. Die Umsatzsteuer-Identifikationsnummer wird auch beim Austausch von Intra-EU-Exportdaten zwischen den Mitgliedstaaten verwendet und lässt die Mitgliedstaaten zu, die erhaltenen Daten der importierenden Firma in ihrem eigenen Land zuzuordnen. Die meldenden Einheiten müssen die Umsatzsteuer-Identifikationsnummer der Firma angeben, die den innergemeinschaftlichen Erwerb von Waren im Status des Einfuhrlandes gemeldet hat. |

Optional können Sie auch Folgendes angeben:

* **Warencodes**: Zoll- und Steuerbehörde haben numerische Codes eingerichtet, die Artikel und Dienstleistungen klassifizieren. Sie geben diese Codes der Artikel an.
* **Gebiete**: Ergänzende Informationen über Länder und Regionen.
* **Eingangs-/Ausgangsorte**: Geben Sie die Orte an, an denen Sie Artikel in andere Länder versenden oder aus anderen Ländern empfangen. Ein Flughafen ist ein Beispiel für einen Eingangs- oder Ausgangspunkt. Sie geben Häfen auf Verkaufs- und Einkaufsbelegen des Inforegisters **Außenhandel** ein. Diese Daten werden auch aus den Artikelposten kopiert, wenn Sie das Intrastat-Buch.-Blatt erstellen.
* **Zusätzliche Maßeinheit**: Die Menge der Waren für die Intrastat-Meldung kann entweder das Nettogewicht (in Kilogramm) oder eine zusätzliche Einheit sein. Wenn zusätzliche Einheiten erforderlich sind, müssen Sie diese für Elemente und Anlagen konfigurieren.

#### Verkehrszweige festlegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Verkehrszweige** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Transaktionsnatur-Codes festlegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Transaktionsarten** ein, und wählen Sie den entsprechenden Link.
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Andere verwandte Konfigurationen

Bevor Sie die Funktion Intrastat-Berichtswesen verwenden, müssen Sie einige Felder auf den Artikel-, Anlage-, Kunden- und Lieferantenkarten konfigurieren.

#### Element-Karten

So legen Sie alle erforderlichen Informationen zu Intrastat auf den Artikelkarten fest:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Element, das Sie konfigurieren möchten.
3. Füllen Sie im Inforegister **Kosten & Buchung** die Felder **Zollsatz-Nr.**, **Zusätzliche Maßeinheit** und **Herkunftsland/Regionscode** aus.
4. Geben Sie im Inforegister **Bestand** den Dezimalwert in das Feld **Nettogewicht** ein.

> [!NOTE]
> Sie können verschiedene Maßeinheiten als zusätzliche Maßeinheit verwenden. Wenn diese nicht mit der **Basis Maßeinheit** übereinstimmt, müssen Sie diese Maßeinheit auf der Seite **Maßeinheiten** konfigurieren.

#### Karten für Anlagen

So legen Sie alle erforderlichen Informationen zu Intrastat auf den Karten für Anlagen fest:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Anlagen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Anlage, die Sie konfigurieren möchten.
3. Füllen Sie im Inforegister **Intrastat** die Felder **Zollsatz-Nr.**, **Nettogewicht** und **Zusätzliche Maßeinheit** aus.

> [!NOTE]
> Sie können verschiedene Maßeinheiten als zusätzliche Maßeinheit verwenden. Aber egal, welchen **Maßeinheiten-Code** Sie wählen, seine **Menge** in den Intrastat-Berichten wird immer 1 sein.

#### Lieferantenkarten

Bevor Sie einen Lieferanten in Intrastat-Berichten verwenden können, müssen Sie für jeden dieser Lieferanten einen eigenen **Länder/Regionen Code** und eine **Mehrwertsteuer-Registrierungsnummer** haben, zusätzlich zu weiteren Informationen auf der Seite **Lieferantenkarte**:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Lieferanten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Anbieter, den Sie konfigurieren möchten.
3. Auf dem Inforegister **Intrastat** können Sie Standardwerte für die **Vorgabe Trans. Type**, **Standard Trans. Typ - Retouren** und **Standard-Transportmethode** festlegen.
4. Geben Sie im Inforegister **Zahlungen** im Feld **Intrastat-Partnertyp** an, ob der Kreditor eine Person oder ein Unternehmen ist.

#### Kundenkarten

Bevor Sie einen Kunden im Intrastat-Reporting verwenden können, müssen Sie für jeden dieser Kunden einen eigenen **Länder/Regionen Code** und eine **Mehrwertsteuer-Registrierungsnummer** haben, zusätzlich zu weiteren Informationen auf der Seite **Kundenkarte**:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Kunden** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Kunden aus, den Sie konfigurieren möchten.
3. Auf dem Inforegister **Intrastat** können Sie Standardwerte für die **Vorgabe Trans. Type**, **Standard Trans. Typ - Retouren** und **Standard-Transportmethode** festlegen.
4. Geben Sie im Inforegister **Zahlungen** im Feld **Intrastat-Partnertyp** an, ob der Kreditor eine Person oder ein Unternehmen ist.

#### Elemente und Anlagen von Intrastat-Berichten ausschließen

Wenn es einen Grund gibt, warum ein bestimmtes Element oder eine Anlage von der Intrastat-Berichterstattung ausgeschlossen werden soll, müssen Sie eine Option auf der Karte ändern.

##### Ein Element von der Intrastat-Berichterstattung ausschließen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Element, das Sie konfigurieren möchten.
3. Wählen Sie im Inforegister **Kalkulation & Buchung** das Feld **Aus Intrastat-Bericht ausschließen** aus.

##### Eine Anlage aus dem Intrastat-Bericht ausschließen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Anlagen** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Anlage, die Sie konfigurieren möchten.
3. Wählen Sie im Inforegister **Intrastat** das Feld **Aus Intrastat-Bericht ausschließen** aus.

## Länderspezifische Intrastat-Einrichtung

Die Intrastat-Anforderungen sind in allen Mitgliedsstaaten der EU ähnlich, obwohl es wichtige Ausnahmen gibt. Theoretisch sollten die Regeln in allen Mitgliedsstaaten einheitlich angewendet werden. Es gibt jedoch Unterschiede bei der Implementierung, da einige Mitgliedstaaten Leitlinien zur Verfügung stellen, wie die allgemeinen Grundsätze der Verordnung in bestimmten Situationen angewendet werden sollen. Beispielsweise Handelsmuster, Warenrücksendungen und so weiter. Diese Leitlinien können für verschiedene Situationen in den EU-Mitgliedstaaten zu unterschiedlichen Ergebnissen führen. Aus diesem Grund haben einige Länder zusätzliche spezifische Informationen, die sich von denen anderer Länder unterscheiden. Sie verwenden auch ein anderes Dateiformat für die Berichterstellung.

### Österreich

Die Intrastat-Berichterstellung in Österreich erfordert zwei unterschiedliche Dateien für Eingänge und Lieferungen. Gehen Sie folgendermaßen vor, um zu überprüfen, ob Ihre Einrichtung korrekt ist:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Einrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Überprüfen Sie im Inferegister **Berichterstellung**, ob **Eingangs-/Sendungsdateien aufteilen** ausgewählt ist. Damit zusammenhängend wurden zwei separate **Datenaustauschdef. Codes** konfiguriert. Das Feld **.zip-Datei(en)** wird ebenfalls ausgewählt, um sicherzustellen, dass Berichtsdateien zur .zip-Datei hinzugefügt werden.

Der Vorgang, mit Intrastat-Berichten zu arbeiten, entspricht dem von globalen Funktionen.

<!-- ### Belgium-->

### Tschechische Republik

Die neue Intrastat-Berichtsumgebung für die Tschechische Republik wird ab der 1. Veröffentlichungszyklus 2023 verfügbar sein. In der Zwischenzeit können Sie die Funktion **Intrastat-Buch.-Blatt** weiter verwenden.

### Finnland

In Finnland sind einige zusätzliche Schritte zur Einrichtung von Intrastat erforderlich. Die Intrastat-Berichterstellung in Finnland erfordert zwei unterschiedliche Dateien für Eingänge und Lieferungen. Damit zusammenhängend wurden zwei separate **Datenaustauschdef. Codes** konfiguriert.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Einrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie auf der Seite **Intrastat-Berichtseinrichtung** im Inforegister **Dateieinrichtung** die erforderlichen Felder gemäß der Beschreibung in der folgenden Tabelle aus:

    |Feld|Beschreibung|  
    |------------------------------------|---------------------------------------|
    | **Benutzerdefinierter Code**|Gibt einen benutzerdefinierten Code für die Einrichtungsinformationen der Intrastat-Datei an. |
    | **Seriennummer des Unternehmens**|Gibt eine Seriennummer des Unternehmens die Einrichtungsinformationen der Intrastat-Datei an. |

3. Überprüfen Sie im Inforegister **Berichterstellung**, ob **Eingangs-/Sendungsdateien aufteilen** ausgewählt ist.

Der Vorgang, mit Intrastat-Berichten zu arbeiten, entspricht dem von globalen Funktionen.

<!-- ### Germany-->

### Italien

Die neue Intrastat-Berichtsumgebung für Italien ist ab Februar 2023 verfügbar. In der Zwischenzeit können Sie die Funktion **Intrastat-Buch.-Blatt** weiter verwenden.

<!-- ### France-->

### Schweden

Die Intrastat-Berichterstellung in Schweden erfordert zwei unterschiedliche Dateien für Eingänge und Lieferungen. Gehen Sie folgendermaßen vor, um zu überprüfen, ob Ihre Einrichtung korrekt ist:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Einrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Überprüfen Sie im Inforegister **Berichterstellung**, ob **Eingangs-/Sendungsdateien aufteilen** ausgewählt ist. Damit zusammenhängend wurden zwei separate **Datenaustauschdef. Codes** konfiguriert.

Der Vorgang, mit Intrastat-Berichten zu arbeiten, entspricht dem von globalen Funktionen.

<!-- ### United Kingdom-->

## Siehe die entsprechende Schulung unter [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Siehe auch

[Intrastat-Berichterstattung in Business Central](finance-how-report-intrastat.md)  
[Finanzmanagement](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
