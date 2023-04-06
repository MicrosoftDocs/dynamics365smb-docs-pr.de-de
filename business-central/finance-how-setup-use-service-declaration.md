---
title: Die Erweiterung Service-Deklaration festlegen und verwenden
description: 'Erfahren Sie, wie Sie die Funktionen der Service-Deklaration (Intrastat für Dienstleistungen) festlegen und verwenden, um den Handel mit Unternehmen in anderen EU-Ländern zu melden.'
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# Die Erweiterung für die Service-Deklaration

In einigen EU-Ländern verlangen die Behörden, dass Unternehmen den Export von Dienstleistungen in andere EU-Länder melden. Mit der Erweiterung **Service Declaration** können Sie Informationen über den Handel mit Dienstleistungen in der EU sammeln und an die Behörden melden. Obwohl sie **Service-Deklaration** heißt, können Sie sie auch als **Intrastat für Dienstleistungen** verwenden. Diese Erweiterung ist für alle EU-Länder als W1-Version verfügbar und kann in Belgien unverändert verwendet werden. Für andere Länder wird eine länderspezifische Erweiterung benötigt. Wenn ein Land nur ein anderes Format benötigt, können Sie die Berichtskonfiguration im **Data Exchange Framework** verwenden, um das Format zu ändern.

## Aktivieren Sie die Service-Erweiterung

Nachdem Sie die Erweiterung in Ihrer Umgebung installiert haben, müssen Sie sie aktivieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Funktionsverwaltung** ein und wählen Sie dann den entsprechenden Link.
2. Suchen Sie **Funktion: Verwendung der Service Deklaration (Intrastat für Services)**, und wählen Sie im Feld **Aktiviert für** **Alle Benutzer**. Mehr über die Funktionsverwaltung erfahren Sie unter [Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management) im Inhalt der Administration.
3. Wenn Sie die Funktion aktivieren, sollten Sie die einzelnen Schritte der Einrichtung durch den Einrichtungsassistenten befolgen. Die meisten Felder sind standardmäßig konfiguriert.
4. Fügen Sie im zweiten Schritt nur **Service Transaktionsarten** hinzu, indem Sie die Option **Öffnen Sie die Seite Service Transaktionsarten, um die Liste der Codes anzugeben** wählen.
5. Bevor Sie beginnen, überprüfen Sie die **Gesamtzahl der Codes**, um festzustellen, wie viele Service-Transaktionsarten bereits angegeben wurden.
6. Wählen Sie **Abschließen** im letzten Schritt, um die Konfiguration abzuschließen.

## Die Erweiterung Service-Deklaration festlegen

Sie können die Erweiterung manuell festlegen oder eine Berichtsdatei in Data Exchange Definitions verwenden.

### Um die Service-Deklaration manuell festzulegen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Wählen Sie im Symbol **Service Einrichtung** und dann den entsprechenden Link aus.
2. Konfigurieren Sie auf der Registerkarte **Allgemein** die in der folgenden Tabelle beschriebenen Felder:

    |Feld  |Description  |
    |---------|---------|
    |**Deklarationsnummernserie**     | Gibt die Nummernserie an, die für die Zuordnung von IDs zu neuen Datensätzen verwendet werden soll.        |
    |**Artikel Zu-/Abschläge melden**  | Legt fest, ob Artikelzu-/abschläge gemeldet werden müssen. Wenn diese Option aktiviert ist, prüft [!INCLUDE [prod_short](includes/prod_short.md)] den Code der Transaktion für Artikelzu-/abschläge und schließt sie in die Service-Deklarationen ein.        |
    |**Verkaufen an/Abrechnen an Kundennr.**     | Gibt den Kunden an, dessen Ländercode mit dem Ländercode auf der Seite **Unternehmensdaten** verglichen werden soll. Nur Dokumente, bei denen diese beiden Codes unterschiedlich sind, werden in die Service-Deklaration aufgenommen.<br><br>* **Rechnung-an.**: Verwenden Sie den Ländercode aus der **Rechnung-an-Kunde** <br<br>* **Verkaufen an.**: Verwenden Sie den Ländercode aus dem Feld **Verkauf an Kunde**.        |
    |**Kaufen von/Zahlen an Lieferant Nr.**  | Gibt an, welcher Lieferant verwendet werden soll, um seinen Ländercode mit dem Ländercode auf der Seite **Unternehmensdaten** zu vergleichen. Nur Dokumente, bei denen diese beiden Codes unterschiedlich sind, werden in die Service-Deklaration aufgenommen.<br><br> * **Kaufen von.**: Verwenden Sie den Ländercode des **Kaufen von Anbieters**. <br><br> * **Zahlen an.**: Verwenden Sie den Ländercode des **Zahlen an Anbieters**.         |
    |**Daten Aust. Def. Code**  | Gibt den Datenaustausch-Definitionscode an, der zum Generieren der exportierten Datei für die Servicemeldung verwendet wird        |
    |**Steuerregistrierungsnummer aktivieren.**     |  Gibt an, ob die **Steuerregistrierungsnummer** für die Service-Deklaration aktiviert ist.       |

3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Geben Sie im Symbol **Service Transaktionsarten** ein und wählen Sie dann den entsprechenden Link.
4. Geben Sie in den Zeilen **Codes** und **Beschreibungen** für die von Ihnen verwendeten Arten von Transaktionen für Dienstleistungen ein.

### Legen Sie eine Berichtsdatei fest

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Geben Sie im Symbol **Data Exchange Definitions** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Beschreiben Sie auf dem Inforegister **Allgemein** die Datenaustauschdefinition, indem Sie den Dateityp, das Spaltentrennzeichen, die zugehörigen Codeunits, XMLport, angeben und die anderen Felder ausfüllen.
4. Auf der Registerkarte **Zeilendefinitionen** beschreiben Sie die Formatierung der Zeilen in der Datendatei, indem Sie die Felder basierend auf dem Feld **Zeilentyp** ausfüllen und die Anzahl der Spalten für diese Zeile festlegen.
5. Auf der Inforegisterkarte **Spaltendefinitionen** füllen Sie die Zeile für jede geplante Spalte aus.
6. Wählen Sie die Aktion **Feldzuordnung** auf dem Inforegister **Zeilendefinitionen**, um die Seite **Feldzuordnung** zu öffnen.
7. Erstellen Sie einen neuen Eintrag, und wählen Sie auf der Registerkarte **Allgemein** Inforegister die **Tabellen-ID** (für **Service-Deklarationszeile** wählen Sie **5024**), und füllen Sie die Felder wie folgt aus:
   1. Geben Sie im Feld **Schlüsselindex** den Schlüsselindex an, nach dem die Quelldatensätze vor dem Export sortiert werden sollen.
   2. Wählen Sie die **Zuordnung Codeunit**.
8. Fügen Sie auf der Inforegisterkarte **Feldzuordnung** die Spalten hinzu, die Sie zuvor auf der Inforegisterkarte **Spaltendefinitionen** konfiguriert haben, und fügen Sie dann Folgendes hinzu:
   1. Geben Sie für jede der Spalten die **Feld-ID** an.
   2. Geben Sie die **Transformationsregel** für jede Spalte nach Bedarf an. Die Regel wandelt importierten Text in einen unterstützten Wert um, bevor er einem bestimmten Feld in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet werden kann. Wenn Sie einen Wert in diesem Feld auswählen, wird der genaue Wert in das Feld **Transformationsregel** in der **Daten Aust. Feld Zuordnung Puf.** Tabelle zugewiesen wird und umgekehrt.
9. Um Einträge auf der Basis von Spalten zu gruppieren, wählen Sie auf der Inforegister-Registerkarte **Feldgruppierung** die Felder aus, die Sie für die Gruppierung verwenden möchten.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] wird mit einer vorkonfigurierten Datenaustauschdefinition für **Service-Deklaration** für alle lokalisierten Länder geliefert. Erfahren Sie mehr über das Erstellen einer neuen Datenaustauschdefinition unter [Datenaustauschdefinitionen einrichten](across-how-to-set-up-data-exchange-definitions.md).

## Andere verwandte Konfigurationen

Bevor Sie die Erweiterung Service-Deklaration verwenden, konfigurieren Sie einige Felder für Artikel, Ressourcen und Artikelzu-/abschläge.

### Artikel

Legen Sie die Informationen zur Service-Deklaration auf den Seiten der Artikelkarte fest:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Posten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie das Element, das Sie konfigurieren möchten.
3. Erweitern Sie das Inforegister **Artikel**, und konfigurieren Sie die folgenden Felder:
   1. Wählen Sie im Feld **Typ** die Option **Service**.
   2. Geben Sie im Feld **Code der Service-Transaktionsart** den Code für eine **Service-Transaktionsart** an.
   3. Wenn Sie dieses Element nicht in Service-Deklarationen aufnehmen möchten, wählen Sie das Feld **Aus Service-Deklaration ausschließen**.

### Ressourcen

Legen Sie auf den Ressourcenkartenseiten Informationen zur Service-Deklaration fest:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Ressourcen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Ressource, die Sie konfigurieren möchten.
3. Erweitern Sie das Inforegister **Allgemein**, und konfigurieren Sie die folgenden Felder:
   1. Geben Sie im Feld **Code der Service-Transaktionsart** den Code für eine **Service-Transaktionsart** an.
   2. Wenn Sie diese Ressource nicht in Service-Deklarationen einbeziehen möchten, wählen Sie das Feld **Aus Service-Deklaration ausschließen**.

### Artikelzu-/abschläge

Legen Sie Informationen zur Service-Deklaration für Artikel Zu-/Abschläge fest:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Artikelzu-/abschläge** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Artikel Zu-/Abschlag aus, den Sie konfigurieren möchten.
3. Geben Sie im Feld **Code der Service-Transaktionsart** den Code für eine **Service-Transaktionsart** an.
4. Wenn Sie diesen Artikel Zu-/Abschlag nicht in Service-Deklarationen aufnehmen möchten, markieren Sie das Feld **Aus Service-Deklaration ausschließen**.

## Neue Servicemeldung erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Service-Deklarationen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie auf der Registerkarte **Allgemein** Inforegister die folgenden Felder aus:
    1. In dem Feld **Konfig. Code** geben Sie den Konfigurationscode an, der verwendet wird, um Zeilen vorzuschlagen und Dateien zu erstellen. Sie müssen einen als **Service Deklaration** auswählen.
    2. Geben Sie in den Feldern **Startdatum** und **Enddatum** das Start- und Enddatum des Zeitraums an, der in die Service-Deklaration aufgenommen werden soll.
4. Wählen Sie die Aktion **Zeilen vorschlagen**, um einen Batchauftrag zu starten, der Zeilen aus Belegen sammelt und die Zeilen der Service-Deklaration ausfüllt.

Der Batchauftrag ruft alle Einträge aus den entsprechenden Kauf- und Verkaufsbelegen im gewünschten Zeitraum ab und fügt sie in die Zeilen der Service-Deklaration ein. Bewegen Sie den Mauszeiger über die Felder in den Zeilen, um eine kurze Beschreibung zu lesen.

## Ändern einer Servicemeldung

Bei Bedarf können Sie die Zeilen ändern oder neue Zeilen hinzufügen.

1. Wählen Sie auf der Seite **Service-Deklaration** die Aktion **Neue Zeile** im Inforegister **Zeilen**.
2. Wählen Sie im Feld **Dokumenttyp** die Option, die sich auf das Dokument bezieht, das Sie verwenden möchten.
3. Füllen Sie auf der Grundlage des **Dokumententyps** das Feld **Dokument-Nr.** aus.
4. Füllen Sie die restlichen Felder aus.

## Übersicht über die Service-Deklarationszeilen

Nachdem Sie eine Service-Deklaration erstellt haben, verwenden Sie die Aktion **Übersicht**, um sich einen Überblick über die Zeilen der Service-Deklaration zu verschaffen. Sie können die Zeilen auf die gleiche Weise gruppieren und zusammenfassen wie die exportierte Datei. Sie können die Zeilen auch in Excel öffnen.

## Servicemeldung in einer Datei melden

Sie können die Servicemeldung als Datei senden, je nach den Anforderungen der verschiedenen lokalen Behörden. So erstellen Sie eine Datei:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Service-Deklarationen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Service-Deklaration, die Sie als Datei melden möchten.
3. Wenn Sie dies noch nicht getan haben, füllen Sie die Service-Deklaration manuell aus oder wählen Sie die Aktion **Zeilen vorschlagen**.
4. Wählen Sie die Aktion **Aus Datei erstellen** aus.
5. Die Servicemeldung wird in dem gewünschten Format gespeichert.

## Andere Überlegungen

Wenn Sie die Erweiterung **Service-Deklaration** verwenden, gibt es noch ein paar weitere Dinge zu beachten. Zum Beispiel ist es wichtig, dass Ihre Gruppen den Anforderungen der Behörden entsprechen. Es ist auch wichtig, dass die Dienstleistungen in den Verkaufs- und Kaufbelegen korrekt angegeben werden.

### Zeilen gruppieren

In den Zeilen der Service-Deklaration gibt es keine Gruppierung nach einem Feld. Alle Einträge werden aus dem Originaldokument als Quelle kopiert.

Die von den Behörden benötigte Gruppierung wird in der exportierten Datei bereitgestellt. Sie müssen die Gruppen in der **Data Exchange Definition** konfigurieren, die vollständig konfigurierbar ist. Weitere Informationen finden Sie unter [Definitionen für den Datenaustausch festlegen](across-how-to-set-up-data-exchange-definitions.md).

### Dienste in Belegzeilen verwenden

Wenn Sie eine Einkaufs-, Verkaufs- oder Dienstleistungsrechnung erstellen, finden Sie in deren Zeilen zwei Felder, die sich auf Servicerechnungen beziehen. Beide Felder sind mit den Standardwerten aus Ihren Artikel-, Ressourcen- oder Artikelzu-/Abschlag-Einstellungen ausgefüllt.

- **Code für Service-Transaktionsart** - Gibt den Code für eine Service-Transaktionsart an.
- **Anwendbar für Service-Deklaration** - Gibt an, ob ein Element oder eine Ressource für eine Service-Deklaration anwendbar ist.

Sie können die Werte in diesen Feldern ändern, aber wenn Sie das Feld **Anwendbar für Service-Deklaration** auswählen, müssen Sie einen Wert im Feld **Code für Service-Transaktionsart** angeben. Wenn Sie das nicht tun, können Sie den Beleg nicht buchen.

Wenn Sie im Feld **Dienstleistung Transaktionsart Code** einen Wert angeben, aber das Feld **Anwendbar für Dienstleistungsdeklaration** nicht markieren, können Sie den Beleg zwar buchen, aber die Zeile wird dabei nicht berechnet.

## Siehe die entsprechende Schulung unter [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Siehe auch

[Intrastat Reporting festlegen](finance-how-setup-report-intrastat.md)
[Intrastat Reporting in Business Central](finance-how-report-intrastat.md)  
[Finanzmanagement](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
