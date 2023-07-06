---
title: Intrastat-Berichterstattung einrichten
description: 'In diesem Artikel erfahren Sie, wie Intrastat-Berichtsfunktionen eingerichtet werden, um den Handel mit Unternehmen in anderen EU-Ländern zu melden.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# <a name="set-up-intrastat-reporting"></a><a name="set-up-intrastat-reporting"></a><a name="set-up-intrastat-reporting"></a>Intrastat-Berichterstattung einrichten

Alle Firmen in der Europäischen Union (EU) müssen ihren Handel mit anderen EU-Ländern/Regionen melden. Unternehmen müssen die Bewegung von Waren jeden Monat an die Statistikbehörden in ihrem Land/ihrer Region melden, und der Bericht muss an die Steuerbehörden geliefert werden. Intrastat ist das System, das zur Erfassung von Handelsstatistiken über Waren innerhalb dieser Länder/Regionen verwendet wird. Verwenden Sie den Intrastat-Bericht, um die periodische Intrastat-Meldung zu vervollständigen, indem Sie den Handel mit Waren gemäß der lokalen Gesetzgebung erfassen, aufzeichnen und melden.

Die Intrastat-Berichterstattung basiert auf grundlegenden EU-Vorschriften, die für alle Länder gelten. Allerdings gibt es Unterschiede innerhalb der einzelnen Länder. Jedes Land hat seine eigenen Regeln, was und wie zu melden ist.

> [!NOTE]
> Intrastat-Informationen gelten nicht für die Bewegung von Dienstleistungen zwischen Ländern. Stattdessen gelten die Informationen nur für Güter wie Artikel und Anlagen. Wenn Ihre Regierung die Registrierung des Dienstleistungsverkehrs zwischen Ländern verlangt, verwenden Sie die Funktion **Dienstleistungserklärung**.
>
> Diese Funktion ist ab November 2022 als App verfügbar, die Sie von [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) herunterladen können. Um diese Funktion zu nutzen, installieren Sie sie auf der Seite **Erweiterungsverwaltung**.

> [!IMPORTANT]
> Dieser Artikel behandelt das neue Intrastat-Erlebnis, das ab [!INCLUDE[prod_short](includes/prod_short.md)] Version 21 verfügbar ist. Wenden Sie sich an Ihren Administrator, um zu erfahren, welche Version Ihre Firma verwendet und ob Sie die neuen Funktionen aktivieren sollten.
>
> Lesen Sie den Artikel zur Einrichtung und Verwendung von Intrastat in der Vorgängerversion unter [Intrastat einrichten und melden](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a><a name="enable-the-new-intrastat-experience"></a><a name="enable-the-new-intrastat-experience"></a>Aktivieren Sie das neue Intrastat-Erlebnis

In der Veröffentlichungswelle 2 von 2022 enthält [!INCLUDE[prod_short](includes/prod_short.md)] ein neu gestaltetes Intrastat-Erlebnis, das erweiterte Funktionen bereitstellt. Wenn die neue Intrastat-Funktion in Ihrer Umgebung nicht aktiviert ist, kann sie von einem Administrator auf der Seite **Funktionsverwaltung** aktiviert werden.

> [!IMPORTANT]
> Sie können nicht die alten und neuen Erfahrungen parallel verwenden. Bevor Sie die Erweiterung in einer Produktionsumgebung aktivieren, wird empfohlen, sie in einer Sandbox-Umgebung zu testen, indem Sie eine Kopie Ihrer Produktionsdaten verwenden. Nachdem Sie eine neue Benutzererfahrung in Ihrer Produktionsumgebung aktiviert haben, können Sie nicht mehr zu der alten Intrastat-Funktionalität zurückkehren.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Funktionsverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Funktionsverwaltung** die Zeile für **Funktionsupdate: Ersetzen der bestehenden Intrastat-Funktionalität durch die neue Intrastat-Erweiterung**. Mehr über die Funktionsverwaltung erfahren Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. Wählen Sie in der Spalte **Aktivieren für** die Option **Alle Benutzer** aus.
4. Lesen Sie die Erklärung darüber, wie das System aktualisiert wird, und wählen Sie dann **Ja**, um zuzustimmen.
5. Wählen Sie **Weiter** aus. Sie erhalten die grundlegende Einrichtung für Intrastat. Weitere Informationen zur Intrastat-Einrichtung lesen Sie im Abschnitt [Intrastat-Konfiguration](#intrastat-configuration).
6. Nachdem die Einrichtung abgeschlossen wurde, wählen Sie **Abschließen**, um das neue Intrastat-Erlebnis zu nutzen.

    > [!NOTE]
    > Je nach Standort Ihrer Firma genügt es, die zuvor beschriebene Funktion zu aktivieren. Für Länder mit speziellen Funktionen für das Intrastat-Berichtswesen aktivieren Sie die länderspezifische Intrastat App zusätzlich zur Haupterweiterung.

## <a name="intrastat-configuration"></a><a name="intrastat-configuration"></a><a name="intrastat-configuration"></a>Intrastat-Konfiguration

Bevor Sie Intrastat-Berichte verwenden können, müssen Sie mehrere Konfigurationen festlegen.

### <a name="intrastat-reporting-setup"></a><a name="intrastat-reporting-setup"></a><a name="intrastat-reporting-setup"></a>Einrichtung der Intrastat-Berichte

Verwenden Sie die Seite **Einrichtung der Intrastat-Berichterstattung**, um das Standardverhalten für das Intrastat-Berichtswesen zu aktivieren und festzulegen. Sie können angeben, ob Sie Intrastat aus Sendungen (Versendungen), Eingängen (Ankünften) oder beidem melden müssen, je nach den Schwellenwerten, die in Ihren lokalen Vorschriften festgelegt sind. Sie können auch Standardtransaktionstypen für die regulären und Retourenbelege festlegen, die für die Meldung von Transaktionen verwendet werden.

Führen Sie die folgenden Schritte aus, um Intrastat-Berichtswesen einzurichten:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Intrastat-Berichtseinrichtung** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie auf dem Inforegister **Allgemein** Feldinformationen nach Bedarf aus oder geben Sie sie ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt einige der Schlüsselfelder.

   | Feld | Description |
   | --- | --- |
   | **Eingänge melden** | Gibt an, dass Sie Zugänge der eingegangenen Waren in Intrastat-Berichte aufnehmen müssen. |
   | **Sendungen melden** | Gibt an, dass Sie Lieferungen versendeter Waren in Intrastat-Berichte aufnehmen müssen. |
   | **Lieferungen auf Basis von**  | Gibt den Ländercode an, auf dessen Grundlage die Intrastat-Berichtszeilen genommen werden.  |
   | **MwSt.-Nr. basierend auf** | Gibt an, basierend auf welchem Debitoren- oder Kreditorencode die Mehrwertsteuernummer (MwSt.) für den Intrastat-Bericht genommen wird.  |
   | **Unternehmens-MwSt.-Nr. in Datei** | Gibt an, wie die Umsatzsteuer-Identifikationsnummer der Firma in die Intrastat-Datei exportiert wird.  |
   | **Kreditoren-MwSt.-Nr. in Datei** | Legt fest, wie die Umsatzsteuer-Identifikationsnummer eines Lieferanten in die Intrastat-Datei exportiert werden soll.  |
   | **Debitoren-MwSt.-Nr. in Datei** | Legt fest, wie die Umsatzsteuer-Identifikationsnummer eines Kunden in die Intrastat-Datei exportiert wird.  |
   | **Partner-Umsatzsteuer abrufen** | Gibt an, aus welcher Zeile des Intrastat-Berichts die Umsatzsteuer-Identifikationsnummer des Partners aktualisiert wird. Je nach Ihren lokalen Anforderungen können Sie Zeilen nur für den Eingang, nur für den Versand oder für beide Arten von Zeilen wählen. |

3. Wählen Sie auf dem Inforegister **Standardtransaktionen** Feldinformationen nach Bedarf aus oder geben Sie sie ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt einige der Schlüsselfelder.

   | Feld | Description |
   | --- | --- |
   | **Standardmäßige Art des Geschäftes** | Gibt den Standardtransaktionstyp für reguläre Verkaufslieferungen, Servicelieferungen und Einkaufslieferungen an. |
   | **Vorgabe Trans. Typ - Retouren** | Legt die Standard-Transaktionsart für Retouren, Service-Retouren und Kauf-Retouren fest. |
   | **Standard-MwSt.-Nr. einer Privatperson** | Gibt die Standard-Umsatzsteueridentifikationsnummer für Privatpersonen an, falls die Privatperson eine dedizierte Umsatzsteuernummer im Intrastat-Bericht haben muss. |
   | **Standard-MwSt.-Nr. des Drittanbieters** | Gibt die Standard-Mehrwertsteuernummer für Drei-Parteien-Handel an, falls Sie die Mehrwertsteuernummer nicht haben. |
   | **Standard-Umsatzsteuer für unbekannten Status** | Gibt die Standard-Mehrwertsteuernummer für einen unbekannten Status an. |
   | **Standardländer-/-regionscode** | Legt den Standardcode für das Empfängerland fest. |

4. Wählen Sie auf dem Inforegister **Berichterstellung** die Feldinformationen nach Bedarf aus oder geben Sie sie ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Die folgende Tabelle beschreibt einige der Schlüsselfelder.

   | Feld | Description |
   | --- | --- |
   | **Datenaustausch-Definitionscode** | Gibt den Datenaustausch-Definitionscode an, um die Intrastat-Datei zu erzeugen. Dieses Feld ist nur verfügbar, wenn das Feld **Dateien für Eingänge/Lieferungen trennen** auf **Nein** festgelegt ist. |
   | **Dateien für Eingänge/Lieferungen trennen** | Gibt an, ob Eingänge und Sendungen in zwei separaten Dateien gemeldet werden sollen. |
   | **Zip-Datei(-s)** | Gibt an, ob die Berichtsdateien der ZIP-Datei hinzugefügt werden sollen. |
   | **Daten Aust. Def. Code - Eingang** | Gibt den Data Exchange Definitionscode an, um die Intrastat-Datei für Wareneingänge zu erzeugen. Dieses Feld ist nur verfügbar, wenn das Feld **Dateien für Eingänge/Lieferungen trennen** auf **Ja** festgelegt ist. |
   | **Daten Aust. Def. Code - Sendung** | Gibt den Datenaustausch-Definitionscode an, um die Intrastat-Datei für versandte Waren zu erzeugen. Dieses Feld ist nur verfügbar, wenn das Feld **Dateien für Eingänge/Lieferungen trennen** auf **Ja** festgelegt ist. |

5. Geben Sie auf dem Inforegister **Nummerierung** einen Wert in das Feld **Intrastat-Nummern** ein.

### <a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a><a name="set-up-a-reporting-file"></a>Legen Sie eine Berichtsdatei fest

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Datenaustauschdefinitionen** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **Neu** aus, und geben Sie dann auf dem Inforegister **Allgemein** Informationen zu Datenaustauschdefinition, Dateityp, Spaltentrennzeichen, zugehörigen Codeunits, XMLport und anderen Feldern nach Bedarf ein.
3. Geben Sie auf dem Inforegister **Zeilendefinitionen** einen Wert im Feld **Zeilentyp** ein, um die Formatierung der Zeilen in der Datendatei zu beschreiben und wo Sie die Anzahl der Spalten für diese Zeile definieren müssen.
4. Auf der Inforegisterkarte **Spaltendefinitionen** füllen Sie die Zeile für jede geplante Spalte aus. Sie können Spaltennamen, Datentypen (wie Text, Datum oder Dezimal), die Länge der Zeile mit fester Breite, die die Spalte enthält, wenn die Datei vom Typ *Fester Text* ist, und einige andere Parameter definieren.
5. Wählen Sie auf dem Inforegister **Zeilendefinitionen** **Feldzuordnung** aus.
6. Erstellen Sie auf der Seite **Feldzuordnung** einen neuen Eintrag. 
7. Wählen Sie auf dem Inforegister **Allgemein** den Wert für **Tabellen-ID** (für **Intrastat-Berichtszeile** wählen Sie **4812**), und geben Sie die folgenden Feldinformationen ein:

   1. Geben Sie in dem Feld **Schlüsselindex** den Schlüsselindex an, nach dem die Quelldatensätze vor dem Export sortiert werden sollen.
   2. Wählen Sie im Feld **Zuordnungs-Codeunit** einen Wert aus.

8. Fügen Sie auf dem Inforegister **Feldzuordnung** die Spalten hinzu, die Sie zuvor auf dem Inforegister **Spaltendefinitionen** konfiguriert haben, und fügen Sie dann folgende Feldinformationen hinzu:

   1. Geben Sie für jede der Spalten den **Feld-ID**-Wert an.
   2. Geben Sie den **Transformationsregel**-Wert für jede Spalte nach Bedarf an. Der Wert gibt die Regel an, die importierten Text in einen unterstützten Wert umwandelt, bevor er einem bestimmten Feld in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden kann. Wenn Sie einen Wert in diesem Feld auswählen, wird der genaue Wert in das Feld **Transformationsregel** in der **Daten Aust. Feld Zuordnung Puf.** Tabelle. (Umgekehrt: Bei Eingabe eines genauen Werts in das Feld **Transformationsregel** in der **Datenaustausch-Feldzuordnungspuffer** Tabelle, wird in diesem Feld ein Wert ausgewählt.)

9. Wenn Sie Einträge auf der Basis einiger Spalten gruppieren müssen, wählen Sie auf dem Inforegister **Feldgruppierung** die Felder aus, die Sie für die Gruppierung verwenden möchten.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] wird mit der vorkonfigurierten Data Exchange Definition für Intrastat für alle lokalisierten Länder geliefert. Um mehr über das Erstellen einer neuen Datenaustauschdefinition zu erfahren, siehe [Datenaustauschdefinitionen einrichten](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a><a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a><a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Pflichtfelder mit der Checkliste für den Intrastat-Bericht festlegen

In einigen Ländern verlangen die Behörden, dass Intrastat-Berichte z.B. die Versandmethode für Einkäufe oder andere Werte enthalten, wenn die Verkäufe einen bestimmten Schwellenwert überschreiten.

Zum Festlegen der Pflichtfelder oder Werte auf der Seite **Intrastat-Bericht** befolgen Sie diese Schritte:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Berichtseinrichtung** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie **Intrastat-Berichtsprüfliste** aus.
3. Befolgen Sie diese Schritte, um die erforderlichen Zeilen für die Überprüfung hinzuzufügen:
   1. Legen Sie das Feld **Feld Nr.** auf ein Feld fest, das auf einen nicht leeren Wert geprüft werden muss.
   2. Geben Sie einen Wert in das Feld **Filterausdruck** bei Bedarf auf der Grundlage der folgenden Regeln ein:

        1. Wenn Sie die **Filterseite** öffnen, wählen Sie den Filter, den Sie für die Überprüfung verwenden müssen.
        2. Wählen Sie einen Wert aus, der sich auf den ausgewählten Filter bezieht.
        3. Wenn Sie weitere Filter für das ausgewählte Feld ausfüllen müssen, wiederholen Sie die beiden vorherigen Schritte, um einen weiteren Filter hinzuzufügen.
        4. Wenn Sie die Eingabe der Filter für das gewählte Feld abgeschlossen haben, wählen Sie **OK** aus.

   3. Markieren Sie das Kontrollkästchen **Umgekehrter Filterausdruck**, um festzulegen, dass die Prüfung der Felder nur in den Zeilen ausgeführt wird, die nicht dem Filterausdruck entsprechen. Wenn die Zeile nicht gefiltert wird, wird dieses Feld ignoriert.

> [!NOTE]
> Wenn Sie die **Filterseite** über die Zeile **Filterausdruck** öffnen, können Sie alle Standardfilterausdrücke verwenden, die sich auf das spezifische Feld beziehen, das Sie filtern möchten.
>
> Seien Sie vorsichtig, wenn Sie Validierungsregeln einrichten, da sie sich von Land zu Land unterscheiden können.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a><a name="use-custom-codeunits-in-intrastat-reporting"></a><a name="use-custom-codeunits-in-intrastat-reporting"></a>Angepasste Codeunits in Intrastat-Berichten verwenden

Wenn Sie die Funktionsweise von Intrastat ändern möchten und die Standardkonfiguration nicht ausreicht, können Sie das System anpassen, indem Sie die Standardfunktionen erweitern. Wenn Sie das Verhalten von Intrastat weiter verändern möchten, können Sie Ihre eigenen Codeunits entwickeln. Wenn Sie Codeunits erstellen, müssen Sie zusätzliche Änderungen vornehmen, um sie verwenden zu können. Um das System für die Verwendung Ihrer eigenen Objekte zu konfigurieren, befolgen Sie diese Schritte.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **MwSt.-Berichtskonfiguration** ein, und wählen Sie dann den zugehörigen Link aus.
2. Fügen Sie auf der Seite **Konfiguration MwSt.-Berichte** eine neue Zeile hinzu.
3. Wählen Sie im Feld **MwSt.-Berichtstyp** die Option **Intrastat-Bericht** aus.
4. Geben Sie im Feld **MwSt.-Berichtsversion** die Version des Berichts an.
5. Fügen Sie Ihre Codeunits für die folgenden Optionen hinzu:
   1. Geben Sie im Feld **Zeilen vorschlagen codeunit-ID** die neue codeunit für das Vorschlagen von Zeilen in den Zeilen des Intrastat-Berichts an.
   2. Geben Sie im Feld **Inhalt codeunit-ID** die neue codeunit für den Export von Daten als Datei über eine Datenaustauschdefinition an.
   3. Geben Sie im Feld **codeunit-ID validieren** die neuen codeunits für die Validierung von Ergebnissen in Intrastat-Berichtszeilen an.

> [!IMPORTANT]
> Diese Zeile muss leer sein, wenn Sie die Standard Codeunits verwenden. Sie sollten nur dann eine Zeile erstellen und konfigurieren, wenn Sie angepasste Codeunits entwickelt haben.

## <a name="other-intrastat-configurations"></a><a name="other-intrastat-configurations"></a><a name="other-intrastat-configurations"></a>Andere Intrastat-Konfigurationen

Debitor- und Kreditorkarten enthalten das Feld **Intrastat-Partnertyp**, das die gleichen Optionswerte wie das Feld **Partnertyp** hat: 

- „“ (leer)
- *Unternehmen*
- *Person*
    
Das Feld **Partnertyp** wurde in der Intrastat-Meldung durch das Feld **Intrastat-Partnertyp** ersetzt. Das Feld **Partnertyp** wird im einheitlichen Euro-Zahlungsverkehrsraum (SEPA) zur Definition des SEPA-Lastschriftverfahrens (Core oder B2B) verwendet. Das Feld **Intrastat-Partnertyp** wird nur für Intrastat-Meldungen verwendet. Deshalb können Sie bei Bedarf unterschiedliche Werte für die beiden Felder angeben.

Wenn das Feld **Intrastat-Partnertyp** leer gelassen wird, wird der Wert aus dem Feld **Partnertyp** für die Intrastat-Meldung verwendet.

Neben **Intrastat-Berichtseinrichtung**, **Datenaustauschdefinition** und **Intrastat-Berichtsprüfliste** müssen noch folgende weitere Einstellungen konfiguriert werden:

| Seite | Description |
| ---- | ----------- |
| **Länder/Regionen** | Fügen Sie auf der Seite **Länder/Regionen** die Informationen zu **EU-Länder-/Regionscode** und **Intrastat-Code** hinzu, um einen Code für das Land/die Region anzugeben, mit dem/der Sie Handel treiben. Diese Informationen werden in Intrastat-Berichten verwendet. |
| **Zollpositionen** | In vielen Ländern werden von den Zoll- und Steuerbehörden achtstellige Codes für verschiedene Artikel vorgeschrieben. Um die Artikelposten so zu aktivieren, dass sie die erforderlichen Informationen enthalten, wenn das Programm sie in die Intrastat-Buchungsblattzeile importiert, geben Sie den Artikelcode auf der Seite **Zollpositionen** ein. Suchen Sie die Codes für die Elemente, mit denen Ihre Firma handelt, und geben Sie sie auf der Seite **Zollpositionen** ein. |
| **Verkehrszweige** | Es gibt sieben einstellige Codes für Intrastat-Transportmethoden: **1** für den Seetransport, **2** für den Schienentransport, **3** für den Straßentransport, **4** für den Lufttransport, **5** für den Posttransport, **7** für feste Anlagen und **9** für den Transport mit eigenem Antrieb (z. B. der Transport eines Autos durch Fahren). [!INCLUDE[prod_short](includes/prod_short.md)] erfordert diese spezifischen Codes nicht. Wir empfehlen jedoch, dass die Beschreibungen eine ähnliche Bedeutung bereitstellen. |
| **Transaktionsarten** | Länder und Regionen haben unterschiedliche Codes für Arten von Intrastat-Transaktionen, wie z.B. gewöhnlicher Kauf und Verkauf, Umtausch von zurückgegebenen Waren und Umtausch von nicht zurückgegebenen Waren. Legen Sie alle Codes fest, die für Ihr Land/Ihre Region gelten. Diese Codes werden dann auf dem Inforegister **Auslandshandel** auf Einkaufs- und Verkaufsbelegen und bei der Bearbeitung von Retouren verwendet. |
| **Transaktionsspezifikationen** | Legen Sie Codes fest, um die Beschreibungen der Transaktionsarten zu ergänzen. |
  
> [!NOTE]
> Ab Januar 2022 verlangt Intrastat unterschiedliche Transaktionsnatur-Codes für Versendungen an Privatpersonen oder nicht mehrwertsteuerlich registrierte Unternehmen und an mehrwertsteuerlich registrierte Unternehmen. Um diese Anforderung zu erfüllen, empfehlen wir Ihnen, die Transaktionsnatur-Codes auf der Seite **Art des Geschäftes** entsprechend den Anforderungen in Ihrem Land zu überprüfen und/oder neue hinzuzufügen. Sie sollten auch das Feld **Intrastat-Partnertyp** auf *Person* für eine Privatperson oder einen nicht mehrwertsteuerlich registrierten Geschäftskunden auf der entsprechenden **Kunden**-Seite überprüfen und aktualisieren. Wenn Sie sich nicht sicher sind, welchen Intrastat-Partnertyp oder Transaktionstyp Sie verwenden sollen, empfehlen wir Ihnen, einen Experten in Ihrem Land oder Ihrer Region zu fragen.

|   Feld   |   Description   |
| --------- | --------------- |
| **Nettogewicht** | Das Gewicht ist eine der grundlegenden Konfigurationen, die mit der Intrastat-Meldung verknüpft sind, da das Gesamtgewicht für die Meldung obligatorisch ist. Um für diese Anforderung bereit zu sein, geben Sie einen Wert in das Feld **Nettogewicht** auf der Karte des Artikels oder der Anlage ein. |
| **Ursprungsland** | Verwenden Sie die zweistelligen ISO-Alpha-Codes auf der Karte des Elements oder der Anlage für das Land, in dem die Ware erworben oder hergestellt wurde. Wenn die Ware in mehr als einem Land hergestellt wurde, ist das Ursprungsland das letzte Land, in dem sie in nennenswertem Umfang verarbeitet wurde. |
| **Mehrwertsteuer-Identifikationsnummer des Partnerunternehmens im Status des Einfuhrlandes** | Dies ist die Umsatzsteuer-Identifikationsnummer des Partnerunternehmens im Status des Einfuhrlandes. Die Umsatzsteuer-Identifikationsnummer wird auch beim Austausch von Intra-EU-Exportdaten zwischen den Mitgliedstaaten verwendet und lässt die Mitgliedstaaten zu, die erhaltenen Daten der importierenden Firma in ihrem eigenen Land zuzuordnen. Die meldenden Einheiten müssen die Umsatzsteuer-Identifikationsnummer der Firma angeben, die den innergemeinschaftlichen Erwerb von Waren im Status des Einfuhrlandes gemeldet hat. |

Optional können Sie auch Folgendes angeben:

* **Warencodes**: Zoll- und Steuerbehörde haben numerische Codes eingerichtet, die Artikel und Dienstleistungen klassifizieren. Sie können diese Codes für Artikel angeben.
* **Gebiete**: Ergänzende Informationen über Länder und Regionen.
* **Eingangs-/Ausgangsorte**: Geben Sie die Orte an, an denen Sie Artikel in andere Länder versenden oder aus anderen Ländern empfangen. Ein Flughafen ist ein Beispiel für einen Eingangs- oder Ausgangspunkt. Sie geben Häfen auf Verkaufs- und Einkaufsbelegen des Inforegisters **Außenhandel** ein. Diese Informationen werden aus den Artikelposten kopiert, wenn Sie das Intrastat-Buch.-Blatt erstellen.
* **Zusätzliche Maßeinheit**: Die Menge der Waren für die Intrastat-Meldung kann entweder das Nettogewicht (in Kilogramm) oder eine zusätzliche Einheit sein. Wenn zusätzliche Einheiten erforderlich sind, müssen Sie diese für Elemente und Anlagen konfigurieren.

#### <a name="set-up-transport-methods"></a><a name="set-up-transport-methods"></a><a name="set-up-transport-methods"></a>Verkehrszweige festlegen

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Verkehrszweige** ein, und wählen Sie dann den zugehörigen Link aus.
2. Geben Sie die Informationen in die Felder wie erforderlich ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a><a name="set-up-transaction-nature-codes"></a><a name="set-up-transaction-nature-codes"></a>Transaktionsnatur-Codes festlegen

1. wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Art des Geschäftes** ein, und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie die Informationen in die Felder wie erforderlich ein. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a><a name="other-related-configurations"></a><a name="other-related-configurations"></a>Andere verwandte Konfigurationen

Bevor Sie die Intrastat-Berichtswesenfunktion verwenden, müssen Sie Felder auf den Artikel-, Anlage-, Debitor- und Kreditorkarten definieren.

#### <a name="item-cards"></a><a name="item-cards"></a><a name="item-cards"></a>Element-Karten

Befolgen Sie diese Schritte, um alle erforderlichen Informationen im Bezug zu Intrastat auf den Artikelkarten einzurichten.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie das Element, das Sie konfigurieren möchten.
3. Geben Sie auf dem Inforegister **Einstandspreise und Buchung** in den Feldern **Zollpos.**, **Besondere Einheit** und **Code Ursprungsland/-region** einen Wert ein.

    > [!NOTE]
    > Um eine Einheit zu verwenden, die die Basiseinheit ergänzt, konfigurieren Sie die zusätzliche Basiseinheit auf der Seite **Artikeleinheiten**.

4. Geben Sie im Inforegister **Bestand** in das Feld **Nettogewicht** einen Wert im Dezimalformat ein.

> [!NOTE]
> Wenn Sie die Zollposition zu einer Einheit hinzufügen, die für den Artikel definiert ist, füllt [!INCLUDE [prod_short](includes/prod_short.md)] das Feld **Besondere Einheit** basierend auf der Konfiguration der Zollposition automatisch aus. Sie können den Wert des Felds **Besondere Einheit** nach Bedarf ändern.

#### <a name="set-up-fixed-assets-for-intrastat"></a><a name="set-up-fixed-assets-for-intrastat"></a><a name="set-up-fixed-assets-for-intrastat"></a>Anlagen für Intrastat einrichten

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Anlagen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Anlage, die Sie konfigurieren möchten.
3. Geben Sie im Inforegister **Intrastat** in die Felder **Zollpos.**, **Nettogewicht** und **Besondere Einheit** einen Wert ein.

> [!NOTE]
> Sie können verschiedene Maßeinheiten als zusätzliche Maßeinheit verwenden. Aber egal, welchen **Maßeinheiten-Code** Sie wählen, seine **Menge** in den Intrastat-Berichten wird immer 1 sein.

#### <a name="set-up-vendors-for-intrastat"></a><a name="set-up-vendors-for-intrastat"></a><a name="set-up-vendors-for-intrastat"></a>Kreditoren für Intrastat einrichten

Bevor Sie einen Kreditor in die Intrastat-Berichterstellung aufnehmen können, geben Sie seine Informationen auf der Seite **Kreditorenkarte** ein. Geben Sie beispielsweise einen Wert für **Länder-/Regionscode** und einen Wert für **USt-IdNr.** an.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Kreditoren** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Anbieter, den Sie konfigurieren möchten.
3. Legen Sie auf dem Inforegister **Intrastat** Standardwerte für die Felder **Standardmäßige Art des Geschäftes**, **Standardmäßige Art des Geschäftes – Rücksendungen** und **Standardverkehrszweig** fest.
4. Geben Sie im Inforegister **Zahlungen** im Feld **Intrastat-Partnertyp** an, ob der Kreditor eine Person oder ein Unternehmen ist.

#### <a name="set-up-customers-for-intrastat"></a><a name="set-up-customers-for-intrastat"></a><a name="set-up-customers-for-intrastat"></a>Debitoren für Intrastat einrichten

Bevor Sie einen Debitor in die Intrastat-Berichterstellung aufnehmen können, geben Sie seine Informationen auf der Seite **Debitorenkarte** ein. Sie müssen beispielsweise einen Wert für **Länder-/Regionscode** und einen Wert für **USt-IdNr.** angeben.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Debitoren** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Kunden aus, den Sie konfigurieren möchten.
3. Legen Sie auf dem Inforegister **Intrastat** die Standardwerte für die Felder **Standardmäßige Art des Geschäftes**, **Standardmäßige Art des Geschäftes – Rücksendungen** und **Standardverkehrszweig** fest.
4. Geben Sie im Inforegister **Zahlungen** im Feld **Intrastat-Partnertyp** an, ob der Kreditor eine Person oder ein Unternehmen ist.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a><a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a><a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Elemente und Anlagen von Intrastat-Berichten ausschließen

Wenn es einen Grund gibt, um einen bestimmten Artikel oder eine bestimmte Anlage von der Intrastat-Berichterstattung auszuschließen, ändern Sie die Option auf der jeweiligen Karte.

##### <a name="exclude-an-item-from-intrastat-reporting"></a><a name="exclude-an-item-from-intrastat-reporting"></a><a name="exclude-an-item-from-intrastat-reporting"></a>Ein Element von der Intrastat-Berichterstattung ausschließen

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Artikel** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Artikel aus, den Sie konfigurieren möchten, und aktivieren Sie dann auf dem Inforegister **Einstandspreise und Buchung** das Kontrollkästchen **Aus Intrastat-Bericht ausschließen**.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a><a name="exclude-a-fixed-asset-from-intrastat-reporting"></a><a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Eine Anlage aus dem Intrastat-Bericht ausschließen

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Anlagen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Anlage, die Sie konfigurieren möchten.
3. Aktivieren Sie im Inforegister **Intrastat** das Kontrollkästchen **Aus Intrastat-Bericht ausschließen**.

#### <a name="set-up-tariff-numbers"></a><a name="set-up-tariff-numbers"></a><a name="set-up-tariff-numbers"></a>Zollpositionen einrichten

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Zollpositionen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Geben Sie auf der Seite **Zollpositionen** Informationen in den Feldern gemäß der Beschreibung in der folgenden Tabelle ein.

    | Feld | Description |  
    |-------|-------------|
    | **Nr.** | Gibt die Zollposition an. |
    | **Beschreibung** | Gibt eine Beschreibung der zugehörigen Zollposition an. |
    | **Besondere Einheiten** | Legt fest, ob die Zoll- und Steuerbehörden Angaben zu Mengen und Einheiten für den Artikel verlangen. |
    | **Umrechnungsfaktor** | Gibt den Umrechnungsfaktor für die Zollposition an |
    | **Einheit** | Gibt die Einheit für die Zollposition an |

> [!NOTE]
> Wenn Sie eine besondere Einheit hinzufügen, fragt [!INCLUDE [prod_short](includes/prod_short.md)], ob Sie zugehörige Artikel aktualisieren möchten. Wenn Sie zugehörige Artikel aktualisieren, wird der Wert **Einheit** auf der Seite **Artikeleinheiten** für alle Artikel mit der gleichen Zollposition aktualisiert.
> 
> Wenn Sie dem Artikel eine Zollposition mit einem definierten **Einheit**-Wert hinzufügen, fügt [!INCLUDE [prod_short](includes/prod_short.md)] dem **Artikeleinheit**-Wert für den Artikel automatisch eine neue Einheit hinzu. Der Wert **Menge pro Einheit** basiert auf dem Feld **Mengenrundungspräzision**.

## <a name="enter-countryregion-intrastat-settings"></a><a name="enter-country-specific-intrastat-settings"></a><a name="enter-country-specific-intrastat-settings"></a>Länderspezifische Intrastat-Einstellungen eingeben

Intrastat-Anforderungen sind in allen Mitgliedsstaaten der EU ähnlich, obwohl es wichtige Ausnahmen gibt. Theoretisch sollten die Regeln in allen Mitgliedsstaaten einheitlich angewendet werden. Es gibt jedoch Unterschiede bei den Implementierungen, da einige Mitgliedstaaten Leitlinien zur Verfügung stellen, wie die Grundsätze in bestimmten Situationen (z. B. Handelsmuster und Rücksendungen von Waren) anzuwenden sind. Diese Leitlinien können für verschiedene Situationen zu unterschiedlichen Ergebnissen führen. Daher können sich die von den Ländern einzugebenden Informationen ebenso unterscheiden wie das Dateiformat, das sie für die Meldung verwenden müssen.

### <a name="austria"></a><a name="austria"></a><a name="austria"></a>Österreich

Die Intrastat-Berichterstellung in Österreich erfordert zwei unterschiedliche Dateien für Eingänge und Lieferungen. Gehen Sie folgendermaßen vor, um zu überprüfen, ob Ihre Einrichtung korrekt ist.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Berichtseinrichtung** ein, und wählen Sie den entsprechenden Link aus.  
2. Überprüfen Sie im Inforegister **Berichterstellung**, ob **Eingangs-/Sendungsdateien aufteilen** ausgewählt ist. Wenn dem so ist, wurden zwei separate **Datenaustausch-Definitionscode**-Werte konfiguriert. 
3. Vergewissern Sie sich, dass das Feld **Zip-Datei(-en)** ausgewählt ist, um sicherzustellen, dass Berichtsdateien zur Zip-Datei hinzugefügt werden.

Der Vorgang, mit Intrastat-Berichten zu arbeiten, entspricht dem von globalen Funktionen.

<!-- ### Belgium-->

### <a name="czech-republic"></a><a name="czech-republic"></a><a name="czech-republic"></a>Tschechische Republik

Die neue Intrastat-Berichtsumgebung für die Tschechische Republik wird ab dem 1. Veröffentlichungszyklus 2023 verfügbar sein. Verwenden Sie in der Zwischenzeit die Funktion **Intrastat-Buch.-Blatt** weiter.

### <a name="finland"></a><a name="finland"></a><a name="finland"></a>Finnland

In Finnland sind einige zusätzliche Schritte zur Einrichtung von Intrastat erforderlich. Die Intrastat-Berichterstellung in Finnland erfordert zwei unterschiedliche Dateien für Eingänge und Lieferungen. Sie werden auch sehen, dass zwei separate **Datenaustausch-Definitionscode**-Werte konfiguriert wurden.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Berichtseinrichtung** ein, und wählen Sie den entsprechenden Link aus.  
2. Geben Sie auf der Seite **Intrastat-Berichtseinrichtung** im Inforegister **Dateieinrichtung** die Feldinformationen gemäß der Beschreibung in der folgenden Tabelle ein.

    |                 Feld              |            Description                |  
    |------------------------------------|---------------------------------------|
    | **Benutzerdefinierter Code** | Gibt einen benutzerdefinierten Code für die Einrichtungsinformationen der Intrastat-Datei an. |
    | **Seriennummer des Unternehmens** | Gibt eine Seriennummer des Unternehmens die Einrichtungsinformationen der Intrastat-Datei an. |

3. Überprüfen Sie im Inforegister **Berichterstellung**, ob **Eingangs-/Sendungsdateien aufteilen** ausgewählt ist.

Der Vorgang, mit Intrastat-Berichten zu arbeiten, entspricht dem von globalen Funktionen.

<!-- ### Germany-->

### <a name="italy"></a><a name="italy"></a><a name="italy"></a>Italien

Eine neue Intrastat-Berichtsumgebung für Italien ist ab Februar 2023 verfügbar. Verwenden Sie in der Zwischenzeit die Funktion **Intrastat-Buch.-Blatt** weiter.

<!-- ### France-->

### <a name="sweden"></a><a name="sweden"></a><a name="sweden"></a>Schweden

Die Intrastat-Berichterstellung in Schweden erfordert zwei unterschiedliche Dateien für Eingänge und Lieferungen. Gehen Sie folgendermaßen vor, um zu überprüfen, ob Ihre Einrichtung korrekt ist.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Intrastat-Berichtseinrichtung** ein, und wählen Sie den entsprechenden Link aus.  
2. Überprüfen Sie im Inforegister **Berichterstellung**, ob **Dateien für Eingänge/Lieferungen trennen** ausgewählt ist. Wenn dem so ist, wurden zwei separate **Datenaustausch-Definitionscode**-Werte konfiguriert.

Der Vorgang, mit Intrastat-Berichten zu arbeiten, entspricht dem von globalen Funktionen.

<!-- ### United Kingdom-->

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Siehe die entsprechende Schulung unter [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Intrastat-Berichterstattung in Business Central](finance-how-report-intrastat.md)  
[Finanzmanagement](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
